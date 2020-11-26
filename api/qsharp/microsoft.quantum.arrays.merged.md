---
uid: Microsoft.Quantum.Arrays.Merged
title: Zusammengeführte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: b3383f8a04e6fa23562aa81e5b911d06752f4fb5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220636"
---
# <a name="merged-function"></a><span data-ttu-id="47a40-102">Zusammengeführte Funktion</span><span class="sxs-lookup"><span data-stu-id="47a40-102">Merged function</span></span>

<span data-ttu-id="47a40-103">Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="47a40-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="47a40-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="47a40-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="47a40-105">Bei zwei sortierten Arrays wird ein einzelnes Array mit den Elementen beider Elemente in sortierter Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47a40-105">Given two sorted arrays, returns a single array containing the elements of both in sorted order.</span></span> <span data-ttu-id="47a40-106">Wird intern von der Merge-Sortierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="47a40-106">Used internally by merge sort.</span></span>

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="47a40-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="47a40-107">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="47a40-108">Vergleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="47a40-108">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>




### <a name="left--t"></a><span data-ttu-id="47a40-109">Left: 't []</span><span class="sxs-lookup"><span data-stu-id="47a40-109">left : 'T[]</span></span>




### <a name="right--t"></a><span data-ttu-id="47a40-110">Right: 't []</span><span class="sxs-lookup"><span data-stu-id="47a40-110">right : 'T[]</span></span>





## <a name="output--t"></a><span data-ttu-id="47a40-111">Ausgabe: 't []</span><span class="sxs-lookup"><span data-stu-id="47a40-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="47a40-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="47a40-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="47a40-113">GIF</span><span class="sxs-lookup"><span data-stu-id="47a40-113">'T</span></span>

