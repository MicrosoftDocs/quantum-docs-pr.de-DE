---
title: Testen und Debuggen
description: Erfahren Sie, wie Sie Komponententests, Fakten und Assertionen sowie Dumpfunktionen zum Testen und Debuggen von Quantum-Programmen verwenden.
author: tcNickolas
ms.author: mamykhai
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2f2181d388a59c1c6c5a0f13c9aa49d5fa1e51ae
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833180"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="5d0cc-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="5d0cc-103">Testing and debugging</span></span>

<span data-ttu-id="5d0cc-104">Wie bei der klassischen Programmierung ist es von entscheidender Bedeutung, zu überprüfen, ob Quantum-Programme erwartungsgemäß agieren, und das falsche Verhalten diagnostizieren zu können.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose incorrect behavior.</span></span>
<span data-ttu-id="5d0cc-105">In diesem Abschnitt werden die Tools beschrieben, die von Q# zum Testen und Debuggen von Quantum-Programmen angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="5d0cc-106">Komponententests</span><span class="sxs-lookup"><span data-stu-id="5d0cc-106">Unit Tests</span></span>

<span data-ttu-id="5d0cc-107">Ein gängiger Ansatz zum Testen klassischer Programme ist das Schreiben von kleinen Programmen namens Komponenten *Tests*, die Code in einer Bibliothek ausführen und die Ausgabe mit einer erwarteten Ausgabe vergleichen.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-107">One common approach to testing classical programs is to write small programs called *unit tests*, which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="5d0cc-108">So können Sie z. b. sicherstellen, dass `Square(2)` zurückgibt, `4` da Sie *eine* mit dem Wert "$ 2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-108">For example, you can ensure that `Square(2)` returns `4` since you know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="5d0cc-109">Q# unterstützt das Erstellen von Komponententests für Quantum-Programme, die als Tests innerhalb des [xUnit](https://xunit.github.io/) -Komponenten Test-Frameworks ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-109">Q# supports creating unit tests for quantum programs, and which can run as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="5d0cc-110">Erstellen eines Test Projekts</span><span class="sxs-lookup"><span data-stu-id="5d0cc-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="5d0cc-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="5d0cc-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="5d0cc-112">Öffnen Sie Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="5d0cc-113">Wechseln Sie zum Menü **Datei** , und wählen Sie **Neu > Projekt...** aus. Suchen Sie in der oberen rechten Ecke nach `Q#` , und wählen Sie die Vorlage \*\* Q# Test Projekt\*\* aus.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-113">Go to the **File** menu and select **New > Project...**. In the upper right corner, search for `Q#`, and select the **Q# Test Project** template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="5d0cc-114">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="5d0cc-114">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="5d0cc-115">Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-115">From your favorite command line, run the following command:</span></span>
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="5d0cc-116">Das neue Projekt verfügt über eine einzelne Datei `Tests.qs` , die einen geeigneten Ort zum Definieren neuer Komponenten Q# Tests bietet.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-116">Your new project has a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="5d0cc-117">Diese Datei enthält zunächst einen Beispiel Komponenten Test, `AllocateQubit` der überprüft, ob sich ein neu zugewiesenes Qubit im Zustand "$ \ket $" befindet {0} und eine Meldung ausgibt:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-117">Initially, this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="5d0cc-118">Alle Vorgänge Q# oder Funktionen, die ein Argument vom Typ `Unit` und zurück `Unit` geben, können über das-Attribut als Komponenten Test gekennzeichnet werden `@Test("...")` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-118">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="5d0cc-119">Im vorherigen Beispiel gibt das-Argument dieses Attributs, `"QuantumSimulator"` , das Ziel an, auf dem der Test ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-119">In the previous example, the argument to that attribute, `"QuantumSimulator"`, specifies the target on which the test runs.</span></span> <span data-ttu-id="5d0cc-120">Ein einzelner Test kann auf mehreren Zielen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-120">A single test can run on multiple targets.</span></span> <span data-ttu-id="5d0cc-121">Fügen Sie z. b. ein Attribut `@Test("ResourcesEstimator")` vor ein `AllocateQubit` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-121">For example, add an attribute `@Test("ResourcesEstimator")` before `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="5d0cc-122">Speichern Sie die Datei, und führen Sie alle Tests aus.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-122">Save the file and run all tests.</span></span> <span data-ttu-id="5d0cc-123">Es sollten nun zwei Komponententests vorhanden sein, von denen eine `AllocateQubit` auf dem ausgeführt wird `QuantumSimulator` , und eine, in der Sie ausgeführt wird `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-123">There should now be two unit tests, one where `AllocateQubit` runs on the `QuantumSimulator`, and one where it runs in the `ResourcesEstimator`.</span></span> 

<span data-ttu-id="5d0cc-124">Der Q# Compiler erkennt die integrierten Ziele `"QuantumSimulator"` , `"ToffoliSimulator"` und `"ResourcesEstimator"` als gültige Testlauf-Ziele für Komponententests.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-124">The Q# compiler recognizes the built-in targets `"QuantumSimulator"`, `"ToffoliSimulator"`, and `"ResourcesEstimator"` as valid run targets for unit tests.</span></span> <span data-ttu-id="5d0cc-125">Es ist auch möglich, einen voll qualifizierten Namen anzugeben, um ein benutzerdefiniertes Lauf Ziel zu definieren.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-125">It is also possible to specify any fully qualified name to define a custom run target.</span></span> 

### <a name="running-no-locq-unit-tests"></a><span data-ttu-id="5d0cc-126">Ausführen von Komponenten Q# Tests</span><span class="sxs-lookup"><span data-stu-id="5d0cc-126">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="5d0cc-127">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="5d0cc-127">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="5d0cc-128">Wechseln Sie als einmalige Einrichtung pro Lösung zum Menü **Test** , und wählen Sie **Testeinstellungen > Standard Prozessorarchitektur > x64**aus.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-128">As a one-time per-solution setup, go to the **Test** menu and select **Test Settings > Default Processor Architecture > X64**.</span></span>

> [!TIP]
> <span data-ttu-id="5d0cc-129">Die Standardeinstellung für die Prozessorarchitektur für Visual Studio wird in der Projektmappendatei ( `.suo` ) für jede Lösung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-129">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="5d0cc-130">Wenn Sie diese Datei löschen, müssen Sie **x64** als Prozessorarchitektur erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-130">If you delete this file, then you need to select **X64** as your processor architecture again.</span></span>

<span data-ttu-id="5d0cc-131">Erstellen Sie das Projekt, öffnen Sie das Menü " **Test** ", und wählen Sie **Windows > Test-Explorer**aus.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-131">Build the project, open the **Test** menu, and select **Windows > Test Explorer**.</span></span> <span data-ttu-id="5d0cc-132">" **Zustellungs Zuordnung** " wird in der Liste der Tests in der Gruppe " **nicht ausgeführt Tests** " angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-132">**AllocateQubit** displays in the list of tests in the **Not Run Tests** group.</span></span> <span data-ttu-id="5d0cc-133">Wählen Sie **alle ausführen** aus, oder führen Sie den einzelnen Test aus.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-133">Select **Run All** or run this individual test.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="5d0cc-134">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="5d0cc-134">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="5d0cc-135">Navigieren Sie zum Ausführen von Tests zum Projektordner (dem Ordner, der enthält `Tests.csproj` ), und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-135">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and run the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="5d0cc-136">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-136">You should get output similar to the following:</span></span>

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

<span data-ttu-id="5d0cc-137">Komponententests können nach Ihrem Namen oder dem Lauf Ziel gefiltert werden:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-137">Unit tests can be filtered according to their name or the run target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="5d0cc-138">Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> weist `(String -> Unit)` den Typ auf und ermöglicht die Erstellung von Diagnosemeldungen.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-138">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="5d0cc-139">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="5d0cc-139">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="5d0cc-140">Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test klicken, wird ein Panel mit Informationen zum Testlauf angezeigt: Status "erfolgreich"/"Fehler", verstrichene Zeit und ein Link zur Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-140">After you run a test in Test Explorer and click on the test, a panel displays with information about test run: Pass/fail status, elapsed time, and a link to the output.</span></span> <span data-ttu-id="5d0cc-141">Klicken Sie auf **Ausgabe** , um die Test Ausgabe in einem neuen Fenster zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-141">Click **Output** to open the test output in a new window.</span></span>

![Test Ausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="5d0cc-143">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="5d0cc-143">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="5d0cc-144">Der Status "erfolgreich/fehlgeschlagen" für jeden Test wird von auf der Konsole gedruckt `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-144">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="5d0cc-145">Bei fehlgeschlagenen Tests werden die Ausgaben auch in der Konsole gedruckt, um den Fehler zu diagnostizieren.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-145">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="5d0cc-146">Fakten und Assertionen</span><span class="sxs-lookup"><span data-stu-id="5d0cc-146">Facts and Assertions</span></span>

<span data-ttu-id="5d0cc-147">Da Funktionen in Q# keine _logischen_ Nebeneffekte haben, können Sie innerhalb eines Programms niemals davon Q# ausgehen, dass eine Funktion, deren Ausgabetyp ein leeres Tupel ist, von einem Programm aus ausgeführt wird `()` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-147">Because functions in Q# have no _logical_ side effects, you can never observe, from within a Q# program, any other kinds of effects from running a function whose output type is the empty tuple `()`.</span></span>
<span data-ttu-id="5d0cc-148">Das heißt, ein Zielcomputer kann festlegen, dass keine Funktion ausgeführt werden soll, die `()` mit der Garantie zurückgibt, dass diese Auslassung das Verhalten eines nachfolgenden Codes nicht ändert Q# .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-148">That is, a target machine can choose not to run any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="5d0cc-149">Dieses Verhalten bewirkt, dass Funktionen, die zurückgeben `()` (z.b. `Unit` ), ein nützliches Tool zum Einbetten von Assertionen und zum Debuggen von Q#</span><span class="sxs-lookup"><span data-stu-id="5d0cc-149">This behavior makes functions returning `()` (such as `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="5d0cc-150">Betrachten wir ein einfaches Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-150">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="5d0cc-151">Hier gibt das Schlüsselwort an, `fail` dass die Berechnung nicht fortgesetzt werden soll, und löst eine Ausnahme auf dem Zielcomputer aus, auf dem das Programm ausgeführt wird Q# .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-151">Here, the keyword `fail` indicates that the computation should not proceed, and raises an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="5d0cc-152">Definitionsgemäß kann ein Fehler dieser Art nicht innerhalb von erkannt werden Q# , da der Zielcomputer den Code nicht mehr ausführt, Q# nachdem eine Anweisung erreicht wurde `fail` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-152">By definition, a failure of this kind cannot be observed from within Q#, as the target machine no longer runs the Q# code after reaching a `fail` statement.</span></span>
<span data-ttu-id="5d0cc-153">Wenn wir also einen Rückruf von fortsetzen `PositivityFact` , können wir sicher sein, dass die Eingabe positiv ist.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-153">Thus, if we proceed past a call to `PositivityFact`, we can be assured that its input was positive.</span></span>

<span data-ttu-id="5d0cc-154">Beachten Sie, dass das gleiche Verhalten wie die `PositivityFact` Verwendung der- [`Fact`](xref:microsoft.quantum.diagnostics.fact) Funktion aus dem-Namespace implementiert werden kann <xref:microsoft.quantum.diagnostics> :</span><span class="sxs-lookup"><span data-stu-id="5d0cc-154">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="5d0cc-155">Assertionen werden dagegen ähnlich wie Fakten *verwendet, hängen*jedoch möglicherweise vom Status des Ziel Computers ab.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-155">*Assertions*, on the other hand, are used similarly to facts but may depend on the state of the target machine.</span></span> <span data-ttu-id="5d0cc-156">Dementsprechend werden Sie als Vorgänge definiert, wohingegen Fakten als Funktionen definiert werden (wie im vorherigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="5d0cc-156">Correspondingly, they are defined as operations, whereas facts are defined as functions (as in the previous example).</span></span>
<span data-ttu-id="5d0cc-157">Um den Unterschied zu verstehen, sollten Sie die folgende Verwendung eines Fakts innerhalb einer Aussage in Erwägung gezogen haben:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-157">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="5d0cc-158">Hier wird der-Vorgang verwendet <xref:microsoft.quantum.environment.getqubitsavailabletouse> , um die Anzahl der zu verwendenden Qubits zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-158">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="5d0cc-159">Da dies vom globalen Status des Programms und seiner Lauf Umgebung abhängig ist, muss unsere Definition von `AssertQubitsAreAvailable` ebenfalls ein Vorgang sein.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-159">As this depends on the global state of the program and its run environment, our definition of `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="5d0cc-160">Der globale Status kann jedoch verwendet werden, um einen einfachen `Bool` Wert als Eingabe für die Funktion zu erhalten `Fact` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-160">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="5d0cc-161">[Der Auftakt](xref:microsoft.quantum.libraries.standard.prelude), auf dem diese Ideen aufbauen, bietet zwei besonders nützliche Assertionen, die <xref:microsoft.quantum.diagnostics.assertmeasurement> <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> beide als Vorgänge für modelliert werden `()` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-161">[The prelude](xref:microsoft.quantum.libraries.standard.prelude), building on these ideas, offers two especially useful assertions, <xref:microsoft.quantum.diagnostics.assertmeasurement> and <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> both modeled as operations onto `()`.</span></span> <span data-ttu-id="5d0cc-162">Diese Assertionen akzeptieren jeweils einen Pauli-Operator, der ein bestimmtes Maß an Interesse, ein Quantum-Register, für das eine Messung durchgeführt wird, und ein hypothetisches Ergebnis beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-162">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="5d0cc-163">Zielcomputer, die bei der Simulation arbeiten, werden nicht durch [das No-Klon-Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen ausführen, ohne das Register zu beeinträchtigen, das an solche Assertionen weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-163">Target machines which work by simulation are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register that passes to such assertions.</span></span>
<span data-ttu-id="5d0cc-164">Ein Simulator kann dann, ähnlich wie bei der `PositivityFact` vorherigen Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beachtet wird:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-164">A simulator can then, similar to the `PositivityFact` function previous, stop computation if the hypothetical outcome is not observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    AssertMeasurement([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="5d0cc-165">Bei physischer Quantum-Hardware, bei der das No-Klon-Theorem die Untersuchung eines Quantum-Zustands verhindert, werden die `AssertMeasurement` -und- `AssertMeasurementProbability` Vorgänge einfach `()` ohne andere Auswirkungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-165">On physical quantum hardware, where the no-cloning theorem prevents examination of a quantum state, the `AssertMeasurement` and `AssertMeasurementProbability` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="5d0cc-166">Der- <xref:microsoft.quantum.diagnostics> Namespace stellt mehrere weitere Funktionen der- `Assert` Familie bereit, mit denen Sie erweiterte Bedingungen überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-166">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family, with which you can check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="5d0cc-167">Dumpfunktionen</span><span class="sxs-lookup"><span data-stu-id="5d0cc-167">Dump Functions</span></span>

<span data-ttu-id="5d0cc-168">Zur Unterstützung der Problembehandlung von Quantum-Programmen bietet der- <xref:microsoft.quantum.diagnostics> Namespace zwei Funktionen, mit denen der aktuelle Status des Ziel Computers in einer Datei gespeichert werden kann: <xref:microsoft.quantum.diagnostics.dumpmachine> und <xref:microsoft.quantum.diagnostics.dumpregister> .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-168">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="5d0cc-169">Die generierte Ausgabe hängt von dem Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-169">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="5d0cc-170">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="5d0cc-170">DumpMachine</span></span>

<span data-ttu-id="5d0cc-171">Der als Teil des Quantum Development Kit verteilte Volltext-Quantum-Simulator schreibt in die Datei der [Wave-Funktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantum-Systems. als eindimensionales Array komplexer Zahlen, bei dem jedes Element die Amplitude der Wahrscheinlichkeits Wahrscheinlichkeit für die Messung des Berechnungsbasis Zustands $ \ket{n} $ darstellt, wobei $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ für Bits $ \{ b_i \} $.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-171">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="5d0cc-172">Beispielsweise wird auf einem Computer, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\call{(1 + i)} {2} \ket die folgende {10} <xref:microsoft.quantum.diagnostics.dumpmachine> Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-172">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="5d0cc-173">Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-173">The first row provides a comment with the ids of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="5d0cc-174">In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{n} $ im kartesischen und Polar Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-174">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="5d0cc-175">Im Detail für die erste Zeile:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-175">In detail for the first row:</span></span>

* <span data-ttu-id="5d0cc-176">**`∣0❭:`** Diese Zeile entspricht dem `0` Status der Berechnungs Ebene.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-176">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="5d0cc-177">**`0.707107 +  0.000000 i`**: die Wahrscheinlichkeits Amplitude im kartesischen Format.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-177">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="5d0cc-178">**` == `**: das `equal` Vorzeichen trennt beide äquivalente Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-178">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="5d0cc-179">**`**********  `**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-179">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="5d0cc-180">**`[ 0.500000 ]`**: der numerische Wert der Größe.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-180">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="5d0cc-181">**`    ---`**: Eine grafische Darstellung der Amplitude-Phase (Weitere Informationen finden Sie in der folgenden Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="5d0cc-181">**`    ---`**: A graphical representation of the amplitude's phase (see the following output).</span></span>
* <span data-ttu-id="5d0cc-182">**`[ 0.0000 rad ]`**: der numerische Wert der Phase (im Bogenmaße).</span><span class="sxs-lookup"><span data-stu-id="5d0cc-182">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="5d0cc-183">Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-183">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="5d0cc-184">Die Größen Darstellung ist geradlinig: Sie zeigt einen Balken an `*` , je größer die Wahrscheinlichkeit, mit der die Leiste größer wird.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-184">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="5d0cc-185">In der Phase zeigen wir die folgenden Symbole zur Darstellung des Winkels basierend auf Bereichen:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-185">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="5d0cc-186">Die folgenden Beispiele zeigen `DumpMachine` einige allgemeine Zustände:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-186">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="5d0cc-187">Die ID eines Qubit wird zur Laufzeit zugewiesen und ist nicht notwendigerweise an die Reihenfolge ausgerichtet, in der das Qubit zugewiesen wurde, oder an seine Position in einem Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-187">The id of a qubit is assigned at runtime and is not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="5d0cc-188">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="5d0cc-188">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="5d0cc-189">Sie können in Visual Studio eine Qubit-ID suchen, indem Sie einen Haltepunkt in Ihrem Code platzieren und den Wert einer Qubit-Variablen untersuchen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-189">You can locate a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Anzeigen der Qubit-ID in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="5d0cc-191">Das Qubit mit Index `0` on `register2` hat ID = `3` , das Qubit mit dem Index `1` hat ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-191">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="5d0cc-192">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="5d0cc-192">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="5d0cc-193">Sie können eine Qubit-ID suchen, indem Sie die <xref:microsoft.quantum.intrinsic.message> -Funktion verwenden und die Qubit-Variable in der Nachricht übergeben, z. b.:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-193">You can locate a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="5d0cc-194">Dies könnte folgende Ausgabe generieren:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-194">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="5d0cc-195">Dies bedeutet, dass das Qubit mit dem Index `0` on `register2` ID = ist `3` , das Qubit mit Index `1` ID = `2` .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-195">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="5d0cc-196">Da <xref:microsoft.quantum.diagnostics.dumpmachine> Teil des-  <xref:microsoft.quantum.diagnostics> Namespace ist, müssen Sie eine-Anweisung hinzufügen, `open` um darauf zugreifen zu können:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-196">Since <xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, you must add an `open` statement to access it:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="5d0cc-197">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="5d0cc-197">DumpRegister</span></span>

<span data-ttu-id="5d0cc-198"><xref:microsoft.quantum.diagnostics.dumpregister> funktioniert wie <xref:microsoft.quantum.diagnostics.dumpmachine> , mit der Ausnahme, dass es auch ein Array von Qubits verwendet, um die Menge der Informationen auf die für die entsprechenden Qubits relevanten Informationen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-198"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except that it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="5d0cc-199">Wie bei <xref:microsoft.quantum.diagnostics.dumpmachine> hängen die von generierten Informationen vom <xref:microsoft.quantum.diagnostics.dumpregister> Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-199">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="5d0cc-200">Für den vollständigen Quantum-Simulator schreibt er in die Datei, die von der Wave-Funktion bis zu einer globalen Phase des von den bereitgestellten Qubits generierten Quantums in demselben Format wie angegeben wird <xref:microsoft.quantum.diagnostics.dumpmachine> .</span><span class="sxs-lookup"><span data-stu-id="5d0cc-200">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="5d0cc-201">Nehmen Sie z. b. erneut einen Computer an, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\bruch {(1 + i)} {2} \ket {10} =-e. ^ {-i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\bruch{(1 + i)} {2} \ket {1} ) \otimes \bruchteil {-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ beim Aufrufen <xref:microsoft.quantum.diagnostics.dumpregister> von wird `qubit[0]` Diese Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-201">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="5d0cc-202">durch <xref:microsoft.quantum.diagnostics.dumpregister> das Aufrufen von für wird `qubit[1]` Diese Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-202">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="5d0cc-203">Im Allgemeinen ist der Status eines Registers, das mit einem anderen Register entkoppelt ist, ein gemischter Zustand und kein reiner Zustand.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-203">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="5d0cc-204">In diesem Fall wird <xref:microsoft.quantum.diagnostics.dumpregister> die folgende Meldung ausgegeben:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-204">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="5d0cc-205">Im folgenden Beispiel wird gezeigt, wie Sie sowohl <xref:microsoft.quantum.diagnostics.dumpregister> als auch <xref:microsoft.quantum.diagnostics.dumpmachine> in Ihrem Q# Code verwenden können:</span><span class="sxs-lookup"><span data-stu-id="5d0cc-205">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="5d0cc-206">Debuggen</span><span class="sxs-lookup"><span data-stu-id="5d0cc-206">Debugging</span></span>

<span data-ttu-id="5d0cc-207">Zusätzlich zu den `Assert` `Dump` Funktionen und Vorgängen von und Q# unterstützt eine Teilmenge der standardmäßigen Visual Studio-Debuggingfunktionen: das [Festlegen von Zeilen Haltepunkten](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), das Durchlaufen von [Code mithilfe von F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)und das Überprüfen [von Werten klassischer Variablen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) sind beim Ausführen des Codes im Simulator alles möglich.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-207">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger), and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible when running your code on the simulator.</span></span>

<span data-ttu-id="5d0cc-208">Beim Debuggen in Visual Studio Code werden die Debuggingfunktionen von c# für Visual Studio Code Erweiterung von omnisharp genutzt, und die [neueste Version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)muss installiert werden.</span><span class="sxs-lookup"><span data-stu-id="5d0cc-208">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
