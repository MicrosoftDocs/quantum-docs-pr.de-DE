---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: _IdentityTimeDependentGeneratorSystem-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 7b93a6674bec974e61496696a3d8403225b16d80
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225600"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="e2715-102">_IdentityTimeDependentGeneratorSystem-Funktion</span><span class="sxs-lookup"><span data-stu-id="e2715-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="e2715-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e2715-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e2715-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e2715-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e2715-105">Gibt ein mit der hamiltonan konsistentes Generator System zurück `H(s) = 0` , wobei `s` ein Zeit Plan Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="e2715-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="e2715-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e2715-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="e2715-107">Zeitplan: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e2715-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e2715-108">Diese Eingabe wird ignoriert und wird aus Gründen der Konsistenz mit dem <xref:microsoft.quantum.canon.timedependentgeneratorsystem> benutzerdefinierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="e2715-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="e2715-109">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="e2715-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="e2715-110">Ein Generator System, das die Evolution unter den hamiltonan $H (s) = $0 für alle $s $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2715-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>