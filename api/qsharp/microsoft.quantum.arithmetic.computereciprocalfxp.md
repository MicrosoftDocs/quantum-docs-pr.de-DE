---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Computereciprocalfxp-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: e8f31d82fc69a3d7f4b571c4a679255dffc28b7f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707362"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="dfe87-102">Computereciprocalfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dfe87-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="dfe87-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="dfe87-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="dfe87-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dfe87-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dfe87-105">Berechnet $1/x $ für eine Festkomma Zahl $x $.</span><span class="sxs-lookup"><span data-stu-id="dfe87-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="input"></a><span data-ttu-id="dfe87-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dfe87-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="dfe87-107">x: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="dfe87-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="dfe87-108">Die Festkomma Zahl, die invertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfe87-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="dfe87-109">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="dfe87-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="dfe87-110">Die fest Komma Zahl, die das Ergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="dfe87-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="dfe87-111">Muss mit "$ \ket{0.0} $" initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="dfe87-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dfe87-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dfe87-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

