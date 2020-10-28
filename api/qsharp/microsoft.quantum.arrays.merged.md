---
uid: Microsoft.Quantum.Arrays.Merged
title: Zusammengeführte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705871"
---
# <a name="merged-function"></a>Zusammengeführte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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

