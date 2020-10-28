---
uid: Microsoft.Quantum.Arrays.Merged
title: Zusammengeführte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705871"
---
# <a name="merged-function"></a><span data-ttu-id="b2357-102">Zusammengeführte Funktion</span><span class="sxs-lookup"><span data-stu-id="b2357-102">Merged function</span></span>

<span data-ttu-id="b2357-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b2357-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b2357-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b2357-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b2357-105">Bei zwei sortierten Arrays wird ein einzelnes Array mit den Elementen beider Elemente in sortierter Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b2357-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="b2357-106">Wird intern von der Merge-Sortierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b2357-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b2357-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2357-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="b2357-108">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b2357-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="b2357-109">Left: 't []</span><span class="sxs-lookup"><span data-stu-id="b2357-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="b2357-110">Right: 't []</span><span class="sxs-lookup"><span data-stu-id="b2357-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="b2357-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="b2357-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b2357-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="b2357-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b2357-113">GIF</span><span class="sxs-lookup"><span data-stu-id="b2357-113">'T</span></span>

