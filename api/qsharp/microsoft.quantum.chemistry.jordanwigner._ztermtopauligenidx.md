---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliGenIdx
title: _ZTermToPauliGenIdx-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliGenIdx
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: f4643ef03a0178f2c3ba1ea68f36f2f3fcd7b9ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215026"
---
# <a name="_ztermtopauligenidx-function"></a><span data-ttu-id="ede0e-102">_ZTermToPauliGenIdx-Funktion</span><span class="sxs-lookup"><span data-stu-id="ede0e-102">_ZTermToPauliGenIdx function</span></span>

<span data-ttu-id="ede0e-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="ede0e-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="ede0e-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="ede0e-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="ede0e-105">Konvertiert einen generatorindex, der einen Z-Begriff beschreibt, in den Ausdruck ' generatorindex [] ' in Bezug auf Paulis.</span><span class="sxs-lookup"><span data-stu-id="ede0e-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliGenIdx (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex[]
```


## <a name="input"></a><span data-ttu-id="ede0e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ede0e-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="ede0e-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="ede0e-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="ede0e-108">`GeneratorIndex` , der einen Z-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="ede0e-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="ede0e-109">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span><span class="sxs-lookup"><span data-stu-id="ede0e-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)[]</span></span>

<span data-ttu-id="ede0e-110">' Generatorindex [] ' ausgedrückt: Z-Begriff als Pauli-Begriffe.</span><span class="sxs-lookup"><span data-stu-id="ede0e-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>