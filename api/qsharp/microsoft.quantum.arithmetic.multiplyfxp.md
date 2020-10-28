---
uid: Microsoft.Quantum.Arithmetic.MultiplyFxP
title: Multiplyf XP-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyFxP
qsharp.summary: Multiplies two fixed-point numbers in quantum registers.
ms.openlocfilehash: 18883f3f4c3793b91e248f4bd89f9def640bf254
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706383"
---
# <a name="multiplyfxp-operation"></a><span data-ttu-id="2d3b4-102">Multiplyf XP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="2d3b4-102">MultiplyFxP operation</span></span>

<span data-ttu-id="2d3b4-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2d3b4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2d3b4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2d3b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2d3b4-105">Multipliziert zwei Festkomma Zahlen in quantenregistern.</span><span class="sxs-lookup"><span data-stu-id="2d3b4-105">Multiplies two fixed-point numbers in quantum registers.</span></span>

```qsharp
operation MultiplyFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="2d3b4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2d3b4-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="2d3b4-107">Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2d3b4-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2d3b4-108">Erste festpunktzahl.</span><span class="sxs-lookup"><span data-stu-id="2d3b4-108">First fixed-point number.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="2d3b4-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2d3b4-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2d3b4-110">Zweite Festkomma Zahl.</span><span class="sxs-lookup"><span data-stu-id="2d3b4-110">Second fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="2d3b4-111">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="2d3b4-111">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="2d3b4-112">Die Ergebnis Festkomma Zahl muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2d3b4-112">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2d3b4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2d3b4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="2d3b4-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2d3b4-114">Remarks</span></span>

<span data-ttu-id="2d3b4-115">Die aktuelle Implementierung erfordert, dass die drei Fixed-Point-Nummern die gleiche Punktposition und die gleiche Anzahl von Qubits aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2d3b4-115">The current implementation requires the three fixed-point numbers to have the same point position and the same number of qubits.</span></span>