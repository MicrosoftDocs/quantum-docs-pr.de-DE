---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Partitionierte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220500"
---
# <a name="partitioned-function"></a><span data-ttu-id="38ca4-102">Partitionierte Funktion</span><span class="sxs-lookup"><span data-stu-id="38ca4-102">Partitioned function</span></span>

<span data-ttu-id="38ca4-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="38ca4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="38ca4-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="38ca4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="38ca4-105">Teilt ein Array in mehrere Teile auf.</span><span class="sxs-lookup"><span data-stu-id="38ca4-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="38ca4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38ca4-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="38ca4-107">nelements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="38ca4-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="38ca4-108">Anzahl von Elementen in jedem Teil des Arrays</span><span class="sxs-lookup"><span data-stu-id="38ca4-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="38ca4-109">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="38ca4-109">arr : 'T[]</span></span>

<span data-ttu-id="38ca4-110">Eingabe Array, das aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38ca4-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="38ca4-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="38ca4-111">Output : 'T[][]</span></span>

<span data-ttu-id="38ca4-112">Mehrere Arrays, bei denen das erste Array der `nElements[0]` erste `arr` und das zweite Array das nächste `nElements[1]` von `arr` usw. ist. Das letzte Array enthält alle verbleibenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="38ca4-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="38ca4-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="38ca4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="38ca4-114">GIF</span><span class="sxs-lookup"><span data-stu-id="38ca4-114">'T</span></span>

