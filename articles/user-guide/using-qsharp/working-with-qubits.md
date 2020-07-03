---
title: Arbeiten mit Qubits
description: füllbeschreibung
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.qubits
ms.openlocfilehash: 1655d18ab9d8638ad356e6fb90994b5c1fd76a25
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885297"
---
# <a name="working-with-qubits"></a>Arbeiten mit Qubits

Qubits sind das grundlegende Objekt der Informationen in Quantum Computing. Eine allgemeine Einführung in Qubits finden Sie Untergrund Legendes zu [Quantum Computing](xref:microsoft.quantum.overview.understanding). Weitere Informationen zu ihrer mathematischen Darstellung finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit). 

In diesem Artikel wird beschrieben, wie Sie mit Qubits in einem Q #-Programm arbeiten. 

> [!IMPORTANT]
>Keine der in diesem Artikel behandelten Anweisungen ist im Text einer Funktion gültig. Sie sind nur innerhalb von Vorgängen gültig.

## <a name="allocating-qubits"></a>Zuordnen von Qubits

Da es sich bei physischen Qubits um eine wertvolle Ressource auf einem Quantum-Computer handelt, besteht der Auftrag des Compilers darin, sicherzustellen, dass Sie so effizient wie möglich verwendet werden.
Daher müssen Sie Q # anweisen, Qubits für die Verwendung in einem bestimmten Anweisungsblock *zuzuordnen* .
Sie können Qubits als einzelnes Qubit oder als Array von Qubits zuordnen, die als *Register*bezeichnet werden. 

### <a name="clean-qubits"></a>Löschen von Qubits

Verwenden Sie die- `using` Anweisung, um neue Qubits für die Verwendung während eines-Anweisungsblocks zuzuordnen.

Die-Anweisung besteht aus dem Schlüsselwort `using` , gefolgt von einer in Klammern eingeschlossenen Bindung `( )` und dem Anweisungsblock, in dem die Qubits verfügbar sind.
Die Bindung folgt demselben Muster wie `let` -Anweisungen: entweder ein einzelnes Symbol oder ein Tupel von Symbolen, gefolgt von einem Gleichheitszeichen `=` und entweder ein einzelner Wert oder ein entsprechendes Tupel von *Initialisierern*.

Initialisierer sind entweder für ein einzelnes Qubit, das als angegeben ist, `Qubit()` oder ein Array von Qubits verfügbar, `Qubit[n]` wobei `n` ein `Int` Ausdruck ist.
Beispiel:

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```

Alle auf diese Weise zugeordneten Qubits beginnen mit dem Status $ \ket {0} $. Daher ist im vorherigen Beispiel `auxiliary` ein einzelnes Qubit im Status $ \ket {0} $, und `register` befindet sich im fünf-Qubit-Zustand $ \ket {00000} = \ket {0} \otimes \ket {0} \otimes \cdots \otimes \ket {0} $.
Am Ende des- `using` Blocks werden alle von diesem Block zugeordneten Qubits sofort freigegeben und können nicht mehr verwendet werden.

> [!WARNING]
> Zielcomputer können zugeordnete Qubits wieder verwenden und anderen Blöcken für die Zuordnung zur Verfügung stellen `using` . Der Zielcomputer erwartet daher, dass sich Qubits unmittelbar vor der Aufhebung der Zuordnung im $ \ket {0} $-Zustand befinden.
> Verwenden Sie nach Möglichkeit einheitliche Vorgänge, um alle zugeordneten Qubits an $ \ket $ zurückzugeben {0} .
> Wenn erforderlich, können Sie den @"microsoft.quantum.intrinsic.reset" -Vorgang verwenden, der das Qubit an $ \ket $ zurückgibt, {0} indem Sie es Messen und bedingt einen Vorgang basierend auf dem Ergebnis ausführen. Eine solche Messung zerstört alle jede Verflechtungen mit den verbleibenden Qubits und kann sich daher auf die Berechnung auswirken.


### <a name="borrowed-qubits"></a>Geliehene Qubits

Verwenden Sie die- `borrowing` Anweisung, um Qubits für die temporäre Verwendung zuzuweisen, die sich nicht in einem bestimmten Zustand befinden müssen.

Sie können geliehene Qubits während einer Berechnung als temporären Speicherplatz verwenden.
Diese Qubits befinden sich in der Regel nicht in einem sauberen Zustand, d. h., Sie werden nicht notwendigerweise in einem bekannten Zustand initialisiert, wie z. b. $ \ket {0} $.
Diese werden häufig als "modifizierte" Qubits bezeichnet, da ihr Zustand unbekannt ist und sogar mit anderen Teilen des Arbeitsspeichers des Quantums Computers entkoppelt werden kann.

Die Bindung folgt demselben Muster und denselben Regeln wie die- `using` Anweisung.
Beispiel:
```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, register) = (Qubit(), Qubit[5])) {
    // ...
}
```
Die geliehenen Qubits befinden sich in einem unbekannten Zustand und verlassen den Gültigkeitsbereich am Ende des Anweisungsblocks.
Der Kreditnehmer führt einen Commit aus, um die Qubits in demselben Zustand zu belassen, in dem Sie sich befanden. Das heißt, ihr Zustand am Anfang und am Ende des Anweisungsblocks sollte identisch sein.
Da dieser Zustand nicht notwendigerweise ein klassischer Zustand ist, sollten in den meisten Fällen die erfassten Bereiche keine Messungen enthalten. 

Beim Abgleich von Qubits versucht das System zuerst, die Anforderung aus Qubits auszufüllen, die verwendet werden, aber nicht während des Texts der Anweisung darauf zugegriffen wird `borrowing` .
Wenn nicht genügend solche Qubits vorhanden sind, werden neue Qubits zugewiesen, um die Anforderung abzuschließen.

Zu den bekannten Anwendungsfällen von Dirty Qubits zählen Implementierungen von multigesteuerten CNOT Gates, die nur sehr wenige Qubits und die Implementierung von inkrementern erfordern.
Ein Beispiel für die Verwendung in Q # finden Sie unter [Beispiel für das Ausleihen von Qubits](#borrowing-qubits-example) in diesem Artikel oder im Whitepaper [*using 2N + 2 Qubits with Toffoli based modulare Multiplikation*](https://arxiv.org/abs/1611.07995) (Haner, roetteler und svore 2017) für einen Algorithmus, der geliehene Qubits verwendet.

## <a name="intrinsic-operations"></a>Intrinsische Vorgänge

Nach der Zuordnung können Sie ein Qubit an Funktionen und Vorgänge übergeben.
In gewisser Hinsicht ist dies alles, was ein Q #-Programm mit einem Qubit tun kann, da die Aktionen, die ausgeführt werden können, als Vorgänge definiert sind.

In diesem Artikel werden einige nützliche Q #-Vorgänge erläutert, die Sie für die Interaktion mit Qubits verwenden können.
Weitere Details zu diesen und anderen finden Sie unter systeminterne [Vorgänge und Funktionen](xref:microsoft.quantum.libraries.standard.prelude). 

Zuerst werden die Single-Qubit-Pauli-Operatoren $X $, $Y $ und $Z $ in Q # durch die intrinsischen Vorgänge [`X`](xref:microsoft.quantum.intrinsic.x) , [`Y`](xref:microsoft.quantum.intrinsic.y) und dargestellt, die jeweils den- [`Z`](xref:microsoft.quantum.intrinsic.z) Typ haben `(Qubit => Unit is Adj + Ctl)` .

Wie in systeminternen [Vorgängen und Funktionen](xref:microsoft.quantum.libraries.standard.prelude)beschrieben, sollten Sie sich $X $ und somit auch `X` als bitflip-Vorgang oder nicht als Gate vorstellen.
Sie können den- `X` Vorgang verwenden, um Zustände der Form $ \ket{s_0 s_1 \dots s_n} $ für eine klassische Bitzeichenfolge vorzubereiten $s $:

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
> Später sehen Sie kompaktere Methoden zum Schreiben dieses Vorgangs, für die keine manuelle Ablauf Steuerung erforderlich ist.

Sie können auch Zustände wie z. b. $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ und $ \ket {-} = \left (\ket {0} -\ket {1} \right)/\sqrt {2} $ mithilfe der Hadamard Transform $H $, das in Q # durch den systeminternen Vorgang [`H`](xref:microsoft.quantum.intrinsic.h) (auch vom Typ (Qubit => Unit is ADJ + CTL)) dargestellt wird:

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

## <a name="measurements"></a>Messungen

Die Messungen einzelner Qubits können in unterschiedlichen Basen durchgeführt werden, die jeweils durch eine Pauli-Achse auf der [Bloch-Kugel](xref:microsoft.quantum.glossary#bloch-sphere)dargestellt werden.
Die *Berechnungsbasis* bezieht sich auf die `PauliZ` Basis und ist die am häufigsten verwendete Grundlage für die Messung.

### <a name="measure-a-single-qubit-in-the-pauliz-basis"></a>Messen eines einzelnen Qubit in der `PauliZ` Basis

Verwenden [`M`](xref:microsoft.quantum.intrinsic.m) Sie den-Vorgang, bei dem es sich um einen integrierten, intrinsischen nicht einheitlichen Vorgang handelt, um ein einzelnes Qubit in der Basis zu messen `PauliZ` und dem Ergebnis einen klassischen Wert zuzuweisen.
`M`verfügt über einen reservierten Rückgabetyp, `Result` , der nur Werte annehmen kann `Zero` oder `One` die den gemessenen Zuständen $ \ket {0} $ oder $ \ket {1} $ entspricht. Dies deutet darauf hin, dass das Ergebnis nicht mehr ein Quantum-Zustand ist.

Ein einfaches Beispiel ist der folgende Vorgang, der ein Qubit im $ \ket $-Zustand zuordnet {0} , dann einen Hadamard-Vorgang `H` darauf anwendet und das Ergebnis in der `PauliZ` Basis misst.

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

### <a name="measure-one-or-more-qubits-in-specific-bases"></a>Messen eines oder mehrerer Qubits in bestimmten Basen

Zum Messen eines Arrays mit einem oder mehreren Qubits in bestimmten Basen können Sie den- [`Measure`](xref:microsoft.quantum.intrinsic.measure) Vorgang verwenden.

Die Eingaben für `Measure` sind ein Array von `Pauli` Typen (z. b `[PauliX, PauliZ, PauliZ]` .) und ein Array von Qubits.

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

Beachten Sie, dass dieses Beispiel immer nur `Measure` auf einzelnen Qubits nacheinander durchführt, aber der Vorgang kann auf gemeinsame Messungen für mehrere Qubits erweitert werden.

## <a name="borrowing-qubits-example"></a>Beispiel für das Ausleihen von Qubits

Es gibt Beispiele im Kanon, die das `borrowing` Schlüsselwort verwenden, wie z. b. die folgende Funktion `MultiControlledXBorrow` . Wenn `controls` die einem Vorgang hinzu zufügenden Steuerelement-Qubits bezeichnet `X` , ist die Anzahl der von dieser Implementierung hinzugefügten modifizierten [ancillas](xref:microsoft.quantum.glossary#ancilla) `Length(controls)-2` .

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

Beachten Sie, dass in diesem Beispiel die kombinierte Verwendung von `With` Combinator in seiner Form verwendet wird, die für Vorgänge anwendbar ist, die Adjoint unterstützen, z `WithA` . b..
Dies ist ein guter Programmierstil, da das Hinzufügen von Steuerelementen zu Strukturen, die das Steuerelement in einbeziehen, `With` nur an den inneren Vorgang
Beachten Sie außerdem, dass zusätzlich zum `body` des Vorgangs eine Implementierung des Texts `controlled` des Vorgangs explizit bereitgestellt wurde, anstatt auf eine-Anweisung zurückzugreifen `controlled auto` .
Der Grund hierfür ist, dass es aufgrund der Struktur der Verbindung einfach ist, weitere Steuerelemente hinzuzufügen. Dies ist im Vergleich zum Hinzufügen des Steuer Elements zu jedem Gate in der von Vorteil `body` . 

Es ist aufschlussreich, diesen Code mit einer anderen Funktion zu vergleichen, die `MultiControlledXClean` das gleiche Ziel hat, eine Multiplikation gesteuerte Operation zu implementieren, bei der `X` jedoch mithilfe des-Mechanismus mehrere saubere Qubits verwendet werden `using` . 

## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über die [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow) in f #.