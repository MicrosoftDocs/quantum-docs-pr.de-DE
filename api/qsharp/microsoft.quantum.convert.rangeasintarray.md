---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Rangeasintarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702923"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="057a3-102">Rangeasintarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="057a3-102">RangeAsIntArray function</span></span>

<span data-ttu-id="057a3-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="057a3-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="057a3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="057a3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="057a3-105">Erstellt ein Array von ganzen Zahlen, die `arr` nach Start. aufgelistet sind. Schritt. Schließlich.</span><span class="sxs-lookup"><span data-stu-id="057a3-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="057a3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="057a3-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="057a3-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="057a3-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="057a3-108">Eine `Range` von Werten `start..step..end` , die in ein Array konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="057a3-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="057a3-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="057a3-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="057a3-110">Ein neues Array von ganzen Zahlen, das den Werten entspricht, die durch durchlaufen werden `range` .</span><span class="sxs-lookup"><span data-stu-id="057a3-110">A new array of integers corresponding to values iterated over by `range`.</span></span>