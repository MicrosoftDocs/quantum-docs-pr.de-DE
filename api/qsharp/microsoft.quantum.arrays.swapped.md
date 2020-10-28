---
uid: Microsoft.Quantum.Arrays.Swapped
title: Vertauscht Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: fa5b37b4caf5d8f19ed05075ddd7bc4217036bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705746"
---
# <a name="swapped-function"></a><span data-ttu-id="904aa-102">Vertauscht Funktion</span><span class="sxs-lookup"><span data-stu-id="904aa-102">Swapped function</span></span>

<span data-ttu-id="904aa-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="904aa-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="904aa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="904aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="904aa-105">Wendet einen Austausch zweier Elemente in einem Array an.</span><span class="sxs-lookup"><span data-stu-id="904aa-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="904aa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="904aa-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="904aa-107">firstindex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="904aa-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="904aa-108">Der Index des ersten Elements, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="904aa-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="904aa-109">secondindex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="904aa-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="904aa-110">Der Index des zweiten Elements, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="904aa-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="904aa-111">Arr: 't []</span><span class="sxs-lookup"><span data-stu-id="904aa-111">arr : 'T[]</span></span>

<span data-ttu-id="904aa-112">Array mit Elementen, die ausgetauscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="904aa-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="904aa-113">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="904aa-113">Output : 'T[]</span></span>

<span data-ttu-id="904aa-114">Das Array, für das der in-Place-Swap angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="904aa-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="904aa-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="904aa-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="904aa-116">Typparameter</span><span class="sxs-lookup"><span data-stu-id="904aa-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="904aa-117">GIF</span><span class="sxs-lookup"><span data-stu-id="904aa-117">'T</span></span>

