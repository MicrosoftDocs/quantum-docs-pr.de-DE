---
title: 'F #-Standardbibliotheken-Fehlerkorrektur | Microsoft-Dokumentation'
description: 'F #-Standardbibliotheken-Fehlerkorrektur'
author: QuantumWriter
uid: microsoft.quantum.libraries.error-correction
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: e1b78cf94ae0a043ad275d4cb06b230eafd7fc85
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2019
ms.locfileid: "74863196"
---
# <a name="error-correction"></a>Fehlerkorrektur #

## <a name="introduction"></a>Einführung ##

Wenn beim klassischen Computing ein wenig vor Fehlern geschützt werden soll, kann es häufig ausreichen, das Bit durch Wiederholen des Daten Bits durch ein *logisches Bit* darzustellen.
Nehmen wir beispielsweise an, dass $ \overline{0} = $0 die Codierung des Datentyps 0 ist. dabei wird die Zeile oberhalb der Bezeichnung 0 verwendet, um anzugeben, dass es sich um eine Codierung eines Bits im Zustand 0 handelt.
Wenn auf ähnliche Weise $ \overline{1} = $111 angezeigt wird, verfügen wir über einen einfachen Wiederholungs Code, der vor einem Bit-Flip-Fehler schützt.
Das heißt, wenn eine der drei Bits gekippt wird, können wir den Zustand des logischen Bits wiederherstellen, indem wir eine Mehrheits Stimme treffen.
Obwohl die klassische Fehlerkorrektur in diesem speziellen Beispiel ein viel reicheres Thema ist (Wir empfehlen die [Einführung in die Codierungstheorie von Lint](https://www.springer.com/us/book/9783540641339)), zeigt der obige Wiederholungs Code bereits auf ein mögliches Problem beim Schutz von Quantum-Informationen.
Das [No-Klon-Theorem](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) impliziert, dass bei der Messung der einzelnen Qubit-Werte und der Stimme der Mehrheit des obigen klassischen Codes die genauen Informationen, die wir zu schützen versuchen, verloren gehen.

In der Quantum-Einstellung werden wir sehen, dass die Messung problematisch ist. Wir können weiterhin die oben beschriebene Codierung implementieren.
Dies ist hilfreich, um zu sehen, wie die Fehlerkorrektur in den Quantum-Fall generalisiert werden kann.
Geben Sie daher $ \ket{\overline{0}} = \ket{000} = \ket{0} \otimes \ket{0} \otimes \ket{0}$ ein, und lassen Sie $ \ket{\overline{1}} = \ket{111}$.
Anschließend haben wir in Linearität unseren Wiederholungs Code für alle Eingaben definiert. Beispiel: $ \ket{\overline{+}} = (\ket{\overline{0}} + \ket{\overline{1}})/\sqrt{2} = (\ket{000} + \ket{111})/\sqrt{2}$.
Insbesondere, wenn Sie einen Bit-Flip-Fehler $X _1 $ Act für das mittlere Qubit, sehen wir, dass die Korrektur, die für beide branches erforderlich ist, genau $X _1 $: $ $ \begin{align} x_1 \ket{\overline{+}} & = \frac{1}{\sqrt{2}} \left (x_1 \ket{000} + x_1 \ket{111} \right) \\\\ & = \frac{1}{\sqrt{2}} \left (\ket{010} + \ket{101} \right).
\end{align} $ $

Um zu sehen, wie wir erkennen können, dass dies der Fall ist, ohne den Zustand zu messen, den wir zu schützen versuchen, ist es hilfreich, die einzelnen anderen Bits-Flip-Fehler in die logischen Zustände zu schreiben:

| Fehler $E $ | $E \ket{\overline{0}} $ | $E \ket{\overline{1}} $ |
| --- | --- | --- |
| $ \boldone $ | $ \ket{000}$ | $ \ket{111}$ |
| $X _0 $ | $ \ket{100}$ | $ \ket{011}$ |
| $X _1 $ | $ \ket{010}$ | $ \ket{101}$ |
| $X _2 $ | $ \ket{001}$ | $ \ket{110}$ |

Um den Zustand zu schützen, den wir codieren, müssen wir die drei Fehler voneinander und von der Identität $ \boldone $ unterscheiden können, ohne zwischen "$ \ket{\overline{0}} $" und "$ \ket{\overline{1}} $" zu unterscheiden.
Wenn z. b. $Z _0 $ gemessen wird, erhalten wir ein anderes Ergebnis für "$ \ket{\overline{0}} $" und "$ \ket{\overline{1}} $" im Fehlerfall, sodass der codierte Zustand reduziert wird.
Auf der anderen Seite können Sie $Z _0 Z_1 $ Messen, die Parität der ersten beiden Bits in den einzelnen Berechnungs Status Zuständen.
Beachten Sie, dass jede Messung eines Pauli-Operators überprüft, welcher eigen Wert der gemessene Wert entspricht. Daher können wir für jeden Status $ \ket{\psi} $ in der obigen Tabelle $Z _0-Z_1 \ket{\psi} $ berechnen, um festzustellen, ob "$ \pm\ket{\psi} $" erhalten wird.
Beachten Sie, dass $Z _0 Z_1 \ket{000} = \ket{000}$ und diese $Z _0 Z_1 \ket{111} = \ket{111}$, sodass wir feststellen, dass diese Maßeinheit den beiden codierten Zuständen dasselbe entspricht.
Auf der anderen Seite $Z _0 Z_1 \ket{100} =-\ket{100}$ und $Z _0 Z_1 \ket{011} =-\ket{011}$. das Ergebnis der Messung $Z _0 $ zeigt daher nützliche Informationen über den Fehler an.

Um dies hervorzuheben, wiederholen wir die obige Tabelle, fügen jedoch die Ergebnisse der Messung $Z _0 Z_1 $ und $Z _1 Z_2 $ für jede Zeile hinzu.
Wir bezeichnen die Ergebnisse der einzelnen Messungen durch das Vorzeichen des Eigenwerts, der beobachtet wird, entweder $ + $ oder $-$, der den Q #-`Result` Werten von `Zero` bzw. der `One`entspricht.

| Fehler $E $ | $E \ket{\overline{0}} $ | $E \ket{\overline{1}} $ | Ergebnis der $Z _0 Z_1 $ | Ergebnis der $Z _1 Z_2 $ |
| --- | --- | --- | --- | --- |
| $ \boldone $ | $ \ket{000}$ | $ \ket{111}$ | $+$ | $+$ |
| $X _0 $ | $ \ket{100}$ | $ \ket{011}$ | $-$ | $+$ |
| $X _1 $ | $ \ket{010}$ | $ \ket{101}$ | $-$ | $-$ |
| $X _2 $ | $ \ket{001}$ | $ \ket{110}$ | $+$ | $-$ |

Folglich wird durch die Ergebnisse der beiden Messungen eindeutig festgelegt, welcher bitflip-Fehler aufgetreten ist, ohne dass Informationen zu dem von uns codierten Zustand offengelegt werden.
Wir bezeichnen diese Ergebnisse als ein- *Syndrom*und verweisen auf den Prozess der Zuordnung eines-Syndroms zu dem Fehler, der die wieder *Herstellung*verursacht hat.
Insbesondere betonen wir, dass die Wiederherstellung eine *klassische* Inferenz ist, die als Eingabe das betreffende-Syndrom übernimmt und eine Korrektur für die Behebung von Fehlern zurückgibt, die möglicherweise aufgetreten sind.

> [!NOTE]
> Der obige bitflip-Code kann nur mit einzelnen Bit-Flip-Fehlern korrigiert werden. Das heißt, ein `X` Vorgang, der auf einem einzelnen Qubit agiert.
> Wenn Sie `X` auf mehr als ein Qubit anwenden, wird "$ \ket{\overline{0}} $" auf "$ \ket{\overline{1}} $" nach der Wiederherstellung zugeordnet.
> Auf ähnliche Weise wird durch das Anwenden eines Phasen kippen `Z` $ \ket{\overline{1}} $ zu $-\ket{\overline{1}} $ zugeordnet. Daher wird $ \ket{\overline{+}} $ zu $ \ket{\overline{-}} $ zugeordnet.
> Im Allgemeinen können Codes erstellt werden, um eine größere Anzahl von Fehlern zu verarbeiten und $Z $ Errors sowie $X $ Errors zu behandeln.

Die Erkenntnis, dass wir Messungen in der Quantum-Fehlerkorrektur beschreiben können, die auf die gleiche Weise für alle Code Zustände agieren, ist der Grund für die *stabilisatformalität*.
Q # Canon bietet ein Framework zum Beschreiben der Codierung in und Decodierung von Stabilisator-Codes und zum Beschreiben der Art und Weise, wie eine von Fehlern wieder hergestellt wird.
In diesem Abschnitt werden dieses Framework und seine Anwendung für einige einfache Quantum-Fehler Behebungs Codes beschrieben.

> [!TIP]
> Eine vollständige Einführung in die Stabilisator-Formalität geht über den Rahmen dieses Abschnitts hinaus.
> Wir freuen uns auf Leser, die mehr über den [Mann 2009](https://arxiv.org/abs/0904.2557)lernen möchten.

## <a name="representing-error-correcting-codes-in-q"></a>Darstellen von Fehler Behebungs Codes in f # ##

Zur Unterstützung der Angabe von Fehler Behebungs Codes bietet Q # Canon mehrere verschiedene benutzerdefinierte Typen:

- <xref:microsoft.quantum.errorcorrection.logicalregister> `= Qubit[]`: gibt an, dass ein Register von Qubits als Codeblock eines Fehler Behebungs Codes interpretiert werden soll.
- <xref:microsoft.quantum.errorcorrection.syndrome> `= Result[]`: gibt an, dass ein Array von Messergebnissen als das auf einem Codeblock gemessene Syndrom interpretiert werden soll.
- <xref:microsoft.quantum.errorcorrection.recoveryfn> `= (Syndrome -> Pauli[])`: gibt an, dass eine *klassische* Funktion verwendet werden soll, um ein-Syndrom zu interpretieren und eine Korrektur zurückzugeben, die angewendet werden soll.
- <xref:microsoft.quantum.errorcorrection.encodeop> `= ((Qubit[], Qubit[]) => LogicalRegister)`: gibt an, dass ein Vorgang Qubits zum Darstellen von Daten zusammen mit neuen Ancilla-Qubits annimmt, um einen Codeblock eines Fehler Behebungs Codes zu entwickeln.
- <xref:microsoft.quantum.errorcorrection.decodeop> `= (LogicalRegister => (Qubit[], Qubit[]))`: bezeichnet, als ein Vorgang einen Codeblock eines Fehlers korrigiert, der den Code in die Daten-Qubits korrigiert, und die für die Darstellung von-Tool Informationen verwendeten Ancilla-Qubits.
- <xref:microsoft.quantum.errorcorrection.syndromemeasop> `= (LogicalRegister => Syndrome)`: bezeichnet einen Vorgang, der zum Extrahieren von Informationen aus einem Codeblock verwendet werden soll, ohne dass der durch den Code geschützte Zustand gestört wird.

Schließlich stellt der Kanon den <xref:microsoft.quantum.errorcorrection.qecc> Typ bereit, um die anderen Typen zu erfassen, die zum Definieren eines Quantum-Fehler Behebungs Codes erforderlich sind. Jedem Stabilisator-quantencode ist die Codelänge $n $, die Anzahl $k $ logischer Qubits und die minimale Entfernung $d $ zugeordnet, die häufig in der Notation ⟦ $n $, $k $, $d $ ⟧ gruppiert sind. Die <xref:microsoft.quantum.errorcorrection.bitflipcode>-Funktion definiert z. b. den ⟦ 3, 1, 1 ⟧ Bit-Flip-Code:

```qsharp
let encodeOp = EncodeOp(BitFlipEncoder);
let decodeOp = DecodeOp(BitFlipDecoder);
let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
    [PauliZ, PauliZ, PauliI],
    [PauliI, PauliZ, PauliZ]
], _, MeasureWithScratch));
let code = QECC(encodeOp, decodeOp, syndMeasOp);
```

Beachten Sie, dass der `QECC` Typ *keine* Wiederherstellungs Funktion enthält.
Dies ermöglicht es uns, die Wiederherstellungs Funktion zu ändern, die bei der Behebung von Fehlern verwendet wird, ohne die Definition des Codes selbst zu ändern. Diese Möglichkeit ist besonders nützlich, wenn Sie Feedback von Charakterisierungs Messungen in das Modell integrieren, das von der Wiederherstellung angenommen wird.

Nachdem ein Code auf diese Weise definiert wurde, können wir den <xref:microsoft.quantum.errorcorrection.recover>-Vorgang verwenden, um nach Fehlern wiederherzustellen:

```qsharp
let code = BitFlipCode();
let fn = BitFlipRecoveryFn();
let X0 = ApplyPauli([PauliX, PauliI, PauliI], _);
using (scratch = Qubit[nScratch]) {
    let logicalRegister = encode(data, scratch);
    // Cause an error.
    X0(logicalRegister);
    Recover(code, fn, logicalRegister);
    let (decodedData, decodedScratch) = decode(logicalRegister);
    ApplyToEach(Reset, decodedScratch);
}
```

Wir untersuchen dies im [bitflip-Codebeispiel](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code)ausführlicher.

Abgesehen vom Bit-Flip-Code wird der Q #-Kanon mit Implementierungen des [perfekten 5-Qubit-Codes](https://arxiv.org/abs/quant-ph/9602019)bereitgestellt, und der [sieben-Qubit](https://arxiv.org/abs/quant-ph/9705052)-Code, der beide einen beliebigen Single-Qubit-Fehler beheben kann.
