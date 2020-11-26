---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Applyfixedpoinmanipulieren-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: 13e70b1ebd5e3bf0996e6a76f4bffe57ca2d2250
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191532"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="20059-102">Applyfixedpoinmanipulieren-Vorgang</span><span class="sxs-lookup"><span data-stu-id="20059-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="20059-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="20059-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="20059-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="20059-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="20059-105">Fixed-Point Amplitude-Verstärkungs Algorithmus</span><span class="sxs-lookup"><span data-stu-id="20059-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="20059-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="20059-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="20059-107">statepreporacle: [stateoracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="20059-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="20059-108">Einheitliches Oracle, das den Startstatus vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="20059-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="20059-109">startqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="20059-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="20059-110">Qubit-Register</span><span class="sxs-lookup"><span data-stu-id="20059-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="20059-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="20059-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="20059-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20059-112">Remarks</span></span>

<span data-ttu-id="20059-113">Startqubits muss sich im Status $ \ket{0\cdots 0} $ befinden.</span><span class="sxs-lookup"><span data-stu-id="20059-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="20059-114">Dieser Vorgang durchläuft eine Reihe von Abfragen in den Befugnissen von $2 $, bis entweder eine maximale Anzahl von Abfragen erreicht oder der Ziel Status gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="20059-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>