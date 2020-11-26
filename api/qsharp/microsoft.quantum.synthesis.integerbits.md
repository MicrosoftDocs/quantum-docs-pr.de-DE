---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Integerbits-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: d6566716f5a63c090668d9582b7b000c16d1f6a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231091"
---
# <a name="integerbits-function"></a><span data-ttu-id="ba9f7-102">Integerbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="ba9f7-102">IntegerBits function</span></span>

<span data-ttu-id="ba9f7-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="ba9f7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="ba9f7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba9f7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba9f7-105">Gibt alle Positionen zurück, in denen Bits einer Ganzzahl festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ba9f7-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="ba9f7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ba9f7-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="ba9f7-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ba9f7-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ba9f7-108">Eine nicht negative Zahl.</span><span class="sxs-lookup"><span data-stu-id="ba9f7-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="ba9f7-109">Länge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ba9f7-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ba9f7-110">Die Anzahl der Bits in der binären Erweiterung von `value` .</span><span class="sxs-lookup"><span data-stu-id="ba9f7-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="ba9f7-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ba9f7-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ba9f7-112">Ein Array, das alle Bitpositionen enthält (beginnend bei 0), die 1 in der binären Erweiterung von sind, in der `value` alle Bits bis zur Position berücksichtigt werden `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="ba9f7-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="ba9f7-113">Alle Positionen werden im Array nach Position in einer zunehmenden Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="ba9f7-113">All positions are ordered in the array by position in an increasing order.</span></span>