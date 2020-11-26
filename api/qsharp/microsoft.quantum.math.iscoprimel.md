---
uid: Microsoft.Quantum.Math.IsCoprimeL
title: Iscoprimel-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeL
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: c78e995801f67822cf98104a7319093d853b6afe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228133"
---
# <a name="iscoprimel-function"></a><span data-ttu-id="d6904-102">Iscoprimel-Funktion</span><span class="sxs-lookup"><span data-stu-id="d6904-102">IsCoprimeL function</span></span>

<span data-ttu-id="d6904-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="d6904-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="d6904-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d6904-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d6904-105">Gibt true zurück, wenn $a $ und $b $ eine Co-Primzahl sind, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="d6904-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="d6904-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d6904-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d6904-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d6904-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d6904-108">die erste Zahl, mit der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="d6904-108">the first number of which co-primality is being tested</span></span>


### <a name="b--bigint"></a><span data-ttu-id="d6904-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d6904-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d6904-110">die zweite Zahl, von der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="d6904-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="d6904-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d6904-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d6904-112">True, wenn $a $ und $b $ eine Co-Primzahl sind (z. b. der größte gemeinsame Divisor ist 1), andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="d6904-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>