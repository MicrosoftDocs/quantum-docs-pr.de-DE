---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Squaresi-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7fe4d27b974a06b019a2b15710fbc51b598027b4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221826"
---
# <a name="squaresi-operation"></a><span data-ttu-id="901ba-102">Squaresi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="901ba-102">SquareSI operation</span></span>

<span data-ttu-id="901ba-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="901ba-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="901ba-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="901ba-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="901ba-105">Eine quadratische Ganzzahl `xs` mit Vorzeichen und speichert das Ergebnis in `result` , das anfänglich NULL sein muss.</span><span class="sxs-lookup"><span data-stu-id="901ba-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="901ba-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="901ba-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="901ba-107">xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="901ba-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="901ba-108">n-Bit-Ganzzahl in Quadrat (signedlittleendian)</span><span class="sxs-lookup"><span data-stu-id="901ba-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="901ba-109">Ergebnis: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="901ba-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="901ba-110">Das 2N-Bit-Ergebnis (signedlittleendian) muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="901ba-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="901ba-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="901ba-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="901ba-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="901ba-112">Remarks</span></span>

<span data-ttu-id="901ba-113">Die-Implementierung basiert auf integersquare.</span><span class="sxs-lookup"><span data-stu-id="901ba-113">The implementation relies on IntegerSquare.</span></span>