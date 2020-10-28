---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Wert für "messbare Ganzzahl"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707175"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="fb54b-102">Wert für "messbare Ganzzahl"</span><span class="sxs-lookup"><span data-stu-id="fb54b-102">MeasureInteger operation</span></span>

<span data-ttu-id="fb54b-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="fb54b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="fb54b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fb54b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fb54b-105">Misst den Inhalt eines Quantum-Registers und konvertiert ihn in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="fb54b-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="fb54b-106">Die Messung erfolgt in Bezug auf die standardmäßige Berechnungsbasis, d. h. auf die eigen Basis von `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="fb54b-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="fb54b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb54b-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="fb54b-108">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fb54b-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fb54b-109">Ein Quantum-Register in der Little-d-Codierung.</span><span class="sxs-lookup"><span data-stu-id="fb54b-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="fb54b-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fb54b-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fb54b-111">Eine ganze Zahl ohne Vorzeichen, die den gemessenen Wert von enthält `target` .</span><span class="sxs-lookup"><span data-stu-id="fb54b-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb54b-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fb54b-112">Remarks</span></span>

<span data-ttu-id="fb54b-113">Durch diesen Vorgang wird das Eingabe Register auf den Zustand "$ \ket{00\cdots 0} $" zurückgesetzt, der für die Freigabe an einen Zielcomputer geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="fb54b-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb54b-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fb54b-114">See Also</span></span>

- [<span data-ttu-id="fb54b-115">Microsoft. Quantum. Canon. Mess reintegerbe</span><span class="sxs-lookup"><span data-stu-id="fb54b-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)