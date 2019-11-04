---
title: Symmetries von molekularen inteden | Microsoft-Dokumentation
description: Symmetries von molekularen inteals konzeptionelle Dokumente
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
ms.openlocfilehash: 041d600bc8d65e7d67f5fe7d61a69426fb42ffbc
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442386"
---
# <a name="symmetries-of-molecular-integrals"></a>Symmetries von molekularen inteden

Die inhärente Symmetrie von Coulomb hamiltonan, der hamiltona in [Quantum-Modellen für elektronische Systeme](xref:microsoft.quantum.chemistry.concepts.quantummodels), die zeigt, dass die durch die Interaktion untereinander und mit den Kernen miteinander interagierenden Elektronen eine Reihe von Symmetries haben können. wird ausgenutzt, um die Begriffe in der hamiltonan zu komprimieren.
Im Allgemeinen gilt: Wenn keine weiteren Annahmen über die Basisfunktionen $ \psi_j $ erfolgen, haben wir nur das "\begin{Equation} H_ {pqrs} = H_ {qpsr}", "\tag{★} \label{EQ: hpqrs} \end{Equation}", das direkt von den inteden in [Quantum-Modellen für Elektronische Systeme](xref:microsoft.quantum.chemistry.concepts.quantummodels) , bei denen festgestellt wird, dass ihre Werte identisch bleiben, wenn $p, q $ und $r, s $ sich von der Anti-typkommunikation unterscheiden.

Wenn wir davon ausgehen, dass die Dreh-orbitwerte Real wertig sind (wie es bei gauschen Orbital Basen der Fall ist), haben wir weitere Informationen: \begin{Equation} H_ {pqrs} = H_ {qpsr} = H_ {srqp} = H_ {rspq} = H_ {RQPS} = H_ {psrq} = H_ {SPQR} = H_ {qrsp} .\tag {★} \label{EQ: hpqrsreal} \end{ Gleichung} wenn solche Annahmen angenommen werden, können wir die oben genannten Symmetries verwenden, um die Daten zu reduzieren, die zum Speichern der Matrix Elemente der hamiltona mit dem Faktor $8 $ benötigt werden. auf diese Weise wird das Importieren von Daten auf konsistente Weise etwas schwieriger.
Glücklicherweise weist die hamiltonan-Simulations Bibliothek Unterroutinen auf, die verwendet werden können, um ganzzahlige Dateien aus " [Liqui $ | \rangle $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) " oder direkt aus " [nwchem](http://www.nwchem-sw.org/index.php/Main_Page)" zu importieren.

Molekulare Orbital inteder (z. b. die $h\_{PQ} $ und $h\_{pqrs} $-Begriffen) wie diese werden mit dem `OrbitalIntegral`-Typ dargestellt, der eine Reihe hilfreicher Funktionen zum Ausdrücken dieser Symmetrie bereitstellt.
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

Zusätzlich zum Auflisten aller in numerischer Weise identischen Orbital-integwerte kann eine Liste aller in der von einem `OrbitalIntegral` dargestellten "Spin-Orbital"-Indizes wie folgt generiert werden.
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a>Konstruieren von fermionic-hamiltonern aus molekularen inteden

Anstatt eine fermionic-hamiltonan durch Hinzufügen von `FermionTerm`en zu konstruieren, werden alle Begriffe, die den einzelnen einzelnen-Ganzzahlen entsprechen, möglicherweise automatisch hinzugefügt.
Der folgende Code listet z. b. automatisch alle permuational Symmetries auf und ordnet die Begriffe in kanonischer Reihenfolge an: 
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
