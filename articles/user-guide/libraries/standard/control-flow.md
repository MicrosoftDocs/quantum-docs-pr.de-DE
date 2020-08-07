---
title: Fluss Steuerungen in den Q# standardmäßigen libararies
description: Erfahren Sie mehr über die Vorgänge und Funktionen der Fluss Steuerung in der Microsoft- Q# Standardbibliothek.
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: a440f1ef2b901b18593816ca27aeadf7ab827104
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868575"
---
# <a name="higher-order-control-flow"></a>Ablauf Steuerung höherer Ordnung #

Eine der Hauptrollen der Standardbibliothek besteht darin, die algorithmischen Ideen auf hoher Ebene einfacher als [Quantum-Programme](https://en.wikipedia.org/wiki/Quantum_programming)auszudrücken.
Folglich stellt der Q# Kanon eine Vielzahl verschiedener flowsteuerungskonstrukte bereit, die jeweils mithilfe der partiellen Anwendung von Funktionen und Vorgängen implementiert werden.
Wenn Sie sofort zu einem Beispiel springen, berücksichtigen Sie den Fall, in dem eine "CNOT-Leiter" für ein Register erstellt werden soll:

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

Dieses Muster kann mithilfe von Iterationen und Schleifen ausgedrückt werden `for` :

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

Ausgedrückt in Bezug auf <xref:microsoft.quantum.canon.applytoeachca> -und-Array Bearbeitungsfunktionen wie <xref:microsoft.quantum.arrays.zip> , ist dies jedoch viel kürzer und leichter zu lesen:

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

Im restlichen Teil dieses Abschnitts werden einige Beispiele für die Verwendung der verschiedenen Fluss Steuerungs Vorgänge und-Funktionen, die von der Canon bereitgestellt werden, zum kompakten Ausdrücken von Quantum-Programmen bereitgestellt.

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a>Anwenden von Vorgängen und Funktionen auf Arrays und Bereiche ##

Eine der primären Abstraktionen, die von der Canon bereitgestellt werden, ist die der Iterationen.
Nehmen Sie zum Beispiel eine einheitliche Form $U \otimes u \otimes \cdots \otimes u $ for a Single-Qubit einheitlicher $U $.
In Q# können wir dies verwenden <xref:microsoft.quantum.arrays.indexrange> , um dies als eine `for` Schleife über ein Register darzustellen:

```qsharp
/// # Summary
/// Applies $H$ to all qubits in a register.
operation ApplyHadamardToAll(
    register : Qubit[])
: Unit is Adj + Ctl {
    for (qubit in register) {
        H(qubit);
    }
}
```

Anschließend können wir diesen neuen Vorgang verwenden `HAll(register)` , um $H \otimes h \otimes \cdots \otimes h $ anzuwenden.

Dies ist jedoch umständlich, insbesondere in einem größeren Algorithmus.
Außerdem ist dieser Ansatz auf den jeweiligen Vorgang spezialisiert, den wir auf die einzelnen Qubits anwenden möchten.
Wir können die Tatsache verwenden, dass Vorgänge erstklassige sind, um dieses algorithmische Konzept expliziter auszudrücken:

```qsharp
ApplyToEachCA(H, register);
```

Hier gibt das-Suffix `CA` an, dass der-Aufrufwert `ApplyToEach` selbst adjointable und steuerbar ist.
Wenn also `U` und unter `Adjoint` stützt `Controlled` , sind die folgenden Zeilen äquivalent:

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

Dies bedeutet insbesondere, dass Aufrufe von `ApplyToEachCA` in Vorgängen angezeigt werden können, für die eine Adjoint-Spezialisierung automatisch generiert wird.
Ebenso <xref:microsoft.quantum.canon.applytoeachindex> eignet sich für die Darstellung von Mustern im Formular `U(0, targets[0]); U(1, targets[1]); ...` und bietet Versionen für jede Kombination von Funktoren, die von der Eingabe unterstützt werden.

> [!TIP]
> `ApplyToEach`ist typparametrisiert, sodass Sie mit-Vorgängen verwendet werden kann, die andere Eingaben als annehmen `Qubit` .
> Nehmen wir beispielsweise an, dass `codeBlocks` ein Array von <xref:microsoft.quantum.errorcorrection.logicalregister> Werten ist, die wieder hergestellt werden müssen.
> Dann `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` wendet den Fehler Behebungs Code `code` und die Wiederherstellungs Funktion `recoveryFn` unabhängig voneinander auf jeden Block an.
> Dies gilt auch für klassische Eingaben: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` wendet eine Drehung von $ \pi/$2 über $X $ an, gefolgt von einer Drehung $pi/$3 über $Y $.

Der Q# Kanon bietet auch Unterstützung für klassische Enumerationsmuster, die der funktionalen Programmierung vertraut sind.
Implementiert beispielsweise <xref:microsoft.quantum.arrays.fold> das Muster $f (f (s \_ {\text{Initial}}, x \_ 0), x \_ 1), \dots) $, um eine Funktion über eine Liste zu reduzieren.
Dieses Muster kann verwendet werden, um Summen, Produkte, Minima, Maxima und andere Funktionen zu implementieren:

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

Ebenso können Funktionen wie <xref:microsoft.quantum.arrays.mapped> und <xref:microsoft.quantum.arrays.mappedbyindex> verwendet werden, um funktionale Programmier Konzepte in auszudrücken Q# .

## <a name="composing-operations-and-functions"></a>Verfassen von Vorgängen und Funktionen ##

Die von der Canon angebotenen Ablaufsteuerungs-Konstrukte nehmen Vorgänge und Funktionen als Eingaben an, sodass es hilfreich ist, mehrere Vorgänge oder Funktionen in einem einzigen Aufruf baren zu verfassen.
Beispielsweise ist das Muster $UVU ^ {\dagger} $ bei der Quantum-Programmierung äußerst häufig, sodass der Kanon den Vorgang <xref:microsoft.quantum.canon.applywith> als Abstraktion für dieses Muster bereitstellt.
Diese Abstraktion ermöglicht auch ein effizienteres durcharbeiten in Verbindungen, da `Controlled` die Reihenfolge der Sequenz `U(qubit); V(qubit); Adjoint U(qubit);` nicht auf jede Weise agieren muss `U` .
Um dies zu sehen, lassen Sie $c (U) $ die einheitliche Darstellung `Controlled U([control], target)` aus, und lassen Sie $c (V) $ auf die gleiche Weise definiert werden.
Für einen beliebigen Status $ \ket{\psi} $, \begin{align} c (u) c (V) c (u) ^ \dagger \ket {1} \otimes \ket{\psi} & = \ket {1} \otimes (UVU ^ {\dagger} \ket{\psi}) \\ \\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {1} \otimes \ket{\psi}.
\end{align} durch die Definition von `Controlled` .
Andererseits: \begin{align} c (u) c (V) c (u) ^ \dagger \ket {0} \otimes \ket{\psi} & = \ket {0} \otimes \ket{\psi} \\ \\ & = \ket {0} \ouhrzeiten (UU ^ \dagger \ket{\psi}) \\ \\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket {0} \otimes \ket{\psi}.
\end{align} nach Linearität können wir den Schluss $U $ out für alle Eingabe Zustände auf diese Weise berücksichtigen.
Das heißt, $c (UVU ^ \dagger) = u c (V) u ^ \dagger $.
Da das Steuern von Vorgängen im allgemeinen teuer sein kann, kann die Verwendung von kontrollierten Varianten wie `WithC` und `WithCA` die Anzahl von Steuerelement-Funktoren verringern, die angewendet werden müssen.

> [!NOTE]
> Eine andere Folge bei der Umgestaltung $U $ besteht darin, dass wir nicht einmal wissen müssen, wie das `Controlled` Funktor angewendet wird `U` .
> `ApplyWithCA`Daher weist eine schwächere Signatur auf, als möglicherweise erwartet wird:
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

Ebenso <xref:microsoft.quantum.canon.bound> erzeugt Vorgänge, die wiederum eine Sequenz anderer Vorgänge anwenden.
Beispielsweise sind die folgenden Punkte äquivalent:

```qsharp
H(qubit); X(qubit);
Bound([H, X], qubit);
```

Das Kombinieren mit Iterations Mustern kann dies besonders nützlich machen:

```qsharp
// Bracket the quantum Fourier transform with $XH$ on each qubit.
ApplyWith(ApplyToEach(Bound([H, X]), _), QFT, _);
```

### <a name="time-ordered-composition"></a>Zeit geordnete Komposition ###

Wir können noch weiter gehen, indem wir die Fluss Steuerung in Bezug auf partielle Anwendungs-und klassische Funktionen betrachten und auch ziemlich ausgereifte Quantum-Konzepte im Hinblick auf die klassische Fluss Steuerung modellieren.
Diese Analogie wird durch die Erkennung präziser, dass einheitliche Operatoren genau den Nebeneffekten von aufrufenden Vorgängen entsprechen, sodass jede Zerlegung einheitlicher Operatoren in Bezug auf andere einheitliche Operatoren die Erstellung einer bestimmten Aufruf Sequenz für klassische Unterroutinen entspricht, die Anweisungen ausgeben, die als bestimmte einheitliche Operatoren fungieren.
In dieser Ansicht `Bound` ist genau die Darstellung des Matrix Produkts, da `Bound([A, B])(target)` gleich ist `A(target); B(target);` , was wiederum die Aufruf Sequenz ist, die $BA $ entspricht.

Ein anspruchsvolleres Beispiel ist die [Erweiterung "Trotter – Suzuki](https://arxiv.org/abs/math-ph/0506007v1)".
Wie im Abschnitt "Dynamical Generator Darstellung" der [Datenstrukturen](xref:microsoft.quantum.libraries.data-structures)erläutert, bietet die Trotter – Suzuki-Erweiterung eine besonders nützliche Methode zum Ausdrücken von Matrix exponentialen.
Wenn Sie die Erweiterung beispielsweise in der untersten Reihenfolge anwenden, ergibt dies für alle Operatoren $A $ und $B $, sodass $A = A ^ \dagger $ und $B = B ^ \dagger $, \begin{align} \tag{★} \label{EQ: Trotter-Suzuki-0} \exp (i [A + B] t) = \ lim_ {n\t\infty} \left (\exp (i A t/n) \exp (i B t/n) \right) ^ n.
\end{align}, das heißt, dass wir einen Status unter $A + B $ weiterentwickeln können, indem Sie sich unter $A $ und $B $ allein weiterentwickeln.
Wenn wir die Weiterentwicklung unter $A $ durch einen Vorgang darstellen `A : (Double, Qubit[]) => Unit` , der $e ^ {i t A} $ angewendet wird, wird die Darstellung des Trotters – Suzuki-Erweiterung in Bezug auf das Neuordnen von Aufruf Sequenzen deutlich.
Konkret: bei einem Vorgang `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` wie `A = U(0, _, _)` und `B = U(1, _, _)` können wir einen neuen Vorgang definieren, der den ganzzahligen Wert von `U` at time $t $ darstellt, indem Sequenzen der Form erzeugt werden.

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

An diesem Punkt können wir nun die –-Erweiterung "Trotter" *ohne Verweis auf die Quantum-Mechanik*in Grund haben.
Die Erweiterung ist ein sehr spezielles Iterations Muster, das durch "$ \eqref {EQ: Trotter-Suzuki-0} $" motiviert ist.
Dieses Iterations Muster wird implementiert von <xref:microsoft.quantum.canon.decomposeintotimestepsca> :

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

Die Signatur von `DecomposeIntoTimeStepsCA` folgt einem allgemeinen Muster in Q# , bei dem Auflistungen, die entweder durch Arrays oder durch Elemente, die im laufenden Betrieb sind, durch Tupel dargestellt werden, deren erste Elemente Werte sind, die `Int` Ihre Längen angeben.

## <a name="putting-it-together-controlling-operations"></a>Kombinieren von Vorgängen: Steuern von Vorgängen ##

Schließlich baut der Kanon auf dem `Controlled` Funktor auf, indem er zusätzliche Möglichkeiten für die Bedingung von Quantum-Vorgängen bereitstellt.
Es ist üblich, insbesondere bei der Quantum-Arithmetik, Vorgänge in anderen Compute-Zuständen als $ \ket{0\cdots 0} $ auszuführen.
Mithilfe der oben eingeführten Steuerungs Vorgänge und-Funktionen können wir in einer einzelnen Anweisung allgemeinere Quantum-Bedingungen verwenden.
<xref:microsoft.quantum.canon.controlledonbitstring>Sehen wir uns nun an, wie dies geschieht (Sans-Typparameter), und dann werden die Teile nacheinander unterbricht.
Als erstes müssen wir einen Vorgang definieren, der tatsächlich den Schwerpunkt der Implementierung des Steuer Elements auf willkürlichen Berechnungsbasis Zuständen leistet.
Dieser Vorgang wird jedoch nicht direkt aufgerufen. daher fügen wir `_` am Anfang des Namens ein, um anzugeben, dass es sich um eine Implementierung eines anderen Konstrukts an anderer Stelle handelt.

```qsharp
operation _ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl),
    controlRegister : Qubit[],
    targetRegister: Qubit[])
: Unit is Adj + Ctl
```

Beachten Sie, dass wir eine als-Array dargestellte Zeichenfolge als `Bool` Array verwenden, mit der wir die gewünschte Anlage für den Vorgang angeben, den `oracle` wir erhalten.
Da dieser Vorgang die Anwendung tatsächlich direkt durchführt, müssen wir auch die Steuer-und Ziel Register verwenden, die beide hier als dargestellt werden `Qubit[]` .

Als Nächstes stellen wir fest, dass die Steuerung des Berechnungs basierten Zustands $ \ket{\vec{s}} = \ket{s \_ 0 s \_ 1 \dots s \_ {n-1}} $ für eine Bitzeichenfolge $ \vec{s} $ durch Umwandeln von $ \ket{\vec{s}} $ in $ \ket{0\cdots 0} $ realisiert werden kann.
Insbesondere: $ \ket{\vec{s}} = X ^ {s \_ 0} \otimes X ^ {s \_ 1} \otimes \cdots \otimes X ^ {s \_ {n-1}} \ket{0\cdots 0} $.
Seit $X ^ {\dagger} = x $ bedeutet dies, dass $ \ket{0\dots 0} = X ^ {s \_ 0} \otimes x ^ {s \_ 1} \otimes \cdots \otimes x ^ {s \_ {n-1}} \ket{\vec{s}} $.
Daher können wir $P = x ^ {s \_ 0} \otimes x ^ {s \_ 1} \otimes \cdots \otimes X ^ {s \_ {n-1}} $, Apply `Controlled oracle` und Transform Back to $ \vec{s} $ anwenden.
Diese Konstruktion ist genau `ApplyWith` , daher wird der Text des neuen Vorgangs entsprechend geschrieben:

```qsharp
{
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

Hier haben wir verwendet, <xref:microsoft.quantum.canon.applypaulifrombitstring> um $P $ anzuwenden, um das Ziel teilweise für die Verwendung mit anzuwenden `ApplyWith` .
Beachten Sie jedoch, dass wir die *Steuer* Element Registrierung in das gewünschte Formular umwandeln müssen, sodass wir den inneren Vorgang `(Controlled oracle)` für das *Ziel*teilweise anwenden.
Dadurch `ApplyWith` wird das Steuerelement in der Klammer mit $P $, genau wie gewünscht, in eine eckige Klammer eingefügt.

An diesem Punkt könnten wir zwar das tun, aber es ist nicht zu erwarten, dass unser neuer Vorgang nicht wie das Anwenden des `Controlled` funktors funktioniert.
Daher haben wir die Definition des neuen Ablauf steuerungskonzepts abgeschlossen, indem wir eine Funktion schreiben, die das Oracle zum Steuern benötigt und einen neuen Vorgang zurückgibt.
Auf diese Weise sieht die neue Funktion sehr ähnlich aus und zeigt `Controlled` , dass wir mit und dem Kanon problemlos leistungsstarke neue Ablaufsteuerungskonstrukte definieren können Q# :

```qsharp
function ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl))
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
