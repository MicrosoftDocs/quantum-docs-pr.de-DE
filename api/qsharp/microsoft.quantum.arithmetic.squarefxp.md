---
uid: Microsoft.Quantum.Arithmetic.SquareFxP
title: Squaref XP-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareFxP
qsharp.summary: Squares a fixed-point number.
ms.openlocfilehash: 8d08cb51e3a7ae892b23be0adbb7cdf3ee0f4de5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221877"
---
# <a name="squarefxp-operation"></a><span data-ttu-id="f814d-102">Squaref XP-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f814d-102">SquareFxP operation</span></span>

<span data-ttu-id="f814d-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f814d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f814d-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="f814d-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="f814d-105">Quadriert eine festpunktzahl.</span><span class="sxs-lookup"><span data-stu-id="f814d-105">Squares a fixed-point number.</span></span>

```qsharp
operation SquareFxP (fp : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f814d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f814d-106">Input</span></span>

### <a name="fp--fixedpoint"></a><span data-ttu-id="f814d-107">fp: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="f814d-107">fp : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="f814d-108">Die Festkomma Zahl.</span><span class="sxs-lookup"><span data-stu-id="f814d-108">Fixed-point number.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="f814d-109">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="f814d-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="f814d-110">Die Ergebnis Festkomma Zahl muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f814d-110">Result fixed-point number, must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f814d-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f814d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

