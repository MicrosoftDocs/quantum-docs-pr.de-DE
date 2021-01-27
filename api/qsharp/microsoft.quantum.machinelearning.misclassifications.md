---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Funktion "falsch Klassifizierungen"
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 3913395fbd9f7cf96732c17ca0c726289e5087ed
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853929"
---
# <a name="misclassifications-function"></a><span data-ttu-id="dc940-102">Funktion "falsch Klassifizierungen"</span><span class="sxs-lookup"><span data-stu-id="dc940-102">Misclassifications function</span></span>

<span data-ttu-id="dc940-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dc940-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="dc940-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="dc940-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="dc940-105">Gibt einen Satz von abhergenten Bezeichnungen und einen Satz korrekter Bezeichnungen zurück, wenn jeder Satz von Bezeichnungen abweicht.</span><span class="sxs-lookup"><span data-stu-id="dc940-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="dc940-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="dc940-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="dc940-107">inferredlabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dc940-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dc940-108">Die Bezeichnungen, die für eine bestimmte Schulung oder einen bestimmten Validierungs Satz abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="dc940-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="dc940-109">actuallabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dc940-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dc940-110">Die echten Bezeichnungen für eine bestimmte Schulung oder einen bestimmten Validierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="dc940-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="dc940-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="dc940-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="dc940-112">Ein Array von Indizes `idx` , die den Wert haben `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="dc940-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>

## <a name="example"></a><span data-ttu-id="dc940-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dc940-113">Example</span></span>

```qsharp
let misclassifications = Misclassifications([0, 1, 0, 0], [0, 1, 1, 0]);
Message($"{misclassifications}"); // Will print [2].
```