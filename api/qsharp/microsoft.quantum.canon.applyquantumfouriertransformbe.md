---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE
title: Applyquantenfouriertransformbe-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransformBE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: a1f4a0a5e94465fc8bf3af344e2e19ee0d1d15e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841561"
---
# <a name="applyquantumfouriertransformbe-operation"></a><span data-ttu-id="a3b83-102">Applyquantenfouriertransformbe-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a3b83-102">ApplyQuantumFourierTransformBE operation</span></span>

<span data-ttu-id="a3b83-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a3b83-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a3b83-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a3b83-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a3b83-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Big-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="a3b83-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransformBE (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a3b83-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a3b83-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="a3b83-107">QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="a3b83-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="a3b83-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a3b83-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="a3b83-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a3b83-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a3b83-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3b83-110">Remarks</span></span>

<span data-ttu-id="a3b83-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="a3b83-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="a3b83-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a3b83-112">See Also</span></span>

- [<span data-ttu-id="a3b83-113">Microsoft. Quantum. Canon. näherateqft</span><span class="sxs-lookup"><span data-stu-id="a3b83-113">Microsoft.Quantum.Canon.ApproximateQFT</span></span>](xref:Microsoft.Quantum.Canon.ApproximateQFT)
- [<span data-ttu-id="a3b83-114">Microsoft. Quantum. Canon. qftle</span><span class="sxs-lookup"><span data-stu-id="a3b83-114">Microsoft.Quantum.Canon.QFTLE</span></span>](xref:Microsoft.Quantum.Canon.QFTLE)