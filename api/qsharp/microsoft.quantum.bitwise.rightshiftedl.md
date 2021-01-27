---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Rightshif tedl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 03ed69c7151e62b91c4a036e301f99b45ce5ab62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842096"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="5aef8-102">Rightshif tedl-Funktion</span><span class="sxs-lookup"><span data-stu-id="5aef8-102">RightShiftedL function</span></span>

<span data-ttu-id="5aef8-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="5aef8-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="5aef8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5aef8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5aef8-105">Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.</span><span class="sxs-lookup"><span data-stu-id="5aef8-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="5aef8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5aef8-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="5aef8-107">Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5aef8-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5aef8-108">Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).</span><span class="sxs-lookup"><span data-stu-id="5aef8-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="5aef8-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5aef8-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5aef8-110">Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5aef8-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="5aef8-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="5aef8-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="5aef8-112">Der Wert von `value` , nach rechts nach `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="5aef8-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="5aef8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5aef8-113">Remarks</span></span>

<span data-ttu-id="5aef8-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="5aef8-114">The following are equivalent:</span></span>

```qsharp
let c = a >>> b;
let c = RightShiftedL(a, b);
```