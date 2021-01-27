---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: Applycnotchain-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: b5a74eb66529095233c89a4ec7ea37c996458cb4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841961"
---
# <a name="applycnotchain-operation"></a><span data-ttu-id="c76d9-102">Applycnotchain-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c76d9-102">ApplyCNOTChain operation</span></span>

<span data-ttu-id="c76d9-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c76d9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c76d9-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c76d9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c76d9-105">Berechnet die Parität eines Registers von Qubits direkt.</span><span class="sxs-lookup"><span data-stu-id="c76d9-105">Computes the parity of a register of qubits in-place.</span></span>

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="c76d9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c76d9-106">Description</span></span>

<span data-ttu-id="c76d9-107">Durch diesen Vorgang wird der Zustand der Eingabe in $ $ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{Q_ {n-1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus Q_ {n-1}}.</span><span class="sxs-lookup"><span data-stu-id="c76d9-107">This operation transforms the state of its input as $$ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{q_{n - 1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus q_{n - 1}}.</span></span>
<span data-ttu-id="c76d9-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="c76d9-108">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="c76d9-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c76d9-109">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="c76d9-110">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c76d9-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c76d9-111">Ein Array von Qubits, dessen Parität berechnet und gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c76d9-111">Array of qubits whose parity is to be computed and stored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c76d9-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c76d9-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

