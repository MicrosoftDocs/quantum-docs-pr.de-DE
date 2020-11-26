---
uid: Microsoft.Quantum.Math._ContinuedFractionConvergentL
title: _ContinuedFractionConvergentL-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: _ContinuedFractionConvergentL
qsharp.summary: Internal recursive call to calculate the GCD with a bound
ms.openlocfilehash: 456893b414373728fff2079e7a9bbbe068edac55
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196071"
---
# <a name="_continuedfractionconvergentl-function"></a><span data-ttu-id="25218-102">_ContinuedFractionConvergentL-Funktion</span><span class="sxs-lookup"><span data-stu-id="25218-102">_ContinuedFractionConvergentL function</span></span>

<span data-ttu-id="25218-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="25218-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="25218-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25218-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25218-105">Interner rekursiver aufrufsbefehl zum Berechnen der GCD mit einer gebundenen</span><span class="sxs-lookup"><span data-stu-id="25218-105">Internal recursive call to calculate the GCD with a bound</span></span>

```qsharp
function _ContinuedFractionConvergentL (signA : Int, signB : Int, r : (BigInt, BigInt), s : (BigInt, BigInt), t : (BigInt, BigInt), denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a><span data-ttu-id="25218-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25218-106">Input</span></span>

### <a name="signa--int"></a><span data-ttu-id="25218-107">Signa: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25218-107">signA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="signb--int"></a><span data-ttu-id="25218-108">signb: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="25218-108">signB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="r--bigintbigint"></a><span data-ttu-id="25218-109">r: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="25218-109">r : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="s--bigintbigint"></a><span data-ttu-id="25218-110">s: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="25218-110">s : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="t--bigintbigint"></a><span data-ttu-id="25218-111">t: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="25218-111">t : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>




### <a name="denominatorbound--bigint"></a><span data-ttu-id="25218-112">Nenner-gebunden: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="25218-112">denominatorBound : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigfraction"></a><span data-ttu-id="25218-113">Ausgabe: [bigbruch](xref:Microsoft.Quantum.Math.BigFraction)</span><span class="sxs-lookup"><span data-stu-id="25218-113">Output : [BigFraction](xref:Microsoft.Quantum.Math.BigFraction)</span></span>

