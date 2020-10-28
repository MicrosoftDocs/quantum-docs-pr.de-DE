---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Inferredlabel-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 1d6edec94f731fe96da797f0c3d77e6eba565149
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722514"
---
# <a name="inferredlabel-function"></a>Inferredlabel-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paketen [](https://nuget.org/packages/)


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