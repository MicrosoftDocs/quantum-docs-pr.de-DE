---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: Greatestcommondivisorl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 77bdb040908e9a8af81dee09451a3582f7b7d159
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723647"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="604d2-102">Greatestcommondivisorl-Funktion</span><span class="sxs-lookup"><span data-stu-id="604d2-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="604d2-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="604d2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="604d2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="604d2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="604d2-105">Berechnet den größten gemeinsamen Divisor von $a $ und $b $.</span><span class="sxs-lookup"><span data-stu-id="604d2-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="604d2-106">Die GCD ist immer positiv.</span><span class="sxs-lookup"><span data-stu-id="604d2-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="604d2-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="604d2-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="604d2-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="604d2-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="604d2-109">die erste Zahl, die der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="604d2-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="604d2-110">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="604d2-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="604d2-111">die zweite Zahl, von der der erweiterte größte gemeinsame Divisor berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="604d2-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="604d2-112">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="604d2-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="604d2-113">Der größte gemeinsame Divisor von $a $ und $b $</span><span class="sxs-lookup"><span data-stu-id="604d2-113">Greatest common divisor of $a$ and $b$</span></span>