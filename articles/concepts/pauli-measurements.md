---
title: Pauli-Messungen | Microsoft-Dokumentation
description: Pauli-Messungen
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 7bea821be7e26e72f2860278486d35be676ca63d
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183708"
---
# <a name="pauli-measurements"></a>Pauli-Messungen

In den vorherigen Diskussionen haben wir uns auf Berechnungsbasis Messungen konzentriert.  Tatsächlich gibt es andere gängige Messungen in der Quantum-Berechnung, die aus Sicht der Sicht bequem in Bezug auf Berechnungsbasis Messungen ausgedrückt werden können.  Die gängigsten Sätze dieser Messungen sind *Pauli-Messungen*.  In solchen Fällen wird das Messen eines Pauli-Operators häufig erläutert, im Allgemeinen ein Operator wie z. b. $X, Y, Z $ oder $Z \otimes Z, x\otimes X, x\otimes Y $ usw.  Die Erörterung von Messungen in Form von Pauli-Operatoren ist vor allem im Unterfeld der Quantum-Fehlerkorrektur üblich. In f # wird eine ähnliche Konvention befolgt. Wir erläutern nun diese Alternative Ansicht von Messungen.

Bevor wir uns mit den Details der Bedeutung einer Pauli-Messung beschäftigen, ist es sinnvoll, sich Gedanken darüber zu machen, was ein einzelnes Qubit innerhalb eines Quantum-Computers in den Quantum-Zustand versetzt.  Stellen Sie sich vor, dass ein $n $-Qubit-Quantum-Status vorhanden ist. Wenn dann ein Qubit sofort gemessen wird, werden die Hälfte der $2 ^ n $-Möglichkeiten, in denen sich der Zustand befinden könnte, sofort ausgeschlossen.  Mit anderen Worten: die Messung projiziert den Quantum-Zustand auf einen von zwei halben Leerzeichen.  Wir können die Art und Weise verallgemeinern, in der wir die Messung berücksichtigen.

Um diese Teilbereiche zu beschreiben, benötigen wir eine Sprache für die Beschreibung.  Eine Möglichkeit besteht darin, die beiden Teilbereiche zu beschreiben, indem Sie Sie über eine Matrix angeben, die nur zwei eindeutige Eigenwerte aufweist, die von der Konvention auf $ \pm $1 übernommen werden.  Das einfachste Beispiel hierfür ist:

$ $ Z = \begin{bmatrix} 1 & 0 \\\\ 0 &-1 \end{bmatrix}.
$$

Die "Pauli-$Z $"-Matrix weist eindeutig zwei Eigenvektoren $ \ket{0}$ und $ \ket{1}$ mit den eigen Werten $ \pm $1 auf.  Wenn wir also das Qubit Messen und $ \ket{0}$ abrufen, befinden wir uns im $ + $1-eigen Raum (der Satz aller Vektoren, die aus Summen von Eigenvektoren mit nur positiven oder nur negativen eigen Werten bestehen) des Operators, und wenn wir $ \ket{1}$ im $-$1 Ei-Format messen. genspace von $Z $.  Dieser Prozess wird in der Sprache von Pauli-Messungen als "Messen von Pauli $Z $" bezeichnet und ist vollständig mit der Durchführung einer Berechnungsbasis Messung identisch.

Natürlich erfüllt eine beliebige $2 \ mal $2-Matrix, die eine einheitliche Transformation von $Z $ ist, auch diese Kriterien.  Dies heißt, dass wir auch Matrix $A = U ^ \dagger Z U $ für jede einheitliche Matrix $U $ berücksichtigen könnten, um eine Matrix zu erhalten, die die beiden Ergebnisse einer Messung in den $ \pm $1-Eigenvektoren definiert.  Die Notation von Pauli-Messungen verweist darauf, indem $X-, Y-, Z $-Messungen als gleichwertige Messungen identifiziert werden, die zur Gewinnung von Informationen aus einem Qubit führen können.  Diese Messungen werden zur einfacheren Verwendung unten angegeben.

$ $ \begin{Array}{| c | c |} \text{Pauli Messung} & U\\\\ Z & \boldone\\\\ X & H\\\\ Y & HS ^ \dagger\\\\ \end{Array} $ $

Das heißt, dass bei Verwendung dieser Sprache "Measure $Y $" dem Anwenden von $HS ^ \dagger $ entspricht und dann auf Berechnungsbasis gemessen wird, wobei $S $ das so genannte Phasen Gate ist, das von angegeben wird.

$ $ \begin{bmatrix}1 & 0\\\\ 0 & i\end {bmatrix}.
$$

Dies entspricht auch dem Anwenden von $HS ^ \dagger $ auf den Quantum State Vector und der anschließenden Messung $Z $.  Der richtige Zustand wird dann durch umwandeln auf die Berechnungsbasis gefunden, was das Anwenden von $SH $ auf den Quantum-Status Vektor bedeutet.

## <a name="q-outcome-classical-information-obtained-from-quantum-state"></a>Informationen zum klassischen Q #-Ergebnis aus dem Quantum-Status
In f # sagen wir, dass das Ergebnis, d. h. die klassischen Informationen, die aus der Interaktion mit dem Zustand extrahiert wurden, $j $ ist, die sich im Satz $\{0, 1\}$ befindet, wenn sich das Ergebnis im $ (-1) ^ j $ eigen Raum des Pauli-Operators befindet.

Die Messungen von multiqubit-Pauli-Operatoren sind ähnlich definiert, wie in:

$ $ Z\otimes Z = \begin{bmatrix}1 & 0 & 0 & 0\\\\ 0 &-1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 & 1 \ Ende {bmatrix}.
$$

Folglich bilden die tensorflow-Produkte von zwei "Pauli-$Z $"-Operatoren eine Matrix aus zwei Leerzeichen, die aus "$ + $1" und "$-$1 Eigenwerte" bestehen  Wie bei einem Single-Qubit-Fall bilden beide einen halben Raum, was bedeutet, dass die Hälfte des zugänglichen Vektor Raums zum $ + $1-eigen Raum und die verbleibende Hälfte bis zum $-$1-eigen Raum gehört.  Im Allgemeinen ist es einfach, von der Definition des tensorflow-Produkts aus zu sehen, dass ein beliebiges tensorflow-Produkt von Pauli-$Z $-Operatoren und die Identität auch diesem entspricht.  Beispiel:

$ $ Z\otimes\boldone = \begin{bmatrix} 1 & 0 & 0 & 0\\\\ 0 & 1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 &-1 \ Ende {bmatrix}.
$$

Wie zuvor beschreibt jede einheitliche Transformation dieser Matrizen auch zwei halb Bereiche mit der Bezeichnung "$ \pm $1 Eigenwerte".  Beispielsweise $X \otimes X = h\otimes h (z\otimes Z) h\otimes h $ aus der Identität, die $Z = HXH $.  Ähnlich wie der One-Qubit-Fall können alle zwei-Qubit-Pauli-Messungen als $U ^ \dagger (z\otimes \id) U $ für $4 \ mal $4 einheitliche Matrizen $U $ geschrieben werden.  Wir zählen die Transformationen in der folgenden Tabelle auf, in der wir das Swap-Gate, das Qubits $0 $ und $1 $: $ \operatorname{Swap} = \operatorname{CNOT}\_{01}\operatschmue{CNOT}\_{10}\operatornamental e{ CNOT}\_{01}$:

$ $ \begin{Array}{| c | c |} \text{Pauli Messung} & U\\\\ \hline z\otimes \boldone & \boldone\otimes \boldone\\\\ x\otimes \boldone & h\otimes \boldone\\\\ y\otimes \boldone & HS ^ \dagger\ otimes \boldone\\\\ \boldone \otimes Z & \operatschmue{tauap}\\\\ \boldone \otimes X & (h\otimes \boldone) \operatschmue{tauap}\\\\ \boldone \otimes Y & (HS ^ \dagger\otimes \boldone) \ Operatorname {Swap}\\\\ z\otimes Z & \operatschmue{CNOT}\_{10}\\\\ x\otimes Z & \operatschmue{CNOT}\_{10}(h\otimes \boldone)\\\\ y\otimes Z & \ Operatorname {CNOT}\_{10}(HS ^ \dagger\otimes \boldone)\\\\ z\otimes x & \operatschmue{CNOT}\_{10}(\boldone\otimes H)\\\\ x\otimes x & \operatschmue{CNOT}\_@no__t _31_ (h\otimes h)\\\\ y\otimes X & \operatschmue{CNOT}\_{10}(HS ^ \dagger\otimes h)\\\\ z\otimes Y & \operatschmue{CNOT}\_{10}(\boldone \otimes HS ^ \dagger)\\\\ x\otimes y & \operatschmue{CNOT}\_{10}(h\otimes HS ^ \dagger)\\\\ y\otimes y & \operatschmue{CNOT}\_{10}(HS ^ \dagger\otimes HS ^ \dagger)\\\\ \end{Array} $ $

Hier wird das Gate $ \operatorname{CNOT}\_{10}$ aus folgendem Grund angezeigt.  Jedes Pauli-Maß, das "$ \boldone $ Matrix" nicht enthält, entspricht einem einheitlichen $Z \otimes Z $ durch die oben genannte Argumentation.  Die Eigenwerte $Z \otimes Z $ hängen nur von der Parität der Qubits ab, aus denen die einzelnen Berechnungsbasis Vektor bestehen, und die in dieser Liste angezeigten kontrollierten Vorgänge dienen dazu, diese Parität zu berechnen und im ersten Bit zu speichern.  Nachdem das erste Bit gemessen wurde, können wir die Identität des resultierenden halb Raums wiederherstellen, der der Messung des Pauli-Operators entspricht.

Ein weiterer Hinweis ist, dass es möglicherweise verlockend ist, dass die Messung $Z \otimes Z $ mit der Messung $Z \otimes \id $ und dann mit $ \id \otimes z $ übereinstimmt. diese Annahme wäre false.  Der Grund hierfür ist, dass die Messung $Z \otimes Z $ den Quantum-Zustand entweder in den "$ + $1"-oder "$-$1"-Zustand dieser Operatoren projiziert.  Durch Messen von $Z \otimes \id $ und dann $ \id \otimes z $ wird der Quantum-Status Vektor zuerst auf einen halben Bereich von $Z \otimes \id $ und dann auf einen halben Bereich von $ \id \otimes z $ projiziert.  Da es vier Berechnungsbasis Vektoren gibt, verringert die Durchführung beider Messungen den Zustand auf einen Viertel Raum und reduziert ihn somit auf einen einzelnen Berechnungsbasis Vektor.


## <a name="correlations-between-qubits"></a>Korrelationen zwischen Qubits
Eine weitere Möglichkeit zum Messen von tensorflow-Produkten von Paulis wie $X \otimes X $ oder $Z \otimes Z $ besteht darin, dass mit diesen Messungen Informationen angezeigt werden können, die in den Korrelationen zwischen den beiden Qubits gespeichert sind.  Durch Messen $X \otimes \id $ können Sie Informationen untersuchen, die lokal im ersten Qubit gespeichert sind.  Obwohl beide Arten von Messungen in Quantum Computing gleichermaßen wertvoll sind, beleuchtet das erste die Leistungsfähigkeit von Quantum Computing. Es wird deutlich, dass bei der Verwendung von Quantum Computing häufig die Informationen, die Sie erlernen möchten, nicht in einem einzigen Qubit gespeichert, sondern nicht lokal in allen Qubits gespeichert werden, sondern nur durch eine gemeinsame Messung mit $Z \otimes Z $ werden diese Informationen kundiger.

Beliebige Pauli-Operatoren, z. b. $X \otimes Y \otimes Z \otimes \boldone $, können ebenfalls gemessen werden.  Alle derartigen tensorflow-Produkte von Pauli-Operatoren verfügen nur über zwei Eigenwerte $ \pm $1, und beide eigen Räume bilden halbräume des gesamten Vektor Bereichs.  Daher stimmen Sie mit den oben genannten Anforderungen überein.

In Q # geben solche Messungen $j $ zurück, wenn die Messung ein Ergebnis im Eigen Bereich von Sign $ (-1) ^ j $ ergibt.  Diese Funktion als integrierte Funktion in Q # ist hilfreich, da die Messung solcher Operatoren lange Ketten von kontrollierten, nicht Gates und Basis Transformationen erfordert, um die Diagonalisierung $U $ Gate zu beschreiben, die erforderlich ist, um den Vorgang als tensorflow-Produkt $Z $ und $ \id $ auszudrücken.  Wenn Sie einfach festlegen können, dass Sie eine dieser vordefinierten Messungen durchführen möchten, müssen Sie sich keine Gedanken darüber machen, wie Sie Ihre Basis so transformieren, dass eine Berechnungsbasis Messung die erforderlichen Informationen bereitstellt.  Q # behandelt alle notwendigen Basis Transformationen automatisch. Weitere Informationen finden Sie unter [Q # Library Reference for Pauli Messungen](/qsharp/api/canon/microsoft.quantum.canon.measurepaulis)

## <a name="the-no-cloning-theorem"></a>Das No-Klon-Theorem
Quantum-Informationen sind leistungsstark.  Dadurch können wir beeindruckende Dinge, wie z. b. die Faktor Zahlen, exponentiell beschleunigen als die besten bekannten klassischen Algorithmen, oder korrelierte Elektronen Systeme effizient simulieren, die für eine genaue Simulation exponentialkosten benötigen.  Es gibt jedoch Einschränkungen hinsichtlich der Leistungsfähigkeit von Quantum Computing.  Eine solche Einschränkung wird durch das *No-Klon-Theorem*angegeben.

Das No-Klon-Theorem weist einen passenden Namen auf.
Sie lässt das Klonen generischer Quantenzustände durch einen Quantum-Computer nicht zu.
Der Beweis für das Theorem ist erstaunlich einfach.
Obwohl ein vollständiger Nachweis für das No-Klon-Theorem für unsere Erörterung etwas zu technisch ist, ist der Proof of the Theorem in dem Fall, in dem der betreffende Quantum-Computer keine weiteren "Ancilla Qubits" hat, innerhalb unseres Bereichs ("Ancilla Qubits" sind Qubits, die für Sie verwendet werden). Leerzeichen während einer Berechnung und können problemlos in Q # verwendet und verwaltet werden. Weitere Informationen finden Sie unter <xref:microsoft.quantum.techniques.qubits>).
Bei einem solchen Quantum-Computer muss der Klon Vorgang eine einheitliche Matrix sein. Die Messung wird nicht zugelassen, da der Quantum-Zustand beschädigt wird, den wir klonen wollen. Die einheitliche Matrix, die wir wünschen, muss über die Eigenschaft "$ $ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}", "$ $" für jeden Status "$ \ket{\psi} $" verfügen.
Die Linearität-Eigenschaft der Matrix Multiplikation impliziert dann, dass für jeden zweiten Quantum-Status $ \ket{\phi} $,

\begin{align} & u\left [\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right] \ket{0}= \frac{1}{\sqrt{2}} u\ket {\ Phi} \ Ket{0}+ \frac{1}{\sqrt{2}} u\ket {\ PSI} \ Ket{0}@no__ t_9_ \\ & \qquad\qquad = \frac{1}{\sqrt{2}} \left (\ket{\phi}\ket{\phi} + \ket{\psi}\ket{\psi}\right)\\\\ & \qquad\qquad\ne \left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \ Right) \right) \otimes\left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right).
\end{align}

Dies stellt die grundlegende Intuition hinter dem No-Klon-Theorem bereit: jedes Gerät, das einen unbekannten Quantum-Zustand kopiert, muss Fehler in mindestens einigen der von ihm kopierte Zustände auslösen.  Die Hauptannahme, dass der Cloner mit dem Eingabe Status linear agiert, kann durch das Hinzufügen von Ancilla und Messungen der Ancilla-Qubits verletzt werden. solche Interaktionen können außerdem Informationen über das System durch die maßstatistik und die Vermeidung von genaues Klonen in solchen Fällen ebenfalls.  Einen ausführlicheren Nachweis für das No-Klon-Theorem finden Sie unter, [um weitere Informationen](xref:microsoft.quantum.more-information)zu erhalten.

Das No-Clone-Theorem ist wichtig für ein qualitativ hochwertiges Verständnis von Quantum Computing, denn wenn Sie Quantum-Zustände ingünstig Klonen könnten, erhalten Sie eine nahezu magische Möglichkeit, von Quantum-Zuständen zu lernen.  Tatsächlich könnten Sie das Prinzip der geunten Unsicherheit von Heisenberg verletzen.  Alternativ können Sie einen optimalen Cloner verwenden, um ein einzelnes Beispiel aus einer komplexen Quantum-Distribution zu erstellen und alles zu erlernen, was Sie möglicherweise über die Verteilung von nur einem Beispiel erfahren.  Dies würden Sie tun, wenn Sie eine Münze kippen und Köpfen beobachten und dann einen Freund über das Ergebnis informieren, dass er antwortet, dass die Verteilung der Münze Bernoulli mit $p = 0.512643 \ ldots $! "lauten muss.  Eine solche Anweisung wäre nicht unsinnig, weil ein Teil der Informationen (das Heads-Ergebnis) einfach nicht die vielen Informationen bereitstellen kann, die erforderlich sind, um die Verteilung ohne wesentliche vorherige Informationen zu codieren.  Ebenso wie ohne vorherige Informationen können wir einen quantumstatus nicht ganz genau so Klonen, wie wir ein Ensemble dieser Münzen nicht vorbereiten können, ohne $p $ zu kennen.

Informationen sind in Quantum Computing nicht kostenlos.  Jedes gemessene Qubit liefert ein einzelnes Bit an Informationen, und das No-Klon-Theorem zeigt, dass es keine Hintertür gibt, die ausgenutzt werden kann, um den grundlegenden Kompromiss zwischen den Informationen, die über das System gewonnen wurden, und der auf ihm aufgerufenen Störung zu umgehen.

