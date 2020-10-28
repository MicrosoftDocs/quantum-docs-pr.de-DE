---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: Inttopauli-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: f0f1186f14a0dc30bb34bd29f148cdc830fd1337
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724851"
---
# <a name="inttopauli-function"></a><span data-ttu-id="ea083-102">Inttopauli-Funktion</span><span class="sxs-lookup"><span data-stu-id="ea083-102">IntToPauli function</span></span>

<span data-ttu-id="ea083-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ea083-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ea083-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ea083-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ea083-105">Konvertiert eine ganze Zahl in einen Single-Qubit-Pauli-Operator.</span><span class="sxs-lookup"><span data-stu-id="ea083-105">Converts a integer to a single-qubit Pauli operator.</span></span>

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a><span data-ttu-id="ea083-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ea083-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="ea083-107">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ea083-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ea083-108">Ganzzahl im Bereich, der in die `0..3` Pauli-Operatoren konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ea083-108">Integer in the range `0..3` to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="ea083-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ea083-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ea083-110">Ein `Pauli` Operator, der von angegeben wird `[PauliI, PauliX, PauliY, PauliZ][idx]` .</span><span class="sxs-lookup"><span data-stu-id="ea083-110">A `Pauli` operator given by `[PauliI, PauliX, PauliY, PauliZ][idx]`.</span></span>