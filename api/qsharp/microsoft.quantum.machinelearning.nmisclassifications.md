---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Nfehllassikationen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: adc7042d6108c7ec72d13340633824d3eaf5e18e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853917"
---
# <a name="nmisclassifications-function"></a>Nfehllassikationen-Funktion

Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)

Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gibt die Anzahl der Indizes zurück, bei denen sich die einzelnen Bezeichnungen unterscheiden, wenn eine Reihe von abhergelegten Bezeichnungen und ein Satz korrekter Bezeichnungen angegeben sind.

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="proposed--int"></a>vorgeschlagen: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="actual--int"></a>tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Indizes `idx` `inferredLabels[idx] != actualLabels[idx]` .

## <a name="example"></a>Beispiel

```qsharp
let nMisclassifications = NMisclassifications([1, 1, 0, 0], [0, 1, 1, 0]);
Message($"{nMisclassifications}"); // Will print 2.
```