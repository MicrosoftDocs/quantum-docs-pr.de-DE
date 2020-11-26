---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: Obliviousamplitubinverstärkationfromstatepreparation-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 44bb394b0eb4ec98fd47fd1b156410b7a33903f1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191294"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="1f053-102">Obliviousamplitubinverstärkationfromstatepreparation-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f053-102">ObliviousAmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="1f053-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="1f053-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="1f053-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f053-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f053-105">Pervirone Amplitude-Verstärkung durch Oracles für partielle Reflektionen.</span><span class="sxs-lookup"><span data-stu-id="1f053-105">Oblivious amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="1f053-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f053-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="1f053-107">Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="1f053-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="1f053-108">Phasen von partiellen Reflektionen</span><span class="sxs-lookup"><span data-stu-id="1f053-108">Phases of partial reflections</span></span>


### <a name="startstateoracle--deterministicstateoracle"></a><span data-ttu-id="1f053-109">startstateoracle: [deterministicstateoracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="1f053-109">startStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="1f053-110">Einheitlicher Oracle-$A $, der den Status des zusätzlichen Starts vorbereitet</span><span class="sxs-lookup"><span data-stu-id="1f053-110">Unitary oracle $A$ that prepares auxiliary start state</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="1f053-111">signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="1f053-111">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="1f053-112">Einheitlicher Oracle-$O $ vom Typ `ObliviousOracle` , der gemeinsam mit dem Hilfssystem und dem System Register agiert</span><span class="sxs-lookup"><span data-stu-id="1f053-112">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system register</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="1f053-113">idxflagqubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1f053-113">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1f053-114">Index für Single-Qubit-Flag-Register</span><span class="sxs-lookup"><span data-stu-id="1f053-114">Index to single-qubit flag register</span></span>



## <a name="output--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="1f053-115">Ausgabe: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="1f053-115">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="1f053-116">Ein Vorgang, der die pervirone Amplitude-Verstärkung basierend auf partiellen Reflektionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="1f053-116">An operation that implements oblivious amplitude amplification based on partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f053-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f053-117">Remarks</span></span>

<span data-ttu-id="1f053-118">Dies erzwingt strengere Bedingungen in Form der zusätzlichen Start-und Ziel Zustände als in `AmpAmpObliviousByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="1f053-118">This imposes stricter conditions on form of the auxiliary start and target states than in `AmpAmpObliviousByReflectionPhases`.</span></span>
<span data-ttu-id="1f053-119">Es wird davon ausgegangen, dass $A \ket {0} \_ f \ket {0} \_ A = \ket{\text{Start}} \_ {FA} $ den zusätzlichen Startstatus $ \ket{\text{Start}} \_ {FA} $ von der Berechnungsbasis $ \ket {0} \_ f \ket {0} $ vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="1f053-119">It is assumed that $A\ket{0}\_f\ket{0}\_a= \ket{\text{start}}\_{fa}$ prepares the auxiliary start state $\ket{\text{start}}\_{fa}$ from the computational basis $\ket{0}\_f\ket{0}$.</span></span>
<span data-ttu-id="1f053-120">Es wird davon ausgegangen, dass der Ziel Status durch "$ \ket f $" gekennzeichnet ist {1} \_ .</span><span class="sxs-lookup"><span data-stu-id="1f053-120">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="1f053-121">Es wird davon ausgegangen, dass \begin{align} o\ket {\ Text {Start}} \_ {FA} \ket{\psi} \_ s = \lambda\ket {1} \_ f \ket {\ Text {Anything}} \_ a\ket {\ Text {Target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f \ cdots, \end{align} für einige einheitliche $U $.</span><span class="sxs-lookup"><span data-stu-id="1f053-121">It is assumed that \begin{align} O\ket{\text{start}}\_{fa}\ket{\psi}\_s= \lambda\ket{1}\_f\ket{\text{anything}}\_a\ket{\text{target}}\_s U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} for some unitary $U$.</span></span>