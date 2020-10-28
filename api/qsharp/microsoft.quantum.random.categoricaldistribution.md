---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Kategoricaldistribution-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 756e9e95cac5554ab8f885dab7c47ac1b174c0f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722821"
---
# <a name="categoricaldistribution-function"></a>Kategoricaldistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paketen [](https://nuget.org/packages/)


Gibt eine diskrete kategorische Verteilung zurück, bei der die Wahrscheinlichkeit für jede endliche Liste der angegebenen Ergebnisse explizit angegeben wird.

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Eingabe

### <a name="probs--double"></a>probs: [Double](xref:microsoft.quantum.lang-ref.double)[]

Die Wahrscheinlichkeiten für die einzelnen Ergebnisse aus der kategorischen Verteilung.
Diese Wahrscheinlichkeiten werden möglicherweise nicht normalisiert, müssen jedoch alle nicht negativ sein.



## <a name="output--discretedistribution"></a>Ausgabe: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Der Index `i` mit der Wahrscheinlichkeit `probs[i] / sum` , wobei `sum` die Summe von ist, die `probs` von angegeben wird `Fold(PlusD, 0.0, probs)` .