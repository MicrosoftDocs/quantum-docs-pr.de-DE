---
uid: Microsoft.Quantum.Math.BigFraction
title: Bigbruchteil-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723213"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="82dd5-102">Bigbruchteil-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="82dd5-102">BigFraction user defined type</span></span>

<span data-ttu-id="82dd5-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="82dd5-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="82dd5-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="82dd5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="82dd5-105">Stellt eine rationale Zahl der Form dar `p/q` .</span><span class="sxs-lookup"><span data-stu-id="82dd5-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="82dd5-106">"Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.</span><span class="sxs-lookup"><span data-stu-id="82dd5-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="82dd5-107">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="82dd5-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="82dd5-108">Zähler: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="82dd5-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="82dd5-109">Zähler des Bruchteils.</span><span class="sxs-lookup"><span data-stu-id="82dd5-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="82dd5-110">Nenner: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="82dd5-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="82dd5-111">Nenner des Bruchteils/</span><span class="sxs-lookup"><span data-stu-id="82dd5-111">Denominator of the fraction/</span></span>