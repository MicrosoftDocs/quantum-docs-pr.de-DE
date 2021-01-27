---
uid: Microsoft.Quantum.Arrays.Merged
title: Zusammengeführte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: 262e7450188370212a7e2a57bf15e9f8ab162814
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845608"
---
# <a name="merged-function"></a><span data-ttu-id="ded6a-102">Zusammengeführte Funktion</span><span class="sxs-lookup"><span data-stu-id="ded6a-102">Merged function</span></span>

<span data-ttu-id="ded6a-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="ded6a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="ded6a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ded6a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ded6a-105">Bei zwei sortierten Arrays wird ein einzelnes Array mit den Elementen beider Elemente in sortierter Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ded6a-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="ded6a-106">Wird intern von der Merge-Sortierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="ded6a-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="ded6a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ded6a-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="ded6a-108">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ded6a-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="ded6a-109">Left: 't []</span><span class="sxs-lookup"><span data-stu-id="ded6a-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="ded6a-110">Right: 't []</span><span class="sxs-lookup"><span data-stu-id="ded6a-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="ded6a-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="ded6a-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ded6a-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="ded6a-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ded6a-113">GIF</span><span class="sxs-lookup"><span data-stu-id="ded6a-113">'T</span></span>

