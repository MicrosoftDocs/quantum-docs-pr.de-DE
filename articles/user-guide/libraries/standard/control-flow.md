---
title: 'Fluss Steuerungen in den Q# standardmäßigen libararies'
description: 'Erfahren Sie mehr über die Vorgänge und Funktionen der Fluss Steuerung in der Microsoft- Q# Standardbibliothek.'
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: ad107f5c65a4bf368d12d30e4a72786f2076205c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690869"
---
# <a name="higher-order-control-flow"></a><span data-ttu-id="430fb-103">Higher-Order Ablauf Steuerung</span><span class="sxs-lookup"><span data-stu-id="430fb-103">Higher-Order Control Flow</span></span> #

<span data-ttu-id="430fb-104">Eine der Hauptrollen der Standardbibliothek besteht darin, die algorithmischen Ideen auf hoher Ebene einfacher als [Quantum-Programme](https://en.wikipedia.org/wiki/Quantum_programming)auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="430fb-104">One of the primary roles of the standard library is to make it easier to express high-level algorithmic ideas as [quantum programs](https://en.wikipedia.org/wiki/Quantum_programming).</span></span>
<span data-ttu-id="430fb-105">Folglich stellt der Q# Kanon eine Vielzahl verschiedener flowsteuerungskonstrukte bereit, die jeweils mithilfe der partiellen Anwendung von Funktionen und Vorgängen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="430fb-105">Thus, the Q# canon provides a variety of different flow control constructs, each implemented using partial application of functions and operations.</span></span>
<span data-ttu-id="430fb-106">Wenn Sie sofort zu einem Beispiel springen, berücksichtigen Sie den Fall, in dem eine "CNOT-Leiter" für ein Register erstellt werden soll:</span><span class="sxs-lookup"><span data-stu-id="430fb-106">Jumping immediately into an example, consider the case in which one wants to construct a "CNOT ladder" on a register:</span></span>

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

<span data-ttu-id="430fb-107">Dieses Muster kann mithilfe von Iterationen und Schleifen ausgedrückt werden `for` :</span><span class="sxs-lookup"><span data-stu-id="430fb-107">We can express this pattern by using iteration and `for` loops:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

<span data-ttu-id="430fb-108">Ausgedrückt in Bezug auf <xref:Microsoft.Quantum.Canon.ApplyToEachCA> -und-Array Bearbeitungsfunktionen wie <xref:Microsoft.Quantum.Arrays.Zipped> , ist dies jedoch viel kürzer und leichter zu lesen:</span><span class="sxs-lookup"><span data-stu-id="430fb-108">Expressed in terms of <xref:Microsoft.Quantum.Canon.ApplyToEachCA> and array manipulation functions such as <xref:Microsoft.Quantum.Arrays.Zipped>, however, this is much shorter and easier to read:</span></span>

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

<span data-ttu-id="430fb-109">Im restlichen Teil dieses Abschnitts werden einige Beispiele für die Verwendung der verschiedenen Fluss Steuerungs Vorgänge und-Funktionen, die von der Canon bereitgestellt werden, zum kompakten Ausdrücken von Quantum-Programmen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="430fb-109">In the rest of this section, we will provide a number of examples of how to use the various flow control operations and functions provided by the canon to compactly express quantum programs.</span></span>

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a><span data-ttu-id="430fb-110">Anwenden von Vorgängen und Funktionen auf Arrays und Bereiche</span><span class="sxs-lookup"><span data-stu-id="430fb-110">Applying Operations and Functions over Arrays and Ranges</span></span> ##

<span data-ttu-id="430fb-111">Eine der primären Abstraktionen, die von der Canon bereitgestellt werden, ist die der Iterationen.</span><span class="sxs-lookup"><span data-stu-id="430fb-111">One of the primary abstractions provided by the canon is that of iteration.</span></span>
<span data-ttu-id="430fb-112">Nehmen Sie zum Beispiel eine einheitliche Form $U \otimes u \otimes \cdots \otimes u $ for a Single-Qubit einheitlicher $U $.</span><span class="sxs-lookup"><span data-stu-id="430fb-112">For instance, consider a unitary of the form $U \otimes U \otimes \cdots \otimes U$ for a single-qubit unitary $U$.</span></span>
<span data-ttu-id="430fb-113">In Q# können wir dies verwenden <xref:Microsoft.Quantum.Arrays.IndexRange> , um dies als eine `for` Schleife über ein Register darzustellen:</span><span class="sxs-lookup"><span data-stu-id="430fb-113">In Q#, we might use <xref:Microsoft.Quantum.Arrays.IndexRange> to represent this as as a `for` loop over a register:</span></span>

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation ApplyHadamardToAll(
    register : Qubit[])
: Unit is Adj + Ctl {
    for (qubit in register) {
        H(qubit);
    }
}
```

<span data-ttu-id="430fb-114">Anschließend können wir diesen neuen Vorgang verwenden `HAll(register)` , um $H \otimes h \otimes \cdots \otimes h $ anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="430fb-114">We can then use this new operation as `HAll(register)` to apply $H \otimes H \otimes \cdots \otimes H$.</span></span>

<span data-ttu-id="430fb-115">Dies ist jedoch umständlich, insbesondere in einem größeren Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="430fb-115">This is cumbersome to do, however, especially in a larger algorithm.</span></span>
<span data-ttu-id="430fb-116">Außerdem ist dieser Ansatz auf den jeweiligen Vorgang spezialisiert, den wir auf die einzelnen Qubits anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="430fb-116">Moreover, this approach is specialized to the particular operation that we wish to apply to each qubit.</span></span>
<span data-ttu-id="430fb-117">Wir können die Tatsache verwenden, dass Vorgänge erstklassige sind, um dieses algorithmische Konzept expliziter auszudrücken:</span><span class="sxs-lookup"><span data-stu-id="430fb-117">We can use the fact that operations are first-class to express this algorithmic concept more explicitly:</span></span>

```qsharp
ApplyToEachCA(H, register);
```

<span data-ttu-id="430fb-118">Hier gibt das-Suffix `CA` an, dass der-Aufrufwert `ApplyToEach` selbst adjointable und steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="430fb-118">Here, the suffix `CA` indicates that the call to `ApplyToEach` is itself adjointable and controllable.</span></span>
<span data-ttu-id="430fb-119">Wenn also `U` und unter `Adjoint` stützt `Controlled` , sind die folgenden Zeilen äquivalent:</span><span class="sxs-lookup"><span data-stu-id="430fb-119">Thus, if `U` supports `Adjoint` and `Controlled`, the following lines are equivalent:</span></span>

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

<span data-ttu-id="430fb-120">Dies bedeutet insbesondere, dass Aufrufe von `ApplyToEachCA` in Vorgängen angezeigt werden können, für die eine Adjoint-Spezialisierung automatisch generiert wird.</span><span class="sxs-lookup"><span data-stu-id="430fb-120">In particular, this means that calls to `ApplyToEachCA` can appear in operations for which an adjoint specialization is auto-generated.</span></span>
<span data-ttu-id="430fb-121">Ebenso <xref:Microsoft.Quantum.Canon.ApplyToEachIndex> eignet sich für die Darstellung von Mustern im Formular `U(0, targets[0]); U(1, targets[1]); ...` und bietet Versionen für jede Kombination von Funktoren, die von der Eingabe unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="430fb-121">Similarly, <xref:Microsoft.Quantum.Canon.ApplyToEachIndex> is useful for representing patterns of the form `U(0, targets[0]); U(1, targets[1]); ...`, and offers versions for each combination of functors supported by its input.</span></span>

> [!TIP]
> <span data-ttu-id="430fb-122">`ApplyToEach` ist typparametrisiert, sodass Sie mit-Vorgängen verwendet werden kann, die andere Eingaben als annehmen `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="430fb-122">`ApplyToEach` is type-parameterized such that it can be used with operations that take inputs other than `Qubit`.</span></span>
> <span data-ttu-id="430fb-123">Nehmen wir beispielsweise an, dass `codeBlocks` ein Array von <xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister> Werten ist, die wieder hergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="430fb-123">For example, suppose that `codeBlocks` is an array of <xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister> values that need to be recovered.</span></span>
> <span data-ttu-id="430fb-124">Dann `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` wendet den Fehler Behebungs Code `code` und die Wiederherstellungs Funktion `recoveryFn` unabhängig voneinander auf jeden Block an.</span><span class="sxs-lookup"><span data-stu-id="430fb-124">Then `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` will apply the error-correcting code `code` and recovery function `recoveryFn` to each block independently.</span></span>
> <span data-ttu-id="430fb-125">Dies gilt auch für klassische Eingaben: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` wendet eine Drehung von $ \pi/$2 über $X $ an, gefolgt von einer Drehung $pi/$3 über $Y $.</span><span class="sxs-lookup"><span data-stu-id="430fb-125">This holds even for classical inputs: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` will apply a rotation of $\pi / 2$ about $X$ followed by a rotation of $pi / 3$ about $Y$.</span></span>

<span data-ttu-id="430fb-126">Der Q# Kanon bietet auch Unterstützung für klassische Enumerationsmuster, die der funktionalen Programmierung vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="430fb-126">The Q# canon also provides support for classical enumeration patterns familiar to functional programming.</span></span>
<span data-ttu-id="430fb-127">Implementiert beispielsweise <xref:Microsoft.Quantum.Arrays.Fold> das Muster $f (f (s \_ {\text{Initial}}, x \_ 0), x \_ 1), \dots) $, um eine Funktion über eine Liste zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="430fb-127">For instance, <xref:Microsoft.Quantum.Arrays.Fold> implements the pattern $f(f(f(s\_{\text{initial}}, x\_0), x\_1), \dots)$ for reducing a function over a list.</span></span>
<span data-ttu-id="430fb-128">Dieses Muster kann verwendet werden, um Summen, Produkte, Minima, Maxima und andere Funktionen zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="430fb-128">This pattern can be used to implement sums, products, minima, maxima and other such functions:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

<span data-ttu-id="430fb-129">Ebenso können Funktionen wie <xref:Microsoft.Quantum.Arrays.Mapped> und <xref:Microsoft.Quantum.Arrays.MappedByIndex> verwendet werden, um funktionale Programmier Konzepte in auszudrücken Q# .</span><span class="sxs-lookup"><span data-stu-id="430fb-129">Similarly, functions like <xref:Microsoft.Quantum.Arrays.Mapped> and <xref:Microsoft.Quantum.Arrays.MappedByIndex> can be used to express functional programming concepts in Q#.</span></span>

## <a name="composing-operations-and-functions"></a><span data-ttu-id="430fb-130">Verfassen von Vorgängen und Funktionen</span><span class="sxs-lookup"><span data-stu-id="430fb-130">Composing Operations and Functions</span></span> ##

<span data-ttu-id="430fb-131">Die von der Canon angebotenen Ablaufsteuerungs-Konstrukte nehmen Vorgänge und Funktionen als Eingaben an, sodass es hilfreich ist, mehrere Vorgänge oder Funktionen in einem einzigen Aufruf baren zu verfassen.</span><span class="sxs-lookup"><span data-stu-id="430fb-131">The control flow constructs offered by the canon take operations and functions as their inputs, such that it is helpful to be able to compose several operations or functions into a single callable.</span></span>
<span data-ttu-id="430fb-132">Beispielsweise ist das Muster $UVU ^ {\dagger} $ bei der Quantum-Programmierung äußerst häufig, sodass der Kanon den Vorgang <xref:Microsoft.Quantum.Canon.ApplyWith> als Abstraktion für dieses Muster bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="430fb-132">For instance, the pattern $UVU^{\dagger}$ is extremely common in quantum programming, such that the canon provides the operation <xref:Microsoft.Quantum.Canon.ApplyWith> as an abstraction for this pattern.</span></span>
<span data-ttu-id="430fb-133">Diese Abstraktion ermöglicht auch ein effizienteres durcharbeiten in Verbindungen, da `Controlled` die Reihenfolge der Sequenz `U(qubit); V(qubit); Adjoint U(qubit);` nicht auf jede Weise agieren muss `U` .</span><span class="sxs-lookup"><span data-stu-id="430fb-133">This abstraction also allows for more efficient compliation into circuits, as `Controlled` acting on the sequence `U(qubit); V(qubit); Adjoint U(qubit);` does not need to act on each `U`.</span></span>
<span data-ttu-id="430fb-134">Um dies zu sehen, lassen Sie $c (U) $ die einheitliche Darstellung `Controlled U([control], target)` aus, und lassen Sie $c (V) $ auf die gleiche Weise definiert werden.</span><span class="sxs-lookup"><span data-stu-id="430fb-134">To see this, let $c(U)$ be the unitary representing `Controlled U([control], target)` and let $c(V)$ be defined in the same way.</span></span>
<span data-ttu-id="430fb-135">Für einen beliebigen Status $ \ket{\psi} $, \begin{align} c (u) c (V) c (u) ^ \dagger \ket {1} \otimes \ket{\psi} & = \ket {1} \otimes (UVU ^ {\dagger} \ket{\psi}) \\ \\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {1} \otimes \ket{\psi}.</span><span class="sxs-lookup"><span data-stu-id="430fb-135">Then for an arbitrary state $\ket{\psi}$, \begin{align} c(U) c(V) c(U)^\dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU^{\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{1} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="430fb-136">\end{align} durch die Definition von `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="430fb-136">\end{align} by the definition of `Controlled`.</span></span>
<span data-ttu-id="430fb-137">Andererseits: \begin{align} c (u) c (V) c (u) ^ \dagger \ket {0} \otimes \ket{\psi} & = \ket {0} \otimes \ket{\psi} \\ \\ & = \ket {0} \ouhrzeiten (UU ^ \dagger \ket{\psi}) \\ \\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {0} \otimes \ket{\psi}.</span><span class="sxs-lookup"><span data-stu-id="430fb-137">On the other hand, \begin{align} c(U) c(V) c(U)^\dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \otimes (UU^\dagger \ket{\psi}) \\\\ & = (\boldone \otimes U) (c(V)) (\boldone \otimes U^\dagger) \ket{0} \otimes \ket{\psi}.</span></span>
<span data-ttu-id="430fb-138">\end{align} nach Linearität können wir den Schluss $U $ out für alle Eingabe Zustände auf diese Weise berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="430fb-138">\end{align} By linearity, we can conclude that we can factor $U$ out in this way for all input states.</span></span>
<span data-ttu-id="430fb-139">Das heißt, $c (UVU ^ \dagger) = u c (V) u ^ \dagger $.</span><span class="sxs-lookup"><span data-stu-id="430fb-139">That is, $c(UVU^\dagger) = U c(V) U^\dagger$.</span></span>
<span data-ttu-id="430fb-140">Da das Steuern von Vorgängen im allgemeinen teuer sein kann, kann die Verwendung von kontrollierten Varianten wie `WithC` und `WithCA` die Anzahl von Steuerelement-Funktoren verringern, die angewendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="430fb-140">Since controlling operations can be expensive in general, using controlled variants such as `WithC` and `WithCA` can help reduce the number of control functors that need to be applied.</span></span>

> [!NOTE]
> <span data-ttu-id="430fb-141">Eine andere Folge bei der Umgestaltung $U $ besteht darin, dass wir nicht einmal wissen müssen, wie das `Controlled` Funktor angewendet wird `U` .</span><span class="sxs-lookup"><span data-stu-id="430fb-141">One other consequence of factoring out $U$ is that we need not even know how to apply the `Controlled` functor to `U`.</span></span>
> <span data-ttu-id="430fb-142">`ApplyWithCA` Daher weist eine schwächere Signatur auf, als möglicherweise erwartet wird:</span><span class="sxs-lookup"><span data-stu-id="430fb-142">`ApplyWithCA` therefore has a weaker signature than might be expected:</span></span>
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

<span data-ttu-id="430fb-143">Ebenso <xref:Microsoft.Quantum.Canon.Bound> erzeugt Vorgänge, die wiederum eine Sequenz anderer Vorgänge anwenden.</span><span class="sxs-lookup"><span data-stu-id="430fb-143">Similarly, <xref:Microsoft.Quantum.Canon.Bound> produces operations which apply a sequence of other operations in turn.</span></span>
<span data-ttu-id="430fb-144">Beispielsweise sind die folgenden Punkte äquivalent:</span><span class="sxs-lookup"><span data-stu-id="430fb-144">For instance, the following are equivalent:</span></span>

```qsharp
H(qubit); X(qubit);
Bound([H, X], qubit);
```

<span data-ttu-id="430fb-145">Das Kombinieren mit Iterations Mustern kann dies besonders nützlich machen:</span><span class="sxs-lookup"><span data-stu-id="430fb-145">Combining with iteration patterns can make this especially useful:</span></span>

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bound([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a><span data-ttu-id="430fb-146">Time-Ordered Komposition</span><span class="sxs-lookup"><span data-stu-id="430fb-146">Time-Ordered Composition</span></span> ###

<span data-ttu-id="430fb-147">Wir können noch weiter gehen, indem wir die Fluss Steuerung in Bezug auf partielle Anwendungs-und klassische Funktionen betrachten und auch ziemlich ausgereifte Quantum-Konzepte im Hinblick auf die klassische Fluss Steuerung modellieren.</span><span class="sxs-lookup"><span data-stu-id="430fb-147">We can go still further by thinking of flow control in terms of partial application and classical functions, and can model even fairly sophisticated quantum concepts in terms of classical flow control.</span></span>
<span data-ttu-id="430fb-148">Diese Analogie wird durch die Erkennung präziser, dass einheitliche Operatoren genau den Nebeneffekten von aufrufenden Vorgängen entsprechen, sodass jede Zerlegung einheitlicher Operatoren in Bezug auf andere einheitliche Operatoren die Erstellung einer bestimmten Aufruf Sequenz für klassische Unterroutinen entspricht, die Anweisungen ausgeben, die als bestimmte einheitliche Operatoren fungieren.</span><span class="sxs-lookup"><span data-stu-id="430fb-148">This analogy is made precise by the recognition that unitary operators correspond exactly to the side effects of calling operations, such that any decomposition of unitary operators in terms of other unitary operators corresponds to constructing a particular calling sequence for classical subroutines which emit instructions to act as particular unitary operators.</span></span>
<span data-ttu-id="430fb-149">In dieser Ansicht `Bound` ist genau die Darstellung des Matrix Produkts, da `Bound([A, B])(target)` gleich ist `A(target); B(target);` , was wiederum die Aufruf Sequenz ist, die $BA $ entspricht.</span><span class="sxs-lookup"><span data-stu-id="430fb-149">Under this view, `Bound` is precisely the representation of the matrix product, since `Bound([A, B])(target)` is equivalent to `A(target); B(target);`, which in turn is the calling sequence corresponding to $BA$.</span></span>

<span data-ttu-id="430fb-150">Ein anspruchsvolleres Beispiel ist die [Erweiterung "Trotter – Suzuki](https://arxiv.org/abs/math-ph/0506007v1)".</span><span class="sxs-lookup"><span data-stu-id="430fb-150">A more sophisticated example is the [Trotter–Suzuki expansion](https://arxiv.org/abs/math-ph/0506007v1).</span></span>
<span data-ttu-id="430fb-151">Wie im Abschnitt "Dynamical Generator Darstellung" der [Datenstrukturen](xref:microsoft.quantum.libraries.data-structures)erläutert, bietet die Trotter – Suzuki-Erweiterung eine besonders nützliche Methode zum Ausdrücken von Matrix exponentialen.</span><span class="sxs-lookup"><span data-stu-id="430fb-151">As discussed in the Dynamical Generator Representation section of [data structures](xref:microsoft.quantum.libraries.data-structures), the Trotter–Suzuki expansion provides a particularly useful way of expressing matrix exponentials.</span></span>
<span data-ttu-id="430fb-152">Wenn Sie die Erweiterung beispielsweise in der untersten Reihenfolge anwenden, ergibt dies für alle Operatoren $A $ und $B $, sodass $A = A ^ \dagger $ und $B = B ^ \dagger $, \begin{align} \tag{★} \label{EQ: Trotter-Suzuki-0} \exp (i [A + B] t) = \ lim_ {n\t\infty} \left (\exp (i A t/n) \exp (i B t/n) \right) ^ n.</span><span class="sxs-lookup"><span data-stu-id="430fb-152">For instance, applying the expansion at its lowest order yields that for any operators $A$ and $B$ such that $A = A^\dagger$ and $B = B^\dagger$, \begin{align} \tag{★} \label{eq:trotter-suzuki-0} \exp(i [A + B] t) = \lim_{n\to\infty} \left(\exp(i A t / n) \exp(i B t / n)\right)^n.</span></span>
<span data-ttu-id="430fb-153">\end{align}, das heißt, dass wir einen Status unter $A + B $ weiterentwickeln können, indem Sie sich unter $A $ und $B $ allein weiterentwickeln.</span><span class="sxs-lookup"><span data-stu-id="430fb-153">\end{align} Colloquially, this says that we can approximately evolve a state under $A + B$ by alternately evolving under $A$ and $B$ alone.</span></span>
<span data-ttu-id="430fb-154">Wenn wir die Weiterentwicklung unter $A $ durch einen Vorgang darstellen `A : (Double, Qubit[]) => Unit` , der $e ^ {i t A} $ angewendet wird, wird die Darstellung des Trotters – Suzuki-Erweiterung in Bezug auf das Neuordnen von Aufruf Sequenzen deutlich.</span><span class="sxs-lookup"><span data-stu-id="430fb-154">If we represent evolution under $A$ by an operation `A : (Double, Qubit[]) => Unit` that applies $e^{i t A}$, then the representation of the Trotter–Suzuki expansion in terms of rearranging calling sequences becomes clear.</span></span>
<span data-ttu-id="430fb-155">Konkret: bei einem Vorgang `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` wie `A = U(0, _, _)` und `B = U(1, _, _)` können wir einen neuen Vorgang definieren, der den ganzzahligen Wert von `U` at time $t $ darstellt, indem Sequenzen der Form erzeugt werden.</span><span class="sxs-lookup"><span data-stu-id="430fb-155">Concretely, given an operation `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` such that `A = U(0, _, _)` and `B = U(1, _, _)`, we can define a new operation representing the integral of `U` at time $t$ by generating sequences of the form</span></span>

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

<span data-ttu-id="430fb-156">An diesem Punkt können wir nun die –-Erweiterung "Trotter" *ohne Verweis auf die Quantum-Mechanik* in Grund haben.</span><span class="sxs-lookup"><span data-stu-id="430fb-156">At this point, we can now reason about the Trotter–Suzuki expansion *without reference to quantum mechanics at all* .</span></span>
<span data-ttu-id="430fb-157">Die Erweiterung ist ein sehr spezielles Iterations Muster, das durch "$ \eqref {EQ: Trotter-Suzuki-0} $" motiviert ist.</span><span class="sxs-lookup"><span data-stu-id="430fb-157">The expansion is effectively a very particular iteration pattern motivated by $\eqref{eq:trotter-suzuki-0}$.</span></span>
<span data-ttu-id="430fb-158">Dieses Iterations Muster wird implementiert von <xref:Microsoft.Quantum.Canon.DecomposedIntoTimestepsCA> :</span><span class="sxs-lookup"><span data-stu-id="430fb-158">This iteration pattern is implemented by <xref:Microsoft.Quantum.Canon.DecomposedIntoTimestepsCA>:</span></span>

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

<span data-ttu-id="430fb-159">Die Signatur von `DecomposeIntoTimeStepsCA` folgt einem allgemeinen Muster in Q# , bei dem Auflistungen, die entweder durch Arrays oder durch Elemente, die im laufenden Betrieb sind, durch Tupel dargestellt werden, deren erste Elemente Werte sind, die `Int` Ihre Längen angeben.</span><span class="sxs-lookup"><span data-stu-id="430fb-159">The signature of `DecomposeIntoTimeStepsCA` follows a common pattern in Q#, where collections that may be backed either by arrays or by something which compute elements on the fly are represented by tuples whose first elements are `Int` values indicating their lengths.</span></span>

## <a name="putting-it-together-controlling-operations"></a><span data-ttu-id="430fb-160">Kombinieren von Vorgängen: Steuern von Vorgängen</span><span class="sxs-lookup"><span data-stu-id="430fb-160">Putting it Together: Controlling Operations</span></span> ##

<span data-ttu-id="430fb-161">Schließlich baut der Kanon auf dem `Controlled` Funktor auf, indem er zusätzliche Möglichkeiten für die Bedingung von Quantum-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="430fb-161">Finally, the canon builds on the `Controlled` functor by providing additional ways to condition quantum operations.</span></span>
<span data-ttu-id="430fb-162">Es ist üblich, insbesondere bei der Quantum-Arithmetik, Vorgänge in anderen Compute-Zuständen als $ \ket{0\cdots 0} $ auszuführen.</span><span class="sxs-lookup"><span data-stu-id="430fb-162">It is common, especially in quantum arithmetic, to condition operations on computational basis states other than $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="430fb-163">Mithilfe der oben eingeführten Steuerungs Vorgänge und-Funktionen können wir in einer einzelnen Anweisung allgemeinere Quantum-Bedingungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="430fb-163">Using the control operations and functions introduced above, we can more general quantum conditions in a single statement.</span></span>
<span data-ttu-id="430fb-164"><xref:Microsoft.Quantum.Canon.ControlledOnBitString>Sehen wir uns nun an, wie dies geschieht (Sans-Typparameter), und dann werden die Teile nacheinander unterbricht.</span><span class="sxs-lookup"><span data-stu-id="430fb-164">Let's jump in to how <xref:Microsoft.Quantum.Canon.ControlledOnBitString> does it (sans type parameters), then we'll break down the pieces one by one.</span></span>
<span data-ttu-id="430fb-165">Als erstes müssen wir einen Vorgang definieren, der tatsächlich den Schwerpunkt der Implementierung des Steuer Elements auf willkürlichen Berechnungsbasis Zuständen leistet.</span><span class="sxs-lookup"><span data-stu-id="430fb-165">The first thing we'll need to do is to define an operation which actually does the heavy lifting of implementing the control on arbitrary computational basis states.</span></span>
<span data-ttu-id="430fb-166">Dieser Vorgang wird jedoch nicht direkt aufgerufen. daher fügen wir `_` am Anfang des Namens ein, um anzugeben, dass es sich um eine Implementierung eines anderen Konstrukts an anderer Stelle handelt.</span><span class="sxs-lookup"><span data-stu-id="430fb-166">We won't call this operation directly, however, and so we add `_` to the beginning of the name to indicate that it's an implementation of another construct elsewhere.</span></span>

```qsharp
operation _ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl),
    controlRegister : Qubit[],
    targetRegister: Qubit[])
: Unit is Adj + Ctl
```

<span data-ttu-id="430fb-167">Beachten Sie, dass wir eine als-Array dargestellte Zeichenfolge als `Bool` Array verwenden, mit der wir die gewünschte Anlage für den Vorgang angeben, den `oracle` wir erhalten.</span><span class="sxs-lookup"><span data-stu-id="430fb-167">Note that we take a string of bits, represented as a `Bool` array, that we use to specify the conditioning that we want to apply to the operation `oracle` that we are given.</span></span>
<span data-ttu-id="430fb-168">Da dieser Vorgang die Anwendung tatsächlich direkt durchführt, müssen wir auch die Steuer-und Ziel Register verwenden, die beide hier als dargestellt werden `Qubit[]` .</span><span class="sxs-lookup"><span data-stu-id="430fb-168">Since this operation actually does the application directly, we also need to take the control and target registers, both represented here as `Qubit[]`.</span></span>

<span data-ttu-id="430fb-169">Als Nächstes stellen wir fest, dass die Steuerung des Berechnungs basierten Zustands $ \ket{\vec{s}} = \ket{s \_ 0 s \_ 1 \dots s \_ {n-1}} $ für eine Bitzeichenfolge $ \vec{s} $ durch Umwandeln von $ \ket{\vec{s}} $ in $ \ket{0\cdots 0} $ realisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="430fb-169">Next, we note that controlling on the computational basis state $\ket{\vec{s}} = \ket{s\_0 s\_1 \dots s\_{n - 1}}$ for a bit string $\vec{s}$ can be realized by transforming $\ket{\vec{s}}$ into $\ket{0\cdots 0}$.</span></span>
<span data-ttu-id="430fb-170">Insbesondere: $ \ket{\vec{s}} = X ^ {s \_ 0} \otimes X ^ {s \_ 1} \otimes \cdots \otimes X ^ {s \_ {n-1}} \ket{0\cdots 0} $.</span><span class="sxs-lookup"><span data-stu-id="430fb-170">In particular, $\ket{\vec{s}} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{0\cdots 0}$.</span></span>
<span data-ttu-id="430fb-171">Seit $X ^ {\dagger} = x $ bedeutet dies, dass $ \ket{0\dots 0} = X ^ {s \_ 0} \otimes x ^ {s \_ 1} \otimes \cdots \otimes x ^ {s \_ {n-1}} \ket{\vec{s}} $.</span><span class="sxs-lookup"><span data-stu-id="430fb-171">Since $X^{\dagger} = X$, this implies that $\ket{0\dots 0} = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}} \ket{\vec{s}}$.</span></span>
<span data-ttu-id="430fb-172">Daher können wir $P = x ^ {s \_ 0} \otimes x ^ {s \_ 1} \otimes \cdots \otimes X ^ {s \_ {n-1}} $, Apply `Controlled oracle` und Transform Back to $ \vec{s} $ anwenden.</span><span class="sxs-lookup"><span data-stu-id="430fb-172">Thus, we can apply $P = X^{s\_0} \otimes X^{s\_1} \otimes \cdots \otimes X^{s\_{n - 1}}$, apply `Controlled oracle`, and transform back to $\vec{s}$.</span></span>
<span data-ttu-id="430fb-173">Diese Konstruktion ist genau `ApplyWith` , daher wird der Text des neuen Vorgangs entsprechend geschrieben:</span><span class="sxs-lookup"><span data-stu-id="430fb-173">This construction is precisely `ApplyWith`, so we write the body of our new operation accordingly:</span></span>

```qsharp
{
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

<span data-ttu-id="430fb-174">Hier haben wir verwendet, <xref:Microsoft.Quantum.Canon.ApplyPauliFromBitString> um $P $ anzuwenden, um das Ziel teilweise für die Verwendung mit anzuwenden `ApplyWith` .</span><span class="sxs-lookup"><span data-stu-id="430fb-174">Here, we have used <xref:Microsoft.Quantum.Canon.ApplyPauliFromBitString> to apply $P$, partially applying over its target for use with `ApplyWith`.</span></span>
<span data-ttu-id="430fb-175">Beachten Sie jedoch, dass wir die *Steuer* Element Registrierung in das gewünschte Formular umwandeln müssen, sodass wir den inneren Vorgang `(Controlled oracle)` für das *Ziel* teilweise anwenden.</span><span class="sxs-lookup"><span data-stu-id="430fb-175">Note, however, that we need to transform the *control* register to our desired form, so we partially apply the inner operation `(Controlled oracle)` on the *target* .</span></span>
<span data-ttu-id="430fb-176">Dadurch `ApplyWith` wird das Steuerelement in der Klammer mit $P $, genau wie gewünscht, in eine eckige Klammer eingefügt.</span><span class="sxs-lookup"><span data-stu-id="430fb-176">This leaves `ApplyWith` acting to bracket the control register with $P$, exactly as we desired.</span></span>

<span data-ttu-id="430fb-177">An diesem Punkt könnten wir zwar das tun, aber es ist nicht zu erwarten, dass unser neuer Vorgang nicht wie das Anwenden des `Controlled` funktors funktioniert.</span><span class="sxs-lookup"><span data-stu-id="430fb-177">At this point, we could be done, but it is somehow unsatisfying that our new operation does not "feel" like applying the `Controlled` functor.</span></span>
<span data-ttu-id="430fb-178">Daher haben wir die Definition des neuen Ablauf steuerungskonzepts abgeschlossen, indem wir eine Funktion schreiben, die das Oracle zum Steuern benötigt und einen neuen Vorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="430fb-178">Thus, we finish defining our new control flow concept by writing a function that takes the oracle to be controlled and that returns a new operation.</span></span>
<span data-ttu-id="430fb-179">Auf diese Weise sieht die neue Funktion sehr ähnlich aus und zeigt `Controlled` , dass wir mit und dem Kanon problemlos leistungsstarke neue Ablaufsteuerungskonstrukte definieren können Q# :</span><span class="sxs-lookup"><span data-stu-id="430fb-179">In this way, our new function looks and feels very much like `Controlled`, illustrating that we can easily define powerful new control flow constructs using Q# and the canon together:</span></span>

```qsharp
function ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl))
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
