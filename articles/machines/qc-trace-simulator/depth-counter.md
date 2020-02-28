---
title: Tiefen Counter
description: Erfahren Sie mehr über den Microsoft QDK-tiefen Zähler, der die Anzahl der tiefen jedes in einem Quantum-Programm aufgerufenen Vorgangs sammelt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: d532a9f512b8c87d83d62ed26e3bb67e1b6f668b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906099"
---
# <a name="depth-counter"></a>Tiefen Counter

Der `Depth Counter` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer.
Es wird verwendet, um die Anzahl der tiefen jedes in einem Quantum-Programm aufgerufenen Vorgangs zu erfassen. Alle Vorgänge aus <xref:microsoft.quantum.intrinsic> werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt. Benutzer können die Tiefe für die einzelnen primitiven Vorgänge über das `gateTimes`-Feld <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>festlegen.

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

## <a name="using-depth-counter-within-a-c-program"></a>Verwenden des tiefen Zählers C# innerhalb eines Programms

Um zu überprüfen, ob `CCNOT` `T` Tiefe 5 hat und `ApplySampleWithCCNOT` `T` Tiefe 6 hat, können C# wir den folgenden Code verwenden:

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

Der erste Teil des Programms führt `ApplySampleWithCCNOT`aus. Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die `T` Tiefe von `CCNOT` und `ApplySampleWithCCNOT`zu erhalten: 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Zum Schluss können Sie zum Ausgeben aller Statistiken, die von `Depth Counter` im CSV-Format gesammelt werden, Folgendes verwenden:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Weitere Informationen ##

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
