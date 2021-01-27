---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: Boolarrayaspauli-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834246"
---
# <a name="boolarrayaspauli-function"></a><span data-ttu-id="4ff9e-102">Boolarrayaspauli-Funktion</span><span class="sxs-lookup"><span data-stu-id="4ff9e-102">BoolArrayAsPauli function</span></span>

<span data-ttu-id="4ff9e-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="4ff9e-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="4ff9e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4ff9e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4ff9e-105">Gibt bei Angabe einer Bitzeichenfolge einen multiqubit-Pauli-Operator zurück, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4ff9e-105">Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.</span></span>

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="4ff9e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ff9e-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="4ff9e-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="4ff9e-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="4ff9e-108">Der Pauli-Operator, der auf Qubits angewendet wird, wobei `bitsApply == bits[idx]` .</span><span class="sxs-lookup"><span data-stu-id="4ff9e-108">Pauli operator to apply to qubits where `bitsApply == bits[idx]`.</span></span>


### <a name="bitapply--bool"></a><span data-ttu-id="4ff9e-109">bitapply: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4ff9e-109">bitApply : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4ff9e-110">Anwenden von Pauli, wenn Bit dieser Wert ist.</span><span class="sxs-lookup"><span data-stu-id="4ff9e-110">apply Pauli if bit is this value.</span></span>


### <a name="bits--bool"></a><span data-ttu-id="4ff9e-111">Bits: [bool](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="4ff9e-111">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="4ff9e-112">Boolesches Array.</span><span class="sxs-lookup"><span data-stu-id="4ff9e-112">Boolean array.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="4ff9e-113">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="4ff9e-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>



## <a name="remarks"></a><span data-ttu-id="4ff9e-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ff9e-114">Remarks</span></span>

<span data-ttu-id="4ff9e-115">Das boolesche Array und das Quantum-Register müssen die gleiche Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4ff9e-115">The Boolean array and the quantum register must be of equal length.</span></span>