---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Multiplyi-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 96922f0147788b37cc9bace5154288a722d4ba95
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222506"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="f4a55-102">Multiplyi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f4a55-102">MultiplyI operation</span></span>

<span data-ttu-id="f4a55-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f4a55-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f4a55-104">Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="f4a55-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="f4a55-105">Multiplizieren Sie Integer `xs` nach Ganzzahl `ys` , und speichern Sie das Ergebnis in `result` , das anfänglich NULL sein muss.</span><span class="sxs-lookup"><span data-stu-id="f4a55-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f4a55-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f4a55-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f4a55-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f4a55-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f4a55-108">$n $-Bit Multiplikand (littleEndian)</span><span class="sxs-lookup"><span data-stu-id="f4a55-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="f4a55-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f4a55-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f4a55-110">$n $-Bit-Multiplikator (littleEndian)</span><span class="sxs-lookup"><span data-stu-id="f4a55-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="f4a55-111">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f4a55-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f4a55-112">$2N $-Bit-Ergebnis (littleEndian) muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f4a55-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f4a55-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f4a55-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f4a55-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4a55-114">Remarks</span></span>

<span data-ttu-id="f4a55-115">Verwendet einen standardmäßigen Verschiebungs-und Add-Ansatz zum Implementieren der Multiplikation.</span><span class="sxs-lookup"><span data-stu-id="f4a55-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="f4a55-116">Die kontrollierte Version wurde verbessert, indem $x _I $ in ein von den Steuerelement-Qubits vorgelegter Ancilla-Qubit kopiert und anschließend die Addition für das Ancilla-Qubit gesteuert wurde.</span><span class="sxs-lookup"><span data-stu-id="f4a55-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>