---
title: Testen und Debuggen von Q-Programmen
description: Erfahren Sie, wie Sie Komponententests, Fakten und Assertionen verwenden und Funktionen zum Testen und Debuggen von Quantenprogrammen absetzen.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030581"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="ea32e-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="ea32e-103">Testing and Debugging</span></span>

<span data-ttu-id="ea32e-104">Wie bei der klassischen Programmierung ist es wichtig, in der Lage zu sein, zu überprüfen, ob Quantenprogramme wie beabsichtigt wirken, und in der Lage zu sein, ein Quantenprogramm zu diagnostizieren, das falsch ist.</span><span class="sxs-lookup"><span data-stu-id="ea32e-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="ea32e-105">In diesem Abschnitt behandeln wir die Tools, die von Q- zum Testen und Debuggen von Quantenprogrammen angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="ea32e-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="ea32e-106">Komponententests</span><span class="sxs-lookup"><span data-stu-id="ea32e-106">Unit Tests</span></span>

<span data-ttu-id="ea32e-107">Ein gängiger Ansatz zum Testen klassischer Programme besteht darin, kleine Programme zu schreiben, die *als Komponententests* bezeichnet werden und Code in einer Bibliothek ausführen, und die Ausgabe mit einer erwarteten Ausgabe zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="ea32e-108">Zum Beispiel können wir sicherstellen, dass `Square(2)` die Rückgabe, `4`da wir von *vornherein* wissen, dass 2 , 2 = 4 .</span><span class="sxs-lookup"><span data-stu-id="ea32e-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="ea32e-109">Die Q-Datei unterstützt das Erstellen von Komponententests für Quantenprogramme, die als Tests innerhalb des xUnit-Komponententestframeworks ausgeführt werden können. [xUnit](https://xunit.github.io/)</span><span class="sxs-lookup"><span data-stu-id="ea32e-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="ea32e-110">Erstellen eines Testprojekts</span><span class="sxs-lookup"><span data-stu-id="ea32e-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ea32e-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ea32e-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ea32e-112">Öffnen Sie Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="ea32e-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="ea32e-113">Gehen Sie `File` zum `New`  >  `Project...`Menü und wählen Sie .</span><span class="sxs-lookup"><span data-stu-id="ea32e-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="ea32e-114">Suchen Sie in der `Q#`oberen rechten `Q# Test Project` Ecke nach , und wählen Sie die Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="ea32e-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ea32e-115">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ea32e-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ea32e-116">Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ea32e-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="ea32e-117">Das neue Projekt verfügt `Tests.qs`über eine einzelne Datei , die einen bequemen Ort zum Definieren neuer Q-Komponententests bietet.</span><span class="sxs-lookup"><span data-stu-id="ea32e-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="ea32e-118">Zunächst enthält diese Datei `AllocateQubit` einen Beispielkomponententest, der überprüft, ob{0}sich ein neu zugewiesenes Qubit im Zustand .'ket' befindet, und eine Meldung ausgibt:</span><span class="sxs-lookup"><span data-stu-id="ea32e-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:neu: <span data-ttu-id="ea32e-119">Jede Operation oder Funktion von Qa, die ein Argument des Typs `Unit` und die Rückgaben `Unit` annimmt, kann über das `@Test("...")` Attribut als Komponententest markiert werden.</span><span class="sxs-lookup"><span data-stu-id="ea32e-119">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="ea32e-120">Das Argument für `"QuantumSimulator"` dieses Attribut oben gibt das Ziel an, auf dem der Test ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="ea32e-121">Ein einzelner Test kann auf mehreren Zielen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ea32e-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="ea32e-122">Fügen Sie z. `@Test("ResourcesEstimator")` `AllocateQubit`B. ein Attribut oben hinzu.</span><span class="sxs-lookup"><span data-stu-id="ea32e-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="ea32e-123">Speichern Sie die Datei, und führen Sie alle Tests aus.</span><span class="sxs-lookup"><span data-stu-id="ea32e-123">Save the file and execute all tests.</span></span> <span data-ttu-id="ea32e-124">Es sollte nun zwei Komponententests geben, einen, bei dem AllocateQubit auf dem QuantumSimulator ausgeführt wird, und einen, bei dem es im ResourceEstimator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="ea32e-125">Die integrierten Ziele "QuantumSimulator", "ToffoliSimulator" und "ResourcesEstimator" werden als gültige Ausführungsziele für Komponententests erkannt.</span><span class="sxs-lookup"><span data-stu-id="ea32e-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="ea32e-126">Es ist auch möglich, einen vollqualifizierten Namen anzugeben, um ein benutzerdefiniertes Ausführungsziel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ea32e-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="ea32e-127">Ausführen von Q-Unit-Tests</span><span class="sxs-lookup"><span data-stu-id="ea32e-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ea32e-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ea32e-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ea32e-129">Gehen Sie als einmaliges Setup pro `Test` Lösung `Test Settings`  >  `Default Processor Architecture`  > zum Menü und wählen Sie `X64`aus.</span><span class="sxs-lookup"><span data-stu-id="ea32e-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="ea32e-130">Die Standardeinstellung für die Prozessorarchitektur für Visual`.suo`Studio wird in der Projektmappenoptionendatei ( ) für jede Projektmappe gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ea32e-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="ea32e-131">Wenn Sie diese Datei löschen, müssen `X64` Sie die Prozessorarchitektur erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="ea32e-132">Erstellen Sie das Projekt, gehen Sie zum `Test` Menü und wählen Sie `Windows`  >  `Test Explorer`.</span><span class="sxs-lookup"><span data-stu-id="ea32e-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="ea32e-133">`AllocateQubit`wird in der Liste der `Not Run Tests` Tests in der Gruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ea32e-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="ea32e-134">Wählen `Run All` oder führen Sie diesen individuellen Test aus, und er sollte bestehen!</span><span class="sxs-lookup"><span data-stu-id="ea32e-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ea32e-135">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ea32e-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ea32e-136">Um Tests auszuführen, navigieren Sie zum Projektordner (dem Ordner, der enthält `Tests.csproj`), und führen Sie den Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ea32e-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="ea32e-137">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="ea32e-137">You should get output similar to the following:</span></span>

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

<span data-ttu-id="ea32e-138">Komponententests können nach ihrem Namen und/oder dem Ausführungsziel gefiltert werden:</span><span class="sxs-lookup"><span data-stu-id="ea32e-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="ea32e-139">Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> hat den Typ `(String -> Unit)` und ermöglicht die Erstellung von Diagnosemeldungen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ea32e-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ea32e-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ea32e-141">Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test geklickt haben, wird ein Bereich mit Informationen zur Testausführung angezeigt: Status "Übergeben/fehlgeschlagen", verstrichene Zeit und ein "Output"-Link.</span><span class="sxs-lookup"><span data-stu-id="ea32e-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="ea32e-142">Wenn Sie auf den Link "Ausgabe" klicken, wird die Testausgabe in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ea32e-142">If you click the "Output" link, test output will open in a new window.</span></span>

![Testausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ea32e-144">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ea32e-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ea32e-145">Der Status "Pass/Fail" für jeden `dotnet test`Test wird von auf der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="ea32e-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="ea32e-146">Bei fehlerhaften Tests werden die Ausgaben auch auf die Konsole gedruckt, um den Fehler zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="ea32e-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="ea32e-147">Fakten und Behauptungen</span><span class="sxs-lookup"><span data-stu-id="ea32e-147">Facts and Assertions</span></span>

<span data-ttu-id="ea32e-148">Da Funktionen in Q-A keine _logischen_ Nebenwirkungen haben, können alle _anderen Arten_ von `()` Effekten der Ausführung einer Funktion, deren Ausgabetyp das leere Tupel ist, niemals innerhalb eines Q-Programms beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="ea32e-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="ea32e-149">Das heißt, ein Zielcomputer kann keine Funktion `()` ausführen, die mit der Garantie zurückkehrt, dass diese Auslassung das Verhalten eines nachfolgenden Q-Codes nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="ea32e-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="ea32e-150">Dies macht `()` die Rückgabe `Unit`von Funktionen (d. h. ) zu einem nützlichen Werkzeug zum Einbetten von Assertionen und Debuggen von Logik in Q-Programme.</span><span class="sxs-lookup"><span data-stu-id="ea32e-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="ea32e-151">Betrachten wir ein einfaches Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ea32e-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="ea32e-152">Hier gibt `fail` das Schlüsselwort an, dass die Berechnung nicht fortgesetzt werden soll, wodurch eine Ausnahme auf dem Zielcomputer ausgelöst wird, auf dem das Q-Programm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="ea32e-153">Definitionsgemäß kann ein solcher Fehler nicht innerhalb von Q- und -Code `fail` beobachtet werden, da nach dem Erreichen einer Anweisung kein weiterer Q-Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="ea32e-154">Wenn wir also über einen `PositivityFact`Aufruf zu gehen, können wir sicher sein, dass sein Input positiv war.</span><span class="sxs-lookup"><span data-stu-id="ea32e-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="ea32e-155">Beachten Sie, dass wir `PositivityFact` das [`Fact`](xref:microsoft.quantum.diagnostics.fact) gleiche Verhalten <xref:microsoft.quantum.diagnostics> wie die Verwendung der Funktion aus dem Namespace implementieren können:</span><span class="sxs-lookup"><span data-stu-id="ea32e-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="ea32e-156">*Assertionen*hingegen werden ähnlich wie Fakten verwendet, können jedoch vom Status der Zielmaschine abhängen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="ea32e-157">Entsprechend werden sie als Vorgänge definiert, während Fakten als Funktionen definiert werden (wie oben).</span><span class="sxs-lookup"><span data-stu-id="ea32e-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="ea32e-158">Um die Unterscheidung zu verstehen, betrachten Sie die folgende Verwendung einer Tatsache innerhalb einer Behauptung:</span><span class="sxs-lookup"><span data-stu-id="ea32e-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="ea32e-159">Hier verwenden wir den <xref:microsoft.quantum.environment.getqubitsavailabletouse> Vorgang, um die Anzahl der qubits zurückzugeben, die zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="ea32e-160">Da dies eindeutig vom globalen Zustand des Programms und `AssertQubitsAreAvailable` seiner Ausführungsumgebung abhängt, muss unsere Definition von auch eine Operation sein.</span><span class="sxs-lookup"><span data-stu-id="ea32e-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="ea32e-161">Wir können diesen globalen Zustand jedoch `Bool` verwenden, um `Fact` einen einfachen Wert als Eingabe für die Funktion zu liefern.</span><span class="sxs-lookup"><span data-stu-id="ea32e-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="ea32e-162">Aufbauend auf diesen Ideen bietet [das Präludium](xref:microsoft.quantum.libraries.standard.prelude) zwei besonders nützliche Behauptungen, <xref:microsoft.quantum.intrinsic.assert> die <xref:microsoft.quantum.intrinsic.assertprob> beide als Operationen auf `()`modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="ea32e-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="ea32e-163">Diese Behauptungen nehmen jeweils einen Pauli-Operator, der eine bestimmte Messung des Interesses beschreibt, ein Quantenregister, an dem eine Messung durchgeführt werden soll, und ein hypothetisches Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="ea32e-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="ea32e-164">Auf Zielmaschinen, die durch Simulation arbeiten, sind wir nicht an [den no-cloning Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen durchführen, ohne das Register zu stören, das an solche Behauptungen übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="ea32e-165">Ein Simulator kann dann, `PositivityFact` ähnlich wie die obige Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beobachtet würde:</span><span class="sxs-lookup"><span data-stu-id="ea32e-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="ea32e-166">Auf physikalischer Quantenhardware, bei der der No-Cloning-Theorem die Untersuchung des Quantenzustands verhindert, kehren die `Assert` und `AssertProb` Operationen einfach ohne andere Wirkung zurück. `()`</span><span class="sxs-lookup"><span data-stu-id="ea32e-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="ea32e-167">Der <xref:microsoft.quantum.diagnostics> Namespace bietet mehrere `Assert` weitere Funktionen der Familie, die es uns ermöglichen, fortgeschrittenere Bedingungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="ea32e-168">Dump-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ea32e-168">Dump Functions</span></span>

<span data-ttu-id="ea32e-169">Zur Fehlerbehebung bei <xref:microsoft.quantum.diagnostics> Quantenprogrammen bietet der Namespace zwei Funktionen, die <xref:microsoft.quantum.diagnostics.dumpmachine> den <xref:microsoft.quantum.diagnostics.dumpregister>aktuellen Status des Zielcomputers in eine Datei einlassen können: und .</span><span class="sxs-lookup"><span data-stu-id="ea32e-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="ea32e-170">Die generierte Ausgabe der einzelnen abhängig enthatonen hängt von der Zielmaschine ab.</span><span class="sxs-lookup"><span data-stu-id="ea32e-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="ea32e-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="ea32e-171">DumpMachine</span></span>

<span data-ttu-id="ea32e-172">Der vollstaatliche Quantensimulator, der als Teil des Quantum Development Kit verteilt ist, schreibt in die Datei die [Wellenfunktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantensystems, als eindimensionales Array komplexer Zahlen, in dem jedes Element die Amplitude der Wahrscheinlichkeit darstellt, den Berechnungsbasiszustand zu messen, wobei "Ket" = "ket"b_.n-1" b_1b_0 für Bits\{b_i\}.</span><span class="sxs-lookup"><span data-stu-id="ea32e-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="ea32e-173">Auf einem Computer mit nur zwei zugeordneten Qubits und im Quantenzustand wird z. B. die{1}Ausgabe des{2}Aufrufs <xref:microsoft.quantum.diagnostics.dumpmachine> {00} von "end" (""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""{2} {10}"""" """""""" """""""" """""""</span><span class="sxs-lookup"><span data-stu-id="ea32e-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="ea32e-174">Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer signifikanten Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ea32e-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="ea32e-175">Der Rest der Zeilen beschreibt die Wahrscheinlichkeitsamplitude der Messung des Basiszustandsvektors in kartesischen und polaren Formaten.</span><span class="sxs-lookup"><span data-stu-id="ea32e-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="ea32e-176">Im Detail für die erste Zeile:</span><span class="sxs-lookup"><span data-stu-id="ea32e-176">In detail for the first row:</span></span>

* <span data-ttu-id="ea32e-177">**`∣0❭:`** Diese Zeile entspricht `0` dem Berechnungsbasiszustand</span><span class="sxs-lookup"><span data-stu-id="ea32e-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="ea32e-178">**`0.707107 +  0.000000 i`**: die Wahrscheinlichkeitsamplitude im kartesischen Format.</span><span class="sxs-lookup"><span data-stu-id="ea32e-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="ea32e-179">**` == `**: `equal` Das Zeichen trennt beide gleichwertigen Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-179">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="ea32e-180">**`**********  `**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustandsvektor zu messen.</span><span class="sxs-lookup"><span data-stu-id="ea32e-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="ea32e-181">**`[ 0.500000 ]`**: der numerische Wert der Magnitude</span><span class="sxs-lookup"><span data-stu-id="ea32e-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="ea32e-182">**`    ---`**: Eine grafische Darstellung der Amplitudenphase (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="ea32e-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="ea32e-183">**`[ 0.0000 rad ]`**: der numerische Wert der Phase (in Radianten).</span><span class="sxs-lookup"><span data-stu-id="ea32e-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="ea32e-184">Sowohl die Größe als auch die Phase werden mit einer grafischen Darstellung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ea32e-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="ea32e-185">Die Größendarstellung ist geradlinig: `*`Sie zeigt einen Balken von , je größer die Wahrscheinlichkeit, je größer der Balken wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="ea32e-186">Für die Phase zeigen wir die folgenden Symbole, um den Winkel basierend auf Bereichen darzustellen:</span><span class="sxs-lookup"><span data-stu-id="ea32e-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="ea32e-187">Die folgenden `DumpMachine` Beispiele zeigen für einige allgemeine Zustände:</span><span class="sxs-lookup"><span data-stu-id="ea32e-187">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="ea32e-188">Die ID eines Qubits wird zur Laufzeit zugewiesen und ist nicht unbedingt an der Reihenfolge ausgerichtet, in der das Qubit zugewiesen wurde, oder seiner Position innerhalb eines Qubit-Registers.</span><span class="sxs-lookup"><span data-stu-id="ea32e-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="ea32e-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ea32e-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="ea32e-190">Sie können eine Qubit-ID in Visual Studio ermitteln, indem Sie einen Haltepunkt in Ihren Code eingeben und den Wert einer qubit-Variablen überprüfen, z. B.:</span><span class="sxs-lookup"><span data-stu-id="ea32e-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Qubit-ID in Visual Studio anzeigen](~/media/qubit_id.png)
  >
  > <span data-ttu-id="ea32e-192">der qubit `0` mit `register2` dem`3`Index auf hat `1` id=`2`, das qubit mit index hat id= .</span><span class="sxs-lookup"><span data-stu-id="ea32e-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="ea32e-193">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ea32e-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="ea32e-194">Sie können eine qubit-ID <xref:microsoft.quantum.intrinsic.message> herausfinden, indem Sie die Funktion verwenden und die qubit-Variable in der Nachricht übergeben, z. B.:</span><span class="sxs-lookup"><span data-stu-id="ea32e-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="ea32e-195">die diese Ausgabe generieren könnte:</span><span class="sxs-lookup"><span data-stu-id="ea32e-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="ea32e-196">was bedeutet, dass das `0` `register2` qubit`3`mit dem Index `1` auf id= hat, hat das qubit mit index id=`2`.</span><span class="sxs-lookup"><span data-stu-id="ea32e-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="ea32e-197"><xref:microsoft.quantum.diagnostics.dumpmachine>ist Teil <xref:microsoft.quantum.diagnostics> des Namespace, daher müssen Sie eine `open` Anweisung hinzufügen, um ihn verwenden zu können:</span><span class="sxs-lookup"><span data-stu-id="ea32e-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="ea32e-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="ea32e-198">DumpRegister</span></span>

<span data-ttu-id="ea32e-199"><xref:microsoft.quantum.diagnostics.dumpregister>funktioniert <xref:microsoft.quantum.diagnostics.dumpmachine>wie , außer es benötigt auch ein Array von Qubits, um die Menge an Informationen auf die für die entsprechenden Qubits relevanten zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="ea32e-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="ea32e-200">Wie <xref:microsoft.quantum.diagnostics.dumpmachine>bei hängt die <xref:microsoft.quantum.diagnostics.dumpregister> von generierten Informationen vom Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="ea32e-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="ea32e-201">Für den Vollzustands-Quantensimulator schreibt er die Wellenfunktion bis zu einer globalen Phase des Quantensubsystems <xref:microsoft.quantum.diagnostics.dumpmachine>in die Datei, die von den bereitgestellten Qubits im gleichen Format wie erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="ea32e-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="ea32e-202">Zum Beispiel, Nehmen Sie erneut einen Computer mit nur zwei zugeordneten Qubits und im Quantenzustand ,{1},,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""({2}{00} {2} {10} {1}(sqrt{2}{0} {2} {1} {2}{0} <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[0]` , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , ,</span><span class="sxs-lookup"><span data-stu-id="ea32e-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="ea32e-203">und <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[1]` aufrufen erzeugt diese Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="ea32e-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="ea32e-204">Im Allgemeinen ist der Zustand eines Registers, das mit einem anderen Register verstrickt ist, ein gemischter Zustand und kein reiner Zustand.</span><span class="sxs-lookup"><span data-stu-id="ea32e-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="ea32e-205">Gibt in <xref:microsoft.quantum.diagnostics.dumpregister> diesem Fall die folgende Meldung aus:</span><span class="sxs-lookup"><span data-stu-id="ea32e-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="ea32e-206">Das folgende Beispiel zeigt Ihnen, <xref:microsoft.quantum.diagnostics.dumpregister> <xref:microsoft.quantum.diagnostics.dumpmachine> wie Sie beides und in Ihrem Q-Code verwenden können:</span><span class="sxs-lookup"><span data-stu-id="ea32e-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="ea32e-207">Debuggen</span><span class="sxs-lookup"><span data-stu-id="ea32e-207">Debugging</span></span>

<span data-ttu-id="ea32e-208">Zusätzlich zu `Assert` `Dump` den Funktionen und Vorgängen unterstützt Qa eine Teilmenge der standardmäßigen Visual Studio-Debugfunktionen: [Festlegen von Zeilenhaltepunkten,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [Schrittweiseieren von Code mit F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) und [Überprüfen von Werten klassischer Variablen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) sind während der Codeausführung im Simulator möglich.</span><span class="sxs-lookup"><span data-stu-id="ea32e-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="ea32e-209">Das Debuggen in Visual Studio Code nutzt die Debugfunktionen, die von der von OmniSharp unterstützten Erweiterung "C" für Visual Studio-Code bereitgestellt werden, und erfordert die Installation der [neuesten Version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span><span class="sxs-lookup"><span data-stu-id="ea32e-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span> 
