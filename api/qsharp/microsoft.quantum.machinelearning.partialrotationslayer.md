---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: Partialrotationslayer-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ab964d2c43a13a5daf64aefdeccd1c26cd371ff4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722430"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="69405-102">Partialrotationslayer-Funktion</span><span class="sxs-lookup"><span data-stu-id="69405-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="69405-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="69405-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="69405-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="69405-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="69405-105">Gibt ein Array von Single-Qubit-Drehungen entlang einer angegebenen Achse zurück, die durch unterschiedliche Modellparameter parametrisiert werden.</span><span class="sxs-lookup"><span data-stu-id="69405-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="69405-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="69405-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="69405-107">idxsqubits: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="69405-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="69405-108">Indizes für die Qubits, die als Ziele für jede Drehung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69405-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="69405-109">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="69405-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="69405-110">Die Drehungs Achse für jede Drehung in der angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="69405-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="69405-111">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="69405-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="69405-112">Ein Array von kontrollierten Rotationen für die angegebene Achse, eines auf jedem der `nQubits` Qubits.</span><span class="sxs-lookup"><span data-stu-id="69405-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>