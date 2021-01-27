---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Iteratethrough cartesianpower-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840294"
---
# <a name="iteratethroughcartesianpower-operation"></a>Iteratethrough cartesianpower-Vorgang

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Vorgang für jeden Index in der kartesischen Potenz eines ganzzahligen Bereichs an.

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Beschreibung

Wendet iterativ einen Vorgang für jedes Element einer kartesischen Potenz des Bereichs an `0..(bound - 1)` .

## <a name="input"></a>Eingabe

### <a name="power--int"></a>Power: [int](xref:microsoft.quantum.lang-ref.int)

Die kartesische Potenz, in die der Bereich `0..(bound - 1)` ausgelöst werden soll.


### <a name="bound--int"></a>gebunden: [int](xref:microsoft.quantum.lang-ref.int)

Eine Spezifikation des Bereichs, der durchlaufen werden soll, angegeben als die Länge des Bereichs.


### <a name="op--int--unit"></a>OP: [int](xref:microsoft.quantum.lang-ref.int)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit) 

Ein Vorgang, der für jedes Element der angegebenen kartesischen Potenz aufgerufen werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Beispiel

Bei einem Vorgang `op` sind die folgenden beiden Code Ausschnitte äquivalent:

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Canon. iteratequercartesianproduct](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)