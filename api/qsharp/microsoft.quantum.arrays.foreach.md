---
uid: Microsoft.Quantum.Arrays.ForEach
title: Foreach-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705999"
---
# <a name="foreach-operation"></a><span data-ttu-id="1c5ae-102">Foreach-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1c5ae-102">ForEach operation</span></span>

<span data-ttu-id="1c5ae-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1c5ae-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1c5ae-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1c5ae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1c5ae-105">Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter dem Vorgang besteht, wenn ein Array und ein Vorgang angegeben sind, der für die Elemente des Arrays definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c5ae-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="1c5ae-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1c5ae-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="1c5ae-107">Aktion: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="1c5ae-107">action : 'T => 'U</span></span> 

<span data-ttu-id="1c5ae-108">Ein Vorgang von `'T` bis `'U` , der auf jedes Element angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c5ae-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="1c5ae-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="1c5ae-109">array : 'T[]</span></span>

<span data-ttu-id="1c5ae-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="1c5ae-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="1c5ae-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="1c5ae-111">Output : 'U[]</span></span>

<span data-ttu-id="1c5ae-112">Ein Array `'U[]` von-Elementen, die durch den-Vorgang zugeordnet werden `action` .</span><span class="sxs-lookup"><span data-stu-id="1c5ae-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1c5ae-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1c5ae-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1c5ae-114">GIF</span><span class="sxs-lookup"><span data-stu-id="1c5ae-114">'T</span></span>

<span data-ttu-id="1c5ae-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="1c5ae-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="1c5ae-116">"U</span><span class="sxs-lookup"><span data-stu-id="1c5ae-116">'U</span></span>

<span data-ttu-id="1c5ae-117">Der Ergebnistyp des `action` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="1c5ae-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c5ae-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c5ae-118">Remarks</span></span>

<span data-ttu-id="1c5ae-119">Der Vorgang ist für generische Typen definiert, d. h., wenn wir ein Array `'T[]` und einen Vorgang haben, `action : 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="1c5ae-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>