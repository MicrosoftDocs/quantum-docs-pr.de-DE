---
title: 'Q#-Ausdrücke'
description: 'Erfahren Sie, wie Konstanten, Variablen, Operatoren, Vorgänge und Funktionen als Ausdrücke in Q# angegeben, referenziert und kombiniert werden.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: fbde873f220d737db17f889d00be33541e3eb59b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907408"
---
# <a name="expressions"></a>Ausdrücke

## <a name="grouping"></a>Gruppierung

Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.
`(7)` ist beispielsweise ein `Int` Ausdruck. `([1,2,3])` ist ein Ausdruck vom Typ Array von `Int`s, und `((1,2))` ist ein Ausdruck vom Typ `(Int, Int)`.

Die Äquivalenz zwischen einfachen Werten und Tupeln mit einem einzelnen Element, die im [Typmodell](xref:microsoft.quantum.language.type-model#tuple-types) beschrieben werden, entfernt die Mehrdeutigkeit zwischen `(6)` als Gruppe und `(6)` als ein Tupel mit einem einzelnen Element.

## <a name="symbols"></a>Symbols

Der Name eines Symbols, das einem Wert des Typs `'T` gebunden oder zugewiesen ist, ist ein Ausdruck vom Typ `'T`.
Wenn beispielsweise das Symbol `count` an den ganzzahligen Wert `5`gebunden ist, ist `count` ein ganzzahliger Ausdruck.

## <a name="numeric-expressions"></a>Numerische Ausdrücke

Numerische Ausdrücke sind Ausdrücke vom Typ `Int`, `BigInt`oder `Double`.
Das heißt, Sie sind entweder ganzzahlige oder Gleit Komma Zahlen.

`Int` Literale in Q# sind mit ganzzahligen literalen C#in identisch, mit dem Unterschied, dass kein nach gestelltes "l" oder "l" erforderlich (oder zulässig) ist.
Hexadezimale und binäre ganze Zahlen werden mit dem Präfix "0x" bzw. "0B" unterstützt.

`BigInt` Literale in Q# sind identisch mit großen ganzzahligen Zeichen folgen in .net mit einem nachfolgenden "l" oder "l".
Hexadezimale große ganze Zahlen werden mit dem Präfix "0x" unterstützt.
Daher sind die folgenden alle gültigen Verwendungsmöglichkeiten von `BigInt` Literalen:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double` Literale in Q# sind mit doppelten Literalen in C#identisch, mit dem Unterschied, dass kein nach gestelltes "d" oder "d" erforderlich (oder zulässig) ist.

Wenn ein Array Ausdruck eines beliebigen Elementtyps vorhanden ist, kann ein `Int` Ausdruck mit der integrierten Funktion `Length` gebildet werden, wobei der Array Ausdruck in Klammern, `(` und `)`eingeschlossen ist.
Wenn `a` beispielsweise an ein Array gebunden ist, ist `Length(a)` ein ganzzahliger Ausdruck.
Wenn `b` ein Array von Arrays mit ganzen Zahlen ist, `Int[][]`, dann ist `Length(b)` die Anzahl der Unterarrays in `b`, und `Length(b[1])` ist die Anzahl von ganzen Zahlen im zweiten Unterarray in `b`.

Bei zwei numerischen Ausdrücken desselben Typs können die binären Operatoren `+`, `-`, `*`und `/` verwendet werden, um einen neuen numerischen Ausdruck zu bilden.
Der Typ des neuen Ausdrucks ist mit den Typen der einzelnen Ausdrücke identisch.

Bei zwei ganzzahligen Ausdrücken kann der binäre Operator `^` (Power) verwendet werden, um einen neuen ganzzahligen Ausdruck zu bilden.
Ebenso können `^` mit zwei doppelten Ausdrücken verwendet werden, um einen neuen doppelten Ausdruck zu bilden.
Schließlich können `^` mit einer großen Ganzzahl auf der linken Seite und einer ganzen Zahl auf der rechten Seite verwendet werden, um einen neuen großen ganzzahligen Ausdruck zu bilden.
In diesem Fall muss der zweite Parameter in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.

Bei zwei ganzzahligen oder großen ganzzahligen Ausdrücken kann ein neuer Integer-Ausdruck oder ein großer ganzzahliger Ausdruck mithilfe des `%` (Modulus), `&&&` (bitweisen und), `|||` (bitweisen OR) oder `^^^` (bitweisen XOR)-Operatoren gebildet werden.

Wenn auf der linken Seite entweder ein ganzzahliger Ausdruck oder ein großer ganzzahliger Ausdruck und ein ganzzahliger Ausdruck auf der rechten Seite angegeben ist, können die `<<<`-Operatoren (arithmetischer Left Shift) oder `>>>` (arithmetische Rechte Shift) zum Erstellen eines neuen Ausdrucks mit demselben Typ wie der linke Ausdruck verwendet werden.

Der zweite Parameter (die UMSCHALT Menge) in einen Verschiebungs Vorgang muss größer oder gleich 0 (null) sein. das Verhalten für negative Verschiebungs Beträge ist nicht definiert.
Der Verschiebungs Betrag für einen der Verschiebungs Vorgänge muss ebenfalls in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.
Wenn die zu Verschiebe Zahl eine ganze Zahl ist, wird die UMSCHALT Menge `mod 64`; Das heißt, dass eine Verschiebung von 1 und eine Schicht von 65 denselben Effekt haben.

Bei ganzzahligen und großen ganzzahligen Werten sind Verschiebungen arithmetisch.
Wenn Sie einen negativen Wert entweder nach links oder rechts verschieben, ergibt dies eine negative Zahl.
Das heißt, die Verschiebung eines Schritts nach links oder rechts ist identisch mit der Multiplikation bzw. Division durch 2.

Die ganzzahlige Division und der ganzzahlige Modulo folgen dem C#Verhalten für negative Zahlen als.
Das heißt, `a % b` immer dasselbe Zeichen wie `a`haben, und `b * (a / b) + a % b` immer gleich `a`.
Beispiel:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

Große ganzzahlige Division und Modulo funktionieren auf dieselbe Weise.

Wenn ein beliebiger numerischer Ausdruck vorhanden ist, kann ein neuer Ausdruck mithilfe des `-` unären Operators gebildet werden.
Der neue Ausdruck hat denselben Typ wie der konstituierende Ausdruck.

Bei jedem Integer-Ausdruck oder einem Big Integer-Ausdruck kann ein neuer Ausdruck desselben Typs mithilfe des `~~~` (bitweisen Komplement) unären Operators gebildet werden.

## <a name="boolean-expressions"></a>Boolesche Ausdrücke

Die beiden `Bool` Literalwerte sind `true` und `false`.

Wenn zwei Ausdrücke desselben primitiven Typs vorhanden sind, können die `==` und `!=` binäre Operatoren verwendet werden, um einen `Bool` Ausdruck zu erstellen.
Der Ausdruck ist true, wenn die beiden Ausdrücke gleich sind, andernfalls false.

Werte von benutzerdefinierten Typen können nicht verglichen werden, sondern es können nur Ihre nicht umschließenden Werte verglichen werden. Verwenden Sie beispielsweise den "Unwrap"-Operator `!` (auf der [Seite "Q# Type Model](xref:microsoft.quantum.language.type-model#user-defined-types)" erläutert).

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Der Gleichheits Vergleich für `Qubit` Werte ist Identitäts Gleichheit. Das heißt, ob die beiden Ausdrücke dasselbe Qubit identifizieren.
Der Zustand der beiden Qubits wird von diesem Vergleich nicht verglichen, auf Sie zugegriffen, gemessen oder geändert.

Der Gleichheits Vergleich für `Double` Werte kann aufgrund von Rundungs Effekten irreführend sein.
Beispielsweise `49.0 * (1.0/49.0) != 1.0`.

Bei zwei numerischen Ausdrücken können die binären Operatoren `>`, `<`, `>=`und `<=` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der erste Ausdruck größer als, kleiner als, größer als oder gleich oder kleiner oder gleich dem zweiten Ausdruck ist.

Bei zwei booleschen Ausdrücken können die `and` und `or` binäre Operatoren verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn die beiden Ausdrücke "true" sind.

Bei jedem booleschen Ausdruck kann der `not` unäre Operator verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der konstituierende Ausdruck false ist.

## <a name="string-expressions"></a>Zeichen folgen Ausdrücke

Q# ermöglicht die Verwendung von Zeichen folgen in der `fail`-Anweisung und der `Log`-Standardfunktion.

Zeichen folgen in Q# sind entweder Literale oder interpoliert Zeichen folgen.
Zeichen folgen Literale ähneln in den meisten Sprachen einfachen Zeichenfolgenliteralen: eine Sequenz von Unicode-Zeichen, die in doppelten Anführungszeichen eingeschlossen sind, `"`.
Innerhalb einer Zeichenfolge kann der umgekehrte Schrägstrich `\` verwendet werden, um ein doppeltes Anführungszeichen zu versehen und eine neue Zeile als `\n`einzufügen, ein Wagen Rücklauf als `\r`und eine Registerkarte als `\t`.
Beispiel:

```qsharp
"\"Hello world!\", she said.\n"
```

Die Q#-Syntax für Zeichen folgen Interpolationen ist eine Teilmenge C# der 7,0-Syntax. Q# unterstützt keine ausführlichen (mehrzeiligen) interpoliert Zeichen folgen.
Informationen zur Syntax finden Sie unter C# [*interpoliert*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) .

Ausdrücke in einer interinterierten Zeichenfolge Folgen der Q#- C# Syntax, nicht der Syntax.
Jeder gültige Q#-Ausdruck kann in einer interinterierten Zeichenfolge angezeigt werden.

## <a name="qubit-expressions"></a>Qubit-Ausdrücke

Die einzigen `Qubit` Ausdrücke sind Symbole, die an `Qubit` Werte oder Array Elemente `Qubit` Arrays gebunden sind.
Es sind keine `Qubit` Literale vorhanden.

## <a name="pauli-expressions"></a>Pauli-Ausdrücke

Die vier `Pauli` Werte `PauliI`, `PauliX`, `PauliY`und `PauliZ`sind alle gültigen `Pauli` Ausdrücke.

Abgesehen davon sind die einzigen `Pauli` Ausdrücke Symbole, die an `Pauli` Werte oder Array Elemente `Pauli` Arrays gebunden sind.

## <a name="result-expressions"></a>Ergebnis Ausdrücke

Die beiden `Result` Werte `One` und `Zero`sind gültige `Result` Ausdrücke.

Abgesehen davon sind die einzigen `Result` Ausdrücke Symbole, die an `Result` Werte oder Array Elemente `Result` Arrays gebunden sind.
Beachten Sie insbesondere, dass `One` nicht mit der ganzzahligen `1`identisch ist, und es gibt keine direkte Konvertierung zwischen Ihnen.
Das gleiche gilt für `Zero` und `0`.

## <a name="range-expressions"></a>Bereichs Ausdrücke

Bei allen drei `Int` Ausdrücken `start`, `step`und `stop`ist `start .. step .. stop` ein Bereichs Ausdruck, dessen erstes Element `start`ist, das zweite Element `start+step`ist, das dritte Element `start+step+step`ist usw., bis `stop` übergeben wird.
Ein Bereich kann leer sein, wenn `step` beispielsweise positiv und `stop < start`ist.
Das letzte Element des Bereichs wird `stop`, wenn der Unterschied zwischen `start` und `stop` ein ganzzahliges Vielfaches von `step`ist. Das heißt, der Bereich ist an beiden Enden inklusiv.

Bei zwei `Int` Ausdrücken `start` und `stop`ist `start .. stop` ein Bereichs Ausdruck, der `start .. 1 .. stop`entspricht.
Beachten Sie, dass der implizierte `step` gleich + 1 ist, auch wenn `stop` kleiner als `start`ist. in einem solchen Fall ist der Bereich leer.

Einige Beispiel Bereiche sind:

- `1..3` ist der Bereich von 1, 2, 3.
- `2..2..5` ist der Bereich von 2, 4.
- `2..2..6` ist der Bereich von 2, 4, 6.
- `6..-2..2` ist der Bereich 6, 4, 2.
- `2..1` ist der leere Bereich.
- `2..6..7` ist der Bereich 2.
- `2..2..1` ist der leere Bereich.
- `1..-1..2` ist der leere Bereich.

## <a name="callable-expressions"></a>Aufruf Bare Ausdrücke

Ein Aufruf bares Literalelement ist der Name eines Vorgangs oder einer Funktion, der im Kompilierungs Bereich definiert ist.
Beispielsweise ist `X` ein vorgangsliteral, das auf den `X` Vorgang der Standardbibliothek verweist, und `Message` ist ein Funktionsliteral, das auf die `Message` Funktion der Standardbibliothek verweist.

Wenn ein Vorgang das `Adjoint`-Funktor unterstützt, ist `Adjoint op` ein Vorgangs Ausdruck.
Wenn der Vorgang das `Controlled`-Funktor unterstützt, ist `Controlled op` ein Vorgangs Ausdruck.
Die Typen dieser Ausdrücke werden in den [Funktoren](xref:microsoft.quantum.language.type-model#functors)angegeben.

Funktoren (`Adjoint` und `Controlled`) werden genauer gebunden als alle anderen Operatoren, mit Ausnahme des Unwrap-Operators `!` und der Array Indizierung mit `[]`.
Folglich sind die folgenden Vorgänge zulässig, vorausgesetzt, dass die Vorgänge die verwendeten Funktoren unterstützen:

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

Ein Aufruf bares Literale kann als Wert verwendet werden, z. b. um einer Variablen zuzuweisen oder um Sie an eine andere Aufruf Bare zu übergeben.
In diesem Fall müssen Sie, wenn die Aufruf Bare Typparameter aufweist, als Teil des Aufruf baren Werts angegeben werden.
Ein Aufruf barer Wert darf keine nicht angegebenen Typparameter aufweisen.

Wenn `Fun` beispielsweise eine Funktion mit Signatur `'T1->Unit`ist:

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aufruf Bare Aufruf Ausdrücke

Bei einem Aufruf baren Ausdruck (Operation oder Funktion) und einem Tupelausdruck des Eingabetyps der Aufruf baren Signatur kann ein Aufruf Ausdruck gebildet werden, indem der Tupelausdruck an den Aufruf baren Ausdruck angefügt wird.
Der Typ des Aufruf Ausdrucks ist der Ausgabetyp der Signatur des Callable-Ausdrucks.

Wenn `Op` z. b. ein Vorgang mit Signatur `((Int, Qubit) => Double)`ist, `Op(3, qubit1)` ein Ausdruck vom Typ `Double`ist.
Ebenso gilt, wenn `Sin` eine Funktion mit Signatur `(Double -> Double)`ist, `Sin(0.1)` ein Ausdruck vom Typ `Double`ist.
Wenn `Builder` eine Funktion mit Signatur `(Int -> (Int -> Int))`ist, dann ist `Builder(3)` eine Funktion von bis zu int.

Zum Aufrufen des Ergebnisses eines Aufruf baren Ausdrucks ist ein zusätzliches Paar von Klammern um den Aufruf baren Ausdruck erforderlich.
Um also das Ergebnis des Aufrufs von `Builder` aus dem vorherigen Absatz aufzurufen, lautet die korrekte Syntax:

```qsharp
(Builder(3))(2)
```

Beim Aufrufen einer typparametrisierten Aufruf baren kann der tatsächliche Typparameter in spitzen Klammern `<` und nach dem Aufruf baren Ausdruck `>` werden.
Dies ist in der Regel unnötig, da der Q#-Compiler die eigentlichen Typen ableiten wird.
Dies ist für die partielle Anwendung erforderlich (siehe unten), wenn ein typparametrisiertes Argument nicht angegeben wird.
Dies ist manchmal auch nützlich, wenn die Übergabe von Vorgängen mit unterschiedlichen Funktoren unterstützt wird.

Wenn `Func` beispielsweise über eine Signatur `('T1, 'T2, 'T1) -> 'T2`verfügt, `Op1` und `Op2` Signatur `(Qubit[] => Unit is Adj)`aufweisen und `Op3` über eine Signatur `(Qubit[] => Unit)`verfügt, um `Func` mit `Op1` als erstes Argument aufzurufen, `Op2` als zweites und `Op3` als drittes Argument:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

Die Typspezifikation ist erforderlich, da `Op3` und `Op1` unterschiedliche Typen aufweisen, sodass der Compiler dies ohne Angabe der Spezifikation als mehrdeutig behandelt.

### <a name="partial-application"></a>Partielle Anwendung

Bei einem Aufruf baren Ausdruck kann ein neuer Aufruf barer Ausdruck erstellt werden, indem eine Teilmenge der Argumente für die Aufruf Bare bereitgestellt wird.
Dies wird als _partielle Anwendung_bezeichnet.

In Q# wird eine teilweise angewendete Aufruf Bare-Datei durch Schreiben eines normalen Aufruf Ausdrucks ausgedrückt, wobei jedoch ein Unterstrich, `_`, für die nicht angegebenen Argumente verwendet wird.
Die sich ergebende Aufruf Bare hat denselben Ergebnistyp wie die basiscallable und die gleichen Spezialisierungs Vorgänge für Vorgänge.
Der Eingabetyp der partiellen Anwendung ist einfach der ursprüngliche Typ mit den angegebenen Argumenten.

Wenn beim Erstellen einer partiellen Anwendung eine änderbare Variable als angegebenes Argument angegeben wird, wird der aktuelle Wert der Variablen verwendet.
Wenn Sie den Wert der Variablen anschließend ändern, wirkt sich dies nicht auf die partielle Anwendung aus.

Wenn `Op` z. b. den Typ `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`hat:

- `Op(5,(_,_))` hat den Typ `(((Qubit,Qubit), Double) => Unit is Adj)`und `Op(5,_)`.
- `Op(_,(_,1.0))` hat den Typ `((Int, (Qubit,Qubit)) => Unit is Adj)`.
- `Op(_,((q1,q2),_))` hat den Typ `((Int,Double) => Unit is Adj)`.
   Beachten Sie, dass hier eine Singleton-tupeläquivalenz angewendet wurde.

Wenn das teilweise angewendete Aufruf Bare Typparameter aufweist, die vom Compiler nicht abgeleitet werden können, müssen Sie auf der Aufruf Site bereitgestellt werden.
Die partielle Anwendung darf keine nicht angegebenen Typparameter aufweisen.

Wenn `Op` z. b. den Typ `(('T1, Qubit, 'T1) => Unit : Adjoint)`hat:

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a>Rekursion

Q#-callables dürfen direkt oder indirekt rekursiv sein.
Das heißt, ein Vorgang oder eine Funktion kann sich selbst aufrufen, oder es kann eine andere Aufruf Bare aufgerufen werden, die den Aufruf baren Vorgang direkt oder indirekt aufruft.

Es gibt jedoch zwei wichtige Kommentare zur Verwendung der Rekursion:

- Die Verwendung von Rekursion bei Vorgängen beeinträchtigt wahrscheinlich bestimmte Optimierungen.
  Dies kann erhebliche Auswirkungen auf die Ausführungszeit des Algorithmus haben.
- Bei der Ausführung auf einem eigentlichen Quantum-Gerät kann der Stapel Speicher eingeschränkt sein, sodass die Tiefe Rekursion zu einem Laufzeitfehler führen kann.
  Insbesondere der Q#-Compiler und die Common Language Runtime erkennen und optimieren die Endrekursion nicht.

## <a name="tuple-expressions"></a>Tupelausdrücke

Ein tupelliteral ist eine Sequenz von Element Ausdrücken des entsprechenden Typs, die durch Kommas getrennt sind und in `(` und `)`eingeschlossen werden.
Beispielsweise ist `(1, One)` ein `(Int, Result)` Ausdruck.

Abgesehen von Literalen sind die einzigen Tupelausdrücke Symbole, die an Tupelwerte, Array Elemente von tupelarrays und Aufruf Bare Aufrufe gebunden sind, die Tupel zurückgeben.

## <a name="user-defined-type-expressions"></a>Benutzerdefinierte typausdrücke

Ein Literalwert eines benutzerdefinierten Typs besteht aus dem Typnamen, gefolgt von einem tupelliteraltyp mit dem basistupeltyp des Typs.
Wenn `IntPair` beispielsweise ein benutzerdefinierter Typ ist, der auf `(Int, Int)`basiert, wäre `IntPair(2,3)` ein gültiges Literale dieses Typs.

Anders als Literale sind die einzigen Ausdrücke eines benutzerdefinierten Typs Symbole, die an Werte dieses Typs gebunden sind, Array Elemente von Arrays dieses Typs und Aufruf Bare Aufrufe, die diesen Typ zurückgeben.

## <a name="unwrap-expressions"></a>Entpacken von Ausdrücken

In Q# ist der Unwrap-Operator ein nach gestelltes Ausrufezeichen `!`.
Wenn `IntPair` beispielsweise einen benutzerdefinierten Typ mit dem zugrunde liegenden Typ `(Int, Int)`und `s` eine Variable mit einem Wert `IntPair(2,3)`war, dann `s!` `(2,3)`.

Für benutzerdefinierte Typen, die in Bezug auf andere benutzerdefinierte Typen definiert sind. der Unwrap-Operator kann wiederholt werden. Beispielsweise gibt `s!!` den doppelt entpackten Wert `s`an.
Wenn `WrappedPair` ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ `IntPair`ist und `t` eine Variable mit einem Wert `WrappedPair(IntPair(1,2))`ist, dann wird `t!!` `(1,2)`.

Der `!` Operator hat eine höhere Rangfolge als alle anderen Operatoren als `[]` für die Array Indizierung und die Slicing.
`!` und `[]` Bindung Positions bedingt; Das heißt, `a[i]![3]` als `((a[i])!)[3]`gelesen werden sollen: nehmen Sie das `i`"th-Element `a`, entpacken Sie es, und holen Sie dann das dritte Element des entpackten Werts (der ein Array sein muss).

Die Rangfolge des `!` Operators hat eine Beeinträchtigung, die möglicherweise nicht offensichtlich ist.
Wenn eine Funktion oder ein Vorgang einen Wert zurückgibt, der dann entpackt wird, muss der Funktions-oder Vorgangs Ausdruck in Klammern eingeschlossen werden, damit das Argument Tupel an den-Ausdruck gebunden wird, anstatt an den Unwrap-Vorgang.
Beispiel:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Array Ausdrücke

Ein Arrayliteral ist eine Sequenz von einem oder mehreren Element Ausdrücken, die durch Kommas getrennt sind und in `[` und `]`eingeschlossen werden.
Alle-Elemente müssen mit demselben Typ kompatibel sein.

Wenn der allgemeine Elementtyp ein Vorgang oder Funktionstyp ist, müssen alle Elemente die gleichen Eingabe-und Ausgabetypen aufweisen.
Der Elementtyp des Arrays unterstützt alle Funktoren, die von allen Elementen unterstützt werden.
Wenn z. b. `Op1`, `Op2`und `Op3` alle `Qubit[] => Unit`sind, `Op1` aber `Adjoint`unterstützt, unterstützt `Op2` `Controlled`, und `Op3` unterstützt beides:

- `[Op1, Op2]` ist ein Array von `(Qubit[] => Unit)` Vorgängen.
- `[Op1, Op3]` ist ein Array von `(Qubit[] => Unit is Adj)` Vorgängen.
- `[Op2, Op3]` ist ein Array von `(Qubit[] => Unit is Ctl)` Vorgängen.

Leere Array Literale, `[]`, sind nicht zulässig.
Verwenden Sie stattdessen `new ★[0]`, bei dem `★` als Platzhalter für einen geeigneten Typ dient, das Erstellen des gewünschten Arrays der Länge 0 (null).

Bei zwei Arrays desselben Typs kann der binäre `+`-Operator verwendet werden, um ein neues Array zu bilden, bei dem es sich um die Verkettung der beiden Arrays handelt.
Beispielsweise ist `[1,2,3] + [4,5,6]` `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Array Erstellung

Wenn ein Typ und ein `Int` Ausdruck verwendet werden, kann der `new` Operator verwendet werden, um ein neues Array mit der angegebenen Größe zuzuordnen.
Beispielsweise wird `new Int[i+1]` ein neues `Int` Array mit `i+1` Elementen zuordnen.

Die Elemente eines neuen Arrays werden mit einem typabhängigen Standardwert initialisiert.
In den meisten Fällen ist dies eine Variation von 0 (null).

Bei Qubits und callables, bei denen es sich um Verweise auf Entitäten handelt, gibt es keinen angemessenen Standardwert.
Daher ist für diese Typen der Standardwert ein ungültiger Verweis, der nicht verwendet werden kann, ohne dass ein Laufzeitfehler verursacht wird.
Dies ähnelt einem NULL-Verweis in Sprachen wie C# oder Java.
Arrays, die Qubits oder callables enthalten, müssen ordnungsgemäß mit nicht standardmäßigen Werten initialisiert werden, bevor ihre Elemente problemlos verwendet werden können. Geeignete Initialisierungs Routinen finden Sie in <xref:microsoft.quantum.arrays>.

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

Tupeltypen werden Element für Element initialisiert.


### <a name="jagged-arrays"></a>Verzweigte Arrays

Eine Jagged Array, manchmal auch als "Array von Arrays" bezeichnet, ist ein Array, dessen Elemente Arrays sind. Die Elemente einer Jagged Array können unterschiedlich sein. Im folgenden Beispiel wird gezeigt, wie Sie eine Jagged Array deklarieren und initialisieren, die eine Multiplikationstabelle darstellt.

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


### <a name="array-slices"></a>Array Slices

Wenn ein Array Ausdruck und ein `Range` Ausdruck vorliegen, kann ein neuer Ausdruck mithilfe des `[`-und `]` Array Slice-Operators gebildet werden.
Der neue Ausdruck hat denselben Typ wie das Array und enthält die Array Elemente, die von den Elementen der `Range`indiziert werden, in der Reihenfolge, die vom `Range`definiert wird.
Wenn `a` beispielsweise an ein Array von `Double`s gebunden ist, ist `a[3..-1..0]` ein `Double[]` Ausdruck, der die ersten vier Elemente von `a` enthält, jedoch in umgekehrter Reihenfolge, wie Sie in `a`angezeigt werden.

Wenn das `Range` leer ist, ist das resultierende Array in der Länge 0 (null).

Wenn es sich bei dem Array Ausdruck nicht um einen einfachen Bezeichner handelt, muss er in Klammern eingeschlossen werden, damit er in einen Slice eingefügt werden kann.
Wenn beispielsweise `a` und `b` beide Arrays `Int`s sind, würde ein Slice aus der Verkettung wie folgt ausgedrückt werden:

```qsharp
(a+b)[1..2..7]
```

Alle Arrays in Q# sind NULL basiert.
Das heißt, dass das erste Element eines Arrays `a` immer `a[0]`ist.

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

## <a name="array-element-expressions"></a>Array Element Ausdrücke

Wenn ein Array Ausdruck und ein `Int` Ausdruck vorliegen, kann ein neuer Ausdruck mithilfe des `[` und `]` Array Element-Operators gebildet werden.
Der neue Ausdruck hat denselben Typ wie der Elementtyp des Arrays.
Wenn `a` beispielsweise an ein Array von `Double`s gebunden ist, ist `a[4]` ein `Double` Ausdruck.

Wenn der Array Ausdruck kein einfacher Bezeichner ist, muss er in Klammern eingeschlossen werden, um ein Element auszuwählen.
Wenn beispielsweise `a` und `b` beide Arrays `Int`s sind, würde ein Element aus der Verkettung wie folgt ausgedrückt werden:

```qsharp
(a+b)[13]
```

Alle Arrays in Q# sind NULL basiert.
Das heißt, dass das erste Element eines Arrays `a` immer `a[0]`ist.


## <a name="copy-and-update-expressions"></a>Copy-und Update-Ausdrücke

Neue Arrays können über Kopier-und Update Ausdrücke aus vorhandenen erstellt werden.
Ein Copy-and-Update-Ausdruck ist ein Ausdruck der Form `expression1 w/ expression2 <- expression3`, bei dem `expression1` für einige Typen `T`vom Typ `T[]` sein muss. Die zweite `expression2` definiert die Indizes der zu ändernden Elemente im Vergleich zum Array in `expression1` und muss entweder vom Typ `Int` oder vom Typ `Range`sein. Wenn `expression2` vom Typ `Int`ist, muss `expression3` vom Typ `T`sein. Wenn `expression2` vom Typ `Range`ist, muss `expression3` vom Typ `T[]`sein.

Ein Copy-and-Update-Ausdruck `arr w/ idx <- value` erstellt ein neues Array mit allen Elementen, die auf das entsprechende Element in `arr`festgelegt sind, mit Ausnahme der Elemente in `idx`, die in `value`auf das entsprechende Element festgelegt sind. Wenn `arr` z. b. ein Array `[0,1,2,3]`enthält, dann 
- `arr w/ 0 <- 10` ist das Array `[10,1,2,3]`.
- `arr w/ 2 <- 10` ist das Array `[0,1,10,3]`.
- `arr w/ 0..2..3 <- [10,12]` ist das Array `[10,1,12,3]`.

Ähnliche Ausdrücke sind für benannte Elemente in benutzerdefinierten Typen vorhanden. Beachten Sie beispielsweise den-Typ. 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Wenn `c` den Wert des Typs `Complex(1.,-1.)`enthält, ist `c w/ Re <- 0.` ein Ausdruck vom Typ `Complex`, der als `Complex(0.,-1.)`ausgewertet wird.

## <a name="conditional-expressions"></a>Bedingte Ausdrücke

Bei zwei anderen Ausdrücken desselben Typs und eines booleschen Ausdrucks kann der bedingte Ausdruck mit dem Fragezeichen `?` und der senkrechten Leiste `|`gebildet werden.
Beispielsweise `a==b ? c | d`.
In diesem Beispiel wird der Wert des bedingten Ausdrucks `c`, wenn `a==b` true ist, und `d`, wenn er false ist.

Die beiden Ausdrücke können zu Vorgängen ausgewertet werden, die über die gleichen Eingaben und Ausgaben verfügen, aber unterschiedliche Funktions tüktoren unterstützen.
In diesem Fall ist der Typ des bedingten Ausdrucks ein Vorgang mit diesen Eingaben und Ausgaben, der alle von beiden Ausdrücken unterstützten Funktoren unterstützt.
Wenn z. b. `Op1`, `Op2`und `Op3` alle `Qubit[]=>Unit`sind, `Op1` aber `Adjoint`unterstützt, unterstützt `Op2` `Controlled`, und `Op3` unterstützt beides:

- `flag ? Op1 | Op2` ist ein `(Qubit[] => Unit)` Vorgang.
- `flag ? Op1 | Op3` ist ein `(Qubit[] => Unit is Adj)` Vorgang.
- `flag ? Op2 | Op3` ist ein `(Qubit[] => Unit is Ctl)` Vorgang.

Wenn einer der beiden möglichen Ergebnis Ausdrücke einen Funktions-oder einen Vorgangs aufzurufen enthält, findet dieser Vorgang nur statt, wenn das Ergebnis das Ergebnis ist, das der Wert des Aufrufes ist.
Wenn `a==b` beispielsweise `a==b ? C(qs) | D(qs)`den Wert true hat, wird der `C` Vorgang aufgerufen, wenn er false ist, und wenn er false ist, wird nur `D` aufgerufen.
Dies ähnelt der Kurzschluss in anderen Sprachen.


## <a name="operator-precedence"></a>Operatorrangfolge

Alle binären Operatoren sind mit Ausnahme von `^`rechts assoziativ.

Eckige Klammern, `[` und `]`für das aufteilen und Indizieren von Arrays werden vor jedem Operator gebunden.

Die Funktoren `Adjoint` und `Controlled` nach der Array Indizierung gebunden werden, aber vor allen anderen Operatoren.

Klammern für Vorgangs-und Funktionsaufrufe werden auch vor jedem Operator gebunden, aber nach der Array Indizierung und den Funktoren.

Operatoren in Rangfolge, vom höchsten zum niedrigsten:

Operator | Ständigkeit | BESCHREIBUNG | Operanden Typen
---------|----------|---------|---------------
 nachfolgende `!` | Unäroperatoren | Aufheben der Umschließung | Ein beliebiger benutzerdefinierter Typ
 `-`, `~~~`, `not` | Unäroperatoren | Numerische negative, bitweise Komplement logische Negation | `Int`, `BigInt` oder `Double` für `-`, `Int` oder `BigInt` `~~~`für `Bool``not`
 `^` | Binary | Ganzzahlige Potenz | `Int` oder `BigInt` für die Basis `Int` für den Exponenten.
 `/`, `*`, `%` | Binary | Division, Multiplikation, ganzzahliger Modulo | `Int`, `BigInt` oder `Double` für `/` und `*`, `Int` oder `BigInt` für `%`
 `+`, `-` | Binary | Addition oder Zeichenfolge und Array Verkettung, Subtraktion | `Int`, `BigInt` oder `Double`, zusätzlich `String` oder ein beliebiger Arraytyp für `+`
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
