---
title: 'Testen und Debuggen von f #-Programmen'
description: Erfahren Sie, wie Sie Komponententests, Fakten und Assertionen sowie Dumpfunktionen zum Testen und Debuggen von Quantum-Programmen verwenden.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 8131c2ec9320b5075c37370e12ad39a4df5bd3d5
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2020
ms.locfileid: "79022860"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="38eaf-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="38eaf-103">Testing and Debugging</span></span>

<span data-ttu-id="38eaf-104">Wie bei der klassischen Programmierung ist es von entscheidender Bedeutung, zu überprüfen, ob Quantum-Programme erwartungsgemäß agieren, und ein ungültiges Quantum-Programm diagnostizieren zu können.</span><span class="sxs-lookup"><span data-stu-id="38eaf-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="38eaf-105">In diesem Abschnitt werden die Tools beschrieben, die von Q # zum Testen und Debuggen von Quantum-Programmen angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="38eaf-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="38eaf-106">Komponententests</span><span class="sxs-lookup"><span data-stu-id="38eaf-106">Unit Tests</span></span>

<span data-ttu-id="38eaf-107">Ein gängiger Ansatz zum Testen klassischer Programme ist das Schreiben von kleinen Programmen namens Komponenten *Tests* , die Code in einer Bibliothek ausführen und die Ausgabe mit einer erwarteten Ausgabe vergleichen.</span><span class="sxs-lookup"><span data-stu-id="38eaf-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="38eaf-108">Beispielsweise möchten wir möglicherweise sicherstellen, dass `Square(2)` `4`zurückgibt, da wir *ein* -Wert von "$ 2 ^ 2 = $4" kennen.</span><span class="sxs-lookup"><span data-stu-id="38eaf-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="38eaf-109">Q # unterstützt das Erstellen von Komponententests für Quantum-Programme und kann als Tests innerhalb des [xUnit](https://xunit.github.io/) -Komponenten Test-Frameworks ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="38eaf-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="38eaf-110">Erstellen eines Test Projekts</span><span class="sxs-lookup"><span data-stu-id="38eaf-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="38eaf-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="38eaf-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="38eaf-112">Öffnen Sie Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="38eaf-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="38eaf-113">Wechseln Sie zum Menü `File`, und wählen Sie `New` > `Project...`aus.</span><span class="sxs-lookup"><span data-stu-id="38eaf-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="38eaf-114">Suchen Sie in der oberen rechten Ecke nach `Q#`, und wählen Sie die `Q# Test Project` Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="38eaf-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="38eaf-115">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="38eaf-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="38eaf-116">Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="38eaf-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="38eaf-117">Das neue Projekt verfügt über eine einzelne Datei `Tests.qs`, die einen geeigneten Ort zum Definieren neuer Q #-Komponententests bietet.</span><span class="sxs-lookup"><span data-stu-id="38eaf-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="38eaf-118">Diese Datei enthält anfänglich einen Beispiel-Komponenten Test `AllocateQubit` der überprüft, ob sich ein neu zugewiesenes Qubit im $ \ket{0}$ State befindet und eine Meldung ausgibt:</span><span class="sxs-lookup"><span data-stu-id="38eaf-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="38eaf-119">: New: jeder Q #-Vorgang bzw. jede Funktion, die ein Argument vom Typ `Unit` und `Unit` zurückgibt, kann mit dem `@Test("...")`-Attribut als Komponenten Test gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="38eaf-119">:new: Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="38eaf-120">Das Argument für dieses Attribut, `"QuantumSimulator"` oben, gibt das Ziel an, auf dem der Test ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38eaf-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="38eaf-121">Ein einzelner Test kann auf mehreren Zielen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="38eaf-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="38eaf-122">Fügen Sie z. b. ein Attribut `@Test("ResourcesEstimator")` oberhalb `AllocateQubit`hinzu.</span><span class="sxs-lookup"><span data-stu-id="38eaf-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="38eaf-123">Speichern Sie die Datei, und führen Sie alle Tests aus.</span><span class="sxs-lookup"><span data-stu-id="38eaf-123">Save the file and execute all tests.</span></span> <span data-ttu-id="38eaf-124">Es sollten nun zwei Komponententests vorhanden sein, eine, in der "zuordnungsequbit" für den quantumsimulator ausgeführt wird, und eine, in der Sie im resourceestimator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38eaf-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="38eaf-125">Der f #-Compiler erkennt die integrierten Ziele "quantumsimulator", "-ffolisimulator" und "resourcesestimator" als gültige Ausführungs Ziele für Komponententests.</span><span class="sxs-lookup"><span data-stu-id="38eaf-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="38eaf-126">Es ist auch möglich, einen voll qualifizierten Namen anzugeben, um ein benutzerdefiniertes Ausführungs Ziel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="38eaf-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="38eaf-127">Ausführen von f #-Komponenten Tests</span><span class="sxs-lookup"><span data-stu-id="38eaf-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="38eaf-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="38eaf-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="38eaf-129">Wechseln Sie als einmalige Einrichtung pro Lösung zu `Test` Menü, und wählen Sie `Test Settings` > `Default Processor Architecture` > `X64`aus.</span><span class="sxs-lookup"><span data-stu-id="38eaf-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="38eaf-130">Die Standardeinstellung für die Prozessorarchitektur für Visual Studio wird in der Projektmappen-Optionsdatei (`.suo`) für jede Lösung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="38eaf-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="38eaf-131">Wenn Sie diese Datei löschen, müssen Sie `X64` als Prozessorarchitektur erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="38eaf-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="38eaf-132">Erstellen Sie das Projekt, wechseln Sie zum Menü `Test`, und wählen Sie `Windows` > `Test Explorer`aus.</span><span class="sxs-lookup"><span data-stu-id="38eaf-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="38eaf-133">`AllocateQubit` wird in der Liste der Tests in der `Not Run Tests` Gruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38eaf-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="38eaf-134">Wählen Sie `Run All` aus, oder führen Sie den einzelnen Test aus, und es sollte bestanden werden!</span><span class="sxs-lookup"><span data-stu-id="38eaf-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="38eaf-135">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="38eaf-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="38eaf-136">Navigieren Sie zum Ausführen von Tests zum Projektordner (dem Ordner, der `Tests.csproj`enthält), und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="38eaf-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="38eaf-137">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="38eaf-137">You should get output similar to the following:</span></span>

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

<span data-ttu-id="38eaf-138">Komponententests können nach Ihrem Namen und/oder dem Ausführungs Ziel gefiltert werden:</span><span class="sxs-lookup"><span data-stu-id="38eaf-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="38eaf-139">Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> hat den Typ `(String -> Unit)` und ermöglicht die Erstellung von Diagnose Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="38eaf-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="38eaf-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="38eaf-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="38eaf-141">Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test klicken, wird ein Panel mit Informationen zur Testausführung angezeigt: Status "erfolgreich"/"Fehler", verstrichene Zeit und "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="38eaf-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="38eaf-142">Wenn Sie auf den Link "Output" klicken, wird die Test Ausgabe in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="38eaf-142">If you click the "Output" link, test output will open in a new window.</span></span>

![Test Ausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="38eaf-144">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="38eaf-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="38eaf-145">Der Status "erfolgreich/fehlgeschlagen" für jeden Test wird von `dotnet test`in der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="38eaf-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="38eaf-146">Bei fehlgeschlagenen Tests werden die Ausgaben auch in der Konsole gedruckt, um den Fehler zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="38eaf-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="38eaf-147">Fakten und Assertionen</span><span class="sxs-lookup"><span data-stu-id="38eaf-147">Facts and Assertions</span></span>

<span data-ttu-id="38eaf-148">Da Funktionen in Q # keine _logischen_ Nebeneffekte haben, können _andere Arten_ von Effekten beim Ausführen einer Funktion, deren Ausgabetyp das leere Tupel ist `()` nicht innerhalb eines Q #-Programms beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="38eaf-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="38eaf-149">Das heißt, ein Zielcomputer kann keine Funktion ausführen, die `()` zurückgibt, wobei sichergestellt wird, dass diese Auslassung das Verhalten eines nachfolgenden f #-Codes nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="38eaf-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="38eaf-150">Dadurch werden Funktionen, die `()` zurückgeben (d.h. `Unit`), ein nützliches Tool zum Einbetten von Assertionen und zum Debuggen in Q #-Programme.</span><span class="sxs-lookup"><span data-stu-id="38eaf-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="38eaf-151">Betrachten wir ein einfaches Beispiel:</span><span class="sxs-lookup"><span data-stu-id="38eaf-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="38eaf-152">Hier gibt das Schlüsselwort `fail` an, dass die Berechnung nicht fortgesetzt werden soll, wodurch eine Ausnahme auf dem Zielcomputer ausgelöst wird, der das Q #-Programm ausführt.</span><span class="sxs-lookup"><span data-stu-id="38eaf-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="38eaf-153">Definitionsgemäß kann ein Fehler dieser Art nicht innerhalb von q # beobachtet werden, da kein weiterer Q #-Code ausgeführt wird, nachdem eine `fail`-Anweisung erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="38eaf-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="38eaf-154">Wenn wir also einen `PositivityFact`-Aufrufvorgang fortsetzen, können wir sicher sein, dass die Eingabe positiv ist.</span><span class="sxs-lookup"><span data-stu-id="38eaf-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="38eaf-155">Beachten Sie, dass das gleiche Verhalten wie `PositivityFact` mithilfe der [`Fact`](xref:microsoft.quantum.diagnostics.fact) -Funktion aus dem <xref:microsoft.quantum.diagnostics>-Namespace implementiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="38eaf-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

<span data-ttu-id="38eaf-156">Assertionen werden dagegen ähnlich wie Fakten *verwendet, sind*aber möglicherweise vom Status des Ziel Computers abhängig.</span><span class="sxs-lookup"><span data-stu-id="38eaf-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="38eaf-157">Dementsprechend werden Sie als Vorgänge definiert, wohingegen Fakten als Funktionen definiert werden (wie oben beschrieben).</span><span class="sxs-lookup"><span data-stu-id="38eaf-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="38eaf-158">Um den Unterschied zu verstehen, sollten Sie die folgende Verwendung eines Fakts innerhalb einer Aussage in Erwägung gezogen haben:</span><span class="sxs-lookup"><span data-stu-id="38eaf-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="38eaf-159">Hier verwenden wir den Vorgang <xref:microsoft.quantum.environment.getqubitsavailabletouse>, um die Anzahl der zu verwendenden Qubits zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="38eaf-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="38eaf-160">Da dies eindeutig vom globalen Status des Programms und seiner Ausführungsumgebung abhängt, muss auch die Definition von `AssertQubitsAreAvailable` ein Vorgang sein.</span><span class="sxs-lookup"><span data-stu-id="38eaf-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="38eaf-161">Der globale Status kann jedoch verwendet werden, um einen einfachen `Bool` Wert als Eingabe für die `Fact`-Funktion zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38eaf-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="38eaf-162">Wenn Sie auf diese Ideen aufbauen, bietet [das präspiel](xref:microsoft.quantum.libraries.standard.prelude) zwei besonders nützliche Assertionen, <xref:microsoft.quantum.intrinsic.assert> und <xref:microsoft.quantum.intrinsic.assertprob> beide als Vorgänge auf `()`modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="38eaf-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="38eaf-163">Diese Assertionen akzeptieren jeweils einen Pauli-Operator, der ein bestimmtes Maß an Interesse beschreibt, ein Quantum-Register, für das eine Messung durchgeführt werden soll, und ein hypothetisches Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="38eaf-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="38eaf-164">Auf Ziel Computern, die bei der Simulation funktionieren, werden wir nicht durch [das No-Klon-Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen durchführen, ohne dass das an diese Assertionen weiter gegebene Register gestört wird.</span><span class="sxs-lookup"><span data-stu-id="38eaf-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="38eaf-165">Ein Simulator kann dann, ähnlich wie in der obigen `PositivityFact`-Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beachtet wird:</span><span class="sxs-lookup"><span data-stu-id="38eaf-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="38eaf-166">Bei physischer Quantum-Hardware, bei der das No-Klon-Theorem die Prüfung des Quantums verhindert, werden die `Assert`-und `AssertProb` Vorgänge einfach `()` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38eaf-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="38eaf-167">Der <xref:microsoft.quantum.diagnostics>-Namespace stellt mehrere weitere Funktionen der `Assert`-Familie bereit, die es uns ermöglichen, erweiterte Bedingungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="38eaf-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="38eaf-168">Dumpfunktionen</span><span class="sxs-lookup"><span data-stu-id="38eaf-168">Dump Functions</span></span>

<span data-ttu-id="38eaf-169">Zur Unterstützung der Problembehandlung von Quantum-Programmen bietet der <xref:microsoft.quantum.diagnostics>-Namespace zwei Funktionen, mit denen der aktuelle Status des Ziel Computers in einer Datei gespeichert werden kann: <xref:microsoft.quantum.diagnostics.dumpmachine> und <xref:microsoft.quantum.diagnostics.dumpregister>.</span><span class="sxs-lookup"><span data-stu-id="38eaf-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="38eaf-170">Die generierte Ausgabe hängt von dem Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="38eaf-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="38eaf-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="38eaf-171">DumpMachine</span></span>

<span data-ttu-id="38eaf-172">Der als Teil des Quantum Development Kit verteilte Volltext-Quantum-Simulator schreibt in die Datei der [Wave-Funktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantum-Systems. als eindimensionales Array komplexer Zahlen, bei dem jedes Element die Amplitude der Wahrscheinlichkeits Wahrscheinlichkeit für die Messung des Berechnungsbasis Zustands $ \ket{n} $ darstellt, wobei $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ für Bits $\{b_i\}$.</span><span class="sxs-lookup"><span data-stu-id="38eaf-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="38eaf-173">Beispielsweise auf einem Computer, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\call{(1 + i)}{2} \ket{10}wird die folgende Ausgabe generiert:<xref:microsoft.quantum.diagnostics.dumpmachine></span><span class="sxs-lookup"><span data-stu-id="38eaf-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="38eaf-174">Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="38eaf-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="38eaf-175">In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{n} $ im kartesischen und Polar Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="38eaf-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="38eaf-176">Im Detail für die erste Zeile:</span><span class="sxs-lookup"><span data-stu-id="38eaf-176">In detail for the first row:</span></span>

* <span data-ttu-id="38eaf-177">**`∣0❭:`** diese Zeile dem Status der `0` Berechnungsbasis entspricht.</span><span class="sxs-lookup"><span data-stu-id="38eaf-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="38eaf-178">**`0.707107 +  0.000000 i`** : die Wahrscheinlichkeits Amplitude im kartesischen Format.</span><span class="sxs-lookup"><span data-stu-id="38eaf-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="38eaf-179">**` == `** : das `equal` Vorzeichen trennt beide äquivalente Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="38eaf-179">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="38eaf-180">**`**********  `** : eine grafische Darstellung der Größe, die Anzahl der `*` proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.</span><span class="sxs-lookup"><span data-stu-id="38eaf-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="38eaf-181">**`[ 0.500000 ]`** : der numerische Wert der Größe.</span><span class="sxs-lookup"><span data-stu-id="38eaf-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="38eaf-182">**`    ---`** : eine grafische Darstellung der Amplitude-Phase (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="38eaf-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="38eaf-183">**`[ 0.0000 rad ]`** : der numerische Wert der Phase (im Bogenmaße).</span><span class="sxs-lookup"><span data-stu-id="38eaf-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="38eaf-184">Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38eaf-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="38eaf-185">Die Größen Darstellung ist geradlinig: Sie zeigt einen Balken `*`an, je größer die Wahrscheinlichkeit, mit der die Leiste größer wird.</span><span class="sxs-lookup"><span data-stu-id="38eaf-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="38eaf-186">In der Phase zeigen wir die folgenden Symbole zur Darstellung des Winkels basierend auf Bereichen:</span><span class="sxs-lookup"><span data-stu-id="38eaf-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="38eaf-187">In den folgenden Beispielen werden `DumpMachine` für einige gängige Zustände veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="38eaf-187">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="38eaf-188">Die ID eines Qubit wird zur Laufzeit zugewiesen und ist nicht notwendigerweise an die Reihenfolge ausgerichtet, in der das Qubit zugeordnet wurde, oder an seine Position in einem Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="38eaf-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="38eaf-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="38eaf-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="38eaf-190">Sie können eine Qubit-ID in Visual Studio ermitteln, indem Sie einen Haltepunkt in Ihrem Code platzieren und den Wert einer Qubit-Variablen untersuchen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="38eaf-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Anzeigen der Qubit-ID in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="38eaf-192">Das Qubit mit Index `0` auf `register2` hat ID =`3`, das Qubit mit Index `1` hat ID =`2`.</span><span class="sxs-lookup"><span data-stu-id="38eaf-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="38eaf-193">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="38eaf-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="38eaf-194">Sie können eine Qubit-ID ermitteln, indem Sie die <xref:microsoft.quantum.intrinsic.message>-Funktion verwenden und die Qubit-Variable in der Nachricht übergeben, z. b.:</span><span class="sxs-lookup"><span data-stu-id="38eaf-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="38eaf-195">Dies könnte folgende Ausgabe generieren:</span><span class="sxs-lookup"><span data-stu-id="38eaf-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="38eaf-196">Dies bedeutet, dass das Qubit mit Index `0` auf `register2` ID =`3`, das Qubit mit Index `1` ID =`2`aufweist.</span><span class="sxs-lookup"><span data-stu-id="38eaf-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="38eaf-197"><xref:microsoft.quantum.diagnostics.dumpmachine> ist Teil des <xref:microsoft.quantum.diagnostics>-Namespace. damit Sie ihn verwenden können, müssen Sie eine `open`-Anweisung hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="38eaf-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="38eaf-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="38eaf-198">DumpRegister</span></span>

<span data-ttu-id="38eaf-199"><xref:microsoft.quantum.diagnostics.dumpregister> funktioniert wie <xref:microsoft.quantum.diagnostics.dumpmachine>, mit dem Unterschied, dass es auch ein Array von Qubits verwendet, um die Menge der Informationen auf die für die entsprechenden Qubits relevanten Informationen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="38eaf-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="38eaf-200">Wie bei <xref:microsoft.quantum.diagnostics.dumpmachine>hängt die von <xref:microsoft.quantum.diagnostics.dumpregister> generierten Informationen vom Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="38eaf-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="38eaf-201">Für den vollständigen Quantum-Simulator schreibt er in die Datei, die von der Wave-Funktion bis zu einer globalen Phase des von den bereitgestellten Qubits generierten Quantums in demselben Format wie <xref:microsoft.quantum.diagnostics.dumpmachine>generiert wird.</span><span class="sxs-lookup"><span data-stu-id="38eaf-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="38eaf-202">Nehmen Sie z. b. einen Computer an, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\bruch {(1 + i)}{2} \ket{10} =-e ^ {-i \ pi/4} ((\frac{1}{\sqrt{2}} \ket{0}-\bruchteil {(1 + i)}{2} \ket{1}) \otimes \bruchteil {-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ Aufrufen von <xref:microsoft.quantum.diagnostics.dumpregister> für `qubit[0]` generiert diese Ausgabe. :</span><span class="sxs-lookup"><span data-stu-id="38eaf-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="38eaf-203">Wenn Sie <xref:microsoft.quantum.diagnostics.dumpregister> für `qubit[1]` aufrufen, wird diese Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="38eaf-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="38eaf-204">Im Allgemeinen ist der Status eines Registers, das mit einem anderen Register entkoppelt ist, ein gemischter Zustand und kein reiner Zustand.</span><span class="sxs-lookup"><span data-stu-id="38eaf-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="38eaf-205">In diesem Fall gibt <xref:microsoft.quantum.diagnostics.dumpregister> die folgende Meldung aus:</span><span class="sxs-lookup"><span data-stu-id="38eaf-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="38eaf-206">Im folgenden Beispiel wird gezeigt, wie Sie sowohl <xref:microsoft.quantum.diagnostics.dumpregister> als auch <xref:microsoft.quantum.diagnostics.dumpmachine> in Ihrem Q #-Code verwenden können:</span><span class="sxs-lookup"><span data-stu-id="38eaf-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="38eaf-207">Debuggen</span><span class="sxs-lookup"><span data-stu-id="38eaf-207">Debugging</span></span>

<span data-ttu-id="38eaf-208">Zusätzlich zu den Funktionen und Vorgängen von `Assert` und `Dump` unterstützt Q # eine Teilmenge der standardmäßigen Visual Studio-Debuggingfunktionen: das [Festlegen von Zeilen Haltepunkten](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), das [durchlaufen von Code mithilfe von F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) und das Überprüfen [von Werten klassischer Variablen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) ist während der Codeausführung im Simulator möglich.</span><span class="sxs-lookup"><span data-stu-id="38eaf-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="38eaf-209">Beim Debuggen in Visual Studio Code werden die Debuggingfunktionen von genutzt [, die von](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)für die C# Visual Studio Code Erweiterung von omnisharp bereitgestellt werden</span><span class="sxs-lookup"><span data-stu-id="38eaf-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span> 
