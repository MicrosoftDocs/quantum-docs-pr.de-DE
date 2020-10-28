---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Trainingoptions-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 5ecc2b5175a4e8db78f72311ac1d5ff964bae811
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722374"
---
# <a name="trainingoptions-user-defined-type"></a>Trainingoptions-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Eine Auflistung von Optionen, die beim Trainieren von Quantum Classifiers verwendet werden sollen.

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a>Benannte Elemente

### <a name="learningrate--double"></a>Learningrate: [Double](xref:microsoft.quantum.lang-ref.double)

Die Lernrate, mit der Gradienten beim Aktualisieren von Modellparametern während der Trainingsschritte neu berechnet werden sollen.
### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)

Die Näherungs Toleranz, die beim Vorbereiten von Beispielen als quantale Zustände verwendet werden soll.
### <a name="minibatchsize--int"></a>Minibatchsize: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Samplings, die in den einzelnen Trainings-minibatches verwendet werden sollen.
### <a name="nmeasurements--int"></a>Nmessungen: [int](xref:microsoft.quantum.lang-ref.int)

Gibt an, wie oft jedes Klassifizierungs Ergebnis gemessen werden soll, um die Klassifizierungs Wahrscheinlichkeit einzuschätzen.
### <a name="maxepochs--int"></a>Maxepochen: [int](xref:microsoft.quantum.lang-ref.int)

Die maximale Anzahl von Epochen, für die jedes Modell trainiert werden soll.
### <a name="maxstalls--int"></a>Maxstems: [int](xref:microsoft.quantum.lang-ref.int)

Die maximale Anzahl von Verläufen für eine Trainings Epoche (ungefähr 0 (null)), bevor ein Fehler auftritt.
### <a name="stochasticrescalefactor--double"></a>Stochastikrescalefactor: [Double](xref:microsoft.quantum.lang-ref.double)

Der Betrag für das erneute Skalieren von mit dem Gerät abgehaltenen Modellen durch vor dem erneuten Ausführen
### <a name="scoringperiod--int"></a>Scoringperiod: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Verlaufs Schritte, die zwischen Bewertungs Punkten durchgeführt werden sollen.
Legen Sie für optimale Genauigkeit den Wert 1 fest.
### <a name="verbosemessage--string---unit"></a>Verbotmessage: [Zeichen](xref:microsoft.quantum.lang-ref.string) folgen -> [Einheit](xref:microsoft.quantum.lang-ref.unit)

Eine Funktion, die verwendet werden kann, um ausführliche Rückmeldungen bereitzustellen.

## <a name="remarks"></a>Hinweise

Dieser UDT sollte nicht direkt erstellt werden, sondern sollte stattdessen durch Aufrufen von angegeben werden @"microsoft.quantum.machinelearning.defaulttrainingoptions" . Anschließend wird der- `w/` Operator verwendet, um andere Standardwerte zu überschreiben.

Beispielsweise, um 100.000 Messungen und höchstens 8 Schulungs Epochen zu verwenden:

```Q#
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a>Referenzen

- [arXiv: 1804.00633](https://arxiv.org/abs/1804.00633)