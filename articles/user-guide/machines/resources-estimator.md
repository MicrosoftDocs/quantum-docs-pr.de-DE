---
title: Ressourcenschätzung für Quantum Development Kit
description: 'Erfahren Sie mehr über die Ressourcenschätzung, mit der die Ressourcen geschätzt werden, die zum Ausführen einer bestimmten Instanz eines Q #-Vorgangs auf einem Quantum-Computer erforderlich sind.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: cbb1c274b64738cc4b47869563d7d02eb717afbc
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415255"
---
# <a name="the-resources-estimator-target-machine"></a>Der Zielcomputer für die Ressourcenschätzung

Wie der Name schon sagt, schätzt die Ressourcen, die erforderlich sind, `ResourcesEstimator` um eine bestimmte Instanz eines Q #-Vorgangs auf einem Quantum-Computer auszuführen.
Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund können Ressourcen für Q #-Vorgänge geschätzt werden, die Tausende von Qubits verwenden, wenn der klassische Teil des Codes in angemessener Zeit ausgeführt werden kann.

## <a name="usage"></a>Zweck

`ResourcesEstimator`Ist nur ein anderer Typ von Zielcomputer und kann daher zum Ausführen beliebiger Q #-Vorgänge verwendet werden. 

Erstellen Sie wie andere Zielcomputer eine-Instanz, um Sie für ein c#-Host Programm zu verwenden, und übergeben Sie Sie als ersten Parameter der-Methode des Vorgangs `Run` :

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

Wie das Beispiel zeigt, `ResourcesEstimator` stellt eine `ToTSV()` Methode zum Generieren einer Tabelle mit durch Tabstopps getrennten Werten (TSV) bereit, die in einer Datei gespeichert oder zur Analyse in die Konsole geschrieben werden kann. Die Ausgabe des obigen Programms sollte in etwa wie folgt aussehen:

```Output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> Die `ResourcesEstimator` Berechnungen werden bei jeder Ausführung von nicht zurückgesetzt, wenn die gleiche Instanz verwendet wird, um einen anderen Vorgang auszuführen, wird die aggregierte Anzahl der vorhandenen Ergebnisse beibehalten.
> Wenn Sie Berechnungen zwischen den Ausführungen zurücksetzen müssen, erstellen Sie für jede Ausführung eine neue Instanz.


## <a name="programmatically-retrieving-the-estimated-data"></a>Programm gesteuertes Abrufen der geschätzten Daten

Zusätzlich zu einer TSV-Tabelle können die geschätzten Ressourcen Programm gesteuert über die `ResourcesEstimator` -Eigenschaft abgerufen werden `Data` . `Data`stellt eine `System.DataTable` -Instanz mit zwei Spalten bereit: `Metric` und `Sum` , indiziert durch die metriknamen.

Der folgende Code zeigt, wie Sie die Gesamtzahl der von `QubitClifford` `T` `CNOT` einem f #-Vorgang verwendeten Gates abrufen und ausdrucken:

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a>Gemeldete Metriken

Im folgenden finden Sie eine Liste der Metriken, die von geschätzt werden `ResourcesEstimator` :

* __CNOT__: die Anzahl der ausgeführten Gates (auch als kontrollierte Pauli X Gate bezeichnet).
* __Qubitclifford__: die Anzahl der einzelnen Qubit Clifford-und Pauli-Gates, die ausgeführt wurden.
* __Measure__: die Anzahl der ausgeführten Messungen.
* __R__: die Anzahl der ausgeführten einzelnen Qubit-Drehungen, ausgenommen T, Clifford und Pauli Gates.
* __T__: die Anzahl der t-Gates und ihre konjugierte, einschließlich t Gate, T_x = h. T. h und T_y = HY. T. HY, ausgeführt.
* __Tiefe__: die untere Grenze für die Tiefe der vom Q #-Vorgang ausgeführten Quantum-Leitung. Standardmäßig werden nur T Gates in der Tiefe gezählt. Weitere Informationen finden Sie unter [tiefen Zähler](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) .
* __Width__: die untere Grenze für die maximale Anzahl von Qubits, die während der Ausführung des Q #-Vorgangs zugeordnet werden. Möglicherweise ist es nicht möglich, sowohl __Tiefe__ als auch __Breite__ Untergrenzen gleichzeitig zu erreichen.
* __Borrowedwidth__: maximale Anzahl von im Q #-Vorgang geliehenen Qubits.


## <a name="providing-the-probability-of-measurement-outcomes"></a>Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen

<xref:microsoft.quantum.intrinsic.assertprob>aus dem- <xref:microsoft.quantum.intrinsic> Namespace kann verwendet werden, um Informationen über die erwartete Wahrscheinlichkeit einer Messung bereitzustellen, um die Ausführung des Q #-Programms zu fördern. Das folgende Beispiel veranschaulicht dies:

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

Wenn die `ResourcesEstimator` gefunden `AssertProb` wird, wird diese Messung auf dem Wert aufgezeichnet, `PauliZ` `source` und es `q` sollte ein Ergebnis von `Zero` mit der Wahrscheinlichkeit 0,5 angegeben werden. Wenn Sie zu einem späteren Zeitpunkt ausgeführt wird `M` , werden die aufgezeichneten Werte der Ergebnis Wahrscheinlichkeiten gefunden, und es `M` wird `Zero` oder `One` mit der Wahrscheinlichkeit 0,5 zurückgegeben.


## <a name="see-also"></a>Siehe auch

Der baut `ResourcesEstimator` auf dem Quantum-Computer-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)auf, der einen umfassenderen Satz an Metriken, die Möglichkeit zum Melden von Metriken für das vollständige Aufruf Diagramm und Features wie die unter [schiedliche Eingabe](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) Prüfung bereitstellt, um Fehler in Q #-Programmen zu finden. Weitere Informationen finden Sie in der Dokumentation des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .

