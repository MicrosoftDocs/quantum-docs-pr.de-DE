---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Leftshibtedl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 17e5c845755f74e9703381bc82bfd63be836d038
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705618"
---
# <a name="leftshiftedl-function"></a><span data-ttu-id="16cb1-102">Leftshibtedl-Funktion</span><span class="sxs-lookup"><span data-stu-id="16cb1-102">LeftShiftedL function</span></span>

<span data-ttu-id="16cb1-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="16cb1-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="16cb1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="16cb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="16cb1-105">Verschiebt die bitweise Darstellung einer Zahl nach links um eine angegebene Anzahl von Bits.</span><span class="sxs-lookup"><span data-stu-id="16cb1-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="16cb1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="16cb1-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="16cb1-107">Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="16cb1-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="16cb1-108">Die Zahl, deren bitweise Darstellung nach links verschoben werden soll (signifikanter).</span><span class="sxs-lookup"><span data-stu-id="16cb1-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="16cb1-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="16cb1-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="16cb1-110">Die Anzahl der Bits, um die `value` nach links verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="16cb1-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="16cb1-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="16cb1-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="16cb1-112">Der Wert von `value` , nach links um `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="16cb1-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="16cb1-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16cb1-113">Remarks</span></span>

<span data-ttu-id="16cb1-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="16cb1-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```