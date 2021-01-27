---
uid: Microsoft.Quantum.Arrays.ForEach
title: Foreach-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: 90dd6f94408d37d2b32d82e772a482b0e69c523f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848582"
---
# <a name="foreach-operation"></a><span data-ttu-id="de84a-102">Foreach-Vorgang</span><span class="sxs-lookup"><span data-stu-id="de84a-102">ForEach operation</span></span>

<span data-ttu-id="de84a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="de84a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="de84a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="de84a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="de84a-105">Gibt ein neues Array zurück, das aus den Bildern des ursprünglichen Arrays unter dem Vorgang besteht, wenn ein Array und ein Vorgang angegeben sind, der für die Elemente des Arrays definiert ist.</span><span class="sxs-lookup"><span data-stu-id="de84a-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="de84a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="de84a-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="de84a-107">Aktion: 't => ' U</span><span class="sxs-lookup"><span data-stu-id="de84a-107">action : 'T => 'U</span></span> 

<span data-ttu-id="de84a-108">Ein Vorgang von `'T` bis `'U` , der auf jedes Element angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="de84a-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="de84a-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="de84a-109">array : 'T[]</span></span>

<span data-ttu-id="de84a-110">Ein Array von-Elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="de84a-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="de84a-111">Ausgabe: ' U []</span><span class="sxs-lookup"><span data-stu-id="de84a-111">Output : 'U[]</span></span>

<span data-ttu-id="de84a-112">Ein Array `'U[]` von-Elementen, die durch den-Vorgang zugeordnet werden `action` .</span><span class="sxs-lookup"><span data-stu-id="de84a-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="de84a-113">Typparameter</span><span class="sxs-lookup"><span data-stu-id="de84a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="de84a-114">GIF</span><span class="sxs-lookup"><span data-stu-id="de84a-114">'T</span></span>

<span data-ttu-id="de84a-115">Der Typ der `array` Elemente.</span><span class="sxs-lookup"><span data-stu-id="de84a-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="de84a-116">"U</span><span class="sxs-lookup"><span data-stu-id="de84a-116">'U</span></span>

<span data-ttu-id="de84a-117">Der Ergebnistyp des `action` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="de84a-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="de84a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de84a-118">Remarks</span></span>

<span data-ttu-id="de84a-119">Der Vorgang ist für generische Typen definiert, d. h., wenn wir ein Array `'T[]` und einen Vorgang haben, `action : 'T -> 'U` können wir die Elemente des Arrays zuordnen und ein neues Array vom Typ entwickeln `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="de84a-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>