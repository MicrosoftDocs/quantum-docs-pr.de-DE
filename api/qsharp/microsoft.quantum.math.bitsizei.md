---
uid: Microsoft.Quantum.Math.BitSizeI
title: Bitsizei-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 561450ef43144aa4d7820e1f15d9300018104acd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195850"
---
# <a name="bitsizei-function"></a><span data-ttu-id="a11a3-102">Bitsizei-Funktion</span><span class="sxs-lookup"><span data-stu-id="a11a3-102">BitSizeI function</span></span>

<span data-ttu-id="a11a3-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a11a3-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a11a3-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a11a3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a11a3-105">Gibt für eine nicht negative ganze `a` Zahl die Anzahl der Bits zurück, die zur Darstellung von erforderlich sind `a` .</span><span class="sxs-lookup"><span data-stu-id="a11a3-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="a11a3-106">Das heißt, die kleinste $n $ wird so zurückgegeben, dass $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="a11a3-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="a11a3-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a11a3-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="a11a3-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a11a3-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a11a3-109">Die ganze Zahl, deren bitgröße berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a11a3-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="a11a3-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a11a3-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a11a3-111">Die bitgröße von `a` .</span><span class="sxs-lookup"><span data-stu-id="a11a3-111">The bit-size of `a`.</span></span>