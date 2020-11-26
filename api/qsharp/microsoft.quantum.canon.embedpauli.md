---
uid: Microsoft.Quantum.Canon.EmbedPauli
title: Embedpauli-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: EmbedPauli
qsharp.summary: Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.
ms.openlocfilehash: e9042ca9eac4b8791057037dc5698eb14deadd31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207036"
---
# <a name="embedpauli-function"></a><span data-ttu-id="6b35a-102">Embedpauli-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b35a-102">EmbedPauli function</span></span>

<span data-ttu-id="6b35a-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6b35a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6b35a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b35a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b35a-105">Gibt bei einem Single-Qubit-Pauli-Operator und dem Index eines Qubits einen multiqubit-Pauli-Operator mit dem angegebenen Single-Qubit-Operator an diesem Index und `PauliI` an jedem anderen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="6b35a-105">Given a single-qubit Pauli operator and the index of a qubit, returns a multi-qubit Pauli operator with the given single-qubit operator at that index and `PauliI` at every other index.</span></span>

```qsharp
function EmbedPauli (pauli : Pauli, location : Int, n : Int) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="6b35a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6b35a-106">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="6b35a-107">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="6b35a-107">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="6b35a-108">Ein Single-Qubit-Pauli-Operator, der an der angegebenen Position platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b35a-108">A single-qubit Pauli operator to be placed at the given location.</span></span>


### <a name="location--int"></a><span data-ttu-id="6b35a-109">Speicherort: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b35a-109">location : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6b35a-110">Ein Index `output[location] == pauli` , bei dem `output` die Ausgabe dieser Funktion ist.</span><span class="sxs-lookup"><span data-stu-id="6b35a-110">An index such that `output[location] == pauli`, where `output` is the output of this function.</span></span>


### <a name="n--int"></a><span data-ttu-id="6b35a-111">n: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6b35a-111">n : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6b35a-112">Länge des Arrays, das zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b35a-112">Length of the array to be returned.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="6b35a-113">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="6b35a-113">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

