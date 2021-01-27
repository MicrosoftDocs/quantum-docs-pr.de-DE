---
uid: Microsoft.Quantum.Convert.IntAsBoolArray
title: Intasboolarray-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: IntAsBoolArray
qsharp.summary: Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.
ms.openlocfilehash: 8b3d230605cc756a5da01e45e47f91c5b8e9f541
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98833306"
---
# <a name="intasboolarray-function"></a><span data-ttu-id="7a54c-102">Intasboolarray-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a54c-102">IntAsBoolArray function</span></span>

<span data-ttu-id="7a54c-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="7a54c-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="7a54c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7a54c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7a54c-105">Erzeugt eine binäre Darstellung einer nicht negativen ganzen Zahl unter Verwendung der Little-dendian-Darstellung für das zurückgegebene Array.</span><span class="sxs-lookup"><span data-stu-id="7a54c-105">Produces a binary representation of a non-negative integer, using the little-endian representation for the returned array.</span></span>

```qsharp
function IntAsBoolArray (number : Int, bits : Int) : Bool[]
```


## <a name="input"></a><span data-ttu-id="7a54c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7a54c-106">Input</span></span>

### <a name="number--int"></a><span data-ttu-id="7a54c-107">Zahl: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a54c-107">number : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a54c-108">Eine nicht negative ganze Zahl, die in ein Array von booleschen Werten konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a54c-108">A non-negative integer to be converted to an array of boolean values.</span></span>


### <a name="bits--int"></a><span data-ttu-id="7a54c-109">Bits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a54c-109">bits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a54c-110">Die Anzahl der Bits in der binären Darstellung von `number` .</span><span class="sxs-lookup"><span data-stu-id="7a54c-110">The number of bits in the binary representation of `number`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7a54c-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="7a54c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="7a54c-112">Ein Array von booleschen Werten, die darstellen `number` .</span><span class="sxs-lookup"><span data-stu-id="7a54c-112">An array of boolean values representing `number`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a54c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a54c-113">Remarks</span></span>

<span data-ttu-id="7a54c-114">Die Eingabe `bits` muss zwischen 0 und 63 liegen.</span><span class="sxs-lookup"><span data-stu-id="7a54c-114">The input `bits` must be between 0 and 63.</span></span>
<span data-ttu-id="7a54c-115">Die Eingabe `number` muss zwischen 0 und $2 ^ {\texttt{Bits}}-$1 liegen.</span><span class="sxs-lookup"><span data-stu-id="7a54c-115">The input `number` must be between 0 and $2^{\texttt{bits}} - 1$.</span></span>