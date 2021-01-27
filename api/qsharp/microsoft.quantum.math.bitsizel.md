---
uid: Microsoft.Quantum.Math.BitSizeL
title: Bitsizel-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: c94d873d7117fd2ee66226fab6d4bfc5b33bc46d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848907"
---
# <a name="bitsizel-function"></a><span data-ttu-id="a21cb-102">Bitsizel-Funktion</span><span class="sxs-lookup"><span data-stu-id="a21cb-102">BitSizeL function</span></span>

<span data-ttu-id="a21cb-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a21cb-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a21cb-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a21cb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a21cb-105">Gibt für eine nicht negative ganze `a` Zahl die Anzahl der Bits zurück, die zur Darstellung von erforderlich sind `a` .</span><span class="sxs-lookup"><span data-stu-id="a21cb-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="a21cb-106">Das heißt, die kleinste $n $ wird so zurückgegeben, dass $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="a21cb-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="a21cb-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a21cb-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a21cb-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a21cb-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a21cb-109">Die ganze Zahl, deren bitgröße berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a21cb-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="a21cb-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a21cb-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a21cb-111">Die bitgröße von `a` .</span><span class="sxs-lookup"><span data-stu-id="a21cb-111">The bit-size of `a`.</span></span>