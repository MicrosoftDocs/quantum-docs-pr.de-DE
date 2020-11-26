---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Comparegreaterthanf XP-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: 1e9afc7645f62b932fa8ebc3d33e21a2a5182361
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223526"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="5df34-102">Comparegreaterthanf XP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5df34-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="5df34-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5df34-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5df34-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="5df34-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="5df34-105">Vergleicht zwei in quantenregistern gespeicherte Fixed-Point-Nummern und steuert einen Flip-Wert für das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="5df34-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5df34-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5df34-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="5df34-107">Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="5df34-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="5df34-108">Die erste zu vergleichende fixpunktzahl.</span><span class="sxs-lookup"><span data-stu-id="5df34-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="5df34-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="5df34-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="5df34-110">Die zweite zu vergleichende Festkomma Zahl.</span><span class="sxs-lookup"><span data-stu-id="5df34-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="5df34-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5df34-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5df34-112">Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="5df34-112">Result of the comparison.</span></span> <span data-ttu-id="5df34-113">Wird gekippt, wenn `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="5df34-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5df34-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5df34-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5df34-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5df34-115">Remarks</span></span>

<span data-ttu-id="5df34-116">Die aktuelle Implementierung erfordert, dass die zwei Festkomma Zahlen dieselbe Punktposition und dieselbe Anzahl von Qubits aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5df34-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>