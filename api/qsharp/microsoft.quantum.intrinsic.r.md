---
uid: Microsoft.Quantum.Intrinsic.R
title: R-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 89aa5b2867068d4352a0b9550e8d22aa77439111
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96199028"
---
# <a name="r-operation"></a><span data-ttu-id="a1ea8-102">R-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a1ea8-102">R operation</span></span>

<span data-ttu-id="a1ea8-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="a1ea8-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="a1ea8-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a1ea8-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a1ea8-105">Wendet eine Drehung auf die angegebene Pauli-Achse an.</span><span class="sxs-lookup"><span data-stu-id="a1ea8-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="a1ea8-106">\begin{align} R_ {\mu} (\orta) \mathrel{: =} e ^ {-i \Der Ta \ sigma_ {\mu}/2}, \end{align} WHERE $ \mu \in \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="a1ea8-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="a1ea8-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1ea8-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="a1ea8-108">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="a1ea8-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="a1ea8-109">Der Pauli-Operator ($ \mu $), der zum bilden der Drehung exponentiell berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1ea8-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="a1ea8-110">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="a1ea8-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="a1ea8-111">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1ea8-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="a1ea8-112">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="a1ea8-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="a1ea8-113">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1ea8-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a1ea8-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1ea8-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a1ea8-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1ea8-115">Remarks</span></span>

<span data-ttu-id="a1ea8-116">Wenn Sie mit aufgerufen `pauli = PauliI` wird, wendet dieser Vorgang eine *globale Phase* an.</span><span class="sxs-lookup"><span data-stu-id="a1ea8-116">When called with `pauli = PauliI`, this operation applies a *global phase*.</span></span> <span data-ttu-id="a1ea8-117">Diese Phase kann bei Verwendung mit dem-Funktor von Bedeutung sein `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="a1ea8-117">This phase can be significant when used with the `Controlled` functor.</span></span>