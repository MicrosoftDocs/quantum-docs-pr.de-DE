---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: Extendedgreatestcommondivisori-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: e86237f39e696485a3496f1c6dd571cd516214ec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857555"
---
# <a name="extendedgreatestcommondivisori-function"></a><span data-ttu-id="0778e-102">Extendedgreatestcommondivisori-Funktion</span><span class="sxs-lookup"><span data-stu-id="0778e-102">ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="0778e-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="0778e-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="0778e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0778e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0778e-105">Berechnet ein Tupel $ (u, v) $, sodass $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, wobei $ \operatschmue{GCD} $ $a $ Greatest common divisor von $a $ und $b $ ist.</span><span class="sxs-lookup"><span data-stu-id="0778e-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="0778e-106">Die GCD ist immer positiv.</span><span class="sxs-lookup"><span data-stu-id="0778e-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="0778e-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0778e-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="0778e-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0778e-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0778e-109">die erste Zahl, die der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0778e-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="0778e-110">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0778e-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0778e-111">die zweite Zahl, von der der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="0778e-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--intint"></a><span data-ttu-id="0778e-112">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="0778e-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="0778e-113">Tuple $ (u, v) $ mit der-Eigenschaft $u \cdot a + v \cdot b = \operatschmue{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="0778e-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="0778e-114">References</span><span class="sxs-lookup"><span data-stu-id="0778e-114">References</span></span>

- <span data-ttu-id="0778e-115">Diese Implementierung ist gemäß https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="0778e-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>