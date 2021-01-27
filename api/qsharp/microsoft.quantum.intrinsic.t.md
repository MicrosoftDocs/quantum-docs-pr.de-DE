---
uid: Microsoft.Quantum.Intrinsic.T
title: T-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: T
qsharp.summary: Applies the T gate to a single qubit.
ms.openlocfilehash: bee252d9905aed26f6bf663f895e464e38073f44
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817515"
---
# <a name="t-operation"></a><span data-ttu-id="ca826-102">T-Vorgang</span><span class="sxs-lookup"><span data-stu-id="ca826-102">T operation</span></span>

<span data-ttu-id="ca826-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="ca826-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="ca826-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="ca826-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="ca826-105">Wendet das T-Gate auf ein einzelnes Qubit an.</span><span class="sxs-lookup"><span data-stu-id="ca826-105">Applies the T gate to a single qubit.</span></span>

```qsharp
operation T (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ca826-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca826-106">Description</span></span>

<span data-ttu-id="ca826-107">Dieser Vorgang kann durch die einheitliche Matrix \begin{ALIGN} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & e ^ {i \pi/4} \end{bmatrix}. simuliert werden.</span><span class="sxs-lookup"><span data-stu-id="ca826-107">This operation can be simulated by the unitary matrix \begin{align} T \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & e^{i \pi / 4} \end{bmatrix}.</span></span>
<span data-ttu-id="ca826-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="ca826-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="ca826-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ca826-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="ca826-110">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ca826-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ca826-111">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca826-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ca826-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca826-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

