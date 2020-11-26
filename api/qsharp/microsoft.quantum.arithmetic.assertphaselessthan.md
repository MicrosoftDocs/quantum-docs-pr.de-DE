---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Assertphas;than-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: 8a943ff937593801bd308ab4224c7051ff8a10cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223747"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="8497c-102">Assertphas;than-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8497c-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="8497c-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="8497c-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="8497c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8497c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8497c-105">Bestätigt, dass der `number` codierte in phaselittleenddian kleiner als ist `value` .</span><span class="sxs-lookup"><span data-stu-id="8497c-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8497c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8497c-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="8497c-107">Wert: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8497c-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8497c-108">`number` muss kleiner sein als.</span><span class="sxs-lookup"><span data-stu-id="8497c-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="8497c-109">Zahl: [phaselittleddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8497c-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="8497c-110">Ganzzahl ohne Vorzeichen, die mit verglichen wird `value` .</span><span class="sxs-lookup"><span data-stu-id="8497c-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8497c-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8497c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8497c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8497c-112">Remarks</span></span>

<span data-ttu-id="8497c-113">Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8497c-113">The controlled version of this operation ignores controls.</span></span>