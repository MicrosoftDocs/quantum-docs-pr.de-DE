---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Benutzerdefinierter controlledrotation-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: 231afe65da3640218cbc97b9d49eae21bf6e1786
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847391"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="f899c-102">Benutzerdefinierter controlledrotation-Typ</span><span class="sxs-lookup"><span data-stu-id="f899c-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="f899c-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f899c-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="f899c-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="f899c-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="f899c-105">Beschreibt eine gesteuerte Drehung in Bezug auf die Ziel-und Steuerelement Indizes, die Drehungs Achse und den Index in einen Modellparameter Vektor.</span><span class="sxs-lookup"><span data-stu-id="f899c-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="f899c-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="f899c-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="f899c-107">TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f899c-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f899c-108">Index des zielqubits für diese gesteuerte Drehung.</span><span class="sxs-lookup"><span data-stu-id="f899c-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="f899c-109">Controlindices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f899c-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f899c-110">Ein Array der-Steuerelement-Qubit-Indizes für diese Drehung.</span><span class="sxs-lookup"><span data-stu-id="f899c-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="f899c-111">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="f899c-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="f899c-112">Die Achse für diese Drehung.</span><span class="sxs-lookup"><span data-stu-id="f899c-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="f899c-113">Parameterindex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f899c-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f899c-114">Ein Index in einem Modellparameter Vektor, der den Winkel für diese Drehung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="f899c-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="example"></a><span data-ttu-id="f899c-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f899c-115">Example</span></span>

<span data-ttu-id="f899c-116">Folgendes stellt eine Drehung zum $X $-Achse des ersten Qubit in einem Register dar, gesteuert auf das zweite Qubit und mit einem Winkel, der durch den vierten Parameter in einem sequenziellen Modell angegeben wird:</span><span class="sxs-lookup"><span data-stu-id="f899c-116">The following represents a rotation about the $X$-axis of the first qubit in a register, controlled on the second qubit, and with an angle given by the fourth parameter in a sequential model:</span></span>

```qsharp
let controlledRotation = ControlledRotation(
    (0, [1]),
    PauliX,
    3
)
```

## <a name="remarks"></a><span data-ttu-id="f899c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f899c-117">Remarks</span></span>

<span data-ttu-id="f899c-118">Eine unkontrollierte Drehung kann dargestellt werden, indem `ControlIndices` auf ein leeres Array von Indizes festgelegt wird `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="f899c-118">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>