---
title: Möglichkeiten zum Ausführen eines Q# Programms
description: Übersicht über die verschiedenen Möglichkeiten zum Ausführen von Q# Programmen. Über die Befehlszeile, Q# jupyter Notebooks und klassische Host Programme in Python oder einer .NET-Sprache.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8e3fa83700417a4ffaf9e3be91796c9e9513b253
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869731"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="d9fde-104">Möglichkeiten zum Ausführen eines Q# Programms</span><span class="sxs-lookup"><span data-stu-id="d9fde-104">Ways to run a Q# program</span></span>

<span data-ttu-id="d9fde-105">Eines der größten Stärken des quantumentwicklungskit ist seine Flexibilität über Plattformen und Entwicklungsumgebungen hinweg.</span><span class="sxs-lookup"><span data-stu-id="d9fde-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="d9fde-106">Dies bedeutet jedoch auch, dass Q# sich neue Benutzer möglicherweise nicht mit den zahlreichen Optionen im [Installationshandbuch](xref:microsoft.quantum.install)verwechselt haben.</span><span class="sxs-lookup"><span data-stu-id="d9fde-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="d9fde-107">Auf dieser Seite erläutern wir, was geschieht, wenn ein Q# Programm ausgeführt wird, und vergleichen die verschiedenen Möglichkeiten, wie Benutzer dies tun können.</span><span class="sxs-lookup"><span data-stu-id="d9fde-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="d9fde-108">Ein primärer Unterschied besteht darin, dass Q# ausgeführt werden kann:</span><span class="sxs-lookup"><span data-stu-id="d9fde-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="d9fde-109">als eigenständige Anwendung, bei Q# der die einzige beteiligte Sprache ist und das Programm direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="d9fde-110">Zwei Methoden fallen tatsächlich in diese Kategorie:</span><span class="sxs-lookup"><span data-stu-id="d9fde-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="d9fde-111">die Befehlszeilenschnittstelle</span><span class="sxs-lookup"><span data-stu-id="d9fde-111">the command line interface</span></span>
  - <span data-ttu-id="d9fde-112">Q#Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="d9fde-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="d9fde-113">mit einem zusätzlichen *Host Programm*, das in Python oder einer .NET-Sprache (z. b. c# oder F #) geschrieben ist, die dann das Programm aufruft und die zurückgegebenen Ergebnisse weiterverarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="d9fde-113">with an additional *host program*, written in Python or a .NET language (e.g. C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="d9fde-114">Um diese Prozesse und deren Unterschiede zu verstehen, wird ein einfaches Q# Programm angenommen, und es wird erläutert, wie es ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9fde-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be executed.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="d9fde-115">Einfaches Q# Programm</span><span class="sxs-lookup"><span data-stu-id="d9fde-115">Basic Q# program</span></span>

<span data-ttu-id="d9fde-116">Ein grundlegendes Quantum-Programm besteht möglicherweise aus der Vorbereitung eines Qubit in derselben Superposition in den Zuständen $ \ket {0} $ und $ \ket {1} $, wobei es gemessen wird und das Ergebnis zurückgegeben wird. dabei wird entweder einer dieser beiden Zustände mit gleicher Wahrscheinlichkeit nach dem Zufallsprinzip verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9fde-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="d9fde-117">Tatsächlich ist dieser Prozess der Kern des Schnellstarts des [Quantum-Zufallszahlen-Generators](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="d9fde-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="d9fde-118">In wird Q# dies durch den folgenden Code ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="d9fde-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="d9fde-119">Dieser Code allein kann jedoch nicht von ausgeführt werden Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-119">However, this code alone can't be executed by Q#.</span></span>
<span data-ttu-id="d9fde-120">Dafür muss der Text eines [Vorgangs](xref:microsoft.quantum.guide.basics#q-operations-and-functions), der dann ausgeführt wird, wenn er---direkt oder durch einen anderen Vorgang aufgerufen wird, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.guide.basics#q-operations-and-functions), which is then executed when called---either directly or by another operation.</span></span> <span data-ttu-id="d9fde-121">Daher können Sie einen Vorgang der folgenden Form schreiben:</span><span class="sxs-lookup"><span data-stu-id="d9fde-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="d9fde-122">Sie haben einen Vorgang definiert, `MeasureSuperposition` der keine Eingaben annimmt und einen Wert vom Typ [Result](xref:microsoft.quantum.guide.types)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="d9fde-123">Obwohl die Beispiele auf dieser Seite nur aus Q# *Vorgängen*bestehen, werden alle Konzepte, die wir erörtern werden, gleichermaßen für Q# *Funktionen*verwendet. daher bezeichnen wir Sie zusammen als *callables*.</span><span class="sxs-lookup"><span data-stu-id="d9fde-123">While the examples on this page only consist of Q# *operations*, all of the concepts we will discuss pertain equally to Q# *functions*, and therefore we refer to them collectively as *callables*.</span></span> <span data-ttu-id="d9fde-124">Die Unterschiede werden in den [ Q# Grundlagen erläutert: Vorgänge und Funktionen](xref:microsoft.quantum.guide.basics#q-operations-and-functions)und weitere Details zur Definition finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="d9fde-124">Their differences are discussed at [Q# basics: operations and functions](xref:microsoft.quantum.guide.basics#q-operations-and-functions), and more details on defining them can be found at [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="d9fde-125">In einer Datei definierte Aufruf Bare Q# Datei</span><span class="sxs-lookup"><span data-stu-id="d9fde-125">Callable defined in a Q# file</span></span>

<span data-ttu-id="d9fde-126">Die Aufruf Bare ist genau das, was von aufgerufen und ausgeführt wird Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-126">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="d9fde-127">Allerdings sind einige weitere Ergänzungen erforderlich, um eine vollständige Datei zu bilden `*.qs` Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-127">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="d9fde-128">Alle Q# Typen und callables (sowohl die, die Sie definieren, als auch die in der Sprache intrinsisch) werden innerhalb von *Namespaces*definiert, die jeweils einen vollständigen Namen bereitstellen, auf den dann verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d9fde-128">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="d9fde-129">Beispielsweise werden die [`H`](xref:microsoft.quantum.intrinsic.h) [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) Vorgänge und in den [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) Namespaces und (Teil der [ Q# Standard Bibliotheken](xref:microsoft.quantum.qsharplibintro)) gefunden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-129">For example, the [`H`](xref:microsoft.quantum.intrinsic.h) and [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.qsharplibintro)).</span></span>
<span data-ttu-id="d9fde-130">Daher können Sie immer über die *vollständigen* Namen und aufgerufen werden `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` . Dies führt jedoch zu einem sehr überlasteten Code.</span><span class="sxs-lookup"><span data-stu-id="d9fde-130">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="d9fde-131">Stattdessen `open` ermöglichen-Anweisungen, dass auf Aufruf Bare Elemente mit präziseren Kurzform verwiesen wird, wie dies im obigen Vorgangs Text geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="d9fde-131">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="d9fde-132">Die vollständige Q# Datei, die den Vorgang enthält, besteht daher darin, einen eigenen Namespace zu definieren, die Namespaces für die von unserem Vorgang verwendeten callables zu öffnen, und dann den Vorgang:</span><span class="sxs-lookup"><span data-stu-id="d9fde-132">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="d9fde-133">Namespaces können auch beim Öffnen einen *Alias* aufweisen. Dies kann hilfreich sein, wenn Aufruf Bare/Typnamen in zwei Namespaces in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-133">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="d9fde-134">Beispielsweise könnten wir stattdessen oben verwenden `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` und dann `H` via anrufen `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-134">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="d9fde-135">Eine Ausnahme ist der [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) Namespace, der immer automatisch geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-135">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="d9fde-136">Daher können callables wie [`Length`](xref:microsoft.quantum.core.length) immer direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-136">Therefore, callables like [`Length`](xref:microsoft.quantum.core.length) can always be used directly.</span></span>

### <a name="execution-on-target-machines"></a><span data-ttu-id="d9fde-137">Ausführung auf Ziel Computern</span><span class="sxs-lookup"><span data-stu-id="d9fde-137">Execution on target machines</span></span>

<span data-ttu-id="d9fde-138">Nun wird das allgemeine Ausführungs Modell eines Q# Programms deutlich.</span><span class="sxs-lookup"><span data-stu-id="d9fde-138">Now the general execution model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="d9fde-139">Zum einen hat die spezifische Aufruf Bare, die ausgeführt werden kann, Zugriff auf alle anderen callables und Typen, die im selben Namespace definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d9fde-139">Firstly, the specific callable to be executed has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="d9fde-140">Außerdem greift er auf die Bibliotheken aus einer der [ Q# Bibliotheken](xref:microsoft.quantum.libraries)zu, aber auf diese müssen entweder über den vollständigen Namen oder über die `open` oben beschriebenen Anweisungen verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-140">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="d9fde-141">Die Aufruf Bare selbst wird dann auf einem *[Zielcomputer](xref:microsoft.quantum.machines)* ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-141">The callable itself is then executed on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="d9fde-142">Bei solchen Ziel Computern kann es sich um tatsächliche Quantum-Hardware oder mehrere Simulatoren handeln, die als Teil des QDK verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="d9fde-142">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="d9fde-143">Zu diesem Zweck ist der nützlichste Zielcomputer eine Instanz des [vollständigen Simulators](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , der das Verhalten des Programms so berechnet, als ob es auf einem Rausch freien Quantum-Computer ausgeführt würde.</span><span class="sxs-lookup"><span data-stu-id="d9fde-143">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being executed on a noise-free quantum computer.</span></span>

<span data-ttu-id="d9fde-144">Bisher haben wir beschrieben, was geschieht, wenn eine bestimmte Q# Aufruf Bare ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-144">So far, we've described what happens when a specific Q# callable is being executed.</span></span>
<span data-ttu-id="d9fde-145">Unabhängig davon Q# , ob in einer eigenständigen Anwendung oder einem Host Programm verwendet wird, ist dieser allgemeine Prozess mehr oder weniger identisch---daher die Flexibilität des QDK.</span><span class="sxs-lookup"><span data-stu-id="d9fde-145">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="d9fde-146">Die Unterschiede zwischen den verschiedenen Methoden zum Aufrufen von Quantum Development Kit zeigen sich daher selbst, *wie* diese Aufruf Q# Bare aufgerufen wird und wie alle Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-146">The differences between the different ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be executed, and in what manner any results are returned.</span></span>
<span data-ttu-id="d9fde-147">Genauer gesagt werden die Unterschiede im Zusammenhang mit</span><span class="sxs-lookup"><span data-stu-id="d9fde-147">More specifically, the differences revolve around</span></span> 
1. <span data-ttu-id="d9fde-148">die Angabe Q# , welche Aufruf Bare ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d9fde-148">indicating which Q# callable is to be executed,</span></span>
2. <span data-ttu-id="d9fde-149">Gibt an, wie potenzielle Aufruf Bare Argumente bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-149">how potential callable arguments are provided,</span></span>
3. <span data-ttu-id="d9fde-150">Angeben des Ziel Computers, auf dem der Computer ausgeführt werden soll, und</span><span class="sxs-lookup"><span data-stu-id="d9fde-150">specifying the target machine on which to execute it, and</span></span>
4. <span data-ttu-id="d9fde-151">Gibt an, wie alle Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-151">how any results are returned.</span></span>

<span data-ttu-id="d9fde-152">Zuerst wird erläutert, wie dies mit der Q# eigenständigen Anwendung über die Befehlszeile erfolgt, und anschließend können Sie mit der Verwendung von Python-und c#-Host Programmen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="d9fde-152">First, we discuss how this is done with the Q# standalone application from the command line, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="d9fde-153">Wir reservieren die eigenständige Anwendung von Q# jupyter-Notebooks für das letzte, da die primäre Funktionalität im Gegensatz zu den ersten drei nicht um eine lokale Datei zentriert ist Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-153">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="d9fde-154">Obwohl wir dies in diesen Beispielen nicht veranschaulichen, besteht eine Gemeinsamkeit zwischen den Ausführungsmethoden darin, dass alle Nachrichten, die aus dem Programm gedruckt werden (z. b. über Q# [`Message`](xref:microsoft.quantum.intrinsic.message) oder [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), in der Regel immer an die jeweilige Konsole ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-154">Although we don't illustrate it in these examples, one commonality between the execution methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:microsoft.quantum.intrinsic.message) or [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-line"></a><span data-ttu-id="d9fde-155">Q#über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="d9fde-155">Q# from the command line</span></span>
<span data-ttu-id="d9fde-156">Eine der einfachsten Möglichkeiten, Programme zu schreiben Q# , besteht darin, die Gedanken über separate Dateien und eine zweite Sprache vollständig zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-156">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="d9fde-157">Die Verwendung von Visual Studio Code oder Visual Studio mit der QDK-Erweiterung ermöglicht einen nahtlosen Workflow, bei dem Q# nur callables aus einer einzelnen Q# Datei ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-157">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="d9fde-158">Hierzu wird die Ausführung des Programms letztendlich aufgerufen, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="d9fde-158">For this, we will ultimately invoke the program's execution by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="d9fde-159">in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="d9fde-159">in the command line.</span></span>
<span data-ttu-id="d9fde-160">Der einfachste Workflow ist, wenn der Verzeichnis Speicherort des Terminals mit der Datei identisch ist Q# , die mit Q# der Dateibearbeitung problemlos über das integrierte Terminal in vs Code behandelt werden kann, z. b..</span><span class="sxs-lookup"><span data-stu-id="d9fde-160">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="d9fde-161">Der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) akzeptiert jedoch zahlreiche Optionen, und das Programm kann auch an einem anderen Speicherort ausgeführt werden, indem einfach `--project <PATH>` der Speicherort der Datei bereitgestellt wird Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-161">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="d9fde-162">Einstiegspunkt zu Datei hinzufügen Q#</span><span class="sxs-lookup"><span data-stu-id="d9fde-162">Add entry point to Q# file</span></span>

<span data-ttu-id="d9fde-163">Die meisten Q# Dateien enthalten mehr als eine Aufruf Bare Funktion. Daher müssen wir dem Compiler natürlich mitteilen, *welche* Callable beim Bereitstellen des Befehls ausgeführt werden soll `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-163">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to execute when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="d9fde-164">Dies erfolgt mit einer einfachen Änderung an der Q# Datei selbst:</span><span class="sxs-lookup"><span data-stu-id="d9fde-164">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="d9fde-165">Fügen Sie eine Zeile hinzu, `@EntryPoint()` die direkt vor dem Aufruf baren steht.</span><span class="sxs-lookup"><span data-stu-id="d9fde-165">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="d9fde-166">Unsere Datei von oben wird daher</span><span class="sxs-lookup"><span data-stu-id="d9fde-166">Our file from above would therefore become</span></span>
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

<span data-ttu-id="d9fde-167">Nun `dotnet run` führt ein-Befehl von der Befehlszeile aus `MeasureSuperposition` , um ausgeführt zu werden, und der zurückgegebene Wert wird dann direkt in das Terminal gedruckt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-167">Now, a call of `dotnet run` from the command line leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="d9fde-168">Daher wird entweder `One` oder `Zero` gedruckt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-168">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="d9fde-169">Beachten Sie, dass es keine Rolle spielt, ob weitere Aufruf Bare aufruben definiert sind, sondern nur `MeasureSuperposition` ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-169">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="d9fde-170">Außerdem ist es kein Problem, wenn die Aufruf Bare-Datei vor der Deklaration [Dokumentations Kommentare](xref:microsoft.quantum.guide.filestructure#documentation-comments) enthält `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-170">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.guide.filestructure#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="d9fde-171">Aufruf Bare Argumente</span><span class="sxs-lookup"><span data-stu-id="d9fde-171">Callable arguments</span></span>

<span data-ttu-id="d9fde-172">Bisher haben wir nur einen Vorgang in Erwägung gezogen, der keine Eingaben annimmt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-172">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="d9fde-173">Angenommen, wir wollten einen ähnlichen Vorgang durchführen, aber auf mehreren Qubits---die Zahl als Argument bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-173">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="d9fde-174">Ein solcher Vorgang könnte als</span><span class="sxs-lookup"><span data-stu-id="d9fde-174">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="d9fde-175">Dabei ist der zurückgegebene Wert ein Array der Messergebnisse.</span><span class="sxs-lookup"><span data-stu-id="d9fde-175">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="d9fde-176">Beachten Sie, dass [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) und [`ForEach`](xref:microsoft.quantum.arrays.foreach) sich im [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) -Namespace und im- [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) Namespace befinden, `open` wobei jeweils zusätzliche Anweisungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d9fde-176">Note that [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) and [`ForEach`](xref:microsoft.quantum.arrays.foreach) are in the [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) and [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="d9fde-177">Wenn Sie das `@EntryPoint()` Attribut vor diesem neuen Vorgang verschieben (Beachten Sie, dass es nur eine Zeile in einer Datei geben kann), und wenn Sie versuchen, es mit einfach auszuführen, führt dies zu `dotnet run` einer Fehlermeldung, die angibt, welche zusätzlichen Befehlszeilenoptionen erforderlich sind, und wie Sie Sie Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="d9fde-177">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command line options are required, and how to express them.</span></span>

<span data-ttu-id="d9fde-178">Das allgemeine Format für die Befehlszeile ist tatsächlich `dotnet run [options]` , und es werden Aufruf Bare Argumente dort bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-178">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="d9fde-179">In diesem Fall fehlt das Argument `n` , und es wird angezeigt, dass die Option bereitgestellt werden muss `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-179">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="d9fde-180">Zum Ausführen `MeasureSuperpositionArray` von for `n=4` Qubits verwenden wir daher</span><span class="sxs-lookup"><span data-stu-id="d9fde-180">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="d9fde-181">Ausgabe ähnlich</span><span class="sxs-lookup"><span data-stu-id="d9fde-181">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="d9fde-182">Dies reicht natürlich auf mehrere Argumente aus.</span><span class="sxs-lookup"><span data-stu-id="d9fde-182">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="d9fde-183">In definierte Argument Namen `camelCase` werden vom Compiler leicht geändert, damit Sie als Eingaben akzeptiert werden Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-183">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="d9fde-184">Wenn z. b. anstelle von `n` der oben genannte Name verwendet wird `numQubits` , wird diese Eingabe in der Befehlszeile über `--num-qubits 4` anstelle von bereitgestellt `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-184">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="d9fde-185">Die Fehlermeldung enthält auch weitere Optionen, die verwendet werden können, einschließlich Informationen zum Ändern des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="d9fde-185">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="d9fde-186">Verschiedene Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="d9fde-186">Different target machines</span></span>

<span data-ttu-id="d9fde-187">Da die Ausgaben unserer Vorgänge bisher die erwarteten Ergebnisse ihrer Aktion in echten Qubits waren, ist es klar, dass der Standardziel Computer von der Befehlszeile aus der vollständige quauntum-Simulator ist `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-187">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quauntum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="d9fde-188">Wir können jedoch Aufruf Bare Aufrufe anweisen, die auf einem bestimmten Zielcomputer mit der Option `--simulator` (oder der kurzseite `-s` ) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-188">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="d9fde-189">Beispielsweise können wir die Anwendung unter Ausführen [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="d9fde-189">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="d9fde-190">Die gedruckte Ausgabe lautet dann</span><span class="sxs-lookup"><span data-stu-id="d9fde-190">The printed output is then</span></span>

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

<span data-ttu-id="d9fde-191">Ausführliche Informationen dazu, was diese Metriken angeben, finden Sie unter [Ressourcenschätzung: gemeldete Metriken](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span><span class="sxs-lookup"><span data-stu-id="d9fde-191">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-execution-summary"></a><span data-ttu-id="d9fde-192">Zusammenfassung der Befehlszeilen Ausführung</span><span class="sxs-lookup"><span data-stu-id="d9fde-192">Command line execution summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="d9fde-193">Nicht- Q# `dotnet run` Optionen</span><span class="sxs-lookup"><span data-stu-id="d9fde-193">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="d9fde-194">Wie bereits kurz erwähnt `--project` , akzeptiert der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) auch Optionen, die nicht mit den Q# Aufruf baren Argumenten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="d9fde-194">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="d9fde-195">Wenn beide Arten von Optionen bereit `dotnet` gestellt werden, müssen zuerst die-spezifischen Optionen, gefolgt von einem Trennzeichen `--` , und dann die Q# -spezifischen Optionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-195">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="d9fde-196">Beispielsweise würde die Angabe eines Pfads zusammen mit einer Zahlen-Qubits für den obigen Vorgang über ausgeführt werden `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-196">For example, specifiying a path along with a number qubits for the operation above would be executed via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="d9fde-197">Q#mit Host Programmen</span><span class="sxs-lookup"><span data-stu-id="d9fde-197">Q# with host programs</span></span>

<span data-ttu-id="d9fde-198">Mit unserer Q# Datei besteht eine Alternative zum Aufrufen eines Vorgangs oder einer Funktion direkt über die Befehlszeile darin, ein *Host Programm* in einer anderen klassischen Sprache zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-198">With our Q# file in hand, an alternative to calling an operation or function directly from the command line is to use a *host program* in another classical language.</span></span> <span data-ttu-id="d9fde-199">Dies kann insbesondere mit Python oder einer .NET-Sprache (z. b. c# oder F #) erfolgen (aus Gründen der Kürze wird c# hier nur ausführlich erläutert).</span><span class="sxs-lookup"><span data-stu-id="d9fde-199">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="d9fde-200">Zum Aktivieren der Interoperabilität ist ein wenig mehr Setup erforderlich. diese Details finden Sie jedoch in den [Installations](xref:microsoft.quantum.install)Handbüchern.</span><span class="sxs-lookup"><span data-stu-id="d9fde-200">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="d9fde-201">Kurz gesagt, enthält die Situation nun eine Host Programmdatei (z. b. `*.py` oder `*.cs` ) am gleichen Speicherort wie die Q# Datei.</span><span class="sxs-lookup"><span data-stu-id="d9fde-201">In a nutshell, the situation now includes a host program file (e.g. `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="d9fde-202">Es ist jetzt das *Host* Programm, das ausgeführt wird, und im Verlauf der Ausführung kann es bestimmte Q# Vorgänge und Funktionen aus der Datei abrufen Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-202">It's now the *host* program that gets run, and in the course of its execution it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="d9fde-203">Der Kern der Interoperabilität basiert auf dem Compiler, der Q# den Inhalt der Q# Datei für das Host Programm zugänglich macht, sodass Sie aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="d9fde-203">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="d9fde-204">Einer der Hauptvorteile der Verwendung eines Host Programms besteht darin, dass die vom Programm zurückgegebenen klassischen Daten Q# dann in der Host Sprache weiterverarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="d9fde-204">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="d9fde-205">Dies kann aus einer erweiterten Datenverarbeitung bestehen (z. b. etwas, das nicht intern in ausgeführt werden kann Q# ). Anschließend werden weitere Aktionen auf der Q# Grundlage dieser Ergebnisse aufgerufen, oder es kann etwas so einfach sein, wie die Ergebnisse gezeichnet werden Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-205">This could consist of some advanced data processing (e.g. something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="d9fde-206">Das allgemeine Schema wird hier angezeigt, und wir erörtern die spezifischen Implementierungen für python und c# weiter unten.</span><span class="sxs-lookup"><span data-stu-id="d9fde-206">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="d9fde-207">Ein Beispiel für die Verwendung eines F #-Host Programms finden Sie unter [.net-Interoperabilitäts Beispiele](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="d9fde-207">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="d9fde-208">Das `@EntryPoint()` für Q# Befehlszeilen Anwendungen verwendete Attribut kann nicht mit Host Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-208">The `@EntryPoint()` attribute used for Q# command line applications cannot be used with host programs.</span></span>
> <span data-ttu-id="d9fde-209">Wenn Sie in der Datei vorhanden ist Q# , die von einem Host aufgerufen wird, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d9fde-209">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="d9fde-210">Um mit unterschiedlichen Host Programmen arbeiten zu können, sind keine Änderungen an einer `*.qs` Q# Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d9fde-210">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="d9fde-211">Die folgenden Host Programm Implementierungen funktionieren alle mit derselben Q# Datei:</span><span class="sxs-lookup"><span data-stu-id="d9fde-211">The following host program implementations all work with the same Q# file:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

<span data-ttu-id="d9fde-212">Wählen Sie die Registerkarte aus, die der gewünschten Host Sprache entspricht.</span><span class="sxs-lookup"><span data-stu-id="d9fde-212">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="d9fde-213">Python</span><span class="sxs-lookup"><span data-stu-id="d9fde-213">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="d9fde-214">Ein python-Host Programm wird wie folgt erstellt:</span><span class="sxs-lookup"><span data-stu-id="d9fde-214">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="d9fde-215">Importieren Sie das- `qsharp` Modul, mit dem das Modul Lade Modul für die Interoperabilität registriert wird Q# .</span><span class="sxs-lookup"><span data-stu-id="d9fde-215">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="d9fde-216">Dadurch Q# können Namespaces als Python-Module angezeigt werden, aus denen Sie Q# callables importieren können.</span><span class="sxs-lookup"><span data-stu-id="d9fde-216">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="d9fde-217">Beachten Sie, dass es sich nicht um die Q# selbst importierbaren, sondern vielmehr um python-Stubdateien handelt, die das Aufrufen von Dateien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-217">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="d9fde-218">Diese werden dann als Objekte von python-Klassen verwendet, auf denen Methoden zum Angeben der Zielcomputer verwendet werden, an die der Vorgang zur Ausführung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-218">These then behave as objects of Python classes, on which we use methods to specify the target machines to send the operation to for execution.</span></span>

2. <span data-ttu-id="d9fde-219">Importieren Sie diese Q# callables, die wir direkt aufrufen---in diesem Fall `MeasureSuperposition` und `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-219">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="d9fde-220">Wenn `qsharp` Sie das Modul importiert haben, können Sie auch callables direkt aus den Q# Bibliotheks Namespaces importieren.</span><span class="sxs-lookup"><span data-stu-id="d9fde-220">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="d9fde-221">Unter jedem anderen Python-Code können Sie jetzt diese callables auf bestimmten Ziel Computern aufrufen und ihre Rückgaben den Variablen (wenn Sie einen Wert zurückgeben) zur weiteren Verwendung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-221">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="d9fde-222">Angeben von Ziel Computern</span><span class="sxs-lookup"><span data-stu-id="d9fde-222">Specifying target machines</span></span>
<span data-ttu-id="d9fde-223">Das Aufrufen eines Vorgangs, der auf einem bestimmten Zielcomputer ausgeführt werden soll, erfolgt über verschiedene python-Methoden auf dem importierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-223">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="d9fde-224">Beispielsweise `.simulate(<args>)` verwendet die `QuantumSimulator` zum Ausführen des Vorgangs, während `.estimate_resources(<args>)` dies in der erfolgt `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-224">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="d9fde-225">Übergeben von Eingaben an Q\#</span><span class="sxs-lookup"><span data-stu-id="d9fde-225">Passing inputs to Q\#</span></span>
<span data-ttu-id="d9fde-226">Argumente für die Q# Aufruf Bare-Datei sollten in Form eines Schlüsselwort Arguments bereitgestellt werden, wobei das-Schlüsselwort der Argument Name in der Q# Aufruf baren Definition ist.</span><span class="sxs-lookup"><span data-stu-id="d9fde-226">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="d9fde-227">Das heißt, `MeasureSuperpositionArray.simulate(n=4)` ist gültig, während `MeasureSuperpositionArray.simulate(4)` einen Fehler auslöst.</span><span class="sxs-lookup"><span data-stu-id="d9fde-227">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="d9fde-228">Daher ist das python-Host Programm</span><span class="sxs-lookup"><span data-stu-id="d9fde-228">Therefore, the Python host program</span></span> 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

<span data-ttu-id="d9fde-229">ergibt eine Ausgabe wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="d9fde-229">results in an output like the following:</span></span>

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[<span data-ttu-id="d9fde-230">C#</span><span class="sxs-lookup"><span data-stu-id="d9fde-230">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="d9fde-231">Ein c#-Host Programm verfügt über mehrere Komponenten, die eng mit einigen Komponenten des QDK funktionieren, z. b. die Simulatoren, die selbst auf c# basieren.</span><span class="sxs-lookup"><span data-stu-id="d9fde-231">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="d9fde-232">Der Q# Compiler arbeitet hier, indem er einen gleichwertig benannten c#-Namespace aus dem Q# Namespace in der Q# Datei erzeugt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-232">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="d9fde-233">Außerdem wird eine gleichwertig benannte c#-Klasse für jede der Q# darin definierten callables oder Typen generiert.</span><span class="sxs-lookup"><span data-stu-id="d9fde-233">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="d9fde-234">Zuerst werden alle Klassen, die in unserem Host Programm verwendet werden, mit-Anweisungen zur Verfügung gestellt `using` , die ungefähr mit den `open` Anweisungen in der Datei zusammengefügt werden Q# :</span><span class="sxs-lookup"><span data-stu-id="d9fde-234">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="d9fde-235">Als nächstes deklarieren wir unseren c#-Namespace, einige andere Bits und Teile (siehe den vollständigen Codeblock unten) und dann eine beliebige klassische Programmierung (z. b. das Berechnen von Argumenten für die Q# callables).</span><span class="sxs-lookup"><span data-stu-id="d9fde-235">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (e.g. computing arguments for the Q# callables).</span></span>
<span data-ttu-id="d9fde-236">Letzteres ist in diesem Fall nicht erforderlich, aber ein Beispiel für eine solche Verwendung finden Sie unter [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet)Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d9fde-236">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="d9fde-237">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="d9fde-237">Target machines</span></span>

<span data-ttu-id="d9fde-238">Bei der Rückkehr zu Q# müssen wir eine Instanz eines beliebigen Ziel Computers erstellen, auf dem wir unsere Vorgänge ausführen werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-238">Getting back to Q#, we must create an instance of whatever target machine we will execute our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="d9fde-239">Die Verwendung anderer Zielcomputer ist so einfach wie das Instanziieren eines anderen Ziel Computers, obwohl die Art und Weise der Rückgabe geringfügig abweichen kann.</span><span class="sxs-lookup"><span data-stu-id="d9fde-239">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="d9fde-240">Aus Gründen der Kürze bleiben wir an der [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) für die Zeit und fügen die [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [folgenden](#including-the-resources-estimator)Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="d9fde-240">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="d9fde-241">Jede aus den Vorgängen generierte c#-Klasse Q# verfügt über eine- `Run` Methode, wobei das erste Argument, das die Zielcomputer Instanz sein muss.</span><span class="sxs-lookup"><span data-stu-id="d9fde-241">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="d9fde-242">Daher `MeasureSuperposition` verwenden wir, um auf dem auszuführen `QuantumSimulator` `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-242">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="d9fde-243">Die zurückgegebenen Ergebnisse können dann Variablen in c# zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="d9fde-243">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="d9fde-244">Die `Run` -Methode wird asynchron ausgeführt, da dies die Groß-und Kleinschreibung für echte Quantum-Hardware ist. Daher blockiert das- `await` Schlüsselwort die weitere Ausführung, bis die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d9fde-244">The `Run` method is executed asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further execution until the task completes.</span></span>

<span data-ttu-id="d9fde-245">Wenn die Q# Aufruf Bare-Datei keine Rückgaben aufweist (d. h. den Rückgabetyp aufweist `Unit` ), kann die Ausführung weiterhin auf dieselbe Weise erfolgen, ohne Sie einer Variablen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-245">If the Q# callable does not have any returns (i.e. has return type `Unit`), then the execution can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="d9fde-246">In diesem Fall würde die gesamte Zeile einfach aus</span><span class="sxs-lookup"><span data-stu-id="d9fde-246">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="d9fde-247">Argumente</span><span class="sxs-lookup"><span data-stu-id="d9fde-247">Arguments</span></span>

<span data-ttu-id="d9fde-248">Alle Argumente für die Q# Aufruf baren werden einfach als zusätzliche Argumente an den Zielcomputer weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d9fde-248">Any arguments to the Q# callable are simply passed as additional arguments afer the target machine.</span></span>
<span data-ttu-id="d9fde-249">Daher werden die Ergebnisse von `MeasureSuperpositionArray` in `n=4` Qubits über</span><span class="sxs-lookup"><span data-stu-id="d9fde-249">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="d9fde-250">Ein vollständiges c#-Host Programm könnte daher wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-250">A full C# host program could thus look like</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

<span data-ttu-id="d9fde-251">Am Speicherort der c#-Datei kann das Host Programm von der Befehlszeile aus ausgeführt werden, indem Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="d9fde-251">At the location of the C# file, the host program can be run from the command line by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="d9fde-252">in diesem Fall wird die Ausgabe in die Konsole geschrieben, ähnlich wie</span><span class="sxs-lookup"><span data-stu-id="d9fde-252">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="d9fde-253">Aufgrund der Interoperabilität des Compilers mit Namespaces könnten wir unsere Q# callables ohne die-Anweisung verfügbar machen `using NamespaceName;` und den c#-Namespace Titel einfach zuordnen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-253">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="d9fde-254">Das heißt, indem durch ersetzt wird `namespace host` `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-254">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="d9fde-255">Einschließen der Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="d9fde-255">Including the resources estimator</span></span>

<span data-ttu-id="d9fde-256">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Erfordert eine etwas andere Implementierung zum Abrufen der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d9fde-256">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="d9fde-257">Anstatt Sie als Variable mit einer-Anweisung zu instanziieren `using` (wie dies bei der der Fall ist `QuantumSimulator` ), können wir die Objekte der Klasse über</span><span class="sxs-lookup"><span data-stu-id="d9fde-257">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="d9fde-258">Beachten Sie, dass anstelle eines einzelnen Ziel Simulators, der von mehreren Vorgängen verwendet werden soll Q# , jeweils eine instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-258">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="d9fde-259">Dies liegt daran, dass die Objekte selbst geändert werden, wenn Sie als Zielcomputer verwendet werden, und ihre Ergebnisse anschließend mit der-Klassenmethode abgerufen werden können `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-259">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="d9fde-260">Zum Ausführen der Vorgänge für die Ressourcenschätzung verwenden wir</span><span class="sxs-lookup"><span data-stu-id="d9fde-260">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="d9fde-261">und dann die Ergebnisse als durch Tabstopps getrennte Werte (TSV) mit `estimatorSingleQ.ToTSV()` und Abrufen `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="d9fde-261">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="d9fde-262">Ein vollständiges c#-Host Programm, das sowohl den als auch den verwendet, könnte das folgende Format haben `QuantumSimulator` `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="d9fde-262">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


<span data-ttu-id="d9fde-263">Dies ergibt eine Ausgabe ähnlich der</span><span class="sxs-lookup"><span data-stu-id="d9fde-263">which would yield output similar to</span></span>

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="d9fde-264">Q#Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="d9fde-264">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="d9fde-265">Q#Jupyter-Notebooks verwenden den I Q# -Kernel, mit dem Sie callables in einem einzigen Notebook definieren, kompilieren und ausführen können, Q# ---alle neben Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-265">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="d9fde-266">Dies bedeutet, dass es zwar möglich ist, den Inhalt von Dateien zu importieren und zu verwenden `*.qs` Q# , aber im Ausführungs Modell nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="d9fde-266">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the execution model.</span></span>

<span data-ttu-id="d9fde-267">Hier wird ausführlich erläutert, wie die Q# oben definierten Vorgänge ausgeführt werden, aber eine umfassendere Einführung in die Verwendung Q# von jupyter Notebooks finden Sie unter Einführung [in Q# und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="d9fde-267">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="d9fde-268">Definieren von Vorgängen</span><span class="sxs-lookup"><span data-stu-id="d9fde-268">Defining operations</span></span>

<span data-ttu-id="d9fde-269">In einem Q# Jupyter Notebook geben Sie den Q# Code genau so ein, wie er im Namespace einer Q# Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="d9fde-269">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="d9fde-270">Daher können wir den Zugriff auf callables aus den [ Q# Standardbibliotheken](xref:microsoft.quantum.qsharplibintro) mit `open` Anweisungen für die jeweiligen Namespaces aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d9fde-270">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.qsharplibintro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="d9fde-271">Wenn eine Zelle mit einer solchen Anweisung ausgeführt wird, sind die Definitionen aus diesen Namespaces im gesamten Arbeitsbereich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9fde-271">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="d9fde-272">Callables von [Microsoft. Quantum. intrinsisch](xref:microsoft.quantum.intrinsic) und [Microsoft. Quantum. Canon](xref:microsoft.quantum.canon) (z. b. [`H`](xref:microsoft.quantum.intrinsic.h) und [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) stehen automatisch für Vorgänge zur Verfügung, die in Zellen in Q# jupyter-Notebooks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d9fde-272">Callables from [Microsoft.Quantum.Intrinsic](xref:microsoft.quantum.intrinsic) and [Microsoft.Quantum.Canon](xref:microsoft.quantum.canon) (e.g. [`H`](xref:microsoft.quantum.intrinsic.h) and [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="d9fde-273">Dies gilt jedoch nicht für Code, der aus externen Q# Quelldateien eingefügt wurde (ein Prozess, der bei Einführung [zu Q# und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="d9fde-273">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="d9fde-274">Ebenso erfordert die Definition von Vorgängen lediglich das Schreiben des Q# Codes und das Ausführen der Zelle.</span><span class="sxs-lookup"><span data-stu-id="d9fde-274">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

<span data-ttu-id="d9fde-275">In der Ausgabe werden dann diese Vorgänge aufgelistet, die aus zukünftigen Zellen aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="d9fde-275">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="d9fde-276">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="d9fde-276">Target machines</span></span>

<span data-ttu-id="d9fde-277">Die Funktionen zum Ausführen von Vorgängen auf bestimmten Ziel Computern werden über [I Q# Magic-Befehle](xref:microsoft.quantum.guide.quickref.iqsharp)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d9fde-277">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="d9fde-278">Beispielsweise `%simulate` verwendet die `QuantumSimulator` , und `%estimate` verwendet Folgendes `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="d9fde-278">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="d9fde-279">Übergeben von Eingaben an Funktionen und Vorgänge</span><span class="sxs-lookup"><span data-stu-id="d9fde-279">Passing inputs to functions and operations</span></span>

<span data-ttu-id="d9fde-280">Derzeit können die Befehle zum Ausführen von Magic nur mit Vorgängen verwendet werden, die keine Argumente annehmen.</span><span class="sxs-lookup"><span data-stu-id="d9fde-280">Currently the execution magic commands can only be used with operations that take no arguments.</span></span> <span data-ttu-id="d9fde-281">Zum Ausführen von `MeasureSuperpositionArray` müssen wir also einen Wrapper Vorgang definieren, der dann den Vorgang mit den Argumenten aufruft:</span><span class="sxs-lookup"><span data-stu-id="d9fde-281">So, to run `MeasureSuperpositionArray`, we need to define a "wrapper" operation which then calls the operation with the arguments:</span></span>

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

<span data-ttu-id="d9fde-282">Dieser Vorgang kann natürlich auch mit `%estimate` und anderen Ausführungs Befehlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9fde-282">This operation can of course be used similarly with `%estimate` and other execution commands.</span></span>
