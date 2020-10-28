---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705695"
---
# <a name="windows-function"></a><span data-ttu-id="dfdaa-102">Windows-Funktion</span><span class="sxs-lookup"><span data-stu-id="dfdaa-102">Windows function</span></span>

<span data-ttu-id="dfdaa-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dfdaa-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dfdaa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dfdaa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dfdaa-105">Gibt alle aufeinanderfolgenden Unterarrays der Länge zurück `size` .</span><span class="sxs-lookup"><span data-stu-id="dfdaa-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="dfdaa-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dfdaa-106">Description</span></span>

<span data-ttu-id="dfdaa-107">Diese Funktion gibt alle `n - size + 1` unter Elemente der Länge `size` in der Reihenfolge zurück, wobei `n` die Länge von ist `arr` .</span><span class="sxs-lookup"><span data-stu-id="dfdaa-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="dfdaa-108">Die ersten unter `arr[0..size - 1], arr[1..size], arr[2..size + 1]` Arrays liegen bis zum letzten Unterarray `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="dfdaa-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="dfdaa-109">Wenn `size <= 0` oder `size > n` , wird ein leeres Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dfdaa-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="dfdaa-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfdaa-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="dfdaa-111">Größe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dfdaa-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dfdaa-112">Länge der Unterbereiche.</span><span class="sxs-lookup"><span data-stu-id="dfdaa-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="dfdaa-113">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="dfdaa-113">array : 'T[]</span></span>

<span data-ttu-id="dfdaa-114">Ein Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="dfdaa-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="dfdaa-115">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="dfdaa-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dfdaa-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="dfdaa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dfdaa-117">GIF</span><span class="sxs-lookup"><span data-stu-id="dfdaa-117">'T</span></span>

<span data-ttu-id="dfdaa-118">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="dfdaa-118">The type of `array` elements.</span></span>