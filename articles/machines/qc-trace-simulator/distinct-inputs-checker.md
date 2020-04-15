---
title: Unterschiedliche Eingaben für Eingaben
description: 'Erfahren Sie mehr über die unterschiedliche e-How-Eingaben von Microsoft QDK, die ihren Q#-Code auf potenzielle Konflikte mit freigegebenen Qubits überprüft.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 11a0573242c8afb12f242aa3be5f9cff18290452
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907102"
---
# <a name="distinct-inputs-checker"></a>Unterschiedliche Eingaben für Eingaben

Der `Distinct Inputs Checker` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer. Es dient zur Erkennung potenzieller Fehler im Code. Sehen Sie sich den folgenden Q#-Code an, um die von diesem Paket erkannten Probleme zu veranschaulichen:

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

## <a name="see-also"></a>Weitere Informationen

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
