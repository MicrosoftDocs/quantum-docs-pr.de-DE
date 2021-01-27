---
title: Symmetries von molekularen inteden
description: Erfahren Sie, wie Sie den Q# Typ "orbitalintegral" verwenden, um molekulare Symmetries aufzulisten.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.symmetries
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2622285fd95eddf0d70402ae99dd18bfd8c38087
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858823"
---
# <a name="symmetries-of-molecular-integrals"></a><span data-ttu-id="54351-103">Symmetries von molekularen inteden</span><span class="sxs-lookup"><span data-stu-id="54351-103">Symmetries of Molecular Integrals</span></span>

<span data-ttu-id="54351-104">Die inhärente Symmetrie von Coulomb hamiltonan, der hamiltona in [Quantum-Modellen für elektronische Systeme](xref:microsoft.quantum.chemistry.concepts.quantummodels), die die interaktive Interaktion von Elektronen und der Kerne beschreiben, führt zu einer Reihe von Symmetries, die ausgenutzt werden können, um die Begriffe in der hamiltona zu komprimieren.</span><span class="sxs-lookup"><span data-stu-id="54351-104">The inherent symmetry of the Coulomb Hamiltonian, which is the Hamiltonian given in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels), that describes electrons interacting electrically with each other and with the nuclei, leads to a number of symmetries that can be exploited to compress the terms in the Hamiltonian.</span></span>
<span data-ttu-id="54351-105">Im Allgemeinen haben wir nur "\begin{Equation}" H_ {pqrs} = H_ {qpsr}, wenn keine weiteren Annahmen über die Basisfunktionen $ \ psi_j $ vorgenommen werden. \tag{★} \label{EQ: hpqrs} \end{Equation}, das direkt von den inteden in [Quantum-Modellen für elektronische Systeme](xref:microsoft.quantum.chemistry.concepts.quantummodels) eingesehen werden kann, wenn Sie feststellen, dass ihre Werte identisch bleiben, wenn sich $p, q $ und $r, s $ von der Anti--typverarbeitung unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="54351-105">In general if no further assumptions are made about the basis functions $\psi_j$ then we only have that \begin{equation} h_{pqrs}= h_{qpsr},\tag{★}\label{eq:hpqrs} \end{equation} which can be immediately seen from the integrals in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) upon noting that their values remain identical if $p,q$ and $r,s$ are interchanged from anti-commutation.</span></span>

<span data-ttu-id="54351-106">Wenn wir davon ausgehen, dass die Dreh-orbitwerte Real wertig sind (wie es bei gauschen Orbital Basen der Fall ist), haben wir die Funktion "\begin{Equation}" H_ {pqrs} = H_ {qpsr} = H_ {srqp} = H_ {rspq} = H_ {RQPS} = H_ {psrq} = H_ {SPQR} = H_ {qrsp} .\tag {★} \label{EQ: hpqrsreal} \end{Equation}, wenn solche Annahmen angenommen werden, wir können die obigen Symmetries verwenden, um die Daten zu reduzieren, die zum Speichern der Matrix Elemente der hamiltona mit dem Faktor $8 $ erforderlich sind; auf diese Weise wird das Importieren von Daten auf konsistente Weise etwas schwieriger.</span><span class="sxs-lookup"><span data-stu-id="54351-106">If we assume that the spin-orbitals are real-valued (as they are for Gaussian orbital bases) then we further have that \begin{equation} h_{pqrs} = h_{qpsr} = h_{srqp} = h_{rspq}=h_{rqps}=h_{psrq}=h_{spqr}=h_{qrsp}.\tag{★}\label{eq:hpqrsreal} \end{equation} Given such assumptions hold, we can use the above symmetries to reduce the data needed to store the matrix elements of the Hamiltonian by a factor of $8$; although doing so makes importing data in a consistent way slightly more challenging.</span></span>
<span data-ttu-id="54351-107">Glücklicherweise weist die hamiltonan-Simulations Bibliothek Unterroutinen auf, die verwendet werden können, um ganzzahlige Dateien aus " [Liqui $ | \rangle $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) " oder direkt aus " [nwchem](http://www.nwchem-sw.org/index.php/Main_Page)" zu importieren.</span><span class="sxs-lookup"><span data-stu-id="54351-107">Fortunately the Hamiltonian simulation library has subroutines that can be used to import integral files from either [LIQUI$|\rangle$](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) or directly from [NWChem](http://www.nwchem-sw.org/index.php/Main_Page).</span></span>

<span data-ttu-id="54351-108">Molekular-Orbital inteder (d. h. die $h \_ {PQ} $ und $h \_ {pqrs} $-Begriffen) wie diese werden mithilfe des- `OrbitalIntegral` Typs dargestellt, der eine Reihe hilfreicher Funktionen zum Ausdrücken dieser Symmetrie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="54351-108">Molecular orbital integrals (i.e. the $h\_{pq}$ and $h\_{pqrs}$ terms) such as these are represented using the `OrbitalIntegral` type, which provides a number of helpful functions to express this symmetry.</span></span>
```csharp
    // Load the namespace containing orbital integral objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // Create a `OrbitalIntegral` instance to store a one-electron molecular 
    // orbital integral data.
    var oneElectronOrbitalIndices = new[] { 0, 1 };
    var oneElectronCoefficient = 1.0;
    var oneElectronIntegral = new OrbitalIntegral(oneElectronOrbitalIndices, oneElectronCoefficient);

    // This enumerates all one-electron integrals with the same coefficient --
    // an array of equivalent `OrbitalIntegral` instances is generated. In this
    // case, there are two elements.
    var oneElectronIntegrals = oneElectronIntegral.EnumerateOrbitalSymmetries();

    // Create a `OrbitalIntegral` instance to store a two-electron molecular orbital integral data.
    var twoElectronOrbitalIndices = new[] { 0, 1, 2, 3 };
    var twoElectronCoefficient = 0.123;
    var twoElectronIntegral = new OrbitalIntegral(twoElectronOrbitalIndices, twoElectronCoefficient);

    // This enumerates all two-electron integrals with the same coefficient -- 
    // an array of equivalent `OrbitalIntegral` instances is generated. In 
    // this case, there are 8 elements.
    var twoElectronIntegrals = twoElectronIntegral.EnumerateOrbitalSymmetries();
```

<span data-ttu-id="54351-109">Zusätzlich zur Enumeration aller auf numerischer Weise identischen Orbital inteder können Sie eine Liste aller Spin-Orbital-Indizes, die in der von einem dargestellten hamiltona enthalten sind, `OrbitalIntegral` wie folgt generieren.</span><span class="sxs-lookup"><span data-stu-id="54351-109">In addition to enumerating over all orbital integrals that are numerically identical, a list of all spin-orbital indices contained in the Hamiltonian represented by an `OrbitalIntegral` may be generated as follows.</span></span>
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a><span data-ttu-id="54351-110">Konstruieren von fermionic-hamiltonern aus molekularen inteden</span><span class="sxs-lookup"><span data-stu-id="54351-110">Constructing Fermionic Hamiltonians from Molecular Integrals</span></span>

<span data-ttu-id="54351-111">Anstatt eine fermionic-hamiltonan durch Hinzufügen von-Objekten `FermionTerm` zu erstellen, werden alle Begriffe, die den einzelnen vollständig verwendeten Ganzzahlen entsprechen, möglicherweise automatisch</span><span class="sxs-lookup"><span data-stu-id="54351-111">Rather than constructing a Fermionic Hamiltonian by adding `FermionTerm`s, all terms corresponding to each orbital integral may be added automatically.</span></span>
<span data-ttu-id="54351-112">Der folgende Code listet z. b. automatisch alle permuational Symmetries auf und ordnet die Begriffe in kanonischer Reihenfolge an:</span><span class="sxs-lookup"><span data-stu-id="54351-112">For example, the following code automatically enumerates over all permutational symmetries and orders the terms in canonical order:</span></span> 
```csharp
    // Load the namespace containing fermion objects. This
    // example also uses LINQ queries.
    using Microsoft.Quantum.Chemistry.Fermion;
    using System.Linq;

    // Create a `OrbitalIntegral` instance to store a two-electron molecular 
    // orbital integral data.
    var orbitalIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // Create an `OrbitalIntegralHamiltonian` instance to store the orbital integral
    // terms
    var orbitalIntegralHamiltonian = new OrbitalIntegralHamiltonian();
    orbitalIntegralHamiltonian.Add(orbitalIntegral);

    // Convert the orbital integral representation to a fermion
    // representation. This also requires choosing a convention for 
    // mapping spin orbital indices to integer indices.
    var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);

    // Alternatively, one can add orbital integrals directly to a fermion Hamiltonian
    // as follows. This automatically enumerates over all symmetries, and then
    // orders the `HermitianFermionTerm` instances in canonical order. We will need to
    // choose an indexing convention as well.
    fermionHamiltonian.AddRange(orbitalIntegral
        .ToHermitianFermionTerms(0, IndexConvention.UpDown)
        .Select(o => (o.Item1, o.Item2.ToDoubleCoeff())));
```
