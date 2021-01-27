---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Drawrandomdouble-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847624"
---
# <a name="drawrandomdouble-operation"></a>Drawrandomdouble-Vorgang

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Zeichnet eine zufällige reelle Zahl in einem angegebenen inklusiven Intervall.

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a>Eingabe

### <a name="min--double"></a>Min: [Double](xref:microsoft.quantum.lang-ref.double)

Die kleinste reelle Zahl, die gezeichnet werden soll.


### <a name="max--double"></a>Max.: [Double](xref:microsoft.quantum.lang-ref.double)

Die größte reelle Zahl, die gezeichnet werden soll.



## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Eine zufällige reelle Zahl im inklusiven Intervall von `min` bis `max` mit einheitlicher Wahrscheinlichkeit.

## <a name="example"></a>Beispiel

Der folgende f #-Code Ausschnitt zeichnet nach dem Zufallsprinzip einen Winkel zwischen $0 $ und $2 \pi $:

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a>Bemerkungen

Schlägt fehl, wenn `max <= min` .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. continuousunifordistribution](xref:Microsoft.Quantum.ContinuousUniformDistribution)