---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Computereciprocali-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: 9024da4a457265c65a41ef681cfbb99ebd4989a5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223356"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="04974-102">Computereciprocali-Vorgang</span><span class="sxs-lookup"><span data-stu-id="04974-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="04974-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="04974-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="04974-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="04974-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="04974-105">Berechnet die gegenseitige 1/x-Datei für eine Ganzzahl x ohne Vorzeichen unter Verwendung der ganzzahligen Division.</span><span class="sxs-lookup"><span data-stu-id="04974-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="04974-106">Das als ganze Zahl interpretierte Ergebnis ist `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="04974-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="04974-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="04974-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="04974-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="04974-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="04974-109">n-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="04974-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="04974-110">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="04974-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="04974-111">die 2N-Bit-Ausgabe muss zunächst in "$ \ket $" liegen {0} .</span><span class="sxs-lookup"><span data-stu-id="04974-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="04974-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="04974-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="04974-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04974-113">Remarks</span></span>

<span data-ttu-id="04974-114">Bei der Eingabe x = 0 ist die Ausgabe alle.</span><span class="sxs-lookup"><span data-stu-id="04974-114">For the input x=0, the output will be all-ones.</span></span>