---
title: Hartree-Fock Theorie
description: Erfahren Sie mehr über die Hartree – Fock-Theorie, eine einfache Möglichkeit, den Anfangszustand für Quantum-Systeme zu erstellen.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.hartreefock
no-loc:
- Q#
- $$v
ms.openlocfilehash: 48d6bc4face90046271dd8705188a92daafad98a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854092"
---
# <a name="hartreefock-theory"></a>Hartree – Fock-Theorie

Die vielleicht wichtigste Menge in der Quantum-Chemie-Simulation ist der Boden Status, der der minimale Energie eigen Vektor der hamiltona-Matrix ist.
Dies liegt daran, dass für die meisten Moleküle in Raumtemperatur Mengen, z. b. die Reaktionsraten, von kostenlosen Energie unterschieden zwischen den Quantum-Zuständen dominiert werden, die den Anfang und das Ende eines Schritts in einem Reaktions Weg beschreiben
Der Bodenzustand ist in der Regel zu schwer zu erlernen (auch bei einem Quantum-Computer), da er eine Verteilung über eine exponentiell große Anzahl von Konfigurationen ist.
Mengen, wie z. b. Energie Energie, können erlernt werden.
Wenn z. b. $ \ket{\psi} $ ein reiner Quantum-Status ist, gibt \begin{Equation} E = \bra{\psi} \hat{h} \ket{\psi} \end{Equation} den Mittelwert der Energie an, den das System in diesem Zustand hat.
Der Zustand "Ground" ist dann der Zustand, der den kleinsten solchen Wert ergibt. Daher ist die Auswahl eines Zustands, der so nah wie möglich an den wahren Zustand ist, äußerst wichtig, um die Energie entweder direkt zu schätzen (wie in Variational eigen Solvers) oder durch die Phasen Schätzung.

Hartree – Fock-Theorie bietet eine einfache Möglichkeit, den Anfangszustand für Quantum-Systeme zu erstellen. Es ergibt eine einzige Slater-Determinante Annäherung an den Grundzustand eines Quantum-Systems. Zu diesem Zweck findet Sie eine Drehung innerhalb von Fock-Space, die den Energieverbrauch minimiert. Insbesondere für ein System von $N $-Elektronen führt die-Methode die Drehung \begin{Equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket {0} \mapsto \ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket {0} \defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket {0} , \end{Equation} mit einem antihermitian (d. h. $u =-u ^ \dagger $) Matrix $u = \ sum_ {PQ} U_ {PQ} a ^ \ dagger_p a_q $. Beachten Sie, dass die Matrix $u $ die Orbital Drehungen und $ \widetilbe{a} ^ \ dagger_j $ und $ \widetilbe{a} darstellt _J $ die Erstellungs-und Vernichtungs Operatoren für Elektronen darstellt, die "Hartree – Fock Molecular Spin-Orbitals" belegen.


Die Matrix $u $ wird dann optimiert, um den erwarteten Wert "Energy $ \bra {0} \ prod_ {j = 0} ^ {n-1} \widetilum{a} \_ j H \prod \_ {k = 0} ^ {N-1} \widetilum{a} ^ \ dagger_k \ket $" zu minimieren {0} . Obwohl solche Optimierungsprobleme generisch schwierig sein können, ist es in der Praxis, dass der Hartree – Fock-Algorithmus schnell zu einer nahezu optimalen Lösung für das Optimierungsproblem führt, insbesondere für geschlossene shellmoleküle in den Gleichgewichts Geometrien. Diese Zustände können als Instanz des-Objekts angegeben werden `FermionWavefunction` . Beispielsweise wird der Status $a ^ \ dagger_ {1} a ^ \ dagger_ {2} a ^ \ dagger_ {6} \ket {0} $ in der Chemie Bibliothek wie folgt instanziiert.
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
Es ist auch möglich, Wellenfunktionen mit Indizes zu indizieren `SpinOrbital` und diese Indizes dann wie folgt in ganze Zahlen zu konvertieren.
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

Das auffälligste Feature von Hartree – Fock theoretisch ist, dass es einen Quantum-Zustand ergibt, der keine entangslänge zwischen den Elektronen aufweist.
Dies bedeutet, dass häufig eine geeignete qualitative Beschreibung der Eigenschaften von molekularen Systemen zur Verfügung steht. 

Der Hartree-Fock Status kann auch wie folgt aus einem rekonstruiert werden `FermionHamiltonian`  .
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

Das Abrufen präziser Ergebnisse, insbesondere bei stark korrelierten Systemen, erfordert aber auch Quantum-Zustände, die über die – Fock-Theorie hinausgehen.
