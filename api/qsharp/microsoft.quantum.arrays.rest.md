---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: c14e4b2902741d7ea70c895aa715cbcaa849af3e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705807"
---
# <a name="rest-function"></a><span data-ttu-id="84ebc-102">Rest-Funktion</span><span class="sxs-lookup"><span data-stu-id="84ebc-102">Rest function</span></span>

<span data-ttu-id="84ebc-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="84ebc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="84ebc-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84ebc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84ebc-105">Erstellt ein Array, das gleich einem Eingabe Array ist, außer dass das erste Array Element gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="84ebc-105">Creates an array that is equal to an input array except that the first array element is dropped.</span></span>

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="84ebc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84ebc-106">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="84ebc-107">Array: 't []</span><span class="sxs-lookup"><span data-stu-id="84ebc-107">array : 'T[]</span></span>

<span data-ttu-id="84ebc-108">Ein Array, dessen zweites bis letztes Element das Ausgabe Array bilden soll.</span><span class="sxs-lookup"><span data-stu-id="84ebc-108">An array whose second to last elements are to form the output array.</span></span>



## <a name="output--t"></a><span data-ttu-id="84ebc-109">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="84ebc-109">Output : 'T[]</span></span>

<span data-ttu-id="84ebc-110">Ein Array, das die Elemente enthält `array[1..Length(array) - 1]` .</span><span class="sxs-lookup"><span data-stu-id="84ebc-110">An array containing the elements `array[1..Length(array) - 1]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="84ebc-111">Typparameter</span><span class="sxs-lookup"><span data-stu-id="84ebc-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="84ebc-112">GIF</span><span class="sxs-lookup"><span data-stu-id="84ebc-112">'T</span></span>

<span data-ttu-id="84ebc-113">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="84ebc-113">The type of the array elements.</span></span>