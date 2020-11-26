---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Rightshif Tedi-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b20a4a8c281a470af9a4828f8a5ca905a7918723
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209773"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="bee3c-102">Rightshif Tedi-Funktion</span><span class="sxs-lookup"><span data-stu-id="bee3c-102">RightShiftedI function</span></span>

<span data-ttu-id="bee3c-103">Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="bee3c-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="bee3c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bee3c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bee3c-105">Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.</span><span class="sxs-lookup"><span data-stu-id="bee3c-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="bee3c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bee3c-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="bee3c-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bee3c-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bee3c-108">Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).</span><span class="sxs-lookup"><span data-stu-id="bee3c-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="bee3c-109">Betrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bee3c-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bee3c-110">Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="bee3c-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="bee3c-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bee3c-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bee3c-112">Der Wert von `value` , nach rechts nach `amount` Bits verschoben.</span><span class="sxs-lookup"><span data-stu-id="bee3c-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="bee3c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bee3c-113">Remarks</span></span>

<span data-ttu-id="bee3c-114">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="bee3c-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```