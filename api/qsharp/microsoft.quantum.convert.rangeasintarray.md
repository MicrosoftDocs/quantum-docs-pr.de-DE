---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Rangeasintarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: f756e42aef7dc600e1fc6943a02513ac791f2320
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214006"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="6bca2-102">Rangeasintarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="6bca2-102">RangeAsIntArray function</span></span>

<span data-ttu-id="6bca2-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="6bca2-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="6bca2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6bca2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6bca2-105">Erstellt ein Array von ganzen Zahlen, die `arr` nach Start. aufgelistet sind. Schritt. Schließlich.</span><span class="sxs-lookup"><span data-stu-id="6bca2-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="6bca2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6bca2-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="6bca2-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="6bca2-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="6bca2-108">Eine `Range` von Werten `start..step..end` , die in ein Array konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6bca2-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="6bca2-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6bca2-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6bca2-110">Ein neues Array von ganzen Zahlen, das den Werten entspricht, die durch durchlaufen werden `range` .</span><span class="sxs-lookup"><span data-stu-id="6bca2-110">A new array of integers corresponding to values iterated over by `range`.</span></span>