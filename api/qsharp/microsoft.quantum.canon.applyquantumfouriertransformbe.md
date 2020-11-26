---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Applyquantenfouriertransformbe-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: 39db7b4c69f7f06418ec257c013837c65b9cc67a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209042"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="5e063-102">Applyquantenfouriertransformbe-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5e063-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="5e063-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5e063-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5e063-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5e063-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5e063-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Big-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="5e063-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="5e063-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5e063-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="5e063-107">QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="5e063-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="5e063-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e063-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="5e063-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5e063-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5e063-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e063-110">Remarks</span></span>

<span data-ttu-id="5e063-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="5e063-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e063-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e063-112">See Also</span></span>

- [<span data-ttu-id="5e063-113">Microsoft. Quantum. Canon. näherateqft</span><span class="sxs-lookup"><span data-stu-id="5e063-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="5e063-114">Microsoft. Quantum. Canon. qftle</span><span class="sxs-lookup"><span data-stu-id="5e063-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)