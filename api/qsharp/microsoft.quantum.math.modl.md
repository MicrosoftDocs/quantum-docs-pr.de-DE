---
uid: Microsoft.Quantum.Math.ModL
title: Modl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 0b1ac69cc1474e9cfa6a3489b2b2fdf497e812e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227793"
---
# <a name="modl-function"></a><span data-ttu-id="60d3a-102">Modl-Funktion</span><span class="sxs-lookup"><span data-stu-id="60d3a-102">ModL function</span></span>

<span data-ttu-id="60d3a-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="60d3a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="60d3a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="60d3a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="60d3a-105">Gibt den Modulo einer Zahl in Bezug auf eine andere Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="60d3a-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="60d3a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="60d3a-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="60d3a-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="60d3a-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="60d3a-108">Der Eingabe $a $, dessen Modulo zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="60d3a-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="60d3a-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="60d3a-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="60d3a-110">Die Zahl, in der der $a $-modulo zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="60d3a-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="60d3a-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="60d3a-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="60d3a-112">Der Modulo $a \bmod b $.</span><span class="sxs-lookup"><span data-stu-id="60d3a-112">The modulus $a \bmod b$.</span></span>