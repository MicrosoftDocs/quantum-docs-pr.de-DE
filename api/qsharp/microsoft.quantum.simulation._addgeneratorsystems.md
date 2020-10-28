---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: _AddGeneratorSystems-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: 3bce9faf229f3b1f683e060437ec08da795ef185
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701784"
---
# <a name="_addgeneratorsystems-function"></a><span data-ttu-id="d11e3-102">_AddGeneratorSystems-Funktion</span><span class="sxs-lookup"><span data-stu-id="d11e3-102">_AddGeneratorSystems function</span></span>

<span data-ttu-id="d11e3-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="d11e3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="d11e3-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d11e3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d11e3-105">Fügt zwei `GeneratorSystem` s hinzu, um einen neuen zu erstellen `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="d11e3-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="d11e3-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d11e3-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="d11e3-107">idxterm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d11e3-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsa--int"></a><span data-ttu-id="d11e3-108">ntermsa: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d11e3-108">nTermsA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsb--int"></a><span data-ttu-id="d11e3-109">ntermsb: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d11e3-109">nTermsB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="generatorindexfunctiona--int---generatorindex"></a><span data-ttu-id="d11e3-110">generatorindexfunctiona: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d11e3-110">generatorIndexFunctionA : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="generatorindexfunctionb--int---generatorindex"></a><span data-ttu-id="d11e3-111">generatorindexfunctionb: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d11e3-111">generatorIndexFunctionB : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>





## <a name="output--generatorindex"></a><span data-ttu-id="d11e3-112">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="d11e3-112">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>



## <a name="remarks"></a><span data-ttu-id="d11e3-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d11e3-113">Remarks</span></span>

<span data-ttu-id="d11e3-114">Dies ist ein Zwischenschritt und sollte nicht aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d11e3-114">This is an intermediate step and should not be called.</span></span>