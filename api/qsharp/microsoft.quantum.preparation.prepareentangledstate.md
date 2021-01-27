---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Prepareentangledstate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 9bf42131860b9fe9bd223ade32f95ec747abefe8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854363"
---
# <a name="prepareentangledstate-operation"></a><span data-ttu-id="248b8-102">Prepareentangledstate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="248b8-102">PrepareEntangledState operation</span></span>

<span data-ttu-id="248b8-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="248b8-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="248b8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="248b8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="248b8-105">Paar Weise entwinkel zwei Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="248b8-105">Pairwise entangles two qubit registers.</span></span>

<span data-ttu-id="248b8-106">Das heißt, wenn zwei Register vorhanden sind, wird der Status "$ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $" zwischen jedem Paar von Qubits in den entsprechenden Registern vorbereitet, wobei angenommen wird, dass jedes Register im Zustand "$ \ket{0\cdots 0} $" beginnt.</span><span class="sxs-lookup"><span data-stu-id="248b8-106">That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.</span></span>

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="248b8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="248b8-107">Input</span></span>

### <a name="left--qubit"></a><span data-ttu-id="248b8-108">Left: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="248b8-108">left : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="248b8-109">Ein Qubit-Array im $ \ket{0\cdots 0} $-Status</span><span class="sxs-lookup"><span data-stu-id="248b8-109">A qubit array in the $\ket{0\cdots 0}$ state</span></span>


### <a name="right--qubit"></a><span data-ttu-id="248b8-110">Right: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="248b8-110">right : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="248b8-111">Ein Qubit-Array im $ \ket{0\cdots 0} $-Status</span><span class="sxs-lookup"><span data-stu-id="248b8-111">A qubit array in the $\ket{0\cdots 0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="248b8-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="248b8-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

