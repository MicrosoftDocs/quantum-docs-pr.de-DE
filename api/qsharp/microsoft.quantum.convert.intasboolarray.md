---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Intasboolarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a positive integer, using the little-endian representation for the returned array.
ms.openlocfilehash: f89cb3d7ca29d7deaaf49573b2670534166caded
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224342"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="0801e-102">Intasboolarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="0801e-102">IntAsBoolArray function</span></span>

<span data-ttu-id="0801e-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="0801e-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="0801e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0801e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0801e-105">Erzeugt eine binäre Darstellung einer positiven ganzen Zahl unter Verwendung der Little-dendian-Darstellung für das zurückgegebene Array.</span><span class="sxs-lookup"><span data-stu-id="0801e-105">Produces a binary representation of a positive integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="0801e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0801e-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="0801e-107">Zahl: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0801e-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0801e-108">Eine positive ganze Zahl, die in ein Array von booleschen Werten konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0801e-108">A positive integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="0801e-109">Bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0801e-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0801e-110">Die Anzahl der Bits in der binären Darstellung von `number` .</span><span class="sxs-lookup"><span data-stu-id="0801e-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="0801e-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="0801e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="0801e-112">Ein Array von booleschen Werten, die darstellen `number` .</span><span class="sxs-lookup"><span data-stu-id="0801e-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="0801e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0801e-113">Remarks</span></span>

<span data-ttu-id="0801e-114">Die Eingabe `bits` muss zwischen 0 und 63 liegen.</span><span class="sxs-lookup"><span data-stu-id="0801e-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="0801e-115">Die Eingabe `number` muss zwischen 0 und $2 ^ {\texttt{Bits}}-$1 liegen.</span><span class="sxs-lookup"><span data-stu-id="0801e-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>