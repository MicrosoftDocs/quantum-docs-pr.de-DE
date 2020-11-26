---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Maybechooeinelement-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 1a69c8d5a6ae022ceda9269e17434b740809b107
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192858"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="60dfd-102">Maybechooeinelement-Vorgang</span><span class="sxs-lookup"><span data-stu-id="60dfd-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="60dfd-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="60dfd-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="60dfd-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="60dfd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="60dfd-105">Wenn ein Array von Daten und eine Verteilung über die Indizes verfügen, versucht, ein Element nach dem Zufallsprinzip auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="60dfd-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="60dfd-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="60dfd-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="60dfd-107">Daten: 't []</span><span class="sxs-lookup"><span data-stu-id="60dfd-107">data : 'T[]</span></span>

<span data-ttu-id="60dfd-108">Das Array, aus dem ein Element ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="60dfd-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="60dfd-109">indexdistribution: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="60dfd-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="60dfd-110">Eine Verteilung über die Indizes von `data` .</span><span class="sxs-lookup"><span data-stu-id="60dfd-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="60dfd-111">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="60dfd-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="60dfd-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="60dfd-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="60dfd-113">GIF</span><span class="sxs-lookup"><span data-stu-id="60dfd-113">'T</span></span>

