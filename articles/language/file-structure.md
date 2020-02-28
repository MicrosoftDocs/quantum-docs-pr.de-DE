---
title: 'F #-Dateistruktur'
description: 'Erfahren Sie, wie Sie Namespaces und Vorgänge, Funktionen und benutzerdefinierte Typdeklarationen in Q #-Programmen und-Bibliotheken strukturieren.'
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: b4bb7d4d70677dbd5d921a9f68313760499a56a1
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907391"
---
# <a name="file-structure"></a>Dateistruktur

Eine Q #-Datei besteht aus einer Sequenz von Namespace Deklarationen.
Jede Namespace Deklaration enthält Deklarationen für benutzerdefinierte Typen, Vorgänge und Funktionen.
Eine Namespace Deklaration kann beliebig viele Typen von Deklarationen und in beliebiger Reihenfolge enthalten.
Der einzige Text, der außerhalb einer Namespace Deklaration angezeigt werden kann, sind Kommentare.
Insbesondere Dokumentations Kommentare für einen Namespace vor der Deklaration.

## <a name="namespace-declarations"></a>Namespacedeklarationen

Eine Q #-Datei hat normalerweise genau eine Namespace Deklaration, kann jedoch keine (und leer sein oder nur Kommentare enthalten) oder mehrere Namespaces enthalten.
Namespace Deklarationen dürfen nicht eingefügt werden.

Derselbe Namespace kann in mehreren Q #-Dateien deklariert werden, die zusammen kompiliert werden, solange keine Typen-, Vorgangs-oder Funktions Deklarationen mit demselben Namen vorhanden sind.
Es ist insbesondere ungültig, denselben Typ im gleichen Namespace in mehreren Dateien zu definieren, auch wenn die Deklarationen identisch sind.

Eine Namespace Deklaration besteht aus dem Schlüsselwort `namespace`, gefolgt vom Namen des Namespace, einer geöffneten geschweifter Klammer `{`, den im Namespace enthaltenen Deklarationen und einer schließenden geschweifter Klammer `}`.
Namespace Namen folgen dem .net-Muster einer Sequenz von mindestens einem juristischen Symbol, das durch Zeiträume `.`getrennt ist.
Beispielsweise sind `MyQuantumStuff` und `Microsoft.Quantum.Canon` gültige Namespace Namen.
Gemäß der Konvention werden die Symbole in einem Namespace Namen groß geschrieben, dies ist jedoch nicht erforderlich.

Deklarationen werden in einer Namespace Deklaration möglicherweise in beliebiger Reihenfolge angezeigt.
Verweise auf Typen oder Aufruf Bare Dateien, die in einer Datei weiter unten deklariert sind, werden ordnungsgemäß aufgelöst. Es ist nicht erforderlich, dass der Typ, der Vorgang oder die Funktionsdeklaration einem Verweis darauf vorangestellt wird.

## <a name="open-directives"></a>Open-Direktiven

Innerhalb eines Namespace Blocks kann die `open`-Direktive verwendet werden, um alle Typen und callables zu importieren, die in einem bestimmten Namespace definiert sind, und auf diese über ihren nicht qualifizierten Namen zu verweisen. 

Eine solche `open` Direktive besteht aus dem Schlüsselwort `open`, gefolgt vom zu öffnenden Namespace und einem abschließenden Semikolon.

Beispiel:

```qsharp
open Microsoft.Quantum.Canon;
```

Optional kann ein Kurzname für den geöffneten Namespace definiert werden, sodass alle Elemente aus diesem Namespace durch den definierten Kurznamen qualifiziert werden können (und müssen). Ein solcher Kurzname wird definiert, indem das Schlüsselwort `as` gefolgt vom gewünschten Kurznamen vor dem Semikolon in einer `open` Direktive hinzugefügt wird:

```qsharp
open Microsoft.Quantum.Math as Math;
```

Alle `open` Direktiven müssen vor allen `function`-, `operation`-oder `newtype` Deklarationen im-Namespace Block angezeigt werden.
Die `open`-Direktive gilt für den gesamten Namespace Block in einer Datei.

## <a name="user-defined-type-declarations"></a>Deklarationen von benutzerdefinierten Typen

Q # bietet Benutzern die Möglichkeit, neue benutzerdefinierte Typen zu deklarieren, wie im Abschnitt " [Q # Type Model](xref:microsoft.quantum.language.type-model) " beschrieben.
Benutzerdefinierte Typen sind unterschiedlich, auch wenn die Basis Typen identisch sind.
Insbesondere, wenn die zugrunde liegenden Typen identisch sind, gibt es keine automatische Konvertierung zwischen Werten von zwei benutzerdefinierten Typen.

Eine benutzerdefinierte Typdeklaration besteht aus dem Schlüsselwort `newtype`, gefolgt vom Namen des benutzerdefinierten Typs, einer `=`, einer gültigen Typspezifikation und einem abschließenden Semikolon.

Beispiel:

```qsharp
newtype PairOfInts = (Int, Int);
```

Jede f #-Quelldatei kann eine beliebige Anzahl benutzerdefinierter Typen deklarieren.
Typnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-und Funktionsnamen in Konflikt stehen.

Es ist nicht möglich, zirkuläre Abhängigkeiten zwischen benutzerdefinierten Typen zu definieren. Rekursive Typen sind in Q # daher nicht möglich.

## <a name="operation-declarations"></a>Vorgangs Deklarationen

Vorgänge sind das Kernstück von Q #, ungefähr analog zu Funktionen in anderen Sprachen.
Jede f #-Quelldatei kann eine beliebige Anzahl von Vorgängen definieren.

Vorgangs Namen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit Typ-und Funktionsnamen verursachen.

Eine Vorgangs Deklaration besteht aus dem Schlüsselwort `operation`, gefolgt vom Symbol, das den Namen des Vorgangs, ein typisiertes bezeichnertupel, das die Argumente für den Vorgang definiert, einen Doppelpunkt `:`, eine Typanmerkung, die den Ergebnistyp des Vorgangs beschreibt, optional eine Anmerkung mit den Vorgangs Merkmalen, eine öffnende geschweifte Klammer `{`, den Text der Vorgangs Deklaration und eine abschließende schließende geschweifte Klammer `}`.

Der Text der Vorgangs Deklaration besteht entweder aus der Standard Implementierung oder einer Liste von spezialisierer.
Die Standard Implementierung kann direkt innerhalb der-Deklaration angegeben werden, wenn nur die Implementierung der Standardtext Spezialisierung explizit angegeben werden muss.
In diesem Fall ist eine Anmerkung mit den Vorgangs Merkmalen in der Deklaration hilfreich, um sicherzustellen, dass der Compiler automatisch andere Spezialisierungs Vorgänge auf der Grundlage der Standard Implementierung generiert. 

Beispiel: 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

Vorgangs Merkmale definieren, welche Arten von functoren auf den deklarierten Vorgang angewendet werden können und welche Auswirkungen Sie haben. Wenn ein Vorgang eine einheitliche Transformation implementiert, ist es möglich, zu definieren, wie der Vorgang beim *angleichen oder* *Steuern*erfolgt.
Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur deklariert werden. Die entsprechende Implementierung für jede solche implizit deklarierte Spezialisierung wird dann vom Compiler generiert. Im obigen Beispiel werden eine Adjoint-, eine gesteuerte und eine kontrollierte Adjoint-Spezialisierung vom Compiler generiert. 

Wenn die Implementierung nicht vom Compiler generiert werden kann, kann Sie explizit angegeben werden. Solche expliziten Spezialisierungs Deklarationen können entweder aus einer geeigneten Generierungs Direktive bestehen, die verdeutlichen, wie eine bestimmte Spezialisierung erstellt werden soll, oder einer benutzerdefinierten Implementierung. Der oben genannte Code in `PrepareEntangledPair` z. b. Äquivalent zum folgenden Code, der explizite Spezialisierungs Deklarationen enthält: 

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
Wenn der Compiler die Implementierung für eine bestimmte Spezialisierung ohne weitere Anweisungen (z. b. eine präzisere Generierungs Direktive) nicht generieren kann, oder wenn eine effizientere Implementierung angegeben werden kann, kann die Implementierung auch manuell definiert werden.

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

Damit ein Vorgang die Anwendung des `Adjoint`-und/oder `Controlled`-funktors unterstützt, muss der Rückgabetyp notwendigerweise `Unit`werden. 


### <a name="explicit-specialization-declarations"></a>Explizite Spezialisierungs Deklarationen

F #-Vorgänge können die folgenden expliziten Spezialisierungs Deklarationen enthalten:

- Die `body` Spezialisierung gibt die Implementierung des Vorgangs ohne angewendete Funktoren an.
- Die `adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit angewendetem `Adjoint`-Funktor an.
- Die `controlled` Spezialisierung gibt die Implementierung des Vorgangs mit angewendetem `Controlled`-Funktor an.
- Die `controlled adjoint` Spezialisierung gibt die Implementierung des Vorgangs an, bei der die `Adjoint`-und `Controlled`-Funktoren angewendet wurden.
  Diese Spezialisierung kann auch `adjoint controlled`benannt werden, da die beiden Funktoren in den Weg gehen.


Eine Vorgangs Spezialisierung besteht aus dem Spezialisierungs Kennzeichen (z. b. `body`oder `adjoint`usw.), gefolgt von einem der folgenden:

- Eine explizite Deklaration, wie unten beschrieben.
- Eine-Direktive, die dem Compiler mitteilt, wie die Spezialisierung generiert werden soll, einer der folgenden:
  - `intrinsic`, das angibt, dass die Spezialisierung vom Zielcomputer bereitgestellt wird.
  - `distribute`, die für die `controlled`-und `controlled adjoint`-Spezialisierung verwendet werden kann.
    Bei Verwendung mit `controlled`wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge im `body`anwendet.
    Bei Verwendung mit `controlled adjoint`wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in der `adjoint` Spezialisierung anwendet.
  - `invert`, das angibt, dass der Compiler die `adjoint` Spezialisierung berechnen soll, indem er die `body`umschließt, d. h. die Reihenfolge der Vorgänge wird umgekehrt und das Adjoint-Attribut auf jeden angewendet.
    Bei Verwendung mit `adjoint controlled`gibt dies an, dass der Compiler die Spezialisierung berechnen soll, indem er die `controlled` Spezialisierung umkehrt.
  - `self`, um anzugeben, dass die Adjoint-Spezialisierung mit der `body` Spezialisierung identisch ist.
    Dies ist für die `adjoint`-und `adjoint controlled` Spezialisierung zulässig.
    Bei `adjoint controlled`impliziert `self`, dass die `adjoint controlled` Spezialisierung mit der `controlled` Spezialisierung identisch ist.
  - `auto`, um anzugeben, dass der Compiler eine geeignete Direktive auswählen soll, die angewendet werden soll.
    `auto` darf nicht für die `body` Spezialisierung verwendet werden.

Die Direktiven und `auto` alle erfordern ein Schließ Endes Semikolon `;`.
Die `auto`-Direktive wird in die folgende Generations Anweisung aufgelöst, wenn eine explizite Deklaration des `body` bereitgestellt wird:

- Die `adjoint` Spezialisierung wird gemäß der-Direktive `invert`generiert.
- Die `controlled` Spezialisierung wird gemäß der-Direktive `distribute`generiert.
- Die `adjoint controlled` Spezialisierung wird gemäß der-Direktive generiert `invert` wenn eine explizite Deklaration für `controlled` angegeben ist, aber nicht für `adjoint`, und andernfalls `distribute`.

> [!TIP]   
> Wenn es sich um einen eigenständigen Vorgang handelt, geben Sie entweder die Adjoint-oder die kontrollierte Adjoint-Spezialisierung mithilfe der Generations Direktive an `self` um dem Compiler zu ermöglichen, diese Informationen zu Optimierungszwecken zu verwenden.

Eine Spezialisierungs Deklaration, die eine benutzerdefinierte Implementierung enthält, besteht aus einem argumenttupel, gefolgt von einem Anweisungsblock mit dem Q #-Code, der die Spezialisierung implementiert.
In der Argumentliste wird `...` verwendet, um die für den Vorgang als Ganzes deklarierten Argumente darzustellen.
Bei `body` und `adjoint`sollte die Argumentliste immer `(...)`sein. bei `controlled` und `adjoint controlled`sollte die Argumentliste ein Symbol sein, das das Array von Steuerelement-Qubits, gefolgt von `...`, in Klammern eingeschlossen ist. beispielsweise `(controls,...)`.

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

### <a name="adjoint"></a>Adjoint

Das Adjoint eines Vorgangs gibt an, wie die komplexe konjugierte, die den Vorgang implementiert, implementiert wird, d. h., wie der Vorgang bei umgekehrter Ausführung funktioniert.
Es ist zulässig, einen Vorgang ohne Adjoint anzugeben. Beispielsweise haben Messvorgänge keinen Adjoint, da Sie nicht invertierbar sind.
Ein Vorgang unterstützt das `Adjoint`-Funktor, wenn seine Deklaration eine implizite oder explizite Deklaration einer Adjoint-Spezialisierung enthält.
Eine explizit deklarierte, kontrollierte Adjoint-Spezialisierung impliziert, dass eine Adjoint-Spezialisierung vorhanden ist. 

Für einen Vorgang, dessen Text Wiederholungs-bis-Erfolg-Schleifen, Set-Anweisungen, Messungen, Rückgabe Anweisungen oder Aufrufe von anderen Vorgängen enthält, die den `Adjoint`-Funktor nicht unterstützen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach der `invert`-oder `auto`-Direktive nicht möglich.

### <a name="controlled"></a>Klimatisiert

Die kontrollierte Version eines Vorgangs gibt an, wie eine Quantum-gesteuerte Version des Vorgangs implementiert wird, d. h., wie ein Vorgang angewendet wird, wenn er auf den Zustand eines Quantum-Register angewendet wird.
Eine ausführlichere Beschreibung finden Sie im Abschnitt " [gesteuert](xref:microsoft.quantum.language.type-model#controlled) ".

Es ist zulässig, einen Vorgang ohne kontrollierte Version anzugeben. Beispielsweise haben Messvorgänge keine kontrollierte Version, da Sie nicht steuerbar sind.
Ein Vorgang unterstützt den `Controlled`-Funktor nur dann, wenn seine Deklaration eine implizite oder explizite Deklaration einer kontrollierten Spezialisierung enthält.
Eine explizit deklarierte, kontrollierte Adjoint-Spezialisierung impliziert das vorhanden sein einer kontrollierten Spezialisierung. 

Bei einem Vorgang, dessen Text Aufrufe anderer Vorgänge enthält, die den `Controlled`-Funktor nicht unterstützen, ist das automatische Erstellen einer kontrollierten Spezialisierung nach der `distribute`-oder `auto`-Direktive nicht möglich.

### <a name="controlled-adjoint"></a>Kontrollierter Adjoint

Die kontrollierte Adjoint-Version eines Vorgangs gibt an, wie eine Quantum-gesteuerte Version des Adjoint-Vorgangs des Vorgangs implementiert wird.
Es ist zulässig, einen Vorgang ohne kontrollierte Adjoint-Version anzugeben. Messvorgänge haben beispielsweise keine kontrollierte Adjoint-Version, da Sie weder steuerbar noch invertierbar sind.

Eine kontrollierte Adjoint-Spezialisierung für einen Vorgang muss nur dann vorhanden sein, wenn sowohl ein Adjoint-als auch eine gesteuerte Spezialisierung vorhanden sind. In diesem Fall wird das vorhanden sein der kontrollierten Adjoint-Spezialisierung abgeleitet, und vom Compiler wird eine entsprechende Spezialisierung generiert, wenn keine Implementierung explizit definiert wurde. 

Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die nicht über eine kontrollierte Adjoint-Version verfügen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach den `invert``distribute`-oder `auto`-Direktive nicht möglich.


### <a name="examples"></a>Beispiele

Eine Vorgangs Deklaration kann so einfach wie die folgende sein, die den primitiven Pauli X-Vorgang definiert:

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

Im folgenden wird der teleportvorgang definiert.

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation EPR (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        EPR(target, ancilla);

        // Do the teleportation
        Adjoint EPR (ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a>Funktionsdeklarationen

Funktionen sind rein klassische Routinen in Q #.
Jede f #-Quelldatei kann eine beliebige Anzahl von Funktionen definieren.

Eine Funktionsdeklaration besteht aus dem Schlüsselwort `function`, gefolgt von dem Symbol, das den Namen der Funktion, ein typisiertes bezeichnertupel, eine Typanmerkung, die den Rückgabetyp der Funktion beschreibt, und einem Anweisungsblock, der die Implementierung der Funktion beschreibt.

Der Anweisungsblock, der eine Funktion definiert, muss in `{` eingeschlossen und `}` wie jeder andere Anweisungsblock sein.

Funktionsnamen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit den Vorgangs-und Typnamen aufweisen.
Funktionen dürfen keine Qubits zuordnen oder ausleihen, oder es werden keine Vorgänge aufgerufen. Die partielle Anwendung von Vorgängen oder die Übergabe von typisierten Werten ist in Ordnung.

Beispiel:

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
