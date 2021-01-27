---
uid: Microsoft.Quantum.Arrays.Merged
title: Zusammengeführte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: 262e7450188370212a7e2a57bf15e9f8ab162814
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845608"
---
# <a name="merged-function"></a>Zusammengeführte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bei zwei sortierten Arrays wird ein einzelnes Array mit den Elementen beider Elemente in sortierter Reihenfolge zurückgegeben. Wird intern von der Merge-Sortierung verwendet.

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="comparison--tt---bool"></a>Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)




### <a name="left--t"></a>Left: 't []




### <a name="right--t"></a>Right: 't []





## <a name="output--t"></a>Ausgabe: 't []



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

