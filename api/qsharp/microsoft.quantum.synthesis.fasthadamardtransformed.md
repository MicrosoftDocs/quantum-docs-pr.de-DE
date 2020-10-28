---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Fasthadamardtransformierte-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 2b84e92d08a3baad2552780cae91f447830cac82
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725187"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="b9c14-102">Fasthadamardtransformierte-Funktion</span><span class="sxs-lookup"><span data-stu-id="b9c14-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="b9c14-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="b9c14-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="b9c14-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b9c14-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b9c14-105">Berechnet die Hadamard-Transformation einer booleschen Funktion in {-1,1} der Codierung mithilfe der Yates-Methode.</span><span class="sxs-lookup"><span data-stu-id="b9c14-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="b9c14-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b9c14-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="b9c14-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b9c14-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b9c14-108">Wahrheitstabelle in der {-1,1} Codierung</span><span class="sxs-lookup"><span data-stu-id="b9c14-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="b9c14-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b9c14-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b9c14-110">Die Spektral Koeffizienten der Funktion</span><span class="sxs-lookup"><span data-stu-id="b9c14-110">Spectral coefficients of the function</span></span>