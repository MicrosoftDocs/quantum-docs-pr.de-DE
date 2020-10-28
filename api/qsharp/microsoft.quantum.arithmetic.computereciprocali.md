---
uid: Microsoft.Quantum.Arithmetic.ComputeReciprocalI
title: Computereciprocali-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ComputeReciprocalI
qsharp.summary: Computes the reciprocal 1/x for an unsigned integer x using integer division. The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.
ms.openlocfilehash: b99e816ed69af6e6d1758442d6f95c5ab0e5c07a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707346"
---
# <a name="computereciprocali-operation"></a><span data-ttu-id="b9f17-102">Computereciprocali-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b9f17-102">ComputeReciprocalI operation</span></span>

<span data-ttu-id="b9f17-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b9f17-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b9f17-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b9f17-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b9f17-105">Berechnet die gegenseitige 1/x-Datei für eine Ganzzahl x ohne Vorzeichen unter Verwendung der ganzzahligen Division.</span><span class="sxs-lookup"><span data-stu-id="b9f17-105">Computes the reciprocal 1/x for an unsigned integer x using integer division.</span></span> <span data-ttu-id="b9f17-106">Das als ganze Zahl interpretierte Ergebnis ist `floor(2^(2*n-1) / x)` .</span><span class="sxs-lookup"><span data-stu-id="b9f17-106">The result, interpreted as an integer, will be `floor(2^(2*n-1) / x)`.</span></span>

```qsharp
operation ComputeReciprocalI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="b9f17-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9f17-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="b9f17-108">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b9f17-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b9f17-109">n-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="b9f17-109">n-bit unsigned integer</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="b9f17-110">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b9f17-110">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b9f17-111">die 2N-Bit-Ausgabe muss zunächst in "$ \ket $" liegen {0} .</span><span class="sxs-lookup"><span data-stu-id="b9f17-111">2n-bit output, must be in $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b9f17-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b9f17-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b9f17-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b9f17-113">Remarks</span></span>

<span data-ttu-id="b9f17-114">Bei der Eingabe x = 0 ist die Ausgabe alle.</span><span class="sxs-lookup"><span data-stu-id="b9f17-114">For the input x=0, the output will be all-ones.</span></span>