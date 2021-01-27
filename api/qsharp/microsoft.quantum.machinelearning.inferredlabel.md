---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Inferredlabel-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 46b24c283a01e6ac1c959ee4a6899591ee708ff7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848420"
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