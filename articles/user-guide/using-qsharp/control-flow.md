---
title: 'Ablauf Steuerung in Q #'
description: Schleifen, Bedingungen usw.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 1f1b641563fe35879abeee32b4f0aeeb7001b1a0
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84326539"
---
# <a name="control-flow-in-q"></a>Ablauf Steuerung in Q #

Innerhalb einer Operation oder Funktion wird jede Anweisung in der richtigen Reihenfolge ausgeführt, ähnlich wie bei den gängigsten, imperativen, klassischen Sprachen.
Diese Ablauf Steuerung kann jedoch auf drei verschiedene Arten geändert werden:

- `if`Äußerungen
- `for`Loops
- `repeat`-`until`Loops

Wir verzögern die Erörterung der letzteren weiter [unten](#repeat-until-success-loop).
Die `if` `for` Ablaufsteuerungs-Konstrukte und sind jedoch für die meisten klassischen Programmiersprachen in einem vertrauten Sinn.

Wichtig ist, `for` dass Schleifen und `if` Anweisungen sogar in Vorgängen verwendet werden können, für die Spezialisierungs Vorgänge automatisch generiert werden. In diesem Fall kehrt das Adjoint einer `for` Schleife die Richtung um und übernimmt das Adjoint der einzelnen Iterationen.
Dies folgt dem Prinzip "Schuh-und-SOCKS": Wenn Sie das Einfügen von SOCKS und dann auf Schuhe rückgängig machen möchten, müssen Sie die einfügende Schuhe rückgängig machen und dann auf SOCKS setzen.
Es funktioniert ausgesprochen weniger gut, wenn Sie versuchen, die SOCKS zu wiederholen, während Sie Ihre Schuhe noch nicht nutzen!

## <a name="if-else-if-else"></a>If, else-if, Else

Die- `if` Anweisung unterstützt die bedingte Ausführung.
Sie besteht aus dem Schlüsselwort `if` , einer offenen Klammer `(` , einem booleschen Ausdruck, einer schließenden Klammer `)` und einem Anweisungsblock (der _Then_ -Block).
Auf diese kann eine beliebige Anzahl von else-if-Klauseln folgen, von denen jede aus dem Schlüsselwort `elif` , einer offenen Klammer `(` , einem booleschen Ausdruck, einer schließenden Klammer `)` und einem Anweisungsblock besteht (der _else-if-_ Block).
Schließlich kann die Anweisung optional mit einer Else-Klausel abgeschlossen werden, die aus dem Schlüsselwort `else` gefolgt von einem anderen Anweisungsblock (dem _else_ -Block) besteht.

Die `if` Bedingung wird ausgewertet, und wenn der Wert true ist, wird der then-Block ausgeführt.
Wenn die Bedingung false ist, wird die erste else-if-Bedingung ausgewertet. Wenn der Wert true ist, wird der Else-If-Block ausgeführt.
Andernfalls wird der zweite Else-If-Block getestet, dann der dritte, usw., bis entweder eine-Klausel mit einer true-Bedingung gefunden wird oder keine else-if-Klauseln mehr vorhanden sind.
Wenn die ursprüngliche if-Bedingung und alle else-if-Klauseln als false ausgewertet werden, wird der Else-Block ausgeführt, wenn ein solcher angegeben wurde.

Beachten Sie, dass der ausgeführte Block in seinem eigenen Bereich ausgeführt wird.
Bindungen, die innerhalb eines- `if` ,-oder-Blocks erstellt werden, `elif` `else` sind nach dem Ende nicht sichtbar.

Beispiel:

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
oder
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a>For-Schleife

Die- `for` Anweisung unterstützt Iterationen über einen ganzzahligen Bereich oder über ein Array.
Die-Anweisung besteht aus dem Schlüsselwort `for` , einer offenen Klammer `(` , gefolgt von einem Symbol oder einem Symbol Tupel, dem Schlüsselwort `in` , einem Ausdruck vom Typ `Range` oder Array, einer schließenden Klammer `)` und einem Anweisungsblock.

Der Anweisungsblock (der Hauptteil der Schleife) wird wiederholt ausgeführt, wobei die definierten Symbole (die Schleifen Variablen) an jeden Wert im Bereich oder Array gebunden sind.
Beachten Sie, dass der Text nicht ausgeführt wird, wenn der Bereichs Ausdruck zu einem leeren Bereich oder Array ausgewertet wird.
Der Ausdruck wird vor der Eingabe der Schleife vollständig ausgewertet und ändert sich nicht, während die Schleife ausgeführt wird.

Die Schleifenvariable wird an jedem Eingang an den Schleifen Text gebunden, und die Bindung am Ende des Texts wird aufgehoben.
Insbesondere wird die Schleifenvariable nicht gebunden, nachdem die for-Schleife abgeschlossen wurde.
Die Bindung der deklarierten Symbole ist unveränderlich und folgt denselben Regeln wie andere Variablen Bindungen. 

Für einige Beispiele ist das unter `qubits` drücken ein Register von Qubits (d. h. vom Typ `Qubit[]` ). 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```
Beachten Sie, dass wir am Ende den binären Operator "arithmetischer Shift-Left", "Details", `<<<` die in [numerischen Ausdrücken](xref:microsoft.quantum.guide.expressions#numeric-expressions) gefunden werden können, verwendet haben.


## <a name="repeat-until-success-loop"></a>Repeat-Until-Success-Schleife

Die Q #-Sprache ermöglicht eine klassische Ablauf Steuerung, die von den Ergebnissen der Messung von Qubits abhängig ist.
Diese Funktion ermöglicht es wiederum, leistungsfähige, probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.
Beispielsweise ist es einfach, so genannte *Wiederholungs-bis-Erfolg-* Muster (RUS) in Q # zu implementieren.
Diese RUS-Muster sind probabilistische Programme, deren Kosten in Bezug auf elementare Gates *erwartungsgemäß* sind, aber für die die echten Kosten von einem tatsächlichen Testlauf und einem tatsächlichen Austausch der verschiedenen möglichen Verzweigungen abhängen.

Zum Vereinfachen von Wiederholungs-bis-Erfolg-Mustern (RUS) unterstützt Q # die-Konstrukte.

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

dabei `expression` ist ein beliebiger gültiger Ausdruck, der zu einem Wert vom Typ ausgewertet wird `Bool` .
Der Schleifen Text wird ausgeführt, und anschließend wird die Bedingung ausgewertet.
Wenn die Bedingung true ist, wird die-Anweisung abgeschlossen. Andernfalls wird das Fixup ausgeführt, und die Anweisung wird erneut ausgeführt, beginnend mit dem Schleifen Text.

Alle drei Teile einer Wiederholung/bis-Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich *für jede Wiederholung*behandelt, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.
Wenn die Ausführung der Fixup-Anweisung abgeschlossen ist, wird der Bereich für die-Anweisung beendet, sodass im Text-oder Fixup-Bereich vorgenommene Symbol Bindungen in nachfolgenden Wiederholungen nicht verfügbar sind.

Außerdem ist die- `fixup` Anweisung häufig hilfreich, aber nicht immer erforderlich.
In Fällen, in denen er nicht benötigt wird, wird das Konstrukt
```qsharp
repeat {
    // do stuff
}
until (expression);
```
ist auch ein gültiges RUS-Muster.

Am unteren Rand dieser Seite werden einige [Beispiele für RUS-Schleifen](#repeat-until-success-examples)vorgestellt.

> [!TIP]   
> Vermeiden Sie die Verwendung von Wiederholungs-bis-Erfolg-Schleifen innerhalb von Funktionen. Die entsprechende Funktionalität wird von while-Schleifen in Funktionen bereitgestellt. 

## <a name="while-loop"></a>While-Schleife

Wiederholungs-bis-Erfolg-Muster verfügen über eine sehr Quantum-spezifische-Anmerkung. Sie werden häufig in bestimmten Klassen von Quantum-Algorithmen verwendet. Dies ist daher das dedizierte Sprachkonstrukt in f #. Allerdings müssen Schleifen, die basierend auf einer Bedingung unterbrechen und deren Ausführungsdauer zur Kompilierzeit nicht bekannt ist, mit bestimmter Sorgfalt in einer Quantum-Laufzeit behandelt werden. Die Verwendung in Funktionen andererseits ist nicht problematisch, da diese nur Code enthalten, der auf herkömmlicher (nicht Quantum-) Hardware ausgeführt wird. 

F # unterstützt daher die Verwendung von while-Schleifen nur innerhalb von Functions. Eine- `while` Anweisung besteht aus dem Schlüsselwort `while` , einer offenen Klammer `(` , einer Bedingung (d. h. einem booleschen Ausdruck), einer schließenden Klammer `)` und einem Anweisungsblock.
Der Anweisungsblock (der Text der Schleife) wird ausgeführt, solange die Bedingung als ausgewertet wird `true` .

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a>Return-Anweisung

Die Return-Anweisung beendet die Ausführung eines Vorgangs oder einer Funktion und gibt einen Wert an den Aufrufer zurück.
Er besteht aus dem Schlüsselwort `return` , gefolgt von einem Ausdruck des entsprechenden Typs und einem abschließenden Semikolon.

Ein Aufruf bares Element, das ein leeres Tupel zurückgibt, `()` erfordert keine Return-Anweisung.
Wenn eine frühe Beendigung gewünscht ist, `return ()` kann in diesem Fall verwendet werden.
Aufruf Bare Elemente, die einen beliebigen anderen Typ zurückgeben, erfordern eine abschließende Return-Anweisung.

Es gibt keine maximale Anzahl von Return-Anweisungen innerhalb eines Vorgangs.
Der Compiler gibt möglicherweise eine Warnung aus, wenn Anweisungen einer Return-Anweisung in einem-Block folgen.

Beispiel:
```qsharp
return 1;
```
oder
```qsharp
return ();
```
oder
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a>Fail-Anweisung

Die Fail-Anweisung beendet die Ausführung eines Vorgangs und gibt einen Fehlerwert an den Aufrufer zurück.
Er besteht aus dem Schlüsselwort `fail` , gefolgt von einer Zeichenfolge und einem abschließenden Semikolon.
Die Zeichenfolge wird als Fehlermeldung an den klassischen Treiber zurückgegeben.

Es gibt keine Einschränkung für die Anzahl der Fail-Anweisungen innerhalb eines Vorgangs.
Der Compiler gibt möglicherweise eine Warnung aus, wenn-Anweisungen einer Fail-Anweisung innerhalb eines-Blocks folgen.

Beispiel:
```qsharp
fail $"Impossible state reached";
```
oder mithilfe von [interpoliert](xref:microsoft.quantum.guide.expressions#interpolated-strings)Zeichen folgen
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a>Beispiele für Wiederholung bis zum Erfolg

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>RUS-Muster für einzelne Qubit-Drehung über eine irrationale Achse 

In einem typischen Anwendungsfall implementiert der folgende Q #-Vorgang eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt {5} $ in der Bloch-Kugel. Dies wird mit einem bekannten RUS-Muster erreicht:

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a>RUS-Schleife mit änderbarer Variable im Gültigkeitsbereich

Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen `finished` , die sich im Gültigkeitsbereich der gesamten Repeat-Until-Fixup-Schleife befindet und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a>RUS ohne`fixup`

Der folgende Code ist z. b. eine probabilistische Verbindung, die ein wichtiges Drehungs Gate implementiert $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ mithilfe der `H` -und- `T` Gates.
Die Schleife wird im Durchschnitt in $ \frac {8} {5} $ Wiederholungen beendet.
Weitere Informationen finden Sie [*unter Repeat-Until-Success: nicht deterministische Zerlegung von Single-Qubit-uniflüssen*](https://arxiv.org/abs/1311.1074) ("Petznick" und "svore", 2014).

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a>RUS zum Vorbereiten eines Quantum-Zustands

Schließlich zeigen wir ein Beispiel für ein RUS-Muster zum Vorbereiten eines Quantum-Zustands $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, beginnend ab dem $ \ket{+} $-Status.
Siehe auch das [Beispiel für Komponententests, das mit der Standardbibliothek bereitgestellt](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)wird:

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
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

Wichtige programmgesteuerte Features, die in diesem Vorgang gezeigt werden, sind ein komplexerer `fixup` Teil der-Schleife, der Quantum-Vorgänge einschließt, und die Verwendung von- `AssertProb` Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantum-Zustand an bestimmten angegebenen Punkten im Programm gemessen wird.
Weitere Informationen zu den-und-Vorgängen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging) [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .


## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über das [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging) in f #.