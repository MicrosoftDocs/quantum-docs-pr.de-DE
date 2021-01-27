---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Enumerierte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: adb13d8b25c9e4a6011ade119ffa3cb2783f60e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848125"
---
# <a name="enumerated-function"></a><span data-ttu-id="89315-102">Enumerierte Funktion</span><span class="sxs-lookup"><span data-stu-id="89315-102">Enumerated function</span></span>

<span data-ttu-id="89315-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="89315-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="89315-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="89315-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="89315-105">Gibt bei Angabe eines Arrays ein neues Array zurück, das die Elemente des ursprünglichen Arrays zusammen mit den Indizes der einzelnen Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="89315-105">Given an array, returns a new array containing elements of the original array along with the indices of each element.</span></span>

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a><span data-ttu-id="89315-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="89315-106">Input</span></span>

### <a name="array--telement"></a><span data-ttu-id="89315-107">Array: ' telements []</span><span class="sxs-lookup"><span data-stu-id="89315-107">array : 'TElement[]</span></span>

<span data-ttu-id="89315-108">Ein Array, dessen Elemente aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89315-108">An array whose elements are to be enumerated.</span></span>



## <a name="output--inttelement"></a><span data-ttu-id="89315-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ' telements) []</span><span class="sxs-lookup"><span data-stu-id="89315-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),'TElement)[]</span></span>

<span data-ttu-id="89315-110">Ein neues Array, das Elemente des ursprünglichen Arrays zusammen mit ihren Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="89315-110">A new array containing elements of the original array along with their indices.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="89315-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="89315-111">Type Parameters</span></span>

### <a name="telement"></a><span data-ttu-id="89315-112">' Telements '</span><span class="sxs-lookup"><span data-stu-id="89315-112">'TElement</span></span>

<span data-ttu-id="89315-113">Der Typ der Elemente des Arrays.</span><span class="sxs-lookup"><span data-stu-id="89315-113">The type of elements of the array.</span></span>

## <a name="example"></a><span data-ttu-id="89315-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="89315-114">Example</span></span>

<span data-ttu-id="89315-115">Die folgenden `for` Schleifen sind äquivalent:</span><span class="sxs-lookup"><span data-stu-id="89315-115">The following `for` loops are equivalent:</span></span>

```qsharp
for (idx in IndexRange(array)) {
    let element = array[idx];
    ...
}
for ((idx, element) in Enumerated(array)) { ... }
```