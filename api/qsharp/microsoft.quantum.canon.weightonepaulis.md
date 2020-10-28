---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: Gewickepaulis-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703709"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="26405-102">Gewickepaulis-Funktion</span><span class="sxs-lookup"><span data-stu-id="26405-102">WeightOnePaulis function</span></span>

<span data-ttu-id="26405-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="26405-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="26405-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="26405-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="26405-105">Gibt ein Array aller Gewichtungs-1-Pauli-Operatoren für eine angegebene Anzahl von Qubits zurück.</span><span class="sxs-lookup"><span data-stu-id="26405-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="26405-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="26405-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="26405-107">nqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="26405-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="26405-108">Die Anzahl der Qubits, für die die zurückgegebenen Pauli-Operatoren definiert sind.</span><span class="sxs-lookup"><span data-stu-id="26405-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="26405-109">Ausgabe: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="26405-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="26405-110">Ein Array von multiqubit-Pauli-Operatoren, die jeweils als ein Array mit einer Länge dargestellt werden `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="26405-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>