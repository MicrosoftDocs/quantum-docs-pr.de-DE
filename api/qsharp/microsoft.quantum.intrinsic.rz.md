---
uid: Microsoft.Quantum.Intrinsic.Rz
title: RZ-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: d637abf3562eb60705da517467939dc588229c39
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198621"
---
# <a name="rz-operation"></a><span data-ttu-id="bcda0-102">RZ-Vorgang</span><span class="sxs-lookup"><span data-stu-id="bcda0-102">Rz operation</span></span>

<span data-ttu-id="bcda0-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="bcda0-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="bcda0-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="bcda0-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="bcda0-105">Wendet eine Drehung zum $z $-Achse um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="bcda0-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="bcda0-106">\begin{align} R_z (\orta) \mathrel{: =} e ^ {-i \Der Ta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \Der Ta/2} & 0 \\ \\ 0 & e ^ {i \Der Ta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="bcda0-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="bcda0-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="bcda0-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bcda0-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="bcda0-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="bcda0-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bcda0-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bcda0-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcda0-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="bcda0-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bcda0-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bcda0-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcda0-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bcda0-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bcda0-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bcda0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcda0-114">Remarks</span></span>

<span data-ttu-id="bcda0-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="bcda0-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```