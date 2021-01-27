---
uid: Microsoft.Quantum.MachineLearning.InferredLabels
title: Inferredlabels-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabels
qsharp.summary: Given an array of classification probabilities and a bias, returns the label inferred from each probability.
ms.openlocfilehash: 576b4b1f11fc21476bbb019d4b0326981294528c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848406"
---
# <a name="inferredlabels-function"></a><span data-ttu-id="8a85f-102">Inferredlabels-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a85f-102">InferredLabels function</span></span>

<span data-ttu-id="8a85f-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8a85f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="8a85f-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="8a85f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="8a85f-105">Gibt ein Array von Klassifizierungs Wahrscheinlichkeiten und eine Abweichung zurück und gibt die Bezeichnung zurück, die aus jeder Wahrscheinlichkeit abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8a85f-105">Given an array of classification probabilities and a bias, returns the label inferred from each probability.</span></span>

```qsharp
function InferredLabels (bias : Double, probabilities : Double[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="8a85f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8a85f-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="8a85f-107">Bias: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8a85f-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8a85f-108">Die Verschiebung zwischen zwei Klassen, in der Regel das Ergebnis des Trainings eines Klassifizierers.</span><span class="sxs-lookup"><span data-stu-id="8a85f-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probabilities--double"></a><span data-ttu-id="8a85f-109">Wahrscheinlichkeiten: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8a85f-109">probabilities : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8a85f-110">Ein Array von Klassifizierungs Wahrscheinlichkeiten für eine Reihe von Beispielen, die sich in der Regel aus der Schätzung von Klassifizierungs Frequenzen ergeben.</span><span class="sxs-lookup"><span data-stu-id="8a85f-110">An array of classification probabilities for a set of samples, typically resulting from estimating classification frequencies.</span></span>



## <a name="output--int"></a><span data-ttu-id="8a85f-111">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="8a85f-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="8a85f-112">Die Bezeichnung, die von den einzelnen Klassifizierungs Wahrscheinlichkeiten abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8a85f-112">The label inferred from each classification probability.</span></span>