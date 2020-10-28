---
uid: Microsoft.Quantum.MachineLearning._UpdatedBias
title: _UpdatedBias-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _UpdatedBias
qsharp.summary: Returns a bias value that leads to near-minimum misclassification score.
ms.openlocfilehash: 2704d08e4c1ce868e1fd9065c3cab0285d431094
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706906"
---
# <a name="_updatedbias-function"></a><span data-ttu-id="34141-102">_UpdatedBias-Funktion</span><span class="sxs-lookup"><span data-stu-id="34141-102">_UpdatedBias function</span></span>

<span data-ttu-id="34141-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="34141-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="34141-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="34141-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="34141-105">Gibt einen Bias-Wert zurück, der zu einer fast minimalen fehl Klassifizierungs Bewertung führt.</span><span class="sxs-lookup"><span data-stu-id="34141-105">Returns a bias value that leads to near-minimum misclassification score.</span></span>

```qsharp
function _UpdatedBias (labeledProbabilities : (Double, Int)[], bias : Double, tolerance : Double) : Double
```


## <a name="input"></a><span data-ttu-id="34141-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34141-106">Input</span></span>

### <a name="labeledprobabilities--doubleint"></a><span data-ttu-id="34141-107">labeledprobabili: ([Double](xref:microsoft.quantum.lang-ref.double),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="34141-107">labeledProbabilities : ([Double](xref:microsoft.quantum.lang-ref.double),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>




### <a name="bias--double"></a><span data-ttu-id="34141-108">Bias: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="34141-108">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="tolerance--double"></a><span data-ttu-id="34141-109">Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="34141-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>





## <a name="output--double"></a><span data-ttu-id="34141-110">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="34141-110">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

