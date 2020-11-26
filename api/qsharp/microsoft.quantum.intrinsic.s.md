---
uid: Microsoft.Quantum.Intrinsic.S
title: S-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: S
qsharp.summary: Applies the S gate to a single qubit.
ms.openlocfilehash: c697408c4efe1963787b5aee8f0d3bb6b9e64dd5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198451"
---
# <a name="s-operation"></a><span data-ttu-id="6940f-102">S-Vorgang</span><span class="sxs-lookup"><span data-stu-id="6940f-102">S operation</span></span>

<span data-ttu-id="6940f-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="6940f-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="6940f-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="6940f-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="6940f-105">Wendet das S-Gate auf ein einzelnes Qubit an.</span><span class="sxs-lookup"><span data-stu-id="6940f-105">Applies the S gate to a single qubit.</span></span>

```qsharp
operation S (qubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="6940f-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6940f-106">Description</span></span>

<span data-ttu-id="6940f-107">Dieser Vorgang kann durch die einheitliche Matrix \begin{align} S \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ 0 & i \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="6940f-107">This operation can be simulated by the unitary matrix \begin{align} S \mathrel{:=} \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="6940f-108">\end{align}</span><span class="sxs-lookup"><span data-stu-id="6940f-108">\end{align}</span></span>

## <a name="input"></a><span data-ttu-id="6940f-109">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6940f-109">Input</span></span>

### <a name="qubit--qubit"></a><span data-ttu-id="6940f-110">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="6940f-110">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="6940f-111">Das Qubit, auf das das Gate angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6940f-111">Qubit to which the gate should be applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6940f-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6940f-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

