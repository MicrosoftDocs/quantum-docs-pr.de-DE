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
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a><span data-ttu-id="cb78f-103">Quantum-Ablauf Verfolgungs Simulator: Ungültige Qubits-Verwendung (Checker)</span><span class="sxs-lookup"><span data-stu-id="cb78f-103">Quantum trace simulator: invalidated qubits use checker</span></span>

<span data-ttu-id="cb78f-104">Die ungültige Qubits-Verwendungs Überprüfung ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit.</span><span class="sxs-lookup"><span data-stu-id="cb78f-104">The invalidated qubits use checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="cb78f-105">Sie können es verwenden, um potenzielle Fehler im Code zu erkennen, die durch ungültige Qubits verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="cb78f-105">You can use it to detect potential bugs in the code caused by invalid qubits.</span></span> 

## <a name="invalid-qubits"></a><span data-ttu-id="cb78f-106">Ungültige Qubits.</span><span class="sxs-lookup"><span data-stu-id="cb78f-106">Invalid qubits</span></span>

<span data-ttu-id="cb78f-107">Sehen Sie sich den folgenden Q #-Code an, um die Probleme zu veranschaulichen, die von der ungültigen Qubits-Verwendungs Überprüfung erkannt werden:</span><span class="sxs-lookup"><span data-stu-id="cb78f-107">Consider the following piece of Q# code to illustrate the issues detected by the invalidated qubits use checker:</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="cb78f-108">Wenn Sie den- `H` Vorgang auf Anwenden `q[0]` , verweist er auf ein bereits veröffentlichtes Qubit, das undefiniertes Verhalten verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="cb78f-108">When you apply the `H` operation to `q[0]`, it points to an already released qubit, which can cause undefined behavior.</span></span> <span data-ttu-id="cb78f-109">Wenn die ungültige Qubits-Verwendung aktivieren aktiviert ist, wird die Ausnahme `InvalidatedQubitsUseCheckerException` ausgelöst, wenn das Programm einen Vorgang auf ein bereits veröffentlichtes Qubit anwendet.</span><span class="sxs-lookup"><span data-stu-id="cb78f-109">When the Invalidated Qubits Use Checker is enabled, it throws the exception `InvalidatedQubitsUseCheckerException` if the program applies an operation to an already released qubit.</span></span> <span data-ttu-id="cb78f-110">Weitere Informationen finden Sie unter <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span><span class="sxs-lookup"><span data-stu-id="cb78f-110">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span></span>

## <a name="invoking-the-invalidated-qubits-use-checker"></a><span data-ttu-id="cb78f-111">Aufrufen der ungültigen Qubits use Checker</span><span class="sxs-lookup"><span data-stu-id="cb78f-111">Invoking the invalidated qubits use checker</span></span>

<span data-ttu-id="cb78f-112">Um den Quantum-Ablauf Verfolgungs Simulator mit der ungültigen Qubits-Verwendung zu verwenden, müssen Sie eine- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> Instanz erstellen, die `UseInvalidatedQubitsUseChecker` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen.</span><span class="sxs-lookup"><span data-stu-id="cb78f-112">To run the quantum trace simulator with the invalidated qubits use checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseInvalidatedQubitsUseChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a><span data-ttu-id="cb78f-113">Verwenden der ungültigen Qubits use Checker in einem c#-Host Programm</span><span class="sxs-lookup"><span data-stu-id="cb78f-113">Using the invalidated qubits use checker in a C# host program</span></span>

<span data-ttu-id="cb78f-114">Im folgenden finden Sie ein Beispiel für c#-Host Programme, die den Quantum-Ablauf Verfolgungs Simulator verwenden, bei dem die ungültige Qubits-Verwendung aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="cb78f-114">The following is an example of C# host programs that uses the quantum trace simulator with the invalidated qubits use checker enabled:</span></span> 

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

## <a name="see-also"></a><span data-ttu-id="cb78f-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cb78f-115">See also</span></span>

- <span data-ttu-id="cb78f-116">Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="cb78f-116">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="cb78f-117">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="cb78f-117">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="cb78f-118">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="cb78f-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="cb78f-119">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="cb78f-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API reference.</span></span>