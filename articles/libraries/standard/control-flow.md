---
title: 'Fluss Steuerungen in den Q# Standard-libararies'
description: 'Erfahren Sie mehr über die Vorgänge und Funktionen der Fluss Steuerung in der Microsoft Q# Standard-Bibliothek.'
author: QuantumWriter
uid: microsoft.quantum.concepts.control-flow
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: b41b3edd7a3e3ac13dbda106a869f4cba8183600
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907170"
---
# <a name="higher-order-control-flow"></a>Ablauf Steuerung höherer Ordnung #

Eine der Hauptrollen der Standardbibliothek besteht darin, die algorithmischen Ideen auf hoher Ebene einfacher als [Quantum-Programme](https://en.wikipedia.org/wiki/Quantum_programming)auszudrücken.
Daher stellt der Q#-Kanon eine Vielzahl verschiedener flowsteuerungskonstrukte bereit, die jeweils mithilfe der partiellen Anwendung von Funktionen und Vorgängen implementiert werden.
Wenn Sie sofort zu einem Beispiel springen, berücksichtigen Sie den Fall, in dem eine "CNOT-Leiter" für ein Register erstellt werden soll:

```qsharp
let nQubits = Length(register);
CNOT(register[0], register[1]);
CNOT(register[1], register[2]);
// ...
CNOT(register[nQubits - 2], register[nQubits - 1]);
```

Dieses Muster kann mithilfe von Iterations-und `for` Schleifen ausgedrückt werden:

```qsharp
for (idxQubit in 0..nQubits - 2) {
    CNOT(register[idxQubit], register[idxQubit + 1]);
}
```

Dies wird im Hinblick auf <xref:microsoft.quantum.canon.applytoeachca> und Array Bearbeitungsfunktionen wie <xref:microsoft.quantum.arrays.zip>ausgedrückt, aber dies ist viel kürzer und leichter zu lesen:

```qsharp
ApplyToEachCA(CNOT, Zip(register[0..nQubits - 2], register[1..nQubits - 1]));
```

Im restlichen Teil dieses Abschnitts werden einige Beispiele für die Verwendung der verschiedenen Fluss Steuerungs Vorgänge und-Funktionen, die von der Canon bereitgestellt werden, zum kompakten Ausdrücken von Quantum-Programmen bereitgestellt.

## <a name="applying-operations-and-functions-over-arrays-and-ranges"></a>Anwenden von Vorgängen und Funktionen auf Arrays und Bereiche ##

Eine der primären Abstraktionen, die von der Canon bereitgestellt werden, ist die der Iterationen.
Nehmen Sie zum Beispiel eine einheitliche Form $U \otimes u \otimes \cdots \otimes u $ for a Single-Qubit einheitlicher $U $.
In Q# könnten wir <xref:microsoft.quantum.arrays.indexrange> verwenden, um dies als `for`-Schleife über ein Register darzustellen:

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

Dieser neue Vorgang kann dann als `HAll(register)` verwendet werden, um $H \otimes h \otimes \cdots \otimes h $ anzuwenden.

Dies ist jedoch umständlich, insbesondere in einem größeren Algorithmus.
Außerdem ist dieser Ansatz auf den jeweiligen Vorgang spezialisiert, den wir auf die einzelnen Qubits anwenden möchten.
Wir können die Tatsache verwenden, dass Vorgänge erstklassige sind, um dieses algorithmische Konzept expliziter auszudrücken:

```qsharp
ApplyToEachCA(H, register);
```

Hier gibt das Suffix `CA` an, dass der Aufruf`ApplyToEach` selbst adjointable und steuerbar ist.
Wenn `U` `Adjoint` und `Controlled`unterstützt, sind die folgenden Zeilen gleichwertig:

```qsharp
Adjoint ApplyToEachCA(U, register);
ApplyToEachCA(Adjoint U, register);
```

Dies bedeutet insbesondere, dass Aufrufe von `ApplyToEachCA` in Vorgängen angezeigt werden können, für die eine Adjoint-Spezialisierung automatisch generiert wird.
Auf ähnliche Weise ist <xref:microsoft.quantum.canon.applytoeachindex> nützlich für das darstellen von Mustern der Form `U(0, targets[0]); U(1, targets[1]); ...`und bietet Versionen für jede Kombination von Funktoren, die von der Eingabe unterstützt werden.

> [!TIP]
> `ApplyToEach` ist typparametrisiert, sodass er mit Vorgängen verwendet werden kann, die andere Eingaben als `Qubit`annehmen.
> Nehmen wir beispielsweise an, dass `codeBlocks` ein Array von <xref:microsoft.quantum.errorcorrection.logicalregister> Werten ist, die wieder hergestellt werden müssen.
> Dann wendet `ApplyToEach(Recover(code, recoveryFn, _), codeBlocks)` den Fehler Behebungs Code `code` und die Wiederherstellungs Funktion `recoveryFn` auf jeden Block unabhängig an.
> Dies gilt auch für klassische Eingaben: `ApplyToEach(R(_, _, qubit), [(PauliX, PI() / 2.0); (PauliY(), PI() / 3.0]))` wendet eine Drehung von $ \pi/$2 auf $X $ an, gefolgt von einer Drehung $pi/$3 über $Y $.

Q# Canon bietet auch Unterstützung für klassische Enumerationstypen, die der funktionalen Programmierung vertraut sind.
<xref:microsoft.quantum.arrays.fold> implementiert beispielsweise das Muster $f (f (s\_{\text{Initial}}, x\_0), x\_1), \dots) $, um eine Funktion über eine Liste zu reduzieren.
Dieses Muster kann verwendet werden, um Summen, Produkte, Minima, Maxima und andere Funktionen zu implementieren:

```qsharp
open Microsoft.Quantum.Arrays;
function Plus(a : Int, b : Int) : Int { return a + b; }
function Sum(xs : Int[]) {
    return Fold(Sum, 0, xs);
}
```

Ebenso können Funktionen wie <xref:microsoft.quantum.arrays.mapped> und <xref:microsoft.quantum.arrays.mappedbyindex> verwendet werden, um funktionale Programmier Konzepte in Q# auszudrücken.

## <a name="composing-operations-and-functions"></a>Verfassen von Vorgängen und Funktionen ##

Die von der Canon angebotenen Ablaufsteuerungs-Konstrukte nehmen Vorgänge und Funktionen als Eingaben an, sodass es hilfreich ist, mehrere Vorgänge oder Funktionen in einem einzigen Aufruf baren zu verfassen.
Beispielsweise ist das Muster $UVU ^ {\dagger} $ bei der Quantum-Programmierung äußerst häufig, sodass der Kanon den Vorgang <xref:microsoft.quantum.canon.applywith> als Abstraktion für dieses Muster bereitstellt.
Diese Abstraktion ermöglicht außerdem eine effizientere Zusammenstellung von Verbindungen, da `Controlled`, die auf die Sequenz reagieren `U(qubit); V(qubit); Adjoint U(qubit);` nicht auf jeder `U`agieren muss.
Um dies zu sehen, lassen Sie $c (U) $ die einheitliche darstellen, die `Controlled U([control], target)` darstellt, und lassen Sie $c (V) $ auf die gleiche Weise definiert.
Für einen beliebigen Status $ \ket{\psi} $, \begin{align} c (u) c (V) c (u) ^ \dagger \ket{1} \otimes \ket{\psi} & = \ket{1} \otimes (UVU ^ {\dagger} \ket{\psi}) \\\\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket{1} \otimes \ket{\psi}.
\end{align} durch die Definition `Controlled`.
Andererseits: \begin{align} c (u) c (V) c (u) ^ \dagger \ket{0} \otimes \ket{\psi} & = \ket{0} \otimes \ket{\psi} \\\\ & = \ket{0} \ otimes (UU ^ \dagger \ket{\psi}) \\\\ & = (\boldone \otimes u) (c (V)) (\boldone \otimes u ^ \dagger) \ket{0} \otimes \ket{\psi}.
\end{align} nach Linearität können wir den Schluss $U $ out für alle Eingabe Zustände auf diese Weise berücksichtigen.
Das heißt, $c (UVU ^ \dagger) = u c (V) u ^ \dagger $.
Da das Steuern von Vorgängen im allgemeinen teuer sein kann, kann die Verwendung von kontrollierten Varianten wie `WithC` und `WithCA` die Anzahl von Steuerelement-Steuerelementen verringern, die angewendet werden müssen.

> [!NOTE]
> Eine andere Folge bei der Umgestaltung $U $ besteht darin, dass wir nicht einmal wissen müssen, wie Sie den `Controlled`-Funktor auf `U`anwenden können.
> `ApplyWithCA` hat daher eine schwächere Signatur, als Sie möglicherweise erwartet wird:
> ```qsharp
> ApplyWithCA<'T> : (('T => Unit is Adj),
>     ('T => Unit is Adj + Ctl), 'T) => Unit
> ```

Ebenso werden von <xref:microsoft.quantum.canon.bound> Vorgänge erzeugt, die wiederum eine Sequenz anderer Vorgänge anwenden.
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
Diese Analogie wird durch die Erkennung präziser, dass einheitliche Operatoren genau den Nebeneffekten von aufrufenden Vorgängen entsprechen, sodass jede Zerlegung einheitlicher Operatoren in Bezug auf andere einheitliche Operatoren die Erstellung eines bestimmten Aufruf Sequenz für klassische Unterroutinen, die Anweisungen ausgeben, die als bestimmte einheitliche Operatoren fungieren.
In dieser Ansicht ist `Bound` genau die Darstellung des Matrix Produkts, da `Bound([A, B])(target)` `A(target); B(target);`entspricht. Dies wiederum ist die Aufruf Sequenz, die $BA $ entspricht.

Ein anspruchsvolleres Beispiel ist die [Erweiterung "Trotter – Suzuki](https://arxiv.org/abs/math-ph/0506007v1)".
Wie im Abschnitt "Dynamical Generator Darstellung" der [Datenstrukturen](xref:microsoft.quantum.libraries.data-structures)erläutert, bietet die Trotter – Suzuki-Erweiterung eine besonders nützliche Methode zum Ausdrücken von Matrix exponentialen.
Wenn Sie die Erweiterung beispielsweise in der untersten Reihenfolge anwenden, ergibt dies für alle Operatoren $A $ und $B $, sodass $A = A ^ \dagger $ und $B = B ^ \dagger $, \begin{align} \tag{★} \label{EQ: Trotter-Suzuki-0} \exp (i [A + B] t) = \ lim_ {n\t\infty} \left (\exp (i A t/n) \exp (i B t/n) \right) ^ n.
\end{align}, das heißt, dass wir einen Status unter $A + B $ weiterentwickeln können, indem Sie sich unter $A $ und $B $ allein weiterentwickeln.
Wenn wir die Evolution unter $A $ durch einen Vorgang darstellen, `A : (Double, Qubit[]) => Unit` der $e ^ {i t A} $ angewendet wird, wird die Darstellung des Trotters – Suzuki-Erweiterung in Bezug auf das Neuordnen von Aufruf Sequenzen deutlich.
Wenn ein Vorgang `U : ((Int, Double, Qubit[]) => Unit is Adj + Ctl` z. b. `A = U(0, _, _)` und `B = U(1, _, _)`, kann ein neuer Vorgang definiert werden, der den integralen `U` zum Zeitpunkt $t $ darstellt, indem Sequenzen der Form erstellt werden.

```qsharp
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
U(0, time / Float(nSteps), target);
U(1, time / Float(nSteps), target);
// ...
```

An diesem Punkt können wir nun die –-Erweiterung "Trotter" *ohne Verweis auf die Quantum-Mechanik*in Grund haben.
Die Erweiterung ist ein sehr spezielles Iterations Muster, das durch "$ \eqref {EQ: Trotter-Suzuki-0} $" motiviert ist.
Dieses Iterations Muster wird <xref:microsoft.quantum.canon.decomposeintotimestepsca>implementiert:

```qsharp
// The 2 indicates how many terms we need to decompose,
// while the 1 indicates that we are using the
// first-order Trotter–Suzuki decomposoition.
DecomposeIntoTimeStepsCA((2, U), 1);
```

Die Signatur von `DecomposeIntoTimeStepsCA` folgt einem allgemeinen Muster in Q#, bei dem Auflistungen, die entweder durch Arrays oder durch Elemente, die im laufenden Betrieb berechnet werden können, durch Tupel dargestellt werden, deren erste Elemente `Int` Werte sind, die ihre Längen angeben.

## <a name="putting-it-together-controlling-operations"></a>Kombinieren von Vorgängen: Steuern von Vorgängen ##

Schließlich baut der Kanon auf dem `Controlled`-Funktor auf, indem er zusätzliche Möglichkeiten zum Erstellen von Quantum-Vorgängen bereitstellt.
Es ist üblich, insbesondere bei der Quantum-Arithmetik, Vorgänge in anderen Compute-Zuständen als $ \ket{0\cdots 0} $ auszuführen.
Mithilfe der oben eingeführten Steuerungs Vorgänge und-Funktionen können wir in einer einzelnen Anweisung allgemeinere Quantum-Bedingungen verwenden.
Nun geht es um die Funktionsweise <xref:microsoft.quantum.canon.controlledonbitstring> (Sans-Typparameter), dann werden wir die Teile nacheinander aufteilen.
Als erstes müssen wir einen Vorgang definieren, der tatsächlich den Schwerpunkt der Implementierung des Steuer Elements auf willkürlichen Berechnungsbasis Zuständen leistet.
Dieser Vorgang wird jedoch nicht direkt aufgerufen, sodass wir `_` am Anfang des Namens hinzufügen, um anzugeben, dass es sich um eine Implementierung eines anderen Konstrukts an anderer Stelle handelt.

```qsharp
operation _ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl),
    controlRegister : Qubit[],
    targetRegister: Qubit[])
: Unit is Adj + Ctl
```

Beachten Sie, dass wir eine als `Bool` Array dargestellte Zeichenfolge mit Bits verwenden, die wir verwenden, um die gewünschte Anlage anzugeben, die auf den von uns angegebenen `oracle` Vorgang angewendet werden soll.
Da dieser Vorgang die Anwendung tatsächlich direkt durchführt, müssen wir auch die Steuer-und Ziel Register verwenden, die hier als `Qubit[]`dargestellt werden.

Als Nächstes stellen wir fest, dass die Steuerung des Berechnungs basierten Zustands $ \ket{\vec{s}} = \ket{s\_0 s\_1 \dpi s\_{n-1}} $ für eine Bitzeichenfolge $ \vec{s} $ durch Umwandeln von $ \ket{\vec{s}} $ in $ \ket{0\cdots 0} $ realisiert werden kann.
Insbesondere: $ \ket{\vec{s}} = X ^ {s\_0} \otimes x ^ {s\_1} \otimes \cdots \otimes X ^ {s\_{n-1}} \ket{0\cdots 0} $.
Seit $X ^ {\dagger} = x $ bedeutet dies, dass $ \ket{0\dots 0} = X ^ {s\_0} \otimes X ^ {s\_1} \otimes \cdots \otimes x ^ {s\_{n-1}} \ket{\vec{s}} $.
Daher können wir $P = x ^ {s\_0} \otimes X ^ {s\_1} \otimes \cdots \otimes X ^ {s\_{n-1}} $, Apply `Controlled oracle`und Transform Back to $ \vec{s} $ anwenden.
Diese Konstruktion ist genau `ApplyWith`, daher wird der Text des neuen Vorgangs entsprechend geschrieben:

```qsharp
{
    ApplyWithCA(
        ApplyPauliFromBitString(PauliX, false, bits, _),
        (Controlled oracle)(_, targetRegister),
        controlRegister
    );
}
```

Hier haben wir <xref:microsoft.quantum.canon.applypaulifrombitstring> verwendet, um $P $ anzuwenden, um das Ziel teilweise für die Verwendung mit `ApplyWith`anzuwenden.
Beachten Sie jedoch, dass wir die *Steuer* Element Registrierung in das gewünschte Formular umwandeln müssen, sodass wir den inneren Vorgang `(Controlled oracle)` auf dem *Ziel*teilweise anwenden.
Dadurch bleibt `ApplyWith` agieren, um das Steuerelement mit $P $ genau wie gewünscht zu Klammern.

An diesem Punkt könnten wir zwar das tun, aber es ist nicht zu erwarten, dass unser neuer Vorgang nicht wie das Anwenden des `Controlled`-funktors funktioniert.
Daher haben wir die Definition des neuen Ablauf steuerungskonzepts abgeschlossen, indem wir eine Funktion schreiben, die das Oracle zum Steuern benötigt und einen neuen Vorgang zurückgibt.
Auf diese Weise sieht die neue Funktion sehr ähnlich wie `Controlled`aus und zeigt, dass wir ganz einfach leistungsstarke neue Ablaufsteuerungskonstrukte mit Q# und dem Kanon definieren können:

```qsharp
function ControlledOnBitString(
    bits : Bool[],
    oracle: (Qubit[] => Unit is Adj + Ctl))
: ((Qubit[], Qubit[]) => Unit is Adj + Ctl) {
    return _ControlledOnBitString(bits, oracle, _, _);
}
```
