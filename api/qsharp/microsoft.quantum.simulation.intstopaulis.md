---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: Intstopaulis-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 6904054bb1aff3a57c80882694b4c217812b2b81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842240"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="26fad-102">Intstopaulis-Funktion</span><span class="sxs-lookup"><span data-stu-id="26fad-102">IntsToPaulis function</span></span>

<span data-ttu-id="26fad-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="26fad-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="26fad-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26fad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26fad-105">Konvertiert ein Array von ganzen Zahlen in ein Array von Single-Qubit-Pauli-Operatoren.</span><span class="sxs-lookup"><span data-stu-id="26fad-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="26fad-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="26fad-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="26fad-107">int: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="26fad-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="26fad-108">Array aus ganzen Zahlen im Bereich, der in die `0..3`  Pauli-Operatoren konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26fad-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="26fad-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="26fad-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="26fad-110">Ein Array `paulis` von Pauli-Operatoren mit `Pauli[]` derselben Länge wie `ints` , das `paulis[idxPauli]` gleich dem Element von ist, das `[PauliI, PauliX, PauliY, PauliZ]` von angegeben wird `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="26fad-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>