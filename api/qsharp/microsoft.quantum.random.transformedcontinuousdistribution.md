---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: Transformedcontinuousdistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: 353442a4245a9e20bb1e4c46d2e8a84d4c9534b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857771"
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

## <a name="example"></a>Beispiel

Die folgenden beiden Distributionen sind identisch:

```qsharp
let dist1 = ContinuousUniformDistribution(1.0, 2.0);
let dist2 = TransformedContinuousDistribution(
    PlusD(1.0, _),
    ContinuousUniformDistribution(0.0, 1.0)
);
```