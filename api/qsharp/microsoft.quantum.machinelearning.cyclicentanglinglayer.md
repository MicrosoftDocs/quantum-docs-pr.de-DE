---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: Zyklicentanglinglayer-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5d0af0a60217b69dc7eb8ece8952f2a7f0c09280
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847382"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="57528-102">Zyklicentanglinglayer-Funktion</span><span class="sxs-lookup"><span data-stu-id="57528-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="57528-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="57528-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="57528-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="57528-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="57528-105">Gibt ein Array von einzeln kontrollierten Drehungen entlang einer angegebenen Achse zurück, das zyklisch über ein Register von Qubits angeordnet und durch unterschiedliche Modellparameter parametrisiert wird.</span><span class="sxs-lookup"><span data-stu-id="57528-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="57528-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="57528-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="57528-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57528-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57528-108">Die Anzahl der Qubits, die durch die angegebene Ebene bearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="57528-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="57528-109">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="57528-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="57528-110">Die Drehungs Achse für jede Drehung in der angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="57528-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="57528-111">Stride: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57528-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57528-112">Die Trennung zwischen den Ziel-und Steuerelement Indizes für jede Drehung.</span><span class="sxs-lookup"><span data-stu-id="57528-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="57528-113">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="57528-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="57528-114">Ein Array von zwei-Qubit-gesteuerten Rotationen, das zyklisch über ein Register von `nQubits` Qubits angelegt ist.</span><span class="sxs-lookup"><span data-stu-id="57528-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>

## <a name="example"></a><span data-ttu-id="57528-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="57528-115">Example</span></span>

<span data-ttu-id="57528-116">Die folgenden sind gleichwertig:</span><span class="sxs-lookup"><span data-stu-id="57528-116">The following are equivalent:</span></span>

```qsharp
let layer = CyclicEntanglingLayer(3, PauliX, 2);
let layer = [
    ControlledRotation((0, [2]), PauliX, 0),
    ControlledRotation((1, [0]), PauliX, 1),
    ControlledRotation((2, [1]), PauliX, 2)
];
```