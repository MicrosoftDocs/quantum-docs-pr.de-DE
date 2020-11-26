---
uid: Microsoft.Quantum.Simulation.IdentityGeneratorIndex
title: Identitygeneratorindex-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IdentityGeneratorIndex
qsharp.summary: Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.
ms.openlocfilehash: 2dd3c705b0496df1719dc677e4defea5e435b839
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229289"
---
# <a name="identitygeneratorindex-function"></a><span data-ttu-id="30e8f-102">Identitygeneratorindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="30e8f-102">IdentityGeneratorIndex function</span></span>

<span data-ttu-id="30e8f-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="30e8f-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="30e8f-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30e8f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30e8f-105">Gibt einen Generator Index zurück, der mit der NULL hamiltonan übereinstimmt, `H = 0` die dem Vorgang zur Identitätsentwicklung entspricht.</span><span class="sxs-lookup"><span data-stu-id="30e8f-105">Returns a generator index consistent with the zero Hamiltonian, `H = 0`, which corresponds to the identity evolution operation.</span></span>

```qsharp
function IdentityGeneratorIndex (idxTerm : Int) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="30e8f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="30e8f-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="30e8f-107">idxterm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="30e8f-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="30e8f-108">Diese Eingabe wird ignoriert und wird aus Gründen der Konsistenz mit dem <xref:microsoft.quantum.simulation.generatorsystem> benutzerdefinierten Typ definiert.</span><span class="sxs-lookup"><span data-stu-id="30e8f-108">This input is ignored, and is defined for consistency with the <xref:microsoft.quantum.simulation.generatorsystem> user-defined type.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="30e8f-109">Ausgabe: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="30e8f-109">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="30e8f-110">Ein Generator Index, der die Evolution unter der hamiltonan $H = $0 darstellt.</span><span class="sxs-lookup"><span data-stu-id="30e8f-110">A generator index representing evolution under the Hamiltonian $H = 0$.</span></span>