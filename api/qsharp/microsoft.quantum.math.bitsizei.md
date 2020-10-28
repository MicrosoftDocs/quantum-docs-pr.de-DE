---
uid: Microsoft.Quantum.Math.BitSizeI
title: Bitsizei-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7cfe03908a8a394fc8ceb1c9facbf02f3db2d48
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723199"
---
# <a name="bitsizei-function"></a><span data-ttu-id="17e12-102">Bitsizei-Funktion</span><span class="sxs-lookup"><span data-stu-id="17e12-102">BitSizeI function</span></span>

<span data-ttu-id="17e12-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="17e12-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="17e12-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="17e12-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="17e12-105">Gibt für eine nicht negative ganze `a` Zahl die Anzahl der Bits zurück, die zur Darstellung von erforderlich sind `a` .</span><span class="sxs-lookup"><span data-stu-id="17e12-105">For a non-negative integer `a`, returns the number of bits required to represent `a`.</span></span>

<span data-ttu-id="17e12-106">Das heißt, die kleinste $n $ wird so zurückgegeben, dass $a < 2 ^ n $.</span><span class="sxs-lookup"><span data-stu-id="17e12-106">That is, returns the smallest $n$ such that $a < 2^n$.</span></span>

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a><span data-ttu-id="17e12-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="17e12-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="17e12-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="17e12-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="17e12-109">Die ganze Zahl, deren bitgröße berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17e12-109">The integer whose bit-size is to be computed.</span></span>



## <a name="output--int"></a><span data-ttu-id="17e12-110">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="17e12-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="17e12-111">Die bitgröße von `a` .</span><span class="sxs-lookup"><span data-stu-id="17e12-111">The bit-size of `a`.</span></span>