---
title: Arbeiten mit Qubits
description: Erfahren Sie, wie Sie Qubits zuordnen, Sie in Vorgängen und Funktionen verwenden und die Ergebnisse messen.
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 1aa2432996dda61d099e3b5bb4db78379ce43d97
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907646"
---
# <a name="working-with-qubits"></a><span data-ttu-id="3b60e-103">Arbeiten mit Qubits</span><span class="sxs-lookup"><span data-stu-id="3b60e-103">Working with Qubits</span></span>

<span data-ttu-id="3b60e-104">Nachdem wir nun eine Vielzahl von verschiedenen Teilen der Q #-Sprache gesehen haben, können wir uns die Thick of IT ansehen und erfahren, wie Sie Qubits selbst verwenden können.</span><span class="sxs-lookup"><span data-stu-id="3b60e-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="3b60e-105">Zuordnen von Qubits</span><span class="sxs-lookup"><span data-stu-id="3b60e-105">Allocating Qubits</span></span>

<span data-ttu-id="3b60e-106">Zum Abrufen eines Qubit, das in Q # verwendet werden kann, weisen wir *Qubits* in einem `using` Block zu:</span><span class="sxs-lookup"><span data-stu-id="3b60e-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="3b60e-107">Alle auf diese Weise zugeordneten Qubits beginnen mit "$ \ket{0}$ State;". im obigen Beispiel befindet sich `register` daher im Status $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="3b60e-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="3b60e-108">Am Ende des `using`-Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b60e-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="3b60e-109">Auf den Ziel Computern wird erwartet, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im $ \ket{0}$-Status befinden, damit Sie wieder verwendet und für die Zuordnung für andere `using` Blöcke angeboten werden können.</span><span class="sxs-lookup"><span data-stu-id="3b60e-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="3b60e-110">Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket{0}$ zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="3b60e-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="3b60e-111">Wenn dies erforderlich ist, kann der @"microsoft.quantum.intrinsic.reset" Vorgang verwendet werden, um stattdessen ein Qubit zu messen und dieses Messergebnis zu verwenden, um sicherzustellen, dass das gemessene Qubit an "$ \ket{0}$" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b60e-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="3b60e-112">Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.</span><span class="sxs-lookup"><span data-stu-id="3b60e-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span>

## <a name="intrinsic-operations"></a><span data-ttu-id="3b60e-113">Intrinsische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="3b60e-113">Intrinsic Operations</span></span>

<span data-ttu-id="3b60e-114">Nach der Zuordnung kann ein Qubit an Funktionen und Vorgänge weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3b60e-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="3b60e-115">In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.</span><span class="sxs-lookup"><span data-stu-id="3b60e-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="3b60e-116">Diese Vorgänge werden in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)ausführlicher angezeigt. vorerst werden jedoch einige nützliche Vorgänge erwähnt, die für die Interaktion mit Qubits verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="3b60e-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="3b60e-117">Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge `X`, `Y`und `Z`dargestellt, von denen jeder über den Typ `(Qubit => Unit is Adj + Ctl)`verfügt.</span><span class="sxs-lookup"><span data-stu-id="3b60e-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="3b60e-118">Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, können wir uns $X $ und somit `X` als bitflip-Vorgang oder nicht als Gate vorstellen.</span><span class="sxs-lookup"><span data-stu-id="3b60e-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="3b60e-119">Mit dem `X` Vorgang können wir die Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorbereiten $s $:</span><span class="sxs-lookup"><span data-stu-id="3b60e-119">The `X` operation lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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
> <span data-ttu-id="3b60e-120">Später werden weitere kompakte Methoden zum Schreiben dieses Vorgangs angezeigt, für die keine manuelle Fluss Steuerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3b60e-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="3b60e-121">Wir können auch Zustände wie $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ und $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ mithilfe der Hadamard Transform $H $, das in Q # durch den systeminternen Vorgang `H : (Qubit => Unit is Adj + Ctl)`dargestellt wird:</span><span class="sxs-lookup"><span data-stu-id="3b60e-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="3b60e-122">Messungen</span><span class="sxs-lookup"><span data-stu-id="3b60e-122">Measurements</span></span>

<span data-ttu-id="3b60e-123">Mithilfe des `Measure`-Vorgangs, bei dem es sich um einen integrierten intrinsischen nicht einheitlichen Vorgang handelt, können wir klassische Informationen aus einem Objekt des Typs `Qubit` extrahieren und einen klassischen Wert als Ergebnis zuweisen, der über einen reservierten Typ `Result`verfügt. Dies deutet darauf hin, dass das Ergebnis kein Quantum-Zustand mehr ist.</span><span class="sxs-lookup"><span data-stu-id="3b60e-123">Using the `Measure` operation, which is a built-in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span>
<span data-ttu-id="3b60e-124">Die Eingabe für `Measure` ist eine Pauli-Achse in der Bloch-Kugel, die durch einen Wert vom Typ `Pauli` (z.b. `PauliX`) und einen Wert vom Typ `Qubit`dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b60e-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by a value of type `Pauli` (for instance `PauliX`) and an value of type `Qubit`.</span></span>

<span data-ttu-id="3b60e-125">Ein einfaches Beispiel ist der folgende Vorgang, bei dem ein Qubit im $ \ket{0}$ State zugewiesen wird. Anschließend wird ein Hadamard-Vorgang `H` darauf angewendet und das Ergebnis auf `PauliZ` Basis gemessen.</span><span class="sxs-lookup"><span data-stu-id="3b60e-125">A simple example is the following operation, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

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

<span data-ttu-id="3b60e-126">Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert `true` zurückgibt, wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli gemessen werden, und der andernfalls `false` zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3b60e-126">A slightly more complicated example is given by the following operation, which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero when measured in a specified Pauli basis, and which returns `false` otherwise.</span></span>

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

<span data-ttu-id="3b60e-127">Die Q #-Sprache ermöglicht eine klassische Ablauf Steuerung, die von den Ergebnissen der Messung von Qubits abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="3b60e-127">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="3b60e-128">Diese Funktion ermöglicht es wiederum, leistungsfähige, probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="3b60e-128">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="3b60e-129">Beispielsweise ist es einfach, so genannte *Wiederholungs-bis-Erfolg-* Muster (RUS) in Q # zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="3b60e-129">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="3b60e-130">Diese RUS-Muster sind probabilistische Programme, deren Kosten in Bezug auf elementare Gates *erwartungsgemäß* sind, aber für die die echten Kosten von einem tatsächlichen Testlauf und einem tatsächlichen Austausch der verschiedenen möglichen Verzweigungen abhängen.</span><span class="sxs-lookup"><span data-stu-id="3b60e-130">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="3b60e-131">Zum Vereinfachen von Wiederholungs-bis-Erfolg-Mustern (RUS) unterstützt Q # das-Konstrukt.</span><span class="sxs-lookup"><span data-stu-id="3b60e-131">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

<span data-ttu-id="3b60e-132">Dabei sind `statementBlock1` und `statementBlock2` keine oder mehrere Q #-Anweisungen, und `expression` alle gültigen Ausdrücke, die zu einem Wert vom Typ `Bool`ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="3b60e-132">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="3b60e-133">In einem typischen Anwendungsfall implementiert der folgende Q #-Vorgang eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt{5}$ in der Bloch-Kugel.</span><span class="sxs-lookup"><span data-stu-id="3b60e-133">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="3b60e-134">Dies wird mit einem bekannten RUS-Muster erreicht:</span><span class="sxs-lookup"><span data-stu-id="3b60e-134">This is accomplished by using a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

<span data-ttu-id="3b60e-135">Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen `finished` die sich im Gültigkeitsbereich der gesamten Repeat-Until-Fixup-Schleife befindet und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b60e-135">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="3b60e-136">Zum Schluss zeigen wir ein Beispiel eines RUS-Musters zum Vorbereiten des Quantums $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, beginnend ab dem $ \ket{+} $-Status.</span><span class="sxs-lookup"><span data-stu-id="3b60e-136">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="3b60e-137">Siehe auch das [Beispiel für Komponententests, das mit der Standardbibliothek bereitgestellt](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)wird:</span><span class="sxs-lookup"><span data-stu-id="3b60e-137">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+⟩ state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+⟩ state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+⟩ state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+⟩ in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+⟩ state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="3b60e-138">Wichtige programmgesteuerte Features, die in diesem Vorgang gezeigt werden, sind eine komplexere `fixup` Teil der Schleife, die Quantum-Vorgänge einschließt, und die Verwendung von `AssertProb`-Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantum-Zustand an bestimmten angegebenen Punkten im Programm gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="3b60e-138">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="3b60e-139">Weitere Informationen zu den [`Assert`](xref:microsoft.quantum.intrinsic.assert) -und [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) Vorgängen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging) .</span><span class="sxs-lookup"><span data-stu-id="3b60e-139">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>
