---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Multiplyf XP-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 3c9ef9ade660e1f420d85162104d773b96722eeb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222608"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="656f8-102">Multiplyf XP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="656f8-102">MultiplyFxP operation</span></span>

<span data-ttu-id="656f8-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="656f8-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="656f8-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="656f8-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="656f8-105">Multipliziert zwei Festkomma Zahlen in quantenregistern.</span><span class="sxs-lookup"><span data-stu-id="656f8-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="656f8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="656f8-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="656f8-107">Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="656f8-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="656f8-108">Erste festpunktzahl.</span><span class="sxs-lookup"><span data-stu-id="656f8-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="656f8-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="656f8-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="656f8-110">Zweite Festkomma Zahl.</span><span class="sxs-lookup"><span data-stu-id="656f8-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="656f8-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="656f8-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="656f8-112">Die Ergebnis Festkomma Zahl muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="656f8-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="656f8-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="656f8-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="656f8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="656f8-114">Remarks</span></span>

<span data-ttu-id="656f8-115">Die aktuelle Implementierung erfordert, dass die drei Fixed-Point-Nummern die gleiche Punktposition und die gleiche Anzahl von Qubits aufweisen.</span><span class="sxs-lookup"><span data-stu-id="656f8-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>