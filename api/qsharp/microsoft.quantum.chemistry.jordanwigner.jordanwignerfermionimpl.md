---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionImpl
title: Jordanwignerfermionimpl-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 5b975457803b8978d846bcd3c8256dfacdb90bee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98838182"
---
# <a name="jordanwignerfermionimpl-operation"></a><span data-ttu-id="3f137-102">Jordanwignerfermionimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3f137-102">JordanWignerFermionImpl operation</span></span>

<span data-ttu-id="3f137-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="3f137-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="3f137-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3f137-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="3f137-105">Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in der jordanwigner-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="3f137-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

<span data-ttu-id="3f137-106">Weitere Informationen finden Sie unter [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) .</span><span class="sxs-lookup"><span data-stu-id="3f137-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation JordanWignerFermionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3f137-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3f137-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="3f137-108">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3f137-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3f137-109">Ein Generator Index, der als einheitliche Evolution in der jordanwigner dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f137-109">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="3f137-110">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3f137-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3f137-111">Ein Multiplikator für die Dauer der Zeit-Evolution mit dem Begriff, auf den in verwiesen wird `generatorIndex` .</span><span class="sxs-lookup"><span data-stu-id="3f137-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3f137-112">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3f137-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3f137-113">Registrieren Sie sich für den Time-Evolution-Operator.</span><span class="sxs-lookup"><span data-stu-id="3f137-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3f137-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3f137-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

