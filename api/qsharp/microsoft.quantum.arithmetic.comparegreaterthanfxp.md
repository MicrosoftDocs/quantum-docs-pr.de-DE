---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Comparegreaterthanf XP-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: bd3bcedd7a4a81fc600f7f4b6bdf1d2a797abbd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707394"
---
# <a name="comparegreaterthanfxp-operation"></a><span data-ttu-id="7c1aa-102">Comparegreaterthanf XP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7c1aa-102">CompareGreaterThanFxP operation</span></span>

<span data-ttu-id="7c1aa-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="7c1aa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="7c1aa-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7c1aa-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7c1aa-105">Vergleicht zwei in quantenregistern gespeicherte Fixed-Point-Nummern und steuert einen Flip-Wert für das Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="7c1aa-105">Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.</span></span>

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="7c1aa-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7c1aa-106">Input</span></span>

### <a name="fp1--fixedpoint"></a><span data-ttu-id="7c1aa-107">Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="7c1aa-107">fp1 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="7c1aa-108">Die erste zu vergleichende fixpunktzahl.</span><span class="sxs-lookup"><span data-stu-id="7c1aa-108">First fixed-point number to be compared.</span></span>


### <a name="fp2--fixedpoint"></a><span data-ttu-id="7c1aa-109">FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="7c1aa-109">fp2 : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="7c1aa-110">Die zweite zu vergleichende Festkomma Zahl.</span><span class="sxs-lookup"><span data-stu-id="7c1aa-110">Second fixed-point number to be compared.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="7c1aa-111">Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7c1aa-111">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7c1aa-112">Ergebnis des Vergleichs.</span><span class="sxs-lookup"><span data-stu-id="7c1aa-112">Result of the comparison.</span></span> <span data-ttu-id="7c1aa-113">Wird gekippt, wenn `fp1 > fp2` .</span><span class="sxs-lookup"><span data-stu-id="7c1aa-113">Will be flipped if `fp1 > fp2`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7c1aa-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7c1aa-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7c1aa-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c1aa-115">Remarks</span></span>

<span data-ttu-id="7c1aa-116">Die aktuelle Implementierung erfordert, dass die zwei Festkomma Zahlen dieselbe Punktposition und dieselbe Anzahl von Qubits aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7c1aa-116">The current implementation requires the two fixed-point numbers to have the same point position and the same number of qubits.</span></span>