---
uid: Microsoft.Quantum.Chemistry.JordanWigner.VQE._prepareTrialStateWrapper
title: _prepareTrialStateWrapper Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner.VQE
qsharp.name: _prepareTrialStateWrapper
qsharp.summary: Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint. EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.
ms.openlocfilehash: 8e1a39cbd307a467ab7f0466c90722e1c8c46d4a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224682"
---
# <a name="_preparetrialstatewrapper-operation"></a><span data-ttu-id="db83d-102">_prepareTrialStateWrapper Vorgang</span><span class="sxs-lookup"><span data-stu-id="db83d-102">_prepareTrialStateWrapper operation</span></span>

<span data-ttu-id="db83d-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner. vqe](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span><span class="sxs-lookup"><span data-stu-id="db83d-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner.VQE](xref:Microsoft.Quantum.Chemistry.JordanWigner.VQE)</span></span>

<span data-ttu-id="db83d-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="db83d-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="db83d-105">Privater Wrapper um preparezstate, um ihn mit estimatefrequescya kompatibel zu machen, indem ein Adjoint-Wert definiert wird.</span><span class="sxs-lookup"><span data-stu-id="db83d-105">Private wrapper around PrepareTrialState to make it compatible with EstimateFrequencyA by defining an adjoint.</span></span>
<span data-ttu-id="db83d-106">Estimatefrequencya verfügt über eine integrierte Emulations Funktion, wenn der quantumsimulator als Ziel verwendet wird, wodurch die Ausführung beschleunigt wird.</span><span class="sxs-lookup"><span data-stu-id="db83d-106">EstimateFrequencyA has built-in emulation feature when targeting the QuantumSimulator, which speeds up its execution.</span></span>

```qsharp
operation _prepareTrialStateWrapper (inputState : (Int, Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[]), qubits : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="db83d-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="db83d-107">Input</span></span>

### <a name="inputstate--intjordanwignerinputstate"></a><span data-ttu-id="db83d-108">inputstate: ([int](xref:microsoft.quantum.lang-ref.int),[jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span><span class="sxs-lookup"><span data-stu-id="db83d-108">inputState : ([Int](xref:microsoft.quantum.lang-ref.int),[JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[])</span></span>

<span data-ttu-id="db83d-109">Die Jordan-Wigner Eingabe, die für die Durchführung von preparezalstate erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="db83d-109">The Jordan-Wigner input required for PrepareTrialState to run.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="db83d-110">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="db83d-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="db83d-111">Ein Qubit-Register.</span><span class="sxs-lookup"><span data-stu-id="db83d-111">A qubit register.</span></span>



## <a name="output--unit"></a><span data-ttu-id="db83d-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="db83d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

