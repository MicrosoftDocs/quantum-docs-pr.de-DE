---
uid: Microsoft.Quantum.Intrinsic.T
title: T-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: 868031386c95f65ae956b5e444c6d87d7ea0a697
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707098"
---
# <a name="t-operation"></a><span data-ttu-id="c6bf9-102">T-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c6bf9-102">T operation</span></span>

<span data-ttu-id="c6bf9-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c6bf9-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c6bf9-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6bf9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6bf9-105">Wendet das T-Gate auf ein einzelnes Qubit an.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="c6bf9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c6bf9-106">Description</span></span>

<span data-ttu-id="c6bf9-107">Dieser Vorgang kann durch die einheitliche Matrix \begin{ALIGN} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \pi/4} \end{bmatrix}. simuliert werden.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="c6bf9-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="c6bf9-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="c6bf9-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c6bf9-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="c6bf9-110">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c6bf9-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c6bf9-111">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6bf9-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c6bf9-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c6bf9-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

