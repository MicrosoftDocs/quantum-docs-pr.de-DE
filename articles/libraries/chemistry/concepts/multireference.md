---
title: Korrelierte wavefunctions | Microsoft-Dokumentation
description: Konzeptionelle Dynamics Dynamics-Dokumentation
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.multireference
ms.openlocfilehash: 0b14f373d31c5b63e313e07810daf62d9195b1d3
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184031"
---
# <a name="correlated-wavefunctions"></a><span data-ttu-id="e0e78-103">Korrelierte wavefunctions</span><span class="sxs-lookup"><span data-stu-id="e0e78-103">Correlated wavefunctions</span></span>

<span data-ttu-id="e0e78-104">Für viele Systeme, insbesondere solche, die sich in der Nähe der Gleichgewichts Geometrie befinden, stellt die " [Hartree – Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) "-Theorie eine qualitative Beschreibung von molekularen Eigenschaften durch einen einzigen Determinanten Verweis Status bereit.</span><span class="sxs-lookup"><span data-stu-id="e0e78-104">For many systems, particularly those near the equilibrium geometry, [Hartree–Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) theory provides a qualitative description of molecular properties through a single-determinant reference state.</span></span> <span data-ttu-id="e0e78-105">Um jedoch eine quantitative Genauigkeit zu erzielen, müssen Sie auch Korrelations Effekte in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="e0e78-105">However, in order to achieve quantitative accuracy, one must also consider correlation effects.</span></span> 

<span data-ttu-id="e0e78-106">In diesem Kontext ist es wichtig, sich zwischen dynamischen und nicht dynamischen Korrelationen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="e0e78-106">In this context, it is important to dinstinguish between dynamic and non-dynamic correlations.</span></span>
<span data-ttu-id="e0e78-107">Dynamical-Korrelationen ergeben sich aus der Tendenz, dass sich die Elektronen voneinander unterscheiden, z. b. aufgrund der interelektronischen Abwehr.</span><span class="sxs-lookup"><span data-stu-id="e0e78-107">Dynamical correlations arise from the tendency of electrons to stay apart, such as due to interelectronic repulsion.</span></span> <span data-ttu-id="e0e78-108">Dieser Effekt kann modelliert werden, indem die Erregung von Elektronen aus dem Verweis Zustand berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="e0e78-108">This effect can be modelled by considering excitations of electrons out of the reference state.</span></span> <span data-ttu-id="e0e78-109">Nicht dynamische Korrelationen treten auf, wenn die Wellenfunktion von mindestens zwei Konfigurationen in nulloverreihenfolge dominiert wird, auch wenn nur eine qualitative Beschreibung des Systems erreicht werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0e78-109">Non-dynamic correlations arise when the wavefunction is dominated by two or more configurations at zeroth order, even to achieve only a qualitative description of the system.</span></span>
<span data-ttu-id="e0e78-110">Dies erfordert eine untergeordnete Position von Determinanten und ist ein Beispiel für eine multireference-wavefunction.</span><span class="sxs-lookup"><span data-stu-id="e0e78-110">This necessitates a superposition of determinants and is an example of a multireference wavefunction.</span></span>

<span data-ttu-id="e0e78-111">Die Bibliothek "Chemistry" bietet eine Möglichkeit, eine nullte-Reihenfolge-wavefunction für das multireference-Problem als Superposition von Determinanten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0e78-111">The chemistry library provides a way to specify a zeroth order wavefunction for the multireference problem as a superposition of determinants.</span></span> <span data-ttu-id="e0e78-112">Dieser Ansatz, der als "Sparse multireference wavefunctions" bezeichnet wird, ist wirksam, wenn nur wenige Komponenten ausreichen, um die Superposition anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0e78-112">This approach, which we call sparse multireference wavefunctions, is effective when only a few components suffice to specify the superposition.</span></span> <span data-ttu-id="e0e78-113">Die Bibliothek bietet auch eine Methode zum einbeziehen dynamischer Korrelationen über einen einzigen Determinanten Verweis über den generalisierten einheitlichen gekoppelt-Cluster-Ansatz.</span><span class="sxs-lookup"><span data-stu-id="e0e78-113">The library also provides a method to include dynamic correlations on top of a single-determinant reference via the generalized unitary coupled-cluster ansatz.</span></span> <span data-ttu-id="e0e78-114">Außerdem erstellt Sie auch Quantum-Leitungen, die diese Zustände auf einem Quantum-Computer generieren.</span><span class="sxs-lookup"><span data-stu-id="e0e78-114">Furthermore, it also constructs quantum circuits that generate these states on a quantum computer.</span></span> <span data-ttu-id="e0e78-115">Diese Zustände können im [broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)angegeben werden, und es wird auch die Funktionalität bereitgestellt, um diese Zustände manuell über die Chemie Bibliothek anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0e78-115">These states may be specified in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), and we also provide the functionality to manually specify these states through the chemistry library.</span></span>

## <a name="sparse-multi-reference-wavefunction"></a><span data-ttu-id="e0e78-116">Multireference-Wellenfunktion mit geringer Dichte</span><span class="sxs-lookup"><span data-stu-id="e0e78-116">Sparse multi-reference wavefunction</span></span>
<span data-ttu-id="e0e78-117">Ein Multi-Reference-Status $ \ket{\psi_{\rM {mcscf}}} kann explizit als lineare Kombination aus $N "$-Electron"-Slater determininants angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0e78-117">A multi-reference state $\ket{\psi_{\rm {MCSCF}}}$ may be specified explicitly as a linear combination of $N$-electron Slater determininants.</span></span>
<span data-ttu-id="e0e78-118">\begin{align} \ket{\psi_{\rM {mcscf}}} \propto \sum_{i_1 < i_2 < \cdots < i_N} \lambda_{i_1, i_2, \cdots, i_N} a ^ \dagger_{i_1}a ^ \dagger_{i_2}\cdots a ^ \dagger_{i_N}\ket{0}.</span><span class="sxs-lookup"><span data-stu-id="e0e78-118">\begin{align} \ket{\psi_{\rm {MCSCF}}} \propto \sum_{i_1 < i_2 < \cdots < i_N} \lambda_{i_1,i_2,\cdots,i_N} a^\dagger_{i_1}a^\dagger_{i_2}\cdots a^\dagger_{i_N}\ket{0}.</span></span>
<span data-ttu-id="e0e78-119">\end{align} beispielsweise kann der Status $ \propto (0,1 a ^ \dagger_1a ^ \dagger_2a ^ \dagger_6-0,2 a ^ \dagger_2a ^ \dagger_1a ^ \dagger_5) \ket{0}$ wie folgt in der Chemie Bibliothek angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0e78-119">\end{align} For example, the state $\propto(0.1 a^\dagger_1a^\dagger_2a^\dagger_6 - 0.2 a^\dagger_2a^\dagger_1a^\dagger_5)\ket{0}$ may be specified in the chemistry library as follows.</span></span>
```csharp
// Create a list of tuples where the first item of each 
// tuple are indices to the creation operators acting on the
// vacuum state, and the second item is the coefficient
// of that basis state.
var superposition = new[] {
    (new[] {1, 2, 6}, 0.1),
    (new[] {2, 1, 5}, -0.2) };

// Create a fermion wavefunction object that represents the superposition.
var wavefunction = new FermionWavefunction<int>(superposition);
```
<span data-ttu-id="e0e78-120">Diese explizite Darstellung der superposition-Komponenten ist wirksam, wenn nur wenige Komponenten angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e0e78-120">This explicit representation of the superposition components is effective when only a few components need to be specified.</span></span> <span data-ttu-id="e0e78-121">Sie sollten diese Darstellung vermeiden, wenn viele Komponenten erforderlich sind, um den gewünschten Zustand exakt zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="e0e78-121">One should avoid using this representation when many components are required to accurately capture the desired state.</span></span> <span data-ttu-id="e0e78-122">Der Grund hierfür sind die Gate-Kosten der Quantum-Leitung, die diesen Status auf einem Quantum-Computer vorbereiten, der mindestens linear mit der Anzahl der superposition-Komponenten skaliert, und höchstens quadratisch mit der einnorm der superposition-Verstärkung.</span><span class="sxs-lookup"><span data-stu-id="e0e78-122">The reason for this is the gate cost of quantum circuit that prepares this state on a quantum computer, which scales at least linearly with the number of superposition components, and at most quadratically with the one-norm of the superposition amplitudes.</span></span>

## <a name="unitary-coupled-cluster-wavefunction"></a><span data-ttu-id="e0e78-123">Einheitliche gekoppelte Cluster Wellenfunktion</span><span class="sxs-lookup"><span data-stu-id="e0e78-123">Unitary coupled-cluster wavefunction</span></span>
<span data-ttu-id="e0e78-124">Es ist auch möglich, eine einheitliche gekoppelte Cluster-wavefunction $ \ket{\psi_{\rM {UCC}}} $ mithilfe der chemisteriebibliothek anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0e78-124">It is also possible to specify a unitary coupled-cluster wavefunction $\ket{\psi_{\rm {UCC}}}$ using the chemistery library.</span></span> <span data-ttu-id="e0e78-125">In dieser Situation haben wir einen einzelnen Determinanten Verweis Status, z. \ket{\psi_{\rM{SCF}}}. $ $.</span><span class="sxs-lookup"><span data-stu-id="e0e78-125">In this situation, we have a single-determinant reference state, say, $\ket{\psi_{\rm{SCF}}}$.</span></span> <span data-ttu-id="e0e78-126">Die Komponenten der einheitlichen, gekoppelten Cluster-wavefunction werden dann mithilfe eines einheitlichen Operators, der auf einen Referenz Zustand agiert, als implizität angegeben.</span><span class="sxs-lookup"><span data-stu-id="e0e78-126">The components of the unitary coupled-cluster wavefunction are then specified implicity through a unitary operator acting on a reference state.</span></span>
<span data-ttu-id="e0e78-127">Dieser einheitliche Operator wird häufig als $e ^ {T-T ^ \dagger} $ geschrieben, wobei $T-T ^ \dagger $ der Anti-hermitian-Cluster Operator ist.</span><span class="sxs-lookup"><span data-stu-id="e0e78-127">This unitary operator is commonly written as $e^{T-T^\dagger}$, where $T-T^\dagger$ is the anti-Hermitian cluster operator.</span></span> <span data-ttu-id="e0e78-128">Folglich \begin{align} \ket{\psi_{\rM {UCC}}} = e ^ {t-T ^ \dagger}\ket{\psi_{\rM{SCF}}}.</span><span class="sxs-lookup"><span data-stu-id="e0e78-128">Thus \begin{align} \ket{\psi_{\rm {UCC}}} = e^{T-T^\dagger}\ket{\psi_{\rm{SCF}}}.</span></span>
<span data-ttu-id="e0e78-129">\end{align}</span><span class="sxs-lookup"><span data-stu-id="e0e78-129">\end{align}</span></span>

<span data-ttu-id="e0e78-130">Es ist auch üblich, den Cluster Operator $T = T_1 + T_2 + \cdots $ in Teile aufzuteilen, wobei jeder Teil $T _J $ $j "$-Body"-Begriffen enthält.</span><span class="sxs-lookup"><span data-stu-id="e0e78-130">It is also common to split the cluster operator $T = T_1 + T_2 + \cdots$ into parts, where each part $T_j$ contains $j$-body terms.</span></span> <span data-ttu-id="e0e78-131">In der Theorie für generalisierte gekoppelte Cluster hat der Einzel Text Cluster-Operator (Singles) das Format \begin{align} T_1 = \sum_{PQ}t ^ {p} _ {q} a ^ \dagger_p a_q, \end{align}</span><span class="sxs-lookup"><span data-stu-id="e0e78-131">In generalized coupled-cluster theory, the one-body cluster operator (singles) is of the form \begin{align} T_1 = \sum_{pq}t^{p}_{q} a^\dagger_p a_q, \end{align}</span></span>

<span data-ttu-id="e0e78-132">und zwei Text Cluster Operator (Double) haben das Format \begin{align} T_2 = \sum_{pqrs}t ^ {PQ} _ {RS} a ^ \dagger_p a ^ \dagger_q a_r a_s.</span><span class="sxs-lookup"><span data-stu-id="e0e78-132">and two-body cluster operator (doubles) is of the form \begin{align} T_2 = \sum_{pqrs}t^{pq}_{rs} a^\dagger_p a^\dagger_q a_r a_s.</span></span>
<span data-ttu-id="e0e78-133">\end{align}</span><span class="sxs-lookup"><span data-stu-id="e0e78-133">\end{align}</span></span>

<span data-ttu-id="e0e78-134">Bedingungen höherer Ordnung (dreipel, Vierbeiner usw.) sind möglich, werden aber derzeit von der Chemie Bibliothek nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0e78-134">Higher-order terms (triples, quadruples, etc.) are possible, but not currently supported by the chemistry library.</span></span>

<span data-ttu-id="e0e78-135">Beispiel: $ \ket{\psi_{\rM{SCF}}} = a ^ \dagger_1 a ^ \dagger_2\ket{0}$ und Let $T = 0,123 a ^ \dagger_0 A_1 + 0,456 a ^ \dagger_0a ^ \dagger_3 A_1 a_2-0,789 a ^ \dagger_3a ^ \dagger_2 A_1 a_0 $.</span><span class="sxs-lookup"><span data-stu-id="e0e78-135">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_1 a^\dagger_2\ket{0}$, and let $T= 0.123 a^\dagger_0 a_1 + 0.456 a^\dagger_0a^\dagger_3 a_1 a_2 - 0.789 a^\dagger_3a^\dagger_2 a_1 a_0$.</span></span> <span data-ttu-id="e0e78-136">Dieser Status wird in der Chemie Bibliothek wie folgt instanziiert.</span><span class="sxs-lookup"><span data-stu-id="e0e78-136">Then this state is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { 1, 2 };

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {0, 1}, 0.123),
    (new [] {0, 3, 1, 2}, 0.456),
    (new [] {3, 2, 1, 0}, 0.789)
};

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunction = new FermionWavefunction<int>(reference, clusterOperator);
```

<span data-ttu-id="e0e78-137">Die drehkonverzierung kann explizit durch Angabe `SpinOrbital` Indizes anstelle von ganzzahligen Indizes vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="e0e78-137">Spin convervation may be made explicit by instead specifying `SpinOrbital` indices instead of integer indices.</span></span> <span data-ttu-id="e0e78-138">Beispiel: $ \ket{\psi_{\rM{SCF}}} = a ^ \dagger_{1, \uparamerow} a ^ \dagger_{2, \downarrow}\ket{0}$ und Let $T = 0,123 a ^ \dagger_{0, \uparamerow} a_ {1, \uparamerow} + 0,456 a ^ \dagger_{0, \uparamerow} a ^ \dagger_{3, \downarrow} a_ {1, \uparamerow} a_ {2, \ Pfeil nach unten}-0,789 a ^ \dagger_{3, \ubirow} a ^ \dagger_{2, \uparamerow} a_ {1, \uparamerow} a_ {0, \uparamerow} $ be.</span><span class="sxs-lookup"><span data-stu-id="e0e78-138">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_{1,\uparrow} a^\dagger_{2, \downarrow}\ket{0}$, and let $T= 0.123 a^\dagger_{0, \uparrow} a_{1, \uparrow} + 0.456 a^\dagger_{0, \uparrow} a^\dagger_{3, \downarrow} a_{1, \uparrow} a_{2, \downarrow} - 0.789 a^\dagger_{3,\uparrow} a^\dagger_{2,\uparrow} a_{1,\uparrow} a_{0, \uparrow}$ be spin convserving.</span></span> <span data-ttu-id="e0e78-139">Dieser Status wird in der Chemie Bibliothek wie folgt instanziiert.</span><span class="sxs-lookup"><span data-stu-id="e0e78-139">Then this state is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {(0, Spin.u), (1, Spin.u)}, 0.123),
    (new [] {(0, Spin.u), (3, Spin.d), (1, Spin.u), (2, Spin.d)}, 0.456),
    (new [] {(3, Spin.u), (2, Spin.u), (1, Spin.u), (0, Spin.u)}, 0.789)
}.Select(o => (o.Item1.ToSpinOrbitals(), o.Item2);

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(reference, clusterOperator);

// Convert the wavefunction indexed by spin-orbitals to one indexed
// by integers
var wavefunctionInteger = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="e0e78-140">Wir stellen auch eine Hilfsfunktion bereit, die alle Spin-konversing-Cluster Operatoren auflistet, die nur besetzte Spin-Orbitals und begeistern nur auf nicht belegte Spin-Orbitals-Elemente zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="e0e78-140">We also provide a convenience function that enumerates over all spin-conversing cluster operators that annihilate only occupied spin-orbitals and excite to only unoccupied spin-orbitals.</span></span>
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Generate all spin-conversing excitations from spin-orbitals 
// occupied by the reference state to virtual orbitals.
var generatedExcitations = reference.CreateAllUCCSDSingletExcitations(nOrbitals: 3).Excitations;

// This is the list of expected spin-consvering excitations
var expectedExcitations = new[]
{
    new []{ (0, Spin.u), (1,Spin.u)},
    new []{ (2, Spin.u), (1,Spin.u)},
    new []{ (0, Spin.d), (2,Spin.d)},
    new []{ (1, Spin.d), (2,Spin.d)},
    new []{ (0, Spin.u), (0, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.u), (1, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)},
    new []{ (1, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)}
}.Select(o => new IndexOrderedSequence<SpinOrbital>(o.ToLadderSequence()));

// The following two assertions are true, and verify that the generated 
// excitations exactly match the expected excitations.
var bool0 = generatedExcitations.Keys.All(expectedExcitations.Contains);
var bool1 = generatedExcitations.Count() == expectedExcitations.Count();
```