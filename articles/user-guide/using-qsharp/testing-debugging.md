---
title: Testen und Debuggen
description: Erfahren Sie, wie Sie Komponententests, Fakten und Assertionen sowie Dumpfunktionen zum Testen und Debuggen von Quantum-Programmen verwenden.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
ms.openlocfilehash: dd6c7ae8a016423f26c37f3eedf0ae9c1d126b78
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630024"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="39089-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="39089-103">Testing and debugging</span></span>

<span data-ttu-id="39089-104">Wie bei der klassischen Programmierung ist es von entscheidender Bedeutung, zu überprüfen, ob Quantum-Programme erwartungsgemäß agieren, und ein ungültiges Quantum-Programm diagnostizieren zu können.</span><span class="sxs-lookup"><span data-stu-id="39089-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="39089-105">In diesem Abschnitt werden die Tools beschrieben, die von Q # zum Testen und Debuggen von Quantum-Programmen angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="39089-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="39089-106">Komponententests</span><span class="sxs-lookup"><span data-stu-id="39089-106">Unit Tests</span></span>

<span data-ttu-id="39089-107">Ein gängiger Ansatz zum Testen klassischer Programme ist das Schreiben von kleinen Programmen namens Komponenten *Tests* , die Code in einer Bibliothek ausführen und die Ausgabe mit einer erwarteten Ausgabe vergleichen.</span><span class="sxs-lookup"><span data-stu-id="39089-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="39089-108">Wir möchten beispielsweise sicherstellen, dass `Square(2)` zurückgibt `4` , da wir *ein* -Wert von "$ 2 ^ 2 = $4" kennen.</span><span class="sxs-lookup"><span data-stu-id="39089-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="39089-109">Q # unterstützt das Erstellen von Komponententests für Quantum-Programme und kann als Tests innerhalb des [xUnit](https://xunit.github.io/) -Komponenten Test-Frameworks ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39089-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="39089-110">Erstellen eines Test Projekts</span><span class="sxs-lookup"><span data-stu-id="39089-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="39089-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="39089-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="39089-112">Öffnen Sie Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="39089-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="39089-113">Wechseln Sie zum `File` Menü, und wählen Sie aus `New`  >  `Project...` .</span><span class="sxs-lookup"><span data-stu-id="39089-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="39089-114">Suchen Sie in der oberen rechten Ecke nach `Q#` der Vorlage, und wählen Sie Sie aus `Q# Test Project` .</span><span class="sxs-lookup"><span data-stu-id="39089-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="39089-115">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="39089-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="39089-116">Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39089-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="39089-117">Das neue Projekt verfügt über eine einzelne Datei `Tests.qs` , die einen geeigneten Ort zum Definieren neuer Q #-Komponententests bietet.</span><span class="sxs-lookup"><span data-stu-id="39089-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="39089-118">Diese Datei enthält anfänglich einen Beispiel Komponenten Test `AllocateQubit` , der überprüft, ob sich ein neu zugewiesenes Qubit im Zustand "$ \ket $" befindet {0} und eine Meldung ausgibt:</span><span class="sxs-lookup"><span data-stu-id="39089-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="39089-119">: New: jeder Q #-Vorgang bzw. jede Funktion, die ein Argument vom Typ annimmt `Unit` und zurückgibt, `Unit` kann mit dem-Attribut als Komponenten Test gekennzeichnet werden `@Test("...")` .</span><span class="sxs-lookup"><span data-stu-id="39089-119">:new: Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="39089-120">Das Argument für dieses Attribut ( `"QuantumSimulator"` oben) gibt das Ziel an, auf dem der Test ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39089-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="39089-121">Ein einzelner Test kann auf mehreren Zielen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39089-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="39089-122">Fügen Sie z. b. oben ein Attribut hinzu `@Test("ResourcesEstimator")` `AllocateQubit` .</span><span class="sxs-lookup"><span data-stu-id="39089-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="39089-123">Speichern Sie die Datei, und führen Sie alle Tests aus.</span><span class="sxs-lookup"><span data-stu-id="39089-123">Save the file and execute all tests.</span></span> <span data-ttu-id="39089-124">Es sollten nun zwei Komponententests vorhanden sein, eine, in der "zuordnungsequbit" für den quantumsimulator ausgeführt wird, und eine, in der Sie im resourceestimator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39089-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="39089-125">Der f #-Compiler erkennt die integrierten Ziele "quantumsimulator", "-ffolisimulator" und "resourcesestimator" als gültige Ausführungs Ziele für Komponententests.</span><span class="sxs-lookup"><span data-stu-id="39089-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="39089-126">Es ist auch möglich, einen voll qualifizierten Namen anzugeben, um ein benutzerdefiniertes Ausführungs Ziel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="39089-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="39089-127">Ausführen von f #-Komponenten Tests</span><span class="sxs-lookup"><span data-stu-id="39089-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="39089-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="39089-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="39089-129">Wechseln Sie als einmalige Einrichtung pro Lösung zum `Test` Menü, und wählen Sie aus `Test Settings`  >  `Default Processor Architecture`  >  `X64` .</span><span class="sxs-lookup"><span data-stu-id="39089-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="39089-130">Die Standardeinstellung für die Prozessorarchitektur für Visual Studio wird in der Projektmappendatei ( `.suo` ) für jede Lösung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="39089-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="39089-131">Wenn Sie diese Datei löschen, müssen Sie `X64` die Prozessorarchitektur erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="39089-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="39089-132">Erstellen Sie das Projekt, klicken Sie auf das `Test` Menü, und wählen Sie aus `Windows`  >  `Test Explorer` .</span><span class="sxs-lookup"><span data-stu-id="39089-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="39089-133">`AllocateQubit`wird in der Liste der Tests in der Gruppe angezeigt `Not Run Tests` .</span><span class="sxs-lookup"><span data-stu-id="39089-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="39089-134">Wählen Sie den `Run All` einzelnen Test aus, oder führen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="39089-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="39089-135">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="39089-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="39089-136">Navigieren Sie zum Ausführen von Tests zum Projektordner (dem Ordner, der enthält `Tests.csproj` ), und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="39089-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="39089-137">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="39089-137">You should get output similar to the following:</span></span>

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

<span data-ttu-id="39089-138">Komponententests können nach Ihrem Namen und/oder dem Ausführungs Ziel gefiltert werden:</span><span class="sxs-lookup"><span data-stu-id="39089-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="39089-139">Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> weist `(String -> Unit)` den Typ auf und ermöglicht die Erstellung von Diagnosemeldungen.</span><span class="sxs-lookup"><span data-stu-id="39089-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="39089-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="39089-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="39089-141">Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test klicken, wird ein Panel mit Informationen zur Testausführung angezeigt: Status "erfolgreich"/"Fehler", verstrichene Zeit und "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="39089-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="39089-142">Wenn Sie auf den Link "Output" klicken, wird die Test Ausgabe in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="39089-142">If you click the "Output" link, test output will open in a new window.</span></span>

![Test Ausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="39089-144">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="39089-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="39089-145">Der Status "erfolgreich/fehlgeschlagen" für jeden Test wird von auf der Konsole gedruckt `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="39089-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="39089-146">Bei fehlgeschlagenen Tests werden die Ausgaben auch in der Konsole gedruckt, um den Fehler zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="39089-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="39089-147">Fakten und Assertionen</span><span class="sxs-lookup"><span data-stu-id="39089-147">Facts and Assertions</span></span>

<span data-ttu-id="39089-148">Da Funktionen in Q # keine _logischen_ Nebeneffekte haben, können _andere Arten_ von Effekten beim Ausführen einer Funktion, deren Ausgabetyp das leere Tupel ist, `()` nie innerhalb eines Q #-Programms beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="39089-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="39089-149">Das heißt, ein Zielcomputer kann festlegen, dass keine Funktion ausgeführt werden soll, die `()` mit der Garantie zurückgibt, dass diese Auslassung das Verhalten eines nachfolgenden f #-Codes nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="39089-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="39089-150">Dies bewirkt, `()` dass Funktionen (d.h. `Unit` ) ein nützliches Tool zum Einbetten von Assertionen und zum Debuggen in Q #-Programme zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="39089-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="39089-151">Betrachten wir ein einfaches Beispiel:</span><span class="sxs-lookup"><span data-stu-id="39089-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="39089-152">Hier gibt das Schlüsselwort `fail` an, dass die Berechnung nicht fortgesetzt werden soll, und es wird eine Ausnahme auf dem Zielcomputer ausgelöst, der das Q #-Programm ausführt</span><span class="sxs-lookup"><span data-stu-id="39089-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="39089-153">Definitionsgemäß kann ein Fehler dieser Art nicht innerhalb von q # beobachtet werden, da kein weiterer Q #-Code ausgeführt wird, nachdem eine `fail` Anweisung erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="39089-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="39089-154">Wenn wir also einen-Rückruf fortsetzen `PositivityFact` , können wir sicher sein, dass die Eingabe positiv ist.</span><span class="sxs-lookup"><span data-stu-id="39089-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="39089-155">Beachten Sie, dass das gleiche Verhalten wie die `PositivityFact` Verwendung der- [`Fact`](xref:microsoft.quantum.diagnostics.fact) Funktion aus dem-Namespace implementiert werden kann <xref:microsoft.quantum.diagnostics> :</span><span class="sxs-lookup"><span data-stu-id="39089-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

<span data-ttu-id="39089-156">Assertionen werden dagegen ähnlich wie Fakten *verwendet, sind*aber möglicherweise vom Status des Ziel Computers abhängig.</span><span class="sxs-lookup"><span data-stu-id="39089-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="39089-157">Dementsprechend werden Sie als Vorgänge definiert, wohingegen Fakten als Funktionen definiert werden (wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="39089-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="39089-158">Um den Unterschied zu verstehen, sollten Sie die folgende Verwendung eines Fakts innerhalb einer Aussage in Erwägung gezogen haben:</span><span class="sxs-lookup"><span data-stu-id="39089-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="39089-159">Hier wird der-Vorgang verwendet <xref:microsoft.quantum.environment.getqubitsavailabletouse> , um die Anzahl der zu verwendenden Qubits zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="39089-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="39089-160">Da dies eindeutig vom globalen Status des Programms und seiner Ausführungsumgebung abhängt, muss unsere Definition von `AssertQubitsAreAvailable` ebenfalls ein Vorgang sein.</span><span class="sxs-lookup"><span data-stu-id="39089-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="39089-161">Der globale Status kann jedoch verwendet werden, um einen einfachen `Bool` Wert als Eingabe für die Funktion zu erhalten `Fact` .</span><span class="sxs-lookup"><span data-stu-id="39089-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="39089-162">Wenn Sie auf diese Ideen aufbauen, bietet [das präspiel](xref:microsoft.quantum.libraries.standard.prelude) zwei besonders nützliche Assertionen, die <xref:microsoft.quantum.intrinsic.assert> <xref:microsoft.quantum.intrinsic.assertprob> beide als Vorgänge für modelliert werden `()` .</span><span class="sxs-lookup"><span data-stu-id="39089-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="39089-163">Diese Assertionen akzeptieren jeweils einen Pauli-Operator, der ein bestimmtes Maß an Interesse beschreibt, ein Quantum-Register, für das eine Messung durchgeführt werden soll, und ein hypothetisches Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="39089-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="39089-164">Auf Ziel Computern, die bei der Simulation funktionieren, werden wir nicht durch [das No-Klon-Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen durchführen, ohne dass das an diese Assertionen weiter gegebene Register gestört wird.</span><span class="sxs-lookup"><span data-stu-id="39089-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="39089-165">Ein Simulator kann dann, ähnlich wie die `PositivityFact` obige Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beachtet wird:</span><span class="sxs-lookup"><span data-stu-id="39089-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="39089-166">Bei physischer Quantum-Hardware, bei der das No-Klon-Theorem die Prüfung des Quantums verhindert, werden die `Assert` `AssertProb` Vorgänge und einfach `()` ohne andere Auswirkungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39089-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="39089-167">Der- <xref:microsoft.quantum.diagnostics> Namespace bietet mehrere weitere Funktionen der- `Assert` Familie, die es uns ermöglichen, erweiterte Bedingungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="39089-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="39089-168">Dumpfunktionen</span><span class="sxs-lookup"><span data-stu-id="39089-168">Dump Functions</span></span>

<span data-ttu-id="39089-169">Zur Unterstützung der Problembehandlung von Quantum-Programmen bietet der- <xref:microsoft.quantum.diagnostics> Namespace zwei Funktionen, mit denen der aktuelle Status des Ziel Computers in einer Datei gespeichert werden kann: <xref:microsoft.quantum.diagnostics.dumpmachine> und <xref:microsoft.quantum.diagnostics.dumpregister> .</span><span class="sxs-lookup"><span data-stu-id="39089-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="39089-170">Die generierte Ausgabe hängt von dem Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="39089-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="39089-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="39089-171">DumpMachine</span></span>

<span data-ttu-id="39089-172">Der als Teil des Quantum Development Kit verteilte Volltext-Quantum-Simulator schreibt in die Datei der [Wave-Funktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantum-Systems. als eindimensionales Array komplexer Zahlen, bei dem jedes Element die Amplitude der Wahrscheinlichkeits Wahrscheinlichkeit für die Messung des Berechnungsbasis Zustands $ \ket{n} $ darstellt, wobei $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ für Bits $ \{ b_i \} $.</span><span class="sxs-lookup"><span data-stu-id="39089-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="39089-173">Beispielsweise wird auf einem Computer, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\call{(1 + i)} {2} \ket die folgende {10} <xref:microsoft.quantum.diagnostics.dumpmachine> Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="39089-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="39089-174">Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="39089-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="39089-175">In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{n} $ im kartesischen und Polar Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="39089-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="39089-176">Im Detail für die erste Zeile:</span><span class="sxs-lookup"><span data-stu-id="39089-176">In detail for the first row:</span></span>

* <span data-ttu-id="39089-177">**`∣0❭:`** Diese Zeile entspricht dem `0` Status der Berechnungs Ebene.</span><span class="sxs-lookup"><span data-stu-id="39089-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="39089-178">**`0.707107 +  0.000000 i`**: die Wahrscheinlichkeits Amplitude im kartesischen Format.</span><span class="sxs-lookup"><span data-stu-id="39089-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="39089-179">**` == `**: das `equal` Vorzeichen trennt beide äquivalente Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="39089-179">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="39089-180">**`**********  `**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.</span><span class="sxs-lookup"><span data-stu-id="39089-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="39089-181">**`[ 0.500000 ]`**: der numerische Wert der Größe.</span><span class="sxs-lookup"><span data-stu-id="39089-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="39089-182">**`    ---`**: Eine grafische Darstellung der Amplitude-Phase (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="39089-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="39089-183">**`[ 0.0000 rad ]`**: der numerische Wert der Phase (im Bogenmaße).</span><span class="sxs-lookup"><span data-stu-id="39089-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="39089-184">Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="39089-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="39089-185">Die Größen Darstellung ist geradlinig: Sie zeigt einen Balken an `*` , je größer die Wahrscheinlichkeit, mit der die Leiste größer wird.</span><span class="sxs-lookup"><span data-stu-id="39089-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="39089-186">In der Phase zeigen wir die folgenden Symbole zur Darstellung des Winkels basierend auf Bereichen:</span><span class="sxs-lookup"><span data-stu-id="39089-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

<span data-ttu-id="39089-187">Die folgenden Beispiele zeigen `DumpMachine` einige allgemeine Zustände:</span><span class="sxs-lookup"><span data-stu-id="39089-187">The following examples show `DumpMachine` for some common states:</span></span>

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > <span data-ttu-id="39089-188">Die ID eines Qubit wird zur Laufzeit zugewiesen und ist nicht notwendigerweise an die Reihenfolge ausgerichtet, in der das Qubit zugeordnet wurde, oder an seine Position in einem Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="39089-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="39089-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="39089-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="39089-190">Sie können eine Qubit-ID in Visual Studio ermitteln, indem Sie einen Haltepunkt in Ihrem Code platzieren und den Wert einer Qubit-Variablen untersuchen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="39089-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Anzeigen der Qubit-ID in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="39089-192">Das Qubit mit Index `0` on `register2` hat ID = `3` , das Qubit mit dem Index `1` hat ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="39089-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="39089-193">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="39089-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="39089-194">Sie können eine Qubit-ID ermitteln, indem Sie die <xref:microsoft.quantum.intrinsic.message> -Funktion verwenden und die Qubit-Variable in der Nachricht übergeben, z. b.:</span><span class="sxs-lookup"><span data-stu-id="39089-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="39089-195">Dies könnte folgende Ausgabe generieren:</span><span class="sxs-lookup"><span data-stu-id="39089-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="39089-196">Dies bedeutet, dass das Qubit mit dem Index `0` on `register2` ID = ist `3` , das Qubit mit Index `1` ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="39089-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="39089-197"><xref:microsoft.quantum.diagnostics.dumpmachine>ist Teil des- <xref:microsoft.quantum.diagnostics> Namespace. damit Sie ihn verwenden können, müssen Sie eine- `open` Anweisung hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="39089-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a><span data-ttu-id="39089-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="39089-198">DumpRegister</span></span>

<span data-ttu-id="39089-199"><xref:microsoft.quantum.diagnostics.dumpregister>funktioniert wie <xref:microsoft.quantum.diagnostics.dumpmachine> , mit der Ausnahme, dass es auch ein Array von Qubits verwendet, um die Menge der Informationen auf die für die entsprechenden Qubits relevanten Informationen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="39089-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="39089-200">Wie bei <xref:microsoft.quantum.diagnostics.dumpmachine> hängen die von generierten Informationen vom <xref:microsoft.quantum.diagnostics.dumpregister> Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="39089-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="39089-201">Für den vollständigen Quantum-Simulator schreibt er in die Datei, die von der Wave-Funktion bis zu einer globalen Phase des von den bereitgestellten Qubits generierten Quantums in demselben Format wie angegeben wird <xref:microsoft.quantum.diagnostics.dumpmachine> .</span><span class="sxs-lookup"><span data-stu-id="39089-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="39089-202">Nehmen Sie z. b. erneut einen Computer an, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\bruch {(1 + i)} {2} \ket {10} =-e. ^ {-i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\bruch{(1 + i)} {2} \ket {1} ) \otimes \bruchteil {-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ beim Aufrufen <xref:microsoft.quantum.diagnostics.dumpregister> von wird `qubit[0]` Diese Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="39089-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="39089-203">durch <xref:microsoft.quantum.diagnostics.dumpregister> das Aufrufen von für wird `qubit[1]` Diese Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="39089-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="39089-204">Im Allgemeinen ist der Status eines Registers, das mit einem anderen Register entkoppelt ist, ein gemischter Zustand und kein reiner Zustand.</span><span class="sxs-lookup"><span data-stu-id="39089-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="39089-205">In diesem Fall wird <xref:microsoft.quantum.diagnostics.dumpregister> die folgende Meldung ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="39089-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="39089-206">Im folgenden Beispiel wird gezeigt, wie Sie sowohl <xref:microsoft.quantum.diagnostics.dumpregister> als auch <xref:microsoft.quantum.diagnostics.dumpmachine> in Ihrem Q #-Code verwenden können:</span><span class="sxs-lookup"><span data-stu-id="39089-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a><span data-ttu-id="39089-207">Debuggen</span><span class="sxs-lookup"><span data-stu-id="39089-207">Debugging</span></span>

<span data-ttu-id="39089-208">Zusätzlich zu den `Assert` -und- `Dump` Funktionen und-Vorgängen unterstützt Q # eine Teilmenge der standardmäßigen Visual Studio-Debuggingfunktionen: das [Festlegen von Zeilen Haltepunkten](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), das [durchlaufen von Code mithilfe von F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) und das Überprüfen [von Werten klassischer Variablen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) ist während der Codeausführung im Simulator möglich.</span><span class="sxs-lookup"><span data-stu-id="39089-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="39089-209">Beim Debuggen in Visual Studio Code werden die Debuggingfunktionen von c# für Visual Studio Code Erweiterung von omnisharp genutzt, und die [neueste Version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)muss installiert werden.</span><span class="sxs-lookup"><span data-stu-id="39089-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
