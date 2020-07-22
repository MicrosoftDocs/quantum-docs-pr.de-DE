---
title: Ungültige Qubits use Checker-Quantum Development Kit
description: 'Erfahren Sie mehr über die von Microsoft QDK ungültige Qubits-Verwendung, die den Quantum-Ablauf Verfolgungs Simulator verwendet, um Ihren Q #-Code auf potenziell ungültige Qubits zu überprüfen.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: fccf6d5784b587f4ad9b659e23027619acd06ffa
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871092"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>Quantum-Ablauf Verfolgungs Simulator: Ungültige Qubits-Verwendung (Checker)

Die ungültige Qubits-Verwendungs Überprüfung ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit. Sie können es verwenden, um potenzielle Fehler im Code zu erkennen, die durch ungültige Qubits verursacht werden. 

## <a name="invalid-qubits"></a>Ungültige Qubits.

Sehen Sie sich den folgenden Q #-Code an, um die Probleme zu veranschaulichen, die von der ungültigen Qubits-Verwendungs Überprüfung erkannt werden:

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Wenn Sie den- `H` Vorgang auf Anwenden `q[0]` , verweist er auf ein bereits veröffentlichtes Qubit, das undefiniertes Verhalten verursachen kann. Wenn die ungültige Qubits-Verwendung aktivieren aktiviert ist, wird die Ausnahme `InvalidatedQubitsUseCheckerException` ausgelöst, wenn das Programm einen Vorgang auf ein bereits veröffentlichtes Qubit anwendet. Weitere Informationen finden Sie unter <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>Aufrufen der ungültigen Qubits use Checker

Um den Quantum-Ablauf Verfolgungs Simulator mit der ungültigen Qubits-Verwendung zu verwenden, müssen Sie eine- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> Instanz erstellen, die `UseInvalidatedQubitsUseChecker` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a>Verwenden der ungültigen Qubits use Checker in einem c#-Host Programm

Im folgenden finden Sie ein Beispiel für c#-Host Programme, die den Quantum-Ablauf Verfolgungs Simulator verwenden, bei dem die ungültige Qubits-Verwendung aktiviert ist: 

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
            traceSimCfg.UseInvalidatedQubitsUseChecker = true; // enables UseInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a>Weitere Informationen

- Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API-Referenz.