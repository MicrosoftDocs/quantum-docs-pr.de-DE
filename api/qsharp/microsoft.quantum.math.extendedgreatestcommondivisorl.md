---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: Extendedgreatestcommondivisorl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: e671405045d6d2587a8c6ccbac4ae3402f92f722
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723717"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="9838b-102">Extendedgreatestcommondivisorl-Funktion</span><span class="sxs-lookup"><span data-stu-id="9838b-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="9838b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9838b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9838b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9838b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9838b-105">Berechnet ein Tupel $ (u, v) $, sodass $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, wobei $ \operatschmue{GCD} $ $a $ Greatest common divisor von $a $ und $b $ ist.</span><span class="sxs-lookup"><span data-stu-id="9838b-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="9838b-106">Die GCD ist immer positiv.</span><span class="sxs-lookup"><span data-stu-id="9838b-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="9838b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9838b-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="9838b-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9838b-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9838b-109">die erste Zahl, die der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9838b-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="9838b-110">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9838b-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9838b-111">die zweite Zahl, von der der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9838b-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="9838b-112">Ausgabe: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="9838b-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="9838b-113">Tuple $ (u, v) $ mit der-Eigenschaft $u \cdot a + v \cdot b = \operatschmue{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="9838b-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="9838b-114">Referenzen</span><span class="sxs-lookup"><span data-stu-id="9838b-114">References</span></span>

- <span data-ttu-id="9838b-115">Diese Implementierung ist gemäß https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="9838b-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>