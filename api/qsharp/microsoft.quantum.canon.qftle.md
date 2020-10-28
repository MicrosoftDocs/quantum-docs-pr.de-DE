---
uid: Microsoft.Quantum.Canon.QFTLE
title: Qftle-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: QFTLE
qsharp.summary: Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.
ms.openlocfilehash: f28f74d34fb4688739646da3dc12ae6734eb4ad4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703896"
---
# <a name="qftle-operation"></a><span data-ttu-id="b879d-102">Qftle-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b879d-102">QFTLE operation</span></span>

<span data-ttu-id="b879d-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b879d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b879d-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b879d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b879d-105">Führt die Quantum Fourier-Transformation für ein Quantum-Register durch, das eine ganze Zahl in der Little-Endian-Darstellung enthält.</span><span class="sxs-lookup"><span data-stu-id="b879d-105">Performs the Quantum Fourier Transform on a quantum register containing an integer in the little-endian representation.</span></span>

```qsharp
operation QFTLE (qs : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="b879d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b879d-106">Input</span></span>

### <a name="qs--littleendian"></a><span data-ttu-id="b879d-107">QS: [Little-Dian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b879d-107">qs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b879d-108">Das Quantum-Register, auf das die Quantum Fourier-Transformation angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="b879d-108">Quantum register to which the Quantum Fourier Transform is applied</span></span>



## <a name="output--unit"></a><span data-ttu-id="b879d-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b879d-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b879d-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b879d-110">Remarks</span></span>

<span data-ttu-id="b879d-111">Es wird davon ausgegangen, dass die Eingabe und die Ausgabe in Little-ercodierungscodierung vorliegen.</span><span class="sxs-lookup"><span data-stu-id="b879d-111">The input and output are assumed to be in little endian encoding.</span></span>

## <a name="see-also"></a><span data-ttu-id="b879d-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b879d-112">See Also</span></span>

- [<span data-ttu-id="b879d-113">Microsoft. Quantum. Canon. qft</span><span class="sxs-lookup"><span data-stu-id="b879d-113">Microsoft.Quantum.Canon.QFT</span></span>](xref:Microsoft.Quantum.Canon.QFT)