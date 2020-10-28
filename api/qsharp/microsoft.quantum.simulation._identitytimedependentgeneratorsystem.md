---
uid: Microsoft.Quantum.Simulation._IdentityTimeDependentGeneratorSystem
title: _IdentityTimeDependentGeneratorSystem-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _IdentityTimeDependentGeneratorSystem
qsharp.summary: Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.
ms.openlocfilehash: 0b440ce9adaab562e16b02da46844c68a7470b11
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701777"
---
# <a name="_identitytimedependentgeneratorsystem-function"></a><span data-ttu-id="b5f27-102">_IdentityTimeDependentGeneratorSystem-Funktion</span><span class="sxs-lookup"><span data-stu-id="b5f27-102">_IdentityTimeDependentGeneratorSystem function</span></span>

<span data-ttu-id="b5f27-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b5f27-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b5f27-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b5f27-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b5f27-105">Gibt ein mit der hamiltonan konsistentes Generator System zurück `H(s) = 0` , wobei `s` ein Zeit Plan Parameter ist.</span><span class="sxs-lookup"><span data-stu-id="b5f27-105">Returns a generator system consistent with the Hamiltonian `H(s) = 0`, where `s` is a schedule parameter.</span></span>

```qsharp
function _IdentityTimeDependentGeneratorSystem (schedule : Double) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="b5f27-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b5f27-106">Input</span></span>

### <a name="schedule--double"></a><span data-ttu-id="b5f27-107">Zeitplan: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b5f27-107">schedule : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b5f27-108">Diese Eingabe wird ignoriert und wird aus Gründen der Konsistenz mit dem <xref:microsoft.quantum.canon.timedependentgeneratorsystem> benutzerdefinierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="b5f27-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.canon.timedependentgeneratorsystem> user-defined type.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="b5f27-109">Ausgabe: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="b5f27-109">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="b5f27-110">Ein Generator System, das die Evolution unter den hamiltonan $H (s) = $0 für alle $s $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5f27-110">A generator system representing evolution under the Hamiltonian $H(s) = 0$ for all $s$.</span></span>