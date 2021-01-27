---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Ispermutations-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848094"
---
# <a name="ispermutation-function"></a>Ispermutations-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt nur dann true aus, wenn ein bestimmtes Array eine Permutation darstellt.

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a>Beschreibung

Gibt bei Angabe eines Arrays `array` der Länge `n` nur dann true zurück, wenn jede Ganzzahl von in `0` `n - 1` genau einmal in angezeigt wird `array` , sodass `array` als permutations für Elemente interpretiert werden kann `n` .

## <a name="input"></a>Eingabe

### <a name="permuation--int"></a>permutung: [int](xref:microsoft.quantum.lang-ref.int)[]

Ein Array, das möglicherweise eine Permutation darstellt.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)



## <a name="example"></a>Beispiel

Der folgende f #-Code gibt die Meldung "alle Diagnosen erfolgreich abgeschlossen" aus:

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a>Bemerkungen

Ein Array der Länge 0 (null) ist trivial eine Permutation.