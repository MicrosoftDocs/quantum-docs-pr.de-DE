---
title: Typen in Q#
description: Erfahren Sie mehr über die verschiedenen Typen, die in der Q# Programmiersprache verwendet werden.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- Q#
- $$v
ms.openlocfilehash: c4a3e6563b8cabee87d1db6b9cb1c1f1c1a7131b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835824"
---
# <a name="types-in-no-locq"></a>Typen in Q#

In diesem Artikel werden das Q# Typmodell und die Syntax zum Angeben von und arbeiten mit Typen beschrieben. Ausführliche Informationen zum Erstellen und Verarbeiten von Ausdrücken dieser Typen finden Sie unter [typausdrücke](xref:microsoft.quantum.guide.expressions).

Beachten Sie, dass Q# eine *stark typisierte* Sprache ist, sodass der Compiler durch eine sorgfältige Verwendung dieser Typen bei der Kompilierung starke Garantien für Programme bereitstellen kann Q# .
Um die bestmöglichen Garantien zu gewährleisten, müssen Konvertierungen zwischen Typen in Q# explizit mithilfe von Aufrufen von Funktionen erfolgen, die diese Konvertierung Ausdrücken. 
Q# stellt eine Vielzahl solcher Funktionen als Teil des- <xref:microsoft.quantum.convert> Namespace bereit.
Auf der anderen Seite werden Upcasts in kompatible Typen implizit durchgeführt. 

Q# stellt beide primitiven Typen bereit, die direkt verwendet werden, und eine Vielzahl von Möglichkeiten, um neue Typen aus anderen Typen zu entwickeln.
Wir beschreiben alle in den restlichen Abschnitten dieses Artikels.

## <a name="primitive-types"></a>Primitive Typen

Die Q# Sprache stellt die folgenden *primitiven Typen*bereit, die Sie alle direkt in Programmen verwenden können Q# . Sie können diese primitiven Typen auch verwenden, um neue Typen zu erstellen.

- Der- `Int` Typ stellt eine 64-Bit-Ganzzahl mit Vorzeichen dar, z `2` . b., `107` , `-5` .
- Der- `BigInt` Typ stellt eine Ganzzahl mit Vorzeichen beliebiger Größe dar, z `2L` . b., `107L` , `-5L` .
   Dieser Typ basiert auf .net. <xref:System.Numerics.BigInteger>
   umgewandelt.

- Der `Double` -Typ stellt eine Gleit Komma Zahl mit doppelter Genauigkeit dar, z `0.0` . b `-1.3` .,, `4e-7` .
- Der- `Bool` Typ stellt einen booleschen Wert von `true` oder dar `false` .
- Der- `Range` Typ stellt eine Sequenz von ganzen Zahlen dar, die durch angegeben wird, `start..step..stop` wobei der Schritt optional ist. 
   Beispielsweise `start .. stop` entspricht `start..1..stop` , und `1..2..7` stellt die Sequenz $ \{ 1, 3, 5, 7 $ dar \} .
- Der- `String` Typ ist eine Sequenz von Unicode-Zeichen, die für den Benutzer nach der Erstellung nicht transparent ist.
  Verwenden Sie den- `string` Typ, um Meldungen bei einem Fehler oder einem Diagnose Ereignis an einen klassischen Host zu melden.
- Der- `Unit` Typ kann nur einen Wert,, aufweisen `()` . 
  Verwenden Sie diesen Typ, um anzugeben, dass eine Q# Funktion oder ein Vorgang keine Informationen zurückgibt. 
- Der- `Qubit` Typ stellt ein Quantum-Bit oder Qubit dar.
   `Qubit`e sind für den Benutzer nicht transparent. Der einzige Vorgang, der mit Ihnen möglich ist, und nicht an einen anderen Vorgang zu übergeben, besteht darin, auf Identity (Gleichheit) zu testen.
   Letztendlich implementieren Sie Aktionen in, indem Sie systeminterne `Qubit` Anweisungen für einen Quantum-Prozessor (oder einen Quantum-Simulator) aufrufen.
- Der- `Pauli` Typ stellt einen der vier Single-Qubit-Pauli-Operatoren dar.
   Verwenden Sie diesen Typ, um den Basis Vorgang für Drehungen anzugeben und um die zu messende Observable anzugeben.
   Dabei handelt es sich um einen enumerierten Typ, der über vier mögliche Werte verfügt: `PauliI` , `PauliX` , `PauliY` und `PauliZ` , bei denen es sich um Konstanten des Typs handelt `Pauli` .
- Der- `Result` Typ stellt das Ergebnis einer Messung dar.
   Dabei handelt es sich um einen enumerierten Typ mit zwei möglichen Werten: und, bei denen es sich um `One` `Zero` Konstanten vom Typ handelt `Result` .
   `Zero` Gibt an, dass der Eigen Wert + 1 gemessen wurde. Gibt an, dass `One` der Eigen Wert-1 gemessen wurde.

Die Konstanten `true` , `false` , `PauliI` ,,, `PauliX` `PauliY` `PauliZ` , `One` und `Zero` sind reservierte Symbole in Q# .

## <a name="array-types"></a>Arraytypen

* Für jeden gültigen Q# Typ gibt es einen Typ, der ein Array von Werten dieses Typs darstellt.
    Beispielsweise `Qubit[]` stellen und Werte `(Bool, Pauli)[]` Arrays `Qubit` und `(Bool, Pauli)` Tupelwerte dar.

* Ein Array von Arrays ist ebenfalls gültig. Im vorherigen Beispiel wird ein Array von `(Bool, Pauli)` Arrays bezeichnet `(Bool, Pauli)[][]` .

> [!NOTE] 
> Dieses Beispiel `(Bool, Pauli)[][]` stellt eine potenziell Jagged Array von Arrays und kein rechteckiges zweidimensionales Array dar. Q# unterstützt keine rechteckigen mehrdimensionalen Arrays.

* Ein Arraywert kann im Q# Quellcode mithilfe von eckigen Klammern um die Elemente eines Arrays geschrieben werden, wie in `[PauliI, PauliX, PauliY, PauliZ]` .
Der allgemeine Basistyp aller Elemente im Array bestimmt den Typ eines Arrayliterals. Daher löst das Erstellen eines Arrays mit Elementen, die keinen gemeinsamen Basistyp aufweisen, einen Fehler aus.  
Ein Beispiel finden Sie unter [Arrays von callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).

    > [!WARNING]
    > Nachdem die Elemente eines Arrays erstellt wurden, können Sie nicht mehr geändert werden.
    > Verwenden Sie zum Erstellen eines geänderten Arrays die [Anweisungen Update-und-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) oder [Copy-and-Update-Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).

* Alternativ kann ein Array mit dem-Schlüsselwort aus seiner Größe erstellt werden `new` :

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* Verwenden Sie die Core-Funktion `Length` , um die Anzahl der Elemente aus einem Array als abzurufen `Int` .
* Arrays können abonniert werden, um entweder einzelne Elemente oder neue Arrays zu erhalten, die eine Teilmenge der Elemente eines Arrays enthalten.
Die Indexwerte von Arrays sind NULL basiert und müssen vom Typ `Int` oder vom Typ sein `Range` :

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a>Tupeltypen

Tupel sind ein leistungsstarkes Konzept, das in der gesamten verwendet wird Q# , um Werte in einem einzelnen Wert zusammenzufassen, sodass es einfacher ist, Sie zu übergeben.
Insbesondere mithilfe von tupelnotation können Sie Ausdrücken, dass jeder Vorgang und Callable genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt.

* Wenn 0 (null) oder mehr unterschiedliche Typen,,..., angezeigt wird, `T0` `T1` `Tn` können Sie einen neuen  *tupeltyp* als angeben `(T0, T1, ..., Tn)` .
Die Typen, die zum Erstellen eines neuen tupeltyps verwendet werden, können selbst Tupel sein, wie in `(Int, (Qubit, Qubit))` .
Eine solche Schachtelung ist jedoch immer begrenzt, da Tupeltypen unter keinen Umständen selbst enthalten.

* Die Werte des neuen tupeltyps sind Tupel, die durch Sequenz von Werten aus jedem Typ im Tupel gebildet werden.
Beispielsweise `(3, false)` ist ein Tupel, dessen Typ der tupeltyp ist `(Int, Bool)` .
Es ist möglich, Arrays von Tupeln, Tupeln von Arrays, Tupeln von subtupeln usw. zu erstellen.

* Ab Q# 0,3 ist `Unit` der Name des *Typs* des leeren Tupels; `()` wird für den *Wert* des leeren Tupels verwendet.

* Tupelinstanzen sind unveränderlich.
Q# bietet keinen Mechanismus zum Ändern des Inhalts eines Tupels, nachdem er erstellt wurde.



### <a name="singleton-tuple-equivalence"></a>Äquivalenz für Singleton-Tupel

Es ist möglich, ein Singleton-Tupel (Einzelelement) zu erstellen `('T1)` , z `(5)` `([1,2,3])` . b. oder.
Behandelt jedoch Q# ein Singleton-Tupel als äquivalent zu einem Wert des eingeschlossenen Typs.
Das heißt, es gibt keinen Unterschied zwischen `5` und `(5)` bzw `5` . zwischen und `(((5)))` oder zwischen `(5, (6))` und `(5, 6)` .
Es ist ebenso gültig, wie geschrieben zu werden, `(5)+3` da `5+3` beide Ausdrücke als ausgewertet werden `8` .

Diese Äquivalenz gilt für alle Zwecke, einschließlich Zuweisung und Ausdrücke.
Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.
Beispielsweise `(7)` ist ein Ausdruck vom Typ `Int` , `([1,2,3])` ist ein Ausdruck vom Typ `Int[]` , und `((1,2))` ist ein Ausdruck vom Typ `(Int, Int)` .

Dies bedeutet insbesondere, dass Sie einen Vorgang oder eine Funktion anzeigen können, deren Eingabe-Tupel oder ausgabetupeltyp ein Feld hat, das ein einzelnes Argument annimmt oder einen einzelnen Wert zurückgibt.

Diese Eigenschaft wird als Übereinstimmung mit einem _Singleton-Tupel_bezeichnet.


## <a name="user-defined-types"></a>Benutzerdefinierte Typen

Eine benutzerdefinierte Typdeklaration besteht aus dem Schlüsselwort `newtype` , gefolgt vom Namen des benutzerdefinierten Typs, einer `=` , einer gültigen Typspezifikation und einem abschließenden Semikolon.

Zum Beispiel:

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* Jede Q# Quelldatei kann eine beliebige Anzahl benutzerdefinierter Typen deklarieren.
* Typnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-und Funktionsnamen in Konflikt stehen.
* Benutzerdefinierte Typen sind unterschiedlich, auch wenn die Basis Typen identisch sind.
Vor allem gibt es keine automatische Konvertierung zwischen den Werten von zwei benutzerdefinierten Typen, auch wenn die zugrunde liegenden Typen identisch sind.

### <a name="named-vs-anonymous-items"></a>Benannte und anonyme Elemente

Eine Q# Datei kann einen neuen benannten Typ definieren, der einen einzelnen Wert eines beliebigen Typs enthält.
Für jeden tupeltyp `T` können Sie einen neuen benutzerdefinierten Typ deklarieren, bei dem es sich um einen Untertyp von `T` mit der- `newtype` Anweisung handelt.
Im- @"microsoft.quantum.math" Namespace werden z. b. komplexe Zahlen als benutzerdefinierter Typ definiert:

```qsharp
newtype Complex = (Double, Double);
```
Diese Anweisung erstellt einen neuen Typ mit zwei anonymen Elementen vom Typ `Double` .   

Abgesehen von anonymen Elementen unterstützen benutzerdefinierte Typen auch *benannte Elemente* ab Q# Version 0,7 oder höher. Beispielsweise können Sie die Elemente `Real` für das Double benennen, das den Realteil einer komplexen Zahl und `Imag` für den imaginären Teil darstellt: 

```qsharp
newtype Complex = (Real : Double, Imag : Double);
```
Das Benennen eines Elements in einem benutzerdefinierten Typ impliziert nicht, dass alle Elemente benannt werden müssen. eine beliebige Kombination aus benannten und unbenannten Elementen wird unterstützt. Außerdem können innere Elemente ebenfalls benannt werden.
Der Typ `Nested` , wie unten definiert, verfügt beispielsweise über einen zugrunde liegenden Typ `(Double, (Int, String))` , von dem nur das Element des Typs `Int` benannt wird und alle anderen Elemente anonym sind. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

Benannte Elemente haben den Vorteil, dass Sie direkt über den *Zugriffs Operator* darauf zugreifen können `::` . 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Real + c2::Real, c1::Imag + c2::Imag);
}
```

Zusätzlich zur Bereitstellung kurzer Aliase für potenziell komplizierte Tupeltypen ist ein wichtiger Vorteil beim Definieren solcher Typen, dass Sie die Absicht eines bestimmten Werts dokumentieren können.
Wenn Sie zum Beispiel zurückkehren `Complex` , können Sie auch eine Polar Koordinate-Neudarstellung als benutzerdefinierten Typ definieren:

```qsharp
newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```

Obwohl sowohl `Complex` als auch `ComplexPolar` beide über einen zugrunde liegenden Typ verfügen `(Double, Double)` , sind die beiden Typen in vollständig inkompatibel Q# , wodurch das Risiko minimiert wird, dass versehentlich eine komplexe mathematische Funktion mit Polarkoordinaten aufgerufen wird und umgekehrt.

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a>Auf anonyme Elemente mit dem Unwrap-Operator zugreifen

Wenn Sie auf anonyme Elemente zugreifen möchten, extrahieren Sie zuerst den umschließenden Wert mithilfe des Postfix-Operators `!` .
Mit dem Operator "Unwrap" `!` können Sie den Wert extrahieren, der in einem benutzerdefinierten Typ enthalten ist.
Der Typ eines solchen "Unwrap"-Ausdrucks ist der zugrunde liegende Typ des benutzerdefinierten Typs. 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

Ein einzelner Unwrap-Operator entpackt eine umschließende Schicht. Verwenden Sie mehrere Unwrap-Operatoren, um auf einen multipliziert umschließenden Wert zuzugreifen.

Zum Beispiel:

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

Weitere Informationen zum Unwrap-Operator finden Sie unter [typausdrücke in Q# ](xref:microsoft.quantum.guide.expressions).

### <a name="creating-values-of-user-defined-types"></a>Erstellen von Werten für benutzerdefinierte Typen

Erstellen Sie Werte eines benutzerdefinierten Typs, indem Sie den entsprechenden Typkonstruktor aufrufen:

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

Alternativ können Sie mithilfe von [Ausdrücken zum Kopieren und aktualisieren](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)neue Werte aus vorhandenen Werten erstellen. Ebenso wie bei Arrays kopieren Copy-und-Update-Ausdrücke alle Element Werte des ursprünglichen Ausdrucks, mit Ausnahme der angegebenen benannten Elemente. Für diese Ausnahmen sind die Werte dieser Elemente die Werte, die auf der rechten Seite des Ausdrucks definiert sind. Alle anderen Sprachkonstrukte, die für Array Elemente verfügbar sind, z. b. [Update-und-REASSIGN-Anweisungen](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), sind auch für benannte Elemente in benutzerdefinierten Typen vorhanden.

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

* Sie können benutzerdefinierte Typen überall dort verwenden, wo Sie beliebige andere Typen verwenden.
Insbesondere ist es möglich, ein Array eines benutzerdefinierten Typs zu definieren und einen benutzerdefinierten Typ als Element eines tupeltyps einzuschließen.

* Es ist nicht möglich, rekursive Typstrukturen zu erstellen.
Das heißt, dass der Typ, der einen benutzerdefinierten Typ definiert, kein tupeltyp sein kann, der ein Element des benutzerdefinierten Typs enthält.
Im Allgemeinen haben benutzerdefinierte Typen möglicherweise keine zyklischen Abhängigkeiten, sodass der folgende Satz von Typdefinitionen ungültig ist:

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a>Vorgangs-und Funktionstypen

Mit den Typen `'Tinput` und `'Tresult` :

* `('Tinput => 'Tresult)` ist der Basistyp für jeden *Vorgang*, z `((Qubit, Pauli) => Result)` . b..
* `('Tinput -> 'Tresult)` ist der Basistyp für jede *Funktion*, z `(Int -> Int)` . b.. 

Diese werden als *Signatur* der aufrufenden bezeichnet.

* Alle Q# callables nehmen einen einzelnen Wert als Eingabe an und geben einen einzelnen Wert als Ausgabe zurück.
* Sie können Tupel sowohl für die Eingabe-als auch für die Ausgabewerte verwenden.
* Callables ohne Ergebnis geben zurück `Unit` .
* Callables ohne Eingabe nehmen das leere Tupel als Eingabe auf.

### <a name="functors"></a>Funktionselemente

*Funktions* Typen werden vollständig durch ihre Signatur angegeben. Eine Funktion, die den Sinus eines Winkels berechnet, hätte z. b. den Typ `(Double -> Double)` . 

*Vorgänge* weisen bestimmte zusätzliche Eigenschaften auf, die als Teil des Vorgangs Typs ausgedrückt werden. Zu diesen Merkmalen zählen Informationen darüber, welche Funktions *tüktoren* der Vorgang unterstützt.
Wenn z. b. die Ausführung des Vorgangs auf dem Zustand anderer Qubits basiert, sollte er das `Controlled` Funktor unterstützen. wenn der Vorgang eine Umkehrung hat, sollte er das `Adjoint` Funktor unterstützen.

> [!NOTE]
> In diesem Artikel wird nur erläutert, wie Funktoren die Vorgangs Signatur ändern. Weitere Informationen zu Funktions tüktoren und Vorgängen finden Sie unter [Vorgänge und Q# Funktionen in ](xref:microsoft.quantum.guide.operationsfunctions). 

Um Unterstützung für den `Controlled` -und/oder- `Adjoint` Funktions tüktor in einem Vorgangstyp zu benötigen, müssen Sie eine Anmerkung hinzufügen, die die entsprechenden Merkmale angibt.
Die-Anmerkung `is Ctl` (z. b. `(Qubit => Unit is Ctl)` ) gibt an, dass der Vorgang steuerbar ist. Das heißt, der Run basiert auf dem Zustand eines anderen Qubit oder Qubits. Entsprechend gibt die-Anmerkung `is Adj` an, dass der Vorgang über ein Adjoint-Zeichen verfügt, d. h., es kann "invertiert" werden, sodass das Fortsetzen eines Vorgangs und dessen Adjoint in einen Zustand den Zustand unverändert lässt. 

Wenn Sie festlegen möchten, dass ein Vorgang dieses Typs sowohl das-als `Adjoint` auch das-Funktor unterstützt, `Controlled` können Sie dies als Ausdrücken `(Qubit => Unit is Adj + Ctl)` . Der integrierte Pauli- <xref:microsoft.quantum.intrinsic.x> Vorgang hat z. b. den-Typ `(Qubit => Unit is Adj + Ctl)` . 

Ein Vorgangstyp, der keine Funktions tüktoren unterstützt, wird von seinem Eingabe-und Ausgabetyp allein angegeben, ohne dass zusätzliche Anmerkungen vorhanden sind.

### <a name="type-parameterized-functions-and-operations"></a>Typparametrisierte Funktionen und Vorgänge

Aufruf Bare Typen können *Typparameter*enthalten.
Verwenden Sie ein Symbol, das mit einem einfachen Anführungszeichen versehen ist, um einen Typparameter anzugeben. beispielsweise `'A` ist ein gültiger Typparameter.
Weitere Informationen und Details zum Definieren von typparametrisierten Aufruf baren aufrufen finden Sie unter [Vorgänge und Funktionen in Q# ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).

Ein Typparameter kann in einer einzigen Signatur mehrmals vorkommen.
Eine Funktion, die eine andere Funktion auf jedes Element eines Arrays anwendet und die gesammelten Ergebnisse zurückgibt, hat z. b. die Signatur `(('A[], 'A->'A) -> 'A[])` .
Ebenso hat eine Funktion, die die Komposition von zwei Vorgängen zurückgibt, die Signatur `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .

Wenn Sie eine typparametrisierte Aufruf Bare Aufruf Liste aufrufen, müssen alle Argumente, die denselben Typparameter aufweisen, denselben Typ aufweisen.

Q# stellt keinen Mechanismus zum Einschränken der möglichen Typen bereit, die ein Benutzer für einen Typparameter ersetzen kann.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie alle Typen gesehen haben, die die Sprache enthalten Q# , finden Sie unter [typausdrücke Q# in](xref:microsoft.quantum.guide.expressions) Informationen zum Erstellen und Bearbeiten von Ausdrücken dieser verschiedenen Typen.
