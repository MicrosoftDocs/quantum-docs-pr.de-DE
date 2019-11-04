---
title: Ablaufverfolgungssimulator für Quantencomputer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 7fd9d1fa4fb3c5dd216d846038abd40454ece2e8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035136"
---
# <a name="quantum-trace-simulator"></a><span data-ttu-id="86968-103">Ablaufverfolgungssimulator für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="86968-103">Quantum Trace Simulator</span></span>

<span data-ttu-id="86968-104">Mit dem Microsoft-Ablaufverfolgungssimulator für Quantencomputer wird ein Quantenprogramm ausgeführt, ohne tatsächlich den Zustand eines Quantencomputers zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="86968-104">The Microsoft quantum computer trace simulator executes a quantum program without actually simulating the state of a quantum computer.</span></span>  <span data-ttu-id="86968-105">Aus diesem Grund kann der Ablaufverfolgungssimulator Quantenprogramme ausführen, für die Tausende von Qubits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86968-105">For this reason, the trace simulator can execute quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="86968-106">Dies ist für zwei Hauptaufgaben hilfreich:</span><span class="sxs-lookup"><span data-stu-id="86968-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="86968-107">Debuggen von klassischem Code, der Teil eines Quantenprogramms ist</span><span class="sxs-lookup"><span data-stu-id="86968-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="86968-108">Schätzen der Ressourcen, die zum Ausführen einer bestimmten Instanz eines Quantenprogramms auf einem Quantencomputer erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="86968-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span>

<span data-ttu-id="86968-109">Für den Ablaufverfolgungssimulator werden zusätzliche Informationen benötigt, die vom Benutzer angegeben werden, wenn Messungen durchgeführt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="86968-109">The trace simulator relies on additional information provided by the user when measurements must be performed.</span></span> <span data-ttu-id="86968-110">Weitere Informationen hierzu finden Sie im Abschnitt [Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen](#providing-the-probability-of-measurement-outcomes).</span><span class="sxs-lookup"><span data-stu-id="86968-110">See Section [Providing the probability of measurement outcomes](#providing-the-probability-of-measurement-outcomes) for more details on this.</span></span> 

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="86968-111">Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen</span><span class="sxs-lookup"><span data-stu-id="86968-111">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="86968-112">Es gibt zwei Arten von Messungen, die in Quantenalgorithmen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="86968-112">There are two kinds of measurements that appear in quantum algorithms.</span></span> <span data-ttu-id="86968-113">Die erste Messung ist eine Hilfsmessung, bei der der Benutzer normalerweise über die Wahrscheinlichkeit der Ergebnisse informiert ist.</span><span class="sxs-lookup"><span data-stu-id="86968-113">The first kind plays an auxiliary role where the user usually knows the probability of the outcomes.</span></span> <span data-ttu-id="86968-114">In diesem Fall kann der Benutzer <xref:microsoft.quantum.primitive.assertprob> über den Namespace <xref:microsoft.quantum.primitive> schreiben, um dies mitzuteilen.</span><span class="sxs-lookup"><span data-stu-id="86968-114">In this case the user can write <xref:microsoft.quantum.primitive.assertprob> from the <xref:microsoft.quantum.primitive> namespace to express this knowledge.</span></span> <span data-ttu-id="86968-115">Das folgende Beispiel veranschaulicht dies:</span><span class="sxs-lookup"><span data-stu-id="86968-115">The following example illustrates this:</span></span>

```qsharp
operation Teleportation (source : Qubit, target : Qubit) : Unit {

    using (ancilla = Qubit()) {

        H(ancilla);
        CNOT(ancilla, target);

        CNOT(source, ancilla);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [ancilla], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(ancilla) == One) { X(target); X(ancilla); }
    }
}
```

<span data-ttu-id="86968-116">Wenn vom Ablaufverfolgungssimulator `AssertProb` ausgeführt wird, wird dies per Messung von `PauliZ` auf `source` aufgezeichnet, und `ancilla` sollte das Ergebnis `Zero` bei einer Wahrscheinlichkeit von 0,5 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="86968-116">When the trace simulator executes `AssertProb` it will record that measuring `PauliZ` on `source` and `ancilla` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="86968-117">Wenn der Simulator später `M` ausführt, erkennt er die aufgezeichneten Werte der Ergebniswahrscheinlichkeiten, und `M` gibt `Zero` oder `One` mit einer Wahrscheinlichkeit von 0,5 zurück.</span><span class="sxs-lookup"><span data-stu-id="86968-117">When the simulator executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span> <span data-ttu-id="86968-118">Wenn derselbe Code in einem Simulator ausgeführt wird, mit dem der Quantenzustand nachverfolgt wird, überprüft dieser die Wahrscheinlichkeiten in `AssertProb` auf ihre Richtigkeit.</span><span class="sxs-lookup"><span data-stu-id="86968-118">When the same code is executed on a simulator that keeps track of the quantum state, such a simulator will check that the provided probabilities in `AssertProb` are correct.</span></span>

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a><span data-ttu-id="86968-119">Ausführen des Programms mit dem Ablaufverfolgungssimulator für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="86968-119">Running your Program with the Quantum Computer Trace Simulator</span></span> 

<span data-ttu-id="86968-120">Sie können sich den Ablaufverfolgungssimulator für Quantencomputer als regulären Zielcomputer vorstellen.</span><span class="sxs-lookup"><span data-stu-id="86968-120">The quantum computer trace simulator may be viewed as just another target machine.</span></span> <span data-ttu-id="86968-121">Das C#-Treiberprogramm für dessen Verwendung ähnelt stark den Programmen für andere Quantensimulatoren:</span><span class="sxs-lookup"><span data-stu-id="86968-121">The C# driver program for using it is very similar to the one for any other quantum Simulator:</span></span> 

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
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="86968-122">Beachten Sie Folgendes: Wenn mindestens eine Messung nicht über `AssertProb` mit Anmerkungen versehen wurde, löst der Simulator `UnconstrainedMeasurementException` über den Namespace `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` aus.</span><span class="sxs-lookup"><span data-stu-id="86968-122">Note that if there is at least one measurement not annotated using `AssertProb`, the simulator will throw `UnconstrainedMeasurementException` from the `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` namespace.</span></span> <span data-ttu-id="86968-123">Weitere Informationen finden Sie in der API-Dokumentation zu [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException).</span><span class="sxs-lookup"><span data-stu-id="86968-123">See the API documentation on [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) for more details.</span></span>

<span data-ttu-id="86968-124">Zusätzlich zur Ausführung von Quantenprogrammen verfügt der Ablaufverfolgungssimulator noch über fünf Komponenten zur Erkennung von Fehlern in Programmen und zur Durchführung von Ressourcenschätzungen für Quantenprogramme:</span><span class="sxs-lookup"><span data-stu-id="86968-124">In addition to running quantum programs, the trace simulator comes with five components for detecting bugs in programs and performing quantum program resource estimates:</span></span> 

* [<span data-ttu-id="86968-125">Überprüfung auf eindeutige Eingaben</span><span class="sxs-lookup"><span data-stu-id="86968-125">Distinct Inputs Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [<span data-ttu-id="86968-126">Überprüfung auf Verwendung von ungültigen Qubits</span><span class="sxs-lookup"><span data-stu-id="86968-126">Invalidated Qubits Use Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [<span data-ttu-id="86968-127">Indikator für primitive Vorgänge</span><span class="sxs-lookup"><span data-stu-id="86968-127">Primitive Operations Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [<span data-ttu-id="86968-128">Depth Counter für Leitung</span><span class="sxs-lookup"><span data-stu-id="86968-128">Circuit Depth Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [<span data-ttu-id="86968-129">Width Counter für Leitung</span><span class="sxs-lookup"><span data-stu-id="86968-129">Circuit Width Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

<span data-ttu-id="86968-130">Jede dieser Komponenten kann aktiviert werden, indem in `QCTraceSimulatorConfiguration` geeignete Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="86968-130">Each of these components may be enabled by setting appropriate flags in `QCTraceSimulatorConfiguration`.</span></span> <span data-ttu-id="86968-131">Weitere Informationen zur Verwendung dieser Komponenten finden Sie in den entsprechenden Referenzdateien.</span><span class="sxs-lookup"><span data-stu-id="86968-131">More details about using each of these components are provided in the corresponding reference files.</span></span> <span data-ttu-id="86968-132">Ausführliche Informationen finden Sie in der API-Dokumentation zu [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span><span class="sxs-lookup"><span data-stu-id="86968-132">See the API documentation on [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for specific details.</span></span>

## <a name="see-also"></a><span data-ttu-id="86968-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="86968-133">See also</span></span>
<span data-ttu-id="86968-134">[Ablaufverfolgungssimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) für Quantencomputer: C#-Referenz</span><span class="sxs-lookup"><span data-stu-id="86968-134">The quantum computer [trace simulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# reference</span></span> 

