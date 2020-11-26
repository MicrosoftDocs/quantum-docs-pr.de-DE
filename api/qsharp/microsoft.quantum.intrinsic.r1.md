---
uid: Microsoft.Quantum.Intrinsic.R1
title: R1-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: R1
qsharp.summary: >-
  Applies a rotation about the $\ket{1}$ state by a given angle.

  \begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}). \end{align}
ms.openlocfilehash: a98c2cc0b309a239650afd2910cc74dffa9f899a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198808"
---
# <a name="r1-operation"></a><span data-ttu-id="85a66-102">R1-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85a66-102">R1 operation</span></span>

<span data-ttu-id="85a66-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="85a66-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="85a66-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="85a66-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="85a66-105">Wendet eine Drehung um den $ \ket {1} $-Zustand um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="85a66-105">Applies a rotation about the $\ket{1}$ state by a given angle.</span></span>

<span data-ttu-id="85a66-106">\begin{align} R_1 (\orta) \mathrel{: =} \operatorname{Diag} (1, e ^ {i\der TA}).</span><span class="sxs-lookup"><span data-stu-id="85a66-106">\begin{align} R_1(\theta) \mathrel{:=} \operatorname{diag}(1, e^{i\theta}).</span></span>
<span data-ttu-id="85a66-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="85a66-107">\end{align}</span></span>

```qsharp
operation R1 (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="85a66-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85a66-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="85a66-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="85a66-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="85a66-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="85a66-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="85a66-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="85a66-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="85a66-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85a66-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="85a66-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="85a66-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="85a66-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85a66-114">Remarks</span></span>

<span data-ttu-id="85a66-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="85a66-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
R(PauliI, -theta, qubit);
```