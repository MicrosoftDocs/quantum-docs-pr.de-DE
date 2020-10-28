---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Assertmugesignifiantbit-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707450"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="a71d5-102">Assertmugesignifiantbit-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a71d5-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="a71d5-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a71d5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a71d5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a71d5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a71d5-105">Bestätigt, dass das signifikanteste Qubit eines Qubit-Registers, das eine Ganzzahl ohne Vorzeichen darstellt, in einem bestimmten Zustand ist.</span><span class="sxs-lookup"><span data-stu-id="a71d5-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="a71d5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a71d5-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="a71d5-107">Wert: __ungültig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a71d5-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="a71d5-108">Der Wert des höchsten zu überprüfenden Bits.</span><span class="sxs-lookup"><span data-stu-id="a71d5-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="a71d5-109">Zahl: [littleenumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a71d5-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a71d5-110">Ganze Zahl ohne Vorzeichen, bei der das höchste Bit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a71d5-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a71d5-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a71d5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a71d5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a71d5-112">Remarks</span></span>

<span data-ttu-id="a71d5-113">Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a71d5-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="a71d5-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a71d5-114">See Also</span></span>

- [<span data-ttu-id="a71d5-115">Microsoft. Quantum. intrinsisch. Assert</span><span class="sxs-lookup"><span data-stu-id="a71d5-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)