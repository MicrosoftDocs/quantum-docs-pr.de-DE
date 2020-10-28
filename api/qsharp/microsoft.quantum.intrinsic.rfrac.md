---
uid: Microsoft.Quantum.Intrinsic.RFrac
title: Rfrac-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: RFrac
qsharp.summary: >-
  Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.

  \begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r".
ms.openlocfilehash: 9fe6aee6c7bb9e52538eae5d2caa2a6025cb85d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723508"
---
# <a name="rfrac-operation"></a><span data-ttu-id="9b1d0-102">Rfrac-Vorgang</span><span class="sxs-lookup"><span data-stu-id="9b1d0-102">RFrac operation</span></span>

<span data-ttu-id="9b1d0-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="9b1d0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9b1d0-105">Wendet eine Drehung um die angegebene Pauli-Achse um einen als dyadic-Bruchteil angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-105">Applies a rotation about the given Pauli axis by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="9b1d0-106">\begin{align} R_ {\mu} (n, k) \mathrel{: =} e ^ {i \pi n \ sigma_ {\mu}/2 ^ k}, \end{align} WHERE $ \mu \in \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-106">\begin{align} R_{\mu}(n, k) \mathrel{:=} e^{i \pi n \sigma_{\mu} / 2^k}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

> [!WARNING]
> <span data-ttu-id="9b1d0-107">Bei diesem Vorgang wird die **gegenüberliegende** Zeichen Konvention von verwendet @"microsoft.quantum.intrinsic.r" .</span><span class="sxs-lookup"><span data-stu-id="9b1d0-107">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r".</span></span>

```qsharp
operation RFrac (pauli : Pauli, numerator : Int, power : Int, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="9b1d0-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9b1d0-108">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="9b1d0-109">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-109">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="9b1d0-110">Der Pauli-Operator, der zum bilden der Drehung exponentiell gebildet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-110">Pauli operator to be exponentiated to form the rotation.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="9b1d0-111">Zähler: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-111">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b1d0-112">Der Zähler in der dyadic-Bruch Darstellung des Winkels, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-112">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="9b1d0-113">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-113">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9b1d0-114">Potenz von zwei, die den Nenner des Winkels angibt, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-114">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="9b1d0-115">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-115">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="9b1d0-116">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b1d0-116">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9b1d0-117">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9b1d0-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="9b1d0-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9b1d0-118">Remarks</span></span>

<span data-ttu-id="9b1d0-119">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="9b1d0-119">Equivalent to:</span></span>

```qsharp
// PI() is a Q# function that returns an approximation of π.
R(pauli, -PI() * IntAsDouble(numerator) / IntAsDouble(2 ^ (power - 1)), qubit);
```