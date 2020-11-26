---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Wert für "messbare Ganzzahl"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: e3ff06e5cbb2ef8a63e4ad12308b382347c90fc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222642"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="e0154-102">Wert für "messbare Ganzzahl"</span><span class="sxs-lookup"><span data-stu-id="e0154-102">MeasureInteger operation</span></span>

<span data-ttu-id="e0154-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e0154-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e0154-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0154-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0154-105">Misst den Inhalt eines Quantum-Registers und konvertiert ihn in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="e0154-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="e0154-106">Die Messung erfolgt in Bezug auf die standardmäßige Berechnungsbasis, d. h. auf die eigen Basis von `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="e0154-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="e0154-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0154-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="e0154-108">Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e0154-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e0154-109">Ein Quantum-Register in der Little-d-Codierung.</span><span class="sxs-lookup"><span data-stu-id="e0154-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="e0154-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e0154-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e0154-111">Eine ganze Zahl ohne Vorzeichen, die den gemessenen Wert von enthält `target` .</span><span class="sxs-lookup"><span data-stu-id="e0154-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0154-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0154-112">Remarks</span></span>

<span data-ttu-id="e0154-113">Durch diesen Vorgang wird das Eingabe Register auf den Zustand "$ \ket{00\cdots 0} $" zurückgesetzt, der für die Freigabe an einen Zielcomputer geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="e0154-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0154-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0154-114">See Also</span></span>

- [<span data-ttu-id="e0154-115">Microsoft. Quantum. Canon. Mess reintegerbe</span><span class="sxs-lookup"><span data-stu-id="e0154-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)