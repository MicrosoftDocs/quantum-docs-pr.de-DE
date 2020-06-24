---
title: Unterschiedliche Eingaben für Eingaben
description: 'Erfahren Sie mehr über die unterschiedliche e-How-Eingaben von Microsoft QDK, die ihren Q #-Code auf potenzielle Konflikte mit freigegebenen Qubits überprüft.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 11a0573242c8afb12f242aa3be5f9cff18290452
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274931"
---
# <a name="distinct-inputs-checker"></a>Unterschiedliche Eingaben für Eingaben

Der `Distinct Inputs Checker` ist ein Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer. Es dient zur Erkennung potenzieller Fehler im Code. Sehen Sie sich den folgenden Q #-Code an, um die von diesem Paket erkannten Probleme zu veranschaulichen:

```qsharp
operation ApplyBoth(
    q1 : Qubit,
    q2 : Qubit,
    op1 : (Qubit => Unit),
    op2 : (Qubit => Unit))
: Unit {
    op1(q1);
    op2(q2);
}
```

Wenn der Benutzer dieses Programm ansieht, geht er davon aus, dass die Reihenfolge, in der `op1` und `op2` aufgerufen werden, keine Rolle spielt, da `q1` und `q2` unterschiedliche Qubits und Vorgänge sind, die auf unterschiedliche Qubits-Aufgaben reagieren. Wir sehen uns nun ein Beispiel an, in dem dieser Vorgang verwendet wird:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Nun `op1` `op2` werden und sowohl mit partieller Anwendung als auch mit einem Qubit verwendet. Wenn der Benutzer `ApplyBoth` im obigen Beispiel aufruft, hängt das Ergebnis des Vorgangs von der Reihenfolge von `op1` und innerhalb von ab `op2` `ApplyBoth` . Dies ist definitiv nicht das, was der Benutzer erwarten würde. Der `Distinct Inputs Checker` erkennt solche Situationen, wenn er aktiviert ist, und löst aus `DistinctInputsCheckerException` . Weitere Informationen finden Sie in der API-Dokumentation zu [distinctinputscheckerexception](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>Verwenden der unterschiedlichen Eingabe Prüfung in Ihrem c#-Programm

Im folgenden finden Sie ein Beispiel für c#-Treibercode für die Verwendung des Ablauf Verfolgungs Simulators für Quantum-Computer mit `Distinct Inputs Checker` aktiviertem:

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
            var traceSimCfg = new QCTraceSimulatorConfiguration();
            traceSimCfg.useDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

Die `QCTraceSimulatorConfiguration` -Klasse speichert die Konfiguration des Ablauf Verfolgungs Simulators für Quantum-Computer und kann als Argument für den- `QCTraceSimulator` Konstruktor angegeben werden. Wenn `useDistinctInputsChecker` auf true festgelegt ist, `Distinct Inputs Checker` wird aktiviert. Weitere Informationen finden Sie in der API-Dokumentation zu [qctracesimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) und [qctracesimulatorconfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .

## <a name="see-also"></a>Weitere Informationen

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
