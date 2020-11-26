---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Withzeroinsertedat-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228864"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="6a8ae-102">Withzeroinsertedat-Funktion</span><span class="sxs-lookup"><span data-stu-id="6a8ae-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="6a8ae-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="6a8ae-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="6a8ae-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a8ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a8ae-105">Einfügen eines 0-Bit-Wert in eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="6a8ae-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="6a8ae-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a8ae-106">Description</span></span>

<span data-ttu-id="6a8ae-107">Dieser Vorgang nimmt eine Ganzzahl an, fügt ein Bit 0 (null) ein `position` und gibt den aktualisierten Wert als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="6a8ae-108">Wenn beispielsweise 0 an Position 2 in der Zahl 10 ($10 _ {10} = 1010_ $) eingefügt wird, wird {2} die Zahl 18 (18 bis 18 _ {10} = 10010_ {2} $) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="6a8ae-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6a8ae-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="6a8ae-110">Position: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a8ae-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a8ae-111">Die Position, an der 0 eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="6a8ae-112">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a8ae-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a8ae-113">Der geänderte Wert.</span><span class="sxs-lookup"><span data-stu-id="6a8ae-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="6a8ae-114">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6a8ae-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6a8ae-115">Geänderter Wert</span><span class="sxs-lookup"><span data-stu-id="6a8ae-115">Modified value</span></span>