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
# <a name="ispermutation-function"></a><span data-ttu-id="1a151-102">Ispermutations-Funktion</span><span class="sxs-lookup"><span data-stu-id="1a151-102">IsPermutation function</span></span>

<span data-ttu-id="1a151-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1a151-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1a151-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1a151-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1a151-105">Gibt nur dann true aus, wenn ein bestimmtes Array eine Permutation darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a151-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="1a151-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a151-106">Description</span></span>

<span data-ttu-id="1a151-107">Gibt bei Angabe eines Arrays `array` der Länge `n` nur dann true zurück, wenn jede Ganzzahl von in `0` `n - 1` genau einmal in angezeigt wird `array` , sodass `array` als permutations für Elemente interpretiert werden kann `n` .</span><span class="sxs-lookup"><span data-stu-id="1a151-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="1a151-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a151-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="1a151-109">permutung: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1a151-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1a151-110">Ein Array, das möglicherweise eine Permutation darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a151-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1a151-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1a151-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="example"></a><span data-ttu-id="1a151-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1a151-112">Example</span></span>

<span data-ttu-id="1a151-113">Der folgende f #-Code gibt die Meldung "alle Diagnosen erfolgreich abgeschlossen" aus:</span><span class="sxs-lookup"><span data-stu-id="1a151-113">The following Q# code prints the message "All diagnostics completed successfully":</span></span>

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a><span data-ttu-id="1a151-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a151-114">Remarks</span></span>

<span data-ttu-id="1a151-115">Ein Array der Länge 0 (null) ist trivial eine Permutation.</span><span class="sxs-lookup"><span data-stu-id="1a151-115">An array of length zero is trivially a permutation.</span></span>