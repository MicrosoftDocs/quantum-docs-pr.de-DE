---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Fasthadamardtransformierte-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: be54413ef2d3fdaf7ddc726bc0906adb4ec382ff
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855448"
---
# <a name="fasthadamardtransformed-function"></a><span data-ttu-id="2d0a7-102">Fasthadamardtransformierte-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d0a7-102">FastHadamardTransformed function</span></span>

<span data-ttu-id="2d0a7-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="2d0a7-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="2d0a7-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2d0a7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2d0a7-105">Berechnet die Hadamard-Transformation einer booleschen Funktion in {-1,1} der Codierung mithilfe der Yates-Methode.</span><span class="sxs-lookup"><span data-stu-id="2d0a7-105">Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method</span></span>

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="2d0a7-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="2d0a7-106">Input</span></span>

### <a name="func--int"></a><span data-ttu-id="2d0a7-107">Func: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2d0a7-107">func : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2d0a7-108">Wahrheitstabelle in der {-1,1} Codierung</span><span class="sxs-lookup"><span data-stu-id="2d0a7-108">Truth table in {-1,1} encoding</span></span>



## <a name="output--int"></a><span data-ttu-id="2d0a7-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2d0a7-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2d0a7-110">Die Spektral Koeffizienten der Funktion</span><span class="sxs-lookup"><span data-stu-id="2d0a7-110">Spectral coefficients of the function</span></span>

## <a name="example"></a><span data-ttu-id="2d0a7-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2d0a7-111">Example</span></span>

```qsharp
FastHadamardTransformed([1, 1, 1, -1]); // [2, 2, 2, -2]
```