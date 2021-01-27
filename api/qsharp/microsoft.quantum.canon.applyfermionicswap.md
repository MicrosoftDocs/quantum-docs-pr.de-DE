---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Applyfermionicswap-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 334f407a32dabc8f4e0a1a29c8f06a1b9f40dc59
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845055"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="be374-102">Applyfermionicswap-Vorgang</span><span class="sxs-lookup"><span data-stu-id="be374-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="be374-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be374-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be374-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be374-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be374-105">Wendet den fermionic-Swap an.</span><span class="sxs-lookup"><span data-stu-id="be374-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="be374-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be374-106">Description</span></span>

<span data-ttu-id="be374-107">Dies vertauscht die Qubits im Wesentlichen beim Anwenden einer globalen Phase von-1, wenn beide Qubits 1 s sind.</span><span class="sxs-lookup"><span data-stu-id="be374-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="be374-108">Behält die antisymmetrisierung von orbitalen bei.</span><span class="sxs-lookup"><span data-stu-id="be374-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="be374-109">Weitere Informationen finden Sie unter .</span><span class="sxs-lookup"><span data-stu-id="be374-109">See  for more information.</span></span>

<span data-ttu-id="be374-110">Dieser Vorgang wird durch den einheitlichen Operator \begin{align} F_ {Swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="be374-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="be374-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="be374-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="be374-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="be374-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="be374-113">qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="be374-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="be374-114">Das erste Qubit, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="be374-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="be374-115">qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="be374-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="be374-116">Das zweite Qubit, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="be374-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be374-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be374-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="be374-118">References</span><span class="sxs-lookup"><span data-stu-id="be374-118">References</span></span>

- [<span data-ttu-id="be374-119">*Ryan babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut netven, Garnet Kin-Lic Chan*, arXiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="be374-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan*, arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="be374-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="be374-120">See Also</span></span>

- [<span data-ttu-id="be374-121">Microsoft. Quantum. intrinsisch. Swap</span><span class="sxs-lookup"><span data-stu-id="be374-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)