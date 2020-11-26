---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Maybechooeinelement-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192858"
---
# <a name="maybechooseelement-operation"></a>Maybechooeinelement-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Wenn ein Array von Daten und eine Verteilung über die Indizes verfügen, versucht, ein Element nach dem Zufallsprinzip auszuwählen.

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a>Eingabe

### <a name="data--t"></a>Daten: 't []

Das Array, aus dem ein Element ausgewählt werden soll.


### <a name="indexdistribution--discretedistribution"></a>indexdistribution: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Eine Verteilung über die Indizes von `data` .



## <a name="output--boolt"></a>Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

