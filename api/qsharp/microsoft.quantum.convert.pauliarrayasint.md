---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: Pauliarrayasint-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702924"
---
# <a name="pauliarrayasint-function"></a><span data-ttu-id="3aa31-102">Pauliarrayasint-Funktion</span><span class="sxs-lookup"><span data-stu-id="3aa31-102">PauliArrayAsInt function</span></span>

<span data-ttu-id="3aa31-103">Namespace: [Microsoft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="3aa31-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="3aa31-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3aa31-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3aa31-105">Codiert einen multiqubit-Pauli-Operator, der als Array von Single-Qubit-Pauli-Operatoren dargestellt wird, in eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="3aa31-105">Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.</span></span>

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a><span data-ttu-id="3aa31-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3aa31-106">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="3aa31-107">Paulis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="3aa31-107">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="3aa31-108">Ein Array mit höchstens 31 Single-Qubit-Pauli-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="3aa31-108">An array of at most 31 single-qubit Pauli operators.</span></span>



## <a name="output--int"></a><span data-ttu-id="3aa31-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3aa31-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3aa31-110">Eine Ganzzahl, die eindeutig identifiziert `paulis` , wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3aa31-110">An integer uniquely identifying `paulis`, as described below.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa31-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3aa31-111">Remarks</span></span>

<span data-ttu-id="3aa31-112">Jeder Pauli-Operator kann mit zwei Bits codiert werden: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span><span class="sxs-lookup"><span data-stu-id="3aa31-112">Each Pauli operator can be encoded using two bits: $$ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.</span></span>
<span data-ttu-id="3aa31-113">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="3aa31-113">\end{align} $$</span></span>

<span data-ttu-id="3aa31-114">Bei einem Array von Pauli-Operatoren `[P0, ..., Pn]` gibt diese Funktion eine ganze Zahl mit binärer Erweiterung zurück, die durch Verkettung der Zuordnungen der einzelnen Pauli-Operatoren in Big-Endian-Reihenfolge gebildet wird `bits(Pn) ... bits(P0)` .</span><span class="sxs-lookup"><span data-stu-id="3aa31-114">Given an array of Pauli operators `[P0, ..., Pn]`, this function returns an integer with binary expansion formed by concatenating the mappings of each Pauli operator in big-endian order `bits(Pn) ... bits(P0)`.</span></span>