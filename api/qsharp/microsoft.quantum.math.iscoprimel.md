---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Iscoprimel-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 7c077d508c93672d58a52a1403b3c5d73df75471
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722304"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="9a59b-102">Iscoprimel-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a59b-102">IsCoprimeL function</span></span>

<span data-ttu-id="9a59b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9a59b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9a59b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a59b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a59b-105">Gibt true zurück, wenn $a $ und $b $ eine Co-Primzahl sind, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="9a59b-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="9a59b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a59b-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="9a59b-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9a59b-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9a59b-108">die erste Zahl, mit der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="9a59b-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="9a59b-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9a59b-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9a59b-110">die zweite Zahl, von der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="9a59b-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="9a59b-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9a59b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9a59b-112">True, wenn $a $ und $b $ eine Co-Primzahl sind (z. b. der größte gemeinsame Divisor ist 1), andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="9a59b-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>