---
uid: Microsoft.Quantum.Math.BitSizeL
title: Bitsizel-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 8b3d4cceb69619ed32977337fc0fe7401db38cbd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211048"
---
# <a name="bitsizel-function"></a><span data-ttu-id="07c90-102">Bitsizel-Funktion</span><span class="sxs-lookup"><span data-stu-id="07c90-102">BitSizeL function</span></span>

<span data-ttu-id="07c90-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="07c90-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="07c90-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07c90-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07c90-105">Gibt für eine nicht negative ganze `a` Zahl die Anzahl der Bits zurück, die zur Darstellung von erforderlich sind `a` .</span><span class="sxs-lookup"><span data-stu-id="07c90-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="07c90-106">Das heißt, die kleinste $n $ wird so zurückgegeben, dass $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="07c90-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a><span data-ttu-id="07c90-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="07c90-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="07c90-108">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="07c90-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="07c90-109">Die ganze Zahl, deren bitgröße berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="07c90-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="07c90-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="07c90-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="07c90-111">Die bitgröße von `a` .</span><span class="sxs-lookup"><span data-stu-id="07c90-111">The bit-size of `a`.</span></span>