---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Iteratethrough cartesianproduct-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: e4fc71f6f707639f6f89eece8546ec2fb434a15a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704095"
---
# <a name="iteratethroughcartesianproduct-operation"></a>Iteratethrough cartesianproduct-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang für jeden Index im kartesischen Produkt mehrerer Bereiche an.

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wendet iterativ einen Vorgang für jedes Element des kartesischen Produkts von `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,... an, `0..(bounds[Length(bounds) - 1] - 1)`

## <a name="input"></a>Eingabe

### <a name="bounds--int"></a>Begrenzungen: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das die Bereiche angibt, die durchlaufen werden sollen, wobei jeder Bereich als ganzzahlige Länge angegeben wird.


### <a name="op--int--unit"></a>OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der für jedes Element des angegebenen kartesischen Produkts aufgerufen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. iteratequercartesianpower](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)