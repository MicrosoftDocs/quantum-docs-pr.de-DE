---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: Multiplygeneratorsystem-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: cebd08c86ad8a3793ba7d0e9ce241d7a1ef046ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858496"
---
# <a name="multiplygeneratorsystem-function"></a><span data-ttu-id="3859e-102">Multiplygeneratorsystem-Funktion</span><span class="sxs-lookup"><span data-stu-id="3859e-102">MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="3859e-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="3859e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="3859e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3859e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3859e-105">Multipliziert den Koeffizient aller Begriffe in einem `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="3859e-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="3859e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3859e-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="3859e-107">Multiplikator: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3859e-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3859e-108">Der Multiplikator des Koeffizienten.</span><span class="sxs-lookup"><span data-stu-id="3859e-108">The multiplier on the coefficient.</span></span>


### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="3859e-109">Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="3859e-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="3859e-110">Die zu multiplizierende `GeneratorSystem`.</span><span class="sxs-lookup"><span data-stu-id="3859e-110">The `GeneratorSystem` to be multiplied.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="3859e-111">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="3859e-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="3859e-112">Ein, das `GeneratorSystem` ein System mit Koeffizienten darstellt, das `multiplier` größer ist.</span><span class="sxs-lookup"><span data-stu-id="3859e-112">A `GeneratorSystem` representing a system with coefficients a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="3859e-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3859e-113">See Also</span></span>

- [<span data-ttu-id="3859e-114">Microsoft. Quantum. Simulation. Generatorsystem</span><span class="sxs-lookup"><span data-stu-id="3859e-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)