---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Transformedcontinuousdistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226263"
---
# <a name="transformedcontinuousdistribution-function"></a>Transformedcontinuousdistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt bei einer kontinuierlichen Verteilung eine neue Verteilung zurück, die den ursprünglichen durch eine angegebene Funktion transformiert.

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Eingabe

### <a name="transform--double---double"></a>Transformation: [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)

Eine Funktion, die variate der ursprünglichen Verteilung in die transformierte Verteilung umwandelt.


### <a name="distribution--continuousdistribution"></a>Verteilung: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Die ursprüngliche Verteilung, die transformiert werden soll.



## <a name="output--continuousdistribution"></a>Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Eine neue Distribution, `distribution` die durch die durch angegebene Transformation verknüpft ist `transform` .