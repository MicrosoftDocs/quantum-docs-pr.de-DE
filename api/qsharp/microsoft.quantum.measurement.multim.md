---
uid: Microsoft.Quantum.Measurement.MultiM
title: Multim-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Measurement
qsharp.name: MultiM
qsharp.summary: Measures each qubit in a given array in the standard basis.
ms.openlocfilehash: 36de9dbdfc96f6e1698ee4537405f7cb74e44262
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701927"
---
# <a name="multim-operation"></a><span data-ttu-id="f6dd2-102">Multim-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f6dd2-102">MultiM operation</span></span>

<span data-ttu-id="f6dd2-103">Namespace: [Microsoft. Quantum. Measurement](xref:Microsoft.Quantum.Measurement)</span><span class="sxs-lookup"><span data-stu-id="f6dd2-103">Namespace: [Microsoft.Quantum.Measurement](xref:Microsoft.Quantum.Measurement)</span></span>

<span data-ttu-id="f6dd2-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f6dd2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f6dd2-105">Misst jedes Qubit in einem angegebenen Array standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="f6dd2-105">Measures each qubit in a given array in the standard basis.</span></span>

```qsharp
operation MultiM (targets : Qubit[]) : Result[]
```


## <a name="input"></a><span data-ttu-id="f6dd2-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f6dd2-106">Input</span></span>

### <a name="targets--qubit"></a><span data-ttu-id="f6dd2-107">Ziele: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f6dd2-107">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f6dd2-108">Ein Array von zu messenden Qubits.</span><span class="sxs-lookup"><span data-stu-id="f6dd2-108">An array of qubits to be measured.</span></span>



## <a name="output--__invalidresult__"></a><span data-ttu-id="f6dd2-109">Ausgabe: __ungültig <Result>__ []</span><span class="sxs-lookup"><span data-stu-id="f6dd2-109">Output : __invalid<Result>__ []</span></span>

<span data-ttu-id="f6dd2-110">Ein Array von Messergebnissen.</span><span class="sxs-lookup"><span data-stu-id="f6dd2-110">An array of measurement results.</span></span>