---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorImpl
title: _JordanWignerClusterOperatorImpl Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: d8301934beedf715c533e00f32a50e76c11875f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851638"
---
# <a name="_jordanwignerclusteroperatorimpl-operation"></a><span data-ttu-id="8fa08-102">_JordanWignerClusterOperatorImpl Vorgang</span><span class="sxs-lookup"><span data-stu-id="8fa08-102">_JordanWignerClusterOperatorImpl operation</span></span>

<span data-ttu-id="8fa08-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="8fa08-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="8fa08-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="8fa08-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="8fa08-105">Stellt einen dynamischen Generator als Satz von simulier baren Gates und eine Erweiterung in der jordanwigner-Basis dar.</span><span class="sxs-lookup"><span data-stu-id="8fa08-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

<span data-ttu-id="8fa08-106">Weitere Informationen finden Sie unter [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) .</span><span class="sxs-lookup"><span data-stu-id="8fa08-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation _JordanWignerClusterOperatorImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="8fa08-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="8fa08-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="8fa08-108">generatorindex: [generatorindex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8fa08-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8fa08-109">Ein Generator Index, der als einheitliche Evolution in der jordanwigner dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8fa08-109">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="8fa08-110">stepSize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8fa08-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8fa08-111">Die Pseudo Variable, die der Signatur von Simulations Algorithmen entsprechen soll.</span><span class="sxs-lookup"><span data-stu-id="8fa08-111">Dummy variable to match signature of simulation algorithms.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="8fa08-112">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="8fa08-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="8fa08-113">Registrieren Sie sich für den Time-Evolution-Operator.</span><span class="sxs-lookup"><span data-stu-id="8fa08-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8fa08-114">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fa08-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

