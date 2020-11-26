---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Gewickepaulis-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 904c606393131d51eaa44d464ad52bec509eaf72
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204537"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="626c0-102">Gewickepaulis-Funktion</span><span class="sxs-lookup"><span data-stu-id="626c0-102">WeightOnePaulis function</span></span>

<span data-ttu-id="626c0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="626c0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="626c0-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="626c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="626c0-105">Gibt ein Array aller Gewichtungs-1-Pauli-Operatoren für eine angegebene Anzahl von Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="626c0-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="626c0-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="626c0-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="626c0-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="626c0-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="626c0-108">Die Anzahl der Qubits, für die die zurückgegebenen Pauli-Operatoren definiert sind.</span><span class="sxs-lookup"><span data-stu-id="626c0-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="626c0-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="626c0-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="626c0-110">Ein Array von multiqubit-Pauli-Operatoren, die jeweils als ein Array mit einer Länge dargestellt werden `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="626c0-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>