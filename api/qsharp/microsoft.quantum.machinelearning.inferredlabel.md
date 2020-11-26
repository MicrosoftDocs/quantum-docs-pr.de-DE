---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Inferredlabel-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: b64bb1ec52d2456ee1b627b920890223d173533b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211779"
---
# <a name="inferredlabel-function"></a>Inferredlabel-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt bei einer Klassifizierungs Wahrscheinlichkeit und einem Bias die Bezeichnung zurück, die von dieser Wahrscheinlichkeit abgeleitet wurde.

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a>Eingabe

### <a name="bias--double"></a>Bias: [Double](xref:microsoft.quantum.lang-ref.double)

Die Verschiebung zwischen zwei Klassen, in der Regel das Ergebnis des Trainings eines Klassifizierers.


### <a name="probability--double"></a>Wahrscheinlichkeit: [Double](xref:microsoft.quantum.lang-ref.double)

Eine Klassifizierungs Wahrscheinlichkeiten für ein bestimmtes Beispiel, die sich in der Regel aus der Schätzung der Klassifizierungs Häufigkeit ergibt.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Bezeichnung, die von der angegebenen Klassifizierungs Wahrscheinlichkeit abgeleitet wurde.