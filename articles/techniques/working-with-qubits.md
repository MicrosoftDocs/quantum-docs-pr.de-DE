---
title: Arbeiten mit Qubits
description: 'Arbeiten mit Qubits-Q #-Techniken'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: dc6db93dadc37534aece9624fe516125d919f8cd
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819993"
---
# <a name="working-with-qubits"></a>Arbeiten mit Qubits

Nachdem wir nun eine Vielzahl von verschiedenen Teilen der Q #-Sprache gesehen haben, können wir uns die Thick of IT ansehen und erfahren, wie Sie Qubits selbst verwenden können.

## <a name="allocating-qubits"></a>Zuordnen von Qubits

Zum Abrufen eines Qubit, das in Q # verwendet werden kann, weisen wir *Qubits* in einem `using` Block zu:

```qsharp
using (register = Qubit[5]) {
    // Do stuff...
}
```

Alle auf diese Weise zugeordneten Qubits beginnen mit "$ \ket{0}$ State;". im obigen Beispiel befindet sich `register` daher im Status $ \ket{00000} = \ket{0} \otimes \ket{0} \otimes \cdots \otimes \ket{0}$.
Am Ende des `using`-Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.

> [!WARNING]
> Auf den Ziel Computern wird erwartet, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im $ \ket{0}$-Status befinden, damit Sie wieder verwendet und für die Zuordnung für andere `using` Blöcke angeboten werden können.
> Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket{0}$ zurückzugeben.
> Wenn dies erforderlich ist, kann der @"microsoft.quantum.intrinsic.reset" Vorgang verwendet werden, um stattdessen ein Qubit zu messen und dieses Messergebnis zu verwenden, um sicherzustellen, dass das gemessene Qubit an "$ \ket{0}$" zurückgegeben wird. Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.

## <a name="intrinsic-operations"></a>Intrinsische Vorgänge

Nach der Zuordnung kann ein Qubit an Funktionen und Vorgänge weitergegeben werden.
In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.
Diese Vorgänge werden in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)ausführlicher angezeigt. vorerst werden jedoch einige nützliche Vorgänge erwähnt, die für die Interaktion mit Qubits verwendet werden können.

Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge `X`, `Y`und `Z`dargestellt, von denen jeder über den Typ `(Qubit => Unit is Adj + Ctl)`verfügt.
Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, können wir uns $X $ und somit `X` als bitflip-Vorgang oder nicht als Gate vorstellen.
Mit dem `X` Vorgang können wir die Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorbereiten $s $:

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
> Später werden weitere kompakte Methoden zum Schreiben dieses Vorgangs angezeigt, für die keine manuelle Fluss Steuerung erforderlich ist.

Wir können auch Zustände wie $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ und $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ mithilfe der Hadamard Transform $H $, das in Q # durch den systeminternen Vorgang `H : (Qubit => Unit is Adj + Ctl)`dargestellt wird:

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

## <a name="measurements"></a>Messungen

Mithilfe des `Measure`-Vorgangs, bei dem es sich um einen integrierten intrinsischen nicht einheitlichen Vorgang handelt, können wir klassische Informationen aus einem Objekt des Typs `Qubit` extrahieren und einen klassischen Wert als Ergebnis zuweisen, der über einen reservierten Typ `Result`verfügt. Dies deutet darauf hin, dass das Ergebnis kein Quantum-Zustand mehr ist.
Die Eingabe für `Measure` ist eine Pauli-Achse in der Bloch-Kugel, die durch einen Wert vom Typ `Pauli` (z.b. `PauliX`) und einen Wert vom Typ `Qubit`dargestellt wird.

Ein einfaches Beispiel ist der folgende Vorgang, bei dem ein Qubit im $ \ket{0}$ State zugewiesen wird. Anschließend wird ein Hadamard-Vorgang `H` darauf angewendet und das Ergebnis auf `PauliZ` Basis gemessen.

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

Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert `true` zurückgibt, wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli gemessen werden, und der andernfalls `false` zurückgibt.

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

Die Q #-Sprache ermöglicht eine klassische Ablauf Steuerung, die von den Ergebnissen der Messung von Qubits abhängig ist.
Diese Funktion ermöglicht es wiederum, leistungsfähige, probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.
Beispielsweise ist es einfach, so genannte *Wiederholungs-bis-Erfolg-* Muster (RUS) in Q # zu implementieren.
Diese RUS-Muster sind probabilistische Programme, deren Kosten in Bezug auf elementare Gates *erwartungsgemäß* sind, aber für die die echten Kosten von einem tatsächlichen Testlauf und einem tatsächlichen Austausch der verschiedenen möglichen Verzweigungen abhängen.

Zum Vereinfachen von Wiederholungs-bis-Erfolg-Mustern (RUS) unterstützt Q # das-Konstrukt.

```qsharp
repeat {
    statementBlock1
}
until (expression)
fixup {
    statementBlock2
}
```

Dabei sind `statementBlock1` und `statementBlock2` keine oder mehrere Q #-Anweisungen, und `expression` alle gültigen Ausdrücke, die zu einem Wert vom Typ `Bool`ausgewertet werden.
In einem typischen Anwendungsfall implementiert der folgende Q #-Vorgang eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt{5}$ in der Bloch-Kugel. Dies wird mit einem bekannten RUS-Muster erreicht:

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

Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen `finished` die sich im Gültigkeitsbereich der gesamten Repeat-Until-Fixup-Schleife befindet und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.

Zum Schluss zeigen wir ein Beispiel eines RUS-Musters zum Vorbereiten des Quantums $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, beginnend ab dem $ \ket{+} $-Status.
Siehe auch das [Beispiel für Komponententests, das mit der Standardbibliothek bereitgestellt](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)wird:

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

Wichtige programmgesteuerte Features, die in diesem Vorgang gezeigt werden, sind eine komplexere `fixup` Teil der Schleife, die Quantum-Vorgänge einschließt, und die Verwendung von `AssertProb`-Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantum-Zustand an bestimmten angegebenen Punkten im Programm gemessen wird.
Weitere Informationen zu den [`Assert`](xref:microsoft.quantum.intrinsic.assert) -und [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) Vorgängen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging) .
