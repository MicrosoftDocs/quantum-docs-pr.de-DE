---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: adfea2b9a2f6c22446817538d29586284dba723e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842194"
---
# <a name="windows-function"></a><span data-ttu-id="37d38-102">Windows-Funktion</span><span class="sxs-lookup"><span data-stu-id="37d38-102">Windows function</span></span>

<span data-ttu-id="37d38-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="37d38-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="37d38-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37d38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37d38-105">Gibt alle aufeinanderfolgenden Unterarrays der Länge zurück `size` .</span><span class="sxs-lookup"><span data-stu-id="37d38-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="37d38-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37d38-106">Description</span></span>

<span data-ttu-id="37d38-107">Diese Funktion gibt alle `n - size + 1` unter Elemente der Länge `size` in der Reihenfolge zurück, wobei `n` die Länge von ist `arr` .</span><span class="sxs-lookup"><span data-stu-id="37d38-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="37d38-108">Die ersten unter `arr[0..size - 1], arr[1..size], arr[2..size + 1]` Arrays liegen bis zum letzten Unterarray `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="37d38-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="37d38-109">Wenn `size <= 0` oder `size > n` , wird ein leeres Array zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="37d38-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="37d38-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="37d38-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="37d38-111">Größe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="37d38-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="37d38-112">Länge der Unterbereiche.</span><span class="sxs-lookup"><span data-stu-id="37d38-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="37d38-113">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="37d38-113">array : 'T[]</span></span>

<span data-ttu-id="37d38-114">Ein Array von-Elementen.</span><span class="sxs-lookup"><span data-stu-id="37d38-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="37d38-115">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="37d38-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37d38-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="37d38-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37d38-117">GIF</span><span class="sxs-lookup"><span data-stu-id="37d38-117">'T</span></span>

<span data-ttu-id="37d38-118">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="37d38-118">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="37d38-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="37d38-119">Example</span></span>

```qsharp
// same as [[1, 2, 3], [2, 3, 4], [3, 4, 5]]
let windows = Windows(3, [1, 2, 3, 4, 5]);
```