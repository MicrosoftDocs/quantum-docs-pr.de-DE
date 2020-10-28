---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Diskreteunifordistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706727"
---
# <a name="discreteuniformdistribution-function"></a>Diskreteunifordistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. drawrandomdouble](xref:Microsoft.Quantum.DrawRandomDouble)