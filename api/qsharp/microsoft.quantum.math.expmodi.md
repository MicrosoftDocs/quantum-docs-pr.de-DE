---
uid: Microsoft.Quantum.Math.ExpModI
title: Expmodi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723367"
---
# <a name="expmodi-function"></a><span data-ttu-id="b552c-102">Expmodi-Funktion</span><span class="sxs-lookup"><span data-stu-id="b552c-102">ExpModI function</span></span>

<span data-ttu-id="b552c-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b552c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b552c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b552c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b552c-105">Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b552c-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="b552c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b552c-106">Description</span></span>

<span data-ttu-id="b552c-107">Wir bezeichnen expbase durch $x $, Power by $p $ und Modulo um $N $.</span><span class="sxs-lookup"><span data-stu-id="b552c-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="b552c-108">Die Funktion gibt $x ^ p \operatschmue{mod} N $ zurück.</span><span class="sxs-lookup"><span data-stu-id="b552c-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="b552c-109">Wir gehen davon aus, dass $N $, $x $ positiv und die Stromversorgung nicht negativ ist.</span><span class="sxs-lookup"><span data-stu-id="b552c-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="b552c-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b552c-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="b552c-111">expbase: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b552c-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="b552c-112">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b552c-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="b552c-113">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b552c-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="b552c-114">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b552c-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="b552c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b552c-115">Remarks</span></span>

<span data-ttu-id="b552c-116">Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.</span><span class="sxs-lookup"><span data-stu-id="b552c-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>