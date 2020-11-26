---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: 4dd10b6e8839fd906ca9c2e36c89c626d5772149
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220389"
---
# <a name="rest-function"></a><span data-ttu-id="80162-102">Rest-Funktion</span><span class="sxs-lookup"><span data-stu-id="80162-102">Rest function</span></span>

<span data-ttu-id="80162-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="80162-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="80162-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="80162-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="80162-105">Erstellt ein Array, das gleich einem Eingabe Array ist, außer dass das erste Array Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="80162-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="80162-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="80162-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="80162-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="80162-107">array : 'T[]</span></span>

<span data-ttu-id="80162-108">Ein Array, dessen zweites bis letztes Element das Ausgabe Array bilden soll.</span><span class="sxs-lookup"><span data-stu-id="80162-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="80162-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="80162-109">Output : 'T[]</span></span>

<span data-ttu-id="80162-110">Ein Array, das die Elemente enthält `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="80162-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="80162-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="80162-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="80162-112">GIF</span><span class="sxs-lookup"><span data-stu-id="80162-112">'T</span></span>

<span data-ttu-id="80162-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="80162-113">The type of the array elements.</span></span>