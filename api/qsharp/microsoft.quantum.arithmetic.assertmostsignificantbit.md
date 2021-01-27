---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Assertmugesignifiantbit-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843422"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="6509f-102">Assertmugesignifiantbit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6509f-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="6509f-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6509f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6509f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6509f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6509f-105">Bestätigt, dass das signifikanteste Qubit eines Qubit-Registers, das eine Ganzzahl ohne Vorzeichen darstellt, in einem bestimmten Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="6509f-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6509f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6509f-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="6509f-107">Wert: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6509f-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="6509f-108">Der Wert des höchsten zu überprüfenden Bits.</span><span class="sxs-lookup"><span data-stu-id="6509f-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="6509f-109">Zahl: [littleenumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6509f-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6509f-110">Ganze Zahl ohne Vorzeichen, bei der das höchste Bit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6509f-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6509f-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6509f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6509f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6509f-112">Remarks</span></span>

<span data-ttu-id="6509f-113">Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6509f-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="6509f-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6509f-114">See Also</span></span>

- [<span data-ttu-id="6509f-115">Microsoft. Quantum. intrinsisch. Assert</span><span class="sxs-lookup"><span data-stu-id="6509f-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)