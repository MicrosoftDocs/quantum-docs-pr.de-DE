---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Ry-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 5a1f762aacca5c72dc8dbe450ab8e8a4aef12c69
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198604"
---
# <a name="ry-operation"></a><span data-ttu-id="3ce17-102">Ry-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ce17-102">Ry operation</span></span>

<span data-ttu-id="3ce17-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="3ce17-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="3ce17-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ce17-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3ce17-105">Wendet eine Drehung zum $y $-Achse um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="3ce17-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="3ce17-106">\begin{align} R_y (\orta) \mathrel{: =} e ^ {-i \erta \ sigma_y/2} = \begin{bmatrix} \cos \bruchteil {\thta} {2} &-\sin \bruchteil {\thta} {2} \\ \\ \sin \bruchteil {\thta} {2} & \cos \bruchteil {\thta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="3ce17-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="3ce17-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="3ce17-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3ce17-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ce17-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="3ce17-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3ce17-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3ce17-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ce17-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="3ce17-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3ce17-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3ce17-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ce17-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ce17-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ce17-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ce17-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ce17-114">Remarks</span></span>

<span data-ttu-id="3ce17-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="3ce17-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```