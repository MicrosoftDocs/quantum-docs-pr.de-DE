---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Partialrotationslayer-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ade0640b07f633982e98d5d02239fa205909bcce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196241"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="5d0e7-102">Partialrotationslayer-Funktion</span><span class="sxs-lookup"><span data-stu-id="5d0e7-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="5d0e7-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5d0e7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="5d0e7-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="5d0e7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="5d0e7-105">Gibt ein Array von Single-Qubit-Drehungen entlang einer angegebenen Achse zurück, die durch unterschiedliche Modellparameter parametrisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5d0e7-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="5d0e7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="5d0e7-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="5d0e7-107">idxsqubits: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="5d0e7-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="5d0e7-108">Indizes für die Qubits, die als Ziele für jede Drehung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5d0e7-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="5d0e7-109">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="5d0e7-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="5d0e7-110">Die Drehungs Achse für jede Drehung in der angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="5d0e7-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="5d0e7-111">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="5d0e7-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="5d0e7-112">Ein Array von kontrollierten Rotationen für die angegebene Achse, eines auf jedem der `nQubits` Qubits.</span><span class="sxs-lookup"><span data-stu-id="5d0e7-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>