---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Applyquantenfouriertransformbe-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: d15310298dc138bdffb612895bbf20ca1371db6f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705095"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="19a21-102">Applyquantenfouriertransformbe-Vorgang</span><span class="sxs-lookup"><span data-stu-id="19a21-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="19a21-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="19a21-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="19a21-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="19a21-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="19a21-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Big-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="19a21-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="19a21-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="19a21-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="19a21-107">QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="19a21-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="19a21-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="19a21-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="19a21-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="19a21-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="19a21-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19a21-110">Remarks</span></span>

<span data-ttu-id="19a21-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="19a21-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="19a21-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="19a21-112">See Also</span></span>

- [<span data-ttu-id="19a21-113">Microsoft. Quantum. Canon. näherateqft</span><span class="sxs-lookup"><span data-stu-id="19a21-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="19a21-114">Microsoft. Quantum. Canon. qftle</span><span class="sxs-lookup"><span data-stu-id="19a21-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)