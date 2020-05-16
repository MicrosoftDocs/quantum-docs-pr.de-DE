---
title: Arbeiten mit Qubits
description: füllbeschreibung
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: e89b9ccfe2a0796e01eedfc99f7ce71038d85f38
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430933"
---
# <a name="working-with-qubits"></a><span data-ttu-id="95f37-103">Arbeiten mit Qubits</span><span class="sxs-lookup"><span data-stu-id="95f37-103">Working with qubits</span></span>

<span data-ttu-id="95f37-104">Nachdem wir nun eine Vielzahl von verschiedenen Teilen der Q #-Sprache gesehen haben, können wir uns die Thick of IT ansehen und erfahren, wie Sie Qubits selbst verwenden können.</span><span class="sxs-lookup"><span data-stu-id="95f37-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

<span data-ttu-id="95f37-105">Beachten Sie, dass keine dieser Anweisungen innerhalb des Texts einer Funktion zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="95f37-105">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="95f37-106">Sie sind nur innerhalb von Vorgängen gültig.</span><span class="sxs-lookup"><span data-stu-id="95f37-106">They are only valid within operations.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="95f37-107">Zuordnen von Qubits</span><span class="sxs-lookup"><span data-stu-id="95f37-107">Allocating Qubits</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="95f37-108">Löschen von Qubits</span><span class="sxs-lookup"><span data-stu-id="95f37-108">Clean qubits</span></span>

<span data-ttu-id="95f37-109">Die- `using` Anweisung wird verwendet, um neue Qubits für die Verwendung während eines-Anweisungsblocks *zuzuordnen* .</span><span class="sxs-lookup"><span data-stu-id="95f37-109">The `using` statement is used to *allocate* new qubits for use during a statement block.</span></span>

<span data-ttu-id="95f37-110">Die-Anweisung besteht aus dem Schlüsselwort `using` , gefolgt von einer öffnenden Klammer `(` , einer Bindung, einer Schließ `)` enden Klammer und dem Anweisungsblock, in dem die Qubits verfügbar sein werden.</span><span class="sxs-lookup"><span data-stu-id="95f37-110">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="95f37-111">Die Bindung folgt demselben Muster wie `let` -Anweisungen: entweder ein einzelnes Symbol oder ein Tupel von Symbolen, gefolgt von einem Gleichheitszeichen `=` und entweder ein einzelner Wert oder ein entsprechendes Tupel von *Initialisierern*.</span><span class="sxs-lookup"><span data-stu-id="95f37-111">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of *initializers*.</span></span>

<span data-ttu-id="95f37-112">Initialisierer sind entweder für ein einzelnes Qubit, das als angegeben ist, `Qubit()` oder ein Array von Qubits verfügbar, `Qubit[n]` wobei `n` ein `Int` Ausdruck ist.</span><span class="sxs-lookup"><span data-stu-id="95f37-112">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, `Qubit[n]`, where `n` is an `Int` expression.</span></span>
<span data-ttu-id="95f37-113">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="95f37-113">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

<span data-ttu-id="95f37-114">Alle auf diese Weise zugeordneten Qubits beginnen im Zustand "$ \ket {0} $". im obigen Beispiel `register` befindet sich daher im Zustand "$ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $".</span><span class="sxs-lookup"><span data-stu-id="95f37-114">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="95f37-115">Am Ende des- `using` Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95f37-115">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="95f37-116">Zielcomputer erwarten, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im Zustand $ \ket {0} $ befinden, damit Sie wieder verwendet und für die Zuordnung anderen Blöcken angeboten werden können `using` .</span><span class="sxs-lookup"><span data-stu-id="95f37-116">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="95f37-117">Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket $ zurückzugeben {0} .</span><span class="sxs-lookup"><span data-stu-id="95f37-117">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="95f37-118">Wenn dies erforderlich ist, @"microsoft.quantum.intrinsic.reset" kann der Vorgang verwendet werden, um stattdessen ein Qubit zu messen und dieses Messergebnis zu verwenden, um sicherzustellen, dass das gemessene Qubit an "$ \ket $" zurückgegeben wird {0} .</span><span class="sxs-lookup"><span data-stu-id="95f37-118">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="95f37-119">Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.</span><span class="sxs-lookup"><span data-stu-id="95f37-119">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>


### <a name="borrowed-qubits"></a><span data-ttu-id="95f37-120">Geliehene Qubits</span><span class="sxs-lookup"><span data-stu-id="95f37-120">Borrowed Qubits</span></span>

<span data-ttu-id="95f37-121">Die- `borrowing` Anweisung wird verwendet, um Qubits für die temporäre Verwendung verfügbar zu machen, die sich nicht in einem bestimmten Zustand befinden müssen.</span><span class="sxs-lookup"><span data-stu-id="95f37-121">The `borrowing` statement is used to make qubits available for temporary use, which do not need be in a specific state.</span></span>

<span data-ttu-id="95f37-122">Der Mechanismus zum ableihen ermöglicht die Zuordnung von Qubits, die während einer Berechnung als Scratch-Speicherplatz verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="95f37-122">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span>
<span data-ttu-id="95f37-123">Diese Qubits befinden sich in der Regel nicht in einem sauberen Zustand, d. h., Sie werden nicht notwendigerweise in einem bekannten Zustand initialisiert, wie z. b. $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="95f37-123">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span>
<span data-ttu-id="95f37-124">Diese werden häufig als "modifizierte" Qubits bezeichnet, da ihr Zustand unbekannt ist und sogar mit anderen Teilen des Arbeitsspeichers des Quantums Computers entkoppelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="95f37-124">These are often referred to as "dirty" qubits because their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span>

<span data-ttu-id="95f37-125">Die Bindung folgt demselben Muster und denselben Regeln wie in einer- `using` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="95f37-125">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>
<span data-ttu-id="95f37-126">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="95f37-126">For example,</span></span>
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
<span data-ttu-id="95f37-127">Die geliehenen Qubits befinden sich in einem unbekannten Zustand und verlassen den Gültigkeitsbereich am Ende des Anweisungsblocks.</span><span class="sxs-lookup"><span data-stu-id="95f37-127">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="95f37-128">Der Kreditnehmer führt einen Commit aus, um die Qubits in demselben Zustand zu belassen, in dem Sie sich befanden, d. h., ihr Zustand am Anfang und am Ende des Anweisungsblocks ist erwartungsgemäß identisch.</span><span class="sxs-lookup"><span data-stu-id="95f37-128">The borrower commits to leaving the qubits in the same state they were in when they were borrowed,  i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="95f37-129">Dabei handelt es sich nicht unbedingt um einen klassischen Zustand, der in den meisten Fällen keine Messungen enthalten sollte.</span><span class="sxs-lookup"><span data-stu-id="95f37-129">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="95f37-130">Beim Abgleich von Qubits versucht das System zunächst, die Anforderung von Qubits auszufüllen, die verwendet werden, aber nicht während des Texts der Anweisung darauf zugegriffen wird `borrowing` .</span><span class="sxs-lookup"><span data-stu-id="95f37-130">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="95f37-131">Wenn nicht genügend derartige Qubits vorhanden sind, werden neue Qubits zum Durchführen der Anforderung zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="95f37-131">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>


<span data-ttu-id="95f37-132">Zu den bekannten Anwendungsfällen von Dirty Qubits zählen Implementierungen von multigesteuerten CNOT Gates, die nur sehr wenige Qubits und die Implementierung von inkrementern erfordern.</span><span class="sxs-lookup"><span data-stu-id="95f37-132">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>
<span data-ttu-id="95f37-133">Im folgenden [Beispiel](#borrowing-qubits-example) finden Sie ein Beispiel für die Verwendung in Q # oder das Paper [*Factoring mit 2n + 2 Qubits mit auf Toffoli basierender modularer Multiplikation*](https://arxiv.org/abs/1611.07995) (Haner, roetteler und svore 2017) für einen Algorithmus, der geliehene Qubits verwendet.</span><span class="sxs-lookup"><span data-stu-id="95f37-133">See the [Borrowing Qubits Example](#borrowing-qubits-example) below to see an example of their use in Q#, or the paper [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an algorithm which utilizes borrowed qubits.</span></span>


## <a name="intrinsic-operations"></a><span data-ttu-id="95f37-134">Intrinsische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="95f37-134">Intrinsic Operations</span></span>

<span data-ttu-id="95f37-135">Nach der Zuordnung kann ein Qubit an Funktionen und Vorgänge weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95f37-135">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="95f37-136">In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.</span><span class="sxs-lookup"><span data-stu-id="95f37-136">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="95f37-137">Diese Vorgänge werden in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)ausführlicher angezeigt. vorerst werden jedoch einige nützliche Vorgänge erwähnt, die für die Interaktion mit Qubits verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="95f37-137">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="95f37-138">Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge `X` , `Y` und dargestellt, die jeweils den- `Z` Typ haben `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="95f37-138">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="95f37-139">Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, können wir uns $X $ und somit auch `X` als bitflip-Vorgang oder nicht als Gate vorstellen.</span><span class="sxs-lookup"><span data-stu-id="95f37-139">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="95f37-140">`X`Mit dem Vorgang können wir die Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorbereiten $s $:</span><span class="sxs-lookup"><span data-stu-id="95f37-140">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
        // Resetting the qubits will allow us to deallocate them properly.
        ResetAll(register);
    }
}
```

> [!TIP]
> <span data-ttu-id="95f37-141">Später werden weitere kompakte Methoden zum Schreiben dieses Vorgangs angezeigt, für die keine manuelle Fluss Steuerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="95f37-141">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="95f37-142">Wir können auch die Zustände, wie z. b. $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ und $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $, mithilfe der Hadamard Transform $H $ vorbereiten, die in Q # durch den intrinsischen Vorgang dargestellt wird `H : (Qubit => Unit is Adj + Ctl)` :</span><span class="sxs-lookup"><span data-stu-id="95f37-142">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

```qsharp
operation PreparePlusMinusState(bitstring : Bool[], register : Qubit[]) : Unit {
    // First, get a computational basis state of the form
    // |s_0 s_1 ... s_n〉 by using PrepareBitString, above.
    PrepareBitString(bitstring, register);
    // Next, we use that |+〉 = H|0〉 and |-〉 = H|1〉 to
    // prepare the state we want.
    for (idxQubit in IndexRange(register)) {
        H(register[idxQubit]);
    }
}
```

## <a name="measurements"></a><span data-ttu-id="95f37-143">Messungen</span><span class="sxs-lookup"><span data-stu-id="95f37-143">Measurements</span></span>

<span data-ttu-id="95f37-144">Mithilfe des `Measure` -Vorgangs, bei dem es sich um eine integrierte intrinsische, nicht einheitliche Operation handelt, können wir klassische Informationen aus einem Objekt des Typs extrahieren `Qubit` und einen klassischen Wert als Ergebnis zuweisen, der einen reservierten Typ aufweist und `Result` angibt, dass das Ergebnis nicht mehr ein Quantum-Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="95f37-144">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="95f37-145">Die Eingabe für `Measure` ist eine Pauli-Achse in der Bloch-Kugel, die durch einen Wert des Typs `Pauli` (z.b. `PauliX` ) und einen Wert des Typs dargestellt wird `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="95f37-145">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="95f37-146">Ein einfaches Beispiel ist der folgende Vorgang, der ein Qubit im $ \ket $-Zustand zuordnet {0} , dann einen Hadamard-Vorgang `H` darauf anwendet und das Ergebnis in der `PauliZ` Basis misst.</span><span class="sxs-lookup"><span data-stu-id="95f37-146">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="95f37-147">Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert zurückgibt, `true` Wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli-Basis gemessen werden und andernfalls andernfalls zurückgegeben werden `false` .</span><span class="sxs-lookup"><span data-stu-id="95f37-147">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

## <a name="borrowing-qubits-example"></a><span data-ttu-id="95f37-148">Beispiel für das Ausleihen von Qubits</span><span class="sxs-lookup"><span data-stu-id="95f37-148">Borrowing Qubits Example</span></span>

<span data-ttu-id="95f37-149">Im Kanon finden Sie Beispiele, in denen das `borrowing` Schlüsselwort verwendet wird, z.b. die `MultiControlledXBorrow` unten definierte Funktion.</span><span class="sxs-lookup"><span data-stu-id="95f37-149">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="95f37-150">Wenn `controls` die Steuerelement-Qubits bezeichnet, die einem Vorgang hinzugefügt werden sollen `X` , `Length(controls)-2` wird durch diese Implementierung eine Gesamtzahl von vielen modifizierten ancillas hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="95f37-150">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

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

<span data-ttu-id="95f37-151">Beachten Sie, dass die kombinierte Verwendung der `With` Combinator----in der Form, die für Vorgänge anwendbar ist, die Adjoint unterstützen, d. h. `WithA` ---in diesem Beispiel erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95f37-151">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example.</span></span>
<span data-ttu-id="95f37-152">Dies ist ein guter Programmierstil, da das Hinzufügen von Steuerelementen zu Strukturen, die das Steuerelement in einbeziehen, `With` nur an den inneren Vorgang</span><span class="sxs-lookup"><span data-stu-id="95f37-152">This is good programming style, because adding control to structures involving `With` propagates control only to the inner operation.</span></span>
<span data-ttu-id="95f37-153">Beachten Sie, dass hier zusätzlich zum `body` des Vorgangs eine Implementierung des Texts `controlled` des Vorgangs explizit bereitgestellt wurde, anstatt auf eine-Anweisung zurückzugreifen `controlled auto` .</span><span class="sxs-lookup"><span data-stu-id="95f37-153">Further, note that here in addition to the `body` of the operation, an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span>
<span data-ttu-id="95f37-154">Der Grund hierfür ist, dass wir aus der Struktur der Verbindung wissen, wie Sie ganz einfach weitere Steuerelemente hinzufügen können, die im Vergleich zum Hinzufügen von Steuerelementen zu jedem einzelnen Gate in der von Vorteil sind `body` .</span><span class="sxs-lookup"><span data-stu-id="95f37-154">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="95f37-155">Es ist aufschlussreich, diesen Code mit einer anderen Funktion zu vergleichen, die `MultiControlledXClean` das gleiche Ziel hat, eine Multiplikation gesteuerte Operation zu implementieren, bei der `X` jedoch mithilfe des-Mechanismus mehrere saubere Qubits verwendet werden `using` .</span><span class="sxs-lookup"><span data-stu-id="95f37-155">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 

## <a name="whats-next"></a><span data-ttu-id="95f37-156">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="95f37-156">What's Next?</span></span>
<span data-ttu-id="95f37-157">Erfahren Sie mehr über die [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow) in f #.</span><span class="sxs-lookup"><span data-stu-id="95f37-157">Learn about [Control Flow](xref:microsoft.quantum.guide.controlflow) in Q#.</span></span>