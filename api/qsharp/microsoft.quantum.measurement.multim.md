---
uid: Microsoft.Quantum.Measurement.MultiM
title: Multim-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: c39601f3e8b272b9341f1789b4c8e7230cb4182c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226994"
---
# <a name="multim-operation"></a><span data-ttu-id="a4718-102">Multim-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a4718-102">MultiM operation</span></span>

<span data-ttu-id="a4718-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="a4718-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="a4718-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a4718-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a4718-105">Misst jedes Qubit in einem angegebenen Array standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="a4718-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="a4718-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a4718-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="a4718-107">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a4718-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a4718-108">Ein Array von zu messenden Qubits.</span><span class="sxs-lookup"><span data-stu-id="a4718-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="a4718-109">Ausgabe: __ungültig <Result>__[]</span><span class="sxs-lookup"><span data-stu-id="a4718-109">Output : __invalid<Result>__[]</span></span>

<span data-ttu-id="a4718-110">Ein Array von Messergebnissen.</span><span class="sxs-lookup"><span data-stu-id="a4718-110">An array of measurement results.</span></span>