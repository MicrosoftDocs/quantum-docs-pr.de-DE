---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Continuousunifordistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701237"
---
# <a name="continuousuniformdistribution-function"></a>Continuousunifordistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


Gibt eine einheitliche Verteilung über ein bestimmtes inklusives Intervall zurück.

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Eingabe

### <a name="min--double"></a>Min: [Double](xref:microsoft.quantum.lang-ref.double)

Die kleinste reelle Zahl, die gezeichnet werden soll.


### <a name="max--double"></a>Max.: [Double](xref:microsoft.quantum.lang-ref.double)

Die größte reelle Zahl, die gezeichnet werden soll.



## <a name="output--continuousdistribution"></a>Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Eine Verteilung, deren zufällige variate echte Zahlen im inklusiven Intervall von `min` bis `max` mit einheitlicher Wahrscheinlichkeit sind.

## <a name="remarks"></a>Hinweise

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. drawrandomdouble](xref:Microsoft.Quantum.DrawRandomDouble)