---
uid: Microsoft.Quantum.Math.ModL
title: Modl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: 15b11a59d189aa881da9fb514cf0fe3bc9f20201
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723102"
---
# <a name="modl-function"></a><span data-ttu-id="1af37-102">Modl-Funktion</span><span class="sxs-lookup"><span data-stu-id="1af37-102">ModL function</span></span>

<span data-ttu-id="1af37-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1af37-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1af37-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1af37-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1af37-105">Gibt den Modulo einer Zahl in Bezug auf eine andere Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="1af37-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="1af37-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1af37-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="1af37-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1af37-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1af37-108">Der Eingabe $a $, dessen Modulo zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1af37-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="1af37-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1af37-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1af37-110">Die Zahl, in der der $a $-modulo zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1af37-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="1af37-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1af37-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1af37-112">Der Modulo $a \bmod b $.</span><span class="sxs-lookup"><span data-stu-id="1af37-112">The modulus $a \bmod b$.</span></span>