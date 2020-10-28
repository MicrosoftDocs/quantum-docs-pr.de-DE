---
uid: Microsoft.Quantum.Simulation.PauliStringFromGenIdx
title: Paulistringfromgenidx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliStringFromGenIdx
qsharp.summary: Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 33da4bc3d7e58b87aef75b453b6af09a51214923
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701712"
---
# <a name="paulistringfromgenidx-function"></a><span data-ttu-id="ff70e-102">Paulistringfromgenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="ff70e-102">PauliStringFromGenIdx function</span></span>

<span data-ttu-id="ff70e-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="ff70e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="ff70e-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ff70e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ff70e-105">Extrahiert die Pauli-Zeichenfolge und ihre Qubit-Indizes eines von einem beschriebenen Pauli-Begriffs `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="ff70e-105">Extracts the Pauli string and its qubit indices of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliStringFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : (Pauli[], Int[])
```


## <a name="input"></a><span data-ttu-id="ff70e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ff70e-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="ff70e-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ff70e-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ff70e-108">`GeneratorIndex` der Typ, der einen Pauli-Begriff codiert.</span><span class="sxs-lookup"><span data-stu-id="ff70e-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--pauliint"></a><span data-ttu-id="ff70e-109">Ausgabe: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="ff70e-109">Output : ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

<span data-ttu-id="ff70e-110">Die Pauli-Zeichenfolge des von einem beschriebenen Begriffs `GeneratorIndex` und Indizes zu den Qubits, auf die Sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ff70e-110">The Pauli string of the term described by a `GeneratorIndex`, and indices to the qubits it acts on.</span></span>