---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Inferredlabels-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 874d1a2f7cc6d67567e0d2baa70b0d26b639a029
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722485"
---
# <a name="inferredlabels-function"></a>Inferredlabels-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


Gibt ein Array von Klassifizierungs Wahrscheinlichkeiten und eine Abweichung zurück und gibt die Bezeichnung zurück, die aus jeder Wahrscheinlichkeit abgeleitet wurde.

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="bias--double"></a>Bias: [Double](xref:microsoft.quantum.lang-ref.double)

Die Verschiebung zwischen zwei Klassen, in der Regel das Ergebnis des Trainings eines Klassifizierers.


### <a name="probabilities--double"></a>Wahrscheinlichkeiten: [Double](xref:microsoft.quantum.lang-ref.double)[]

Ein Array von Klassifizierungs Wahrscheinlichkeiten für eine Reihe von Beispielen, die sich in der Regel aus der Schätzung von Klassifizierungs Frequenzen ergeben.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Die Bezeichnung, die von den einzelnen Klassifizierungs Wahrscheinlichkeiten abgeleitet wurde.