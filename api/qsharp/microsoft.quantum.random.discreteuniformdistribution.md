---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Diskreteunifordistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 08a62805f59df339ef6b91dff802c40c407808f4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193011"
---
# <a name="discreteuniformdistribution-function"></a>Diskreteunifordistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt eine einheitliche Verteilung für einen angegebenen inklusiven Bereich zurück.

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Eingabe

### <a name="min--int"></a>Min: [int](xref:microsoft.quantum.lang-ref.int)

Die kleinste Ganzzahl, die gezeichnet werden soll.


### <a name="max--int"></a>Max: [int](xref:microsoft.quantum.lang-ref.int)

Die größte Ganzzahl, die gezeichnet werden soll.



## <a name="output--discretedistribution"></a>Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Eine Verteilung, deren zufällige variate ganze Zahlen im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.

## <a name="remarks"></a>Bemerkungen

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. drawrandomdouble](xref:Microsoft.Quantum.DrawRandomDouble)