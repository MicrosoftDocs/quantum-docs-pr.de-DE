---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: "\"Mustandtail\"-Funktion"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 392efb20e4aaba80a77664444bb415d8bc9b0930
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220568"
---
# <a name="mostandtail-function"></a><span data-ttu-id="20ea5-102">"Mustandtail"-Funktion</span><span class="sxs-lookup"><span data-stu-id="20ea5-102">MostAndTail function</span></span>

<span data-ttu-id="20ea5-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="20ea5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="20ea5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="20ea5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="20ea5-105">Gibt ein Tupel von allen bis auf ein und das letzte Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="20ea5-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="20ea5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20ea5-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="20ea5-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="20ea5-107">array : 'A[]</span></span>

<span data-ttu-id="20ea5-108">Ein Array mit mindestens einem Element.</span><span class="sxs-lookup"><span data-stu-id="20ea5-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="20ea5-109">Ausgabe: (' a [], ' a ')</span><span class="sxs-lookup"><span data-stu-id="20ea5-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="20ea5-110">Ein Tupel von allen bis auf ein und das letzte Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="20ea5-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="20ea5-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="20ea5-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="20ea5-112">"A</span><span class="sxs-lookup"><span data-stu-id="20ea5-112">'A</span></span>

<span data-ttu-id="20ea5-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="20ea5-113">The type of the array elements.</span></span>