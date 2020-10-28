---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Rightshif Tedi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b0ca7d3cb84c58429e9b3a29893a6140a717006b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705583"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="24b5b-102">Rightshif Tedi-Funktion</span><span class="sxs-lookup"><span data-stu-id="24b5b-102">RightShiftedI function</span></span>

<span data-ttu-id="24b5b-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="24b5b-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="24b5b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24b5b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24b5b-105">Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.</span><span class="sxs-lookup"><span data-stu-id="24b5b-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="24b5b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="24b5b-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="24b5b-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24b5b-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24b5b-108">Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).</span><span class="sxs-lookup"><span data-stu-id="24b5b-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="24b5b-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24b5b-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24b5b-110">Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="24b5b-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="24b5b-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="24b5b-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="24b5b-112">Der Wert von `value` , nach rechts nach `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="24b5b-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="24b5b-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24b5b-113">Remarks</span></span>

<span data-ttu-id="24b5b-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="24b5b-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```