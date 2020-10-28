---
uid: Microsoft.Quantum.Arrays.Head
title: Head-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 7b26a9c414ab2caad70f96f3c26c2d1cf0b03e95
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705986"
---
# <a name="head-function"></a><span data-ttu-id="88067-102">Head-Funktion</span><span class="sxs-lookup"><span data-stu-id="88067-102">Head function</span></span>

<span data-ttu-id="88067-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="88067-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="88067-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="88067-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="88067-105">Gibt das erste Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="88067-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="88067-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="88067-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="88067-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="88067-107">array : 'A[]</span></span>

<span data-ttu-id="88067-108">Ein Array, dessen erstes Element angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="88067-108">Array of which the first element is taken.</span></span> <span data-ttu-id="88067-109">Das Array muss eine Länge von mindestens 1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="88067-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="88067-110">Ausgabe: "A</span><span class="sxs-lookup"><span data-stu-id="88067-110">Output : 'A</span></span>

<span data-ttu-id="88067-111">Das erste Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="88067-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="88067-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="88067-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="88067-113">"A</span><span class="sxs-lookup"><span data-stu-id="88067-113">'A</span></span>

<span data-ttu-id="88067-114">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="88067-114">The type of the array elements.</span></span>