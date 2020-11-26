---
uid: Microsoft.Quantum.Arrays.ElementsAt
title: Elementsat-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementsAt
qsharp.summary: Returns the array's elements at a given range of indices.
ms.openlocfilehash: 83b5e97085234e8249869f858400cba265d13058
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221452"
---
# <a name="elementsat-function"></a><span data-ttu-id="1be21-102">Elementsat-Funktion</span><span class="sxs-lookup"><span data-stu-id="1be21-102">ElementsAt function</span></span>

<span data-ttu-id="1be21-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1be21-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1be21-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1be21-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1be21-105">Gibt die Elemente des Arrays in einem angegebenen Bereich von Indizes zurück.</span><span class="sxs-lookup"><span data-stu-id="1be21-105">Returns the array's elements at a given range of indices.</span></span>

```qsharp
function ElementsAt<'T> (range : Range, array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="1be21-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1be21-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="1be21-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="1be21-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="1be21-108">Bereich von Array Indizes</span><span class="sxs-lookup"><span data-stu-id="1be21-108">Range of array indexes</span></span>


### <a name="array--t"></a><span data-ttu-id="1be21-109">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="1be21-109">array : 'T[]</span></span>

<span data-ttu-id="1be21-110">Array</span><span class="sxs-lookup"><span data-stu-id="1be21-110">Array</span></span>



## <a name="output--t"></a><span data-ttu-id="1be21-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="1be21-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1be21-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="1be21-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1be21-113">GIF</span><span class="sxs-lookup"><span data-stu-id="1be21-113">'T</span></span>

<span data-ttu-id="1be21-114">Der Typ der einzelnen Elemente von `array` .</span><span class="sxs-lookup"><span data-stu-id="1be21-114">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1be21-115">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1be21-115">See Also</span></span>

- [<span data-ttu-id="1be21-116">Microsoft. Quantum. Arrays. ElementAt</span><span class="sxs-lookup"><span data-stu-id="1be21-116">Microsoft.Quantum.Arrays.ElementAt</span></span>](xref:Microsoft.Quantum.Arrays.ElementAt)
- [<span data-ttu-id="1be21-117">Microsoft. Quantum. Arrays. lookupfunction</span><span class="sxs-lookup"><span data-stu-id="1be21-117">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)