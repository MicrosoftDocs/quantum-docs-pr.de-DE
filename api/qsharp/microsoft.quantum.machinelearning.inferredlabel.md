---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: Inferredlabel-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: b64bb1ec52d2456ee1b627b920890223d173533b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211779"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="917a1-102">Inferredlabel-Funktion</span><span class="sxs-lookup"><span data-stu-id="917a1-102">InferredLabel function</span></span>

<span data-ttu-id="917a1-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="917a1-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="917a1-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="917a1-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="917a1-105">Gibt bei einer Klassifizierungs Wahrscheinlichkeit und einem Bias die Bezeichnung zurück, die von dieser Wahrscheinlichkeit abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="917a1-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="917a1-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="917a1-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="917a1-107">Bias: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="917a1-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="917a1-108">Die Verschiebung zwischen zwei Klassen, in der Regel das Ergebnis des Trainings eines Klassifizierers.</span><span class="sxs-lookup"><span data-stu-id="917a1-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="917a1-109">Wahrscheinlichkeit: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="917a1-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="917a1-110">Eine Klassifizierungs Wahrscheinlichkeiten für ein bestimmtes Beispiel, die sich in der Regel aus der Schätzung der Klassifizierungs Häufigkeit ergibt.</span><span class="sxs-lookup"><span data-stu-id="917a1-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="917a1-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="917a1-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="917a1-112">Die Bezeichnung, die von der angegebenen Klassifizierungs Wahrscheinlichkeit abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="917a1-112">The label inferred from the given classification probability.</span></span>