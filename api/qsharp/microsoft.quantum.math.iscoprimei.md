---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Iscoprimei-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 53131a755571ad1ac0a8a984bf229b16f67dbe51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195357"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="e3a6a-102">Iscoprimei-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3a6a-102">IsCoprimeI function</span></span>

<span data-ttu-id="e3a6a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="e3a6a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="e3a6a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3a6a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3a6a-105">Gibt true zurück, wenn $a $ und $b $ eine Co-Primzahl sind, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="e3a6a-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="e3a6a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e3a6a-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="e3a6a-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3a6a-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e3a6a-108">die erste Zahl, mit der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="e3a6a-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="e3a6a-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e3a6a-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e3a6a-110">die zweite Zahl, von der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="e3a6a-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="e3a6a-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e3a6a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e3a6a-112">True, wenn $a $ und $b $ eine Co-Primzahl sind (z. b. der größte gemeinsame Divisor ist 1), andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="e3a6a-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>