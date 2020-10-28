---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Multiplygeneratorsystem-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: 1d28de99dab3f7aca4bf3706fe98f5ef7c5286a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706687"
---
# <a name="multiplygeneratorsystem-function"></a><span data-ttu-id="1ce87-102">Multiplygeneratorsystem-Funktion</span><span class="sxs-lookup"><span data-stu-id="1ce87-102">MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="1ce87-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1ce87-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1ce87-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1ce87-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1ce87-105">Multipliziert den Koeffizient aller Begriffe in einem `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="1ce87-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="1ce87-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1ce87-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="1ce87-107">Multiplikator: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1ce87-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1ce87-108">Der Multiplikator des Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="1ce87-108">The multiplier on the coefficient.</span></span>


### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="1ce87-109">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="1ce87-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="1ce87-110">Die zu multiplizierende `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="1ce87-110">The `GeneratorSystem` to be multiplied.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="1ce87-111">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="1ce87-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="1ce87-112">Ein, das `GeneratorSystem` ein System mit Koeffizienten darstellt, das `multiplier` größer ist.</span><span class="sxs-lookup"><span data-stu-id="1ce87-112">A `GeneratorSystem` representing a system with coefficients a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ce87-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1ce87-113">See Also</span></span>

- [<span data-ttu-id="1ce87-114">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="1ce87-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)