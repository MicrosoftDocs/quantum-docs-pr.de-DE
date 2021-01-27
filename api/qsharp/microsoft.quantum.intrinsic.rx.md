---
uid: Microsoft.Quantum.Intrinsic.Rx
title: RX-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rx
qsharp.summary: >-
  Applies a rotation about the $x$-axis by a given angle.

  \begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: b6224952ea5eabfc7177ead557378fb07b9e597f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849302"
---
# <a name="rx-operation"></a><span data-ttu-id="3ab75-102">RX-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3ab75-102">Rx operation</span></span>

<span data-ttu-id="3ab75-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="3ab75-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="3ab75-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ab75-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3ab75-105">Wendet eine Drehung zum $x $-Achse um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="3ab75-105">Applies a rotation about the $x$-axis by a given angle.</span></span>

<span data-ttu-id="3ab75-106">\begin{align} R_x (\orta) \mathrel{: =} e ^ {-i \erta \ sigma_x/2} = \begin{bmatrix} \cos \bruchteil {\thta} {2} &-i\sin \bruchteil {\thta} {2} \\ \\ -i\sin \bruchteil {\thta} {2} & \cos \bruch {\thta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="3ab75-106">\begin{align} R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -i\sin \frac{\theta}{2}  \\\\ -i\sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="3ab75-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="3ab75-107">\end{align}</span></span>

```qsharp
operation Rx (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3ab75-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3ab75-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="3ab75-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3ab75-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3ab75-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ab75-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="3ab75-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3ab75-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3ab75-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ab75-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ab75-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ab75-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ab75-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3ab75-114">Remarks</span></span>

<span data-ttu-id="3ab75-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="3ab75-115">Equivalent to:</span></span>

```qsharp
R(PauliX, theta, qubit);
```