---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Leftshibtedi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: ce68311adf211169c2fb499bb189332370a6d6ac
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705639"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="31305-102">Leftshibtedi-Funktion</span><span class="sxs-lookup"><span data-stu-id="31305-102">LeftShiftedI function</span></span>

<span data-ttu-id="31305-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="31305-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="31305-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="31305-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="31305-105">Verschiebt die bitweise Darstellung einer Zahl nach links um eine angegebene Anzahl von Bits.</span><span class="sxs-lookup"><span data-stu-id="31305-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="31305-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="31305-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="31305-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31305-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31305-108">Die Zahl, deren bitweise Darstellung nach links verschoben werden soll (signifikanter).</span><span class="sxs-lookup"><span data-stu-id="31305-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="31305-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31305-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31305-110">Die Anzahl der Bits, um die `value` nach links verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="31305-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="31305-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="31305-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="31305-112">Der Wert von `value` , nach links um `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="31305-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="31305-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31305-113">Remarks</span></span>

<span data-ttu-id="31305-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="31305-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```