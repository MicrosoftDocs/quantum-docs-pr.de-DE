---
title: Zweite Quantifizierung | Microsoft-Dokumentation
description: Konzeptionelle Dokumentation zur zweiten Quantisierung
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.secondquantization
ms.openlocfilehash: b3cc7eb8139d2df6e02de371ccf7a423e58ea76d
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2019
ms.locfileid: "73210410"
---
# <a name="second-quantization"></a><span data-ttu-id="0524d-103">Zweite Quantifizierung</span><span class="sxs-lookup"><span data-stu-id="0524d-103">Second Quantization</span></span>

<span data-ttu-id="0524d-104">Die zweite Quantifizierung untersucht das Problem der elektronischen Struktur durch einen anderen.</span><span class="sxs-lookup"><span data-stu-id="0524d-104">Second quantization looks at the problem of electronic structure through a different lens.</span></span>
<span data-ttu-id="0524d-105">Anstatt jeden der $N _E $-Elektronen einem bestimmten Zustand (oder einer beliebigen Orbital) zuzuweisen, verfolgt die zweite Quantifizierung jede Zwischenspeicherung nach und speichert, ob ein Elektron vorhanden ist, und stellt gleichzeitig automatisch die symmetrischen Eigenschaften der entsprechende Wave-Funktion.</span><span class="sxs-lookup"><span data-stu-id="0524d-105">Rather than assigning each of the $N_e$ electrons to a specific state (or orbital), second quantization tracks each orbital and stores whether there is an electron present in each of them and at the same time automatically ensures symmetry properties of the corresponding wave function.</span></span>
<span data-ttu-id="0524d-106">Dies ist wichtig, da die Verwendung von Quantum-Chemie Modellen möglich ist, ohne sich Gedanken über die antisymmetrierung des Eingabe Zustands machen zu müssen (wie für Fermions erforderlich), und auch weil die zweite Quantifizierung das simulieren solcher Modelle mithilfe von Small Quantum ermöglicht. Computer.</span><span class="sxs-lookup"><span data-stu-id="0524d-106">This is important because it allows quantum chemistry models to be specified without having to worry about anti-symmetrizing the input state (as is required for fermions) and also because second quantization allows such models to be simulated using small quantum computers.</span></span>

<span data-ttu-id="0524d-107">Als Beispiel für die zweite Quantifizierung in Aktion gehen wir davon aus, dass $ \psi_0\cdots \psi_{N-1} $ ein orthonormale Satz räumlicher Orbit ist.</span><span class="sxs-lookup"><span data-stu-id="0524d-107">As an example of second quantization in action, let's assume that $\psi_0\cdots \psi_{N-1}$ are an orthonormal set of spatial orbitals.</span></span>
<span data-ttu-id="0524d-108">Diese Orbitals stellen fest, dass das System so genau wie möglich innerhalb des festgelegten begrenzten Basis Satzes dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0524d-108">These orbitals are chosen to represent the system as accurately as possible within the finite basis set considered.</span></span>
<span data-ttu-id="0524d-109">Ein gängiges Beispiel für solche Orbitals sind atomarische Orbitals, die eine eigenständige Basis für das Atom-Atom bilden.</span><span class="sxs-lookup"><span data-stu-id="0524d-109">A common example of such orbitals are atomic orbitals which form an eigenbasis for the hydrogen atom.</span></span>
<span data-ttu-id="0524d-110">Da mit zwei Dreh Zuständen zwei Elektronen vorhanden sind, können zwei Elektronen in jeder solchen räumlichen zwischen Raum angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0524d-110">Because electrons have two spin states, two electrons can be crammed into each such spatial orbital.</span></span>
<span data-ttu-id="0524d-111">Das heißt, gültige Basiszustände sind das Format "$ \psi_{0", "\ubirow}", "\ldots", "\psi_{N-1", "\ubirow}", "\psi_{0", "downarrow}", "\ldots, \psi_{N-1, \downarrow} $", wobei "$ \ubirow $" und "$ \downpfeil $" Freiheit.</span><span class="sxs-lookup"><span data-stu-id="0524d-111">That is to say, the valid basis states are of the form $\psi_{0,\uparrow},\ldots,\psi_{N-1,\uparrow}, \psi_{0,\downarrow},\ldots,\psi_{N-1,\downarrow}$ where $\uparrow$ and $\downarrow$ are labels that specify the two eigenstates of the spin degree of freedom.</span></span>
<span data-ttu-id="0524d-112">Dieser kombinierte Index von $ (j, \sigma) $ für $ \sigma \in \{\ubirow, \downpfeil\}$ wird als Spin-Orbital bezeichnet, da sowohl der räumliche als auch der Dreh Freiheitsgrad gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0524d-112">This combined index of $(j,\sigma)$ for $\sigma \in \{\uparrow,\downarrow\}$ is called a spin-orbital because it stores both the spatial as well as the spin degree of freedom.</span></span>
<span data-ttu-id="0524d-113">In der Chemie Bibliothek werden Spin-Orbitals in einer `SpinOrbital` Datenstruktur gespeichert und wie folgt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0524d-113">In the chemistry library, spin-orbitals are stored in a `SpinOrbital` data structure, and are created as follows.</span></span>

```csharp
    // First, we load the namespace containing spin-orbital objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // First, we assign an orbital index, say `5`. Note that we use 0-indexing,
    // so this is the 6th orbital.
    var orbitalIdx = 5;

    // Second, we assign a spin index, say `Spin.u` for spin up or `Spin.d` for spin down.
    var spin = Spin.d;

    // the spin-orbital (5, ↓) is then
    var spinOrbital = new SpinOrbital(orbitalIdx, spin);

    // A tuple `(int, Spin)` is also implicitly recognized as a spin-orbital.
    (int, Spin) tuple = (orbitalIdx, spin);

    // We explicitly specify the type of `spinOrbital1` to demonstrate
    // the implicit cast to `SpinOrbital`.
    SpinOrbital spinOrbital1 = tuple;
```

<span data-ttu-id="0524d-114">Dies bedeutet, dass wir formal die Basis für die Drehung und den räumlichen Teil der Wave-Funktion als $ \psi_{0} \cdots \psi_{2n-1} $ vorstellen können, wobei jeder der Indizes jetzt eine Enumeration von $ (j, \sigma) $ ist.</span><span class="sxs-lookup"><span data-stu-id="0524d-114">This means that we can formally think of the basis for both the spin and spatial part of the wave function as $\psi_{0} \cdots \psi_{2N-1}$ where each of the indices now is an enumeration of a $(j,\sigma)$.</span></span>
<span data-ttu-id="0524d-115">Eine mögliche Enumeration ist $g (j, \sigma) = j + n\sigma ' $.</span><span class="sxs-lookup"><span data-stu-id="0524d-115">One possible enumeration is $g(j,\sigma) = j+N\sigma'$.</span></span>
<span data-ttu-id="0524d-116">Eine weitere mögliche Enumeration ist $h (j, \sigma) = 2 \* j + \sigma $.</span><span class="sxs-lookup"><span data-stu-id="0524d-116">Another possible enumeration is $h(j,\sigma) = 2\*j + \sigma$.</span></span>
<span data-ttu-id="0524d-117">Die Quantum-Chemie Bibliothek kann diese Konventionen verwenden, und die Spin-Orbitals in einer solchen Codierung können wie folgt instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="0524d-117">The quantum chemistry library can use these conventions, and the spin-orbitals in such an encoding can be instantiated as follows.</span></span>

```csharp
    // Let us use the spin orbital created in the previous snippet.
   var spinOrbital = new SpinOrbital(5, Spin.d);

   // Let us set the total number of orbitals to be say, `7`.
   var nOrbitals = 7;

    // This converts a spin-orbital index to a unique integer, in this case `12`,
    // using the formula `g(j,σ)`.
    var integerIndexHalfUp = spinOrbital.ToInt(IndexConvention.HalfUp);

    // This converts a spin-orbital index to a unique integer, in this case `11`,
    // using the formula `h(j,σ)`.
    var integerIndexUpDown = spinOrbital.ToInt(IndexConvention.UpDown);

    // The default conversion uses the formula `h(j,σ)`, in this case `11`.
    var integerIndexDefault = spinOrbital.ToInt();
```

<span data-ttu-id="0524d-118">Bei fermionic Systems verhindert das Ausschlussprinzip von Pauli, dass mehrere Elektronen gleichzeitig in einer beliebigen Spin-Orbital vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0524d-118">For fermionic systems, the Pauli exclusion principle prevents more than one electron from being present in any spin-orbital at the same time.</span></span>
<span data-ttu-id="0524d-119">Dies bedeutet, dass wir die zwei rechtlichen Zustände für $ \psi_1 $ wie folgt schreiben können: \begin{Equation} \psi_1 \rightarrow \begin{Cases} \ket{0}_1 & \text{if $ \psi_1 $ ist nicht belegt,} </span><span class="sxs-lookup"><span data-stu-id="0524d-119">This means that we can write the two legal states for $\psi_1$ as \begin{equation} \psi_1 \rightarrow \begin{cases} \ket{0}_1 & \text{if $\psi_1$ is not occupied,} </span></span>\\\
<span data-ttu-id="0524d-120">\ket{1}_1 & \text{if $ \psi_1 $ ist belegt.}</span><span class="sxs-lookup"><span data-stu-id="0524d-120">\ket{1}_1 & \text{if $\psi_1$ is occupied.}</span></span> <span data-ttu-id="0524d-121">\end{Cases} \end{Equation} diese Codierung eignet sich hervorragend für Quantum-Computer, da dies bedeutet, dass wir den elektronischen Beruf als einzelnes Quantum-Bit speichern können.</span><span class="sxs-lookup"><span data-stu-id="0524d-121">\end{cases} \end{equation} This encoding is great for quantum computers because it means that we can store the electronic occupation as a single quantum bit.</span></span>

<span data-ttu-id="0524d-122">Die Berufs Zustände für die $2N $ Spin-Orbitals können auf ähnliche Weise in $2N $ Qubits gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0524d-122">The occupation states for the $2N$ spin orbitals can similarly be stored in $2N$ qubits.</span></span>
<span data-ttu-id="0524d-123">Beispiel: Wenn $N = $2, dann lautet der Status $ $ \ket{0} \ket{1} \ket{1} \ket{0}, $ $</span><span class="sxs-lookup"><span data-stu-id="0524d-123">As an example, if $N=2$ then the state $$ \ket{0} \ket{1} \ket{1} \ket{0}, $$</span></span>

<span data-ttu-id="0524d-124">entspricht den Dreh Orbitals $1 $ und $2 $, die mit dem Restwert "Empty" belegt werden.</span><span class="sxs-lookup"><span data-stu-id="0524d-124">would correspond to spin orbitals $1$ and $2$ being occupied with the remainder empty.</span></span>
<span data-ttu-id="0524d-125">Ebenso lautet der Status $ $ \ket{0} \equiv \ket{0} _{0} \cdots \ket{0}_ {N-1}, $ $</span><span class="sxs-lookup"><span data-stu-id="0524d-125">Similarly, the state $$ \ket{0} \equiv \ket{0}_{0} \cdots \ket{0}_{N-1}, $$</span></span>

<span data-ttu-id="0524d-126">hat keine Elektronen und wird als "Vakuumzustand" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0524d-126">has no electrons and is known as the 'vacuum state'.</span></span>

<span data-ttu-id="0524d-127">Ein schöner Nebeneffekt der zweiten Quantifizierung besteht darin, dass die Antisymmetrie des Quantum-Zustands nicht mehr explizit verfolgt werden muss.</span><span class="sxs-lookup"><span data-stu-id="0524d-127">A beautiful side-effect of second quantization is that we no longer have to explicitly keep track of the anti-symmetry of the quantum state.</span></span>
<span data-ttu-id="0524d-128">Der Grund hierfür ist, dass die Antisymmetrie des Zustands selbst durch die Anti-komtypregeln der Operatoren, die elektronische Berufe einer Spin-Orbital erstellen und zerstören, repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="0524d-128">This is because, as we will see, the anti-symmetry of the state represents itself instead through the anti-commutation rules of the operators that create and destroy electronic occupations of a spin orbital.</span></span>

## <a name="fermionic-operators"></a><span data-ttu-id="0524d-129">Fermionic-Operatoren</span><span class="sxs-lookup"><span data-stu-id="0524d-129">Fermionic operators</span></span>

<span data-ttu-id="0524d-130">Die beiden grundlegenden Operatoren, die auf die zweiten quantifizierten Basis-Vektoren reagieren, werden als Erstellungs-und Vernichtungs Operatoren bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0524d-130">The two fundamental operators that act on the second-quantized basis vectors are known as creation and annihilation operators.</span></span>
<span data-ttu-id="0524d-131">Diese Operatoren fügen Elektronen an einer bestimmten Position ein oder zerstören diese.</span><span class="sxs-lookup"><span data-stu-id="0524d-131">These operators insert or destroy electrons at a particular location.</span></span>
<span data-ttu-id="0524d-132">Diese werden $a ^ \dagger_j $ und $a _J $ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0524d-132">These are denoted $a^\dagger_j$ and $a_j$ respectively.</span></span>

<span data-ttu-id="0524d-133">Beispiel: \begin{align} a ^ \dagger_1 \ket{0}_1 = \ket{1}_1, \quad a ^ \dagger_1 \ket{1}_1 = 0, \quad A_1 \ket{0}_1 = 0, \quad A_1 \ket{1}_1 = \ket{0}_1.</span><span class="sxs-lookup"><span data-stu-id="0524d-133">For example, \begin{align} a^\dagger_1 \ket{0}_1 = \ket{1}_1,\quad a^\dagger_1 \ket{1}_1 = 0,\quad a_1 \ket{0}_1 = 0,\quad a_1 \ket{1}_1 = \ket{0}_1.</span></span>
<span data-ttu-id="0524d-134">\end{align} beachten Sie, dass hier $a ^ \dagger_1 \ket{1}_1 = 0 $ und $a _1 \ket{0}_1 $ den NULL-Vektor nicht $ \ket{0}_1 $ ergibt.</span><span class="sxs-lookup"><span data-stu-id="0524d-134">\end{align} Note that here $a^\dagger_1 \ket{1}_1=0$ and $a_1 \ket{0}_1$ yield the zero-vector not $\ket{0}_1$.</span></span>
<span data-ttu-id="0524d-135">Diese Operatoren sind daher weder hermitian noch einheitlich.</span><span class="sxs-lookup"><span data-stu-id="0524d-135">Such operators are therefore neither Hermitian nor unitary.</span></span>
<span data-ttu-id="0524d-136">Wir stellen allgemeine Erstellungs-und Vernichtungs Operatoren mithilfe des <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> Typs dar.</span><span class="sxs-lookup"><span data-stu-id="0524d-136">We represent general creation and annihilation operators using the <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> type.</span></span>
<span data-ttu-id="0524d-137">Beispielsweise wird ein einzelner Erstellungs Operator wie folgt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0524d-137">For instance, a single creation operator is represented as follow.</span></span>

```csharp
    // We load the namespace containing ladder operator objects.
    using Microsoft.Quantum.Chemistry.LadderOperators;

    // Let us use the spin orbital created in the previous snippet.
    var spinOrbitalInteger = new SpinOrbital(5, Spin.d).ToInt();

    // We specify either a creation or annihilation operator using 
    // the enumerable type `RaisingLowering.u` or `RaisingLowering.d`
    // respectively;
    var creationEnum = RaisingLowering.u;

    // The type representing a creation operator is then initialized 
    // as follows. Here, we index these operators with integers.
    // Hence we initialize the generic ladder operator with an
    // integer index type.
    var ladderOperator0 = new LadderOperator<int>(creationEnum, spinOrbitalInteger);

    // An alternate constructor for a LadderOperator instead uses
    // a tuple.
    var ladderOperator1 = new LadderOperator<int>((creationEnum, spinOrbitalInteger));
```

<span data-ttu-id="0524d-138">Mit diesen Operatoren können wir auch $ $ \ket{0} \ket{1} \ket{1} \ket{0} = a ^ \dagger_1 a ^ \dagger_2 \ket{0}^ {\otimes 4} Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="0524d-138">Also using such operators we can express $$ \ket{0} \ket{1} \ket{1} \ket{0} = a^\dagger_1 a^\dagger_2 \ket{0}^{\otimes 4}.</span></span>
<span data-ttu-id="0524d-139">$ $ Diese Sequenz von Operatoren wird in der hamiltona-Simulations Bibliothek mithilfe C# von Code erstellt, der mit dem Single-Spin-Orbital Fall vergleichbar ist, der oben weiter oben behandelt wird:</span><span class="sxs-lookup"><span data-stu-id="0524d-139">$$ This sequence of operators would be constructed within the Hamiltonian simulation library using C# code that is similar to the single-spin orbital case considered above above:</span></span>
```csharp
    // We load the namespace containing fermion-related objects.
    using Microsoft.Quantum.Chemistry.Fermion;

    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We can convert this array of tuples to a sequence of ladder
    // operators using the `ToLadderSequence()` methods.
    var ladderSequences = indices.ToLadderSequence();

    // Sequences of ladder operators are quite general. For instance,
    // they could be bosonic operators, instead of fermionic operators.
    // We specialize them by constructing a `FermionTerm` representing 
    // a fermion creation operator on the index `2` followed by `1`.
    var fermionTerm = new FermionTerm(ladderSequences);
```

<span data-ttu-id="0524d-140">Bei einem System von $k $ Fermions wird in der zweiten Quantisierung die Aktion des Erstellungs Operators $a ^ \dagger_i $ durch $ $ a ^ \dagger_i \ket{n_1, n_2, \ldots, 0_i, \ldots, n_k} = (-1) ^ {S_i} \ket{n_1, n_2, \ldots, 1_I , \ldots, n_k}, $ $ und $ $ a ^ \dagger_i \ket{n_1, n_2, \ldots, 1_I, \ldots, n_k} = 0, $ $ WHERE $S _I = \sum_{j < i} a ^ \dagger_j a_j $ misst die Gesamtzahl der Fermions im Zustand eines einzelnen Partikels, die über einen Index $j < i $ verfügen.</span><span class="sxs-lookup"><span data-stu-id="0524d-140">For a system of $k$ Fermions, in second quantization the action of the creation operator $a^\dagger_i$ is given by $$ a^\dagger_i \ket{n_1, n_2, \ldots, 0_i, \ldots, n_k } = (-1)^{S_i} \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k}, $$ and $$ a^\dagger_i \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k } = 0, $$ where $S_i = \sum_{j<i} a^\dagger_j a_j$ measures the total number of Fermions that are in the state of a single particle and that have an index $j < i$.</span></span>

<span data-ttu-id="0524d-141">Ein Dritter Operator wird häufig auch in zweiten quantifizierten Darstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0524d-141">A third operator is also often used in second quantized representations.</span></span>
<span data-ttu-id="0524d-142">Dieser Operator wird als Zahlen Operator bezeichnet und durch \begin{Equation} n_i = a ^ \dagger_i a_i definiert.</span><span class="sxs-lookup"><span data-stu-id="0524d-142">This operator is known as the number operator and is defined by \begin{equation} n_i = a^\dagger_i a_i.</span></span>
<span data-ttu-id="0524d-143">\end{Equation} dieser Operator zählt die Besetzung eines bestimmten Drehfelds, d. h. "\begin{align} n_i \ket{0}_I & = 0 \ nicht Umlauf</span><span class="sxs-lookup"><span data-stu-id="0524d-143">\end{equation} This operator counts the occupation of a given spin orbital, which is to say \begin{align} n_i \ket{0}_i &= 0\nonumber</span></span>\\\
<span data-ttu-id="0524d-144">n_i \ket{1}_I & = \ket{1}_i.</span><span class="sxs-lookup"><span data-stu-id="0524d-144">n_i \ket{1}_i &= \ket{1}_i.</span></span>
<span data-ttu-id="0524d-145">\end{align} ähnlich wie in den obigen `FermionTerm` Beispielen, wird dieser Zahlen Operator wie folgt konstruiert.</span><span class="sxs-lookup"><span data-stu-id="0524d-145">\end{align} Similar to the above `FermionTerm` examples, this number operator is constructed as follows.</span></span>
```csharp
    // Let us use a new method to compactly create a sequence of ladder
    // operators. Note that we have ommitted specifying whether the 
    // operators are raising or lowering. In this case, the first half
    // will be raising operators, and the second half will be lowering 
    // operators.
    var indices = new[] { 1, 1 }.ToLadderSequence();

    // We now construct a `FermionTerm` representing an annihilation operator
    // on the index 1 followed by the creation operator on the index 1.
    var fermionTerm0 = new FermionTerm(indices);
```

<span data-ttu-id="0524d-146">Bei der Verwendung von Erstellungs-oder Vernichtungs Operatoren in fermionic-Systemen tritt jedoch eine Feinheit auf.</span><span class="sxs-lookup"><span data-stu-id="0524d-146">A subtlety emerges though when using creation or annihilation operators in fermionic systems.</span></span>
<span data-ttu-id="0524d-147">Wir verlangen, dass ein beliebiger gültiger Quantum-Zustand unter dem Austausch von Bezeichnungen antisymmetrisch ist.</span><span class="sxs-lookup"><span data-stu-id="0524d-147">We require that any valid quantum state is anti-symmetric under exchange of labels.</span></span>
<span data-ttu-id="0524d-148">Dies bedeutet, dass $ $ a ^ \dagger_2 a ^ \dagger_1 \ket{0} =-a ^ \dagger_1 a ^ \dagger_2 \ket{0}.</span><span class="sxs-lookup"><span data-stu-id="0524d-148">This means that $$ a^\dagger_2 a^\dagger_1 \ket{0} = -a^\dagger_1 a^\dagger_2 \ket{0}.</span></span>
<span data-ttu-id="0524d-149">$ $ Solche Operatoren werden als "Anti-pendeln" bezeichnet und im Allgemeinen für alle $i. j $ wir haben diese \begin{align} a ^ \dagger_i a ^ \dagger_j =-(1-\delta_{i, j}) a ^ \dagger_j a ^ \dagger_i, \quad a ^ \dagger_i a_j = \delta_{i, j}-a_j a ^ \dagger_i.</span><span class="sxs-lookup"><span data-stu-id="0524d-149">$$ Such operators are said to 'anti-commute' and in general for any $i, j$ we have that \begin{align} a^\dagger_i a^\dagger_j  = -(1-\delta_{i,j})a^\dagger_j a^\dagger_i,\quad a^\dagger_i a_j =\delta_{i,j} - a_j a^\dagger_i.</span></span>
<span data-ttu-id="0524d-150">\end{align} die beiden folgenden <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> Instanzen werden als nicht äquivalent betrachtet.</span><span class="sxs-lookup"><span data-stu-id="0524d-150">\end{align} Thus the following two <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> instances are considered inequivalent</span></span>
```csharp
    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We now construct a `LadderSequence` representing a creation operator
    // on the index 1 followed by 2, then a term with the reverse ordering.
    var laddderSeqeunce = indices.ToLadderSequence();
    var laddderSeqeunceReversed = indices.Reverse().ToLadderSequence();

    // The following Boolean is `false`.
    var equal = laddderSeqeunce == laddderSeqeunceReversed;
```

<span data-ttu-id="0524d-151">Durch die Verwendung einer zweiten quantifizierten Darstellung werden die Anforderungen der Antisymmetrie von Fermionen durch die Verwendung einer zweiten quantifizierten Darstellung vermieden.</span><span class="sxs-lookup"><span data-stu-id="0524d-151">The requirement that each of the creation operators anti-commute means that using a second quantized representation does obviate the challenges faced by the anti-symmetry of Fermions.</span></span>
<span data-ttu-id="0524d-152">Stattdessen wird die Herausforderung in unserer Definition der Erstellungs Operatoren wieder auftauchen.</span><span class="sxs-lookup"><span data-stu-id="0524d-152">Instead the challenge re-emerges in our definition of the creation operators.</span></span> 

<span data-ttu-id="0524d-153">Bei Verwendung der Anti--komtypregeln entsprechen einige `LadderSequence` Instanzen tatsächlich derselben Sequenz von fermionic-Operatoren, manchmal bis zu einem Minuszeichen.</span><span class="sxs-lookup"><span data-stu-id="0524d-153">Using the anti-commutation rules, some `LadderSequence` instances actually correspond to the same sequence of fermionic operators, sometimes up to a minus sign.</span></span>
<span data-ttu-id="0524d-154">Sehen Sie sich beispielsweise den hamiltonan $a _0 ^ \dagger A_1 ^ \dagger A_1 a_0 =-A_1 ^ \dagger a_0 ^ \dagger A_1 a_0 $ an.</span><span class="sxs-lookup"><span data-stu-id="0524d-154">For instance, consider the Hamiltonian $a_0^\dagger a_1^\dagger a_1 a_0 = - a_1^\dagger a_0^\dagger a_1 a_0$.</span></span>
<span data-ttu-id="0524d-155">Dies motiviert uns, eine kanonische Reihenfolge für jede `FermionTerm`zu definieren.</span><span class="sxs-lookup"><span data-stu-id="0524d-155">This motivates us to define a canonical ordering for every `FermionTerm`.</span></span>
<span data-ttu-id="0524d-156">Alle `FermionTerm` werden wie folgt automatisch in kanonischer Reihenfolge eingefügt.</span><span class="sxs-lookup"><span data-stu-id="0524d-156">Any `FermionTerm` is automatically put into canonical order as follows.</span></span>
```csharp
    // We now construct two `FermionTerms` that are equivalent with respect to
    // anti-commutation up to a sign change.
    var fermionTerm0 = new FermionTerm(new[] { 0, 1, 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 1, 0, 1, 0 }.ToLadderSequence());

    // The following Boolean is `true`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // The change in sign is not compared above, but is an internally tracked
    // property of `FermionTerm`.
    int sign0 = fermionTerm0.Coefficient;
    var sign1 = fermionTerm1.Coefficient;

    // The following Boolean is `false`.
    var signEqual = sign0 == sign1;
```

## <a name="second-quantized-fermionic-hamiltonian"></a><span data-ttu-id="0524d-157">Zweite quantifizierte fermionische hamiltonan</span><span class="sxs-lookup"><span data-stu-id="0524d-157">Second-Quantized Fermionic Hamiltonian</span></span>

<span data-ttu-id="0524d-158">Vielleicht ist es nicht verwunderlich, dass die hamiltonan in [Quantum-Modellen für elektronische Systeme](xref:microsoft.quantum.chemistry.concepts.quantummodels) in Form von Erstellungs-und Vernichtungs Operatoren geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0524d-158">It is perhaps unsurprising that the Hamiltonian in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) can be written in terms of creation and annihilation operators.</span></span>
<span data-ttu-id="0524d-159">Insbesondere, wenn "$ \psi\_j $" die Dreh-und Ausgangs Typen sind, die die Grundlage bilden,</span><span class="sxs-lookup"><span data-stu-id="0524d-159">In particular, if $\psi\_j$ are the spin orbitals that form the basis then</span></span>

<span data-ttu-id="0524d-160">\begin{Equation} \hat{h} = \sum\_{PQ} h\_{PQ} a ^ \dagger\_p a\_q + \frac{1}{2}\sum\_{pqrs} h\_{pqrs} a ^ \dagger\_p a ^ \dagger\_q a\_RA\_s + h\_{\textrm NUC}, \label{EQ: totalham} \end{Equation}, wobei $h\_{\textrm NUC} $ die atomare Strom Energie (eine Konstante unter der "Born-Oppenheimer Näherung") und</span><span class="sxs-lookup"><span data-stu-id="0524d-160">\begin{equation} \hat{H} = \sum\_{pq} h\_{pq}a^\dagger\_p a\_q + \frac{1}{2}\sum\_{pqrs} h\_{pqrs}a^\dagger\_p a^\dagger\_q a\_ra\_s +h\_{\textrm nuc},\label{eq:totalHam} \end{equation} where $h\_{\textrm nuc}$ is the nuclear energy (which is a constant under the Born-Oppenheimer approximation) and</span></span>

<span data-ttu-id="0524d-161">\begin{align} h\_{PQ} & = \int\_{-\infty} ^ \infty \psi ^\*\_p (x\_1) \left (-\bruchteil {\nabla ^ 2}{2} + V (x\_1) \right) \psi\_q (x\_1) \mathrm{d} ^ 3X @no__ t_9_ 1, \end{align}</span><span class="sxs-lookup"><span data-stu-id="0524d-161">\begin{align} h\_{pq} &= \int\_{-\infty}^\infty \psi^\*\_p(x\_1) \left(-\frac{\nabla^2}{2} +V(x\_1)\right)  \psi\_q(x\_1)\mathrm{d}^3x\_1, \end{align}</span></span>

<span data-ttu-id="0524d-162">Dabei ist $V (x) $ das Mittelfeld Potenzial und</span><span class="sxs-lookup"><span data-stu-id="0524d-162">where $V(x)$ is the mean-field potential, and</span></span>

<span data-ttu-id="0524d-163">\begin{align} h\_{pqrs} & = \int\_{-\infty} ^ \infty \int\_{-\infty} ^ \infty\psi\_p ^\*(x\_1) \psi\_q ^\*(x\_2) \left (\frac{1}{| x_1-x_2 |} \ Right) \psi\_r (x\_2) \psi\_s (x\_1) \mathrm{d} ^ 3X\_1 \ mathrm {d} ^ 3X\_2. \ Bezeichnung {EQ: Integrals} \end{align}</span><span class="sxs-lookup"><span data-stu-id="0524d-163">\begin{align} h\_{pqrs} &= \int\_{-\infty}^\infty \int\_{-\infty}^\infty\psi\_p^\*(x\_1)\psi\_q^\*(x\_2) \left(\frac{1}{|x_1-x_2|} \right)\psi\_r(x\_2)\psi\_s(x\_1)\mathrm{d}^3x\_1\mathrm{d}^3x\_2.\label{eq:integrals} \end{align}</span></span>

<span data-ttu-id="0524d-164">Die Begriffe $h\_{PQ} $ werden als One-Electron-inteder refereniert, da nur einzelne Elektronen und $h\_{pqrs} $ die zwei-Elektronen-integleich sind.</span><span class="sxs-lookup"><span data-stu-id="0524d-164">The terms $h\_{pq}$ are refered to as one-electron integrals because all such terms only involve single electrons and likewise $h\_{pqrs}$ are the two-electron integrals.</span></span>
<span data-ttu-id="0524d-165">Sie werden als integrale bezeichnet, da das Berechnen der Werte dieser Koeffizienten einen integralen Wert erfordert.</span><span class="sxs-lookup"><span data-stu-id="0524d-165">They are called integrals because computing the values of these coefficients requires an integral.</span></span>
<span data-ttu-id="0524d-166">Die einzelnen Elektronen Begriffe beschreiben die kinetische Energie der einzelnen Elektronen und ihre Interaktionen mit den elektrischen Feldern der Kerne.</span><span class="sxs-lookup"><span data-stu-id="0524d-166">The one electron terms describe the kinetic energy of the individual electrons and their interactions with the electric fields of the nuclei.</span></span>
<span data-ttu-id="0524d-167">Die zwei-Elektronen-inteder auf der anderen Seite beschreiben die Interaktionen zwischen den Elektronen.</span><span class="sxs-lookup"><span data-stu-id="0524d-167">The two-electron integrals on the other hand describe the interactions between the electrons.</span></span>

<span data-ttu-id="0524d-168">Eine Intuition für das, was diese Begriffe bedeuten, kann von den Erstellungs-und Vernichtungs Operatoren abgeleitet werden, die die einzelnen Komponenten bilden.</span><span class="sxs-lookup"><span data-stu-id="0524d-168">An intuition for what these terms mean can be gleaned from the creation and annihilation operators that comprise each of them.</span></span>
<span data-ttu-id="0524d-169">$H _ {PQ} a ^ \dagger_p a_q $ beschreibt z. b. das aus Spin-Orbital $q $ zum Drehen von Orbital $p $ zu drehende Elektron.</span><span class="sxs-lookup"><span data-stu-id="0524d-169">For example, $h_{pq}a^\dagger_p a_q$ describes the electron hopping from spin orbital $q$ to spin orbital $p$.</span></span>
<span data-ttu-id="0524d-170">Ebenso beschreibt der Begriff "$h _ {pqrs} a ^ \dagger_p a ^ \dagger_q a_r a_s $ (für eindeutige $p, q, r, s $)" zwei Elektronen in $r Drehungs-und $s $-Gliederung und endet in Drehungs-Orbitals $p $ und $q $.</span><span class="sxs-lookup"><span data-stu-id="0524d-170">Similarly, the term $h_{pqrs} a^\dagger_p a^\dagger_q a_r a_s$ (for distinct $p,q,r,s$) describes two electrons in spin orbitals $r$ and $s$ scattering off of each other and ending up in spin orbitals $p$ and $q$.</span></span>
<span data-ttu-id="0524d-171">Wenn $r = q $ und $p = s $, gibt $h _ {prrp} a ^ \dagger_p a ^ \dagger_r a_r a_p = H_ {prrp} n_p n_r $ den Energie Nachteil aus, der mit den beiden jeweils naheliegenden Elektronen verbunden ist, aber keinen dynamischen Prozess beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0524d-171">If $r=q$ and $p=s$ then $h_{prrp} a^\dagger_p a^\dagger_r a_r a_p = h_{prrp} n_p n_r$ gives the energy penalty associated with the two electrons being near each other, but does not describe a dynamical process.</span></span>

<span data-ttu-id="0524d-172">Mit der `FermionHamiltonian`-Klasse, die im Wesentlichen eine Liste mit allen gewünschten `FermionTerm`-Instanzen ist, können wir solche hamiltonoren darstellen.</span><span class="sxs-lookup"><span data-stu-id="0524d-172">We may represent such Hamiltonians using the `FermionHamiltonian` class, which is essentially a list containing all the desired `FermionTerm` instances.</span></span>
<span data-ttu-id="0524d-173">Da hamiltonane in der Definition "hermitian" sind, indizieren wir Begriffe mithilfe des spezielleren Typs `HermitianFermionTerm`, der auch die hermitian Symmetrie verwendet, wenn überprüft wird, ob Begriffe äquivalent sind.</span><span class="sxs-lookup"><span data-stu-id="0524d-173">As Hamiltonians are Hermitian by definition, we index terms using the more specialized type `HermitianFermionTerm` that also uses Hermitian symmetry when checking whether terms are equivalent.</span></span>

<span data-ttu-id="0524d-174">Lassen Sie uns einige anschauliche Beispiele erstellen.</span><span class="sxs-lookup"><span data-stu-id="0524d-174">Let us construct a few illustrative examples.</span></span>
<span data-ttu-id="0524d-175">Beachten Sie die hamiltonan $ \hat{h} = a_0 ^ \dagger A_1 + A_1 ^ \dagger a_0 $.</span><span class="sxs-lookup"><span data-stu-id="0524d-175">Consider the Hamiltonian $\hat{H} = a_0^\dagger a_1 + a_1^\dagger a_0$.</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the terms to be added.
    var fermionTerm0 = new FermionTerm(new[] { 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 0, 1 }.ToLadderSequence());

    // These fermion terms are not equal. The following Boolean is `false`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // However, these terms are equal under Hermitian symmetry.
    // We also take the opportunity to demonstrate equivalent constructors
    // for hermitian fermion terms
    var hermitianFermionTerm0 = new HermitianFermionTerm(fermionTerm0);
    var hermitianFermionTerm1 = new HermitianFermionTerm(new[] { 0, 1 });

    // These Hermitian fermion terms are equal. The following Boolean is `true`.
    var hermitianSequenceEqual = hermitianFermionTerm0 == hermitianFermionTerm1;

    // We add the terms to the Hamiltonian with the appropriate coefficient.
    // Note that these terms are identical.
    hamiltonian.Add(hermitianFermionTerm0, 1.0);
    hamiltonian.Add(hermitianFermionTerm1, 1.0);
```
<span data-ttu-id="0524d-176">Wir können diese Konstruktion mit der Tatsache vereinfachen, dass hamiltonan-Operatoren hermitian-Operatoren sind.</span><span class="sxs-lookup"><span data-stu-id="0524d-176">We may simplify this construction using the fact that Hamiltonian operators are Hermitian operators.</span></span>
<span data-ttu-id="0524d-177">Beim Hinzufügen von Begriffen zu "hamiltona" mithilfe von "`Add`" wird davon ausgegangen, dass es sich bei jedem nicht-hermitischen Begriff wie `fermionTerm0` um mit seinem hermitian-konjugitor gekoppelt</span><span class="sxs-lookup"><span data-stu-id="0524d-177">When adding terms to the Hamiltonian using `Add`, any non-Hermitian term such as `fermionTerm0` is assumed to be paired with its Hermitian conjugate.</span></span>
<span data-ttu-id="0524d-178">Der folgende Code Ausschnitt stellt daher auch dieselbe hamiltonan dar:</span><span class="sxs-lookup"><span data-stu-id="0524d-178">Thus the following snippet also represents the same Hamiltonian:</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

<span data-ttu-id="0524d-179">Bei der Verwendung der Anti--komtypregeln entsprechen einige `FermionTerm` Instanzen in der hamiltona tatsächlich derselben Sequenz von fermionic-Operatoren, manchmal bis zu einem Minuszeichen.</span><span class="sxs-lookup"><span data-stu-id="0524d-179">Using the anti-commutation rules, some `FermionTerm` instances in the Hamiltonian actually correspond to the same sequence of fermionic operators, sometimes up to a minus sign.</span></span>
<span data-ttu-id="0524d-180">Sehen Sie sich beispielsweise den hamiltonan $H = a_0 ^ \dagger A_1 ^ \dagger A_1 a_0-A_1 ^ \dagger a_0 ^ \dagger A_1 a_0 = 2a_0 ^ \dagger A_1 ^ \dagger A_1 a_0 $ an, der eine Summe der oben erstellten Begriffe ist.</span><span class="sxs-lookup"><span data-stu-id="0524d-180">For instance, consider the Hamiltonian $H=a_0^\dagger a_1^\dagger a_1 a_0 - a_1^\dagger a_0^\dagger a_1 a_0 =2a_0^\dagger a_1^\dagger a_1 a_0$, which is a sum of terms constructed above.</span></span>
<span data-ttu-id="0524d-181">Es ist für den Benutzer möglicherweise nicht immer klar, dass es sich um äquivalente Begriffe handelt, und daher können Sie der hamiltona separat hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0524d-181">It may not always be clear to the user that these are equivalent terms, and so they may be added to the Hamiltonian separately.</span></span>
<span data-ttu-id="0524d-182">Alternativ kann eine Änderung bereits vorhandener Begriffe in der hamiltonan sinnvoll sein.</span><span class="sxs-lookup"><span data-stu-id="0524d-182">Alternatively, one may be interested in modifying already-existing terms in the Hamiltonian.</span></span>
<span data-ttu-id="0524d-183">In diesen Fällen können wir äquivalente Begriffe wie folgt kombinieren.</span><span class="sxs-lookup"><span data-stu-id="0524d-183">In these cases, we may combine equivalent terms as follows.</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We now create two Hermitian fermion terms that are equivalent with respect to
    // anti-commutation and Hermitian symmetry.
    var terms = new[] {
        (new[] { 0, 1, 1, 0 }, 1.0),
        (new[] { 1, 0, 1, 0 }, 1.0) }
    .Select(o => (new HermitianFermionTerm(o.Item1.ToLadderSequence()), o.Item2.ToDoubleCoeff()));

    // Now add `terms` to the Hamiltonian.
    hamiltonian.AddRange(terms);

    // There is only one unique term. `nTerms == 1` is `true`.
    var nTerms = hamiltonian.CountTerms();
```
<span data-ttu-id="0524d-184">Durch die Kombination von Koeffizienten der äquivalenten Begriffe verringern wir die Gesamtzahl der Begriffe in der hamiltona.</span><span class="sxs-lookup"><span data-stu-id="0524d-184">By combining coefficients of equivalent terms, we reduce the total number of terms in the Hamiltonian.</span></span>
<span data-ttu-id="0524d-185">Später wird dadurch die Anzahl der zum Simulieren der hamiltonan erforderlichen Quantum-Gates reduziert.</span><span class="sxs-lookup"><span data-stu-id="0524d-185">Later on, this reduces the number of quantum gates required to simulate the Hamiltonian.</span></span>

### <a name="internal-representation"></a><span data-ttu-id="0524d-186">Interne Darstellung</span><span class="sxs-lookup"><span data-stu-id="0524d-186">Internal Representation</span></span>

<span data-ttu-id="0524d-187">Eine fermionic-hamiltonan mit ein-und zwei-Text-Interaktionen wird in der zweiten quantifizierten Notation als dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0524d-187">A fermionic Hamiltonian with one- and two-body interactions is represented in second-quantized notation as</span></span>

<span data-ttu-id="0524d-188">$ $ \begin{align} h = \sum\_{PQ} h\_{PQ} a ^ \dagger\_{p} a\_{q} + \frac{1}{2}\sum\_{pqrs} h\_{pqrs} a ^ \dagger\_{p} a ^ \dagger\_{q} a @no__ t_10_ {r} a\_{s}.</span><span class="sxs-lookup"><span data-stu-id="0524d-188">$$ \begin{align} H=\sum\_{pq}h\_{pq}a^\dagger\_{p}a\_{q}+\frac{1}{2}\sum\_{pqrs}h\_{pqrs}a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}.</span></span>
<span data-ttu-id="0524d-189">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="0524d-189">\end{align} $$</span></span>

<span data-ttu-id="0524d-190">In dieser Notation sind höchstens $N ^ 2 + N ^ 4 $ Koeffizienten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0524d-190">In this notation, there are at most $N^2+N^4$ coefficients.</span></span>
<span data-ttu-id="0524d-191">Viele dieser Koeffizienten können jedoch gesammelt werden, da Sie demselben Operator entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0524d-191">However, many of these coefficients may be collected as they correspond to the same operator.</span></span>
<span data-ttu-id="0524d-192">Beispielsweise wenn $p, q, r, s $ unterschiedliche Indizes darstellen, können wir mithilfe der Anti--typzuordnungs Regeln Folgendes anzeigen: $ $ a ^ \dagger\_{p} a ^ \dagger\_{q} a\_{r} a\_{s} =-a ^ \dagger\_{q} a ^ \dagger\_{ p} a\_{r} a\_{s} =-a ^ \dagger\_{p} a ^ \dagger\_{q} a\_{s} a\_{r} = a ^ \dagger\_{q} a ^ \dagger\_{p} a\_{s} a\_{r}.</span><span class="sxs-lookup"><span data-stu-id="0524d-192">For instance, in the case where $p,q,r,s$ are distinct indices, we may use the anti-commutation rules to show that: $$ a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s} = -a^\dagger\_{q}a^\dagger\_{p}a\_{r}a\_{s} = -a^\dagger\_{p}a^\dagger\_{q}a\_{s}a\_{r} = a^\dagger\_{q}a^\dagger\_{p}a\_{s}a\_{r}.</span></span>
$$

<span data-ttu-id="0524d-193">Ebenso wie $H $ "hermitian" ist jeder nicht-hermitian fermionic-Operator, z. b. $h\_{pqrs} a ^ \dagger\_{p} a ^ \dagger\_{q} a\_{r} a\_{s} $, ein hermitian-Konjugate, das auch in $H $ gefunden wird</span><span class="sxs-lookup"><span data-stu-id="0524d-193">Furthermore, as $H$ is Hermitian, every non-Hermitian fermionic operator, say $h\_{pqrs}a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}$, has a Hermitian conjugate that is also found in $H$.</span></span> <span data-ttu-id="0524d-194">Um Gruppen von Begriffen eindeutig zu indizieren, die durch diese Symmetries gekennzeichnet sind, definieren wir eine kanonische Sortierung für die Indizes $ (i\_1, \cdots, i\_n, j\_1, \cdots, j\_m) $ einer beliebigen Sequenz von $n + m $ fermionic Operators $a ^ \dagger\_{i\_1} \cdots a ^ \dagger\_{i\_n} a\_{j\_1} \cdots a\_{j\_m} $As folgt:</span><span class="sxs-lookup"><span data-stu-id="0524d-194">In order to uniquely index groups of terms characterized by these symmetries, we define a canonical ordering on the indices $(i\_1,\cdots,i\_n,j\_1,\cdots,j\_m)$ of any sequence of $n+m$ fermionic operators $a^\dagger\_{i\_1}\cdots a^\dagger\_{i\_n}a\_{j\_1}\cdots a\_{j\_m}$as follows:</span></span>
-   <span data-ttu-id="0524d-195">Alle Erstellungs Operatoren $a ^ \dagger\_{i\_\cdot} $ werden vor allen Vernichtungs Operatoren $a\_{j\_\cdot} $ platziert.</span><span class="sxs-lookup"><span data-stu-id="0524d-195">All creation operators $a^\dagger\_{i\_\cdot}$ are placed before all annihilation operators $a\_{j\_\cdot}$.</span></span>
-   <span data-ttu-id="0524d-196">Alle Erstellungs Operator Indizes werden in aufsteigender Reihenfolge sortiert, d. h. $i\_1 < i\_2 < \cdots < i\_n $.</span><span class="sxs-lookup"><span data-stu-id="0524d-196">All creation operator indices are sorted in ascending order, that is $i\_1< i\_2< \cdots < i\_n$.</span></span>
-   <span data-ttu-id="0524d-197">Alle Vernichtungs Operator Indizes werden in absteigender Reihenfolge sortiert, d. h. $j\_1 > j\_2 \cdots > j\_m $.</span><span class="sxs-lookup"><span data-stu-id="0524d-197">All annihilation operator indices are sorted in descending order, that is $j\_1> j\_2 \cdots > j\_m$.</span></span>
-   <span data-ttu-id="0524d-198">Der linke Index ist kleiner als oder gleich dem äußersten rechten Index, $i\_1 \ Le j\_m $.</span><span class="sxs-lookup"><span data-stu-id="0524d-198">The left-most index is less than or equal to the right-most index, that is $i\_1\le j\_m$.</span></span>

<span data-ttu-id="0524d-199">Lassen Sie uns diesen Satz von kanonationshierorxen als $ $ \begin{align} (i\_1, \cdots, i\_n, j\_1, \cdots, j\_m) \in S\_{n, m} identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0524d-199">Let us identify this set of canonically ordered indices as $$ \begin{align} (i\_1,\cdots,i\_n,j\_1,\cdots,j\_m) \in S\_{n,m}.</span></span>
<span data-ttu-id="0524d-200">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="0524d-200">\end{align} $$</span></span>

<span data-ttu-id="0524d-201">Mit dieser kanonischen Reihenfolge die fermionic-hamiltonan kann als $ $ \begin{align} H = \sum\_{(p, q) \in S\_{1,1}} H '\_{PQ} \bruchteil {a ^ \dagger\_{p} a\_{q} + a ^ \dagger\_{q} a\_{ p}}{2}+ \sum\_{(p, q, r, s) \in s\_{2,2}} h '\_{pqrs} \bruchteil {a ^ \dagger\_{p} a ^ \dagger\_{q} a\_{r} a\_{s} + a ^ \dagger\_{s} a ^ \ der Kreuz\_{r} a\_{q} a\_{p}}{2}, \end{align} $ $ mit angemessen angepassten 1-und zwei-Elektronen-inteden $h '\_{PQ} $ und $h '\_{pqrs} $.</span><span class="sxs-lookup"><span data-stu-id="0524d-201">With this canonical ordering, the fermionic Hamiltonian may be expressed as $$ \begin{align} H=\sum\_{(p,q)\in S\_{1,1}}h'\_{pq}\frac{a^\dagger\_{p}a\_{q}+a^\dagger\_{q}a\_{p}}{2}+\sum\_{(p,q,r,s)\in S\_{2,2}}h'\_{pqrs}\frac{a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}+a^\dagger\_{s}a^\dagger\_{r}a\_{q}a\_{p}}{2}, \end{align} $$ with suitably adapted one- and two-electron integrals $h'\_{pq}$ and $h'\_{pqrs}$, respectively.</span></span>

