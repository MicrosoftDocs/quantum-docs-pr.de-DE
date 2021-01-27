---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionFunction
title: Jordanwignerfermionfunction-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: a1c0b56e18f3adfb6c413880cc0c155741a3255a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98838861"
---
# <a name="jordanwignerfermionfunction-function"></a><span data-ttu-id="34876-102">Jordanwignerfermionfunction-Funktion</span><span class="sxs-lookup"><span data-stu-id="34876-102">JordanWignerFermionFunction function</span></span>

<span data-ttu-id="34876-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="34876-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="34876-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="34876-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="34876-105">Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in der jordanwigner-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="34876-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function JordanWignerFermionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="34876-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="34876-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="34876-107">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="34876-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="34876-108">Ein Generator Index, der als einheitliche Evolution in der jordanwigner dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="34876-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="34876-109">Ausgabe: [evolutioneinheitlich](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="34876-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="34876-110">Ein, `EvolutionUnitary` der die Zeitentwicklung durch den in ' generatorindex ' referenzierten Begriff darstellt.</span><span class="sxs-lookup"><span data-stu-id="34876-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>