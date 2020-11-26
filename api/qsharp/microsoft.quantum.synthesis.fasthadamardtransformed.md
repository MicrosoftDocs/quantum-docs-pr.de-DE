---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Fasthadamardtransformierte-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 3e48701f22ddf154721355866e15a85fca0bc7df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203092"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="0cac5-102">Fasthadamardtransformierte-Funktion</span><span class="sxs-lookup"><span data-stu-id="0cac5-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="0cac5-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="0cac5-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="0cac5-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0cac5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0cac5-105">Berechnet die Hadamard-Transformation einer booleschen Funktion in {-1,1} der Codierung mithilfe der Yates-Methode.</span><span class="sxs-lookup"><span data-stu-id="0cac5-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="0cac5-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0cac5-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="0cac5-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="0cac5-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="0cac5-108">Wahrheitstabelle in der {-1,1} Codierung</span><span class="sxs-lookup"><span data-stu-id="0cac5-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="0cac5-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="0cac5-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="0cac5-110">Die Spektral Koeffizienten der Funktion</span><span class="sxs-lookup"><span data-stu-id="0cac5-110">Spectral coefficients of the function</span></span>