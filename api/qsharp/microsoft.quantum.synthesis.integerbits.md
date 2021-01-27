---
uid: Microsoft.Quantum.Synthesis.IntegerBits
title: Integerbits-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: IntegerBits
qsharp.summary: Returns all positions in which bits of an integer are set.
ms.openlocfilehash: 3352c1b3003ee387fb03b72461fedb400e29046d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855402"
---
# <a name="integerbits-function"></a><span data-ttu-id="838c3-102">Integerbits-Funktion</span><span class="sxs-lookup"><span data-stu-id="838c3-102">IntegerBits function</span></span>

<span data-ttu-id="838c3-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="838c3-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="838c3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="838c3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="838c3-105">Gibt alle Positionen zurück, in denen Bits einer Ganzzahl festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="838c3-105">Returns all positions in which bits of an integer are set.</span></span>

```qsharp
function IntegerBits (value : Int, length : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="838c3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="838c3-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="838c3-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="838c3-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="838c3-108">Eine nicht negative Zahl.</span><span class="sxs-lookup"><span data-stu-id="838c3-108">A nonnegative number.</span></span>


### <a name="length--int"></a><span data-ttu-id="838c3-109">Länge: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="838c3-109">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="838c3-110">Die Anzahl der Bits in der binären Erweiterung von `value` .</span><span class="sxs-lookup"><span data-stu-id="838c3-110">The number of bits in the binary expansion of `value`.</span></span>



## <a name="output--int"></a><span data-ttu-id="838c3-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="838c3-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="838c3-112">Ein Array, das alle Bitpositionen enthält (beginnend bei 0), die 1 in der binären Erweiterung von sind, in der `value` alle Bits bis zur Position berücksichtigt werden `length - 1` .</span><span class="sxs-lookup"><span data-stu-id="838c3-112">An array containing all bit positions (starting from 0) that are 1 in the binary expansion of `value` considering all bits up to position `length - 1`.</span></span>  <span data-ttu-id="838c3-113">Alle Positionen werden im Array nach Position in einer zunehmenden Reihenfolge sortiert.</span><span class="sxs-lookup"><span data-stu-id="838c3-113">All positions are ordered in the array by position in an increasing order.</span></span>

## <a name="example"></a><span data-ttu-id="838c3-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="838c3-114">Example</span></span>

```qsharp
IntegerBits(23, 5); // [0, 1, 2, 4]
IntegerBits(10, 4); // [1, 3]
```