---
uid: Microsoft.Quantum.Arrays.Most
title: Most-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Most
qsharp.summary: Creates an array that is equal to an input array except that the last array element is dropped.
ms.openlocfilehash: ca89041a4e70472e9bf7a63ffcacccb35aad527c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705863"
---
# <a name="most-function"></a><span data-ttu-id="bdfea-102">Most-Funktion</span><span class="sxs-lookup"><span data-stu-id="bdfea-102">Most function</span></span>

<span data-ttu-id="bdfea-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bdfea-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bdfea-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bdfea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bdfea-105">Erstellt ein Array, das gleich einem Eingabe Array ist, mit dem Unterschied, dass das letzte Array Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="bdfea-105">Creates an array that is equal to an input array except that the last array element is dropped.</span></span>

```qsharp
function Most<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="bdfea-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bdfea-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="bdfea-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="bdfea-107">array : 'T[]</span></span>

<span data-ttu-id="bdfea-108">Ein Array, dessen erstes bis zu letztes Element das Ausgabe Array bilden soll.</span><span class="sxs-lookup"><span data-stu-id="bdfea-108">An array whose first to second-to-last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="bdfea-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="bdfea-109">Output : 'T[]</span></span>

<span data-ttu-id="bdfea-110">Ein Array, das die Elemente enthält `array[0..Length(array) - 2]` .</span><span class="sxs-lookup"><span data-stu-id="bdfea-110">An array containing the elements `array[0..Length(array) - 2]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bdfea-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="bdfea-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bdfea-112">GIF</span><span class="sxs-lookup"><span data-stu-id="bdfea-112">'T</span></span>

<span data-ttu-id="bdfea-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="bdfea-113">The type of the array elements.</span></span>