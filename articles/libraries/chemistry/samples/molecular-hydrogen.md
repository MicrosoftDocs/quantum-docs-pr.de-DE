---
title: Abrufen von Energie Stufen Schätzungen | Microsoft-Dokumentation
description: Dokumente zum Abrufen von Energiepegel Schätzungen
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: 0fd457b152083af364d924502c18bc0813e34b83
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442586"
---
# <a name="obtaining-energy-level-estimates"></a>Abrufen von Energiestandschätzungen
Das Einschätzen der Werte von Energie Stufen ist eine der Hauptanwendungen der Quantum-Chemie. Hier wird erläutert, wie dies für das kanonische Beispiel für den molekularen Wasserstoff ausgeführt werden kann. Das in diesem Abschnitt referenzierte Beispiel ist `MolecularHydrogen` im Repository "Chemistry Samples". Ein visuelles Beispiel, in dem die Ausgabe dargestellt wird, ist die `MolecularHydrogenGUI` Demo.

Der erste Schritt ist das Erstellen der hamiltona, die den molekularen Wasserstoff darstellt. Obwohl dies über das nwchem-Tool erstellt werden kann, fügen wir der in diesem Beispiel hinzu.

```csharp
    // These orbital integrals are represented using the OrbitalIntegral
    // data structure.
    var energyOffset = 0.713776188; // This is the coulomb repulsion
    var nElectrons = 2; // Molecular hydrogen has two electrons
    var orbitalIntegrals = new OrbitalIntegral[]
    {
        new OrbitalIntegral(new[] { 0,0 }, -1.252477495),
        new OrbitalIntegral(new[] { 1,1 }, -0.475934275),
        new OrbitalIntegral(new[] { 0,0,0,0 }, 0.674493166),
        new OrbitalIntegral(new[] { 0,1,0,1 }, 0.181287518),
        new OrbitalIntegral(new[] { 0,1,1,0 }, 0.663472101),
        new OrbitalIntegral(new[] { 1,1,1,1 }, 0.697398010),
        // This line adds the identity term.
        new OrbitalIntegral(new int[] { }, energyOffset)
    };

    // We initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Zum Simulieren der hamiltona müssen wir die Fermion-Operatoren in Qubit-Operatoren konvertieren. Diese Konvertierung erfolgt wie folgt über die Jordanien-Wigner-Codierung.

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // We also need to create an input quantum state to this Hamiltonian.
    // Let us use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Wir übergeben nun die `qSharpData`, die die "hamiltonan" darstellt, an die Funktion "`TrotterStepOracle`", um [hamiltonan Dynamics zu simulieren](xref:microsoft.quantum.libraries.standard.algorithms). `TrotterStepOracle` gibt eine Quantum-Operation zurück, die der echtzeitentwicklung der hamiltonan entspricht.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operatrion.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

Wir können nun die Phasen Schätz Algorithmen der Standardbibliothek verwenden, um die Grund Zustands Energie mithilfe der obigen Simulation zu erlernen. Dies erfordert, dass eine gute Näherung für den Quantum-Grundzustand vorbereitet wird. Vorschläge für solche Näherungen werden im `Broombridge` Schema bereitgestellt, aber diese Vorschläge sind nicht vorhanden. der Standardansatz fügt eine Reihe von `hamiltonian.NElectrons`-Elektronen hinzu, um die diagonalen ein-Elektronen-ergriffsenergien zu minimieren. Die Funktionen und Vorgänge der Phasen Schätzung befinden sich im [Microsoft. Quantum. Charakterisierung-Namespace](xref:microsoft.quantum.characterization in DocFX notation).

Der folgende Code Ausschnitt zeigt, wie die Real-Time-Evolution-Ausgabe durch die Simulations Bibliothek der Chemie in die Quantum-Phasen Schätzung integriert werden kann.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined below.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // We use the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // We obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // We return both the estimated phase, and the estimated energy.
    return (estPhase, estEnergy);
}
```

Dieser Q #-Code kann jetzt vom Treiber Programm aufgerufen werden. Im folgenden erstellen wir einen vollständigen Simulator und führen `GetEnergyByTrotterization` aus, um die Energie des Energie Zustands zu erhalten.

```csharp
using (var qsim = new QuantumSimulator())
{
    // We specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // We specify the step-size of the simulated time-evolution. This needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, let us run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular Hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

Beachten Sie, dass zwei Parameter zurückgegeben werden. `energyEst` ist die Schätzung der Energie des Mittel Zustands und sollte im Durchschnitt um `-1.137` herumliegen. `phaseEst` ist die vom Phasen Schätz Algorithmus zurückgegebene unformatierte Phase und ist hilfreich, um zu diagnostizieren, wenn Aliasing aufgrund einer zu großen `trotterStep` auftritt.
