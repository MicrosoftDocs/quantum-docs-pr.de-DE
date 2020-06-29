---
title: 'Ablauf Steuerung in Q #'
description: Schleifen, Bedingungen usw.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: 0cf62a128170bd0c28ff77f00fc23414567b1ea4
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415302"
---
# <a name="control-flow-in-q"></a>Ablauf Steuerung in Q #

Innerhalb eines Vorgangs oder einer Funktion wird jede Anweisung in der richtigen Reihenfolge ausgeführt, ähnlich wie andere gängige imperative klassische Sprachen.
Allerdings können Sie die Ablauf Steuerung auf drei verschiedene Arten ändern:

* `if`Äußerungen
* `for`Loops
* `repeat-until-success`Loops

Die `if` `for` Ablaufsteuerungskonstrukte und sind für die meisten klassischen Programmiersprachen vertraut. [`Repeat-until-success`](#repeat-until-success-loop)Schleifen werden später in diesem Artikel erläutert.

Wichtig ist, `for` dass Schleifen und `if` Anweisungen in Vorgängen verwendet werden können, für die [Spezialisierungs](xref:microsoft.quantum.guide.operationsfunctions) Vorgänge automatisch generiert werden. In diesem Szenario kehrt das Adjoint einer `for` Schleife die Richtung um und übernimmt das Adjoint der einzelnen Iterationen.
Diese Aktion folgt dem Prinzip "Schuh-und-SOCKS": Wenn Sie das Einfügen von SOCKS und den Schuhen rückgängig machen möchten, müssen Sie die einfügende Schuhe rückgängig machen und dann auf die SOCKS setzen. 

## <a name="if-else-if-else"></a>If, else-if, Else

Die- `if` Anweisung unterstützt die bedingte Ausführung.
Er besteht aus dem Schlüsselwort `if` , einem booleschen Ausdruck in Klammern und einem Anweisungsblock (der _Then_ -Block).
Optional kann eine beliebige Anzahl von else-if-Klauseln befolgt werden, von denen jeder aus dem Schlüsselwort `elif` , einem booleschen Ausdruck in Klammern und einem Anweisungsblock (der _else-if-_ Block) besteht.
Schließlich kann die Anweisung optional mit einer Else-Klausel abgeschlossen werden, die aus dem Schlüsselwort `else` gefolgt von einem anderen Anweisungsblock (dem _else_ -Block) besteht.

Die `if` Bedingung wird ausgewertet, und wenn der Wert *true*ist, wird der *Then* -Block ausgeführt.
Wenn die Bedingung *false*ist, wird die erste else-if-Bedingung ausgewertet. Wenn dies zutrifft, wird der *else-if-* Block ausgeführt.
Andernfalls wertet der zweite Else-If-Block aus, und dann der dritte, usw., bis entweder eine-Klausel mit einer true-Bedingung gefunden wird oder keine else-if-Klauseln mehr vorhanden sind.
Wenn die ursprüngliche *if* -Bedingung und alle else-if-Klauseln als *false*ausgewertet werden, wird der *else* -Block ausgeführt, falls angegeben.

Beachten Sie, dass der ausgeführte Block in seinem eigenen Bereich ausgeführt wird.
Bindungen, die innerhalb eines- `if` ,-oder-Blocks erstellt werden, `elif` `else` sind nach Beendigung des-Blocks nicht sichtbar.

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

## <a name="for-loop"></a>for-Schleife

Die- `for` Anweisung unterstützt Iterationen über einen ganzzahligen Bereich oder ein Array.
Die-Anweisung besteht aus dem `for` -Schlüsselwort, gefolgt von einem Symbol-oder Symbol-Tupel, dem-Schlüsselwort `in` und einem Ausdruck vom Typ `Range` oder Array, alle in Klammern und einem Anweisungsblock.

Der Anweisungsblock (der Hauptteil der Schleife) wird wiederholt ausgeführt, wobei das definierte Symbol (die Schleifenvariable) an jeden Wert im Bereich oder Array gebunden ist.
Beachten Sie Folgendes: Wenn der Bereichs Ausdruck einen leeren Bereich oder ein leeres Array ergibt, wird der Text überhaupt nicht ausgeführt.
Der Ausdruck wird vor der Eingabe der Schleife vollständig ausgewertet und ändert sich nicht, während die Schleife ausgeführt wird.

Die Schleifenvariable wird an jedem Eingang an den Schleifen Text gebunden, und die Bindung am Ende des Texts wird aufgehoben.
Die Schleifenvariable wird nicht gebunden, nachdem die for-Schleife abgeschlossen wurde.
Die Bindung der Schleifen Variablen ist unveränderlich und folgt denselben Regeln wie andere Variablen Bindungen. 

In diesen Beispielen `qubits` ist ein Register von Qubits (d. h. vom Typ `Qubit[]` ). 

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

Beachten Sie, dass wir am Ende den binären Operator "arithmetischer Shift-Left" () verwendet haben `<<<` . Weitere Informationen finden Sie unter [numerische Ausdrücke](xref:microsoft.quantum.guide.expressions#numeric-expressions).

## <a name="repeat-until-success-loop"></a>Repeat-Until-Success-Schleife

Die Q #-Sprache ermöglicht eine klassische Ablauf Steuerung, die von den Ergebnissen der Messung von Qubits abhängig ist.
Diese Funktion ermöglicht es wiederum, leistungsstarke probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.
Beispiele hierfür sind die RUS *-Muster (Repeat-Until-Success* ) in f #.
Diese RUS-Muster sind probabilistische Programme, die zu den *erwarteten* niedrigen Kosten in Bezug auf elementare Gates gehören. die anfallenden Kosten hängen von der tatsächlichen Durchführung und der Überführung der zahlreichen möglichen Verzweigungen ab.

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
Wenn die Bedingung true ist, wird die-Anweisung abgeschlossen. Andernfalls wird der Fixup ausgeführt, und die Anweisung wird erneut ausgeführt, beginnend mit dem Schleifen Text.

Alle drei Teile einer RUS-Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich *für jede Wiederholung*behandelt, sodass im Text gebundene Symbole sowohl im Test als auch im Fixup verfügbar sind.
Wenn Sie die Ausführung des Fixup abschließen, wird der Gültigkeitsbereich für die-Anweisung beendet, sodass Symbol Bindungen, die während des Texts oder Fixup erstellt werden, in nachfolgenden Wiederholungen nicht verfügbar sind.

Außerdem ist die- `fixup` Anweisung häufig hilfreich, aber nicht immer erforderlich.
In Fällen, in denen er nicht benötigt wird, wird das Konstrukt

```qsharp
repeat {
    // do stuff
}
until (expression);
```

ist auch ein gültiges RUS-Muster.

Weitere Beispiele und Details finden Sie in diesem Artikel unter [Wiederholungs-bis-Erfolg-Beispiele](#repeat-until-success-examples) .

> [!TIP]   
> Vermeiden Sie die Verwendung von Wiederholungs-bis-Erfolg-Schleifen innerhalb von Funktionen. Verwenden Sie *while* -Schleifen, um die entsprechende Funktionalität in Funktionen bereitzustellen. 

## <a name="while-loop"></a>While-Schleife

Wiederholungs-bis-Erfolg-Muster verfügen über eine sehr Quantum-spezifische-Anmerkung. Sie werden häufig in bestimmten Klassen von Quantum-Algorithmen verwendet. Dies ist also das dedizierte Sprachkonstrukt in f #. Schleifen, die basierend auf einer Bedingung unterbrechen und deren Ausführungsdauer zur Kompilierzeit somit unbekannt ist, werden jedoch mit einer bestimmten Sorgfalt in einer Quantum-Laufzeit behandelt. Die Verwendung innerhalb von Funktionen ist jedoch nicht problematisch, da diese Schleifen nur Code enthalten, der auf herkömmlicher (nicht Quantum-) Hardware ausgeführt wird. 

F # unterstützt daher die Verwendung von while-Schleifen innerhalb von Functions. Eine- `while` Anweisung besteht aus dem Schlüsselwort `while` , einem booleschen Ausdruck in Klammern und einem Anweisungsblock.
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

Beispiel:
```qsharp
return 1;
```
oder
```qsharp
return (results, qubits);
```

* Ein Aufruf bares Element, das ein leeres Tupel zurückgibt, `()` erfordert keine Return-Anweisung.
* Verwenden Sie, um eine frühe Beendigung des Vorgangs oder der Funktion anzugeben `return ();` .
Aufruf Bare Elemente, die einen beliebigen anderen Typ zurückgeben, erfordern eine abschließende Return-Anweisung.
* Es gibt keine maximale Anzahl von Return-Anweisungen innerhalb eines Vorgangs.
Der Compiler gibt möglicherweise eine Warnung aus, wenn Anweisungen einer Return-Anweisung in einem-Block folgen.

   
## <a name="fail-statement"></a>Fail-Anweisung

Die Fail-Anweisung beendet die Ausführung eines Vorgangs und gibt einen Fehlerwert an den Aufrufer zurück.
Er besteht aus dem Schlüsselwort `fail` , gefolgt von einer Zeichenfolge und einem abschließenden Semikolon.
Die-Anweisung gibt die Zeichenfolge an den klassischen Treiber als Fehlermeldung zurück.

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

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a>RUS-Muster für Single-Qubit-Drehung über eine irrationale Achse 

In einem typischen Anwendungsfall implementiert der folgende Q #-Vorgang eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt {5} $ in der Bloch-Kugel. Die Implementierung verwendet ein bekanntes RUS-Muster:

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

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a>RUS-Schleife mit einer änderbaren Variablen im Gültigkeitsbereich

Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen, `finished` die innerhalb des Gültigkeits Bereichs der gesamten Repeat-Until-Fixup-Schleife liegt und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.

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

Dieses Beispiel zeigt eine RUS-Schleife ohne den fixupschritt. Der Code ist eine probabilistische Verbindung, die ein wichtiges Drehungs Gate implementiert $V _3 = (\boldone + 2 i)/\sqrt {5} $ mithilfe von `H` und `T` Gates.
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

Im folgenden finden Sie ein Beispiel für ein RUS-Muster zum Vorbereiten des Quantums $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, beginnend mit dem Status $ \ket{+} $.

Wichtige programmgesteuerte Features, die in diesem Vorgang angezeigt werden, sind:

* Ein komplexerer `fixup` Teil der Schleife, der Quantum-Vorgänge einschließt. 
* Die Verwendung von- `AssertProb` Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantenzustand an bestimmten angegebenen Punkten im Programm gemessen wird.

Weitere Informationen zu den [`Assert`](xref:microsoft.quantum.intrinsic.assert) -und- [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) Vorgängen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging).

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

Weitere Informationen finden Sie unter [Beispiel für Komponententests mit der Standardbibliothek](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):

## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über das [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging) in f #.
