---
uid: Microsoft.Quantum.Math.BigFraction
title: Bigbruchteil-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: bfbf49e7a3d060417e506a1977c20adc08b81f0e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846903"
---
# <a name="bigfraction-user-defined-type"></a><span data-ttu-id="e0b09-102">Bigbruchteil-benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0b09-102">BigFraction user defined type</span></span>

<span data-ttu-id="e0b09-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e0b09-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e0b09-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e0b09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e0b09-105">Stellt eine rationale Zahl der Form dar `p/q` .</span><span class="sxs-lookup"><span data-stu-id="e0b09-105">Represents a rational number of the form `p/q`.</span></span> <span data-ttu-id="e0b09-106">"Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.</span><span class="sxs-lookup"><span data-stu-id="e0b09-106">Integer `p` is the first element of the tuple and `q` is the second element of the tuple.</span></span>

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a><span data-ttu-id="e0b09-107">Benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="e0b09-107">Named Items</span></span>

### <a name="numerator--bigint"></a><span data-ttu-id="e0b09-108">Zähler: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e0b09-108">Numerator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="e0b09-109">Zähler des Bruchteils.</span><span class="sxs-lookup"><span data-stu-id="e0b09-109">Numerator of the fraction.</span></span>
### <a name="denominator--bigint"></a><span data-ttu-id="e0b09-110">Nenner: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="e0b09-110">Denominator : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="e0b09-111">Nenner des Bruchteils/</span><span class="sxs-lookup"><span data-stu-id="e0b09-111">Denominator of the fraction/</span></span>