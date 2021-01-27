---
uid: Microsoft.Quantum.Canon.ApplyQuantumFourierTransform
title: Applyquantumfouriertransform-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyQuantumFourierTransform
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: d99000c21c79d2ca97b1fe92ad331c7ba8599700
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844756"
---
# <a name="applyquantumfouriertransform-operation"></a><span data-ttu-id="6f429-102">Applyquantumfouriertransform-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6f429-102">ApplyQuantumFourierTransform operation</span></span>

<span data-ttu-id="6f429-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6f429-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6f429-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f429-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6f429-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Little-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="6f429-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation ApplyQuantumFourierTransform (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6f429-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6f429-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="6f429-107">QS: [Little-Dian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6f429-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6f429-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f429-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="6f429-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6f429-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6f429-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f429-110">Remarks</span></span>

<span data-ttu-id="6f429-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in Little-ercodierungscodierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="6f429-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f429-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6f429-112">See Also</span></span>

- [<span data-ttu-id="6f429-113">Microsoft. Quantum. Canon. applyquantumfouriertransformbe</span><span class="sxs-lookup"><span data-stu-id="6f429-113">Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE</span></span>](xref:Microsoft.Quantum.Canon.ApplyQuantumFourierTransformBE)