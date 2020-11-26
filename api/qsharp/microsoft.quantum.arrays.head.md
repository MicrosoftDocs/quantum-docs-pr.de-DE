---
uid: Microsoft.Quantum.Arrays.Head
title: Head-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Head
qsharp.summary: Returns the first element of the array.
ms.openlocfilehash: 834cbe2384122463be6a0efcb6e09785aae9c092
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221112"
---
# <a name="head-function"></a><span data-ttu-id="b62b0-102">Head-Funktion</span><span class="sxs-lookup"><span data-stu-id="b62b0-102">Head function</span></span>

<span data-ttu-id="b62b0-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b62b0-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b62b0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b62b0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b62b0-105">Gibt das erste Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="b62b0-105">Returns the first element of the array.</span></span>

```qsharp
function Head<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="b62b0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b62b0-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="b62b0-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="b62b0-107">array : 'A[]</span></span>

<span data-ttu-id="b62b0-108">Ein Array, dessen erstes Element angenommen wird.</span><span class="sxs-lookup"><span data-stu-id="b62b0-108">Array of which the first element is taken.</span></span> <span data-ttu-id="b62b0-109">Das Array muss eine Länge von mindestens 1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b62b0-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="b62b0-110">Ausgabe: "A</span><span class="sxs-lookup"><span data-stu-id="b62b0-110">Output : 'A</span></span>

<span data-ttu-id="b62b0-111">Das erste Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="b62b0-111">The first element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b62b0-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b62b0-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="b62b0-113">"A</span><span class="sxs-lookup"><span data-stu-id="b62b0-113">'A</span></span>

<span data-ttu-id="b62b0-114">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="b62b0-114">The type of the array elements.</span></span>