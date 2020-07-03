---
title: 'Möglichkeiten zum Ausführen eines Q #-Programms'
description: 'Übersicht über die verschiedenen Möglichkeiten zum Ausführen von Q #-Programmen. Über die Befehlszeile, Q # jupyter Notebooks und klassische Host Programme in Python oder einer .NET-Sprache.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
ms.openlocfilehash: 132c138d7c392ed2b4bd3d0079180b68adae4cfc
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85887683"
---
# <a name="ways-to-run-a-q-program"></a><span data-ttu-id="5322a-104">Möglichkeiten zum Ausführen eines Q #-Programms</span><span class="sxs-lookup"><span data-stu-id="5322a-104">Ways to run a Q# program</span></span>

<span data-ttu-id="5322a-105">Eines der größten Stärken des quantumentwicklungskit ist seine Flexibilität über Plattformen und Entwicklungsumgebungen hinweg.</span><span class="sxs-lookup"><span data-stu-id="5322a-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="5322a-106">Dies bedeutet jedoch auch, dass neue Q #-Benutzer von den zahlreichen Optionen im [Installationshandbuch](xref:microsoft.quantum.install)möglicherweise verwirrt oder überlastet werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="5322a-107">Auf dieser Seite erklären wir, was geschieht, wenn ein Q #-Programm ausgeführt wird, und vergleichen die verschiedenen Möglichkeiten, wie Benutzer dies tun können.</span><span class="sxs-lookup"><span data-stu-id="5322a-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="5322a-108">Ein primärer Unterschied besteht darin, dass Q # ausgeführt werden kann:</span><span class="sxs-lookup"><span data-stu-id="5322a-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="5322a-109">als eigenständige Anwendung, bei der Q # die einzige beteiligte Sprache ist und das Programm direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="5322a-110">Zwei Methoden fallen tatsächlich in diese Kategorie:</span><span class="sxs-lookup"><span data-stu-id="5322a-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="5322a-111">die Befehlszeilenschnittstelle</span><span class="sxs-lookup"><span data-stu-id="5322a-111">the command line interface</span></span>
  - <span data-ttu-id="5322a-112">Jupyter Notebook-Instanzen in Q#</span><span class="sxs-lookup"><span data-stu-id="5322a-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="5322a-113">mit einem zusätzlichen *Host Programm*, das in Python oder einer .NET-Sprache (z. b. c# oder F #) geschrieben ist, die dann das Programm aufruft und die zurückgegebenen Ergebnisse weiterverarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5322a-113">with an additional *host program*, written in Python or a .NET language (e.g. C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="5322a-114">Um diese Prozesse und deren Unterschiede zu verstehen, wird ein einfaches Q #-Programm berücksichtigt und die Art und Weise erläutert, wie Sie ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5322a-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be executed.</span></span>

## <a name="basic-q-program"></a><span data-ttu-id="5322a-115">Einfaches Q #-Programm</span><span class="sxs-lookup"><span data-stu-id="5322a-115">Basic Q# program</span></span>

<span data-ttu-id="5322a-116">Ein grundlegendes Quantum-Programm besteht möglicherweise aus der Vorbereitung eines Qubit in derselben Superposition in den Zuständen $ \ket {0} $ und $ \ket {1} $, wobei es gemessen wird und das Ergebnis zurückgegeben wird. dabei wird entweder einer dieser beiden Zustände mit gleicher Wahrscheinlichkeit nach dem Zufallsprinzip verwendet.</span><span class="sxs-lookup"><span data-stu-id="5322a-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="5322a-117">Tatsächlich ist dieser Prozess der Kern des Schnellstarts des [Quantum-Zufallszahlen-Generators](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="5322a-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="5322a-118">In f # wird dies durch den folgenden Code durchgeführt:</span><span class="sxs-lookup"><span data-stu-id="5322a-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="5322a-119">Dieser Code allein kann jedoch nicht von Q # ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-119">However, this code alone can't be executed by Q#.</span></span>
<span data-ttu-id="5322a-120">Dafür muss der Text eines [Vorgangs](xref:microsoft.quantum.guide.basics#q-operations-and-functions), der dann ausgeführt wird, wenn er---direkt oder durch einen anderen Vorgang aufgerufen wird, ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.guide.basics#q-operations-and-functions), which is then executed when called---either directly or by another operation.</span></span> <span data-ttu-id="5322a-121">Daher können Sie einen Vorgang der folgenden Form schreiben:</span><span class="sxs-lookup"><span data-stu-id="5322a-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="5322a-122">Sie haben einen Vorgang definiert, `MeasureSuperposition` der keine Eingaben annimmt und einen Wert vom Typ [Result](xref:microsoft.quantum.guide.types)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5322a-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="5322a-123">Obwohl die Beispiele auf dieser Seite nur aus q #- *Vorgängen*bestehen, werden alle Konzepte, die wir erörtern werden, gleichermaßen für die f #- *Funktionen*verwendet. daher bezeichnen wir Sie zusammen als *callables*.</span><span class="sxs-lookup"><span data-stu-id="5322a-123">While the examples on this page only consist of Q# *operations*, all of the concepts we will discuss pertain equally to Q# *functions*, and therefore we refer to them collectively as *callables*.</span></span> <span data-ttu-id="5322a-124">Die Unterschiede werden unter [Q # Basics: Vorgänge und Funktionen](xref:microsoft.quantum.guide.basics#q-operations-and-functions)erläutert. Weitere Informationen zur Definition finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="5322a-124">Their differences are discussed at [Q# basics: operations and functions](xref:microsoft.quantum.guide.basics#q-operations-and-functions), and more details on defining them can be found at [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

### <a name="callable-defined-in-a-q-file"></a><span data-ttu-id="5322a-125">In einer Q #-Datei definierte Aufruf Bare Datei</span><span class="sxs-lookup"><span data-stu-id="5322a-125">Callable defined in a Q# file</span></span>

<span data-ttu-id="5322a-126">Die Aufruf Bare ist genau das, was von Q # aufgerufen und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-126">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="5322a-127">Allerdings sind einige weitere Ergänzungen erforderlich, um eine vollständige `*.qs` Q #-Datei zu bilden.</span><span class="sxs-lookup"><span data-stu-id="5322a-127">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="5322a-128">Alle Q #-Typen und callables (sowohl die, die Sie definieren, als auch die in der Sprache intrinsisch) werden innerhalb von *Namespaces*definiert, die jeweils einen vollständigen Namen bereitstellen, auf den dann verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5322a-128">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="5322a-129">Beispielsweise befinden sich die [`H`](xref:microsoft.quantum.intrinsic.h) -und- [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) Vorgänge im [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) - [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) Namespace und im-Namespace (Teil der [Q # Standard-Bibliotheken](xref:microsoft.quantum.qsharplibintro)).</span><span class="sxs-lookup"><span data-stu-id="5322a-129">For example, the [`H`](xref:microsoft.quantum.intrinsic.h) and [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.qsharplibintro)).</span></span>
<span data-ttu-id="5322a-130">Daher können Sie immer über die *vollständigen* Namen und aufgerufen werden `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` . Dies führt jedoch zu einem sehr überlasteten Code.</span><span class="sxs-lookup"><span data-stu-id="5322a-130">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="5322a-131">Stattdessen `open` ermöglichen-Anweisungen, dass auf Aufruf Bare Elemente mit präziseren Kurzform verwiesen wird, wie dies im obigen Vorgangs Text geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="5322a-131">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="5322a-132">Die vollständige f #-Datei, die den Vorgang enthält, besteht daher darin, einen eigenen Namespace zu definieren, die Namespaces für die von unserem Vorgang verwendeten callables zu öffnen, und dann den Vorgang:</span><span class="sxs-lookup"><span data-stu-id="5322a-132">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

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
> <span data-ttu-id="5322a-133">Namespaces können auch beim Öffnen einen *Alias* aufweisen. Dies kann hilfreich sein, wenn Aufruf Bare/Typnamen in zwei Namespaces in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="5322a-133">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="5322a-134">Beispielsweise könnten wir stattdessen oben verwenden `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` und dann `H` via anrufen `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="5322a-134">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="5322a-135">Eine Ausnahme ist der [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) Namespace, der immer automatisch geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-135">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="5322a-136">Daher können callables wie [`Length`](xref:microsoft.quantum.core.length) immer direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-136">Therefore, callables like [`Length`](xref:microsoft.quantum.core.length) can always be used directly.</span></span>

### <a name="execution-on-target-machines"></a><span data-ttu-id="5322a-137">Ausführung auf Ziel Computern</span><span class="sxs-lookup"><span data-stu-id="5322a-137">Execution on target machines</span></span>

<span data-ttu-id="5322a-138">Nun wird das allgemeine Ausführungs Modell eines f #-Programms deutlich.</span><span class="sxs-lookup"><span data-stu-id="5322a-138">Now the general execution model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="5322a-139">Zum einen hat die spezifische Aufruf Bare, die ausgeführt werden kann, Zugriff auf alle anderen callables und Typen, die im selben Namespace definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-139">Firstly, the specific callable to be executed has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="5322a-140">Außerdem greifen Sie auf die Bibliotheken aus einer der [Q #-Bibliotheken](xref:microsoft.quantum.libraries)zu, aber auf diese muss entweder über den vollständigen Namen oder über die `open` oben beschriebenen Anweisungen verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-140">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="5322a-141">Die Aufruf Bare selbst wird dann auf einem *[Zielcomputer](xref:microsoft.quantum.machines)* ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5322a-141">The callable itself is then executed on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="5322a-142">Bei solchen Ziel Computern kann es sich um tatsächliche Quantum-Hardware oder mehrere Simulatoren handeln, die als Teil des QDK verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-142">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="5322a-143">Zu diesem Zweck ist der nützlichste Zielcomputer eine Instanz des [vollständigen Simulators](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , der das Verhalten des Programms so berechnet, als ob es auf einem Rausch freien Quantum-Computer ausgeführt würde.</span><span class="sxs-lookup"><span data-stu-id="5322a-143">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being executed on a noise-free quantum computer.</span></span>

<span data-ttu-id="5322a-144">Bisher haben wir beschrieben, was geschieht, wenn ein bestimmtes Q # Callable-Element ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-144">So far, we've described what happens when a specific Q# callable is being executed.</span></span>
<span data-ttu-id="5322a-145">Unabhängig davon, ob Q # in einer eigenständigen Anwendung oder einem Host Programm verwendet wird, ist dieser allgemeine Prozess mehr oder weniger identisch---daher die Flexibilität des QDK.</span><span class="sxs-lookup"><span data-stu-id="5322a-145">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="5322a-146">Die Unterschiede zwischen den verschiedenen Methoden zum Aufrufen von Quantum Development Kit zeigen sich daher selbst, wie die Ausführung von Q # Callable aufgerufen wird und *wie* alle Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-146">The differences between the different ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be executed, and in what manner any results are returned.</span></span>
<span data-ttu-id="5322a-147">Genauer gesagt werden die Unterschiede im Zusammenhang mit</span><span class="sxs-lookup"><span data-stu-id="5322a-147">More specifically, the differences revolve around</span></span> 
1. <span data-ttu-id="5322a-148">Es wird angegeben, welche Q # Callable ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5322a-148">indicating which Q# callable is to be executed,</span></span>
2. <span data-ttu-id="5322a-149">Gibt an, wie potenzielle Aufruf Bare Argumente bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-149">how potential callable arguments are provided,</span></span>
3. <span data-ttu-id="5322a-150">Angeben des Ziel Computers, auf dem der Computer ausgeführt werden soll, und</span><span class="sxs-lookup"><span data-stu-id="5322a-150">specifying the target machine on which to execute it, and</span></span>
4. <span data-ttu-id="5322a-151">Gibt an, wie alle Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-151">how any results are returned.</span></span>

<span data-ttu-id="5322a-152">Zuerst wird erläutert, wie dies mit der eigenständigen f #-Anwendung über die Befehlszeile erfolgt, und anschließend können Sie mit der Verwendung von Python-und c#-Host Programmen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="5322a-152">First, we discuss how this is done with the Q# standalone application from the command line, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="5322a-153">Wir reservieren die eigenständige Anwendung der q # jupyter-Notebooks für das letzte, da die primäre Funktionalität im Gegensatz zu den ersten drei nicht in einer lokalen q #-Datei liegt.</span><span class="sxs-lookup"><span data-stu-id="5322a-153">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="5322a-154">Obwohl wir dies in diesen Beispielen nicht veranschaulichen, besteht eine Gemeinsamkeit zwischen den Ausführungsmethoden darin, dass alle Nachrichten, die aus dem Q #-Programm gedruckt werden (z. b. über [`Message`](xref:microsoft.quantum.intrinsic.message) oder [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), in der Regel immer in der jeweiligen Konsole gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-154">Although we don't illustrate it in these examples, one commonality between the execution methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:microsoft.quantum.intrinsic.message) or [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="q-from-the-command-line"></a><span data-ttu-id="5322a-155">F # von der Befehlszeile aus</span><span class="sxs-lookup"><span data-stu-id="5322a-155">Q# from the command line</span></span>
<span data-ttu-id="5322a-156">Eine der einfachsten Möglichkeiten, Q #-Programme zu schreiben, besteht darin, die Gedanken über separate Dateien und eine zweite Sprache vollständig zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="5322a-156">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="5322a-157">Die Verwendung von Visual Studio Code oder Visual Studio mit der QDK-Erweiterung ermöglicht einen nahtlosen Workflow, bei dem wir q #-callables nur aus einer einzelnen q #-Datei ausführen.</span><span class="sxs-lookup"><span data-stu-id="5322a-157">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="5322a-158">Hierzu wird die Ausführung des Programms letztendlich aufgerufen, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="5322a-158">For this, we will ultimately invoke the program's execution by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="5322a-159">in der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="5322a-159">in the command line.</span></span>
<span data-ttu-id="5322a-160">Der einfachste Workflow ist, wenn der Verzeichnis Speicherort des Terminals mit der q #-Datei identisch ist, die mit der q #-Dateibearbeitung problemlos über das integrierte Terminal in vs Code behandelt werden kann, z. b..</span><span class="sxs-lookup"><span data-stu-id="5322a-160">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="5322a-161">Der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) akzeptiert jedoch zahlreiche Optionen, und das Programm kann auch an einem anderen Speicherort ausgeführt werden, indem einfach `--project <PATH>` der Speicherort der Q #-Datei bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-161">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-q-file"></a><span data-ttu-id="5322a-162">Einstiegspunkt zu Q #-Datei hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5322a-162">Add entry point to Q# file</span></span>

<span data-ttu-id="5322a-163">Die meisten Q #-Dateien enthalten mehr als eine Aufruf Bare Funktion. Daher muss der Compiler wissen, *welche* Callable ausgeführt werden soll, wenn der Befehl bereitgestellt wird `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="5322a-163">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to execute when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="5322a-164">Dies erfolgt mit einer einfachen Änderung an der Q #-Datei selbst:</span><span class="sxs-lookup"><span data-stu-id="5322a-164">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="5322a-165">Fügen Sie eine Zeile hinzu, `@EntryPoint()` die direkt vor dem Aufruf baren steht.</span><span class="sxs-lookup"><span data-stu-id="5322a-165">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="5322a-166">Unsere Datei von oben wird daher</span><span class="sxs-lookup"><span data-stu-id="5322a-166">Our file from above would therefore become</span></span>
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

<span data-ttu-id="5322a-167">Nun `dotnet run` führt ein-Befehl von der Befehlszeile aus `MeasureSuperposition` , um ausgeführt zu werden, und der zurückgegebene Wert wird dann direkt in das Terminal gedruckt.</span><span class="sxs-lookup"><span data-stu-id="5322a-167">Now, a call of `dotnet run` from the command line leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="5322a-168">Daher wird entweder `One` oder `Zero` gedruckt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5322a-168">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="5322a-169">Beachten Sie, dass es keine Rolle spielt, ob weitere Aufruf Bare aufruben definiert sind, sondern nur `MeasureSuperposition` ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-169">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="5322a-170">Außerdem ist es kein Problem, wenn die Aufruf Bare-Datei vor der Deklaration [Dokumentations Kommentare](xref:microsoft.quantum.guide.filestructure#documentation-comments) enthält `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="5322a-170">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.guide.filestructure#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="5322a-171">Aufruf Bare Argumente</span><span class="sxs-lookup"><span data-stu-id="5322a-171">Callable arguments</span></span>

<span data-ttu-id="5322a-172">Bisher haben wir nur einen Vorgang in Erwägung gezogen, der keine Eingaben annimmt.</span><span class="sxs-lookup"><span data-stu-id="5322a-172">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="5322a-173">Angenommen, wir wollten einen ähnlichen Vorgang durchführen, aber auf mehreren Qubits---die Zahl als Argument bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5322a-173">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="5322a-174">Ein solcher Vorgang könnte als</span><span class="sxs-lookup"><span data-stu-id="5322a-174">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="5322a-175">Dabei ist der zurückgegebene Wert ein Array der Messergebnisse.</span><span class="sxs-lookup"><span data-stu-id="5322a-175">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="5322a-176">Beachten Sie, dass [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) und [`ForEach`](xref:microsoft.quantum.arrays.foreach) sich im [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) -Namespace und im- [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) Namespace befinden, `open` wobei jeweils zusätzliche Anweisungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-176">Note that [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) and [`ForEach`](xref:microsoft.quantum.arrays.foreach) are in the [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) and [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="5322a-177">Wenn Sie das `@EntryPoint()` Attribut vor diesem neuen Vorgang verschieben (Beachten Sie, dass es nur eine Zeile in einer Datei geben kann), und wenn Sie versuchen, es mit einfach auszuführen, führt dies zu `dotnet run` einer Fehlermeldung, die angibt, welche zusätzlichen Befehlszeilenoptionen erforderlich sind, und wie Sie Sie Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="5322a-177">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command line options are required, and how to express them.</span></span>

<span data-ttu-id="5322a-178">Das allgemeine Format für die Befehlszeile ist tatsächlich `dotnet run [options]` , und es werden Aufruf Bare Argumente dort bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5322a-178">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="5322a-179">In diesem Fall fehlt das Argument `n` , und es wird angezeigt, dass die Option bereitgestellt werden muss `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="5322a-179">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="5322a-180">Zum Ausführen `MeasureSuperpositionArray` von for `n=4` Qubits verwenden wir daher</span><span class="sxs-lookup"><span data-stu-id="5322a-180">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="5322a-181">Ausgabe ähnlich</span><span class="sxs-lookup"><span data-stu-id="5322a-181">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="5322a-182">Dies reicht natürlich auf mehrere Argumente aus.</span><span class="sxs-lookup"><span data-stu-id="5322a-182">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="5322a-183">In definierte Argument Namen `camelCase` werden vom Compiler leicht geändert, damit Sie als f #-Eingaben akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-183">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="5322a-184">Wenn z. b. anstelle von `n` der oben genannte Name verwendet wird `numQubits` , wird diese Eingabe in der Befehlszeile über `--num-qubits 4` anstelle von bereitgestellt `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="5322a-184">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="5322a-185">Die Fehlermeldung enthält auch weitere Optionen, die verwendet werden können, einschließlich Informationen zum Ändern des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="5322a-185">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="5322a-186">Verschiedene Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="5322a-186">Different target machines</span></span>

<span data-ttu-id="5322a-187">Da die Ausgaben unserer Vorgänge bisher die erwarteten Ergebnisse ihrer Aktion in echten Qubits waren, ist es klar, dass der Standardziel Computer von der Befehlszeile aus der vollständige quauntum-Simulator ist `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="5322a-187">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quauntum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="5322a-188">Wir können jedoch Aufruf Bare Aufrufe anweisen, die auf einem bestimmten Zielcomputer mit der Option `--simulator` (oder der kurzseite `-s` ) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-188">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="5322a-189">Beispielsweise können wir die Anwendung unter Ausführen [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="5322a-189">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="5322a-190">Die gedruckte Ausgabe lautet dann</span><span class="sxs-lookup"><span data-stu-id="5322a-190">The printed output is then</span></span>

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

<span data-ttu-id="5322a-191">Ausführliche Informationen dazu, was diese Metriken angeben, finden Sie unter [Ressourcenschätzung: gemeldete Metriken](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span><span class="sxs-lookup"><span data-stu-id="5322a-191">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-execution-summary"></a><span data-ttu-id="5322a-192">Zusammenfassung der Befehlszeilen Ausführung</span><span class="sxs-lookup"><span data-stu-id="5322a-192">Command line execution summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-q-dotnet-run-options"></a><span data-ttu-id="5322a-193">Nicht-Q #- `dotnet run` Optionen</span><span class="sxs-lookup"><span data-stu-id="5322a-193">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="5322a-194">Wie bereits kurz erwähnt `--project` , akzeptiert der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) auch Optionen, die nicht mit den Q # Callable-Argumenten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-194">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="5322a-195">Wenn beide Arten von Optionen bereit `dotnet` gestellt werden, müssen zuerst die-spezifischen Optionen, gefolgt von einem Trennzeichen `--` , und dann die Q #-spezifischen Optionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-195">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="5322a-196">Beispielsweise würde die Angabe eines Pfads zusammen mit einer Zahlen-Qubits für den obigen Vorgang über ausgeführt werden `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="5322a-196">For example, specifiying a path along with a number qubits for the operation above would be executed via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="q-with-host-programs"></a><span data-ttu-id="5322a-197">Q # mit Host Programmen</span><span class="sxs-lookup"><span data-stu-id="5322a-197">Q# with host programs</span></span>

<span data-ttu-id="5322a-198">Mit unserer f #-Datei besteht eine Alternative zum Aufrufen eines Vorgangs oder einer Funktion direkt über die Befehlszeile darin, ein *Host Programm* in einer anderen klassischen Sprache zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5322a-198">With our Q# file in hand, an alternative to calling an operation or function directly from the command line is to use a *host program* in another classical language.</span></span> <span data-ttu-id="5322a-199">Dies kann insbesondere mit Python oder einer .NET-Sprache (z. b. c# oder F #) erfolgen (aus Gründen der Kürze wird c# hier nur ausführlich erläutert).</span><span class="sxs-lookup"><span data-stu-id="5322a-199">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="5322a-200">Zum Aktivieren der Interoperabilität ist ein wenig mehr Setup erforderlich. diese Details finden Sie jedoch in den [Installations](xref:microsoft.quantum.install)Handbüchern.</span><span class="sxs-lookup"><span data-stu-id="5322a-200">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="5322a-201">Kurz gesagt, enthält die Situation nun eine Host Programmdatei (z. b. `*.py` oder `*.cs` ) am gleichen Speicherort wie unsere Q #-Datei.</span><span class="sxs-lookup"><span data-stu-id="5322a-201">In a nutshell, the situation now includes a host program file (e.g. `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="5322a-202">Es ist jetzt das *Host* Programm, das ausgeführt wird, und im Verlauf seiner Ausführung kann es bestimmte q #-Vorgänge und-Funktionen aus der q #-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="5322a-202">It's now the *host* program that gets run, and in the course of its execution it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="5322a-203">Der Kern der Interoperabilität basiert auf dem f #-Compiler, der den Inhalt der q #-Datei für das Host Programm zugänglich macht, sodass Sie aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="5322a-203">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="5322a-204">Einer der Hauptvorteile der Verwendung eines Host Programms besteht darin, dass die vom Q #-Programm zurückgegebenen klassischen Daten dann in der Host Sprache weiterverarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="5322a-204">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="5322a-205">Dies kann aus einer erweiterten Datenverarbeitung bestehen (z. b. etwas, das nicht intern in Q # ausgeführt werden kann), und anschließend weitere Q #-Aktionen auf der Grundlage dieser Ergebnisse oder etwas so einfach wie das Zeichnen der q #-Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="5322a-205">This could consist of some advanced data processing (e.g. something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="5322a-206">Das allgemeine Schema wird hier angezeigt, und wir erörtern die spezifischen Implementierungen für python und c# weiter unten.</span><span class="sxs-lookup"><span data-stu-id="5322a-206">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="5322a-207">Ein Beispiel für die Verwendung eines F #-Host Programms finden Sie unter [.net-Interoperabilitäts Beispiele](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="5322a-207">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="5322a-208">Das `@EntryPoint()` für Q #-Befehlszeilen Anwendungen verwendete Attribut kann nicht mit Host Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-208">The `@EntryPoint()` attribute used for Q# command line applications cannot be used with host programs.</span></span>
> <span data-ttu-id="5322a-209">Wenn Sie in der von einem Host aufgerufenen Q #-Datei vorhanden ist, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="5322a-209">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="5322a-210">Um mit unterschiedlichen Host Programmen arbeiten zu können, sind keine Änderungen an einer `*.qs` Q #-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5322a-210">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="5322a-211">Die folgenden Host Programm Implementierungen funktionieren alle mit derselben Q #-Datei:</span><span class="sxs-lookup"><span data-stu-id="5322a-211">The following host program implementations all work with the same Q# file:</span></span>

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

<span data-ttu-id="5322a-212">Wählen Sie die Registerkarte aus, die der gewünschten Host Sprache entspricht.</span><span class="sxs-lookup"><span data-stu-id="5322a-212">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="5322a-213">Python</span><span class="sxs-lookup"><span data-stu-id="5322a-213">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="5322a-214">Ein python-Host Programm wird wie folgt erstellt:</span><span class="sxs-lookup"><span data-stu-id="5322a-214">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="5322a-215">Importieren Sie das- `qsharp` Modul, das das Modul Lade Modul für die Q #-Interoperabilität registriert.</span><span class="sxs-lookup"><span data-stu-id="5322a-215">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="5322a-216">Dadurch können q #-Namespaces als Python-Module angezeigt werden, aus denen Sie q #-callables importieren können.</span><span class="sxs-lookup"><span data-stu-id="5322a-216">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="5322a-217">Beachten Sie, dass es sich nicht um die selbst importierenden Q #-callables handelt, sondern um die python-stubweise, die das Aufrufen in Sie ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5322a-217">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="5322a-218">Diese werden dann als Objekte von python-Klassen verwendet, auf denen Methoden zum Angeben der Zielcomputer verwendet werden, an die der Vorgang zur Ausführung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-218">These then behave as objects of Python classes, on which we use methods to specify the target machines to send the operation to for execution.</span></span>

2. <span data-ttu-id="5322a-219">Importieren Sie die f #-callables, die wir direkt aufrufen---in diesem Fall `MeasureSuperposition` und `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="5322a-219">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="5322a-220">Wenn `qsharp` Sie das Modul importiert haben, können Sie auch callables direkt aus den Q # Library-Namespaces importieren.</span><span class="sxs-lookup"><span data-stu-id="5322a-220">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="5322a-221">Unter jedem anderen Python-Code können Sie jetzt diese callables auf bestimmten Ziel Computern aufrufen und ihre Rückgaben den Variablen (wenn Sie einen Wert zurückgeben) zur weiteren Verwendung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="5322a-221">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="5322a-222">Angeben von Ziel Computern</span><span class="sxs-lookup"><span data-stu-id="5322a-222">Specifying target machines</span></span>
<span data-ttu-id="5322a-223">Das Aufrufen eines Vorgangs, der auf einem bestimmten Zielcomputer ausgeführt werden soll, erfolgt über verschiedene python-Methoden auf dem importierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="5322a-223">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="5322a-224">Beispielsweise `.simulate(<args>)` verwendet die `QuantumSimulator` zum Ausführen des Vorgangs, während `.estimate_resources(<args>)` dies in der erfolgt `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="5322a-224">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="5322a-225">Übergeben von Eingaben an Q\#</span><span class="sxs-lookup"><span data-stu-id="5322a-225">Passing inputs to Q\#</span></span>
<span data-ttu-id="5322a-226">Argumente für q # Callable sollten in Form eines Schlüsselwort Arguments bereitgestellt werden, wobei das Schlüsselwort der Argument Name in der Q # Callable-Definition ist.</span><span class="sxs-lookup"><span data-stu-id="5322a-226">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="5322a-227">Das heißt, `MeasureSuperpositionArray.simulate(n=4)` ist gültig, während `MeasureSuperpositionArray.simulate(4)` einen Fehler auslöst.</span><span class="sxs-lookup"><span data-stu-id="5322a-227">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="5322a-228">Daher ist das python-Host Programm</span><span class="sxs-lookup"><span data-stu-id="5322a-228">Therefore, the Python host program</span></span> 

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

<span data-ttu-id="5322a-229">ergibt eine Ausgabe wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="5322a-229">results in an output like the following:</span></span>

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[<span data-ttu-id="5322a-230">C#</span><span class="sxs-lookup"><span data-stu-id="5322a-230">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="5322a-231">Ein c#-Host Programm verfügt über mehrere Komponenten, die eng mit einigen Komponenten des QDK funktionieren, z. b. die Simulatoren, die selbst auf c# basieren.</span><span class="sxs-lookup"><span data-stu-id="5322a-231">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="5322a-232">Der f #-Compiler funktioniert hier, indem er einen gleichwertig benannten c#-Namespace aus dem q #-Namespace in unserer q #-Datei erzeugt.</span><span class="sxs-lookup"><span data-stu-id="5322a-232">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="5322a-233">Außerdem wird eine gleichwertig benannte c#-Klasse für jeden der Q #-callables oder-Typen generiert, die darin definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-233">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="5322a-234">Zuerst werden alle Klassen, die in unserem Host Programm verwendet werden, mit-Anweisungen zur Verfügung gestellt `using` , die ungefähr mit den `open` Anweisungen in unserer Q #-Datei zu tun haben:</span><span class="sxs-lookup"><span data-stu-id="5322a-234">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="5322a-235">Als nächstes deklarieren wir den c#-Namespace, einige andere Bits und Teile (siehe den vollständigen Codeblock unten) und dann eine beliebige klassische Programmierung (z. b. das Berechnen von Argumenten für die Q # callables).</span><span class="sxs-lookup"><span data-stu-id="5322a-235">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (e.g. computing arguments for the Q# callables).</span></span>
<span data-ttu-id="5322a-236">Letzteres ist in diesem Fall nicht erforderlich, aber ein Beispiel für eine solche Verwendung finden Sie unter [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet)Beispiel.</span><span class="sxs-lookup"><span data-stu-id="5322a-236">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="5322a-237">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="5322a-237">Target machines</span></span>

<span data-ttu-id="5322a-238">Bei der Rückkehr zu f # müssen wir eine Instanz eines beliebigen Ziel Computers erstellen, auf dem wir unsere Vorgänge ausführen werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-238">Getting back to Q#, we must create an instance of whatever target machine we will execute our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="5322a-239">Die Verwendung anderer Zielcomputer ist so einfach wie das Instanziieren eines anderen Ziel Computers, obwohl die Art und Weise der Rückgabe geringfügig abweichen kann.</span><span class="sxs-lookup"><span data-stu-id="5322a-239">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="5322a-240">Aus Gründen der Kürze bleiben wir an der [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) für die Zeit und fügen die [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [folgenden](#including-the-resources-estimator)Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="5322a-240">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="5322a-241">Jede c#-Klasse, die aus den Q #-Vorgängen generiert wird, verfügt über eine- `Run` Methode, deren erstes Argument die Zielcomputer Instanz sein muss.</span><span class="sxs-lookup"><span data-stu-id="5322a-241">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="5322a-242">Daher `MeasureSuperposition` verwenden wir, um auf dem auszuführen `QuantumSimulator` `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="5322a-242">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="5322a-243">Die zurückgegebenen Ergebnisse können dann Variablen in c# zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="5322a-243">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="5322a-244">Die `Run` -Methode wird asynchron ausgeführt, da dies die Groß-und Kleinschreibung für echte Quantum-Hardware ist. Daher blockiert das- `await` Schlüsselwort die weitere Ausführung, bis die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5322a-244">The `Run` method is executed asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further execution until the task completes.</span></span>

<span data-ttu-id="5322a-245">Wenn das Q # Callable-Element keine Rückgaben aufweist (d. h. den Rückgabetyp aufweist `Unit` ), kann die Ausführung weiterhin auf dieselbe Weise erfolgen, ohne Sie einer Variablen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="5322a-245">If the Q# callable does not have any returns (i.e. has return type `Unit`), then the execution can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="5322a-246">In diesem Fall würde die gesamte Zeile einfach aus</span><span class="sxs-lookup"><span data-stu-id="5322a-246">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="5322a-247">Argumente</span><span class="sxs-lookup"><span data-stu-id="5322a-247">Arguments</span></span>

<span data-ttu-id="5322a-248">Alle Argumente für Q # Callable werden einfach als zusätzliche Argumente an den Zielcomputer weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="5322a-248">Any arguments to the Q# callable are simply passed as additional arguments afer the target machine.</span></span>
<span data-ttu-id="5322a-249">Daher werden die Ergebnisse von `MeasureSuperpositionArray` in `n=4` Qubits über</span><span class="sxs-lookup"><span data-stu-id="5322a-249">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="5322a-250">Ein vollständiges c#-Host Programm könnte daher wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="5322a-250">A full C# host program could thus look like</span></span>

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

<span data-ttu-id="5322a-251">Am Speicherort der c#-Datei kann das Host Programm von der Befehlszeile aus ausgeführt werden, indem Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="5322a-251">At the location of the C# file, the host program can be run from the command line by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="5322a-252">in diesem Fall wird die Ausgabe in die Konsole geschrieben, ähnlich wie</span><span class="sxs-lookup"><span data-stu-id="5322a-252">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="5322a-253">Aufgrund der Interoperabilität des Compilers mit Namespaces könnten wir unsere Q #-callables ohne die `using NamespaceName;` -Anweisung verfügbar machen und den c#-Namespace Titel einfach zuordnen.</span><span class="sxs-lookup"><span data-stu-id="5322a-253">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="5322a-254">Das heißt, indem durch ersetzt wird `namespace host` `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="5322a-254">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="5322a-255">Einschließen der Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="5322a-255">Including the resources estimator</span></span>

<span data-ttu-id="5322a-256">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Erfordert eine etwas andere Implementierung zum Abrufen der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5322a-256">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="5322a-257">Anstatt Sie als Variable mit einer-Anweisung zu instanziieren `using` (wie dies bei der der Fall ist `QuantumSimulator` ), können wir die Objekte der Klasse über</span><span class="sxs-lookup"><span data-stu-id="5322a-257">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="5322a-258">Beachten Sie, dass anstelle eines einzelnen Ziel Simulators, der von mehreren Q #-Vorgängen verwendet werden soll, jeweils eine instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="5322a-258">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="5322a-259">Dies liegt daran, dass die Objekte selbst geändert werden, wenn Sie als Zielcomputer verwendet werden, und ihre Ergebnisse anschließend mit der-Klassenmethode abgerufen werden können `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="5322a-259">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="5322a-260">Zum Ausführen der Vorgänge für die Ressourcenschätzung verwenden wir</span><span class="sxs-lookup"><span data-stu-id="5322a-260">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="5322a-261">und dann die Ergebnisse als durch Tabstopps getrennte Werte (TSV) mit `estimatorSingleQ.ToTSV()` und Abrufen `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="5322a-261">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="5322a-262">Ein vollständiges c#-Host Programm, das sowohl den als auch den verwendet, könnte das folgende Format haben `QuantumSimulator` `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="5322a-262">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

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


<span data-ttu-id="5322a-263">Dies ergibt eine Ausgabe ähnlich der</span><span class="sxs-lookup"><span data-stu-id="5322a-263">which would yield output similar to</span></span>

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

## <a name="q-jupyter-notebooks"></a><span data-ttu-id="5322a-264">Jupyter Notebook-Instanzen in Q#</span><span class="sxs-lookup"><span data-stu-id="5322a-264">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="5322a-265">Q # jupyter Notebooks nutzen den IQ #-Kernel, mit dem Sie q #-callables in einem einzigen Notebook definieren, kompilieren und ausführen können---zusammen mit Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="5322a-265">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="5322a-266">Dies bedeutet, dass es zwar möglich ist, den Inhalt von Q #-Dateien zu importieren und zu verwenden `*.qs` , aber im Ausführungs Modell nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-266">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the execution model.</span></span>

<span data-ttu-id="5322a-267">Hier wird ausführlich erläutert, wie die oben beschriebenen q #-Vorgänge ausgeführt werden, aber eine umfassendere Einführung in die Verwendung von q # jupyter Notebooks finden Sie unter Einführung [in q # und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="5322a-267">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="5322a-268">Definieren von Vorgängen</span><span class="sxs-lookup"><span data-stu-id="5322a-268">Defining operations</span></span>

<span data-ttu-id="5322a-269">In einem q #-Jupyter Notebook geben Sie f #-Code genau so ein, wie es im Namespace einer q #-Datei der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="5322a-269">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="5322a-270">Daher können wir den Zugriff auf callables aus den [Q # Standard-Bibliotheken](xref:microsoft.quantum.qsharplibintro) mit `open` Anweisungen für die jeweiligen Namespaces aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5322a-270">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.qsharplibintro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="5322a-271">Wenn eine Zelle mit einer solchen Anweisung ausgeführt wird, sind die Definitionen aus diesen Namespaces im gesamten Arbeitsbereich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5322a-271">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="5322a-272">Callables von [Microsoft. Quantum. intrinsisch](xref:microsoft.quantum.intrinsic) und [Microsoft. Quantum. Canon](xref:microsoft.quantum.canon) (z. b. [`H`](xref:microsoft.quantum.intrinsic.h) und [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) stehen automatisch für Vorgänge zur Verfügung, die in Zellen in Q # jupyter-Notebooks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5322a-272">Callables from [Microsoft.Quantum.Intrinsic](xref:microsoft.quantum.intrinsic) and [Microsoft.Quantum.Canon](xref:microsoft.quantum.canon) (e.g. [`H`](xref:microsoft.quantum.intrinsic.h) and [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="5322a-273">Dies gilt jedoch nicht für Code, der aus externen Q #-Quelldateien eingefügt wurde (ein Prozess, der unter Einführung [in q # und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="5322a-273">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="5322a-274">Ebenso erfordert das Definieren von Vorgängen lediglich den Q #-Code und die Ausführung der Zelle.</span><span class="sxs-lookup"><span data-stu-id="5322a-274">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

<span data-ttu-id="5322a-275">In der Ausgabe werden dann diese Vorgänge aufgelistet, die aus zukünftigen Zellen aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="5322a-275">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="5322a-276">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="5322a-276">Target machines</span></span>

<span data-ttu-id="5322a-277">Die Funktionen zum Ausführen von Vorgängen auf bestimmten Ziel Computern werden über die [Befehle "IQ # Magic](xref:microsoft.quantum.guide.quickref.iqsharp)" bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5322a-277">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="5322a-278">Beispielsweise `%simulate` verwendet die `QuantumSimulator` , und `%estimate` verwendet Folgendes `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="5322a-278">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="5322a-279">Übergeben von Eingaben an Funktionen und Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5322a-279">Passing inputs to functions and operations</span></span>

<span data-ttu-id="5322a-280">Derzeit können die Befehle zum Ausführen von Magic nur mit Vorgängen verwendet werden, die keine Argumente annehmen.</span><span class="sxs-lookup"><span data-stu-id="5322a-280">Currently the execution magic commands can only be used with operations that take no arguments.</span></span> <span data-ttu-id="5322a-281">Zum Ausführen von `MeasureSuperpositionArray` müssen wir also einen Wrapper Vorgang definieren, der dann den Vorgang mit den Argumenten aufruft:</span><span class="sxs-lookup"><span data-stu-id="5322a-281">So, to run `MeasureSuperpositionArray`, we need to define a "wrapper" operation which then calls the operation with the arguments:</span></span>

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

<span data-ttu-id="5322a-282">Dieser Vorgang kann natürlich auch mit `%estimate` und anderen Ausführungs Befehlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5322a-282">This operation can of course be used similarly with `%estimate` and other execution commands.</span></span>
