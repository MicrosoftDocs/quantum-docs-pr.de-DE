---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Partitionierte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845537"
---
# <a name="partitioned-function"></a><span data-ttu-id="40219-102">Partitionierte Funktion</span><span class="sxs-lookup"><span data-stu-id="40219-102">Partitioned function</span></span>

<span data-ttu-id="40219-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="40219-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="40219-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40219-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40219-105">Teilt ein Array in mehrere Teile auf.</span><span class="sxs-lookup"><span data-stu-id="40219-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="40219-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="40219-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="40219-107">nelements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="40219-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="40219-108">Anzahl von Elementen in jedem Teil des Arrays</span><span class="sxs-lookup"><span data-stu-id="40219-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="40219-109">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="40219-109">arr : 'T[]</span></span>

<span data-ttu-id="40219-110">Eingabe Array, das aufgeteilt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40219-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="40219-111">Ausgabe: 't [] []</span><span class="sxs-lookup"><span data-stu-id="40219-111">Output : 'T[][]</span></span>

<span data-ttu-id="40219-112">Mehrere Arrays, bei denen das erste Array der `nElements[0]` erste `arr` und das zweite Array das nächste `nElements[1]` von `arr` usw. ist. Das letzte Array enthält alle verbleibenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="40219-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="40219-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="40219-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="40219-114">GIF</span><span class="sxs-lookup"><span data-stu-id="40219-114">'T</span></span>



## <a name="example"></a><span data-ttu-id="40219-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="40219-115">Example</span></span>

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```