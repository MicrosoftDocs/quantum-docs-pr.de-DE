---
title: 'Ablaufverfolgungssimulator für Quantencomputer: Quantum Development Kit'
description: Es wird beschrieben, wie Sie den Microsoft-Ablaufverfolgungssimulator für Quantencomputer verwenden, um klassischen Code zu debuggen und die Ressourcenanforderungen eines Q#-Programms zu schätzen.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: c01f01973ea08153cbfa35d87a588a4eae46f1b7
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871109"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a><span data-ttu-id="8a462-103">Microsoft Quantum Development Kit (QDK): Ablaufverfolgungssimulator für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8a462-103">Microsoft Quantum Development Kit (QDK) quantum trace simulator</span></span>

<span data-ttu-id="8a462-104">Mit der QDK-Klasse <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> wird ein Quantenprogramm ausgeführt, ohne den Zustand eines Quantencomputers tatsächlich zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="8a462-104">The QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> class runs a quantum program without actually simulating the state of a quantum computer.</span></span> <span data-ttu-id="8a462-105">Aus diesem Grund können mit dem Ablaufverfolgungssimulator für Quantencomputer Quantenprogramme ausgeführt werden, für die Tausende von Qubits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a462-105">For this reason, the quantum trace simulator is able to run quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="8a462-106">Dies ist für zwei Hauptaufgaben hilfreich:</span><span class="sxs-lookup"><span data-stu-id="8a462-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="8a462-107">Debuggen von klassischem Code, der Teil eines Quantenprogramms ist</span><span class="sxs-lookup"><span data-stu-id="8a462-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="8a462-108">Schätzen der Ressourcen, die zum Ausführen einer bestimmten Instanz eines Quantenprogramms auf einem Quantencomputer erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="8a462-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span> <span data-ttu-id="8a462-109">Die [Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator), die über eine stärker eingeschränkte Gruppe von Metriken verfügt, basiert beispielsweise auf dem Ablaufverfolgungssimulator.</span><span class="sxs-lookup"><span data-stu-id="8a462-109">In fact, the [Resources estimator](xref:microsoft.quantum.machines.resources-estimator), which provides a more limited set of metrics, is built upon the trace simulator.</span></span>

## <a name="invoking-the-quantum-trace-simulator"></a><span data-ttu-id="8a462-110">Aufrufen des Ablaufverfolgungssimulators für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8a462-110">Invoking the quantum trace simulator</span></span>

<span data-ttu-id="8a462-111">Sie können den Ablaufverfolgungssimulator für Quantencomputer nutzen, um beliebige Q#-Operationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8a462-111">You can use the quantum trace simulator to run any Q# operation.</span></span>

<span data-ttu-id="8a462-112">Wie bei anderen Zielcomputern auch, erstellen Sie zuerst eine Instanz der Klasse `QCTraceSimulator` und übergeben sie anschließend als ersten Parameter der `Run`-Methode einer Operation.</span><span class="sxs-lookup"><span data-stu-id="8a462-112">As with other target machines, you first create an instance of the `QCTraceSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="8a462-113">Beachten Sie hierbei Folgendes: Im Gegensatz zur Klasse `QuantumSimulator` wird mit der Klasse `QCTraceSimulator` nicht die <xref:System.IDisposable>-Schnittstelle implementiert, sodass Sie sie nicht in eine `using`-Anweisung einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="8a462-113">Note that, unlike the `QuantumSimulator` class, the `QCTraceSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="8a462-114">Angeben der Wahrscheinlichkeit von Messergebnissen</span><span class="sxs-lookup"><span data-stu-id="8a462-114">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="8a462-115">Da vom Ablaufverfolgungssimulator für Quantencomputer der tatsächliche Quantenzustand nicht simuliert wird, kann die Wahrscheinlichkeit von Messergebnissen für eine Operation nicht berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8a462-115">Because the quantum trace simulator does not simulate the actual quantum state, it cannot calculate the probability of measurement outcomes within an operation.</span></span> 

<span data-ttu-id="8a462-116">Falls eine Operation Messungen enthält, müssen Sie diese Wahrscheinlichkeiten daher explizit angeben, indem Sie die Operation <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> aus dem Namespace <xref:microsoft.quantum.diagnostics> verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a462-116">Therefore, if an operation includes measurements, you must explicitly provide these probabilities using the <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> operation from the <xref:microsoft.quantum.diagnostics> namespace.</span></span> <span data-ttu-id="8a462-117">Das folgende Beispiel veranschaulicht dies:</span><span class="sxs-lookup"><span data-stu-id="8a462-117">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="8a462-118">Wenn vom Ablaufverfolgungssimulator für Quantencomputer das Element `AssertMeasurementProbability` erkannt wird, zeichnet er auf, dass die Messung von `PauliZ` auf `source` und `q` zum Ergebnis `Zero` mit einer Wahrscheinlichkeit von **0,5** führen sollte.</span><span class="sxs-lookup"><span data-stu-id="8a462-118">When the quantum trace simulator encounters `AssertMeasurementProbability` it records that measuring `PauliZ` on `source` and `q` should give an outcome of `Zero`, with probability **0.5**.</span></span> <span data-ttu-id="8a462-119">Später beim Ausführen der Operation `M` werden dann die aufgezeichneten Werte für die Ergebniswahrscheinlichkeiten erkannt, und für `M` wird `Zero` oder `One` mit der Wahrscheinlichkeit **0,5** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a462-119">When it runs the `M` operation later, it finds the recorded values of the outcome probabilities, and `M` returns `Zero` or `One`, with probability **0.5**.</span></span> <span data-ttu-id="8a462-120">Wenn derselbe Code in einem Simulator ausgeführt wird, mit dem der Quantenzustand nachverfolgt wird, überprüft dieser die Wahrscheinlichkeiten in `AssertMeasurementProbability` auf ihre Richtigkeit.</span><span class="sxs-lookup"><span data-stu-id="8a462-120">When the same code runs on a simulator that keeps track of the quantum state, that simulator checks that the provided probabilities in `AssertMeasurementProbability` are correct.</span></span>

<span data-ttu-id="8a462-121">Beachten Sie Folgendes: Wenn mindestens eine Messoperation nicht über `AssertMeasurementProbability` mit Anmerkungen versehen wurde, wird vom Simulator [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception) ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8a462-121">Note that if there is at least one measurement operation that is not annotated using `AssertMeasurementProbability`, the simulator throws an [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span></span>

## <a name="quantum-trace-simulator-tools"></a><span data-ttu-id="8a462-122">Tools für den Ablaufverfolgungssimulator für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8a462-122">Quantum trace simulator tools</span></span>

<span data-ttu-id="8a462-123">Das QDK enthält fünf Tools, die Sie mit einem Ablaufverfolgungssimulator für Quantencomputer nutzen können, um Fehler in Ihren Programmen zu erkennen und Ressourcenschätzungen für Quantenprogramme durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="8a462-123">The QDK includes five tools that you can use with the quantum trace simulator to detect bugs in your programs and perform quantum program resource estimates:</span></span> 

|<span data-ttu-id="8a462-124">Tool</span><span class="sxs-lookup"><span data-stu-id="8a462-124">Tool</span></span> | <span data-ttu-id="8a462-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a462-125">Description</span></span> |
|-----| -----|
|[<span data-ttu-id="8a462-126">Überprüfung auf eindeutige Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a462-126">Distinct inputs checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |<span data-ttu-id="8a462-127">Dient zum Durchführen einer Überprüfung auf potenzielle Konflikte mit freigegebenen Qubits.</span><span class="sxs-lookup"><span data-stu-id="8a462-127">Checks for potential conflicts with shared qubits</span></span> |
|[<span data-ttu-id="8a462-128">Überprüfung auf Verwendung von ungültigen Qubits</span><span class="sxs-lookup"><span data-stu-id="8a462-128">Invalidated qubits use checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |<span data-ttu-id="8a462-129">Dient zum Durchführen einer Überprüfung, ob eine Operation vom Programm auf ein bereits freigegebenes Qubit angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a462-129">Checks if the program applies an operation to a qubit that is already released</span></span> |
|[<span data-ttu-id="8a462-130">Indikator für primitive Vorgänge</span><span class="sxs-lookup"><span data-stu-id="8a462-130">Primitive operations counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | <span data-ttu-id="8a462-131">Dient zum Ermitteln der Anzahl von Primitivenausführungen in allen Operationen, die in einem Quantenprogramm aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8a462-131">Counts the number of primitive executions used by every operation invoked in a quantum program</span></span>  |
|[<span data-ttu-id="8a462-132">Tiefenindikator</span><span class="sxs-lookup"><span data-stu-id="8a462-132">Depth counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |<span data-ttu-id="8a462-133">Dient zum Erfassen der jeweiligen Anzahl für die Untergrenze der Tiefe aller Operationen, die in einem Quantenprogramm ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="8a462-133">Gathers counts that represent the lower bound of the depth of every operation invoked in a quantum program</span></span>   |
|[<span data-ttu-id="8a462-134">Breitenindikator</span><span class="sxs-lookup"><span data-stu-id="8a462-134">Width counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |<span data-ttu-id="8a462-135">Dient zum Zählen der Qubits, die von den einzelnen Operationen eines Quantenprogramms zugeordnet und geliehen werden.</span><span class="sxs-lookup"><span data-stu-id="8a462-135">Counts the number of qubits allocated and borrowed by each operation in a quantum program</span></span> |

<span data-ttu-id="8a462-136">Diese Tools werden jeweils aktiviert, indem in `QCTraceSimulatorConfiguration` die entsprechenden Flags festgelegt und anschließend die Konfiguration an die `QCTraceSimulator`-Deklaration übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8a462-136">Each of these tools is enabled by setting appropriate flags in `QCTraceSimulatorConfiguration` and then passing the configuration to the `QCTraceSimulator` declaration.</span></span> <span data-ttu-id="8a462-137">Informationen zur Verwendung dieser Tools finden Sie unter den Links in der obigen Liste.</span><span class="sxs-lookup"><span data-stu-id="8a462-137">For information on using each of these tools, see the links in the preceding list.</span></span> <span data-ttu-id="8a462-138">Weitere Informationen zum Konfigurieren von `QCTraceSimulator` finden Sie unter [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span><span class="sxs-lookup"><span data-stu-id="8a462-138">For more information about configuring `QCTraceSimulator`, see [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span></span>

## <a name="qctracesimulator-methods"></a><span data-ttu-id="8a462-139">QCTraceSimulator-Methoden</span><span class="sxs-lookup"><span data-stu-id="8a462-139">QCTraceSimulator methods</span></span>

<span data-ttu-id="8a462-140">`QCTraceSimulator` verfügt über mehrere integrierte Methoden, um die Werte der Metriken abzurufen, die während einer Quantenoperation nachverfolgt werden.</span><span class="sxs-lookup"><span data-stu-id="8a462-140">`QCTraceSimulator` has several built-in methods to retrieve the values of the metrics tracked during a quantum operation.</span></span> <span data-ttu-id="8a462-141">Beispiele für die Methoden [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) und [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) finden Sie in den Artikeln zu den Tools [Indikator für primitive Vorgänge](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Tiefenindikator](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) und [Breitenindikator](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="8a462-141">Examples of the [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) and the [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) methods can be found in the [Primitive operations counter](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter), and [Width counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) articles.</span></span> <span data-ttu-id="8a462-142">Weitere Informationen zu allen verfügbaren Methoden finden Sie in der Q#-API-Referenz unter [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator).</span><span class="sxs-lookup"><span data-stu-id="8a462-142">For more information on all available methods, see [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in the Q# API reference.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8a462-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8a462-143">See also</span></span>

- [<span data-ttu-id="8a462-144">Ressourcenschätzung für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8a462-144">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="8a462-145">Toffoli-Simulator für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8a462-145">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="8a462-146">Simulator für den vollständigen Zustand für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8a462-146">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 