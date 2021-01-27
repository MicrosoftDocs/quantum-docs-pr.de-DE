---
uid: Microsoft.Quantum.Intrinsic.Reset
title: Vorgang zurücksetzen
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Reset
qsharp.summary: Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.
ms.openlocfilehash: b4275796b966bfe7f55271f4e92866410a14e830
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98818644"
---
# <a name="reset-operation"></a><span data-ttu-id="c14ea-102">Vorgang zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="c14ea-102">Reset operation</span></span>

<span data-ttu-id="c14ea-103">Namespace: [Microsoft. Quantum. intrinsisch](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c14ea-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c14ea-104">Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c14ea-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c14ea-105">Wenn ein einzelnes Qubit angegeben ist, wird es gemessen und sichergestellt, dass es sich im | 0 ⟩-Zustand befindet, sodass es sicher freigegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="c14ea-105">Given a single qubit, measures it and ensures it is in the |0⟩ state such that it can be safely released.</span></span>

```qsharp
operation Reset (target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="c14ea-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c14ea-106">Input</span></span>

### <a name="target--qubit"></a><span data-ttu-id="c14ea-107">Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="c14ea-107">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="c14ea-108">Das Qubit, dessen Zustand auf $ \ket $ zurückgesetzt werden soll {0} .</span><span class="sxs-lookup"><span data-stu-id="c14ea-108">The qubit whose state is to be reset to $\ket{0}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c14ea-109">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c14ea-109">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

