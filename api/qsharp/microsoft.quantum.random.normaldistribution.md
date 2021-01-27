---
uid: Microsoft.Quantum.Random.NormalDistribution
title: Normaldistribution-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: NormalDistribution
qsharp.summary: Returns a normal distribution with a given mean and variance.
ms.openlocfilehash: 733a2763dca6d75f81d538f63c3084331a8e1d51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814182"
---
# <a name="normaldistribution-function"></a>Normaldistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt eine normale Verteilung mit einem angegebenen Mittelwert und Varianz zurück.

```qsharp
function NormalDistribution (mean : Double, variance : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Eingabe

### <a name="mean--double"></a>Mittelwert: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="variance--double"></a>Varianz: [Double](xref:microsoft.quantum.lang-ref.double)





## <a name="output--continuousdistribution"></a>Ausgabe: [continuousdistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)



## <a name="example"></a>Beispiel

Der folgende Code zeichnet 10 Beispiele aus der normalen Verteilung mit dem Mittelwert 2 und der Standardabweichung 0,1:

```qsharp
let samples = DrawMany(
    (NormalDistribution(2.0, PowD(0.1, 2.0)))::Sample,
    10, ()
);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Random. standardnormaldistribution](xref:Microsoft.Quantum.Random.StandardNormalDistribution)