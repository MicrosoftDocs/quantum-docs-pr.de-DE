---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: ResetAll-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: d22ce607e8e5cb3a1c041dc1973875f2a0777d2b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198689"
---
# <a name="resetall-operation"></a><span data-ttu-id="38be9-102">ResetAll-Vorgang</span><span class="sxs-lookup"><span data-stu-id="38be9-102">ResetAll operation</span></span>

<span data-ttu-id="38be9-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="38be9-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="38be9-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="38be9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="38be9-105">Messen Sie bei einem Array von Qubits diese, und stellen Sie sicher, dass Sie sich im Zustand | 0 ⟩ befinden, sodass Sie sicher freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="38be9-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="38be9-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="38be9-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="38be9-107">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="38be9-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="38be9-108">Ein Array von Qubits, deren Zustände auf $ \ket $ zurückgesetzt werden sollen {0} .</span><span class="sxs-lookup"><span data-stu-id="38be9-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="38be9-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="38be9-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

