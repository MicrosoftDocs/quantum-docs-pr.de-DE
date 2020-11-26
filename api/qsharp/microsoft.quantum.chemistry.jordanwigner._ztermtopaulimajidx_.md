---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ZTermToPauliMajIdx_
title: _Ztermtopaulimajidx_ -Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ZTermToPauliMajIdx_
qsharp.summary: Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.
ms.openlocfilehash: 13897d831bc3382dbb23b653c5905978330eb622
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214992"
---
# <a name="_ztermtopaulimajidx_-function"></a><span data-ttu-id="4ec48-102">_Ztermtopaulimajidx_ -Funktion</span><span class="sxs-lookup"><span data-stu-id="4ec48-102">_ZTermToPauliMajIdx_ function</span></span>

<span data-ttu-id="4ec48-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="4ec48-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="4ec48-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="4ec48-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="4ec48-105">Konvertiert einen generatorindex, der einen Z-Begriff beschreibt, in den Ausdruck ' generatorindex [] ' in Bezug auf Paulis.</span><span class="sxs-lookup"><span data-stu-id="4ec48-105">Converts a GeneratorIndex describing a Z term to an expression 'GeneratorIndex[]' in terms of Paulis.</span></span>

```qsharp
function _ZTermToPauliMajIdx_ (term : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex
```


## <a name="input"></a><span data-ttu-id="4ec48-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4ec48-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="4ec48-107">Begriff: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="4ec48-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="4ec48-108">`GeneratorIndex` , der einen Z-Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ec48-108">`GeneratorIndex` representing a Z term.</span></span>



## <a name="output--optimizedbetermindex"></a><span data-ttu-id="4ec48-109">Ausgabe: [optimizedbetermindex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span><span class="sxs-lookup"><span data-stu-id="4ec48-109">Output : [OptimizedBETermIndex](xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedBETermIndex)</span></span>

<span data-ttu-id="4ec48-110">' Generatorindex [] ' ausgedrückt: Z-Begriff als Pauli-Begriffe.</span><span class="sxs-lookup"><span data-stu-id="4ec48-110">'GeneratorIndex[]' expressing Z term as Pauli terms.</span></span>