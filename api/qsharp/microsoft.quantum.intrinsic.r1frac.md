---
uid: Microsoft.Quantum.Intrinsic.R1Frac
title: R1Frac-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1Frac
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.

  \begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}). \end{align}

  > [!WARNING] > This operation uses the **opposite** sign convention from > @"microsoft.quantum.intrinsic.r", and does not include the > factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".
ms.openlocfilehash: eb2dd8750ed5ad9fc75ca24bb4c8ef36298f69f4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198774"
---
# <a name="r1frac-operation"></a><span data-ttu-id="10173-102">R1Frac-Vorgang</span><span class="sxs-lookup"><span data-stu-id="10173-102">R1Frac operation</span></span>

<span data-ttu-id="10173-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="10173-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="10173-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="10173-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="10173-105">Wendet eine Drehung über den $ \ket {1} $-Zustand um einen als dyadic-Bruchteil angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="10173-105">Applies a rotation about the $\ket{1}$ state by an angle specified as a dyadic fraction.</span></span>

<span data-ttu-id="10173-106">\begin{align} R_1 (n, k) \mathrel{: =} \operatschmue{Diag} (1, e ^ {i \pi k/2 ^ n}).</span><span class="sxs-lookup"><span data-stu-id="10173-106">\begin{align} R_1(n, k) \mathrel{:=} \operatorname{diag}(1, e^{i \pi k / 2^n}).</span></span>
<span data-ttu-id="10173-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="10173-107">\end{align}</span></span>

> [!WARNING]
> <span data-ttu-id="10173-108">Bei diesem Vorgang wird die **gegenüberliegende** Zeichen Konvention aus verwendet @"microsoft.quantum.intrinsic.r" , und der in enthaltene Faktor von $1/2 $ ist nicht enthalten @"microsoft.quantum.intrinsic.r1" .</span><span class="sxs-lookup"><span data-stu-id="10173-108">This operation uses the **opposite** sign convention from @"microsoft.quantum.intrinsic.r", and does not include the factor of $1/ 2$ included by @"microsoft.quantum.intrinsic.r1".</span></span>

```qsharp
operation R1Frac (numerator : Int, power : Int, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="10173-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10173-109">Input</span></span>

### <a name="numerator--int"></a><span data-ttu-id="10173-110">Zähler: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10173-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10173-111">Der Zähler in der dyadic-Bruch Darstellung des Winkels, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="10173-111">Numerator in the dyadic fraction representation of the angle by which the qubit is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="10173-112">Power: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="10173-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="10173-113">Potenz von zwei, die den Nenner des Winkels angibt, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="10173-113">Power of two specifying the denominator of the angle by which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="10173-114">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="10173-114">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="10173-115">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10173-115">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="10173-116">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10173-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="10173-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10173-117">Remarks</span></span>

<span data-ttu-id="10173-118">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="10173-118">Equivalent to:</span></span>

```qsharp
RFrac(PauliZ, -numerator, denominator + 1, qubit);
RFrac(PauliI, numerator, denominator + 1, qubit);
```