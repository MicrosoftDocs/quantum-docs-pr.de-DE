---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalFxP
title: Computereciprocalfxp-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalFxP
qsharp.summary: Computes $1/x$ for a fixed-point number $x$.
ms.openlocfilehash: db7425f1a8a9b5ddfdc6b123dad003298e3670e6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843245"
---
# <a name="computereciprocalfxp-operation"></a><span data-ttu-id="c3279-102">Computereciprocalfxp-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c3279-102">ComputeReciprocalFxP operation</span></span>

<span data-ttu-id="c3279-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="c3279-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="c3279-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="c3279-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="c3279-105">Berechnet $1/x $ für eine Festkomma Zahl $x $.</span><span class="sxs-lookup"><span data-stu-id="c3279-105">Computes $1/x$ for a fixed-point number $x$.</span></span>

```qsharp
operation ComputeReciprocalFxP (x : Microsoft.Quantum.Arithmetic.FixedPoint, result : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c3279-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c3279-106">Input</span></span>

### <a name="x--fixedpoint"></a><span data-ttu-id="c3279-107">x: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="c3279-107">x : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="c3279-108">Die Festkomma Zahl, die invertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3279-108">Fixed-point number to be inverted.</span></span>


### <a name="result--fixedpoint"></a><span data-ttu-id="c3279-109">Ergebnis: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span><span class="sxs-lookup"><span data-stu-id="c3279-109">result : [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)</span></span>

<span data-ttu-id="c3279-110">Die fest Komma Zahl, die das Ergebnis enthält.</span><span class="sxs-lookup"><span data-stu-id="c3279-110">Fixed-point number that will hold the result.</span></span> <span data-ttu-id="c3279-111">Muss mit "$ \ket{0.0} $" initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="c3279-111">Must be initialized to $\ket{0.0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3279-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3279-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

