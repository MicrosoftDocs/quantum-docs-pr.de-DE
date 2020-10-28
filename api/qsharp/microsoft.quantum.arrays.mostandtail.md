---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: "\"Mustandtail\"-Funktion"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: 8786250cf2f78ce2e9ff8baddc856d0bc07cb9a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705858"
---
# <a name="mostandtail-function"></a><span data-ttu-id="c011a-102">"Mustandtail"-Funktion</span><span class="sxs-lookup"><span data-stu-id="c011a-102">MostAndTail function</span></span>

<span data-ttu-id="c011a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c011a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c011a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c011a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c011a-105">Gibt ein Tupel von allen bis auf ein und das letzte Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="c011a-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="c011a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c011a-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="c011a-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="c011a-107">array : 'A[]</span></span>

<span data-ttu-id="c011a-108">Ein Array mit mindestens einem Element.</span><span class="sxs-lookup"><span data-stu-id="c011a-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="c011a-109">Ausgabe: (' a [], ' a ')</span><span class="sxs-lookup"><span data-stu-id="c011a-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="c011a-110">Ein Tupel von allen bis auf ein und das letzte Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="c011a-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c011a-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c011a-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="c011a-112">"A</span><span class="sxs-lookup"><span data-stu-id="c011a-112">'A</span></span>

<span data-ttu-id="c011a-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="c011a-113">The type of the array elements.</span></span>