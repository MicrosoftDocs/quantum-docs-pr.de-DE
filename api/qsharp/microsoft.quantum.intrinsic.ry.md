---
uid: Microsoft.Quantum.Intrinsic.Ry
title: Ry-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Ry
qsharp.summary: >-
  Applies a rotation about the $y$-axis by a given angle.

  \begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 9966693eb7283e855f7b72e910aa3604d6c2bd61
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706535"
---
# <a name="ry-operation"></a><span data-ttu-id="15b84-102">Ry-Vorgang</span><span class="sxs-lookup"><span data-stu-id="15b84-102">Ry operation</span></span>

<span data-ttu-id="15b84-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="15b84-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="15b84-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="15b84-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="15b84-105">Wendet eine Drehung zum $y $-Achse um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="15b84-105">Applies a rotation about the $y$-axis by a given angle.</span></span>

<span data-ttu-id="15b84-106">\begin{align} R_y (\orta) \mathrel{: =} e ^ {-i \erta \ sigma_y/2} = \begin{bmatrix} \cos \bruchteil {\thta} {2} &-\sin \bruchteil {\thta} {2} \\ \\ \sin \bruchteil {\thta} {2} & \cos \bruchteil {\thta} {2} \end{bmatrix}.  </span><span class="sxs-lookup"><span data-stu-id="15b84-106">\begin{align} R_y(\theta) \mathrel{:=} e^{-i \theta \sigma_y / 2} = \begin{bmatrix} \cos \frac{\theta}{2} & -\sin \frac{\theta}{2}  \\\\ \sin \frac{\theta}{2} & \cos \frac{\theta}{2} \end{bmatrix}.</span></span>
<span data-ttu-id="15b84-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="15b84-107">\end{align}</span></span>

```qsharp
operation Ry (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="15b84-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="15b84-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="15b84-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="15b84-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="15b84-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="15b84-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="15b84-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="15b84-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="15b84-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15b84-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="15b84-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="15b84-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="15b84-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15b84-114">Remarks</span></span>

<span data-ttu-id="15b84-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="15b84-115">Equivalent to:</span></span>

```qsharp
R(PauliY, theta, qubit);
```