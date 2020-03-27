---
title: Ressourcenschätzung für Quantum Development Kit
description: 'Erfahren Sie mehr über die Ressourcenschätzung, mit der die Ressourcen geschätzt werden, die zum Ausführen einer bestimmten Instanz eines Q #-Vorgangs auf einem Quantum-Computer erforderlich sind.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 51186134e9279727fec212cdce84f69493aaa656
ms.sourcegitcommit: a0e50c5f07841b99204c068cf5b5ec8ed087ffea
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2020
ms.locfileid: "80320823"
---
# <a name="the-resourcesestimator-target-machine"></a>Der resourcesestimator-Zielcomputer

Wie der Name schon sagt, schätzt der `ResourcesEstimator` die Ressourcen, die erforderlich sind, um eine bestimmte Instanz eines Q #-Vorgangs auf einem Quantum-Computer auszuführen.
Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund können Ressourcen für Q #-Vorgänge geschätzt werden, die Tausende von Qubits verwenden, wenn der klassische Teil des Codes in angemessener Zeit ausgeführt werden kann.

## <a name="usage"></a>Verwendung

Der `ResourcesEstimator` ist nur ein anderer Typ von Zielcomputer und kann daher verwendet werden, um einen beliebigen Q #-Vorgang auszuführen. 

Erstellen Sie wie andere Zielcomputer eine-Instanz, C# um Sie auf einem Host Programm zu verwenden, und übergeben Sie Sie als ersten Parameter der `Run`-Methode des Vorgangs:

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

Wie das Beispiel zeigt, stellt die `ResourcesEstimator` eine `ToTSV()` Methode zum Generieren einer Tabelle mit "Tabulator getrennten Werten" (TSV) bereit, die in einer Datei gespeichert oder zur Analyse in die Konsole geschrieben werden kann. Die Ausgabe des obigen Programms sollte in etwa wie folgt aussehen:

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
> Der `ResourcesEstimator` setzt seine Berechnungen bei jeder Ausführung nicht zurück. wenn dieselbe Instanz verwendet wird, um einen anderen Vorgang auszuführen, wird die Aggregation der Anzahl vorhandener Ergebnisse beibehalten.
> Wenn Sie Berechnungen zwischen den Ausführungen zurücksetzen müssen, erstellen Sie für jede Ausführung eine neue Instanz.


## <a name="programmatically-retrieving-the-estimated-data"></a>Programm gesteuertes Abrufen der geschätzten Daten

Zusätzlich zu einer TSV-Tabelle können die geschätzten Ressourcen Programm gesteuert über die `Data`-Eigenschaft des `ResourcesEstimator`abgerufen werden. `Data` stellt eine `System.DataTable` Instanz mit zwei Spalten bereit: `Metric` und `Sum`, indiziert durch die metriknamen.

Der folgende Code zeigt, wie Sie die Gesamtzahl der `QubitClifford`, `T` und `CNOT` Gates abrufen und ausdrucken, die von einem Q #-Vorgang verwendet werden:

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

Im folgenden finden Sie eine Liste der Metriken, die vom `ResourcesEstimator`geschätzt werden:

* __CNOT__: die Anzahl der ausgeführten Gates (auch als kontrollierte Pauli X Gate bezeichnet).
* __Qubitclifford__: die Anzahl der einzelnen Qubit Clifford-und Pauli-Gates, die ausgeführt wurden.
* __Measure__: die Anzahl der ausgeführten Messungen.
* __R__: die Anzahl der ausgeführten einzelnen Qubit-Drehungen, ausgenommen T, Clifford und Pauli Gates.
* __T__: die Anzahl der t-Gates und ihre konjugierte, einschließlich t Gate, T_x = h. T. h und T_y = HY. T. HY, ausgeführt.
* __Tiefe__: Tiefe der vom Q #-Vorgang ausgeführten Quantum-Leitung. Standardmäßig werden nur T Gates in der Tiefe gezählt. Weitere Informationen finden Sie unter [tiefen Zähler](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) .
* __Width__: maximale Anzahl von Qubits, die während der Ausführung des Q #-Vorgangs zugeordnet wurden.
* __Borrowedwidth__: maximale Anzahl von im Q #-Vorgang geliehenen Qubits.


## <a name="providing-the-probability-of-measurement-outcomes"></a>Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen

<xref:microsoft.quantum.intrinsic.assertprob> aus dem <xref:microsoft.quantum.intrinsic>-Namespace kann verwendet werden, um Informationen über die erwartete Wahrscheinlichkeit einer Messung bereitzustellen, um die Ausführung des Q #-Programms zu fördern. Das folgende Beispiel veranschaulicht dies:

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

Wenn die `ResourcesEstimator` `AssertProb`, wird festgestellt, dass das Messen `PauliZ` auf `source` und `q` das Ergebnis `Zero` mit der Wahrscheinlichkeit 0,5 erhalten soll. Wenn Sie später `M` ausgeführt wird, werden die aufgezeichneten Werte der Ergebnis Wahrscheinlichkeiten gefunden, und `M` gibt `Zero` oder `One` mit der Wahrscheinlichkeit 0,5 zurück.


## <a name="see-also"></a>Siehe auch

Der `ResourcesEstimator` basiert auf dem Quantum-Computer-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), der einen umfassenderen Satz an Metriken, die Möglichkeit zum Melden von Metriken für das vollständige Aufruf Diagramm und Features wie die unter [schiedliche Eingabe](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) Prüfung bereitstellt, um Fehler in Q #-Programmen zu finden. Weitere Informationen finden Sie in der Dokumentation des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .

