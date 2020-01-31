---
title: 'Alles zusammengeh Otten: f #-Techniken | Microsoft-Dokumentation'
description: 'Alles zusammengeh Otten: f #-Techniken'
uid: microsoft.quantum.techniques.puttingittogether
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 3605826da159757d4b321dbf4ec6acd7f4e6be05
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820163"
---
# <a name="putting-it-all-together-teleportation"></a>Alles zusammen: teleportierung #
Wir kehren zum Beispiel der in [Quantum](xref:microsoft.quantum.concepts.circuits)-Leitungen definierten Teleportations-Verbindung zurück. Wir werden diese Informationen verwenden, um die bisher gelernten Konzepte zu veranschaulichen. Eine Erläuterung der Quantum-Teleportation finden Sie unten für Personen, die mit der Theorie nicht vertraut sind, gefolgt von einer exemplarischen Vorgehensweise der Code Implementierung in f #. 

## <a name="quantum-teleportation-theory"></a>Quantum-Teleportation: Theorie
Die Quantum-Teleportation ist eine Technik zum Senden eines unbekannten Quantums (als "__Message__" bezeichnet) von einem Qubit an einem Speicherort an einem Ort an einem Qubit an einem anderen Speicherort (wir bezeichnen diese Qubits als __"This" bzw__. "__there__"). Wir können unsere __Nachricht__ mithilfe der Dirac-Notation als Vektor darstellen: 

$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $

Der Status des __nachrichtenqubits__ ist für uns unbekannt, da wir die Werte von $ \alpha $ und $ \beta $ nicht kennen.

### <a name="step-1-create-an-entangled-state"></a>Schritt 1: Erstellen eines entkoppelt-Zustands
Um die __Nachricht__ zu senden, muss das Qubit __hier__ mit dem Qubit entkoppelt __werden.__ Dies wird erreicht, indem ein Hadamard-Gate, gefolgt von einem CNOT-Gate, angewendet wird. Sehen wir uns die mathematische hinter diesen Gate-Vorgängen an.

Wir beginnen mit den __Qubits und__ __dort__ sowohl im $ \ket-{0}$ State. Nachdem Sie diese Qubits entwursten, befinden Sie sich im Zustand:

$ $ \ket{\phi ^ +} = \frac{1}{\sqrt{2}} (\ket{00} + \ket{11}) $ $

### <a name="step-2-send-the-message"></a>Schritt 2: Senden der Nachricht
Zum Senden der __Nachricht__ wenden wir zuerst ein CNOT Gate mit dem __Message__ Qubit und diesem Qubit als Eingaben an (das __Nachrichten__ Qubit ist das Steuerelement, __und das this-Qubit__ ist das __Ziel-__ Qubit, in diesem Fall). Dieser Eingabe Zustand kann geschrieben werden:

$ $ \ket{\psi}\ket{\phi ^ +} = (\alpha\ket{0} + \beta\ket{1}) (\frac{1}{\sqrt{2}} (\ket{00} + \ket{11})) $ $

Dies erweitert zu:

$ $ \ket{\psi}\ket{\phi ^ +} = \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{100} + \frac{\beta}{\sqrt{2}} \ket{111} $ $

Zur Erinnerung: das CNOT-Gate flippt das Ziel-Qubit, wenn das Steuerelement-Qubit 1 ist. Eine Eingabe von $ \ket{000}$ führt z. b. zu keiner Änderung, da das erste Qubit (das Steuerelement) 0 ist. Nehmen Sie jedoch einen Fall, bei dem das erste Qubit 1 ist, z. b. eine Eingabe von $ \ket{100}$. In diesem Beispiel ist die Ausgabe $ \ket{110}$, da das zweite Qubit (das Ziel) vom CNOT-Gate gekippt wird.

Sehen wir uns nun unsere Ausgabe an, sobald das CNOT-Gate in der obigen Eingabe agiert hat. Es wird folgendes Ergebnis ausgegeben:

$ $ \frac{\alpha}{\sqrt{2}} \ket{000} + \frac{\alpha}{\sqrt{2}} \ket{011} + \frac{\beta}{\sqrt{2}} \ket{110} + \frac{\beta}{\sqrt{2}} \ket{101} $ $

Der nächste Schritt zum Senden der __Nachricht__ ist das Anwenden eines Hadamard-Gates auf das __Message__ -Qubit (das die erste Qubit jedes Begriffs ist). 

Zur Erinnerung: das Hadamard-Gate führt Folgendes aus:

Eingabe | Output
---------------------------| ---------------------------------------------------------------
$ \ket{0}$  | $ \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}) $
$ \ket{1}$  | $ \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}) $

Wenn wir das Hadamard-Gate auf das erste Qubit für jeden Begriff der obigen Ausgabe anwenden, erhalten wir folgendes Ergebnis:

$ $ \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{00} + \frac{\alpha}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0} + \ket{1})) \ket{11} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{10} + \frac{\beta}{\sqrt{2}} (\frac{1}{\sqrt{2}} (\ket{0}-\ket{1})) \ket{01} $ $

Beachten Sie, dass jeder Begriff $2 \frac{1}{\sqrt{2}} $ Factors hat. Wir können diese multiplizieren, indem wir folgendes Ergebnis erhalten:

$ $ \bruchteil {\alpha}{2}(\ket{0} + \ket{1}) \ket{00} + \bruchteil {\alpha}{2}(\ket{0} + \ket{1}) \ket{11} + \bruchteil {\beta}{2}(\ket{0}-\ket{1}) \ket{10} + \bruchteil {\beta}{2}(\ket{0}-\ket{1}) \ket{01} $ $

Der $ \frac-{1}{2}$ Factor ist für jeden Begriff üblich, sodass wir ihn jetzt außerhalb der Klammern nehmen können:

$ $ \frac{1}{2}\big [\alpha (\ket{0} + \ket{1}) \ket{00} + \alpha (\ket{0} + \ket{1}) \ket{11} + \beta (\ket{0}-\ket{1}) \ket{10} + \beta (\ket{0}-\ket{1}) \ket{01}\big] $ $

Anschließend können wir die Klammern für jeden Begriff multiplizieren, der Folgendes bietet:

$ $ \frac{1}{2}\big [\alpha\ket{000} + \alpha\ket{100} + \alpha\ket{011} + \alpha\ket{111} + \beta\ket{010}-\beta\ket{110} + \beta\ket{001}-\beta\ket{101}\big] $ $

### <a name="step-3-measure-the-result"></a>Schritt 3: Messen des Ergebnisses

Da __hier__ __und die entkoppelt werden,__ wirkt sich jede Messung __hier__ auf den Status von __dort__aus. Wenn wir das erste und zweite Qubit (__Nachricht__ und __hier__) messen, können wir aufgrund dieser Eigenschaft von entanglement erfahren, welcher Zustand in __vorhanden__ ist. 

* Wenn wir ein Ergebnis 00 Messen und erzielen, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind. Das ist $ \alpha\ket{000} + \beta\ket{001}$. Dieser kann auf $ \ket{00}(\alpha\ket{0} + \beta\ket{1}) $ umformatiert werden. Wenn wir also das erste und zweite Qubit als "00" Messen, wissen wir, __dass sich das__dritte Qubit in dem Status "$ (\alpha\ket{0} + \beta\ket{1}) $" befindet.
* Wenn wir ein Ergebnis 01 Messen und erhalten, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind. Das ist $ \alpha\ket{011} + \beta\ket{010}$. Dieser kann auf $ \ket{01}(\alpha\ket{1} + \beta\ket{0}) $ umformatiert werden. Wenn wir also das erste und zweite Qubit als "01" Messen, wissen wir, __dass sich das__dritte Qubit in dem Status "$ (\alpha\ket{1} + \beta\ket{0}) $" befindet.
* Wenn wir das Ergebnis 10 Messen und erzielen, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind. Das ist $ \alpha\ket{100}-\beta\ket{101}$. Dieser kann auf $ \ket{10}(\alpha\ket{0}-\beta\ket{1}) $ umformatiert werden. Wenn wir also das erste und zweite Qubit als 10 Messen, wissen wir, __dass sich das__dritte Qubit in dem Status $ (\alpha\ket{0}-\beta\ket{1}) $ befindet.
* Wenn wir das Ergebnis 11 Messen und erzielen, wird die Superposition reduziert, sodass nur die Begriffe mit diesem Ergebnis konsistent sind. Das ist $ \alpha\ket{111}-\beta\ket{110}$. Dieser kann auf $ \ket{11}(\alpha\ket{1}-\beta\ket{0}) $ umformatiert werden. Wenn wir also das erste und zweite Qubit als 11 Messen, wissen wir, __dass sich das__dritte Qubit in dem Status $ (\alpha\ket{1}-\beta\ket{0}) $ befindet.

### <a name="step-4-interpret-the-result"></a>Schritt 4: interpretieren des Ergebnisses

Die ursprüngliche __Nachricht__ , die wir senden wollten, lautete als Erinnerung:

$ $ \ket{\psi} = \alpha\ket{0} + \beta\ket{1} $ $

Wir müssen __das Qubit__ in diesen Zustand bringen, damit der empfangene Zustand der gewünschte Zustand ist. 

* Wenn wir gemessen haben und das Ergebnis 00 erhalten haben, befindet sich das dritte Qubit __dort__im Status $ (\alpha\ket{0} + \beta\ket{1}) $. Da es sich hierbei um die beabsichtigte __Nachricht__handelt, ist keine Änderung erforderlich.
* Wenn wir gemessen und ein Ergebnis von 01 erhalten haben, befindet sich das dritte Qubit __dort__im Status $ (\alpha\ket{1} + \beta\ket{0}) $. Dies unterscheidet sich von der vorgesehenen __Nachricht__, aber durch das Anwenden eines not-Gates erhält der gewünschte Status $ (\alpha\ket{0} + \beta\ket{1}) $.
* Wenn wir gemessen und ein Ergebnis von 10 erhalten haben, befindet sich das dritte Qubit __dort__im Status $ (\alpha\ket{0}-\beta\ket{1}) $. Dies unterscheidet sich von der vorgesehenen __Nachricht__, aber durch Anwenden eines Z-Gates erhält der gewünschte Status $ (\alpha\ket{0} + \beta\ket{1}) $.
* Wenn wir gemessen haben und ein Ergebnis von 11 erhalten haben, befindet sich das dritte Qubit __dort__im Status $ (\alpha\ket{1}-\beta\ket{0}) $. Dies unterscheidet sich von der vorgesehenen __Nachricht__, aber durch das Anwenden eines nicht-Gates gefolgt von einem Z-Gate erhält der gewünschte Zustand $ (\alpha\ket{0} + \beta\ket{1}) $.

Zusammenfassend gilt: Wenn wir Messen und das erste Qubit den Wert 1 hat, wird ein Z-Gate angewendet. Wenn wir Messen und das zweite Qubit den Wert 1 hat, wird ein Not-Gate angewendet.

### <a name="summary"></a>Zusammenfassung
Nachstehend sehen Sie eine Textbuch-Quantum-Verbindung, die die Teleportation implementiert. Wenn Sie von links nach rechts wechseln, sehen Sie Folgendes:
- Schritt 1: entwenden Sie __hier__ und __dort__ , indem Sie ein Hadamard-Gate und ein CNOT Gate anwenden.
- Schritt 2: Senden der __Nachricht__ mit einem CNOT-Gate und einem Hadamard-Gate
- Schritt 3: die Messung der ersten und zweiten Qubits, der __Nachricht__ und __hier__.
- Schritt 4: Anwenden eines nicht-Gates oder eines Z-Gates, abhängig vom Ergebnis der Messung in Schritt 3.

![' Teleport (msg: Qubit, there: Qubit): Unit '](~/media/teleportation.svg)

## <a name="quantum-teleportation-code"></a>Quantum-Teleportation: Code

Wir haben unsere Verbindung für Quantum-Teleportation:

![' Teleport (msg: Qubit, there: Qubit): Unit '](~/media/teleportation.svg)

Wir können nun jeden der Schritte in dieser Quantum-Leitung in Q # übersetzen.

### <a name="step-0-definition"></a>Schritt 0: Definition
Bei der Durchführung von Teleportationen müssen wir die __Nachricht__ kennen, die gesendet werden soll, und an welche Stelle wir Sie senden möchten (__dort__). Aus diesem Grund definieren wir zunächst einen neuen teleportvorgang, der zwei Qubits als Argumente, `msg` und `there`erhält:

```qsharp
operation Teleport(msg : Qubit, there : Qubit) : Unit {
```

Wir müssen auch eine Qubit-`here` zuordnen, die wir mit einem `using` Block erreichen:

```qsharp
    using (here = Qubit()) {
```

### <a name="step-1-create-an-entangled-state"></a>Schritt 1: Erstellen eines entkoppelt-Zustands
Anschließend können Sie das entkoppelt-Paar zwischen `here` und `there` erstellen, indem Sie die @"microsoft.quantum.intrinsic.h" und @"microsoft.quantum.intrinsic.cnot" Vorgänge verwenden:

```qsharp
        H(here);
        CNOT(here, there);
```

### <a name="step-2-send-the-message"></a>Schritt 2: Senden der Nachricht
Anschließend verwenden wir das nächste $ \operatschmue{CNOT} $ und $H $ Gates, um das Nachrichten-Qubit zu verschieben:

```qsharp
        CNOT(msg, here);
        H(msg);
```

### <a name="step-3--4-measuring-and-interpreting-the-result"></a>Schritt 3 & 4: Messen und interpretieren des Ergebnisses
Zum Schluss verwenden wir @"microsoft.quantum.intrinsic.m", um die Messungen durchzuführen und die notwendigen Gate-Vorgänge auszuführen, um den gewünschten Zustand zu erhalten, wie von `if`-Anweisungen angegeben:

```qsharp
        // Measure out the entanglement
        if (M(msg) == One)  { Z(there); }
        if (M(here) == One) { X(there); }
```

Dadurch wird die Definition des Teleportation-Operators abgeschlossen, sodass wir die Zuteilung `here`, den Text beenden und den Vorgang beenden können.

```qsharp
    }
}
```
