---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Integerbits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706426"
---
# <a name="integerbits-function"></a>Integerbits-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)


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