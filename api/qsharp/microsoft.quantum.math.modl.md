---
uid: Microsoft.Quantum.Math.ModL
title: Modl-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModL
qsharp.summary: Returns the modulus of a number with respect to another number.
ms.openlocfilehash: f044ae16d93d31d0f28f5fcf076cff2bfef62eb8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846835"
---
# <a name="modl-function"></a><span data-ttu-id="1e77b-102">Modl-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e77b-102">ModL function</span></span>

<span data-ttu-id="1e77b-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="1e77b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="1e77b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1e77b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1e77b-105">Gibt den Modulo einer Zahl in Bezug auf eine andere Zahl zurück.</span><span class="sxs-lookup"><span data-stu-id="1e77b-105">Returns the modulus of a number with respect to another number.</span></span>

```qsharp
function ModL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="1e77b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1e77b-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="1e77b-107">a: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1e77b-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1e77b-108">Der Eingabe $a $, dessen Modulo zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e77b-108">The input $a$ whose modulus is to be returned.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="1e77b-109">b: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1e77b-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1e77b-110">Die Zahl, in der der $a $-modulo zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1e77b-110">The number with respect to which the modulus of $a$ is to be returned.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="1e77b-111">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1e77b-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1e77b-112">Der Modulo $a \bmod b $.</span><span class="sxs-lookup"><span data-stu-id="1e77b-112">The modulus $a \bmod b$.</span></span>