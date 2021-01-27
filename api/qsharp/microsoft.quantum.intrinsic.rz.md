---
uid: Microsoft.Quantum.Intrinsic.Rz
title: RZ-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 4282fcc216173234ec742991b8f0fa1be203da0d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849291"
---
# <a name="rz-operation"></a><span data-ttu-id="e81fd-102">RZ-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e81fd-102">Rz operation</span></span>

<span data-ttu-id="e81fd-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="e81fd-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="e81fd-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e81fd-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e81fd-105">Wendet eine Drehung zum $z $-Achse um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="e81fd-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="e81fd-106">\begin{align} R_z (\orta) \mathrel{: =} e ^ {-i \Der Ta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \Der Ta/2} & 0 \\ \\ 0 & e ^ {i \Der Ta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="e81fd-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="e81fd-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="e81fd-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e81fd-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e81fd-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="e81fd-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e81fd-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e81fd-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e81fd-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="e81fd-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e81fd-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e81fd-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e81fd-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e81fd-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e81fd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="e81fd-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e81fd-114">Remarks</span></span>

<span data-ttu-id="e81fd-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="e81fd-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```