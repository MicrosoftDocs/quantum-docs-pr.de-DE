---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Iteratethrough cartesianpower-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704087"
---
# <a name="iteratethroughcartesianpower-operation"></a>Iteratethrough cartesianpower-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Wendet einen Vorgang für jeden Index in der kartesischen Potenz eines ganzzahligen Bereichs an.

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Wendet iterativ einen Vorgang für jedes Element einer kartesischen Potenz des Bereichs an `0..(bound - 1)` .

## <a name="input"></a>Eingabe

### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Die kartesische Potenz, in die der Bereich `0..(bound - 1)` ausgelöst werden soll.


### <a name="bound--int"></a>gebunden: [int](xref:microsoft.quantum.lang-ref.int)

Eine Spezifikation des Bereichs, der durchlaufen werden soll, angegeben als die Länge des Bereichs.


### <a name="op--int--unit"></a>OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der für jedes Element der angegebenen kartesischen Potenz aufgerufen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. iteratequercartesianproduct](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)