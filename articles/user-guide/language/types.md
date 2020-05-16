---
title: 'Typen in Q #'
description: 'Erfahren Sie mehr über die verschiedenen Typen, die in der Programmiersprache Q # verwendet werden.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: 58370193bd62e306197a9e07c28f8611f043e55c
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431137"
---
# <a name="types-in-q"></a>Typen in Q #

Auf dieser Seite wird das Q #-Typmodell und die Syntax zum Angeben von und arbeiten mit Typen beschrieben.
Auf der nächsten Seite, [typausdrücke](xref:microsoft.quantum.guide.expressions), wird erläutert, wie Ausdrücke dieser Typen erstellt und verwendet werden.

Beachten Sie, dass Q # eine *stark typisierte* Sprache ist, sodass der Compiler durch eine sorgfältige Verwendung dieser Typen bei der Kompilierung starke Garantien für Q #-Programme bereitstellen kann.
Um die bestmögliche Garantie bereitzustellen, müssen Konvertierungen zwischen Typen in Q # explizit mithilfe von Aufrufen von Funktionen erfolgen, die diese Konvertierung Ausdrücken. Eine Vielzahl solcher Funktionen werden als Teil des- <xref:microsoft.quantum.convert> Namespace bereitgestellt.
Auf der anderen Seite werden Upcasts zu kompatiblen Typen implizit durchgeführt. 

Q # stellt beide primitiven Typen bereit, die direkt verwendet werden können, und eine Vielzahl von Möglichkeiten, um neue Typen aus anderen Typen zu entwickeln.
Diese werden im restlichen Teil dieses Abschnitts beschrieben.

## <a name="primitive-types"></a>Primitive Typen

Die Sprache Q # stellt mehrere *primitive Typen*bereit, von denen andere Typen erstellt werden können:

- Der- `Int` Typ stellt eine 64-Bit-Ganzzahl mit Vorzeichen dar, z. b.: `2` , `107` , `-5` .
- Der- `BigInt` Typ stellt eine Ganzzahl mit Vorzeichen beliebiger Größe dar, z. b., `2L` `107L` , `-5L` .
   Dieser Typ basiert auf .net.<xref:System.Numerics.BigInteger>
   Sorte.
- Der `Double` -Typ stellt eine Gleit Komma Zahl mit doppelter Genauigkeit dar, z. b.: `0.0` , `-1.3` , `4e-7` .
- Der- `Bool` Typ stellt einen booleschen Wert dar, der entweder oder sein kann `true` `false` .
- Der- `Range` Typ stellt eine Sequenz von ganzen Zahlen dar, die durch angegeben wird, `start..step..stop` wobei der Schritt "Options" ist. 
   Dies `start .. stop` entspricht `start..1..stop` , und stellt z. b. `1..2..7` die Sequenz $ \{ 1, 3, 5, 7 \} $ dar.
- Der- `String` Typ ist eine Sequenz von Unicode-Zeichen, die für den Benutzer nach der Erstellung nicht transparent ist.
  Dieser Typ wird verwendet, um Nachrichten an einen klassischen Host zu melden, wenn ein Fehler oder ein Diagnose Ereignis vorliegt.
- Der `Unit` Typ ist der Typ, der nur einen Wert zulässt `()` . 
  Dieser Typ wird verwendet, um anzugeben, dass die Q #-Funktion oder der-Vorgang keine Informationen zurückgibt. 
- Der- `Qubit` Typ stellt ein Quantum-Bit oder Qubit dar.
   `Qubit`e sind für den Benutzer nicht transparent. der einzige Vorgang, der mit Ihnen möglich ist, und nicht an einen anderen Vorgang zu übergeben, besteht darin, auf Identity (Gleichheit) zu testen.
   Letztendlich werden Aktionen für `Qubit` s implementiert, indem systeminterne Anweisungen für einen Quantum-Prozessor (oder eine Simulation) aufgerufen werden.
- Der- `Pauli` Typ stellt einen der vier Single-Qubit-Pauli-Operatoren dar.
   Dieser Typ wird verwendet, um den Basis Vorgang für Drehungen anzugeben und um die zu messende Observable anzugeben.
   Dies ist ein enumerierter Typ, der über vier mögliche Werte verfügt: `PauliI` , `PauliX` , `PauliY` und `PauliZ` , bei denen es sich um Konstanten des Typs handelt `Pauli` .
- Der- `Result` Typ stellt das Ergebnis einer Messung dar.
   Dabei handelt es sich um einen enumerierten Typ mit zwei möglichen Werten: und, bei denen es sich um `One` `Zero` Konstanten vom Typ handelt `Result` .
   `Zero`Gibt an, dass der Eigen Wert + 1 gemessen wurde. `One`gibt den eigen Wert-1 an.

Die Konstanten `true` , `false` , `PauliI` ,,, `PauliX` `PauliY` `PauliZ` , `One` und `Zero` sind reservierte Symbole in Q #.

## <a name="array-types"></a>Array Typen

Bei jedem gültigen Q #-Typ `'T` gibt es einen Typ, der ein Array von Werten vom Typ darstellt `'T` .
Dieser Arraytyp wird als dargestellt `'T[]` , z `Qubit[]` . b `Int[][]` . oder.
Beispielsweise ist eine Auflistung von ganzen Zahlen gekennzeichnet `Int[]` , während ein Array von `(Bool, Pauli)` Werten mit Werten gekennzeichnet wird `(Bool, Pauli)[][]` .

Beachten Sie im zweiten Beispiel, dass dies eine potenziell Jagged Array von Arrays und kein rechteckiges zweidimensionales Array darstellt.
Q # bietet keine Unterstützung für rechteckige mehrdimensionale Arrays.

Ein Arraywert kann in Q #-Quellcode mithilfe von eckigen Klammern um die Elemente eines Arrays geschrieben werden, wie in `[PauliI, PauliX, PauliY, PauliZ]` .
Der Typ eines Arrayliterals hängt von dem allgemeinen Basistyp aller Elemente im Array ab. 

> [!WARNING]
> Die Elemente eines Arrays können nicht geändert werden, nachdem das Array erstellt wurde.
> Die [Anweisungen Update-und-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) und/oder [Copy-und-Update-Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) können zum Erstellen eines geänderten Arrays verwendet werden.

Alternativ kann ein Array mit dem-Schlüsselwort aus seiner Größe erstellt werden `new` :

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

In beiden Fällen kann die Core-Funktion `Length` verwendet werden, um die Anzahl von Elementen als zu erhalten, sobald ein Array erstellt wurde `Int` .
Arrays können mithilfe von eckigen Klammern, wobei es sich `Int` um einen Typ oder einen Typ handelt, abonniert werden, `Range` um entweder einzelne Elemente oder neue Arrays zu erhalten, die eine Teilmenge der Elemente eines Arrays enthalten.
Die Indizes von Arrays sind NULL basiert:

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a>Tupeltypen

Wenn 0 (null) oder mehr unterschiedliche Typen `T0` , `T1` ,..., `Tn` , kann ein neuer *tupeltyp* als bezeichnet werden `(T0, T1, ..., Tn)` .
Die Typen, die zum Erstellen eines neuen tupeltyps verwendet werden, können selbst Tupel sein, wie in `(Int, (Qubit, Qubit))` .
Eine solche Schachtelung ist jedoch immer begrenzt, da Tupeltypen unter keinen Umständen selbst enthalten.

Werte des neuen tupeltyps sind Tupel, die durch Sequenz von Werten aus jedem Typ im Tupel gebildet werden.
Beispielsweise `(3, false)` ist ein Tupel, dessen Typ der tupeltyp ist `(Int, Bool)` .
Es ist möglich, Arrays von Tupeln, Tupeln von Arrays, Tupeln von subtupeln usw. zu erstellen.

Ab Q # 0,3 `Unit` ist der Name des *Typs* des leeren Tupels; `()` wird für den leeren *tupelwert*verwendet.

Tupelinstanzen sind unveränderlich.
Q # stellt keinen Mechanismus zum Ändern des Inhalts eines Tupels bereit, nachdem er erstellt wurde.

Tupel sind ein leistungsfähiges Konzept, das in Q # verwendet wird, um Werte in einem einzelnen Wert zusammenzufassen, sodass Sie einfacher zu übergeben sind.
Insbesondere mithilfe von tupelnotation können wir ausdrücken, dass jeder Vorgang und Callable genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt.

### <a name="singleton-tuple-equivalence"></a>Äquivalenz für Singleton-Tupel

Es ist möglich, ein Singleton-Tupel (Einzelelement) zu erstellen, `('T1)` z `(5)` . b `([1,2,3])` . oder.
Q # behandelt jedoch ein Singleton-Tupel als vollständig Äquivalent zu einem Wert des eingeschlossenen Typs.
Das heißt, es gibt keinen Unterschied zwischen `5` und `(5)` bzw `5` . zwischen und `(((5)))` oder zwischen `(5, (6))` und `(5, 6)` .
Es ist ebenso gültig, wie geschrieben zu `(5)+3` werden, um zu schreiben `5+3` , und beide Ausdrücke werden in ausgewertet `8` .

Diese Äquivalenz gilt für alle Zwecke, einschließlich Zuweisung und Ausdrücke.
Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.
Beispielsweise `(7)` ist ein `Int` Ausdruck, `([1,2,3])` ist ein Ausdruck vom Typ Array von `Int` s, und `((1,2))` ist ein Ausdruck vom Typ `(Int, Int)` .

Dies bedeutet insbesondere, dass ein Vorgang oder eine Funktion, deren Eingabetyp oder Ausgabetyp ein Feld hat, sich als ein einzelnes Argument oder einen einzelnen Wert vorstellen kann.

Diese Eigenschaft wird als Übereinstimmung mit einem _Singleton-Tupel_bezeichnet.


## <a name="user-defined-types"></a>Benutzerdefinierte Typen

Eine benutzerdefinierte Typdeklaration besteht aus dem Schlüsselwort `newtype` , gefolgt vom Namen des benutzerdefinierten Typs, einer `=` , einer gültigen Typspezifikation und einem abschließenden Semikolon.

Zum Beispiel:

```qsharp
newtype PairOfInts = (Int, Int);
```

Jede f #-Quelldatei kann eine beliebige Anzahl benutzerdefinierter Typen deklarieren.
Typnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-und Funktionsnamen in Konflikt stehen.

Benutzerdefinierte Typen sind unterschiedlich, auch wenn die Basis Typen identisch sind.
Insbesondere, wenn die zugrunde liegenden Typen identisch sind, gibt es keine automatische Konvertierung zwischen Werten von zwei benutzerdefinierten Typen.

### <a name="named-vs-anonymous-items"></a>Benannte und anonyme Elemente

Eine Q #-Datei kann einen neuen benannten Typ definieren, der einen einzelnen Wert eines beliebigen Typs enthält.
Für jeden tupeltyp `T` können wir einen neuen benutzerdefinierten Typ deklarieren, bei dem es sich um einen Untertyp von `T` mit der- `newtype` Anweisung handelt.
Im- @"microsoft.quantum.math" Namespace sind komplexe Zahlen beispielsweise als benutzerdefinierter Typ definiert:

```qsharp
newtype Complex = (Double, Double);
```
Diese Anweisung erstellt einen neuen Typ mit zwei anonymen Elementen vom Typ `Double` .   

Abgesehen von anonymen Elementen unterstützen benutzerdefinierte Typen auch *benannte Elemente* ab Q # Version 0,7 oder höher. Beispielsweise könnten wir den in Elemente `Re` für das Double benennen, das den Realteil einer komplexen Zahl und `Im` für den imaginären Teil darstellt: 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Das Benennen eines Elements in einem benutzerdefinierten Typ impliziert nicht, dass alle Elemente benannt werden müssen. eine beliebige Kombination aus benannten und unbenannten Elementen wird unterstützt. Außerdem können innere Elemente ebenfalls benannt werden.
Der Typ `Nested` , wie unten definiert, verfügt über einen zugrunde liegenden Typ `(Double, (Int, String))` , von dem nur das Element des Typs `Int` benannt wird und alle anderen Elemente anonym sind. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

Benannte Elemente haben den Vorteil, dass Sie direkt über den *Zugriffs Operator* darauf zugreifen können `::` . 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

Zusätzlich zur Bereitstellung kurzer Aliase für potenziell komplizierte Tupeltypen ist ein wesentlicher Vorteil der Definition solcher Typen, dass Sie die Absicht eines bestimmten Werts dokumentieren können.
Wenn Sie zum Beispiel zurückkehren `Complex` , können Sie auch 2D-Polarkoordinaten als benutzerdefinierten Typ definieren:

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

Obwohl sowohl `Complex` als auch `Polar` beide über einen zugrunde liegenden Typ verfügen `(Double, Double)` , sind die beiden Typen in f # vollständig inkompatibel. Dadurch wird das Risiko minimiert, dass versehentlich eine komplexe mathematische Funktion mit Polarkoordinaten aufgerufen wird und umgekehrt.
Auf diese Weise haben benutzerdefinierte Typen eine ähnliche Rolle wie Datensätze in F #. 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>Auf anonyme Elemente mit dem Unwrap-Operator zugreifen

Um auf anonyme Elemente zugreifen zu können, muss der umschließende Wert zuerst mithilfe des Postfix-Operators extrahiert werden `!` .
Der Unwrap-Operator () `!` ermöglicht, den in einem benutzerdefinierten Typ enthaltenen Wert zu extrahieren.
Der Typ eines solchen "Unwrap"-Ausdrucks ist der zugrunde liegende Typ des benutzerdefinierten Typs. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

Der Unwrap-Operator entpackt genau eine Ebene der Umbruch.
Mehrere Unwrap-Operatoren können verwendet werden, um auf einen multipliziert-umschließenden Wert zuzugreifen.

Beispiel:

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

Weitere Informationen zum Unwrap-Operator finden Sie unter [typanexpressions in f #](xref:microsoft.quantum.guide.expressions).

### <a name="creating-values-of-user-defined-types"></a>Erstellen von Werten für benutzerdefinierte Typen

Werte eines benutzerdefinierten Typs können erstellt werden, indem der entsprechende Typkonstruktor aufgerufen wird:

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

Alternativ können neue Werte mithilfe von [Ausdrücken zum Kopieren und aktualisieren](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)aus vorhandenen erstellt werden. Wie bei Arrays Kopieren solche Ausdrücke alle Element Werte des ursprünglichen Ausdrucks, mit Ausnahme der angegebenen benannten Elemente. Für diese werden die Werte auf die Werte festgelegt, die auf der rechten Seite des Ausdrucks definiert sind. Alle anderen Sprachkonstrukte, wie z. b. [Update-und-REASSIGN-Anweisungen](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), die für Array Elemente verfügbar sind, sind auch für benannte Elemente in benutzerdefinierten Typen vorhanden.

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

Benutzerdefinierte Typen können überall dort verwendet werden, wo jeder andere Typ verwendet werden kann.
Insbesondere ist es möglich, ein Array eines benutzerdefinierten Typs zu definieren und einen benutzerdefinierten Typ als Element eines tupeltyps einzuschließen.

Beachten Sie, dass keine rekursiven Typstrukturen erstellt werden können.
Das heißt, der Typ, der einen benutzerdefinierten Typ definiert, darf kein tupeltyp sein, der ein Element des benutzerdefinierten Typs enthält.
Im Allgemeinen haben benutzerdefinierte Typen möglicherweise keine zyklischen Abhängigkeiten, sodass der folgende Satz von Typdefinitionen unzulässig wäre:

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a>Vorgangs-und Funktionstypen

Der Basistyp für alle Aufruf baren wird als `('Tinput => 'Tresult)` oder geschrieben `('Tinput -> 'Tresult)` , wobei sowohl als `'Tinput` auch- `'Tresult` Typen sind.
Diese werden als *Signatur* der aufrufenden bezeichnet.

Alle f #-callables werden als Eingabe betrachtet und geben einen einzelnen Wert als Ausgabe zurück.
Sowohl der Eingabe-als auch der Ausgabewert können Tupel sein.
Callables ohne Ergebnis Rückgabe `Unit` .
Callables ohne Eingabe nehmen das leere Tupel als Eingabe auf.

> [!NOTE]
> Das erste Formular, mit `=>` wird für-Vorgänge verwendet, das zweite Formular, mit `->` für-Funktionen.
> `((Qubit, Pauli) => Result)`Stellt z. b. die Signatur für einen möglichen Single-Qubit-Messvorgang dar.
*Funktions* Typen werden vollständig durch ihre Signatur angegeben.
Eine Funktion, die den Sinus eines Winkels berechnet, hätte z. b. den Typ `(Double -> Double)` .

*Vorgänge*---, aber keine Funktionen---bestimmte zusätzliche Merkmale aufweisen, die als Teil des Vorgangs Typs ausgedrückt werden. Zu diesen Merkmalen zählen Informationen darüber, welche Funktions *tüktoren* der Vorgang unterstützt.
Wenn die Ausführung des Vorgangs z. b. auf den Zustand anderer Qubits bedingt sein kann, sollte er das `Controlled` Funktor unterstützen. wenn der Vorgang eine Umkehrung hat, sollte er das `Adjoint` Funktor unterstützen. Funktoren und Vorgänge werden ausführlich unter [Vorgänge und Funktionen in Q #](xref:microsoft.quantum.guide.operationsfunctions)erläutert, aber hier wird einfach erläutert, wie dies die Vorgangs Signatur verändert.

Um Unterstützung für den `Controlled` -und/oder- `Adjoint` Funktions tüktor in einem Vorgangstyp zu benötigen, müssen Sie eine Anmerkung hinzufügen, die die entsprechenden Merkmale angibt.
Eine Anmerkung `is Ctl` (z. b `(Qubit => Unit is Ctl)` .) gibt an, dass der Vorgang steuerbar ist---d. h., die Ausführung ist für den Zustand eines anderen Qubit oder Qubits bedingt. Analog dazu `is Adj` gibt an, dass der Vorgang über ein Adjoint verfügt, oder einfach, dass er "invertiert" werden kann, sodass das Fortsetzen eines Vorgangs und dessen Adjoint auf einen Zustand den Zustand unverändert lässt. 

Wenn Sie festlegen möchten, dass ein Vorgang dieses Typs sowohl das-als `Adjoint` auch das-Funktor unterstützt, `Controlled` können wir dies als Ausdrücken `(Qubit => Unit is Adj + Ctl)` . Der integrierte Pauli- <xref:microsoft.quantum.intrinsic.x> Vorgang hat z. b. den-Typ `(Qubit => Unit is Adj + Ctl)` . 

Ein Vorgangstyp, der keine Funktions tüktoren unterstützt, wird von seinem Eingabe-und Ausgabetyp allein angegeben, ohne dass zusätzliche Anmerkungen vorhanden sind.

### <a name="type-parameterized-functions-and-operations"></a>Typparametrisierte Funktionen und Vorgänge

Aufruf Bare Typen können Typparameter enthalten.
Typparameter werden durch ein Symbol angegeben, das ein einzelnes Anführungszeichen als Präfix hat. beispielsweise `'A` ist ein gültiger Typparameter.
Details zum Definieren von parametrisierten typparametrisierten aufrufen finden Sie auf der Seite [Vorgänge und Funktionen in f #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .

Ein Typparameter kann in einer einzigen Signatur mehrmals vorkommen.
Eine Funktion, die eine andere Funktion auf jedes Element eines Arrays anwendet und die gesammelten Ergebnisse zurückgibt, hätte z. b. eine Signatur `(('A[], 'A->'A) -> 'A[])` .
Ebenso kann eine Funktion, die die Komposition von zwei Vorgängen zurückgibt, eine Signatur aufweisen `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .

Beim Aufrufen eines typparametrisierten Aufruf baren Typs müssen alle Argumente, die denselben Typparameter aufweisen, denselben Typ aufweisen.

Q # stellt keinen Mechanismus zum Einschränken der möglichen Typen bereit, die durch einen Typparameter ersetzt werden könnten.

## <a name="whats-next"></a>Wie geht es weiter?
Nachdem Sie alle Typen gesehen haben, die die Q #-Sprache bilden, können Sie [in q # Ausdrücke eingeben](xref:microsoft.quantum.guide.expressions) , um zu erfahren, wie Sie Ausdrücke dieser verschiedenen Typen erstellen und bearbeiten.


