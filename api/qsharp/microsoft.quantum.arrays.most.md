---
uid: Microsoft.Quantum.Arrays.Most
title: Most-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: 2b212b38ec55f3798eb9397f03b842573173eb88
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845582"
---
# <a name="most-function"></a><span data-ttu-id="b2237-102">Most-Funktion</span><span class="sxs-lookup"><span data-stu-id="b2237-102">Most function</span></span>

<span data-ttu-id="b2237-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b2237-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b2237-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2237-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2237-105">Erstellt ein Array, das gleich einem Eingabe Array ist, mit dem Unterschied, dass das letzte Array Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b2237-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b2237-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2237-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="b2237-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="b2237-107">array : 'T[]</span></span>

<span data-ttu-id="b2237-108">Ein Array, dessen erstes bis zu letztes Element das Ausgabe Array bilden soll.</span><span class="sxs-lookup"><span data-stu-id="b2237-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="b2237-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="b2237-109">Output : 'T[]</span></span>

<span data-ttu-id="b2237-110">Ein Array, das die Elemente enthält `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="b2237-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b2237-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b2237-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b2237-112">GIF</span><span class="sxs-lookup"><span data-stu-id="b2237-112">'T</span></span>

<span data-ttu-id="b2237-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="b2237-113">The type of the array elements.</span></span>