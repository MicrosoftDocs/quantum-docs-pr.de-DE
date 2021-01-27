---
uid: Microsoft.Quantum.MachineLearning.ApplySequentialClassifier
title: Applysequentialclassifier-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApplySequentialClassifier
qsharp.summary: Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.
ms.openlocfilehash: 8186bc57e64a52e123bef8e3556d3385c4df7034
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851440"
---
# <a name="applysequentialclassifier-operation"></a><span data-ttu-id="7397a-102">Applysequentialclassifier-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7397a-102">ApplySequentialClassifier operation</span></span>

<span data-ttu-id="7397a-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7397a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="7397a-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="7397a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="7397a-105">Bei der Struktur und Parametrisierung eines sequenziellen Klassifizierers wendet den Klassifizierer auf ein Register von Qubits an.</span><span class="sxs-lookup"><span data-stu-id="7397a-105">Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.</span></span>

```qsharp
operation ApplySequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="7397a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7397a-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="7397a-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="7397a-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="7397a-108">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="7397a-108">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="7397a-109">Ein Ziel Register, auf das der Klassifizierer angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7397a-109">A target register to which the classifier should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="7397a-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7397a-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

