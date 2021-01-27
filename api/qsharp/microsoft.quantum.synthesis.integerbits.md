---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Integerbits-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855402"
---
# <a name="integerbits-function"></a>Integerbits-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt alle Positionen zurück, in denen Bits einer Ganzzahl festgelegt sind.

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)

Eine nicht negative Zahl.


### <a name="length--int"></a>Länge: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits in der binären Erweiterung von `value` .



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das alle Bitpositionen enthält (beginnend bei 0), die 1 in der binären Erweiterung von sind, in der `value` alle Bits bis zur Position berücksichtigt werden `length - 1` .  Alle Positionen werden im Array nach Position in einer zunehmenden Reihenfolge sortiert.

## <a name="example"></a>Beispiel

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```