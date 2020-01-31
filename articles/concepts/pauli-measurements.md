---
title: Pauli-Messungen
description: Pauli-Messungen
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 0a3ee595022ec389ecadcab081ccd126cb3252ae
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819908"
---
# <a name="pauli-measurements"></a>Pauli-Messungen

In den vorherigen Diskussionen haben wir uns auf Berechnungsbasis Messungen konzentriert.
Tatsächlich gibt es weitere allgemeine Messungen, die bei der Quantum-Berechnung auftreten, die aus Sicht der Sicht bequem in Bezug auf Berechnungsbasis Messungen ausgedrückt werden können.
Bei der Arbeit mit Q # sind die gängigsten Arten von Messungen wahrscheinlich *Pauli-Messungen*, die Berechnungsbasis Messungen verallgemeinern, um Messungen in anderen Basen und die Parität zwischen verschiedenen Qubits zu berücksichtigen.
In solchen Fällen ist es üblich, das Messen eines Pauli-Operators zu erörtern, im Allgemeinen ein Operator wie $X, Y, Z $ oder $Z \otimes Z, x\otimes X, x\otimes Y $ und so weiter.

> [!TIP]
> In Q # werden multiqubit-Pauli-Operatoren in der Regel durch Arrays vom Typ `Pauli[]`dargestellt.
> Wenn Sie z. b. $X \otimes Z \otimes Y $ darstellen möchten, können Sie das Array `[PauliX, PauliZ, PauliY]`verwenden.

Die Erörterung von Messungen in Form von Pauli-Operatoren ist vor allem im Unterfeld der Quantum-Fehlerkorrektur üblich.
In f # wird eine ähnliche Konvention befolgt. Wir erläutern nun diese Alternative Ansicht von Messungen.

Bevor wir uns mit den Details der Bedeutung einer Pauli-Messung beschäftigen, ist es sinnvoll, sich Gedanken darüber zu machen, was ein einzelnes Qubit innerhalb eines Quantum-Computers in den Quantum-Zustand versetzt.
Stellen Sie sich vor, dass ein $n $-Qubit-Quantum-Status vorhanden ist. Wenn dann ein Qubit sofort gemessen wird, werden die Hälfte der $2 ^ n $-Möglichkeiten, in denen sich der Zustand befinden könnte, sofort ausgeschlossen.
Mit anderen Worten: die Messung projiziert den Quantum-Zustand auf einen von zwei halben Leerzeichen.
Wir können die Art und Weise verallgemeinern, in der Messungen für diese Intuition durchdacht werden.

Um diese Teilbereiche zu beschreiben, benötigen wir eine Sprache für die Beschreibung.
Eine Möglichkeit, die beiden Teilbereiche zu beschreiben, besteht darin, Sie durch eine Matrix anzugeben, die nur zwei eindeutige Eigenwerte aufweist, die von der Konvention auf $ \pm $1 übernommen werden.
Um ein einfaches Beispiel für das Beschreiben von Teilbereichen auf diese Weise zu beschreiben, sollten Sie $Z $:

$ $ \begin{align} Z & = \begin{bmatrix} 1 & 0 \\\\ 0 &-1 \end{bmatrix}.
\end{align} $ $

Wenn Sie die diagonalen Elemente der "Pauli-$Z $"-Matrix lesen, sehen Sie, dass $Z $ zwei Eigenvektoren, $ \ket{0}$ und $ \ket{1}$ mit den entsprechenden eigen Werten $ \pm $1 hat.
Wenn wir also das Qubit Messen und `Zero` abrufen (entsprechend dem State $ \ket{0}$), wissen wir, dass der Status des Qubit ein $ + $1-eigen Status des $Z $-Operators ist.
Ebenso wissen wir, wenn wir `One`erhalten, dass der Status des Qubit ein $-$1-eigen Status $Z $ ist.
Dieser Prozess wird in der Sprache von Pauli-Messungen als "Messen von Pauli $Z $" bezeichnet und ist vollständig mit der Durchführung einer Berechnungsbasis Messung identisch.

Eine beliebige $2 \ Times $2-Matrix, bei der es sich um eine einheitliche Transformation von $Z $ handelt, erfüllt auch diese Kriterien.
Das heißt, wir könnten auch eine Matrix $A = U ^ \dagger Z U $ verwenden, wobei $U $ eine beliebige andere einheitliche Matrix ist, um eine Matrix zu erstellen, die die beiden Ergebnisse einer Messung in den $ \pm $1-Eigenvektoren definiert.
Die Notation von Pauli-Messungen verweist auf diese einheitliche Äquivalenz, indem $X-, Y-und Z $-Messungen als gleichwertige Messungen identifiziert werden, die zur Gewinnung von Informationen aus einem Qubit führen könnten.
Diese Messungen werden zur einfacheren Verwendung unten angegeben.


|Pauli-Messung  |Einheitliche Transformation  |
|-------------------|------------------------|
| $Z $               | $ \boldone $             |
| $X $               | $H $                    |
| $Y $               | $HS ^ {\dagger} $         |

Das heißt, dass bei Verwendung dieser Sprache "Measure $Y $" dem Anwenden von $HS ^ \dagger $ entspricht und dann auf Berechnungsbasis gemessen wird, wobei [`S`](xref:microsoft.quantum.intrinsic.s) ein System interner Quantum-Vorgang ist, der manchmal als "Phasen Gate" bezeichnet wird und durch die einheitliche Matrix simuliert werden kann.

$ $ \begin{align} S = \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.
\end{align} $ $

Dies entspricht auch dem Anwenden von $HS ^ \dagger $ auf den Quantum State Vector und der anschließenden Messung $Z $, sodass der folgende Vorgang dem `Measure([PauliY], [q]])`entspricht:

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

Der richtige Zustand wird dann durch umwandeln auf die Berechnungsbasis gefunden, was das Anwenden $SH $ auf den Quantum-Status Vektor bedeutet. im obigen Code Ausschnitt wird die Transformation zurück zur Berechnungsbasis automatisch durch die Verwendung des `within … apply`-Blocks verarbeitet.

In f # wird das Ergebnis---, das heißt, die klassischen Informationen, die aus der Interaktion mit dem Status---extrahiert werden, werden durch einen `Result` Wert $j \in \\{\texttt{Zero}, \texttt{One}\\} $ angegeben, der angibt, ob das Ergebnis im $ (-1) ^ j $ eigen Raum des ggf


## <a name="multiple-qubit-measurements"></a>Multiple-Qubit-Messungen

Die Messungen von multiqubit-Pauli-Operatoren sind ähnlich definiert, wie in:

$ $ Z\otimes Z = \begin{bmatrix}1 & 0 & 0 & 0\\\\ 0 &-1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 & 1 \ Ende {bmatrix}.
$$

Folglich bilden die tensorflow-Produkte von zwei "Pauli-$Z $"-Operatoren eine Matrix aus zwei Leerzeichen, die aus "$ + $1" und "$-$1 Eigenwerte" bestehen
Wie bei einem Single-Qubit-Fall bilden beide einen halben Raum, was bedeutet, dass die Hälfte des zugänglichen Vektor Raums zum $ + $1-eigen Raum und die verbleibende Hälfte bis zum $-$1-eigen Raum gehört.
Im Allgemeinen ist es einfach, von der Definition des tensorflow-Produkts aus zu sehen, dass ein beliebiges tensorflow-Produkt von Pauli-$Z $-Operatoren und die Identität auch diesem entspricht.
Beispiel:

$ $ \begin{align} Z \otimes \boldone = \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 &-1 & 0 \\\\ 0 & 0 & 0 &-1 \end{bmatrix}.
\end{align} $ $

Wie zuvor beschreibt jede einheitliche Transformation dieser Matrizen auch zwei halb Bereiche mit der Bezeichnung "$ \pm $1 Eigenwerte".
Beispielsweise $X \otimes X = h\otimes h (z\otimes Z) h\otimes h $ aus der Identität, die $Z = HXH $.
Ähnlich wie der One-Qubit-Fall können alle zwei-Qubit-Pauli-Messungen als $U ^ \dagger (z\otimes \id) U $ für $4 \ mal $4 einheitliche Matrizen $U $ geschrieben werden. Die Transformationen in der folgenden Tabelle werden aufgelistet.

> [!NOTE]
> In der folgenden Tabelle wird $ \operatorname{curap} $ verwendet, um die Matrix $ $ \begin{align} \operatorname{tauap} & = \left (\begin{Matrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{Matrix}\right) \end{align} $ $ zum Simulieren des intrinsischen Vorgangs [`SWAP`](xref:microsoft.quantum.intrinsic)verwendet.

|Pauli-Messung     |Einheitliche Transformation  |
|----------------------|------------------------|
| $Z \otimes \boldone $ | $ \boldone \otimes \boldone $ |
| $Z \otimes \boldone $ | $ \boldone\otimes \boldone $ |
| $X \otimes \boldone $ | $H \otimes \boldone $ |
| $Y \otimes \boldone $ | $HS ^ \dagger\otimes \boldone $ |
| $ \boldone \otimes Z $ | $ \operatschmue{tauap} $ |
| $ \boldone \otimes X $ | $ (H\otimes \boldone) \operatschmue{Swap} $ |
| $ \boldone \otimes Y $ | $ (HS ^ \dagger\otimes \boldone) \operatorname{tauap} $ |
| $Z \otimes Z $ | $ \operatschmue{CNOT}\_{10}$ |
| $X \otimes Z $ | $ \operatschmue{CNOT}\_{10}(h\otimes \boldone) $ |
| $Y \otimes Z $ | $ \operatschmue{CNOT}\_{10}(HS ^ \dagger\otimes \boldone) $ |
| $Z \otimes X $ | $ \operatschmue{CNOT}\_{10}(\boldone\otimes H) $ |
| $X \otimes X $ | $ \operatschmue{CNOT}\_{10}(h\otimes H) $ |
| $Y \otimes X $ | $ \operatschmue{CNOT}\_{10}(HS ^ \dagger\otimes H) $ |
| $Z \otimes Y $ | $ \operatschmue{CNOT}\_{10}(\boldone \otimes HS ^ \dagger) $ |
| $X \otimes Y $ | $ \operatschmue{CNOT}\_{10}(h\otimes HS ^ \dagger) $ |
| $Y \otimes Y $ | $ \operatschmue{CNOT}\_{10}(HS ^ \dagger\otimes HS ^ \dagger) $ |

Hier wird der [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) Vorgang aus folgendem Grund angezeigt.
Jedes Pauli-Maß, das "$ \boldone $ Matrix" nicht enthält, entspricht einem einheitlichen $Z \otimes Z $ durch die oben genannte Argumentation.
Die Eigenwerte $Z \otimes Z $ hängen nur von der Parität der Qubits ab, aus denen die einzelnen Berechnungsbasis Vektor bestehen, und die kontrollierten Vorgänge dienen dazu, diese Parität zu berechnen und im ersten Bit zu speichern.
Nachdem das erste Bit gemessen wurde, können wir die Identität des resultierenden halb Raums wiederherstellen, was dem Messen des Pauli-Operators entspricht.

Ein weiterer Hinweis: in diesem Fall ist es möglicherweise verlockend zu vermuten, dass die Messung $Z \otimes Z $ mit der sequenziellen Messung $Z \otimes \mathbb{1}$ und dann $ \mathbb{1} \otimes z $ übereinstimmt. diese Annahme wäre false.
Der Grund hierfür ist, dass die Messung $Z \otimes Z $ den Quantum-Zustand entweder in den "$ + $1"-oder "$-$1"-Zustand dieser Operatoren projiziert.
Messen von $Z \otimes \mathbb{1}$ und dann $ \mathbb{1} \otimes Z $ projiziert den Quantum-Status Vektor zuerst auf einen halben Bereich von $Z \otimes \mathbb{1}$ und dann auf einen halben Bereich von $ \mathbb{1} \otimes z $.
Da es vier Berechnungsbasis Vektoren gibt, verringert die Durchführung beider Messungen den Zustand auf einen Viertel Raum und reduziert ihn somit auf einen einzelnen Berechnungsbasis Vektor.

## <a name="correlations-between-qubits"></a>Korrelationen zwischen Qubits
Eine weitere Möglichkeit zum Messen von tensorflow-Produkten von Pauli-Matrizen, wie $X \otimes X $ oder $Z \otimes Z $, besteht darin, dass mit diesen Messungen Informationen untersucht werden können, die in den Korrelationen zwischen den beiden Qubits gespeichert sind.
Durch Messen $X \otimes \id $ können Sie Informationen untersuchen, die lokal im ersten Qubit gespeichert sind.
Obwohl beide Arten von Messungen in Quantum Computing gleichermaßen wertvoll sind, beleuchtet das erste die Leistungsfähigkeit von Quantum Computing.
Es wird deutlich, dass die Informationen, die Sie erlernen möchten, bei der Quantum-Verarbeitung nicht in einem einzelnen Qubit gespeichert werden, sondern nicht lokal in allen Qubits gespeichert werden. Daher wird dies nur durch eine gemeinsame Messung (z. b. $Z \otimes Z $) bewirkt. Informationen werden zu einem Manifest.

Beispielsweise möchten wir bei der Fehlerkorrektur häufig ermitteln, welche Fehler aufgetreten sind, wenn Sie nichts über den Zustand erfahren möchten, den wir zu schützen versuchen.
Das Beispiel für [bitflip-Code](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) zeigt ein Beispiel dafür, wie Sie dies mithilfe von Messungen wie $Z \otimes z \otimes \id $ und $ \id \otimes z \otimes z $ erreichen können.
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

Beliebige Pauli-Operatoren, z. b. $X \otimes Y \otimes Z \otimes \boldone $, können ebenfalls gemessen werden.
Alle derartigen tensorflow-Produkte von Pauli-Operatoren verfügen nur über zwei Eigenwerte $ \pm $1, und beide eigen Räume bilden halbräume des gesamten Vektor Bereichs.
Daher stimmen Sie mit den oben genannten Anforderungen überein.

In Q # geben solche Messungen $j $ zurück, wenn die Messung ein Ergebnis im Eigen Bereich von Sign $ (-1) ^ j $ ergibt.
Die Verwendung von Pauli-Messungen als integriertes Feature in Q # ist hilfreich, da die Messung solcher Operatoren lange Ketten von gesteuerten und nicht-Transformationen und Basis Transformationen erfordert, um die Diagonalisierung $U $ Gate zu beschreiben, die erforderlich ist, um den Vorgang als tensorflow-Produkt $Z $ und $ \id $ auszudrücken.
Wenn Sie festlegen können, dass Sie eine dieser vordefinierten Messungen durchführen möchten, müssen Sie sich keine Gedanken darüber machen, wie Sie Ihre Basis so transformieren, dass eine Berechnungsbasis Messung die erforderlichen Informationen bereitstellt.
Q # behandelt alle notwendigen Basis Transformationen automatisch.
Weitere Informationen finden Sie in den [`Measure`](xref:microsoft.quantum.intrinsic.measure) -und [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) Vorgängen.

## <a name="the-no-cloning-theorem"></a>Das No-Klon-Theorem

Quantum-Informationen sind leistungsstark.
Dadurch können wir beeindruckende Dinge, wie z. b. die Faktor Zahlen, exponentiell beschleunigen als die besten bekannten klassischen Algorithmen, oder korrelierte Elektronen Systeme effizient simulieren, die für eine genaue Simulation exponentialkosten benötigen.
Es gibt jedoch Einschränkungen hinsichtlich der Leistungsfähigkeit von Quantum Computing.
Eine solche Einschränkung wird durch das *No-Klon-Theorem*angegeben.

Das No-Klon-Theorem weist einen passenden Namen auf.
Sie lässt das Klonen generischer Quantenzustände durch einen Quantum-Computer nicht zu.
Der Beweis für das Theorem ist erstaunlich einfach.
Obwohl ein vollständiger Nachweis für das No-Klon-Theorem für unsere Erörterung etwas zu technisch ist, liegt der Nachweis im Fall von zusätzlichen Qubits in unserem Bereich. (zusätzliche Qubits sind für den temporären Speicherplatz während einer Berechnung verwendeter Qubits und können in f # problemlos verwendet und verwaltet werden. Weitere Informationen finden Sie unter <xref:microsoft.quantum.techniques.qubits>).

Bei solch einem Quantum-Computer muss der Klon Vorgang durch eine einheitliche Matrix beschrieben werden.
Die Messung wird nicht zugelassen, da der Quantum-Zustand beschädigt wird, den wir klonen wollen.
Um den Klon Vorgang zu simulieren, soll für die einheitliche Matrix die Eigenschaft $ $ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi} $ $ für jeden Status $ \ket{\psi} $ verwendet werden.
Die Linearität-Eigenschaft der Matrix Multiplikation impliziert dann, dass für jeden zweiten Quantum-Status $ \ket{\phi} $,

$ $ \begin{align} U \left [\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right] \ket{0} & = \frac{1}{\sqrt{2}} u\ket {\ Phi} \ Ket{0} + \frac{1}{\sqrt{2}} u\ket {\ PSI} \ Ket{0} \\\\ & = \frac{1}{\sqrt{2}} \left (\ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi} \right) \\\\ & \nE \left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right) \otimes \ Left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right).
\end{align} $ $

Dies stellt die grundlegende Intuition hinter dem No-Klon-Theorem bereit: jedes Gerät, das einen unbekannten Quantum-Zustand kopiert, muss Fehler in mindestens einigen der von ihm kopierte Zustände auslösen.
Während die Hauptannahme, dass der Cloner für den Eingabe Status linear agiert, durch Hinzufügen und Messen von hilfssbits verletzt werden kann, können solche Interaktionen auch Informationen über das System durch die maßstatistik und eine exakte Vermeidung von auch in solchen Fällen Klonen.
Einen ausführlicheren Nachweis für das No-Klon-Theorem finden Sie unter, [um weitere Informationen](xref:microsoft.quantum.more-information)zu erhalten.

Das No-Clone-Theorem ist wichtig für ein qualitativ hochwertiges Verständnis von Quantum Computing, denn wenn Sie Quantum-Zustände ingünstig Klonen könnten, erhalten Sie eine nahezu magische Möglichkeit, von Quantum-Zuständen zu lernen.
Tatsächlich könnten Sie das Prinzip der geunten Unsicherheit von Heisenberg verletzen.
Alternativ können Sie einen optimalen Cloner verwenden, um ein einzelnes Beispiel aus einer komplexen Quantum-Distribution zu erstellen und alles zu erlernen, was Sie möglicherweise über die Verteilung von nur einem Beispiel erfahren.
Dies würden Sie tun, wenn Sie eine Münze kippen und Köpfen beobachten und dann einen Freund über das Ergebnis informieren, dass er antwortet, dass die Verteilung der Münze Bernoulli mit $p = 0.512643 \ ldots $! "lauten muss.  Eine solche Anweisung wäre nicht unsinnig, weil ein Teil der Informationen (das Heads-Ergebnis) einfach nicht die vielen Informationen bereitstellen kann, die erforderlich sind, um die Verteilung ohne wesentliche vorherige Informationen zu codieren.
Ebenso wie ohne vorherige Informationen können wir einen quantumstatus nicht ganz genau so Klonen, wie wir ein Ensemble dieser Münzen nicht vorbereiten können, ohne $p $ zu kennen.

Informationen sind in Quantum Computing nicht kostenlos.
Jedes gemessene Qubit liefert ein einzelnes Bit an Informationen, und das No-Klon-Theorem zeigt, dass es keine Hintertür gibt, die ausgenutzt werden kann, um den grundlegenden Kompromiss zwischen den Informationen, die über das System gewonnen wurden, und der auf ihm aufgerufenen Störung zu umgehen.
