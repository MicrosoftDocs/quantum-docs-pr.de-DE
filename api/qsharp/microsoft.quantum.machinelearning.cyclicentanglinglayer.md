---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Zyklicentanglinglayer-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 6e0f5057b35baefe2677126ba70ee4fddde7d4db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706871"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="b3be5-102">Zyklicentanglinglayer-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3be5-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="b3be5-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="b3be5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="b3be5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b3be5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b3be5-105">Gibt ein Array von einzeln kontrollierten Drehungen entlang einer angegebenen Achse zurück, das zyklisch über ein Register von Qubits angeordnet und durch unterschiedliche Modellparameter parametrisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b3be5-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="b3be5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3be5-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="b3be5-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b3be5-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b3be5-108">Die Anzahl der Qubits, die durch die angegebene Ebene bearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="b3be5-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="b3be5-109">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="b3be5-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="b3be5-110">Die Drehungs Achse für jede Drehung in der angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="b3be5-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="b3be5-111">Stride: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b3be5-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b3be5-112">Die Trennung zwischen den Ziel-und Steuerelement Indizes für jede Drehung.</span><span class="sxs-lookup"><span data-stu-id="b3be5-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="b3be5-113">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="b3be5-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="b3be5-114">Ein Array von zwei-Qubit-gesteuerten Rotationen, das zyklisch über ein Register von `nQubits` Qubits angelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b3be5-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>