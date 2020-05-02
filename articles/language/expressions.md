---
title: 'F #-Ausdrücke'
description: 'Erfahren Sie, wie Konstanten, Variablen, Operatoren, Vorgänge und Funktionen als Ausdrücke in Q # angegeben, referenziert und kombiniert werden.'
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 095be52af27f827f3e52d39a70702f50d6d59ee8
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82683928"
---
# <a name="expressions"></a>Ausdrücke

## <a name="grouping"></a>Gruppierung

Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.
`(7)` Beispielsweise `Int` ist ein Ausdruck, `([1,2,3])` ist ein Ausdruck vom Typ Array von `Int`s, und `((1,2))` ist ein Ausdruck vom Typ. `(Int, Int)`

Die Äquivalenz zwischen einfachen Werten und Tupeln mit einem einzelnen Element, die im [Typmodell](xref:microsoft.quantum.language.type-model#tuple-types) beschrieben `(6)` werden, entfernt die `(6)` Mehrdeutigkeit zwischen als Gruppe und als Tupel mit einem einzelnen Element.

## <a name="symbols"></a>Symbole

Der Name eines einem Wert des Typs `'T` zugeordneten Symbols ist ein Ausdruck vom Typ. `'T`
Wenn das Symbol `count` beispielsweise an den ganzzahligen Wert `5`gebunden ist, `count` ist ein ganzzahliger Ausdruck.

## <a name="numeric-expressions"></a>Numerische Ausdrücke

Numerische Ausdrücke sind Ausdrücke vom Typ `Int`, `BigInt`oder `Double`.
Das heißt, Sie sind entweder ganzzahlige oder Gleit Komma Zahlen.

`Int`Literale in Q # sind mit ganzzahligen Literalen in c# identisch, mit dem Unterschied, dass kein nach gestelltes "l" oder "l" erforderlich (oder zulässig) ist.
Hexadezimale und binäre ganze Zahlen werden mit dem Präfix "0x" bzw. "0B" unterstützt.

`BigInt`Literale in Q # sind identisch mit großen ganzzahligen Zeichen folgen in .net mit einem nachfolgenden "l" oder "l".
Hexadezimale große ganze Zahlen werden mit dem Präfix "0x" unterstützt.
Daher sind die folgenden alle gültigen Verwendungsmöglichkeiten von `BigInt` Literalen:

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

`Double`Literale in Q # sind mit doppelten Literalen in c# identisch, mit dem Unterschied, dass kein nach gestelltes "d" oder "d" erforderlich (oder zulässig) ist.

Wenn ein Array Ausdruck eines beliebigen Elementtyps vorhanden ist `Int` , kann ein Ausdruck mithilfe der `Length` integrierten Funktion gebildet werden, wobei der Array Ausdruck in Klammern eingeschlossen ist, `(` und. `)`
Wenn `a` beispielsweise an ein Array gebunden ist, dann `Length(a)` ist ein ganzzahliger Ausdruck.
Wenn `b` ein Array von Arrays ganzer Zahlen ist, `Int[][]`dann `Length(b)` ist die Anzahl der Unterarrays in `b`, und `Length(b[1])` die Anzahl von ganzen Zahlen im zweiten Unterarray in. `b`

Bei zwei `+`numerischen Ausdrücken desselben Typs können die binären Operatoren `-` `*`,, und `/` verwendet werden, um einen neuen numerischen Ausdruck zu bilden.
Der Typ des neuen Ausdrucks ist mit den Typen der einzelnen Ausdrücke identisch.

Bei zwei ganzzahligen Ausdrücken kann der `^` binäre Operator (Power) verwendet werden, um einen neuen ganzzahligen Ausdruck zu bilden.
Auf ähnliche `^` Weise kann mit zwei doppelten Ausdrücken verwendet werden, um einen neuen doppelten Ausdruck zu bilden.
Schließlich `^` kann mit einer großen Ganzzahl auf der linken Seite und einer Ganzzahl auf der rechten Seite verwendet werden, um einen neuen großen ganzzahligen Ausdruck zu bilden.
In diesem Fall muss der zweite Parameter in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.

Bei zwei ganzzahligen oder großen ganzzahligen Ausdrücken kann ein neuer Integer-Ausdruck oder ein großer `%` ganzzahliger Ausdruck mit `&&&` den Operatoren (Modulus) `|||` , (bitweiser and), ( `^^^` bitweiser or) oder (Bitweiser XOR) gebildet werden.

Beim Ausdruck "Integer" oder "Big Integer" auf der linken Seite und einem ganzzahligen Ausdruck auf `<<<` der rechten Seite können die Operatoren (arithmetischer Left Shift) oder `>>>` (arithmetischer rechts Schiebe Operator) zum Erstellen eines neuen Ausdrucks mit dem gleichen Typ wie der linke Ausdruck verwendet werden.

Der zweite Parameter (die UMSCHALT Menge) in einen Verschiebungs Vorgang muss größer oder gleich 0 (null) sein. das Verhalten für negative Verschiebungs Beträge ist nicht definiert.
Der Verschiebungs Betrag für einen der Verschiebungs Vorgänge muss ebenfalls in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.
Wenn die zu Verschiebe Zahl eine ganze Zahl ist, wird der Verschiebungs Betrag `mod 64`interpretiert. Das heißt, dass eine Verschiebung von 1 und eine Schicht von 65 denselben Effekt haben.

Bei ganzzahligen und großen ganzzahligen Werten sind Verschiebungen arithmetisch.
Wenn Sie einen negativen Wert entweder nach links oder rechts verschieben, ergibt dies eine negative Zahl.
Das heißt, die Verschiebung eines Schritts nach links oder rechts ist identisch mit der Multiplikation bzw. Division durch 2.

Die ganzzahlige Division und der ganzzahlige Modulo folgen dem Verhalten für negative Zahlen wie c#.
Das heißt, `a % b` dass immer dasselbe Vorzeichen wie `a`hat und `b * (a / b) + a % b` immer gleich `a`ist.
Beispiel:

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 5 | 2 | 2 | 1
 5 | -2 | -2 | 1
 -5 | 2 | -2 | -1
 -5 | -2 | 2 | -1

Große ganzzahlige Division und Modulo funktionieren auf dieselbe Weise.

Wenn ein beliebiger numerischer Ausdruck vorhanden ist, kann ein neuer `-` Ausdruck mit dem unären Operator gebildet werden.
Der neue Ausdruck hat denselben Typ wie der konstituierende Ausdruck.

Bei allen ganzzahligen oder großen ganzzahligen Ausdrücken kann ein neuer Ausdruck desselben Typs mit dem `~~~` unären Operator (bitweiser Komplement) gebildet werden.

## <a name="boolean-expressions"></a>Boolesche Ausdrücke

Die beiden `Bool` Literalwerte `true` sind `false`und.

Wenn zwei Ausdrücke desselben primitiven Typs vorhanden sind, können die `==` binären `!=` Operatoren und verwendet werden, um einen `Bool` -Ausdruck zu erstellen.
Der Ausdruck ist true, wenn die beiden Ausdrücke gleich sind, andernfalls false.

Werte von benutzerdefinierten Typen können nicht verglichen werden, sondern es können nur Ihre nicht umschließenden Werte verglichen werden. Verwenden Sie z. b. den Operator `!` "Unwrap" (auf der Seite " [Q # Type Model](xref:microsoft.quantum.language.type-model#user-defined-types)" erläutert).

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

Der Gleichheits `Qubit` Vergleich für Werte ist Identitäts Gleichheit. Das heißt, ob die beiden Ausdrücke dasselbe Qubit identifizieren.
Der Zustand der beiden Qubits wird von diesem Vergleich nicht verglichen, auf Sie zugegriffen, gemessen oder geändert.

Der Gleichheits `Double` Vergleich für Werte kann aufgrund von Rundungs Effekten irreführend sein.
Beispielsweise `49.0 * (1.0/49.0) != 1.0`.

Bei zwei numerischen Ausdrücken können die binären Operatoren `>` `<` `>=`,, und `<=` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der erste Ausdruck größer als, kleiner als, größer als oder gleich oder kleiner oder gleich dem zweiten Ausdruck ist.

Bei zwei booleschen Ausdrücken können die `and` binären Operatoren und `or` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn beide Ausdrücke den Wert true haben.

Bei jedem booleschen Ausdruck kann der `not` unäre Operator verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der konstituierende Ausdruck false ist.

## <a name="string-expressions"></a>Zeichen folgen Ausdrücke

Q # ermöglicht die Verwendung von Zeichen folgen in `fail` der-Anweisung `Log` und der Standardfunktion.

Zeichen folgen in Q # sind entweder Literale oder interpoliert Zeichen folgen.
Zeichenfolgenliterale ähneln in den meisten Sprachen einfachen Zeichenfolgenliteralen: eine Sequenz von Unicode- `"`Zeichen, die in doppelten Anführungszeichen eingeschlossen sind.
Innerhalb einer Zeichen `\` Folge kann der umgekehrte Schrägstrich verwendet werden, um ein doppeltes Anführungszeichen mit Escapezeichen zu versehen und eine neue Zeile als `\n` `\r`einzufügen, als und als Tabstopp Zeichen. `\t`
Beispiel:

```qsharp
"\"Hello world!\", she said.\n"
```

Die Q #-Syntax für Zeichen folgen Interpolationen ist eine Teilmenge der c# 7,0-Syntax. Q # unterstützt keine ausführlichen (mehrzeiligen) interpoliert Zeichen folgen.
Informationen zur c#-Syntax finden Sie unter [*interpoliert*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) .

Ausdrücke in einer interinterierten Zeichenfolge Folgen der Q #-Syntax, nicht der c#-Syntax.
Jeder gültige Q #-Ausdruck kann in einer interinterierten Zeichenfolge angezeigt werden.

## <a name="qubit-expressions"></a>Qubit-Ausdrücke

Die einzigen `Qubit` Ausdrücke sind Symbole, die an `Qubit` Werte oder Array Elemente von `Qubit` Arrays gebunden sind.
Es sind keine `Qubit` Literale vorhanden.

## <a name="pauli-expressions"></a>Pauli-Ausdrücke

Die vier `Pauli` Werte `PauliI` `PauliX` `PauliY`,,, und `PauliZ`sind gültige `Pauli` Ausdrücke.

Abgesehen davon sind die einzigen `Pauli` Ausdrücke Symbole, die an `Pauli` Werte oder Array Elemente von `Pauli` Arrays gebunden sind.

## <a name="result-expressions"></a>Ergebnis Ausdrücke

Die beiden `Result` Werte `One` und `Zero`sind gültige `Result` Ausdrücke.

Abgesehen davon sind die einzigen `Result` Ausdrücke Symbole, die an `Result` Werte oder Array Elemente von `Result` Arrays gebunden sind.
Beachten Sie insbesondere, dass `One` nicht mit der ganzen `1`Zahl identisch ist, und es gibt keine direkte Konvertierung zwischen Ihnen.
Das gleiche gilt für `Zero` und. `0`

## <a name="range-expressions"></a>Bereichs Ausdrücke

Bei allen drei `Int` Ausdrücken `start` `start .. step .. stop` `start`ist `step`, und `stop`ein Bereichs Ausdruck, dessen erstes Element, zweites Element `start+step`, drittes Element `start+step+step`, usw. ist, bis `stop` übergeben wird.
Ein Bereich kann leer sein, wenn z.b. positiv und `step` `stop < start`ist.
Das letzte `stop` Element des Bereichs ist, wenn der Unterschied zwischen `start` und `stop` ein ganzzahliges Vielfaches `step`von ist. Das heißt, der Bereich ist an beiden Enden inklusiv.

Bei `Int` `start` `stop`zwei Ausdrücken und `start .. stop` ist ein Bereichs Ausdruck, der gleich ist. `start .. 1 .. stop`
Beachten Sie, dass `step` der implizierte Wert + `stop` 1 ist, `start`auch wenn kleiner als ist. in einem solchen Fall ist der Bereich leer.

Einige Beispiel Bereiche sind:

- `1..3`der Bereich von 1, 2, 3.
- `2..2..5`ist der Bereich von 2, 4.
- `2..2..6`ist der Bereich von 2, 4, 6.
- `6..-2..2`der Bereich ist 6, 4, 2.
- `2..1`der leere Bereich.
- `2..6..7`der Bereich 2.
- `2..2..1`der leere Bereich.
- `1..-1..2`der leere Bereich.

## <a name="callable-expressions"></a>Aufruf Bare Ausdrücke

Ein Aufruf bares Literalelement ist der Name eines Vorgangs oder einer Funktion, der im Kompilierungs Bereich definiert ist.
Beispielsweise `X` ist ein vorgangsliteral, das auf den `X` -Standard Bibliotheks `Message` Vorgang verweist, und ist ein Funktionsliteral `Message` , das auf die Standard Bibliotheksfunktion verweist.

Wenn ein Vorgang das `Adjoint` Funktor unterstützt, `Adjoint op` ist ein Vorgangs Ausdruck.
Entsprechend `Controlled op` ist ein Vorgangs Ausdruck, wenn `Controlled` der Vorgang das Funktor unterstützt.
Die Typen dieser Ausdrücke werden in den [Funktoren](xref:microsoft.quantum.language.type-model#functors)angegeben.

Funktoren (`Adjoint` und `Controlled`) werden genauer gebunden als alle anderen Operatoren, mit Ausnahme des Unwrap `!` -Operators und der `[]`Array Indizierung mit.
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

Wenn `Fun` beispielsweise eine Funktion mit der Signatur `'T1->Unit`ist:

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomeOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a>Aufruf Bare Aufruf Ausdrücke

Bei einem Aufruf baren Ausdruck (Operation oder Funktion) und einem Tupelausdruck des Eingabetyps der Aufruf baren Signatur kann ein Aufruf Ausdruck gebildet werden, indem der Tupelausdruck an den Aufruf baren Ausdruck angefügt wird.
Der Typ des Aufruf Ausdrucks ist der Ausgabetyp der Signatur des Callable-Ausdrucks.

Wenn `Op` z. b. ein Vorgang mit der `((Int, Qubit) => Double)`Signatur `Op(3, qubit1)` ist, ist ein Ausdruck `Double`vom Typ.
Ebenso ist, `Sin` wenn eine Funktion mit der `(Double -> Double)`Signatur `Sin(0.1)` ist, ein Ausdruck vom `Double`Typ.
Wenn `Builder` schließlich eine Funktion mit der Signatur `(Int -> (Int -> Int))`ist, dann `Builder(3)` ist eine Funktion von in bis int.

Zum Aufrufen des Ergebnisses eines Aufruf baren Ausdrucks ist ein zusätzliches Paar von Klammern um den Aufruf baren Ausdruck erforderlich.
Um also das Ergebnis des Aufrufs aus `Builder` dem vorherigen Absatz aufzurufen, ist die korrekte Syntax:

```qsharp
(Builder(3))(2)
```

Wenn Sie einen vom Typ parametrisierten Aufruf baren aufrufen, können die tatsächlichen Typparameter in spitzen Klammern `<` und `>` nach dem Aufruf baren Ausdruck angegeben werden.
Dies ist in der Regel unnötig, da der Q #-Compiler die eigentlichen Typen ableiten wird.
Dies ist für die partielle Anwendung erforderlich (siehe unten), wenn ein typparametrisiertes Argument nicht angegeben wird.
Dies ist manchmal auch nützlich, wenn die Übergabe von Vorgängen mit unterschiedlichen Funktoren unterstützt wird.

`Func` Wenn `('T1, 'T2, 'T1) -> 'T2`beispielsweise die Signatur aufweist `Op1` und `Op2` die Signatur `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)`und die Signatur aufweisen, um mit `Func` `Op1` als erstes Argument, `Op2` als zweites und `Op3` als drittes aufzurufen:

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

Die Typspezifikation ist erforderlich, `Op3` da `Op1` und unterschiedliche Typen aufweisen, sodass der Compiler dies ohne Angabe der Spezifikation als mehrdeutig behandelt.

### <a name="partial-application"></a>Partielle Anwendung

Bei einem Aufruf baren Ausdruck kann ein neuer Aufruf barer Ausdruck erstellt werden, indem eine Teilmenge der Argumente für die Aufruf Bare bereitgestellt wird.
Dies wird als _partielle Anwendung_bezeichnet.

In f # wird eine teilweise angewendete Aufruf Bare-Datei durch Schreiben eines normalen Aufruf Ausdrucks ausgedrückt, wobei jedoch ein `_`unterstrich für die nicht angegebenen Argumente verwendet wird.
Die sich ergebende Aufruf Bare hat denselben Ergebnistyp wie die basiscallable und die gleichen Spezialisierungs Vorgänge für Vorgänge.
Der Eingabetyp der partiellen Anwendung ist einfach der ursprüngliche Typ mit den angegebenen Argumenten.

Wenn beim Erstellen einer partiellen Anwendung eine änderbare Variable als angegebenes Argument angegeben wird, wird der aktuelle Wert der Variablen verwendet.
Wenn Sie den Wert der Variablen anschließend ändern, wirkt sich dies nicht auf die partielle Anwendung aus.

Wenn `Op` z. b. den `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`-Typ aufweist:

- `Op(5,(_,_))`weist den `(((Qubit,Qubit), Double) => Unit is Adj)`-Typ auf und `Op(5,_)`hat daher.
- `Op(_,(_,1.0))` weist den Typ `((Int, (Qubit,Qubit)) => Unit is Adj)` auf.
- `Op(_,((q1,q2),_))` weist den Typ `((Int,Double) => Unit is Adj)` auf.
   Beachten Sie, dass hier eine Singleton-tupeläquivalenz angewendet wurde.

Wenn das teilweise angewendete Aufruf Bare Typparameter aufweist, die vom Compiler nicht abgeleitet werden können, müssen Sie auf der Aufruf Site bereitgestellt werden.
Die partielle Anwendung darf keine nicht angegebenen Typparameter aufweisen.

Wenn `Op` z. b. den `(('T1, Qubit, 'T1) => Unit : Adjoint)`-Typ aufweist:

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a>Rekursion

F #-callables dürfen direkt oder indirekt rekursiv sein.
Das heißt, ein Vorgang oder eine Funktion kann sich selbst aufrufen, oder es kann eine andere Aufruf Bare aufgerufen werden, die den Aufruf baren Vorgang direkt oder indirekt aufruft.

Es gibt jedoch zwei wichtige Kommentare zur Verwendung der Rekursion:

- Die Verwendung von Rekursion bei Vorgängen beeinträchtigt wahrscheinlich bestimmte Optimierungen.
  Dies kann erhebliche Auswirkungen auf die Ausführungszeit des Algorithmus haben.
- Bei der Ausführung auf einem eigentlichen Quantum-Gerät kann der Stapel Speicher eingeschränkt sein, sodass die Tiefe Rekursion zu einem Laufzeitfehler führen kann.
  Insbesondere der Q #-Compiler und die Common Language Runtime erkennen und optimieren die Endrekursion nicht.

## <a name="tuple-expressions"></a>Tupelausdrücke

Ein tupelliteral ist eine Sequenz von Element Ausdrücken des entsprechenden Typs, die durch Kommas getrennt sind und `(` in `)`und eingeschlossen sind.
Beispielsweise `(1, One)` ist ein `(Int, Result)` Ausdruck.

Abgesehen von Literalen sind die einzigen Tupelausdrücke Symbole, die an Tupelwerte, Array Elemente von tupelarrays und Aufruf Bare Aufrufe gebunden sind, die Tupel zurückgeben.

## <a name="user-defined-type-expressions"></a>Benutzerdefinierte typausdrücke

Ein Literalwert eines benutzerdefinierten Typs besteht aus dem Typnamen, gefolgt von einem tupelliteraltyp mit dem basistupeltyp des Typs.
Wenn `IntPair` beispielsweise ein benutzerdefinierter Typ ist, der auf `(Int, Int)`basiert, dann `IntPair(2,3)` wäre ein gültiges Literale dieses Typs.

Anders als Literale sind die einzigen Ausdrücke eines benutzerdefinierten Typs Symbole, die an Werte dieses Typs gebunden sind, Array Elemente von Arrays dieses Typs und Aufruf Bare Aufrufe, die diesen Typ zurückgeben.

## <a name="unwrap-expressions"></a>Entpacken von Ausdrücken

In Q # ist der Unwrap-Operator ein nach gestelltes `!`Ausrufezeichen.
`IntPair` Wenn `(Int, Int)`beispielsweise ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ und `s` eine Variable mit Wert `IntPair(2,3)`ist, `s!` wäre. `(2,3)`

Für benutzerdefinierte Typen, die in Bezug auf andere benutzerdefinierte Typen definiert sind. der Unwrap-Operator kann wiederholt werden. `s!!` gibt beispielsweise den doppelt entpackten Wert von an `s`.
Wenn `WrappedPair` `IntPair`also ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ und `t` eine Variable mit Wert `WrappedPair(IntPair(1,2))`ist, dann `t!!` ist. `(1,2)`

Der `!` Operator hat `[]` eine höhere Rangfolge als alle anderen Operatoren, außer für die Array Indizierung und die Slicing.
`!`und `[]` Bindung Positions bedingt; Das heißt, `a[i]![3]` sollte als `((a[i])!)[3]`gelesen werden: nehmen Sie `i`das ' th ' `a`-Element von, entpacken Sie es, und holen Sie dann das dritte Element des entpackten Werts (der ein Array sein muss).

Die Rangfolge des `!` Operators hat eine Beeinträchtigung, die möglicherweise nicht offensichtlich ist.
Wenn eine Funktion oder ein Vorgang einen Wert zurückgibt, der dann entpackt wird, muss der Funktions-oder Vorgangs Ausdruck in Klammern eingeschlossen werden, damit das Argument Tupel an den-Ausdruck gebunden wird, anstatt an den Unwrap-Vorgang.
Beispiel:

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a>Array Ausdrücke

Ein Arrayliteral ist eine Sequenz von einem oder mehreren Element Ausdrücken, die durch Kommas getrennt `[` sind `]`und in und eingeschlossen ist.
Alle-Elemente müssen mit demselben Typ kompatibel sein.

Wenn der allgemeine Elementtyp ein Vorgang oder Funktionstyp ist, müssen alle Elemente die gleichen Eingabe-und Ausgabetypen aufweisen.
Der Elementtyp des Arrays unterstützt alle Funktoren, die von allen Elementen unterstützt werden.
Wenn `Op1`z. b. `Op2`, und `Op3` alle sind `Qubit[] => Unit`, `Op1` `Adjoint` `Op2` `Controlled`unterstützt, unterstützt und `Op3` unterstützt jedoch beide:

- `[Op1, Op2]`ist ein Array von `(Qubit[] => Unit)` Vorgängen.
- `[Op1, Op3]`ist ein Array von `(Qubit[] => Unit is Adj)` Vorgängen.
- `[Op2, Op3]`ist ein Array von `(Qubit[] => Unit is Ctl)` Vorgängen.

Leere Array Literale, `[]`, sind nicht zulässig.
Wenn Sie `new ★[0]`stattdessen verwenden `★` , wobei als Platzhalter für einen geeigneten Typ verwendet, ermöglicht das Erstellen des gewünschten Arrays der Länge 0 (null).

Bei zwei Arrays desselben Typs kann der binäre `+` Operator verwendet werden, um ein neues Array zu bilden, bei dem es sich um die Verkettung der beiden Arrays handelt.
Beispielsweise `[1,2,3] + [4,5,6]` ist `[1,2,3,4,5,6]`.

### <a name="array-creation"></a>Array Erstellung

Bei Angabe eines Typs und `Int` eines Ausdrucks kann `new` der Operator verwendet werden, um ein neues Array mit der angegebenen Größe zuzuordnen.
Beispielsweise `new Int[i+1]` würde ein neues `Int` Array mit `i+1` -Elementen zuordnen.

Die Elemente eines neuen Arrays werden mit einem typabhängigen Standardwert initialisiert.
In den meisten Fällen ist dies eine Variation von 0 (null).

Bei Qubits und callables, bei denen es sich um Verweise auf Entitäten handelt, gibt es keinen angemessenen Standardwert.
Daher ist für diese Typen der Standardwert ein ungültiger Verweis, der nicht verwendet werden kann, ohne dass ein Laufzeitfehler verursacht wird.
Dies ähnelt einem NULL-Verweis in Sprachen wie c# oder Java.
Arrays, die Qubits oder callables enthalten, müssen ordnungsgemäß mit nicht standardmäßigen Werten initialisiert werden, bevor ihre Elemente problemlos verwendet werden können. Geeignete Initialisierungs Routinen finden Sie unter <xref:microsoft.quantum.arrays>.

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

Bei einem Array Ausdruck und einem `Range` -Ausdruck kann ein neuer Ausdruck mit dem und dem `[` Array `]` Slice-Operator gebildet werden.
Der neue Ausdruck `Range`hat denselben Typ wie das Array und enthält die Array Elemente, die von den Elementen des-Elements indiziert werden, in der Reihenfolge, `Range`die durch definiert wird.
Wenn `a` beispielsweise an ein Array von `Double`s gebunden ist, dann `a[3..-1..0]` ist ein `Double[]` -Ausdruck, der die ersten vier Elemente von `a` enthält, jedoch in umgekehrter Reihenfolge, `a`wie Sie in angezeigt werden.

Wenn das `Range` leer ist, ist das resultierende Array in der Länge 0 (null).

Wenn es sich bei dem Array Ausdruck nicht um einen einfachen Bezeichner handelt, muss er in Klammern eingeschlossen werden, damit er in einen Slice eingefügt werden kann.
Wenn `a` und `b` beispielsweise beide Arrays von `Int`s sind, würde ein Slice aus der Verkettung wie folgt ausgedrückt werden:

```qsharp
(a+b)[1..2..7]
```

Alle Arrays in Q # sind NULL basiert.
Das heißt, das erste Element eines Arrays `a` ist immer. `a[0]`

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

Bei einem Array Ausdruck und einem `Int` Ausdruck kann ein neuer Ausdruck mit dem und `[` `]` dem Array Element Operator gebildet werden.
Der neue Ausdruck hat denselben Typ wie der Elementtyp des Arrays.
Wenn `a` beispielsweise an ein Array von `Double`s gebunden ist, dann `a[4]` ist ein `Double` -Ausdruck.

Wenn der Array Ausdruck kein einfacher Bezeichner ist, muss er in Klammern eingeschlossen werden, um ein Element auszuwählen.
Wenn `a` und `b` beispielsweise beide Arrays von `Int`s sind, würde ein Element aus der Verkettung wie folgt ausgedrückt werden:

```qsharp
(a+b)[13]
```

Alle Arrays in Q # sind NULL basiert.
Das heißt, das erste Element eines Arrays `a` ist immer. `a[0]`


## <a name="copy-and-update-expressions"></a>Copy-und Update-Ausdrücke

Neue Arrays können über Kopier-und Update Ausdrücke aus vorhandenen erstellt werden.
Ein Copy-and-Update-Ausdruck ist ein Ausdruck der Form `expression1 w/ expression2 <- expression3`, wobei `expression1` für einen Typ vom Typ `T[]` sein muss `T`. Die zweite `expression2` definiert die Indizes der Elemente, die im Vergleich zum Array in `expression1` geändert werden sollen, und muss entweder vom Typ `Int` oder vom Typ `Range`sein. Wenn `expression2` vom Typ `Int`ist, `expression3` muss vom Typ `T`sein. Wenn `expression2` vom Typ `Range`ist, `expression3` muss vom Typ `T[]`sein.

Ein Copy-and-Update- `arr w/ idx <- value` Ausdruck erstellt ein neues Array, bei dem alle Elemente auf das entsprechende `arr`Element in festgelegt sind, mit Ausnahme der `idx`Elemente in, die auf die 1 (n) in `value`festgelegt sind. Wenn `arr` z. b. ein Array `[0,1,2,3]`enthält, dann 
- `arr w/ 0 <- 10`ist das Array `[10,1,2,3]`.
- `arr w/ 2 <- 10`ist das Array `[0,1,10,3]`.
- `arr w/ 0..2..3 <- [10,12]`ist das Array `[10,1,12,3]`.

Ähnliche Ausdrücke sind für benannte Elemente in benutzerdefinierten Typen vorhanden. Beachten Sie beispielsweise den-Typ. 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Wenn `c` den `Complex(1.,-1.)`Wert des Typs enthält, dann `c w/ Re <- 0.` ist ein Ausdruck vom Typ `Complex` , der ergibt `Complex(0.,-1.)`.

## <a name="conditional-expressions"></a>Bedingte Ausdrücke

Bei zwei anderen Ausdrücken desselben Typs und eines booleschen Ausdrucks kann der bedingte Ausdruck mit dem Fragezeichen `?` und dem senkrechten Strich `|`gebildet werden.
Beispielsweise `a==b ? c | d`.
In diesem Beispiel ist der Wert des bedingten Ausdrucks, `c` Wenn `a==b` den Wert true hat und `d` wenn der Wert false ist.

Die beiden Ausdrücke können zu Vorgängen ausgewertet werden, die über die gleichen Eingaben und Ausgaben verfügen, aber unterschiedliche Funktions tüktoren unterstützen.
In diesem Fall ist der Typ des bedingten Ausdrucks ein Vorgang mit diesen Eingaben und Ausgaben, der alle von beiden Ausdrücken unterstützten Funktoren unterstützt.
Wenn `Op1`z. b. `Op2`, und `Op3` alle sind `Qubit[]=>Unit`, `Op1` `Adjoint` `Op2` `Controlled`unterstützt, unterstützt und `Op3` unterstützt jedoch beide:

- `flag ? Op1 | Op2`ist ein `(Qubit[] => Unit)` -Vorgang.
- `flag ? Op1 | Op3`ist ein `(Qubit[] => Unit is Adj)` -Vorgang.
- `flag ? Op2 | Op3`ist ein `(Qubit[] => Unit is Ctl)` -Vorgang.

Wenn einer der beiden möglichen Ergebnis Ausdrücke einen Funktions-oder einen Vorgangs aufzurufen enthält, findet dieser Vorgang nur statt, wenn das Ergebnis das Ergebnis ist, das der Wert des Aufrufes ist.
`a==b ? C(qs) | D(qs)`Wenn `a==b` beispielsweise true ist, wird der `C` Vorgang aufgerufen, und wenn false ist, wird nur `D` aufgerufen.
Dies ähnelt der Kurzschluss in anderen Sprachen.


## <a name="operator-precedence"></a>Operatorrangfolge

Alle binären Operatoren sind mit Ausnahme von `^`rechts assoziativ.

Eckige Klammern `[` und `]`, für das Aufteilen von Arrays und Indizierung, binden vor jedem Operator.

Die Funktoren `Adjoint` und `Controlled` die Bindung nach der Array Indizierung, aber vor allen anderen Operatoren.

Klammern für Vorgangs-und Funktionsaufrufe werden auch vor jedem Operator gebunden, aber nach der Array Indizierung und den Funktoren.

Operatoren in Rangfolge, vom höchsten zum niedrigsten:

Operator | Ständigkeit | BESCHREIBUNG | Operanden Typen
---------|----------|---------|---------------
 nachträ`!` | Unär | Aufheben der Umschließung | Ein beliebiger benutzerdefinierter Typ
 `-`, `~~~`, `not` | Unär | Numerische negative, bitweise Komplement logische Negation | `Int`, `BigInt` oder `Double` für `-` `Int` `Bool` , für `BigInt` `~~~``not`
 `^` | Binary | Ganzzahlige Potenz | `Int`oder `BigInt` für die Basisklasse `Int` für den Exponenten
 `/`, `*`, `%` | Binary | Division, Multiplikation, ganzzahliger Modulo | `Int`, `BigInt` oder `Double` für `/` und `*` `Int` oder `BigInt` für`%`
 `+`, `-` | Binary | Addition oder Zeichenfolge und Array Verkettung, Subtraktion | `Int`, `BigInt` oder `Double`, zusätzlich `String` oder ein beliebiger Arraytyp für`+`
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
