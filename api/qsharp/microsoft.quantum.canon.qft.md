---
uid: Microsoft.Quantum.Canon.QFT
title: QFT-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFT
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.
ms.openlocfilehash: e5b40be6c86647205fe1c764b6b043272296a354
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703902"
---
# <a name="qft-operation"></a><span data-ttu-id="6b46f-102">QFT-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6b46f-102">QFT operation</span></span>

<span data-ttu-id="6b46f-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6b46f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6b46f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6b46f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6b46f-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Big-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="6b46f-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the big-endian representation.</span></span>

```qsharp
operation QFT (qs : Microsoft.Quantum.Arithmetic.BigEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="6b46f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b46f-106">Input</span></span>

### <a name="qs--bigendian"></a><span data-ttu-id="6b46f-107">QS: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="6b46f-107">qs : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="6b46f-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b46f-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="6b46f-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6b46f-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6b46f-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b46f-110">Remarks</span></span>

<span data-ttu-id="6b46f-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in der Big-d-Codierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6b46f-111">The input and output are assumed to be in big endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b46f-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b46f-112">See Also</span></span>

- [<span data-ttu-id="6b46f-113">Microsoft. Quantum. Canon. applyquantumfouriertransformbe</span><span class="sxs-lookup"><span data-stu-id="6b46f-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)