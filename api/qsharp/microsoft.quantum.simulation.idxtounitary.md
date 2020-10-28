---
uid: Microsoft.Quantum.Simulation.IdxToUnitary
title: Idx| einheitliche-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdxToUnitary
qsharp.summary: Used in implementation of `PauliBlockEncoding`
ms.openlocfilehash: a142d8a5af56a43de6341e3c0bdc77f50030f06e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701736"
---
# <a name="idxtounitary-function"></a><span data-ttu-id="b3726-102">Idx| einheitliche-Funktion</span><span class="sxs-lookup"><span data-stu-id="b3726-102">IdxToUnitary function</span></span>

<span data-ttu-id="b3726-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b3726-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b3726-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b3726-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b3726-105">Wird in der Implementierung von `PauliBlockEncoding`</span><span class="sxs-lookup"><span data-stu-id="b3726-105">Used in implementation of `PauliBlockEncoding`</span></span>

```qsharp
function IdxToUnitary (idx : Int, genFun : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), genIdxToUnitary : (Microsoft.Quantum.Simulation.GeneratorIndex -> (Qubit[] => Unit is Adj + Ctl))) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="b3726-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3726-106">Input</span></span>

### <a name="idx--int"></a><span data-ttu-id="b3726-107">idx: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b3726-107">idx : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="genfun--int---generatorindex"></a><span data-ttu-id="b3726-108">genfun: [int](xref:microsoft.quantum.lang-ref.int) -> [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="b3726-108">genFun : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="genidxtounitary--generatorindex---qubit--unit-adj--ctl"></a><span data-ttu-id="b3726-109">genidxdeeinheitlicher: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) - -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="b3726-109">genIdxToUnitary : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>





## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="b3726-110">Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="b3726-110">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="see-also"></a><span data-ttu-id="b3726-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b3726-111">See Also</span></span>

- [<span data-ttu-id="b3726-112">Microsoft. Quantum. Simulation. pauliblockencoding</span><span class="sxs-lookup"><span data-stu-id="b3726-112">Microsoft.Quantum.Simulation.PauliBlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.PauliBlockEncoding)