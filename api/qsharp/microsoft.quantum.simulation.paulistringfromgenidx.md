---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Paulistringfromgenidx-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: a937dc648c5de5a5f6de7da996448af497b92185
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230309"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="4dc1d-102">Paulistringfromgenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="4dc1d-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="4dc1d-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4dc1d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4dc1d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4dc1d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4dc1d-105">Extrahiert die Pauli-Zeichenfolge und ihre Qubit-Indizes eines von einem beschriebenen Pauli-Begriffs `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="4dc1d-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="4dc1d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4dc1d-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="4dc1d-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="4dc1d-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="4dc1d-108">`GeneratorIndex` der Typ, der einen Pauli-Begriff codiert.</span><span class="sxs-lookup"><span data-stu-id="4dc1d-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="4dc1d-109">Ausgabe: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="4dc1d-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="4dc1d-110">Die Pauli-Zeichenfolge des von einem beschriebenen Begriffs `GeneratorIndex` und Indizes zu den Qubits, auf die Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4dc1d-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>