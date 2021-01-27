---
uid: Microsoft.Quantum.Measurement.MultiM
title: Multim-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: b7f4083bde84c204611ea33746ae351a3e27b946
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857008"
---
# <a name="multim-operation"></a><span data-ttu-id="43101-102">Multim-Vorgang</span><span class="sxs-lookup"><span data-stu-id="43101-102">MultiM operation</span></span>

<span data-ttu-id="43101-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="43101-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="43101-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="43101-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="43101-105">Misst jedes Qubit in einem angegebenen Array standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="43101-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="43101-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="43101-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="43101-107">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="43101-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="43101-108">Ein Array von zu messenden Qubits.</span><span class="sxs-lookup"><span data-stu-id="43101-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="43101-109">Ausgabe: __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="43101-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="43101-110">Ein Array von Messergebnissen.</span><span class="sxs-lookup"><span data-stu-id="43101-110">An array of measurement results.</span></span>