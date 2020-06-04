---
title: 'Typausdrücke in Q #'
description: 'Erfahren Sie, wie Konstanten, Variablen, Operatoren, Vorgänge und Funktionen als Ausdrücke in Q # angegeben, referenziert und kombiniert werden.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
ms.openlocfilehash: c4b2cc0bed44ffdfb191ba522d6526959e7c6708
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327304"
---
# <a name="type-expressions-in-q"></a>Typausdrücke in Q #

## <a name="numeric-expressions"></a>Numerische Ausdrücke

Numerische Ausdrücke sind Ausdrücke vom Typ `Int` , `BigInt` oder `Double` .
Das heißt, Sie sind entweder ganzzahlige oder Gleit Komma Zahlen.

`Int`Literale in Q # werden einfach als Sequenz von Ziffern geschrieben.
Hexadezimale und binäre ganze Zahlen werden mit dem `0x` `0b` Präfix und bzw. unterstützt.

`BigInt`Literale in Q # werden mit einem nachfolgenden- `l` oder- `L` Suffix geschrieben.
Hexadezimale große ganze Zahlen werden mit dem Präfix "0x" unterstützt.
Daher sind die folgenden alle gültigen Verwendungsmöglichkeiten von `BigInt` Literalen:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`Literale in Q # sind Gleit Komma Zahlen, die mithilfe von Dezimalziffern geschrieben werden.
Sie können mit einem Dezimaltrennzeichen () `.` und/oder einem exponentiellen Teil geschrieben werden, der mit "e" oder "e" angegeben wird (nach dem nur ein mögliches negatives Vorzeichen und Dezimalziffern gültig sind).
Die folgenden `Double` Literale sind gültig: `0.0` , `1.2e5` , `1e-5` .

Wenn ein Array Ausdruck eines beliebigen Elementtyps vorhanden ist, `Int` kann ein Ausdruck mithilfe der [`Length`](xref:microsoft.quantum.core.length) integrierten Funktion gebildet werden, wobei der Array Ausdruck in Klammern eingeschlossen ist, `(` und `)` .
Wenn beispielsweise `a` an ein Array gebunden ist, dann `Length(a)` ist ein ganzzahliger Ausdruck.
Wenn `b` ein Array von Arrays ganzer Zahlen ist, `Int[][]` dann `Length(b)` ist die Anzahl der Unterarrays in `b` , und `Length(b[1])` die Anzahl von ganzen Zahlen im zweiten Unterarray in `b` .

Bei zwei numerischen Ausdrücken desselben Typs können die binären Operatoren, `+` , `-` `*` und `/` verwendet werden, um einen neuen numerischen Ausdruck zu bilden.
Der Typ des neuen Ausdrucks ist mit den Typen der einzelnen Ausdrücke identisch.

Bei zwei ganzzahligen Ausdrücken kann der binäre Operator `^` (Power) verwendet werden, um einen neuen ganzzahligen Ausdruck zu bilden.
Auf ähnliche Weise `^` kann mit zwei doppelten Ausdrücken verwendet werden, um einen neuen doppelten Ausdruck zu bilden.
Schließlich `^` kann mit einer großen Ganzzahl auf der linken Seite und einer Ganzzahl auf der rechten Seite verwendet werden, um einen neuen großen ganzzahligen Ausdruck zu bilden.
In diesem Fall muss der zweite Parameter in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.

Bei zwei ganzzahligen oder großen ganzzahligen Ausdrücken kann ein neuer Integer-Ausdruck oder ein großer ganzzahliger Ausdruck mit den `%` Operatoren (Modulus), (bitweiser `&&&` and), `|||` (bitweiser or) oder `^^^` (Bitweiser XOR) gebildet werden.

Beim Ausdruck "Integer" oder "Big Integer" auf der linken Seite und einem ganzzahligen Ausdruck auf der rechten Seite `<<<` können die Operatoren (arithmetischer Left Shift) oder `>>>` (arithmetischer rechts Schiebe Operator) zum Erstellen eines neuen Ausdrucks mit dem gleichen Typ wie der linke Ausdruck verwendet werden.

Der zweite Parameter (die UMSCHALT Menge) in einen Verschiebungs Vorgang muss größer oder gleich 0 (null) sein. das Verhalten für negative Verschiebungs Beträge ist nicht definiert.
Der Verschiebungs Betrag für einen der Verschiebungs Vorgänge muss ebenfalls in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.
Wenn die zu Verschiebe Zahl eine ganze Zahl ist, wird der Verschiebungs Betrag interpretiert, d `mod 64` . h. eine Verschiebung von 1 und eine Schicht von 65 haben dieselbe Wirkung.

Bei ganzzahligen und großen ganzzahligen Werten sind Verschiebungen arithmetisch.
Wenn Sie einen negativen Wert entweder nach links oder rechts verschieben, ergibt dies eine negative Zahl.
Das heißt, die Verschiebung eines Schritts nach links oder rechts ist identisch mit der Multiplikation bzw. Division durch 2.

Die ganzzahlige Division und der ganzzahlige Modulo folgen dem Verhalten für negative Zahlen wie c#.
Das heißt, dass `a % b` immer dasselbe Vorzeichen wie hat `a` und `b * (a / b) + a % b` immer gleich ist `a` .
Beispiel:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

Große ganzzahlige Division und Modulo funktionieren auf dieselbe Weise.

Wenn ein beliebiger numerischer Ausdruck vorhanden ist, kann ein neuer Ausdruck mit dem `-` unären Operator gebildet werden.
Der neue Ausdruck hat denselben Typ wie der konstituierende Ausdruck.

Bei allen ganzzahligen oder großen ganzzahligen Ausdrücken kann ein neuer Ausdruck desselben Typs mit dem `~~~` unären Operator (bitweiser Komplement) gebildet werden.

## <a name="boolean-expressions"></a>Boolesche Ausdrücke

Die beiden `Bool` Literalwerte sind `true` und `false` .

Wenn zwei Ausdrücke desselben primitiven Typs vorhanden sind, können die `==` `!=` binären Operatoren und verwendet werden, um einen-Ausdruck zu erstellen `Bool` .
Der Ausdruck ist true, wenn die beiden Ausdrücke gleich sind, andernfalls false.

Werte von benutzerdefinierten Typen können nicht verglichen werden, sondern es können nur Ihre nicht umschließenden Werte verglichen werden. Verwenden Sie beispielsweise den "Unwrap"-Operator `!` (ausführlich unter [Typen in f #](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)erläutert).

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Der Gleichheits Vergleich für `Qubit` Werte ist die Identitäts Gleichheit, d. h., ob die beiden Ausdrücke dasselbe Qubit identifizieren.
Der Zustand der beiden Qubits wird von diesem Vergleich nicht verglichen, auf Sie zugegriffen, gemessen oder geändert.

Der Gleichheits Vergleich für `Double` Werte kann aufgrund von Rundungs Effekten irreführend sein.
Beispielsweise `49.0 * (1.0/49.0) != 1.0` .

Bei zwei numerischen Ausdrücken können die binären Operatoren,, `>` `<` `>=` und `<=` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der erste Ausdruck größer als, kleiner als, größer als oder gleich oder kleiner oder gleich dem zweiten Ausdruck ist.

Bei zwei booleschen Ausdrücken `and` `or` können die binären Operatoren und verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn beide Ausdrücke den Wert true haben.

Bei jedem booleschen Ausdruck kann der `not` unäre Operator verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der konstituierende Ausdruck false ist.

## <a name="string-expressions"></a>Zeichen folgen Ausdrücke

Q # ermöglicht die Verwendung von Zeichen folgen in der `fail` Anweisung (erläutert in der [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow#fail-statement)) und in der [`Message`](xref:microsoft.quantum.intrinsic.message) Standardfunktion.
Das spezifische Verhalten der letzteren hängt von dem verwendeten Simulator ab, schreibt jedoch in der Regel eine Meldung in die Host Konsole, wenn Sie während eines Q #-Programms aufgerufen wird.

Zeichen folgen in Q # sind entweder Literale oder interpoliert Zeichen folgen.

Zeichenfolgenliterale ähneln in den meisten Sprachen einfachen Zeichenfolgenliteralen: eine Sequenz von Unicode-Zeichen, die in doppelten Anführungszeichen eingeschlossen sind `"` .
Innerhalb einer Zeichenfolge kann der umgekehrte Schrägstrich `\` verwendet werden, um ein doppeltes Anführungszeichen mit Escapezeichen zu versehen und eine neue Zeile als einzufügen, als `\n` und als `\r` Tabstopp Zeichen `\t` .
Zum Beispiel:

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>Interpolierte Zeichenfolgen

Die Q #-Syntax für Zeichen folgen Interpolationen ist eine Teilmenge der c#-Syntax, aber wir fassen hier die wichtigsten Punkte zusammen, die Sie für Q # betreffen.
Die wichtigsten Unterschiede werden im folgenden erläutert.

Wenn Sie ein Zeichenfolgenliteral als interpolierte Zeichenfolge ermitteln möchten, stellen Sie ihm ein `$`-Symbol voran.
Zwischen dem `$` und dem `"` , das einen zeichenfolgenliteralvorgang startet, darf kein Leerraum vorhanden sein.

Im folgenden finden Sie ein einfaches Beispiel, in dem die-Funktion verwendet wird [`Message`](xref:microsoft.quantum.intrinsic.message) , um das Ergebnis einer Maßeinheit zusammen mit anderen Q #-Ausdrücken in die Konsole zu schreiben.

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```
Jeder gültige Q #-Ausdruck kann in einer interinterierten Zeichenfolge angezeigt werden.

Weitere Informationen zur c#-Syntax finden Sie unter [*interpoliert*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).
Der wichtigste Unterschied besteht darin, dass Q # keine ausführlichen (mehrzeiligen) interpoliert-Zeichen folgen unterstützt.
Ausdrücke in einer interinterierten Zeichenfolge Folgen der Q #-Syntax, nicht der c#-Syntax.

## <a name="range-expressions"></a>Bereichs Ausdrücke

Bei allen drei `Int` Ausdrücken `start` `step` ist, und `stop` `start .. step .. stop` ein Bereichs Ausdruck, dessen erstes Element `start` , zweites Element `start+step` , drittes Element `start+step+step` , usw. ist, bis `stop` übergeben wird.
Ein Bereich kann leer sein, wenn z.b. `step` positiv und ist `stop < start` .
Das letzte Element des Bereichs `stop` ist, wenn der Unterschied zwischen `start` und ein ganzzahliges `stop` Vielfaches von ist, d. h `step` ., der Bereich ist an beiden Enden inklusiv.

`Int`Bei zwei Ausdrücken `start` und `stop` `start .. stop` ist ein Bereichs Ausdruck, der gleich ist `start .. 1 .. stop` .
Beachten Sie, dass der implizierte Wert `step` + 1 ist, auch wenn `stop` kleiner als ist `start` . in einem solchen Fall ist der Bereich leer.

Einige Beispiel Bereiche sind:

- `1..3`der Bereich von 1, 2, 3.
- `2..2..5`ist der Bereich von 2, 4.
- `2..2..6`ist der Bereich von 2, 4, 6.
- `6..-2..2`der Bereich ist 6, 4, 2.
- `2..1`der leere Bereich.
- `2..6..7`der Bereich 2.
- `2..2..1`der leere Bereich.
- `1..-1..2`der leere Bereich.

## <a name="qubit-expressions"></a>Qubit-Ausdrücke

Die einzigen `Qubit` Ausdrücke sind Symbole, die an `Qubit` Werte oder Array Elemente von Arrays gebunden sind `Qubit` .
Es sind keine `Qubit` Literale vorhanden.

## <a name="pauli-expressions"></a>Pauli-Ausdrücke

Die vier Werte,,, `Pauli` `PauliI` `PauliX` `PauliY` und `PauliZ` sind gültige `Pauli` Ausdrücke.

Abgesehen davon sind die einzigen `Pauli` Ausdrücke Symbole, die an `Pauli` Werte oder Array Elemente von Arrays gebunden sind `Pauli` .

## <a name="result-expressions"></a>Ergebnis Ausdrücke

Die beiden `Result` Werte `One` und `Zero` sind gültige `Result` Ausdrücke.

Abgesehen davon sind die einzigen `Result` Ausdrücke Symbole, die an `Result` Werte oder Array Elemente von Arrays gebunden sind `Result` .
Beachten Sie insbesondere, dass `One` nicht mit der ganzen Zahl identisch ist `1` , und es gibt keine direkte Konvertierung zwischen Ihnen.
Das gleiche gilt für `Zero` und `0` .

## <a name="tuple-expressions"></a>Tupelausdrücke

Ein tupelliteral ist eine Sequenz von Element Ausdrücken des entsprechenden Typs, die durch Kommas getrennt sind und in und eingeschlossen sind `(` `)` .
Beispielsweise `(1, One)` ist ein `(Int, Result)` Ausdruck.

Abgesehen von Literalen sind die einzigen Tupelausdrücke Symbole, die an Tupelwerte, Array Elemente von tupelarrays und Aufruf Bare Aufrufe gebunden sind, die Tupel zurückgeben.

## <a name="user-defined-type-expressions"></a>Benutzerdefinierte typausdrücke

Ein Literalwert eines benutzerdefinierten Typs besteht aus dem Typnamen, gefolgt von einem tupelliteraltyp mit dem basistupeltyp des Typs.
Wenn beispielsweise `IntPair` ein benutzerdefinierter Typ ist, der auf basiert `(Int, Int)` , dann `IntPair(2, 3)` wäre ein gültiges Literale dieses Typs.

Anders als Literale sind die einzigen Ausdrücke eines benutzerdefinierten Typs Symbole, die an Werte dieses Typs gebunden sind, Array Elemente von Arrays dieses Typs und Aufruf Bare Aufrufe, die diesen Typ zurückgeben.

## <a name="unwrap-expressions"></a>Entpacken von Ausdrücken

In Q # ist der Unwrap-Operator ein nach gestelltes Ausrufezeichen `!` .
Wenn beispielsweise `IntPair` ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ `(Int, Int)` und `s` eine Variable mit Wert ist `IntPair(2, 3)` , `s!` wäre `(2, 3)` .

Für benutzerdefinierte Typen, die in Bezug auf andere benutzerdefinierte Typen definiert sind. der Unwrap-Operator kann wiederholt werden. gibt beispielsweise `s!!` den doppelt entpackten Wert von an `s` .
Wenn also `WrappedPair` ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ `IntPair` und `t` eine Variable mit Wert ist `WrappedPair(IntPair(1,2))` , dann ist `t!!` `(1,2)` .

Der `!` Operator hat eine höhere Rangfolge als alle anderen Operatoren, außer `[]` für die Array Indizierung und die Slicing.
`!`und `[]` binden Sie Positions bedingt, d. h., Sie `a[i]![3]` sollten als gelesen werden `((a[i])!)[3]` : nehmen `i` Sie das ' th '-Element von `a` , entpacken Sie es, und dann das dritte Element des nicht umschließenden Werts (der ein Array sein muss).

Die Rangfolge des `!` Operators hat eine Beeinträchtigung, die möglicherweise nicht offensichtlich ist.
Wenn eine Funktion oder ein Vorgang einen Wert zurückgibt, der dann entpackt wird, muss der Funktions-oder Vorgangs Ausdruck in Klammern eingeschlossen werden, damit das Argument Tupel an den-Ausdruck gebunden wird, anstatt an den Unwrap-Vorgang.
Beispiel:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Array Ausdrücke

Ein Arrayliteral ist eine Sequenz von einem oder mehreren Element Ausdrücken, die durch Kommas getrennt sind und in und eingeschlossen ist `[` `]` .
Alle-Elemente müssen mit demselben Typ kompatibel sein.

Bei zwei Arrays desselben Typs kann der binäre `+` Operator verwendet werden, um ein neues Array zu bilden, bei dem es sich um die Verkettung der beiden Arrays handelt.
Beispielsweise `[1,2,3] + [4,5,6]` ist `[1,2,3,4,5,6]` .

### <a name="array-creation"></a>Array Erstellung

Bei Angabe eines Typs und eines `Int` Ausdrucks `new` kann der Operator verwendet werden, um ein neues Array mit der angegebenen Größe zuzuordnen.
Beispielsweise `new Int[i + 1]` würde ein neues `Int` Array mit- `i + 1` Elementen zuordnen.

Leere Array Literale, `[]` , sind nicht zulässig.
Wenn Sie stattdessen verwenden `new ★[0]` , wobei `★` als Platzhalter für einen geeigneten Typ verwendet, ermöglicht das Erstellen des gewünschten Arrays der Länge 0 (null).

Die Elemente eines neuen Arrays werden mit einem typabhängigen Standardwert initialisiert.
In den meisten Fällen ist dies eine Variation von 0 (null).

Bei Qubits und callables, bei denen es sich um Verweise auf Entitäten handelt, gibt es keinen angemessenen Standardwert.
Daher ist für diese Typen der Standardwert ein ungültiger Verweis, der nicht verwendet werden kann, ohne dass ein Laufzeitfehler verursacht wird.
Dies ähnelt einem NULL-Verweis in Sprachen wie c# oder Java.
Arrays, die Qubits oder callables enthalten, müssen ordnungsgemäß mit nicht standardmäßigen Werten initialisiert werden, bevor ihre Elemente problemlos verwendet werden können. Geeignete Initialisierungs Routinen finden Sie unter <xref:microsoft.quantum.arrays> .

Die Standardwerte für jeden Typ lauten:

type | Standard
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | _Ungültiges Qubit_
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | Der leere Bereich,`1..1..0`
 `Callable` | _Ungültige Aufruf Bare_
 `Array['T]` | `'T[0]`

Tupeltypen werden Element für Element initialisiert.


### <a name="array-elements"></a>Array Elemente

Bei einem Array Ausdruck und einem `Int` Ausdruck kann ein neuer Ausdruck mit dem `[` und dem `]` Array Element Operator gebildet werden.
Der neue Ausdruck hat denselben Typ wie der Elementtyp des Arrays.
Wenn beispielsweise `a` an ein Array von s gebunden ist `Double` , dann `a[4]` ist ein- `Double` Ausdruck.

Wenn der Array Ausdruck kein einfacher Bezeichner ist, muss er in Klammern eingeschlossen werden, um ein Element auszuwählen.
Wenn `a` und Beispiels `b` Weise beide Arrays von s sind `Int` , würde ein Element aus der Verkettung wie folgt ausgedrückt werden:

```qsharp
(a + b)[13]
```

Alle Arrays in Q # sind NULL basiert.
Das heißt, das erste Element eines Arrays `a` ist immer `a[0]` .


### <a name="array-slices"></a>Array Slices

Bei einem Array Ausdruck und einem- `Range` Ausdruck kann ein neuer Ausdruck mit dem und dem `[` `]` Array Slice-Operator gebildet werden.
Der neue Ausdruck hat denselben Typ wie das Array und enthält die Array Elemente, die von den Elementen des-Elements indiziert werden `Range` , in der Reihenfolge, die durch definiert wird `Range` .
Wenn beispielsweise `a` an ein Array von s gebunden ist `Double` , dann `a[3..-1..0]` ist ein- `Double[]` Ausdruck, der die ersten vier Elemente von enthält, `a` jedoch in umgekehrter Reihenfolge, wie Sie in angezeigt werden `a` .

Wenn das `Range` leer ist, ist das resultierende Array in der Länge 0 (null).

Ebenso wie beim Verweisen auf Array Elemente muss der Array Ausdruck, wenn es sich nicht um einen einfachen Bezeichner handelt, in Klammern eingeschlossen werden, um Sie in Slices aufzuteilen.
Wenn `a` und `b` beide Arrays von `Int` s sind, würde ein Slice aus der Verkettung folgendermaßen ausgedrückt werden:

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>Abherleitet anfangs-/Endwerte

Ab unserer Version 0,8 unterstützen wir Kontext Ausdrücke für die Bereichs Aufteilung. Insbesondere können Bereichs Start-und Endwerte im Kontext eines Bereichs aufteilen-Ausdrucks weggelassen werden. In diesem Fall wendet der Compiler die folgenden Regeln an, um die vorgesehenen Trennzeichen für den Bereich abzuleiten. 

Wenn z. b. der Bereichs Start Wert weggelassen wird, wird der abherleitet Startwert 
- ist 0 (null), wenn kein Schritt angegeben oder der angegebene Schritt positiv ist. 
- die Länge des aufgeschnittenen Arrays minus 1, wenn der angegebene Schritt negativ ist. 

Wenn der Wert für den Bereichs Endpunkt weggelassen wird, wird der abherende Endwert 
- die Länge des aufgeschnittenen Arrays minus 1, wenn kein Schritt angegeben oder der angegebene Schritt positiv ist. 
- ist 0 (null), wenn der angegebene Schritt negativ ist. 

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

### <a name="copy-and-update-expressions"></a>Copy-und Update-Ausdrücke

Da es sich bei allen Q #-Typen um Werttypen handelt – wobei die Qubits eine etwas besondere Rolle einnehmen – wird formal eine "Kopie" erstellt, wenn ein Wert an ein Symbol gebunden ist oder wenn ein Symbol erneut erstellt wird. Dies heißt, dass das Verhalten von Q # identisch ist, wenn eine Kopie bei der Zuweisung erstellt wurde.
Natürlich werden in der Praxis nur die relevanten Teile bei Bedarf neu erstellt. 

Dies gilt insbesondere für Arrays.
Insbesondere ist es nicht möglich, Array Elemente zu aktualisieren. Zum Ändern eines vorhandenen Arrays muss ein *Kopier-und Aktualisierungs* Mechanismus genutzt werden.

Neue Arrays können über *Kopier-und Update* Ausdrücke aus vorhandenen erstellt werden.
Ein Copy-and-Update-Ausdruck ist ein Ausdruck der Form `expression1 w/ expression2 <- expression3` , wobei `expression1` für einen Typ vom Typ sein muss `T[]` `T` .
Die zweite `expression2` definiert die Indizes der Elemente, die im Vergleich zum Array in geändert werden sollen, `expression1` und muss entweder vom Typ `Int` oder vom Typ sein `Range` .
Wenn `expression2` vom Typ ist `Int` , `expression3` muss vom Typ sein `T` . Wenn `expression2` vom Typ ist `Range` , `expression3` muss vom Typ sein `T[]` .

Ein Copy-and-Update-Ausdruck erstellt `arr w/ idx <- value` ein neues Array, bei dem alle Elemente auf das entsprechende Element in festgelegt `arr` sind, mit Ausnahme der Elemente in `idx` , die auf die 1 (n) in festgelegt sind `value` . Wenn z. b. `arr` ein Array enthält `[0,1,2,3]` , dann 
- `arr w/ 0 <- 10`ist das Array `[10,1,2,3]` .
- `arr w/ 2 <- 10`ist das Array `[0,1,10,3]` .
- `arr w/ 0..2..3 <- [10,12]`ist das Array `[10,1,12,3]` .

#### <a name="copy-and-update-expressions-for-named-items"></a>Copy-und Update-Ausdrücke für benannte Elemente

Ähnliche Ausdrücke sind für benannte Elemente in benutzerdefinierten Typen vorhanden. 

Beachten Sie beispielsweise den-Typ. 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Wenn `c` den Wert des Typs enthält `Complex(1., -1.)` , dann `c w/ Re <- 0.` ist ein Ausdruck vom Typ, der ergibt `Complex` `Complex(0., -1.)` .

### <a name="jagged-arrays"></a>Verzweigte Arrays

Eine Jagged Array, manchmal auch als "Array von Arrays" bezeichnet, ist ein Array, dessen Elemente Arrays sind.
Die Elemente einer Jagged Array können unterschiedlich sein.
Im folgenden Beispiel wird gezeigt, wie Sie eine Jagged Array deklarieren und initialisieren, die eine Multiplikationstabelle darstellt.

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {
    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```

### <a name="arrays-of-callables"></a>Arrays von callables 

Beachten Sie, dass weitere Details zu Aufruf baren Typen unten und auf der nächsten Seite, [Vorgänge und Funktionen in f #](xref:microsoft.quantum.guide.operationsfunctions)gefunden werden können.

Wenn der allgemeine Elementtyp ein Vorgang oder Funktionstyp ist, müssen alle Elemente die gleichen Eingabe-und Ausgabetypen aufweisen.
Der Elementtyp des Arrays unterstützt alle Funktoren, die von allen Elementen unterstützt werden.
Wenn z. b. `Op1` , `Op2` und `Op3` alle sind, unterstützt, unterstützt und unterstützt jedoch `Qubit[] => Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` beide:

- `[Op1, Op2]`ist ein Array von `(Qubit[] => Unit)` Vorgängen.
- `[Op1, Op3]`ist ein Array von `(Qubit[] => Unit is Adj)` Vorgängen.
- `[Op2, Op3]`ist ein Array von `(Qubit[] => Unit is Ctl)` Vorgängen.

Während `(Qubit[] => Unit is Adj)` und `(Qubit[] => Unit is Ctl)` Vorgänge den allgemeinen Basistyp haben `(Qubit[] => Unit)` , beachten Sie jedoch, dass Arrays *of* dieser Operatoren keinen gemeinsamen Basistyp aufweisen. Beispielsweise `[[Op1], [Op2]]` gibt derzeit einen Fehler aus, da versucht wird, ein Array der nicht kompatiblen Array Typen und zu `(Qubit[] => Unit is Adj)[]` Erstellen `(Qubit[] => Unit is Ctl)[]` .


## <a name="conditional-expressions"></a>Bedingte Ausdrücke

Bei zwei anderen Ausdrücken desselben Typs und eines booleschen Ausdrucks kann der bedingte Ausdruck mit dem Fragezeichen `?` und dem senkrechten Strich gebildet werden `|` .
Beispielsweise `a==b ? c | d` .
In diesem Beispiel ist der Wert des bedingten Ausdrucks, wenn den `c` Wert `a==b` true hat und wenn der Wert `d` false ist.

### <a name="conditional-expressions-with-callables"></a>Bedingte Ausdrücke mit callables

Die beiden Ausdrücke können zu Vorgängen ausgewertet werden, die über die gleichen Eingaben und Ausgaben verfügen, aber unterschiedliche Funktions tüktoren unterstützen.
In diesem Fall ist der Typ des bedingten Ausdrucks ein Vorgang mit diesen Eingaben und Ausgaben, der alle von beiden Ausdrücken unterstützten Funktoren unterstützt.
Wenn z. b. `Op1` , `Op2` und `Op3` alle sind, unterstützt, unterstützt und unterstützt jedoch `Qubit[]=>Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` beide:

- `flag ? Op1 | Op2`ist ein- `(Qubit[] => Unit)` Vorgang.
- `flag ? Op1 | Op3`ist ein- `(Qubit[] => Unit is Adj)` Vorgang.
- `flag ? Op2 | Op3`ist ein- `(Qubit[] => Unit is Ctl)` Vorgang.

Wenn einer der beiden möglichen Ergebnis Ausdrücke einen Funktions-oder einen Vorgangs aufzurufen enthält, findet dieser Vorgang nur statt, wenn das Ergebnis das Ergebnis ist, das der Wert des Aufrufes ist.
`a==b ? C(qs) | D(qs)`Wenn Beispiels `a==b` Weise true ist, wird der `C` Vorgang aufgerufen, und wenn false ist, wird nur `D` aufgerufen.
Dies ähnelt der Kurzschluss in anderen Sprachen.

## <a name="callable-expressions"></a>Aufruf Bare Ausdrücke

Ein Aufruf bares Literalelement ist der Name eines Vorgangs oder einer Funktion, der im Kompilierungs Bereich definiert ist.
Beispielsweise ist ein vorgangsliteral, `X` das auf den `X` -Standard Bibliotheks Vorgang verweist, und `Message` ist ein Funktionsliteral, das auf die Standard Bibliotheks `Message` Funktion verweist.

Wenn ein Vorgang das `Adjoint` Funktor unterstützt, `Adjoint op` ist ein Vorgangs Ausdruck.
Entsprechend `Controlled` `Controlled op` ist ein Vorgangs Ausdruck, wenn der Vorgang das Funktor unterstützt.
Die Typen dieser Ausdrücke werden bei Aufrufen von [Vorgangs Spezialisierungs](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)Vorgängen angegeben.

Funktoren ( `Adjoint` und `Controlled` ) werden genauer gebunden als alle anderen Operatoren, mit Ausnahme des Unwrap `!` -Operators und der Array Indizierung mit [] '.
Folglich sind die folgenden Vorgänge zulässig, vorausgesetzt, dass die Vorgänge die verwendeten Funktoren unterstützen:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>Typparametrisierte Aufruf Bare Ausdrücke

Ein Aufruf bares Literale kann als Wert verwendet werden, z. b. um einer Variablen zuzuweisen oder um Sie an eine andere Aufruf Bare zu übergeben.
In diesem Fall müssen Sie, wenn die Aufruf Bare [Typparameter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)aufweist, als Teil des Aufruf baren Werts angegeben werden.
Ein Aufruf barer Wert darf keine nicht angegebenen Typparameter aufweisen.

Wenn beispielsweise `Fun` eine Funktion mit der Signatur ist `'T1->Unit` :

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aufruf Bare Aufruf Ausdrücke

Bei einem Aufruf baren Ausdruck (Operation oder Funktion) und einem Tupelausdruck des Eingabetyps der Aufruf baren Signatur kann ein Aufruf Ausdruck gebildet werden, indem der Tupelausdruck an den Aufruf baren Ausdruck angefügt wird.
Der Typ des Aufruf Ausdrucks ist der Ausgabetyp der Signatur des Callable-Ausdrucks.

Wenn z. b `Op` . ein Vorgang mit der Signatur ist `((Int, Qubit) => Double)` , `Op(3, qubit1)` ist ein Ausdruck vom Typ `Double` .
Ebenso ist, wenn `Sin` eine Funktion mit der Signatur ist `(Double -> Double)` , `Sin(0.1)` ein Ausdruck vom Typ `Double` .
Wenn schließlich `Builder` eine Funktion mit der Signatur ist `(Int -> (Int -> Int))` , dann `Builder(3)` ist eine Funktion von in bis int.

Zum Aufrufen des Ergebnisses eines Aufruf baren Ausdrucks ist ein zusätzliches Paar von Klammern um den Aufruf baren Ausdruck erforderlich.
Um also das Ergebnis des Aufrufs `Builder` aus dem vorherigen Absatz aufzurufen, ist die korrekte Syntax:

```qsharp
(Builder(3))(2)
```

Wenn Sie einen [vom Typ parametrisierten](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) Aufruf baren aufrufen, können die tatsächlichen Typparameter in spitzen Klammern `<` und `>` nach dem Aufruf baren Ausdruck angegeben werden.
Dies ist in der Regel unnötig, da der Q #-Compiler die eigentlichen Typen ableiten wird.
Es *ist* jedoch für die [partielle Anwendung](xref:microsoft.quantum.guide.operationsfunctions#partial-application) erforderlich, wenn ein typparametrisiertes Argument nicht angegeben wird.
Dies ist manchmal auch nützlich, wenn die Übergabe von Vorgängen mit unterschiedlichen Funktoren unterstützt wird.

Wenn beispielsweise `Func` die Signatur aufweist und die Signatur und die Signatur `('T1, 'T2, 'T1) -> 'T2` aufweisen, `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` um `Func` mit `Op1` als erstes Argument, `Op2` als zweites und `Op3` als drittes aufzurufen:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

Die Typspezifikation ist erforderlich `Op3` , da und `Op1` unterschiedliche Typen aufweisen, sodass der Compiler dies ohne Angabe der Spezifikation als mehrdeutig behandelt.


## <a name="operator-precedence"></a>Operatorrangfolge

Alle binären Operatoren sind mit Ausnahme von rechts assoziativ `^` .

Eckige Klammern `[` und `]` , für das Aufteilen von Arrays und Indizierung, binden vor jedem Operator.

Die Funktoren `Adjoint` und die `Controlled` Bindung nach der Array Indizierung, aber vor allen anderen Operatoren.

Klammern für Vorgangs-und Funktionsaufrufe werden auch vor jedem Operator gebunden, aber nach der Array Indizierung und den Funktoren.

Operatoren in Rangfolge, vom höchsten zum niedrigsten:

Operator | Ständigkeit | Beschreibung | Operanden Typen
---------|----------|---------|---------------
 nachträ`!` | Unäroperatoren | Aufheben der Umschließung | Ein beliebiger benutzerdefinierter Typ
 `-`, `~~~`, `not` | Unäroperatoren | Numerische negative, bitweise Komplement logische Negation | `Int`, `BigInt` oder `Double` für `-` , `Int` `BigInt` `~~~` `Bool` für`not`
 `^` | Binary | Ganzzahlige Potenz | `Int`oder `BigInt` für die Basisklasse `Int` für den Exponenten
 `/`, `*`, `%` | Binary | Division, Multiplikation, ganzzahliger Modulo | `Int`, `BigInt` oder `Double` für `/` und `*` `Int` oder `BigInt` für`%`
 `+`, `-` | Binary | Addition oder Zeichenfolge und Array Verkettung, Subtraktion | `Int`, `BigInt` oder `Double` , zusätzlich `String` oder ein beliebiger Arraytyp für`+`
 `<<<`, `>>>` | Binary | Left Shift, Right Shift | `Int` oder `BigInt`
 `<`, `<=`, `>`, `>=` | Binary | Kleiner-als-, kleiner-als-oder-gleich-, größer-als-, größer-als-oder-gleich-Vergleiche | `Int`, `BigInt` oder`Double`
 `==`, `!=` | Binary | gleich, nicht gleichmäßige Vergleiche | beliebiger primitiver Typ
 `&&&` | Binary | Bitweises AND | `Int` oder `BigInt`
 `^^^` | Binary | Bitweises XOR | `Int` oder `BigInt`
 <code>\|\|\|</code> | Binary | Bitweises OR | `Int` oder `BigInt`
 `and` | Binary | Logisches AND | `Bool`
 `or` | Binary | Logisches OR | `Bool`
 `..` | Binär/Ternär | Bereichs Operator | `Int`
 `?` `|` | TERNÄRE | Bedingt | `Bool`für die linke Seite
`w/` `<-` | TERNÄRE | Kopieren und aktualisieren | Weitere Informationen finden Sie unter [Copy-and-Update-Ausdrücke](#copy-and-update-expressions)

## <a name="next-steps"></a>Nächste Schritte

Nun, da Sie mit Ausdrücken in q # arbeiten können, können Sie sich mit den [Vorgängen und Funktionen in q #](xref:microsoft.quantum.guide.operationsfunctions) vertraut machen, um zu erfahren, wie Sie Vorgänge und Funktionen definieren und aufzurufen.
