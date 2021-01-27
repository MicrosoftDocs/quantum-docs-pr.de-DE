---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Inttopauli-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842248"
---
# <a name="inttopauli-function"></a><span data-ttu-id="815b6-102">Inttopauli-Funktion</span><span class="sxs-lookup"><span data-stu-id="815b6-102">IntToPauli function</span></span>

<span data-ttu-id="815b6-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="815b6-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="815b6-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="815b6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="815b6-105">Konvertiert eine ganze Zahl in einen Single-Qubit-Pauli-Operator.</span><span class="sxs-lookup"><span data-stu-id="815b6-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="815b6-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="815b6-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="815b6-107">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="815b6-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="815b6-108">Ganzzahl im Bereich, der in die `0..3` Pauli-Operatoren konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="815b6-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="815b6-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="815b6-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="815b6-110">Ein `Pauli` Operator, der von angegeben wird `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="815b6-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>