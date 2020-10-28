---
uid: Microsoft.Quantum.Intrinsic.Rz
title: RZ-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Rz
qsharp.summary: >-
  Applies a rotation about the $z$-axis by a given angle.

  \begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}. \end{align}
ms.openlocfilehash: 954b0b097d4bffcb8047a9f0c8a4c28445653c5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707106"
---
# <a name="rz-operation"></a><span data-ttu-id="ca67b-102">RZ-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ca67b-102">Rz operation</span></span>

<span data-ttu-id="ca67b-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="ca67b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="ca67b-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca67b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ca67b-105">Wendet eine Drehung zum $z $-Achse um einen angegebenen Winkel an.</span><span class="sxs-lookup"><span data-stu-id="ca67b-105">Applies a rotation about the $z$-axis by a given angle.</span></span>

<span data-ttu-id="ca67b-106">\begin{align} R_z (\orta) \mathrel{: =} e ^ {-i \Der Ta \ sigma_z/2} = \begin{bmatrix} e ^ {-i \Der Ta/2} & 0 \\ \\ 0 & e ^ {i \Der Ta/2} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="ca67b-106">\begin{align} R_z(\theta) \mathrel{:=} e^{-i \theta \sigma_z / 2} = \begin{bmatrix} e^{-i \theta / 2} & 0 \\\\ 0 & e^{i \theta / 2} \end{bmatrix}.</span></span>
<span data-ttu-id="ca67b-107">\end{align}</span><span class="sxs-lookup"><span data-stu-id="ca67b-107">\end{align}</span></span>

```qsharp
operation Rz (theta : Double, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="ca67b-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca67b-108">Input</span></span>

### <a name="theta--double"></a><span data-ttu-id="ca67b-109">-Ta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ca67b-109">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ca67b-110">Der Winkel, um den das Qubit gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca67b-110">Angle about which the qubit is to be rotated.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="ca67b-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ca67b-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ca67b-112">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca67b-112">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ca67b-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca67b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ca67b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca67b-114">Remarks</span></span>

<span data-ttu-id="ca67b-115">Äquivalent zu:</span><span class="sxs-lookup"><span data-stu-id="ca67b-115">Equivalent to:</span></span>

```qsharp
R(PauliZ, theta, qubit);
```