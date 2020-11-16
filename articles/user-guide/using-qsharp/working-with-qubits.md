---
title: Arbeiten mit Qubits
description: 'Weitere Informationen zum Arbeiten mit Qubits in Q#'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 9a3d7e03016332a04ac9d1610428b6fcd546d1f6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691578"
---
# <a name="working-with-qubits"></a><span data-ttu-id="c92dd-103">Arbeiten mit Qubits</span><span class="sxs-lookup"><span data-stu-id="c92dd-103">Working with qubits</span></span>

<span data-ttu-id="c92dd-104">Qubits sind das grundlegende Objekt der Informationen in Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="c92dd-104">Qubits are the fundamental object of information in quantum computing.</span></span> <span data-ttu-id="c92dd-105">Eine allgemeine Einführung in Qubits finden Sie Untergrund Legendes zu [Quantum Computing](xref:microsoft.quantum.overview.understanding). Weitere Informationen zu ihrer mathematischen Darstellung finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="c92dd-105">For a general introduction to qubits, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding), and to dive deeper into their mathematical representation, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span> 

<span data-ttu-id="c92dd-106">In diesem Artikel wird beschrieben, wie Sie in einem Programm mit Qubits arbeiten und diese verwenden Q# .</span><span class="sxs-lookup"><span data-stu-id="c92dd-106">This article explores how to use and work with qubits in a Q# program.</span></span> 

> [!IMPORTANT]
><span data-ttu-id="c92dd-107">Keine der in diesem Artikel behandelten Anweisungen ist im Text einer Funktion gültig.</span><span class="sxs-lookup"><span data-stu-id="c92dd-107">None of the statements discussed in this article are valid within the body of a function.</span></span> <span data-ttu-id="c92dd-108">Sie sind nur innerhalb von Vorgängen gültig.</span><span class="sxs-lookup"><span data-stu-id="c92dd-108">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="c92dd-109">Zuordnen von Qubits</span><span class="sxs-lookup"><span data-stu-id="c92dd-109">Allocating Qubits</span></span>

<span data-ttu-id="c92dd-110">Da es sich bei physischen Qubits um eine wertvolle Ressource auf einem Quantum-Computer handelt, besteht der Auftrag des Compilers darin, sicherzustellen, dass Sie so effizient wie möglich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-110">Because physical qubits are a precious resource in a quantum computer, part of the compiler's job is to make sure they are being used as efficiently as possible.</span></span>
<span data-ttu-id="c92dd-111">Daher müssen Sie angeben, Q# dass Qubits zur Verwendung in einem bestimmten Anweisungsblock *zuzuordnen* sind.</span><span class="sxs-lookup"><span data-stu-id="c92dd-111">As such, you need to tell Q# to *allocate* qubits for use within a particular statement block.</span></span>
<span data-ttu-id="c92dd-112">Sie können Qubits als einzelnes Qubit oder als Array von Qubits zuordnen, die als *Register* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-112">You can allocate qubits as a single qubit, or as an array of qubits, known as a *register* .</span></span> 

### <a name="clean-qubits"></a><span data-ttu-id="c92dd-113">Löschen von Qubits</span><span class="sxs-lookup"><span data-stu-id="c92dd-113">Clean qubits</span></span>

<span data-ttu-id="c92dd-114">Verwenden Sie die- `using` Anweisung, um neue Qubits für die Verwendung während eines-Anweisungsblocks zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-114">Use the `using` statement to allocate new qubits for use during a statement block.</span></span>

<span data-ttu-id="c92dd-115">Die-Anweisung besteht aus dem Schlüsselwort `using` , gefolgt von einer in Klammern eingeschlossenen Bindung `( )` und dem Anweisungsblock, in dem die Qubits verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c92dd-115">The statement consists of the keyword `using`, followed by a binding enclosed in parentheses `( )` and the statement block within which the qubits are available.</span></span>
<span data-ttu-id="c92dd-116">Die Bindung folgt demselben Muster wie `let` -Anweisungen: entweder ein einzelnes Symbol oder ein Tupel von Symbolen, gefolgt von einem Gleichheitszeichen `=` und entweder ein einzelner Wert oder ein entsprechendes Tupel von *Initialisierern* .</span><span class="sxs-lookup"><span data-stu-id="c92dd-116">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers* .</span></span>

<span data-ttu-id="c92dd-117">Initialisierer sind entweder für ein einzelnes Qubit, das als angegeben ist, `Qubit()` oder ein Array von Qubits verfügbar, `Qubit[n]` wobei `n` ein `Int` Ausdruck ist.</span><span class="sxs-lookup"><span data-stu-id="c92dd-117">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="c92dd-118">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="c92dd-118">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="c92dd-119">Alle auf diese Weise zugeordneten Qubits beginnen mit dem Status $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="c92dd-119">Any qubits allocated in this way start off in the $\ket{0}$ state.</span></span> <span data-ttu-id="c92dd-120">Daher ist im vorherigen Beispiel `auxiliary` ein einzelnes Qubit im Status $ \ket {0} $, und `register` befindet sich im fünf-Qubit-Zustand $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="c92dd-120">Thus in the previous example, `auxiliary` is a single qubit in the state $\ket{0}$, and `register` is in the five-qubit state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="c92dd-121">Am Ende des- `using` Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-121">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="c92dd-122">Zielcomputer können zugeordnete Qubits wieder verwenden und anderen Blöcken für die Zuordnung zur Verfügung stellen `using` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-122">Target machines can reuse deallocated qubits and offer them to other `using` blocks for allocation.</span></span> <span data-ttu-id="c92dd-123">Der Zielcomputer erwartet daher, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im $ \ket {0} $-Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-123">As such, the target machine expects that qubits are in the $\ket{0}$ state immediately before deallocation.</span></span>
> <span data-ttu-id="c92dd-124">Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket $ zurückzugeben {0} .</span><span class="sxs-lookup"><span data-stu-id="c92dd-124">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="c92dd-125">Wenn erforderlich, können Sie den @"microsoft.quantum.intrinsic.reset" -Vorgang verwenden, der das Qubit an $ \ket $ zurückgibt, {0} indem Sie es Messen und bedingt einen Vorgang basierend auf dem Ergebnis ausführen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-125">If need be, you can use the @"microsoft.quantum.intrinsic.reset" operation, which returns the qubit to $\ket{0}$ by measuring it and conditionally performing an operation based on the result.</span></span> <span data-ttu-id="c92dd-126">Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.</span><span class="sxs-lookup"><span data-stu-id="c92dd-126">Such a measurement destroys any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="c92dd-127">Geliehene Qubits</span><span class="sxs-lookup"><span data-stu-id="c92dd-127">Borrowed Qubits</span></span>

<span data-ttu-id="c92dd-128">Verwenden Sie die- `borrowing` Anweisung, um Qubits für die temporäre Verwendung zuzuweisen, die sich nicht in einem bestimmten Zustand befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-128">Use the `borrowing` statement to allocate qubits for temporary use, which do not need to be in a specific state.</span></span>

<span data-ttu-id="c92dd-129">Sie können geliehene Qubits während einer Berechnung als temporären Speicherplatz verwenden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-129">You can use borrowed qubits as scratch space during a computation.</span></span>
<span data-ttu-id="c92dd-130">Diese Qubits befinden sich in der Regel nicht in einem sauberen Zustand, d. h., Sie werden nicht notwendigerweise in einem bekannten Zustand initialisiert, wie z. b. $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="c92dd-130">These qubits are generally not in a clean state, that is, they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="c92dd-131">Diese werden häufig als "modifizierte" Qubits bezeichnet, da ihr Zustand unbekannt ist und sogar mit anderen Teilen des Arbeitsspeichers des Quantums Computers entkoppelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c92dd-131">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="c92dd-132">Die Bindung folgt demselben Muster und denselben Regeln wie die- `using` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="c92dd-132">The binding follows the same pattern and rules as the `using` statement.</span></span>
<span data-ttu-id="c92dd-133">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="c92dd-133">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="c92dd-134">Die geliehenen Qubits befinden sich in einem unbekannten Zustand und verlassen den Gültigkeitsbereich am Ende des Anweisungsblocks.</span><span class="sxs-lookup"><span data-stu-id="c92dd-134">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="c92dd-135">Der Kreditnehmer führt einen Commit aus, um die Qubits in demselben Zustand zu belassen, in dem Sie sich befanden. Das heißt, ihr Zustand am Anfang und am Ende des Anweisungsblocks sollte identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c92dd-135">The borrower commits to leaving the qubits in the same state they were in when they borrowed them; that is, their state at the beginning and the end of the statement block should be the same.</span></span>
<span data-ttu-id="c92dd-136">Da dieser Zustand nicht notwendigerweise ein klassischer Zustand ist, sollten in den meisten Fällen die erfassten Bereiche keine Messungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="c92dd-136">Because this state is not necessarily a classical state, in most cases borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="c92dd-137">Beim Abgleich von Qubits versucht das System zuerst, die Anforderung aus Qubits auszufüllen, die verwendet werden, aber nicht während des Texts der Anweisung darauf zugegriffen wird `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-137">When borrowing qubits, the system first tries to fill the request from qubits that are in use but not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="c92dd-138">Wenn nicht genügend solche Qubits vorhanden sind, werden neue Qubits zugewiesen, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-138">If there aren't enough such qubits, then it allocates new qubits to complete the request.</span></span>

<span data-ttu-id="c92dd-139">Zu den bekannten Anwendungsfällen von Dirty Qubits zählen Implementierungen von multigesteuerten CNOT Gates, die nur sehr wenige Qubits und die Implementierung von inkrementern erfordern.</span><span class="sxs-lookup"><span data-stu-id="c92dd-139">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="c92dd-140">Ein Beispiel für die Verwendung in Q# finden Sie unter Beispiel für das [Ausleihen von Qubits](#borrowing-qubits-example) in diesem Artikel oder im Whitepaper [*using 2N + 2 Qubits with Toffoli based modulare Multiplikation*](https://arxiv.org/abs/1611.07995) (Haner, roetteler und svore 2017) für einen Algorithmus, der geliehene Qubits verwendet.</span><span class="sxs-lookup"><span data-stu-id="c92dd-140">For an example of their use in Q#, see [Borrowing Qubits Example](#borrowing-qubits-example) in this article, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="c92dd-141">Intrinsische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c92dd-141">Intrinsic Operations</span></span>

<span data-ttu-id="c92dd-142">Nach der Zuordnung können Sie ein Qubit an Funktionen und Vorgänge übergeben.</span><span class="sxs-lookup"><span data-stu-id="c92dd-142">Once allocated, you can pass a qubit to functions and operations.</span></span>
<span data-ttu-id="c92dd-143">In gewisser Hinsicht ist dies alles, was ein Q# Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.</span><span class="sxs-lookup"><span data-stu-id="c92dd-143">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>

<span data-ttu-id="c92dd-144">In diesem Artikel werden einige nützliche Q# Vorgänge erläutert, die Sie für die Interaktion mit Qubits verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c92dd-144">This article discusses a few useful Q# operations that you can use to interact with qubits.</span></span>
<span data-ttu-id="c92dd-145">Weitere Details zu diesen und anderen finden Sie unter systeminterne [Vorgänge und Funktionen](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="c92dd-145">For more detail about these and others, see [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span> 

<span data-ttu-id="c92dd-146">Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q# durch die intrinsischen Vorgänge [`X`](xref:Microsoft.Quantum.Intrinsic.X) , und dargestellt, die jeweils den- [`Y`](xref:Microsoft.Quantum.Intrinsic.Y) [`Z`](xref:Microsoft.Quantum.Intrinsic.Z) Typ haben `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-146">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations [`X`](xref:Microsoft.Quantum.Intrinsic.X), [`Y`](xref:Microsoft.Quantum.Intrinsic.Y), and [`Z`](xref:Microsoft.Quantum.Intrinsic.Z), each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="c92dd-147">Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, sollten Sie sich $X $ und somit auch `X` als bitflip-Vorgang oder nicht als Gate vorstellen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-147">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="c92dd-148">Sie können den- `X` Vorgang verwenden, um Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorzubereiten $s $:</span><span class="sxs-lookup"><span data-stu-id="c92dd-148">You can use the `X` operation to prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

```qsharp
operation PrepareBitString(bitstring : Bool[], register : Qubit[]) : Unit
is Adj + Ctl {
    let nQubits = Length(register);
    for (idxQubit in 0..nQubits - 1) {
        if (bitstring[idxQubit]) {
            X(register[idxQubit]);
        }
    }
}

operation RunExample() : Unit {
    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
        // Remember to reset the qubits before deallocation:
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="c92dd-149">Später sehen Sie kompaktere Methoden zum Schreiben dieses Vorgangs, für die keine manuelle Ablauf Steuerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c92dd-149">Later, you will see more compact ways of writing this operation that do not require manual control flow.</span></span>

<span data-ttu-id="c92dd-150">Sie können auch Zustände wie z. b. $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ und $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ mithilfe der Hadamard Transform $H $, die in Q# durch den systeminternen Vorgang [`H`](xref:Microsoft.Quantum.Intrinsic.H) (auch vom Typ (Qubit => Unit is ADJ + CTL)) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c92dd-150">You can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation [`H`](xref:Microsoft.Quantum.Intrinsic.H) (also of type (Qubit => Unit is Adj + Ctl)\`):</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString in the earlier example.
    PrepareBitString(bitstring, register);
    // Next, use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the desired state.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="c92dd-151">Messungen</span><span class="sxs-lookup"><span data-stu-id="c92dd-151">Measurements</span></span>

<span data-ttu-id="c92dd-152">Die Messungen einzelner Qubits können in unterschiedlichen Basen durchgeführt werden, die jeweils durch eine Pauli-Achse auf der [Bloch-Kugel](xref:microsoft.quantum.glossary#bloch-sphere)dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-152">Measurements of individual qubits can be performed in different bases, each represented by a Pauli axis on the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere).</span></span>
<span data-ttu-id="c92dd-153">Die *Berechnungsbasis* bezieht sich auf die `PauliZ` Basis und ist die am häufigsten verwendete Grundlage für die Messung.</span><span class="sxs-lookup"><span data-stu-id="c92dd-153">The *computational basis* refers to the `PauliZ` basis, and is the most common basis used for measurement.</span></span>

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a><span data-ttu-id="c92dd-154">Messen eines einzelnen Qubit in der `PauliZ` Basis</span><span class="sxs-lookup"><span data-stu-id="c92dd-154">Measure a single qubit in the `PauliZ` basis</span></span>

<span data-ttu-id="c92dd-155">Verwenden [`M`](xref:Microsoft.Quantum.Intrinsic.M) Sie den-Vorgang, bei dem es sich um einen integrierten, intrinsischen nicht einheitlichen Vorgang handelt, um ein einzelnes Qubit in der Basis zu messen `PauliZ` und dem Ergebnis einen klassischen Wert zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c92dd-155">Use the [`M`](xref:Microsoft.Quantum.Intrinsic.M) operation, which is a built-in intrinsic non-unitary operation, to measure a single qubit in the `PauliZ` basis and assign a classical value to the result.</span></span>
<span data-ttu-id="c92dd-156">`M` verfügt über einen reservierten Rückgabetyp, `Result` , der nur Werte annehmen kann `Zero` oder `One` die den gemessenen Zuständen $ \ket {0} $ oder $ \ket {1} $ entspricht. Dies deutet darauf hin, dass das Ergebnis nicht mehr ein Quantum-Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="c92dd-156">`M` has a reserved return type, `Result`, which can only take values `Zero` or `One` corresponding to the measured states $\ket{0}$ or $\ket{1}$ - indicating that the result is no longer a quantum state.</span></span>

<span data-ttu-id="c92dd-157">Ein einfaches Beispiel ist der folgende Vorgang, der ein Qubit im $ \ket $-Zustand zuordnet {0} , dann einen Hadamard-Vorgang `H` darauf anwendet und das Ergebnis in der `PauliZ` Basis misst.</span><span class="sxs-lookup"><span data-stu-id="c92dd-157">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // Apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, return the result of the measurement.
        return result;
    }
}
```

### <a name="measure-one-or-more-qubits-in-specific-bases"></a><span data-ttu-id="c92dd-158">Messen eines oder mehrerer Qubits in bestimmten Basen</span><span class="sxs-lookup"><span data-stu-id="c92dd-158">Measure one or more qubits in specific bases</span></span>

<span data-ttu-id="c92dd-159">Zum Messen eines Arrays mit einem oder mehreren Qubits in bestimmten Basen können Sie den- [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) Vorgang verwenden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-159">To measure an array of one or more qubits in specific bases, you can use the [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) operation.</span></span>

<span data-ttu-id="c92dd-160">Die Eingaben für `Measure` sind ein Array von `Pauli` Typen (z. b `[PauliX, PauliZ, PauliZ]` .) und ein Array von Qubits.</span><span class="sxs-lookup"><span data-stu-id="c92dd-160">The inputs to `Measure` are an array of `Pauli` types (for example, `[PauliX, PauliZ, PauliZ]`) and an array of qubits.</span></span>

<span data-ttu-id="c92dd-161">Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert zurückgibt, `true` Wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli-Basis gemessen werden und andernfalls andernfalls zurückgegeben werden `false` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-161">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

```qsharp
operation MeasureIfAllQubitsAreZero(qubits : Qubit[], pauli : Pauli) : Bool {
    mutable value = true;
    for (qubit in qubits) {
        if (Measure([pauli], [qubit]) == One) {
            set value = false;
        }
    }
    return value;
}
```

<span data-ttu-id="c92dd-162">Beachten Sie, dass dieses Beispiel immer nur `Measure` auf einzelnen Qubits nacheinander durchführt, aber der Vorgang kann auf gemeinsame Messungen für mehrere Qubits erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="c92dd-162">Note that this example still only performs `Measure` on individual qubits one at a time, but the operation can be extended to joint measurements on multiple qubits.</span></span>

## <a name="borrowing-qubits-example"></a><span data-ttu-id="c92dd-163">Beispiel für das Ausleihen von Qubits</span><span class="sxs-lookup"><span data-stu-id="c92dd-163">Borrowing Qubits Example</span></span>

<span data-ttu-id="c92dd-164">Es gibt Beispiele im Kanon, die das `borrowing` Schlüsselwort verwenden, wie z. b. die folgende Funktion `MultiControlledXBorrow` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-164">There are examples in the canon that use the `borrowing` keyword, such as the following function `MultiControlledXBorrow`.</span></span> <span data-ttu-id="c92dd-165">Wenn `controls` die einem Vorgang hinzu zufügenden Steuerelement-Qubits bezeichnet `X` , ist die Anzahl der von dieser Implementierung hinzugefügten modifizierten [ancillas](xref:microsoft.quantum.glossary#ancilla) `Length(controls)-2` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-165">If `controls` denotes the control qubits to add to an `X` operation, then the number of dirty [ancillas](xref:microsoft.quantum.glossary#ancilla) added by this implementation is `Length(controls)-2`.</span></span>

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

<span data-ttu-id="c92dd-166">Beachten Sie, dass in diesem Beispiel die kombinierte Verwendung von `With` Combinator in seiner Form verwendet wird, die für Vorgänge anwendbar ist, die Adjoint unterstützen, z `WithA` . b..</span><span class="sxs-lookup"><span data-stu-id="c92dd-166">Note that this example used extensive use of the `With` combinator, in its form that is applicable for operations that support adjoint, for example, `WithA`.</span></span>
<span data-ttu-id="c92dd-167">Dies ist ein guter Programmierstil, da das Hinzufügen von Steuerelementen zu Strukturen, die das Steuerelement in einbeziehen, `With` nur an den inneren Vorgang</span><span class="sxs-lookup"><span data-stu-id="c92dd-167">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="c92dd-168">Beachten Sie außerdem, dass zusätzlich zum `body` des Vorgangs eine Implementierung des Texts `controlled` des Vorgangs explizit bereitgestellt wurde, anstatt auf eine-Anweisung zurückzugreifen `controlled auto` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-168">Also note that, in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="c92dd-169">Der Grund hierfür ist, dass es aufgrund der Struktur der Verbindung einfach ist, weitere Steuerelemente hinzuzufügen. Dies ist im Vergleich zum Hinzufügen des Steuer Elements zu jedem Gate in der von Vorteil `body` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-169">The reason for this is that, because of the structure of the circuit, it is easy to add further controls, which is beneficial compared to adding control to each gate in the `body`.</span></span> 

<span data-ttu-id="c92dd-170">Es ist aufschlussreich, diesen Code mit einer anderen Funktion zu vergleichen, die `MultiControlledXClean` das gleiche Ziel hat, eine Multiplikation gesteuerte Operation zu implementieren, bei der `X` jedoch mithilfe des-Mechanismus mehrere saubere Qubits verwendet werden `using` .</span><span class="sxs-lookup"><span data-stu-id="c92dd-170">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="c92dd-171">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c92dd-171">Next steps</span></span>

<span data-ttu-id="c92dd-172">Erfahren Sie mehr über die [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow) in Q# .</span><span class="sxs-lookup"><span data-stu-id="c92dd-172">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>