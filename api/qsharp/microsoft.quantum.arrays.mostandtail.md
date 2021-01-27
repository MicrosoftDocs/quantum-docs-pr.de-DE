---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: "\"Mustandtail\"-Funktion"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845600"
---
# <a name="mostandtail-function"></a><span data-ttu-id="aa615-102">"Mustandtail"-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa615-102">MostAndTail function</span></span>

<span data-ttu-id="aa615-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aa615-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aa615-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa615-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa615-105">Gibt ein Tupel von allen bis auf ein und das letzte Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="aa615-105">Returns a tuple of all but one and the last element of the array.</span></span>

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a><span data-ttu-id="aa615-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="aa615-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="aa615-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="aa615-107">array : 'A[]</span></span>

<span data-ttu-id="aa615-108">Ein Array mit mindestens einem Element.</span><span class="sxs-lookup"><span data-stu-id="aa615-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="aa615-109">Ausgabe: (' a [], ' a ')</span><span class="sxs-lookup"><span data-stu-id="aa615-109">Output : ('A[],'A)</span></span>

<span data-ttu-id="aa615-110">Ein Tupel von allen bis auf ein und das letzte Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="aa615-110">A tuple of all but one and the last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="aa615-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="aa615-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="aa615-112">"A</span><span class="sxs-lookup"><span data-stu-id="aa615-112">'A</span></span>

<span data-ttu-id="aa615-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="aa615-113">The type of the array elements.</span></span>