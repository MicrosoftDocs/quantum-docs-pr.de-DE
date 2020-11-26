---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Ispermutations-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220925"
---
# <a name="ispermutation-function"></a>Ispermutations-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt nur dann true aus, wenn ein bestimmtes Array eine Permutation darstellt.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>BESCHREIBUNG

Gibt bei Angabe eines Arrays `array` der Länge `n` nur dann true zurück, wenn jede Ganzzahl von in `0` `n - 1` genau einmal in angezeigt wird `array` , sodass `array` als permutations für Elemente interpretiert werden kann `n` .

## <a name="input"></a>Eingabe

### <a name="permuation--int"></a>permutung: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das möglicherweise eine Permutation darstellt.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)



## <a name="remarks"></a>Bemerkungen

Ein Array der Länge 0 (null) ist trivial eine Permutation.