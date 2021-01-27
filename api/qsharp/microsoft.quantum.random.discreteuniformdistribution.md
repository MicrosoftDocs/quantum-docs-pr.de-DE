---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: Diskreteunifordistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853719"
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

## <a name="example"></a>Beispiel

Der folgende f #-Code Ausschnitt führt nach dem Zufallsprinzip zu einem sechsseitigen Würfel:

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a>Bemerkungen

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. drawrandomdouble](xref:Microsoft.Quantum.DrawRandomDouble)