---
uid: Microsoft.Quantum.MachineLearning.ControlledRotation
title: Benutzerdefinierter controlledrotation-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ControlledRotation
qsharp.summary: Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.
ms.openlocfilehash: afc425c16ab550fd414e656484c9ff6f0f8f3ef4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702065"
---
# <a name="controlledrotation-user-defined-type"></a><span data-ttu-id="9d1e5-102">Benutzerdefinierter controlledrotation-Typ</span><span class="sxs-lookup"><span data-stu-id="9d1e5-102">ControlledRotation user defined type</span></span>

<span data-ttu-id="9d1e5-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="9d1e5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="9d1e5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d1e5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d1e5-105">Beschreibt eine gesteuerte Drehung in Bezug auf die Ziel-und Steuerelement Indizes, die Drehungs Achse und den Index in einen Modellparameter Vektor.</span><span class="sxs-lookup"><span data-stu-id="9d1e5-105">Describes a controlled rotation in terms of its target and control indices, rotation axis, and index into a model parameter vector.</span></span>

```qsharp

newtype ControlledRotation = ((TargetIndex : Int, ControlIndices : Int[]), Axis : Pauli, ParameterIndex : Int);
```



## <a name="named-items"></a><span data-ttu-id="9d1e5-106">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="9d1e5-106">Named Items</span></span>

### <a name="targetindex--int"></a><span data-ttu-id="9d1e5-107">TargetIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9d1e5-107">TargetIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9d1e5-108">Index des zielqubits für diese gesteuerte Drehung.</span><span class="sxs-lookup"><span data-stu-id="9d1e5-108">Index of the target qubit for this controlled rotation.</span></span>
### <a name="controlindices--int"></a><span data-ttu-id="9d1e5-109">Controlindices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9d1e5-109">ControlIndices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9d1e5-110">Ein Array der-Steuerelement-Qubit-Indizes für diese Drehung.</span><span class="sxs-lookup"><span data-stu-id="9d1e5-110">An array of the control qubit indices for this rotation.</span></span>
### <a name="axis--pauli"></a><span data-ttu-id="9d1e5-111">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="9d1e5-111">Axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="9d1e5-112">Die Achse für diese Drehung.</span><span class="sxs-lookup"><span data-stu-id="9d1e5-112">The axis for this rotation.</span></span>
### <a name="parameterindex--int"></a><span data-ttu-id="9d1e5-113">Parameterindex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9d1e5-113">ParameterIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9d1e5-114">Ein Index in einem Modellparameter Vektor, der den Winkel für diese Drehung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9d1e5-114">An index into a model parameter vector describing the angle for this rotation.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d1e5-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d1e5-115">Remarks</span></span>

<span data-ttu-id="9d1e5-116">Eine unkontrollierte Drehung kann dargestellt werden, indem `ControlIndices` auf ein leeres Array von Indizes festgelegt wird `new Int[0]` .</span><span class="sxs-lookup"><span data-stu-id="9d1e5-116">An uncontrolled rotation can be represented by setting `ControlIndices` to an empty array of indexes, `new Int[0]`.</span></span>