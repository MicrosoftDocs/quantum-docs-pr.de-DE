---
uid: Microsoft.Quantum.MachineLearning.NMisclassifications
title: Nfehllassikationen-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NMisclassifications
qsharp.summary: Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.
ms.openlocfilehash: 30d049ba54630cd2f5f350280bad7f587599f459
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196309"
---
# <a name="nmisclassifications-function"></a><span data-ttu-id="898b0-102">Nfehllassikationen-Funktion</span><span class="sxs-lookup"><span data-stu-id="898b0-102">NMisclassifications function</span></span>

<span data-ttu-id="898b0-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="898b0-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="898b0-104">Paket: [Microsoft. Quantum. machinelearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="898b0-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="898b0-105">Gibt die Anzahl der Indizes zurück, bei denen sich die einzelnen Bezeichnungen unterscheiden, wenn eine Reihe von abhergelegten Bezeichnungen und ein Satz korrekter Bezeichnungen angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="898b0-105">Given a set of inferred labels and a set of correct labels, returns the number of indices at which each set of labels differ.</span></span>

```qsharp
function NMisclassifications (proposed : Int[], actual : Int[]) : Int
```


## <a name="input"></a><span data-ttu-id="898b0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="898b0-106">Input</span></span>

### <a name="proposed--int"></a><span data-ttu-id="898b0-107">vorgeschlagen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="898b0-107">proposed : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="actual--int"></a><span data-ttu-id="898b0-108">tatsächlicher Wert: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="898b0-108">actual : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>





## <a name="output--int"></a><span data-ttu-id="898b0-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="898b0-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="898b0-110">Die Anzahl der Indizes `idx` `inferredLabels[idx] != actualLabels[idx]` .</span><span class="sxs-lookup"><span data-stu-id="898b0-110">The number of indices `idx` such that `inferredLabels[idx] != actualLabels[idx]`.</span></span>