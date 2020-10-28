---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Drawrandomint-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724656"
---
# <a name="drawrandomint-operation"></a>Drawrandomint-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


Zeichnet eine zufällige ganze Zahl in einem angegebenen inklusiven Bereich.

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a>Eingabe

### <a name="min--int"></a>Min: [int](xref:microsoft.quantum.lang-ref.int)

Die kleinste Ganzzahl, die gezeichnet werden soll.


### <a name="max--int"></a>Max: [int](xref:microsoft.quantum.lang-ref.int)

Die größte Ganzzahl, die gezeichnet werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl im inklusiven Bereich von `min` bis `max` mit einheitlicher Wahrscheinlichkeit.

## <a name="remarks"></a>Hinweise

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. diskreteunifordistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)