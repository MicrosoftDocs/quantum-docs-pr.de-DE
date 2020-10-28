---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Applyfixedpoinmanipulieren-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92721911"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="3c15c-102">Applyfixedpoinmanipulieren-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3c15c-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="3c15c-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="3c15c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="3c15c-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3c15c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3c15c-105">Fixed-Point Amplitude-Verstärkungs Algorithmus</span><span class="sxs-lookup"><span data-stu-id="3c15c-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="3c15c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="3c15c-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="3c15c-107">statepreporacle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="3c15c-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="3c15c-108">Einheitliches Oracle, das den Startstatus vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="3c15c-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="3c15c-109">startqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3c15c-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3c15c-110">Qubit-Register</span><span class="sxs-lookup"><span data-stu-id="3c15c-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="3c15c-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3c15c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3c15c-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c15c-112">Remarks</span></span>

<span data-ttu-id="3c15c-113">Startqubits muss sich im Status $ \ket{0\cdots 0} $ befinden.</span><span class="sxs-lookup"><span data-stu-id="3c15c-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="3c15c-114">Dieser Vorgang durchläuft eine Reihe von Abfragen in den Befugnissen von $2 $, bis entweder eine maximale Anzahl von Abfragen erreicht oder der Ziel Status gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="3c15c-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>