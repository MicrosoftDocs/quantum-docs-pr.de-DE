---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Iteratethrough cartesianpower-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 2883e7cb30633afe51d380befe806665207c5abd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206475"
---
# <a name="iteratethroughcartesianpower-operation"></a>Iteratethrough cartesianpower-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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