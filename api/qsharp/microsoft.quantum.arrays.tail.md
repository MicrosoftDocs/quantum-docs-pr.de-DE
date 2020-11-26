---
uid: Microsoft.Quantum.Arrays.Tail
title: Tail-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Tail
qsharp.summary: Returns the last element of the array.
ms.openlocfilehash: 7084cd8bc75f295024dce361153b58490074cdc5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220092"
---
# <a name="tail-function"></a><span data-ttu-id="fa73f-102">Tail-Funktion</span><span class="sxs-lookup"><span data-stu-id="fa73f-102">Tail function</span></span>

<span data-ttu-id="fa73f-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fa73f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fa73f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fa73f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fa73f-105">Gibt das letzte Element des Arrays zurück.</span><span class="sxs-lookup"><span data-stu-id="fa73f-105">Returns the last element of the array.</span></span>

```qsharp
function Tail<'A> (array : 'A[]) : 'A
```


## <a name="input"></a><span data-ttu-id="fa73f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fa73f-106">Input</span></span>

### <a name="array--a"></a><span data-ttu-id="fa73f-107">Array: ' A []</span><span class="sxs-lookup"><span data-stu-id="fa73f-107">array : 'A[]</span></span>

<span data-ttu-id="fa73f-108">Das Array, von dem das letzte Element entnommen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa73f-108">Array of which the last element is taken.</span></span> <span data-ttu-id="fa73f-109">Das Array muss eine Länge von mindestens 1 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fa73f-109">Array must have length at least 1.</span></span>



## <a name="output--a"></a><span data-ttu-id="fa73f-110">Ausgabe: "A</span><span class="sxs-lookup"><span data-stu-id="fa73f-110">Output : 'A</span></span>

<span data-ttu-id="fa73f-111">Das letzte Element des Arrays.</span><span class="sxs-lookup"><span data-stu-id="fa73f-111">The last element of the array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fa73f-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="fa73f-112">Type Parameters</span></span>

### <a name="a"></a><span data-ttu-id="fa73f-113">"A</span><span class="sxs-lookup"><span data-stu-id="fa73f-113">'A</span></span>

<span data-ttu-id="fa73f-114">Der Typ der Arrayelemente.</span><span class="sxs-lookup"><span data-stu-id="fa73f-114">The type of the array elements.</span></span>