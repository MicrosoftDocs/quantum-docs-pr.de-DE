---
uid: Microsoft.Quantum.MachineLearning.Misclassifications
title: Funktion "falsch Klassifizierungen"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Misclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.
ms.openlocfilehash: 500c2910f7c5616c88ff6c70ab3cc16680e199fb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723578"
---
# <a name="misclassifications-function"></a><span data-ttu-id="25035-102">Funktion "falsch Klassifizierungen"</span><span class="sxs-lookup"><span data-stu-id="25035-102">Misclassifications function</span></span>

<span data-ttu-id="25035-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="25035-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="25035-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="25035-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="25035-105">Gibt einen Satz von abhergenten Bezeichnungen und einen Satz korrekter Bezeichnungen zurück, wenn jeder Satz von Bezeichnungen abweicht.</span><span class="sxs-lookup"><span data-stu-id="25035-105">Given a set of inferred labels and a set of correct labels, returns indices for where each set of labels differs.</span></span>

```qsharp
function Misclassifications (inferredLabels : Int[], actualLabels : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="25035-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25035-106">Input</span></span>

### <a name="inferredlabels--int"></a><span data-ttu-id="25035-107">inferredlabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25035-107">inferredLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25035-108">Die Bezeichnungen, die für eine bestimmte Schulung oder einen bestimmten Validierungs Satz abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="25035-108">The labels inferred for a given training or validation set.</span></span>


### <a name="actuallabels--int"></a><span data-ttu-id="25035-109">actuallabels: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25035-109">actualLabels : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25035-110">Die echten Bezeichnungen für eine bestimmte Schulung oder einen bestimmten Validierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="25035-110">The true labels for a given training or validation set.</span></span>



## <a name="output--int"></a><span data-ttu-id="25035-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25035-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25035-112">Ein Array von Indizes `idx` , die den Wert haben `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="25035-112">An array of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>