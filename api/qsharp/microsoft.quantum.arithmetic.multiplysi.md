---
uid: Microsoft.Quantum.Arithmetic.MultiplySI
title: Multiplysi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplySI
qsharp.summary: Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 9ca781cbe90a8ec13e6a85a5babaf043bc8f2b5b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706362"
---
# <a name="multiplysi-operation"></a><span data-ttu-id="ae3e4-102">Multiplysi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ae3e4-102">MultiplySI operation</span></span>

<span data-ttu-id="ae3e4-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="ae3e4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ae3e4-105">Multiplizieren Sie eine ganze Zahl `xs` mit Vorzeichen `ys` , und speichern Sie das Ergebnis in `result` , das anfänglich NULL sein muss.</span><span class="sxs-lookup"><span data-stu-id="ae3e4-105">Multiply signed integer `xs` by signed integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplySI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, ys : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="ae3e4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ae3e4-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="ae3e4-107">xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="ae3e4-108">n-Bit Multiplikand (signedlittleendian)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-108">n-bit multiplicand (SignedLittleEndian)</span></span>


### <a name="ys--signedlittleendian"></a><span data-ttu-id="ae3e4-109">YS: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-109">ys : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="ae3e4-110">n-Bit-Multiplikator (signedlittleendian)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-110">n-bit multiplier (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="ae3e4-111">Ergebnis: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-111">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="ae3e4-112">Das 2N-Bit-Ergebnis (signedlittleendian) muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="ae3e4-112">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ae3e4-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ae3e4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

