---
title: Ausdrücke in Q#
description: Erfahren Sie, wie Konstanten, Variablen, Operatoren, Vorgänge und Funktionen als Ausdrücke in angegeben, referenziert und kombiniert werden Q# .
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- Q#
- $$v
ms.openlocfilehash: e95a7cb9b74136ef9a6f51b4bbc32d1d93c43a0d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691606"
---
# <a name="expressions-in-no-locq"></a>Ausdrücke in Q#

## <a name="numeric-expressions"></a>Numerische Ausdrücke

Numerische Ausdrücke sind Ausdrücke vom Typ `Int` , `BigInt` oder `Double` .
Das heißt, Sie sind entweder ganzzahlige oder Gleit Komma Zahlen.

`Int` Literale in Q# werden als Sequenz von Ziffern geschrieben.
Hexadezimale und binäre ganzzahlige Werte werden unterstützt `0x` `0b` bzw. mit dem Präfix und geschrieben.

`BigInt` Literale in Q# verfügen über ein nach gestelltes- `l` oder- `L` Suffix.
Hexadezimale Big Integerwerte werden unterstützt und mit einem Präfix "0x" geschrieben.
Daher sind die folgenden alle gültigen Verwendungsmöglichkeiten von `BigInt` Literalen:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double` Literale in Q# sind Gleit Komma Zahlen, die mithilfe von Dezimalziffern geschrieben werden.
Sie können mit oder ohne Dezimaltrennzeichen, oder mit einem `.` exponentiellen Teil geschrieben werden, der mit "e" oder "e" angegeben wird (nach dem nur ein mögliches negatives Vorzeichen und Dezimalziffern gültig sind).
Die folgenden `Double` Literale sind gültig: `0.0` , `1.2e5` , `1e-5` .

Wenn ein Array Ausdruck eines beliebigen Elementtyps vorhanden ist, können Sie `Int` mithilfe der integrierten Funktion einen Ausdruck bilden [`Length`](xref:Microsoft.Quantum.Core.Length) , wobei der Array Ausdruck in Klammern eingeschlossen ist.
Wenn z. b `a` . an ein Array gebunden ist, dann `Length(a)` ist ein ganzzahliger Ausdruck.
Wenn `b` ein Array von Arrays ganzer Zahlen ist, `Int[][]` dann `Length(b)` ist die Anzahl der Unterarrays in `b` , und `Length(b[1])` die Anzahl von ganzen Zahlen im zweiten Unterarray in `b` .

Bei zwei numerischen Ausdrücken desselben Typs können die binären Operatoren, `+` , `-` `*` und `/` verwendet werden, um einen neuen numerischen Ausdruck zu bilden.
Der Typ des neuen Ausdrucks ist mit den Typen der einzelnen Ausdrücke identisch.

Verwenden Sie bei zwei ganzzahligen Ausdrücken den binären Operator `^` (Power), um einen neuen ganzzahligen Ausdruck zu bilden.
Auf ähnliche Weise können Sie auch `^` mit zwei doppelten Ausdrücken verwenden, um einen neuen doppelten Ausdruck zu bilden.
Schließlich können Sie `^` mit einer großen Ganzzahl auf der linken Seite und einer Ganzzahl auf der rechten Seite verwenden, um einen neuen großen ganzzahligen Ausdruck zu bilden.
In diesem Fall muss der zweite Parameter in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.

Bei zwei ganzzahligen oder großen ganzzahligen Ausdrücken bilden Sie mithilfe der `%` Operatoren (Modulus), `&&&` (Bitweises and), `|||` (bitweiser or) oder `^^^` (Bitweiser XOR) einen neuen Integer-oder Big Integer-Ausdruck.

Verwenden Sie auf der linken Seite entweder einen ganzzahligen Ausdruck oder einen großen ganzzahligen Ausdruck und einen ganzzahligen Ausdruck auf der rechten Seite, `<<<` `>>>` um einen neuen Ausdruck mit dem gleichen Typ wie den linken Ausdruck zu erstellen.

Der zweite Parameter (die UMSCHALT Menge) in einen Verschiebungs Vorgang muss größer oder gleich 0 (null) sein. das Verhalten für negative Verschiebungs Beträge ist nicht definiert.
Der Verschiebungs Betrag für einen der Verschiebungs Vorgänge muss ebenfalls in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.
Wenn die verschobene Zahl eine ganze Zahl ist, wird der Verschiebungs Betrag interpretiert, d `mod 64` . h. eine Verschiebung von 1 und eine UMSCHALT 65 haben dieselbe Wirkung.

Bei ganzzahligen und großen ganzzahligen Werten sind Verschiebungen arithmetisch.
Wenn Sie einen negativen Wert entweder nach links oder nach rechts verschieben, ergibt dies eine negative Zahl.
Das heißt, dass ein Schritt nach links oder rechts verschoben wird, entspricht dem multiplizieren bzw. aufteilen durch 2.

Die ganzzahlige Division und der ganzzahlige Modulo folgen dem Verhalten für negative Zahlen wie c#. Das heißt, dass `a % b` immer das gleiche Vorzeichen wie hat `a` und `b * (a / b) + a % b` immer gleich ist `a` . Beispiel:

|`A` | `B` | `A / B` | `A % B`|
|:---------:|:----------:|:---------:|:---------:|
| 5 | 2 | 2 | 1 |
| 5 | -2 | -2 | 1 |
| -5 | 2 | -2 | -1 |
| -5 | -2 | 2 | -1 |

Die Division von großen ganzzahligen und Modulo funktioniert auf dieselbe Weise.

Wenn ein beliebiger numerischer Ausdruck vorhanden ist, können Sie mit dem unären Operator einen neuen Ausdruck bilden `-` .
Der neue Ausdruck ist derselbe Typ wie der konstituierende Ausdruck.

Wenn Sie einen ganzzahligen Ausdruck oder einen großen ganzzahligen Ausdruck verwenden, können Sie einen neuen Ausdruck desselben Typs mit dem `~~~` unären Operator (bitweiser Komplement) bilden.

## <a name="boolean-expressions"></a>Boolesche Ausdrücke

Die beiden `Bool` Literalwerte sind `true` und `false` .

Wenn zwei Ausdrücke desselben primitiven Typs vorhanden sind, können die `==` `!=` binären Operatoren und verwendet werden, um einen-Ausdruck zu erstellen `Bool` .
Der Ausdruck ist true, wenn die beiden Ausdrücke gleich sind, andernfalls false.

Werte von benutzerdefinierten Typen können nicht verglichen werden, sondern es können nur Ihre nicht umschließenden Werte verglichen werden. Verwenden Sie z. b. den Operator "Unwrap" `!` (ausführlich unter [Typen in Q# ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)erläutert).

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Der Gleichheits Vergleich für `Qubit` Werte ist die Identitäts Gleichheit, d. h., ob die beiden Ausdrücke dasselbe Qubit identifizieren.
Die Zustände der beiden Qubits werden von diesem Vergleich nicht verglichen, auf Sie zugegriffen, gemessen oder geändert.

Der Gleichheits Vergleich für `Double` Werte kann aufgrund von Rundungs Effekten irreführend sein.
Beispiel: `49.0 * (1.0/49.0) != 1.0`.

Bei zwei numerischen Ausdrücken können die binären Operatoren,, `>` `<` `>=` und `<=` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der erste Ausdruck größer als, kleiner als, größer als oder gleich oder kleiner oder gleich dem zweiten Ausdruck ist.

Verwenden Sie bei zwei booleschen Ausdrücken den `and` binären-Operator, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn beide Ausdrücke True sind. Ebenso erstellt die Verwendung des- `or` Operators einen Ausdruck, der true ist, wenn einer der beiden Ausdrücke True ist.

Bei jedem booleschen Ausdruck kann der `not` unäre Operator verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der konstituierende Ausdruck false ist.

## <a name="string-expressions"></a>Zeichenfolgenausdrücke

Q# ermöglicht die Verwendung von Zeichen folgen in der `fail` Anweisung (in der [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow#fail-statement)erläutert) und in der [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) Standardfunktion. Das spezifische Verhalten der letzteren hängt vom verwendeten Simulator ab, schreibt jedoch in der Regel eine Meldung in die Host Konsole, wenn Sie während eines Programms aufgerufen wird Q# .

Zeichen folgen in Q# sind entweder Literale oder interpoliert Zeichen folgen.

Zeichenfolgenliterale ähneln in den meisten Sprachen einfachen Zeichenfolgenliteralen: eine Sequenz von Unicode-Zeichen, die in doppelten Anführungszeichen eingeschlossen sind `" "` .
Verwenden Sie innerhalb einer Zeichenfolge den umgekehrten Schrägstrich, `\` um ein doppeltes Anführungszeichen () mit Escapezeichen `\"` zu versehen, oder um eine neue Zeile ( `\n` ), ein Wagen Rücklauf Zeichen ( `\r` ) oder eine Registerkarte ( `\t` ) einzufügen.
Beispiel:

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a>Interpolierte Zeichenfolgen

Die Q# Syntax für Zeichen folgen Interpolationen ist eine Teilmenge der c#-Syntax. Im folgenden finden Sie die wichtigsten Punkte, die Sie betreffen Q# :

* Wenn Sie ein Zeichenfolgenliteral als interpolierte Zeichenfolge ermitteln möchten, stellen Sie ihm ein `$`-Symbol voran. Zwischen dem `$` und dem `"` , das einen zeichenfolgenliteralvorgang startet, darf kein Leerraum vorhanden sein.

* Im folgenden finden Sie ein einfaches Beispiel, in dem die-Funktion verwendet wird [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) , um das Ergebnis einer Maßeinheit zusammen mit anderen Ausdrücken in die Konsole zu schreiben Q# .

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* Jeder gültige Q# Ausdruck wird möglicherweise in einer interinterierten Zeichenfolge angezeigt.

* Ausdrücke in einer interinterierten Zeichenfolge Folgen der Q# Syntax, nicht der c#-Syntax. Der wichtigste Unterschied besteht darin, dass Q# keine ausführlichen (mehrzeiligen) interpoliert-Zeichen folgen unterstützt.

Weitere Informationen zur c#-Syntax finden Sie unter [*interpoliert*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).

## <a name="range-expressions"></a>Bereichs Ausdrücke

Bei den drei `Int` Ausdrücken `start` , `step` und `stop` ist der Ausdruck `start .. step .. stop` ein Bereichs Ausdruck, dessen erstes Element `start` , zweites Element `start+step` , drittes Element `start+step+step` , usw. ist, bis Sie übergeben werden `stop` .
Ein Bereich kann leer sein, wenn z. b `step` . positiv und ist `stop < start` .

Der Bereich ist an beiden Enden inklusiv. Das heißt, wenn der Unterschied zwischen `start` und `stop` ein ganzzahliges Vielfache von ist `step` , ist das letzte Element des Bereichs `stop` .

`Int`Bei zwei Ausdrücken `start` und `stop` ist der Ausdruck `start .. stop` ein Bereichs Ausdruck, der gleich ist `start .. 1 .. stop` .
Beachten Sie, dass der implizierte Wert `step` + 1 ist, auch wenn `stop` kleiner als ist `start` . in einem solchen Fall ist der Bereich leer.

Einige Beispiel Bereiche sind:

- `1..3` der Bereich von 1, 2, 3.
- `2..2..5` ist der Bereich von 2, 4.
- `2..2..6` ist der Bereich von 2, 4, 6.
- `6..-2..2` der Bereich ist 6, 4, 2.
- `2..1` der leere Bereich.
- `2..6..7` der Bereich 2.
- `2..2..1` der leere Bereich.
- `1..-1..2` der leere Bereich.

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

Ein tupelliteralelement ist eine Sequenz von Element Ausdrücken des entsprechenden Typs, die durch Kommas getrennt sind und in Klammern eingeschlossen sind.
Beispielsweise `(1, One)` ist ein `(Int, Result)` Ausdruck.

Abgesehen von Literalen sind die einzigen Tupelausdrücke Symbole, die an Tupelwerte, Array Elemente von tupelarrays und Aufruf Bare Aufrufe gebunden sind, die Tupel zurückgeben.

## <a name="user-defined-type-expressions"></a>User-Defined typausdrücke

Ein Literalwert eines benutzerdefinierten Typs besteht aus dem Typnamen, gefolgt von einem tupelliteraltyp mit dem basistupeltyp des Typs.
Wenn z. b. `IntPair` ein benutzerdefinierter Typ ist `(Int, Int)` , der auf basiert, dann `IntPair(2, 3)` ist ein gültiges Literale dieses Typs.

Anders als Literale sind die einzigen Ausdrücke eines benutzerdefinierten Typs Symbole, die an Werte dieses Typs gebunden sind, Array Elemente von Arrays dieses Typs und Aufruf Bare Aufrufe, die diesen Typ zurückgeben.

## <a name="unwrap-expressions"></a>Entpacken von Ausdrücken

In Q# handelt es sich bei dem Unwrap-Operator um ein nach gestelltes Ausrufezeichen `!` .
Wenn z. b `IntPair` . ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ `(Int, Int)` und `s` eine Variable mit Wert ist `IntPair(2, 3)` , dann `s!` ist `(2, 3)` .

Bei benutzerdefinierten Typen, die in Bezug auf andere benutzerdefinierte Typen definiert sind, können Sie den Unwrap-Operator wiederholen. `s!!`Gibt z. b. den doppelt entpackten Wert von an `s` .
Wenn `WrappedPair` ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ ist `IntPair` und `t` eine Variable mit dem Wert ist, `WrappedPair(IntPair(1,2))` dann `t!!` ist `(1,2)` .

Der `!` Operator hat eine höhere Rangfolge als alle anderen Operatoren, außer `[]` für die Array Indizierung und die Slicing.
`!` und `[]` binden Sie Positions bedingt, `a[i]![3]` d. h., wird gelesen als `((a[i])!)[3]` : nehmen Sie das `i` th-Element von `a` , entpacken Sie es, und holen Sie dann das dritte Element des entpackten Werts (der ein Array sein muss).

Die Rangfolge des `!` Operators hat eine Beeinträchtigung, die möglicherweise nicht offensichtlich ist.
Wenn eine Funktion oder ein Vorgang einen Wert zurückgibt, der dann entpackt wird, muss der Funktions-oder Vorgangs Ausdruck in Klammern eingeschlossen werden, damit das Argument Tupel an den-Ausdruck gebunden wird, anstatt an den Unwrap-Vorgang.
Beispiel:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Array Ausdrücke

Ein Arrayliteral ist eine Sequenz von einem oder mehreren Element Ausdrücken, die durch Kommas getrennt sind und in eckige Klammern eingeschlossen sind `[]` .
Alle-Elemente müssen mit demselben Typ kompatibel sein.

Verwenden Sie bei zwei Arrays desselben Typs den binären Operator, `+` um ein neues Array zu bilden, das die Verkettung der beiden Arrays ist.
Beispiel: `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`

### <a name="array-creation"></a>Array Erstellung

Verwenden Sie bei Angabe eines Typs und eines `Int` Ausdrucks den- `new` Operator, um ein neues Array mit der angegebenen Größe zuzuweisen.
`new Int[i + 1]`Weist z. b. ein neues `Int` Array mit- `i + 1` Elementen zu.

Leere Array Literale, wie z `[]` . b., sind nicht zulässig.
Stattdessen können Sie ein Array der Länge 0 (null) erstellen, indem Sie verwenden `new T[0]` , wobei `T` ein Platzhalter für einen geeigneten Typ ist.

Die Elemente eines neuen Arrays initialisieren einen typabhängigen Standardwert.
In den meisten Fällen ist dies eine Variation von 0 (null).

Bei Qubits und callables, bei denen es sich um Verweise auf Entitäten handelt, gibt es keinen angemessenen Standardwert.
Daher ist für diese Typen der Standardwert ein ungültiger Verweis, den Sie nicht ohne einen Laufzeitfehler verwenden können, ähnlich wie bei einem NULL-Verweis in Sprachen wie c# oder Java.
Arrays, die Qubits oder callables enthalten, müssen mit nicht standardmäßigen Werten initialisiert werden, bevor Sie Ihre Elemente sicher verwenden können. Geeignete Initialisierungs Routinen finden Sie unter <xref:Microsoft.Quantum.Arrays> .

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
 `Range` | Der leere Bereich, `1..1..0`
 `Callable` | _Ungültige Aufruf Bare_
 `Array['T]` | `'T[0]`

Tupeltypen initialisieren Element für Element.


### <a name="array-elements"></a>Array Elemente

Wenn ein Array Ausdruck und ein `Int` Ausdruck angegeben sind, erstellen Sie einen neuen Ausdruck mit dem Array Element-Operator `[]` .
Der neue Ausdruck ist derselbe Typ wie der Elementtyp des Arrays.
Wenn z. b. `a` an ein Array vom Typ gebunden ist `Double` , dann `a[4]` ist ein- `Double` Ausdruck.

Wenn es sich bei dem Array Ausdruck nicht um einen einfachen Bezeichner handelt, müssen Sie ihn in Klammern einschließen, um ein Element auszuwählen.
Wenn z. b. `a` und `b` beide Arrays vom Typ sind `Int` , wird ein Element aus der Verkettung folgendermaßen ausgedrückt:

```qsharp
(a + b)[13]
```

Alle Arrays in Q# sind NULL basiert.
Das heißt, das erste Element eines Arrays `a` ist immer `a[0]` .


### <a name="array-slices"></a>Array Slices

Wenn ein Array Ausdruck und ein `Range` Ausdruck angegeben sind, erstellen Sie einen neuen Ausdruck mithilfe des Array Slice-Operators `[ ]` .
Der neue Ausdruck hat denselben Typ wie das Array und enthält die Array Elemente, die von den Elementen des-Elements indiziert `Range` werden, in der Reihenfolge, die von definiert wird `Range` .
Wenn z. b. `a` an ein Array vom Typ gebunden ist `Double` , dann `a[3..-1..0]` ist ein-Ausdruck, `Double[]` der die ersten vier Elemente von enthält, `a` jedoch in umgekehrter Reihenfolge, wie Sie in angezeigt werden `a` .

Wenn das `Range` leer ist, ist das resultierende Array in der Länge 0 (null).

Ebenso wie beim Verweisen auf Array Elemente müssen Sie, wenn der Array Ausdruck kein einfacher Bezeichner ist, ihn in Klammern einschließen, um ihn in Slices aufzuteilen.
Wenn z. b. `a` und `b` beide Arrays vom Typ sind `Int` , wird ein Slice aus der Verkettung folgendermaßen ausgedrückt:

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a>Abherleitet anfangs-/Endwerte

Ab unserer [Version 0,8](xref:microsoft.quantum.relnotes)unterstützen wir Kontext Ausdrücke für die Bereichs Aufteilung. Vor allem können Sie Bereichs Start-und Endwerte im Kontext eines Bereichs aufteilen-Ausdrucks weglassen. In diesem Fall wendet der Compiler die folgenden Regeln an, um die vorgesehenen Trennzeichen für den Bereich abzuleiten:

* Wenn der Bereichs *Start* Wert weggelassen wird, wird der abherleitet Startwert
  * ist 0 (null), wenn kein Schritt angegeben oder der angegebene Schritt positiv ist.  
  * die Länge des aufgeschnittenen Arrays minus 1, wenn der angegebene Schritt negativ ist.

* Wenn der Wert für den Bereichs *Endpunkt* weggelassen wird, wird der abherende Endwert
  * die Länge des aufgeschnittenen Arrays minus 1, wenn kein Schritt angegeben oder der angegebene Schritt positiv ist.
  * ist 0 (null), wenn der angegebene Schritt negativ ist.

Beispiele:

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

Da es Q# sich bei allen Typen um Werttypen handelt (wobei die Qubits eine etwas besondere Rolle einnehmen), wird formal eine "Copy"-Kopie erstellt, wenn ein Wert an ein Symbol gebunden ist oder wenn ein Symbol erneut hergestellt wird. Dies heißt, dass das Verhalten von Q# mit dem identisch ist, wenn eine Kopie mithilfe eines Zuweisungs Operators erstellt wurde. 

Natürlich werden in der Praxis nur die relevanten Teile nach Bedarf neu erstellt. Dies wirkt sich darauf aus, wie Arrays kopiert werden, da Array Elemente nicht aktualisiert werden können. Zum Ändern eines vorhandenen Arrays muss ein *Kopier-und Aktualisierungs* Mechanismus genutzt werden.

Sie können ein neues Array aus einem vorhandenen Array mithilfe von *Copy-und Update-* Ausdrücken erstellen, die die Operatoren `w/` und verwenden `<-` .
Ein Copy-and-Update-Ausdruck ist ein Ausdruck der Form `expression1 w/ expression2 <- expression3` , wobei

* `expression1` muss `T[]` für einen Typ vom Typ sein `T` .
* `expression2` definiert, welche Indizes in dem in angegebenen Array `expression1` geändert werden. `expression2` muss entweder vom Typ `Int` oder vom Typ sein `Range` .
* `expression3` der Wert (n), der zum Aktualisieren von Elementen in verwendet wird `expression1` , basierend auf den in angegebenen Indizes `expression2` . Wenn `expression2` vom Typ ist `Int` , `expression3` muss vom Typ sein `T` . Wenn `expression2` vom Typ ist `Range` , `expression3` muss vom Typ sein `T[]` .

Beispielsweise erstellt der Copy-and-Update-Ausdruck `arr w/ idx <- value` ein neues Array mit allen Elementen, die auf die entsprechenden Elemente in festgelegt sind `arr` , mit Ausnahme der durch angegebenen Elemente `idx` , die auf den Wert (e) in festgelegt ist `value` . 

`arr`Das angegebene enthält das Array. `[0,1,2,3]` 

- `arr w/ 0 <- 10` ist das Array `[10,1,2,3]` .
- `arr w/ 2 <- 10` ist das Array `[0,1,10,3]` .
- `arr w/ 0..2..3 <- [10,12]` ist das Array `[10,1,12,3]` .

#### <a name="copy-and-update-expressions-for-named-items"></a>Copy-und Update-Ausdrücke für benannte Elemente

Ähnliche Ausdrücke sind für benannte Elemente in benutzerdefinierten Typen vorhanden. 

Nehmen Sie z. b. den Typ. 

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

Sie können auch ein Array von callables erstellen.

* Wenn der allgemeine Elementtyp ein Vorgang oder Funktionstyp ist, müssen alle Elemente die gleichen Eingabe-und Ausgabetypen aufweisen.
* Der Elementtyp des Arrays unterstützt alle [Funktoren](xref:microsoft.quantum.guide.operationsfunctions) , die von allen Elementen unterstützt werden.
Wenn z. b. `Op1` , `Op2` und `Op3` alle Vorgänge sind, unterstützt, unterstützt und unterstützt jedoch `Qubit[] => Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` beide:
  * `[Op1, Op2]` ist ein Array von `(Qubit[] => Unit)` Vorgängen.
  * `[Op1, Op3]` ist ein Array von `(Qubit[] => Unit is Adj)` Vorgängen.
  * `[Op2, Op3]` ist ein Array von `(Qubit[] => Unit is Ctl)` Vorgängen.

Während die Vorgänge `(Qubit[] => Unit is Adj)` und  `(Qubit[] => Unit is Ctl)` den gemeinsamen Basistyp aufweisen `(Qubit[] => Unit)` , verwenden *Arrays* dieser Vorgänge jedoch keinen gemeinsamen Basistyp.

Beispielsweise gibt `[[Op1], [Op2]]` derzeit einen Fehler aus, da versucht wird, ein Array der beiden inkompatiblen Array Typen und zu erstellen `(Qubit[] => Unit is Adj)[]` `(Qubit[] => Unit is Ctl)[]` .

Weitere Informationen zu callables finden Sie unter [Aufruf Bare Ausdrücke](#callable-expressions) auf dieser Seite bzw. [in den Vorgängen und Funktionen in Q# ](xref:microsoft.quantum.guide.operationsfunctions).

## <a name="conditional-expressions"></a>Bedingte Ausdrücke

Wenn zwei Ausdrücke desselben Typs und ein boolescher Ausdruck verwendet werden, bilden Sie einen Bedingungs Ausdruck mithilfe des Fragezeichens, `?` und des vertikalen Balkens `|` . Gibt `a==b ? c | d` an, dass der Wert des bedingten Ausdrucks ist, wenn den Wert `c` `a==b` true hat und wenn der Wert `d` false ist.

### <a name="conditional-expressions-with-callables"></a>Bedingte Ausdrücke mit callables

Bedingte Ausdrücke können zu Vorgängen ausgewertet werden, die über die gleichen Eingaben und Ausgaben verfügen, aber unterschiedliche Funktions tüktoren unterstützen. In diesem Fall ist der Typ des bedingten Ausdrucks ein Vorgang mit Eingaben und Ausgaben, die alle von beiden Ausdrücken unterstützten Funktoren unterstützen.
Wenn z. b. `Op1` , `Op2` und `Op3` alle sind, unterstützt, unterstützt und unterstützt jedoch `Qubit[]=>Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` beide:

- `flag ? Op1 | Op2` ist ein- `(Qubit[] => Unit)` Vorgang.
- `flag ? Op1 | Op3` ist ein- `(Qubit[] => Unit is Adj)` Vorgang.
- `flag ? Op2 | Op3` ist ein- `(Qubit[] => Unit is Ctl)` Vorgang.

Wenn einer der beiden möglichen Ergebnis Ausdrücke einen Funktions-oder einen Vorgangs aufzurufen enthält, findet dieser Vorgang nur statt, wenn das Ergebnis das Ergebnis ist, das der Wert des Aufrufes ist. Wenn z. b. `a==b ? C(qs) | D(qs)` `a==b` true ist, wird der `C` Vorgang aufgerufen, und wenn false ist, wird nur der `D` Vorgang aufgerufen. Diese Vorgehensweise ähnelt der *Kurzschluss* in anderen Sprachen.

## <a name="callable-expressions"></a>Aufruf Bare Ausdrücke

Ein Aufruf bares Literalelement ist der Name eines Vorgangs oder einer Funktion, der im Kompilierungs Bereich definiert ist. Beispielsweise ist ein vorgangsliteral, `X` das auf den `X` -Standard Bibliotheks Vorgang verweist, und `Message` ist ein Funktionsliteral, das auf die Standard Bibliotheks `Message` Funktion verweist.

Wenn ein Vorgang das `Adjoint` Funktor unterstützt, `Adjoint op` ist ein Vorgangs Ausdruck.
Entsprechend `Controlled` `Controlled op` ist ein Vorgangs Ausdruck, wenn der Vorgang das Funktor unterstützt.
Weitere Informationen zu den Typen dieser Ausdrücke finden Sie unter [Aufrufen von Vorgangs Spezialisierungs](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)Vorgängen.

Funktoren ( `Adjoint` und `Controlled` ) werden genauer gebunden als alle anderen Operatoren, mit Ausnahme des Unwrap `!` -Operators und der Array Indizierung mit `[ ]` .
Daher sind die folgenden Elemente gültig, vorausgesetzt, dass die-Vorgänge die verwendeten Funktoren unterstützen:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a>Typparametrisierte Aufruf Bare Ausdrücke

Sie können ein Aufruf bares Literalzeichen als Wert verwenden, um es z. b. einer Variablen zuzuweisen oder es an eine andere Aufruf Bare zu übergeben. Wenn die Aufruf Bare [Typparameter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)enthält, müssen Sie in diesem Fall die Parameter als Teil des Aufruf baren Werts angeben.

Ein Aufruf barer Wert darf keine nicht angegebenen Typparameter aufweisen. Wenn z. b. `Fun` eine Funktion mit der Signatur ist `'T1->Unit` :

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aufruf Bare Aufruf Ausdrücke

Wenn ein Aufruf barer Ausdruck (Vorgang oder Funktion) und ein Tupelausdruck des Eingabetyps der Aufruf baren Signatur angegeben werden, können Sie einen *Aufruf Ausdruck* bilden, indem Sie den Tupelausdruck an den Aufruf baren Ausdruck anhängen.
Der Typ des Aufruf Ausdrucks ist der Ausgabetyp der Signatur des Callable-Ausdrucks.

Wenn z. b `Op` . ein Vorgang mit der Signatur ist `((Int, Qubit) => Double)` , `Op(3, qubit1)` ist ein Ausdruck vom Typ `Double` .
Ebenso ist, wenn `Sin` eine Funktion mit der Signatur ist `(Double -> Double)` , `Sin(0.1)` ein Ausdruck vom Typ `Double` .
Wenn schließlich `Builder` eine Funktion mit der Signatur ist `(Int -> (Int -> Int))` , dann `Builder(3)` ist eine Funktion von `Int` zu `Int` .

Zum Aufrufen des Ergebnisses eines Aufruf baren Ausdrucks ist ein zusätzliches Paar von Klammern um den Aufruf baren Ausdruck erforderlich.
Um also das Ergebnis des Aufrufs `Builder` aus dem vorherigen Absatz aufzurufen, ist die korrekte Syntax:

```qsharp
(Builder(3))(2)
```

Wenn Sie einen [vom Typ parametrisierten](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) Aufruf baren aufrufen, können Sie die tatsächlichen Typparameter innerhalb von spitzen Klammern `< >` nach dem Aufruf baren Ausdruck angeben.
Diese Aktion ist in der Regel unnötig, da der Q# Compiler die eigentlichen Typen leitet.
Es *ist* jedoch für die [partielle Anwendung](xref:microsoft.quantum.guide.operationsfunctions#partial-application) erforderlich, wenn ein typparametrisiertes Argument nicht angegeben wird.
Dies ist auch nützlich, wenn die Übergabe von Vorgängen mit unterschiedlichen Funktoren unterstützt wird.

Wenn z. b. die Signatur hat und die Signatur und die Signatur aufweisen, muss `Func` `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` `Func` mit `Op1` als erstes Argument, `Op2` als zweites und `Op3` als drittes aufgerufen werden:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

Die Typspezifikation ist erforderlich `Op3` , da und `Op1` unterschiedliche Typen aufweisen, sodass der Compiler dies ohne Angabe der Spezifikation als mehrdeutig behandelt.


## <a name="operator-precedence"></a>Operatorrangfolge

* Alle binären Operatoren sind mit Ausnahme von rechts assoziativ `^` .

* Eckige Klammern (für das Aufteilen `[ ]` und Indizieren von Arrays) werden vor jedem Operator gebunden.

* Die Funktoren `Adjoint` und die `Controlled` Bindung nach der Array Indizierung, aber vor allen anderen Operatoren.

* Klammern für Vorgangs-und Funktionsaufrufe werden auch vor jedem Operator gebunden, aber nach der Array Indizierung und den Funktoren.

Q# Operatoren in Rangfolge, vom höchsten zum niedrigsten:

Betreiber | Ständigkeit | BESCHREIBUNG | Operanden Typen
---------|----------|---------|---------------
 nachträ `!` | Unär | Aufheben der Umschließung | Ein beliebiger benutzerdefinierter Typ
 `-`, `~~~`, `not` | Unär | Numerische negative, bitweise Komplement logische Negation | `Int`, `BigInt` oder `Double` für `-` , `Int` `BigInt` `~~~` `Bool` für `not`
 `^` | Binary | Ganzzahlige Potenz | `Int` oder `BigInt` für die Basisklasse `Int` für den Exponenten
 `/`, `*`, `%` | Binary | Division, Multiplikation, ganzzahliger Modulo | `Int`, `BigInt` oder `Double` für `/` und `*` `Int` oder `BigInt` für `%`
 `+`, `-` | Binary | Addition oder Zeichenfolge und Array Verkettung, Subtraktion | `Int`, `BigInt` oder `Double` , zusätzlich `String` oder ein beliebiger Arraytyp für `+`
 `<<<`, `>>>` | Binary | Left Shift, Right Shift | `Int` oder `BigInt`
 `<`, `<=`, `>`, `>=` | Binary | Kleiner-als-, kleiner-als-oder-gleich-, größer-als-, größer-als-oder-gleich-Vergleiche | `Int`, `BigInt` oder `Double`
 `==`, `!=` | Binary | gleich, nicht gleichmäßige Vergleiche | beliebiger primitiver Typ
 `&&&` | Binary | Bitweises AND | `Int` oder `BigInt`
 `^^^` | Binary | Bitweises XOR | `Int` oder `BigInt`
 <code>\|\|\|</code> | Binary | Bitweises OR | `Int` oder `BigInt`
 `and` | Binary | Logisches AND | `Bool`
 `or` | Binary | Logisches OR | `Bool`
 `..` | Binär/Ternär | Bereichs Operator | `Int`
 `?` `|` | TERNÄRE | Bedingt | `Bool` für die linke Seite
`w/` `<-` | TERNÄRE | Kopieren und aktualisieren | Weitere Informationen finden Sie unter [Copy-and-Update-Ausdrücke](#copy-and-update-expressions)

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie nun mit Ausdrücken in arbeiten können Q# , fahren Sie mit den [Vorgängen und Q# Funktionen in](xref:microsoft.quantum.guide.operationsfunctions) fort, um zu erfahren, wie Sie Vorgänge und Funktionen definieren und aufzurufen.
