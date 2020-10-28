---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: Ispermutations-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 361bb21bedc725c25a1f3dfc811e9cfda4cb45ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705935"
---
# <a name="ispermutation-function"></a><span data-ttu-id="edafc-102">Ispermutations-Funktion</span><span class="sxs-lookup"><span data-stu-id="edafc-102">IsPermutation function</span></span>

<span data-ttu-id="edafc-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="edafc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="edafc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="edafc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="edafc-105">Gibt nur dann true aus, wenn ein bestimmtes Array eine Permutation darstellt.</span><span class="sxs-lookup"><span data-stu-id="edafc-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="edafc-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edafc-106">Description</span></span>

<span data-ttu-id="edafc-107">Gibt bei Angabe eines Arrays `array` der Länge `n` nur dann true zurück, wenn jede Ganzzahl von in `0` `n - 1` genau einmal in angezeigt wird `array` , sodass `array` als permutations für Elemente interpretiert werden kann `n` .</span><span class="sxs-lookup"><span data-stu-id="edafc-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="edafc-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="edafc-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="edafc-109">permutung: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="edafc-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="edafc-110">Ein Array, das möglicherweise eine Permutation darstellt.</span><span class="sxs-lookup"><span data-stu-id="edafc-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="edafc-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="edafc-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="edafc-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edafc-112">Remarks</span></span>

<span data-ttu-id="edafc-113">Ein Array der Länge 0 (null) ist trivial eine Permutation.</span><span class="sxs-lookup"><span data-stu-id="edafc-113">An array of length zero is trivially a permutation.</span></span>