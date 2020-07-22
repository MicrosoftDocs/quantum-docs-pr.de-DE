---
title: Quantum Machine Learning-Bibliothek
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 11/22/2019
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.intro
ms.openlocfilehash: 4a4ecbb85cc5bbfb1ccb1f111309578bcc5bce3d
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86872629"
---
# <a name="introduction-to-quantum-machine-learning"></a>Einführung in Quantum Machine Learning

## <a name="framework-and-goals"></a>Framework und Ziele

Die Quantum-Codierung und-Verarbeitung von Informationen ist eine leistungsfähige Alternative zu klassischen Machine Learning-Quantum-Klassifizierungen, insbesondere zum Codieren von Daten in quantatenregistern, die in Bezug auf die Anzahl der Features präzise sind.
Die Verbindungs zentrierte Quantum-Klassifizierung ist eine relativ einfache Quantum-Lösung, die die Daten Codierung mit einer schnellen Entangling/Disentangling-Quantum-Verbindung gefolgt von Messungen zum Ableiten von Klassen Bezeichnungen von Daten Beispielen kombiniert.
Das Ziel besteht darin, die klassische Charakterisierung und Speicherung von Themen Verbindungen zu gewährleisten sowie hybride Quantum/klassische Schulungen der Verbindungsparameter auch für extrem große Merkmals Räume zu gewährleisten.

## <a name="classifier-architecture"></a>Klassifizierungs Architektur

Bei der Klassifizierung handelt es sich um eine überwachte Machine Learning-Aufgabe, bei der das Ziel darin besteht, Klassen Bezeichnungen $ \{ Y_1, y_2, \ldots y_d \} $ bestimmter Daten Beispiele abzuleiten. Das Trainings Dataset ist eine Sammlung von Beispielen $ \mathcal{d} = \{ (x, y)} $ mit bekannten vorzugewiesenen Bezeichnungen. Hier $x $ ein Daten Sample, und $y $ ist die bekannte Bezeichnung "Trainings Bezeichnung".
Ähnlich wie herkömmliche Methoden besteht die Quantum-Klassifizierung aus drei Schritten:
- Daten Codierung
- Vorbereitung eines Klassifizierungs Zustands
- Messung aufgrund der Wahrscheinlichkeits Natur der Messung müssen diese drei Schritte mehrmals wiederholt werden. Die Messung kann als Quantum-Entsprechung der nichtlinearen Aktivierung angezeigt werden.
Sowohl die Codierung als auch das Berechnen des Klassifizierungs Zustands werden mithilfe von *Quantum*-Verbindungen durchgeführt. Während die Codierungs Verbindung in der Regel Daten gesteuert und Parameter frei ist, enthält die Klassifizierungs Leitung einen ausreichenden Satz von erlernbaren Parametern. 

In der vorgeschlagenen Lösung besteht die Klassifizierungs Leitung aus Single-Qubit-Drehungen und zwei-Qubit-gesteuerten Rotationen. Die erlernbaren Parameter sind die Drehwinkel. Die Drehung und kontrollierten Drehungs Gates sind bekanntermaßen für die Quantum-Berechnung *universell* , was bedeutet, dass jede einheitliche Gewichtungs Matrix in eine lange genug Verbindung zerlegt werden kann, die aus solchen Gates besteht.

![Mehrschichtiges Perzeptron und Circuit zentrierter Klassifizierer](~/media/DLvsQCC.png)

Wir können dieses Modell mit einem mehrschichtigen Perzeptron vergleichen, um die grundlegende Struktur besser zu verstehen. Im Perzeptron wird der prätorialisierer $p (y | x, \anta) $ durch den Satz von Gewichtungen $ \denta $ parameteriert, die die linearen Funktionen bestimmen, die die nichtlinearen Aktivierungs Funktionen verbinden (Neuronen). Diese Parameter können trainiert werden, um das Modell zu erstellen. Auf der Ausgabe Ebene können wir die Wahrscheinlichkeit eines Beispiels, das zu einer Klasse gehört, mithilfe von nichtlinearen Aktivierungs Funktionen wie "Software Maximum" erhalten. In der Verbindungs zentrierten Klassifizierer wird der präkator durch die Drehwinkel der einzelnen Qubit-und zwei-Qubit-Steuerelement Drehungen der Modell Leitung parametert. Auf ähnliche Weise können diese Parameter durch eine hybride Quantum/Classic-Version des Algorithmus für den Farbverlaufs Abstieg trainiert werden. Um die Ausgabe zu berechnen, anstatt nichtlineare Aktivierungs Funktionen zu verwenden, wird die Wahrscheinlichkeit der Klasse durch das Lesen von wiederholten Messungen über ein bestimmtes Qubit nach den kontrollierten Drehungen erreicht. Zum Codieren der klassischen Daten in einem Quantenzustand verwenden wir eine steuerbare Codierungs Verbindung für die Zustands Vorbereitung.

Unsere Architektur untersucht relativ flache Verbindungen, die daher *schnell entfangen* müssen, um alle Korrelationen zwischen den Daten Features in allen Bereichen aufzuzeichnen. In der folgenden Abbildung ist ein Beispiel für die sehr nützliche schnell Verlaufs-Leitungs Komponente dargestellt. Obwohl eine Verbindung mit dieser Geometrie nur aus $3 n + 1 $ Gates besteht, gewährleistet die einheitliche Gewichtungs Matrix, die Sie berechnet, eine bedeutende Kreuz Diskussion zwischen den $2 ^ n $-Features.

![Das schnelle entwirren von Quantum Circuit auf 5 Qubits (mit zwei zyklischen Ebenen).](~/media/5-qubit-qccc.png)

Die Verbindung im obigen Beispiel besteht aus 6 Single-Qubit Gates $ (G_1, \ldots, G_5; G_ {16} ) $ und 10 2-Qubits Gates $ (G_6, \ldots, g_ {15} ) $. Angenommen, jedes der Gates ist mit einem learnable-Parameter definiert. Wir haben 16 learnable-Parameter, während die Dimension des 5-Qubit-Hilbert-Raums 32 ist. Eine solche Schaltflächen Geometrie kann problemlos in beliebige $n $-Qubit-Register verallgemeinert werden, wenn $n $ ungerade ist, und gibt Verbindungen mit $3 n + 1 $-Parametern für $2 ^ n $-dimensionaler Merkmals Raum.

## <a name="classifier-training-as-a-supervised-learning-task"></a>Klassifizierungs Training als beaufsichtigte lernaufgabe

Das Trainieren eines Klassifizierungs Modells umfasst das Auffinden optimaler Werte der operativen Parameter, sodass Sie die durchschnittliche Wahrscheinlichkeit maximieren, dass die richtigen Trainings Bezeichnungen in den Trainings Beispielen abgeleitet werden.
Hier betreffen wir nur die Klassifizierung mit zwei Ebenen, d. h. die Groß-/Kleinschreibung von $d = $2 und nur zwei Klassen mit den Bezeichnungen $y _1, y_2 $.

> [!NOTE]
> Eine prinzipielle Methode der Generalisierung unserer Methoden für eine beliebige Anzahl von Klassen besteht darin, Qubits durch qudits, d. h. durch $d $-Basiszustände, und die bidirektionale Messung mit $d $-Way-Messung zu ersetzen.

### <a name="likelihood-as-the-training-goal"></a>Wahrscheinlichkeit als Trainingsziel

Bei einem Informations fähigen Quantum Circuit $U (\orta) $, wobei $ \thta $ ein Vektor von Parametern ist, und die abschließende Messung durch $M $ bezeichnet, ist die durchschnittliche Wahrscheinlichkeit, dass der richtige Bezeichnungs Schluss ergibt, $ $ \begin{align} \mathcal{l} (\teta) = \frac {1} {| \mathcal{d} |} \left (\ sum_ {(x, Y_1) \in\mathcal{D}} P (M = Y_1 | U (\orta) x) + \ sum_ {(x, y_2) \in\mathcal{D}} P (M = y_2 | U (\urta) x) \right) \end{align} $ $ WHERE $P (M = y | z) $ ist die Wahrscheinlichkeit, $y $ im Quantum-Status $z $ zu messen.
Hier genügt es zu verstehen, dass die Wahrscheinlichkeitsfunktion $ \mathcal{l} (\teta) $ in $ \teta $ reibungslos ist und die Ableitung in $ \ theta_j $ im Grunde dasselbe Quantum-Protokoll berechnet werden kann, das auch zum Berechnen der Wahrscheinlichkeitsfunktion verwendet wird. Dies ermöglicht die Optimierung von $ \mathcal{l} (\teta) $ by Gradient Descent.

### <a name="classifier-bias-and-training-score"></a>Klassifizierungs-und Trainings Bewertung

Bei einigen zwischen Werten (oder Endwerten) der Parameter in $ \teta $ muss ein einzelner realer Wert identifiziert werden, $b $ als *klassifizierungsbias* für die Rückschlüsse bekannt ist. Die Regel für die Bezeichnung der Bezeichnung funktioniert wie folgt: 
- Ein Beispiel $x $ wird die Bezeichnung $y _2 $ if und nur dann zugewiesen, wenn $P (M = y_2 | U (\erta) x) + b > $0,5 (Regel 1) (andernfalls wird die Bezeichnung $y _1 $ zugewiesen)

Eindeutig $b $ muss das Intervall von $ (-0,5, + 0,5) $ aufweisen, damit es sinnvoll ist.

Ein Trainings Fall $ (x, y) \in \mathcal{d} $ wird bei Berücksichtigung der Bias-$b $ als fehl *Klassifizierung* betrachtet, wenn sich die Bezeichnung, die für $x $ as per Regel 1 abgeleitet wurde, tatsächlich von $y $ unterscheidet. Die Gesamtanzahl der fehl Klassifizierungen ist die *Trainings Bewertung* des Klassifizierers, bei der der Bias $b $ liegt. Der *optimale* Klassifizierungs Aufwand $b $ minimiert die Trainings Bewertung. Wenn die Voraus berechnete Wahrscheinlichkeitsschätzung $ \{ P (M = y_2 | U (\orta) x) | (x, *) \in\mathcal{d} \} $. die optimale klassifizierungsabweichung kann durch die binäre Suche im Intervall von $ (-0,5, + 0,5) $ gefunden werden, indem höchstens $ \ Log_2 (| \mathcal{d} |) festgestellt wird. $ Steps.

### <a name="reference"></a>Verweis

Diese Informationen sollten ausreichen, um mit dem Code zu beginnen. Wenn Sie jedoch mehr über dieses Modell erfahren möchten, lesen Sie den ursprünglichen Vorschlag: [ *"Circuit-zentrierte Quantum Classifiers", Maria Schuld, Alex Bocharov, Krysta svore und Nathan Wiebe*](https://arxiv.org/abs/1804.00633)
