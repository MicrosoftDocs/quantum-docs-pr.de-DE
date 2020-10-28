---
uid: Microsoft.Quantum.Arithmetic.SquareSI
title: Squaresi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: SquareSI
qsharp.summary: Square signed integer `xs` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: c8c4e3cca001aa6d7ce1b9df106ce77f74524301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706218"
---
# <a name="squaresi-operation"></a><span data-ttu-id="84ef4-102">Squaresi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="84ef4-102">SquareSI operation</span></span>

<span data-ttu-id="84ef4-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="84ef4-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="84ef4-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="84ef4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="84ef4-105">Eine quadratische Ganzzahl `xs` mit Vorzeichen und speichert das Ergebnis in `result` , das anfänglich NULL sein muss.</span><span class="sxs-lookup"><span data-stu-id="84ef4-105">Square signed integer `xs` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation SquareSI (xs : Microsoft.Quantum.Arithmetic.SignedLittleEndian, result : Microsoft.Quantum.Arithmetic.SignedLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="84ef4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="84ef4-106">Input</span></span>

### <a name="xs--signedlittleendian"></a><span data-ttu-id="84ef4-107">xs: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="84ef4-107">xs : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="84ef4-108">n-Bit-Ganzzahl in Quadrat (signedlittleendian)</span><span class="sxs-lookup"><span data-stu-id="84ef4-108">n-bit integer to square (SignedLittleEndian)</span></span>


### <a name="result--signedlittleendian"></a><span data-ttu-id="84ef4-109">Ergebnis: [signedlittleenddian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="84ef4-109">result : [SignedLittleEndian](xref:Microsoft.Quantum.Arithmetic.SignedLittleEndian)</span></span>

<span data-ttu-id="84ef4-110">Das 2N-Bit-Ergebnis (signedlittleendian) muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="84ef4-110">2n-bit result (SignedLittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="84ef4-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="84ef4-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="84ef4-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84ef4-112">Remarks</span></span>

<span data-ttu-id="84ef4-113">Die-Implementierung basiert auf integersquare.</span><span class="sxs-lookup"><span data-stu-id="84ef4-113">The implementation relies on IntegerSquare.</span></span>