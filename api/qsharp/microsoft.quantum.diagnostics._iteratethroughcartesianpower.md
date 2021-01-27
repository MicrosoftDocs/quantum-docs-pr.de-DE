---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: a27302be75ee701b0629310700b56d222aaef7db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853563"
---
# <a name="_iteratethroughcartesianpower-operation"></a>_iterateThroughCartesianPower Vorgang

Namespace: [Microsoft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Iteriert eine Variable über ein kartesisches Produkt [0, Begrenzungen [0]-1] × [0, Begrenzungen [1]-1] × [0, Begrenzungen [length (Begrenzungen)-1]-1] und ruft op (arr) für jedes Element des kartesischen Produkts auf.

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a>Eingabe

### <a name="length--int"></a>Länge: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--int--unit"></a>OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 





## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)

