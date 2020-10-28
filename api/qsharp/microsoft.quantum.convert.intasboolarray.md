---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Intasboolarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 9783a49a77bdc39ffe8c7725196eb620f4cd0100
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702960"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="0dff1-102">Intasboolarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="0dff1-102">IntAsBoolArray function</span></span>

<span data-ttu-id="0dff1-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="0dff1-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="0dff1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0dff1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0dff1-105">Erzeugt eine binäre Darstellung einer positiven ganzen Zahl unter Verwendung der Little-dendian-Darstellung für das zurückgegebene Array.</span><span class="sxs-lookup"><span data-stu-id="0dff1-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="0dff1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0dff1-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="0dff1-107">Zahl: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dff1-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dff1-108">Eine positive ganze Zahl, die in ein Array von booleschen Werten konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0dff1-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="0dff1-109">Bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0dff1-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0dff1-110">Die Anzahl der Bits in der binären Darstellung von `number` .</span><span class="sxs-lookup"><span data-stu-id="0dff1-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="0dff1-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="0dff1-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="0dff1-112">Ein Array von booleschen Werten, die darstellen `number` .</span><span class="sxs-lookup"><span data-stu-id="0dff1-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dff1-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0dff1-113">Remarks</span></span>

<span data-ttu-id="0dff1-114">Die Eingabe `bits` muss zwischen 0 und 63 liegen.</span><span class="sxs-lookup"><span data-stu-id="0dff1-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="0dff1-115">Die Eingabe `number` muss zwischen 0 und $2 ^ {\texttt{Bits}}-$1 liegen.</span><span class="sxs-lookup"><span data-stu-id="0dff1-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>