---
title: Abrufen von Energiestandschätzungen
description: Exemplarische Vorgehensweise Q# für ein Beispielprogramm, mit dem die Energiepegel Werte von molekularen Wasserstoff geschätzt werden.
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
no-loc:
- Q#
- $$v
ms.openlocfilehash: a2df4b829a3f4946c6de6e6b80ad72a5bc192b2c
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869204"
---
# <a name="obtaining-energy-level-estimates"></a>Abrufen von Energiestandschätzungen
Das Einschätzen der Werte von Energie Stufen ist eine der Hauptanwendungen der Quantum-Chemie. In diesem Artikel wird beschrieben, wie Sie dies für das kanonische Beispiel für den molekularen Wasserstoff durchführen können. Das in diesem Abschnitt referenzierte Beispiel befindet sich [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) im Repository "Chemistry Samples". Ein visuelles Beispiel, in dem die Ausgabe dargestellt wird, ist die [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogenGUI) Demo.

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a>Schätzen der Energiewerte von molekularer Wasserstoff

Der erste Schritt ist das Erstellen der hamiltona, die den molekularen Wasserstoff darstellt. Obwohl Sie dies mithilfe des nwchem-Tools erstellen können, werden in diesem Beispiel die hamiltona-Begriffe manuell hinzugefügt.

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

    // Initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Zum Simulieren der hamiltona müssen die Fermion-Operatoren in Qubit-Operatoren umgerechnet werden. Diese Konvertierung erfolgt wie folgt über die Jordanien-Wigner-Codierung:

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // You also need to create an input quantum state to this Hamiltonian.
    // Use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Als Nächstes übergeben `qSharpData` Sie, das den hamiltonan die Funktion darstellt `TrotterStepOracle` . `TrotterStepOracle`gibt eine Quantum-Operation zurück, die der echtzeitentwicklung der hamiltonan entspricht. Weitere Informationen finden Sie unter [Simulieren von hamiltona Dynamics](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms).

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

An diesem Punkt können Sie die [Phasen Schätz Algorithmen](xref:microsoft.quantum.libraries.characterization) der Standardbibliothek verwenden, um die Grund Zustands Energie mithilfe der vorherigen Simulation zu erlernen. Dies erfordert, dass eine gute Näherung für den Quantum-Grundzustand vorbereitet wird. Vorschläge für solche Näherungen werden im Schema bereitgestellt [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) . Ohne diese Vorschläge fügt der Standardansatz jedoch eine Reihe von Elektronen hinzu, `hamiltonian.NElectrons` um die diagonalen 1-Elektronen-ergriffsenergien zu minimieren. Die Funktionen und Vorgänge der Phasen Schätzung werden in der docfx-Notation im [Microsoft. Quantum. Charakterisierung](xref:microsoft.quantum.characterization) -Namespace bereitgestellt.

Der folgende Code Ausschnitt zeigt, wie die echtzeitentwicklung durch die Simulations Bibliothek für die Chemie in die Quantum-Phasen-Schätzung integriert wird.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // Using a Product formula, also known as `Trotterization`, to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined here.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // Using the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // Now, obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // Return both the estimated phase and the estimated energy.
    return (estPhase, estEnergy);
}
```

Nun können Sie den Q# Code aus dem Host Programm aufrufen. Mit dem folgenden c#-Code wird ein vollständiger Simulator erstellt und ausgeführt `GetEnergyByTrotterization` , um die Energie des Mittel Zustands zu erhalten.

```csharp
using (var qsim = new QuantumSimulator())
{
    // Specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // Specify the step size of the simulated time evolution. The step size needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

Der-Vorgang gibt zwei Parameter zurück: 

- `energyEst`Gibt an, wie hoch die Energie des Mittelwerts ist und wie `-1.137` im Durchschnitt liegen sollte. 
- `phaseEst`die vom Phasen Schätz Algorithmus zurückgegebene RAW-Phase. Dies ist nützlich für die Diagnose von Aliasing, wenn es aufgrund eines `trotterStep` zu großen Werts auftritt.
