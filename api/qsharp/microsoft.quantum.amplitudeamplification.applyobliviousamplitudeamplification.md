---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Applyobliviousamplitudeverstärkungsvorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: 9b0060201bcdae02a207362a753a0a403cdbb896
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191515"
---
# <a name="applyobliviousamplitudeamplification-operation"></a><span data-ttu-id="51bca-102">Applyobliviousamplitudeverstärkungsvorgang</span><span class="sxs-lookup"><span data-stu-id="51bca-102">ApplyObliviousAmplitudeAmplification operation</span></span>

<span data-ttu-id="51bca-103">Namespace: [Microsoft. Quantum. Verstärkungs Verstärkung](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="51bca-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="51bca-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51bca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51bca-105">Durch die Angabe partieller Reflektionen wird die Verstärkung der Amplitude-Verstärkung unterstreicht</span><span class="sxs-lookup"><span data-stu-id="51bca-105">Oblivious amplitude amplification by specifying partial reflections.</span></span>

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="51bca-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="51bca-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="51bca-107">Phasen: [reflectionphasen](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="51bca-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="51bca-108">Phasen von partiellen Reflektionen</span><span class="sxs-lookup"><span data-stu-id="51bca-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="51bca-109">Startstatus-eflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="51bca-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="51bca-110">Reflektionsoperator zum Startstatus des Zusatz Registers</span><span class="sxs-lookup"><span data-stu-id="51bca-110">Reflection operator about start state of auxiliary register</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="51bca-111">targetstatuereflection: [reflectionoracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="51bca-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="51bca-112">Reflektionsoperator zum Ziel Status des Zusatz Registers</span><span class="sxs-lookup"><span data-stu-id="51bca-112">Reflection operator about target state of auxiliary register</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="51bca-113">signaloracle: [obliviousoracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="51bca-113">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="51bca-114">Einheitlicher Oracle-$O $ vom Typ `ObliviousOracle` , der gemeinsam auf dem Hilfssystem und dem System Register agiert.</span><span class="sxs-lookup"><span data-stu-id="51bca-114">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system registers.</span></span>


### <a name="auxiliaryregister--qubit"></a><span data-ttu-id="51bca-115">auxiliaryregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="51bca-115">auxiliaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="51bca-116">Zusatz Register</span><span class="sxs-lookup"><span data-stu-id="51bca-116">Auxiliary register</span></span>


### <a name="systemregister--qubit"></a><span data-ttu-id="51bca-117">Systemregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="51bca-117">systemRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="51bca-118">System Register</span><span class="sxs-lookup"><span data-stu-id="51bca-118">System register</span></span>



## <a name="output--unit"></a><span data-ttu-id="51bca-119">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51bca-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="51bca-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51bca-120">Remarks</span></span>

<span data-ttu-id="51bca-121">Bei einem bestimmten Zusatz Status $ \ket{\text{Start}} \_ a $, einem bestimmten Zusatz Ziel Status $ \ket{\text{Target}} \_ a $ und jedem Systemstatus $ \ket{\psi} \_ s $, angenommen, \begin{align} o\ket {\ Text {Start}} \_ a\ket {\ PSI} \_ s = \lambda\ket{\text{Target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\text{Target} ^ \perp} \_ a\cdots \end{align} für einige einheitliche $U $.</span><span class="sxs-lookup"><span data-stu-id="51bca-121">Given a particular auxiliary start state $\ket{\text{start}}\_a$, a particular auxiliary target state $\ket{\text{target}}\_a$, and any system state $\ket{\psi}\_s$, suppose that \begin{align} O\ket{\text{start}}\_a\ket{\psi}\_s= \lambda\ket{\text{target}}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{\text{target}^\perp}\_a\cdots \end{align} for some unitary $U$.</span></span>
<span data-ttu-id="51bca-122">Durch eine Sequenz von Reflektionen zu den Start-und Ziel Zuständen im Zusatz Register, die von Anwendungen von `signalOracle` und dessen Adjoint überschneidet werden, kann die Erfolgswahrscheinlichkeit der Anwendung U geändert werden.</span><span class="sxs-lookup"><span data-stu-id="51bca-122">By a sequence of reflections about the start and target states on the auxiliary register interleaved by applications of `signalOracle` and its adjoint, the success probability of applying U may be altered.</span></span>

<span data-ttu-id="51bca-123">In den meisten Fällen `auxiliaryRegister` wird im Status $ \ket{\text{Start}} \_ a $ initialisiert.</span><span class="sxs-lookup"><span data-stu-id="51bca-123">In most cases, `auxiliaryRegister` is initialized in the state $\ket{\text{start}}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="51bca-124">Referenzen</span><span class="sxs-lookup"><span data-stu-id="51bca-124">References</span></span>

<span data-ttu-id="51bca-125">Siehe</span><span class="sxs-lookup"><span data-stu-id="51bca-125">See</span></span>

- <span data-ttu-id="51bca-126">[ *D.W. Berry, Uhr Childs, r. Cleve, r. Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) für die Standardversion.</span><span class="sxs-lookup"><span data-stu-id="51bca-126">[ *D.W. Berry, A.M. Childs, R. Cleve, R. Kothari, R.D. Somma* ](https://arxiv.org/abs/1312.1414) for the standard version.</span></span>
  <span data-ttu-id="51bca-127">Siehe</span><span class="sxs-lookup"><span data-stu-id="51bca-127">See</span></span>
- <span data-ttu-id="51bca-128">[ *G.H. Low, I.L. Chuang*](https://arxiv.org/abs/1610.06546) for a Generalisierung to partielle Reflektionen.</span><span class="sxs-lookup"><span data-stu-id="51bca-128">[ *G.H. Low, I.L. Chuang* ](https://arxiv.org/abs/1610.06546) for a generalization to partial reflections.</span></span>