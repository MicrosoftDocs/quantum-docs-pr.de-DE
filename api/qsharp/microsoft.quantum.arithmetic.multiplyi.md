---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Multiplyi-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7b44f64fdddfd95f51683c2c3b2f4d37d0cf6841
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706370"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="9cc05-102">Multiplyi-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9cc05-102">MultiplyI operation</span></span>

<span data-ttu-id="9cc05-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="9cc05-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="9cc05-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9cc05-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9cc05-105">Multiplizieren Sie Integer `xs` nach Ganzzahl `ys` , und speichern Sie das Ergebnis in `result` , das anfänglich NULL sein muss.</span><span class="sxs-lookup"><span data-stu-id="9cc05-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="9cc05-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9cc05-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="9cc05-107">xs: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9cc05-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9cc05-108">$n $-Bit Multiplikand (littleEndian)</span><span class="sxs-lookup"><span data-stu-id="9cc05-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="9cc05-109">YS: [littleumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9cc05-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9cc05-110">$n $-Bit-Multiplikator (littleEndian)</span><span class="sxs-lookup"><span data-stu-id="9cc05-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="9cc05-111">Ergebnis: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="9cc05-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="9cc05-112">$2N $-Bit-Ergebnis (littleEndian) muss zunächst den Status $ \ket {0} $ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9cc05-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9cc05-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9cc05-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9cc05-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9cc05-114">Remarks</span></span>

<span data-ttu-id="9cc05-115">Verwendet einen standardmäßigen Verschiebungs-und Add-Ansatz zum Implementieren der Multiplikation.</span><span class="sxs-lookup"><span data-stu-id="9cc05-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="9cc05-116">Die kontrollierte Version wurde verbessert, indem $x _I $ in ein von den Steuerelement-Qubits vorgelegter Ancilla-Qubit kopiert und anschließend die Addition für das Ancilla-Qubit gesteuert wurde.</span><span class="sxs-lookup"><span data-stu-id="9cc05-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>