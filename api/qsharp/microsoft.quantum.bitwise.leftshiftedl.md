---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Leftshibtedl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 014653011574d0fabb4b9aa04cedf58b87ddf798
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842144"
---
# <a name="leftshiftedl-function"></a><span data-ttu-id="2bd08-102">Leftshibtedl-Funktion</span><span class="sxs-lookup"><span data-stu-id="2bd08-102">LeftShiftedL function</span></span>

<span data-ttu-id="2bd08-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="2bd08-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="2bd08-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2bd08-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2bd08-105">Verschiebt die bitweise Darstellung einer Zahl nach links um eine angegebene Anzahl von Bits.</span><span class="sxs-lookup"><span data-stu-id="2bd08-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="2bd08-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2bd08-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="2bd08-107">Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2bd08-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2bd08-108">Die Zahl, deren bitweise Darstellung nach links verschoben werden soll (signifikanter).</span><span class="sxs-lookup"><span data-stu-id="2bd08-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="2bd08-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2bd08-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2bd08-110">Die Anzahl der Bits, um die `value` nach links verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="2bd08-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="2bd08-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2bd08-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2bd08-112">Der Wert von `value` , nach links um `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="2bd08-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd08-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2bd08-113">Remarks</span></span>

<span data-ttu-id="2bd08-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="2bd08-114">The following are equivalent:</span></span>

```qsharp
let c = a <<< b;
let c = LeftShiftedL(a, b);
```