---
title: Tiefen Counter-Quantum Development Kit
description: Erfahren Sie mehr über den Microsoft QDK-tiefen Zähler, der den Quantum-Ablauf Verfolgungs Simulator verwendet, um die Anzahl der einzelnen in einem Programm aufgerufenen Vorgänge zu erfassen Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9c3a772861582e5c49fe5ad27519c25a59d617b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859045"
---
# <a name="quantum-trace-simulator-depth-counter"></a>Quantum-Ablauf Verfolgungs Simulator: tiefen Counter

Der tiefen Counter ist Teil des quantumlaufverfolgungs- [Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum Development Kit.
Sie können es zum Erfassen von Anzahlen verwenden, die die untere Grenze der Tiefe jedes in einem Quantum-Programm aufgerufenen Vorgangs darstellen. 

## <a name="depth-values"></a>Tiefen Werte

Standardmäßig haben alle Vorgänge eine Tiefe von **0** (null), mit Ausnahme des `T` Vorgangs mit einer Tiefe von **1**. Dies bedeutet, dass standardmäßig nur die `T` Tiefe der Vorgänge berechnet wird (was häufig wünschenswert ist). Der tiefen Counter aggregiert und sammelt Statistiken über alle Ränder des [Aufruf Diagramms](https://en.wikipedia.org/wiki/Call_graph)des Vorgangs.

Alle <xref:Microsoft.Quantum.Intrinsic> Vorgänge werden in Form von Single-Qubit-Drehungen, <xref:Microsoft.Quantum.Intrinsic.T> Vorgängen, einzelqubit-Clifford-Vorgängen, <xref:Microsoft.Quantum.Intrinsic.CNOT> Vorgängen und Messungen von Multi-Qubit-,-Observables ausgedrückt. Benutzer können die Tiefe für jeden der primitiven Vorgänge über das- `gateTimes` Feld von festlegen <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>Aufrufen des tiefen Zählers

Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit dem tiefen Counter müssen Sie eine <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> -Instanz erstellen, die zugehörige `UseDepthCounter` -Eigenschaft auf **true** festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a>Verwenden des tiefen Zählers in einem c#-Host Programm

Das c#-Beispiel, das in diesem Abschnitt folgt, berechnet die `T` Tiefe des `CCNOT` Vorgangs basierend auf dem folgenden Q# Beispielcode:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Verwenden Sie den folgenden c#-Code, um zu überprüfen, ob die `CCNOT` `T` Tiefe **5** und `ApplySampleWithCCNOT` `T` die Tiefe **6** hat:

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

## <a name="see-also"></a>Siehe auch

- Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API-Referenz.
