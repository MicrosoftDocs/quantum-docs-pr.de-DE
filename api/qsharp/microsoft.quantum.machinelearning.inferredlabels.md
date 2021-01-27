---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Inferredlabels-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848406"
---
# <a name="inferredlabels-function"></a>Inferredlabels-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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