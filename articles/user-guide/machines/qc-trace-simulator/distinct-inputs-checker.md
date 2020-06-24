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
# <a name="distinct-inputs-checker"></a><span data-ttu-id="cea75-103">Unterschiedliche Eingaben für Eingaben</span><span class="sxs-lookup"><span data-stu-id="cea75-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="cea75-104">Der `Distinct Inputs Checker` ist ein Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.</span><span class="sxs-lookup"><span data-stu-id="cea75-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="cea75-105">Es dient zur Erkennung potenzieller Fehler im Code.</span><span class="sxs-lookup"><span data-stu-id="cea75-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="cea75-106">Sehen Sie sich den folgenden Q #-Code an, um die von diesem Paket erkannten Probleme zu veranschaulichen:</span><span class="sxs-lookup"><span data-stu-id="cea75-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

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

<span data-ttu-id="cea75-107">Wenn der Benutzer dieses Programm ansieht, geht er davon aus, dass die Reihenfolge, in der `op1` und `op2` aufgerufen werden, keine Rolle spielt, da `q1` und `q2` unterschiedliche Qubits und Vorgänge sind, die auf unterschiedliche Qubits-Aufgaben reagieren.</span><span class="sxs-lookup"><span data-stu-id="cea75-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="cea75-108">Wir sehen uns nun ein Beispiel an, in dem dieser Vorgang verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="cea75-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="cea75-109">Nun `op1` `op2` werden und sowohl mit partieller Anwendung als auch mit einem Qubit verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea75-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="cea75-110">Wenn der Benutzer `ApplyBoth` im obigen Beispiel aufruft, hängt das Ergebnis des Vorgangs von der Reihenfolge von `op1` und innerhalb von ab `op2` `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="cea75-110">When the user calls `ApplyBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `ApplyBoth`.</span></span> <span data-ttu-id="cea75-111">Dies ist definitiv nicht das, was der Benutzer erwarten würde.</span><span class="sxs-lookup"><span data-stu-id="cea75-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="cea75-112">Der `Distinct Inputs Checker` erkennt solche Situationen, wenn er aktiviert ist, und löst aus `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="cea75-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="cea75-113">Weitere Informationen finden Sie in der API-Dokumentation zu [distinctinputscheckerexception](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) .</span><span class="sxs-lookup"><span data-stu-id="cea75-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="cea75-114">Verwenden der unterschiedlichen Eingabe Prüfung in Ihrem c#-Programm</span><span class="sxs-lookup"><span data-stu-id="cea75-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="cea75-115">Im folgenden finden Sie ein Beispiel für c#-Treibercode für die Verwendung des Ablauf Verfolgungs Simulators für Quantum-Computer mit `Distinct Inputs Checker` aktiviertem:</span><span class="sxs-lookup"><span data-stu-id="cea75-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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

<span data-ttu-id="cea75-116">Die `QCTraceSimulatorConfiguration` -Klasse speichert die Konfiguration des Ablauf Verfolgungs Simulators für Quantum-Computer und kann als Argument für den- `QCTraceSimulator` Konstruktor angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cea75-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="cea75-117">Wenn `useDistinctInputsChecker` auf true festgelegt ist, `Distinct Inputs Checker` wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cea75-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="cea75-118">Weitere Informationen finden Sie in der API-Dokumentation zu [qctracesimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) und [qctracesimulatorconfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) .</span><span class="sxs-lookup"><span data-stu-id="cea75-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="cea75-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cea75-119">See also</span></span>

- <span data-ttu-id="cea75-120">Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer</span><span class="sxs-lookup"><span data-stu-id="cea75-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
