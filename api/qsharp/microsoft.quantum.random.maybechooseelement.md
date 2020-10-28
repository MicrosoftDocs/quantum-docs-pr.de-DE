---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Maybechooeinelement-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 12640d9dc3aad301146eff7bcbbaae33d3ccd420
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722164"
---
# <a name="maybechooseelement-operation"></a>Maybechooeinelement-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


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

