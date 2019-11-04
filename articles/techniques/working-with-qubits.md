---
title: Arbeiten mit Qubits | Microsoft-Dokumentation
description: Arbeiten mit Qubits
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.qubits
ms.openlocfilehash: d1a8ccc9423a9a04e12bc98e3783790232b2f5d8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183470"
---
# <a name="working-with-qubits"></a>Arbeiten mit Qubits #

Nachdem wir nun eine Vielzahl von verschiedenen Teilen der Q #-Sprache gesehen haben, können wir uns die Thick of IT ansehen und erfahren, wie Sie Qubits selbst verwenden können.

## <a name="allocating-qubits"></a>Zuordnen von Qubits ##

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

## <a name="intrinsic-operations"></a>Intrinsische Vorgänge ##

Nach der Zuordnung kann ein Qubit an Funktionen und Vorgänge weitergegeben werden.
In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.
Diese Vorgänge werden in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)ausführlicher angezeigt. vorerst werden jedoch einige nützliche Vorgänge erwähnt, die für die Interaktion mit Qubits verwendet werden können.

Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge `X`, `Y`und `Z`dargestellt, von denen jeder über den Typ `(Qubit => Unit is Adj + Ctl)`verfügt.
Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, können wir uns $X $ und somit `X` als bitflip-Vorgang oder nicht als Gate vorstellen.
Auf diese Weise können wir die Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für einige klassische Bitzeichenfolgen vorbereiten $s $:

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
> Später werden weitere kompakte Methoden zum Schreiben dieses Vorgangs angezeigt, für die keine manuelle Fluss Steuerung erforderlich ist.

Wir können auch die Zustände wie $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$ und $ \ket{-} = \left (\ket{0}-\ket{1}\right)/\sqrt{2}$ mithilfe der Hadamard Transform $H $ , der in f # durch den intrinsischen Vorgang `H : (Qubit => Unit is Adj + Ctl)`dargestellt wird:

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

## <a name="measurements"></a>Measurements (Messungen) ##

Mithilfe des `Measure`-Vorgangs, bei dem es sich um einen integrierten, systeminternen, nicht einheitlichen Vorgang handelt, können wir klassische Informationen aus einem Objekt des Typs `Qubit` extrahieren und einen klassischen Wert als Ergebnis zuweisen, der einen reservierten Typ hat `Result`, der angibt, dass das Ergebnis "No" ist. längerer quantumzustand. Die Eingabe für `Measure` ist eine Pauli-Achse in der Bloch-Kugel, die durch ein Objekt vom Typ `Pauli` (z. BB`PauliX`) und ein Objekt vom Typ `Qubit`dargestellt wird. 

Ein einfaches Beispiel ist der folgende Vorgang, bei dem ein Qubit im $ \ket-{0}$ State erstellt wird. Anschließend wird ein Hadamard-Gate ``H`` darauf angewendet, und dann wird das Ergebnis auf `PauliZ` Basis gemessen. 

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

Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert `true` zurückgibt, wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli-Basis gemessen werden und andernfalls `false`. 

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

Die Q #-Sprache ermöglicht Abhängigkeiten der klassischen Ablauf Steuerung bei Messergebnissen von Qubits. Dies wiederum ermöglicht es, leistungsstarke, probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können. Beispielsweise ist es einfach, eine so genannte *Wiederholung bis zum Erfolg* in Q # zu implementieren, bei der es sich um probabilistische Verbindungen handelt, die in Bezug auf elementare Gates *erwartete* niedrige Kosten aufweisen, aber für die die tatsächlichen Kosten von einem tatsächlichen Testlauf und einem tatsächlichen Austausch Vorgänge verschiedener möglicher Verzweigungen. 

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
Dabei sind `statementBlock1` und `statementBlock2` keine oder mehrere Q #-Anweisungen, und `expression` alle gültigen Ausdrücke, die zu einem Wert vom Typ `Bool`ausgewertet werden. In einem typischen Anwendungsfall implementiert die folgende Verbindung eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt{5}$ in der Bloch-Kugel. Dies wird mit einem bekannten RUS-Muster erreicht: 

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

Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen `finished` die sich im Gültigkeitsbereich der gesamten Repeat-Until-Fixup-Schleife befindet und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.

Zum Schluss zeigen wir ein Beispiel eines RUS-Musters zum Vorbereiten des Quantums $ \frac{1}{\sqrt{3}} \left (\sqrt{2}\ket{0}+ \ket{1}\right) $, beginnend ab dem $ \ket{+} $-Status. Siehe auch das [Beispiel für Komponententests, das mit der Standardbibliothek bereitgestellt](https://github.com/Microsoft/Quantum/blob/master/Samples/src/UnitTesting/RepeatUntilSuccessCircuits.qs)wird: 

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
 
Wichtige programmgesteuerte Features, die in diesem Vorgang gezeigt werden, sind eine komplexere `fixup` Teil der Schleife, die Quantum-Vorgänge einschließt, und die Verwendung von `AssertProb`-Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantum-Zustand an bestimmten bestimmten Punkten im Oren. Weitere Informationen zu `Assert`-und `AssertProb`-Anweisungen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging) . 
