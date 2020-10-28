---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Assertphas;than-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: d003d83a84356ce52c5601135000813c7f119e4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707447"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="15440-102">Assertphas;than-Vorgang</span><span class="sxs-lookup"><span data-stu-id="15440-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="15440-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="15440-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="15440-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="15440-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="15440-105">Bestätigt, dass der `number` codierte in phaselittleenddian kleiner als ist `value` .</span><span class="sxs-lookup"><span data-stu-id="15440-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="15440-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="15440-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="15440-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="15440-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="15440-108">`number` muss kleiner sein als.</span><span class="sxs-lookup"><span data-stu-id="15440-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="15440-109">Zahl: [phaselittleddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="15440-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="15440-110">Ganzzahl ohne Vorzeichen, die mit verglichen wird `value` .</span><span class="sxs-lookup"><span data-stu-id="15440-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="15440-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="15440-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="15440-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15440-112">Remarks</span></span>

<span data-ttu-id="15440-113">Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="15440-113">The controlled version of this operation ignores controls.</span></span>