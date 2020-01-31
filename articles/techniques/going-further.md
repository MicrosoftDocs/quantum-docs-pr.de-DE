---
title: 'Weitere Schritte: f #-Techniken | Microsoft-Dokumentation'
description: 'Weitere Schritte: Q #-Techniken'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.going-further
ms.openlocfilehash: bd2b799d4001e280baccb04158247891b9cbb5bc
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820197"
---
# <a name="going-further"></a>Weiter #

Nachdem Sie nun erfahren haben, wie Sie interessante Quantum-Programme in Q # schreiben, werden in diesem Abschnitt noch einige erweiterte Themen vorgestellt, die sich in Zukunft als nützlich erweisen sollten.


## <a name="generic-operations-and-functions"></a>Generische Vorgänge und Funktionen ##

> [!TIP]
> In diesem Abschnitt wird die grundlegende Vertrautheit mit [Generika C#in ](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [Generika in F# ](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [ C++ Vorlagen](https://docs.microsoft.com/cpp/cpp/templates-cpp)oder ähnlichen Ansätzen für die Metaprogrammierung in anderen Sprachen vorausgesetzt.

Viele Funktionen und Vorgänge, die wir möglicherweise definieren möchten, sind nicht wirklich stark von den Typen Ihrer Eingaben abhängig, sondern verwenden nur implizit ihre Typen über eine andere Funktion oder einen anderen Vorgang.
Sehen Sie sich beispielsweise das *Karten* Konzept an, das vielen funktionalen Sprachen gemeinsam ist. bei Angabe einer Funktion $f (x) $ und einer Auflistung von Werten $\{x_1, x_2, \dots, x_n\}$ gibt MAP eine neue Auflistung $\{f (x_1), f (x_2), \dots, f (x_n)\}$ zurück.
Um dies in Q # zu implementieren, können wir diese Funktionen als erste Klasse nutzen.
Sehen wir uns ein kurzes Beispiel für `Map`an, indem wir ★ als Platzhalter verwenden, während wir herausfinden, welche Typen wir benötigen.

```qsharp
function Map(fn : ★ -> ★, values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Beachten Sie, dass diese Funktion unabhängig von den tatsächlichen Typen, die wir ersetzen, sehr gut aussieht.
Eine Zuordnung von Ganzzahlen zu Paulis sieht beispielsweise genauso wie eine Zuordnung von Gleit Komma Zahlen zu Zeichen folgen aus:

```qsharp
function MapIntsToPaulis(fn : Int -> Pauli, values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : Double -> String, values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Im Prinzip könnten wir eine Version von `Map` für jedes Paar von Typen schreiben, auf die wir stoßen, aber dies führt zu einer Reihe von Schwierigkeiten.
Wenn beispielsweise in `Map`ein Fehler gefunden wird, müssen wir sicherstellen, dass die Korrektur in allen Versionen von `Map`einheitlich angewendet wird.
Wenn ein neues Tupel oder ein neues UDT erstellt wird, muss nun auch eine neue `Map` erstellt werden, um zusammen mit dem neuen Typ zu gelangen.
Obwohl dies für eine kleine Anzahl solcher Funktionen überlastet ist, da wir mehr und mehr Funktionen derselben Form wie `Map`erfassen, werden die Kosten für die Einführung neuer Typen in relativ kurzer Reihenfolge zu groß.

Ein Großteil dieser Schwierigkeiten ergibt sich jedoch darin, dass wir dem Compiler nicht die Informationen gegeben haben, die er benötigt, um zu erkennen, wie die verschiedenen Versionen von `Map` verknüpft sind.
Effektiv möchten wir, dass der Compiler `Map` als eine mathematische Funktion von q #- *Typen* zu q #-Funktionen behandelt.
Dieses Konzept wird formalisiert, indem Funktionen und Vorgänge *Typparameter*sowie ihre normalen tupelparameter enthalten können.
In den obigen Beispielen möchten wir `Map`, dass im ersten Fall Typparameter `Int, Pauli` und im zweiten Fall `Double, String` werden.
In den meisten Fällen können diese Typparameter so verwendet werden, als wären Sie normale Typen: Wir verwenden Werte von Typparametern, um Arrays und Tupel zu erstellen, Funktionen und Vorgänge aufzurufen und gewöhnliche oder änderbare Variablen zuzuweisen.

> [!NOTE]
> Der extremste Fall der indirekten Abhängigkeit ist die von Qubits, bei denen ein Q #-Programm nicht direkt auf die Struktur des `Qubit` Typs zurückgreifen kann, sondern solche Typen an andere Vorgänge und Funktionen übergeben **muss** .

Wenn Sie zum obigen Beispiel zurückkehren, sehen Sie, dass `Map` über Typparameter verfügen müssen, eine zum Darstellen der Eingabe für `fn` und eine, die die Ausgabe von `fn`darstellen soll.
In f # wird dies durch Hinzufügen von spitzen Klammern (das `<>`, nicht von Klammern $ \braket{}$!) nach dem Namen einer Funktion oder eines Vorgangs in der Deklaration und durch Auflisten der einzelnen Typparameter geschrieben.
Der Name jedes Typparameters muss mit einem Tick-`'`beginnen, was darauf hinweist, dass es sich um einen Typparameter handelt und nicht um einen normalen Typ (auch als *konkreter* Typ bezeichnet).
Für `Map`schreiben wir daher Folgendes:

```qsharp
function Map<'Input, 'Output>(fn : 'Input -> 'Output, values : 'Input[]) : 'Output {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Beachten Sie, dass die Definition von `Map<'Input, 'Output>` den Versionen, die wir zuvor geschrieben haben, sehr ähnlich aussieht.
Der einzige Unterschied besteht darin, dass der Compiler explizit informiert hat, dass `Map` nicht direkt von der `'Input` und `'Output` abhängig ist, sondern für zwei Typen funktioniert, indem Sie Sie indirekt über `fn`verwenden.
Nachdem wir `Map<'Input, 'Output>` auf diese Weise definiert haben, können wir es so nennen, als wäre es eine gewöhnliche Funktion:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Das Schreiben von generischen Funktionen und Vorgängen ist eine Stelle, an der "Tupel-in-Tupel-out" eine sehr nützliche Methode für den Umgang mit Q #-Funktionen und-Vorgängen ist.
> Da jede Funktion genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt, entspricht eine Eingabe des Typs `'T -> 'U` *jeder beliebigen* Q #-Funktion.
> Ebenso kann jeder Vorgang an eine Eingabe des Typs `'T => 'U`übermittelt werden.

Sehen Sie sich als zweites Beispiel die Herausforderung an, eine Funktion zu schreiben, die die Komposition zweier anderer Funktionen zurückgibt:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Hier müssen Sie genau angeben, welche `A`, `B`und `C` sind, und so das Dienstprogramm der neuen `Compose` Funktion stark einschränken.
Schließlich ist `Compose` nur über `innerFn` und `outerFn`von `A`, `B`und *`C` abhängig* .
Als Alternative können wir Typparameter zu `Compose` hinzufügen, die angeben, dass Sie für *alle* `A`, `B`und `C`funktioniert, solange diese Parameter den von `innerFn` und `outerFn`erwarteten entsprechen:

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Die Q #-Standardbibliotheken stellen eine Reihe von Typen parametrisierten Vorgängen und Funktionen bereit, um die Express-Ablauf Steuerung leichter zu gestalten.
Diese werden im [Leitfaden der Q #-Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro)erläutert.

## <a name="borrowing-qubits"></a>Ausleihen von Qubits ##

Der Mechanismus zum ableihen ermöglicht die Zuordnung von Qubits, die während einer Berechnung als Scratch-Speicherplatz verwendet werden kann. Diese Qubits befinden sich in der Regel nicht in einem sauberen Zustand, d. h., Sie werden nicht notwendigerweise in einem bekannten Zustand initialisiert, wie z. b. $ \ket{0}$. Außerdem spricht man von "Dirty"-Qubits, weil ihr Zustand unbekannt ist, und kann sogar mit anderen Teilen des Arbeitsspeichers des Quantums Computers entkoppelt werden. Zu den bekannten Anwendungsfällen von Dirty Qubits zählen Implementierungen von multigesteuerten CNOT Gates, die nur sehr wenige Qubits und die Implementierung von inkrementern erfordern.

Im Kanon finden Sie Beispiele, in denen das `borrowing`-Schlüsselwort verwendet wird, z. `MultiControlledXBorrow`. die Funktion, die unten definiert ist.
Wenn `controls` die Steuerungs Qubits angibt, die einem `X` Vorgang hinzugefügt werden sollen, wird eine Gesamtzahl von `Length(controls)-2` vielen Dirty ancillas durch diese Implementierung hinzugefügt.

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

Beachten Sie, dass die umfangreiche Verwendung des `With` Combinator in seinem Formular---, das für Vorgänge anwendbar ist, die Adjoint unterstützen, d. h., `WithA`---in diesem Beispiel erstellt wurde. Dies ist ein guter Programmierstil, als das Steuerelement zu Strukturen hinzuzufügen, die `With` nur Steuerelemente an den inneren Vorgang weitergibt Beachten Sie, dass hier zusätzlich zum `body` des Vorgangs eine Implementierung des `controlled` Texts des Vorgangs explizit bereitgestellt wurde, anstatt auf eine `controlled auto`-Anweisung zurückgreifen zu müssen. Der Grund hierfür ist, dass wir aus der Struktur der Verbindung wissen, wie Sie ganz einfach weitere Steuerelemente hinzufügen können, die im Vergleich zum Hinzufügen von Steuerelementen zu jedem und jedem einzelnen Gate im `body`von Vorteil sind. 

Es ist aufschlussreich, diesen Code mit einer anderen Funktion von `MultiControlledXClean` zu vergleichen, die das gleiche Ziel erreicht, eine mehrfach gesteuerte `X` Operation zu implementieren, bei der jedoch mithilfe des `using` Mechanismus mehrere Clean Qubits verwendet werden. 
