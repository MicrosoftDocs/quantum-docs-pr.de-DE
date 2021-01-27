---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: Localrotationslayer-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: a3658bbf62068c9eea2d9b763cbff5596f426135
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854980"
---
# <a name="localrotationslayer-function"></a><span data-ttu-id="a81b7-102">Localrotationslayer-Funktion</span><span class="sxs-lookup"><span data-stu-id="a81b7-102">LocalRotationsLayer function</span></span>

<span data-ttu-id="a81b7-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a81b7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="a81b7-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="a81b7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="a81b7-105">Gibt ein Array von unkontrollierten Rotationen (Single-Qubit) entlang einer angegebenen Achse zurück, wobei für jedes Qubit in einem Register eine Drehung durch unterschiedliche Modellparameter parametrisiert ist.</span><span class="sxs-lookup"><span data-stu-id="a81b7-105">Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.</span></span>

```qsharp
function LocalRotationsLayer (nQubits : Int, axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="a81b7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a81b7-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="a81b7-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a81b7-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a81b7-108">Die Anzahl der Qubits, die durch die angegebene Ebene bearbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="a81b7-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="a81b7-109">Achse: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="a81b7-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="a81b7-110">Die Drehungs Achse für jede Drehung in der angegebenen Ebene.</span><span class="sxs-lookup"><span data-stu-id="a81b7-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="a81b7-111">Ausgabe: [controlledrotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="a81b7-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="a81b7-112">Ein Array von kontrollierten Rotationen für die angegebene Achse, eines auf jedem der `nQubits` Qubits.</span><span class="sxs-lookup"><span data-stu-id="a81b7-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>