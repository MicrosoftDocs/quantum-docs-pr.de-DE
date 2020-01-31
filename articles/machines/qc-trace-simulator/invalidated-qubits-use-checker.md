---
title: Ungültige Qubits-Verwendungs Überprüfung | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 093937346488725eacb69ef7da6affde764ec5c1
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820877"
---
# <a name="invalidated-qubits-use-checker"></a>Ungültige Qubits-Verwendungs Überprüfung

Der `Invalidated Qubits Use Checker` ist Teil des Quantum- [computertracesimulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , der zum Erkennen potenzieller Fehler im Code entworfen wurde. Sehen Sie sich den folgenden Q #-Code an, um die vom `Invalidated Qubits Use Checker`erkannten Probleme zu veranschaulichen.

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Wenn `H` auf `q[0]` angewendet wird, verweist er auf ein bereits veröffentlichtes Qubit. Dies kann zu undefiniertem Verhalten führen. Wenn die `Invalidated Qubits Use Checker` aktiviert ist, wird die Ausnahme `InvalidatedQubitsUseCheckerException` ausgelöst, wenn ein Vorgang auf ein bereits veröffentlichtes Qubit angewendet wird. Weitere Informationen finden Sie in der API-Dokumentation zu [invalidatedqubitsumencheckerexception](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>Verwenden der ungültigen Qubits use Checker in Ihrem C# Programm

Im folgenden finden Sie ein Beispiel C# für einen Treibercode zur Verwendung der Quantum-Computer `Trace
Simulator` mit aktiviertem `Invalidated Qubits Use Checker`: 

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
            traceSimCfg.useInvalidatedQubitsUseChecker = true; // enables useInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

Die Klasse `QCTraceSimulatorConfiguration` speichert die Konfiguration des Ablauf Verfolgungs Simulators für Quantum-Computer und kann als Argument für den `QCTraceSimulator`-Konstruktor angegeben werden. Wenn `useInvalidatedQubitsUseChecker` auf true festgelegt ist, ist `Invalidated Qubits Use Checker` aktiviert. Weitere Informationen finden Sie in der API-Dokumentation zu [qctracesimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) und [qctracesimulatorconfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .

## <a name="see-also"></a>Siehe auch ##

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
