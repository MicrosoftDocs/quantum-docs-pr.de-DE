---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: Kategoricaldistribution-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210249"
---
# <a name="categoricaldistribution-function"></a>Kategoricaldistribution-Funktion

Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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