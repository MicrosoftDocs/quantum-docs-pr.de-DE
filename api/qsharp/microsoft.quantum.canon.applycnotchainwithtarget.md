---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Applycnotchainwithtarget-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: fd0a0f3e1db89946aec2c63f3cde7a021608eea5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705439"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="f9ab7-102">Applycnotchainwithtarget-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f9ab7-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="f9ab7-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f9ab7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f9ab7-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f9ab7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f9ab7-105">Berechnet die Parität eines Arrays von Qubits in einem Ziel-Qubit.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="f9ab7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9ab7-106">Description</span></span>

<span data-ttu-id="f9ab7-107">Wenn sich das Array anfänglich im Status $ \ket{q_0} \ket{q_1} \cdots \ket{Q_ {\text{Target}}} $ befindet, wird der endgültige Zustand durch $ \ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{Q_ {n-1} \oplus \cdots \oplus q_0 \oplus Q_ {\text{target}}} $ angegeben.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="f9ab7-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f9ab7-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="f9ab7-109">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f9ab7-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f9ab7-110">Array von Qubits, für das die Parität berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="f9ab7-111">targetqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f9ab7-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f9ab7-112">Endgültiges Qubit, in das die Parität von ' Qubits ' XoReD ist.</span><span class="sxs-lookup"><span data-stu-id="f9ab7-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f9ab7-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f9ab7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f9ab7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f9ab7-114">Remarks</span></span>

<span data-ttu-id="f9ab7-115">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="f9ab7-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="f9ab7-116">und</span><span class="sxs-lookup"><span data-stu-id="f9ab7-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```