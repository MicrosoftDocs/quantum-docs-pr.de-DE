---
uid: Microsoft.Quantum.Math.IsCoprimeI
title: Iscoprimei-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: IsCoprimeI
qsharp.summary: Returns true if $a$ and $b$ are co-prime and false otherwise.
ms.openlocfilehash: 2c110f9abf18ee81bd72a68601d5c41ff756290a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851363"
---
# <a name="iscoprimei-function"></a><span data-ttu-id="303a0-102">Iscoprimei-Funktion</span><span class="sxs-lookup"><span data-stu-id="303a0-102">IsCoprimeI function</span></span>

<span data-ttu-id="303a0-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="303a0-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="303a0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="303a0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="303a0-105">Gibt true zurück, wenn $a $ und $b $ eine Co-Primzahl sind, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="303a0-105">Returns true if $a$ and $b$ are co-prime and false otherwise.</span></span>

```qsharp
function IsCoprimeI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="303a0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="303a0-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="303a0-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="303a0-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="303a0-108">die erste Zahl, mit der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="303a0-108">the first number of which co-primality is being tested</span></span>


### <a name="b--int"></a><span data-ttu-id="303a0-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="303a0-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="303a0-110">die zweite Zahl, von der die Co-primalität getestet wird.</span><span class="sxs-lookup"><span data-stu-id="303a0-110">the second number of which co-primality is being tested</span></span>



## <a name="output--bool"></a><span data-ttu-id="303a0-111">Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="303a0-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="303a0-112">True, wenn $a $ und $b $ eine Co-Primzahl sind (z. b. der größte gemeinsame Divisor ist 1), andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="303a0-112">True, if $a$ and $b$ are co-prime (e.g. their greatest common divisor is 1 ), and false otherwise</span></span>