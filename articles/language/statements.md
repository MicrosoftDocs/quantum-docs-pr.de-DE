---
title: 'Q #-Anweisungen | Microsoft-Dokumentation'
description: 'Q #-Anweisungen'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 5bcbee868c76aaf53d0b7969e6e634da62689aaa
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184864"
---
# <a name="statements-and-other-constructs"></a>Anweisungen und andere Konstrukte

## <a name="comments"></a>Kommentare

Kommentare beginnen mit zwei Schrägstrichen, `//`und werden bis zum Ende der Zeile fortgesetzt.
Ein Kommentar kann an beliebiger Stelle in einer f #-Quelldatei angezeigt werden.

### <a name="documentation-comments"></a>Dokumentations Kommentare

Kommentare, die mit drei Schrägstrichen (`///`) beginnen, werden vom Compiler speziell behandelt, wenn Sie unmittelbar vor einem Namespace, einem Vorgang, einer Spezialisierung, einer Funktion oder einer Typdefinition erscheinen.
In diesem Fall wird der Inhalt als Dokumentation für den definierten Aufruf baren oder benutzerdefinierten Typ, wie für andere .NET-Sprachen, übernommen.

In `///` Kommentaren wird Text, der als Teil der API-Dokumentation angezeigt wird, als [markdown](https://daringfireball.net/projects/markdown/syntax)formatiert, wobei verschiedene Teile der Dokumentation durch speziell benannte Header angezeigt werden.
Als Erweiterung von markdown können Querverweise auf Vorgänge, Funktionen und benutzerdefinierte Typen in Q # mithilfe des `@"<ref target>"`eingeschlossen werden, wobei `<ref target>` durch den voll qualifizierten Namen des Code Objekts ersetzt wird, auf das verwiesen wird.
Optional kann eine Dokumentations-Engine auch zusätzliche markdownerweiterungen unterstützen.

Beispiel:

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit
{
    op(target);
    op(target);
}
```

Die folgenden Namen werden als Dokumentations Kommentar Header erkannt.

- **Zusammenfassung**: eine kurze Zusammenfassung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs. Der erste Absatz der Zusammenfassung wird für Hover-Informationen verwendet. Es sollte nur Text sein.
- **Beschreibung**: eine Beschreibung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs. Die Zusammenfassung und Beschreibung werden verkettet, um die generierte Dokumentations Datei für die Funktion, den Vorgang oder den Typ zu bilden.
  Die Beschreibung enthält möglicherweise in-line-Symbole und-Gleichungen in der Zeile.
- **Input**: eine Beschreibung des eingabetupels für einen Vorgang oder eine Funktion.
  Kann zusätzliche markdown-Unterabschnitte enthalten, die jedes einzelne Element des eingabetupels angeben.
- **Output**: eine Beschreibung des Tupels, das von einem Vorgang oder einer Funktion zurückgegeben wird.
- **Typparameter**: ein leerer Abschnitt, der einen zusätzlichen unter Abschnitt für jeden generischen Typparameter enthält.
- **Beispiel**: ein kurzes Beispiel für den Vorgang, die Funktion oder den Typ, der verwendet wird.
- **Hinweise**: verschiedene Prosa, die einen Aspekt des Vorgangs, der Funktion oder des Typs beschreibt.
- **Siehe auch**: eine Liste der voll qualifizierten Namen, die verwandte Funktionen, Vorgänge oder benutzerdefinierte Typen angeben.
- **Verweise**: eine Liste von verweisen und citationen für das Element, das dokumentiert wird.

## <a name="namespaces"></a>Namespaces

Jeder Q #-Vorgang, jede Funktion und jeder benutzerdefinierte Typ wird in einem Namespace definiert.
F # befolgt die gleichen Regeln für die Benennung wie andere .NET-Sprachen.
F # unterstützt jedoch keine relativen Verweise auf Namespaces.
Das heißt, wenn der Namespace `a.b` geöffnet wurde, wird ein Verweis auf die Vorgangs Namen `c.d` nicht in einen Vorgang mit vollständigem Namen `a.b.c.d`aufgelöst.

Innerhalb eines Namespace Blocks kann die `open` Direktive verwendet werden, um alle Typen und callables zu importieren, die in einem bestimmten Namespace deklariert sind, und auf diese mit Ihrem nicht qualifizierten Namen zu verweisen. Optional kann ein Kurzname für den geöffneten Namespace definiert werden, sodass alle Elemente aus diesem Namespace durch den definierten Kurznamen qualifiziert werden können (und müssen). Die `open`-Direktive gilt für den gesamten Namespace Block in einer Datei.

Auf einen Typ oder Aufruf baren Wert, der in einem anderen Namespace definiert ist, der nicht im aktuellen Namespace geöffnet ist, muss mit seinem voll qualifizierten Namen darauf verwiesen werden.
Beispielsweise muss ein Vorgang mit dem Namen `Op` im `X.Y`-Namespace mit dem voll qualifizierten Namen `X.Y.Op`referenziert werden, es sei denn, der `X.Y`-Namespace wurde zuvor im aktuellen Block geöffnet. Wie bereits erwähnt, ist es nicht möglich, auf den Vorgang als `Y.Op`zu verweisen, auch wenn der `X` Namespace geöffnet wurde.
Wenn ein Kurzname `Z` für `X.Y` in diesem Namespace und in der Datei definiert ist, muss `Op` als `Z.Op`bezeichnet werden. 

```qsharp
namespace NS {

    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

Es ist in der Regel besser, einen Namespace mit einer `open`-Direktive einzubeziehen.
Die Verwendung eines voll qualifizierten Namens ist erforderlich, wenn zwei Namespaces Konstrukte mit dem gleichen Namen definieren und die aktuelle Quelle Konstrukte aus beidem verwendet.

## <a name="formatting"></a>Formatierung

Die meisten Q #-Anweisungen und-Direktiven enden mit einem abschließenden Semikolon, `;`.
-Anweisungen und-Deklarationen wie `for` und `operation`, die mit einem-Anweisungsblock enden, erfordern kein abschließendes Semikolon.
Jede Anweisungs Beschreibung gibt an, ob das abschließende Semikolon erforderlich ist.

Anweisungen, wie Ausdrücke, Deklarationen und Direktiven, werden möglicherweise über mehrere Zeilen hinweg aufgeteilt.
Das vorhanden sein mehrerer Anweisungen in einer einzelnen Zeile sollte vermieden werden.

## <a name="statement-blocks"></a>Anweisungsblöcke

Q #-Anweisungen werden in Anweisungsblöcke gruppiert.
Ein Anweisungsblock beginnt mit einem öffnenden `{` und endet mit einem schließenden `}`.

Ein Anweisungsblock, der lexikalisch in einem anderen-Block eingeschlossen ist, wird als Teil Block des enthaltenden Blocks angesehen; enthaltende-und-Unterblöcke werden auch als äußere und innere Blöcke bezeichnet.

## <a name="symbol-binding-and-assignment"></a>Symbol Bindung und-Zuweisung

Q # unterscheidet zwischen veränderbaren und unveränderlichen Symbolen.
Im Allgemeinen wird die Verwendung unveränderlicher Symbole empfohlen, da es dem Compiler ermöglicht, weitere Optimierungen auszuführen.

Die linke Seite der Bindung besteht aus einem symboltupel und der rechten Seite eines Ausdrucks.

Da es sich bei allen Q #-Typen um Werttypen handelt, bei denen die Qubits eine etwas besondere Rolle übernimmt, wird formal eine Kopie erstellt, wenn ein Wert an ein Symbol gebunden ist oder wenn ein Symbol erneut erstellt wird. Dies heißt, dass das Verhalten von Q # identisch ist, wenn eine Kopie bei der Zuweisung erstellt wurde. Dies gilt insbesondere für Arrays. Natürlich werden in der Praxis nur die relevanten Teile bei Bedarf neu erstellt. 

### <a name="tuple-deconstruction"></a>Tupelerstellung

Wenn die Rechte Seite der Bindung ein Tupel ist, kann dieses Tupel bei der Zuweisung dekonstruiert werden.
Solche Dekonstruktionen können geschaltete Tupel einschließen, und jede vollständige oder partielle Dekonstruktion ist gültig, solange die Form des Tupels auf der rechten Seite mit der Form des symboltupels kompatibel ist.
Die Dekonstruktion von Tupeln kann insbesondere dann auch verwendet werden, wenn die Rechte Seite des `=` ein tupelwertausdruck ist.

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a>Unveränderliche Symbole

Unveränderliche Symbole werden mithilfe der `let`-Anweisung gebunden.
Dies entspricht ungefähr der Variablen Deklaration und Initialisierung in Sprachen wie C#, mit dem Unterschied, dass Q #-Symbole nach der Bindung möglicherweise nicht geändert werden. `let` Bindungen sind unveränderlich.

Eine unveränderliche Bindung besteht aus dem Schlüsselwort `let`, gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=`, einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.
Der Typ der gebundenen Symbole wird basierend auf dem Ausdruck auf der rechten Seite abgeleitet.

### <a name="mutable-symbols"></a>Änderbare Symbole

Änderbare Symbole werden mithilfe der `mutable` Anweisung definiert und initialisiert.
Symbole, die als Teil einer `mutable` Anweisung deklariert und gebunden werden, können später im Code an einen anderen Wert zurückgebunden werden. 

Eine änderbare Bindungs Anweisung besteht aus dem Schlüsselwort `mutable`, gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=`, einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.
Der Typ der gebundenen Symbole wird basierend auf dem Ausdruck auf der rechten Seite abgeleitet. Wenn ein Symbol später im Code wieder verwendet wird, wird der Typ nicht geändert, und der gebundene Wert muss mit diesem Typ kompatibel sein.

### <a name="rebinding-of-mutable-symbols"></a>Neubinden von änderbaren Symbolen

Eine änderbare Variable kann mit einer `set`-Anweisung erneut gebunden werden.
Eine solche erneute Bindung besteht aus dem Schlüsselwort `set`, gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=`, einem Ausdruck zum erneuten Binden der Symbole an und einem abschließenden Semikolon.
Der Wert muss mit den Typen der Symbole kompatibel sein, an die er gebunden ist.

#### <a name="apply-and-reassign-statement"></a>Apply-and-REASSIGN-Anweisung

Eine bestimmte Art von Set-Statement, auf die als Apply-and-REASSIGN-Anweisung verwiesen wird, stellt eine bequeme Methode für die Verkettung dar, wenn die Rechte Seite aus der Anwendung eines binären Operators besteht und das Ergebnis an das linke Argument des Operators zurückgesetzt werden soll. Beispiel:
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
erhöht den Wert des Zählers `counter` in jeder Iterationen der `for` Schleife. Der obige Code entspricht 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
Ähnliche Anweisungen sind für alle binären Operatoren verfügbar, in denen der Typ der linken Seite mit dem Ausdruckstyp übereinstimmt. Dies stellt beispielsweise eine bequeme Möglichkeit zum Sammeln von Werten dar:
```qsharp
mutable results = new Result[0];
for (q in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a>Update-and-REASSIGN-Anweisung

Eine ähnliche Verkettung ist für Kopier-und Update Ausdrücke auf der rechten Seite vorhanden. Entsprechend sind Update-und-REASSIGN-Anweisungen für benannte Elemente in benutzerdefinierten Typen sowie für Array Elemente vorhanden.  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function AddAll (reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

Im Fall von Arrays enthalten unsere Standardbibliotheken die erforderlichen Tools für viele gängige Anforderungen an die Initialisierung und Bearbeitung von Arrays. dadurch ist es nicht mehr erforderlich, Array Elemente an erster Stelle zu aktualisieren. Update-und-REASSIGN-Anweisungen stellen bei Bedarf eine Alternative dar:

```qsharp
operation RandomInts(maxInt : Int, nrSamples : Int) : Int[] {

    mutable samples = new Double[0];
    for (i in 1 .. nrSamples) {
        set samples += [RandomInt(maxInt)];
    }
    return samples;
}

operation SampleUniformDistr(nrSamples : Int, prec : Int) : Double[] {

    let normalization = 1. / IntAsDouble(prec);
    mutable samples = RandomInts(prec, nrSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

> [!TIP]   
> Vermeiden Sie unnötige Verwendung von Update-und-REASSIGN-Anweisungen, indem Sie die in <xref:microsoft.quantum.arrays>bereitgestellten Tools nutzen.

Die-Funktion
```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
{
    mutable pauliArray = new Pauli[n];
    for (index in 0 .. n - 1) {
        set pauliArray w/= index <- 
            index == location ? pauli | PauliI;
    }    
    return pauliArray;
}
```
kann z. b. einfach mithilfe der in `Microsoft.Quantum.Arrays``ConstantArray` Funktion vereinfacht werden und gibt einen Copy-and-Update-Ausdruck zurück:

```qsharp
function EmbedPauli (pauli : Pauli, i : Int, n : Int) : Pauli[] {
    return ConstantArray(n, PauliI) w/ i <- pauli;
}
```

### <a name="binding-scopes"></a>Bindungs Bereiche

Im allgemeinen verlassen Symbol Bindungen den Gültigkeitsbereich und werden am Ende des Anweisungsblocks, in dem Sie auftreten, inaktiv.
Für diese Regel gibt es zwei Ausnahmen:

- Die Bindung der Schleifen Variablen einer `for`-Schleife liegt im Gültigkeitsbereich des Texts der for-Schleife, aber nicht nach dem Ende der Schleife.
- Alle drei Teile eines `repeat`/`until`-Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich behandelt, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.

Für beide Schleifen Typen wird jeder Durchlauf der Schleife in einem eigenen Bereich ausgeführt, sodass Bindungen aus einem früheren Durchlauf in einem späteren Durchlauf nicht verfügbar sind.

Symbol Bindungen aus äußeren Blöcken werden von inneren Blöcken geerbt.
Ein Symbol kann nur einmal pro Block gebunden werden. Es ist unzulässig, ein Symbol mit dem gleichen Namen wie ein anderes Symbol zu definieren, das sich im Gültigkeitsbereich befindet (kein "shadodown").
Die folgenden Sequenzen sind zulässig:

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

und der

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
```

Dies wäre jedoch unzulässig:

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

wie folgt:

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="control-flow"></a>Ablaufsteuerung

### <a name="for-loop"></a>For-Schleife

Die `for`-Anweisung unterstützt Iterationen über einen ganzzahligen Bereich oder über ein Array.
Die-Anweisung besteht aus dem Schlüsselwort `for`, einer öffnenden Klammer `(`, gefolgt von einem Symbol-oder symboltupel, dem Schlüsselwort `in`, einem Ausdruck vom Typ `Range` oder Array, einer schließenden Klammer `)`und einem Anweisungsblock.

Der Anweisungsblock (der Hauptteil der Schleife) wird wiederholt ausgeführt, wobei die definierten Symbole (die Schleifen Variablen) an jeden Wert im Bereich oder Array gebunden sind.
Beachten Sie, dass der Text nicht ausgeführt wird, wenn der Bereichs Ausdruck zu einem leeren Bereich oder Array ausgewertet wird.
Der Ausdruck wird vor der Eingabe der Schleife vollständig ausgewertet und ändert sich nicht, während die Schleife ausgeführt wird.

Die Bindung der deklarierten Symbole ist unveränderlich und folgt denselben Regeln wie andere Variablen Bindungen. Insbesondere ist es möglich, bei der Zuweisung zu den Schleifen Variablen z. b. Array Elemente für eine Iterationen über ein Array zu strukturieren.

Beispiel:

```qsharp
// ...
for (qb in qubits) { // qubits contains a Qubit[]
    H(qb);
}

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {
    set results w/= index <- (index, M(qubits[index]));
}

mutable accumulated = 0;
for ((index, measured) in results) {
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

Die Schleifenvariable wird an jedem Eingang an den Schleifen Text gebunden, und die Bindung am Ende des Texts wird aufgehoben.
Insbesondere wird die Schleifenvariable nicht gebunden, nachdem die for-Schleife abgeschlossen wurde.

### <a name="repeat-until-success-loop"></a>Repeat-Until-Success-Schleife

Die `repeat`-Anweisung unterstützt das Quantum-Muster "Wiederholung bis Erfolg".
Sie besteht aus dem Schlüsselwort `repeat`, gefolgt von einem Anweisungsblock ( _Schleifen_ Text), dem Schlüsselwort `until`, einem booleschen Ausdruck und einem abschließenden Semikolon oder dem Schlüsselwort `fixup` gefolgt von einem anderen Anweisungsblock (der _Fixup_).
Der Schleifen Text, die Bedingung und das Fixup werden als einzelner Bereich betrachtet, sodass im Text gebundene Symbole in der Bedingung und dem Fixup verfügbar sind.

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qs);
    let success = ComputeSuccessIndicator(qs);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qs);
}
```

Der Schleifen Text wird ausgeführt, und anschließend wird die Bedingung ausgewertet.
Wenn die Bedingung true ist, wird die-Anweisung abgeschlossen. Andernfalls wird das Fixup ausgeführt, und die Anweisung wird erneut ausgeführt, beginnend mit dem Schleifen Text.
Beachten Sie, dass das Abschließen der Ausführung des Fixup den Bereich für die-Anweisung beendet, sodass Symbol Bindungen, die während des Texts oder Fixup erstellt werden, in nachfolgenden Wiederholungen nicht verfügbar sind.

Der folgende Code ist z. b. eine probabilistische Verbindung, die ein wichtiges Drehungs Gate implementiert $V _3 = (\boldone + 2 i)/\sqrt{5}$ mithilfe von Hadamard und t Gates.
Die Schleife wird im Durchschnitt 8/5 Wiederholungen beendet.
Weitere Informationen finden Sie [*unter Repeat-Until-Success: nicht deterministische Zerlegung von Single-Qubit-uniflüssen*](https://arxiv.org/abs/1311.1074) ("Petznick" und "svore", 2014).

```qsharp
using (anc = Qubit()) {
    repeat {
        H(anc);
        T(anc);
        CNOT(target,anc);
        H(anc);
        Adjoint T(anc);
        H(anc);
        T(anc);
        H(anc);
        CNOT(target,anc);
        T(anc);
        Z(target);
        H(anc);
        let result = M(anc);
    } until (result == Zero);
}
```

> [!TIP]   
> Vermeiden Sie die Verwendung von Wiederholungs-bis-Erfolg-Schleifen innerhalb von Funktionen. Die entsprechende Funktionalität wird von while-Schleifen in Funktionen bereitgestellt. 

### <a name="while-loop"></a>While-Schleife

Wiederholungs-bis-Erfolg-Muster verfügen über eine sehr Quantum-spezifische-Anmerkung. Sie werden häufig in bestimmten Klassen von Quantum-Algorithmen verwendet. Dies ist daher das dedizierte Sprachkonstrukt in f #. Allerdings müssen Schleifen, die basierend auf einer Bedingung unterbrechen und deren Ausführungsdauer zur Kompilierzeit nicht bekannt ist, mit bestimmter Sorgfalt in einer Quantum-Laufzeit behandelt werden. Die Verwendung in Funktionen andererseits ist nicht problematisch, da diese nur Code enthalten, der auf herkömmlicher (nicht Quantum-) Hardware ausgeführt wird. 

F # unterstützt daher die Verwendung von while-Schleifen nur innerhalb von Functions. Eine `while`-Anweisung besteht aus dem Schlüsselwort `while`, einer öffnenden Klammer `(`, einer Bedingung (d. h. einem booleschen Ausdruck), einer schließenden Klammer `)`und einem Anweisungsblock.
Der Anweisungsblock (der Text der Schleife) wird ausgeführt, solange die Bedingung als `true`ausgewertet wird.

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a>Bedingte Anweisung

Die `if`-Anweisung unterstützt die bedingte Ausführung.
Sie besteht aus dem Schlüsselwort `if`, einer öffnenden Klammer `(`, einem booleschen Ausdruck, einer schließenden Klammer `)`und einem Anweisungsblock (der _Then_ -Block).
Auf diese kann eine beliebige Anzahl von else-if-Klauseln folgen, von denen jede aus dem Schlüsselwort `elif`, einer öffnenden Klammer `(`, einem booleschen Ausdruck, einer schließenden Klammer `)`und einem Anweisungsblock (der _else-if-_ Block) besteht.
Schließlich kann die Anweisung optional mit einer Else-Klausel abgeschlossen werden, die aus dem Schlüsselwort besteht `else` gefolgt von einem anderen Anweisungsblock (der _else_ -Block).
Die Bedingung wird ausgewertet, und wenn der Wert true ist, wird der then-Block ausgeführt.
Wenn die Bedingung false ist, wird die erste else-if-Bedingung ausgewertet. Wenn der Wert true ist, wird der Else-If-Block ausgeführt.
Andernfalls wird der zweite Else-If-Block getestet, dann der dritte, usw., bis entweder eine-Klausel mit einer true-Bedingung gefunden wird oder keine else-if-Klauseln mehr vorhanden sind.
Wenn die ursprüngliche if-Bedingung und alle else-if-Klauseln als false ausgewertet werden, wird der Else-Block ausgeführt, wenn ein solcher angegeben wurde.

Beachten Sie, dass der ausgeführte Block in seinem eigenen Bereich ausgeführt wird.
Bindungen, die innerhalb eines then-, else-if-oder Else-Blocks erstellt werden, sind nach dem Ende der if-Anweisung nicht sichtbar.

Beispiel:

```qsharp
if (result == One) {
    X(target);
} 
```

oder

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a>return

Die Return-Anweisung beendet die Ausführung eines Vorgangs oder einer Funktion und gibt einen Wert an den Aufrufer zurück.
Er besteht aus dem Schlüsselwort `return`, gefolgt von einem Ausdruck des entsprechenden Typs und einem abschließenden Semikolon.

Ein Aufruf bares Element, das ein leeres Tupel zurückgibt, `()`, erfordert keine Return-Anweisung.
Wenn eine frühe Beendigung gewünscht ist, können `return ()` in diesem Fall verwendet werden.
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

### <a name="fail"></a>Fail

Die Fail-Anweisung beendet die Ausführung eines Vorgangs und gibt einen Fehlerwert an den Aufrufer zurück.
Er besteht aus dem Schlüsselwort `fail`, gefolgt von einer Zeichenfolge und einem abschließenden Semikolon.
Die Zeichenfolge wird als Fehlermeldung an den klassischen Treiber zurückgegeben.

Es gibt keine Einschränkung für die Anzahl der Fail-Anweisungen innerhalb eines Vorgangs.
Der Compiler gibt möglicherweise eine Warnung aus, wenn-Anweisungen einer Fail-Anweisung innerhalb eines-Blocks folgen.

Beispiel:

```qsharp
fail $"Impossible state reached";
```

oder

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a>Qubit-Verwaltung

Beachten Sie, dass keine dieser Anweisungen innerhalb des Texts einer Funktion zulässig ist.
Sie sind nur innerhalb von Vorgängen gültig.

### <a name="clean-qubits"></a>Löschen von Qubits

Die `using`-Anweisung wird verwendet, um neue Qubits für die Verwendung während eines-Anweisungsblocks abzurufen.
Es ist garantiert, dass die Qubits mit dem Berechnungs `Zero` Zustand initialisiert werden.
Die Qubits sollten sich am Ende des Anweisungsblocks im Status der Berechnungs `Zero` befinden. Simulatoren werden empfohlen, dies zu erzwingen.

Die-Anweisung besteht aus dem Schlüsselwort `using`, gefolgt von einer öffnenden Klammer `(`, einer Bindung, einer schließenden Klammer `)`und dem Anweisungsblock, in dem die Qubits verfügbar sein werden.
Die Bindung folgt dem gleichen Muster wie `let`-Anweisungen: entweder ein einzelnes Symbol oder ein Tupel von Symbolen, gefolgt von einem Gleichheitszeichen `=`und entweder ein einzelner Wert oder ein entsprechendes Tupel von Initialisierern.
Initialisierer sind entweder für ein einzelnes Qubit, das als `Qubit()`angegeben wird, oder ein Array von Qubits verfügbar, das durch `Qubit[`, einen `Int` Ausdruck und `]`angegeben wird.

Beispiel:

```qsharp
using (q = Qubit()) {
    // ...
}
using ((ancilla, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="dirty-qubits"></a>Geänderte Qubits

Die `borrowing`-Anweisung wird verwendet, um Qubits für die temporäre Verwendung abzurufen. Die-Anweisung besteht aus dem Schlüsselwort `borrowing`, gefolgt von einer öffnenden Klammer `(`, einer Bindung, einer schließenden Klammer `)`und dem Anweisungsblock, in dem die Qubits verfügbar sein werden.
Die Bindung folgt demselben Muster und denselben Regeln wie in einer `using`-Anweisung.

Beispiel:

```qsharp
borrowing (q = Qubit()) {
    // ...
}
borrowing ((ancilla, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

Die geliehenen Qubits befinden sich in einem unbekannten Zustand und verlassen den Gültigkeitsbereich am Ende des Anweisungsblocks.
Der Kreditnehmer führt einen Commit aus, um die Qubits in demselben Zustand zu belassen, in dem Sie sich befanden, d. h., ihr Zustand am Anfang und am Ende des Anweisungsblocks ist erwartungsgemäß identisch.
Dabei handelt es sich nicht unbedingt um einen klassischen Zustand, der in den meisten Fällen keine Messungen enthalten sollte. 

Solche Qubits werden oft als "Dirty Ancilla" bezeichnet.
Ein Beispiel für die Verwendung von modifiziertem Ancilla finden [*Sie unter Factoring mithilfe von 2N + 2 Qubits mit Toffoli-basierter Modularität*](https://arxiv.org/abs/1611.07995) (Haner, roetteler und svore 2017).

Beim Abgleich von Qubits versucht das System zunächst, die Anforderung von Qubits auszufüllen, die verwendet werden, auf die jedoch nicht während des Texts der `borrowing` Anweisung zugegriffen wird.
Wenn nicht genügend derartige Qubits vorhanden sind, werden neue Qubits zum Durchführen der Anforderung zugeteilt.

## <a name="conjugations"></a>Konjugationen

Im Gegensatz zu klassischen Bits ist das Freigeben von Quantum-Speicher etwas komplizierter, da das Blind Zurücksetzen von Qubits unerwünschte Auswirkungen auf die verbleibende Berechnung haben kann, wenn die Qubits noch entkoppelt sind. Dies kann vermieden werden, indem Berechnungen vor der Freigabe des Arbeitsspeichers ordnungsgemäß durchgeführt werden. Ein gängiges Muster in Quantum Computing ist daher Folgendes: 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

: neu: ab unserer Version 0,9 wird eine Konjugations Anweisung unterstützt, die die oben beschriebene Transformation implementiert. Mithilfe dieser Anweisung kann der Vorgang `ApplyWith` folgendermaßen implementiert werden:

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
Eine solche Konjugation-Anweisung wird deutlich nützlicher, wenn die äußere und die innere Transformation nicht als Vorgänge verfügbar sind, sondern eher durch einen Block, der aus mehreren Anweisungen besteht, beschreibbar ist. 

Die umgekehrte Transformation für die-Anweisungen, die im-Block innerhalb von definiert sind, wird automatisch vom Compiler generiert und nach Abschluss von Apply-Block ausgeführt. Da alle änderbaren Variablen, die als Teil des Blocks innerhalb von verwendet werden, im Apply-Block nicht wieder hergestellt werden können, ist die generierte Transformation garantiert das Adjoint der Berechnung im within-Block. 

## <a name="expression-evaluation-statements"></a>Ausdrucks Auswertungs Anweisungen

Jeder aufrufsausdruck vom Typ "`Unit`" kann als Anweisung verwendet werden.
Dies wird hauptsächlich beim Aufrufen von Vorgängen für Qubits verwendet, die `Unit` zurückgeben, da der Zweck der Anweisung darin besteht, den impliziten Quantum-Zustand zu ändern.
Ausdrucks Auswertungs Anweisungen erfordern ein abschließendes Semikolon.

Beispiel:

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
