---
title: Vorgänge und Funktionen in Q#
description: Definieren und aufzurufen von Vorgängen und Funktionen sowie der kontrollierten und der Adjoint-Vorgangs Spezialisierung.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: e9a84de2753bc3293f441e66ee53e78559263e5c
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833479"
---
# <a name="operations-and-functions-in-no-locq"></a>Vorgänge und Funktionen in Q#

## <a name="defining-new-operations"></a>Definieren von neuen Vorgängen

Vorgänge sind der Kern von Q# .
Nach der Deklaration können Sie entweder von klassischen .NET-Anwendungen aus aufgerufen werden, z. b. durch die Verwendung eines Simulators oder durch andere Vorgänge in Q# .
Jeder in definierte Vorgang Q# kann eine beliebige Anzahl anderer Vorgänge, einschließlich der integrierten systeminternen Vorgänge, die von der Sprache definiert sind, aufzurufen. Die spezielle Methode, mit der diese systeminternen Q# Vorgänge definiert werden, hängt vom Zielcomputer ab.
Bei der Kompilierung wird jeder Vorgang als .NET-Klassentyp dargestellt, der den Ziel Computern bereitgestellt werden kann.

Jede Q# Quelldatei kann eine beliebige Anzahl von Vorgängen definieren.
Vorgangs Namen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit Typ-oder Funktionsnamen verursachen.

Eine Vorgangs Deklaration besteht aus dem Schlüsselwort `operation` , gefolgt von dem Symbol, das den Namen des Vorgangs enthält, einem typisierten bezeichnertupel, das die Argumente für den Vorgang definiert, einem Doppelpunkt `:` , einer Typanmerkung, die den Ergebnistyp des Vorgangs beschreibt, optional einer Anmerkung mit den Vorgangs Merkmalen, einer geöffneten geschweiften Klammer und dem Text der Vorgangs Deklaration in geschweiften `{ }`

Jeder Vorgang nimmt eine Eingabe an, erzeugt eine Ausgabe und gibt die Implementierung für eine oder mehrere Vorgangs Spezialisierungs Vorgänge an.
Die möglichen Spezialisierungsmöglichkeiten und die Vorgehensweise zum Definieren und anrufen werden in den verschiedenen Abschnitten dieses Artikels beschrieben.
Sehen Sie sich den folgenden Vorgang an, der nur eine Standard Textzeile definiert und ein einzelnes Qubit als Eingabe annimmt und dann den integrierten <xref:microsoft.quantum.intrinsic.x> Vorgang für diese Eingabe aufruft:

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

Das Schlüsselwort `operation` beginnt mit der Vorgangs Definition, gefolgt vom Namen; hier, `BitFlip` .
Als nächstes wird der Typ der Eingabe definiert ( `Qubit` ), zusammen mit einem Namen, `target` , um auf die Eingabe innerhalb des neuen Vorgangs zu verweisen.
Schließlich `Unit` definiert, dass die Ausgabe des Vorgangs leer ist.
`Unit` wird ähnlich wie `void` in c# und anderen imperativen Sprachen verwendet und entspricht `unit` in F # und anderen funktionalen Sprachen.

Vorgänge können auch interessantere Typen als zurückgeben `Unit` .
Der- <xref:microsoft.quantum.intrinsic.m> Vorgang gibt beispielsweise eine Ausgabe vom Typ zurück `Result` , die angibt, dass eine Messung durchgeführt wurde.  Sie können Sie von einem Vorgang an einen anderen Vorgang übergeben oder mit dem- `let` Schlüsselwort verwenden, um eine neue Variable zu definieren.

Mit diesem Ansatz können Sie die klassische Berechnung darstellen, die mit Quantum-Vorgängen auf niedriger Ebene interagiert, wie z. b. in einer über [geordneten Codierung](https://github.com/microsoft/QuantumKatas/tree/main/SuperdenseCoding):

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
> Jeder Vorgang in Q# erfordert genau eine Eingabe und gibt genau eine Ausgabe zurück.
> Mehrere Eingaben und Ausgaben werden mithilfe von *Tupeln*dargestellt, die mehrere Werte in einem einzelnen Wert zusammenfassen.
> In dieser Hinsicht Q# ist eine "Tupel-in-tupelout"-Sprache.
> Im Anschluss an dieses Konzept sollte ein Satz leerer Klammern, `()` , als leeres Tupel mit dem-Typ gelesen werden `Unit` .

## <a name="controlled-and-adjoint-operations"></a>Kontrollierte und Adjoint-Vorgänge

Wenn ein Vorgang eine einheitliche Transformation implementiert, wie dies bei vielen Vorgängen in der Fall ist Q# , ist es möglich, zu definieren, wie der *adjointed* Vorgang bei Anfügevorgang oder *Kontrolle*agiert. Eine *Adjoint* -Spezialisierung eines Vorgangs gibt an, wie die "Umkehrung" des Vorgangs agiert, während eine *kontrollierte* Spezialisierung angibt, wie ein Vorgang funktioniert, wenn die Anwendung auf den Zustand eines bestimmten Quantum-Registers angewendet wird.

Adjoints von Quantum-Vorgängen sind für viele Aspekte von Quantum Computing von entscheidender Bedeutung. Ein Beispiel für eine solche Situation, die zusammen mit einer nützlichen Q# Programmiertechnik erläutert wird, finden Sie unter [Ablauf Steuerung: Konjugationen](xref:microsoft.quantum.guide.controlflow#conjugations). Bei der kontrollierten Version eines Vorgangs handelt es sich um einen neuen Vorgang, der den Basis Vorgang effektiv anwendet, wenn sich alle Steuerelement-Qubits in einem angegebenen Zustand befinden.
Wenn sich die Steuerelement-Qubits in der superposition befinden, wird der Basis Vorgang einheitlich auf den entsprechenden Teil der superposition angewendet.
Folglich werden kontrollierte Vorgänge häufig zum Generieren von entanglement verwendet.

Natürlich könnte auch eine *kontrollierte Adjoint* -Spezialisierung vorhanden sein, die die kontrollierte Anwendung des Adjoint eines Vorgangs angibt.

> [!NOTE]
> Wenn $U $ die von einem Vorgang implementierte einheitliche Transformation ist `U` , `Adjoint U` stellt die einheitliche Transformation $U ^ \dagger $ dar, die die komplexe konjugierte Transformation ist.
> Wenn Sie einen Vorgang nacheinander anwenden und dessen Adjoint in einen Zustand versetzt wird, bleibt der Zustand unverändert, wie in der Tatsache veranschaulicht, dass $UU ^ \dagger = U ^ \dagger U = \id $ die Identitätsmatrix ist.
> Die einheitliche Darstellung eines kontrollierten Vorgangs ist etwas flexibler, aber weitere Informationen finden Sie unter [Quantum Computing Concepts: Multiple Qubits](xref:microsoft.quantum.concepts.multiple-qubits).

Im folgenden Abschnitt wird beschrieben, wie Sie diese verschiedenen Spezialisierungs Informationen in Ihrem Code aufzurufen Q# und wie Sie Vorgänge zur Unterstützung definieren.

### <a name="calling-operation-specializations"></a>Aufrufen von Vorgangs Spezialisierungs Vorgängen

Ein *Funktor* in Q# ist eine Factory, die einen neuen Vorgang aus einem anderen Vorgang definiert.
Die beiden standardfunktoren in Q# sind `Adjoint` und `Controlled` .

Funktoren haben Zugriff auf die Implementierung des Basis Vorgangs, wenn die Implementierung des neuen Vorgangs definiert wird.
Daher können Funktoren komplexere Funktionen als herkömmliche Funktionen höherer Ebene ausführen. Funktoren haben keine Darstellung im Q# Typsystem. Daher ist es derzeit nicht möglich, Sie an eine Variable zu binden oder Sie als Argumente zu übergeben. 

Verwenden Sie ein Funktor, indem Sie es auf einen Vorgang anwenden, der einen neuen Vorgang zurückgibt.
Wenn Sie das Funktor beispielsweise auf den-Vorgang anwenden, wird `Adjoint` `Y` der neue-Vorgang zurückgegeben `Adjoint Y` . Sie können den neuen Vorgang wie jeden anderen Vorgang aufrufen.
Damit ein Vorgang die Anwendung des-oder- `Adjoint` `Controlled` funktors unterstützt, muss der Rückgabetyp notwendigerweise sein `Unit` . 

#### <a name="adjoint-functor"></a>`Adjoint` Funktionselement

Folglich `Adjoint Y(q1)` wendet das `Adjoint` Funktor auf den `Y` Vorgang an, um einen neuen Vorgang zu generieren, und wendet diesen neuen Vorgang auf an `q1` .
Der neue Vorgang hat dieselbe Signatur und denselben Typ wie der Basis Vorgang `Y` .
Insbesondere unterstützt der neue-Vorgang auch `Adjoint` , und unterstützt nur dann, wenn `Controlled` der Basis Vorgang durchgeführt wurde.
Das `Adjoint` Funktor ist eine eigene Umkehrung, d. h `Adjoint Adjoint Op` ., ist immer identisch mit `Op` .

#### <a name="controlled-functor"></a>`Controlled` Funktionselement

Ebenso `Controlled X(controls, target)` wendet das `Controlled` Funktor auf den `X` -Vorgang an, um einen neuen-Vorgang zu generieren, und wendet diesen neuen-Vorgang auf `controls` und an `target` .

> [!NOTE]
> In Q# werden von kontrollierten Versionen immer ein Array von Steuerelement-Qubits übernommen, und die Steuerung basiert immer auf allen Steuerelement-Qubits, die sich im Status "Compu()" befinden ( `PauliZ` `One` $ \ket {1} $).
> Das Steuern auf der Grundlage anderer Zustände wird erreicht, indem der entsprechende einheitliche Vorgang auf die Steuerungs Qubits vor dem kontrollierten Vorgang angewendet und dann die Umkehrung des einheitlichen Vorgangs nach dem kontrollierten Vorgang angewendet wird.
> Wenn Sie z. b `X` . einen Vorgang vor und nach einer kontrollierten Operation auf ein Steuerelement-Qubit anwenden, steuert der Vorgang den `Zero` Zustand ($ \ket {0} $) für dieses Qubit. Anwenden eines `H` Vorgangs vor und nach der Steuerung des `PauliX` `One` Zustands, d. h.-1 eigen Wert von Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ anstelle des- `PauliZ` `One` Zustands.

Bei Angabe eines Vorgangs Ausdrucks können Sie mithilfe des-funktors einen neuen Vorgangs Ausdruck bilden `Controlled` .
Die Signatur des neuen Vorgangs basiert auf der Signatur des ursprünglichen Vorgangs.
Der Ergebnistyp ist identisch, aber der Eingabetyp ist ein zwei Tupel mit einem Qubit-Array, das die Steuerelement-Qubit (s) als erstes Element und die Argumente des ursprünglichen Vorgangs als zweites Element enthält.
Der neue-Vorgang unterstützt `Controlled` , und unterstützt `Adjoint` nur dann, wenn der ursprüngliche Vorgang durchgeführt wurde.

Wenn für den ursprünglichen Vorgang nur ein einzelnes Argument benötigt wurde, wird hier die [entsprechgabe von Singleton-Tupeln](xref:microsoft.quantum.guide.types) berücksichtigt.
Beispiels `Controlled X` Weise ist die gesteuerte Version des `X` Vorgangs. 
`X` weist den Typ auf `(Qubit => Unit is Adj + Ctl)` , `Controlled X` hat also `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` den Typ; aufgrund der Äquivalenz von Singleton-Tupeln ist dies identisch mit `((Qubit[], Qubit) => Unit is Adj + Ctl)` .

Wenn der Basis Vorgang mehrere Argumente benötigt hat, denken Sie daran, die entsprechenden Argumente der kontrollierten Version des Vorgangs in Klammern einzuschließen, um Sie in ein Tupel zu konvertieren.
Beispiels `Controlled Rz` Weise ist die gesteuerte Version des `Rz` Vorgangs. 
`Rz` weist den Typ auf `((Double, Qubit) => Unit is Adj + Ctl)` , hat also den `Controlled Rz` Typ `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .
Daher ist `Controlled Rz(controls, (0.1, target))` ein gültiger Aufruf von `Controlled Rz` (Beachten Sie die Klammern `0.1, target` ).

Als weiteres Beispiel `CNOT(control, target)` kann als implementiert werden `Controlled X([control], target)` . Wenn ein Ziel von zwei Steuerungs Qubits (ccnot) gesteuert werden soll, verwenden Sie eine- `Controlled X([control1, control2], target)` Anweisung.

#### `Controlled Adjoint` 

Das `Controlled` -und das- `Adjoint` funktorin werden angewendet, sodass es keinen Unterschied zwischen dem Anwenden von `Controlled Adjoint Op` oder gibt `Adjoint Controlled Op`


## <a name="defining-controlled-and-adjoint-implementations"></a>Definieren von kontrollierten und Adjoint-Implementierungen

In der ersten Vorgangs Deklaration in den vorherigen Beispielen wurden die Vorgänge `BitFlip` und `DecodeSuperdense` mit Signaturen `(Qubit => Unit)` `((Qubit, Qubit) => (Result, Result))` bzw. definiert.
Wie z. b. `DecodeSuperdense` Messungen, ist es kein einheitlicher Vorgang. Daher könnten weder die kontrollierten noch die nicht zusammenhängenden Spezialisierungs Maßnahmen vorhanden sein `Unit` .
Wenn Sie jedoch `BitFlip` einfach den einheitlichen <xref:microsoft.quantum.intrinsic.x> Vorgang ausführen, können Sie ihn mit beiden Spezialisierungs Vorgängen definieren.

In diesem Abschnitt wird erläutert, wie Sie das vorhanden sein von Spezialisierungs Funktionen in die Q# Vorgangs Deklarationen einschließen und somit die Möglichkeit haben, in Verbindung mit dem-oder dem- `Adjoint` `Controlled` funktors aufzurufen.
Weitere Informationen zu einigen Situationen, in denen es entweder gültig oder nicht zulässig ist, bestimmte Spezialisierungs Informationen zu deklarieren, finden Sie unter Umstände für die Überprüfung [von Spezialisierungs](#circumstances-for-validly-defining-specializations) Informationen in diesem Artikel.

Vorgangs Merkmale definieren, welche Arten von Funktions tüktoren Sie auf den deklarierten Vorgang anwenden können und welche Auswirkungen Sie haben. Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur deklariert werden, insbesondere über eine Anmerkung mit den Vorgangs Merkmalen: entweder `is Adj` , `is Ctl` oder `is Adj + Ctl` .
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
Daher können Sie das `DecodeSuperdense` im vorherigen Beispiel mit einem kompakteren schreiben, indem Sie das Adjoint von verwenden, `PrepareEntangledPair` um den entzickten Zustand wieder in ein nicht verwinkelter Qubits-paar umzuwandeln:

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

Wenn der Compiler die Implementierung nicht generieren kann, können Sie ihn explizit angeben. Solche expliziten Spezialisierungs Deklarationen können aus einer geeigneten *Generierungs Direktive* oder einer benutzerdefinierten Implementierung bestehen.
Im folgenden finden Sie die vollständige Palette der Möglichkeiten mit einigen Beispielen für eine explizite Spezialisierung. 


#### <a name="explicit-specialization-declarations"></a>Explizite Spezialisierungs Deklarationen

Q# Vorgänge können die folgenden expliziten Spezialisierungs Deklarationen enthalten:

- Die `body` Spezialisierung gibt die Implementierung des Vorgangs ohne angewendete Funktoren an.
- Die `adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit `Adjoint` angewendetem Funktionselement an.
- Die `controlled` Spezialisierung gibt die Implementierung des Vorgangs mit `Controlled` angewendetem Funktionselement an.
- Die `controlled adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit den `Adjoint` `Controlled` angewendeten-und-Funktoren an.
  Diese Spezialisierung kann auch benannt werden `adjoint controlled` , da die beiden Funktoren in den Weg gehen.


Eine Vorgangs Spezialisierung besteht aus dem Spezialisierungs Kennzeichen (z. b. `body` oder `adjoint` ), gefolgt von einem der folgenden:

- Eine explizite Deklaration, wie im folgenden beschrieben.
- Eine- *Direktive* , die dem Compiler mitteilt, *wie* die Spezialisierung generiert werden soll, einer der folgenden:
  - `intrinsic`Gibt an, dass der Zielcomputer die Spezialisierung bereitstellt.
  - `distribute`wird mit den `controlled` -und- `controlled adjoint` Spezialisierungs-verwendet.
    Bei Verwendung mit `controlled` wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in angewendet wird `body` .
    Bei Verwendung mit `controlled adjoint` wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in der Spezialisierung anwendet `adjoint` .
  - `invert`Gibt an, dass der Compiler die `adjoint` Spezialisierung durch Umkehren von berechnen soll, indem `body` z. b. die Reihenfolge der Vorgänge umkehren und das Adjoint-Attribut auf jedes angewendet wird.
    Wenn Sie mit verwendet `adjoint controlled` wird, gibt dies an, dass der Compiler die Spezialisierung durch Umkehren der `controlled` Spezialisierung berechnen soll.
  - `self`, um anzugeben, dass die Adjoint-Spezialisierung mit der Spezialisierung identisch ist `body` .
    `self`Die Verwendung von ist für die `adjoint` -und- `adjoint controlled` Spezialisierung zulässig.
    Für `adjoint controlled` `self` impliziert, dass die `adjoint controlled` Spezialisierung mit der Spezialisierung identisch ist `controlled` .
  - `auto`, um anzugeben, dass der Compiler eine entsprechende anzuwendende Direktive auswählen soll.
    Sie können `auto` für die Spezialisierung nicht verwenden `body` .

Die-Direktiven und `auto` alle erfordern ein Schließ Endes Semikolon `;` .
Die- `auto` Direktive wird in die folgende generierte-Direktive aufgelöst, wenn eine explizite Deklaration von `body` bereitgestellt wird:

- Die `adjoint` Spezialisierung wird gemäß der-Direktive generiert `invert` .
- Die `controlled` Spezialisierung wird gemäß der-Direktive generiert `distribute` .
- Die `adjoint controlled` Spezialisierung wird gemäß der-Direktive generiert `invert` , wenn eine explizite Deklaration für `controlled` angegeben ist, aber nicht für `adjoint` , und `distribute` andernfalls.

> [!TIP]   
> Wenn es sich um einen eigenständigen Vorgang handelt, geben Sie entweder die Adjoint-oder die kontrollierte Adjoint-Spezialisierung mithilfe der Generations Direktive explizit `self` an, damit der Compiler diese Informationen für Optimierungszwecke nutzen kann.

Eine Spezialisierungs Deklaration, die eine benutzerdefinierte Implementierung enthält, besteht aus einem argumenttupel, gefolgt von einem Anweisungsblock mit dem Q# Code, der die Spezialisierung implementiert.
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

Im vorherigen `PrepareEntangledPair` Beispiel entspricht der Code dem folgenden Code, der explizite Spezialisierungs Deklarationen enthält: 

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

Wenn der Compiler die Implementierung für eine bestimmte Spezialisierung nicht automatisch generieren kann oder wenn eine effizientere Implementierung angegeben werden kann, können Sie die Implementierung manuell definieren.

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
Im vorherigen Beispiel gibt an, `adjoint invert;` dass die Adjoint-Spezialisierung durch das Umkehren der Text Implementierung generiert werden soll, und `controlled adjoint invert;` gibt an, dass die kontrollierte Adjoint-Spezialisierung generiert werden soll, indem die angegebene Implementierung der kontrollierten Spezialisierung umgekehrt wird.

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

Es ist zulässig, einen Vorgang ohne Adjoint oder kontrollierte Versionen anzugeben. Beispielsweise haben Messungs Vorgänge keinen, weil Sie nicht invertierbar oder steuerbar sind.

Ein-Vorgang unterstützt die `Adjoint` -und- `Controlled` Funktoren, wenn seine Deklaration eine implizite oder explizite Deklaration der jeweiligen Spezialisierungs Elemente enthält.

Eine explizit deklarierte Adjoint/gesteuerte Spezialisierung impliziert das vorhanden sein einer Adjoint/kontrollierten Spezialisierung. 

Bei einem Vorgang, dessen Text Wiederholungs-bis-Erfolg-Schleifen, Set-Anweisungen, Messungen, Rückgabe Anweisungen oder Aufrufe von anderen Vorgängen enthält, die das Funktor nicht unterstützen `Adjoint` , ist das automatische Erstellen einer Adjoint-Spezialisierung nach der- `invert` oder- `auto` Direktive nicht möglich.

Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die das `Controlled` Funktor nicht unterstützen, ist das automatische Erstellen einer kontrollierten Spezialisierung nach der- `distribute` oder- `auto` Direktive nicht möglich.

#### <a name="controlled-adjoint"></a>Kontrollierter Adjoint

Die kontrollierte Adjoint-Version eines Vorgangs gibt an, wie eine durch eine Quantum gesteuerte Version des Adjoint-Vorgangs des Vorgangs implementiert wird.
Es ist zulässig, einen Vorgang ohne kontrollierte Adjoint-Version anzugeben. Messvorgänge haben beispielsweise keine kontrollierte Adjoint-Version, da Sie weder steuerbar noch invertierbar sind.

Eine kontrollierte Adjoint-Spezialisierung für einen Vorgang muss nur dann vorhanden sein, wenn sowohl ein Adjoint-als auch eine gesteuerte Spezialisierung vorhanden sind. In diesem Fall wird das vorhanden sein der kontrollierten Adjoint-Spezialisierung abgeleitet. Wenn keine Implementierung explizit definiert ist, generiert die Kompilierung eine entsprechende Spezialisierung.

Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die nicht über eine kontrollierte Adjoint-Version verfügen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach der- `invert` ,- `distribute` oder- `auto` Direktive nicht möglich.


### <a name="type-compatibility"></a>Typkompatibilität

Verwenden Sie einen Vorgang mit zusätzlichen Funktoren, die überall unterstützt werden, wenn Sie einen Vorgang mit weniger Funktoren, aber derselben Signatur verwenden. Verwenden Sie beispielsweise einen Vorgang des Typs an einer beliebigen Stelle, an `(Qubit => Unit is Adj)` der Sie einen Vorgang des Typs verwenden `(Qubit => Unit)` .

Q# ist *kovariant* in Bezug auf Aufruf Bare Rückgabe Typen: ein Aufruf barer, der einen-Typ zurückgibt, `'A` ist mit einem Aufruf baren-Element mit demselben Eingabetyp und einem Ergebnistyp kompatibel, der mit kompatibel ist `'A` .

Q# ist *kontra Variant* in Bezug auf Eingabetypen: ein Aufruf bares Element, das einen Typ `'A` als Eingabe annimmt, ist mit einem Aufruf baren mit dem gleichen Ergebnistyp und einem Eingabetyp kompatibel, der mit kompatibel ist `'A` .

Das heißt, wenn die folgenden Definitionen definiert sind,

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

Sie können

- Rufen Sie die Funktion `ConjugateInvertWith` mit einem `inner` Argument von `Invert` oder auf `ApplyUnitary` .
- Rufen Sie die Funktion `ConjugateUnitaryWith` mit einem `inner` Argument von auf `ApplyUnitary` , jedoch nicht `Invert` .
- Gibt einen Wert vom Typ `(Qubit[] => Unit is Adj + Ctl)` aus zurück `ConjugateInvertWith` .

> [!IMPORTANT]
> Q# 0,3 hat einen signifikanten Unterschied im Verhalten von benutzerdefinierten Typen eingeführt.

Benutzerdefinierte Typen werden als umschließende Version des zugrunde liegenden Typs und nicht als Untertyp behandelt.
Dies bedeutet, dass ein Wert eines benutzerdefinierten Typs nicht verwendbar ist, wenn Sie erwarten, dass ein Wert des zugrunde liegenden Typs ist.


## <a name="defining-new-functions"></a>Definieren neuer Funktionen

Funktionen sind rein deterministische, klassische Routinen in Q# , die sich von Vorgängen unterscheiden, da Sie keine Auswirkungen auf die Berechnung eines Ausgabe Werts haben dürfen.
Insbesondere können Funktionen keine Vorgänge aufzurufen. reagieren, zuordnen oder ausleihen von Qubits Stichproben von Zufallszahlen oder hängt anderweitig von dem Zustand ab, der über den Eingabe Wert zu einer Funktion hinausgeht.
Folglich Q# sind Funktionen *rein*, da Sie die gleichen Eingabewerte immer denselben Ausgabe Werten zuordnen.
Dieses Verhalten ermöglicht es dem Q# Compiler, sicherzustellen, wie und wann Funktionen beim Erzeugen von Vorgangs speziationen aufgerufen werden.

Jede Q# Quelldatei kann eine beliebige Anzahl von Funktionen definieren.
Funktionsnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-oder Typnamen in Konflikt stehen.

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

Wenn dies möglich ist, ist es hilfreich, Klassische Logik in Bezug auf Funktionen anstelle von Vorgängen zu schreiben, damit Vorgänge Sie leichter verwenden können. Wenn Sie z. b. die vorherige `Square` Deklaration als *Vorgang*geschrieben haben, konnte der Compiler nicht garantieren, dass der Aufruf mit derselben Eingabe konstant die gleichen Ausgaben erzeugt.

Um den Unterschied zwischen Funktionen und Vorgängen zu unterstreichen, sollten Sie das Problem der klassischen Stichprobenentnahme für eine Zufallszahl innerhalb eines- Q# Vorgangs beachten:

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

Jedes Mal `U` , wenn aufgerufen wird, wird eine andere Aktion für ausgeführt `target` .
Insbesondere kann der Compiler nicht garantieren, dass, wenn Sie eine `adjoint auto` Spezialisierung-Deklaration hinzufügen `U` , `U(target); Adjoint U(target);` als Identität agiert (d. h. als No-OP).
Dies verstößt gegen die Definition des in [Vektoren und Matrizen](xref:microsoft.quantum.concepts.vectors)definierten Adjoint, sodass der Compiler die automatische Generierung einer Adjoint-Spezialisierung in einem Vorgang gestattet, bei dem Sie den Vorgang aufzurufen, <xref:microsoft.quantum.math.randomreal> die vom Compiler bereitgestellten Garantien sprengen würde <xref:microsoft.quantum.math.randomreal> . ist ein Vorgang, für den keine Adjoint-oder kontrollierte Version vorhanden ist.

Auf der anderen Seite können Funktionsaufrufe wie z. b. `Square` sicher sein, und der Compiler wird sichergestellt, dass nur die Eingabe in beibehalten werden muss, damit die `Square` Ausgabe stabil bleibt.
Daher ist es einfach, diese Logik in anderen Funktionen und Vorgängen zu verwenden, damit Sie so viel Klassische Logik wie möglich in Functions isolieren kann.


## <a name="generic-type-parameterized-callables"></a>Generische (typparametrisierte) callables

Viele Funktionen und Vorgänge, die Sie möglicherweise definieren möchten, sind nicht wirklich stark von den Typen Ihrer Eingaben abhängig, sondern verwenden nur implizit ihre Typen über eine andere Funktion oder einen anderen Vorgang.
Sehen Sie sich beispielsweise das *Karten* Konzept an, das vielen funktionalen Sprachen gemeinsam ist. bei Angabe einer Funktion $f (x) $ und einer Auflistung von Werten $ \{ x_1, x_2, \dots, x_n \} $ gibt MAP eine neue Auflistung $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $ zurück.
Um dies in zu implementieren Q# , nutzen Sie die Tatsache, dass Functions die erste Klasse ist.
Im folgenden finden Sie ein kurzes Beispiel für die `Map` Verwendung von `T` als Platzhalter, während Sie herausfinden, welche Typen Sie benötigen.

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Beachten Sie, dass diese Funktion unabhängig von den tatsächlichen Typen, in denen Sie ersetzen, sehr ähnlich aussieht.
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

Im Prinzip können Sie eine Version von `Map` für jedes Paar von Typen schreiben, das auftreten, aber dies führt zu mehreren Schwierigkeiten.
Wenn Sie beispielsweise einen Fehler in feststellen `Map` , müssen Sie sicherstellen, dass die Korrektur in allen Versionen von einheitlich angewendet wird `Map` .
Wenn Sie ein neues Tupel oder einen neuen UDT erstellen, müssen Sie nun auch ein neues erstellen, `Map` um zusammen mit dem neuen Typ zu wechseln.
Diese Funktion ist zwar für eine kleine Anzahl solcher Funktionen übertragbar, da Sie jedoch mehr und mehr Funktionen der gleichen Form wie erfassen `Map` , werden die Kosten für die Einführung neuer Typen in einer relativ kurzen Reihenfolge nicht sehr groß.

Ein Großteil dieser Schwierigkeit ergibt sich jedoch aus der Tatsache, dass Sie dem Compiler nicht die erforderlichen Informationen zur Erkennung der verschiedenen Versionen von erhalten haben `Map` .
Effektiv möchten Sie, dass der Compiler `Map` als eine mathematische Funktion von Q# *Typen* zu Q# Funktionen behandelt.

Q# formalisiert dieses Konzept, indem Funktionen und Vorgänge sowohl *Typparameter*als auch Ihre normalen tupelparameter aufweisen können.
In den vorherigen Beispielen möchten Sie sich vorstellen, `Map` dass im `Int, Pauli` ersten Fall Typparameter und `Double, String` im zweiten Fall vorhanden sind.
Verwenden Sie zum größten Teil diese Typparameter, als wären Sie normale Typen. Verwenden Sie Werte von Typparametern, um Arrays und Tupel zu erstellen, Funktionen und Vorgänge aufzurufen und gewöhnliche oder änderbare Variablen zuzuweisen.

> [!NOTE]
> Der extremste Fall der indirekten Abhängigkeit ist die von Qubits, bei denen sich ein Q# Programm nicht direkt auf die Struktur des Typs verlassen kann, `Qubit` sondern solche Typen an andere Vorgänge und Funktionen übergeben **muss** .

Wenn Sie zum vorherigen Beispiel zurückkehren, sehen Sie, dass `Map` über Typparameter verfügen muss, eines für die Darstellung der Eingabe `fn` und eines zum Darstellen der Ausgabe `fn` .
In Q# wird dies durch Hinzufügen von spitzen Klammern (d `<>` . h. nicht Klammer $ \braket {} $!) nach dem Namen einer Funktion oder eines Vorgangs in der Deklaration und durch Auflisten der einzelnen Typparameter geschrieben.
Der Name jedes Typparameters muss mit einem Tick beginnen `'` , was darauf hinweist, dass es sich um einen Typparameter handelt und nicht um einen normalen Typ (auch als *konkreter* Typ bezeichnet).
Daher `Map` wird geschrieben:

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

Beachten Sie, dass die Definition von `Map<'Input, 'Output>` den previoius-Versionen sehr ähnlich aussieht.
Der einzige Unterschied besteht darin, dass Sie den Compiler explizit informiert haben, der `Map` nicht direkt davon abhängt `'Input` , was und `'Output` sind, sondern für alle zwei Typen funktionieren, indem Sie Sie indirekt durch verwenden `fn` .
Wenn Sie `Map<'Input, 'Output>` auf diese Weise definiert haben, können Sie Sie wie eine normale Funktion nennen:

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> Das Schreiben von generischen Funktionen und Vorgängen ist eine Stelle, an der "Tupel-in-tupelout" eine sehr nützliche Methode ist, um Q# Funktionen und Vorgänge zu übernehmen.
> Da jede Funktion genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt, gleicht eine Eingabe vom Typ `'T -> 'U` *jede beliebige* Q# Funktion ab.
> Entsprechend können Sie jeden Vorgang an eine Eingabe vom Typ übergeben `'T => 'U` .

Sehen Sie sich als zweites Beispiel die Herausforderung an, eine Funktion zu schreiben, die die Komposition zweier anderer Funktionen zurückgibt:

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Hier müssen Sie genau angeben, was `A` , `B` und `C` sind, und so das Dienstprogramm der neuen Funktion stark einschränken `Compose` .
Schließlich ist `Compose` nur von `A` , `B` und `C` *über* `innerFn` und abhängig `outerFn` .
Als Alternative können Sie auch Typparameter hinzufügen, `Compose` die angeben, dass Sie für *alle* `A` , und funktioniert `B` , solange `C` diese Parameter den von und erwarteten entsprechen `innerFn` `outerFn` :

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

Die Q# Standardbibliotheken stellen einen Bereich von Typen parametrisierten Vorgängen und Funktionen bereit, um die Express-Ablauf Steuerung zu vereinfachen.
Diese werden im [ Q# Handbuch zur Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro)erläutert.


## <a name="callables-as-first-class-values"></a>Callables als First-Class-Werte

Ein wichtiges Verfahren, um die Ablauf Steuerung und die klassische Logik mithilfe von Funktionen anstelle von Vorgängen zu überdenken, besteht darin, diese Vorgänge und Funktionen in als Q# *erste Klasse*zu verwenden.
Das heißt, Sie sind jeweils die einzelnen Werte in der Sprache.
Beispielsweise ist der folgende vollständig gültige Q# Code, wenn ein wenig indirekt:

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

Der Wert der Variablen `ourH` im vorherigen Code Ausschnitt ist dann der Vorgang <xref:microsoft.quantum.intrinsic.h> , sodass Sie diesen Wert wie jeder andere Vorgang abrufen können.
Mit dieser Fähigkeit können Sie Vorgänge schreiben, die Vorgänge als Teil Ihrer Eingabe ausführen und so die Konzepte der Ablauf Steuerung in höherer Ordnung bilden.
Beispielsweise können Sie sich vorstellen, einen Vorgang zu "quadrieren", indem Sie ihn zweimal auf das gleiche Ziel-Qubit anwenden.

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a>Zurückgeben von Vorgängen aus einer Funktion

Es ist wichtig zu betonen, dass Sie auch Vorgänge als Teil der Ausgaben zurückgeben können, sodass Sie einige Arten von klassischer bedingter Logik als klassische Funktion isolieren können, die eine Beschreibung eines Quantum-Programms in Form eines Vorgangs zurückgibt.
Als einfaches Beispiel sehen Sie sich das Beispiel für die teleportung an, in dem die Partei, die eine zwei-Bit-klassische Nachricht empfängt, die Nachricht verwenden muss, um Ihr Qubit in den richtigen teleportierten Zustand zu decodieren.
Sie könnten dies im Hinblick auf eine Funktion schreiben, die diese beiden klassischen Bits annimmt und den richtigen Decodierungs Vorgang zurückgibt.

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

Diese neue Funktion ist tatsächlich eine Funktion, wenn Sie Sie mit den gleichen Werten von und aufzurufen `hereBit` `thereBit` , und Sie erhalten immer denselben Vorgang.
Daher kann der Decoder sicher innerhalb von Vorgängen ausgeführt werden, ohne dass es darum geht, zu bedenken, wie die Decodierungs Logik mit den Definitionen der verschiedenen Vorgangs Spezialisierungs Maßnahmen interagiert.
Das heißt, die klassische Logik innerhalb einer Funktion ist isoliert, sodass dem Compiler gewährleistet wird, dass der Funktions aufrufbedarf mit Straffreiheit neu angeordnet werden kann, solange die Eingabe beibehalten wird.


## <a name="partial-application"></a>Partielle Anwendung

Sie können mit Funktionen, die Vorgänge mithilfe einer *partiellen Anwendung*zurückgeben, wesentlich mehr tun, bei der Sie einen oder mehrere Teile der Eingabe für eine Funktion oder einen Vorgang bereitstellen, ohne Sie tatsächlich aufrufen zu müssen. Im vorherigen `ApplyTwice` Beispiel können Sie angeben, dass Sie nicht sofort angeben möchten, auf welchem Qubit der Eingabevorgang angewendet werden soll:

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

In diesem Fall enthält die lokale Variable `twiceOp` den teilweise angewendeten Vorgang `ApplyTwice(op, _)` , wobei `_` Teile der Eingabe angibt, die noch nicht angegeben wurden.
Wenn Sie `twiceOp` in der nächsten Zeile aufzurufen, übergeben Sie als Eingabe an den teilweise angewendeten Vorgang alle verbleibenden Teile der Eingabe für den ursprünglichen Vorgang.
Folglich ist der vorherige Code Ausschnitt tatsächlich identisch mit dem `ApplyTwice(op, target)` direkten Aufruf von, da Sie eine neue lokale Variable eingeführt haben, damit Sie den Aufruf bei der Bereitstellung einiger Teile der Eingabe verzögern können.

Da ein Vorgang, der teilweise angewendet wurde, erst aufgerufen wird, wenn die gesamte Eingabe bereitgestellt wurde, können Sie Vorgänge auf sichere Weise sogar aus Funktionen anwenden.

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

Im Prinzip könnte die klassische Logik in `SquareOperation` viel stärker einbezogen werden, aber Sie ist weiterhin vom Rest eines Vorgangs isoliert, indem die Garantien, die der Compiler über Funktionen bereitstellen kann. Die Q# Standardbibliothek verwendet diesen Ansatz, um die klassische Ablauf Steuerung so auszudrücken, dass Quantum-Programme Sie problemlos verwenden können.


## <a name="recursion"></a>Rekursion

Q# callables dürfen direkt oder indirekt rekursiv sein.
Das heißt, ein Vorgang oder eine Funktion kann sich selbst aufrufen, oder Sie kann eine andere Aufruf Bare aufrufen, die den Aufruf baren Vorgang direkt oder indirekt aufruft.

Es gibt jedoch zwei wichtige Kommentare zur Verwendung der Rekursion:

- Die Verwendung von Rekursion bei Vorgängen beeinträchtigt wahrscheinlich bestimmte Optimierungen.
  Diese Störungen können erhebliche Auswirkungen auf die Laufzeit des Algorithmus haben.
- Bei der Ausführung auf einem eigentlichen Quantum-Gerät ist der Stapel Speicherplatz möglicherweise eingeschränkt, sodass die Tiefe Rekursion zu einem Laufzeitfehler führen kann.
  Der Q# Compiler und die Laufzeit identifizieren und optimieren die Endrekursion insbesondere nicht.

## <a name="next-steps"></a>Nächste Schritte

Erfahren Sie mehr über [Variablen](xref:microsoft.quantum.guide.variables) in Q# .