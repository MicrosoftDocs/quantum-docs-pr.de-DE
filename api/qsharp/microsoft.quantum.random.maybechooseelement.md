---
uid: Microsoft.Quantum.Random.MaybeChooseElement
title: Maybechooeinelement-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: MaybeChooseElement
qsharp.summary: Given an array of data and an a distribution over its indices, attempts to choose an element at random.
ms.openlocfilehash: 86a69110fc92a2b6238cc757c09185c9fbcdb035
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856117"
---
# <a name="maybechooseelement-operation"></a><span data-ttu-id="c1ae0-102">Maybechooeinelement-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c1ae0-102">MaybeChooseElement operation</span></span>

<span data-ttu-id="c1ae0-103">Namespace: [Microsoft. Quantum. Random](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="c1ae0-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="c1ae0-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c1ae0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c1ae0-105">Wenn ein Array von Daten und eine Verteilung über die Indizes verfügen, versucht, ein Element nach dem Zufallsprinzip auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c1ae0-105">Given an array of data and an a distribution over its indices, attempts to choose an element at random.</span></span>

```qsharp
operation MaybeChooseElement<'T> (data : 'T[], indexDistribution : Microsoft.Quantum.Random.DiscreteDistribution) : (Bool, 'T)
```


## <a name="input"></a><span data-ttu-id="c1ae0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1ae0-106">Input</span></span>

### <a name="data--t"></a><span data-ttu-id="c1ae0-107">Daten: 't []</span><span class="sxs-lookup"><span data-stu-id="c1ae0-107">data : 'T[]</span></span>

<span data-ttu-id="c1ae0-108">Das Array, aus dem ein Element ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c1ae0-108">The array from which an element should be chosen.</span></span>


### <a name="indexdistribution--discretedistribution"></a><span data-ttu-id="c1ae0-109">indexdistribution: [diskretedistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="c1ae0-109">indexDistribution : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="c1ae0-110">Eine Verteilung über die Indizes von `data` .</span><span class="sxs-lookup"><span data-stu-id="c1ae0-110">A distribution over the indices of `data`.</span></span>



## <a name="output--boolt"></a><span data-ttu-id="c1ae0-111">Ausgabe: ([bool](xref:microsoft.quantum.lang-ref.bool), 't)</span><span class="sxs-lookup"><span data-stu-id="c1ae0-111">Output : ([Bool](xref:microsoft.quantum.lang-ref.bool),'T)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c1ae0-112">Typparameter</span><span class="sxs-lookup"><span data-stu-id="c1ae0-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c1ae0-113">GIF</span><span class="sxs-lookup"><span data-stu-id="c1ae0-113">'T</span></span>



## <a name="example"></a><span data-ttu-id="c1ae0-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c1ae0-114">Example</span></span>

<span data-ttu-id="c1ae0-115">Der folgende f #-Ausschnitt wählt ein Element zufällig aus einem Array aus:</span><span class="sxs-lookup"><span data-stu-id="c1ae0-115">The following Q# snippet chooses an element at random from an array:</span></span>

```qsharp
let (succeeded, element) = MaybeChooseElement(
    data,
    DiscreteUniformDistribution(0, Length(data) - 1)
);
Fact(succeeded, "Index chosen by MaybeChooseElement was not valid.");
```