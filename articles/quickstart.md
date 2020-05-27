---
title: Erkunden der Verschränkung mit Q#
description: Erfahren Sie, wie Sie ein Quantenprogramm in Q# schreiben. Entwickeln Sie eine Bell-Zustandsanwendung mithilfe des Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 10/07/2019
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 7836e39227fa2282c6e2faa039f6e625103d5403
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426840"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="96235-104">Tutorial: Erkunden der Verschränkung mit Q\#</span><span class="sxs-lookup"><span data-stu-id="96235-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="96235-105">In diesem Tutorial erfahren Sie, wie Sie ein Q#-Programm schreiben, mit dem Qubits bearbeitet und gemessen werden können. Darüber hinaus werden die Auswirkungen von Superposition und Verschränkung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="96235-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>
<span data-ttu-id="96235-106">Es wird beschrieben, wie Sie das QDK installieren und das Programm erstellen und mit einem Quantensimulator ausführen.</span><span class="sxs-lookup"><span data-stu-id="96235-106">This guides you on installing the QDK, building the program and executing that program on a quantum simulator.</span></span>  

<span data-ttu-id="96235-107">Sie schreiben eine Anwendung mit dem Namen „Bell“, um die Quantenverschränkung zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="96235-107">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="96235-108">Der Name „Bell“ bezieht sich auf die Bell-Zustände. Hierbei handelt es sich um spezifische Quantenzustände von zwei Qubits, die zum Darstellen der einfachsten Beispiele für Überlagerungen und Quantenverschränkungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="96235-108">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="96235-109">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="96235-109">Pre-requisites</span></span>

<span data-ttu-id="96235-110">Führen Sie zunächst diese Schritte aus, wenn Sie bereit zum Codieren sind:</span><span class="sxs-lookup"><span data-stu-id="96235-110">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="96235-111">[Installieren](xref:microsoft.quantum.install) Sie das Quantum Development Kit in Ihrer bevorzugten Sprache und Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="96235-111">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment</span></span>
* <span data-ttu-id="96235-112">Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde</span><span class="sxs-lookup"><span data-stu-id="96235-112">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="96235-113">Sie können den Vorgang auch ohne Installation des QDK durchführen, indem Sie sich die Übersichten zur Q#-Programmiersprache und die wichtigsten Konzepte des Quantencomputings ansehen.</span><span class="sxs-lookup"><span data-stu-id="96235-113">You can also follow along with the narrative without installing the QDK, reviewing the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="demonstrating-qubit-behavior-with-q"></a><span data-ttu-id="96235-114">Veranschaulichen des Qubit-Verhaltens mit Q#</span><span class="sxs-lookup"><span data-stu-id="96235-114">Demonstrating qubit behavior with Q#</span></span>

<span data-ttu-id="96235-115">Denken Sie an unsere einfache [Qubit-Definition](xref:microsoft.quantum.overview.understanding) zurück.</span><span class="sxs-lookup"><span data-stu-id="96235-115">Recall our simple [definition of a qubit](xref:microsoft.quantum.overview.understanding).</span></span>  <span data-ttu-id="96235-116">Klassische Bits enthalten einen einzelnen binären Wert (0 oder 1). Der Zustand eines Qubits kann dagegen eine **Superposition** sein (also 0 und 1 gleichzeitig).</span><span class="sxs-lookup"><span data-stu-id="96235-116">Where classical bits hold a single binary value such as a 0 or 1, the state of a qubit can be in a **superposition** of 0 and 1 simultaneously.</span></span>  <span data-ttu-id="96235-117">Vom Konzept her können Sie sich ein Qubit als eine Richtung im Raum vorstellen (auch als Vektor bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="96235-117">Conceptually, a qubit can be thought of as a direction in space (also known as a vector).</span></span>  <span data-ttu-id="96235-118">Ein Qubit kann eine beliebige der möglichen Richtungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="96235-118">A qubit can be in any of the possible directions.</span></span> <span data-ttu-id="96235-119">Die beiden **klassischen Zustände** sind die beiden Richtungen, die für die einhundertprozentige Chance einer Messung von 0 und die einhundertprozentige Chance einer Messung von 1 stehen.</span><span class="sxs-lookup"><span data-stu-id="96235-119">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>  <span data-ttu-id="96235-120">Diese Darstellung wird formal durch die [Bloch-Kugel](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) visualisiert.</span><span class="sxs-lookup"><span data-stu-id="96235-120">This representation is also more formally visualized by the [bloch sphere](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>


<span data-ttu-id="96235-121">Mit dem Messvorgang wird ein binäres Ergebnis erzeugt und ein Qubit-Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="96235-121">The act of measurement produces a binary result and changes a qubit state.</span></span> <span data-ttu-id="96235-122">Bei der Messung wird ein binärer Wert erzeugt (0 oder 1).</span><span class="sxs-lookup"><span data-stu-id="96235-122">Measurement produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="96235-123">Das Qubit geht von einem Überlagerungszustand (beliebige Richtung) in einen der klassischen Zustände über.</span><span class="sxs-lookup"><span data-stu-id="96235-123">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="96235-124">Danach führt die Wiederholung der gleichen Messung ohne Eingriff zu demselben binären Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="96235-124">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="96235-125">Mehrere Qubits können **verschränkt** sein.</span><span class="sxs-lookup"><span data-stu-id="96235-125">Multiple qubits can be **entangled**.</span></span> <span data-ttu-id="96235-126">Bei der Messung eines verschränkten Qubits wird unsere Kenntnis des Zustands der anderen Qubits ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="96235-126">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="96235-127">Nun können wir veranschaulichen, wie dieses Verhalten von Q# ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="96235-127">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="96235-128">Sie beginnen mit dem einfachsten möglichen Programm und erweitern es anschließend, um die Quantenüberlagerung und -verschränkung zu demonstrieren.</span><span class="sxs-lookup"><span data-stu-id="96235-128">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="setup"></a><span data-ttu-id="96235-129">Einrichten</span><span class="sxs-lookup"><span data-stu-id="96235-129">Setup</span></span>

<span data-ttu-id="96235-130">Anwendungen, die mit dem Quantum Development Kit von Microsoft entwickelt wurden, bestehen aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="96235-130">Applications developed with Microsoft's Quantum Development Kit consist of two parts:</span></span>

1. <span data-ttu-id="96235-131">Einem oder mehreren Quantenalgorithmen, die mithilfe der Quantenprogrammiersprache Q# implementiert wurden.</span><span class="sxs-lookup"><span data-stu-id="96235-131">One or more quantum algorithms, implemented using the Q# quantum programming language.</span></span>
1. <span data-ttu-id="96235-132">Einem Hostprogramm, das in einer Programmiersprache wie Python oder C# implementiert wurde, das als Haupteinstiegspunkt dient und Q#-Vorgänge aufruft, um einen Quantenalgorithmus auszuführen.</span><span class="sxs-lookup"><span data-stu-id="96235-132">A host program, implemented in a programming language like Python or C# that serves as the main entry point and invokes Q# operations to execute a quantum algorithm.</span></span>

#### <a name="python"></a>[<span data-ttu-id="96235-133">Python</span><span class="sxs-lookup"><span data-stu-id="96235-133">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="96235-134">Wählen Sie einen Speicherort für Ihre Anwendung aus</span><span class="sxs-lookup"><span data-stu-id="96235-134">Choose a location for your application</span></span>

1. <span data-ttu-id="96235-135">Erstellen Sie eine Datei namens `Bell.qs`.</span><span class="sxs-lookup"><span data-stu-id="96235-135">Create a file called `Bell.qs`.</span></span> <span data-ttu-id="96235-136">Diese Datei enthält Ihren Q #-Code.</span><span class="sxs-lookup"><span data-stu-id="96235-136">This file will contain your Q# code.</span></span>

1. <span data-ttu-id="96235-137">Erstellen Sie eine Datei namens `host.py`.</span><span class="sxs-lookup"><span data-stu-id="96235-137">Create a file called `host.py`.</span></span> <span data-ttu-id="96235-138">Diese Datei enthält Ihren Python-Hostcode.</span><span class="sxs-lookup"><span data-stu-id="96235-138">This file will contain your Python host code.</span></span>

#### <a name="c-command-line"></a>[<span data-ttu-id="96235-139">C#-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="96235-139">C# Command Line</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="96235-140">Erstellen Sie ein neues Q#-Projekt:</span><span class="sxs-lookup"><span data-stu-id="96235-140">Create a new Q# project:</span></span>

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    <span data-ttu-id="96235-141">Sie sollten eine `.csproj`-Datei, eine Q#-Datei mit dem Namen `Operations.qs` und eine Hostprogrammdatei mit dem Namen `Driver.cs` sehen.</span><span class="sxs-lookup"><span data-stu-id="96235-141">You should see a `.csproj` file, a Q# file called `Operations.qs`, and a host program file called `Driver.cs`</span></span>

1. <span data-ttu-id="96235-142">Benennen Sie die Q#-Datei um.</span><span class="sxs-lookup"><span data-stu-id="96235-142">Rename the Q# file</span></span>

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[<span data-ttu-id="96235-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96235-143">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="96235-144">Erstellen eines neuen Projekts</span><span class="sxs-lookup"><span data-stu-id="96235-144">Create a new project</span></span>

   * <span data-ttu-id="96235-145">Öffnen Sie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="96235-145">Open Visual Studio</span></span>
   * <span data-ttu-id="96235-146">Navigieren Sie zum Menü **Datei**, und wählen Sie **Neu** -> **Projekt...** aus.</span><span class="sxs-lookup"><span data-stu-id="96235-146">Go to the **File** menu and select **New** -> **Project...**</span></span>
   * <span data-ttu-id="96235-147">Geben Sie im Projektvorlagen-Explorer `Q#` in das Suchfeld ein, und wählen Sie die Vorlage `Q# Application` aus.</span><span class="sxs-lookup"><span data-stu-id="96235-147">In the project template explorer, type `Q#` into the search field and select the `Q# Application` template</span></span>
   * <span data-ttu-id="96235-148">Geben Sie dem Projekt den Namen `Bell`.</span><span class="sxs-lookup"><span data-stu-id="96235-148">Give your project the name `Bell`</span></span>

1. <span data-ttu-id="96235-149">Benennen Sie die Q#-Datei um.</span><span class="sxs-lookup"><span data-stu-id="96235-149">Rename the Q# file</span></span>

   * <span data-ttu-id="96235-150">Navigieren Sie zum **Projektmappen-Explorer**</span><span class="sxs-lookup"><span data-stu-id="96235-150">Navigate to the **Solution Explorer**</span></span>
   * <span data-ttu-id="96235-151">Klicken Sie mit der rechten Maustaste auf die `Operations.qs`-Datei.</span><span class="sxs-lookup"><span data-stu-id="96235-151">Right click on the `Operations.qs` file</span></span>
   * <span data-ttu-id="96235-152">Benennen Sie sie in `Bell.qs` um.</span><span class="sxs-lookup"><span data-stu-id="96235-152">Rename it to `Bell.qs`</span></span>

* * *

## <a name="write-a-q-operation"></a><span data-ttu-id="96235-153">Schreiben einer Q#-Operation</span><span class="sxs-lookup"><span data-stu-id="96235-153">Write a Q# operation</span></span>

<span data-ttu-id="96235-154">Unser Ziel ist die Festlegung eines spezifischen Quantenzustands für zwei Qubits. Hiermit soll demonstriert werden, wie Sie mit Q# bei Qubits vorgehen, um den Zustand zu ändern und die Auswirkungen von Überlagerung und Verschränkung zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="96235-154">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="96235-155">Wir bauen dies Stück für Stück auf, um Zustände, Vorgänge und Messungen von Qubits zu demonstrieren.</span><span class="sxs-lookup"><span data-stu-id="96235-155">We will build this up piece by piece to demonstrate qubit states, operations, and measurement.</span></span>

<span data-ttu-id="96235-156">**Übersicht:**  Im ersten unten aufgeführten Code wird gezeigt, wie Sie in Q# mit Qubits arbeiten.</span><span class="sxs-lookup"><span data-stu-id="96235-156">**Overview:**  In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="96235-157">Wir verwenden die beiden Vorgänge `M` und `X`, um den Zustand eines Qubits zu transformieren.</span><span class="sxs-lookup"><span data-stu-id="96235-157">We’ll introduce two operations, `M` and `X` that transform the state of a qubit.</span></span> 

<span data-ttu-id="96235-158">In diesem Codeausschnitt wird der Vorgang `Set` definiert, für den als Parameter ein Qubit verwendet wird, sowie ein weiterer Parameter `desired`, mit dem der gewünschte Zustand für das Qubit dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="96235-158">In this code snippet, an operation `Set` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="96235-159">Der Vorgang `Set` führt eine Messung für das Qubit durch, indem der Vorgang `M` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="96235-159">The operation `Set` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="96235-160">In Q# wird für eine Qubit-Messung immer entweder `Zero` oder `One` zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96235-160">In Q#, a qubit measurement always returns either  `Zero` or `One`.</span></span>  <span data-ttu-id="96235-161">Wenn die Messung einen Wert zurückgibt, der nicht einem gewünschten Wert entspricht, wird das Qubit von „Set“ umgekehrt. Der Vorgang `X` wird ausgeführt, mit dem der Qubit-Zustand in einen neuen Zustand geändert wird, bei dem die Wahrscheinlichkeiten, dass für eine Messung `Zero` und `One` zurückgegeben wird, umgekehrt sind.</span><span class="sxs-lookup"><span data-stu-id="96235-161">If the measurement returns a value not equal to a desired value, Set “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span>  <span data-ttu-id="96235-162">Zur Veranschaulichung der Auswirkungen des Vorgangs `Set` wird dann der Vorgang `TestBellState` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="96235-162">To demonstrate the effect of the `Set` operation, a `TestBellState` operation is then added.</span></span>  <span data-ttu-id="96235-163">Für diesen Vorgang wird `Zero` oder `One` als Eingabe verwendet, und der Vorgang `Set` wird einige Male mit dieser Eingabe aufgerufen. Es wird gezählt, wie oft bei der Messung des Qubits `Zero` und wie oft `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96235-163">This operation takes as input a `Zero` or `One`, and calls the `Set` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="96235-164">Bei der ersten Simulation des Vorgangs `TestBellState` erwarten wir natürlich, dass in der Ausgabe für alle Messungen des Qubits mit `Zero` als Parametereingabe `Zero` und für alle Messungen eines Qubits mit `One` als Parametereingabe `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96235-164">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span>  <span data-ttu-id="96235-165">Später fügen wir `TestBellState` Code hinzu, um die Überlagerung und Verschränkung zu demonstrieren.</span><span class="sxs-lookup"><span data-stu-id="96235-165">Further on, we’ll add code to `TestBellState` to demonstrating superposition and entanglement.</span></span>


### <a name="q-operation-code"></a><span data-ttu-id="96235-166">Q#-Operationscode</span><span class="sxs-lookup"><span data-stu-id="96235-166">Q# operation code</span></span>

1. <span data-ttu-id="96235-167">Ersetzen Sie den Inhalt der Datei „Bell.qs“ durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="96235-167">Replace the contents of the Bell.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    <span data-ttu-id="96235-168">Dieser Vorgang kann jetzt aufgerufen werden, um ein Qubit auf einen klassischen Zustand festzulegen, indem entweder immer `Zero` oder immer `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96235-168">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>  <span data-ttu-id="96235-169">`Zero` und `One` sind Konstanten, die die beiden einzigen möglichen Ergebnisse der Messung eines Qubits darstellen.</span><span class="sxs-lookup"><span data-stu-id="96235-169">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

    <span data-ttu-id="96235-170">Mit dem Vorgang `Set` wird das Qubit gemessen.</span><span class="sxs-lookup"><span data-stu-id="96235-170">The operation `Set` measures the qubit.</span></span>
    <span data-ttu-id="96235-171">Falls sich das Qubit im gewünschten Zustand befindet, wird es von `Set` unverändert gelassen. Andernfalls ändern wir den Qubit-Zustand in den gewünschten Zustand, indem wir den Vorgang `X` ausführen.</span><span class="sxs-lookup"><span data-stu-id="96235-171">If the qubit is in the state we want, `Set` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

### <a name="about-q-operations"></a><span data-ttu-id="96235-172">Informationen zu Q#-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="96235-172">About Q# operations</span></span>

<span data-ttu-id="96235-173">Ein Q#-Vorgang ist eine Quantenunterroutine.</span><span class="sxs-lookup"><span data-stu-id="96235-173">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="96235-174">Dies bedeutet, dass es sich um eine aufrufbare Routine handelt, die Quantenvorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="96235-174">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="96235-175">Die Argumente für eine Operation werden als Tupel angegeben, in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="96235-175">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="96235-176">Der Rückgabetyp der Operation wird nach einem Doppelpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="96235-176">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="96235-177">In diesem Fall hat die Operation `Set` keinen Rückgabewert, daher ist sie als `Unit` zurückgebend markiert.</span><span class="sxs-lookup"><span data-stu-id="96235-177">In this case, the `Set` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="96235-178">Dies ist die Q#-Entsprechung von `unit` in F#, das in etwa analog zu `void` in C# und einem leeren Tupel (`Tuple[()]`) in Python ist.</span><span class="sxs-lookup"><span data-stu-id="96235-178">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="96235-179">Sie haben in Ihrem ersten Q#-Vorgang zwei Quantenvorgänge verwendet:</span><span class="sxs-lookup"><span data-stu-id="96235-179">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="96235-180">Den Vorgang [M](xref:microsoft.quantum.intrinsic.m), mit dem der Zustand des Qubits gemessen wird</span><span class="sxs-lookup"><span data-stu-id="96235-180">The [M](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="96235-181">Den Vorgang [X](xref:microsoft.quantum.intrinsic.x), mit dem der Zustand eines Qubits umgekehrt wird</span><span class="sxs-lookup"><span data-stu-id="96235-181">The [X](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="96235-182">Mit einem Quantenvorgang wird der Zustand eines Qubits transformiert.</span><span class="sxs-lookup"><span data-stu-id="96235-182">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="96235-183">Analog zu klassischen Logikgattern wird anstelle von Vorgängen auch von Quantengattern gesprochen.</span><span class="sxs-lookup"><span data-stu-id="96235-183">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="96235-184">Diese Bezeichnung stammt aus den Anfängen des Quantencomputings, als Algorithmen lediglich ein theoretisches Konstrukt waren und in Form von Diagrammen visualisiert wurden – ähnlich wie bei einem Schaltplan im Bereich des klassischen Computings.</span><span class="sxs-lookup"><span data-stu-id="96235-184">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="add-q-test-code"></a><span data-ttu-id="96235-185">Hinzufügen von Q#-Testcode</span><span class="sxs-lookup"><span data-stu-id="96235-185">Add Q# test code</span></span>

1. <span data-ttu-id="96235-186">Fügen Sie der `Bell.qs`-Datei die folgende Operation hinzu, innerhalb des Namespaces, nach dem Ende der `Set`-Operation:</span><span class="sxs-lookup"><span data-stu-id="96235-186">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `Set` operation:</span></span>

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    <span data-ttu-id="96235-187">Diese Operation (`TestBellState`) iteriert `count` Iterationen lang in einer Schleife, legt einen angegebenen `initial`-Wert für ein Qubit fest, und misst (`M`) dann das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="96235-187">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="96235-188">Sie führt eine Statistik zur Anzahl der gemessenen Nullen und Einsen und gibt diese an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="96235-188">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="96235-189">Sie führt eine weitere erforderliche Operation aus.</span><span class="sxs-lookup"><span data-stu-id="96235-189">It performs one other necessary operation.</span></span> <span data-ttu-id="96235-190">Sie setzt das Qubit auf einen bekannten Zustand (`Zero`) zurück, bevor sie es zurückgibt, was es anderen ermöglicht, dieses Qubit in einem bekannten Zustand zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="96235-190">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="96235-191">Dies ist aufgrund der `using`-Anweisung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="96235-191">This is required by the `using` statement.</span></span>

### <a name="about-variables-in-q"></a><span data-ttu-id="96235-192">Informationen zu Variablen in Q#</span><span class="sxs-lookup"><span data-stu-id="96235-192">About variables in Q#</span></span>

<span data-ttu-id="96235-193">Standardmäßig sind Variablen in Q# unveränderlich; ihr Wert kann nach der Bindung nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="96235-193">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="96235-194">Das `let`-Schlüsselwort wird verwendet, um die Bindung einer unveränderlichen Variable anzugeben.</span><span class="sxs-lookup"><span data-stu-id="96235-194">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="96235-195">Operationsargumente sind immer unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="96235-195">Operation arguments are always immutable.</span></span>

<span data-ttu-id="96235-196">Wenn Sie eine Variable benötigen, deren Wert geändert werden kann, wie etwa `numOnes` im Beispiel, können Sie die Variable mit dem Schlüsselwort `mutable` deklarieren.</span><span class="sxs-lookup"><span data-stu-id="96235-196">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="96235-197">Der Wert einer veränderlichen Variable kann mithilfe einer `set`-Anweisung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="96235-197">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="96235-198">In beiden Fällen wird der Typ einer Variablen vom Compiler abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="96235-198">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="96235-199">Q# erfordert keine Typanmerkungen für Variablen.</span><span class="sxs-lookup"><span data-stu-id="96235-199">Q# doesn't require any type annotations for variables.</span></span>

### <a name="about-using-statements-in-q"></a><span data-ttu-id="96235-200">Informationen zu `using`-Anweisungen in Q#</span><span class="sxs-lookup"><span data-stu-id="96235-200">About `using` statements in Q#</span></span>

<span data-ttu-id="96235-201">Die `using`-Anweisung ist eine weitere Besonderheit in Q#.</span><span class="sxs-lookup"><span data-stu-id="96235-201">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="96235-202">Sie wird verwendet, um Qubits für die Verwendung in einem Codeblock zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="96235-202">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="96235-203">In Q# werden alle Qubits dynamisch zugewiesen und freigegeben, sie stellen also keine festen Ressourcen dar, die für die gesamte Lebensdauer eines komplexen Algorithmus vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="96235-203">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="96235-204">Eine `using`-Anweisung weist eine Reihe Qubits am Anfang zu und gibt diese Qubits am Ende des Blocks wieder frei.</span><span class="sxs-lookup"><span data-stu-id="96235-204">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="create-the-host-application-code"></a><span data-ttu-id="96235-205">Erstellen des Hostanwendungscodes</span><span class="sxs-lookup"><span data-stu-id="96235-205">Create the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="96235-206">Python</span><span class="sxs-lookup"><span data-stu-id="96235-206">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="96235-207">Öffnen Sie die Datei `host.py`, und fügen Sie den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="96235-207">Open the `host.py` file and add the following code:</span></span>

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[<span data-ttu-id="96235-208">C#</span><span class="sxs-lookup"><span data-stu-id="96235-208">C#</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="96235-209">Ersetzen Sie den Inhalt der Datei `Driver.cs` durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="96235-209">Replace the contents of the `Driver.cs` file with the following code:</span></span>

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a><span data-ttu-id="96235-210">Informationen zum Hostanwendungscode</span><span class="sxs-lookup"><span data-stu-id="96235-210">About the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="96235-211">Python</span><span class="sxs-lookup"><span data-stu-id="96235-211">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="96235-212">Die Python-Hostanwendung weist drei Teile auf:</span><span class="sxs-lookup"><span data-stu-id="96235-212">The Python host application has three parts:</span></span>

* <span data-ttu-id="96235-213">Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="96235-213">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="96235-214">Im Beispiel ist `count` auf 1000 festgelegt, und `initial` ist der Anfangswert des Qubits.</span><span class="sxs-lookup"><span data-stu-id="96235-214">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="96235-215">Ausführen des Quantenalgorithmus durch Aufrufen der `simulate()`-Methode der importierten Q#-Operation.</span><span class="sxs-lookup"><span data-stu-id="96235-215">Run the quantum algorithm by calling the `simulate()` method of the imported Q# operation.</span></span>
* <span data-ttu-id="96235-216">Verarbeiten des Ergebnisses der Operation.</span><span class="sxs-lookup"><span data-stu-id="96235-216">Process the result of the operation.</span></span> <span data-ttu-id="96235-217">Im Beispiel empfängt `res` das Ergebnis der Operation.</span><span class="sxs-lookup"><span data-stu-id="96235-217">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="96235-218">Hier ist das Ergebnis ein Tupel der Anzahl von Nullen (`num_zeros`) und der Anzahl von Einsen (`num_ones`), die vom Simulator gemessen wurden.</span><span class="sxs-lookup"><span data-stu-id="96235-218">Here the result is a tuple of the number of zeros (`num_zeros`) and number of ones (`num_ones`) measured by the simulator.</span></span> <span data-ttu-id="96235-219">Wir dekonstruieren das Tupel, um die zwei Felder zu erhalten, und geben die Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="96235-219">We deconstruct the tuple to get the two fields, and print the results.</span></span>

#### <a name="c"></a>[<span data-ttu-id="96235-220">C#</span><span class="sxs-lookup"><span data-stu-id="96235-220">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="96235-221">Die C#-Hostanwendung weist vier Teile auf:</span><span class="sxs-lookup"><span data-stu-id="96235-221">The C# host application has four parts:</span></span>

* <span data-ttu-id="96235-222">Konstruieren eines Quantensimulators.</span><span class="sxs-lookup"><span data-stu-id="96235-222">Construct a quantum simulator.</span></span> <span data-ttu-id="96235-223">Im Beispiel ist `qsim` der Simulator.</span><span class="sxs-lookup"><span data-stu-id="96235-223">In the example, `qsim` is the simulator.</span></span>
* <span data-ttu-id="96235-224">Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="96235-224">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="96235-225">Im Beispiel ist `count` auf 1000 festgelegt, und `initial` ist der Anfangswert des Qubits.</span><span class="sxs-lookup"><span data-stu-id="96235-225">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="96235-226">Ausführen des Quantenalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="96235-226">Run the quantum algorithm.</span></span> <span data-ttu-id="96235-227">Jede Q#-Operation generiert eine C#-Klasse gleichen Namens.</span><span class="sxs-lookup"><span data-stu-id="96235-227">Each Q# operation generates a C# class with the same name.</span></span> <span data-ttu-id="96235-228">Diese Klasse weist eine `Run`-Methode auf, die die Operation **asynchron** ausführt.</span><span class="sxs-lookup"><span data-stu-id="96235-228">This class has a `Run` method that **asynchronously** executes the operation.</span></span> <span data-ttu-id="96235-229">Die Ausführung ist asynchron, weil die Ausführung auf realer Hardware asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="96235-229">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> <span data-ttu-id="96235-230">Da die `Run`-Methode asynchron ist, rufen wir die `Result`-Eigenschaft ab; dies blockiert die Ausführung, bis die Aufgabe abgeschlossen ist und das Ergebnis synchron zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="96235-230">Because the `Run` method is asynchronous, we fetch the `Result` property; this blocks execution until the task completes and returns the result synchronously.</span></span>
* <span data-ttu-id="96235-231">Verarbeiten des Ergebnisses der Operation.</span><span class="sxs-lookup"><span data-stu-id="96235-231">Process the result of the operation.</span></span> <span data-ttu-id="96235-232">Im Beispiel empfängt `res` das Ergebnis der Operation.</span><span class="sxs-lookup"><span data-stu-id="96235-232">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="96235-233">Hier ist das Ergebnis ein Tupel der Anzahl von Nullen (`numZeros`) und der Anzahl von Einsen (`numOnes`), die vom Simulator gemessen wurden.</span><span class="sxs-lookup"><span data-stu-id="96235-233">Here the result is a tuple of the number of zeros (`numZeros`) and number of ones (`numOnes`) measured by the simulator.</span></span> <span data-ttu-id="96235-234">Dies wird in C# als ein ValueTuple zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="96235-234">This is returned as a ValueTuple in C#.</span></span> <span data-ttu-id="96235-235">Wir dekonstruieren das Tupel, um die zwei Felder zu erhalten, geben die Ergebnisse aus und warten auf einen Tastendruck.</span><span class="sxs-lookup"><span data-stu-id="96235-235">We deconstruct the tuple to get the two fields, print the results, and wait for a keypress.</span></span>

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a><span data-ttu-id="96235-236">Erstellen und Ausführen</span><span class="sxs-lookup"><span data-stu-id="96235-236">Build and run</span></span>

#### <a name="python"></a>[<span data-ttu-id="96235-237">Python</span><span class="sxs-lookup"><span data-stu-id="96235-237">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="96235-238">Führen Sie den folgenden Befehl an Ihrem Terminal aus:</span><span class="sxs-lookup"><span data-stu-id="96235-238">Run the following command at your terminal:</span></span>

    ```
    python host.py
    ```

    <span data-ttu-id="96235-239">Dieser Befehl führt die Hostanwendung aus, die die Q#-Operation simuliert.</span><span class="sxs-lookup"><span data-stu-id="96235-239">This command runs the host application, which simulates the Q# operation.</span></span>

<span data-ttu-id="96235-240">Dies sollten die Ergebnisse sein:</span><span class="sxs-lookup"><span data-stu-id="96235-240">The results should be:</span></span>

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="96235-241">Befehlszeile/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="96235-241">Command Line / Visual Studio Code</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="96235-242">Führen Sie Folgendes an Ihrem Terminal aus:</span><span class="sxs-lookup"><span data-stu-id="96235-242">Run the following at your terminal:</span></span>

    ```bash
    dotnet run
    ```

    <span data-ttu-id="96235-243">Durch diesen Befehl werden alle erforderlichen Pakete automatisch heruntergeladen, die Anwendung erstellt und anschließend an der Befehlszeile ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96235-243">This command will automatically download all required packages, build the application, then run it at the command line.</span></span>

1. <span data-ttu-id="96235-244">Drücken Sie alternativ **F1**, um die Befehlspalette zu öffnen, und wählen Sie **Debug: Starten ohne Debuggen** aus.</span><span class="sxs-lookup"><span data-stu-id="96235-244">Alternatively, press **F1** to open the Command Palette and select **Debug: Start Without Debugging.**</span></span>
<span data-ttu-id="96235-245">Möglicherweise werden Sie aufgefordert, eine neue ``launch.json``-Datei zu erstellen, die beschreibt, wie das Programm gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="96235-245">You may be prompted to create a new ``launch.json`` file describing how to start the program.</span></span>
<span data-ttu-id="96235-246">Die standardmäßige ``launch.json`` sollte für die meisten Anwendungen gut funktionieren.</span><span class="sxs-lookup"><span data-stu-id="96235-246">The default ``launch.json`` should work well for most applications.</span></span>

<span data-ttu-id="96235-247">Dies sollten die Ergebnisse sein:</span><span class="sxs-lookup"><span data-stu-id="96235-247">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[<span data-ttu-id="96235-248">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96235-248">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="96235-249">Drücken Sie einfach `F5`, dann sollte Ihr Programm erstellt und ausgeführt werden!</span><span class="sxs-lookup"><span data-stu-id="96235-249">Just hit `F5`, and your program should build and run!</span></span>

<span data-ttu-id="96235-250">Dies sollten die Ergebnisse sein:</span><span class="sxs-lookup"><span data-stu-id="96235-250">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

<span data-ttu-id="96235-251">Das Programm wird beendet, nachdem Sie eine Taste drücken.</span><span class="sxs-lookup"><span data-stu-id="96235-251">The program will exit after you press a key.</span></span>

* * *

## <a name="prepare-superposition"></a><span data-ttu-id="96235-252">Vorbereiten von Überlagerung</span><span class="sxs-lookup"><span data-stu-id="96235-252">Prepare superposition</span></span>

<span data-ttu-id="96235-253">**Übersicht** Wir sehen uns nun an, wie in Q# die Überlagerung von Qubits erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="96235-253">**Overview** Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="96235-254">Sie wissen bereits, dass der Zustand eines Qubits den Überlagerungswert 0 und 1 aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="96235-254">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="96235-255">Wir verwenden den Vorgang `Hadamard`, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="96235-255">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="96235-256">Wenn das Qubit einen der klassischen Zustände aufweist (bei dem für eine Messung immer `Zero` oder immer `One` zurückgegeben wird), versetzt der Vorgang `Hadamard` bzw. `H` das Qubit in einen Zustand, in dem für eine Messung des Qubits in 50 % der Fälle `Zero` und in 50 % der Fälle `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96235-256">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="96235-257">Sie können sich das Qubit als Mischung von `Zero` und `One` vorstellen.</span><span class="sxs-lookup"><span data-stu-id="96235-257">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="96235-258">Wenn wir nun den Vorgang `TestBellState` simulieren, sehen wir nach der Messung, dass ungefähr mit der gleichen Häufigkeit `Zero` und `One` als Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96235-258">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

<span data-ttu-id="96235-259">Zuerst versuchen wir, das Qubit umzukehren (wenn das Qubit den Zustand `Zero` aufweist, wird in `One` umgekehrt (bzw. andersherum)).</span><span class="sxs-lookup"><span data-stu-id="96235-259">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="96235-260">Dies wird dadurch erreicht, dass wir den Vorgang `X` durchführen, bevor die Messung in `TestBellState` erfolgt:</span><span class="sxs-lookup"><span data-stu-id="96235-260">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="96235-261">Jetzt sind die Ergebnisse (nach dem Drücken von `F5`) umgekehrt:</span><span class="sxs-lookup"><span data-stu-id="96235-261">Now the results (after pressing `F5`) are reversed:</span></span>

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

<span data-ttu-id="96235-262">Aber alles, was wir bisher gesehen haben, ist klassisch.</span><span class="sxs-lookup"><span data-stu-id="96235-262">However, everything we've seen so far is classical.</span></span> <span data-ttu-id="96235-263">Rufen wir mal ein Quantenergebnis ab.</span><span class="sxs-lookup"><span data-stu-id="96235-263">Let's get a quantum result.</span></span> <span data-ttu-id="96235-264">Hierfür müssen wir lediglich den Vorgang `X` in der vorherigen Ausführung durch den Vorgang `H` (Hadamard-Vorgang) ersetzen.</span><span class="sxs-lookup"><span data-stu-id="96235-264">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="96235-265">Statt das Qubit ganz von 0 in 1 umzukehren, kehren wir es nur halb um.</span><span class="sxs-lookup"><span data-stu-id="96235-265">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="96235-266">Die ersetzten Zeilen in `TestBellState` sehen jetzt so aus:</span><span class="sxs-lookup"><span data-stu-id="96235-266">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="96235-267">Jetzt werden die Ergebnisse interessanter:</span><span class="sxs-lookup"><span data-stu-id="96235-267">Now the results get more interesting:</span></span>

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

<span data-ttu-id="96235-268">Jedes Mal, wenn wir messen, fragen wir nach einem klassischen Wert, aber das Qubit befindet sich auf halbem Weg zwischen 0 und 1, also erhalten wir (statistisch) die Hälfte der Zeit 0 und die Hälfte der Zeit 1.</span><span class="sxs-lookup"><span data-stu-id="96235-268">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span> <span data-ttu-id="96235-269">Dies wird als __Überlagerung__ bezeichnet und gibt uns unseren ersten echten Einblick in einen Quantenzustand.</span><span class="sxs-lookup"><span data-stu-id="96235-269">This is known as __superposition__ and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="96235-270">Vorbereiten von Verschränkung</span><span class="sxs-lookup"><span data-stu-id="96235-270">Prepare entanglement</span></span>

<span data-ttu-id="96235-271">**Übersicht:**  Als Nächstes sehen wir uns an, wie Qubits in Q# verschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="96235-271">**Overview:**  Now let’s look at how Q# expresses ways to entangle qubits.</span></span>  <span data-ttu-id="96235-272">Zuerst legen wir das erste Qubit auf den Anfangszustand fest und verwenden dann den Vorgang `H`, um die Überlagerung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="96235-272">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="96235-273">Vor dem Messen des ersten Qubits verwenden wir den neuen Vorgang `CNOT`. Diese Abkürzung steht für „Controlled-Not“.</span><span class="sxs-lookup"><span data-stu-id="96235-273">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-Not.</span></span>  <span data-ttu-id="96235-274">Das Ergebnis der Ausführung dieses Vorgangs für zwei Qubits ist, dass das zweite Qubit umgekehrt wird, wenn das erste Qubit `One` ist.</span><span class="sxs-lookup"><span data-stu-id="96235-274">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="96235-275">Die beiden Qubits sind nun verschränkt.</span><span class="sxs-lookup"><span data-stu-id="96235-275">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="96235-276">Unsere Statistiken für das erste Qubit haben sich nicht geändert (50:50-Wahrscheinlichkeit für `Zero` oder `One` nach der Messung), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits.</span><span class="sxs-lookup"><span data-stu-id="96235-276">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="96235-277">Unser `CNOT` hat die zwei Qubits verschränkt, sodass was immer mit dem einen von ihnen geschieht, auch mit dem anderen geschieht.</span><span class="sxs-lookup"><span data-stu-id="96235-277">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="96235-278">Wenn Sie die Messungen umkehrten (das zweite Qubit vor dem ersten messen), würde das Gleiche passieren.</span><span class="sxs-lookup"><span data-stu-id="96235-278">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="96235-279">Die erste Messung wäre zufällig, und die zweite wäre im Gleichschritt mit dem, was bei der ersten herausgefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="96235-279">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="96235-280">Im ersten Schritt müssen wir dazu in `TestBellState` 2 Qubits anstelle von einem zuweisen:</span><span class="sxs-lookup"><span data-stu-id="96235-280">The first thing we'll need to do is allocate 2 qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="96235-281">Dies ermöglicht es uns, einen neuen Vorgang (`CNOT`) hinzuzufügen, bevor wir in `TestBellState` die Messung (`M`) durchführen:</span><span class="sxs-lookup"><span data-stu-id="96235-281">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="96235-282">Wir haben eine weitere `Set`-Operation hinzugefügt, um das erste Qubit zu initialisieren, um sicherzustellen, dass es sich anfangs immer im `Zero`-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="96235-282">We've added another `Set` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="96235-283">Wir müssen außerdem das zweite Qubit zurücksetzen, bevor wir es freigeben.</span><span class="sxs-lookup"><span data-stu-id="96235-283">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

<span data-ttu-id="96235-284">Die vollständige Routine sieht jetzt so aus:</span><span class="sxs-lookup"><span data-stu-id="96235-284">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="96235-285">Wenn wir dies ausführen, erhalten wir exakt das gleiche 50-50-Ergebnis, das wir zuvor erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="96235-285">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="96235-286">Woran wir interessiert sind, ist aber die Reaktion des zweiten Qubits auf die Messung des ersten.</span><span class="sxs-lookup"><span data-stu-id="96235-286">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="96235-287">Wir fügen diese Statistik mit einer neuen Version der `TestBellState`-Operation hinzu:</span><span class="sxs-lookup"><span data-stu-id="96235-287">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="96235-288">Der neue Rückgabewert (`agree`) hält fest, wenn die Messung des ersten Qubits mit der Messung des zweiten Qubits übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="96235-288">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span> <span data-ttu-id="96235-289">Außerdem müssen wir die Hostanwendung entsprechend aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="96235-289">We also have to update the host application accordingly:</span></span>

#### <a name="python"></a>[<span data-ttu-id="96235-290">Python</span><span class="sxs-lookup"><span data-stu-id="96235-290">Python</span></span>](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[<span data-ttu-id="96235-291">C#</span><span class="sxs-lookup"><span data-stu-id="96235-291">C#</span></span>](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

<span data-ttu-id="96235-292">Bei einer erneuten Ausführung erhalten wir jetzt etwas ziemlich Erstaunliches:</span><span class="sxs-lookup"><span data-stu-id="96235-292">Now when we run, we get something pretty amazing:</span></span>

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

<span data-ttu-id="96235-293">Wie in der Übersicht beschrieben, haben sich unsere Statistiken für das erste Qubit nicht geändert (50:50-Wahrscheinlichkeit für 0 oder 1), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits, weil sie verschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="96235-293">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

<span data-ttu-id="96235-294">Herzlichen Glückwunsch, Sie haben Ihr erstes Quantenprogramm geschrieben!</span><span class="sxs-lookup"><span data-stu-id="96235-294">Congratulations, you've written your first quantum program!</span></span>

## <a name="whats-next"></a><span data-ttu-id="96235-295">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="96235-295">What's next?</span></span>

<span data-ttu-id="96235-296">Im Tutorial zur [Grover-Suche](xref:microsoft.quantum.quickstarts.search) wird veranschaulicht, wie Sie die Grover-Suche erstellen und ausführen. Dies ist einer der beliebtesten Algorithmen des Quantencomputings und ein schönes Beispiel für ein Q#-Programm, das zum Lösen echter Probleme im Bereich des Quantencomputings eingesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="96235-296">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="96235-297">Der [Artikel zum Einstieg in das Quantum Development Kit](xref:microsoft.quantum.welcome) enthält Informationen zu weiteren Möglichkeiten, wie Sie Q# und die Quantenprogrammierung erlernen können.</span><span class="sxs-lookup"><span data-stu-id="96235-297">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>

