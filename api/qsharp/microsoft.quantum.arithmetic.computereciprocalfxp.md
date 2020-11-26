---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Computereciprocalfxp-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: 3ca050d6ce9daaa10e14c2f12dd571398cf436b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223390"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="baff4-102">Computereciprocalfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="baff4-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="baff4-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="baff4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="baff4-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="baff4-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="baff4-105">Berechnet $1/x $ für eine Festkomma Zahl $x $.</span><span class="sxs-lookup"><span data-stu-id="baff4-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="baff4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="baff4-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="baff4-107">x: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="baff4-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="baff4-108">Die Festkomma Zahl, die invertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="baff4-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="baff4-109">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="baff4-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="baff4-110">Die fest Komma Zahl, die das Ergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="baff4-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="baff4-111">Muss mit "$ \ket{0.0} $" initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="baff4-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="baff4-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="baff4-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

