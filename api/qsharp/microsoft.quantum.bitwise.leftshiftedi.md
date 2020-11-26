---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Leftshibtedi-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3a7220489bfa241e2337df14291bafb1d6e0e19e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209858"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="baeab-102">Leftshibtedi-Funktion</span><span class="sxs-lookup"><span data-stu-id="baeab-102">LeftShiftedI function</span></span>

<span data-ttu-id="baeab-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="baeab-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="baeab-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="baeab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="baeab-105">Verschiebt die bitweise Darstellung einer Zahl nach links um eine angegebene Anzahl von Bits.</span><span class="sxs-lookup"><span data-stu-id="baeab-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="baeab-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="baeab-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="baeab-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="baeab-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="baeab-108">Die Zahl, deren bitweise Darstellung nach links verschoben werden soll (signifikanter).</span><span class="sxs-lookup"><span data-stu-id="baeab-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="baeab-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="baeab-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="baeab-110">Die Anzahl der Bits, um die `value` nach links verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="baeab-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="baeab-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="baeab-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="baeab-112">Der Wert von `value` , nach links um `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="baeab-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="baeab-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="baeab-113">Remarks</span></span>

<span data-ttu-id="baeab-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="baeab-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```