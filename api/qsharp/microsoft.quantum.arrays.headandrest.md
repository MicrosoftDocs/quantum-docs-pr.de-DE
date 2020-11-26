---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: Headandrest-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221078"
---
# <a name="headandrest-function"></a><span data-ttu-id="e1a41-102">Headandrest-Funktion</span><span class="sxs-lookup"><span data-stu-id="e1a41-102">HeadAndRest function</span></span>

<span data-ttu-id="e1a41-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e1a41-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e1a41-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e1a41-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e1a41-105">Gibt ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="e1a41-105">Returns a tuple of first and all remaining elements of the array.</span></span>

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a><span data-ttu-id="e1a41-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e1a41-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="e1a41-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="e1a41-107">array : 'A[]</span></span>

<span data-ttu-id="e1a41-108">Ein Array mit mindestens einem Element.</span><span class="sxs-lookup"><span data-stu-id="e1a41-108">An array with at least one element.</span></span>



## <a name="output--aa"></a><span data-ttu-id="e1a41-109">Ausgabe: ("a", "a" [])</span><span class="sxs-lookup"><span data-stu-id="e1a41-109">Output : ('A,'A[])</span></span>

<span data-ttu-id="e1a41-110">Ein Tupel mit dem ersten und allen verbleibenden Elementen des Arrays.</span><span class="sxs-lookup"><span data-stu-id="e1a41-110">A tuple of first and all remaining elements of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e1a41-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="e1a41-111">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="e1a41-112">"A</span><span class="sxs-lookup"><span data-stu-id="e1a41-112">'A</span></span>

<span data-ttu-id="e1a41-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="e1a41-113">The type of the array elements.</span></span>