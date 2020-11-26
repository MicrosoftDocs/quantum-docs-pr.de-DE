---
uid: Microsoft.Quantum.Math._ExtendedGreatestCommonDivisorL
title: _ExtendedGreatestCommonDivisorL-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: _ExtendedGreatestCommonDivisorL
qsharp.summary: Internal recursive call to calculate the GCD.
ms.openlocfilehash: 8798026de0c468562630f6441f8cf0c7b2b82850
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196037"
---
# <a name="_extendedgreatestcommondivisorl-function"></a><span data-ttu-id="b0571-102">_ExtendedGreatestCommonDivisorL-Funktion</span><span class="sxs-lookup"><span data-stu-id="b0571-102">_ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="b0571-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b0571-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b0571-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b0571-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b0571-105">Interner rekursiver aufrufsbefehl zum Berechnen der GCD.</span><span class="sxs-lookup"><span data-stu-id="b0571-105">Internal recursive call to calculate the GCD.</span></span>

```qsharp
function _ExtendedGreatestCommonDivisorL (signA : Int, signB : Int, r : (BigInt, BigInt), s : (BigInt, BigInt), t : (BigInt, BigInt)) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="b0571-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b0571-106">Input</span></span>

### <a name="signa--int"></a><span data-ttu-id="b0571-107">Signa: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b0571-107">signA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="signb--int"></a><span data-ttu-id="b0571-108">signb: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b0571-108">signB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="r--bigintbigint"></a><span data-ttu-id="b0571-109">r: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="b0571-109">r : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="s--bigintbigint"></a><span data-ttu-id="b0571-110">s: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="b0571-110">s : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="t--bigintbigint"></a><span data-ttu-id="b0571-111">t: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="b0571-111">t : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>





## <a name="output--bigintbigint"></a><span data-ttu-id="b0571-112">Ausgabe: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="b0571-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

