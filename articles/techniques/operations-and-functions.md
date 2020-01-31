---
title: 'Vorgänge und Funktionen: f #-Techniken | Microsoft-Dokumentation'
description: 'Vorgänge und Funktionen: Q #-Techniken'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 1fca20bb44cc42008f7d25d2fc71a39b962525c2
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820775"
---
# <a name="q-operations-and-functions"></a>F #-Vorgänge und-Funktionen

Q #-Programme bestehen aus mindestens einem *Vorgang* , bei dem die Nebeneffekte, die Quantum-Vorgänge auf Quantum-Daten haben können, und eine oder mehrere *Funktionen* , die Änderungen an klassischen Daten zulassen, beschrieben werden. Im Gegensatz zu Vorgängen werden Funktionen verwendet, um rein klassisches Verhalten zu beschreiben, und Sie haben keine Auswirkungen, außer wenn Sie klassische Ausgabewerte berechnen.

Jeder in Q # definierte Vorgang kann dann eine beliebige Anzahl anderer Vorgänge aufzurufen, einschließlich der integrierten systeminternen Vorgänge, die von der Sprache definiert werden. Die spezielle Methode, mit der diese systeminternen Vorgänge definiert werden, hängt vom Zielcomputer ab. Bei der Kompilierung wird jeder Vorgang als .NET-Klassentyp dargestellt, der den Ziel Computern bereitgestellt werden kann.

## <a name="defining-new-operations"></a>Definieren von neuen Vorgängen

Wie oben beschrieben, ist der grundlegendste Baustein eines in q # geschriebenen Quantum-Programms ein *Vorgang*, der entweder von klassischen .NET-Anwendungen aus aufgerufen werden kann, z. b. durch die Verwendung eines Simulators oder durch andere Vorgänge in q #.
Jeder Vorgang nimmt eine Eingabe an, erzeugt eine Ausgabe und gibt die Implementierung für eine oder mehrere Vorgangs Spezialisierungs Vorgänge an.
Beispielsweise wird durch den folgenden Vorgang nur eine standardmäßige Text Spezialisierung definiert, und es wird ein einzelnes Qubit als Eingabe benötigt. Anschließend wird der integrierte `X` Vorgang für diese Eingabe aufgerufen:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

Das Schlüsselwort `operation` beginnt die Vorgangs Definition, gefolgt vom Namen. Hier `BitFlip`.
Als nächstes wird der Typ der Eingabe als `Qubit`definiert, zusammen mit einem Namen `target`, um auf die Eingabe innerhalb des neuen Vorgangs zu verweisen.
Ebenso definiert das `Unit`, dass die Ausgabe des Vorgangs leer ist.
Dies wird ähnlich wie bei `void` in C# und anderen imperativen Sprachen verwendet und entspricht `unit` in F# und anderen funktionalen Sprachen.

> [!NOTE]
> Dies wird im folgenden ausführlicher erläutert, aber jeder Vorgang in Q # nimmt genau eine Eingabe an und gibt genau eine Ausgabe zurück.
> Anschließend werden mehrere Eingaben und Ausgaben mithilfe von *Tupeln*dargestellt, die mehrere Werte in einem einzelnen Wert zusammenfassen.
> Informell gesagt, dass Q # eine "tupelin tupelout"-Sprache ist.
> Nach diesem Konzept sollten `()` als "leeres" Tupel mit dem Typ "`Unit`" gelesen werden.

Innerhalb des neuen Vorgangs kann die Implementierung direkt innerhalb der-Deklaration angegeben werden, wenn nur die Implementierung der Standardtext Spezialisierung explizit angegeben werden muss. Außerdem ist es möglich, die Implementierungen von (z. b. eine oder mehrere `functor` Vorgänge) zu definieren, wie unten erläutert. Im obigen Beispiel besteht die einzige Anweisung darin, den integrierten f #-Vorgang <xref:microsoft.quantum.intrinsic.x>aufzurufen.

Vorgänge können auch interessantere Typen als `Unit`zurückgeben.
Der <xref:microsoft.quantum.intrinsic.m>-Vorgang gibt beispielsweise eine Ausgabe des Typs `Result`zurück, die angibt, dass eine Messung durchgeführt wurde. Die Ausgabe kann entweder von einem Vorgang an einen anderen Vorgang übergeben werden, oder Sie kann mit dem `let`-Schlüsselwort verwendet werden, um eine neue Variable zu definieren.
<!-- Link to UID for superdense conceptual and example documentation. -->
Dies ermöglicht die Darstellung der klassischen Berechnung, die mit Quantum-Vorgängen auf niedriger Ebene interagiert, wie z. b. in einer übergeordneten Codierung:

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a>Funktoren, Adjoint und gesteuert
Wenn ein Vorgang eine einheitliche Transformation implementiert, ist es möglich, zu definieren, wie der Vorgang beim *angleichen oder* *Steuern*erfolgt. Eine Adjoint-Spezialisierung eines Vorgangs gibt an, wie er bei umgekehrter Ausführung agiert, während eine kontrollierte Spezialisierung angibt, wie ein Vorgang angewendet wird, wenn er auf den Zustand eines Quantum-Register angewendet wird.
Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur: `is Adj + Ctl` im folgenden Beispiel deklariert werden. Die entsprechende Implementierung für jede solche implizit deklarierte Spezialisierung wird dann vom Compiler generiert. 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> Viele Vorgänge in Q # stellen einheitliche Gates dar.
> Wenn $U $ das einheitliche Gate ist, das durch einen Vorgang `U`dargestellt wird, stellt `Adjoint U` das einheitliche Gate $U ^ \dagger $ dar.

Wenn die Implementierung nicht vom Compiler generiert werden kann, kann Sie explizit angegeben werden. Solche expliziten Spezialisierungs Deklarationen können aus einer geeigneten Generierungs Direktive oder einer benutzerdefinierten Implementierung bestehen. Der oben genannte Code in `PrepareEntangledPair` z. b. Äquivalent zum folgenden Code, der explizite Spezialisierungs Deklarationen enthält: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
Das Schlüsselwort `auto` gibt an, dass der Compiler bestimmen soll, wie die Spezialisierungs Implementierung generiert werden soll.
Wenn der Compiler die Implementierung für eine bestimmte Spezialisierung nicht automatisch generieren kann oder wenn eine effizientere Implementierung angegeben werden kann, kann die Implementierung auch manuell definiert werden.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
Im obigen Beispiel gibt `adjoint invert;` an, dass die Adjoint-Spezialisierung generiert werden soll, indem Sie die Text Implementierung umkehren, und `controlled adjoint invert;` gibt an, dass die kontrollierte Adjoint-Spezialisierung generiert werden soll, indem Sie die angegebene Implementierung der kontrollierten Spezialisierung umkehren.

Weitere Beispiele hierfür finden Sie in der [Ablauf Steuerung in höherer Reihenfolge](xref:microsoft.quantum.concepts.control-flow).

Um eine Spezialisierung eines Vorgangs aufzurufen, verwenden Sie die Schlüsselwörter `Adjoint` oder `Controlled`.
So kann z. b. das oben beschriebene Codierungs Beispiel mit dem Adjoint von `PrepareEntangledPair` kompakter geschrieben werden, um den entzickten Zustand zurück in ein nicht verziges paar von Qubits umzuwandeln:

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

Beim Entwerfen von Vorgängen für die Verwendung mit Funktoren sind einige wichtige Einschränkungen zu beachten.
In den meisten Fällen können Spezialisierungs Vorgänge für einen Vorgang, der den Ausgabewert eines beliebigen anderen Vorgangs verwendet, nicht automatisch vom Compiler generiert werden, da er nicht eindeutig ist, wie die Anweisungen in einem solchen Vorgang neu angeordnet werden, um denselben Effekt zu erhalten.


## <a name="defining-new-functions"></a>Definieren neuer Funktionen

Q # ermöglicht außerdem das Definieren von *Funktionen*, die sich von Vorgängen unterscheiden, da Sie keine Auswirkungen auf die Berechnung eines Ausgabe Werts haben dürfen.
Insbesondere können Funktionen keine Vorgänge aufzurufen, auf Qubits reagieren, Zufallszahlen in Stichproben oder anderweitig abhängig von dem Zustand, der über den Eingabe Wert hinausgeht, auf eine Funktion setzen.
Folglich sind Q #-Funktionen *rein*, da Sie die gleichen Eingabewerte immer denselben Ausgabe Werten zuordnen.
Dadurch kann der Q #-Compiler sicher neu anordnen, wie und wann Funktionen beim Erstellen von Vorgangs speziationen aufgerufen werden.

Das Definieren einer Funktion funktioniert ähnlich wie ein Vorgang, mit dem Unterschied, dass für eine Funktion keine Adjoint-oder kontrollierten Spezialisierungs Funktionen definiert werden können.
Beispiel:

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
Wenn dies möglich ist, ist es hilfreich, Klassische Logik in Bezug auf Funktionen anstelle von Vorgängen zu schreiben, damit Sie von innerhalb von Vorgängen leichter verwendet werden kann.
Wenn wir z. b. `Square` als Vorgang geschrieben hätten, wäre der Compiler nicht in der Lage, zu garantieren, dass der Aufruf mit derselben Eingabe konsistent die gleichen Ausgaben erzeugt.

Um den Unterschied zwischen Funktionen und Vorgängen zu unterstreichen, sollten Sie das Problem der klassischen Stichprobenentnahme einer Zufallszahl aus einem f #-Vorgang in Erwägung gezogen

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Jedes Mal, wenn `U` aufgerufen wird, wird eine andere Aktion auf `target`ausgeführt.
Insbesondere kann der Compiler nicht garantieren, dass beim Hinzufügen einer `adjoint auto`-Spezialisierungs Deklaration zu `U`, `U(target); Adjoint U(target);` als Identität agiert (d. h. als No-OP).
Dies verstößt gegen die Definition des Adjoint, das wir in [Vektoren und Matrizen](xref:microsoft.quantum.concepts.vectors)erkannt haben, sodass das automatische Generieren einer Adjoint-Spezialisierung in einem Vorgang möglich ist, bei dem der Vorgang aufgerufen wurde <xref:microsoft.quantum.math.randomreal> die vom Compiler bereitgestellten Garantien unterbrechen würde. <xref:microsoft.quantum.math.randomreal> ist ein Vorgang, für den keine Adjoint-oder kontrollierte Version vorhanden ist.

Das Zulassen von Funktionsaufrufen, wie z. b. `Square`, ist darin sicherzustellen, dass der Compiler sicher sein kann, dass nur die Eingabe für `Square` beibehalten werden muss, damit die Ausgabe stabil bleibt.
Daher ist es einfach, diese Logik in anderen Funktionen und Vorgängen zu verwenden, damit Sie so viel Klassische Logik wie möglich in Functions isolieren kann.

## <a name="control-flow"></a>Ablaufsteuerung

Innerhalb einer Operation oder Funktion wird jede Anweisung in der richtigen Reihenfolge ausgeführt, ähnlich wie bei den gängigsten, imperativen, klassischen Sprachen.
Diese Ablauf Steuerung kann jedoch auf drei verschiedene Arten geändert werden:

- `if`-Anweisungen
- `for` Schleifen
- `repeat`-`until` Schleifen

Wir verzögern die Erörterung der letzteren, bis wir eine [Wiederholung von Wiederholungs Läufen (RUS bis Erfolg)](xref:microsoft.quantum.techniques.qubits#measurements) erörtern.
Die `if`-und `for` Ablaufsteuerungskonstrukte werden jedoch in den meisten klassischen Programmiersprachen als vertrauter bezeichnet.
Vor allem kann eine `if`-Anweisung eine Bedingung annehmen, auf die eine oder mehrere `elif` Anweisungen folgen können und mit einem `else`enden:

```qsharp
if (pauli == PauliX) {
    X(qubit);
} elif (pauli == PauliY) {
    Y(qubit);
} elif (pauli == PauliZ) {
    Z(qubit);
} else {
    fail "Cannot use PauliI here.";
}
```

Auf ähnliche Weise geben `for` Schleifen Iterationen über einen Bereich von ganzen Zahlen oder über die Elemente eines Arrays an:

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

Wichtig ist, dass `for` Schleifen und `if` Anweisungen sogar in Vorgängen verwendet werden können, für die Spezialisierungs Vorgänge automatisch generiert werden. In diesem Fall kehrt das Adjoint-Zeichen einer `for`-Schleife die Richtung um und nimmt das Adjoint der einzelnen Iterationen an.
Dies folgt dem Prinzip "Schuh-und-SOCKS": Wenn Sie das Einfügen von SOCKS und dann auf Schuhe rückgängig machen möchten, müssen Sie die einfügende Schuhe rückgängig machen und dann auf SOCKS setzen.
Es funktioniert ausgesprochen weniger gut, wenn Sie versuchen, die SOCKS zu wiederholen, während Sie Ihre Schuhe noch nicht nutzen!

## <a name="operations-and-functions-as-first-class-values"></a>Vorgänge und Funktionen als First-Class-Werte

Ein wichtiges Verfahren, um die Ablauf Steuerung und die klassische Logik mithilfe von Funktionen anstelle von Vorgängen zu überdenken, besteht darin, diese Vorgänge und Funktionen in Q # als *erste Klasse*zu verwenden.
Das heißt, Sie sind jeweils die einzelnen Werte in der Sprache.
Beispielsweise ist der folgende vollständig gültige Q #-Code, wenn ein wenig indirekt:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

Der Wert der Variablen, die im obigen Code Ausschnitt `ourH` ist, ist der Vorgang <xref:microsoft.quantum.intrinsic.h>, sodass wir diesen Wert wie jeder andere Vorgang abrufen können.
Dies ermöglicht es uns, Vorgänge zu schreiben, die Vorgänge als Teil Ihrer Eingabe ausführen und so die Konzepte der Ablauf Steuerung auf höherer Ordnung bilden.
Beispielsweise könnten wir uns vorstellen, einen Vorgang zu "quadrieren", indem wir ihn zweimal auf das gleiche Ziel-Qubit anwenden.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

In diesem Beispiel gibt der `=>` Pfeil, der im Typ `(Qubit => Unit)` angezeigt wird, an, dass das Eingabefeld `op` ein Vorgang ist, der als Eingabe den Typ `Qubit` annimmt und ein leeres Tupel als Ausgabe erzeugt.
Außerdem geben wir die Merkmale dieses Vorgangs Typs an, die die Informationen zu den unterstützten Funktoren enthalten.
Ein Vorgang vom Typ `(Qubit => Unit)` unterstützt weder den `Adjoint` noch den `Controlled`-Funktor. Wenn Sie angeben möchten, dass ein Vorgang dieses Typs z. b. den `Adjoint`-Funktor unterstützen muss, müssen wir ihn als adjointable deklarieren. Dies erfolgt mithilfe der-Anmerkung `is Adj` für den-Typ. Ebenso gibt `(Qubit => Unit is Ctl)` an, dass ein Vorgang dieses Typs den `Controlled`-Funktor unterstützt. Wir werden dies weiter untersuchen, wenn wir [types in Q #] (Xref: Microsoft. Quantum. Language. Type-Model) allgemeiner erörtern.

Vorerst betonen wir, dass wir auch Vorgänge als Teil der Ausgaben zurückgeben können, sodass wir einige Arten von klassischer bedingter Logik als klassische Funktion isolieren können, die eine Beschreibung eines Quantum-Programms in Form eines Vorgangs zurückgibt.
Als einfaches Beispiel sehen Sie sich das Beispiel für die teleportung an, in dem die Partei, die eine zwei-Bit-klassische Nachricht empfängt, die Nachricht verwenden muss, um Ihr Qubit in den richtigen teleportierten Zustand zu decodieren.
Wir könnten dies im Hinblick auf eine Funktion schreiben, die diese beiden klassischen Bits annimmt und den richtigen Decodierungs Vorgang zurückgibt.

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

Diese neue Funktion ist tatsächlich eine Funktion, denn wenn wir Sie mit denselben Werten von `hereBit` und `thereBit`nennen, erhalten wir immer denselben Vorgang.
Daher kann der Decoder sicher innerhalb von Vorgängen ausgeführt werden, ohne dass es darum geht, zu bedenken, wie die Decodierungs Logik mit den Definitionen der verschiedenen Vorgangs Spezialisierungs Maßnahmen interagiert.
Das heißt, wir haben die klassische Logik innerhalb einer Funktion isoliert und dem Compiler dadurch sichergestellt, dass der Funktions aufrufbedarf mit Straffreiheit neu angeordnet werden kann, solange die Eingabe beibehalten wird.

Wir können Funktionen auch als First-Class-Werte behandeln, da wir bei der Erörterung von [Vorgängen und Funktionstypen](#operations-and-functions-as-first-class-values)ausführlicher sehen werden.

## <a name="partially-applying-operations-and-functions"></a>Teilweise Anwenden von Vorgängen und Funktionen

Wir können mit Funktionen, die Vorgänge mithilfe einer *partiellen Anwendung*zurückgeben, wesentlich mehr tun, in der wir einen oder mehrere Teile der Eingabe für eine Funktion oder einen Vorgang bereitstellen können, ohne Sie tatsächlich aufrufen zu müssen. Wenn Sie z. b. das obige `ApplyTwice` Beispiel beachten, können wir angeben, dass wir nicht sofort angeben möchten, auf welchem Qubit der Eingabevorgang angewendet werden soll:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

In diesem Fall enthält die lokale Variable `twiceOp` den teilweise angewendeten Vorgang `ApplyTwice(op, _)`, bei dem noch nicht angegebene Teile der Eingabe durch `_`angegeben werden.
Wenn `twiceOp` in der nächsten Zeile aufgerufen wird, übergeben wir als Eingabe an den teilweise angewendeten Vorgang alle verbleibenden Teile der Eingabe für den ursprünglichen Vorgang.
Folglich ist der obige Code Ausschnitt effektiv identisch mit dem Aufruf von `ApplyTwice(op, target)` direkt. speichern Sie, damit wir eine neue lokale Variable eingeführt haben, die es uns ermöglicht, den Aufruf zu verzögern, während einige Teile der Eingabe bereitgestellt werden.

Da ein Vorgang, der teilweise angewendet wurde, erst aufgerufen wird, wenn die gesamte Eingabe bereitgestellt wurde, können wir Vorgänge auf sichere Weise sogar aus Funktionen anwenden.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

Im Prinzip könnte die klassische Logik in `SquareOperation` viel komplizierter sein, aber Sie ist weiterhin vom Rest eines Vorgangs isoliert, indem die Garantien, die der Compiler über Funktionen bereitstellen kann.
Diese Vorgehensweise wird in der Q #-Standardbibliothek verwendet, um die klassische Ablauf Steuerung so auszudrücken, dass Sie in quantenprogrammen problemlos verwendet werden kann.
