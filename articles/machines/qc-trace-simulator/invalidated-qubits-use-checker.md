---
title: Überprüfung auf Verwendung von ungültigen Qubits
description: 'Erfahren Sie mehr über das von Microsoft QDK ungültige Qubits use Checker, das den Q #-Code auf potenziell ungültige Qubits überprüft.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: e2bbb12448e27f28db030a0084302fb24f46f26b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907068"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="c1e7d-103">Ungültige Qubits-Verwendungs Überprüfung</span><span class="sxs-lookup"><span data-stu-id="c1e7d-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="c1e7d-104">Der `Invalidated Qubits Use Checker` ist Teil des Quantum- [computertracesimulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro) , der zum Erkennen potenzieller Fehler im Code entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="c1e7d-105">Sehen Sie sich den folgenden Q #-Code an, um die vom `Invalidated Qubits Use Checker`erkannten Probleme zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="c1e7d-106">Wenn `H` auf `q[0]` angewendet wird, verweist er auf ein bereits veröffentlichtes Qubit.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="c1e7d-107">Dies kann zu undefiniertem Verhalten führen.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-107">This can cause undefined behavior.</span></span> <span data-ttu-id="c1e7d-108">Wenn die `Invalidated Qubits Use Checker` aktiviert ist, wird die Ausnahme `InvalidatedQubitsUseCheckerException` ausgelöst, wenn ein Vorgang auf ein bereits veröffentlichtes Qubit angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="c1e7d-109">Weitere Informationen finden Sie in der API-Dokumentation zu [invalidatedqubitsumencheckerexception](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="c1e7d-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="c1e7d-110">Verwenden der ungültigen Qubits use Checker in Ihrem C# Programm</span><span class="sxs-lookup"><span data-stu-id="c1e7d-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="c1e7d-111">Im folgenden finden Sie ein Beispiel C# für einen Treibercode zur Verwendung der Quantum-Computer `Trace
Simulator` mit aktiviertem `Invalidated Qubits Use Checker`:</span><span class="sxs-lookup"><span data-stu-id="c1e7d-111">The following is an example of C# driver code for using the quantum computer `Trace
Simulator` with the `Invalidated Qubits Use Checker` enabled:</span></span> 

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

<span data-ttu-id="c1e7d-112">Die Klasse `QCTraceSimulatorConfiguration` speichert die Konfiguration des Ablauf Verfolgungs Simulators für Quantum-Computer und kann als Argument für den `QCTraceSimulator`-Konstruktor angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="c1e7d-113">Wenn `useInvalidatedQubitsUseChecker` auf true festgelegt ist, ist `Invalidated Qubits Use Checker` aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c1e7d-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="c1e7d-114">Weitere Informationen finden Sie in der API-Dokumentation zu [qctracesimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) und [qctracesimulatorconfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="c1e7d-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1e7d-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c1e7d-115">See also</span></span> ##

- <span data-ttu-id="c1e7d-116">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="c1e7d-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
