---
uid: Microsoft.Quantum.Math.ExpModL
title: Expmodl-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723731"
---
# <a name="expmodl-function"></a><span data-ttu-id="590ad-102">Expmodl-Funktion</span><span class="sxs-lookup"><span data-stu-id="590ad-102">ExpModL function</span></span>

<span data-ttu-id="590ad-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="590ad-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="590ad-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="590ad-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="590ad-105">Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="590ad-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="590ad-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="590ad-106">Description</span></span>

<span data-ttu-id="590ad-107">Wir bezeichnen expbase durch $x $, Power by $p $ und Modulo um $N $.</span><span class="sxs-lookup"><span data-stu-id="590ad-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="590ad-108">Die Funktion gibt $x ^ p \operatschmue{mod} N $ zurück.</span><span class="sxs-lookup"><span data-stu-id="590ad-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="590ad-109">Wir gehen davon aus, dass $N $, $x $ positiv und die Stromversorgung nicht negativ ist.</span><span class="sxs-lookup"><span data-stu-id="590ad-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="590ad-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="590ad-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="590ad-111">expbase: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="590ad-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="590ad-112">Leistung: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="590ad-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="590ad-113">Modulo: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="590ad-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="590ad-114">Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="590ad-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="590ad-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="590ad-115">Remarks</span></span>

<span data-ttu-id="590ad-116">Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.</span><span class="sxs-lookup"><span data-stu-id="590ad-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>