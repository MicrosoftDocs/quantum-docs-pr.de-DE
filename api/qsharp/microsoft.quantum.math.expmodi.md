---
uid: Microsoft.Quantum.Math.ExpModI
title: Expmodi-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: dd4fc7d98275f6a02e3b13163b92f0812c92a82f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857034"
---
# <a name="expmodi-function"></a><span data-ttu-id="a98db-102">Expmodi-Funktion</span><span class="sxs-lookup"><span data-stu-id="a98db-102">ExpModI function</span></span>

<span data-ttu-id="a98db-103">Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="a98db-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="a98db-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a98db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a98db-105">Gibt eine ganze Zahl zurück, die in Bezug auf einen angegebenen Modulus zu einer gegebenen Potenz ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="a98db-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="a98db-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a98db-106">Description</span></span>

<span data-ttu-id="a98db-107">Wir bezeichnen expbase durch $x $, Power by $p $ und Modulo um $N $.</span><span class="sxs-lookup"><span data-stu-id="a98db-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="a98db-108">Die Funktion gibt $x ^ p \operatschmue{mod} N $ zurück.</span><span class="sxs-lookup"><span data-stu-id="a98db-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="a98db-109">Wir gehen davon aus, dass $N $, $x $ positiv und die Stromversorgung nicht negativ ist.</span><span class="sxs-lookup"><span data-stu-id="a98db-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="a98db-110">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a98db-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="a98db-111">expbase: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a98db-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="a98db-112">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a98db-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="a98db-113">Modulo: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a98db-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="a98db-114">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a98db-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="a98db-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a98db-115">Remarks</span></span>

<span data-ttu-id="a98db-116">Nimmt Zeit proportional zur Anzahl der Bits in `power` , nicht an `power` sich selbst.</span><span class="sxs-lookup"><span data-stu-id="a98db-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>