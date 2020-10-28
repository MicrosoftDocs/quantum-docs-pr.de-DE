---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Identitygeneratorindex-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: d2af2dafaf75a68546cb3f16c04cf4c7ee50c6ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724543"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="4a706-102">Identitygeneratorindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a706-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="4a706-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4a706-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4a706-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4a706-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4a706-105">Gibt einen Generator Index zurück, der mit der NULL hamiltonan übereinstimmt, `H = 0` die dem Vorgang zur Identitätsentwicklung entspricht.</span><span class="sxs-lookup"><span data-stu-id="4a706-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="4a706-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="4a706-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="4a706-107">idxterm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a706-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a706-108">Diese Eingabe wird ignoriert und wird aus Gründen der Konsistenz mit dem <xref:microsoft.quantum.simulation.generatorsystem> benutzerdefinierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="4a706-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="4a706-109">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="4a706-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="4a706-110">Ein Generator Index, der die Evolution unter der hamiltonan $H = $0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="4a706-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>