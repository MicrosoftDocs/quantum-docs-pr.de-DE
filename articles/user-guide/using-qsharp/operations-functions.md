---
title: 'Vorgänge und Funktionen in Q #'
description: Definieren und aufzurufen von Vorgängen und Funktionen sowie der kontrollierten und der Adjoint-Vorgangs Spezialisierung.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
ms.openlocfilehash: bc9695b85b68807801225ccbc903a4622b450768
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431069"
---
# <a name="operations-and-functions-in-q"></a>Vorgänge und Funktionen in Q #

## <a name="defining-new-operations"></a>Definieren von neuen Vorgängen

Vorgänge sind das Kernstück von Q #.
Nach der Deklaration können Sie entweder von klassischen .NET-Anwendungen aus aufgerufen werden, z. b. durch die Verwendung eines Simulators oder durch andere Vorgänge in Q #.
Jeder in Q # definierte Vorgang kann dann eine beliebige Anzahl anderer Vorgänge aufzurufen, einschließlich der integrierten systeminternen Vorgänge, die von der Sprache definiert werden. Die spezielle Methode, mit der diese systeminternen Vorgänge definiert werden, hängt vom Zielcomputer ab.
Bei der Kompilierung wird jeder Vorgang als .NET-Klassentyp dargestellt, der den Ziel Computern bereitgestellt werden kann.

Jede f #-Quelldatei kann eine beliebige Anzahl von Vorgängen definieren.
Vorgangs Namen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit Typ-oder Funktionsnamen verursachen.

Eine Vorgangs Deklaration besteht aus dem Schlüsselwort `operation` , gefolgt von dem Symbol, das den Namen des Vorgangs enthält, einem typisierten bezeichnertupel, das die Argumente für den Vorgang definiert, einem Doppelpunkt `:` , einer Typanmerkung, die den Ergebnistyp des Vorgangs beschreibt, optional einer Anmerkung mit den Vorgangs Merkmalen, einer öffnenden geschweifte Klammer `{` , dem Text der Vorgangs Deklaration und einer `}`

Jeder Vorgang nimmt eine Eingabe an, erzeugt eine Ausgabe und gibt die Implementierung für eine oder mehrere Vorgangs Spezialisierungs Vorgänge an.
Weitere Informationen zu den möglichen Spezialisierungsmöglichkeiten und zum Definieren/anrufen finden Sie weiter unten.
Sehen Sie sich den folgenden Vorgang an, der nur eine Standard Textzeile definiert und ein einzelnes Qubit als Eingabe annimmt und dann den integrierten <xref:microsoft.quantum.intrinsic.x> Vorgang für diese Eingabe aufruft:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

Das Schlüsselwort `operation` beginnt mit der Vorgangs Definition, gefolgt vom Namen `BitFlip` .
Als nächstes wird der Typ der Eingabe als definiert `Qubit` , zusammen mit einem Namen `target` für den Verweis auf die Eingabe innerhalb des neuen Vorgangs.
Ebenso definiert das, `Unit` dass die Ausgabe des Vorgangs leer ist.
Dies wird ähnlich wie `void` in c# und anderen imperativen Sprachen verwendet und entspricht `unit` in F # und anderen funktionalen Sprachen.

Vorgänge können auch interessantere Typen als zurückgeben `Unit` .
Der- <xref:microsoft.quantum.intrinsic.m> Vorgang gibt beispielsweise eine Ausgabe vom Typ zurück `Result` , die angibt, dass eine Messung durchgeführt wurde. Die Ausgabe kann entweder von einem Vorgang an einen anderen Vorgang übergeben werden, oder Sie kann mit dem `let` Schlüsselwort verwendet werden, um eine neue Variable zu definieren.

Dies ermöglicht die Darstellung der klassischen Berechnung, die mit Quantum-Vorgängen auf niedriger Ebene interagiert, wie z. b. in einer über [geordneten Codierung](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> Jeder Vorgang in Q # nimmt genau eine Eingabe an und gibt genau eine Ausgabe zurück.
> Anschließend werden mehrere Eingaben und Ausgaben mithilfe von *Tupeln*dargestellt, die mehrere Werte in einem einzelnen Wert zusammenfassen.
> Informell gesagt, dass Q # eine "tupelin tupelout"-Sprache ist.
> Nach diesem Konzept `()` sollte dann als "leeres" Tupel mit dem Typ gelesen werden `Unit` .


## <a name="controlled-and-adjoint-operations"></a>Kontrollierte und Adjoint-Vorgänge

*Wenn ein* Vorgang eine einheitliche Transformation implementiert, wie dies bei vielen Vorgängen in Q # der Fall ist, ist es möglich, zu definieren, wie der Vorgang beim angleichen oder *Steuern*agiert. Eine *Adjoint* -Spezialisierung eines Vorgangs gibt an, wie die "Umkehrung" des Vorgangs agiert, während eine *kontrollierte* Spezialisierung angibt, wie ein Vorgang funktioniert, wenn die Anwendung auf den Zustand eines bestimmten Quantum-Registers angewendet wird.

Adjoints von Quantum-Vorgängen sind für viele Aspekte von Quantum Computing von entscheidender Bedeutung. Weiter unten im Abschnitt " [Konjugationen](#conjugations) " finden Sie eine solche Situation, die zusammen mit einer nützlichen Q #-Programmiertechnik erläutert wird.

Bei der kontrollierten Version eines Vorgangs handelt es sich um einen neuen Vorgang, der den Basis Vorgang effektiv anwendet, wenn sich alle Steuerelement-Qubits in einem angegebenen Zustand befinden.
Wenn sich die Steuerelement-Qubits in der superposition befinden, wird der Basis Vorgang einheitlich auf den entsprechenden Teil der superposition angewendet.
Folglich werden kontrollierte Vorgänge häufig zum Generieren von entanglement verwendet.

Natürlich könnte auch eine *kontrollierte Adjoint* -Spezialisierung vorhanden sein, die die kontrollierte Anwendung des Adjoint eines Vorgangs angibt.

> [!NOTE]
> Wenn $U $ die von einem Vorgang implementierte einheitliche Transformation ist `U` , `Adjoint U` stellt die einheitliche Transformation $U ^ \dagger $ dar, die die komplexe konjugierte Transformation ist.
> Wenn Sie einen Vorgang nacheinander anwenden und dessen Adjoint in einen Zustand versetzt wird, bleibt der Zustand unverändert, wie in der Tatsache veranschaulicht, dass $UU ^ \dagger = U ^ \dagger U = \id $ die Identitätsmatrix ist.
> Die einheitliche Darstellung eines kontrollierten Vorgangs ist etwas flexibler, aber weitere Informationen finden Sie unter [Quantum Computing Concepts: Multiple Qubits](xref:microsoft.quantum.concepts.multiple-qubits).

Im folgenden Abschnitt wird beschrieben, wie Sie diese verschiedenen Spezialisierungs Informationen in Ihrem Q #-Code aufzurufen.
Im folgenden wird ausführlich erläutert, wie Sie Vorgänge für deren Unterstützung definieren.

### <a name="calling-operation-specializations"></a>Aufrufen von Vorgangs Spezialisierungs Vorgängen

Ein *Funktor* in Q # ist eine Factory, die einen neuen Vorgang aus einem anderen Vorgang definiert.
Die zwei standardfunktoren in Q # sind `Adjoint` und `Controlled` .

Funktoren haben Zugriff auf die Implementierung des Basis Vorgangs, wenn die Implementierung des neuen Vorgangs definiert wird.
Daher können Funktoren komplexere Funktionen als herkömmliche Funktionen höherer Ebene ausführen. Funktoren haben keine Darstellung im Q #-Typsystem. Daher ist es derzeit nicht möglich, Sie an eine Variable zu binden oder Sie als Argumente zu übergeben. 

Ein Funktor wird verwendet, indem er auf einen Vorgang angewendet und ein neuer Vorgang zurückgegeben wird.
Beispielsweise wird der Vorgang, der sich aus der Anwendung des `Adjoint` funktors auf den Vorgang ergibt, `Y` als geschrieben `Adjoint Y` .
Der neue Vorgang kann dann wie jeder andere Vorgang aufgerufen werden.
Damit ein Vorgang die Anwendung des `Adjoint` -und/oder- `Controlled` funktors unterstützt, muss der Rückgabetyp unbedingt sein `Unit` . 

#### <a name="adjoint-functor"></a>`Adjoint`Funktionselement

Folglich `Adjoint Y(q1)` wendet das Adjoint-Funktor auf den `Y` -Vorgang an, um einen neuen-Vorgang zu generieren, und wendet diesen neuen Vorgang auf an `q1` .
Der neue Vorgang hat dieselbe Signatur und denselben Typ wie der Basis Vorgang `Y` .
Der neue-Vorgang ermöglicht insbesondere auch `Adjoint` , und lässt nur dann zu, wenn `Controlled` der Basis Vorgang durchgeführt wurde.
Der Adjoint-Funktor ist eine eigene Umkehrung. Das heißt, `Adjoint Adjoint Op` ist immer identisch mit `Op` .

#### <a name="controlled-functor"></a>`Controlled`Funktionselement

Entsprechend `Controlled X(controls, target)` wendet den gesteuerten Funktor auf den `X` -Vorgang an, um einen neuen-Vorgang zu generieren, und wendet diesen neuen-Vorgang auf `controls` und an `target` .

> [!NOTE]
> In Q # nehmen kontrollierte Versionen immer ein Array von Steuerelement-Qubits auf, und der angegebene Zustand ist immer, wenn alle Steuerelement-Qubits den Status "Compu()" (" `PauliZ` `One` $ \ket $") aufweisen {1} .
> Das Steuern auf der Grundlage anderer Zustände kann erreicht werden, indem der entsprechende einheitliche Vorgang auf die Steuerungs Qubits vor dem kontrollierten Vorgang angewendet und dann nach dem kontrollierten Vorgang die Umkehrung des einheitlichen Vorgangs angewendet wird.
> Wenn Sie z. b `X` . einen Vorgang vor und nach einer kontrollierten Operation auf ein Steuerelement-Qubit anwenden, führt der Vorgang zu einer Steuerung des `Zero` Zustands ($ \ket {0} $) für dieses Qubit. Wenn Sie einen `H` Vorgang vor und nach anwenden, wird die Kontrolle über den `PauliX` `One` Zustand, d. h.-1 eigen Wert von Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ anstelle des `PauliZ` `One` Zustands.

Bei einem Vorgangs Ausdruck kann ein neuer Vorgangs Ausdruck mithilfe des `Controlled` funktors gebildet werden.
Die Signatur des neuen Vorgangs basiert auf der Signatur des ursprünglichen Vorgangs.
Der Ergebnistyp ist identisch, aber der Eingabetyp ist ein zwei Tupel mit einem Qubit-Array, das die Steuerelement-Qubit (s) als erstes Element und die Argumente des ursprünglichen Vorgangs als zweites Element enthält.
Der neue-Vorgang unterstützt `Controlled` , und unterstützt `Adjoint` nur dann, wenn der ursprüngliche Vorgang durchgeführt wurde.

Wenn für den ursprünglichen Vorgang nur ein einzelnes Argument verwendet wurde, wird hier die entsprechgabe von Singleton-Tupeln berücksichtigt.
Beispiels `Controlled X` Weise ist die gesteuerte Version des `X` Vorgangs. 
`X`weist den Typ auf `(Qubit => Unit is Adj + Ctl)` , `Controlled X` hat also `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` den Typ; aufgrund der Äquivalenz von Singleton-Tupeln ist dies identisch mit `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

Wenn der Basis Vorgang mehrere Argumente benötigt hat, denken Sie daran, die entsprechenden Argumente der kontrollierten Version des Vorgangs in Klammern einzuschließen, um Sie in ein Tupel zu konvertieren.
Beispiels `Controlled Rz` Weise ist die gesteuerte Version des `Rz` Vorgangs. 
`Rz`weist den Typ auf `((Double, Qubit) => Unit is Adj + Ctl)` , hat also den `Controlled Rz` Typ `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .
Daher ist `Controlled Rz(controls, (0.1, target))` ein gültiger Aufruf von `Controlled Rz` (Beachten Sie die Klammern `0.1, target` ).

Als weiteres Beispiel `CNOT(control, target)` kann als implementiert werden `Controlled X([control], target)` . Wenn ein Ziel von 2 Steuerungs Qubits (ccnot) gesteuert werden soll, können wir die- `Controlled X([control1, control2], target)` Anweisung verwenden.

#### `Controlled Adjoint` 

Das `Controlled` -und das- `Adjoint` funktorin werden angewendet, sodass es keinen Unterschied zwischen dem Anwenden von `Controlled Adjoint Op` oder gibt `Adjoint Controlled Op`


## <a name="defining-controlled-and-adjoint-implementations"></a>Definieren von kontrollierten und Adjoint-Implementierungen

In den ersten Beispielen oben werden die Vorgänge `BitFlip` und `DecodeSuperdense` mit Signaturen `(Qubit => Unit)` `((Qubit, Qubit) => (Result, Result))` bzw. definiert.
Wie z. b. `DecodeSuperdense` Messungen, ist es kein einheitlicher Vorgang. Daher könnten weder die kontrollierten noch die nicht zusammenhängenden Spezialisierungs Maßnahmen vorhanden sein `Unit` .
Da jedoch `BitFlip` einfach der einheitliche <xref:microsoft.quantum.intrinsic.x> Vorgang durchführt, können wir ihn mit beiden Spezialisierungs Vorgängen definieren.

Hier wird ausführlich erläutert, wie Sie das vorhanden sein von spezialisierern in Ihre f #-Vorgangs Deklarationen einschließen, sodass Sie in Verbindung mit den `Adjoint` -und/oder-Funktoren aufgerufen werden können `Controlled` .
Im [folgenden](#circumstances-for-validly-defining-specializations)werden einige der Situationen beschrieben, in denen es entweder gültig oder nicht gültig ist, bestimmte Spezialisierungs-zu deklarieren.

Vorgangs Merkmale definieren, welche Arten von functoren auf den deklarierten Vorgang angewendet werden können und welche Auswirkungen Sie haben. Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur deklariert werden, insbesondere über eine Anmerkung mit den Vorgangs Merkmalen: entweder `is Adj` , `is Ctl` oder `is Adj + Ctl` .
Die tatsächliche Implementierung jeder Spezialisierung kann entweder *implizit* oder *explizit* definiert werden.

### <a name="implicitly-specifying-implementations"></a>Implizit angeben von Implementierungen

In diesem Fall besteht der Text der Vorgangs Deklaration ausschließlich aus der Standard Implementierung. Zum Beispiel:

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
Hier wird die entsprechende Implementierung für jede solche implizit deklarierte Spezialisierung automatisch vom Compiler generiert, die ausgeführt werden soll, wenn `Adjoint` die `Controlled` Funktoren oder verwendet werden.

Ein-Rückruf würde also dazu führen, dass `Adjoint PrepareEntangledPair` der Compiler das Adjoint von `CNOT` und dann das Adjoint von implementiert `H` .
Diese einzelnen Vorgänge sind beide selbst Adjoint, sodass der resultierende `Adjoint PrepareEntangledPair` Vorgang einfach aus der Anwendung `CNOT(here, there)` und dann besteht `H(here)` .
Daher können wir dieses Beispiel verwenden, um das `DecodeSuperdense` obige Beispiel mit einem kompakteren zu schreiben, indem wir das Adjoint von verwenden `PrepareEntangledPair` , um den entzickten Zustand wieder in ein nicht verwinkelter Qubits-paar umzuwandeln:

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

Die-Anmerkung mit den Vorgangs Merkmalen in der Deklaration ist hilfreich, um sicherzustellen, dass der Compiler automatisch andere Spezialisierungs Vorgänge auf der Grundlage der Standard Implementierung generiert. 

Beim Entwerfen von Vorgängen für die Verwendung mit Funktoren sind einige wichtige Einschränkungen zu beachten.
In den meisten Fällen können Spezialisierungs Vorgänge für einen Vorgang, der den Ausgabewert eines beliebigen anderen Vorgangs verwendet, nicht automatisch vom Compiler generiert werden, da er *nicht* eindeutig ist, wie die Anweisungen in einem solchen Vorgang neu angeordnet werden, um denselben Effekt zu erhalten.

Daher ist es häufig hilfreich, die verschiedenen Implementierungen explizit anzugeben.

### <a name="explicitly-specifying-implementations"></a>Explizite Angabe von Implementierungen

Wenn die Implementierung nicht vom Compiler generiert werden kann, kann Sie explizit angegeben werden. Solche expliziten Spezialisierungs Deklarationen können aus einer geeigneten *Generierungs Direktive* oder einer benutzerdefinierten Implementierung bestehen.
Hier finden Sie die vollständige Palette der Möglichkeiten, mit folgenden Beispielen.


#### <a name="explicit-specialization-declarations"></a>Explizite Spezialisierungs Deklarationen

F #-Vorgänge können die folgenden expliziten Spezialisierungs Deklarationen enthalten:

- Die `body` Spezialisierung gibt die Implementierung des Vorgangs ohne angewendete Funktoren an.
- Die `adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit `Adjoint` angewendetem Funktionselement an.
- Die `controlled` Spezialisierung gibt die Implementierung des Vorgangs mit `Controlled` angewendetem Funktionselement an.
- Die `controlled adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit den `Adjoint` `Controlled` angewendeten-und-Funktoren an.
  Diese Spezialisierung kann auch benannt werden `adjoint controlled` , da die beiden Funktoren in den Weg gehen.


Eine Vorgangs Spezialisierung besteht aus dem Spezialisierungs Kennzeichen (z. b. `body` oder `adjoint` usw.), gefolgt von einem der folgenden:

- Eine explizite Deklaration, wie unten beschrieben.
- Eine- *Direktive* , die dem Compiler mitteilt, *wie* die Spezialisierung generiert werden soll, einer der folgenden:
  - `intrinsic`Gibt an, dass die Spezialisierung vom Zielcomputer bereitgestellt wird.
  - `distribute`, die mit den `controlled` Spezialisierungs-und-Spezialisierungs-verwendet werden kann `controlled adjoint` .
    Bei Verwendung mit `controlled` wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in angewendet wird `body` .
    Bei Verwendung mit `controlled adjoint` wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in der Spezialisierung anwendet `adjoint` .
  - `invert`Gibt an, dass der Compiler die `adjoint` Spezialisierung durch Umkehren der berechnen soll `body` , d. h., die Reihenfolge der Vorgänge wird umgekehrt und das Adjoint-Attribut auf jeden angewendet.
    Wenn Sie mit verwendet `adjoint controlled` wird, gibt dies an, dass der Compiler die Spezialisierung durch Umkehren der `controlled` Spezialisierung berechnen soll.
  - `self`, um anzugeben, dass die Adjoint-Spezialisierung mit der Spezialisierung identisch ist `body` .
    Dies gilt für die `adjoint` Spezialisierungs-und- `adjoint controlled` Spezialisierungs-.
    Für `adjoint controlled` `self` impliziert, dass die `adjoint controlled` Spezialisierung mit der Spezialisierung identisch ist `controlled` .
  - `auto`, um anzugeben, dass der Compiler eine entsprechende anzuwendende Direktive auswählen soll.
    `auto`darf nicht für die Spezialisierung verwendet werden `body` .

Die-Direktiven und `auto` alle erfordern ein Schließ Endes Semikolon `;` .
Die- `auto` Direktive wird in die folgende Generierungs Direktive aufgelöst, wenn eine explizite Deklaration von `body` bereitgestellt wird:

- Die `adjoint` Spezialisierung wird gemäß der-Direktive generiert `invert` .
- Die `controlled` Spezialisierung wird gemäß der-Direktive generiert `distribute` .
- Die `adjoint controlled` Spezialisierung wird gemäß der-Direktive generiert `invert` , wenn eine explizite Deklaration für `controlled` angegeben ist, aber nicht für `adjoint` , und `distribute` andernfalls.

> [!TIP]   
> Wenn es sich um einen eigenständigen Vorgang handelt, geben Sie entweder die Adjoint-oder die kontrollierte Adjoint-Spezialisierung mithilfe der Generations Direktive explizit `self` an, damit der Compiler diese Informationen für Optimierungszwecke nutzen kann.

Eine Spezialisierungs Deklaration, die eine benutzerdefinierte Implementierung enthält, besteht aus einem argumenttupel, gefolgt von einem Anweisungsblock mit dem Q #-Code, der die Spezialisierung implementiert.
In der Argumentliste `...` wird verwendet, um die Argumente darzustellen, die für den Vorgang als Ganzes deklariert werden.
Für `body` und `adjoint` sollte die Argumentliste immer sein `(...)` . bei `controlled` und `adjoint controlled` sollte die Argumentliste ein Symbol sein, das das Array von Steuerelement-Qubits, gefolgt von `...` , in Klammern darstellt, z. b `(controls,...)` ..

### <a name="examples"></a>Beispiele

Eine Vorgangs Deklaration kann so einfach wie die folgende sein, die den primitiven Pauli X-Vorgang definiert:

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
Beachten Sie, dass das Adjoint des Pauli X-Vorgangs mit der-Direktive definiert ist, `self` da definitionsgemäß `X` eine eigene Umkehrung ist.

Der `PrepareEntangledPair` oben genannte Code entspricht beispielsweise dem folgenden Code, der explizite Spezialisierungs Deklarationen enthält: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
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

#### <a name="user-defined-specialization-implementation"></a>Implementierung benutzerdefinierter Spezialisierungen

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
Im obigen Beispiel gibt an, `adjoint invert;` dass die Adjoint-Spezialisierung durch das Umkehren der Text Implementierung generiert werden soll, und `controlled adjoint invert;` gibt an, dass die kontrollierte Adjoint-Spezialisierung generiert werden soll, indem die angegebene Implementierung der kontrollierten Spezialisierung umgekehrt wird.

Wenn eine oder mehrere Spezialisierungen neben dem Standardtext explizit deklariert werden müssen, muss die Implementierung für den Standardtext ebenfalls in eine passende Spezialisierungs Deklaration integriert werden:

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a>Umstände für das valide definieren von Spezialisierungs Informationen

#### <a name="operation-declarations-with-adjointcontrolled"></a>Vorgangs Deklarationen mit Adjoint/kontrolliertem

Es ist zulässig, einen Vorgang ohne Adjoint oder kontrollierte Versionen anzugeben. Beispielsweise haben Messvorgänge keine, da Sie nicht invertierbar oder steuerbar sind.

Ein-Vorgang unterstützt die- `Adjoint` und/oder- `Controlled` Funktoren, wenn die-Deklaration eine implizite oder explizite Deklaration der jeweiligen Spezialisierungs Elemente enthält.

Eine explizit deklarierte Adjoint/gesteuerte Spezialisierung impliziert das vorhanden sein einer Adjoint/kontrollierten Spezialisierung. 

Bei einem Vorgang, dessen Text Wiederholungs-bis-Erfolg-Schleifen, Set-Anweisungen, Messungen, Rückgabe Anweisungen oder Aufrufe von anderen Vorgängen enthält, die das Funktor nicht unterstützen `Adjoint` , ist das automatische Erstellen einer Adjoint-Spezialisierung nach der- `invert` oder- `auto` Direktive nicht möglich.

Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die das `Controlled` Funktor nicht unterstützen, ist das automatische Erstellen einer kontrollierten Spezialisierung nach der- `distribute` oder- `auto` Direktive nicht möglich.

#### <a name="controlled-adjoint"></a>Kontrollierter Adjoint

Die kontrollierte Adjoint-Version eines Vorgangs gibt an, wie eine Quantum-gesteuerte Version des Adjoint-Vorgangs des Vorgangs implementiert wird.
Es ist zulässig, einen Vorgang ohne kontrollierte Adjoint-Version anzugeben. Messvorgänge haben beispielsweise keine kontrollierte Adjoint-Version, da Sie weder steuerbar noch invertierbar sind.

Eine kontrollierte Adjoint-Spezialisierung für einen Vorgang muss nur dann vorhanden sein, wenn sowohl ein Adjoint-als auch eine gesteuerte Spezialisierung vorhanden sind. In diesem Fall wird das vorhanden sein der kontrollierten Adjoint-Spezialisierung abgeleitet, und vom Compiler wird eine entsprechende Spezialisierung generiert, wenn keine Implementierung explizit definiert wurde. 

Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die nicht über eine kontrollierte Adjoint-Version verfügen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach der- `invert` ,- `distribute` oder- `auto` Direktive nicht möglich.


### <a name="type-compatibility"></a>Typkompatibilität

Ein Vorgang mit zusätzlichen Funktoren, die unterstützt werden, kann überall dort verwendet werden, wo ein Vorgang mit weniger Funktoren, jedoch mit derselben Signatur erwartet wird.
Beispielsweise kann ein Vorgang des Typs `(Qubit => Unit is Adj)` überall dort verwendet werden, wo ein Vorgang des Typs `(Qubit => Unit)` erwartet wird.

Q # ist in Bezug auf Aufruf Bare Rückgabe Typen *kovariant* : ein Aufruf bares Element, das einen Typ zurückgibt, `'A` ist mit einem Aufruf baren Element mit dem gleichen Eingabetyp und einem Ergebnistyp kompatibel, der `'A` mit kompatibel ist.

Q # ist in Bezug auf Eingabetypen *kontra Variant* : ein Aufruf bares Element, das einen Typ `'A` als Eingabe annimmt, ist mit einem Aufruf baren mit demselben Ergebnistyp und einem Eingabetyp kompatibel, der mit kompatibel ist `'A` .

Das heißt, dass die folgenden Definitionen gegeben sind:

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

Folgendes gilt:

- Die-Funktion `ConjugateInvertWith` kann mit einem `inner` Argument von oder aufgerufen `Invert` werden `ApplyUnitary` .
- Die Funktion `ConjugateUnitaryWith` kann mit einem `inner` Argument von aufgerufen werden `ApplyUnitary` , aber nicht `Invert` .
- Ein Wert vom Typ `(Qubit[] => Unit is Adj + Ctl)` kann von zurückgegeben werden `ConjugateInvertWith` .

> [!IMPORTANT]
> F # 0,3 hat einen signifikanten Unterschied im Verhalten von benutzerdefinierten Typen eingeführt.

Benutzerdefinierte Typen werden als umschließende Version des zugrunde liegenden Typs und nicht als Untertyp behandelt.
Dies bedeutet, dass ein Wert eines benutzerdefinierten Typs nicht verwendbar ist, wenn ein Wert des zugrunde liegenden Typs erwartet wird.


### <a name="conjugations"></a>Konjugationen

Im Gegensatz zu klassischen Bits ist das Freigeben von Quantum-Speicher etwas komplizierter, da das Blind Zurücksetzen von Qubits unerwünschte Auswirkungen auf die verbleibende Berechnung haben kann, wenn die Qubits noch entkoppelt sind. Dies kann vermieden werden, indem Berechnungen vor der Freigabe des Arbeitsspeichers ordnungsgemäß durchgeführt werden. Ein gängiges Muster in Quantum Computing ist daher Folgendes: 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

Ab unserer Version 0,9 wird eine Konjugations Anweisung unterstützt, die die oben beschriebene Transformation implementiert. Mit dieser Anweisung kann der Vorgang `ApplyWith` folgendermaßen implementiert werden:

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
Eine solche Konjugation-Anweisung wird deutlich nützlicher, wenn die äußere und die innere Transformation nicht als Vorgänge verfügbar sind, sondern eher durch einen Block, der aus mehreren Anweisungen besteht, beschreibbar ist. 

Die umgekehrte Transformation für die-Anweisungen, die im-Block innerhalb von definiert sind, wird automatisch vom Compiler generiert und nach Abschluss von Apply-Block ausgeführt.
Da alle änderbaren Variablen, die als Teil des Blocks innerhalb von verwendet werden, im Apply-Block nicht wieder hergestellt werden können, ist die generierte Transformation garantiert das Adjoint der Berechnung im within-Block. 


## <a name="defining-new-functions"></a>Definieren neuer Funktionen

Funktionen sind rein deterministische, klassische Routinen in Q #, die sich von Vorgängen unterscheiden, da Sie keine Auswirkungen auf die Berechnung eines Ausgabe Werts haben können.
Insbesondere können Funktionen keine Vorgänge aufzurufen. reagieren, zuordnen oder ausleihen von Qubits Stichproben von Zufallszahlen oder hängt anderweitig von dem Zustand ab, der über den Eingabe Wert zu einer Funktion hinausgeht.
Folglich sind Q #-Funktionen *rein*, da Sie die gleichen Eingabewerte immer denselben Ausgabe Werten zuordnen.
Dadurch kann der Q #-Compiler sicher neu anordnen, wie und wann Funktionen beim Erstellen von Vorgangs speziationen aufgerufen werden.

Jede f #-Quelldatei kann eine beliebige Anzahl von Funktionen definieren.
Funktionsnamen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit Vorgangs-oder Typnamen aufweisen.

Das Definieren einer Funktion funktioniert ähnlich wie ein Vorgang, mit dem Unterschied, dass für eine Funktion keine Adjoint-oder kontrollierten Spezialisierungs Funktionen definiert werden können.
Beispiel:

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

oder 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a>Klassische Logik in Functions = = Good

Wenn dies möglich ist, ist es hilfreich, Klassische Logik in Bezug auf Funktionen anstelle von Vorgängen zu schreiben, damit Sie von innerhalb von Vorgängen leichter verwendet werden kann.
Wenn Sie z. b. die `Square` obige Deklaration als *Vorgang*geschrieben hätten, wäre der Compiler nicht in der Lage, zu garantieren, dass der Aufruf mit derselben Eingabe konsistent die gleichen Ausgaben erzeugt.

Um den Unterschied zwischen Funktionen und Vorgängen zu unterstreichen, sollten Sie das Problem der klassischen Stichprobenentnahme einer Zufallszahl aus einem f #-Vorgang in Erwägung gezogen

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Jedes Mal `U` , wenn aufgerufen wird, wird eine andere Aktion für ausgeführt `target` .
Insbesondere kann der Compiler nicht garantieren, dass, wenn wir eine `adjoint auto` Spezialisierung-Deklaration hinzugefügt `U` haben, `U(target); Adjoint U(target);` als Identität agiert (d. h. als No-OP).
Dies verstößt gegen die Definition des Adjoint, das in [Vektoren und Matrizen](xref:microsoft.quantum.concepts.vectors)aufgetreten ist, sodass das automatische Generieren einer Adjoint-Spezialisierung in einem Vorgang, bei dem der Vorgang aufgerufen wurde, <xref:microsoft.quantum.math.randomreal> die vom Compiler bereitgestellten Garantien unterbrechen würde <xref:microsoft.quantum.math.randomreal> . ist ein Vorgang, für den keine Adjoint-oder kontrollierte Version vorhanden ist.

Das Zulassen von Funktionsaufrufen wie `Square` ist jedoch sicher, dass der Compiler sicher sein kann, dass nur die Eingabe in beibehalten werden muss, damit die `Square` Ausgabe stabil bleibt.
Daher ist es einfach, diese Logik in anderen Funktionen und Vorgängen zu verwenden, damit Sie so viel Klassische Logik wie möglich in Functions isolieren kann.


## <a name="generic-type-parameterized-callables"></a>Generische (typparametrisierte) callables

Viele Funktionen und Vorgänge, die wir möglicherweise definieren möchten, sind nicht wirklich stark von den Typen Ihrer Eingaben abhängig, sondern verwenden nur implizit ihre Typen über eine andere Funktion oder einen anderen Vorgang.
Sehen Sie sich beispielsweise das *Karten* Konzept an, das vielen funktionalen Sprachen gemeinsam ist. bei Angabe einer Funktion $f (x) $ und einer Auflistung von Werten $ \{ x_1, x_2, \dots, x_n \} $ gibt MAP eine neue Auflistung $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $ zurück.
Um dies in Q # zu implementieren, können wir diese Funktionen als erste Klasse nutzen.
Sehen wir uns ein kurzes Beispiel für an `Map` , indem wir ★ als Platzhalter verwenden, während wir herausfinden, welche Typen wir benötigen.

```qsharp
function Map(fn : (★ -> ★), values : ★[]) : ★[] {
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
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Im Prinzip könnten wir eine Version von `Map` für jedes Paar von Typen schreiben, auf die wir stoßen, aber dies führt zu einer Reihe von Schwierigkeiten.
Wenn beispielsweise ein Fehler in gefunden wird `Map` , müssen wir sicherstellen, dass die Korrektur in allen Versionen von einheitlich angewendet wird `Map` .
Wenn wir ein neues Tupel oder einen neuen UDT erstellen, müssen wir nun auch ein neues erstellen, `Map` um zusammen mit dem neuen Typ zu gelangen.
Diese Funktion ist zwar für eine kleine Anzahl solcher Funktionen übertragbar, da wir jedoch mehr und mehr Funktionen der gleichen Form wie erfassen `Map` , werden die Kosten für die Einführung neuer Typen in einer relativ kurzen Reihenfolge nicht zu groß.

Ein Großteil dieser Schwierigkeiten ergibt sich jedoch darin, dass wir dem Compiler nicht die Informationen gegeben haben, die er benötigt, um zu erkennen, wie die verschiedenen Versionen von `Map` verknüpft sind.
Effektiv möchten wir, dass der Compiler `Map` als eine mathematische Funktion von q #- *Typen* zu q #-Funktionen behandelt.

Dieses Konzept wird formalisiert, indem Funktionen und Vorgänge *Typparameter*sowie ihre normalen tupelparameter enthalten können.
In den obigen Beispielen möchten wir uns vorstellen, `Map` dass im `Int, Pauli` ersten Fall Typparameter und `Double, String` im zweiten Fall vorhanden sind.
In den meisten Fällen können diese Typparameter so verwendet werden, als wären Sie normale Typen: Wir verwenden Werte von Typparametern, um Arrays und Tupel zu erstellen, Funktionen und Vorgänge aufzurufen und gewöhnliche oder änderbare Variablen zuzuweisen.

> [!NOTE]
> Der extremste Fall der indirekten Abhängigkeit ist die von Qubits, bei denen ein Q #-Programm nicht direkt auf die Struktur des `Qubit` Typs zurückgreifen kann, sondern solche Typen an andere Vorgänge und Funktionen übergeben **muss** .

Wenn Sie zum obigen Beispiel zurückkehren, sehen Sie, dass wir über `Map` Typparameter verfügen müssen, eine zur Darstellung der Eingabe `fn` und eine, die die Ausgabe darstellt `fn` .
In f # wird dies durch Hinzufügen von spitzen Klammern (d `<>` . h. nicht Klammer $ \braket {} $!) nach dem Namen einer Funktion oder eines Vorgangs in der Deklaration und durch Auflisten der einzelnen Typparameter geschrieben.
Der Name jedes Typparameters muss mit einem Tick beginnen `'` , was darauf hinweist, dass es sich um einen Typparameter handelt und nicht um einen normalen Typ (auch als *konkreter* Typ bezeichnet).
Für `Map` schreiben wir daher Folgendes:

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Beachten Sie, dass die Definition von `Map<'Input, 'Output>` sehr ähnlich wie die Versionen ist, die wir bereits geschrieben haben.
Der einzige Unterschied besteht darin, dass wir den Compiler explizit informiert haben, der `Map` nicht direkt davon abhängt `'Input` , was und `'Output` sind, sondern für alle zwei Typen funktionieren, indem Sie Sie indirekt durch verwenden `fn` .
Nachdem wir `Map<'Input, 'Output>` auf diese Weise definiert haben, können wir Sie als normale Funktion bezeichnen:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Das Schreiben von generischen Funktionen und Vorgängen ist eine Stelle, an der "Tupel-in-Tupel-out" eine sehr nützliche Methode für den Umgang mit Q #-Funktionen und-Vorgängen ist.
> Da jede Funktion genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt, gleicht eine Eingabe vom Typ `'T -> 'U` *jede beliebige* Q #-Funktion ab.
> Ebenso kann jeder Vorgang an eine Eingabe des Typs übermittelt werden `'T => 'U` .

Sehen Sie sich als zweites Beispiel die Herausforderung an, eine Funktion zu schreiben, die die Komposition zweier anderer Funktionen zurückgibt:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Hier müssen wir genau angeben, was `A` , `B` und `C` sind, und damit das-Hilfsprogramm der neuen Funktion stark einschränken `Compose` .
Schließlich ist `Compose` nur von `A` , `B` und `C` *über* `innerFn` und abhängig `outerFn` .
Als Alternative können wir Typparameter hinzufügen, `Compose` die angeben, dass Sie für *alle* `A` , `B` und funktionieren, solange `C` diese Parameter mit den von und erwarteten entsprechen `innerFn` `outerFn` :

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


## <a name="callables-as-first-class-values"></a>Callables als First-Class-Werte

Ein wichtiges Verfahren, um die Ablauf Steuerung und die klassische Logik mithilfe von Funktionen anstelle von Vorgängen zu überdenken, besteht darin, diese Vorgänge und Funktionen in Q # als *erste Klasse*zu verwenden.
Das heißt, Sie sind jeweils die einzelnen Werte in der Sprache.
Beispielsweise ist der folgende vollständig gültige Q #-Code, wenn ein wenig indirekt:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

Der Wert der Variablen `ourH` im obigen Code Ausschnitt ist dann der Vorgang <xref:microsoft.quantum.intrinsic.h> , sodass dieser Wert wie jeder andere Vorgang aufgerufen werden kann.
Dies ermöglicht es uns, Vorgänge zu schreiben, die Vorgänge als Teil Ihrer Eingabe ausführen und so die Konzepte der Ablauf Steuerung auf höherer Ordnung bilden.
Beispielsweise könnten wir uns vorstellen, einen Vorgang zu "quadrieren", indem wir ihn zweimal auf das gleiche Ziel-Qubit anwenden.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>Zurückgeben von Vorgängen aus einer Funktion

Wir betonen, dass wir auch Vorgänge als Teil der Ausgaben zurückgeben können, sodass wir einige Arten von klassischer bedingter Logik als klassische Funktion isolieren können, die eine Beschreibung eines Quantum-Programms in Form eines Vorgangs zurückgibt.
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

Diese neue Funktion ist tatsächlich eine Funktion, denn wenn wir Sie mit denselben Werten von `hereBit` und nennen `thereBit` , erhalten wir immer denselben Vorgang.
Daher kann der Decoder sicher innerhalb von Vorgängen ausgeführt werden, ohne dass es darum geht, zu bedenken, wie die Decodierungs Logik mit den Definitionen der verschiedenen Vorgangs Spezialisierungs Maßnahmen interagiert.
Das heißt, wir haben die klassische Logik innerhalb einer Funktion isoliert und dem Compiler dadurch sichergestellt, dass der Funktions aufrufbedarf mit Straffreiheit neu angeordnet werden kann, solange die Eingabe beibehalten wird.


## <a name="partial-application"></a>Partielle Anwendung

Wir können mit Funktionen, die Vorgänge mithilfe einer *partiellen Anwendung*zurückgeben, wesentlich mehr tun, in der wir einen oder mehrere Teile der Eingabe für eine Funktion oder einen Vorgang bereitstellen können, ohne Sie tatsächlich aufrufen zu müssen. Wenn Sie z. b. das `ApplyTwice` obige Beispiel verwenden, können Sie angeben, dass Sie nicht sofort angeben möchten, auf welchem Qubit der Eingabevorgang angewendet werden soll:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

In diesem Fall enthält die lokale Variable `twiceOp` den teilweise angewendeten Vorgang `ApplyTwice(op, _)` , bei dem Teile der Eingabe, die noch nicht angegeben wurden, durch angegeben werden `_` .
Wenn `twiceOp` in der nächsten Zeile tatsächlich aufgerufen wird, übergeben wir als Eingabe an den teilweise angewendeten Vorgang alle verbleibenden Teile der Eingabe für den ursprünglichen Vorgang.
Folglich ist der obige Code Ausschnitt tatsächlich identisch mit dem `ApplyTwice(op, target)` direkten Aufruf von, da wir eine neue lokale Variable eingeführt haben, die es uns ermöglicht, den Aufruf zu verzögern, während einige Teile der Eingabe bereitgestellt werden.

Da ein Vorgang, der teilweise angewendet wurde, erst aufgerufen wird, wenn die gesamte Eingabe bereitgestellt wurde, können wir Vorgänge auf sichere Weise sogar aus Funktionen anwenden.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

Im Prinzip könnte die klassische Logik in `SquareOperation` viel stärker einbezogen werden, aber Sie ist weiterhin vom Rest eines Vorgangs isoliert, indem die Garantien, die der Compiler über Funktionen bereitstellen kann.
Diese Vorgehensweise wird in der Q #-Standardbibliothek verwendet, um die klassische Ablauf Steuerung so auszudrücken, dass Sie in quantenprogrammen problemlos verwendet werden kann.


## <a name="recursion"></a>Rekursion

F #-callables dürfen direkt oder indirekt rekursiv sein.
Das heißt, ein Vorgang oder eine Funktion kann sich selbst aufrufen, oder es kann eine andere Aufruf Bare aufgerufen werden, die den Aufruf baren Vorgang direkt oder indirekt aufruft.

Es gibt jedoch zwei wichtige Kommentare zur Verwendung der Rekursion:

- Die Verwendung von Rekursion bei Vorgängen beeinträchtigt wahrscheinlich bestimmte Optimierungen.
  Dies kann erhebliche Auswirkungen auf die Ausführungszeit des Algorithmus haben.
- Bei der Ausführung auf einem eigentlichen Quantum-Gerät kann der Stapel Speicher eingeschränkt sein, sodass die Tiefe Rekursion zu einem Laufzeitfehler führen kann.
  Insbesondere der Q #-Compiler und die Common Language Runtime erkennen und optimieren die Endrekursion nicht.

## <a name="whats-next"></a>Wie geht es weiter?
Erfahren Sie mehr über [Variablen](xref:microsoft.quantum.guide.variables) in f #.