---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Wert für "messbare Ganzzahl"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843123"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="3f61a-102">Wert für "messbare Ganzzahl"</span><span class="sxs-lookup"><span data-stu-id="3f61a-102">MeasureInteger operation</span></span>

<span data-ttu-id="3f61a-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3f61a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3f61a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f61a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f61a-105">Misst den Inhalt eines Quantum-Registers und konvertiert ihn in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="3f61a-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="3f61a-106">Die Messung erfolgt in Bezug auf die standardmäßige Berechnungsbasis, d. h. auf die eigen Basis von `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="3f61a-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="3f61a-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f61a-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="3f61a-108">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3f61a-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3f61a-109">Ein Quantum-Register in der Little-d-Codierung.</span><span class="sxs-lookup"><span data-stu-id="3f61a-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="3f61a-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3f61a-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3f61a-111">Eine ganze Zahl ohne Vorzeichen, die den gemessenen Wert von enthält `target` .</span><span class="sxs-lookup"><span data-stu-id="3f61a-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f61a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3f61a-112">Remarks</span></span>

<span data-ttu-id="3f61a-113">Durch diesen Vorgang wird das Eingabe Register auf den Zustand "$ \ket{00\cdots 0} $" zurückgesetzt, der für die Freigabe an einen Zielcomputer geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="3f61a-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="3f61a-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3f61a-114">See Also</span></span>

- [<span data-ttu-id="3f61a-115">Microsoft. Quantum. Canon. Mess reintegerbe</span><span class="sxs-lookup"><span data-stu-id="3f61a-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)