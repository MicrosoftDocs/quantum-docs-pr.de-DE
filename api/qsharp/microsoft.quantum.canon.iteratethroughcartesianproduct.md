---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Iteratethrough cartesianproduct-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840278"
---
# <a name="iteratethroughcartesianproduct-operation"></a>Iteratethrough cartesianproduct-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Vorgang für jeden Index im kartesischen Produkt mehrerer Bereiche an.

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Beschreibung

Wendet iterativ einen Vorgang für jedes Element des kartesischen Produkts von `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,... an, `0..(bounds[Length(bounds) - 1] - 1)`

## <a name="input"></a>Eingabe

### <a name="bounds--int"></a>Begrenzungen: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das die Bereiche angibt, die durchlaufen werden sollen, wobei jeder Bereich als ganzzahlige Länge angegeben wird.


### <a name="op--int--unit"></a>OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der für jedes Element des angegebenen kartesischen Produkts aufgerufen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Bei einem Vorgang `op` sind die folgenden beiden Code Ausschnitte äquivalent:

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. iteratequercartesianpower](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)