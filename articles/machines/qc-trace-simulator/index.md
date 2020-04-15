---
title: Ablaufverfolgungssimulator für Quantencomputer
description: Es wird beschrieben, wie Sie den Microsoft-Ablaufverfolgungssimulator für Quantencomputer verwenden, um klassischen Code zu debuggen und die Ressourcenanforderungen eines Quantenprogramms zu schätzen.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 72c259933d2df8f79319e6c0c65ae181a9f9cff3
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "77906082"
---
# <a name="quantum-trace-simulator"></a>Ablaufverfolgungssimulator für Quantencomputer

Mit dem Microsoft-Ablaufverfolgungssimulator für Quantencomputer wird ein Quantenprogramm ausgeführt, ohne tatsächlich den Zustand eines Quantencomputers zu simulieren.  Aus diesem Grund kann der Ablaufverfolgungssimulator Quantenprogramme ausführen, für die Tausende von Qubits verwendet werden.  Dies ist für zwei Hauptaufgaben hilfreich: 

* Debuggen von klassischem Code, der Teil eines Quantenprogramms ist 
* Schätzen der Ressourcen, die zum Ausführen einer bestimmten Instanz eines Quantenprogramms auf einem Quantencomputer erforderlich sind

Für den Ablaufverfolgungssimulator werden zusätzliche Informationen benötigt, die vom Benutzer angegeben werden, wenn Messungen durchgeführt werden müssen. Weitere Informationen hierzu finden Sie im Abschnitt [Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen](#providing-the-probability-of-measurement-outcomes). 

## <a name="providing-the-probability-of-measurement-outcomes"></a>Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen

Es gibt zwei Arten von Messungen, die in Quantenalgorithmen angezeigt werden. Die erste Messung ist eine Hilfsmessung, bei der der Benutzer normalerweise über die Wahrscheinlichkeit der Ergebnisse informiert ist. In diesem Fall kann der Benutzer <xref:microsoft.quantum.intrinsic.assertprob> über den Namespace <xref:microsoft.quantum.intrinsic> schreiben, um dies mitzuteilen. Das folgende Beispiel veranschaulicht dies:

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Wenn vom Ablaufverfolgungssimulator `AssertProb` ausgeführt wird, wird dies per Messung von `PauliZ` auf `source` aufgezeichnet, und `q` sollte das Ergebnis `Zero` bei einer Wahrscheinlichkeit von 0,5 aufweisen. Wenn der Simulator später `M` ausführt, erkennt er die aufgezeichneten Werte der Ergebniswahrscheinlichkeiten, und `M` gibt `Zero` oder `One` mit einer Wahrscheinlichkeit von 0,5 zurück. Wenn derselbe Code in einem Simulator ausgeführt wird, mit dem der Quantenzustand nachverfolgt wird, überprüft dieser die Wahrscheinlichkeiten in `AssertProb` auf ihre Richtigkeit.

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a>Ausführen des Programms mit dem Ablaufverfolgungssimulator für Quantencomputer 

Sie können sich den Ablaufverfolgungssimulator für Quantencomputer als regulären Zielcomputer vorstellen. Das C#-Treiberprogramm für dessen Verwendung ähnelt stark den Programmen für andere Quantensimulatoren: 

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
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

Beachten Sie Folgendes: Wenn mindestens eine Messung nicht über `AssertProb` mit Anmerkungen versehen wurde, löst der Simulator `UnconstrainedMeasurementException` über den Namespace `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` aus. Weitere Informationen finden Sie in der API-Dokumentation zu [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException).

Zusätzlich zur Ausführung von Quantenprogrammen verfügt der Ablaufverfolgungssimulator noch über fünf Komponenten zur Erkennung von Fehlern in Programmen und zur Durchführung von Ressourcenschätzungen für Quantenprogramme: 

* [Überprüfung auf eindeutige Eingaben](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [Überprüfung auf Verwendung von ungültigen Qubits](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [Indikator für primitive Vorgänge](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [Depth Counter für Leitung](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [Width Counter für Leitung](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

Jede dieser Komponenten kann aktiviert werden, indem in `QCTraceSimulatorConfiguration` geeignete Flags festgelegt werden. Weitere Informationen zur Verwendung dieser Komponenten finden Sie in den entsprechenden Referenzdateien. Ausführliche Informationen finden Sie in der API-Dokumentation zu [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).

## <a name="see-also"></a>Weitere Informationen
[Ablaufverfolgungssimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) für Quantencomputer: C#-Referenz 

