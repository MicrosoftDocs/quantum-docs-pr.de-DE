---
title: Quantum Machine Learning-Bibliothek
author: alexeib2
ms.author: alexei.bocharov@microsoft.com
ms.date: 2/27/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.training
no-loc:
- Q#
- $$v
ms.openlocfilehash: 52c3f69fb99384270a27e57c4f32212d18bee1a4
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868898"
---
# <a name="quantum-machine-learning-glossary"></a>Quantum Machine Learning Glossar

Das Training eines Circuit-zentrierten quantumers ist ein Prozess mit vielen beweglichen Teilen, bei denen die gleiche (oder etwas größere) Menge an Kalibrierung nach Testversion und Fehler als das Training herkömmlicher Klassifizierungen erforderlich ist. Hier werden die Hauptkonzepte und-Komponenten dieses Schulungsprozesses definiert.

## <a name="trainingtesting-schedules"></a>Trainings-/Testzeitpläne

Im Kontext des Klassifizierungs Trainings wird in einem *Zeitplan* eine Teilmenge der Daten Stichproben in einem allgemeinen Trainings-oder Testsatz beschrieben. Ein Zeitplan wird normalerweise als Sammlung von Beispiel Indizes definiert.

## <a name="parameterbias-scores"></a>Parameter/Bias-Ergebnisse

Wenn Sie einen Kandidaten Parameter Vektor und einen Klassifizierungs-Bias haben, wird das *Validierungs Ergebnis* in Relation zu einem ausgewählten Überprüfungs Zeitplan s gemessen und durch eine Reihe von fehl Klassifizierungen ausgedrückt, die über alle Stichproben im Zeitplan hinaus gezählt werden.

## <a name="hyperparameters"></a>Hyperparameter

Der Modell Trainingsprozess unterliegt bestimmten voreingestellten Werten, die als *Hyperparameter*bezeichnet werden:

### <a name="learning-rate"></a>Learning rate (Lernrate)

Dabei handelt es sich um einen der wichtigsten Hyperparameter. Es definiert, wie viel aktuelle stochastischen Gradient-Schätzung Auswirkungen auf das Update des Parameters hat. Die Größe der Delta-Aktualisierungsrate ist proportional zur Lernrate. Kleinere Lernraten Werte führen zu einer langsameren Parameter Entwicklung und einer langsameren Konvergenz, aber übermäßig große Werte von LR können die Konvergenz nicht beeinträchtigt werden, da der gradientenabstieg niemals ein bestimmtes lokales minimal Commit durchführt. Obwohl die Lernrate in gewisser Weise vom Trainings Algorithmus angepasst wird, ist es wichtig, einen guten Anfangswert auszuwählen. Ein üblicher Standard Anfangswert für die Lernrate ist 0,1. Die Auswahl des besten Werts der Lernrate ist eine gute Grafik (z. b. Abschnitt 4,3 von Goodfellow et al., Deep Learning, mit Press, 2017).

### <a name="minibatch-size"></a>Minibatch-Größe

Definiert, wie viele Daten Beispiele für eine einzelne Schätzung des stochastischen Farbverlaufs verwendet werden. Größere Werte der Mini Batch-Größe führen in der Regel zu stabilerer und mehr monotonischer Konvergenz, können den Trainingsprozess jedoch möglicherweise verlangsamen, da die Kosten einer einzelnen gradientenschätzung proportional zur Minimalgröße sind. Ein üblicher Standardwert für die Mini Batch-Größe ist 10.

### <a name="training-epochs-tolerance-gridlocks"></a>Schulungs Epochen, Toleranz, Gridlocks

"Epoche" bedeutet eine komplette Durchführung der geplanten Trainingsdaten.
Die maximale Anzahl von Epochen pro Trainings Thread (siehe unten) sollte begrenzt sein. Der Trainings Thread wird so definiert, dass er (mit den besten bekannten Kandidaten Parametern) beendet wird, wenn die maximale Anzahl von Epochen ausgeführt wurde. Diese Schulung würde jedoch früher beendet werden, wenn die fehl Klassifizierungs Rate bei einem Überprüfungs Zeitplan unter eine ausgewählte Toleranz fällt. Angenommen, die falsche Klassifizierungs Toleranz ist 0,01 (1%); Wenn bei einem Validierungs Satz von 2000 Beispielen weniger als 20 fehl Klassifizierungen angezeigt werden, ist die Toleranzstufe erreicht. Ein Trainings Thread wird auch vorzeitig beendet, wenn das Validierungs Ergebnis des Kandidaten Modells in mehreren aufeinander folgenden Epochen (einem gridlock) keine Verbesserung zeigte. Die Logik für das Beenden des gridlock ist zurzeit hart codiert.

### <a name="measurements-count"></a>Anzahl von Messungen

Das schätzen der Trainings-/Validierungsergebnisse und der Komponenten des stochastischen-Farbverlaufs auf einem Quantum-Gerät bedeutet, dass Quantum-Status Überschneidungen geschätzt werden, die mehrere Messungen der entsprechenden Observables erfordern. Die Anzahl der Messungen sollte als $O (1/\ Epsilon ^ 2) $ skaliert werden, wobei $ \epsilon $ der gewünschte Schätz Fehler ist.
Als Faustregel gilt, dass die anfängliche Anzahl von Messungen ungefähr $1/\ mbox {Tolerance} ^ 2 $ betragen kann (siehe Definition der Toleranz im vorherigen Absatz). Sie müssen die Anzahl der Messungen aufwärts überarbeiten, wenn der Verlaufs Abstieg zu unregelmäßig und die Konvergenz zu schwer zu erreichen ist.

### <a name="training-threads"></a>Trainieren von Threads

Die Wahrscheinlichkeitsfunktion, bei der es sich um das Schulungs Dienstprogramm für den Klassifizierer handelt, ist sehr selten eine Konstante, was bedeutet, dass Sie in der Regel über eine Vielzahl von lokalem Optima im Parameter Bereich verfügt, die sich durch Qualität Da der SGD-Prozess nur mit einer bestimmten optimalen konvergiert werden kann, ist es wichtig, mehrere Startparameter Vektoren zu untersuchen. Gängige Vorgehensweise beim maschinellen Lernen besteht darin, solche Start Vektoren nach dem Zufallsprinzip zu initialisieren. Die Q# Trainings-API akzeptiert ein beliebiges Array solcher Start Vektoren, aber der zugrunde liegende Code untersucht sie sequenziell. Auf einem Computer mit mehreren Kernen oder in einer beliebigen Parallel Computing-Architektur empfiehlt es sich, mehrere Aufrufe Q# der Trainings-API parallel mit verschiedenen Parameter Initialisierungen über die Aufrufe auszuführen.

#### <a name="how-to-modify-the-hyperparameters"></a>Ändern der Hyperparameter

In der QML-Bibliothek besteht die beste Möglichkeit zum Ändern der Hyperparameter darin, die Standardwerte des UDT zu überschreiben [`TrainingOptions`](xref:microsoft.quantum.machinelearning.trainingoptions) . Zu diesem Zweck wird diese mit der-Funktion aufgerufen [`DefaultTrainingOptions`](xref:microsoft.quantum.machinelearning.defaulttrainingoptions) und der-Operator angewendet `w/` , um die Standardwerte zu überschreiben. Um z. b. 100.000 Messungen und eine Lernrate von 0,01 zu verwenden, verwenden Sie Folgendes:
 ```qsharp
let options = DefaultTrainingOptions()
w/ LearningRate <- 0.01
w/ NMeasurements <- 100000;
 ```
