---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Applyquantumfouriertransform-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: fa8d135c0665f0a576229797d208b321ba0329a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705098"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="81702-102">Applyquantumfouriertransform-Vorgang</span><span class="sxs-lookup"><span data-stu-id="81702-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="81702-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="81702-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="81702-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81702-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81702-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Little-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="81702-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="81702-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="81702-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="81702-107">QS: [Little-Dian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="81702-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="81702-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="81702-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="81702-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81702-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="81702-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="81702-110">Remarks</span></span>

<span data-ttu-id="81702-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in Little-ercodierungscodierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="81702-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="81702-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="81702-112">See Also</span></span>

- [<span data-ttu-id="81702-113">Microsoft. Quantum. Canon. applyquantumfouriertransformbe</span><span class="sxs-lookup"><span data-stu-id="81702-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)