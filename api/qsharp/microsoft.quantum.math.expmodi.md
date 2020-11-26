---
uid: Microsoft.Quantum.Math.ExpModI
title: Expmodi-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 197f7351ce76ebb7684ca8014cab9ab65d9c784c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228489"
---
# <a name="expmodi-function"></a><span data-ttu-id="7ef22-102">Expmodi-Funktion</span><span class="sxs-lookup"><span data-stu-id="7ef22-102">ExpModI function</span></span>

<span data-ttu-id="7ef22-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="7ef22-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="7ef22-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7ef22-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7ef22-105">Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7ef22-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="7ef22-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7ef22-106">Description</span></span>

<span data-ttu-id="7ef22-107">Wir bezeichnen expbase durch $x $, Power by $p $ und Modulo um $N $.</span><span class="sxs-lookup"><span data-stu-id="7ef22-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="7ef22-108">Die Funktion gibt $x ^ p \operatschmue{mod} N $ zurück.</span><span class="sxs-lookup"><span data-stu-id="7ef22-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="7ef22-109">Wir gehen davon aus, dass $N $, $x $ positiv und die Stromversorgung nicht negativ ist.</span><span class="sxs-lookup"><span data-stu-id="7ef22-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="7ef22-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="7ef22-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="7ef22-111">expbase: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7ef22-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="7ef22-112">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7ef22-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="7ef22-113">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7ef22-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="7ef22-114">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7ef22-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="7ef22-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7ef22-115">Remarks</span></span>

<span data-ttu-id="7ef22-116">Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.</span><span class="sxs-lookup"><span data-stu-id="7ef22-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>