---
title: 'Schreiben und Simulieren von Programmen auf Qubit-Ebene in Q #'
description: Schritt-für-Schritt-Tutorial zum Schreiben und Simulieren eines Quantum-Programms, das auf der einzelnen Qubit-Ebene funktioniert
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
ms.openlocfilehash: 05d3292e1c6e3c8c1163c460f2aaa51c591aa1d5
ms.sourcegitcommit: 8d9d392bf5e114ae223e6f689ba80d25866ff586
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2020
ms.locfileid: "84422239"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a><span data-ttu-id="c499e-103">Tutorial: schreiben und Simulieren von Programmen auf Qubit-Ebene in Q\#</span><span class="sxs-lookup"><span data-stu-id="c499e-103">Tutorial: Write and simulate qubit-level programs in Q\#</span></span>

<span data-ttu-id="c499e-104">Willkommen beim Quantum Development Kit-Tutorial zum Schreiben und Simulieren eines grundlegenden quantumprogramms, das auf einzelnen Qubits funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c499e-104">Welcome to the Quantum Development Kit tutorial on writing and simulating a basic quantum program that operates on individual qubits.</span></span> 

<span data-ttu-id="c499e-105">Obwohl Q # primär als allgemeine Programmiersprache für große Quantum-Programme erstellt wurde, kann es genauso einfach verwendet werden, um die niedrigere Ebene der Quantum-Programme zu untersuchen: direktes adressieren spezifischer Qubits.</span><span class="sxs-lookup"><span data-stu-id="c499e-105">Although Q# was primarily created as a high-level programming language for large-scale quantum programs, it can just as easily be used to explore the lower level of quantum programs: directly addressing specific qubits.</span></span>
<span data-ttu-id="c499e-106">Die Flexibilität von Q # ermöglicht es Benutzern, Quantum-Systeme von einer beliebigen Art von Abstraktion anzugehen, und in diesem Tutorial werden die Qubits selbst beleuchtet.</span><span class="sxs-lookup"><span data-stu-id="c499e-106">The flexibility of Q# allows users to approach quantum systems from any such level of abstraction, and in this tutorial we dive into the qubits themselves.</span></span>
<span data-ttu-id="c499e-107">Insbesondere betrachten wir die [Dynamik der Quantum Fourier-Transformation](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), eine Unterroutine, die für viele größere Quantum-Algorithmen von wesentlicher Bedeutung ist.</span><span class="sxs-lookup"><span data-stu-id="c499e-107">Specifically, we take a look under the hood of the [quantum Fourier transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), a subroutine that is integral to many larger quantum algorithms.</span></span>

<span data-ttu-id="c499e-108">Beachten Sie, dass dieser Low-Level-Überblick über die Verarbeitung von Quantum-Informationen häufig in Bezug auf "[Quantum](xref:microsoft.quantum.concepts.circuits)-Verbindungen" beschrieben wird, die die sequenzielle Anwendung von Gates auf bestimmte Qubits eines Systems darstellen.</span><span class="sxs-lookup"><span data-stu-id="c499e-108">Note that this low-level view of quantum information processing is often described in terms of "[quantum circuits](xref:microsoft.quantum.concepts.circuits)," which represent the sequential application of gates to specific qubits of a system.</span></span>

<span data-ttu-id="c499e-109">Folglich können die von uns sequenziell angewendenden Single-und Multi-Qubit-Vorgänge in einem "Verbindungs Diagramm" dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-109">Thus, the single- and multi-qubit operations we sequentially apply can be readily represented in a "circuit diagram."</span></span>
<span data-ttu-id="c499e-110">In unserem Fall definieren wir einen Q #-Vorgang, um die vollständige drei-Qubit-Quantum Fourier-Transformation durchzuführen, die die folgende Darstellung als Verbindung aufweist:</span><span class="sxs-lookup"><span data-stu-id="c499e-110">In our case, we will define a Q# operation to perform the full three-qubit quantum Fourier transform, which has the following representation as a circuit:</span></span>

<br/>
<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a><span data-ttu-id="c499e-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c499e-111">Prerequisites</span></span>

* <span data-ttu-id="c499e-112">[Installieren](xref:microsoft.quantum.install) Sie das Quantum Development Kit mit Ihrer bevorzugten Sprache und Entwicklungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="c499e-112">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment.</span></span>
* <span data-ttu-id="c499e-113">Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde</span><span class="sxs-lookup"><span data-stu-id="c499e-113">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>


## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="c499e-114">In diesem Tutorial lernen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c499e-114">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c499e-115">Definieren von Quantum-Vorgängen in Q #</span><span class="sxs-lookup"><span data-stu-id="c499e-115">Define quantum operations in Q#</span></span>
> * <span data-ttu-id="c499e-116">F #-Vorgänge direkt über die Befehlszeile oder ein klassisches Host Programm abrufen</span><span class="sxs-lookup"><span data-stu-id="c499e-116">Call Q# operations directly from the command line or using a classical host program</span></span>
> * <span data-ttu-id="c499e-117">Simulieren eines Quantum-Vorgangs von der Qubit-Zuordnung zur Mess Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c499e-117">Simulate a quantum operation from qubit allocation to measurement output</span></span>
> * <span data-ttu-id="c499e-118">Beobachten Sie, wie sich die simulierte wavefunction des Quantum-Systems während des Vorgangs weiterentwickelt</span><span class="sxs-lookup"><span data-stu-id="c499e-118">Observe how the quantum system's simulated wavefunction evolves throughout the operation</span></span>

<span data-ttu-id="c499e-119">Das Ausführen eines Quantum-Programms mit dem Quantum Development Kit von Microsoft besteht in der Regel aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="c499e-119">Running a quantum program with Microsoft's Quantum Development Kit typically consists of two parts:</span></span>
1. <span data-ttu-id="c499e-120">Das Programm selbst, das mithilfe der Programmiersprache Q # Quantum implementiert wird und dann aufgerufen wird, um auf einem Quantum-Computer oder einem Quantum-Simulator ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-120">The program itself, which is implemented using the Q# quantum programming language, and then invoked to run on a quantum computer or quantum simulator.</span></span> <span data-ttu-id="c499e-121">Diese bestehen aus</span><span class="sxs-lookup"><span data-stu-id="c499e-121">These consist of</span></span> 
    - <span data-ttu-id="c499e-122">F #-Vorgänge: Unterroutinen, die in quantatenregistern agieren, und</span><span class="sxs-lookup"><span data-stu-id="c499e-122">Q# operations: subroutines acting on quantum registers, and</span></span> 
    - <span data-ttu-id="c499e-123">F #-Funktionen: klassische Unterroutinen, die innerhalb des Quantum-Algorithmus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-123">Q# functions: classical subroutines used within the quantum algorithm.</span></span>
2. <span data-ttu-id="c499e-124">Der Einstiegspunkt, der verwendet wird, um das Quantum-Programm aufzurufen und den Zielcomputer anzugeben, auf dem er ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c499e-124">The entry point used to call the quantum program and specify the target machine on which it should be run.</span></span>
    <span data-ttu-id="c499e-125">Dies kann direkt über die Befehlszeile oder über ein Host Programm erfolgen, das in einer klassischen Programmiersprache wie Python oder c# geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="c499e-125">This can be done directly from the command line, or through a host program written in a classical programming language like Python or C#.</span></span>
    <span data-ttu-id="c499e-126">Dieses Tutorial enthält Anweisungen für die gewünschte Methode.</span><span class="sxs-lookup"><span data-stu-id="c499e-126">This tutorial includes instructions for whichever method you prefer.</span></span>

## <a name="allocate-qubits-and-define-quantum-operations"></a><span data-ttu-id="c499e-127">Zuordnen von Qubits und Definieren von Quantum-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="c499e-127">Allocate qubits and define quantum operations</span></span>

<span data-ttu-id="c499e-128">Der erste Teil dieses Tutorials besteht darin, den Q #-Vorgang `Perform3qubitQFT` zu definieren, der die Quantum Fourier-Transformation auf drei Qubits ausführt.</span><span class="sxs-lookup"><span data-stu-id="c499e-128">The first part of this tutorial consists of defining the Q# operation `Perform3qubitQFT`, which performs the quantum Fourier transform on three qubits.</span></span> 

<span data-ttu-id="c499e-129">Außerdem verwenden wir die- [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) Funktion, um zu beobachten, wie sich die simulierte wavefunction unseres drei Qubit-Systems über den gesamten Vorgang hinweg weiterentwickelt.</span><span class="sxs-lookup"><span data-stu-id="c499e-129">In addition, we will use the [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) function to observe how the simulated wavefunction of our three qubit system evolves across the operation.</span></span>

<span data-ttu-id="c499e-130">Der erste Schritt besteht darin, das Q #-Projekt und die-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c499e-130">The first step is creating your Q# project and file.</span></span>
<span data-ttu-id="c499e-131">Die Schritte hierfür hängen von der Umgebung ab, die Sie zum Anrufen des Programms verwenden, und Sie finden die Details in den entsprechenden [Installations](xref:microsoft.quantum.install)Handbüchern.</span><span class="sxs-lookup"><span data-stu-id="c499e-131">The steps for this depend on the environment you will use to call the program, and you can find the details in the respective [installation guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="c499e-132">Wir führen Sie Schritt für Schritt durch die Komponenten der Datei. der Code ist jedoch auch als vollständige Block weiter unten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c499e-132">We will walk you through the components of the file step-by-step, but the code is also available as a full block below.</span></span>

### <a name="namespaces-to-access-other-q-operations"></a><span data-ttu-id="c499e-133">Namespaces für den Zugriff auf andere Q #-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c499e-133">Namespaces to access other Q# operations</span></span>
<span data-ttu-id="c499e-134">Innerhalb der Datei wird zunächst der Namespace definiert, `NamespaceQFT` auf den der Compiler zugreift.</span><span class="sxs-lookup"><span data-stu-id="c499e-134">Inside the file, we first define the namespace `NamespaceQFT` which will be accessed by the compiler.</span></span>
<span data-ttu-id="c499e-135">Damit der Vorgang vorhandene Q #-Vorgänge nutzen kann, öffnen wir die relevanten `Microsoft.Quantum.<>` Namespaces.</span><span class="sxs-lookup"><span data-stu-id="c499e-135">For our operation to make use of existing Q# operations, we open the relevant `Microsoft.Quantum.<>` namespaces.</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a><span data-ttu-id="c499e-136">Definieren von Vorgängen mit Argumenten und Rückgabe</span><span class="sxs-lookup"><span data-stu-id="c499e-136">Define operations with arguments and returns</span></span>
<span data-ttu-id="c499e-137">Als nächstes definieren wir den `Perform3qubitQFT` Vorgang:</span><span class="sxs-lookup"><span data-stu-id="c499e-137">Next, we define the `Perform3qubitQFT` operation:</span></span>

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

<span data-ttu-id="c499e-138">Der Vorgang nimmt vorerst keine Argumente an und gibt nichts zurück---in diesem Fall schreiben wir, dass Sie ein-Objekt zurückgibt `Unit` , das `void` in c# oder in einem leeren Tupel `Tuple[()]` in python ähnelt.</span><span class="sxs-lookup"><span data-stu-id="c499e-138">For now, the operation takes no arguments and does not return anything---in this case we write that it returns a `Unit` object, which is akin to `void` in C# or an empty tuple, `Tuple[()]`, in Python.</span></span>
<span data-ttu-id="c499e-139">Später werden wir Sie ändern, um ein Array von Messergebnissen zurückzugeben, an dem der Punkt `Unit` durch ersetzt wird `Result[]` .</span><span class="sxs-lookup"><span data-stu-id="c499e-139">Later, we will modify it to return an array of measurement results, at which point `Unit` will be replaced by `Result[]`.</span></span> 

### <a name="allocate-qubits-with-using"></a><span data-ttu-id="c499e-140">Zuordnen von Qubits mit`using`</span><span class="sxs-lookup"><span data-stu-id="c499e-140">Allocate qubits with `using`</span></span>
<span data-ttu-id="c499e-141">In unserem Q #-Vorgang weisen wir zuerst ein Register von drei Qubits mit der- `using` Anweisung zu:</span><span class="sxs-lookup"><span data-stu-id="c499e-141">Within our Q# operation, we first allocate a register of three qubits with the `using` statement:</span></span>

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

<span data-ttu-id="c499e-142">Bei `using` werden die Qubits automatisch im $ \ket {0} $-Status zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c499e-142">With `using`, the qubits are automatically allocated in the $\ket{0}$ state.</span></span> <span data-ttu-id="c499e-143">Wir können dies mithilfe von und überprüfen [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , wodurch eine Zeichenfolge und der aktuelle Zustand des Systems auf der Konsole gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-143">We can verify this by using [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) and [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine), which print a string and the system's current state to the console.</span></span>

> [!NOTE]
> <span data-ttu-id="c499e-144">Die `Message(<string>)` -Funktion und die- `DumpMachine()` Funktion (von [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) bzw.) werden beide direkt in der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="c499e-144">The `Message(<string>)` and `DumpMachine()` functions (from [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics), respectively) both print directly to the console.</span></span> <span data-ttu-id="c499e-145">Genau wie bei einer echten Quantum-Berechnung lässt Q # den direkten Zugriff auf Qubit-Zustände nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c499e-145">Just like a real quantum computation, Q# does not allow us to directly access qubit states.</span></span>
> <span data-ttu-id="c499e-146">`DumpMachine`Wenn jedoch den aktuellen Zustand des Ziel Computers ausgibt, kann er wertvolle Einblicke in das Debuggen und Erlernen von Informationen liefern, wenn er in Verbindung mit dem vollständigen Zustands Simulator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c499e-146">However, as `DumpMachine` prints the target machine's current state, it can provide valuable insight for debugging and learning when used in conjunction with the full state simulator.</span></span>


### <a name="applying-single-qubit-and-controlled-gates"></a><span data-ttu-id="c499e-147">Anwenden von Single-Qubit und kontrollierten Gates</span><span class="sxs-lookup"><span data-stu-id="c499e-147">Applying single-qubit and controlled gates</span></span>

<span data-ttu-id="c499e-148">Als nächstes wenden wir die Gates an, aus denen der Vorgang besteht.</span><span class="sxs-lookup"><span data-stu-id="c499e-148">Next, we apply the gates which comprise the operation itself.</span></span>
<span data-ttu-id="c499e-149">Q # enthält bereits viele grundlegende Quantum-Gates als Vorgänge im [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) -Namespace, und dies ist keine Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="c499e-149">Q# already contains many basic quantum gates as operations in the [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, and these are no exception.</span></span> 

<span data-ttu-id="c499e-150">In einem Q #-Vorgang werden die Anweisungen, die callables aufrufen, natürlich in sequenzieller Reihenfolge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c499e-150">Within a Q# operation, the statements invoking callables will of course be executed in sequential order.</span></span>
<span data-ttu-id="c499e-151">Daher ist das erste anzuwendende Gate der [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) zum ersten Qubit:</span><span class="sxs-lookup"><span data-stu-id="c499e-151">Hence, the first gate to apply is the [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) to the first qubit:</span></span>

<br/>
<img src="./qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

<span data-ttu-id="c499e-152">Um einen Vorgang auf ein bestimmtes Qubit aus einem Register (d. h. einem einzelnen `Qubit` aus einem Array) anzuwenden, `Qubit[]` verwenden wir die standardmäßige Index Notation.</span><span class="sxs-lookup"><span data-stu-id="c499e-152">To apply an operation to a specific qubit from a register (i.e. a single `Qubit` from an array `Qubit[]`) we use standard index notation.</span></span>
<span data-ttu-id="c499e-153">Daher hat das Anwenden [`H`](xref:microsoft.quantum.intrinsic.h) von auf das erste Qubit des Registers folgendes Format `qs` :</span><span class="sxs-lookup"><span data-stu-id="c499e-153">So, applying the [`H`](xref:microsoft.quantum.intrinsic.h) to the first qubit of our register `qs` takes the form:</span></span>

```qsharp
            H(qs[0]);
```

<span data-ttu-id="c499e-154">Neben dem Anwenden des- `H` Tors (Hadamard) auf einzelne Qubits besteht die QFT-Leitung hauptsächlich aus kontrollierten [`R1`](xref:microsoft.quantum.intrinsic.r1) Rotationen.</span><span class="sxs-lookup"><span data-stu-id="c499e-154">Besides applying the `H` (Hadamard) gate to individual qubits, the QFT circuit consists primarily of controlled [`R1`](xref:microsoft.quantum.intrinsic.r1) rotations.</span></span>
<span data-ttu-id="c499e-155">`R1(θ, <qubit>)`Bei einem Vorgang im Allgemeinen bleibt die $ \ket {0} $-Komponente des Qubit unverändert, während eine Rotation $e ^ {i\orta} $ auf die $ \ket $-Komponente angewendet wird {1} .</span><span class="sxs-lookup"><span data-stu-id="c499e-155">An `R1(θ, <qubit>)` operation in general leaves the $\ket{0}$ component of the qubit unchanged, while applying a rotation of $e^{i\theta}$ to the $\ket{1}$ component.</span></span>

#### <a name="controlled-operations"></a><span data-ttu-id="c499e-156">Kontrollierte Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c499e-156">Controlled operations</span></span>

<span data-ttu-id="c499e-157">F # macht es äußerst einfach, die Ausführung eines Vorgangs auf ein oder mehrere Steuerelement-Qubits zu bedinieren.</span><span class="sxs-lookup"><span data-stu-id="c499e-157">Q# makes it extremely easy to condition the execution of an operation upon one or multiple control qubits.</span></span>
<span data-ttu-id="c499e-158">Im Allgemeinen wird dem-Befehl lediglich `Controlled` vorangestellt, und die Vorgangs Argumente ändern sich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c499e-158">In general, we merely preface the call with `Controlled`, and the operation arguments change as:</span></span>

 <span data-ttu-id="c499e-159">`Op(<normal args>)`$ \bis $ `Controlled Op([<control qubits>], (<normal args>))` .</span><span class="sxs-lookup"><span data-stu-id="c499e-159">`Op(<normal args>)` $\to$ `Controlled Op([<control qubits>], (<normal args>))`.</span></span>

<span data-ttu-id="c499e-160">Beachten Sie, dass die Steuerelement-Qubits als Array bereitgestellt werden müssen, selbst wenn es sich um ein einzelnes Qubit handelt.</span><span class="sxs-lookup"><span data-stu-id="c499e-160">Note that the control qubits must be provided as an array, even if it is a single qubit.</span></span>

<span data-ttu-id="c499e-161">Nach dem `H` sehen wir, dass es sich bei den nächsten Gates um die Gates handelt, die `R1` auf dem ersten Qubit agieren (und durch das zweite/dritte gesteuert werden):</span><span class="sxs-lookup"><span data-stu-id="c499e-161">After the `H`, we see that the next gates are the `R1` gates acting on the first qubit (and controlled by the second/third):</span></span>

<br/>
<img src="./qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

<span data-ttu-id="c499e-162">Wir nennen diese mit</span><span class="sxs-lookup"><span data-stu-id="c499e-162">We call these with</span></span>

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

<span data-ttu-id="c499e-163">Beachten Sie, dass die- [`PI()`](xref:microsoft.quantum.math.pi) Funktion aus dem- [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) Namespace verwendet wird, um die Rotationen in Bezug auf Pi-radiane zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c499e-163">Note that we use the [`PI()`](xref:microsoft.quantum.math.pi) function from the [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace to define the rotations in terms of pi radians.</span></span>
<span data-ttu-id="c499e-164">Darüber hinaus dividieren wir durch einen `Double` (z. b. `2.0` ), da die Division durch eine ganze Zahl `2` einen Typfehler auslösen würde.</span><span class="sxs-lookup"><span data-stu-id="c499e-164">Additionally, we divide by a `Double` (e.g. `2.0`) because dividing by an integer `2` would throw a type error.</span></span> 

> [!TIP]
> <span data-ttu-id="c499e-165">`R1(π/2)`und `R1(π/4)` sind äquivalent zu den `S` -und- `T` Vorgängen (auch in `Microsoft.Quantum.Intrinsic` ).</span><span class="sxs-lookup"><span data-stu-id="c499e-165">`R1(π/2)` and `R1(π/4)` are equivalent to the `S` and `T` operations (also in `Microsoft.Quantum.Intrinsic`).</span></span>


<span data-ttu-id="c499e-166">Nach dem Anwenden der relevanten `H` Vorgänge und der kontrollierten Rotationen auf das zweite und dritte Qubits:</span><span class="sxs-lookup"><span data-stu-id="c499e-166">After applying the relevant `H` operations and controlled rotations to the second and third qubits:</span></span>

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

<span data-ttu-id="c499e-167">Wir müssen nur ein [`SWAP`](xref:microsoft.quantum.intrinsic.swap) Gate anwenden, um die Verbindung abzuschließen:</span><span class="sxs-lookup"><span data-stu-id="c499e-167">we need only apply a [`SWAP`](xref:microsoft.quantum.intrinsic.swap) gate to complete the circuit:</span></span>

```qsharp
            SWAP(qs[2], qs[0]);
```

<span data-ttu-id="c499e-168">Dies ist erforderlich, da die Natur der Quantum Fourier-Transformation die Qubits in umgekehrter Reihenfolge ausgibt, sodass die Austausch Vorgängen eine nahtlose Integration der Unterroutine in größere Algorithmen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c499e-168">This is necessary because the nature of the quantum Fourier transform outputs the qubits in reverse order, so the swaps allow for seamless integration of the subroutine into larger algorithms.</span></span>

<span data-ttu-id="c499e-169">Daher haben wir das Schreiben der Qubit-Level-Vorgänge der Quantum Fourier-Transformation in unseren f #-Vorgang abgeschlossen:</span><span class="sxs-lookup"><span data-stu-id="c499e-169">Hence we have finished writing the qubit-level operations of the quantum Fourier transform into our Q# operation:</span></span>

<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

<span data-ttu-id="c499e-170">Wir können ihn jedoch noch nicht an einem Tag anrufen.</span><span class="sxs-lookup"><span data-stu-id="c499e-170">However, we can't call it a day just yet.</span></span>
<span data-ttu-id="c499e-171">Unsere Qubits befanden sich im Status "$ \ket {0} $", als wir Sie zugewiesen haben, und ähnlich wie im Leben sollten wir in Q # die Dinge auf dieselbe Weise wie Sie gefunden haben (oder besser!).</span><span class="sxs-lookup"><span data-stu-id="c499e-171">Our qubits were in state $\ket{0}$ when we allocated them, and much like in life, in Q# we should leave things the same way we found them (or better!).</span></span>

### <a name="deallocate-qubits"></a><span data-ttu-id="c499e-172">Freigabe von Qubits aufgehoben</span><span class="sxs-lookup"><span data-stu-id="c499e-172">Deallocate qubits</span></span>

<span data-ttu-id="c499e-173">Wir [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) werden erneut aufgerufen, um den Zustand nach dem Betrieb anzuzeigen, und schließlich [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) auf das Qubit-Register angewendet, um die Qubits auf "$ \ket $" zurückzusetzen, {0} bevor der Vorgang abgeschlossen wird:</span><span class="sxs-lookup"><span data-stu-id="c499e-173">We call [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) again to see the post-operation state, and finally apply [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) to the qubit register to reset our qubits to $\ket{0}$ before completing the operation:</span></span>

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

<span data-ttu-id="c499e-174">Das festlegen, dass alle zugeordneten Qubits explizit auf "$ \ket $" festgelegt werden müssen {0} , ist eine grundlegende Funktion von Q #, da andere Vorgänge ihren Zustand genau erkennen können, wenn Sie mit der Verwendung der gleichen Qubits (knappe Ressource) beginnen.</span><span class="sxs-lookup"><span data-stu-id="c499e-174">Requiring that all deallocated qubits be explicitly set to $\ket{0}$ is a basic feature of Q#, as it allows other operations to know their state precisely when they begin using those same qubits (a scarce resource).</span></span>
<span data-ttu-id="c499e-175">Außerdem wird dadurch sichergestellt, dass Sie nicht mit anderen Qubits im System entkoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-175">Additionally, this assures that they not be entangled with any other qubits in the system.</span></span>
<span data-ttu-id="c499e-176">Wenn die zurück setzung am Ende eines `using` Zuordnungs Blocks nicht ausgeführt wird, wird ein Laufzeitfehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="c499e-176">If the reset is not performed at the end of a `using` allocation block, a runtime error will be thrown.</span></span>

<span data-ttu-id="c499e-177">Ihre vollständige f #-Datei sollte nun wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c499e-177">Your full Q# file should now look like this:</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


<span data-ttu-id="c499e-178">Wenn die f #-Datei und der Vorgang abgeschlossen sind, kann unser Quantum-Programm aufgerufen und simuliert werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-178">With the Q# file and operation complete, our quantum program is ready to be called and simulated.</span></span>

## <a name="execute-the-program"></a><span data-ttu-id="c499e-179">Programm ausführen</span><span class="sxs-lookup"><span data-stu-id="c499e-179">Execute the program</span></span>

<span data-ttu-id="c499e-180">Nachdem wir den Q #-Vorgang in einer Datei definiert haben `.qs` , müssen wir diesen Vorgang jetzt aufrufen und alle zurückgegebenen klassischen Daten beobachten.</span><span class="sxs-lookup"><span data-stu-id="c499e-180">Having defined our Q# operation in a `.qs` file, we now need to call that operation and observe any returned classical data.</span></span>
<span data-ttu-id="c499e-181">Zurzeit gibt es nichts zurückgegeben (Beachten Sie, dass der oben definierte Vorgang zurückgibt `Unit` ), doch wenn wir später den Q #-Vorgang ändern, um ein Array von Messergebnissen () zurückzugeben `Result[]` , wird dies behandelt.</span><span class="sxs-lookup"><span data-stu-id="c499e-181">For now, there isn't anything returned (recall that our operation defined above returns `Unit`), but when we later modify the Q# operation to return an array of measurement results (`Result[]`), we will address this.</span></span>

<span data-ttu-id="c499e-182">Wenngleich das Q #-Programm in den Umgebungen, in denen es aufgerufen wird, universell ist, ist die Vorgehensweise natürlich unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="c499e-182">While the Q# program is ubiquitous across the environments used to call it, the manner of doing so will of course vary.</span></span> <span data-ttu-id="c499e-183">Befolgen Sie daher einfach die Anweisungen auf der Registerkarte, die dem Setup entspricht: Arbeiten Sie mit der Befehlszeilen Anwendung "Q #" oder mit einem Host Programm in Python oder c#.</span><span class="sxs-lookup"><span data-stu-id="c499e-183">As such, simply follow the instructions in the tab corresponding to your setup: working from the Q# command line application or using a host program in Python or C#.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="c499e-184">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c499e-184">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="c499e-185">Wenn das q #-Programm über die Befehlszeile ausgeführt wird, ist nur eine kleine Änderung an der q #-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c499e-185">Running the Q# program from the command line requires only a small change to the Q# file.</span></span>

<span data-ttu-id="c499e-186">Fügen Sie einfach `@EntryPoint()` zu einer Zeile vor der Vorgangs Definition hinzu:</span><span class="sxs-lookup"><span data-stu-id="c499e-186">Simply add `@EntryPoint()` to a line preceding the operation definition:</span></span>

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

<span data-ttu-id="c499e-187">Um das Programm auszuführen, öffnen Sie das Terminal im Ordner des Projekts, und geben Sie ein.</span><span class="sxs-lookup"><span data-stu-id="c499e-187">To run the program, open the terminal in the folder of your project and enter</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="c499e-188">Bei der Ausführung sollten die `Message` `DumpMachine` Ausgaben und unten in der Konsole gedruckt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c499e-188">Upon execution, you should see the `Message` and `DumpMachine` outputs below printed in your console.</span></span>


#### <a name="python"></a>[<span data-ttu-id="c499e-189">Python</span><span class="sxs-lookup"><span data-stu-id="c499e-189">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="c499e-190">Erstellen Sie eine python-Hostdatei: `host.py` .</span><span class="sxs-lookup"><span data-stu-id="c499e-190">Create a Python host file: `host.py`.</span></span>

<span data-ttu-id="c499e-191">Die Hostdatei wird wie folgt erstellt:</span><span class="sxs-lookup"><span data-stu-id="c499e-191">The host file is constructed as follows:</span></span> 
1. <span data-ttu-id="c499e-192">Zuerst importieren wir das `qsharp` Modul, das das Modul Lade Modul für die Q #-Interoperabilität registriert.</span><span class="sxs-lookup"><span data-stu-id="c499e-192">First, we import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="c499e-193">Dadurch können q #-Namespaces (z. b. die `NamespaceQFT` in der Q #-Datei definierten) als Python-Module angezeigt werden, von denen wir q #-Vorgänge importieren können.</span><span class="sxs-lookup"><span data-stu-id="c499e-193">This allows Q# namespaces (e.g. the `NamespaceQFT` we defined in our Q# file) to appear as Python modules, from which we can import Q# operations.</span></span>
2. <span data-ttu-id="c499e-194">Importieren Sie dann die f #-Vorgänge, die wir direkt aufrufen---in diesem Fall `Perform3qubitQFT` .</span><span class="sxs-lookup"><span data-stu-id="c499e-194">Then, import the Q# operations which we will directly invoke---in this case, `Perform3qubitQFT`.</span></span>
    <span data-ttu-id="c499e-195">Wir müssen den Einstiegspunkt nur in ein Q #-Programm importieren (d. h. _keine_ Vorgänge wie `H` und `R1` , die von anderen Q #-Vorgängen, aber nie vom klassischen Host aufgerufen werden).</span><span class="sxs-lookup"><span data-stu-id="c499e-195">We need only import the entry point into a Q# program (i.e. _not_ operations like `H` and `R1`, which are called by other Q# operations but never by the classical host).</span></span>
3. <span data-ttu-id="c499e-196">Verwenden Sie beim Simulieren von f #-Vorgängen oder-Funktionen das Formular, `<Q#callable>.simulate(<args>)` um Sie auf dem `QuantumSimulator()` Zielcomputer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c499e-196">In simulating Q# operations or functions, use the form `<Q#callable>.simulate(<args>)` to run them on the `QuantumSimulator()` target machine.</span></span> 

> [!NOTE]
> <span data-ttu-id="c499e-197">Wenn der Vorgang auf einem anderen Computer aufgerufen werden soll, z `ResourceEstimator()` . b., verwenden wir einfach `<Q#callable>.estimate_resources(<args>)` .</span><span class="sxs-lookup"><span data-stu-id="c499e-197">If we wanted to call the operation on a different machine, for example the `ResourceEstimator()`, we would simply use `<Q#callable>.estimate_resources(<args>)`.</span></span>
> <span data-ttu-id="c499e-198">Im Allgemeinen sind Q #-Vorgänge auf den Computern, auf denen Sie ausgeführt werden, agnostisch, einige Features wie können sich jedoch unter `DumpMachine` schiedlich Verhalten.</span><span class="sxs-lookup"><span data-stu-id="c499e-198">In general, Q# operations are agnostic to the machines on which they're run, but some features such as `DumpMachine` may behave differently.</span></span>

4. <span data-ttu-id="c499e-199">Beim Ausführen der Simulation gibt der Vorgangs Aufrufwert Werte zurück, die in der Q #-Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c499e-199">Upon performing the simulation, the operation call will return values as defined in the Q# file.</span></span>
    <span data-ttu-id="c499e-200">Vorerst wird nichts zurückgegeben, aber später wird ein Beispiel für das zuweisen und Verarbeiten dieser Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c499e-200">For now there is nothing returned, but later on we will see an example of assigning and processing these values.</span></span>
    <span data-ttu-id="c499e-201">Wenn sich die resultierenden Daten in unserer Praxis und ganz klassisch befinden, können wir mit Ihnen alles tun, was wir wollen.</span><span class="sxs-lookup"><span data-stu-id="c499e-201">With the resultant data in our hands and totally classical, we can do whatever we'd like with it.</span></span>

<span data-ttu-id="c499e-202">Die vollständige `host.py` Datei sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="c499e-202">Your full `host.py` file should be this:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

<span data-ttu-id="c499e-203">Wenn Sie die python-Datei ausführen und in der Konsole gedruckt werden, sollten die `Message` Ausgaben und unten angezeigt werden `DumpMachine` .</span><span class="sxs-lookup"><span data-stu-id="c499e-203">Run the Python file, and printed in your console you should see the `Message` and `DumpMachine` outputs below.</span></span> 


#### <a name="c"></a>[<span data-ttu-id="c499e-204">C#</span><span class="sxs-lookup"><span data-stu-id="c499e-204">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="c499e-205">Befolgen Sie die Anweisungen im [Installationshandbuch](xref:microsoft.quantum.install.cs), erstellen Sie eine c#-Hostdatei, und benennen Sie Sie in um `host.cs` .</span><span class="sxs-lookup"><span data-stu-id="c499e-205">Following the same instructions as in the [install guide](xref:microsoft.quantum.install.cs), create a C# host file, and rename it to `host.cs`.</span></span>

<span data-ttu-id="c499e-206">Der c#-Host besteht aus vier Teilen:</span><span class="sxs-lookup"><span data-stu-id="c499e-206">The C# host has four parts:</span></span>
1. <span data-ttu-id="c499e-207">Konstruieren eines Quantensimulators.</span><span class="sxs-lookup"><span data-stu-id="c499e-207">Construct a quantum simulator.</span></span>
    <span data-ttu-id="c499e-208">Im folgenden Code ist dies die Variable `qsim` .</span><span class="sxs-lookup"><span data-stu-id="c499e-208">In the code below, this is the variable `qsim`.</span></span>
2. <span data-ttu-id="c499e-209">Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c499e-209">Compute any arguments required for the quantum algorithm.</span></span>
    <span data-ttu-id="c499e-210">In diesem Beispiel gibt es keine.</span><span class="sxs-lookup"><span data-stu-id="c499e-210">There are none in this example.</span></span>
3. <span data-ttu-id="c499e-211">Ausführen des Quantenalgorithmus.</span><span class="sxs-lookup"><span data-stu-id="c499e-211">Run the quantum algorithm.</span></span> 
    <span data-ttu-id="c499e-212">Jede Q#-Operation generiert eine C#-Klasse gleichen Namens.</span><span class="sxs-lookup"><span data-stu-id="c499e-212">Each Q# operation generates a C# class with the same name.</span></span> 
    <span data-ttu-id="c499e-213">Diese Klasse weist eine `Run`-Methode auf, die die Operation **asynchron** ausführt.</span><span class="sxs-lookup"><span data-stu-id="c499e-213">This class has a `Run` method that **asynchronously** executes the operation.</span></span>
    <span data-ttu-id="c499e-214">Die Ausführung ist asynchron, weil die Ausführung auf realer Hardware asynchron ist.</span><span class="sxs-lookup"><span data-stu-id="c499e-214">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> 
    <span data-ttu-id="c499e-215">Da die- `Run` Methode asynchron ist, wird die- `Wait()` Methode aufgerufen. Dadurch wird die Ausführung blockiert, bis die Aufgabe abgeschlossen ist, und das Ergebnis synchron zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c499e-215">Because the `Run` method is asynchronous, we call the `Wait()` method; this blocks execution until the task completes and returns the result synchronously.</span></span> 
4. <span data-ttu-id="c499e-216">Verarbeiten Sie das zurückgegebene Ergebnis des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c499e-216">Process the returned result of the operation.</span></span>
    <span data-ttu-id="c499e-217">Vorerst gibt der Vorgang nichts zurück.</span><span class="sxs-lookup"><span data-stu-id="c499e-217">For now, the operation returns nothing.</span></span>


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
<span data-ttu-id="c499e-218">Führen Sie die Anwendung aus, und die Ausgabe sollte der folgenden Abbildung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c499e-218">Run the application, and your output should match that below.</span></span>
<span data-ttu-id="c499e-219">Das Programm wird beendet, nachdem Sie eine Taste drücken.</span><span class="sxs-lookup"><span data-stu-id="c499e-219">The program will exit after you press a key.</span></span>
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

<span data-ttu-id="c499e-220">Wenn Sie im vollständigen Simulator aufgerufen wird, `DumpMachine()` stellt diese ungendarstellungen der wavefunction des Quantum State bereit.</span><span class="sxs-lookup"><span data-stu-id="c499e-220">When called on the full-state simulator, `DumpMachine()` provides these mutliple representations of the quantum state's wavefunction.</span></span> <span data-ttu-id="c499e-221">Die möglichen Zustände eines $n $-Qubit-Systems können durch die Zustände "$ 2 ^ n $ Compute" dargestellt werden, die jeweils über einen entsprechenden komplexen Koeffizienten verfügen (einfach eine Amplitude und eine Phase).</span><span class="sxs-lookup"><span data-stu-id="c499e-221">The possible states of an $n$-qubit system can be represented by $2^n$ computational basis states, each with a corresponding complex coefficient (simply an amplitude and a phase).</span></span>
<span data-ttu-id="c499e-222">Die Berechnungs Zustände entsprechen allen möglichen binären Zeichen folgen der Länge $n $---d. h. alle möglichen Kombinationen aus Qubit-Zuständen $ \ket {0} $ und $ \ket {1} $, wobei jede binäre Ziffer einem einzelnen Qubit entspricht.</span><span class="sxs-lookup"><span data-stu-id="c499e-222">The computational basis states correspond to all the possible binary strings of length $n$---that is, all the possible combinations of qubit states $\ket{0}$ and $\ket{1}$, where each binary digit corresponds to an individual qubit.</span></span>

<span data-ttu-id="c499e-223">Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c499e-223">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="c499e-224">Qubit `2` ist die "größte Bedeutung", d. h., dass in der binären Darstellung von "Basis Zustands Vektor $ \ket{i} $" der Status von Qubit `2` der äußersten linken Ziffer entspricht.</span><span class="sxs-lookup"><span data-stu-id="c499e-224">Qubit `2` being the "most significant" simply means that in the binary representation of basis state vector $\ket{i}$, the state of qubit `2` corresponds to the left-most digit.</span></span> <span data-ttu-id="c499e-225">Beispiel: $ \ket {6} = \ket {110} $ umfasst Qubits `2` und in `1` $ \ket {1} $ und Qubit `0` in $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="c499e-225">For example, $\ket{6} = \ket{110}$ comprises qubits `2` and `1` both in $\ket{1}$ and qubit `0` in $\ket{0}$.</span></span>


<span data-ttu-id="c499e-226">In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{i} $ im kartesischen und Polar Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c499e-226">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{i}$ in both Cartesian and polar formats.</span></span>
<span data-ttu-id="c499e-227">Im Detail für die erste Zeile des Eingabe Zustands $ \ket {000} $:</span><span class="sxs-lookup"><span data-stu-id="c499e-227">In detail for the first row of our input state $\ket{000}$:</span></span>
* <span data-ttu-id="c499e-228">**`|0>:`** Diese Zeile entspricht dem `0` Status "computebasis" (da der anfängliche Status nach der Zuordnung "$ \ket $" war {000} , erwartet wir, dass dies der einzige Zustand mit Wahrscheinlichkeits Amplitude an diesem Punkt ist).</span><span class="sxs-lookup"><span data-stu-id="c499e-228">**`|0>:`** this row corresponds to the `0` computational basis state (given that our initial state post-allocation was $\ket{000}$, we would expect this to be the only state with probability amplitude at this point).</span></span>
* <span data-ttu-id="c499e-229">**`1.000000 +  0.000000 i`**: die Wahrscheinlichkeits Amplitude im kartesischen Format.</span><span class="sxs-lookup"><span data-stu-id="c499e-229">**`1.000000 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="c499e-230">**` == `**: das `equal` Vorzeichen trennt beide äquivalente Darstellungen.</span><span class="sxs-lookup"><span data-stu-id="c499e-230">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="c499e-231">**`********************`**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.</span><span class="sxs-lookup"><span data-stu-id="c499e-231">**`********************`**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span> 
* <span data-ttu-id="c499e-232">**`[ 1.000000 ]`**: der numerische Wert der Größe.</span><span class="sxs-lookup"><span data-stu-id="c499e-232">**`[ 1.000000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="c499e-233">**`    ---`**: Eine grafische Darstellung der Amplitude-Phase.</span><span class="sxs-lookup"><span data-stu-id="c499e-233">**`    ---`**: A graphical representation of the amplitude's phase.</span></span>
* <span data-ttu-id="c499e-234">**`[ 0.0000 rad ]`**: der numerische Wert der Phase (im Bogenmaße).</span><span class="sxs-lookup"><span data-stu-id="c499e-234">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="c499e-235">Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c499e-235">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="c499e-236">Die Größen Darstellung ist einfach: Sie zeigt einen Balken an `*` , und je höher die Wahrscheinlichkeit ist, desto größer ist der Balken.</span><span class="sxs-lookup"><span data-stu-id="c499e-236">The magnitude representation is straightforward: it shows a bar of `*`, and the higher the probability, the larger the bar will be.</span></span> <span data-ttu-id="c499e-237">Informationen zu den einzelnen Phasen finden Sie unter [Testen und Debuggen: Dumpfunktionen](xref:microsoft.quantum.guide.testingdebugging#dump-functions) für die möglichen Symbol Darstellungen auf der Grundlage von Winkel Bereichen.</span><span class="sxs-lookup"><span data-stu-id="c499e-237">For the phase, see [Testing and debugging: dump functions](xref:microsoft.quantum.guide.testingdebugging#dump-functions) for the possible symbol representations based on angle ranges.</span></span>


<span data-ttu-id="c499e-238">Die gedruckte Ausgabe zeigt also, dass unsere programmierten Gates unseren Zustand von</span><span class="sxs-lookup"><span data-stu-id="c499e-238">So, the printed output is illustrating that our programmed gates transformed our state from</span></span>

<span data-ttu-id="c499e-239">$ $ \ket{\psi} \_ {Initial} = \ket {000} $ $</span><span class="sxs-lookup"><span data-stu-id="c499e-239">$$ \ket{\psi}\_{initial} = \ket{000} $$</span></span>

<span data-ttu-id="c499e-240">zu</span><span class="sxs-lookup"><span data-stu-id="c499e-240">to</span></span> 

<span data-ttu-id="c499e-241">$ $ \begin{align} \ket{\psi} \_ {Final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="c499e-241">$$ \begin{align} \ket{\psi}\_{final} &= \frac{1}{\sqrt{8}} \left( \ket{000} + \ket{001} + \ket{010} + \ket{011} + \ket{100} + \ket{101} + \ket{110} + \ket{111}  \right) \\\\ &= \frac{1}{\sqrt{2^n}}\sum\_{j=0}^{2^n-1} \ket{j}, \end{align} $$</span></span>

<span data-ttu-id="c499e-242">Dabei handelt es sich genau um das Verhalten der 3-Qubit-Fourier-Transformation.</span><span class="sxs-lookup"><span data-stu-id="c499e-242">which is precisely the behavior of the 3-qubit Fourier transform.</span></span> 

<span data-ttu-id="c499e-243">Wenn Sie neugierig sind, wie andere Eingabe Zustände betroffen sind, empfehlen wir Ihnen, mit der Anwendung von Qubit-Vorgängen vor der Transformation zu experimentieren.</span><span class="sxs-lookup"><span data-stu-id="c499e-243">If you are curious about how other input states are affected, we encourage you to play around with applying qubit operations before the transform.</span></span>

## <a name="adding-measurements"></a><span data-ttu-id="c499e-244">Hinzufügen von Messungen</span><span class="sxs-lookup"><span data-stu-id="c499e-244">Adding measurements</span></span>

<span data-ttu-id="c499e-245">Leider weist ein Eckpfeiler der Quantum-Mechanik darauf hin, dass ein reales Quantum-System nicht über eine solche Funktion verfügen kann `DumpMachine` .</span><span class="sxs-lookup"><span data-stu-id="c499e-245">Unfortunately, a cornerstone of quantum mechanics tells us that a real quantum system cannot have such a `DumpMachine` function.</span></span> <span data-ttu-id="c499e-246">Stattdessen sind wir gezwungen, Informationen durch Messungen zu extrahieren, was im Allgemeinen nicht nur den vollständigen Quantum-Status bereitstellt, sondern auch das System selbst drastisch verändern kann.</span><span class="sxs-lookup"><span data-stu-id="c499e-246">Instead, we're forced to extract information through measurements, which in general not only fail to provide us the full quantum state, but can also drastically alter the system itself.</span></span>
<span data-ttu-id="c499e-247">Es gibt viele Arten von Quantum-Messungen, aber wir konzentrieren uns auf die grundlegendsten: Projective Messungen in einzelnen Qubits.</span><span class="sxs-lookup"><span data-stu-id="c499e-247">There are many sorts of quantum measurements, but we will focus on the most basic: projective measurements on single qubits.</span></span>
<span data-ttu-id="c499e-248">Bei der Messung (z. b. der Berechnungsbasis $ \{ \ket {0} , \ket {1} \} $) wird der Qubit-Zustand auf den jeweiligen Basisstatus projiziert,---daher jede übergeordnete Position zwischen den beiden zerstört.</span><span class="sxs-lookup"><span data-stu-id="c499e-248">Upon measurement in a given basis (e.g. the computational basis $ \{ \ket{0}, \ket{1} \} $), the qubit state is projected onto whichever basis state was measured---hence destroying any superposition between the two.</span></span>

<span data-ttu-id="c499e-249">Zum Implementieren von Messungen in einem Q #-Programm verwenden wir den- `M` Vorgang (from `Microsoft.Quantum.Intrinsic` ), der einen-Typ zurückgibt `Result` .</span><span class="sxs-lookup"><span data-stu-id="c499e-249">To implement measurements within a Q# program, we use the `M` operation (from `Microsoft.Quantum.Intrinsic`), which returns a `Result` type.</span></span>

<span data-ttu-id="c499e-250">Zuerst wird der Vorgang so geändert, dass `Perform3QubitQFT` ein Array von Messergebnissen, `Result[]` , anstelle von zurückgegeben wird `Unit` .</span><span class="sxs-lookup"><span data-stu-id="c499e-250">First, we modify our `Perform3QubitQFT` operation to return an array of measurement results, `Result[]`, instead of `Unit`.</span></span>

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a><span data-ttu-id="c499e-251">Array definieren und initialisieren `Result[]`</span><span class="sxs-lookup"><span data-stu-id="c499e-251">Define and initialize `Result[]` array</span></span>

<span data-ttu-id="c499e-252">Vor der Zuweisung von Qubits (d.h. vor der- `using` Anweisung) deklarieren und binden wir dieses length-3-Array (eines `Result` für jedes Qubit):</span><span class="sxs-lookup"><span data-stu-id="c499e-252">Before even allocating qubits (i.e. before the `using` statement), we declare and bind this length-3 array (one `Result` for each qubit):</span></span> 

```qsharp
        mutable resultArray = new Result[3];
```

<span data-ttu-id="c499e-253">Mit dem- `mutable` Schlüsselwort, das mit der vorangestellt `resultArray` ist, kann die Variable später im Code wieder aufgefüllt werden---beispielsweise beim Hinzufügen unserer Messergebnisse.</span><span class="sxs-lookup"><span data-stu-id="c499e-253">The `mutable` keyword prefacing `resultArray` allows the variable to be rebound later in the code---for example, when adding our measurement results.</span></span>

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a><span data-ttu-id="c499e-254">Ausführen von Messungen in einer `for` Schleife und Hinzufügen von Ergebnissen zu einem Array</span><span class="sxs-lookup"><span data-stu-id="c499e-254">Perform measurements in a `for` loop and add results to array</span></span>

<span data-ttu-id="c499e-255">Fügen Sie nach den Fourier Transform-Vorgängen innerhalb des- `using` Blocks den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="c499e-255">After the Fourier transform operations inside the `using` block, insert the following code:</span></span>

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
<span data-ttu-id="c499e-256">Die [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) Funktion, die für ein Array (z. b. unser Array von Qubits) aufgerufen wird, `qs` gibt einen Bereich über die Indizes des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="c499e-256">The [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) function called on an array (e.g. our array of qubits, `qs`) returns a range over the indices of the array.</span></span> <span data-ttu-id="c499e-257">Hier verwenden wir Sie in unserer `for` Schleife, um jedes Qubit mithilfe der-Anweisung sequenziell zu messen `M(qs[i])` .</span><span class="sxs-lookup"><span data-stu-id="c499e-257">Here, we use it in our `for` loop to sequentially measure each qubit using the `M(qs[i])` statement.</span></span>
<span data-ttu-id="c499e-258">Jeder gemessene `Result` Typ (entweder `Zero` oder `One` ) wird dann der entsprechenden Indexposition in `resultArray` mit einer Update-and-REASSIGN-Anweisung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c499e-258">Each measured `Result` type (either `Zero` or `One`) is then added to the corresponding index position in `resultArray` with an update-and-reassign statement.</span></span>

> [!NOTE]
> <span data-ttu-id="c499e-259">Die Syntax dieser Anweisung ist für Q # eindeutig, entspricht jedoch der ähnlichen Variablen Neuzuweisung `resultArray[i] <- M(qs[i])` in anderen Sprachen, wie z. b. F # und R.</span><span class="sxs-lookup"><span data-stu-id="c499e-259">The syntax of this statement is unique to Q#, but corresponds to the similar variable reassignment `resultArray[i] <- M(qs[i])` seen in other languages such as F# and R.</span></span>

<span data-ttu-id="c499e-260">Das-Schlüsselwort `set` wird immer zum erneuten Zuweisen von Variablen verwendet, die mit gebunden sind `mutable` .</span><span class="sxs-lookup"><span data-stu-id="c499e-260">The keyword `set` is always used to reassign variables bound using `mutable`.</span></span>

#### <a name="return-resultarray"></a><span data-ttu-id="c499e-261">Hre`resultArray`</span><span class="sxs-lookup"><span data-stu-id="c499e-261">Return `resultArray`</span></span>

<span data-ttu-id="c499e-262">Wenn alle drei Qubits gemessen werden und die Ergebnisse zu hinzugefügt `resultArray` wurden, ist es sicher, die Qubits wie zuvor zurückzusetzen und deren Zuteilung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="c499e-262">With all three qubits measured and the results added to `resultArray`, we are safe to reset and deallocate the qubits as before.</span></span>
<span data-ttu-id="c499e-263">Fügen Sie nach dem Schließen des Blocks ein. `using`</span><span class="sxs-lookup"><span data-stu-id="c499e-263">After the `using` block's close, insert</span></span>

```qsharp
        return resultArray;
```
<span data-ttu-id="c499e-264">, wenn die Ausgabe des Vorgangs letztendlich zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="c499e-264">to ultimately return the output of our operation.</span></span> 

### <a name="understanding-the-effects-of-measurement"></a><span data-ttu-id="c499e-265">Grundlegendes zu den Auswirkungen der Messung</span><span class="sxs-lookup"><span data-stu-id="c499e-265">Understanding the effects of measurement</span></span>

<span data-ttu-id="c499e-266">Ändern wir nun die Platzierung unserer `DumpMachine` Funktionen, um den Zustand vor und nach den Messungen auszugeben.</span><span class="sxs-lookup"><span data-stu-id="c499e-266">Let's change the placement of our `DumpMachine` functions to output the state before and after the measurements.</span></span>
<span data-ttu-id="c499e-267">Der endgültige Vorgangs Code sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c499e-267">The final operation code should look like:</span></span> 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

<span data-ttu-id="c499e-268">Wenn Sie von der Befehlszeile aus arbeiten, wird das zurückgegebene Array am Ende der Ausführung einfach direkt in der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="c499e-268">If you are working from the command line, the returned array will simply be printed directly to the console at the end of the execution.</span></span>
<span data-ttu-id="c499e-269">Aktualisieren Sie andernfalls das Host Programm, um das zurückgegebene Array zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c499e-269">Otherwise, update your host program to process the returned array.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="c499e-270">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c499e-270">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="c499e-271">Um mehr über das zurückgegebene Array zu erfahren, das in der Konsole gedruckt wird, können wir eine weitere `Message` in der Q #-Datei direkt vor der-Anweisung hinzufügen `return` :</span><span class="sxs-lookup"><span data-stu-id="c499e-271">To have more understanding of the returned array which will be printed in the console, we can add another `Message` in the Q# file just before the `return` statement:</span></span>

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

<span data-ttu-id="c499e-272">Führen Sie das Projekt aus, und die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c499e-272">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[<span data-ttu-id="c499e-273">Python</span><span class="sxs-lookup"><span data-stu-id="c499e-273">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="c499e-274">Aktualisieren Sie das Python-Programm wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c499e-274">Update your Python program to the following:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

<span data-ttu-id="c499e-275">Führen Sie die Datei aus, und die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c499e-275">Run the file, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[<span data-ttu-id="c499e-276">C#</span><span class="sxs-lookup"><span data-stu-id="c499e-276">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="c499e-277">Nachdem der Vorgang nun ein Ergebnis zurückgegeben hat, ersetzen Sie den-Methodenaufrufe `Wait()` durch Abrufen der- `Result` Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c499e-277">Now that our operation is returning a result, replace the method call `Wait()` with fetching the `Result` property.</span></span> <span data-ttu-id="c499e-278">Dadurch wird immer noch die gleiche Synchronisierung erzielt, die bereits erläutert wurde, und wir können diesen Wert direkt an die Variable binden `measurementResult` .</span><span class="sxs-lookup"><span data-stu-id="c499e-278">This still accomplishes the same synchronicity discussed earlier, and we can directly bind this value to the variable `measurementResult`.</span></span>

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="c499e-279">Führen Sie das Projekt aus, und die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="c499e-279">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

<span data-ttu-id="c499e-280">Diese Ausgabe veranschaulicht einige verschiedene Dinge:</span><span class="sxs-lookup"><span data-stu-id="c499e-280">This output illustrates a few different things:</span></span>
1. <span data-ttu-id="c499e-281">Wenn Sie das zurückgegebene Ergebnis mit der prämessung vergleichen `DumpMachine` , wird die Post-QFT-Superposition in den Basis Zuständen eindeutig _nicht_ veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c499e-281">Comparing the returned result to the pre-measurement `DumpMachine`, it clearly does _not_ illustrate the post-QFT superposition over basis states.</span></span>
    <span data-ttu-id="c499e-282">Eine Messung gibt nur einen einzelnen Basiszustand zurück, wobei eine Wahrscheinlichkeit von der Amplitude dieses Zustands in der wavefunction des Systems bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="c499e-282">A measurement only returns a single basis state, with a probability determined by the amplitude of that state in the system's wavefunction.</span></span>
2. <span data-ttu-id="c499e-283">Aus dem nach Maß der Messung `DumpMachine` sehen wir, dass die Messung den Zustand selbst _ändert_ und ihn von der anfänglichen übergeordneten Position über die Basiszustände in den einzelnen Basisstatus projiziert, der dem gemessenen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="c499e-283">From the post-measurement `DumpMachine`, we see that measurement _changes_ the state itself, projecting it from the initial superposition over basis states to the single basis state that corresponds to the measured value.</span></span>

<span data-ttu-id="c499e-284">Wenn wir diesen Vorgang mehrmals wiederholen, sehen wir, dass die Ergebnis Statistik beginnt, um die gleich gewichtete Superposition des postqft-Zustands zu veranschaulichen, die zu einem zufälligen Ergebnis bei jedem Screenshot führt.</span><span class="sxs-lookup"><span data-stu-id="c499e-284">If we were to repeat this operation many times, we would see the result statistics begin to illustrate the equally weighted superposition of the post-QFT state that gives rise to a random result on each shot.</span></span>
<span data-ttu-id="c499e-285">Da es _jedoch_nicht ineffizient und immer noch unvollständig ist, würde dies trotzdem nur die relativen Verstärkung der Basiszustände reproduzieren, nicht die relativen Phasen zwischen diesen.</span><span class="sxs-lookup"><span data-stu-id="c499e-285">_However_, besides being inefficient and still imperfect, this would nevertheless only reproduce the relative amplitudes of the basis states, not the relative phases between them.</span></span>
<span data-ttu-id="c499e-286">Letzteres stellt in diesem Beispiel kein Problem dar. es werden jedoch relative Phasen angezeigt, wenn eine komplexere Eingabe für die QFT als $ \ket {000} $ vorliegt.</span><span class="sxs-lookup"><span data-stu-id="c499e-286">The latter is not an issue in this example, but we would see relative phases appear if given a more complex input to the QFT than $\ket{000}$.</span></span>

#### <a name="partial-measurements"></a><span data-ttu-id="c499e-287">Partielle Messungen</span><span class="sxs-lookup"><span data-stu-id="c499e-287">Partial measurements</span></span> 
<span data-ttu-id="c499e-288">Wenn Sie untersuchen möchten, wie sich die Messung nur einiger Qubits des Registers auf den Zustand des Systems auswirken kann, versuchen Sie `for` , nach der Maßeinheit Folgendes in der Schleife hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="c499e-288">To explore how measuring only some qubits of the register can affect the system's state, try adding the following inside the `for` loop, after the measurement line:</span></span>
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

<span data-ttu-id="c499e-289">Beachten Sie, dass Sie für den Zugriff auf die `IntAsString` Funktion Folgendes hinzufügen müssen:</span><span class="sxs-lookup"><span data-stu-id="c499e-289">Note that to access the `IntAsString` function you will have to add</span></span> 
```qsharp
    open Microsoft.Quantum.Convert;
```
<span data-ttu-id="c499e-290">mit den restlichen Namespace- `open` Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="c499e-290">with the rest of the namespace `open` statements.</span></span>

<span data-ttu-id="c499e-291">In der resultierenden Ausgabe wird die schrittweise Projektion in Teilbereiche angezeigt, wenn jedes Qubit gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="c499e-291">In the resulting output, you will see the gradual projection into subspaces as each qubit is measured.</span></span>


## <a name="use-the-q-libraries"></a><span data-ttu-id="c499e-292">Verwenden der Q #-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="c499e-292">Use the Q# libraries</span></span>
<span data-ttu-id="c499e-293">Wie in der Einführung erwähnt, liegt viel von den f #-Leistungsfähigkeit darin, dass es Ihnen ermöglicht, die sorgen für den Umgang mit einzelnen Qubits zu abstrahieren.</span><span class="sxs-lookup"><span data-stu-id="c499e-293">As we mentioned in the introduction, much of Q#'s power rests in the fact that it allows you to abstract-away the worries of dealing with individual qubits.</span></span>
<span data-ttu-id="c499e-294">Wenn Sie vollständige, anwendbare Quantum-Programme entwickeln möchten, müssen Sie sich Gedanken darüber machen, ob ein `H` Vorgang vor oder nach einer bestimmten Drehung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="c499e-294">Indeed, if you want to develop full-scale, applicable quantum programs, worrying about whether an `H` operation goes before or after a particular rotation would only slow you down.</span></span> 

<span data-ttu-id="c499e-295">Die Q #-Bibliotheken enthalten den [QFT](xref:microsoft.quantum.canon.qft) -Vorgang, den Sie einfach ausführen und auf eine beliebige Anzahl von Qubits anwenden können.</span><span class="sxs-lookup"><span data-stu-id="c499e-295">The Q# libraries contain the [QFT](xref:microsoft.quantum.canon.qft) operation, which you can simply take and apply for any number of qubits.</span></span>
<span data-ttu-id="c499e-296">Um es auszuprobieren, definieren Sie einen neuen Vorgang in der Q #-Datei, der denselben Inhalt von aufweist. `Perform3QubitQFT` allerdings ist alles vom ersten `H` bis zum `SWAP` Ersetzen durch zwei einfache Zeilen:</span><span class="sxs-lookup"><span data-stu-id="c499e-296">To give it a try, define a new operation in your Q# file which has the same contents of `Perform3QubitQFT`, but with everything from the first `H` to the `SWAP` replaced by two easy lines:</span></span>
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
<span data-ttu-id="c499e-297">In der ersten Zeile wird einfach ein- [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) Ausdruck des zugeordneten Arrays von Qubits erstellt, `qs` was der [QFT](xref:microsoft.quantum.canon.qft) -Vorgang als Argument annimmt.</span><span class="sxs-lookup"><span data-stu-id="c499e-297">The first line simply creates a [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expression of the allocated array of qubits, `qs`, which is what the [QFT](xref:microsoft.quantum.canon.qft) operation takes as an argument.</span></span>
<span data-ttu-id="c499e-298">Dies entspricht der Index Reihenfolge der Qubits im Register.</span><span class="sxs-lookup"><span data-stu-id="c499e-298">This corresponds to index ordering of the qubits in the register.</span></span>

<span data-ttu-id="c499e-299">Um Zugriff auf diese Vorgänge zu erhalten, fügen Sie `open` am Anfang der Q #-Datei-Anweisungen für ihre jeweiligen Namespaces hinzu:</span><span class="sxs-lookup"><span data-stu-id="c499e-299">To have access to these operations, add `open` statements for their respective namespaces at the beginning of the Q# file:</span></span>
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

<span data-ttu-id="c499e-300">Passen Sie nun das Host Programm so an, dass der Name des neuen Vorgangs (z. b. `PerformIntrinsicQFT` ) aufgerufen wird, und fügen Sie ihm einen Leerraum hinzu.</span><span class="sxs-lookup"><span data-stu-id="c499e-300">Now, adjust your host program to call the name of your new operation (e.g. `PerformIntrinsicQFT`), and give it a whirl.</span></span>

<span data-ttu-id="c499e-301">Um den tatsächlichen Vorteil der Verwendung der Q #-Bibliotheks Vorgänge anzuzeigen, ändern Sie die Anzahl der Qubits in einen anderen Wert als `3` :</span><span class="sxs-lookup"><span data-stu-id="c499e-301">To see the real benefit of using the Q# library operations, change the number of qubits to something other than `3`:</span></span>
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
<span data-ttu-id="c499e-302">Auf diese Weise können Sie den richtigen QFT für eine beliebige Anzahl von Qubits anwenden, ohne sich Gedanken über das Durcheinander neuer `H` Vorgänge und Rotationen für jedes Qubit machen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="c499e-302">You can thus apply the proper QFT for any given number of qubits, without having to worry about the mess of new `H` operations and rotations on each qubit.</span></span>

<span data-ttu-id="c499e-303">Beachten Sie, dass der Quantum-Simulator exponentiell mehr Zeit benötigt, wenn Sie die Anzahl der Qubits erhöhen---genau warum wir uns auf echte Quantum-Hardware freuen!</span><span class="sxs-lookup"><span data-stu-id="c499e-303">Note that the quantum simulator takes exponentially more time to run as you increase the number of qubits---precisely why we look forward to real quantum hardware!</span></span>













