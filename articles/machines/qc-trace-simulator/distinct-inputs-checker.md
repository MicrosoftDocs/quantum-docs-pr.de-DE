---
title: Unterschiedliche Eingaben für Eingaben | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: ce3f156a84a4509781a74c9276b953c79670a756
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864303"
---
# <a name="distinct-inputs-checker"></a><span data-ttu-id="55c47-103">Unterschiedliche Eingaben für Eingaben</span><span class="sxs-lookup"><span data-stu-id="55c47-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="55c47-104">Der `Distinct Inputs Checker` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.</span><span class="sxs-lookup"><span data-stu-id="55c47-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="55c47-105">Es dient zur Erkennung potenzieller Fehler im Code.</span><span class="sxs-lookup"><span data-stu-id="55c47-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="55c47-106">Sehen Sie sich den folgenden Q #-Code an, um die von diesem Paket erkannten Probleme zu veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="55c47-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

```qsharp
operation DoBoth(q1 : Qubit, q2 : Qubit, op1 : (Qubit => Unit), op2 : (Qubit => Unit)) : Unit {

    op1(q1);
    op2(q2);
}
```

<span data-ttu-id="55c47-107">Wenn der Benutzer dieses Programm ansieht, geht er davon aus, dass die Reihenfolge, in der `op1` und `op2` aufgerufen werden, keine Rolle spielt, da `q1` und `q2` unterschiedliche Qubits und Vorgänge sind, die auf unterschiedliche Qubits-Vorgänge reagieren.</span><span class="sxs-lookup"><span data-stu-id="55c47-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="55c47-108">Wir sehen uns nun ein Beispiel an, in dem dieser Vorgang verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="55c47-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation CapturedQubits () : Unit {

    using (q = Qubit[3]) {
        let op1 = CNOT(_, q[1]);
        let op2 = CNOT(q[1], _);
        DoBoth(q[0], q[2], op1, op2);
    }
}
```

<span data-ttu-id="55c47-109">Nun werden `op1` und `op2` mithilfe einer partiellen Anwendung abgerufen und ein Qubit gemeinsam verwendet.</span><span class="sxs-lookup"><span data-stu-id="55c47-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="55c47-110">Wenn der Benutzer im obigen Beispiel `DoBoth` aufruft, hängt das Ergebnis des Vorgangs von der Reihenfolge der `op1` und `op2` innerhalb `DoBoth`ab.</span><span class="sxs-lookup"><span data-stu-id="55c47-110">When the user calls `DoBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `DoBoth`.</span></span> <span data-ttu-id="55c47-111">Dies ist definitiv nicht das, was der Benutzer erwarten würde.</span><span class="sxs-lookup"><span data-stu-id="55c47-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="55c47-112">Der `Distinct Inputs Checker` erkennt solche Situationen, wenn er aktiviert wird, und löst `DistinctInputsCheckerException`aus.</span><span class="sxs-lookup"><span data-stu-id="55c47-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="55c47-113">Weitere Informationen finden Sie in der API-Dokumentation zu [distinctinputscheckerexception](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="55c47-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="55c47-114">Verwenden der unterschiedlichen Eingabe Prüfung in C# Ihrem Programm</span><span class="sxs-lookup"><span data-stu-id="55c47-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="55c47-115">Im folgenden finden Sie ein Beispiel C# für einen Treibercode für die Verwendung des Ablauf Verfolgungs Simulators für Quantum-Computer mit aktiviertem `Distinct Inputs Checker`:</span><span class="sxs-lookup"><span data-stu-id="55c47-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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

<span data-ttu-id="55c47-116">Die Klasse `QCTraceSimulatorConfiguration` speichert die Konfiguration des Ablauf Verfolgungs Simulators für Quantum-Computer und kann als Argument für den `QCTraceSimulator`-Konstruktor angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="55c47-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="55c47-117">Wenn `useDistinctInputsChecker` auf true festgelegt ist, ist `Distinct Inputs Checker` aktiviert.</span><span class="sxs-lookup"><span data-stu-id="55c47-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="55c47-118">Weitere Informationen finden Sie in der API-Dokumentation zu [qctracesimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) und [qctracesimulatorconfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .</span><span class="sxs-lookup"><span data-stu-id="55c47-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="55c47-119">Informationen finden Sie auch unter</span><span class="sxs-lookup"><span data-stu-id="55c47-119">See also</span></span>

- <span data-ttu-id="55c47-120">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="55c47-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
