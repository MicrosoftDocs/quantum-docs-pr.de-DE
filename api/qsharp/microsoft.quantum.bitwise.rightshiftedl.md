---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Rightshif tedl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 3d941e1a0bcd96fe54ab01019293d883f11547a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219514"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="85f00-102">Rightshif tedl-Funktion</span><span class="sxs-lookup"><span data-stu-id="85f00-102">RightShiftedL function</span></span>

<span data-ttu-id="85f00-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="85f00-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="85f00-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="85f00-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="85f00-105">Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.</span><span class="sxs-lookup"><span data-stu-id="85f00-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="85f00-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85f00-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="85f00-107">Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="85f00-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="85f00-108">Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).</span><span class="sxs-lookup"><span data-stu-id="85f00-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="85f00-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="85f00-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="85f00-110">Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="85f00-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="85f00-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="85f00-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="85f00-112">Der Wert von `value` , nach rechts nach `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="85f00-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="85f00-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85f00-113">Remarks</span></span>

<span data-ttu-id="85f00-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="85f00-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```