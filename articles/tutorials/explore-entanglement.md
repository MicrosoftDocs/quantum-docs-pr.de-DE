---
title: Entdecken Sie jede Verflechtungen mit Q#
description: Erfahren Sie, wie Sie ein Quantum-Programm in schreiben Q# . Entwickeln Sie eine Bell-Zustandsanwendung mithilfe des Quantum Development Kit (QDK)
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- Q#
- $$v
ms.openlocfilehash: d815a9a25b8ba5e9489b6d3d27fb0d64ab4aaa1d
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863442"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="a32e8-104">Tutorial: Erkunden der Verschränkung mit Q\#</span><span class="sxs-lookup"><span data-stu-id="a32e8-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="a32e8-105">In diesem Tutorial zeigen wir Ihnen, wie Sie ein Q# Programm schreiben, das Qubits manipuliert und misst und die Auswirkungen von Superposition und entanglement veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="a32e8-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>

<span data-ttu-id="a32e8-106">Sie schreiben eine Anwendung mit dem Namen „Bell“, um die Quantenverschränkung zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-106">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="a32e8-107">Der Name „Bell“ bezieht sich auf die Bell-Zustände. Hierbei handelt es sich um spezifische Quantenzustände von zwei Qubits, die zum Darstellen der einfachsten Beispiele für Überlagerungen und Quantenverschränkungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-107">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="a32e8-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a32e8-108">Pre-requisites</span></span>

<span data-ttu-id="a32e8-109">Führen Sie zunächst diese Schritte aus, wenn Sie bereit zum Codieren sind:</span><span class="sxs-lookup"><span data-stu-id="a32e8-109">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="a32e8-110">[Installieren](xref:microsoft.quantum.install) Sie das Quantum Development Kit mit Ihrer bevorzugten Sprache und Entwicklungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="a32e8-110">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your  preferred language and development environment.</span></span>
* <span data-ttu-id="a32e8-111">Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde</span><span class="sxs-lookup"><span data-stu-id="a32e8-111">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="a32e8-112">Sie können auch mit der Erzählung arbeiten, ohne das QDK zu installieren, indem Sie die Übersichten der Q# Programmiersprache und die ersten Konzepte von Quantum Computing überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-112">You can also follow along with the narrative without installing the QDK, reviewing  the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="a32e8-113">In diesem Tutorial lernen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a32e8-113">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="a32e8-114">Erstellen und Kombinieren von Vorgängen in Q\#</span><span class="sxs-lookup"><span data-stu-id="a32e8-114">Create and combine operations in Q\#</span></span>
> * <span data-ttu-id="a32e8-115">Erstellen Sie Vorgänge zum Platzieren von Qubits in der superposition, entangle und messen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-115">Create operations to put qubits in superposition, entangle and measure them.</span></span>
> * <span data-ttu-id="a32e8-116">Veranschaulichen von Quantum jede Verflechtungen mit einem Programm, das Q# in einem Simulator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-116">Demonstrate quantum entanglement with a Q# program run in a simulator.</span></span> 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a><span data-ttu-id="a32e8-117">Demonstrieren des Qubit-Verhaltens mit dem QDK</span><span class="sxs-lookup"><span data-stu-id="a32e8-117">Demonstrating qubit behavior with the QDK</span></span>

<span data-ttu-id="a32e8-118">Klassische Bits enthalten einen einzelnen binären Wert (0 oder 1). Der Zustand eines [Qubits](xref:microsoft.quantum.glossary#qubit) kann dagegen eine **Superposition** sein (also 0 und 1).</span><span class="sxs-lookup"><span data-stu-id="a32e8-118">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="a32e8-119">Konzeptionell kann der Zustand eines Qubit als Richtung in einem abstrakten Raum (auch als Vektor bezeichnet) betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-119">Conceptually, the state of a qubit can be thought of as a direction in an abstract space (also known as a vector).</span></span>  <span data-ttu-id="a32e8-120">Ein Qubit-Zustand kann sich in einer der möglichen Richtungen befinden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-120">A qubit state can be in any of the possible directions.</span></span> <span data-ttu-id="a32e8-121">Die beiden **klassischen Zustände** sind die beiden Richtungen, die für die einhundertprozentige Chance einer Messung von 0 und die einhundertprozentige Chance einer Messung von 1 stehen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-121">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>

<span data-ttu-id="a32e8-122">Mit dem Messvorgang wird ein binäres Ergebnis erzeugt und ein Qubit-Zustand geändert.</span><span class="sxs-lookup"><span data-stu-id="a32e8-122">The act of measurement produces a binary result and changes a qubit state.</span></span>
<span data-ttu-id="a32e8-123">Die Messung erzeugt einen binären Wert, entweder 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="a32e8-123">Measurement  produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="a32e8-124">Das Qubit geht von einem Überlagerungszustand (beliebige Richtung) in einen der klassischen Zustände über.</span><span class="sxs-lookup"><span data-stu-id="a32e8-124">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="a32e8-125">Danach führt die Wiederholung der gleichen Messung ohne Eingriff zu demselben binären Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="a32e8-125">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="a32e8-126">Mehrere Qubits können [**verschränkt**](xref:microsoft.quantum.glossary#entanglement) sein.</span><span class="sxs-lookup"><span data-stu-id="a32e8-126">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span>  <span data-ttu-id="a32e8-127">Bei der Messung eines verschränkten Qubits wird unsere Kenntnis des Zustands der anderen Qubits ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a32e8-127">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="a32e8-128">Nun können wir veranschaulichen, wie Q# dieses Verhalten ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-128">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="a32e8-129">Sie beginnen mit dem einfachsten möglichen Programm und erweitern es anschließend, um die Quantenüberlagerung und -verschränkung zu demonstrieren.</span><span class="sxs-lookup"><span data-stu-id="a32e8-129">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="creating-a-no-locq-project"></a><span data-ttu-id="a32e8-130">Erstellen eines Q# Projekts</span><span class="sxs-lookup"><span data-stu-id="a32e8-130">Creating a Q# project</span></span>

<span data-ttu-id="a32e8-131">Als erstes müssen Sie ein neues Q# Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-131">The first thing we have to do is to create a new Q# project.</span></span> <span data-ttu-id="a32e8-132">In diesem Tutorial verwenden wir die Umgebung auf der Grundlage von [ Q# Anwendungen mit vs Code](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="a32e8-132">In this tutorial we are going to use the environment based on [Q# applications with VS Code](xref:microsoft.quantum.install.standalone).</span></span>

<span data-ttu-id="a32e8-133">So erstellen Sie ein neues Projekt in vs Code:</span><span class="sxs-lookup"><span data-stu-id="a32e8-133">To create a new project, in VS Code:</span></span> 

1. <span data-ttu-id="a32e8-134">Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="a32e8-134">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="a32e8-135">Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).</span><span class="sxs-lookup"><span data-stu-id="a32e8-135">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="a32e8-136">Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="a32e8-136">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="a32e8-137">Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).</span><span class="sxs-lookup"><span data-stu-id="a32e8-137">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="a32e8-138">In diesem Fall haben wir das Projekt aufgerufen `Bell` .</span><span class="sxs-lookup"><span data-stu-id="a32e8-138">In this case we called the project `Bell`.</span></span> <span data-ttu-id="a32e8-139">Hierdurch werden zwei Dateien generiert: `Bell.csproj` , die Projektdatei und `Program.qs` , eine Vorlage einer-Anwendung, die Q# wir zum Schreiben der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-139">This generates two files: `Bell.csproj`, the project file and `Program.qs`, a template of a Q# application that we will use to write our application.</span></span> <span data-ttu-id="a32e8-140">Der Inhalt von `Program.qs` sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="a32e8-140">The content of `Program.qs` should be:</span></span>

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a><span data-ttu-id="a32e8-141">Schreiben der Q- \# Anwendung</span><span class="sxs-lookup"><span data-stu-id="a32e8-141">Write the Q\# application</span></span>
 
<span data-ttu-id="a32e8-142">Unser Ziel ist es, zwei Qubits in einem bestimmten Quantum-Zustand vorzubereiten. Dies veranschaulicht, wie Sie mit Qubits in arbeiten, Q# um ihren Zustand zu ändern und die Auswirkungen von Superposition und entanglement zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-142">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="a32e8-143">Wir erstellen Dies Stück für Stück, um Qubit-Zustände,-Vorgänge und-Messungen vorzustellen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-143">We will build this up piece by piece to introduce qubit states, operations, and measurement.</span></span>

### <a name="initialize-qubit-using-measurement"></a><span data-ttu-id="a32e8-144">Initialisieren von Qubit mithilfe von Messungen</span><span class="sxs-lookup"><span data-stu-id="a32e8-144">Initialize qubit using measurement</span></span>

<span data-ttu-id="a32e8-145">Im ersten nachfolgenden Code wird gezeigt, wie Sie in mit Qubits arbeiten Q# .</span><span class="sxs-lookup"><span data-stu-id="a32e8-145">In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="a32e8-146">Wir führen zwei Vorgänge ein, [`M`](xref:microsoft.quantum.intrinsic.m) die [`X`](xref:microsoft.quantum.intrinsic.x) den Zustand eines Qubit transformieren.</span><span class="sxs-lookup"><span data-stu-id="a32e8-146">We’ll introduce two operations, [`M`](xref:microsoft.quantum.intrinsic.m) and [`X`](xref:microsoft.quantum.intrinsic.x) that transform the state of a qubit.</span></span> <span data-ttu-id="a32e8-147">In diesem Codeausschnitt wird der Vorgang `SetQubitState` definiert, für den als Parameter ein Qubit verwendet wird, sowie ein weiterer Parameter `desired`, mit dem der gewünschte Zustand für das Qubit dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-147">In this code snippet, an operation `SetQubitState` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="a32e8-148">Der Vorgang `SetQubitState` führt eine Messung für das Qubit durch, indem der Vorgang `M` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-148">The operation `SetQubitState` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="a32e8-149">In Q# gibt eine Qubit-Messung immer entweder `Zero` oder zurück `One` .</span><span class="sxs-lookup"><span data-stu-id="a32e8-149">In Q#, a qubit measurement always returns either `Zero` or `One`.</span></span>  <span data-ttu-id="a32e8-150">Wenn die Messung einen Wert zurückgibt, der nicht gleich dem gewünschten Wert ist, wird `SetQubitState` das Qubit geflippt, d. h., es wird ein `X` Vorgang ausgeführt, der den Qubit-Zustand in einen neuen Zustand ändert, in dem die Wahrscheinlichkeiten eines Messwerts, der zurück `Zero` gibt, und `One` umgekehrt werden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-150">If the measurement returns a value not equal to the desired value, `SetQubitState` “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span> <span data-ttu-id="a32e8-151">Auf diese Weise wird `SetQubitState` das Ziel-Qubit immer in den gewünschten Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-151">This way, `SetQubitState` always puts the target qubit in the desired state.</span></span>

<span data-ttu-id="a32e8-152">Ersetzen Sie den Inhalt von `Program.qs` durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="a32e8-152">Replace the contents of `Program.qs` with the following code:</span></span>


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

<span data-ttu-id="a32e8-153">Dieser Vorgang kann jetzt aufgerufen werden, um ein Qubit auf einen klassischen Zustand festzulegen, indem entweder immer `Zero` oder immer `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-153">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>
<span data-ttu-id="a32e8-154">`Zero` und `One` sind Konstanten, die die beiden einzigen möglichen Ergebnisse der Messung eines Qubits darstellen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-154">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

<span data-ttu-id="a32e8-155">Mit dem Vorgang `SetQubitState` wird das Qubit gemessen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-155">The operation `SetQubitState` measures the qubit.</span></span> <span data-ttu-id="a32e8-156">Falls sich das Qubit im gewünschten Zustand befindet, wird es von `SetQubitState` unverändert gelassen. Andernfalls ändern wir den Qubit-Zustand in den gewünschten Zustand, indem wir den Vorgang `X` ausführen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-156">If the qubit is in the state we want, `SetQubitState` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

#### <a name="about-no-locq-operations"></a><span data-ttu-id="a32e8-157">Informationen zu Q# Vorgängen</span><span class="sxs-lookup"><span data-stu-id="a32e8-157">About Q# operations</span></span>

<span data-ttu-id="a32e8-158">Ein- Q# Vorgang ist eine Quantum-Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="a32e8-158">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="a32e8-159">Das heißt, es handelt sich um eine Aufruf Bare Routine, die Aufrufe von anderen Quantum-Vorgängen enthält.</span><span class="sxs-lookup"><span data-stu-id="a32e8-159">That is, it is a callable routine that contains calls to other quantum operations.</span></span>

<span data-ttu-id="a32e8-160">Die Argumente für eine Operation werden als Tupel angegeben, in Klammern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-160">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="a32e8-161">Der Rückgabetyp der Operation wird nach einem Doppelpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="a32e8-161">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="a32e8-162">In diesem Fall hat die Operation `SetQubitState` keinen Rückgabewert, daher ist sie als `Unit` zurückgebend markiert.</span><span class="sxs-lookup"><span data-stu-id="a32e8-162">In this case, the `SetQubitState` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="a32e8-163">Dies Q# entspricht `unit` in F #, das ungefähr analog zu `void` in c# ist, und ein leeres Tupel ( `Tuple[()]` ) in Python.</span><span class="sxs-lookup"><span data-stu-id="a32e8-163">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="a32e8-164">Sie haben im ersten Vorgang zwei Quantum-Vorgänge verwendet Q# :</span><span class="sxs-lookup"><span data-stu-id="a32e8-164">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="a32e8-165">Der [`M`](xref:microsoft.quantum.intrinsic.m) Vorgang, der den Zustand des Qubit misst.</span><span class="sxs-lookup"><span data-stu-id="a32e8-165">The [`M`](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="a32e8-166">Der [`X`](xref:microsoft.quantum.intrinsic.x) Vorgang, der den Zustand eines Qubit kippt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-166">The [`X`](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="a32e8-167">Mit einem Quantenvorgang wird der Zustand eines Qubits transformiert.</span><span class="sxs-lookup"><span data-stu-id="a32e8-167">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="a32e8-168">Analog zu klassischen Logikgattern wird anstelle von Vorgängen auch von Quantengattern gesprochen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-168">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="a32e8-169">Diese Bezeichnung stammt aus den Anfängen des Quantencomputings, als Algorithmen lediglich ein theoretisches Konstrukt waren und in Form von Diagrammen visualisiert wurden – ähnlich wie bei einem Schaltplan im Bereich des klassischen Computings.</span><span class="sxs-lookup"><span data-stu-id="a32e8-169">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="counting-measurement-outcomes"></a><span data-ttu-id="a32e8-170">Zählen der Messergebnisse</span><span class="sxs-lookup"><span data-stu-id="a32e8-170">Counting measurement outcomes</span></span>

<span data-ttu-id="a32e8-171">Zur Veranschaulichung der Auswirkungen des Vorgangs `SetQubitState` wird dann der Vorgang `TestBellState` hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-171">To demonstrate the effect of the `SetQubitState` operation, a `TestBellState` operation is then added.</span></span> <span data-ttu-id="a32e8-172">Für diesen Vorgang wird `Zero` oder `One` als Eingabe verwendet, und der Vorgang `SetQubitState` wird einige Male mit dieser Eingabe aufgerufen. Es wird gezählt, wie oft bei der Messung des Qubits `Zero` und wie oft `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-172">This operation takes as input a `Zero` or `One`, and calls the `SetQubitState` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="a32e8-173">Bei der ersten Simulation des Vorgangs `TestBellState` erwarten wir natürlich, dass in der Ausgabe für alle Messungen des Qubits mit `Zero` als Parametereingabe `Zero` und für alle Messungen eines Qubits mit `One` als Parametereingabe `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-173">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span> <span data-ttu-id="a32e8-174">Im weiteren Verlauf fügen wir Code hinzu, `TestBellState` um Superposition und entanglement zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-174">Further on, we’ll add code to `TestBellState` to demonstrate superposition and entanglement.</span></span>

<span data-ttu-id="a32e8-175">Fügen Sie der `Program.qs`-Datei die folgende Operation hinzu, innerhalb des Namespaces, nach dem Ende der `SetQubitState`-Operation:</span><span class="sxs-lookup"><span data-stu-id="a32e8-175">Add the following operation to the `Program.qs` file, inside the namespace, after the end of the `SetQubitState` operation:</span></span>

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
<span data-ttu-id="a32e8-176">Beachten Sie, dass wir eine Zeile vor hinzugefügt haben `return` , um eine erklärende Nachricht in der-Konsole mit der-Funktion ( `Message` ) [Microsoft. Quantum. intrinsi. Message] zu drucken.</span><span class="sxs-lookup"><span data-stu-id="a32e8-176">Note that we added a line before the `return` to print an explanatory message in the console with the function (`Message`)[microsoft.quantum.intrinsic.message]</span></span>

<span data-ttu-id="a32e8-177">Diese Operation (`TestBellState`) iteriert `count` Iterationen lang in einer Schleife, legt einen angegebenen `initial`-Wert für ein Qubit fest, und misst (`M`) dann das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="a32e8-177">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="a32e8-178">Sie führt eine Statistik zur Anzahl der gemessenen Nullen und Einsen und gibt diese an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="a32e8-178">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="a32e8-179">Sie führt eine weitere erforderliche Operation aus.</span><span class="sxs-lookup"><span data-stu-id="a32e8-179">It performs one other necessary operation.</span></span> <span data-ttu-id="a32e8-180">Sie setzt das Qubit auf einen bekannten Zustand (`Zero`) zurück, bevor sie es zurückgibt, was es anderen ermöglicht, dieses Qubit in einem bekannten Zustand zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-180">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="a32e8-181">Dies ist aufgrund der `using`-Anweisung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a32e8-181">This is required by the `using` statement.</span></span>

#### <a name="about-variables-in-q"></a><span data-ttu-id="a32e8-182">Informationen zu Variablen in Q\#</span><span class="sxs-lookup"><span data-stu-id="a32e8-182">About variables in Q\#</span></span>

<span data-ttu-id="a32e8-183">Standardmäßig sind Variablen in Q# unveränderlich; ihr Wert kann nicht geändert werden, nachdem Sie gebunden wurden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-183">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="a32e8-184">Das `let`-Schlüsselwort wird verwendet, um die Bindung einer unveränderlichen Variable anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a32e8-184">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="a32e8-185">Operationsargumente sind immer unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="a32e8-185">Operation arguments are always immutable.</span></span>

<span data-ttu-id="a32e8-186">Wenn Sie eine Variable benötigen, deren Wert geändert werden kann, wie etwa `numOnes` im Beispiel, können Sie die Variable mit dem Schlüsselwort `mutable` deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a32e8-186">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="a32e8-187">Der Wert einer veränderlichen Variable kann mithilfe einer `setQubitState`-Anweisung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a32e8-187">A mutable variable's value may be changed using a `setQubitState` statement.</span></span>

<span data-ttu-id="a32e8-188">In beiden Fällen wird der Typ einer Variablen vom Compiler abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="a32e8-188">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="a32e8-189">Q# Es sind keine Typanmerkungen für Variablen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a32e8-189">Q# doesn't require any type annotations for variables.</span></span>

#### <a name="about-using-statements-in-q"></a><span data-ttu-id="a32e8-190">Informationen zu `using` Anweisungen in Q\#</span><span class="sxs-lookup"><span data-stu-id="a32e8-190">About `using` statements in Q\#</span></span>

<span data-ttu-id="a32e8-191">Die- `using` Anweisung ist auch speziell für Q# .</span><span class="sxs-lookup"><span data-stu-id="a32e8-191">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="a32e8-192">Sie wird verwendet, um Qubits für die Verwendung in einem Codeblock zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-192">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="a32e8-193">In Q# werden alle Qubits dynamisch zugeordnet und freigegeben, anstatt fixierte Ressourcen zu sein, die für die gesamte Lebensdauer eines komplexen Algorithmus vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a32e8-193">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="a32e8-194">Eine `using`-Anweisung weist eine Reihe Qubits am Anfang zu und gibt diese Qubits am Ende des Blocks wieder frei.</span><span class="sxs-lookup"><span data-stu-id="a32e8-194">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="run-the-code-from-the-command-prompt"></a><span data-ttu-id="a32e8-195">Ausführen des Codes an der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="a32e8-195">Run the code from the command prompt</span></span>

<span data-ttu-id="a32e8-196">Um den Code auszuführen, muss der Compiler angegeben werden *, der* beim Bereitstellen des Befehls aufgerufen werden kann `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="a32e8-196">In order to run the code we need to specify the compiler *which* callable to run when we provide the `dotnet run` command.</span></span> <span data-ttu-id="a32e8-197">Dies erfolgt mit einer einfachen Änderung in der Q# Datei, indem eine Zeile hinzugefügt wird, die `@EntryPoint()` direkt vor der Aufruf baren Zeile steht: der `TestBellState` Vorgang in diesem Fall.</span><span class="sxs-lookup"><span data-stu-id="a32e8-197">This is done with a simple change in the Q# file by adding a line with `@EntryPoint()` directly preceding the callable: the `TestBellState` operation in this case.</span></span> <span data-ttu-id="a32e8-198">Der vollständige Code sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="a32e8-198">The full code should be:</span></span>

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

<span data-ttu-id="a32e8-199">Um das Programm auszuführen, müssen Sie die `count` Argumente und an `initial` der Eingabeaufforderung angeben.</span><span class="sxs-lookup"><span data-stu-id="a32e8-199">To run the program we need to specify `count` and `initial` arguments from the command prompt.</span></span> <span data-ttu-id="a32e8-200">Wählen Sie z. b `count = 1000` . und aus `initial = One` .</span><span class="sxs-lookup"><span data-stu-id="a32e8-200">Let's choose for example `count = 1000` and `initial = One`.</span></span> <span data-ttu-id="a32e8-201">Geben Sie den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="a32e8-201">Enter the following command:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

<span data-ttu-id="a32e8-202">Und Sie sollten die folgende Ausgabe beachten:</span><span class="sxs-lookup"><span data-stu-id="a32e8-202">And you should observe the following output:</span></span>

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="a32e8-203">Wenn Sie mit versuchen, `initial = Zero` sollten Sie Folgendes beachten:</span><span class="sxs-lookup"><span data-stu-id="a32e8-203">If you try with `initial = Zero` you should observe:</span></span>

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a><span data-ttu-id="a32e8-204">Vorbereiten von Überlagerung</span><span class="sxs-lookup"><span data-stu-id="a32e8-204">Prepare superposition</span></span>

<span data-ttu-id="a32e8-205">Sehen wir uns nun an, wie die Q# Methoden zum Platzieren von Qubits in der superposition ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-205">Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="a32e8-206">Sie wissen bereits, dass der Zustand eines Qubits den Überlagerungswert 0 und 1 aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="a32e8-206">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="a32e8-207">Wir verwenden den Vorgang `Hadamard`, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-207">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="a32e8-208">Wenn das Qubit einen der klassischen Zustände aufweist (bei dem für eine Messung immer `Zero` oder immer `One` zurückgegeben wird), versetzt der Vorgang `Hadamard` bzw. `H` das Qubit in einen Zustand, in dem für eine Messung des Qubits in 50 % der Fälle `Zero` und in 50 % der Fälle `One` zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-208">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="a32e8-209">Sie können sich das Qubit als Mischung von `Zero` und `One` vorstellen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-209">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="a32e8-210">Wenn wir nun den Vorgang `TestBellState` simulieren, sehen wir nach der Messung, dass ungefähr mit der gleichen Häufigkeit `Zero` und `One` als Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a32e8-210">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

### <a name="x-flips-qubit-state"></a><span data-ttu-id="a32e8-211">`X` kippt-Qubit-Status</span><span class="sxs-lookup"><span data-stu-id="a32e8-211">`X` flips qubit state</span></span>

<span data-ttu-id="a32e8-212">Zuerst versuchen wir, das Qubit umzukehren (wenn das Qubit den Zustand `Zero` aufweist, wird in `One` umgekehrt (bzw. andersherum)).</span><span class="sxs-lookup"><span data-stu-id="a32e8-212">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="a32e8-213">Dies wird dadurch erreicht, dass wir den Vorgang `X` durchführen, bevor die Messung in `TestBellState` erfolgt:</span><span class="sxs-lookup"><span data-stu-id="a32e8-213">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="a32e8-214">Nun werden die Ergebnisse umgekehrt:</span><span class="sxs-lookup"><span data-stu-id="a32e8-214">Now the results are reversed:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="a32e8-215">Sehen wir uns nun die Quantum-Eigenschaften der Qubits an.</span><span class="sxs-lookup"><span data-stu-id="a32e8-215">Now let's explore the quantum properties of the qubits.</span></span>

### <a name="h-prepares-superposition"></a><span data-ttu-id="a32e8-216">`H` bereitet die Superposition vor</span><span class="sxs-lookup"><span data-stu-id="a32e8-216">`H` prepares superposition</span></span>

<span data-ttu-id="a32e8-217">Hierfür müssen wir lediglich den Vorgang `X` in der vorherigen Ausführung durch den Vorgang `H` (Hadamard-Vorgang) ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-217">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="a32e8-218">Statt das Qubit ganz von 0 in 1 umzukehren, kehren wir es nur halb um.</span><span class="sxs-lookup"><span data-stu-id="a32e8-218">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="a32e8-219">Die ersetzten Zeilen in `TestBellState` sehen jetzt so aus:</span><span class="sxs-lookup"><span data-stu-id="a32e8-219">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="a32e8-220">Jetzt werden die Ergebnisse interessanter:</span><span class="sxs-lookup"><span data-stu-id="a32e8-220">Now the results get more interesting:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

<span data-ttu-id="a32e8-221">Jedes Mal, wenn wir messen, fragen wir nach einem klassischen Wert, aber das Qubit befindet sich auf halbem Weg zwischen 0 und 1, also erhalten wir (statistisch) die Hälfte der Zeit 0 und die Hälfte der Zeit 1.</span><span class="sxs-lookup"><span data-stu-id="a32e8-221">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span>
<span data-ttu-id="a32e8-222">Dies wird als **Überlagerung** bezeichnet und gibt uns unseren ersten echten Einblick in einen Quantenzustand.</span><span class="sxs-lookup"><span data-stu-id="a32e8-222">This is known as **superposition** and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="a32e8-223">Vorbereiten von Verschränkung</span><span class="sxs-lookup"><span data-stu-id="a32e8-223">Prepare entanglement</span></span>

<span data-ttu-id="a32e8-224">Sehen wir uns nun an Q# , wie Methoden zum entangle-Qubits ausdrückt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-224">Now let’s look at how Q# expresses ways to entangle qubits.</span></span>
<span data-ttu-id="a32e8-225">Zuerst legen wir das erste Qubit auf den Anfangszustand fest und verwenden dann den Vorgang `H`, um die Überlagerung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-225">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="a32e8-226">Bevor wir das erste Qubit Messen, verwenden wir dann einen neuen Vorgang ( `CNOT` ), der für "kontrolliert-not" steht.</span><span class="sxs-lookup"><span data-stu-id="a32e8-226">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-NOT.</span></span>  <span data-ttu-id="a32e8-227">Das Ergebnis der Ausführung dieses Vorgangs für zwei Qubits ist, dass das zweite Qubit umgekehrt wird, wenn das erste Qubit `One` ist.</span><span class="sxs-lookup"><span data-stu-id="a32e8-227">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="a32e8-228">Die beiden Qubits sind nun verschränkt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-228">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="a32e8-229">Unsere Statistiken für das erste Qubit haben sich nicht geändert (50:50-Wahrscheinlichkeit für `Zero` oder `One` nach der Messung), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits.</span><span class="sxs-lookup"><span data-stu-id="a32e8-229">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="a32e8-230">Unser `CNOT` hat die zwei Qubits verschränkt, sodass was immer mit dem einen von ihnen geschieht, auch mit dem anderen geschieht.</span><span class="sxs-lookup"><span data-stu-id="a32e8-230">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="a32e8-231">Wenn Sie die Messungen umkehrten (das zweite Qubit vor dem ersten messen), würde das Gleiche passieren.</span><span class="sxs-lookup"><span data-stu-id="a32e8-231">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="a32e8-232">Die erste Messung wäre zufällig, und die zweite wäre im Gleichschritt mit dem, was bei der ersten herausgefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="a32e8-232">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="a32e8-233">Als erstes müssen wir zwei Qubits anstelle eines in zuordnen `TestBellState` :</span><span class="sxs-lookup"><span data-stu-id="a32e8-233">The first thing we'll need to do is allocate two qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="a32e8-234">Dies ermöglicht es uns, einen neuen Vorgang (`CNOT`) hinzuzufügen, bevor wir in `TestBellState` die Messung (`M`) durchführen:</span><span class="sxs-lookup"><span data-stu-id="a32e8-234">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="a32e8-235">Wir haben eine weitere `SetQubitState`-Operation hinzugefügt, um das erste Qubit zu initialisieren, um sicherzustellen, dass es sich anfangs immer im `Zero`-Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="a32e8-235">We've added another `SetQubitState` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="a32e8-236">Wir müssen außerdem das zweite Qubit zurücksetzen, bevor wir es freigeben.</span><span class="sxs-lookup"><span data-stu-id="a32e8-236">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

<span data-ttu-id="a32e8-237">Die vollständige Routine sieht jetzt so aus:</span><span class="sxs-lookup"><span data-stu-id="a32e8-237">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="a32e8-238">Wenn wir dies ausführen, erhalten wir exakt das gleiche 50-50-Ergebnis, das wir zuvor erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="a32e8-238">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="a32e8-239">Woran wir interessiert sind, ist aber die Reaktion des zweiten Qubits auf die Messung des ersten.</span><span class="sxs-lookup"><span data-stu-id="a32e8-239">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="a32e8-240">Wir fügen diese Statistik mit einer neuen Version der `TestBellState`-Operation hinzu:</span><span class="sxs-lookup"><span data-stu-id="a32e8-240">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="a32e8-241">Der neue Rückgabewert (`agree`) hält fest, wenn die Messung des ersten Qubits mit der Messung des zweiten Qubits übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a32e8-241">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span>

<span data-ttu-id="a32e8-242">Der folgende Code wird ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="a32e8-242">Running the code we obtain:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

<span data-ttu-id="a32e8-243">Wie in der Übersicht beschrieben, haben sich unsere Statistiken für das erste Qubit nicht geändert (50:50-Wahrscheinlichkeit für 0 oder 1), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits, weil sie verschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="a32e8-243">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

## <a name="next-steps"></a><span data-ttu-id="a32e8-244">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a32e8-244">Next steps</span></span>

<span data-ttu-id="a32e8-245">Im Lernprogramm [Grover](xref:microsoft.quantum.quickstarts.search) finden Sie Informationen zum Erstellen und Ausführen der Grover-Suche, einer der gängigsten Quantum Computing-Algorithmen und bietet ein gutes Beispiel für ein Q# Programm, das verwendet werden kann, um reale Probleme mit Quantum Computing zu lösen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-245">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="a32e8-246">In den ersten Schritten [mit dem Quantum Development Kit werden](xref:microsoft.quantum.welcome) weitere Möglichkeiten zum Erlernen Q# und der quantumprogrammierung empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a32e8-246">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
