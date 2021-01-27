---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Gewickepaulis-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 8aeea795ef5409339e8a1b39c3ffcfaf29d675b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851971"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="0e369-102">Gewickepaulis-Funktion</span><span class="sxs-lookup"><span data-stu-id="0e369-102">WeightOnePaulis function</span></span>

<span data-ttu-id="0e369-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0e369-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0e369-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0e369-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0e369-105">Gibt ein Array aller Gewichtungs-1-Pauli-Operatoren für eine angegebene Anzahl von Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="0e369-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="0e369-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="0e369-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="0e369-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0e369-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0e369-108">Die Anzahl der Qubits, für die die zurückgegebenen Pauli-Operatoren definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0e369-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="0e369-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="0e369-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="0e369-110">Ein Array von multiqubit-Pauli-Operatoren, die jeweils als ein Array mit einer Länge dargestellt werden `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="0e369-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>