---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Permutequbits-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 0f4d8819d5b08f4d5370f8fdc407b2eb2a3e5f21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703907"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="c6751-102">Permutequbits-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c6751-102">PermuteQubits operation</span></span>

<span data-ttu-id="c6751-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c6751-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c6751-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c6751-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c6751-105">Permutes Qubits mithilfe des Swap-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c6751-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="c6751-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c6751-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="c6751-107">Reihenfolge: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c6751-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c6751-108">Beschreibt die neue Reihenfolge der Qubits, bei der das Qubit bei Index i nun die Reihenfolge [i] hat.</span><span class="sxs-lookup"><span data-stu-id="c6751-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="c6751-109">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c6751-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c6751-110">Das Qubit-Register, das bearbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6751-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c6751-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c6751-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

