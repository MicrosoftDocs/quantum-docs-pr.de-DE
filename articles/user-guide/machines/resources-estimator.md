---
title: Quantum-Ressourcenschätzung-Quantum Development Kit
description: Erfahren Sie mehr über die Ressourcenschätzung von Microsoft QDK, die die Ressourcen schätzt, die zum Ausführen einer bestimmten Instanz eines Q# Vorgangs auf einem Quantum-Computer erforderlich sind.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: de425c2d91c6528b13c3bedd81acb4b4273ed711
ms.sourcegitcommit: 7c687495a79d75ae9e029e5a41baec84d9e07bb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2020
ms.locfileid: "96604642"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>Ressourcenschätzung für das Quantum Development Kit (QDK)

Wie der Name schon sagt, `ResourcesEstimator` schätzt die-Klasse die Ressourcen, die erforderlich sind, um eine bestimmte Instanz eines- Q# Vorgangs auf einem Quantum-Computer auszuführen. Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund werden Ressourcen für Vorgänge geschätzt, bei Q# denen Tausende von Qubits verwendet werden, vorausgesetzt, dass der klassische Teil des Codes in angemessener Zeit ausgeführt wird.

Die Ressourcenschätzung basiert auf dem Quantum-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), der einen umfassenderen Satz an Metriken und Tools bereitstellt, um das Debuggen von Programmen zu erleichtern Q# .

## <a name="invoking-and-running-the-resources-estimator"></a>Aufrufen und Ausführen der Ressourcenschätzung

Sie können den Ressourcen Schätz verwenden, um jeden Q# Vorgang auszuführen. Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q# Programms](xref:microsoft.quantum.guide.host-programs).

### <a name="invoking-the-resources-estimator-from-c"></a>Aufrufen der Ressourcenschätzung von C # 

Wie bei anderen Zielcomputern auch, erstellen Sie zuerst eine Instanz der Klasse `ResourcesEstimator` und übergeben sie anschließend als ersten Parameter der `Run`-Methode einer Operation.

Beachten Sie hierbei Folgendes: Im Gegensatz zur Klasse `QuantumSimulator` wird mit der Klasse `ResourcesEstimator` nicht die <xref:System.IDisposable>-Schnittstelle implementiert, sodass Sie sie nicht in eine `using`-Anweisung einschließen müssen.

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

Verwenden Sie die [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) -Methode aus der Python-Bibliothek mit dem importierten Q# Vorgang:

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
|__Tiefe__|Die Tiefe der vom Vorgang durchgeführten Quantum-Verbindung Q# (siehe [unten](#depth-width-and-qubitcount)). Standardmäßig zählt die Tiefe Metrik nur `T` Gates. Weitere Informationen finden Sie unter [tiefen Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).   |
|__Width__|Breite der vom Vorgang durchgeführten quantumleitung Q# (siehe [unten](#depth-width-and-qubitcount)). Standardmäßig zählt die Tiefe Metrik nur `T` Gates. Weitere Informationen finden Sie unter [Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).   |
|__Qubitcount__    |Die untere Grenze für die maximale Anzahl von Qubits, die während der Ausführung des Q# Vorgangs zugeordnet wurden. Diese Metrik ist möglicherweise nicht mit der __Tiefe__ kompatibel (siehe unten).  |
|__Borrowedwidth__    |Die maximale Anzahl der im Vorgang geliehenen Qubits Q# .  |


## <a name="depth-width-and-qubitcount"></a>Tiefe, Breite und qubitcount

Die gemeldeten tiefen und breiten Schätzungen sind miteinander kompatibel.
(Bisher waren beide Zahlen erreichbar, aber für Tiefe und Breite sind unterschiedliche Verbindungen erforderlich.) Derzeit können beide Metriken in diesem Paar gleichzeitig von derselben Verbindung erreicht werden.

Folgende Metriken werden gemeldet:

__Tiefe:__ Für den Stamm Vorgang, der für die Ausführung benötigt wird, wobei bestimmte Gate-Zeiten angenommen werden.
Für Vorgänge namens oder nachfolgende Vorgänge: Zeitunterschied zwischen der aktuellen Qubit-Verfügbarkeits Zeit am Anfang und am Ende des Vorgangs.

__Breite:__ Für den Stamm Vorgang: die Anzahl von Qubits, die tatsächlich verwendet wurden, um Sie auszuführen (und der Vorgang, den Sie aufruft).
Für Vorgänge mit dem Namen oder nachfolgende Vorgänge: wie viele weitere Qubits wurden zusätzlich zu den Qubits verwendet, die bereits am Anfang des Vorgangs verwendet wurden.

Beachten Sie, dass wiederverwendete Qubits nicht zu dieser Zahl beitragen.
Wenn beispielsweise einige Qubits freigegeben wurden, bevor der Vorgang a startet, und alle von diesem Vorgang angeforderten Qubit (und Vorgänge, die von einem aufgerufen wurden) durch wieder verwenden von zuvor releasequbits erfüllt wurden, wird die Breite des Vorgangs a als 0 (null) gemeldet. Erfolgreich geliehene Qubits tragen nicht an die Breite an.

__Qubitcount:__ Für den Stamm Vorgang: minimale Anzahl von Qubits, die ausreichen, um diesen Vorgang auszuführen (und von ihm aufgerufene Vorgänge).
Für Vorgänge mit dem Namen oder nachfolgende Vorgänge: minimale Anzahl von Qubits, die ausreichen, um diesen Vorgang separat auszuführen. Diese Zahl enthält keine Eingabe-Qubits. Sie enthält auch geliehene Qubits.

Zwei Betriebsmodi werden unterstützt. Der Modus wird ausgewählt, indem qctracesimulatorconfiguration. optimizetiefe festgelegt wird.

__Optimizetiefe = true:__ Bei qubitmanager wird von der Qubit-Wiederverwendung abgeraten, und jedes Mal, wenn ein Qubit angefordert wird, wird ein neues Qubit zugewiesen. Die __Tiefe__ des Stamm Vorgangs wird zur minimalen Tiefe (untere Grenze). Für diese Tiefe wird eine kompatible __Breite__ gemeldet (beide können gleichzeitig erreicht werden). Beachten Sie, dass diese Breite bei dieser Tiefe wahrscheinlich nicht optimal ist. " __Qubitcount__ " ist möglicherweise niedriger als die Breite für den Stamm Vorgang, da die Wiederverwendung vorausgesetzt wird

__Optimizetiefe = false:__ Qubitmanager wird empfohlen, Qubits wiederzuverwenden und veröffentlichte Qubits wiederzuverwenden, bevor neue zugeordnet werden. Die __Breite__ des Stamm Vorgangs wird zur minimalen Breite (untere Grenze). Es wird eine kompatible __Tiefe__ gemeldet, für die Sie erreicht werden kann. __Qubitcount__ ist die gleiche wie die __Breite__ für den Stamm Vorgang, vorausgesetzt, dass keine Kreditaufnahme erfolgt.

## <a name="providing-the-probability-of-measurement-outcomes"></a>Angeben der Wahrscheinlichkeit von Messergebnissen

Sie können <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> aus dem- <xref:Microsoft.Quantum.Diagnostics> Namespace verwenden, um Informationen über die erwartete Wahrscheinlichkeit eines Messvorgangs bereitzustellen. Weitere Informationen finden Sie unter [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)

## <a name="see-also"></a>Weitere Informationen

- [Quantum-Ablauf Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Toffoli-Simulator für Quantencomputer](xref:microsoft.quantum.machines.toffoli-simulator)
- [Simulator für den vollständigen Zustand für Quantencomputer](xref:microsoft.quantum.machines.full-state-simulator) 
