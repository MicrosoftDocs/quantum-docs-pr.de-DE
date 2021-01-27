---
uid: Microsoft.Quantum.Intrinsic.R
title: R-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R
qsharp.summary: >-
  Applies a rotation about the given Pauli axis.

  \begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.
ms.openlocfilehash: 1df4b1197e885e479339e542e8c1ffaeb392543d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818714"
---
# <a name="r-operation"></a><span data-ttu-id="25527-102">R-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25527-102">R operation</span></span>

<span data-ttu-id="25527-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="25527-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="25527-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="25527-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="25527-105">Wendet eine Drehung auf die angegebene Pauli-Achse an.</span><span class="sxs-lookup"><span data-stu-id="25527-105">Applies a rotation about the given Pauli axis.</span></span>

<span data-ttu-id="25527-106">\begin{align} R_ {\mu} (\orta) \mathrel{: =} e ^ {-i \Der Ta \ sigma_ {\mu}/2}, \end{align} WHERE $ \mu \in \{ i, X, Y, Z \} $.</span><span class="sxs-lookup"><span data-stu-id="25527-106">\begin{align} R_{\mu}(\theta) \mathrel{:=} e^{-i \theta \sigma_{\mu} / 2}, \end{align} where $\mu \in \{I, X, Y, Z\}$.</span></span>

```qsharp
operation R (pauli : Pauli, theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="25527-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="25527-107">Input</span></span>

### <a name="pauli--pauli"></a><span data-ttu-id="25527-108">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="25527-108">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="25527-109">Der Pauli-Operator ($ \mu $), der zum bilden der Drehung exponentiell berechnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25527-109">Pauli operator ($\mu$) to be exponentiated to form the rotation.</span></span>


### <a name="theta--double"></a><span data-ttu-id="25527-110">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="25527-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="25527-111">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="25527-111">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="25527-112">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="25527-112">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="25527-113">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25527-113">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="25527-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="25527-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="25527-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25527-115">Remarks</span></span>

<span data-ttu-id="25527-116">Wenn Sie mit aufgerufen `pauli = PauliI` wird, wendet dieser Vorgang eine *globale Phase* an.</span><span class="sxs-lookup"><span data-stu-id="25527-116">When called with `pauli = PauliI`, this operation applies a *global phase*.</span></span> <span data-ttu-id="25527-117">Diese Phase kann bei Verwendung mit dem-Funktor von Bedeutung sein `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="25527-117">This phase can be significant when used with the `Controlled` functor.</span></span>