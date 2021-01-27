---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: Rangeasintarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: 8c6b83d78e3b22ea1a17a48de66592950bf905a3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850099"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="ff69e-102">Rangeasintarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="ff69e-102">RangeAsIntArray function</span></span>

<span data-ttu-id="ff69e-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="ff69e-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="ff69e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ff69e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ff69e-105">Erstellt ein Array von ganzen Zahlen, die `arr` nach Start. aufgelistet sind. Schritt. Schließlich.</span><span class="sxs-lookup"><span data-stu-id="ff69e-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="ff69e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff69e-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="ff69e-107">Bereich: [Bereich](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="ff69e-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="ff69e-108">Eine `Range` von Werten `start..step..end` , die in ein Array konvertiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff69e-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="ff69e-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ff69e-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ff69e-110">Ein neues Array von ganzen Zahlen, das den Werten entspricht, die durch durchlaufen werden `range` .</span><span class="sxs-lookup"><span data-stu-id="ff69e-110">A new array of integers corresponding to values iterated over by `range`.</span></span>

## <a name="example"></a><span data-ttu-id="ff69e-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff69e-111">Example</span></span>

```qsharp
// The following returns [1,3,5,7];
let array = RangeAsIntArray(1..2..8);
```