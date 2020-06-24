---
title: Pauli-Messungen
description: Erfahren Sie, wie Sie mit Einzel-und Multi-Qubit-Pauli-Mess Vorgängen arbeiten.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 7f10c4ad5eb325da97552d60ff47ea89a699f08d
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269472"
---
# <a name="pauli-measurements"></a>Pauli-Messungen

In den vorherigen Diskussionen haben wir uns auf Berechnungsbasis Messungen konzentriert.
Tatsächlich gibt es weitere allgemeine Messungen, die bei der Quantum-Berechnung auftreten, die aus Sicht der Sicht bequem in Bezug auf Berechnungsbasis Messungen ausgedrückt werden können.
Bei der Arbeit mit Q # sind die gängigsten Arten von Messungen wahrscheinlich *Pauli-Messungen*, die Berechnungsbasis Messungen verallgemeinern, um Messungen in anderen Basen und die Parität zwischen verschiedenen Qubits zu berücksichtigen.
In solchen Fällen ist es üblich, das Messen eines Pauli-Operators zu erörtern, im Allgemeinen ein Operator wie $X, Y, Z $ oder $Z \otimes Z, x \otimes x, x \otimes Y $ usw.

> [!TIP]
> In Q # werden multiqubit-Pauli-Operatoren in der Regel durch Arrays des Typs dargestellt `Pauli[]` .
> Wenn Sie z. b. $X \otimes Z \otimes Y darstellen möchten $ , können Sie das Array verwenden `[PauliX, PauliZ, PauliY]` .

Die Erörterung von Messungen in Form von Pauli-Operatoren ist vor allem im Unterfeld der Quantum-Fehlerkorrektur üblich.
In f # wird eine ähnliche Konvention befolgt. Wir erläutern nun diese Alternative Ansicht von Messungen.

Bevor wir uns mit den Details der Bedeutung einer Pauli-Messung beschäftigen, ist es sinnvoll, sich Gedanken darüber zu machen, was ein einzelnes Qubit innerhalb eines Quantum-Computers in den Quantum-Zustand versetzt.
Stellen Sie sich vor, dass ein $n $ -Qubit-Quantum-Status vorhanden ist. Anschließend wird ein Qubit sofort mit der Hälfte der $2 ^ n- $ Möglichkeiten, in denen sich der Zustand befindet, fest.
Mit anderen Worten: die Messung projiziert den Quantum-Zustand auf einen von zwei halben Leerzeichen.
Wir können die Art und Weise verallgemeinern, in der Messungen für diese Intuition durchdacht werden.

Um diese Teilbereiche zu beschreiben, benötigen wir eine Sprache für die Beschreibung.
Eine Möglichkeit, die beiden Teilbereiche zu beschreiben, besteht darin, Sie durch eine Matrix anzugeben, die nur zwei eindeutige Eigenwerte hat, die gemäß der Konvention $ \pm 1 übernommen werden $ .
Um ein einfaches Beispiel für das Beschreiben von Teilbereichen auf diese Weise zu beschreiben, sollten Sie $Z beachten $ :

$ $ \begin{align}
  Z & = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \end{ bmatrix } .
\end{align}
$$

Wenn Sie die diagonalen Elemente der Pauli-$Z $ Matrix lesen, sehen Sie, dass $Z $ zwei Eigenvektoren, $ \ket{0$ } und $ \ket{1$ } , mit den entsprechenden eigen Werten $ \pm 1 aufweist $ .
Wenn wir also das Qubit Messen und Abrufen `Zero` (entsprechend dem Status $ \ket{0$ } ), wissen wir, dass der Status des Qubit ein $ + 1-Zustand $ des $Z Operators ist $ .
Ebenso wissen wir, wenn wir `One` , dass der Zustand unseres Qubit ein "$-1"- $ Zustand der $Z ist $ .
Dieser Prozess wird in der Sprache von Pauli-Messungen als "Messen von Pauli $Z $ " bezeichnet und ist vollständig mit der Durchführung einer Berechnungsbasis Messung identisch.

Jede $2 \times 2- $ Matrix, die eine einheitliche Transformation von $Z ist, $ erfüllt diese Kriterien ebenfalls.
Das heißt, wir könnten auch eine Matrix $A = U ^ \dagger Z U verwenden $ , wobei $U eine $ beliebige andere einheitliche Matrix ist, um eine Matrix zu erstellen, die die beiden Ergebnisse einer Messung in den $ \pm 1- $ Eigenvektoren definiert.
Die Notation von Pauli-Messungen verweist auf diese einheitliche Äquivalenz, indem $X-, Y-und Z- $ Messungen als gleichwertige Messungen identifiziert werden, die zur Gewinnung von Informationen aus einem Qubit führen könnten.
Diese Messungen werden zur einfacheren Verwendung unten angegeben.


|Pauli-Messung  |Einheitliche Transformation  |
|-------------------|------------------------|
| $Z$               | $ \boldone$             |
| $X$               | $H$                    |
| $Y$               | $HS ^ {\dagger}$         |

Das heißt, "Measure $Y $ " entspricht der Anwendung von $HS ^ \dagger $ und der anschließenden Messung, wobei ein System interner [`S`](xref:microsoft.quantum.intrinsic.s) Quantum-Vorgang ist, der manchmal als "Phasen Gate" bezeichnet wird, und durch die einheitliche Matrix simuliert werden kann.

$ $ \begin{align}
    S = \begin{bmatrix}
        1 & 0 \\ \\ 0 & i \end{ bmatrix } .
\end{align}
$$

Dies entspricht auch dem Anwenden von $HS ^ \dagger $ auf den Quantum-Status Vektor und dem anschließenden Messen $Z $ , sodass der folgende Vorgang dem entspricht `Measure([PauliY], [q])` :

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

Der richtige Zustand wird dann durch umwandeln auf die Berechnungsbasis gefunden, was das Anwenden $ von $SH auf den Quanten Zustands Vektor bedeutet. im obigen Code Ausschnitt wird die Transformation zurück zur Berechnungsbasis automatisch durch die Verwendung des- `within … apply` Blocks verarbeitet.

In f # wird das Ergebnis---, das heißt, die klassischen Informationen, die aus der Interaktion mit dem Status---extrahiert werden, werden durch einen `Result` Wert $j \in \\ {\texttt{Zero } , \texttt{One} $ angegeben, der } \\ angibt, ob das Ergebnis im $ (-1) ^ j- $ eigen Raum des angehängten Pauli-Operators ist.


## <a name="multiple-qubit-measurements"></a>Multiple-Qubit-Messungen

Die Messungen von multiqubit-Pauli-Operatoren sind ähnlich definiert, wie in:

$ $ Z \otimes z = \begin{ bmatrix } 1 &0 &0&0 \\\\ 0 & -1&0&0 \\\\ 0&0 & -1&0 \\\\ 0&0&0&1 \end{bmatrix} .
$$

Daher bilden die tensorflow-Produkte von zwei Pauli-$Z- $ Operatoren eine Matrix, die aus zwei Leerzeichen besteht, die aus $ + 1 $ und $-1 $ eigen Werten bestehen.
Wie bei einem Single-Qubit-Fall bilden beide einen halben Leerraum, was bedeutet, dass die Hälfte des zugänglichen Vektor Raums zum $ + 1 $ -eigen Raum und die verbleibende Hälfte des Eigen Raums $-1 gehört $ .
Im Allgemeinen ist es einfach, aus der Definition des tensorflow-Produkts zu erkennen, dass ein beliebiges tensorflow-Produkt von Pauli-$Z $ -Operatoren und die Identität auch diesem entspricht.
Beispiel:

$ $ \begin{align}
    Z \otimes \boldone = \begin{bmatrix}
        1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 &-1 & 0 \\ \\ 0 & 0 & 0 &-1 \ End{ bmatrix } .
\end{align}
$$

Wie zuvor beschreibt jede einheitliche Transformation dieser Matrizen auch zwei halbe Leerzeichen, die durch $ \pm 1 $ Eigenwerte bezeichnet werden.
Beispielsweise $X \otimes X = h \otimes h (z \otimes z) h \otimes h $ von der Identität, die $Z = HXH ist $ .
Ähnlich wie der One-Qubit-Fall können alle zwei-Qubit-Pauli-Messungen als $U ^ \dagger (Z \otimes \id) U $ für $4 \times 4 $ einheitliche Matrizen $U $ geschrieben werden. Die Transformationen in der folgenden Tabelle werden aufgelistet.

> [!NOTE]
> In der folgenden Tabelle wird $ \operatorname{Swap $ verwendet, } um die Matrix $ $ \begin{align anzugeben.}
>     \operatschmue{Swap } & = \left (\begin{Matrix}
>         1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{Matrix } \right) \end{align}
> $ $, mit dem der systeminterne Vorgang simuliert wird [`SWAP`](xref:microsoft.quantum.intrinsic) .

|Pauli-Messung     |Einheitliche Transformation  |
|----------------------|------------------------|
| $Z \otimes \boldone$ | $ \boldone \otimes \boldone$ |
| $Z \otimes \boldone$ | $ \boldone \otimes \boldone$ |
| $X \otimes \boldone$ | $H \otimes \boldone$ |
| $Y \otimes \boldone$ | $HS ^ \dagger \otimes \boldone$ |
| $ \boldone \otimes Z$ | $ \operatschmue{Swap}$ |
| $ \boldone \otimes X$ | $ (H \otimes \boldone) \operatschmue{Swap}$ |
| $ \boldone \otimes Y$ | $ (HS ^ \dagger \otimes \boldone) \operatschmue{Swap}$ |
| $Z \otimes Z$ | $ \operatorname{CNOT } \_ {10}$ |
| $X \otimes Z$ | $ \operatschmue{CNOT } \_ {10 } (H \otimes \boldone) $ |
| $Y \otimes Z$ | $ \operatschmue{CNOT } \_ {10 } (HS ^ \dagger \otimes \boldone) $ |
| $Z \otimes X$ | $ \operatschmue{CNOT } \_ {10 } (\boldone \otimes H) $ |
| $X \otimes X$ | $ \operatschmue{CNOT } \_ {10 } (h \otimes h) $ |
| $Y \otimes X$ | $ \operatschmue{CNOT } \_ {10 } (HS ^ \dagger \otimes H) $ |
| $Z \otimes Y$ | $ \operatschmue{CNOT } \_ {10 } (\boldone \otimes HS ^ \dagger) $ |
| $X \otimes Y$ | $ \operatorname{CNOT } \_ {10 } (H \otimes HS ^ \dagger) $ |
| $Y \otimes Y$ | $ \operatschmue{CNOT } \_ {10 } (HS ^ \dagger \otimes HS ^ \dagger) $ |

Hier wird der [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) Vorgang aus folgendem Grund angezeigt.
Jede Pauli-Messung, die die "$ \boldone"-Matrix nicht enthält, $ entspricht der oben beschriebenen Argumentation einem einheitlichen $Z \otimes Z $ .
Die Eigenwerte von $Z \otimes Z $ hängen nur von der Parität der Qubits ab, aus denen die einzelnen Berechnungsbasis Vektor bestehen, und die kontrollierten Vorgänge dienen dazu, diese Parität zu berechnen und im ersten Bit zu speichern.
Nachdem das erste Bit gemessen wurde, können wir die Identität des resultierenden halb Raums wiederherstellen, was dem Messen des Pauli-Operators entspricht.

Ein weiterer Hinweis: Obwohl es möglicherweise verlockend ist, zu übernehmen, dass die Messung $Z \otimes Z $ identisch mit der sequenziellen Messung $Z \otimes \mathbb{1$ } und dann $ \mathbb{1 } \otimes Z ist $ , wäre diese Annahme falsch.
Der Grund hierfür ist, dass \otimes die Messung $Z Z $ den Quantum-Zustand entweder in den "$ + 1"- $ oder "$-1"- $ Zustand dieser Operatoren projiziert.
Wenn Sie $Z \otimes \mathbb{1$ } und dann $ \mathbb{1\otimes z Messen, wird } $ der Quantum-Status Vektor zuerst auf einen halben Bereich $Z \otimes \mathbb{1$ } und dann auf einen halben Bereich von $ \mathbb{1\otimes } z projiziert $ . Da es vier Berechnungsbasis Vektoren gibt, verringert die Durchführung beider Messungen den Zustand auf einen Viertel Raum und reduziert ihn somit auf einen einzelnen Berechnungsbasis Vektor.

## <a name="correlations-between-qubits"></a>Korrelationen zwischen Qubits
Eine weitere Möglichkeit zum Messen von tensorflow-Produkten von Pauli-Matrizen, wie $X \otimes X $ oder $Z \otimes Z $ , besteht darin, dass mit diesen Messungen die in den Korrelationen zwischen den beiden Qubits gespeicherten Informationen untersucht werden können.
\otimesWenn Sie $X \id Messen $ , sehen Sie sich die lokal im ersten Qubit gespeicherten Informationen an.
Obwohl beide Arten von Messungen in Quantum Computing gleichermaßen wertvoll sind, beleuchtet das erste die Leistungsfähigkeit von Quantum Computing.
Es ist offensichtlich, dass die Informationen, die Sie erlernen möchten, häufig nicht in einem einzigen Qubit gespeichert werden, sondern nicht lokal in allen Qubits gespeichert werden und daher nur durch eine gemeinsame Messung (z. b. $Z Z), dass \otimes $ diese Informationen zu einem Manifest werden.

Beispielsweise möchten wir bei der Fehlerkorrektur häufig ermitteln, welche Fehler aufgetreten sind, wenn Sie nichts über den Zustand erfahren möchten, den wir zu schützen versuchen.
Das [Bit-Flip-Code](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) Beispiel zeigt ein Beispiel dafür, wie Sie dies mithilfe von Messungen wie $Z \otimes z \otimes \id $ und $ \id \otimes z \ otimes z erreichen können $ .
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

Beliebige Pauli-Operatoren wie \otimes Z. b. $X Y \otimes Z \otimes \boldone $ können ebenfalls gemessen werden.
Alle derartigen tensorflow-Produkte von Pauli-Operatoren haben nur zwei Eigenwerte $ \pm 1, $ und beide eigen Räume bilden halbräume des gesamten Vektor Bereichs.
Daher stimmen Sie mit den oben genannten Anforderungen überein.

In Q # geben solche Messungen $j zurück, $ Wenn die Messung ein Ergebnis im Eigen Bereich von Sign $ (-1) ^ j ergibt $ .
Die Verwendung von Pauli-Messungen als integriertes Feature in Q # ist hilfreich, da die Messung solcher Operatoren lange Ketten von gesteuerten und nicht-Transformationen und Basis Transformationen erfordert, um die Diagonalisierung $U Gate zu beschreiben, $ die erforderlich ist, um den Vorgang als tensorflow-Produkt $Z $ und $ \id auszudrücken $ . Wenn Sie festlegen können, dass Sie eine dieser vordefinierten Messungen durchführen möchten, müssen Sie sich keine Gedanken darüber machen, wie Sie Ihre Basis so transformieren, dass eine Berechnungsbasis Messung die erforderlichen Informationen bereitstellt.
Q # behandelt alle notwendigen Basis Transformationen automatisch.
Weitere Informationen finden Sie unter den [`Measure`](xref:microsoft.quantum.intrinsic.measure) -und- [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) Vorgängen.

## <a name="the-no-cloning-theorem"></a>Das No-Klon-Theorem

Quantum-Informationen sind leistungsstark.
Dadurch können wir beeindruckende Dinge, wie z. b. die Faktor Zahlen, exponentiell beschleunigen als die besten bekannten klassischen Algorithmen, oder korrelierte Elektronen Systeme effizient simulieren, die für eine genaue Simulation exponentialkosten benötigen.
Es gibt jedoch Einschränkungen hinsichtlich der Leistungsfähigkeit von Quantum Computing.
Eine solche Einschränkung wird durch das *No-Klon-Theorem*angegeben.

Das No-Klon-Theorem weist einen passenden Namen auf.
Sie lässt das Klonen generischer Quantenzustände durch einen Quantum-Computer nicht zu.
Der Beweis für das Theorem ist erstaunlich einfach.
Obwohl ein vollständiger Nachweis für das No-Klon-Theorem für unsere Erörterung etwas zu technisch ist, liegt der Nachweis im Fall von zusätzlichen Qubits in unserem Bereich. (zusätzliche Qubits sind für den temporären Speicherplatz während einer Berechnung verwendeter Qubits und können problemlos in Q # verwendet werden, siehe [geliehene Qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).

Bei solch einem Quantum-Computer muss der Klon Vorgang durch eine einheitliche Matrix beschrieben werden.
Die Messung wird nicht zugelassen, da der Quantum-Zustand beschädigt wird, den wir klonen wollen.
Um den Klon Vorgang zu simulieren, soll für die einheitliche Matrix die Eigenschaft $ $ U \ket { \psi } \ket{0= } \ket { \psi } \ket { \psi verwendet werden.}
$ $ für einen beliebigen Status $ \ket { \psi } $.
Die Linearität-Eigenschaft der Matrix Multiplikation impliziert dann, dass für jeden zweiten Quantum-Status $ \ket { \phi } $,

$ $ \begin{align}
    U \left [\bruchteil {1 } {\sqrt{2} } \left (\ket { \phi } + \ket { \psi } \right) \right] \ket{0}
    & = \bruchteil {1 } {\sqrt{2} } U \ket { \phi } \ket{0}
      + \bruchteil {1 } {\sqrt{2} } U \ket { \psi } \ket{0 } \\ \\ & = \bruchteil {1 } {\sqrt{2} } \left (\ket { \phi } \ket { \phi } + \ket { \psi } \ket { \psi}
        \right) \\ \\ & \nE \left (\bruchteil {1 } {\sqrt{2} } \left (\ket { \phi } + \ket { \psi } \right) \right) \otimes \left (\bruchteil {1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right).
\end{align}
$$

Dies stellt die grundlegende Intuition hinter dem No-Klon-Theorem bereit: jedes Gerät, das einen unbekannten Quantum-Zustand kopiert, muss Fehler in mindestens einigen der von ihm kopierte Zustände auslösen.
Während die Hauptannahme, dass der Cloner den Eingabe Status linear verarbeitet, durch Hinzufügen und Messen von hilfssbits verletzt werden kann, können solche Interaktionen auch Informationen über das System durch die maßstatistik und das exakte Klonen in solchen Fällen vermeiden.
Einen ausführlicheren Nachweis für das No-Klon-Theorem finden Sie unter, [um weitere Informationen](xref:microsoft.quantum.more-information)zu erhalten.

Das No-Clone-Theorem ist wichtig für ein qualitativ hochwertiges Verständnis von Quantum Computing, denn wenn Sie Quantum-Zustände ingünstig Klonen könnten, erhalten Sie eine nahezu magische Möglichkeit, von Quantum-Zuständen zu lernen.
Tatsächlich könnten Sie das Prinzip der geunten Unsicherheit von Heisenberg verletzen.
Alternativ können Sie einen optimalen Cloner verwenden, um ein einzelnes Beispiel aus einer komplexen Quantum-Distribution zu erstellen und alles zu erlernen, was Sie möglicherweise über die Verteilung von nur einem Beispiel erfahren.
Dies wäre so, als würden Sie eine Münze kippen und Köpfe beobachten und dann einen Freund über das Ergebnis informieren, dass Sie Antworten müssen. "ah die Verteilung der Münze muss Bernoulli mit $p = 0.512643 \ ldots $ !" lauten.  Eine solche Anweisung wäre nicht unsinnig, weil ein Teil der Informationen (das Heads-Ergebnis) einfach nicht die vielen Informationen bereitstellen kann, die erforderlich sind, um die Verteilung ohne wesentliche vorherige Informationen zu codieren.
Ebenso wie ohne vorherige Informationen können wir einen quantumstatus nicht ganz genau so Klonen, wie wir ein Ensemble dieser Münzen nicht vorbereiten können, ohne $p zu kennen $ .

Informationen sind in Quantum Computing nicht kostenlos.
Jedes gemessene Qubit liefert ein einzelnes Bit an Informationen, und das No-Klon-Theorem zeigt, dass es keine Hintertür gibt, die ausgenutzt werden kann, um den grundlegenden Kompromiss zwischen den Informationen, die über das System gewonnen wurden, und der auf ihm aufgerufenen Störung zu umgehen.
