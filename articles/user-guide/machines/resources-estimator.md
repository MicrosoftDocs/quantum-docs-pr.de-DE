---
title: Quantum-Ressourcenschätzung-Quantum Development Kit
description: 'Erfahren Sie mehr über die Ressourcenschätzung von Microsoft QDK, die die Ressourcen schätzt, die zum Ausführen einer bestimmten Instanz eines Q #-Vorgangs auf einem Quantum-Computer erforderlich sind.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 0909a050e89d6295664e54ab63cfda5d407a8f12
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870537"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="43499-103">Ressourcenschätzung für das Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="43499-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="43499-104">Wie der Name schon sagt, `ResourcesEstimator` schätzt die-Klasse die Ressourcen, die erforderlich sind, um eine bestimmte Instanz eines Q #-Vorgangs auf einem Quantum-Computer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43499-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="43499-105">Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund werden Ressourcen für Q #-Vorgänge geschätzt, bei denen Tausende von Qubits verwendet werden, vorausgesetzt, dass der klassische Teil des Codes in angemessener Zeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43499-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="43499-106">Die Ressourcenschätzung basiert auf dem Quantum-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), der einen umfassenderen Satz an Metriken und Tools bereitstellt, um das Debuggen von f #-Programmen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="43499-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="43499-107">Aufrufen und Ausführen der Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="43499-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="43499-108">Sie können die Ressourcenschätzung verwenden, um einen beliebigen Q #-Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="43499-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="43499-109">Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q #-Programms](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="43499-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="43499-110">Aufrufen der Ressourcenschätzung von C #</span><span class="sxs-lookup"><span data-stu-id="43499-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="43499-111">Wie bei anderen Ziel Computern erstellen Sie zunächst eine Instanz der `ResourceEstimator` -Klasse und übergeben Sie dann als ersten Parameter der-Methode eines Vorgangs `Run` .</span><span class="sxs-lookup"><span data-stu-id="43499-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="43499-112">Beachten Sie, dass die-Klasse im Gegensatz zur- `QuantumSimulator` Klasse `ResourceEstimator` die <xref:System.IDisposable> -Schnittstelle nicht implementiert, sodass Sie Sie nicht in eine-Anweisung einschließen müssen `using` .</span><span class="sxs-lookup"><span data-stu-id="43499-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

<span data-ttu-id="43499-113">Wie das Beispiel zeigt, `ResourcesEstimator` stellt die- `ToTSV()` Methode bereit, die eine Tabelle mit durch Tabstopps getrennten Werten (TSV) generiert.</span><span class="sxs-lookup"><span data-stu-id="43499-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="43499-114">Sie können die Tabelle in einer Datei speichern oder Sie zur Analyse in der Konsole anzeigen.</span><span class="sxs-lookup"><span data-stu-id="43499-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="43499-115">Im folgenden finden Sie eine Beispielausgabe des vorangehenden Programms:</span><span class="sxs-lookup"><span data-stu-id="43499-115">The following is a sample output from the preceding program:</span></span>

```output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> <span data-ttu-id="43499-116">Eine- `ResourcesEstimator` Instanz setzt ihre Berechnungen bei jedem Testlauf nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="43499-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="43499-117">Wenn Sie dieselbe-Instanz verwenden, um einen anderen Vorgang auszuführen, werden die neuen Ergebnisse mit den vorhandenen Ergebnissen aggregiert.</span><span class="sxs-lookup"><span data-stu-id="43499-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="43499-118">Wenn Sie Berechnungen zwischen den Ausführungen zurücksetzen müssen, erstellen Sie für jede Ausführung eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="43499-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="43499-119">Aufrufen der Ressourcenschätzung von python</span><span class="sxs-lookup"><span data-stu-id="43499-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="43499-120">Verwenden Sie die [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) -Methode aus der Python-Bibliothek mit dem importierten Q #-Vorgang:</span><span class="sxs-lookup"><span data-stu-id="43499-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="43499-121">Aufrufen der Ressourcenschätzung von der Befehlszeile aus</span><span class="sxs-lookup"><span data-stu-id="43499-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="43499-122">Wenn Sie ein Q #-Programm über die Befehlszeile ausführen, verwenden Sie den Parameter **--Simulator** (oder **-s** ), um den `ResourcesEstimator` Zielcomputer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="43499-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="43499-123">Der folgende Befehl führt ein Programm mit der Ressourcenschätzung aus:</span><span class="sxs-lookup"><span data-stu-id="43499-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="43499-124">Aufrufen der Ressourcenschätzung von juptyer Notebooks</span><span class="sxs-lookup"><span data-stu-id="43499-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="43499-125">Verwenden Sie zum Ausführen des Q #-Vorgangs den IQ # Magic-Befehl [% Schätzung](xref:microsoft.quantum.iqsharp.magic-ref.simulate) .</span><span class="sxs-lookup"><span data-stu-id="43499-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="43499-126">Programm gesteuertes Abrufen der geschätzten Daten</span><span class="sxs-lookup"><span data-stu-id="43499-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="43499-127">Zusätzlich zu einer TSV-Tabelle können Sie die während der Durchführung geschätzten Ressourcen Programm gesteuert über die- `Data` Eigenschaft der Ressourcenschätzung abrufen.</span><span class="sxs-lookup"><span data-stu-id="43499-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="43499-128">Die `Data` -Eigenschaft stellt eine `System.DataTable` -Instanz mit zwei Spalten bereit: `Metric` und `Sum` , indiziert nach den Namen der Metriken.</span><span class="sxs-lookup"><span data-stu-id="43499-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="43499-129">Der folgende Code zeigt, wie die Gesamtanzahl von `QubitClifford` `T` -und- `CNOT` Vorgängen, die von einem f #-Vorgang verwendet werden, abgerufen und gedruckt werden:</span><span class="sxs-lookup"><span data-stu-id="43499-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a><span data-ttu-id="43499-130">Gemeldete Metriken</span><span class="sxs-lookup"><span data-stu-id="43499-130">Metrics Reported</span></span>

<span data-ttu-id="43499-131">Die Ressourcenschätzung verfolgt die folgenden Metriken:</span><span class="sxs-lookup"><span data-stu-id="43499-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="43499-132">Metrik</span><span class="sxs-lookup"><span data-stu-id="43499-132">Metric</span></span>|<span data-ttu-id="43499-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43499-133">Description</span></span>|
|----|----|
|<span data-ttu-id="43499-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="43499-134">__CNOT__</span></span>    |<span data-ttu-id="43499-135">Die Ausführung von `CNOT` Vorgängen (auch als kontrollierte Pauli X-Vorgänge bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="43499-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="43499-136">__Qubitclifford__</span><span class="sxs-lookup"><span data-stu-id="43499-136">__QubitClifford__</span></span> |<span data-ttu-id="43499-137">Die Testlauf-Anzahl einzelner Qubit Clifford-und Pauli-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="43499-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="43499-138">__Measure__</span><span class="sxs-lookup"><span data-stu-id="43499-138">__Measure__</span></span>    |<span data-ttu-id="43499-139">Die Testlauf-Anzahl von Messungen.</span><span class="sxs-lookup"><span data-stu-id="43499-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="43499-140">__R__</span><span class="sxs-lookup"><span data-stu-id="43499-140">__R__</span></span>    |<span data-ttu-id="43499-141">Die Anzahl der Testlauf mit einzelnen Qubit-Drehungen, ausgenommen `T` , Clifford-und Pauli-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="43499-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="43499-142">__T__</span><span class="sxs-lookup"><span data-stu-id="43499-142">__T__</span></span>    |<span data-ttu-id="43499-143">Die Anzahl der `T` Vorgänge und ihre konjutoren, einschließlich der `T` Vorgänge, T_x = h. T. h und T_y = HY. T. HY.</span><span class="sxs-lookup"><span data-stu-id="43499-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="43499-144">__Tiefe__</span><span class="sxs-lookup"><span data-stu-id="43499-144">__Depth__</span></span>|<span data-ttu-id="43499-145">Die untere Grenze für die Tiefe der vom Q #-Vorgang durchgeführten Quantum-Leitung.</span><span class="sxs-lookup"><span data-stu-id="43499-145">The lower bound for the depth of the quantum circuit run by the Q# operation.</span></span> <span data-ttu-id="43499-146">Standardmäßig zählt die Tiefe Metrik nur `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="43499-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="43499-147">Weitere Informationen finden Sie unter [tiefen Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span><span class="sxs-lookup"><span data-stu-id="43499-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="43499-148">__Width__</span><span class="sxs-lookup"><span data-stu-id="43499-148">__Width__</span></span>    |<span data-ttu-id="43499-149">Die untere Grenze für die maximale Anzahl von Qubits, die während der Ausführung des Q #-Vorgangs zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="43499-149">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="43499-150">Möglicherweise ist es nicht möglich, sowohl __Tiefe__ als auch __Breite__ Untergrenzen gleichzeitig zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="43499-150">It might not be possible to achieve both __Depth__ and __Width__ lower bounds simultaneously.</span></span>  |
|<span data-ttu-id="43499-151">__Borrowedwidth__</span><span class="sxs-lookup"><span data-stu-id="43499-151">__BorrowedWidth__</span></span>    |<span data-ttu-id="43499-152">Die maximale Anzahl der im Q #-Vorgang geliehenen Qubits.</span><span class="sxs-lookup"><span data-stu-id="43499-152">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="43499-153">Bereitstellen der Wahrscheinlichkeit von Messergebnissen</span><span class="sxs-lookup"><span data-stu-id="43499-153">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="43499-154">Sie können <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> aus dem- <xref:microsoft.quantum.diagnostics> Namespace verwenden, um Informationen über die erwartete Wahrscheinlichkeit eines Messvorgangs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="43499-154">You can use <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> from the <xref:microsoft.quantum.diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="43499-155">Weitere Informationen finden Sie unter [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span><span class="sxs-lookup"><span data-stu-id="43499-155">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="43499-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="43499-156">See also</span></span>

- [<span data-ttu-id="43499-157">Quantum-Ablauf Verfolgungs Simulator</span><span class="sxs-lookup"><span data-stu-id="43499-157">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="43499-158">Quantum-zu-ffoli-Simulator</span><span class="sxs-lookup"><span data-stu-id="43499-158">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="43499-159">Quantum-vollständiger Zustands Simulator</span><span class="sxs-lookup"><span data-stu-id="43499-159">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 