---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Withzeroinsertedat-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 7d5f8838b6ae555524fb0e82e14f93e6c77e43d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855196"
---
# <a name="withzeroinsertedat-function"></a><span data-ttu-id="8dc84-102">Withzeroinsertedat-Funktion</span><span class="sxs-lookup"><span data-stu-id="8dc84-102">WithZeroInsertedAt function</span></span>

<span data-ttu-id="8dc84-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="8dc84-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="8dc84-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8dc84-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8dc84-105">Einfügen eines 0-Bit-Wert in eine ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="8dc84-105">Insert a 0-bit into an integer</span></span>

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a><span data-ttu-id="8dc84-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8dc84-106">Description</span></span>

<span data-ttu-id="8dc84-107">Dieser Vorgang nimmt eine Ganzzahl an, fügt ein Bit 0 (null) ein `position` und gibt den aktualisierten Wert als Ganzzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="8dc84-107">This operation takes an integer, inserts a 0 at bit `position`, and returns the updated value as an integer.</span></span>  <span data-ttu-id="8dc84-108">Wenn beispielsweise 0 an Position 2 in der Zahl 10 ($10 _ {10} = 1010_ $) eingefügt wird, wird {2} die Zahl 18 (18 bis 18 _ {10} = 10010_ {2} $) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8dc84-108">For example, inserting a 0 at position 2 in the number 10 ($10_{10} = 1010_{2}$) returns the number 18 ($18_{10} = 10010_{2}$).</span></span>

## <a name="input"></a><span data-ttu-id="8dc84-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8dc84-109">Input</span></span>

### <a name="position--int"></a><span data-ttu-id="8dc84-110">Position: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8dc84-110">position : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8dc84-111">Die Position, an der 0 eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8dc84-111">The position at which 0 is inserted</span></span>


### <a name="value--int"></a><span data-ttu-id="8dc84-112">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8dc84-112">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8dc84-113">Der geänderte Wert.</span><span class="sxs-lookup"><span data-stu-id="8dc84-113">The value that is modified</span></span>



## <a name="output--int"></a><span data-ttu-id="8dc84-114">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8dc84-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8dc84-115">Geänderter Wert</span><span class="sxs-lookup"><span data-stu-id="8dc84-115">Modified value</span></span>