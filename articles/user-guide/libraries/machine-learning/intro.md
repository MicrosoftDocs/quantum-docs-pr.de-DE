---
title: Quantum Machine Learning-Bibliothek
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 11/22/2019
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 65b0aa6a7f385765933d4d89ce34901f77cf76ec
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863097"
---
# <a name="introduction-to-quantum-machine-learning"></a>Einführung in Quantum Machine Learning

## <a name="framework-and-goals"></a>Framework und Ziele

Die Quantum-Codierung und-Verarbeitung von Informationen ist eine leistungsfähige Alternative zu klassischen Machine Learning-Quantum-Klassifizierungen. Dies ermöglicht es uns, Daten in Quantum-Registern zu codieren, die relativ zur Anzahl der Features präzise sind. dabei wird die Quantum-jede Verflechtungen systematisch als Berechnungs Ressource verwendet und die Quantum-Messung für den Klassen Rückschluss verwendet.
Die Verbindungs zentrierte Quantum-Klassifizierung ist eine relativ einfache Quantum-Lösung, die die Daten Codierung mit einer schnellen Entangling/Disentangling-Quantum-Verbindung gefolgt von Messungen zum Ableiten von Klassen Bezeichnungen von Daten Beispielen kombiniert.
Das Ziel besteht darin, die klassische Charakterisierung und Speicherung von Themen Verbindungen zu gewährleisten sowie hybride Quantum/klassische Schulungen der Verbindungsparameter auch für extrem große Merkmals Räume zu gewährleisten.

## <a name="classifier-architecture"></a>Klassifizierungs Architektur

Bei der Klassifizierung handelt es sich um eine überwachte Machine Learning-Aufgabe, bei der das Ziel darin besteht, Klassen Bezeichnungen $ \{ Y_1, y_2, \ldots y_d \} $ bestimmter Daten Beispiele abzuleiten. Das Trainings Dataset ist eine Sammlung von Beispielen $ \mathcal{d} = \{ (x, y)} $ mit bekannten vorzugewiesenen Bezeichnungen. Hier $x $ ein Daten Sample, und $y $ ist die bekannte Bezeichnung "Trainings Bezeichnung".
Ähnlich wie herkömmliche Methoden besteht die Quantum-Klassifizierung aus drei Schritten:
- Daten Codierung
- Vorbereitung eines Klassifizierungs Zustands
- Messung aufgrund der Wahrscheinlichkeits Natur der Messung müssen diese drei Schritte mehrmals wiederholt werden. Sowohl die Codierung als auch das Berechnen des Klassifizierungs Zustands werden mithilfe von *Quantum*-Verbindungen durchgeführt. Während die Codierungs Verbindung in der Regel Daten gesteuert und Parameter frei ist, enthält die Klassifizierungs Leitung einen ausreichenden Satz von erlernbaren Parametern. 

In der vorgeschlagenen Lösung besteht die Klassifizierungs Leitung aus Single-Qubit-Drehungen und zwei-Qubit-gesteuerten Rotationen. Die erlernbaren Parameter sind die Drehwinkel. Die Drehung und kontrollierten Drehungs Gates sind bekanntermaßen für die Quantum-Berechnung *universell* , was bedeutet, dass jede einheitliche Gewichtungs Matrix in eine lange genug Verbindung zerlegt werden kann, die aus solchen Gates besteht.

In der vorgeschlagenen Version wird nur eine Verbindung gefolgt von einer einzelnen Frequenz Schätzung unterstützt.
Folglich ist die Lösung eine Quantum-Analog eines Unterstützungs Vektor Computers mit einem Low-Degree-Polynoms-Kernel.

![Mehrschichtiges Perzeptron und Circuit zentrierter Klassifizierer](~/media/DLvsQCC.png)

Ein einfacher Quantum Klassifizierungs-Entwurf kann mit einer herkömmlichen SVM-Lösung (Support Vector Machine) verglichen werden. Der Rückschluss für ein Daten Beispiel $x $ im Fall von SVM erfolgt mithilfe der optimalen Kernel Form $ \sum \ alpha_j k (x_j, x) $, wobei $k $ eine bestimmte Kernel Funktion ist.

Im Gegensatz dazu verwendet ein Quantum Klassifizierungs den präktor $p (y │ x, U (\orta)) = 〈 U (\erta) x | M | U (\urta) x 〉 $, das in Spirit ähnlich ist, aber technisch genau anders ist. Wenn also eine einfache Amplitude-Codierung verwendet wird, ist $p (y │ x, U (\theta)) $ ein quadratisches Formular in den verstärken $x $, aber die Koeffizienten dieses Formulars werden nicht mehr unabhängig erlernt. Sie werden stattdessen aus den Matrixelementen der Verbindungs $U (\orta) $ aggregiert, die in der Regel deutlich weniger learnable-Parameter $ \orta $ als die Dimension des Vektors $x $. Der polynomale Grad des $p (y │ x, U (\urta)) $ in den ursprünglichen Funktionen kann auf $2 ^ l $ erweitert werden, indem eine Quantum-Produktcodierung in $l $-Kopien von $x $ verwendet wird.

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

### <a name="reference"></a>Referenz

Diese Informationen sollten ausreichen, um mit dem Code zu beginnen. Wenn Sie jedoch mehr über dieses Modell erfahren möchten, lesen Sie den ursprünglichen Vorschlag: [ *"Circuit-zentrierte Quantum Classifiers", Maria Schuld, Alex Bocharov, Krysta svore und Nathan Wiebe*](https://arxiv.org/abs/1804.00633)

Zusätzlich zum Codebeispiel, das Sie in den nächsten Schritten sehen werden, können Sie in [diesem Tutorial](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/QuantumClassification) auch mit der Erkundung der Quantum-Klassifizierung beginnen. 
