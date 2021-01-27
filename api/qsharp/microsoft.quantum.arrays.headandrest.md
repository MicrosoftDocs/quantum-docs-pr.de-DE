---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Headandrest-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: c082e0a917343c18e5f511f065b2e78f1e217ecc
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848561"
---
# <a name="headandrest-function"></a><span data-ttu-id="87591-102">Headandrest-Funktion</span><span class="sxs-lookup"><span data-stu-id="87591-102">HeadAndRest function</span></span>

<span data-ttu-id="87591-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="87591-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="87591-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="87591-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="87591-105">Gibt ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="87591-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="87591-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="87591-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="87591-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="87591-107">array : 'A[]</span></span>

<span data-ttu-id="87591-108">Ein Array mit mindestens einem Element.</span><span class="sxs-lookup"><span data-stu-id="87591-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="87591-109">Ausgabe: ("a", "a" [])</span><span class="sxs-lookup"><span data-stu-id="87591-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="87591-110">Ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays.</span><span class="sxs-lookup"><span data-stu-id="87591-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="87591-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="87591-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="87591-112">"A</span><span class="sxs-lookup"><span data-stu-id="87591-112">'A</span></span>

<span data-ttu-id="87591-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="87591-113">The type of the array elements.</span></span>