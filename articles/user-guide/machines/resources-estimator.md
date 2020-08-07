---
title: Quantum-Ressourcenschätzung-Quantum Development Kit
description: Erfahren Sie mehr über die Ressourcenschätzung von Microsoft QDK, die die Ressourcen schätzt, die zum Ausführen einer bestimmten Instanz eines Q# Vorgangs auf einem Quantum-Computer erforderlich sind.
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: d5338eb740716d9d7f408703347f572688bbccb2
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868184"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>Ressourcenschätzung für das Quantum Development Kit (QDK)

Wie der Name schon sagt, `ResourcesEstimator` schätzt die-Klasse die Ressourcen, die erforderlich sind, um eine bestimmte Instanz eines- Q# Vorgangs auf einem Quantum-Computer auszuführen. Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund werden Ressourcen für Vorgänge geschätzt, bei Q# denen Tausende von Qubits verwendet werden, vorausgesetzt, dass der klassische Teil des Codes in angemessener Zeit ausgeführt wird.

Die Ressourcenschätzung basiert auf dem Quantum-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), der einen umfassenderen Satz an Metriken und Tools bereitstellt, um das Debuggen von Programmen zu erleichtern Q# .

## <a name="invoking-and-running-the-resources-estimator"></a>Aufrufen und Ausführen der Ressourcenschätzung

Sie können den Ressourcen Schätz verwenden, um jeden Q# Vorgang auszuführen. Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q# Programms](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-resources-estimator-from-c"></a>Aufrufen der Ressourcenschätzung von C # 

Wie bei anderen Zielcomputern auch, erstellen Sie zuerst eine Instanz der Klasse `ResourceEstimator` und übergeben sie anschließend als ersten Parameter der `Run`-Methode einer Operation.

Beachten Sie hierbei Folgendes: Im Gegensatz zur Klasse `QuantumSimulator` wird mit der Klasse `ResourceEstimator` nicht die <xref:System.IDisposable>-Schnittstelle implementiert, sodass Sie sie nicht in eine `using`-Anweisung einschließen müssen.

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

Wie das Beispiel zeigt, `ResourcesEstimator` stellt die- `ToTSV()` Methode bereit, die eine Tabelle mit durch Tabstopps getrennten Werten (TSV) generiert. Sie können die Tabelle in einer Datei speichern oder Sie zur Analyse in der Konsole anzeigen. Im folgenden finden Sie eine Beispielausgabe des vorangehenden Programms:

```output
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
> Eine- `ResourcesEstimator` Instanz setzt ihre Berechnungen bei jedem Testlauf nicht zurück. Wenn Sie dieselbe-Instanz verwenden, um einen anderen Vorgang auszuführen, werden die neuen Ergebnisse mit den vorhandenen Ergebnissen aggregiert. Wenn Sie Berechnungen zwischen den Ausführungen zurücksetzen müssen, erstellen Sie für jede Ausführung eine neue Instanz.

### <a name="invoking-the-resources-estimator-from-python"></a>Aufrufen der Ressourcenschätzung von python

Verwenden Sie die [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) -Methode aus der Python-Bibliothek mit dem importierten Q# Vorgang:

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a>Aufrufen der Ressourcenschätzung von der Befehlszeile aus

Wenn Sie ein Q# Programm über die Befehlszeile ausführen, verwenden Sie den Parameter **--Simulator** (oder **-s** ), um den `ResourcesEstimator` Zielcomputer anzugeben. Der folgende Befehl führt ein Programm mit der Ressourcenschätzung aus: 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a>Aufrufen der Ressourcenschätzung von juptyer Notebooks

Verwenden Sie den I Q# Magic-Befehl " [% schätzkraft](xref:microsoft.quantum.iqsharp.magic-ref.simulate) ", um den Q# Vorgang auszuführen.

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a>Programm gesteuertes Abrufen der geschätzten Daten

Zusätzlich zu einer TSV-Tabelle können Sie die während der Durchführung geschätzten Ressourcen Programm gesteuert über die- `Data` Eigenschaft der Ressourcenschätzung abrufen. Die `Data` -Eigenschaft stellt eine `System.DataTable` -Instanz mit zwei Spalten bereit: `Metric` und `Sum` , indiziert nach den Namen der Metriken.

Der folgende Code zeigt, wie die Gesamtanzahl von `QubitClifford` `T` -und- `CNOT` Vorgängen, die von einem-Vorgang verwendet werden, abgerufen und gedruckt werden Q# :

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

Die Ressourcenschätzung verfolgt die folgenden Metriken:

|Metrik|BESCHREIBUNG|
|----|----|
|__CNOT__    |Die Ausführung von `CNOT` Vorgängen (auch als kontrollierte Pauli X-Vorgänge bezeichnet).|
|__Qubitclifford__ |Die Testlauf-Anzahl einzelner Qubit Clifford-und Pauli-Vorgänge.|
|__Measure__    |Die Testlauf-Anzahl von Messungen.  |
|__R__    |Die Anzahl der Testlauf mit einzelnen Qubit-Drehungen, ausgenommen `T` , Clifford-und Pauli-Vorgänge.  |
|__T__    |Die Anzahl der `T` Vorgänge und ihre konjutoren, einschließlich der `T` Vorgänge, T_x = h. T. h und T_y = HY. T. HY.  |
|__Tiefe__|Die untere Grenze für die Tiefe der vom Vorgang durchgeführten Quantum-Leitung Q# . Standardmäßig zählt die Tiefe Metrik nur `T` Gates. Weitere Informationen finden Sie unter [tiefen Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).   |
|__Width__    |Die untere Grenze für die maximale Anzahl von Qubits, die während der Ausführung des Q# Vorgangs zugeordnet wurden. Möglicherweise ist es nicht möglich, sowohl __Tiefe__ als auch __Breite__ Untergrenzen gleichzeitig zu erreichen.  |
|__Borrowedwidth__    |Die maximale Anzahl der im Vorgang geliehenen Qubits Q# .  |

## <a name="providing-the-probability-of-measurement-outcomes"></a>Angeben der Wahrscheinlichkeit von Messergebnissen

Sie können <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> aus dem- <xref:microsoft.quantum.diagnostics> Namespace verwenden, um Informationen über die erwartete Wahrscheinlichkeit eines Messvorgangs bereitzustellen. Weitere Informationen finden Sie unter [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)

## <a name="see-also"></a>Weitere Informationen

- [Quantum-Ablauf Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Toffoli-Simulator für Quantencomputer](xref:microsoft.quantum.machines.toffoli-simulator)
- [Simulator für den vollständigen Zustand für Quantencomputer](xref:microsoft.quantum.machines.full-state-simulator) 