---
title: Tiefen Counter-Quantum Development Kit
description: 'Erfahren Sie mehr über den Microsoft QDK-tiefen Zähler, der den Quantum-Ablauf Verfolgungs Simulator verwendet, um die Anzahl der einzelnen in einem Q #-Programm aufgerufenen Vorgänge zu erfassen.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 811e387fedf547d2681518ae0bb525c13dc84ff4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871126"
---
# <a name="quantum-trace-simulator-depth-counter"></a>Quantum-Ablauf Verfolgungs Simulator: tiefen Counter

Der tiefen Counter ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit.
Sie können es zum Erfassen von Anzahlen verwenden, die die untere Grenze der Tiefe jedes in einem Quantum-Programm aufgerufenen Vorgangs darstellen. 

## <a name="depth-values"></a>Tiefen Werte

Standardmäßig haben alle Vorgänge eine Tiefe von **0** (null), mit Ausnahme des `T` Vorgangs mit einer Tiefe von **1**. Dies bedeutet, dass standardmäßig nur die `T` Tiefe der Vorgänge berechnet wird (was häufig wünschenswert ist). Der tiefen Counter aggregiert und sammelt Statistiken über alle Ränder des [Aufruf Diagramms](https://en.wikipedia.org/wiki/Call_graph)des Vorgangs.

Alle <xref:microsoft.quantum.intrinsic> Vorgänge werden in Form von Single-Qubit-Drehungen, <xref:microsoft.quantum.intrinsic.t> Vorgängen, einzelqubit-Clifford-Vorgängen, <xref:microsoft.quantum.intrinsic.cnot> Vorgängen und Messungen von Multi-Qubit-,-Observables ausgedrückt. Benutzer können die Tiefe für jeden der primitiven Vorgänge über das- `gateTimes` Feld von festlegen <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>Aufrufen des tiefen Zählers

Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit dem tiefen Counter müssen Sie eine <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> -Instanz erstellen, die zugehörige `UseDepthCounter` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a>Verwenden des tiefen Zählers in einem c#-Host Programm

Das c#-Beispiel, das in diesem Abschnitt folgt, berechnet die `T` Tiefe des `CCNOT` Vorgangs basierend auf dem folgenden f #-Beispielcode:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Verwenden Sie den folgenden c#-Code, um zu überprüfen, ob die `CCNOT` `T` Tiefe **5** und `ApplySampleWithCCNOT` `T` die Tiefe **6**hat:

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Der erste Teil des Programms wird ausgeführt `ApplySampleWithCCNOT` . Im zweiten Teil wird die [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) -Methode verwendet, um die `T` Tiefe von `CCNOT` und abzurufen `ApplySampleWithCCNOT` . 

Zum Schluss können Sie mithilfe der folgenden Informationen alle vom tiefen Leistungs befassenden Statistiken im CSV-Format ausgeben:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Weitere Informationen

- Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API-Referenz.
