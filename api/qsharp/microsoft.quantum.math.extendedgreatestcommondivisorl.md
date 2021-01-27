---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: Extendedgreatestcommondivisorl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 1445f1c3d2a5852459a492fa5e6bfd2a685786d9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857530"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="50624-102">Extendedgreatestcommondivisorl-Funktion</span><span class="sxs-lookup"><span data-stu-id="50624-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="50624-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="50624-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="50624-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="50624-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="50624-105">Berechnet ein Tupel $ (u, v) $, sodass $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, wobei $ \operatschmue{GCD} $ $a $ Greatest common divisor von $a $ und $b $ ist.</span><span class="sxs-lookup"><span data-stu-id="50624-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="50624-106">Die GCD ist immer positiv.</span><span class="sxs-lookup"><span data-stu-id="50624-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="50624-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="50624-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="50624-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="50624-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="50624-109">die erste Zahl, die der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="50624-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="50624-110">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="50624-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="50624-111">die zweite Zahl, von der der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="50624-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="50624-112">Ausgabe: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="50624-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="50624-113">Tuple $ (u, v) $ mit der-Eigenschaft $u \cdot a + v \cdot b = \operatschmue{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="50624-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="50624-114">References</span><span class="sxs-lookup"><span data-stu-id="50624-114">References</span></span>

- <span data-ttu-id="50624-115">Diese Implementierung ist gemäß https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="50624-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>