---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: Nqubistratrequired-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: d7ed687e9c75ed7cc71917aa1cdf32a6fbb93106
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723577"
---
# <a name="nqubitsrequired-function"></a><span data-ttu-id="70b2a-102">Nqubistratrequired-Funktion</span><span class="sxs-lookup"><span data-stu-id="70b2a-102">NQubitsRequired function</span></span>

<span data-ttu-id="70b2a-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="70b2a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="70b2a-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="70b2a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="70b2a-105">Gibt die Anzahl der zum Anwenden eines bestimmten sequenziellen Klassifizierers erforderlichen Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="70b2a-105">Returns the number of qubits required to apply a given sequential classifier.</span></span>

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a><span data-ttu-id="70b2a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="70b2a-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="70b2a-107">Modell: [sequentialmodel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="70b2a-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>





## <a name="output--int"></a><span data-ttu-id="70b2a-108">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="70b2a-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="70b2a-109">Die Mindestgröße eines Registers, für das der sequenzielle Klassifizierer angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="70b2a-109">The minimum size of a register on which the sequential classifier may be applied.</span></span>