---
uid: Microsoft.Quantum.Intrinsic.ResetAll
title: ResetAll-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ResetAll
qsharp.summary: Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.
ms.openlocfilehash: 2b8e7fc0e7881d8c1bd6f14c150476262b7a2b19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849320"
---
# <a name="resetall-operation"></a><span data-ttu-id="26a0b-102">ResetAll-Vorgang</span><span class="sxs-lookup"><span data-stu-id="26a0b-102">ResetAll operation</span></span>

<span data-ttu-id="26a0b-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="26a0b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="26a0b-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="26a0b-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="26a0b-105">Messen Sie bei einem Array von Qubits diese, und stellen Sie sicher, dass Sie sich im Zustand | 0 ⟩ befinden, sodass Sie sicher freigegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="26a0b-105">Given an array of qubits, measure them and ensure they are in the |0⟩ state such that they can be safely released.</span></span>

```qsharp
operation ResetAll (qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="26a0b-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="26a0b-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="26a0b-107">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="26a0b-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="26a0b-108">Ein Array von Qubits, deren Zustände auf $ \ket $ zurückgesetzt werden sollen {0} .</span><span class="sxs-lookup"><span data-stu-id="26a0b-108">An array of qubits whose states are to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="26a0b-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="26a0b-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

