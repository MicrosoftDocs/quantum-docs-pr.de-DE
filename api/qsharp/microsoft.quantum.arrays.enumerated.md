---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Enumerierte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: 94e8fdb7288bc43ed84d10a3292819b455a2be31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221418"
---
# <a name="enumerated-function"></a><span data-ttu-id="3b054-102">Enumerierte Funktion</span><span class="sxs-lookup"><span data-stu-id="3b054-102">Enumerated function</span></span>

<span data-ttu-id="3b054-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3b054-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3b054-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3b054-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3b054-105">Gibt bei Angabe eines Arrays ein neues Array zurück, das die Elemente des ursprünglichen Arrays zusammen mit den Indizes der einzelnen Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="3b054-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="3b054-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3b054-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="3b054-107">Array: ' telements []</span><span class="sxs-lookup"><span data-stu-id="3b054-107">array : 'TElement[]</span></span>

<span data-ttu-id="3b054-108">Ein Array, dessen Elemente aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3b054-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="3b054-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ' telements) []</span><span class="sxs-lookup"><span data-stu-id="3b054-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="3b054-110">Ein neues Array, das Elemente des ursprünglichen Arrays zusammen mit ihren Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="3b054-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3b054-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="3b054-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="3b054-112">' Telements '</span><span class="sxs-lookup"><span data-stu-id="3b054-112">'TElement</span></span>

<span data-ttu-id="3b054-113">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="3b054-113">The type of elements of the array.</span></span>