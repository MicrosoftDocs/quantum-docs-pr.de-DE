---
uid: Microsoft.Quantum.Arrays.EqualA
title: Equala-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706055"
---
# <a name="equala-function"></a><span data-ttu-id="d80a8-102">Equala-Funktion</span><span class="sxs-lookup"><span data-stu-id="d80a8-102">EqualA function</span></span>

<span data-ttu-id="d80a8-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d80a8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d80a8-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d80a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d80a8-105">Überprüft zwei Arrays desselben Typs und ein Prädikat, das für Paare von Elementen der Arrays definiert ist, und überprüft, ob die Arrays gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d80a8-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="d80a8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d80a8-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="d80a8-107">gleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d80a8-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d80a8-108">Eine Funktion von Tupel `('T, 'T)` auf `Bool` , die verwendet wird, um zu überprüfen, ob zwei Elemente von Arrays gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d80a8-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="d80a8-109">array1: 't []</span><span class="sxs-lookup"><span data-stu-id="d80a8-109">array1 : 'T[]</span></span>

<span data-ttu-id="d80a8-110">Das erste Array, das verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d80a8-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="d80a8-111">array2: 't []</span><span class="sxs-lookup"><span data-stu-id="d80a8-111">array2 : 'T[]</span></span>

<span data-ttu-id="d80a8-112">Das zweite Array, das verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d80a8-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d80a8-113">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d80a8-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d80a8-114">Der `true` -Wert nur dann, wenn `array1` und `array2` gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d80a8-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="d80a8-115">Das heißt, wenn beide Arrays die gleiche Länge aufweisen und alle Elemente gleich sind, wie von definiert `equal` .</span><span class="sxs-lookup"><span data-stu-id="d80a8-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d80a8-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="d80a8-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d80a8-117">GIF</span><span class="sxs-lookup"><span data-stu-id="d80a8-117">'T</span></span>

<span data-ttu-id="d80a8-118">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="d80a8-118">The type of each array's elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="d80a8-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d80a8-119">Remarks</span></span>

<span data-ttu-id="d80a8-120">Diese Funktion ist für generische Typen definiert. Wenn also zwei Arrays `'T[]` und eine Funktion vorhanden sind `equal: ('T, 'T) -> Bool` , gibt diese Funktion einen Wert zurück, `Bool` der angibt, ob die Arrays gleich sind.</span><span class="sxs-lookup"><span data-stu-id="d80a8-120">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="d80a8-121">Damit zwei Arrays als gleich betrachtet werden, müssen Sie die gleiche Länge aufweisen, und die Elemente an denselben Positionen in den Arrays müssen gleich sein.</span><span class="sxs-lookup"><span data-stu-id="d80a8-121">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>