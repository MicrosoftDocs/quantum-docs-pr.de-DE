---
title: Unterschiedliche Inputs-Eingaben-Quantum Development Kit
description: 'Erfahren Sie mehr über die unterschiedliche unterschiedliche Inputs-Eingaben von Microsoft QDK, die den Quantum-Ablauf Verfolgungs Simulator zum Überprüfen Ihres Q #-Codes auf potenzielle Konflikte mit freigegebenen Qubits'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 49a1ccc5f37acfeaa1ee08bd974be45a40a76f93
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871143"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a>Quantum-Ablauf Verfolgungs Simulator: unterschiedliche Eingaben für Eingaben

Die unterschiedliche Inputs-Prüfung ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit. Sie können es verwenden, um potenzielle Fehler im Code zu erkennen, die durch Konflikte mit freigegebenen Qubits verursacht werden. 

## <a name="conflicts-with-shared-qubits"></a>Konflikte mit freigegebenen Qubits

Sehen Sie sich den folgenden Q #-Code an, um die Probleme zu veranschaulichen, die von der unterschiedlichen Eingaben Prüfung erkannt werden:

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

Wenn Sie sich dieses Programm ansehen, können Sie davon ausgehen, dass die Reihenfolge, in der es aufruft `op1` und `op2` keine Rolle spielt, da `q1` und `q2` unterschiedliche Qubits und Vorgänge sind, die auf unterschiedliche Qubits-Vorgänge reagieren. 

Sehen Sie sich nun das folgende Beispiel an:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Beachten Sie, dass `op1` und `op2` sowohl mit einer partiellen Anwendung als auch mit einem Qubit abgerufen werden. Wenn Sie `ApplyBoth` in diesem Beispiel aufzurufen, hängt das Ergebnis des Vorgangs von der Reihenfolge von und innerhalb von ab, `op1` `op2` `ApplyBoth` was Sie erwarten. Wenn Sie die unterschiedliche Eingaben-Überprüfung aktivieren, werden derartige Situationen erkannt, und es wird eine ausgelöst `DistinctInputsCheckerException` . Weitere Informationen finden Sie unter <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in der Q #-API-Bibliothek.

## <a name="invoking-the-distinct-inputs-checker"></a>Aufrufen der unterschiedlichen Eingabe Prüfung

Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit der unterschiedlichen Eingabe Prüfung müssen Sie eine- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> Instanz erstellen, die `UseDistinctInputsChecker` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a>Verwenden der unterschiedlichen Eingabe Prüfung in einem c#-Host Programm

Im folgenden finden Sie ein Beispiel für ein c#-Host Programm, das den Quantum-Ablauf Verfolgungs Simulator mit aktivierter unterschiedlicher Eingabe Prüfung verwendet:

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
            traceSimCfg.UseDistinctInputsChecker = true; //enables distinct inputs checker
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
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API-Referenz.
