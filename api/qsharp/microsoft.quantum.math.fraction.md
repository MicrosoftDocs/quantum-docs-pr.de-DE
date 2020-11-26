---
uid: Microsoft.Quantum.Math.Fraction
title: Benutzerdefinierter Bruchteil-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210674"
---
# <a name="fraction-user-defined-type"></a><span data-ttu-id="fbc9c-102">Benutzerdefinierter Bruchteil-Typ</span><span class="sxs-lookup"><span data-stu-id="fbc9c-102">Fraction user defined type</span></span>

<span data-ttu-id="fbc9c-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="fbc9c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="fbc9c-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fbc9c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fbc9c-105">Stellt eine rationale Zahl der Form dar `p/q` .</span><span class="sxs-lookup"><span data-stu-id="fbc9c-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="fbc9c-106">"Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.</span><span class="sxs-lookup"><span data-stu-id="fbc9c-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a><span data-ttu-id="fbc9c-107">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="fbc9c-107">Named Items</span></span>

### <a name="numerator--int"></a><span data-ttu-id="fbc9c-108">Zähler: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fbc9c-108">Numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fbc9c-109">Zähler des Bruchteils.</span><span class="sxs-lookup"><span data-stu-id="fbc9c-109">Numerator of the fraction.</span></span>
### <a name="denominator--int"></a><span data-ttu-id="fbc9c-110">Nenner: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fbc9c-110">Denominator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fbc9c-111">Nenner des Bruchteils/</span><span class="sxs-lookup"><span data-stu-id="fbc9c-111">Denominator of the fraction/</span></span>