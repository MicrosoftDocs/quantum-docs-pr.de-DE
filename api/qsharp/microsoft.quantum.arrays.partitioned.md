---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Partitionierte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705847"
---
# <a name="partitioned-function"></a><span data-ttu-id="1f1cd-102">Partitionierte Funktion</span><span class="sxs-lookup"><span data-stu-id="1f1cd-102">Partitioned function</span></span>

<span data-ttu-id="1f1cd-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1f1cd-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1f1cd-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1f1cd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1f1cd-105">Teilt ein Array in mehrere Teile auf.</span><span class="sxs-lookup"><span data-stu-id="1f1cd-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="1f1cd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f1cd-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="1f1cd-107">nelements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="1f1cd-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="1f1cd-108">Anzahl von Elementen in jedem Teil des Arrays</span><span class="sxs-lookup"><span data-stu-id="1f1cd-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="1f1cd-109">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="1f1cd-109">arr : 'T[]</span></span>

<span data-ttu-id="1f1cd-110">Eingabe Array, das aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f1cd-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="1f1cd-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="1f1cd-111">Output : 'T[][]</span></span>

<span data-ttu-id="1f1cd-112">Mehrere Arrays, bei denen das erste Array der `nElements[0]` erste `arr` und das zweite Array das nächste `nElements[1]` von `arr` usw. ist. Das letzte Array enthält alle verbleibenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="1f1cd-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1f1cd-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1f1cd-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1f1cd-114">GIF</span><span class="sxs-lookup"><span data-stu-id="1f1cd-114">'T</span></span>

