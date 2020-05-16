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
# <a name="working-with-qubits"></a>Arbeiten mit Qubits

Nachdem wir nun eine Vielzahl von verschiedenen Teilen der Q #-Sprache gesehen haben, können wir uns die Thick of IT ansehen und erfahren, wie Sie Qubits selbst verwenden können.

Beachten Sie, dass keine dieser Anweisungen innerhalb des Texts einer Funktion zulässig ist.
Sie sind nur innerhalb von Vorgängen gültig.

## <a name="allocating-qubits"></a>Zuordnen von Qubits

### <a name="clean-qubits"></a>Löschen von Qubits

Die- `using` Anweisung wird verwendet, um neue Qubits für die Verwendung während eines-Anweisungsblocks *zuzuordnen* .

Die-Anweisung besteht aus dem Schlüsselwort `using` , gefolgt von einer öffnenden Klammer `(` , einer Bindung, einer Schließ `)` enden Klammer und dem Anweisungsblock, in dem die Qubits verfügbar sein werden.
Die Bindung folgt demselben Muster wie `let` -Anweisungen: entweder ein einzelnes Symbol oder ein Tupel von Symbolen, gefolgt von einem Gleichheitszeichen `=` und entweder ein einzelner Wert oder ein entsprechendes Tupel von *Initialisierern*.

Initialisierer sind entweder für ein einzelnes Qubit, das als angegeben ist, `Qubit()` oder ein Array von Qubits verfügbar, `Qubit[n]` wobei `n` ein `Int` Ausdruck ist.
Ein auf ein Objekt angewendeter

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

Alle auf diese Weise zugeordneten Qubits beginnen im Zustand "$ \ket {0} $". im obigen Beispiel `register` befindet sich daher im Zustand "$ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $".
Am Ende des- `using` Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.

> [!WARNING]
> Zielcomputer erwarten, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im Zustand $ \ket {0} $ befinden, damit Sie wieder verwendet und für die Zuordnung anderen Blöcken angeboten werden können `using` .
> Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket $ zurückzugeben {0} .
> Wenn dies erforderlich ist, @"microsoft.quantum.intrinsic.reset" kann der Vorgang verwendet werden, um stattdessen ein Qubit zu messen und dieses Messergebnis zu verwenden, um sicherzustellen, dass das gemessene Qubit an "$ \ket $" zurückgegeben wird {0} . Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.


### <a name="borrowed-qubits"></a>Geliehene Qubits

Die- `borrowing` Anweisung wird verwendet, um Qubits für die temporäre Verwendung verfügbar zu machen, die sich nicht in einem bestimmten Zustand befinden müssen.

Der Mechanismus zum ableihen ermöglicht die Zuordnung von Qubits, die während einer Berechnung als Scratch-Speicherplatz verwendet werden kann.
Diese Qubits befinden sich in der Regel nicht in einem sauberen Zustand, d. h., Sie werden nicht notwendigerweise in einem bekannten Zustand initialisiert, wie z. b. $ \ket {0} $.
Diese werden häufig als "modifizierte" Qubits bezeichnet, da ihr Zustand unbekannt ist und sogar mit anderen Teilen des Arbeitsspeichers des Quantums Computers entkoppelt werden kann.

Die Bindung folgt demselben Muster und denselben Regeln wie in einer- `using` Anweisung.
Ein auf ein Objekt angewendeter
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
Die geliehenen Qubits befinden sich in einem unbekannten Zustand und verlassen den Gültigkeitsbereich am Ende des Anweisungsblocks.
Der Kreditnehmer führt einen Commit aus, um die Qubits in demselben Zustand zu belassen, in dem Sie sich befanden, d. h., ihr Zustand am Anfang und am Ende des Anweisungsblocks ist erwartungsgemäß identisch.
Dabei handelt es sich nicht unbedingt um einen klassischen Zustand, der in den meisten Fällen keine Messungen enthalten sollte. 

Beim Abgleich von Qubits versucht das System zunächst, die Anforderung von Qubits auszufüllen, die verwendet werden, aber nicht während des Texts der Anweisung darauf zugegriffen wird `borrowing` .
Wenn nicht genügend derartige Qubits vorhanden sind, werden neue Qubits zum Durchführen der Anforderung zugeteilt.


Zu den bekannten Anwendungsfällen von Dirty Qubits zählen Implementierungen von multigesteuerten CNOT Gates, die nur sehr wenige Qubits und die Implementierung von inkrementern erfordern.
Im folgenden [Beispiel](#borrowing-qubits-example) finden Sie ein Beispiel für die Verwendung in Q # oder das Paper [*Factoring mit 2n + 2 Qubits mit auf Toffoli basierender modularer Multiplikation*](https://arxiv.org/abs/1611.07995) (Haner, roetteler und svore 2017) für einen Algorithmus, der geliehene Qubits verwendet.


## <a name="intrinsic-operations"></a>Intrinsische Vorgänge

Nach der Zuordnung kann ein Qubit an Funktionen und Vorgänge weitergegeben werden.
In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.
Diese Vorgänge werden in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)ausführlicher angezeigt. vorerst werden jedoch einige nützliche Vorgänge erwähnt, die für die Interaktion mit Qubits verwendet werden können.

Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge `X` , `Y` und dargestellt, die jeweils den- `Z` Typ haben `(Qubit => Unit is Adj + Ctl)` .
Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, können wir uns $X $ und somit auch `X` als bitflip-Vorgang oder nicht als Gate vorstellen.
`X`Mit dem Vorgang können wir die Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorbereiten $s $:

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

Wir können auch die Zustände, wie z. b. $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ und $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $, mithilfe der Hadamard Transform $H $ vorbereiten, die in Q # durch den intrinsischen Vorgang dargestellt wird `H : (Qubit => Unit is Adj + Ctl)` :

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

Mithilfe des `Measure` -Vorgangs, bei dem es sich um eine integrierte intrinsische, nicht einheitliche Operation handelt, können wir klassische Informationen aus einem Objekt des Typs extrahieren `Qubit` und einen klassischen Wert als Ergebnis zuweisen, der einen reservierten Typ aufweist und `Result` angibt, dass das Ergebnis nicht mehr ein Quantum-Zustand ist.
Die Eingabe für `Measure` ist eine Pauli-Achse in der Bloch-Kugel, die durch einen Wert des Typs `Pauli` (z.b. `PauliX` ) und einen Wert des Typs dargestellt wird `Qubit` .

Ein einfaches Beispiel ist der folgende Vorgang, der ein Qubit im $ \ket $-Zustand zuordnet {0} , dann einen Hadamard-Vorgang `H` darauf anwendet und das Ergebnis in der `PauliZ` Basis misst.

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

Ein etwas komplizierteres Beispiel wird durch den folgenden Vorgang vorgegeben, der den booleschen Wert zurückgibt, `true` Wenn sich alle Qubits in einem Register des Typs `Qubit[]` im Zustand NULL befinden, wenn Sie in einer angegebenen Pauli-Basis gemessen werden und andernfalls andernfalls zurückgegeben werden `false` .

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

## <a name="borrowing-qubits-example"></a>Beispiel für das Ausleihen von Qubits

Im Kanon finden Sie Beispiele, in denen das `borrowing` Schlüsselwort verwendet wird, z.b. die `MultiControlledXBorrow` unten definierte Funktion.
Wenn `controls` die Steuerelement-Qubits bezeichnet, die einem Vorgang hinzugefügt werden sollen `X` , `Length(controls)-2` wird durch diese Implementierung eine Gesamtzahl von vielen modifizierten ancillas hinzugefügt.

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

Beachten Sie, dass die kombinierte Verwendung der `With` Combinator----in der Form, die für Vorgänge anwendbar ist, die Adjoint unterstützen, d. h. `WithA` ---in diesem Beispiel erstellt wurde.
Dies ist ein guter Programmierstil, da das Hinzufügen von Steuerelementen zu Strukturen, die das Steuerelement in einbeziehen, `With` nur an den inneren Vorgang
Beachten Sie, dass hier zusätzlich zum `body` des Vorgangs eine Implementierung des Texts `controlled` des Vorgangs explizit bereitgestellt wurde, anstatt auf eine-Anweisung zurückzugreifen `controlled auto` .
Der Grund hierfür ist, dass wir aus der Struktur der Verbindung wissen, wie Sie ganz einfach weitere Steuerelemente hinzufügen können, die im Vergleich zum Hinzufügen von Steuerelementen zu jedem einzelnen Gate in der von Vorteil sind `body` . 

Es ist aufschlussreich, diesen Code mit einer anderen Funktion zu vergleichen, die `MultiControlledXClean` das gleiche Ziel hat, eine Multiplikation gesteuerte Operation zu implementieren, bei der `X` jedoch mithilfe des-Mechanismus mehrere saubere Qubits verwendet werden `using` . 

## <a name="whats-next"></a>Wie geht es weiter?
Erfahren Sie mehr über die [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow) in f #.