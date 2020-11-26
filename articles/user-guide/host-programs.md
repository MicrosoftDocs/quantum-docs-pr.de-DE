---
title: Möglichkeiten zum Ausführen eines Q# Programms
description: Übersicht über die verschiedenen Möglichkeiten zum Ausführen von Q# Programmen. An der Eingabeaufforderung, Q# jupyter Notebooks und klassischen Host Programmen in Python oder einer .NET-Sprache.
author: gillenhaalb
ms.author: a-gibec
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2c5bdebc826bb85f6d7e0ade6232e15e29e8fb19
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231688"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="8bc25-104">Möglichkeiten zum Ausführen eines Q# Programms</span><span class="sxs-lookup"><span data-stu-id="8bc25-104">Ways to run a Q# program</span></span>

<span data-ttu-id="8bc25-105">Eines der größten Stärken des quantumentwicklungskit ist seine Flexibilität über Plattformen und Entwicklungsumgebungen hinweg.</span><span class="sxs-lookup"><span data-stu-id="8bc25-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="8bc25-106">Dies bedeutet jedoch auch, dass Q# sich neue Benutzer möglicherweise nicht mit den zahlreichen Optionen im [Installationshandbuch](xref:microsoft.quantum.install)verwechselt haben.</span><span class="sxs-lookup"><span data-stu-id="8bc25-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="8bc25-107">Auf dieser Seite erläutern wir, was geschieht, wenn ein Q# Programm ausgeführt wird, und vergleichen die verschiedenen Möglichkeiten, wie Benutzer dies tun können.</span><span class="sxs-lookup"><span data-stu-id="8bc25-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="8bc25-108">Ein primärer Unterschied besteht darin, dass Q# ausgeführt werden kann:</span><span class="sxs-lookup"><span data-stu-id="8bc25-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="8bc25-109">als eigenständige Anwendung, bei Q# der die einzige beteiligte Sprache ist und das Programm direkt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="8bc25-110">Zwei Methoden fallen tatsächlich in diese Kategorie:</span><span class="sxs-lookup"><span data-stu-id="8bc25-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="8bc25-111">die Befehlszeilenschnittstelle</span><span class="sxs-lookup"><span data-stu-id="8bc25-111">the command-line interface</span></span>
  - <span data-ttu-id="8bc25-112">Q# Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="8bc25-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="8bc25-113">mit einem zusätzlichen *Host Programm*, das in Python oder einer .NET-Sprache (z. b. c# oder F #) geschrieben ist, die dann das Programm aufruft und die zurückgegebenen Ergebnisse weiterverarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="8bc25-113">with an additional *host program*, written in Python or a .NET language (for example, C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="8bc25-114">Um diese Prozesse und deren Unterschiede zu verstehen, wird ein einfaches Q# Programm angenommen, und es wird erläutert, wie es ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8bc25-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be run.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="8bc25-115">Einfaches Q# Programm</span><span class="sxs-lookup"><span data-stu-id="8bc25-115">Basic Q# program</span></span>

<span data-ttu-id="8bc25-116">Ein grundlegendes Quantum-Programm besteht möglicherweise aus der Vorbereitung eines Qubit in derselben Superposition in den Zuständen $ \ket {0} $ und $ \ket {1} $, wobei es gemessen wird und das Ergebnis zurückgegeben wird. dabei wird entweder einer dieser beiden Zustände mit gleicher Wahrscheinlichkeit nach dem Zufallsprinzip verwendet.</span><span class="sxs-lookup"><span data-stu-id="8bc25-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="8bc25-117">Tatsächlich ist dieser Prozess der Kern des Schnellstarts des [Quantum-Zufallszahlen-Generators](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="8bc25-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="8bc25-118">In wird Q# dies durch den folgenden Code ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="8bc25-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="8bc25-119">Dieser Code allein kann jedoch nicht von ausgeführt werden Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-119">However, this code alone can't be run by Q#.</span></span>
<span data-ttu-id="8bc25-120">Dafür muss der Text eines [Vorgangs](xref:microsoft.quantum.qsharp.operationsandfunctions)ausgeführt werden, der dann ausgeführt wird, wenn er---entweder direkt oder durch einen anderen Vorgang aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.qsharp.operationsandfunctions), which is then run when called---either directly or by another operation.</span></span> <span data-ttu-id="8bc25-121">Daher können Sie einen Vorgang der folgenden Form schreiben:</span><span class="sxs-lookup"><span data-stu-id="8bc25-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="8bc25-122">Sie haben einen Vorgang definiert, `MeasureSuperposition` der keine Eingaben annimmt und einen Wert vom Typ [Result](xref:microsoft.quantum.qsharp.typesystem-index#available-types)zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.qsharp.typesystem-index#available-types).</span></span>

<span data-ttu-id="8bc25-123">Zusätzlich zu den Vorgängen Q# ermöglicht auch das Kapseln deterministischer Berechnungen in Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-123">In addition to operations, Q# also allows to encapsulate deterministic computations into functions.</span></span> <span data-ttu-id="8bc25-124">Abgesehen von der Determinismus Garantie, die impliziert, dass Berechnungen, die auf Qubits reagieren, in Vorgänge und nicht in Funktionen gekapselt werden müssen, gibt es kaum Unterschiede zwischen den Vorgängen und der Funktion.</span><span class="sxs-lookup"><span data-stu-id="8bc25-124">Aside from the determinism guarantee that implies that computations that act on qubits need to be encapsulated into operations rather than functions, there is little difference between operations and function.</span></span> <span data-ttu-id="8bc25-125">Diese werden zusammen als *callables* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8bc25-125">We refer to them collectively as *callables*.</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="8bc25-126">In einer Datei definierte Aufruf Bare Q# Datei</span><span class="sxs-lookup"><span data-stu-id="8bc25-126">Callable defined in a Q# file</span></span>

<span data-ttu-id="8bc25-127">Die Aufruf Bare ist genau das, was von aufgerufen und ausgeführt wird Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-127">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="8bc25-128">Allerdings sind einige weitere Ergänzungen erforderlich, um eine vollständige Datei zu bilden `*.qs` Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-128">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="8bc25-129">Alle Q# Typen und callables (sowohl die, die Sie definieren, als auch die in der Sprache intrinsisch) werden innerhalb von *Namespaces* definiert, die jeweils einen vollständigen Namen bereitstellen, auf den dann verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8bc25-129">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="8bc25-130">Beispielsweise werden die [`H`](xref:Microsoft.Quantum.Intrinsic.H) [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) Vorgänge und in den [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) Namespaces und (Teil der [ Q# Standard Bibliotheken](xref:microsoft.quantum.libraries.standard.intro)) gefunden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-130">For example, the [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) and [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.libraries.standard.intro)).</span></span>
<span data-ttu-id="8bc25-131">Daher können Sie immer über die *vollständigen* Namen und aufgerufen werden `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` . Dies führt jedoch zu einem sehr überlasteten Code.</span><span class="sxs-lookup"><span data-stu-id="8bc25-131">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="8bc25-132">Stattdessen `open` ermöglichen-Anweisungen, dass auf Aufruf Bare Elemente mit präziseren Kurzform verwiesen wird, wie dies im obigen Vorgangs Text geschehen ist.</span><span class="sxs-lookup"><span data-stu-id="8bc25-132">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="8bc25-133">Die vollständige Q# Datei, die den Vorgang enthält, besteht daher darin, einen eigenen Namespace zu definieren, die Namespaces für die von unserem Vorgang verwendeten callables zu öffnen, und dann den Vorgang:</span><span class="sxs-lookup"><span data-stu-id="8bc25-133">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

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
> <span data-ttu-id="8bc25-134">Namespaces können auch beim Öffnen einen *Alias* aufweisen. Dies kann hilfreich sein, wenn Aufruf Bare/Typnamen in zwei Namespaces in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-134">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="8bc25-135">Beispielsweise könnten wir stattdessen oben verwenden `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` und dann `H` via anrufen `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-135">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="8bc25-136">Eine Ausnahme ist der [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) Namespace, der immer automatisch geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-136">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="8bc25-137">Daher können callables wie [`Length`](xref:Microsoft.Quantum.Core.Length) immer direkt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-137">Therefore, callables like [`Length`](xref:Microsoft.Quantum.Core.Length) can always be used directly.</span></span>

### <a name="running-on-target-machines"></a><span data-ttu-id="8bc25-138">Ausführen auf Ziel Computern</span><span class="sxs-lookup"><span data-stu-id="8bc25-138">Running on target machines</span></span>

<span data-ttu-id="8bc25-139">Nun wird das allgemeine Lauf Zeitmodell eines Q# Programms deutlich.</span><span class="sxs-lookup"><span data-stu-id="8bc25-139">Now the general run model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="8bc25-140">Zum einen hat die spezifische Aufruf Bare, die ausgeführt werden kann, Zugriff auf alle anderen callables und Typen, die im selben Namespace definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-140">Firstly, the specific callable to be run has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="8bc25-141">Außerdem greift er auf die Bibliotheken aus einer der [ Q# Bibliotheken](xref:microsoft.quantum.libraries)zu, aber auf diese müssen entweder über den vollständigen Namen oder über die `open` oben beschriebenen Anweisungen verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-141">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="8bc25-142">Die Aufruf Bare selbst wird dann auf einem *[Zielcomputer](xref:microsoft.quantum.machines)* ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-142">The callable itself is then run on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="8bc25-143">Bei solchen Ziel Computern kann es sich um tatsächliche Quantum-Hardware oder mehrere Simulatoren handeln, die als Teil des QDK verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-143">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="8bc25-144">Zu diesem Zweck ist der nützlichste Zielcomputer eine Instanz des [vollständigen Simulators](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , der das Verhalten des Programms so berechnet, als ob es auf einem Rausch freien Quantum-Computer ausgeführt würde.</span><span class="sxs-lookup"><span data-stu-id="8bc25-144">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being run on a noise-free quantum computer.</span></span>

<span data-ttu-id="8bc25-145">Bisher haben wir beschrieben, was geschieht, wenn eine bestimmte Q# Aufruf Bare ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-145">So far, we've described what happens when a specific Q# callable is being run.</span></span>
<span data-ttu-id="8bc25-146">Unabhängig davon Q# , ob in einer eigenständigen Anwendung oder einem Host Programm verwendet wird, ist dieser allgemeine Prozess mehr oder weniger identisch---daher die Flexibilität des QDK.</span><span class="sxs-lookup"><span data-stu-id="8bc25-146">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="8bc25-147">Die Unterschiede zwischen den Methoden zum Aufrufen von Quantum Development Kit zeigen sich daher selbst, *wie* diese Aufruf Q# Bare aufgerufen wird und wie alle Ergebnisse zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-147">The differences between the ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be run, and in what manner any results are returned.</span></span>
<span data-ttu-id="8bc25-148">Genauer gesagt, gibt es die folgenden Unterschiede:</span><span class="sxs-lookup"><span data-stu-id="8bc25-148">More specifically, the differences revolve around:</span></span>

- <span data-ttu-id="8bc25-149">Angeben, welche Q# Aufruf Bare ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="8bc25-149">Indicating which Q# callable is to be run</span></span>
- <span data-ttu-id="8bc25-150">Bereitstellung potenzieller Aufruf barer Argumente</span><span class="sxs-lookup"><span data-stu-id="8bc25-150">How potential callable arguments are provided</span></span>
- <span data-ttu-id="8bc25-151">Angeben des Ziel Computers, auf dem der Computer ausgeführt werden soll</span><span class="sxs-lookup"><span data-stu-id="8bc25-151">Specifying the target machine on which to run it</span></span>
- <span data-ttu-id="8bc25-152">Zurückgegebene Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="8bc25-152">How any results are returned</span></span>

<span data-ttu-id="8bc25-153">Zuerst wird erläutert, wie dies mit der Q# eigenständigen Anwendung an der Eingabeaufforderung erfolgt, und anschließend können Sie mit der Verwendung von Python-und c#-Host Programmen fortfahren.</span><span class="sxs-lookup"><span data-stu-id="8bc25-153">First, we discuss how this is done with the Q# standalone application from the command prompt, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="8bc25-154">Wir reservieren die eigenständige Anwendung von Q# jupyter-Notebooks für das letzte, da die primäre Funktionalität im Gegensatz zu den ersten drei nicht um eine lokale Datei zentriert ist Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-154">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="8bc25-155">Obwohl wir dies in diesen Beispielen nicht veranschaulichen, besteht eine Gemeinsamkeit zwischen den Lauf Methoden darin, dass alle Nachrichten, die aus dem Programm gedruckt werden (z. b. über Q# [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) oder [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine) ), in der Regel immer an die jeweilige Konsole ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-155">Although we don't illustrate it in these examples, one commonality between the run methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) or [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-prompt"></a><span data-ttu-id="8bc25-156">Q# an der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="8bc25-156">Q# from the command prompt</span></span>
<span data-ttu-id="8bc25-157">Eine der einfachsten Möglichkeiten, Programme zu schreiben Q# , besteht darin, die Gedanken über separate Dateien und eine zweite Sprache vollständig zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-157">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="8bc25-158">Die Verwendung von Visual Studio Code oder Visual Studio mit der QDK-Erweiterung ermöglicht einen nahtlosen Workflow, bei dem Q# nur callables aus einer einzelnen Q# Datei ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-158">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="8bc25-159">Zu diesem Zweck wird das Programm letztendlich durch Eingabe von</span><span class="sxs-lookup"><span data-stu-id="8bc25-159">For this, we will ultimately run the program by entering</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="8bc25-160">an der Eingabeaufforderung ein.</span><span class="sxs-lookup"><span data-stu-id="8bc25-160">at the command prompt.</span></span>
<span data-ttu-id="8bc25-161">Der einfachste Workflow ist, wenn der Verzeichnis Speicherort des Terminals mit der Datei identisch ist Q# , die mit Q# der Dateibearbeitung problemlos über das integrierte Terminal in vs Code behandelt werden kann, z. b..</span><span class="sxs-lookup"><span data-stu-id="8bc25-161">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="8bc25-162">Der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) akzeptiert jedoch zahlreiche Optionen, und das Programm kann auch an einem anderen Speicherort ausgeführt werden, indem einfach `--project <PATH>` der Speicherort der Datei bereitgestellt wird Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-162">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="8bc25-163">Einstiegspunkt zu Datei hinzufügen Q#</span><span class="sxs-lookup"><span data-stu-id="8bc25-163">Add entry point to Q# file</span></span>

<span data-ttu-id="8bc25-164">Die meisten Q# Dateien enthalten mehr als eine Aufruf Bare Funktion. Daher muss der Compiler wissen, *welche* Aufruf Liste ausgeführt werden soll, wenn der Befehl bereitgestellt wird `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-164">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to run when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="8bc25-165">Dies erfolgt mit einer einfachen Änderung an der Q# Datei selbst:</span><span class="sxs-lookup"><span data-stu-id="8bc25-165">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="8bc25-166">Fügen Sie eine Zeile hinzu, `@EntryPoint()` die direkt vor dem Aufruf baren steht.</span><span class="sxs-lookup"><span data-stu-id="8bc25-166">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="8bc25-167">Unsere Datei von oben wird daher</span><span class="sxs-lookup"><span data-stu-id="8bc25-167">Our file from above would therefore become</span></span>
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

<span data-ttu-id="8bc25-168">Nun `dotnet run` führt ein-Befehl von der Eingabeaufforderung aus `MeasureSuperposition` , und der zurückgegebene Wert wird dann direkt in das Terminal gedruckt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-168">Now, a call of `dotnet run` from the command prompt leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="8bc25-169">Daher wird entweder `One` oder `Zero` gedruckt angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-169">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="8bc25-170">Beachten Sie, dass es keine Rolle spielt, ob weitere Aufruf Bare aufruben definiert sind, sondern nur `MeasureSuperposition` ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-170">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="8bc25-171">Außerdem ist es kein Problem, wenn die Aufruf Bare-Datei vor der Deklaration [Dokumentations Kommentare](xref:microsoft.quantum.qsharp.comments#documentation-comments) enthält `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-171">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.qsharp.comments#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="8bc25-172">Aufruf Bare Argumente</span><span class="sxs-lookup"><span data-stu-id="8bc25-172">Callable arguments</span></span>

<span data-ttu-id="8bc25-173">Bisher haben wir nur einen Vorgang in Erwägung gezogen, der keine Eingaben annimmt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-173">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="8bc25-174">Angenommen, wir wollten einen ähnlichen Vorgang durchführen, aber auf mehreren Qubits---die Zahl als Argument bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-174">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="8bc25-175">Ein solcher Vorgang könnte als</span><span class="sxs-lookup"><span data-stu-id="8bc25-175">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="8bc25-176">Dabei ist der zurückgegebene Wert ein Array der Messergebnisse.</span><span class="sxs-lookup"><span data-stu-id="8bc25-176">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="8bc25-177">Beachten Sie, dass [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) und [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) sich im [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) -Namespace und im- [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) Namespace befinden, `open` wobei jeweils zusätzliche Anweisungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-177">Note that [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) and [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) are in the [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) and [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="8bc25-178">Wenn Sie das `@EntryPoint()` Attribut vor diesem neuen Vorgang verschieben (Beachten Sie, dass es nur eine Zeile in einer Datei geben kann), und wenn Sie versuchen, es mit einfach auszuführen, führt dies zu `dotnet run` einer Fehlermeldung, die angibt, welche zusätzlichen Befehlszeilenoptionen erforderlich sind, und wie Sie Sie Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="8bc25-178">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command-line options are required, and how to express them.</span></span>

<span data-ttu-id="8bc25-179">Das allgemeine Format für die Befehlszeile ist tatsächlich `dotnet run [options]` , und es werden Aufruf Bare Argumente dort bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-179">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="8bc25-180">In diesem Fall fehlt das Argument `n` , und es wird angezeigt, dass die Option bereitgestellt werden muss `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-180">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="8bc25-181">Zum Ausführen `MeasureSuperpositionArray` von for `n=4` Qubits verwenden wir daher</span><span class="sxs-lookup"><span data-stu-id="8bc25-181">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="8bc25-182">Ausgabe ähnlich</span><span class="sxs-lookup"><span data-stu-id="8bc25-182">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="8bc25-183">Dies reicht natürlich auf mehrere Argumente aus.</span><span class="sxs-lookup"><span data-stu-id="8bc25-183">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="8bc25-184">In definierte Argument Namen `camelCase` werden vom Compiler leicht geändert, damit Sie als Eingaben akzeptiert werden Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-184">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="8bc25-185">Wenn z. b. anstelle von `n` der oben genannte Name verwendet wird `numQubits` , wird diese Eingabe in der Befehlszeile über `--num-qubits 4` anstelle von bereitgestellt `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-185">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="8bc25-186">Die Fehlermeldung enthält auch weitere Optionen, die verwendet werden können, einschließlich Informationen zum Ändern des Ziel Computers.</span><span class="sxs-lookup"><span data-stu-id="8bc25-186">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="8bc25-187">Verschiedene Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="8bc25-187">Different target machines</span></span>

<span data-ttu-id="8bc25-188">Da die Ausgaben unserer Vorgänge bisher die erwarteten Ergebnisse ihrer Aktion in echten Qubits waren, ist klar, dass der Standardziel Computer von der Befehlszeile aus der vollzustandsquantum-Simulator ist `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-188">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quantum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="8bc25-189">Wir können jedoch Aufruf Bare Aufrufe anweisen, die auf einem bestimmten Zielcomputer mit der Option `--simulator` (oder der kurzseite `-s` ) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-189">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="8bc25-190">Beispielsweise können wir die Anwendung unter Ausführen [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="8bc25-190">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="8bc25-191">Die gedruckte Ausgabe lautet dann</span><span class="sxs-lookup"><span data-stu-id="8bc25-191">The printed output is then</span></span>

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

<span data-ttu-id="8bc25-192">Ausführliche Informationen dazu, was diese Metriken angeben, finden Sie unter [Ressourcenschätzung: gemeldete Metriken](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span><span class="sxs-lookup"><span data-stu-id="8bc25-192">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-run-summary"></a><span data-ttu-id="8bc25-193">Befehlszeilen-Lauf Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="8bc25-193">Command line run summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="8bc25-194">Nicht- Q# `dotnet run` Optionen</span><span class="sxs-lookup"><span data-stu-id="8bc25-194">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="8bc25-195">Wie bereits kurz erwähnt `--project` , akzeptiert der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) auch Optionen, die nicht mit den Q# Aufruf baren Argumenten verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-195">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="8bc25-196">Wenn beide Arten von Optionen bereit `dotnet` gestellt werden, müssen zuerst die-spezifischen Optionen, gefolgt von einem Trennzeichen `--` , und dann die Q# -spezifischen Optionen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-196">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="8bc25-197">Wenn Sie z. b. einen Pfad zusammen mit einer Zahlen-Qubits für den obigen Vorgang angeben, wird über ausgeführt `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-197">For example, specifying a path along with a number qubits for the operation above would be run via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="8bc25-198">Q# mit Host Programmen</span><span class="sxs-lookup"><span data-stu-id="8bc25-198">Q# with host programs</span></span>

<span data-ttu-id="8bc25-199">Mit unserer Q# Datei ist eine Alternative zum Aufrufen eines Vorgangs oder einer Funktion direkt über die Eingabeaufforderung die Verwendung eines *Host Programms* in einer anderen klassischen Sprache.</span><span class="sxs-lookup"><span data-stu-id="8bc25-199">With our Q# file in hand, an alternative to calling an operation or function directly from the command prompt is to use a *host program* in another classical language.</span></span> <span data-ttu-id="8bc25-200">Dies kann insbesondere mit Python oder einer .NET-Sprache (z. b. c# oder F #) erfolgen (aus Gründen der Kürze wird c# hier nur ausführlich erläutert).</span><span class="sxs-lookup"><span data-stu-id="8bc25-200">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="8bc25-201">Zum Aktivieren der Interoperabilität ist ein wenig mehr Setup erforderlich. diese Details finden Sie jedoch in den [Installations](xref:microsoft.quantum.install)Handbüchern.</span><span class="sxs-lookup"><span data-stu-id="8bc25-201">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="8bc25-202">Kurz gesagt, enthält die Situation nun eine Host Programmdatei (z `*.py` . b. oder `*.cs` ) am gleichen Speicherort wie die Q# Datei.</span><span class="sxs-lookup"><span data-stu-id="8bc25-202">In a nutshell, the situation now includes a host program file (for example, `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="8bc25-203">Es ist jetzt das *Host* Programm, das ausgeführt wird. während es ausgeführt wird, kann es bestimmte Q# Vorgänge und Funktionen aus der Q# Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-203">It's now the *host* program that gets run, and while it is running, it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="8bc25-204">Der Kern der Interoperabilität basiert auf dem Compiler, der Q# den Inhalt der Q# Datei für das Host Programm zugänglich macht, sodass Sie aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="8bc25-204">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="8bc25-205">Einer der Hauptvorteile der Verwendung eines Host Programms besteht darin, dass die vom Programm zurückgegebenen klassischen Daten Q# dann in der Host Sprache weiterverarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="8bc25-205">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="8bc25-206">Dies kann aus einer erweiterten Datenverarbeitung bestehen (z. b. etwas, das nicht intern in ausgeführt werden kann Q# ). Anschließend werden weitere Aktionen auf der Q# Grundlage dieser Ergebnisse aufgerufen, oder es kann etwas so einfach sein, wie die Ergebnisse gezeichnet werden Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-206">This could consist of some advanced data processing (for example, something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="8bc25-207">Das allgemeine Schema wird hier angezeigt, und wir erörtern die spezifischen Implementierungen für python und c# weiter unten.</span><span class="sxs-lookup"><span data-stu-id="8bc25-207">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="8bc25-208">Ein Beispiel für die Verwendung eines F #-Host Programms finden Sie unter [.net-Interoperabilitäts Beispiele](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="8bc25-208">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="8bc25-209">Das `@EntryPoint()` für-Anwendungen verwendete Attribut Q# kann nicht mit Host Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-209">The `@EntryPoint()` attribute used for Q# applications cannot be used with host programs.</span></span>
> <span data-ttu-id="8bc25-210">Wenn Sie in der Datei vorhanden ist Q# , die von einem Host aufgerufen wird, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8bc25-210">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="8bc25-211">Um mit unterschiedlichen Host Programmen arbeiten zu können, sind keine Änderungen an einer `*.qs` Q# Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8bc25-211">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="8bc25-212">Die folgenden Host Programm Implementierungen funktionieren alle mit derselben Q# Datei:</span><span class="sxs-lookup"><span data-stu-id="8bc25-212">The following host program implementations all work with the same Q# file:</span></span>

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

<span data-ttu-id="8bc25-213">Wählen Sie die Registerkarte aus, die der gewünschten Host Sprache entspricht.</span><span class="sxs-lookup"><span data-stu-id="8bc25-213">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="8bc25-214">Python</span><span class="sxs-lookup"><span data-stu-id="8bc25-214">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="8bc25-215">Ein python-Host Programm wird wie folgt erstellt:</span><span class="sxs-lookup"><span data-stu-id="8bc25-215">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="8bc25-216">Importieren Sie das- `qsharp` Modul, mit dem das Modul Lade Modul für die Interoperabilität registriert wird Q# .</span><span class="sxs-lookup"><span data-stu-id="8bc25-216">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="8bc25-217">Dadurch Q# können Namespaces als Python-Module angezeigt werden, aus denen Sie Q# callables importieren können.</span><span class="sxs-lookup"><span data-stu-id="8bc25-217">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="8bc25-218">Beachten Sie, dass es sich nicht um die Q# selbst importierbaren, sondern vielmehr um python-Stubdateien handelt, die das Aufrufen von Dateien ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-218">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="8bc25-219">Diese Verhalten sich als Objekte von python-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-219">These behave as objects of Python classes.</span></span> <span data-ttu-id="8bc25-220">Wir verwenden Methoden für diese Objekte, um die Zielcomputer anzugeben, an die der Vorgang beim Ausführen des Programms gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-220">We use methods on these objects to specify the target machines that we send the operation to when running the program.</span></span>

2. <span data-ttu-id="8bc25-221">Importieren Sie diese Q# callables, die wir direkt aufrufen---in diesem Fall `MeasureSuperposition` und `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-221">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="8bc25-222">Wenn `qsharp` Sie das Modul importiert haben, können Sie auch callables direkt aus den Q# Bibliotheks Namespaces importieren.</span><span class="sxs-lookup"><span data-stu-id="8bc25-222">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="8bc25-223">Unter jedem anderen Python-Code können Sie jetzt diese callables auf bestimmten Ziel Computern aufrufen und ihre Rückgaben den Variablen (wenn Sie einen Wert zurückgeben) zur weiteren Verwendung zuweisen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-223">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="8bc25-224">Angeben von Ziel Computern</span><span class="sxs-lookup"><span data-stu-id="8bc25-224">Specifying target machines</span></span>
<span data-ttu-id="8bc25-225">Das Aufrufen eines Vorgangs, der auf einem bestimmten Zielcomputer ausgeführt werden soll, erfolgt über verschiedene python-Methoden auf dem importierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-225">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="8bc25-226">Beispielsweise `.simulate(<args>)` verwendet die `QuantumSimulator` zum Ausführen des Vorgangs, während `.estimate_resources(<args>)` dies in der erfolgt `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-226">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="8bc25-227">Übergeben von Eingaben an Q\#</span><span class="sxs-lookup"><span data-stu-id="8bc25-227">Passing inputs to Q\#</span></span>
<span data-ttu-id="8bc25-228">Argumente für die Q# Aufruf Bare-Datei sollten in Form eines Schlüsselwort Arguments bereitgestellt werden, wobei das-Schlüsselwort der Argument Name in der Q# Aufruf baren Definition ist.</span><span class="sxs-lookup"><span data-stu-id="8bc25-228">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="8bc25-229">Das heißt, `MeasureSuperpositionArray.simulate(n=4)` ist gültig, während `MeasureSuperpositionArray.simulate(4)` einen Fehler auslöst.</span><span class="sxs-lookup"><span data-stu-id="8bc25-229">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="8bc25-230">Daher ist das python-Host Programm</span><span class="sxs-lookup"><span data-stu-id="8bc25-230">Therefore, the Python host program</span></span> 

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

<span data-ttu-id="8bc25-231">ergibt eine Ausgabe wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="8bc25-231">results in an output like the following:</span></span>

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="8bc25-232">Verwenden Q# von Code aus anderen Projekten oder Paketen</span><span class="sxs-lookup"><span data-stu-id="8bc25-232">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="8bc25-233">Standardmäßig lädt der `import qsharp` Befehl alle `.qs` Dateien im aktuellen Ordner und macht Ihre Q# Vorgänge und Funktionen für die Verwendung innerhalb des python-Skripts verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bc25-233">By default, the `import qsharp` command loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the Python script.</span></span>

<span data-ttu-id="8bc25-234">Zum Laden Q# von Code aus einem anderen Ordner kann die [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) verwendet werden, um einen Verweis auf eine `.csproj` Datei für ein Q# Projekt (d. h. ein Projekt, das auf verweist) hinzuzufügen `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-234">To load Q# code from another folder, the [`qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span>
<span data-ttu-id="8bc25-235">Mit diesem Befehl werden alle `.qs` Dateien im Ordner kompiliert, die die `.csproj` und deren Unterordner enthalten.</span><span class="sxs-lookup"><span data-stu-id="8bc25-235">This command will compile any `.qs` files in the folder containing the `.csproj` and its subfolders.</span></span> <span data-ttu-id="8bc25-236">Außerdem werden alle Pakete rekursiv geladen `PackageReference` Q# `ProjectReference` , auf die über-oder-Projekte verwiesen wird `.csproj`</span><span class="sxs-lookup"><span data-stu-id="8bc25-236">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span>

<span data-ttu-id="8bc25-237">Der folgende Python-Code importiert z. b. ein externes Projekt, das auf seinen Pfad relativ zum aktuellen Ordner verweist und einen seiner Vorgänge aufruft Q# :</span><span class="sxs-lookup"><span data-stu-id="8bc25-237">As an example, the following Python code imports an external project, referencing its path relative to the current folder, and invokes one of its Q# operations:</span></span>

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

<span data-ttu-id="8bc25-238">Dies führt zu einer Ausgabe wie der folgenden:</span><span class="sxs-lookup"><span data-stu-id="8bc25-238">This results in output like the following:</span></span>

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

<span data-ttu-id="8bc25-239">Q#Verwenden Sie die- [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages), um externe Pakete mit Code zu laden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-239">To load external packages containing Q# code, use the [`qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span></span>

<span data-ttu-id="8bc25-240">Wenn der Q# Code im aktuellen Ordner von externen Projekten oder Paketen abhängt, werden bei der Ausführung möglicherweise Fehler angezeigt `import qsharp` , da die Abhängigkeiten noch nicht geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-240">If the Q# code in the current folder depends on external projects or packages, you may see errors when running `import qsharp`, since the dependencies have not yet been loaded.</span></span>
<span data-ttu-id="8bc25-241">Wenn Sie erforderliche externe Pakete oder Q# Projekte während des `import qsharp` Befehls laden möchten, stellen Sie sicher, dass der Ordner mit dem Python-Skript eine Datei enthält, auf `.csproj` die verweist `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-241">To load required external packages or Q# projects during the `import qsharp` command, ensure that the folder with the Python script contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="8bc25-242">Fügen Sie der-Eigenschaft die- `.csproj` Eigenschaft hinzu `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-242">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="8bc25-243">Dies weist Q# darauf hin, `ProjectReference` `PackageReference` dass `.csproj` während des Befehls rekursiv alle-oder-Elemente geladen werden `import qsharp` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-243">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` during the `import qsharp` command.</span></span>

<span data-ttu-id="8bc25-244">Hier ist beispielsweise eine einfache Datei, die `.csproj` bewirkt, dass Q# das Paket automatisch geladen wird `Microsoft.Quantum.Chemistry` :</span><span class="sxs-lookup"><span data-stu-id="8bc25-244">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="8bc25-245">Diese benutzerdefinierte `<IQSharpLoadAutomatically>` Eigenschaft ist derzeit für python-Hosts erforderlich. in Zukunft kann dies jedoch das Standardverhalten für eine Datei sein, die `.csproj` sich im gleichen Ordner wie das Python-Skript befindet.</span><span class="sxs-lookup"><span data-stu-id="8bc25-245">Currently this custom `<IQSharpLoadAutomatically>` property is required by Python hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the Python script.</span></span>

> [!NOTE]
> <span data-ttu-id="8bc25-246">Die `<QsharpCompile>` -Einstellung in `.csproj` wird derzeit von python-Hosts ignoriert, und alle `.qs` Dateien im-Ordner der `.csproj` (einschließlich der Unterordner) werden geladen und kompiliert.</span><span class="sxs-lookup"><span data-stu-id="8bc25-246">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Python hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="8bc25-247">Die Unterstützung für `.csproj` Einstellungen wird in Zukunft verbessert (Weitere Informationen finden Sie unter [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) ).</span><span class="sxs-lookup"><span data-stu-id="8bc25-247">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>


### <a name="c"></a>[<span data-ttu-id="8bc25-248">C#</span><span class="sxs-lookup"><span data-stu-id="8bc25-248">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="8bc25-249">Ein c#-Host Programm verfügt über mehrere Komponenten, die eng mit einigen Komponenten des QDK funktionieren, z. b. die Simulatoren, die selbst auf c# basieren.</span><span class="sxs-lookup"><span data-stu-id="8bc25-249">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="8bc25-250">Der Q# Compiler arbeitet hier, indem er einen gleichwertig benannten c#-Namespace aus dem Q# Namespace in der Q# Datei erzeugt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-250">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="8bc25-251">Außerdem wird eine gleichwertig benannte c#-Klasse für jede der Q# darin definierten callables oder Typen generiert.</span><span class="sxs-lookup"><span data-stu-id="8bc25-251">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="8bc25-252">Zuerst werden alle Klassen, die in unserem Host Programm verwendet werden, mit-Anweisungen zur Verfügung gestellt `using` , die ungefähr mit den `open` Anweisungen in der Datei zusammengefügt werden Q# :</span><span class="sxs-lookup"><span data-stu-id="8bc25-252">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (for example, QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="8bc25-253">Als nächstes deklarieren wir den c#-Namespace, einige andere Bits und Teile (siehe den vollständigen Codeblock unten) und dann alle klassischen Programmierungen, die wir wünschen (z. b. das Berechnen von Argumenten für die Q# callables).</span><span class="sxs-lookup"><span data-stu-id="8bc25-253">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (for example, computing arguments for the Q# callables).</span></span>
<span data-ttu-id="8bc25-254">Letzteres ist in diesem Fall nicht erforderlich, aber ein Beispiel für eine solche Verwendung finden Sie unter  [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet)Beispiel.</span><span class="sxs-lookup"><span data-stu-id="8bc25-254">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="8bc25-255">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="8bc25-255">Target machines</span></span>

<span data-ttu-id="8bc25-256">Bei der Rückkehr zu Q# müssen wir eine Instanz eines beliebigen Ziel Computers erstellen, auf dem wir unsere Vorgänge ausführen werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-256">Getting back to Q#, we must create an instance of whatever target machine we will run our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="8bc25-257">Die Verwendung anderer Zielcomputer ist so einfach wie das Instanziieren eines anderen Ziel Computers, obwohl die Art und Weise der Rückgabe geringfügig abweichen kann.</span><span class="sxs-lookup"><span data-stu-id="8bc25-257">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="8bc25-258">Aus Gründen der Kürze bleiben wir an der [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) für die Zeit und fügen die [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [folgenden](#including-the-resources-estimator)Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="8bc25-258">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="8bc25-259">Jede aus den Vorgängen generierte c#-Klasse Q# verfügt über eine- `Run` Methode, wobei das erste Argument, das die Zielcomputer Instanz sein muss.</span><span class="sxs-lookup"><span data-stu-id="8bc25-259">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="8bc25-260">Daher `MeasureSuperposition` verwenden wir, um auf dem auszuführen `QuantumSimulator` `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-260">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="8bc25-261">Die zurückgegebenen Ergebnisse können dann Variablen in c# zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="8bc25-261">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="8bc25-262">Die `Run` -Methode wird asynchron ausgeführt, da dies die Groß-und Kleinschreibung für echte Quantum-Hardware ist. Daher blockiert das- `await` Schlüsselwort die weitere Verarbeitung, bis die Aufgabe abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8bc25-262">The `Run` method is run asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further processing until the task completes.</span></span>

<span data-ttu-id="8bc25-263">Wenn die Q# Aufruf Bare-Datei keine Rückgaben aufweist (z. b. den Rückgabetyp `Unit` ), kann die Ausführung weiterhin auf dieselbe Weise erfolgen, ohne Sie einer Variablen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-263">If the Q# callable does not have any returns (for example, it has return type `Unit`), then the run can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="8bc25-264">In diesem Fall würde die gesamte Zeile einfach aus</span><span class="sxs-lookup"><span data-stu-id="8bc25-264">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="8bc25-265">Argumente</span><span class="sxs-lookup"><span data-stu-id="8bc25-265">Arguments</span></span>

<span data-ttu-id="8bc25-266">Alle Argumente für die Q# Aufruf baren werden einfach als zusätzliche Argumente nach dem Zielcomputer weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="8bc25-266">Any arguments to the Q# callable are simply passed as additional arguments after the target machine.</span></span>
<span data-ttu-id="8bc25-267">Daher werden die Ergebnisse von `MeasureSuperpositionArray` in `n=4` Qubits über</span><span class="sxs-lookup"><span data-stu-id="8bc25-267">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="8bc25-268">Ein vollständiges c#-Host Programm könnte daher wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-268">A full C# host program could thus look like</span></span>

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

<span data-ttu-id="8bc25-269">Am Speicherort der c#-Datei kann das Host Programm von der Eingabeaufforderung aus ausgeführt werden, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="8bc25-269">At the location of the C# file, the host program can be run from the command prompt by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="8bc25-270">in diesem Fall wird die Ausgabe in die Konsole geschrieben, ähnlich wie</span><span class="sxs-lookup"><span data-stu-id="8bc25-270">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="8bc25-271">Aufgrund der Interoperabilität des Compilers mit Namespaces könnten wir unsere Q# callables ohne die-Anweisung verfügbar machen `using NamespaceName;` und den c#-Namespace Titel einfach zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8bc25-271">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="8bc25-272">Das heißt, indem durch ersetzt wird `namespace host` `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-272">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="8bc25-273">Einschließen der Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="8bc25-273">Including the resources estimator</span></span>

<span data-ttu-id="8bc25-274">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Erfordert eine etwas andere Implementierung zum Abrufen der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8bc25-274">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="8bc25-275">Anstatt Sie als Variable mit einer-Anweisung zu instanziieren `using` (wie dies bei der der Fall ist `QuantumSimulator` ), können wir die Objekte der Klasse über</span><span class="sxs-lookup"><span data-stu-id="8bc25-275">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="8bc25-276">Beachten Sie, dass anstelle eines einzelnen Ziel Simulators, der von mehreren Vorgängen verwendet werden soll Q# , jeweils eine instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-276">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="8bc25-277">Dies liegt daran, dass die Objekte selbst geändert werden, wenn Sie als Zielcomputer verwendet werden, und ihre Ergebnisse anschließend mit der-Klassenmethode abgerufen werden können `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-277">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="8bc25-278">Zum Ausführen der Vorgänge für die Ressourcenschätzung verwenden wir</span><span class="sxs-lookup"><span data-stu-id="8bc25-278">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="8bc25-279">und dann die Ergebnisse als durch Tabstopps getrennte Werte (TSV) mit `estimatorSingleQ.ToTSV()` und Abrufen `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-279">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="8bc25-280">Ein vollständiges c#-Host Programm, das sowohl den als auch den verwendet, könnte das folgende Format haben `QuantumSimulator` `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="8bc25-280">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

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


<span data-ttu-id="8bc25-281">Dies ergibt eine Ausgabe ähnlich der</span><span class="sxs-lookup"><span data-stu-id="8bc25-281">which would yield output similar to</span></span>

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

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="8bc25-282">Q# Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="8bc25-282">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="8bc25-283">Q# Jupyter-Notebooks verwenden den I Q# -Kernel, mit dem Sie callables in einem einzigen Notebook definieren, kompilieren und ausführen können, Q# ---alle neben Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-283">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="8bc25-284">Dies bedeutet, dass es zwar möglich ist, den Inhalt von Dateien zu importieren und zu verwenden `*.qs` Q# , aber im Lauf Zeitmodell nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-284">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the run model.</span></span>

<span data-ttu-id="8bc25-285">Hier wird ausführlich erläutert, wie die Q# oben definierten Vorgänge ausgeführt werden, aber eine umfassendere Einführung in die Verwendung Q# von jupyter Notebooks finden Sie unter Einführung [in Q# und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="8bc25-285">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="8bc25-286">Definieren von Vorgängen</span><span class="sxs-lookup"><span data-stu-id="8bc25-286">Defining operations</span></span>

<span data-ttu-id="8bc25-287">In einem Q# Jupyter Notebook geben Sie den Q# Code genau so ein, wie er im Namespace einer Q# Datei gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="8bc25-287">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="8bc25-288">Daher können wir den Zugriff auf callables aus den [ Q# Standardbibliotheken](xref:microsoft.quantum.libraries.standard.intro) mit `open` Anweisungen für die jeweiligen Namespaces aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8bc25-288">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.libraries.standard.intro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="8bc25-289">Wenn eine Zelle mit einer solchen Anweisung ausgeführt wird, sind die Definitionen aus diesen Namespaces im gesamten Arbeitsbereich verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bc25-289">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="8bc25-290">Callables von [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic) und [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon) (z. b. [`H`](xref:Microsoft.Quantum.Intrinsic.H) und [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) ) sind automatisch für Vorgänge verfügbar, die in Zellen in Q# jupyter-Notebooks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-290">Callables from [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic) and [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon) (for example, [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="8bc25-291">Dies gilt jedoch nicht für Code, der aus externen Q# Quelldateien eingefügt wurde (ein Prozess, der bei Einführung [zu Q# und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)angezeigt wird).</span><span class="sxs-lookup"><span data-stu-id="8bc25-291">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="8bc25-292">Ebenso erfordert die Definition von Vorgängen lediglich das Schreiben des Q# Codes und das Ausführen der Zelle.</span><span class="sxs-lookup"><span data-stu-id="8bc25-292">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

<span data-ttu-id="8bc25-293">In der Ausgabe werden dann diese Vorgänge aufgelistet, die aus zukünftigen Zellen aufgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="8bc25-293">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="8bc25-294">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="8bc25-294">Target machines</span></span>

<span data-ttu-id="8bc25-295">Die Funktionen zum Ausführen von Vorgängen auf bestimmten Ziel Computern werden über [I Q# Magic-Befehle](xref:microsoft.quantum.guide.quickref.iqsharp)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8bc25-295">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="8bc25-296">Beispielsweise `%simulate` verwendet die `QuantumSimulator` , und `%estimate` verwendet Folgendes `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="8bc25-296">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="8bc25-297">Übergeben von Eingaben an Funktionen und Vorgänge</span><span class="sxs-lookup"><span data-stu-id="8bc25-297">Passing inputs to functions and operations</span></span>

<span data-ttu-id="8bc25-298">Um Eingaben an die Vorgänge zu übergeben Q# , können die Argumente als `key=value` Paare an den Befehl "Magic ausführen" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-298">To pass inputs to the Q# operations, the arguments can be passed as `key=value` pairs to the run magic command.</span></span>
<span data-ttu-id="8bc25-299">Um also `MeasureSuperpositionArray` mit vier Qubits auszuführen, können wir Folgendes ausführen `%simulate MeasureSuperpositionArray n=4` :</span><span class="sxs-lookup"><span data-stu-id="8bc25-299">So, to run `MeasureSuperpositionArray` with four qubits, we can run `%simulate MeasureSuperpositionArray n=4`:</span></span>

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

<span data-ttu-id="8bc25-300">Dieses Muster kann ähnlich mit `%estimate` und anderen Run-Befehlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-300">This pattern can be used similarly with `%estimate` and other run commands.</span></span>

### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="8bc25-301">Verwenden Q# von Code aus anderen Projekten oder Paketen</span><span class="sxs-lookup"><span data-stu-id="8bc25-301">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="8bc25-302">Standardmäßig lädt eine Q# Jupyter Notebook alle `.qs` Dateien im aktuellen Ordner und macht Ihre Q# Vorgänge und Funktionen für die Verwendung im Notebook verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8bc25-302">By default, a Q# Jupyter Notebook loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the notebook.</span></span> <span data-ttu-id="8bc25-303">Der [ `%who` Magic-Befehl](xref:microsoft.quantum.iqsharp.magic-ref.who) listet alle zurzeit verfügbaren Q# Vorgänge und Funktionen auf.</span><span class="sxs-lookup"><span data-stu-id="8bc25-303">The [`%who` magic command](xref:microsoft.quantum.iqsharp.magic-ref.who) lists all currently-available Q# operations and functions.</span></span>

<span data-ttu-id="8bc25-304">Zum Laden Q# von Code aus einem anderen Ordner kann der [ `%project` Magic-Befehl](xref:microsoft.quantum.iqsharp.magic-ref.project) verwendet werden, um einen Verweis auf eine `.csproj` Datei für ein Q# Projekt (d. h. ein Projekt, das auf verweist) hinzuzufügen `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-304">To load Q# code from another folder, the [`%project` magic command](xref:microsoft.quantum.iqsharp.magic-ref.project) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span> <span data-ttu-id="8bc25-305">Mit diesem Befehl werden alle `.qs` Dateien im Ordner kompiliert, die die `.csproj` (und Unterordner) enthalten.</span><span class="sxs-lookup"><span data-stu-id="8bc25-305">This command will compile any `.qs` files in the folder containing the `.csproj` (and subfolders).</span></span> <span data-ttu-id="8bc25-306">Außerdem werden alle Pakete rekursiv geladen `PackageReference` Q# `ProjectReference` , auf die über-oder-Projekte verwiesen wird `.csproj`</span><span class="sxs-lookup"><span data-stu-id="8bc25-306">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span> 

<span data-ttu-id="8bc25-307">Beispielsweise simulieren die folgenden Zellen einen- Q# Vorgang aus einem externen Projekt, bei dem auf den Projektpfad relativ zum aktuellen Ordner verwiesen wird:</span><span class="sxs-lookup"><span data-stu-id="8bc25-307">As an example, the following cells simulate a Q# operation from an external project, where the project path is referenced relative to the current folder:</span></span>

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

<span data-ttu-id="8bc25-308">Q#Verwenden Sie den [ `%package` Magic-Befehl](xref:microsoft.quantum.iqsharp.magic-ref.package), um externe Pakete mit Code zu laden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-308">To load external packages containing Q# code, use the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="8bc25-309">Durch das Laden eines Pakets werden auch alle benutzerdefinierten Magic-Befehle oder Anzeige Encoder verfügbar gemacht, die in Assemblys enthalten sind, die Teil des Pakets sind.</span><span class="sxs-lookup"><span data-stu-id="8bc25-309">Loading a package will also make available any custom magic commands or display encoders that are contained in any assemblies that are part of the package.</span></span>

<span data-ttu-id="8bc25-310">Stellen Sie zum Laden externer Pakete oder Q# Projekte bei der Notebook-Initialisierung sicher, dass der Notebook-Ordner eine Datei enthält, auf `.csproj` die verweist `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-310">To load external packages or Q# projects at notebook intialization time, ensure that the notebook folder contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="8bc25-311">Fügen Sie der-Eigenschaft die- `.csproj` Eigenschaft hinzu `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="8bc25-311">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="8bc25-312">Dies weist Q# darauf hin, `ProjectReference` dass alle `PackageReference` Elemente in der `.csproj` Ladezeit des Notebooks rekursiv geladen werden.</span><span class="sxs-lookup"><span data-stu-id="8bc25-312">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` at notebook load time.</span></span>

<span data-ttu-id="8bc25-313">Hier ist beispielsweise eine einfache Datei, die `.csproj` bewirkt, dass Q# das Paket automatisch geladen wird `Microsoft.Quantum.Chemistry` :</span><span class="sxs-lookup"><span data-stu-id="8bc25-313">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="8bc25-314">Diese benutzerdefinierte `<IQSharpLoadAutomatically>` Eigenschaft wird derzeit von Q# Jupyter Notebook Hosts benötigt, aber in Zukunft kann dies das Standardverhalten für eine Datei sein, die `.csproj` sich im selben Ordner wie die Notebook-Datei befindet.</span><span class="sxs-lookup"><span data-stu-id="8bc25-314">Currently this custom `<IQSharpLoadAutomatically>` property is required by Q# Jupyter Notebook hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the notebook file.</span></span>

> [!NOTE]
> <span data-ttu-id="8bc25-315">Die `<QsharpCompile>` -Einstellung in `.csproj` wird derzeit von Q# Jupyter Notebook Hosts ignoriert, und alle `.qs` Dateien im-Ordner der `.csproj` (einschließlich der Unterordner) werden geladen und kompiliert.</span><span class="sxs-lookup"><span data-stu-id="8bc25-315">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Q# Jupyter Notebook hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="8bc25-316">Die Unterstützung für `.csproj` Einstellungen wird in Zukunft verbessert (Weitere Informationen finden Sie unter [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) ).</span><span class="sxs-lookup"><span data-stu-id="8bc25-316">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>
