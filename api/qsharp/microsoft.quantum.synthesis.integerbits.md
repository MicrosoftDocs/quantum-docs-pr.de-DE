---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Integerbits-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: ab459cd841cdac116cf0e98c094834f628b6a2d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706426"
---
# <a name="integerbits-function"></a><span data-ttu-id="7941f-102">Integerbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="7941f-102">IntegerBits function</span></span>

<span data-ttu-id="7941f-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="7941f-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="7941f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7941f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7941f-105">Gibt alle Positionen zurück, in denen Bits einer Ganzzahl festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="7941f-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="7941f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7941f-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="7941f-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7941f-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7941f-108">Eine nicht negative Zahl.</span><span class="sxs-lookup"><span data-stu-id="7941f-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="7941f-109">Länge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7941f-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7941f-110">Die Anzahl der Bits in der binären Erweiterung von `value` .</span><span class="sxs-lookup"><span data-stu-id="7941f-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="7941f-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="7941f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="7941f-112">Ein Array, das alle Bitpositionen enthält (beginnend bei 0), die 1 in der binären Erweiterung von sind, in der `value` alle Bits bis zur Position berücksichtigt werden `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="7941f-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="7941f-113">Alle Positionen werden im Array nach Position in einer zunehmenden Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="7941f-113">All positions are ordered in the array by position in an increasing order.</span></span>