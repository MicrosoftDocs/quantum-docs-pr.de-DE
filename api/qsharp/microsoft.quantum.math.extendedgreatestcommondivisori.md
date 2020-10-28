---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: Extendedgreatestcommondivisori-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 8cb21ae5052ae6c5a8aed8be71d6bd3d32034272
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723718"
---
# <a name="extendedgreatestcommondivisori-function"></a><span data-ttu-id="b65e1-102">Extendedgreatestcommondivisori-Funktion</span><span class="sxs-lookup"><span data-stu-id="b65e1-102">ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="b65e1-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b65e1-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b65e1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b65e1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b65e1-105">Berechnet ein Tupel $ (u, v) $, sodass $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, wobei $ \operatschmue{GCD} $ $a $ Greatest common divisor von $a $ und $b $ ist.</span><span class="sxs-lookup"><span data-stu-id="b65e1-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="b65e1-106">Die GCD ist immer positiv.</span><span class="sxs-lookup"><span data-stu-id="b65e1-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="b65e1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b65e1-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="b65e1-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b65e1-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b65e1-109">die erste Zahl, die der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b65e1-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="b65e1-110">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b65e1-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b65e1-111">die zweite Zahl, von der der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="b65e1-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--intint"></a><span data-ttu-id="b65e1-112">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="b65e1-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="b65e1-113">Tuple $ (u, v) $ mit der-Eigenschaft $u \cdot a + v \cdot b = \operatschmue{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="b65e1-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="b65e1-114">Referenzen</span><span class="sxs-lookup"><span data-stu-id="b65e1-114">References</span></span>

- <span data-ttu-id="b65e1-115">Diese Implementierung ist gemäß https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="b65e1-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>