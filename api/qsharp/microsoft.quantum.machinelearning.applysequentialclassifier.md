---
uid: Microsoft.Quantum.MachineLearning.ApplySequentialClassifier
title: Applysequentialclassifier-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApplySequentialClassifier
qsharp.summary: Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.
ms.openlocfilehash: 1b4b4853491489f11f222507bb14b48e941e7859
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706895"
---
# <a name="applysequentialclassifier-operation"></a><span data-ttu-id="eb2de-102">Applysequentialclassifier-Vorgang</span><span class="sxs-lookup"><span data-stu-id="eb2de-102">ApplySequentialClassifier operation</span></span>

<span data-ttu-id="eb2de-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="eb2de-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="eb2de-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eb2de-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eb2de-105">Bei der Struktur und Parametrisierung eines sequenziellen Klassifizierers wendet den Klassifizierer auf ein Register von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="eb2de-105">Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.</span></span>

```qsharp
operation ApplySequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="eb2de-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="eb2de-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="eb2de-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="eb2de-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="eb2de-108">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="eb2de-108">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eb2de-109">Ein Ziel Register, auf das der Klassifizierer angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb2de-109">A target register to which the classifier should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb2de-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb2de-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

