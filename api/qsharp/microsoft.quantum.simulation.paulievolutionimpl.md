---
uid: Microsoft.Quantum.Simulation.PauliEvolutionImpl
title: Paulievolutionimpl-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.

  See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 1c588c225cb7c91830e986c7eca9b9fafd445d4e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847949"
---
# <a name="paulievolutionimpl-operation"></a><span data-ttu-id="06b92-102">Paulievolutionimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="06b92-102">PauliEvolutionImpl operation</span></span>

<span data-ttu-id="06b92-103">Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="06b92-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="06b92-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="06b92-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="06b92-105">Stellt einen dynamischen Generator als Satz von simulsierbaren Gates und eine Erweiterung in der Pauli-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="06b92-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

<span data-ttu-id="06b92-106">Weitere Informationen finden Sie unter [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) .</span><span class="sxs-lookup"><span data-stu-id="06b92-106">See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation PauliEvolutionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, delta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="06b92-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="06b92-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="06b92-108">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="06b92-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="06b92-109">Ein Generator Index, der im Pauli als einheitliche Evolution dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="06b92-109">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>


### <a name="delta--double"></a><span data-ttu-id="06b92-110">Delta: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="06b92-110">delta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="06b92-111">Ein Multiplikator für die Dauer der Zeit-Evolution mit dem Begriff, auf den in verwiesen wird `generatorIndex` .</span><span class="sxs-lookup"><span data-stu-id="06b92-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="06b92-112">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="06b92-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="06b92-113">Registrieren Sie sich für den Time-Evolution-Operator.</span><span class="sxs-lookup"><span data-stu-id="06b92-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="06b92-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="06b92-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

