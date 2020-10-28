---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Enumerierte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 0a591025a4eef79e08b47527c0bdb556f5645334
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706066"
---
# <a name="enumerated-function"></a><span data-ttu-id="de62a-102">Enumerierte Funktion</span><span class="sxs-lookup"><span data-stu-id="de62a-102">Enumerated function</span></span>

<span data-ttu-id="de62a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="de62a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="de62a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="de62a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="de62a-105">Gibt bei Angabe eines Arrays ein neues Array zurück, das die Elemente des ursprünglichen Arrays zusammen mit den Indizes der einzelnen Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="de62a-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="de62a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="de62a-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="de62a-107">Array: ' telements []</span><span class="sxs-lookup"><span data-stu-id="de62a-107">array : 'TElement[]</span></span>

<span data-ttu-id="de62a-108">Ein Array, dessen Elemente aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="de62a-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="de62a-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ' telements) []</span><span class="sxs-lookup"><span data-stu-id="de62a-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="de62a-110">Ein neues Array, das Elemente des ursprünglichen Arrays zusammen mit ihren Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="de62a-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="de62a-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="de62a-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="de62a-112">' Telements '</span><span class="sxs-lookup"><span data-stu-id="de62a-112">'TElement</span></span>

<span data-ttu-id="de62a-113">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="de62a-113">The type of elements of the array.</span></span>