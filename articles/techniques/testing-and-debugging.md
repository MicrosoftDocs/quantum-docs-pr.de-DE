---
title: 'F #-Techniken, testen und Debuggen | Microsoft-Dokumentation'
description: 'F #-Techniken, testen und Debuggen'
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 25679331f1bed9f98b86c6eb20f511c891bac1af
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183487"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="ab886-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="ab886-103">Testing and Debugging</span></span>

<span data-ttu-id="ab886-104">Wie bei der klassischen Programmierung ist es von entscheidender Bedeutung, zu überprüfen, ob Quantum-Programme erwartungsgemäß agieren, und ein ungültiges Quantum-Programm diagnostizieren zu können.</span><span class="sxs-lookup"><span data-stu-id="ab886-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="ab886-105">In diesem Abschnitt werden die Tools beschrieben, die von Q # zum Testen und Debuggen von Quantum-Programmen angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="ab886-106">Komponenten Tests</span><span class="sxs-lookup"><span data-stu-id="ab886-106">Unit Tests</span></span>

<span data-ttu-id="ab886-107">Ein gängiger Ansatz zum Testen klassischer Programme ist das Schreiben von kleinen Programmen namens Komponenten *Tests* , die Code in einer Bibliothek ausführen und die Ausgabe mit einer erwarteten Ausgabe vergleichen.</span><span class="sxs-lookup"><span data-stu-id="ab886-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="ab886-108">Beispielsweise möchten wir möglicherweise sicherstellen, dass `Square(2)` `4`zurückgibt, da wir *ein* -Wert von "$ 2 ^ 2 = $4" kennen.</span><span class="sxs-lookup"><span data-stu-id="ab886-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="ab886-109">Q # unterstützt das Erstellen von Komponententests für Quantum-Programme und kann als Tests innerhalb des [xUnit](https://xunit.github.io/) -Komponenten Test-Frameworks ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="ab886-110">Erstellen eines Test Projekts</span><span class="sxs-lookup"><span data-stu-id="ab886-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="ab886-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab886-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ab886-112">Öffnen Sie Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="ab886-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="ab886-113">Wechseln Sie zum Menü `File`, und wählen Sie `New` > `Project...`aus.</span><span class="sxs-lookup"><span data-stu-id="ab886-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="ab886-114">Wählen Sie im Projektvorlagen-Explorer unter `Installed` > `Visual C#`die `Q# Test Project` Vorlage aus.</span><span class="sxs-lookup"><span data-stu-id="ab886-114">In the project template explorer, under `Installed` > `Visual C#`, select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="ab886-115">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab886-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ab886-116">Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ab886-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="ab886-117">In beiden Fällen werden für das neue Projekt zwei Dateien geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ab886-117">In either case, your new project will have two files open.</span></span>
<span data-ttu-id="ab886-118">Die erste Datei, `Tests.qs`, bietet einen geeigneten Ort zum Definieren neuer Q #-Komponententests.</span><span class="sxs-lookup"><span data-stu-id="ab886-118">The first file, `Tests.qs`, provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="ab886-119">Diese Datei enthält anfänglich einen Beispiel-Komponenten Test `AllocateQubitTest` der überprüft, ob sich ein neu zugewiesenes Qubit im $ \ket{0}$ State befindet und eine Meldung ausgibt:</span><span class="sxs-lookup"><span data-stu-id="ab886-119">Initially this file contains one sample unit test `AllocateQubitTest` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    operation AllocateQubitTest () : Unit {
        using (q = Qubit()) {
            Assert([PauliZ], [q], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="ab886-120">Jeder Q #-Vorgang, der mit dem Typ `(Unit => Unit)` oder mit `(Unit -> Unit)` kompatiblen Funktion kompatibel ist, kann als Komponenten Test ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-120">Any Q# operation compatible with the type `(Unit => Unit)` or function compatible with `(Unit -> Unit)` can be executed as a unit test.</span></span> 

<span data-ttu-id="ab886-121">Die zweite Datei, `TestSuiteRunner.cs` enthält eine Methode, die Q #-Komponententests ermittelt und ausführt.</span><span class="sxs-lookup"><span data-stu-id="ab886-121">The second file, `TestSuiteRunner.cs` contains a method that discovers and runs Q# unit tests.</span></span> <span data-ttu-id="ab886-122">Dies ist die Methode, `TestTarget` mit `OperationDriver` Attribut kommentiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-122">This is the method `TestTarget` annotated with `OperationDriver` attribute.</span></span>
<span data-ttu-id="ab886-123">Das `OperationDriver`-Attribut ist ein Teil der xUnit-Erweiterungs Bibliothek Microsoft. Quantum. Simulation. xUnit.</span><span class="sxs-lookup"><span data-stu-id="ab886-123">The `OperationDriver` attribute is a part of the Xunit extension library Microsoft.Quantum.Simulation.Xunit.</span></span>
<span data-ttu-id="ab886-124">Das Komponenten Test-Framework ruft `TestTarget` Methode für jeden erkannten Q #-Komponenten Test auf.</span><span class="sxs-lookup"><span data-stu-id="ab886-124">The unit testing framework calls `TestTarget` method for every Q# unit test it has discovered.</span></span>
<span data-ttu-id="ab886-125">Das Framework übergibt die Komponenten Testbeschreibung über `op` Argument an die-Methode.</span><span class="sxs-lookup"><span data-stu-id="ab886-125">The framework passes the unit test description to the method through `op` argument.</span></span> <span data-ttu-id="ab886-126">Die folgende Codezeile:</span><span class="sxs-lookup"><span data-stu-id="ab886-126">The following line of code:</span></span>
```csharp
op.TestOperationRunner(sim);
```
<span data-ttu-id="ab886-127">führt den Komponenten Test auf `QuantumSimulator`aus.</span><span class="sxs-lookup"><span data-stu-id="ab886-127">executes the unit test on `QuantumSimulator`.</span></span>

<span data-ttu-id="ab886-128">Standardmäßig sucht der Mechanismus für die Komponenten Test Ermittlung nach allen Q #-Funktionen oder-Vorgängen mit kompatiblem Typ, die die folgenden Eigenschaften erfüllen:</span><span class="sxs-lookup"><span data-stu-id="ab886-128">By default, the unit test discovery mechanism looks for all Q# functions or operations of compatible type that satisfy the following properties:</span></span>
* <span data-ttu-id="ab886-129">Befindet sich in der gleichen Assembly wie die Methode, die mit dem `OperationDriver`-Attribut kommentiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-129">Located in the same assembly as the method annotated with the `OperationDriver` attribute.</span></span>
* <span data-ttu-id="ab886-130">Befindet sich im gleichen Namespace wie die Methode, die mit dem `OperationDriver`-Attribut kommentiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-130">Located in the same namespace as the method annotated with the `OperationDriver` attribute.</span></span>
* <span data-ttu-id="ab886-131">Hat einen Namen, der mit `Test`endet.</span><span class="sxs-lookup"><span data-stu-id="ab886-131">Has a name ending with `Test`.</span></span>

<span data-ttu-id="ab886-132">Eine Assembly, ein Namespace und ein Suffix für Komponenten Testfunktionen und-Vorgänge können mithilfe optionaler Parameter des `OperationDriver` Attributs festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="ab886-132">An assembly, a namespace, and a suffix for unit test functions and operations can be set using optional parameters of the `OperationDriver` attribute:</span></span>
* <span data-ttu-id="ab886-133">`AssemblyName` Parameter legt den Namen der Assembly fest, die nach Tests durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-133">`AssemblyName` parameter sets the name of the assembly which is being searched for tests.</span></span>
* <span data-ttu-id="ab886-134">`TestNamespace` Parameter legt den Namen des Namespace fest, der nach Tests durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-134">`TestNamespace` parameter sets the name of the namespace which is being searched for tests.</span></span>
* <span data-ttu-id="ab886-135">`Suffix` legt das Suffix von Vorgangs-oder Funktionsnamen fest, die als Unittests betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-135">`Suffix` sets the suffix of operation or function names that are considered to be unit tests.</span></span>

<span data-ttu-id="ab886-136">Außerdem können Sie mit dem `TestCasePrefix` optionalen-Parameter ein Präfix für den Namen des Testfalls festlegen.</span><span class="sxs-lookup"><span data-stu-id="ab886-136">In addition, the `TestCasePrefix` optional parameter lets you set a prefix for the name of the test case.</span></span> <span data-ttu-id="ab886-137">Das Präfix vor dem Vorgangs Namen wird in der Liste der Testfälle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab886-137">The prefix in front of the operation name will appear in the list of test cases.</span></span> <span data-ttu-id="ab886-138">Beispielsweise führt `TestCasePrefix = "QSim:"` dazu, dass `AllocateQubitTest` in der Liste der gefundenen Tests als `QSim:AllocateQubitTest` angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-138">For example, `TestCasePrefix = "QSim:"` will cause `AllocateQubitTest` to appear as `QSim:AllocateQubitTest` in the list of found tests.</span></span> <span data-ttu-id="ab886-139">Dies kann beispielsweise hilfreich sein, um anzugeben, welcher Simulator zum Ausführen eines Tests verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-139">This can be useful to indicate, for instance, which simulator is used to run a test.</span></span>

### <a name="running-q-unit-tests"></a><span data-ttu-id="ab886-140">Ausführen von f #-Komponenten Tests</span><span class="sxs-lookup"><span data-stu-id="ab886-140">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="ab886-141">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab886-141">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ab886-142">Wechseln Sie als einmalige Einrichtung pro Lösung zu `Test` Menü, und wählen Sie `Test Settings` > `Default Processor Architecture` > `X64`aus.</span><span class="sxs-lookup"><span data-stu-id="ab886-142">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="ab886-143">Die Standardeinstellung für die Prozessorarchitektur für Visual Studio wird in der Projektmappen-Optionsdatei (`.suo`) für jede Lösung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ab886-143">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="ab886-144">Wenn Sie diese Datei löschen, müssen Sie `X64` als Prozessorarchitektur erneut auswählen.</span><span class="sxs-lookup"><span data-stu-id="ab886-144">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="ab886-145">Erstellen Sie das Projekt, wechseln Sie zum Menü `Test`, und wählen Sie `Windows` > `Test Explorer`aus.</span><span class="sxs-lookup"><span data-stu-id="ab886-145">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="ab886-146">`AllocateQubitTest` wird in der Liste der Tests in der `Not Run Tests` Gruppe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab886-146">`AllocateQubitTest` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="ab886-147">Wählen Sie `Run All` aus, oder führen Sie den einzelnen Test aus, und es sollte bestanden werden!</span><span class="sxs-lookup"><span data-stu-id="ab886-147">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="ab886-148">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab886-148">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ab886-149">Navigieren Sie zum Ausführen von Tests zum Projektordner (dem Ordner, der `Tests.csproj`enthält), und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="ab886-149">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="ab886-150">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="ab886-150">You should get output similar to the following:</span></span>

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

***

## <a name="logging-and-assertions"></a><span data-ttu-id="ab886-151">Protokollierung und Assertionen</span><span class="sxs-lookup"><span data-stu-id="ab886-151">Logging and Assertions</span></span>

<span data-ttu-id="ab886-152">Eine wichtige Folge der Tatsache, dass Funktionen in Q # keine Nebeneffekte haben, besteht darin, dass alle Auswirkungen der Ausführung einer Funktion, deren Ausgabetyp das leere Tupel ist `()` nicht innerhalb eines Q #-Programms beobachtet werden können.</span><span class="sxs-lookup"><span data-stu-id="ab886-152">One important consequence of the fact that functions in Q# have no side effects is that any effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="ab886-153">Das heißt, ein Zielcomputer kann keine Funktion ausführen, die `()` zurückgibt, wobei sichergestellt wird, dass diese Auslassung das Verhalten eines nachfolgenden f #-Codes nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="ab886-153">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="ab886-154">Dadurch werden Funktionen `()` ein nützliches Tool zum Einbetten von Assertionen und zum Debuggen von Logik in Q #-Programme.</span><span class="sxs-lookup"><span data-stu-id="ab886-154">This makes functions returning `()` a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

### <a name="logging"></a><span data-ttu-id="ab886-155">Protokollierung</span><span class="sxs-lookup"><span data-stu-id="ab886-155">Logging</span></span>

<span data-ttu-id="ab886-156">Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> hat den Typ `(String -> Unit)` und ermöglicht die Erstellung von Diagnose Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ab886-156">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

<span data-ttu-id="ab886-157">Die `onLog` Aktion `QuantumSimulator` kann verwendet werden, um Aktionen zu definieren, die ausgeführt werden, wenn f #-Code `Message`aufruft.</span><span class="sxs-lookup"><span data-stu-id="ab886-157">The `onLog` action of `QuantumSimulator` can be used to define actions performed when Q# code calls `Message`.</span></span> <span data-ttu-id="ab886-158">Standardmäßig werden protokollierte Nachrichten in der Standardausgabe ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab886-158">By default logged messages are printed to standard output.</span></span>

<span data-ttu-id="ab886-159">Beim Definieren einer Komponenten Test Sammlung können die protokollierten Nachrichten an die Test Ausgabe weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-159">When defining a unit test suite, the logged messages can be directed to the test output.</span></span> <span data-ttu-id="ab886-160">Wenn ein Projekt aus einer f #-Test Projektvorlage erstellt wird, wird diese Umleitung für die Suite vorkonfiguriert und wie folgt standardmäßig erstellt:</span><span class="sxs-lookup"><span data-stu-id="ab886-160">When a project is created from Q# Test Project template, this redirection is pre-configured for the suite and created by default as follows:</span></span>

```qsharp
using (var sim = new QuantumSimulator())
{
    // OnLog defines action(s) performed when Q# test calls operation Message
    sim.OnLog += (msg) => { output.WriteLine(msg); };
    op.TestOperationRunner(sim);
}
```

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="ab886-161">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab886-161">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="ab886-162">Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test klicken, wird ein Panel mit Informationen zur Testausführung angezeigt: Status "erfolgreich"/"Fehler", verstrichene Zeit und "Ausgabe".</span><span class="sxs-lookup"><span data-stu-id="ab886-162">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="ab886-163">Wenn Sie auf den Link "Output" klicken, wird die Test Ausgabe in einem neuen Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ab886-163">If you click the "Output" link, test output will open in a new window.</span></span>

![Test Ausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="ab886-165">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab886-165">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="ab886-166">Der Status "erfolgreich/fehlgeschlagen" für jeden Test wird von `dotnet test`in der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="ab886-166">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="ab886-167">Bei fehlgeschlagenen Tests werden die Ausgaben, die als Ergebnis des obigen `output.WriteLine(msg)` Aufrufens protokolliert werden, auch in der Konsole gedruckt, um die Diagnose des Fehlers zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="ab886-167">For failing tests, the outputs logged as a result of the `output.WriteLine(msg)` call above are also printed to the console to help diagnose the failure.</span></span>

***

### <a name="assertions"></a><span data-ttu-id="ab886-168">TeilI</span><span class="sxs-lookup"><span data-stu-id="ab886-168">Assertions</span></span>

<span data-ttu-id="ab886-169">Die gleiche Logik kann auch für die Implementierung von Assertionen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-169">The same logic can be applied to implementing assertions.</span></span> <span data-ttu-id="ab886-170">Betrachten wir ein einfaches Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ab886-170">Let's consider a simple example:</span></span>

```qsharp
function AssertPositive(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="ab886-171">Hier gibt das Schlüsselwort `fail` an, dass die Berechnung nicht fortgesetzt werden soll, wodurch eine Ausnahme auf dem Zielcomputer ausgelöst wird, der das Q #-Programm ausführt.</span><span class="sxs-lookup"><span data-stu-id="ab886-171">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="ab886-172">Definitionsgemäß kann ein Fehler dieser Art nicht innerhalb von q # beobachtet werden, da kein weiterer Q #-Code ausgeführt wird, nachdem eine `fail`-Anweisung erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="ab886-172">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="ab886-173">Wenn wir also einen `AssertPositive`-Aufrufvorgang fortsetzen, können wir sicher sein, dass die Eingabe positiv ist.</span><span class="sxs-lookup"><span data-stu-id="ab886-173">Thus, if we proceed past a call to `AssertPositive`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="ab886-174">Wenn Sie auf diese Ideen aufbauen, bietet [das präspiel](xref:microsoft.quantum.libraries.standard.prelude) zwei besonders nützliche Assertionen, <xref:microsoft.quantum.intrinsic.assert> und <xref:microsoft.quantum.intrinsic.assertprob> beide als Vorgänge auf `()`modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="ab886-174">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="ab886-175">Diese Assertionen akzeptieren jeweils einen Pauli-Operator, der ein bestimmtes Maß an Interesse beschreibt, ein Quantum-Register, für das eine Messung durchgeführt werden soll, und ein hypothetisches Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="ab886-175">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="ab886-176">Auf Ziel Computern, die bei der Simulation funktionieren, werden wir nicht durch [das No-Klon-Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen durchführen, ohne dass das an diese Assertionen weiter gegebene Register gestört wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-176">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="ab886-177">Ein Simulator kann dann, ähnlich wie in der obigen `AssertPositive`-Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beachtet wird:</span><span class="sxs-lookup"><span data-stu-id="ab886-177">A simulator can then, similar to the `AssertPositive` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="ab886-178">Bei physischer Quantum-Hardware, bei der das No-Klon-Theorem die Prüfung des Quantums verhindert, werden die `Assert`-und `AssertProb` Vorgänge einfach `()` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ab886-178">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="ab886-179">Der <xref:microsoft.quantum.diagnostics>-Namespace stellt mehrere weitere Funktionen der `Assert`-Familie bereit, die es uns ermöglichen, erweiterte Bedingungen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ab886-179">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="ab886-180">Dumpfunktionen</span><span class="sxs-lookup"><span data-stu-id="ab886-180">Dump Functions</span></span>

<span data-ttu-id="ab886-181">Zur Unterstützung der Problembehandlung von Quantum-Programmen bietet der <xref:microsoft.quantum.diagnostics>-Namespace zwei Funktionen, mit denen der aktuelle Status des Ziel Computers in einer Datei gespeichert werden kann: <xref:microsoft.quantum.diagnostics.dumpmachine> und <xref:microsoft.quantum.diagnostics.dumpregister>.</span><span class="sxs-lookup"><span data-stu-id="ab886-181">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="ab886-182">Die generierte Ausgabe hängt von dem Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="ab886-182">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="ab886-183">Dumpmachine</span><span class="sxs-lookup"><span data-stu-id="ab886-183">DumpMachine</span></span>

<span data-ttu-id="ab886-184">Der als Teil des Quantum Development Kit verteilte Volltext-Quantum-Simulator schreibt die [Wellenfunktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantum-Systems als eindimensionales Array komplexer Zahlen in die Datei, in der jedes Element die Amplitude der Wahrscheinlichkeit für die Messung des Berechnungsbasis Zustands $ \ket{n} $, wobei $ \ket{n} = \ket{b_{n-1}... b_1b_0} $ für Bits $\{b_i\}$.</span><span class="sxs-lookup"><span data-stu-id="ab886-184">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="ab886-185">Beispielsweise auf einem Computer, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\bruchteil {(1 + i)}{2} \ket{10}, \end{align} $ $ Call <xref:microsoft.quantum.diagnostics.dumpmachine> generiert diese Ausgabe. :</span><span class="sxs-lookup"><span data-stu-id="ab886-185">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="ab886-186">Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="ab886-186">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="ab886-187">In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{n} $ im kartesischen und Polar Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ab886-187">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="ab886-188">Im Detail für die erste Zeile:</span><span class="sxs-lookup"><span data-stu-id="ab886-188">In detail for the first row:</span></span>

* <span data-ttu-id="ab886-189">**`∣0❭:`** diese Zeile dem Status der `0` Berechnungsbasis entspricht.</span><span class="sxs-lookup"><span data-stu-id="ab886-189">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="ab886-190">**`0.707107 +  0.000000 i`** : die Wahrscheinlichkeits Amplitude im kartesischen Format.</span><span class="sxs-lookup"><span data-stu-id="ab886-190">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="ab886-191">**` == `** : das `equal` Vorzeichen trennt beide äquivalente Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="ab886-191">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="ab886-192">**`**********  `** : eine grafische Darstellung der Größe, die Anzahl der `*` proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.</span><span class="sxs-lookup"><span data-stu-id="ab886-192">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="ab886-193">**`[ 0.500000 ]`** : der numerische Wert der Größe.</span><span class="sxs-lookup"><span data-stu-id="ab886-193">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="ab886-194">**`    ---`** : eine grafische Darstellung der Amplitude-Phase (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="ab886-194">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="ab886-195">**`[ 0.0000 rad ]`** : der numerische Wert der Phase (im Bogenmaße).</span><span class="sxs-lookup"><span data-stu-id="ab886-195">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="ab886-196">Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ab886-196">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="ab886-197">Die Größen Darstellung ist geradlinig: Sie zeigt einen Balken `*`an, je größer die Wahrscheinlichkeit, mit der die Leiste größer wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-197">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="ab886-198">In der Phase zeigen wir die folgenden Symbole zur Darstellung des Winkels basierend auf Bereichen:</span><span class="sxs-lookup"><span data-stu-id="ab886-198">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="ab886-199">In den folgenden Beispielen werden `DumpMachine` für einige gängige Zustände veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="ab886-199">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="ab886-200">Die ID eines Qubit wird zur Laufzeit zugewiesen und ist nicht notwendigerweise an die Reihenfolge ausgerichtet, in der das Qubit zugeordnet wurde, oder an seine Position in einem Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="ab886-200">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="ab886-201">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="ab886-201">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="ab886-202">Sie können eine Qubit-ID in Visual Studio ermitteln, indem Sie einen Haltepunkt in Ihrem Code platzieren und den Wert einer Qubit-Variablen untersuchen, z. b.:</span><span class="sxs-lookup"><span data-stu-id="ab886-202">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Anzeigen der Qubit-ID in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="ab886-204">Das Qubit mit Index `0` auf `register2` hat ID =`3`, das Qubit mit Index `1` hat ID =`2`.</span><span class="sxs-lookup"><span data-stu-id="ab886-204">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="ab886-205">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ab886-205">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="ab886-206">Sie können eine Qubit-ID ermitteln, indem Sie die <xref:microsoft.quantum.intrinsic.message>-Funktion verwenden und die Qubit-Variable in der Nachricht übergeben, z. b.:</span><span class="sxs-lookup"><span data-stu-id="ab886-206">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="ab886-207">Dies könnte folgende Ausgabe generieren:</span><span class="sxs-lookup"><span data-stu-id="ab886-207">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="ab886-208">Dies bedeutet, dass das Qubit mit Index `0` auf `register2` ID =`3`, das Qubit mit Index `1` ID =`2`aufweist.</span><span class="sxs-lookup"><span data-stu-id="ab886-208">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="ab886-209"><xref:microsoft.quantum.diagnostics.dumpmachine> ist Teil des <xref:microsoft.quantum.diagnostics>-Namespace. damit Sie ihn verwenden können, müssen Sie eine `open`-Anweisung hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ab886-209"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="ab886-210">Dumpregiester</span><span class="sxs-lookup"><span data-stu-id="ab886-210">DumpRegister</span></span>

<span data-ttu-id="ab886-211"><xref:microsoft.quantum.diagnostics.dumpregister> funktioniert wie <xref:microsoft.quantum.diagnostics.dumpmachine>, mit dem Unterschied, dass es auch ein Array von Qubits verwendet, um die Menge der Informationen auf die für die entsprechenden Qubits relevanten Informationen einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="ab886-211"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="ab886-212">Wie bei <xref:microsoft.quantum.diagnostics.dumpmachine>hängt die von <xref:microsoft.quantum.diagnostics.dumpregister> generierten Informationen vom Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="ab886-212">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="ab886-213">Für den vollständigen Quantum-Simulator schreibt er in die Datei, die von der Wave-Funktion bis zu einer globalen Phase des von den bereitgestellten Qubits generierten Quantums in demselben Format wie <xref:microsoft.quantum.diagnostics.dumpmachine>generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ab886-213">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="ab886-214">Beispiel: Wiederholen Sie einen Computer, auf dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\bruchteil {(1 + i)}{2} \ket{10} =-e ^ {-i \ pi/4} ((\frac{1}{\sqrt{2}} \ Ket{0}-\bruch{(1 + i)}{2} \ket{1}) \otimes \bruchteil {-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ aufrufen <xref:microsoft.quantum.diagnostics.dumpregister> für `qubit[0]` generiert diese Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="ab886-214">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="ab886-215">Wenn Sie <xref:microsoft.quantum.diagnostics.dumpregister> für `qubit[1]` aufrufen, wird diese Ausgabe generiert:</span><span class="sxs-lookup"><span data-stu-id="ab886-215">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="ab886-216">Im Allgemeinen ist der Status eines Registers, das mit einem anderen Register entkoppelt ist, ein gemischter Zustand und kein reiner Zustand.</span><span class="sxs-lookup"><span data-stu-id="ab886-216">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="ab886-217">In diesem Fall gibt <xref:microsoft.quantum.diagnostics.dumpregister> die folgende Meldung aus:</span><span class="sxs-lookup"><span data-stu-id="ab886-217">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="ab886-218">Im folgenden Beispiel wird gezeigt, wie Sie sowohl <xref:microsoft.quantum.diagnostics.dumpregister> als auch <xref:microsoft.quantum.diagnostics.dumpmachine> in Ihrem Q #-Code verwenden können:</span><span class="sxs-lookup"><span data-stu-id="ab886-218">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="ab886-219">Debuggen</span><span class="sxs-lookup"><span data-stu-id="ab886-219">Debugging</span></span>

<span data-ttu-id="ab886-220">Zusätzlich zu den Funktionen und Vorgängen von `Assert` und `Dump` unterstützt Q # eine Teilmenge der standardmäßigen Visual Studio-Debugfunktionen: [Festlegen von Zeilen Haltepunkten](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), schrittweise [durchlaufen von Code mithilfe von F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) und überprüfen [von Werten klassischer Variablen ](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows)sind während der Codeausführung im Simulator möglich.</span><span class="sxs-lookup"><span data-stu-id="ab886-220">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="ab886-221">Das Debuggen in Visual Studio Code wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab886-221">Debugging in Visual Studio Code is not yet supported.</span></span>

