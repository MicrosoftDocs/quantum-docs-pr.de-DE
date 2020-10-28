---
uid: Microsoft.Quantum.Simulation.PauliCoefficientFromGenIdx
title: Paulicoefficientfromgenidx-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliCoefficientFromGenIdx
qsharp.summary: Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.
ms.openlocfilehash: 5bbc8d6113fb36bfd4050b98538bb61bbac02185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706671"
---
# <a name="paulicoefficientfromgenidx-function"></a><span data-ttu-id="c4e29-102">Paulicoefficientfromgenidx-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4e29-102">PauliCoefficientFromGenIdx function</span></span>

<span data-ttu-id="c4e29-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c4e29-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c4e29-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4e29-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4e29-105">Extrahiert den Koeffizient eines Pauli-Begriffs, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="c4e29-105">Extracts the coefficient of a Pauli term described by a `GeneratorIndex`.</span></span>

```qsharp
function PauliCoefficientFromGenIdx (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Double
```


## <a name="input"></a><span data-ttu-id="c4e29-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="c4e29-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="c4e29-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c4e29-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="c4e29-108">`GeneratorIndex` der Typ, der einen Pauli-Begriff codiert.</span><span class="sxs-lookup"><span data-stu-id="c4e29-108">`GeneratorIndex` type that encodes a Pauli term.</span></span>



## <a name="output--double"></a><span data-ttu-id="c4e29-109">Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c4e29-109">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c4e29-110">Der Koeffizient des Begriffs, der von einem beschrieben wird `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="c4e29-110">The coefficient of the term described by a `GeneratorIndex`.</span></span>