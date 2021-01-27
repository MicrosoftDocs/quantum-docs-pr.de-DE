---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Drawrandomint-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851135"
---
# <a name="drawrandomint-operation"></a>Drawrandomint-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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

## <a name="example"></a>Beispiel

Der folgende f #-Code Ausschnitt führt nach dem Zufallsprinzip zu einem sechsseitigen Würfel:

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a>Bemerkungen

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. diskreteunifordistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)