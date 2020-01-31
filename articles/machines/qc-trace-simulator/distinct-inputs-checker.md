---
title: Unterschiedliche Eingaben für Eingaben | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 3c21a54f5da83bf1ea0792e79cc773be5fba71e8
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820962"
---
# <a name="distinct-inputs-checker"></a>Unterschiedliche Eingaben für Eingaben

Der `Distinct Inputs Checker` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer. Es dient zur Erkennung potenzieller Fehler im Code. Sehen Sie sich den folgenden Q #-Code an, um die von diesem Paket erkannten Probleme zu veranschaulichen:

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

Wenn der Benutzer dieses Programm ansieht, geht er davon aus, dass die Reihenfolge, in der `op1` und `op2` aufgerufen werden, keine Rolle spielt, da `q1` und `q2` unterschiedliche Qubits und Vorgänge sind, die auf unterschiedliche Qubits-Vorgänge reagieren. Wir sehen uns nun ein Beispiel an, in dem dieser Vorgang verwendet wird:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Nun werden `op1` und `op2` mithilfe einer partiellen Anwendung abgerufen und ein Qubit gemeinsam verwendet. Wenn der Benutzer im obigen Beispiel `ApplyBoth` aufruft, hängt das Ergebnis des Vorgangs von der Reihenfolge der `op1` und `op2` innerhalb `ApplyBoth`ab. Dies ist definitiv nicht das, was der Benutzer erwarten würde. Der `Distinct Inputs Checker` erkennt solche Situationen, wenn er aktiviert wird, und löst `DistinctInputsCheckerException`aus. Weitere Informationen finden Sie in der API-Dokumentation zu [distinctinputscheckerexception](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>Verwenden der unterschiedlichen Eingabe Prüfung in C# Ihrem Programm

Im folgenden finden Sie ein Beispiel C# für einen Treibercode für die Verwendung des Ablauf Verfolgungs Simulators für Quantum-Computer mit aktiviertem `Distinct Inputs Checker`:

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

Die Klasse `QCTraceSimulatorConfiguration` speichert die Konfiguration des Ablauf Verfolgungs Simulators für Quantum-Computer und kann als Argument für den `QCTraceSimulator`-Konstruktor angegeben werden. Wenn `useDistinctInputsChecker` auf true festgelegt ist, ist `Distinct Inputs Checker` aktiviert. Weitere Informationen finden Sie in der API-Dokumentation zu [qctracesimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) und [qctracesimulatorconfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .

## <a name="see-also"></a>Siehe auch

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
