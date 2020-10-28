---
uid: Microsoft.Quantum.Intrinsic.R
title: R-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 7d1d51031f4587b1c501feab459e614fc1530457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707151"
---
# <a name="r-operation"></a><span data-ttu-id="10d25-102">R-Vorgang</span><span class="sxs-lookup"><span data-stu-id="10d25-102">R operation</span></span>

<span data-ttu-id="10d25-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="10d25-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="10d25-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="10d25-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="10d25-105">Wendet eine Drehung auf die angegebene Pauli-Achse an.</span><span class="sxs-lookup"><span data-stu-id="10d25-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="10d25-106">\begin{align} R_ {\mu} (\orta) \mathrel{: =} e ^ {-i \Der Ta \ sigma_ {\mu}/2}, \end{align} WHERE $ \mu \in \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="10d25-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="10d25-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="10d25-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="10d25-108">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="10d25-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="10d25-109">Der Pauli-Operator ($ \mu $), der zum bilden der Drehung exponentiell berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10d25-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="10d25-110">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="10d25-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="10d25-111">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="10d25-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="10d25-112">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="10d25-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="10d25-113">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="10d25-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="10d25-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10d25-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="10d25-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="10d25-115">Remarks</span></span>

<span data-ttu-id="10d25-116">Wenn Sie mit aufgerufen `pauli = PauliI` wird, wendet dieser Vorgang eine *globale Phase* an.</span><span class="sxs-lookup"><span data-stu-id="10d25-116">When called with `pauli = PauliI`, this operation applies a *global phase* .</span></span> <span data-ttu-id="10d25-117">Diese Phase kann bei Verwendung mit dem-Funktor von Bedeutung sein `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="10d25-117">This phase can be significant when used with the `Controlled` functor.</span></span>