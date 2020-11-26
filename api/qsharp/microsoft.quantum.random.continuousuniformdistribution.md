---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: Continuousunifordistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193079"
---
# <a name="continuousuniformdistribution-function"></a>Continuousunifordistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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

## <a name="remarks"></a>Bemerkungen

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. drawrandomdouble](xref:Microsoft.Quantum.DrawRandomDouble)