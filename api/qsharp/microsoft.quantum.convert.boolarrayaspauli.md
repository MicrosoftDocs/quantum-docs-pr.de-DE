---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Boolarrayaspauli-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: 8e7088ec3918165d7b2afb1056a8319c6fb17796
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214278"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="e0a9a-102">Boolarrayaspauli-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0a9a-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="e0a9a-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="e0a9a-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="e0a9a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0a9a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0a9a-105">Gibt bei Angabe einer Bitzeichenfolge einen multiqubit-Pauli-Operator zurück, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="e0a9a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e0a9a-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="e0a9a-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="e0a9a-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="e0a9a-108">Der Pauli-Operator, der auf Qubits angewendet wird, wobei `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="e0a9a-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="e0a9a-109">bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e0a9a-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e0a9a-110">Anwenden von Pauli, wenn Bit dieser Wert ist.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="e0a9a-111">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="e0a9a-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="e0a9a-112">Boolesches Array.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="e0a9a-113">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="e0a9a-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="e0a9a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0a9a-114">Remarks</span></span>

<span data-ttu-id="e0a9a-115">Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e0a9a-115">The Boolean array and the quantum register must be of equal length.</span></span>