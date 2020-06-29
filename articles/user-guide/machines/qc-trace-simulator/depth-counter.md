---
title: Tiefen Counter
description: Erfahren Sie mehr über den Microsoft QDK-tiefen Zähler, der die Anzahl der tiefen jedes in einem Quantum-Programm aufgerufenen Vorgangs sammelt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 0029a00e6a3563dc542daeda2afa7cabf42441fb
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415260"
---
# <a name="depth-counter"></a>Tiefen Counter

Der `Depth Counter` ist ein Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.
Es wird verwendet, um Zähler zu erfassen, die die untere Grenze der Tiefe jedes in einem Quantum-Programm aufgerufenen Vorgangs darstellen. Alle Vorgänge von <xref:microsoft.quantum.intrinsic> werden als einzelne Qubit-Drehungen, T Gates, Single Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt. Benutzer können die Tiefe für jeden der primitiven Vorgänge über das- `gateTimes` Feld von festlegen <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

Standardmäßig haben alle Vorgänge eine Tiefe von 0, außer dem T-Gate, das Tiefe 1 hat. Dies bedeutet, dass standardmäßig nur die T-Tiefe der Vorgänge berechnet wird (was häufig wünschenswert ist). Gesammelte Statistiken werden über alle Ränder des Vorgangs Aufruf Diagramms aggregiert. 

Wir berechnen nun die <xref:microsoft.quantum.intrinsic.t> Tiefe des <xref:microsoft.quantum.intrinsic.ccnot> Vorgangs. Der folgende f #-Beispielcode wird verwendet:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>Verwenden des tiefen Zählers innerhalb eines c#-Programms

Um zu überprüfen, ob `CCNOT` `T` die Tiefe 5 hat und `ApplySampleWithCCNOT` `T` die Tiefe 6 aufweist, können wir den folgenden c#-Code verwenden:

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Der erste Teil des Programms wird ausgeführt `ApplySampleWithCCNOT` . Im zweiten Teil wird die-Methode verwendet, `QCTraceSimulator.GetMetric` um die `T` Tiefe von und zu erhalten `CCNOT` `ApplySampleWithCCNOT` : 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Zum Schluss können Sie, um alle im CSV-Format gesammelten Statistiken auszugeben, `Depth Counter` Folgendes verwenden:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Siehe auch ##

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
