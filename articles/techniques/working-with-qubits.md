---
title: Arbeiten mit Qubits | Microsoft-Dokumentation
description: Arbeiten mit Qubits
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: 477b358c3eba58b62926b4e9094770c9741cac92
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864252"
---
# <a name="working-with-qubits"></a><span data-ttu-id="fae03-103">Arbeiten mit Qubits</span><span class="sxs-lookup"><span data-stu-id="fae03-103">Working with Qubits</span></span> #

<span data-ttu-id="fae03-104">Nachdem wir nun eine Vielzahl von verschiedenen Teilen der Q #-Sprache gesehen haben, können wir uns die Thick of IT ansehen und erfahren, wie Sie Qubits selbst verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fae03-104">Having now seen a variety of different parts of the Q# language, let us get into the thick of it and see how to use qubits themselves.</span></span>

## <a name="allocating-qubits"></a><span data-ttu-id="fae03-105">Speicherbelegung für Qubits</span><span class="sxs-lookup"><span data-stu-id="fae03-105">Allocating Qubits</span></span> ##

<span data-ttu-id="fae03-106">Zum Abrufen eines Qubit, das in Q # verwendet werden kann, weisen wir *Qubits* in einem `using` Block zu:</span><span class="sxs-lookup"><span data-stu-id="fae03-106">First, to obtain a qubit that we can use in Q#, we *allocate* qubits within a `using` block:</span></span>

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

<span data-ttu-id="fae03-107">Alle auf diese Weise zugeordneten Qubits beginnen mit "$ \ket{0}$ State;". im obigen Beispiel befindet sich `register` daher im Status $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="fae03-107">Any qubits allocated in this way start off in the $\ket{0}$ state; in the example above, `register` is thus in the state $\ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.</span></span>
<span data-ttu-id="fae03-108">Am Ende des `using`-Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fae03-108">At the end of the `using` block, any qubits allocated by that block are immediately deallocated and cannot be used further.</span></span>

> [!WARNING]
> <span data-ttu-id="fae03-109">Auf den Ziel Computern wird erwartet, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im $ \ket{0}$-Status befinden, damit Sie wieder verwendet und für die Zuordnung für andere `using` Blöcke angeboten werden können.</span><span class="sxs-lookup"><span data-stu-id="fae03-109">Target machines expect that qubits are in the $\ket{0}$ state immediately before deallocation, so that they can be reused and offered to other `using` blocks for allocation.</span></span>
> <span data-ttu-id="fae03-110">Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket{0}$ zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fae03-110">Whenever possible, use unitary operations to return any allocated qubits to $\ket{0}$.</span></span>
> <span data-ttu-id="fae03-111">Wenn dies erforderlich ist, kann der @"microsoft.quantum.intrinsic.reset" Vorgang verwendet werden, um stattdessen ein Qubit zu messen und dieses Messergebnis zu verwenden, um sicherzustellen, dass das gemessene Qubit an "$ \ket{0}$" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fae03-111">If need be, the @"microsoft.quantum.intrinsic.reset" operation can be used to measure a qubit instead, and to use that measurement result to ensure that the measured qubit is returned to $\ket{0}$.</span></span> <span data-ttu-id="fae03-112">Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.</span><span class="sxs-lookup"><span data-stu-id="fae03-112">Such a measurement will destroy any entanglement with the remaining qubits and can thus impact the computation.</span></span> 

## <a name="intrinsic-operations"></a><span data-ttu-id="fae03-113">Intrinsische Vorgänge</span><span class="sxs-lookup"><span data-stu-id="fae03-113">Intrinsic Operations</span></span> ##

<span data-ttu-id="fae03-114">Nach der Zuordnung kann ein Qubit an Funktionen und Vorgänge weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fae03-114">Once allocated, a qubit can then be passed to functions and operations.</span></span>
<span data-ttu-id="fae03-115">In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.</span><span class="sxs-lookup"><span data-stu-id="fae03-115">In some sense, this is all that a Q# program can do with a qubit, as the actions that can be taken are all defined as operations.</span></span>
<span data-ttu-id="fae03-116">Diese Vorgänge werden in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)ausführlicher angezeigt. vorerst werden jedoch einige nützliche Vorgänge erwähnt, die für die Interaktion mit Qubits verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="fae03-116">We will see these operations in more detail in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), but for now, we mention a few useful operations that can be used to interact with qubits.</span></span>

<span data-ttu-id="fae03-117">Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge `X`, `Y`und `Z`dargestellt, von denen jeder über den Typ `(Qubit => Unit is Adj + Ctl)`verfügt.</span><span class="sxs-lookup"><span data-stu-id="fae03-117">First, the single-qubit Pauli operators $X$, $Y$, and $Z$ are represented in Q# by the intrinsic operations `X`, `Y`, and `Z`, each of which has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="fae03-118">Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, können wir uns $X $ und somit `X` als bitflip-Vorgang oder nicht als Gate vorstellen.</span><span class="sxs-lookup"><span data-stu-id="fae03-118">As described in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude), we can think of $X$ and hence of `X` as a bit-flip operation or NOT gate.</span></span>
<span data-ttu-id="fae03-119">Auf diese Weise können wir die Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorbereiten $s $:</span><span class="sxs-lookup"><span data-stu-id="fae03-119">This lets us prepare states of the form $\ket{s_0 s_1 \dots s_n}$ for some classical bit string $s$:</span></span>

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

operation Example() : Unit {

    using (register = Qubit[8]) {
        PrepareBitString(
            [true, true, false, false, true, false, false, true],
            register
        );
        // At this point, register now has the state |11001001〉.
    }
}
```

> [!TIP]
> <span data-ttu-id="fae03-120">Später werden weitere kompakte Methoden zum Schreiben dieses Vorgangs angezeigt, für die keine manuelle Fluss Steuerung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fae03-120">Later, we will see more compact ways of writing this operation that do not require manual flow control.</span></span>

<span data-ttu-id="fae03-121">Wir können auch Zustände wie $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ und $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ mithilfe der Hadamard Transform $H $, das in Q # durch den systeminternen Vorgang `H : (Qubit => Unit is Adj + Ctl)`dargestellt wird:</span><span class="sxs-lookup"><span data-stu-id="fae03-121">We can also prepare states such as $\ket{+} = \left(\ket{0} + \ket{1}\right) / \sqrt{2}$ and $\ket{-} = \left(\ket{0} - \ket{1}\right) / \sqrt{2}$ by using the Hadamard transform $H$, which is represented in Q# by the intrinsic operation `H : (Qubit => Unit is Adj + Ctl)`:</span></span>

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

## <a name="measurements"></a><span data-ttu-id="fae03-122">Measurements (Messungen)</span><span class="sxs-lookup"><span data-stu-id="fae03-122">Measurements</span></span> ##

<span data-ttu-id="fae03-123">Mithilfe des `Measure`-Vorgangs, bei dem es sich um einen integrierten, systeminternen, nicht einheitlichen Vorgang handelt, können wir klassische Informationen aus einem Objekt des Typs `Qubit` extrahieren und einen klassischen Wert als Ergebnis zuweisen, der einen reservierten Typ hat `Result`, der angibt, dass das Ergebnis nicht mehr ein Quantum-Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="fae03-123">Using the `Measure` operation, which is a built in intrinsic non-unitary operation, we can extract classical information from an object of type `Qubit` and assign a classical value as a result, which has a reserved type `Result`, indicating that the result is no longer a quantum state.</span></span> <span data-ttu-id="fae03-124">Die Eingabe für `Measure` ist eine Pauli-Achse in der Bloch-Kugel, die durch ein Objekt vom Typ `Pauli` (z. BB`PauliX`) und ein Objekt vom Typ `Qubit`dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fae03-124">The input to `Measure` is a Pauli axis on the Bloch sphere, represented by an object of type `Pauli` (i.e., for instance `PauliX`) and an object of type `Qubit`.</span></span> 

<span data-ttu-id="fae03-125">Ein einfaches Beispiel ist der folgende Vorgang, bei dem ein Qubit im $ \ket-{0}$ State erstellt wird. Anschließend wird ein Hadamard-Gate ``H`` darauf angewendet, und dann wird das Ergebnis auf `PauliZ` Basis gemessen.</span><span class="sxs-lookup"><span data-stu-id="fae03-125">A simple example is the following operation which creates one qubit in the $\ket{0}$ state, then applies a Hadamard gate ``H`` to it and then measures the result in the `PauliZ` basis.</span></span> 

```qsharp
operation MeasurementOneQubit () : Result {

    // The following using block creates a fresh qubit and initializes it 
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby creating the 
        // state 1/sqrt(2)(|0〉+|1〉). 
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

<span data-ttu-id="fae03-126">Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert `true` zurückgibt, wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli-Basis gemessen werden und andernfalls `false`.</span><span class="sxs-lookup"><span data-stu-id="fae03-126">A slightly more complicated example is given by the following operation which returns the Boolean value `true` if all qubits in a register of type `Qubit[]` are in the state zero, when measured in a specified Pauli basis and `false` otherwise.</span></span> 

```qsharp
operation AllMeasurementsZero (qs : Qubit[], pauli : Pauli) : Bool {

    mutable value = true;
    for (q in qs) {
        if ( Measure([pauli], [q]) == One ) {
            set value = false;
        }
    }
    return value;
}
```

<span data-ttu-id="fae03-127">Die Q #-Sprache ermöglicht Abhängigkeiten der klassischen Ablauf Steuerung bei Messergebnissen von Qubits.</span><span class="sxs-lookup"><span data-stu-id="fae03-127">The Q# language allows dependencies of classical control flow on measurement results of qubits.</span></span> <span data-ttu-id="fae03-128">Dies wiederum ermöglicht es, leistungsstarke, probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="fae03-128">This in turn enables to implement powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span> <span data-ttu-id="fae03-129">Beispielsweise ist es einfach, eine so genannte *Wiederholung bis zum Erfolg* in Q # zu implementieren, bei der es sich um probabilistische Verbindungen handelt, die in Bezug auf elementare Gates *erwartete* niedrige Kosten aufweisen, aber für die die echten Kosten von einem tatsächlichen Testlauf und einem tatsächlichen Austausch der verschiedenen möglichen Verzweigungen abhängen.</span><span class="sxs-lookup"><span data-stu-id="fae03-129">As an example, it is easy to implement so-called *Repeat-Until-Success* in Q# which are probabilistic circuits that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span> 

<span data-ttu-id="fae03-130">Zum Vereinfachen von Wiederholungs-bis-Erfolg-Mustern (RUS) unterstützt Q # das-Konstrukt.</span><span class="sxs-lookup"><span data-stu-id="fae03-130">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the construct</span></span>
```qsharp
repeat {
    statementBlock1 
}
until (expression)
fixup {
    statementBlock2
}
```
<span data-ttu-id="fae03-131">Dabei sind `statementBlock1` und `statementBlock2` keine oder mehrere Q #-Anweisungen, und `expression` alle gültigen Ausdrücke, die zu einem Wert vom Typ `Bool`ausgewertet werden.</span><span class="sxs-lookup"><span data-stu-id="fae03-131">where `statementBlock1` and `statementBlock2` are zero or more Q# statements, and `expression` any valid expression that evaluates to a value of type `Bool`.</span></span> <span data-ttu-id="fae03-132">In einem typischen Anwendungsfall implementiert die folgende Verbindung eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt{5}$ in der Bloch-Kugel.</span><span class="sxs-lookup"><span data-stu-id="fae03-132">In a typical use case, the following circuit implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="fae03-133">Dies wird mit einem bekannten RUS-Muster erreicht:</span><span class="sxs-lookup"><span data-stu-id="fae03-133">This is accomplished by using a known RUS pattern:</span></span> 

```qsharp
operation RUScircuit (qubit : Qubit) : Unit {

    using(ancillas = Qubit[2]) {
        ApplyToEachA(H, ancillas);
        mutable finished = false;
        repeat {
            Controlled X(ancillas, qubit);
            S(qubit);
            Controlled X(ancillas, qubit);
            Z(qubit);
        }
        until(finished)
        fixup {
            if AllMeasurementsZero(ancillas, Xpauli) {
                set finished = true;
            }
        }
    }
}
```

<span data-ttu-id="fae03-134">Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen `finished` die sich im Gültigkeitsbereich der gesamten Repeat-Until-Fixup-Schleife befindet und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="fae03-134">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

<span data-ttu-id="fae03-135">Zum Schluss zeigen wir ein Beispiel eines RUS-Musters zum Vorbereiten des Quantums $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, beginnend ab dem $ \ket{+} $-Status.</span><span class="sxs-lookup"><span data-stu-id="fae03-135">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span> <span data-ttu-id="fae03-136">Siehe auch das [Beispiel für Komponententests, das mit der Standardbibliothek bereitgestellt](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)wird:</span><span class="sxs-lookup"><span data-stu-id="fae03-136">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span> 

```qsharp
operation RepeatUntilSuccessStatePreparation( target : Qubit ) : Unit {

    using( ancilla = Qubit() ) {
        H(ancilla);
        repeat {
            // We expect target and ancilla qubit to be in |+⟩ state.
            AssertProb( 
                [PauliX], [target], Zero, 1.0, 
                "target qubit should be in the |+⟩ state", 1e-10 );
            AssertProb( 
                [PauliX], [ancilla], Zero, 1.0,
                "ancilla qubit should be in the |+⟩ state", 1e-10 );
                
            Adjoint T(ancilla);
            CNOT(target, ancilla);
            T(ancilla);

            // The probability of measuring |+⟩ state on ancilla is 3/4.
            AssertProb( 
                [PauliX], [ancilla], Zero, 3. / 4., 
                "Error: the probability to measure |+⟩ in the first 
                ancilla must be 3/4",
                1e-10);

            // If we get measurement outcome Zero, we prepare the required state 
            let outcome = Measure([PauliX], [ancilla]);
        }
        until( outcome == Zero )
        fixup {
            // Bring ancilla and target back to |+⟩ state
            if( outcome == One ) {
                Z(ancilla);
                X(target);
                H(target);
            }
        }
        // Return ancilla back to Zero state
        H(ancilla);
    }
}
```
 
<span data-ttu-id="fae03-137">Wichtige programmgesteuerte Features, die in diesem Vorgang gezeigt werden, sind eine komplexere `fixup` Teil der Schleife, die Quantum-Vorgänge einschließt, und die Verwendung von `AssertProb`-Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantum-Zustand an bestimmten angegebenen Punkten im Programm gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="fae03-137">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span> <span data-ttu-id="fae03-138">Weitere Informationen zu `Assert`-und `AssertProb`-Anweisungen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging) .</span><span class="sxs-lookup"><span data-stu-id="fae03-138">See also [Testing and debugging](xref:microsoft.quantum.techniques.testing-and-debugging) for more information about `Assert` and `AssertProb` statements.</span></span> 
