---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Applylowdepthand-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 092a350e42d8d90942de13530fefd761b5187e1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705207"
---
# <a name="applylowdepthand-operation"></a><span data-ttu-id="e5a68-102">Applylowdepthand-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e5a68-102">ApplyLowDepthAnd operation</span></span>

<span data-ttu-id="e5a68-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e5a68-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e5a68-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e5a68-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e5a68-105">Kehrt ein angegebenes Ziel-Qubit nur dann ein, wenn beide Steuerelement-Qubits den Status 1 aufweisen, mit T-Tiefe 1 und mithilfe von Messungen zum Ausführen der Adjoint-Operation.</span><span class="sxs-lookup"><span data-stu-id="e5a68-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="e5a68-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5a68-106">Description</span></span>

<span data-ttu-id="e5a68-107">Kehrt `target` nur dann zu, wenn beide Steuerelemente 1 sind, jedoch wird davon ausgegangen, dass `target` sich der Status 0 (null) befindet.</span><span class="sxs-lookup"><span data-stu-id="e5a68-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="e5a68-108">Der Vorgang verfügt über t-count 4, t-Tiefe 1 und erfordert ein Hilfsobjekt und ist daher möglicherweise einem ccnot-Vorgang vorzuziehen, wenn `target` bekanntermaßen 0 ist.</span><span class="sxs-lookup"><span data-stu-id="e5a68-108">The operation has T-count 4, T-depth 1 and requires one helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="e5a68-109">Das Hilfsobjekt dieses Vorgangs ist Messungs basiert und erfordert keine T-Gates und kein Hilfsobjekt.</span><span class="sxs-lookup"><span data-stu-id="e5a68-109">The adjoint of this operation is measurement based and requires no T gates, and no helper qubit.</span></span>

## <a name="input"></a><span data-ttu-id="e5a68-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e5a68-110">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="e5a68-111">Control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e5a68-111">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e5a68-112">Qubit für erstes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e5a68-112">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="e5a68-113">Control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e5a68-113">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e5a68-114">Qubit für zweites Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e5a68-114">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="e5a68-115">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e5a68-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e5a68-116">Zusätzliches Qubit für Ziel muss den Status 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e5a68-116">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="e5a68-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e5a68-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="e5a68-118">Referenzen</span><span class="sxs-lookup"><span data-stu-id="e5a68-118">References</span></span>

- <span data-ttu-id="e5a68-119">Cody Jones: "neuartige Konstruktionen für das Fault-tolerante yffoli Gate", Phys. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) doi: 10.1103/physreva. 87.022328</span><span class="sxs-lookup"><span data-stu-id="e5a68-119">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="e5a68-120">Peter Selinger: "Quantum-Leitungen von T-tiefen One", Phys. Rev. A 87, 042302, 2013 [arXiv: 1210.0974](https://arxiv.org/abs/1210.0974) doi: 10.1103/physreva. 87.042302</span><span class="sxs-lookup"><span data-stu-id="e5a68-120">Peter Selinger: "Quantum circuits of T-depth one", Phys. Rev. A 87, 042302, 2013 [arXiv:1210.0974](https://arxiv.org/abs/1210.0974) doi:10.1103/PhysRevA.87.042302</span></span>