---
uid: Microsoft.Quantum.Preparation.PrepareChoiState
title: Preparechoistate-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareChoiState
qsharp.summary: Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.
ms.openlocfilehash: ced71c4278f42f577760acd54ae53e7f5e6dae4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210572"
---
# <a name="preparechoistate-operation"></a><span data-ttu-id="d4cd2-102">Preparechoistate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d4cd2-102">PrepareChoiState operation</span></span>

<span data-ttu-id="d4cd2-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d4cd2-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d4cd2-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d4cd2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d4cd2-105">Bereitet den Status "Choi – jamiołkowski" für einen bestimmten Vorgang auf angegebene Verweis-und Ziel Register vor.</span><span class="sxs-lookup"><span data-stu-id="d4cd2-105">Prepares the Choi–Jamiołkowski state for a given operation onto given reference and target registers.</span></span>

```qsharp
operation PrepareChoiState (op : (Qubit[] => Unit), reference : Qubit[], target : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d4cd2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d4cd2-106">Input</span></span>

### <a name="op--qubit--unit"></a><span data-ttu-id="d4cd2-107">OP: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4cd2-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d4cd2-108">Der Vorgang $ \lambda $, dessen Metadaten– jamiołkowski State $J (\lambda)/2 ^ N $ vorbereitet werden soll, wobei $N $ die Anzahl der Qubits ist, die von verwendet werden `op` .</span><span class="sxs-lookup"><span data-stu-id="d4cd2-108">Operation $\Lambda$ whose Choi–Jamiołkowski state $J(\Lambda) / 2^N$ is to be prepared, where $N$ is the number of qubits on which `op` acts.</span></span>


### <a name="reference--qubit"></a><span data-ttu-id="d4cd2-109">Verweis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4cd2-109">reference : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d4cd2-110">Ein Register von Qubits, beginnend mit dem Status $ \ket{00\cdots 0} $, der als Verweis für die Aktion von verwendet werden soll `op` .</span><span class="sxs-lookup"><span data-stu-id="d4cd2-110">A register of qubits starting in the $\ket{00\cdots 0}$ state to be used as a reference for the action of `op`.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d4cd2-111">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d4cd2-111">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d4cd2-112">Ein Register von Qubits, das anfänglich im $ \ket{00\cdots 0} $-Zustand `op` ist, in dem Sie angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4cd2-112">A register of qubits initially in the $\ket{00\cdots 0}$ state on which `op` is to be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4cd2-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4cd2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d4cd2-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4cd2-114">Remarks</span></span>

<span data-ttu-id="d4cd2-115">Der Bundesstaat Choi – jamiłkowski $J (\lambda) $ eines Quantum-Prozesses ist als $ $ \begin{align} J (\lambda) \mathrel{: =} (\boldone \otimes \lambda) (| \boldone\rangle \! \rangle\langle \! \langle\boldone |), \end{align} $ $ WHERE $ | X\rangle \! \rangle $ ist die *Vektorisierung* einer Matrix $X $ in der spaltenstapel Konvention.</span><span class="sxs-lookup"><span data-stu-id="d4cd2-115">The Choi–Jamiłkowski state $J(\Lambda)$ of a quantum process is defined as $$ \begin{align} J(\Lambda) \mathrel{:=} (\boldone \otimes \Lambda) (|\boldone\rangle\!\rangle\langle\!\langle\boldone|), \end{align} $$ where $|X\rangle\!\rangle$ is the *vectorization* of a matrix $X$ in the column-stacking convention.</span></span> <span data-ttu-id="d4cd2-116">Das Erlernen einer klassischen Beschreibung dieses Zustands enthält vollständige Informationen zu den Auswirkungen von $ \lambda $, die auf beliebige Eingabe Zustände reagieren, und bildet die Grundlage der *Quantum-Prozess Tomographie*.</span><span class="sxs-lookup"><span data-stu-id="d4cd2-116">Learning a classical description of this state provides full information about the effect of $\Lambda$ acting on arbitrary input states, and forms the foundation of *quantum process tomography*.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4cd2-117">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4cd2-117">See Also</span></span>

- [<span data-ttu-id="d4cd2-118">Microsoft. Quantum. Preparation. preparechoistatuea</span><span class="sxs-lookup"><span data-stu-id="d4cd2-118">Microsoft.Quantum.Preparation.PrepareChoiStateA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateA)
- [<span data-ttu-id="d4cd2-119">Microsoft. Quantum. Preparation. preparechoistatus EC</span><span class="sxs-lookup"><span data-stu-id="d4cd2-119">Microsoft.Quantum.Preparation.PrepareChoiStateC</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateC)
- [<span data-ttu-id="d4cd2-120">Microsoft. Quantum. Preparation. preparechoistatueca</span><span class="sxs-lookup"><span data-stu-id="d4cd2-120">Microsoft.Quantum.Preparation.PrepareChoiStateCA</span></span>](xref:Microsoft.Quantum.Preparation.PrepareChoiStateCA)