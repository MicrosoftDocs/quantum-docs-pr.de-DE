---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Boolarrayaspauli-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c5ef71322dae248fc2c6b1db3adf891de7d72488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703025"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="cf9f2-102">Boolarrayaspauli-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf9f2-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="cf9f2-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="cf9f2-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="cf9f2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cf9f2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cf9f2-105">Gibt bei Angabe einer Bitzeichenfolge einen multiqubit-Pauli-Operator zurück, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf9f2-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="cf9f2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="cf9f2-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="cf9f2-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="cf9f2-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="cf9f2-108">Der Pauli-Operator, der auf Qubits angewendet wird, wobei `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="cf9f2-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="cf9f2-109">bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cf9f2-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cf9f2-110">Anwenden von Pauli, wenn Bit dieser Wert ist.</span><span class="sxs-lookup"><span data-stu-id="cf9f2-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="cf9f2-111">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="cf9f2-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="cf9f2-112">Boolesches Array.</span><span class="sxs-lookup"><span data-stu-id="cf9f2-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="cf9f2-113">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="cf9f2-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="cf9f2-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cf9f2-114">Remarks</span></span>

<span data-ttu-id="cf9f2-115">Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cf9f2-115">The Boolean array and the quantum register must be of equal length.</span></span>