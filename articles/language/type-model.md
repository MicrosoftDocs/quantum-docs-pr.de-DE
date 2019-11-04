---
title: 'F #-Typmodell | Microsoft-Dokumentation'
description: 'Q #-Typmodell'
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4e251053d1b8306bf8956314d8099e95c56bce55
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184745"
---
# <a name="the-type-model"></a>Das Typmodell

In diesem Abschnitt wird das Q # Type-Modell erläutert und die Syntax zum Angeben von und arbeiten mit Typen beschrieben.
Beachten Sie, dass Q # eine *stark typisierte* Sprache ist, sodass der Compiler durch eine sorgfältige Verwendung dieser Typen bei der Kompilierung starke Garantien für Q #-Programme bereitstellen kann.

Um die bestmögliche Garantie bereitzustellen, müssen Konvertierungen zwischen Typen in Q # explizit mithilfe von Aufrufen von Funktionen erfolgen, die diese Konvertierung Ausdrücken. Eine Vielzahl solcher Funktionen werden als Teil des <xref:microsoft.quantum.convert>-Namespace bereitgestellt.
Auf der anderen Seite werden Upcasts zu kompatiblen Typen implizit durchgeführt. 

Q # stellt beide primitiven Typen bereit, die direkt verwendet werden können, und eine Vielzahl von Möglichkeiten, um neue Typen aus anderen Typen zu entwickeln.
Diese werden im restlichen Teil dieses Abschnitts beschrieben.

## <a name="primitive-types"></a>Primitive Typen

Die Sprache Q # stellt mehrere *primitive Typen*bereit, von denen andere Typen erstellt werden können:

- Der `Int`-Typ stellt eine 64-Bit-Ganzzahl mit Vorzeichen dar, z. b.: `2`, `107`, `-5`.
- Der `BigInt`-Typ stellt eine Ganzzahl mit Vorzeichen beliebiger Größe dar, z. b. `2L`, `107L``-5L`.
   Dieser Typ basiert auf der .net-<xref:System.Numerics.BigInteger>
   Sorte.
- Der `Double`-Typ stellt eine Gleit Komma Zahl mit doppelter Genauigkeit dar, z. b.: `0.0`, `-1.3`, `4e-7`.
- Der `Bool`-Typ stellt einen booleschen Wert dar, der entweder `true` oder `false`sein kann.
- Der `Qubit` Typ stellt ein Quantum-Bit oder ein Qubit dar.
   `Qubit`s sind für den Benutzer nicht transparent. der einzige Vorgang, der mit Ihnen möglich ist, und nicht an einen anderen Vorgang zu übergeben, besteht darin, auf Identity (Gleichheit) zu testen.
   Letztendlich werden Aktionen auf `Qubit`s implementiert, indem systeminterne Anweisungen für einen Quantum-Prozessor (oder eine Simulation) aufgerufen werden.
- Der `Pauli`-Typ stellt einen der vier Single-Qubit-Pauli-Operatoren dar.
   Dieser Typ wird verwendet, um den Basis Vorgang für Drehungen anzugeben und um die zu messende Observable anzugeben.
   Dabei handelt es sich um einen enumerierten Typ, der über vier mögliche Werte verfügt: `PauliI`, `PauliX`, `PauliY`und `PauliZ`, bei denen es sich um Konstanten vom Typ `Pauli`handelt.
- Der `Result` Typ stellt das Ergebnis einer Messung dar.
   Dabei handelt es sich um einen enumerierten Typ mit zwei möglichen Werten: `One` und `Zero`, bei denen es sich um Konstanten vom Typ `Result`handelt.
   `Zero` gibt an, dass der Eigen Wert + 1 gemessen wurde. `One` gibt den eigen Wert-1 an.
- Der `Range`-Typ stellt eine Sequenz von ganzen Zahlen dar, die durch `start.step.stop`bezeichnet wird, wobei der Schritt "Optionen" angibt. 
   Dies ist `start . stop` der `start.1.stop`entspricht, und z. b. `1.2.7` die Sequenz $\{1, 3, 5, 7\}$ darstellt.
- Der `String`-Typ ist eine Sequenz von Unicode-Zeichen, die für den Benutzer nach der Erstellung nicht transparent ist.
  Dieser Typ wird verwendet, um Nachrichten an einen klassischen Host zu melden, wenn ein Fehler oder ein Diagnose Ereignis vorliegt.
- Der `Unit` Typ ist der Typ, der nur einen Wert `()`zulässt. 
  Dieser Typ wird verwendet, um anzugeben, dass die Q #-Funktion oder der-Vorgang keine Informationen zurückgibt. 

Die Konstanten `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`und `Zero` sind alle reservierten Symbole in f #.

## <a name="array-types"></a>Array Typen

Bei jedem gültigen Q #-`'T`gibt es einen Typ, der ein Array von Werten des Typs "`'T`" darstellt.
Dieser Arraytyp wird als `'T[]`dargestellt. beispielsweise `Qubit[]` oder `Int[][]`.
Beispielsweise wird eine Auflistung von ganzen Zahlen als `Int[]`bezeichnet, während ein Array von Arrays mit `(Bool, Pauli)` Werten `(Bool, Pauli)[][]`angegeben wird.

Beachten Sie im zweiten Beispiel, dass dies eine potenziell Jagged Array von Arrays und kein rechteckiges zweidimensionales Array darstellt.
Q # bietet keine Unterstützung für rechteckige mehrdimensionale Arrays.

Ein Arraywert kann in Q #-Quellcode mithilfe von eckigen Klammern um die Elemente eines Arrays geschrieben werden, wie in `[PauliI, PauliX, PauliY, PauliZ]`.
Der Typ eines Arrayliterals hängt von dem allgemeinen Basistyp aller Elemente im Array ab. 

> [!WARNING]
> Die Elemente eines Arrays können nicht geändert werden, nachdem das Array erstellt wurde.
> Die Anweisungen Update-und-REASSIGN und/oder Copy-und-Update-Ausdrücke können zum Erstellen eines geänderten Arrays verwendet werden.

Alternativ kann ein Array mit dem `new`-Schlüsselwort aus seiner Größe erstellt werden:

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

Wenn ein Array erstellt wurde, kann in beiden Fällen die Core-Funktion `Length` zum Abrufen der Anzahl von Elementen als `Int`verwendet werden.
Arrays können mithilfe von eckigen Klammern abonniert werden, wobei entweder der Typ `Int` oder der Typ `Range`ist, um entweder einzelne Elemente oder neue Arrays zu erhalten, die eine Teilmenge der Elemente eines Arrays enthalten.
Die Indizes von Arrays sind NULL basiert:

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a>Tupeltypen

Wenn 0 (null) oder mehr unterschiedliche Typen `T0`, `T1`,..., `Tn`, kann ein neuer *tupeltyp* als `(T0, T1, ..., Tn)`bezeichnet werden.
Die Typen, die zum Erstellen eines neuen tupeltyps verwendet werden, können selbst Tupel sein, wie in `(Int, (Qubit, Qubit))`.
Eine solche Schachtelung ist jedoch immer begrenzt, da Tupeltypen unter keinen Umständen selbst enthalten.

Werte des neuen tupeltyps sind Tupel, die durch Sequenz von Werten aus jedem Typ im Tupel gebildet werden.
`(3, false)` ist beispielsweise ein Tupel, dessen Typ der tupeltyp `(Int, Bool)`ist.
Es ist möglich, Arrays von Tupeln, Tupeln von Arrays, Tupeln von subtupeln usw. zu erstellen.

Ab Q # 0,3 ist `Unit` der Name des *Typs* des leeren Tupels. `()` wird für den leeren *tupelwert*verwendet.

Tupelinstanzen sind unveränderlich.
Q # stellt keinen Mechanismus zum Ändern des Inhalts eines Tupels bereit, nachdem er erstellt wurde.

Tupel sind ein leistungsfähiges Konzept, das in Q # verwendet wird, um Werte in einem einzelnen Wert zusammenzufassen, sodass Sie einfacher zu übergeben sind.
Insbesondere mithilfe von tupelnotation können wir ausdrücken, dass jeder Vorgang und Callable genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt.

### <a name="singleton-tuple-equivalence"></a>Äquivalenz für Singleton-Tupel

Es ist möglich, ein Singleton-Tupel (Single-Element) zu erstellen, `('T1)`, z. b. `(5)` oder `([1,2,3])`.
Q # behandelt jedoch ein Singleton-Tupel als vollständig Äquivalent zu einem Wert des eingeschlossenen Typs.
Das heißt, es gibt keinen Unterschied zwischen `5` und `(5)`bzw. zwischen `5` und `(((5)))`oder zwischen `(5, (6))` und `(5, 6)`.

Diese Äquivalenz gilt für alle Zwecke, einschließlich Zuweisung und Ausdrücke.
Es ist ebenso gültig, `(5)+3` als zu schreiben, um `5+3`zu schreiben, und beide Ausdrücke werden zu `8`ausgewertet.
Dies bedeutet insbesondere, dass ein Vorgang oder eine Funktion, deren Eingabetyp oder Ausgabetyp ein Feld hat, sich als ein einzelnes Argument oder einen einzelnen Wert vorstellen kann.

Diese Eigenschaft wird als Übereinstimmung mit einem _Singleton-Tupel_bezeichnet.

## <a name="user-defined-types"></a>Benutzerdefinierte Typen

Eine Q #-Datei kann einen neuen benannten Typ definieren, der einen einzelnen Wert eines beliebigen Typs enthält.
Für jeden tupeltyp `T`können wir einen neuen benutzerdefinierten Typ deklarieren, bei dem es sich um einen Untertyp von `T` mit der `newtype`-Anweisung handelt.
Im @"microsoft.quantum.canon" Namespace sind komplexe Zahlen beispielsweise als benutzerdefinierter Typ definiert:

```qsharp
newtype Complex = (Double, Double);
```

Mit dieser Anweisung wird ein neuer Typ mit zwei anonymen Elementen vom Typ "`Double`" erstellt.   
Abgesehen von anonymen Elementen unterstützen benutzerdefinierte Typen auch benannte Elemente ab Q # Version 0,7 oder höher. Beispielsweise könnten wir den `Re` für das Double benennen, das den Realteil einer komplexen Zahl darstellt, und `Im` für den imaginären Teil: 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
Das Benennen eines Elements in einem benutzerdefinierten Typ impliziert nicht, dass alle Elemente benannt werden müssen. eine beliebige Kombination aus benannten und unbenannten Elementen wird unterstützt. Darüber hinaus können auch innere Elemente benannt werden.
Der Typ `Nested`, wie unten definiert, verfügt über einen zugrunde liegenden Typ `(Double, (Int, String))`, von dem nur das Element des Typs `Int` benannt wird und alle anderen Elemente anonym sind. 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
Benannte Elemente haben den Vorteil, dass direkt über den Zugriffs Operator `::`auf Sie zugegriffen werden kann. 

```qsharp
function Addition (c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

Um auf anonyme Elemente zugreifen zu können, muss der umschließende Wert zuerst mithilfe des Postfix-Operators `!`extrahiert werden.
Der Unwrap-Operator (`!`) ermöglicht das Extrahieren des Werts, der in einem benutzerdefinierten Typ enthalten ist.
Der Typ eines solchen "Unwrap"-Ausdrucks ist der zugrunde liegende Typ des benutzerdefinierten Typs. 

```qsharp
function PrintMsg (value : Nested) : Unit {
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

Weitere Informationen finden Sie im Abschnitt über die [Unwrap-Ausdrücke](xref:microsoft.quantum.language.expressions#unwrap-expressions) und die [Operatorrangfolge](xref:microsoft.quantum.language.expressions#operator-precedence) .

Werte eines benutzerdefinierten Typs können erstellt werden, indem der entsprechende Typkonstruktor aufgerufen wird:

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

Alternativ können neue Werte mithilfe von [Ausdrücken zum Kopieren und aktualisieren](xref:microsoft.quantum.language.expressions#copy-and-update-expressions)aus vorhandenen erstellt werden. Wie bei Arrays Kopieren solche Ausdrücke alle Element Werte des ursprünglichen Ausdrucks, mit Ausnahme der angegebenen benannten Elemente. Für diese werden die Werte auf die Werte festgelegt, die auf der rechten Seite des Ausdrucks definiert sind. Alle anderen Sprachkonstrukte, wie z. b. [Update-und-REASSIGN-Anweisungen](xref:microsoft.quantum.language.statements#update-and-reassign-statement), die für Array Elemente verfügbar sind, sind auch für benannte Elemente in benutzerdefinierten Typen vorhanden.

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

Es ist nicht möglich, rekursive Typstrukturen zu erstellen.
Das heißt, der Typ, der einen benutzerdefinierten Typ definiert, darf kein tupeltyp sein, der ein Element des benutzerdefinierten Typs enthält.
Im Allgemeinen haben benutzerdefinierte Typen möglicherweise keine zyklischen Abhängigkeiten, sodass der folgende Satz von Typdefinitionen unzulässig wäre:

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

Zusätzlich zur Bereitstellung kurzer Aliase für potenziell komplizierte Tupeltypen ist ein wesentlicher Vorteil der Definition solcher Typen, dass Sie die Absicht eines bestimmten Werts dokumentieren können.
Wenn Sie zum Beispiel `Complex`zurückkehren, können Sie auch 2D-Polarkoordinaten als benutzerdefinierten Typ definieren:

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

Obwohl sowohl `Complex` als auch `Polar` beide über einen zugrunde liegenden Typ `(Double, Double)`verfügen, sind die beiden Typen in f # vollständig inkompatibel. Dadurch wird das Risiko minimiert, dass versehentlich eine komplexe mathematische Funktion mit Polarkoordinaten aufgerufen wird und umgekehrt.
Auf diese Weise haben benutzerdefinierte Typen eine ähnliche Rolle wie Datensätze in F# z. b. 


## <a name="operation-and-function-types"></a>Vorgangs-und Funktionstypen

Ein f #- _Vorgang_ ist eine Quantum-Unterroutine.
Das heißt, es handelt sich um eine Aufruf Bare Routine, die Quantum-Vorgänge enthält.

Eine Q #- _Funktion_ ist eine klassische Unterroutine, die innerhalb eines Quantum-Algorithmus verwendet wird.
Sie kann klassischen Code, aber keine Quantum-Vorgänge enthalten.
Insbesondere können Funktionen keine Qubits zuordnen oder ausleihen, und Sie können auch keine Vorgänge aufzurufen.
Es ist jedoch möglich, dass Sie Vorgänge oder Qubits für die Verarbeitung übergeben.
Funktionen sind daher vollständig deterministisch, da der Aufruf mit denselben Argumenten immer dasselbe Ergebnis erzeugt. 

Vorgänge und Funktionen werden kombiniert als _callables_bezeichnet.  Einige [Beispiele hierfür](#examples) finden Sie unten.

Alle f #-callables werden als Eingabe betrachtet und geben einen einzelnen Wert als Ausgabe zurück.
Sowohl der Eingabe-als auch der Ausgabewert können Tupel sein.
Callables ohne Ergebnis Rückgabe `Unit`.
Callables ohne Eingabe nehmen das leere Tupel als Eingabe auf.

Der Basistyp für beliebige Callable wird als `('Tinput => 'Tresult)` oder `('Tinput -> 'Tresult)`geschrieben, wobei sowohl `'Tinput` als auch `'Tresult` Typen sind.
Das erste Formular, mit `=>`, wird für-Vorgänge verwendet. Das zweite Formular mit `->`für Funktionen.
`((Qubit, Pauli) => Result)` stellt z. b. die Signatur für einen möglichen Single-Qubit-Messvorgang dar.

Funktionstypen werden vollständig durch ihre Signatur angegeben.
Eine Funktion, die den Sinus eines Winkels berechnet, hätte z. b. den Typ `(Double -> Double)`.

Vorgänge – aber keine Funktionen – verfügen über bestimmte zusätzliche _Eigenschaften_ , die als Teil des Vorgangs Typs ausgedrückt werden. Zu diesen Merkmalen zählen Informationen darüber, welche Funktions tüktoren der Vorgang unterstützt.
Funktoren sind metaoperationen, die eine Spezialisierung eines Basis Vorgangs generieren. Weitere Informationen finden Sie [unten unter.](#functors)

Vorgangs Typen werden durch den Eingabetyp, den Ausgabetyp und deren Merkmale angegeben.    
Um Unterstützung für den `Controlled`-und/oder `Adjoint`-Funktions tüktor in einem Vorgangstyp zu benötigen, müssen wir eine Anmerkung hinzufügen, die die entsprechenden Merkmale angibt.
Eine Anmerkung `is Ctl` z. b. gibt an, dass der Vorgang steuerbar ist. Wenn Sie festlegen möchten, dass ein Vorgang dieses Typs sowohl das `Adjoint`-als auch das `Controlled`-Funktor unterstützt, können wir dies als `(Qubit => Unit is Adj + Ctl)`Ausdrücken. Die verwendeten Vorgangs Merkmale `Adj` und `Ctl` streng genommen sind zwei vordefinierte Sätze von Bezeichnungen, wobei jede Bezeichnung eine bestimmte Vorgangs Merkmale angibt, z. b. Unterstützung für ein bestimmtes Funktor.
Daher wird `+` verwendet, um die Kombination dieser beiden Mengen anzugeben, und `*` verwendet, um die Schnittmenge anzugeben, d. h. die Bezeichnungen, die beide Sätze gemeinsam haben.  

Der Pauli-`X` Vorgang hat z. b. den Typ `(Qubit => Unit is Adj + Ctl)`.
Ein Vorgangstyp, der keine Funktions tüktoren unterstützt, wird von seinem Eingabe-und Ausgabetyp allein angegeben, ohne dass zusätzliche Anmerkungen vorhanden sind.


### <a name="type-parameterized-functions-and-operations"></a>Typparametrisierte Funktionen und Vorgänge

Aufruf Bare Typen können Typparameter enthalten.
Typparameter werden durch ein Symbol angegeben, das ein einzelnes Anführungszeichen als Präfix hat. Beispielsweise ist `'A` ein gültiger Typparameter.

Ein Typparameter kann in einer einzigen Signatur mehrmals vorkommen.
Eine Funktion, die eine andere Funktion auf jedes Element eines Arrays anwendet und die gesammelten Ergebnisse zurückgibt, hätte z. b. eine Signatur `(('A[], 'A->'A) -> 'A[])`.
Ebenso kann eine Funktion, die die Komposition von zwei Vorgängen zurückgibt, über Signatur `((('A=>'B), ('B=>'C)) -> ('A=>'C))`verfügen.

Beim Aufrufen eines typparametrisierten Aufruf baren Typs müssen alle Argumente, die denselben Typparameter aufweisen, denselben Typ aufweisen.

Q # stellt keinen Mechanismus zum Einschränken der möglichen Typen bereit, die durch einen Typparameter ersetzt werden könnten.

### <a name="type-compatibility"></a>Typkompatibilität

Ein Vorgang mit zusätzlichen Funktoren, die unterstützt werden, kann überall dort verwendet werden, wo ein Vorgang mit weniger Funktoren, jedoch mit derselben Signatur erwartet wird.
Beispielsweise kann ein Vorgang des Typs `(Qubit => Unit is Adj)` überall dort verwendet werden, wo ein Vorgang des Typs `(Qubit => Unit)` erwartet wird.

Q # ist kovariant in Bezug auf Aufruf Bare Rückgabe Typen: ein Aufruf bares Element, das einen Typ zurückgibt `'A` ist mit einem Aufruf baren mit dem gleichen Eingabetyp und einem Ergebnistyp kompatibel, mit dem `'A` kompatibel ist.

Q # ist in Bezug auf Eingabetypen kontra Variant: ein Aufruf barer, der einen Typ `'A` als Eingabe annimmt, ist mit einem Aufruf baren mit demselben Ergebnistyp und einem Eingabetyp kompatibel, der mit `'A`kompatibel ist.

Das heißt, dass die folgenden Definitionen gegeben sind:

```qsharp
operation Invertible (qs : Qubit[]) : Unit 
is Adj {...} 
operation Unitary (qs : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertibleWith (
   inner: (Qubit[] => Unit is Adj),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith (
   inner: (Qubit[] => Unit is Adj + Ctl),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

Folgendes gilt:

- Der Vorgang `ConjugateInvertibleWith` kann mit einem `inner`-Argument entweder `Invertible` oder `Unitary`aufgerufen werden.
- Der Vorgang `ConjugateUnitaryWith` kann mit einem `inner`-Argument `Unitary`aufgerufen werden, jedoch nicht mit `Invertible`.
- Ein Wert vom Typ "`(Qubit[] => Unit is Adj + Ctl)`" kann von `ConjugateInvertibleWith`zurückgegeben werden.

> [!IMPORTANT]
> F # 0,3 führt einen signifikanten Unterschied im Verhalten von benutzerdefinierten Typen ein.

Benutzerdefinierte Typen werden als umschließende Version des zugrunde liegenden Typs und nicht als Untertyp behandelt.
Dies bedeutet, dass ein Wert eines benutzerdefinierten Typs nicht verwendbar ist, wenn ein Wert des zugrunde liegenden Typs erwartet wird.

### <a name="functors"></a>Funktionselemente

Ein Funktor in Q # ist eine Factory, die einen neuen Vorgang aus einem anderen Vorgang definiert.
Funktoren haben Zugriff auf die Implementierung des Basis Vorgangs, wenn die Implementierung des neuen Vorgangs definiert wird.
Daher können Funktoren komplexere Funktionen als herkömmliche Funktionen höherer Ebene ausführen.

Funktoren haben keine Darstellung im Q #-Typsystem. Daher ist es derzeit nicht möglich, Sie an eine Variable zu binden oder Sie als Argumente zu übergeben. 

Ein Funktor wird verwendet, indem er auf einen Vorgang angewendet und ein neuer Vorgang zurückgegeben wird.
Beispielsweise wird der Vorgang, der sich aus der Anwendung des `Adjoint`-funktors auf den `Y` Vorgang ergibt, als `Adjoint Y`geschrieben.
Der neue Vorgang kann dann wie jeder andere Vorgang aufgerufen werden.
Folglich wendet `Adjoint Y(q1)` das Adjoint-Funktor auf den `Y` Vorgang an, um einen neuen Vorgang zu generieren, und wendet diesen neuen Vorgang auf `q1`an.

Entsprechend wendet `Controlled X(controls, target)` den gesteuerten Funktor auf den `X` Vorgang an, um einen neuen Vorgang zu generieren, und wendet diesen neuen Vorgang auf `controls` und `target`an.

Die zwei standardfunktoren in Q # sind `Adjoint` und `Controlled`.

#### <a name="adjoint"></a>Adjoint

Bei Quantum Computing ist das Adjoint eines Vorgangs die komplexe konjugierte Operation des Vorgangs.
Bei Vorgängen, die einen einheitlichen Operator implementieren, ist das Adjoint das Gegenteil des Vorgangs.
Bei einem einfachen Vorgang, bei dem nur eine Sequenz anderer einheitlicher Vorgänge für einen Satz von Qubits aufgerufen wird, kann das Adjoint durch Anwenden der adjoints der unter Vorgänge auf die gleichen Qubits in umgekehrter Reihenfolge berechnet werden.

Bei einem Vorgangs Ausdruck kann ein neuer Vorgangs Ausdruck mithilfe des `Adjoint`-funktors gebildet werden.
Beispielsweise `Adjoint QFT` den Adjoint-Vorgang des `QFT` Vorgangs fest.
Der neue Vorgang hat dieselbe Signatur und denselben Typ wie der Basis Vorgang.
Insbesondere ermöglicht der neue Vorgang auch das `Adjoint`und lässt `Controlled` nur dann zu, wenn der Basis Vorgang durchgeführt wurde.

Der Adjoint-Funktor ist eine eigene Umkehrung. Das heißt, `Adjoint Adjoint Op` ist immer identisch mit `Op`.

#### <a name="controlled"></a>Klimatisiert

Bei der kontrollierten Version eines Vorgangs handelt es sich um einen neuen Vorgang, der den Basis Vorgang effektiv anwendet, wenn sich alle Steuerelement-Qubits in einem angegebenen Zustand befinden.
Wenn sich die Steuerelement-Qubits in der superposition befinden, wird der Basis Vorgang einheitlich auf den entsprechenden Teil der superposition angewendet.
Folglich werden kontrollierte Vorgänge häufig zum Generieren von entanglement verwendet.

In Q # nehmen kontrollierte Versionen immer ein Array von Steuerelement-Qubits auf, und der angegebene Status ist immer, damit alle Steuerelement-Qubits im Berechnungs Zustand (`PauliZ`) `One`, $ \ket{1}$.
Das Steuern auf der Grundlage anderer Zustände kann erreicht werden, indem der entsprechende einheitliche Vorgang auf die Steuerungs Qubits vor dem kontrollierten Vorgang angewendet und dann nach dem kontrollierten Vorgang die Umkehrung des einheitlichen Vorgangs angewendet wird.
Wenn Sie z. b. einen `X` Vorgang auf ein Steuerelement Qubit vor und nach einer kontrollierten Operation anwenden, bewirkt dies, dass der Vorgang den `Zero` Zustand ($ \ket{0}$) für dieses Qubit steuert. Wenn Sie einen `H` Vorgang vor und nach anwenden, wird die `PauliX` `One` Status gesteuert, d. h.-1 eigen Wert von Pauli X, $ \ket{-} \mathrel{: =} (\ket{0}-\ket{1})/\sqrt{2}$ und nicht der `PauliZ` `One` Status.

Bei einem Vorgangs Ausdruck kann ein neuer Vorgangs Ausdruck mithilfe des `Controlled`-funktors gebildet werden.
Die Signatur des neuen Vorgangs basiert auf der Signatur des ursprünglichen Vorgangs.
Der Ergebnistyp ist identisch, aber der Eingabetyp ist ein zwei Tupel mit einem Qubit-Array, das die Steuerelement-Qubit (s) als erstes Element und die Argumente des ursprünglichen Vorgangs als zweites Element enthält.
Der neue-Vorgang unterstützt `Controlled`und unterstützt `Adjoint` nur dann, wenn der ursprüngliche Vorgang durchgeführt wurde.

Wenn für den ursprünglichen Vorgang nur ein einzelnes Argument verwendet wurde, wird hier die entsprechgabe von Singleton-Tupeln berücksichtigt.
Beispielsweise ist `Controlled X` die gesteuerte Version des `X` Vorgangs.
`X` hat den Typ `(Qubit => Unit is Adj + Ctl)`, sodass `Controlled X` den Typ `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`hat. aufgrund der Übereinstimmung mit einem Singleton-Tupel ist dies mit `((Qubit[], Qubit) => Unit is Adj + Ctl)`identisch.

Wenn der Basis Vorgang mehrere Argumente benötigt hat, denken Sie daran, die entsprechenden Argumente der kontrollierten Version des Vorgangs in Klammern einzuschließen, um Sie in ein Tupel zu konvertieren.
Beispielsweise ist `Controlled Rz` die gesteuerte Version des `Rz` Vorgangs.
`Rz` hat den Typ `((Double, Qubit) => Unit is Adj + Ctl)`, sodass `Controlled Rz` den Typ `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`hat.
Daher ist `Controlled Rz(controls, (0.1, target))` ein gültiger Aufruf `Controlled Rz` (Beachten Sie die Klammern um `0.1, target`).

Als weiteres Beispiel können `CNOT(control, target)` als `Controlled X([control], target)`implementiert werden. Wenn ein Ziel von 2 Steuerungs Qubits (ccnot) gesteuert werden soll, können wir `Controlled X([control1, control2], target)`-Anweisung verwenden.

### <a name="examples"></a>Beispiele

Dieses Beispiel für einen Q #-Vorgang stammt aus dem [Mess](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) Beispiel. Innerhalb von Vorgängen können wir Qubits zuordnen und Quantum-Vorgänge für diese Qubits verwenden, wie z. b. `H` und `X`:

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit () : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit

            set result = M(qubit);      // Measure the qubit

            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

Dieses Beispiel für eine Funktion stammt aus dem [phaseschätzungsbeispiel](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) . Sie enthält reinen klassischen Code. Sie können sehen, dass im Gegensatz zum obigen Beispiel keine Qubits zugeordnet sind und keine Quantum-Vorgänge verwendet werden.


```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function MultiplyPointwise (left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

Es ist auch möglich, dass für eine Funktion Qubits für die Verarbeitung übergeben werden, wie in diesem Beispiel aus dem Beispiel " [reversiblelogicsynthese](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) ". Qubits werden an die Funktion geleitet und zur Verarbeitung verwendet, obwohl die Qubit-Zustände zu keinem Zeitpunkt geändert werden.

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates (qubits : Qubit[], masks : MCMTMask[]) : MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
