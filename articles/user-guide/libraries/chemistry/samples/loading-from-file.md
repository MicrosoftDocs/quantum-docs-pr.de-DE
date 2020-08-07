---
title: Laden eines Hamiltonoperators aus einer Datei
description: Erfahren Sie, wie Sie mithilfe des broombridge-Schemas automatisch eine große hamiltona generieren.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.loadhamiltonian
no-loc:
- Q#
- $$v
ms.openlocfilehash: 57e25bf55009797b01695cef0f3d29b94662ccc0
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869238"
---
# <a name="loading-a-hamiltonian-from-file"></a>Laden eines Hamiltonoperators aus einer Datei
Zuvor haben wir hamiltonane erstellt, indem wir Ihr einzelne Begriffe hinzugefügt haben. Obwohl dies für kleine Beispiele in Ordnung ist, erfordert die Skalierung von Quantum-Chemie eine hamiltonation mit Millionen oder Milliarden von Begriffen. Solche, die von Chemie Paketen wie nwchem generiert werden, sind zu groß, um von Hand zu importieren. In diesem Beispiel wird veranschaulicht, wie eine- `FermionHamiltonian` Instanz automatisch aus einem durch das [broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)dargestellten Molekül generiert werden kann. Zu Referenzzwecken können Sie das bereitgestellte `LithiumHydrideGUI` Beispiel oder das Beispiel überprüfen `RunSimulation` . Eingeschränkte Unterstützung ist auch zum Importieren aus dem Format verfügbar, das von " [Liqui |>](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/)" verwendet wird.

Betrachten wir das Beispiel des Stickstoff Moleküls, das im `IntegralData/YAML` Ordner des beispielrepository bereitgestellt wird. Die Methode zum Laden des `Broombridge` Schemas ist unkompliziert.

```csharp
// This is the name of the file we want to load
var filename = @"n2_1_00Re_sto3g.nw.out.yaml";
// This is the directory containing the file
var root = @"IntegralData\YAML";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge($@"{root}\{filename}");

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.First()`, which selects the first element of the list.
var problem = broombridge.ProblemDescriptions.First();

// This extracts the `OrbitalIntegralHamiltonian` from Broombridge format,
// then converts it to a fermion Hamiltonian, then to a Jordan-Wigner
// representation.
var orbitalIntegralHamiltonian = problem.OrbitalIntegralHamiltonian;
var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);
var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);
```

Das broombridge-Schema enthält auch Vorschläge für den Anfangszustand, der vorbereitet werden soll. Die Bezeichnungen, z. b. `"|G⟩"` oder `"|E1⟩"` , für diese Zustände können angezeigt werden, indem die Datei überprüft wird. Um diese anfänglichen Zustände vorzubereiten, `qSharpData` wird der von den Quantum- Q# Algorithmen verwendete ähnlich dem [vorherigen Abschnitt](xref:microsoft.quantum.chemistry.examples.energyestimate)abgerufen, aber mit einem zusätzlichen Parameter, der den gewünschten Anfangszustand auswählt. Beispiel:
```csharp
// The desired initial state, assuming that a description of it is present in the
// Broombridge schema.
var state = "|E1>";
var wavefunction = problem.Wavefunctions[state].ToIndexing(IndexConvention.UpDown);

// This creates the qSharpData consumable by the Q# chemistry library algorithms.
var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
var qSharpWavefunctionData = wavefunction.ToQSharpFormat();
var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Alle oben aufgeführten Schritte können wie folgt mit den bereitgestellten Hilfsmethoden abgekürzt werden.
```csharp
// This is the name of the file we want to load
var filename = "...";

// This deserializes a Broombridge file, given its filename.
var broombridge = Broombridge.Deserializers.DeserializeBroombridge(filename);

// Note that the deserializer returns a list of `ProblemDescription` instances 
// as the file might describe multiple Hamiltonians. In this example, there is 
// only one Hamiltonian. So we use `.Single()`, which selects the only element of the list.
var problem = broombridge.ProblemDescriptions.Single();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
// If no state is specified, the Hartree-Fock state is used by default.
var qSharpData = problem.ToQSharpFormat("|E1>");
```

Wir können auch eine "hamiltonan" aus der "Liqui" Laden |> Format mit einer sehr ähnlichen Syntax. 

```csharp
// This is the name of the file we want to load
var filename = @"fe2s2_sto3g.dat"; // This is Ferrodoxin.
// This is the directory containing the file
var root = @"IntegralData\Liquid";

// Deserialize the LiQuiD format.
var problem = LiQuiD.Deserialize($@"{root}\{filename}").First();

// This is a data structure representing the Jordan-Wigner encoding 
// of the Hamiltonian that we may pass to a Q# algorithm.
var qSharpData = problem.ToQSharpFormat();
```

Wenn Sie diesen Prozess von einer beliebigen Instanz von broombridge oder einem beliebigen Zwischenschritt ausführen, können Quantum-Algorithmen wie z. b. die Quantum-Phasen-Schätzung auf dem angegebenen elektronischen Strukturproblem ausgeführt werden.
