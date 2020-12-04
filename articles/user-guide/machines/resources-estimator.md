---
title: Quantum-Ressourcenschätzung-Quantum Development Kit
description: Erfahren Sie mehr über die Ressourcenschätzung von Microsoft QDK, die die Ressourcen schätzt, die zum Ausführen einer bestimmten Instanz eines Q# Vorgangs auf einem Quantum-Computer erforderlich sind.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: de425c2d91c6528b13c3bedd81acb4b4273ed711
ms.sourcegitcommit: 7c687495a79d75ae9e029e5a41baec84d9e07bb0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/04/2020
ms.locfileid: "96604642"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="a6c47-103">Ressourcenschätzung für das Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="a6c47-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="a6c47-104">Wie der Name schon sagt, `ResourcesEstimator` schätzt die-Klasse die Ressourcen, die erforderlich sind, um eine bestimmte Instanz eines- Q# Vorgangs auf einem Quantum-Computer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="a6c47-105">Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund werden Ressourcen für Vorgänge geschätzt, bei Q# denen Tausende von Qubits verwendet werden, vorausgesetzt, dass der klassische Teil des Codes in angemessener Zeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6c47-105">It accomplishes this by running the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="a6c47-106">Die Ressourcenschätzung basiert auf dem Quantum-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), der einen umfassenderen Satz an Metriken und Tools bereitstellt, um das Debuggen von Programmen zu erleichtern Q# .</span><span class="sxs-lookup"><span data-stu-id="a6c47-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="a6c47-107">Aufrufen und Ausführen der Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="a6c47-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="a6c47-108">Sie können den Ressourcen Schätz verwenden, um jeden Q# Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="a6c47-109">Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q# Programms](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="a6c47-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="a6c47-110">Aufrufen der Ressourcenschätzung von C #</span><span class="sxs-lookup"><span data-stu-id="a6c47-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="a6c47-111">Wie bei anderen Zielcomputern auch, erstellen Sie zuerst eine Instanz der Klasse `ResourcesEstimator` und übergeben sie anschließend als ersten Parameter der `Run`-Methode einer Operation.</span><span class="sxs-lookup"><span data-stu-id="a6c47-111">As with other target machines, you first create an instance of the `ResourcesEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="a6c47-112">Beachten Sie hierbei Folgendes: Im Gegensatz zur Klasse `QuantumSimulator` wird mit der Klasse `ResourcesEstimator` nicht die <xref:System.IDisposable>-Schnittstelle implementiert, sodass Sie sie nicht in eine `using`-Anweisung einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-112">Note that, unlike the `QuantumSimulator` class, the `ResourcesEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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

<span data-ttu-id="a6c47-113">Wie das Beispiel zeigt, `ResourcesEstimator` stellt die- `ToTSV()` Methode bereit, die eine Tabelle mit durch Tabstopps getrennten Werten (TSV) generiert.</span><span class="sxs-lookup"><span data-stu-id="a6c47-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="a6c47-114">Sie können die Tabelle in einer Datei speichern oder Sie zur Analyse in der Konsole anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="a6c47-115">Im folgenden finden Sie eine Beispielausgabe des vorangehenden Programms:</span><span class="sxs-lookup"><span data-stu-id="a6c47-115">The following is a sample output from the preceding program:</span></span>

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
> <span data-ttu-id="a6c47-116">Eine- `ResourcesEstimator` Instanz setzt ihre Berechnungen bei jedem Testlauf nicht zurück.</span><span class="sxs-lookup"><span data-stu-id="a6c47-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="a6c47-117">Wenn Sie dieselbe-Instanz verwenden, um einen anderen Vorgang auszuführen, werden die neuen Ergebnisse mit den vorhandenen Ergebnissen aggregiert.</span><span class="sxs-lookup"><span data-stu-id="a6c47-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="a6c47-118">Wenn Sie Berechnungen zwischen den Ausführungen zurücksetzen müssen, erstellen Sie für jede Ausführung eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="a6c47-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="a6c47-119">Aufrufen der Ressourcenschätzung von python</span><span class="sxs-lookup"><span data-stu-id="a6c47-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="a6c47-120">Verwenden Sie die [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) -Methode aus der Python-Bibliothek mit dem importierten Q# Vorgang:</span><span class="sxs-lookup"><span data-stu-id="a6c47-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="a6c47-121">Aufrufen der Ressourcenschätzung von der Befehlszeile aus</span><span class="sxs-lookup"><span data-stu-id="a6c47-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="a6c47-122">Wenn Sie ein Q# Programm über die Befehlszeile ausführen, verwenden Sie den Parameter **--Simulator** (oder **-s** ), um den `ResourcesEstimator` Zielcomputer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a6c47-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="a6c47-123">Der folgende Befehl führt ein Programm mit der Ressourcenschätzung aus:</span><span class="sxs-lookup"><span data-stu-id="a6c47-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="a6c47-124">Aufrufen der Ressourcenschätzung von juptyer Notebooks</span><span class="sxs-lookup"><span data-stu-id="a6c47-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="a6c47-125">Verwenden Sie den I Q# Magic-Befehl " [% schätzkraft](xref:microsoft.quantum.iqsharp.magic-ref.simulate) ", um den Q# Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="a6c47-126">Programm gesteuertes Abrufen der geschätzten Daten</span><span class="sxs-lookup"><span data-stu-id="a6c47-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="a6c47-127">Zusätzlich zu einer TSV-Tabelle können Sie die während der Durchführung geschätzten Ressourcen Programm gesteuert über die- `Data` Eigenschaft der Ressourcenschätzung abrufen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="a6c47-128">Die `Data` -Eigenschaft stellt eine `System.DataTable` -Instanz mit zwei Spalten bereit: `Metric` und `Sum` , indiziert nach den Namen der Metriken.</span><span class="sxs-lookup"><span data-stu-id="a6c47-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="a6c47-129">Der folgende Code zeigt, wie die Gesamtanzahl von `QubitClifford` `T` -und- `CNOT` Vorgängen, die von einem-Vorgang verwendet werden, abgerufen und gedruckt werden Q# :</span><span class="sxs-lookup"><span data-stu-id="a6c47-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="a6c47-130">Gemeldete Metriken</span><span class="sxs-lookup"><span data-stu-id="a6c47-130">Metrics Reported</span></span>

<span data-ttu-id="a6c47-131">Die Ressourcenschätzung verfolgt die folgenden Metriken:</span><span class="sxs-lookup"><span data-stu-id="a6c47-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="a6c47-132">Metrik</span><span class="sxs-lookup"><span data-stu-id="a6c47-132">Metric</span></span>|<span data-ttu-id="a6c47-133">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6c47-133">Description</span></span>|
|----|----|
|<span data-ttu-id="a6c47-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="a6c47-134">__CNOT__</span></span>    |<span data-ttu-id="a6c47-135">Die Ausführung von `CNOT` Vorgängen (auch als kontrollierte Pauli X-Vorgänge bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="a6c47-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="a6c47-136">__Qubitclifford__</span><span class="sxs-lookup"><span data-stu-id="a6c47-136">__QubitClifford__</span></span> |<span data-ttu-id="a6c47-137">Die Testlauf-Anzahl einzelner Qubit Clifford-und Pauli-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a6c47-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="a6c47-138">__Measure__</span><span class="sxs-lookup"><span data-stu-id="a6c47-138">__Measure__</span></span>    |<span data-ttu-id="a6c47-139">Die Testlauf-Anzahl von Messungen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="a6c47-140">__R__</span><span class="sxs-lookup"><span data-stu-id="a6c47-140">__R__</span></span>    |<span data-ttu-id="a6c47-141">Die Anzahl der Testlauf mit einzelnen Qubit-Drehungen, ausgenommen `T` , Clifford-und Pauli-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a6c47-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="a6c47-142">__T__</span><span class="sxs-lookup"><span data-stu-id="a6c47-142">__T__</span></span>    |<span data-ttu-id="a6c47-143">Die Anzahl der `T` Vorgänge und ihre konjutoren, einschließlich der `T` Vorgänge, T_x = h. T. h und T_y = HY. T. HY.</span><span class="sxs-lookup"><span data-stu-id="a6c47-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="a6c47-144">__Tiefe__</span><span class="sxs-lookup"><span data-stu-id="a6c47-144">__Depth__</span></span>|<span data-ttu-id="a6c47-145">Die Tiefe der vom Vorgang durchgeführten Quantum-Verbindung Q# (siehe [unten](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="a6c47-145">Depth of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="a6c47-146">Standardmäßig zählt die Tiefe Metrik nur `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="a6c47-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="a6c47-147">Weitere Informationen finden Sie unter [tiefen Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span><span class="sxs-lookup"><span data-stu-id="a6c47-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="a6c47-148">__Width__</span><span class="sxs-lookup"><span data-stu-id="a6c47-148">__Width__</span></span>|<span data-ttu-id="a6c47-149">Breite der vom Vorgang durchgeführten quantumleitung Q# (siehe [unten](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="a6c47-149">Width of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="a6c47-150">Standardmäßig zählt die Tiefe Metrik nur `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="a6c47-150">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="a6c47-151">Weitere Informationen finden Sie unter [Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="a6c47-151">For more details, see [Width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span></span>   |
|<span data-ttu-id="a6c47-152">__Qubitcount__</span><span class="sxs-lookup"><span data-stu-id="a6c47-152">__QubitCount__</span></span>    |<span data-ttu-id="a6c47-153">Die untere Grenze für die maximale Anzahl von Qubits, die während der Ausführung des Q# Vorgangs zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="a6c47-153">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="a6c47-154">Diese Metrik ist möglicherweise nicht mit der __Tiefe__ kompatibel (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="a6c47-154">This metric might not be compatible with __Depth__ (see below).</span></span>  |
|<span data-ttu-id="a6c47-155">__Borrowedwidth__</span><span class="sxs-lookup"><span data-stu-id="a6c47-155">__BorrowedWidth__</span></span>    |<span data-ttu-id="a6c47-156">Die maximale Anzahl der im Vorgang geliehenen Qubits Q# .</span><span class="sxs-lookup"><span data-stu-id="a6c47-156">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |


## <a name="depth-width-and-qubitcount"></a><span data-ttu-id="a6c47-157">Tiefe, Breite und qubitcount</span><span class="sxs-lookup"><span data-stu-id="a6c47-157">Depth, Width, and QubitCount</span></span>

<span data-ttu-id="a6c47-158">Die gemeldeten tiefen und breiten Schätzungen sind miteinander kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a6c47-158">Reported Depth and Width estimates are compatible with each other.</span></span>
<span data-ttu-id="a6c47-159">(Bisher waren beide Zahlen erreichbar, aber für Tiefe und Breite sind unterschiedliche Verbindungen erforderlich.) Derzeit können beide Metriken in diesem Paar gleichzeitig von derselben Verbindung erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="a6c47-159">(Previously both numbers were achievable, but different circuits would be required for Depth and for Width.) Currently both metrics in this pair can be achieved by the same circuit at the same time.</span></span>

<span data-ttu-id="a6c47-160">Folgende Metriken werden gemeldet:</span><span class="sxs-lookup"><span data-stu-id="a6c47-160">The following metrics are reported:</span></span>

<span data-ttu-id="a6c47-161">__Tiefe:__ Für den Stamm Vorgang, der für die Ausführung benötigt wird, wobei bestimmte Gate-Zeiten angenommen werden.</span><span class="sxs-lookup"><span data-stu-id="a6c47-161">__Depth:__ For the root operation - time it takes to execute it assuming specific gate times.</span></span>
<span data-ttu-id="a6c47-162">Für Vorgänge namens oder nachfolgende Vorgänge: Zeitunterschied zwischen der aktuellen Qubit-Verfügbarkeits Zeit am Anfang und am Ende des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a6c47-162">For operations called or subsequent operations - time difference between latest qubit availability time at the beginning and the end of the operation.</span></span>

<span data-ttu-id="a6c47-163">__Breite:__ Für den Stamm Vorgang: die Anzahl von Qubits, die tatsächlich verwendet wurden, um Sie auszuführen (und der Vorgang, den Sie aufruft).</span><span class="sxs-lookup"><span data-stu-id="a6c47-163">__Width:__ For the root operation - number of qubits actually used to execute it (and operation it calls).</span></span>
<span data-ttu-id="a6c47-164">Für Vorgänge mit dem Namen oder nachfolgende Vorgänge: wie viele weitere Qubits wurden zusätzlich zu den Qubits verwendet, die bereits am Anfang des Vorgangs verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="a6c47-164">For operations called or subsequent operations - how many more qubits were used in addition to the qubits already used at the beginning of the operation.</span></span>

<span data-ttu-id="a6c47-165">Beachten Sie, dass wiederverwendete Qubits nicht zu dieser Zahl beitragen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-165">Please note, that reused qubits do not contribute to this number.</span></span>
<span data-ttu-id="a6c47-166">Wenn beispielsweise einige Qubits freigegeben wurden, bevor der Vorgang a startet, und alle von diesem Vorgang angeforderten Qubit (und Vorgänge, die von einem aufgerufen wurden) durch wieder verwenden von zuvor releasequbits erfüllt wurden, wird die Breite des Vorgangs a als 0 (null) gemeldet.</span><span class="sxs-lookup"><span data-stu-id="a6c47-166">I.e. if a few qubits have been released before operation A starts, and all qubit demanded by this operation A (and operations called from A) were satisfied by reusing previously release qubits, the Width of operation A is reported as 0.</span></span> <span data-ttu-id="a6c47-167">Erfolgreich geliehene Qubits tragen nicht an die Breite an.</span><span class="sxs-lookup"><span data-stu-id="a6c47-167">Successfully borrowed qubits do not contribute to the Width either.</span></span>

<span data-ttu-id="a6c47-168">__Qubitcount:__ Für den Stamm Vorgang: minimale Anzahl von Qubits, die ausreichen, um diesen Vorgang auszuführen (und von ihm aufgerufene Vorgänge).</span><span class="sxs-lookup"><span data-stu-id="a6c47-168">__QubitCount:__ For the root operation - minimum number of qubits that would be sufficient to execute this operation (and operations called from it).</span></span>
<span data-ttu-id="a6c47-169">Für Vorgänge mit dem Namen oder nachfolgende Vorgänge: minimale Anzahl von Qubits, die ausreichen, um diesen Vorgang separat auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-169">For operations called or subsequent operations - minimum number of qubits that would be sufficient to execute this operation separately.</span></span> <span data-ttu-id="a6c47-170">Diese Zahl enthält keine Eingabe-Qubits.</span><span class="sxs-lookup"><span data-stu-id="a6c47-170">This number doesn't include input qubits.</span></span> <span data-ttu-id="a6c47-171">Sie enthält auch geliehene Qubits.</span><span class="sxs-lookup"><span data-stu-id="a6c47-171">It does include borrowed qubits.</span></span>

<span data-ttu-id="a6c47-172">Zwei Betriebsmodi werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6c47-172">Two modes of operation are supported.</span></span> <span data-ttu-id="a6c47-173">Der Modus wird ausgewählt, indem qctracesimulatorconfiguration. optimizetiefe festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a6c47-173">Mode is selected by setting QCTraceSimulatorConfiguration.OptimizeDepth.</span></span>

<span data-ttu-id="a6c47-174">__Optimizetiefe = true:__ Bei qubitmanager wird von der Qubit-Wiederverwendung abgeraten, und jedes Mal, wenn ein Qubit angefordert wird, wird ein neues Qubit zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-174">__OptimizeDepth=true:__ QubitManager is discouraged from qubit reuse and allocates new qubit every time it is asked for a qubit.</span></span> <span data-ttu-id="a6c47-175">Die __Tiefe__ des Stamm Vorgangs wird zur minimalen Tiefe (untere Grenze).</span><span class="sxs-lookup"><span data-stu-id="a6c47-175">For the root operation __Depth__ becomes the minimum depth (lower bound).</span></span> <span data-ttu-id="a6c47-176">Für diese Tiefe wird eine kompatible __Breite__ gemeldet (beide können gleichzeitig erreicht werden).</span><span class="sxs-lookup"><span data-stu-id="a6c47-176">Compatible __Width__ is reported for this depth (both can be achieved at the same time).</span></span> <span data-ttu-id="a6c47-177">Beachten Sie, dass diese Breite bei dieser Tiefe wahrscheinlich nicht optimal ist.</span><span class="sxs-lookup"><span data-stu-id="a6c47-177">Note, that this width will likely be not optimal given this depth.</span></span> <span data-ttu-id="a6c47-178">" __Qubitcount__ " ist möglicherweise niedriger als die Breite für den Stamm Vorgang, da die Wiederverwendung vorausgesetzt wird</span><span class="sxs-lookup"><span data-stu-id="a6c47-178">__QubitCount__ may be lower than Width for the root operation because it assumes reuse.</span></span>

<span data-ttu-id="a6c47-179">__Optimizetiefe = false:__ Qubitmanager wird empfohlen, Qubits wiederzuverwenden und veröffentlichte Qubits wiederzuverwenden, bevor neue zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="a6c47-179">__OptimizeDepth=false:__ QubitManager is encouraged to reuse qubits and will reuse released qubits before allocating new ones.</span></span> <span data-ttu-id="a6c47-180">Die __Breite__ des Stamm Vorgangs wird zur minimalen Breite (untere Grenze).</span><span class="sxs-lookup"><span data-stu-id="a6c47-180">For the root operation __Width__ becomes the minimal width (lower bound).</span></span> <span data-ttu-id="a6c47-181">Es wird eine kompatible __Tiefe__ gemeldet, für die Sie erreicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="a6c47-181">Compatible __Depth__ is reported on which it can be achieved.</span></span> <span data-ttu-id="a6c47-182">__Qubitcount__ ist die gleiche wie die __Breite__ für den Stamm Vorgang, vorausgesetzt, dass keine Kreditaufnahme erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a6c47-182">__QubitCount__ will be the same as __Width__ for the root operation assuming no borrowing.</span></span>

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="a6c47-183">Angeben der Wahrscheinlichkeit von Messergebnissen</span><span class="sxs-lookup"><span data-stu-id="a6c47-183">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="a6c47-184">Sie können <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> aus dem- <xref:Microsoft.Quantum.Diagnostics> Namespace verwenden, um Informationen über die erwartete Wahrscheinlichkeit eines Messvorgangs bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6c47-184">You can use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> from the <xref:Microsoft.Quantum.Diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="a6c47-185">Weitere Informationen finden Sie unter [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span><span class="sxs-lookup"><span data-stu-id="a6c47-185">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="a6c47-186">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a6c47-186">See also</span></span>

- [<span data-ttu-id="a6c47-187">Quantum-Ablauf Verfolgungs Simulator</span><span class="sxs-lookup"><span data-stu-id="a6c47-187">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="a6c47-188">Toffoli-Simulator für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="a6c47-188">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="a6c47-189">Simulator für den vollständigen Zustand für Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="a6c47-189">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 
