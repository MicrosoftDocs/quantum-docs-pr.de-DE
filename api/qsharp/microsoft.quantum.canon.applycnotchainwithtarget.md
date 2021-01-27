---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Applycnotchainwithtarget-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: ba1a4e99c411a4718b5a09fdcd57a7239eb4dbd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845118"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="7bbaa-102">Applycnotchainwithtarget-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7bbaa-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="7bbaa-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7bbaa-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7bbaa-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7bbaa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7bbaa-105">Berechnet die Parität eines Arrays von Qubits in einem Ziel-Qubit.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="7bbaa-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bbaa-106">Description</span></span>

<span data-ttu-id="7bbaa-107">Wenn sich das Array anfänglich im Status $ \ket{q_0} \ket{q_1} \cdots \ket{Q_ {\text{Target}}} $ befindet, wird der endgültige Zustand durch $ \ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{Q_ {n-1} \oplus \cdots \oplus q_0 \oplus Q_ {\text{target}}} $ angegeben.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="7bbaa-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7bbaa-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="7bbaa-109">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7bbaa-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7bbaa-110">Array von Qubits, für das die Parität berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="7bbaa-111">targetqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7bbaa-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7bbaa-112">Endgültiges Qubit, in das die Parität von ' Qubits ' XoReD ist.</span><span class="sxs-lookup"><span data-stu-id="7bbaa-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7bbaa-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7bbaa-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="7bbaa-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bbaa-114">Remarks</span></span>

<span data-ttu-id="7bbaa-115">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="7bbaa-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="7bbaa-116">and</span><span class="sxs-lookup"><span data-stu-id="7bbaa-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```