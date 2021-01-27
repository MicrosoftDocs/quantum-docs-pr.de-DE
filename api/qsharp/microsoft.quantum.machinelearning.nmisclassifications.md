---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Nfehllassikationen-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: adc7042d6108c7ec72d13340633824d3eaf5e18e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853917"
---
# <a name="nmisclassifications-function"></a><span data-ttu-id="ea7b4-102">Nfehllassikationen-Funktion</span><span class="sxs-lookup"><span data-stu-id="ea7b4-102">NMisclassifications function</span></span>

<span data-ttu-id="ea7b4-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ea7b4-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ea7b4-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ea7b4-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="ea7b4-105">Gibt die Anzahl der Indizes zurück, bei denen sich die einzelnen Bezeichnungen unterscheiden, wenn eine Reihe von abhergelegten Bezeichnungen und ein Satz korrekter Bezeichnungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="ea7b4-105">Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.</span></span>

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a><span data-ttu-id="ea7b4-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ea7b4-106">Input</span></span>

### <a name="proposed--int"></a><span data-ttu-id="ea7b4-107">vorgeschlagen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ea7b4-107">proposed : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="actual--int"></a><span data-ttu-id="ea7b4-108">tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ea7b4-108">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--int"></a><span data-ttu-id="ea7b4-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea7b4-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ea7b4-110">Die Anzahl der Indizes `idx` `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="ea7b4-110">The number of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>

## <a name="example"></a><span data-ttu-id="ea7b4-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ea7b4-111">Example</span></span>

```qsharp
let nMisclassifications = NMisclassifications([1, 1, 0, 0], [0, 1, 1, 0]);
Message($"{nMisclassifications}"); // Will print 2.
```