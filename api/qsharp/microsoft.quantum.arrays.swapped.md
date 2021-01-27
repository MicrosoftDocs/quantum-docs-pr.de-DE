---
uid: Microsoft.Quantum.Arrays.Swapped
title: Vertauscht Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: 575d6b76e52f198d91ab5557ada8032df491cfa3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850955"
---
# <a name="swapped-function"></a><span data-ttu-id="afa20-102">Vertauscht Funktion</span><span class="sxs-lookup"><span data-stu-id="afa20-102">Swapped function</span></span>

<span data-ttu-id="afa20-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="afa20-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="afa20-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="afa20-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="afa20-105">Wendet einen Austausch zweier Elemente in einem Array an.</span><span class="sxs-lookup"><span data-stu-id="afa20-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="afa20-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="afa20-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="afa20-107">firstindex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="afa20-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="afa20-108">Der Index des ersten Elements, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="afa20-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="afa20-109">secondindex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="afa20-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="afa20-110">Der Index des zweiten Elements, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="afa20-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="afa20-111">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="afa20-111">arr : 'T[]</span></span>

<span data-ttu-id="afa20-112">Array mit Elementen, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="afa20-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="afa20-113">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="afa20-113">Output : 'T[]</span></span>

<span data-ttu-id="afa20-114">Das Array, für das der in-Place-Swap angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="afa20-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="afa20-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="afa20-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="afa20-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="afa20-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="afa20-117">GIF</span><span class="sxs-lookup"><span data-stu-id="afa20-117">'T</span></span>

