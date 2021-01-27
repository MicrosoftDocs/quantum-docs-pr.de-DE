---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Identitygeneratorindex-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: b389ca1e0737463e6ccd5ce885b849c6b32d65d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844336"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="e88d8-102">Identitygeneratorindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="e88d8-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="e88d8-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e88d8-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e88d8-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e88d8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e88d8-105">Gibt einen Generator Index zurück, der mit der NULL hamiltonan übereinstimmt, `H = 0` die dem Vorgang zur Identitätsentwicklung entspricht.</span><span class="sxs-lookup"><span data-stu-id="e88d8-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="e88d8-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="e88d8-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="e88d8-107">idxterm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e88d8-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e88d8-108">Diese Eingabe wird ignoriert und wird aus Gründen der Konsistenz mit dem <xref:microsoft.quantum.simulation.generatorsystem> benutzerdefinierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="e88d8-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="e88d8-109">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e88d8-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e88d8-110">Ein Generator Index, der die Evolution unter der hamiltonan $H = $0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="e88d8-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>