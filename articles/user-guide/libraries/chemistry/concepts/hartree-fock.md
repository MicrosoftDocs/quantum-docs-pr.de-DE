---
title: Hartree-Fock-Theorie
description: Erfahren Sie mehr über die Hartree – Fock-Theorie, eine einfache Möglichkeit, den Anfangszustand für Quantum-Systeme zu erstellen.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
ms.openlocfilehash: 6fa63cbe13fe98565ffb42b56f3ade86720cedb3
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275110"
---
# <a name="hartreefock-theory"></a><span data-ttu-id="739e7-103">Hartree – Fock-Theorie</span><span class="sxs-lookup"><span data-stu-id="739e7-103">Hartree–Fock Theory</span></span>

<span data-ttu-id="739e7-104">Die vielleicht wichtigste Menge in der Quantum-Chemie-Simulation ist der Boden Status, der der minimale Energie eigen Vektor der hamiltona-Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="739e7-104">Perhaps the most important quantity in quantum chemistry simulation is the ground state, which is the minimum energy eigenvector of the Hamiltonian matrix.</span></span>
<span data-ttu-id="739e7-105">Dies liegt daran, dass für die meisten Moleküle in Raumtemperatur Mengen, z. b. die Reaktionsraten, von kostenlosen Energie unterschieden zwischen den Quantum-Zuständen dominiert werden, die den Anfang und das Ende eines Schritts in einem Reaktions Weg beschreiben</span><span class="sxs-lookup"><span data-stu-id="739e7-105">This is because for most molecules at room temperature quantities such as reaction rates are dominated by free energy differences between quantum states that describe the beginning and end of a step in a reaction pathway and at room temperature such intermediate state are usually ground states.</span></span>
<span data-ttu-id="739e7-106">Der Bodenzustand ist in der Regel zu schwer zu erlernen (auch bei einem Quantum-Computer), da er eine Verteilung über eine exponentiell große Anzahl von Konfigurationen ist.</span><span class="sxs-lookup"><span data-stu-id="739e7-106">While the ground state is typically too hard to learn (even with a quantum computer) because it is a distribution over an exponentially large number of configurations.</span></span>
<span data-ttu-id="739e7-107">Mengen, wie z. b. Energie Energie, können erlernt werden.</span><span class="sxs-lookup"><span data-stu-id="739e7-107">Quantities such as ground state energy can be learned.</span></span>
<span data-ttu-id="739e7-108">Wenn z. b. $ \ket{\psi} $ ein reiner Quantum-Status ist, gibt \begin{Equation} E = \bra{\psi} \hat{h} \ket{\psi} \end{Equation} den Mittelwert der Energie an, den das System in diesem Zustand hat.</span><span class="sxs-lookup"><span data-stu-id="739e7-108">For example, if $\ket{\psi}$ is any pure quantum state then \begin{equation} E = \bra{ \psi } \hat{H} \ket{\psi} \end{equation} gives the mean energy that the system has in that state.</span></span>
<span data-ttu-id="739e7-109">Der Zustand "Ground" ist dann der Zustand, der den kleinsten solchen Wert ergibt.</span><span class="sxs-lookup"><span data-stu-id="739e7-109">The ground state then is the state that gives the smallest such value.</span></span> <span data-ttu-id="739e7-110">Daher ist die Auswahl eines Zustands, der so nah wie möglich an den wahren Zustand ist, äußerst wichtig, um die Energie entweder direkt zu schätzen (wie in Variational eigen Solvers) oder durch die Phasen Schätzung.</span><span class="sxs-lookup"><span data-stu-id="739e7-110">As a result, choosing a state that is as close as possible to the true ground state is vitally important for estimating the energy either directly (as is done in variational eigensolvers) or through phase estimation.</span></span>

<span data-ttu-id="739e7-111">Hartree – Fock-Theorie bietet eine einfache Möglichkeit, den Anfangszustand für Quantum-Systeme zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="739e7-111">Hartree–Fock theory gives a simple way to construct the initial state for quantum systems.</span></span> <span data-ttu-id="739e7-112">Es ergibt eine einzige Slater-Determinante Annäherung an den Grundzustand eines Quantum-Systems.</span><span class="sxs-lookup"><span data-stu-id="739e7-112">It yields a single Slater-determinant approximation to the ground state of a quantum system.</span></span> <span data-ttu-id="739e7-113">Zu diesem Zweck findet Sie eine Drehung innerhalb von Fock-Space, die den Energieverbrauch minimiert.</span><span class="sxs-lookup"><span data-stu-id="739e7-113">To that end, it finds a rotation within Fock-space that minimizes the ground state energy.</span></span> <span data-ttu-id="739e7-114">Insbesondere für ein System von $N $-Elektronen führt die-Methode die Drehung \begin{Equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket {0} \mapsto \ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket {0} \defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket {0} , \end{Equation} mit einem antihermitian (d. h. $u =-u ^ \dagger $) Matrix $u = \ sum_ {PQ} U_ {PQ} a ^ \ dagger_p a_q $.</span><span class="sxs-lookup"><span data-stu-id="739e7-114">In particular, for a system of $N$ electrons the method performs the rotation \begin{equation} \prod_{j=0}^{N-1} a^\dagger_j \ket{0} \mapsto \prod_{j=0}^{N-1} e^{u} a^\dagger_j e^{-u} \ket{0}\defeq\prod_{j=0}^{N-1}  \widetilde{a}^\dagger_j  \ket{0}, \end{equation} with an anti-Hermitian (i.e. $u= -u^\dagger$) matrix $u = \sum_{pq} u_{pq} a^\dagger_p a_q$.</span></span> <span data-ttu-id="739e7-115">Beachten Sie, dass die Matrix $u $ die Orbital Drehungen und $ \widetilbe{a} ^ \ dagger_j $ und $ \widetilbe{a} darstellt _J $ die Erstellungs-und Vernichtungs Operatoren für Elektronen darstellt, die "Hartree – Fock Molecular Spin-Orbitals" belegen.</span><span class="sxs-lookup"><span data-stu-id="739e7-115">It should be noted that the matrix $u$ represents the orbital rotations and $\widetilde{a}^\dagger_j$ and $\widetilde{a}_j$ represent creation and annihilation operators for electrons occupying Hartree–Fock molecular spin-orbitals.</span></span>


<span data-ttu-id="739e7-116">Die Matrix $u $ wird dann optimiert, um den erwarteten Wert "Energy $ \bra {0} \ prod_ {j = 0} ^ {n-1} \widetilum{a} \_ j H \prod \_ {k = 0} ^ {N-1} \widetilum{a} ^ \ dagger_k \ket $" zu minimieren {0} .</span><span class="sxs-lookup"><span data-stu-id="739e7-116">The matrix $u$ is then optimized to minimize the expected energy $\bra{0} \prod_{j=0}^{N-1}  \widetilde{a}\_j  H \prod\_{k=0}^{N-1}  \widetilde{a}^\dagger_k\ket{0}$.</span></span> <span data-ttu-id="739e7-117">Obwohl solche Optimierungsprobleme generisch schwierig sein können, ist es in der Praxis, dass der Hartree – Fock-Algorithmus schnell zu einer nahezu optimalen Lösung für das Optimierungsproblem führt, insbesondere für geschlossene shellmoleküle in den Gleichgewichts Geometrien.</span><span class="sxs-lookup"><span data-stu-id="739e7-117">While such optimization problems may be generically hard, in practice the Hartree–Fock algorithm tends to rapidly converge to a near-optimal solution to the optimization problem, especially for closed-shell molecules in the equilibrium geometries.</span></span> <span data-ttu-id="739e7-118">Diese Zustände können als Instanz des-Objekts angegeben werden `FermionWavefunction` .</span><span class="sxs-lookup"><span data-stu-id="739e7-118">We may specify these states as an instance of the `FermionWavefunction` object.</span></span> <span data-ttu-id="739e7-119">Beispielsweise wird der Status $a ^ \ dagger_ {1} a ^ \ dagger_ {2} a ^ \ dagger_ {6} \ket {0} $ in der Chemie Bibliothek wie folgt instanziiert.</span><span class="sxs-lookup"><span data-stu-id="739e7-119">For instance, the state $a^\dagger_{1}a^\dagger_{2}a^\dagger_{6}\ket{0}$ is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
<span data-ttu-id="739e7-120">Es ist auch möglich, Wellenfunktionen mit Indizes zu indizieren `SpinOrbital` und diese Indizes dann wie folgt in ganze Zahlen zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="739e7-120">It is also possible to index wave functions with `SpinOrbital` indices, and then convert these indices to integers as follows.</span></span>
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="739e7-121">Das auffälligste Feature von Hartree – Fock theoretisch ist, dass es einen Quantum-Zustand ergibt, der keine entangslänge zwischen den Elektronen aufweist.</span><span class="sxs-lookup"><span data-stu-id="739e7-121">The most striking feature about Hartree–Fock theory is that it yields a quantum state that has no entanglement between the electrons.</span></span>
<span data-ttu-id="739e7-122">Dies bedeutet, dass häufig eine geeignete qualitative Beschreibung der Eigenschaften von molekularen Systemen zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="739e7-122">This means that it often provides a suitable qualitative description of properties of molecular systems.</span></span> 

<span data-ttu-id="739e7-123">Der Zustand "Hartree-Fock" kann auch wie folgt von einem rekonstruiert werden `FermionHamiltonian` .</span><span class="sxs-lookup"><span data-stu-id="739e7-123">The Hartree-Fock state may also be reconstructed from a `FermionHamiltonian`  as follows.</span></span>
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

<span data-ttu-id="739e7-124">Das Abrufen präziser Ergebnisse, insbesondere bei stark korrelierten Systemen, erfordert aber auch Quantum-Zustände, die über die – Fock-Theorie hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="739e7-124">However, obtaining accurate results, especially for strongly correlated systems, necessitate quantum states that go beyond Hartree–Fock theory.</span></span>
