---
uid: Microsoft.Quantum.Intrinsic.R1
title: R1-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: 07cce580b50fef5664fdac32bb4fae0ba22d25e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849352"
---
# <a name="r1-operation"></a><span data-ttu-id="b71d9-102">R1-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b71d9-102">R1 operation</span></span>

<span data-ttu-id="b71d9-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="b71d9-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="b71d9-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b71d9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b71d9-105">Wendet eine Drehung um den $ \ket {1} $-Zustand um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="b71d9-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="b71d9-106">\begin{align} R_1 (\orta) \mathrel{: =} \operatorname{Diag} (1, e ^ {i\der TA}).</span><span class="sxs-lookup"><span data-stu-id="b71d9-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="b71d9-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="b71d9-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b71d9-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b71d9-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="b71d9-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b71d9-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b71d9-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b71d9-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="b71d9-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="b71d9-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="b71d9-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b71d9-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b71d9-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b71d9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b71d9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b71d9-114">Remarks</span></span>

<span data-ttu-id="b71d9-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="b71d9-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```