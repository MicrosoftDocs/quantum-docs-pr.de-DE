---
title: 'Ablaufverfolgungssimulator für Quantencomputer: Quantum Development Kit'
description: Hier erfahren Sie, wie Sie den Microsoft-Ablaufverfolgungssimulator für Quantencomputer verwenden, um klassischen Code zu debuggen und die Ressourcenanforderungen eines Q#-Programms zu schätzen.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1e9207d7dcd6ec09353b234654e0567b377144e9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858637"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a>Microsoft Quantum Development Kit (QDK): Ablaufverfolgungssimulator für Quantencomputer

Mit der QDK-Klasse <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> wird ein Quantenprogramm ausgeführt, ohne den Zustand eines Quantencomputers tatsächlich zu simulieren. Aus diesem Grund können mit dem Ablaufverfolgungssimulator für Quantencomputer Quantenprogramme ausgeführt werden, für die Tausende von Qubits verwendet werden.  Dies ist für zwei Hauptaufgaben hilfreich: 

* Debuggen von klassischem Code, der Teil eines Quantenprogramms ist 
* Schätzen der Ressourcen, die zum Ausführen einer bestimmten Instanz eines Quantenprogramms auf einem Quantencomputer erforderlich sind Die [Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator), die über eine stärker eingeschränkte Gruppe von Metriken verfügt, basiert beispielsweise auf dem Ablaufverfolgungssimulator.

## <a name="invoking-the-quantum-trace-simulator"></a>Aufrufen des Ablaufverfolgungssimulators für Quantencomputer

Sie können den Ablaufverfolgungssimulator für Quantencomputer nutzen, um beliebige Q#-Operationen auszuführen.

Wie bei anderen Zielcomputern auch, erstellen Sie zuerst eine Instanz der Klasse `QCTraceSimulator` und übergeben sie anschließend als ersten Parameter der `Run`-Methode einer Operation.

Beachten Sie hierbei Folgendes: Im Gegensatz zur Klasse `QuantumSimulator` wird mit der Klasse `QCTraceSimulator` nicht die <xref:System.IDisposable>-Schnittstelle implementiert, sodass Sie sie nicht in eine `using`-Anweisung einschließen müssen.

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a>Angeben der Wahrscheinlichkeit von Messergebnissen

Da vom Ablaufverfolgungssimulator für Quantencomputer der tatsächliche Quantenzustand nicht simuliert wird, kann die Wahrscheinlichkeit von Messergebnissen für eine Operation nicht berechnet werden. 

Falls eine Operation Messungen enthält, müssen Sie diese Wahrscheinlichkeiten daher explizit angeben, indem Sie die Operation <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> aus dem Namespace <xref:Microsoft.Quantum.Diagnostics> verwenden. Das folgende Beispiel veranschaulicht dies:

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Wenn vom Ablaufverfolgungssimulator für Quantencomputer das Element `AssertMeasurementProbability` erkannt wird, zeichnet er auf, dass die Messung von `PauliZ` auf `source` und `q` zum Ergebnis `Zero` mit einer Wahrscheinlichkeit von **0,5** führen sollte. Später beim Ausführen der Operation `M` werden dann die aufgezeichneten Werte für die Ergebniswahrscheinlichkeiten erkannt, und für `M` wird `Zero` oder `One` mit der Wahrscheinlichkeit **0,5** zurückgegeben. Wenn derselbe Code in einem Simulator ausgeführt wird, mit dem der Quantenzustand nachverfolgt wird, überprüft dieser die Wahrscheinlichkeiten in `AssertMeasurementProbability` auf ihre Richtigkeit.

Beachten Sie Folgendes: Wenn mindestens eine Messoperation nicht über `AssertMeasurementProbability` mit Anmerkungen versehen wurde, wird vom Simulator [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception) ausgelöst.

## <a name="quantum-trace-simulator-tools"></a>Tools für den Ablaufverfolgungssimulator für Quantencomputer

Das QDK enthält fünf Tools, die Sie mit einem Ablaufverfolgungssimulator für Quantencomputer nutzen können, um Fehler in Ihren Programmen zu erkennen und Ressourcenschätzungen für Quantenprogramme durchzuführen: 

|Tool | Beschreibung |
|-----| -----|
|[Überprüfung auf eindeutige Eingaben](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |Dient zum Durchführen einer Überprüfung auf potenzielle Konflikte mit freigegebenen Qubits. |
|[Überprüfung auf Verwendung von ungültigen Qubits](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |Dient zum Durchführen einer Überprüfung, ob eine Operation vom Programm auf ein bereits freigegebenes Qubit angewendet wird. |
|[Indikator für primitive Vorgänge](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | Dient zum Ermitteln der Anzahl von Primitiven in allen Operationen, die in einem Quantenprogramm aufgerufen werden.  |
|[Tiefenindikator](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |Dient zum Erfassen der jeweiligen Anzahl für die Untergrenze der Tiefe aller Operationen, die in einem Quantenprogramm ausgelöst werden.   |
|[Breitenindikator](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |Dient zum Zählen der Qubits, die von den einzelnen Operationen eines Quantenprogramms zugeordnet und geliehen werden. |

Diese Tools werden jeweils aktiviert, indem in `QCTraceSimulatorConfiguration` die entsprechenden Flags festgelegt und anschließend die Konfiguration an die `QCTraceSimulator`-Deklaration übergeben wird. Informationen zur Verwendung dieser Tools finden Sie unter den Links in der obigen Liste. Weitere Informationen zum Konfigurieren von `QCTraceSimulator` finden Sie unter [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).

## <a name="qctracesimulator-methods"></a>QCTraceSimulator-Methoden

`QCTraceSimulator` verfügt über mehrere integrierte Methoden, um die Werte der Metriken abzurufen, die während einer Quantenoperation nachverfolgt werden. Beispiele für die Methoden [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) und [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) finden Sie in den Artikeln zu den Tools [Indikator für primitive Vorgänge](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Tiefenindikator](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) und [Breitenindikator](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter). Weitere Informationen zu allen verfügbaren Methoden finden Sie in der Q#-API-Referenz unter [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator).  

## <a name="see-also"></a>Weitere Informationen

- [Ressourcenschätzung für Quantencomputer](xref:microsoft.quantum.machines.resources-estimator)
- [Toffoli-Simulator für Quantencomputer](xref:microsoft.quantum.machines.toffoli-simulator)
- [Simulator für den vollständigen Zustand für Quantencomputer](xref:microsoft.quantum.machines.full-state-simulator) 