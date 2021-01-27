---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Partialrotationslayer-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852919"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="71ac4-102">Partialrotationslayer-Funktion</span><span class="sxs-lookup"><span data-stu-id="71ac4-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="71ac4-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="71ac4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="71ac4-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="71ac4-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="71ac4-105">Gibt ein Array von Single-Qubit-Drehungen entlang einer angegebenen Achse zurück, die durch unterschiedliche Modellparameter parametrisiert werden.</span><span class="sxs-lookup"><span data-stu-id="71ac4-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="71ac4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71ac4-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="71ac4-107">idxsqubits: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="71ac4-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="71ac4-108">Indizes für die Qubits, die als Ziele für jede Drehung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71ac4-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="71ac4-109">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="71ac4-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="71ac4-110">Die Drehungs Achse für jede Drehung in der angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="71ac4-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="71ac4-111">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="71ac4-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="71ac4-112">Ein Array von kontrollierten Rotationen für die angegebene Achse, eines auf jedem der `nQubits` Qubits.</span><span class="sxs-lookup"><span data-stu-id="71ac4-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>