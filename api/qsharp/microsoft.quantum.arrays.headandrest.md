---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Headandrest-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705983"
---
# <a name="headandrest-function"></a><span data-ttu-id="f2089-102">Headandrest-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2089-102">HeadAndRest function</span></span>

<span data-ttu-id="f2089-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f2089-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f2089-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f2089-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f2089-105">Gibt ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="f2089-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="f2089-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f2089-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="f2089-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="f2089-107">array : 'A[]</span></span>

<span data-ttu-id="f2089-108">Ein Array mit mindestens einem Element.</span><span class="sxs-lookup"><span data-stu-id="f2089-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="f2089-109">Ausgabe: ("a", "a" [])</span><span class="sxs-lookup"><span data-stu-id="f2089-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="f2089-110">Ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays.</span><span class="sxs-lookup"><span data-stu-id="f2089-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f2089-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="f2089-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="f2089-112">"A</span><span class="sxs-lookup"><span data-stu-id="f2089-112">'A</span></span>

<span data-ttu-id="f2089-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="f2089-113">The type of the array elements.</span></span>