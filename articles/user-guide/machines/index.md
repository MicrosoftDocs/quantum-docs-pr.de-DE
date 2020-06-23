---
title: Quantensimulatoren und Hostanwendungen | Microsoft-Dokumentation
description: Es wird beschrieben, wie Sie Quantensimulatoren mit einer klassischen .NET-Computingsprache (normalerweise C# oder Q#) betreiben.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273524"
---
# <a name="quantum-simulators-and-host-applications"></a><span data-ttu-id="8ad6f-103">Quantensimulatoren und Hostanwendungen</span><span class="sxs-lookup"><span data-stu-id="8ad6f-103">Quantum simulators and host applications</span></span>

## <a name="what-youll-learn"></a><span data-ttu-id="8ad6f-104">Sie lernen Folgendes</span><span class="sxs-lookup"><span data-stu-id="8ad6f-104">What You'll Learn</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="8ad6f-105">Ausführen von Quantenalgorithmen</span><span class="sxs-lookup"><span data-stu-id="8ad6f-105">How quantum algorithms are executed</span></span>
> * <span data-ttu-id="8ad6f-106">Quantensimulatoren in diesem Release</span><span class="sxs-lookup"><span data-stu-id="8ad6f-106">What quantum simulators are included in this release</span></span>
> * <span data-ttu-id="8ad6f-107">Schreiben eines C#-Treibers für Ihren Quantenalgorithmus</span><span class="sxs-lookup"><span data-stu-id="8ad6f-107">How to write a C# driver for your quantum algorithm</span></span>

## <a name="the-quantum-development-kit-execution-model"></a><span data-ttu-id="8ad6f-108">Modell für die Quantum Development Kit-Ausführung</span><span class="sxs-lookup"><span data-stu-id="8ad6f-108">The Quantum Development Kit Execution Model</span></span>

<span data-ttu-id="8ad6f-109">Unter [Schreiben eines Quantenprogramms](xref:microsoft.quantum.write-program) haben wir unseren Quantenalgorithmus ausgeführt, indem wir ein `QuantumSimulator`-Objekt an die `Run`-Methode der Algorithmusklasse übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-109">In [Writing a quantum program](xref:microsoft.quantum.write-program), we executed our quantum algorithm by passing a `QuantumSimulator` object to the algorithm class's `Run` method.</span></span>
<span data-ttu-id="8ad6f-110">Die `QuantumSimulator`-Klasse führt den Quantenalgorithmus aus, indem der Quantenzustandsvektor vollständig simuliert wird. Dies ist der perfekte Ansatz für das Ausführen und Testen von `Teleport`.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-110">The `QuantumSimulator` class executes the quantum algorithm by fully simulating the quantum state vector, which is perfect for running and testing `Teleport`.</span></span>
<span data-ttu-id="8ad6f-111">Weitere Informationen zu Quantenzustandsvektoren finden Sie im [Leitfaden zu den Konzepten](xref:microsoft.quantum.concepts.intro).</span><span class="sxs-lookup"><span data-stu-id="8ad6f-111">See the [Concepts guide](xref:microsoft.quantum.concepts.intro) for more on quantum state vectors.</span></span>

<span data-ttu-id="8ad6f-112">Andere Zielcomputer können verwendet werden, um einen Quantenalgorithmus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-112">Other target machines may be used to run a quantum algorithm.</span></span>
<span data-ttu-id="8ad6f-113">Der Computer ist für das Bereitstellen der Implementierungen von Quantenprimitiven für den Algorithmus zuständig.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-113">The machine is responsible for providing implementations of quantum primitives for the algorithm.</span></span>
<span data-ttu-id="8ad6f-114">Dies gilt auch für primitive Vorgänge, z. B. H, CNOT und Measure, sowie für die Verwaltung und Nachverfolgung von Qubits.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-114">This includes primitive operations such as H, CNOT, and Measure, as well as qubit management and tracking.</span></span>
<span data-ttu-id="8ad6f-115">Verschiedene Klassen von Quantencomputern stehen für unterschiedliche Ausführungsmodelle desselben Quantenalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-115">Different classes of quantum machines represent different execution models for the same quantum algorithm.</span></span>

<span data-ttu-id="8ad6f-116">Mit jeder Art von Quantencomputer können unterschiedliche Implementierungen dieser Primitive bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-116">Each type of quantum machine may provide different implementations of these primitives.</span></span>
<span data-ttu-id="8ad6f-117">Mit dem Simulator für die Nachverfolgung von Quantencomputern, der im Development Kit enthalten ist, werden beispielsweise keine Simulationen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-117">For instance, the quantum computer trace simulator included in the development kit doesn't do any simulation at all.</span></span>
<span data-ttu-id="8ad6f-118">Stattdessen wird hiermit die Nutzung von Gates, Qubits und anderen Ressourcen für den Algorithmus nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-118">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machines"></a><span data-ttu-id="8ad6f-119">Quantencomputer</span><span class="sxs-lookup"><span data-stu-id="8ad6f-119">Quantum Machines</span></span>

<span data-ttu-id="8ad6f-120">Für die Zukunft ist die Definition weiterer Quantencomputerklassen geplant, um andere Arten von Simulationen und die Ausführung auf topologischen Quantencomputern zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-120">In the future, we will define additional quantum machine classes to support other types of simulation and to support execution on topological quantum computers.</span></span>
<span data-ttu-id="8ad6f-121">Indem der Algorithmus konstant gehalten wird, während die zugrunde liegende Computerimplementierung variiert, wird das Testen und Debuggen eines simulierten Algorithmus vereinfacht. Anschließend können Sie beim Ausführen auf echter Hardware sicher sein, dass sich der Algorithmus nicht geändert hat.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-121">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

### <a name="whats-included-in-this-release"></a><span data-ttu-id="8ad6f-122">Was ist in diesem Release enthalten?</span><span class="sxs-lookup"><span data-stu-id="8ad6f-122">What's Included in this Release</span></span>

<span data-ttu-id="8ad6f-123">Dieses Release des Quantum Developer Kit umfasst mehrere Quantencomputerklassen.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-123">This release of the quantum developer kit includes several quantum machine classes.</span></span>
<span data-ttu-id="8ad6f-124">Diese sind im Namespace `Microsoft.Quantum.Simulation.Simulators` definiert.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-124">All of them are defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

* <span data-ttu-id="8ad6f-125">Ein [umfassender Zustandsvektorsimulator](xref:microsoft.quantum.machines.full-state-simulator) (die `QuantumSimulator`-Klasse).</span><span class="sxs-lookup"><span data-stu-id="8ad6f-125">A [full state vector simulator](xref:microsoft.quantum.machines.full-state-simulator), the `QuantumSimulator` class.</span></span>
* <span data-ttu-id="8ad6f-126">Eine [einfache Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator) (die `ResourcesEstimator`-Klasse). Sie ermöglicht für die Ressourcen, die zum Ausführen eines Quantenalgorithmus benötigt werden, eine Analyse der Ressourcen auf oberster Ebene.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-126">A [simple resources estimator](xref:microsoft.quantum.machines.resources-estimator), the `ResourcesEstimator` class, it allows a top level analysis of the resources needed to run a quantum algorithm.</span></span>
* <span data-ttu-id="8ad6f-127">Eine [auf der Ablaufverfolgung basierende Ressourcenschätzung](xref:microsoft.quantum.machines.qc-trace-simulator.intro) (die `QCTraceSimulator`-Klasse). Sie ermöglicht eine erweiterte Analyse des Ressourcenverbrauchs für das gesamte Aufrufdiagramm des Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-127">A [trace-based resource estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), the `QCTraceSimulator` class, it allows advanced analysis of resources consumptions for the algorithm's entire call-graph.</span></span>
* <span data-ttu-id="8ad6f-128">Ein [Toffoli-Simulator](xref:microsoft.quantum.machines.toffoli-simulator) (die `ToffoliSimulator`-Klasse).</span><span class="sxs-lookup"><span data-stu-id="8ad6f-128">A [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator), the `ToffoliSimulator` class.</span></span>

## <a name="writing-a-host-application"></a><span data-ttu-id="8ad6f-129">Schreiben einer Hostanwendung</span><span class="sxs-lookup"><span data-stu-id="8ad6f-129">Writing a host application</span></span>

<span data-ttu-id="8ad6f-130">Unter [Schreiben eines Quantenprogramms](xref:microsoft.quantum.write-program) haben wir einen einfachen C#-Treiber für unseren Teleportalgorithmus geschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-130">In [Writing a quantum program](xref:microsoft.quantum.write-program), we wrote a simple C# driver for our teleport algorithm.</span></span> <span data-ttu-id="8ad6f-131">Ein C#-Treiber hat vier Hauptaufgaben:</span><span class="sxs-lookup"><span data-stu-id="8ad6f-131">A C# driver has 4 main purposes:</span></span>

* <span data-ttu-id="8ad6f-132">Erstellen des Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="8ad6f-132">Constructing the target machine</span></span>
* <span data-ttu-id="8ad6f-133">Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="8ad6f-133">Computing any arguments required for the quantum algorithm</span></span>
* <span data-ttu-id="8ad6f-134">Ausführen des Quantenalgorithmus mit dem Simulator</span><span class="sxs-lookup"><span data-stu-id="8ad6f-134">Running the quantum algorithm using the simulator</span></span>
* <span data-ttu-id="8ad6f-135">Verarbeiten des Vorgangsergebnisses</span><span class="sxs-lookup"><span data-stu-id="8ad6f-135">Processing the result of the operation</span></span>

<span data-ttu-id="8ad6f-136">Hier werden die einzelnen Schritte ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-136">Here we'll discuss each step in more detail.</span></span>

### <a name="constructing-the-target-machine"></a><span data-ttu-id="8ad6f-137">Erstellen des Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="8ad6f-137">Constructing the Target Machine</span></span>

<span data-ttu-id="8ad6f-138">Quantencomputer sind Instanzen normaler .NET-Klassen. Sie werden also genauso wie .NET-Klassen erstellt, indem ihr Konstruktor aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-138">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span>
<span data-ttu-id="8ad6f-139">Da von einigen Simulatoren, z. B. `QuantumSimulator`, die <xref:System.IDisposable?displayProperty=nameWithType>-.NET-Schnittstelle implementiert wird, sollten diese mit einer C#-Anweisung vom Typ `using` umschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-139">Some simulators, including the `QuantumSimulator`, implement the .NET <xref:System.IDisposable?displayProperty=nameWithType> interface, and so should be wrapped in a C# `using` statement.</span></span>

### <a name="computing-arguments-for-the-algorithm"></a><span data-ttu-id="8ad6f-140">Berechnen von Argumenten für den Algorithmus</span><span class="sxs-lookup"><span data-stu-id="8ad6f-140">Computing Arguments for the Algorithm</span></span>

<span data-ttu-id="8ad6f-141">Im `Teleport`-Beispiel haben wir einige etwas künstliche Argumente für die Übergabe an unseren Quantenalgorithmus berechnet.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-141">In our `Teleport` example, we computed some relatively artificial arguments to pass to our quantum algorithm.</span></span>
<span data-ttu-id="8ad6f-142">Typischer ist aber, dass für den Quantenalgorithmus umfangreiche Daten benötigt werden, die am einfachsten über den klassischen Treiber bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-142">More typically, however, there is significant data required by the quantum algorithm, and it is easiest to provide it from the classical driver.</span></span>

<span data-ttu-id="8ad6f-143">Beim Durchführen von chemischen Simulationen ist für den Quantenalgorithmus beispielsweise eine umfassende Tabelle mit Molekülorbital-Interaktionsintegralen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-143">For instance, when doing chemical simulations, the quantum algorithm requires a large table of molecular orbital interaction integrals.</span></span>
<span data-ttu-id="8ad6f-144">Normalerweise werden diese Daten aus einer Datei eingelesen, die beim Ausführen des Algorithmus angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-144">Generally these are read in from a file that is provided when running the algorithm.</span></span>
<span data-ttu-id="8ad6f-145">Da Q# nicht über einen Mechanismus für den Zugriff auf das Dateisystem verfügt, ist es am besten, diese Daten über den klassischen Treiber zu erfassen und dann an die `Run`-Methode des Quantenalgorithmus zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-145">Since Q# does not have a mechanism for accessing the file system, this sort of data is best collected by the classical driver and then passed to the quantum algorithm's `Run` method.</span></span>

<span data-ttu-id="8ad6f-146">Ein weiterer Fall, in dem der klassische Treiber eine wichtige Rolle spielt, sind Variationsmethoden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-146">Another case where the classical driver plays a key role is in variational methods.</span></span>
<span data-ttu-id="8ad6f-147">Bei dieser Klasse von Algorithmen wird basierend auf einigen klassischen Parametern ein Quantenzustand vorbereitet, der dann zum Berechnen eines benötigten Werts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-147">In this class of algorithms, a quantum state is prepared based on some classical parameters, and that state is used to compute some value of interest.</span></span>
<span data-ttu-id="8ad6f-148">Die Parameter werden basierend auf einer Art von Bergsteiger- oder Machine Learning-Algorithmus angepasst, und der Quantenalgorithmus wird erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-148">The parameters are adjusted based on some type of hill climbing or machine learning algorithm and the quantum algorithm run again.</span></span>
<span data-ttu-id="8ad6f-149">Bei Algorithmen dieser Art wird der Bergsteigeralgorithmus selbst am besten als reine klassische Funktion implementiert, die vom klassischen Treiber aufgerufen wird. Die Ergebnisse des Bergsteigervorgangs werden dann an die nächste Ausführung des Quantenalgorithmus übergeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-149">For such algorithms, the hill climbing algorithm itself is best implemented as a purely classical function that is called by the classical driver; the results of the hill climbing are then passed to the next execution of the quantum algorithm.</span></span>

### <a name="running-the-quantum-algorithm"></a><span data-ttu-id="8ad6f-150">Ausführen des Quantenalgorithmus</span><span class="sxs-lookup"><span data-stu-id="8ad6f-150">Running the Quantum Algorithm</span></span>

<span data-ttu-id="8ad6f-151">Dieser Teil ist im Allgemeinen nicht sehr kompliziert.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-151">This part is generally very straightforward.</span></span>
<span data-ttu-id="8ad6f-152">Jeder Q#-Vorgang wird zu einer Klasse kompiliert, die eine statische `Run`-Methode bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-152">Each Q# operation is compiled into a class that provides a static `Run` method.</span></span>
<span data-ttu-id="8ad6f-153">Die Argumente für diese Methode werden vom vereinfachten Argumenttupel des Vorgangs selbst bereitgestellt – sowie ein weiteres erstes Argument, bei dem es sich um den Simulator für die Ausführung handelt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-153">The arguments to this method are given by the flattened argument tuple of the operation itself, plus an additional first argument which is the simulator to execute with.</span></span> <span data-ttu-id="8ad6f-154">Für einen Vorgang, für den das benannte Tupel vom Typ `(a: String, (b: Double, c: Double))` erwartet wird, hat das vereinfachte Gegenstück den Typ `(String a, Double b, Double c)`.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-154">For an operation that expects the named tuple of type `(a: String, (b: Double, c: Double))` its flattened counterpart is of type `(String a, Double b, Double c)`.</span></span>


<span data-ttu-id="8ad6f-155">Beim Übergeben von Argumenten an eine `Run`-Methode sind einige Besonderheiten zu beachten:</span><span class="sxs-lookup"><span data-stu-id="8ad6f-155">There are some subtleties when passing arguments to a `Run` method:</span></span>

* <span data-ttu-id="8ad6f-156">Arrays müssen mit einem `Microsoft.Quantum.Simulation.Core.QArray<T>`-Objekt umschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-156">Arrays must be wrapped in a `Microsoft.Quantum.Simulation.Core.QArray<T>` object.</span></span>
    <span data-ttu-id="8ad6f-157">Eine `QArray`-Klasse verfügt über einen Konstruktor, für den eine beliebige sortierte Sammlung (`IEnumerable<T>`) mit geeigneten Objekten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-157">A `QArray` class has a constructor that can take any ordered collection (`IEnumerable<T>`) of appropriate objects.</span></span>
* <span data-ttu-id="8ad6f-158">Das leere Tupel (`()` in Q#) wird in C# mit `QVoid.Instance` dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-158">The empty tuple, `()` in Q#, is represented by `QVoid.Instance` in C#.</span></span>
* <span data-ttu-id="8ad6f-159">Tupel, die nicht leer sind, werden als `ValueTuple`-.NET-Instanzen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-159">Non-empty tuples are represented as .NET `ValueTuple` instances.</span></span>
* <span data-ttu-id="8ad6f-160">Benutzerdefinierte Q#-Typen werden als Basistyp übergeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-160">Q# user-defined types are passed as their base type.</span></span>
* <span data-ttu-id="8ad6f-161">Zum Übergeben eines Vorgangs oder einer Funktion an eine `Run`-Methode müssen Sie eine Instanz der Vorgangs- oder Funktionsklasse abrufen, indem Sie die `Get<>`-Methode des Simulators verwenden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-161">To pass an operation or a function to a `Run` method, you have to obtain an   instance of the operation's or function's class, using the simulator's `Get<>` method.</span></span>

### <a name="processing-the-results"></a><span data-ttu-id="8ad6f-162">Verarbeiten der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="8ad6f-162">Processing the Results</span></span>

<span data-ttu-id="8ad6f-163">Die Ergebnisse des Quantenalgorithmus werden von der `Run`-Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-163">The results of the quantum algorithm are returned from the `Run` method.</span></span>
<span data-ttu-id="8ad6f-164">Da die `Run`-Methode asynchron ausgeführt wird, gibt sie eine Instanz von <xref:System.Threading.Tasks.Task`1> zurück.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-164">The `Run` method executes asynchronously thus it returns an instance of <xref:System.Threading.Tasks.Task`1>.</span></span>
<span data-ttu-id="8ad6f-165">Es gibt mehrere Möglichkeiten, die Ergebnisse des tatsächlichen Vorgangs zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-165">There are multiple ways to get the actual operation's results.</span></span> <span data-ttu-id="8ad6f-166">Der einfachste Weg ist die Verwendung der [`Result`-Eigenschaft](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result) der `Task`:</span><span class="sxs-lookup"><span data-stu-id="8ad6f-166">The simplest is by using the `Task`'s [`Result` property](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):</span></span>

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
<span data-ttu-id="8ad6f-167">Andere Verfahren, z. B. die [`Wait`-Methode](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) oder das C#-Schlüsselwort [`await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await), funktionieren ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-167">but other techniques, like using the [`Wait` method](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) or C# [`await` keyword](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) will also work.</span></span>

<span data-ttu-id="8ad6f-168">Wie auch bei Argumenten, werden Q#-Tupel als `ValueTuple`-Instanzen und Q#-Arrays als `QArray`-Instanzen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-168">As with arguments, Q# tuples are represented as `ValueTuple` instances and Q# arrays are represented as `QArray` instances.</span></span>
<span data-ttu-id="8ad6f-169">Benutzerdefinierte Typen werden als Basistypen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-169">User-defined types are returned as their base types.</span></span>
<span data-ttu-id="8ad6f-170">Das leere Tupel `()` wird als Instanz der `QVoid`-Klasse zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-170">The empty tuple, `()`, is returned as an instance of the `QVoid` class.</span></span>

<span data-ttu-id="8ad6f-171">Für viele Quantenalgorithmen ist eine umfangreiche Nachbearbeitung erforderlich, um nützliche Antworten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-171">Many quantum algorithms require substantial post-processing to derive useful answers.</span></span>
<span data-ttu-id="8ad6f-172">Der Quantenteil des Shor-Algorithmus ist beispielsweise nur der Anfang einer Berechnung, bei der die Faktoren einer Zahl ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-172">For instance, the quantum part of Shor's algorithm is just the beginning of a computation that finds the factors of a number.</span></span>

<span data-ttu-id="8ad6f-173">In den meisten Fällen ist es am einfachsten, diese Art der Nachbearbeitung über den klassischen Treiber durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-173">In most cases, it is simplest and easiest to do this sort of post-processing in the classical driver.</span></span>
<span data-ttu-id="8ad6f-174">Nur mit dem klassischen Treiber können Ergebnisse an den Benutzer gemeldet oder auf Datenträger geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-174">Only the classical driver can report results to the user or write them to disk.</span></span>
<span data-ttu-id="8ad6f-175">Der klassische Treiber verfügt über Zugriff auf Analysebibliotheken und andere mathematische Funktionen, die in Q# nicht verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-175">The classical driver will have access to analytical libraries and other mathematical functions that are not exposed in Q#.</span></span>


## <a name="failures"></a><span data-ttu-id="8ad6f-176">Fehler</span><span class="sxs-lookup"><span data-stu-id="8ad6f-176">Failures</span></span>

<span data-ttu-id="8ad6f-177">Wenn bei der Ausführung eines Vorgangs die Q#-Anweisung `fail` erreicht wird, wird `ExecutionFailException` ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-177">When the Q# `fail` statement is reached during the execution of an operation, an `ExecutionFailException` is thrown.</span></span>

<span data-ttu-id="8ad6f-178">Aufgrund der Verwendung von `System.Task` in der `Run`-Methode ist die Ausnahme, die aufgrund einer `fail`-Anweisung ausgelöst wird, von `System.AggregateException` umschlossen.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-178">Due to the use of `System.Task` in the `Run` method, the exception thrown as a result of a `fail` statement will be wrapped into a `System.AggregateException`.</span></span>
<span data-ttu-id="8ad6f-179">Zum Ermitteln der tatsächlichen Ursache des Fehlers müssen Sie eine Iteration in `AggregateException` 
`InnerExceptions` durchführen. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8ad6f-179">To find the actual reason for the failure, you need to iterate into the `AggregateException` 
`InnerExceptions`, for example:</span></span>

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a><span data-ttu-id="8ad6f-180">Andere klassische Sprachen</span><span class="sxs-lookup"><span data-stu-id="8ad6f-180">Other Classical Languages</span></span>

<span data-ttu-id="8ad6f-181">Die bereitgestellten Beispiele gelten für C#, F# und Python, aber das Quantum Development Kit unterstützt auch das Schreiben klassischer Hostprogramme in anderen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="8ad6f-181">While the samples we have provided are in C#, F#, and Python, the Quantum Development Kit also supports writing classical host programs in other languages.</span></span>
<span data-ttu-id="8ad6f-182">Wenn Sie beispielsweise ein Hostprogramm in Visual Basic schreiben möchten, [sollte dies problemlos funktionieren](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span><span class="sxs-lookup"><span data-stu-id="8ad6f-182">For example, if you want to write a host program in Visual Basic, [it should work just fine](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span></span>
