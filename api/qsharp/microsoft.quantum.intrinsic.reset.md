---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Vorgang zurücksetzen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: 61b5e4ccdf009dcb6c639e3d8e23bc73a6e475b5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198672"
---
# <a name="reset-operation"></a><span data-ttu-id="82cfb-102">Vorgang zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="82cfb-102">Reset operation</span></span>

<span data-ttu-id="82cfb-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="82cfb-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="82cfb-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="82cfb-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="82cfb-105">Wenn ein einzelnes Qubit angegeben ist, wird es gemessen und sichergestellt, dass es sich im | 0 ⟩-Zustand befindet, sodass es sicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="82cfb-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="82cfb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="82cfb-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="82cfb-107">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="82cfb-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="82cfb-108">Das Qubit, dessen Zustand auf $ \ket $ zurückgesetzt werden soll {0} .</span><span class="sxs-lookup"><span data-stu-id="82cfb-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="82cfb-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="82cfb-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

