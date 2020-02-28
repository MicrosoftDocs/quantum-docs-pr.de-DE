---
title: Mehrere Qubits
description: Erfahren Sie, wie Sie Vorgänge für zwei oder mehr Qubits ausführen.
author: QuantumWriter
uid: microsoft.quantum.concepts.multiple-qubits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 2fa227c823cd87df9c799c043c699e4ce818b8e3
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907544"
---
# <a name="multiple-qubits"></a>Mehrere Qubits

Single-Qubit-Gates haben einige kontraintuitive Features, wie z. b. die Möglichkeit, zu einem bestimmten Zeitpunkt in mehreren Zuständen zu sein, wenn wir auf einem Quantum-Computer nur ein einzelnes Qubit haben, hätten wir ein Gerät mit Rechenleistung, das durch selbst bei einem Rechner können Sie einen klassischen Supercomputer verwenden.
Die wahre Leistungsfähigkeit von Quantum Computing wird nur offensichtlich, wenn wir die Anzahl der Qubits erhöhen.
Dies liegt teilweise daran, dass die Dimension des Vektor Raums von Quantum State Vektoren exponentiell mit der Anzahl von Qubits wächst.
Dies bedeutet, dass ein einzelnes Qubit trivial modelliert werden kann. das Simulieren einer 50-Qubit-Quantum-Berechnung würde jedoch die Grenzen vorhandener Supercomputer überschreiten.
Das Erhöhen der Größe der Berechnung durch nur ein zusätzliches Qubit *verdoppelt* den Arbeitsspeicher, der zum Speichern des Zustands erforderlich ist, und *verdoppelt* die Rechenzeit ungefähr.
Diese schnelle Verdoppelung der computeleistung liegt darin begründet, dass ein Quantum-Computer mit einer relativ kleinen Anzahl von Qubits die leistungsstärksten superpcs von heute, Morgen und mehr für einige Rechenaufgaben überschreiten kann.

Warum haben wir exponentielles Wachstum für Quantum State Vectors?  Unser Ziel in diesem Abschnitt besteht darin, die Regeln zu überprüfen, die zum Erstellen von Multi-Qubit-Zuständen aus den Single-Qubit-Zuständen verwendet werden, und die Gate-Vorgänge zu erörtern, die wir in unserem Gate festlegen müssen, um einen Universal many-Qubit-Quantum-Computer zu bilden.
Diese Tools sind absolut notwendig, um die Gate-Sätze zu verstehen, die häufig in Q #-Code verwendet werden, und um sich darüber zu informieren, warum Quantum-Effekte wie jede Verflechtungen oder Störungen das Quantum-Computing leistungsfähiger als klassisches Computing darstellen.

## <a name="representing-two-qubits"></a>Darstellen von zwei Qubits
Der Hauptunterschied zwischen einem-und zwei-Qubit-Zuständen besteht darin, dass zwei-Qubit-Zustände vierdimensional und nicht zweidimensional sind.
Dies liegt daran, dass die Berechnungsbasis für zwei-Qubit-Zustände durch die tensorflow-Produkte von einem-Qubit-Status gebildet wird.  Beispiel: \begin{align} 00 \equiv \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix}1 \\\\ 0 \ End{bmatrix} & = \begin{bmatrix}1 \\\\ 0\\\\ 0\\\\ 0 \ End{bmatrix}, \qquad 01 \equiv \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix}0 \\\\ 1 \ End{bmatrix} = \begin{bmatrix}0 \\\\ 1\\\\ 0\\\\ 0 \end{bmatrix},\\\\ 10 \equiv \begin{bmatrix}0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix}1 \\\\ 0 \ End{bmatrix} & = \begin{bmatrix}0 \\\\ 0\\\\ 1\\\\ 0 \end{bmatrix}, \qquad 11 \equiv \begin{bmatrix}0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix}0 \\\\ 1 \end{bmatrix} = \begin{bmatrix}0 \\\\ 0\\\\ 0 @no__ t_40_ \\ 1 \end{bmatrix}.\\
\end{align}

Es ist leicht zu erkennen, dass der Quantum-Status $n $ Qubits in der Regel durch einen Einheits Vektor der Dimension "$ 2 ^ n $" dargestellt wird, der diese Konstruktion verwendet.  Der Vektor

$ $ \begin{bmatrix} \ alpha_{00} \\\\ \ alpha_{01} \\\\ \ alpha_{10} \\\\ \ alpha_{11} \end{bmatrix} $ $

stellt einen Quantum-Zustand auf zwei Qubits dar, wenn $ | \ alpha_{00}| ^ 2 + | \ alpha_{01}| ^ 2 + | \ alpha_{10}| ^ 2 + | \ alpha_{11}| ^ 2 = 1 $. Ebenso wie bei einzelnen Qubits enthält der Quantum-Status Vektor mehrerer Qubits alle Informationen, die zum Beschreiben des Systemverhaltens erforderlich sind.

Wenn wir zwei separate Qubits erhalten, eine im Zustand $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ und ein zweites Qubit im Zustand $ \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} $, ist der entsprechende zwei-Qubit-Zustand.

$ $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} \otimes \begin{bmatrix} \gamma \\\\ \delta \ End{bmatrix} = \begin{bmatrix} \alpha \begin{bmatrix} \gamma \\\\ \delta \end{bmatrix} \\\\ \beta \begin{bmatrix}\gamma \\\\ \delta \end{bmatrix} \end{bmatrix} = \begin{bmatrix} \alpha\gamma \\\\ \alpha\delta \\\\ \beta\gamma \\\\ \beta\delta \end{bmatrix} , $$

Dabei wird der Vorgang $ \otimes $ als tensorflow Product (oder Kronecker Product) von Vektoren bezeichnet. Beachten Sie, dass zwar immer das tensorflow-Produkt zweier Single-Qubit-Zustände erstellt werden kann, um einen zwei-Qubit-Status zu bilden, aber nicht alle zwei-Qubit-quantumzustände können als tensorflow-Produkt von zwei Single-Qubit-Zuständen geschrieben werden.
Beispielsweise gibt es keine Zustände $ \psi = \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ und $ \phi = \begin{bmatrix} \gamma \\\\ \delta \ End{bmatrix} $, sodass Ihr tensorflow-Produkt den Status aufweist. 

$ $ \psi\otimes \phi = \begin{bmatrix} 1/\ sqrt{2} \\\\ 0 \\\\ 0 \\\\ 1/\ sqrt{2} \end{bmatrix}. $ $ 

Ein solch ein zwei-Qubit-Zustand, der nicht als tensorflow-Produkt von Single-Qubit-Zuständen geschrieben werden kann, wird als "entwinkelter Zustand" bezeichnet. die beiden Qubits werden als [*entkoppelt*](https://en.wikipedia.org/wiki/Quantum_entanglement)bezeichnet.  Da der Quantum-Zustand nicht als tensorflow-Produkt eines einzelnen Qubit-Zustands angesehen werden kann, werden die Informationen, die der Zustand enthält, nicht einzeln auf eine der Qubits beschränkt.  Stattdessen werden die Informationen nicht lokal in den Korrelationen zwischen den beiden Zuständen gespeichert.  Diese nicht Lokalität von Informationen ist eines der wichtigsten Merkmale von Quantum Computing gegenüber klassischem Computing und ist für eine Reihe von Quantum-Protokollen, einschließlich [Quantum-Teleportation](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/teleportation) und [Quantum-Fehlerkorrektur](xref:microsoft.quantum.libraries.error-correction), von entscheidender Bedeutung.

## <a name="measuring-two-qubit-states"></a>Messen von zwei-Qubit-Zuständen ##
Das Messen von zwei-Qubit-Zuständen ähnelt den einzelnen Qubit-Messungen. Messen des Zustands

$ $ \begin{bmatrix} \ alpha_{00} \\\\ \ alpha_{01} \\\\ \ alpha_{10} \\\\ \ alpha_{11} \end{bmatrix} $ $

ergibt $0 $ mit der Wahrscheinlichkeit $ | \ alpha_{00}| ^ $2, $1 $ mit der Wahrscheinlichkeit $ | \ alpha_{01}| ^ $2, $10 $ mit der Wahrscheinlichkeit $ | \ alpha_{10}| ^ $2 und $11 $ mit der Wahrscheinlichkeit $ | \ alpha_{11}| ^ $2. Die Variablen $ \ alpha_{00}, \ alpha_{01}, \ alpha_{10}, $ und $ \ alpha_{11}$ wurden absichtlich benannt, um die Verbindung zu löschen. Wenn das Ergebnis nach der Messung $0 $ ist, wurde der Quantum-Status des Two-Qubit-Systems reduziert und ist jetzt

$ $0 \equiv \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix}.
$$

Es ist auch möglich, nur ein Qubit mit einem zwei-Qubit-Quantum-Zustand zu messen. In Fällen, in denen nur eine der Qubits gemessen wird, unterscheiden sich die Auswirkungen der Messung ganz leicht, da der gesamte Zustand nicht in den Status "Compute-Basis" reduziert wird, sondern nur auf ein unter System reduziert wird.  Anders ausgedrückt: in solchen Fällen, in denen nur ein Qubit gemessen wird, reduziert nur eines der Subsysteme, aber nicht alle.  

Um dies zu sehen, sollten Sie das erste Qubit des folgenden Zustands Messen, das durch Anwenden der Hadamard-Transformation $H $ auf zwei Qubits gebildet wird, die anfänglich auf den Status "0" festgelegt sind: $ $ H ^ {\otimes 2} \left (\begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix}1 \\\\ 0 \end{bmatrix} \right) = \frac{1}{2}\begin{bmatrix}1 & 1 & 1 & 1 \\\\ 1 &-1 & 1 &-1 \\\\ & 1 & 1 &-1 \\-1 \\ & 1- 1 &-1 & 1 \end{bmatrix}\begin{bmatrix}1\\\\ 0\\\\ 0\\\\ 0 \ Ende {bmatrix} = \frac{1}{2}\begin{bmatrix}1\\\\ 1\\\\ 1\\\\ 1 \ Ende {bmatrix} \mapsto \begin{Cases}\text{Outcome} = 0 & \frac{1}{\sqrt{2}} \begin{bmatrix}1\\\\ 1\\\\ 0\\\\ 0 \end{bmatrix}\\\\ \text{Ergebnis} = 1 & \frac{1}{\sqrt{2}} \begin{bmatrix}0\\\\ 0\\\\ 1\\\\ 1 \ End{bmatrix}\\\\ \end{Cases}.
Beide Ergebnisse haben eine Wahrscheinlichkeit von 50%.  Das Ergebnis, das 50% Wahrscheinlichkeit für beides ergibt, kann aus der Tatsache intuitiv werden, dass der anfängliche Quantum-Status Vektor beim Austauschen von $0 $ mit $1 $ auf dem ersten Qubit invariante ist.

Die mathematische Regel zum Messen des ersten oder zweiten Qubits ist einfach.  Wenn wir $e _K $ der $k ^ {\rM Th} $ computevektor und $S $ der Satz aller $e _K $ sein, damit das betreffende Qubit den Wert $1 $ für diesen Wert von $k $ übernimmt.  Wenn z. b. das erste Qubit gemessen werden soll, besteht $S $ aus $e _2 \ equiv $10 und $e _3 \ equiv $11.  Wenn wir am zweiten Qubit interessiert sind, $S $ aus $e _1 \ equiv $1 und $e _3 \equiv $11.  Anschließend ist die Wahrscheinlichkeit, dass das ausgewählte Qubit als $1 $ gemessen wird, für den Status Vektor $ \psi $ festgelegt.

$ $ P (\text{Outcome} = 1) = \ sum_ {e_k \text{in der Gruppe} S} \psi ^ \dagger e_k e_k ^ \dagger \psi.
$$

Da jede Qubit-Messung nur $0 $ oder $1 $ ergeben kann, ist die Wahrscheinlichkeit für das Messen von $0 $ einfach $1-P (\text{Outcome} = 1) $.  Aus diesem Grund wird nur explizit eine Formel für die Wahrscheinlichkeit der Messung von $1 $ zugewiesen.

Die Aktion, die für den Zustand einer solchen Messung ausgeführt wird, kann mathematisch ausgedrückt werden.

$ $ \psi \mapsto \bruchteil {\ sum_ {e_k \text{in der Gruppe} S} e_k e_k ^ \dagger \psi}{\sqrt{P (\text{Outcome} = 1)}}.
$$

Der vorsichtige Reader kann sich Gedanken darüber machen, was passiert, wenn die Wahrscheinlichkeit der Messung 0 (null) ist.  Obwohl der resultierende Zustand in diesem Fall technisch nicht definiert ist, müssen wir uns nicht um solche Eventualitäten kümmern, da die Wahrscheinlichkeit NULL ist.


Wenn wir $ \psi $ als den oben genannten Uniform State Vector verwenden und an der Messung des ersten Qubit interessiert sind, 

$ $ P (\text{Messung des ersten Qubit} = 1) = (\psi ^ \dagger e_2) (e_2 ^ \dagger \psi) + (\psi ^ \dagger e_3) (e_3 ^ \dagger \psi) = | e_2 ^ \dagger \psi | ^ 2 + | e_3 ^ \dagger \psi | ^ 2.
$$

Beachten Sie, dass dies nur die Summe der beiden Wahrscheinlichkeiten ist, die für das Messen der Ergebnisse erwartet werden, $10 $ und $11 $ wären alle zu messenden Qubits.
In unserem Beispiel ergibt dies

$ $ \frac{1}{4}\left | \begin{bmatrix}0 & 0 & 1 & 0 \ Ende {bmatrix} \ BEGIN {bmatrix} 1\\\\ 1\\\\ 1\\\\ 1 \ End {bmatrix} \right | ^ 2 + \frac{1}{4}\left | \begin{bmatrix}0 & 0 & 0 & 1 \ Ende {bmatrix} \ BEGIN {bmatrix} 1\\\\ 1\\\\ 1\\\\ 1 \ End {bmatrix} \right | ^ 2 = \frac{1}{2}.
$$

was mit unserer Intuition übereinstimmt, gibt Aufschluss über die Wahrscheinlichkeit.  Ebenso kann der Zustand geschrieben werden:

$ $ \bruchteil {\bruch{e_2}{2}+ \bruchteil {e_3}{2}} {\sqrt{\frac{1}{2}}} = \frac{1}{\sqrt{2}} \begin{bmatrix} 0\\\\ 0\\\\ 1\\\\ 1 \ Ende {bmatrix} $ $

auch in Übereinstimmung mit unserer Intuition.

## <a name="two-qubit-operations"></a>Zwei-Qubit-Vorgänge
Wie bei einem Single-Qubit-Fall ist jede einheitliche Transformation ein gültiger Vorgang für Qubits. Im Allgemeinen ist eine einheitliche Transformation auf $n $ Qubits eine Matrix $U $ der Größe $2 ^ n \times 2 ^ n $ (sodass Sie auf Vektoren der Größe von $2 ^ n $ basiert), sodass $U ^{-1} = U ^ \dagger $ vorliegt. Beispielsweise ist das CNOT-Gate (kontrollierter not) ein häufig verwendetes zwei-Qubit-Gate und wird durch die folgende einheitliche Matrix dargestellt:

$ $ \operatschmue{CNOT} = \begin{bmatrix} 1 \ 0 \ 0 \ 0 \\\\ 0 \ 1 \ 0 \ 0 \\\\ 0 \ 0 \ 0 \ 1 \\\\ 0 \ 0 \ 1 \ 0 \end{bmatrix} $ $

Wir können auch zwei Qubit-Gates durch Anwenden von Single-Qubit Gates auf beide Qubits bilden. Wenn wir z. b. die Gates anwenden 

$ $ \begin{bmatrix} a \ b\\\\ c \ d \end{bmatrix} $ $

and

$ $ \begin{bmatrix} e \ f\\\\ g \ h \end{bmatrix} $ $

zum ersten bzw. zweiten Qubits entspricht dies dem Anwenden der zwei-Qubit-einheitlich, die durch ihr tensorflow-Produkt angegeben wird: $ $ \begin{bmatrix} a \ b\\\\ c \ d \end{bmatrix} \otimes \begin{bmatrix} e \ f\\\\ g \ h \end{bmatrix} = \begin{bmatrix} AE \ AF \ be \ BF \\\\ AG \ AH \ BG \ BH \\\\ CE \ CF \ de \ DF \\\\ CG \ ch \ DG \ dh \end{bmatrix}. $ $, damit wir zwei-Qubit-Gates erstellen können, indem wir das tensorflow-Produkt von einigen bekannten Single-Qubit-Gates nehmen. Einige Beispiele für zwei-Qubit-Gates sind $H \otimes H $, $X \otimes \boldone $ und $X \otimes Z $.

Beachten Sie, dass zwei Single-Qubit-Gates ein zwei-Qubit-Gate durch Übernahme Ihres tensorflow-Produkts definieren. der umgekehrte Wert ist nicht "true". Nicht alle zwei-Qubit-Gates können als tensorflow-Produkt von Single-Qubit Gates geschrieben werden.  Ein solches Gate wird als *Entangling* -Gate bezeichnet. Ein Beispiel für ein Entangling-Gate ist das CNOT-Gate.

Die Intuition hinter einem kontrollierten-not-Gate kann zu beliebigen Gates generalisiert werden.  Ein kontrolliertes Gate im Allgemeinen ist ein Gate, das als Identität agiert (d. h. es hat keine Aktion), es sei denn, ein bestimmtes Qubit ist $1 $.  Wir bezeichnen ein kontrolliertes einheitliches, das in diesem Fall auf dem Qubit mit der Bezeichnung "$x $" mit "$ \lambda\_x (U) $" gesteuert wird.  Beispiel: $ \ Lambda_0 (U) e\_{1}\otimes {\psi} = e\_{1}\otimes U {\psi} $ und $ \lambda\_0 (u) e\_{0}\otimes {\psi} = e\_{0}\otimes{\psi} $, dabei sind $e\_$0 und $e\_$1 Die Berechnungsbasis Vektoren für ein einzelnes Qubit, das den Werten $0 $ und $1 $ entspricht.  Sehen Sie sich beispielsweise die folgenden kontrollierten $Z $ Gate an, und dies kann als $ $ \lambda\_0 (Z) = \begin{bmatrix}1 & 0 & 0 & 0\\\\0 & 1 & 0 & 0\\\\0 & 0 & 1 ausgedrückt werden. & 0\\\\0 & 0 & 0 &-1 \end{bmatrix} = (\boldone\otimes h) \operatschmue{CNOT} (\boldone\otimes h).
$$

Die effiziente durch Bildung von kontrollierten Uni-Trägern ist eine große Herausforderung.  Die einfachste Möglichkeit, dies zu implementieren, erfordert, eine Datenbank mit kontrollierten Versionen von grundlegenden Gates zu bilden und jedes grundlegende Gate im ursprünglichen einheitlichen Vorgang durch sein kontrolliertes Pendant zu ersetzen.  Dies ist oft ziemlich verschwenderisch, und ein intelligenter Einblick kann häufig verwendet werden, um nur einige Gates durch kontrollierte Versionen zu ersetzen, um die gleichen Auswirkungen zu erzielen.  Aus diesem Grund wird in unserem Framework die Möglichkeit zur Verfügung gestellt, die naive Methode zu steuern oder zuzulassen, dass der Benutzer eine kontrollierte Version der einheitlich definiert, wenn eine optimierte, Hand abgestimmte Version bekannt ist.

Gates können auch mit klassischen Informationen gesteuert werden.  Ein klassisch kontrolliertes not-Gate ist z. b. nur ein normales, nicht-Gate, aber es wird nur angewendet, wenn ein klassisches Bit $1 $ und nicht ein Quantum-Bit ist.  In diesem Sinne kann ein klassisch kontrolliertes Gate als if-Anweisung im Quantum-Code betrachtet werden, wobei das Gate nur in einer Verzweigung des Codes angewendet wird.


Wie bei einem Single-Qubit-Fall ist ein zwei-Qubit-Gate auf Universal festgelegt, wenn eine $4 \ Times $4-einheitliche Matrix durch ein Produkt von Gates von diesem Satz auf willkürliche Genauigkeit angeglichen werden kann.
Ein Beispiel für einen universellen Gate-Satz sind das Hadamard-Gate, das T-Gate und das CNOT-Gate. Durch die Übernahme von Produkten dieser Gates können wir jede einheitliche Matrix auf zwei Qubits angleichen.

## <a name="many-qubit-systems"></a>Viele-Qubit-Systeme
Wir befolgen genau dieselben Muster, die im zwei-Qubit-Fall untersucht werden, um viele-Qubit-Quantenzustände aus kleineren Systemen zu erstellen.  Solche Zustände werden erstellt, indem tensorflow-Produkte mit kleineren Zuständen gebildet werden.  Beispielsweise können Sie die Bitzeichenfolge $1011001 $ in einem Quantum-Computer codieren.  Diese Codierung kann als

$ $1011001 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}.
$$

Quantum-Gates funktionieren auf genau dieselbe Weise.  Wenn Sie z. b. die $X $ Gate auf das erste Qubit anwenden und dann ein CNOT zwischen dem zweiten und dritten Qubits ausführen möchten, können wir diese Transformation als

\begin{align} & (X \otimes \operatorname{CNOT}_{12}\otimes \boldone\otimes \boldone \otimes \boldone \otimes \boldone) \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \ End{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}\otimes \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}\\\\ & \qquad\qquad\equiv 0011001.
\end{align}

In vielen Qubit-Systemen ist es häufig erforderlich, Qubits zuzuordnen und aufzuheben, die als temporärer Arbeitsspeicher für den Quantum-Computer fungieren.  Solch ein Qubit wird als "Ancilla" bezeichnet.  Standardmäßig wird davon ausgegangen, dass der Qubit-Zustand mit $e _0 $ bei der Zuordnung initialisiert wird.  Wir gehen davon aus, dass es wieder $e _0 $ zurückgegeben wird, bevor die Zuordnung aufgehoben wird.  Diese Annahme ist wichtig, denn wenn ein Ancilla-Qubit mit einem anderen Qubit-Register entkoppelt wird, wenn die Zuordnung aufgehoben wird, wird die "Ancilla" durch den Prozess der Aufhebung der Zuordnung beschädigt.  Aus diesem Grund wird immer angenommen, dass solche Qubits in ihren ursprünglichen Zustand zurückversetzt werden, bevor Sie veröffentlicht werden.

Und schließlich müssen der Gate-Satz neue Gates hinzugefügt werden, um Universal Quantum Computing für zwei Qubit-Quantum-Computer zu erreichen. im Fall von Multi-Qubit müssen keine neuen Gates eingeführt werden.  Die Gates $H $, $T $ und CNOT bilden ein universelles Gate, das auf viele Qubits festgelegt ist, da jede allgemeine einheitliche Transformation in eine Reihe von zwei Qubit-Drehungen aufgeteilt werden kann.  Wir können dann die für den zwei-Qubit-Fall entwickelte Theorie nutzen und Sie hier wieder verwenden, wenn viele Qubits vorhanden sind.

Obwohl die bisher verwendete lineare algebraische Notation sicherlich zum Beschreiben von Multi-Qubit-Zuständen verwendet werden kann, wird Sie immer schwieriger, da wir die Größe der Zustände erhöhen.  Der resultierende Spalten Vektor für eine Zeichenfolge mit einer Länge von 7 Zeichen ist beispielsweise $128 $ dimensional, wodurch das Ausdrücken mit der zuvor beschriebenen Notation sehr umständlich wird.  Aus diesem Grund präsentieren wir als nächstes eine gängige Notation in Quantum Computing, mit der wir diese hochdimensionalen Vektoren kurz beschreiben können.
