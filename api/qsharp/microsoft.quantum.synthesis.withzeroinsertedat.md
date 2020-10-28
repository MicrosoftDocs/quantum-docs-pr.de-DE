---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Withzeroinsertedat-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 6e13251741dadb19740b208cdfc13a14964a48dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725159"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="0c872-102">Withzeroinsertedat-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c872-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="0c872-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="0c872-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="0c872-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0c872-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0c872-105">Einfügen eines 0-Bit-Wert in eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="0c872-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="0c872-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c872-106">Description</span></span>

<span data-ttu-id="0c872-107">Dieser Vorgang nimmt eine Ganzzahl an, fügt ein Bit 0 (null) ein `position` und gibt den aktualisierten Wert als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="0c872-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="0c872-108">Wenn beispielsweise 0 an Position 2 in der Zahl 10 ($10 _ {10} = 1010_ $) eingefügt wird, wird {2} die Zahl 18 (18 bis 18 _ {10} = 10010_ {2} $) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0c872-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="0c872-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c872-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="0c872-110">Position: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0c872-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0c872-111">Die Position, an der 0 eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="0c872-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="0c872-112">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0c872-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0c872-113">Der geänderte Wert.</span><span class="sxs-lookup"><span data-stu-id="0c872-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="0c872-114">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0c872-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0c872-115">Geänderter Wert</span><span class="sxs-lookup"><span data-stu-id="0c872-115">Modified value</span></span>