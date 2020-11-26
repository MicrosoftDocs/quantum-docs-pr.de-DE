---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Intstopaulis-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 2333dcbd2988480e2b2b9b217b26705f3578de00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230530"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="79970-102">Intstopaulis-Funktion</span><span class="sxs-lookup"><span data-stu-id="79970-102">IntsToPaulis function</span></span>

<span data-ttu-id="79970-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="79970-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="79970-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79970-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79970-105">Konvertiert ein Array von ganzen Zahlen in ein Array von Single-Qubit-Pauli-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="79970-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="79970-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="79970-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="79970-107">int: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="79970-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="79970-108">Array aus ganzen Zahlen im Bereich, der in die `0..3`  Pauli-Operatoren konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="79970-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="79970-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="79970-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="79970-110">Ein Array `paulis` von Pauli-Operatoren mit `Pauli[]` derselben Länge wie `ints` , das `paulis[idxPauli]` gleich dem Element von ist, das `[PauliI, PauliX, PauliY, PauliZ]` von angegeben wird `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="79970-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>