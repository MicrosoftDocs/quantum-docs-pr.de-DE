---
uid: Microsoft.Quantum.Canon.ApplyFermionicSWAP
title: Applyfermionicswap-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyFermionicSWAP
qsharp.summary: Applies the Fermionic SWAP.
ms.openlocfilehash: 25dd91b200700d1474cf27bf1d0fa71d57f2e09b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705378"
---
# <a name="applyfermionicswap-operation"></a><span data-ttu-id="430c2-102">Applyfermionicswap-Vorgang</span><span class="sxs-lookup"><span data-stu-id="430c2-102">ApplyFermionicSWAP operation</span></span>

<span data-ttu-id="430c2-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="430c2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="430c2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="430c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="430c2-105">Wendet den fermionic-Swap an.</span><span class="sxs-lookup"><span data-stu-id="430c2-105">Applies the Fermionic SWAP.</span></span>

```qsharp
operation ApplyFermionicSWAP (qubit1 : Qubit, qubit2 : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="430c2-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="430c2-106">Description</span></span>

<span data-ttu-id="430c2-107">Dies vertauscht die Qubits im Wesentlichen beim Anwenden einer globalen Phase von-1, wenn beide Qubits 1 s sind.</span><span class="sxs-lookup"><span data-stu-id="430c2-107">This essentially swaps the qubits while applying a global phase of -1 if both qubits are 1s.</span></span> <span data-ttu-id="430c2-108">Behält die antisymmetrisierung von orbitalen bei.</span><span class="sxs-lookup"><span data-stu-id="430c2-108">Preserves anti-symmetrization of orbitals.</span></span>
<span data-ttu-id="430c2-109">Weitere Informationen finden Sie unter .</span><span class="sxs-lookup"><span data-stu-id="430c2-109">See  for more information.</span></span>

<span data-ttu-id="430c2-110">Dieser Vorgang wird durch den einheitlichen Operator \begin{align} F_ {Swap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 &-1 \\ \\ \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="430c2-110">This operation is represented by the unitary operator \begin{align} f_{swap} \mathrel{:=} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & -1 \\\\ \end{bmatrix}.</span></span>
<span data-ttu-id="430c2-111">\end{align}</span><span class="sxs-lookup"><span data-stu-id="430c2-111">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="430c2-112">Eingabe</span><span class="sxs-lookup"><span data-stu-id="430c2-112">Input</span></span>

### <a name="qubit1--qubit"></a><span data-ttu-id="430c2-113">qubit1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="430c2-113">qubit1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="430c2-114">Das erste Qubit, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="430c2-114">The first qubit to be swapped.</span></span>


### <a name="qubit2--qubit"></a><span data-ttu-id="430c2-115">qubit2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="430c2-115">qubit2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="430c2-116">Das zweite Qubit, das ausgetauscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="430c2-116">The second qubit to be swapped.</span></span>



## <a name="output--unit"></a><span data-ttu-id="430c2-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="430c2-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="430c2-118">Referenzen</span><span class="sxs-lookup"><span data-stu-id="430c2-118">References</span></span>

- [<span data-ttu-id="430c2-119">*Ryan babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut netven, Garnet Kin-Lic Chan* , arXiv: 1706.00023</span><span class="sxs-lookup"><span data-stu-id="430c2-119"> *Ryan Babbush, Nathan Wiebe, Jarrod McClean, James McClain, Hartmut Neven, Garnet Kin-Lic Chan* , arXiv:1706.00023 </span></span>](https://arxiv.org/pdf/1706.00023.pdf)

## <a name="see-also"></a><span data-ttu-id="430c2-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="430c2-120">See Also</span></span>

- [<span data-ttu-id="430c2-121">Microsoft. Quantum. intrinsisch. Swap</span><span class="sxs-lookup"><span data-stu-id="430c2-121">Microsoft.Quantum.Intrinsic.SWAP</span></span>](xref:Microsoft.Quantum.Intrinsic.SWAP)