---
uid: Microsoft.Quantum.Arrays.ForEach
title: Foreach-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: b362d28e77c8dea2b3daeed4a4d605e1dd42e487
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221146"
---
# <a name="foreach-operation"></a><span data-ttu-id="a3d23-102">Foreach-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a3d23-102">ForEach operation</span></span>

<span data-ttu-id="a3d23-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a3d23-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a3d23-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3d23-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3d23-105">Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter dem Vorgang besteht, wenn ein Array und ein Vorgang angegeben sind, der für die Elemente des Arrays definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a3d23-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="a3d23-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3d23-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="a3d23-107">Aktion: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="a3d23-107">action : 'T => 'U</span></span> 

<span data-ttu-id="a3d23-108">Ein Vorgang von `'T` bis `'U` , der auf jedes Element angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3d23-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="a3d23-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="a3d23-109">array : 'T[]</span></span>

<span data-ttu-id="a3d23-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="a3d23-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="a3d23-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="a3d23-111">Output : 'U[]</span></span>

<span data-ttu-id="a3d23-112">Ein Array `'U[]` von-Elementen, die durch den-Vorgang zugeordnet werden `action` .</span><span class="sxs-lookup"><span data-stu-id="a3d23-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a3d23-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="a3d23-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a3d23-114">GIF</span><span class="sxs-lookup"><span data-stu-id="a3d23-114">'T</span></span>

<span data-ttu-id="a3d23-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="a3d23-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="a3d23-116">"U</span><span class="sxs-lookup"><span data-stu-id="a3d23-116">'U</span></span>

<span data-ttu-id="a3d23-117">Der Ergebnistyp des `action` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="a3d23-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d23-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3d23-118">Remarks</span></span>

<span data-ttu-id="a3d23-119">Der Vorgang ist für generische Typen definiert, d. h., wenn wir ein Array `'T[]` und einen Vorgang haben, `action : 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="a3d23-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>