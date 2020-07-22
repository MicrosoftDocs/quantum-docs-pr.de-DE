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
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a><span data-ttu-id="d40f8-103">Quantum-Ablauf Verfolgungs Simulator: unterschiedliche Eingaben für Eingaben</span><span class="sxs-lookup"><span data-stu-id="d40f8-103">Quantum trace simulator: distinct inputs checker</span></span>

<span data-ttu-id="d40f8-104">Die unterschiedliche Inputs-Prüfung ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="d40f8-104">The distinct inputs checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="d40f8-105">Sie können es verwenden, um potenzielle Fehler im Code zu erkennen, die durch Konflikte mit freigegebenen Qubits verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="d40f8-105">You can use it to detect potential bugs in the code caused by conflicts with shared qubits.</span></span> 

## <a name="conflicts-with-shared-qubits"></a><span data-ttu-id="d40f8-106">Konflikte mit freigegebenen Qubits</span><span class="sxs-lookup"><span data-stu-id="d40f8-106">Conflicts with shared qubits</span></span>

<span data-ttu-id="d40f8-107">Sehen Sie sich den folgenden Q #-Code an, um die Probleme zu veranschaulichen, die von der unterschiedlichen Eingaben Prüfung erkannt werden:</span><span class="sxs-lookup"><span data-stu-id="d40f8-107">Consider the following piece of Q# code to illustrate the issues detected by the distinct inputs checker:</span></span>

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

<span data-ttu-id="d40f8-108">Wenn Sie sich dieses Programm ansehen, können Sie davon ausgehen, dass die Reihenfolge, in der es aufruft `op1` und `op2` keine Rolle spielt, da `q1` und `q2` unterschiedliche Qubits und Vorgänge sind, die auf unterschiedliche Qubits-Vorgänge reagieren.</span><span class="sxs-lookup"><span data-stu-id="d40f8-108">When you look at this program, you can assume that the order in which it calls `op1` and `op2` does not matter, because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> 

<span data-ttu-id="d40f8-109">Sehen Sie sich nun das folgende Beispiel an:</span><span class="sxs-lookup"><span data-stu-id="d40f8-109">Now, consider this example:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="d40f8-110">Beachten Sie, dass `op1` und `op2` sowohl mit einer partiellen Anwendung als auch mit einem Qubit abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d40f8-110">Note that `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="d40f8-111">Wenn Sie `ApplyBoth` in diesem Beispiel aufzurufen, hängt das Ergebnis des Vorgangs von der Reihenfolge von und innerhalb von ab, `op1` `op2` `ApplyBoth` was Sie erwarten.</span><span class="sxs-lookup"><span data-stu-id="d40f8-111">When you call `ApplyBoth` in this example, the result of the operation depends on the order of `op1` and `op2` inside `ApplyBoth` - not what you would expect to happen.</span></span> <span data-ttu-id="d40f8-112">Wenn Sie die unterschiedliche Eingaben-Überprüfung aktivieren, werden derartige Situationen erkannt, und es wird eine ausgelöst `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="d40f8-112">When you enable the distinct inputs checker, it detects such situations and throws a `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="d40f8-113">Weitere Informationen finden Sie unter <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in der Q #-API-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="d40f8-113">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in the Q# API library.</span></span>

## <a name="invoking-the-distinct-inputs-checker"></a><span data-ttu-id="d40f8-114">Aufrufen der unterschiedlichen Eingabe Prüfung</span><span class="sxs-lookup"><span data-stu-id="d40f8-114">Invoking the distinct inputs checker</span></span>

<span data-ttu-id="d40f8-115">Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit der unterschiedlichen Eingabe Prüfung müssen Sie eine- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> Instanz erstellen, die `UseDistinctInputsChecker` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen.</span><span class="sxs-lookup"><span data-stu-id="d40f8-115">To run the quantum trace simulator with the distinct inputs checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseDistinctInputsChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a><span data-ttu-id="d40f8-116">Verwenden der unterschiedlichen Eingabe Prüfung in einem c#-Host Programm</span><span class="sxs-lookup"><span data-stu-id="d40f8-116">Using the distinct inputs checker in a C# host program</span></span>

<span data-ttu-id="d40f8-117">Im folgenden finden Sie ein Beispiel für ein c#-Host Programm, das den Quantum-Ablauf Verfolgungs Simulator mit aktivierter unterschiedlicher Eingabe Prüfung verwendet:</span><span class="sxs-lookup"><span data-stu-id="d40f8-117">The following is an example of C# host program that uses the quantum trace simulator with the distinct inputs checker enabled:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d40f8-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d40f8-118">See also</span></span>

- <span data-ttu-id="d40f8-119">Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="d40f8-119">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="d40f8-120">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="d40f8-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="d40f8-121">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="d40f8-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="d40f8-122">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="d40f8-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API reference.</span></span>
