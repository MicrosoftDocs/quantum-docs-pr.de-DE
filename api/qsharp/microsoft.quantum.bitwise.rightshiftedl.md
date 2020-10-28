---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Rightshif tedl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 2929ba58b636847257391930e1019769fd2c2580
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705578"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="0c26c-102">Rightshif tedl-Funktion</span><span class="sxs-lookup"><span data-stu-id="0c26c-102">RightShiftedL function</span></span>

<span data-ttu-id="0c26c-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="0c26c-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="0c26c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0c26c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0c26c-105">Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.</span><span class="sxs-lookup"><span data-stu-id="0c26c-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="0c26c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0c26c-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="0c26c-107">Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0c26c-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0c26c-108">Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).</span><span class="sxs-lookup"><span data-stu-id="0c26c-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="0c26c-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0c26c-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0c26c-110">Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c26c-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="0c26c-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0c26c-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0c26c-112">Der Wert von `value` , nach rechts nach `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="0c26c-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c26c-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0c26c-113">Remarks</span></span>

<span data-ttu-id="0c26c-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="0c26c-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```