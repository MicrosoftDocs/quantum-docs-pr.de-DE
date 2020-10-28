---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Transformedcontinuousdistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 6a6e0c26bd650fd4c05208197ff23f951d1c3b5c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701885"
---
# <a name="transformedcontinuousdistribution-function"></a>Transformedcontinuousdistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


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