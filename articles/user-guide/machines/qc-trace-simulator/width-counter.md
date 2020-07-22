---
title: Width Counter-Quantum Development Kit
description: 'Erfahren Sie mehr über den Microsoft QDK Width-Zähler, der den Quantum-Ablauf Verfolgungs Simulator verwendet, um die Anzahl der von Vorgängen zugeordneten und zugeordneten Qubits in einem Q #-Programm zu zählen.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: af8609dc5c05f7a19b8d21755281427feb29b84c
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871518"
---
# <a name="quantum-trace-simulator-width-counter"></a>Quantum-Ablauf Verfolgungs Simulator: width-Counter

Der Width-Counter ist Teil des Quantum Development Kit- [quantumlaufverfolgungssimulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Sie können es verwenden, um die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits in einem Q #-Programm zu zählen. Einige primitive Vorgänge können zusätzliche Qubits zuordnen, z. b. durch Multiplizieren von kontrollierten `X` Vorgängen oder kontrollierten `T` Vorgängen.

## <a name="invoking-the-width-counter"></a>Aufrufen des breiten Zählers

Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit dem width-Wert müssen Sie eine <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> -Instanz erstellen, die `UseWidthCounter` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a>Verwenden des Width-Zählers in einem c#-Host Programm

Das c#-Beispiel, das in diesem Abschnitt folgt, berechnet die Anzahl zusätzlicher Qubits, die durch die Implementierung eines Multiplikations gesteuerten Vorgangs zugeordnet werden <xref:microsoft.quantum.intrinsic.x> , basierend auf dem folgenden f #-Beispielcode:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

Der Vorgang zum Multiplizieren <xref:microsoft.quantum.intrinsic.x> von Aktionen wirkt sich auf insgesamt fünf Qubits aus, ordnet zwei [hilfskbits](xref:microsoft.quantum.glossary#ancilla)zu und hat eine Eingabe Breite von **5**. Verwenden Sie das folgende c#-Programm, um die Anzahl zu überprüfen:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

Der erste Teil des Programms führt den `ApplyMultiControlledX` Vorgang aus. Im zweiten Teil wird die- [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) Methode verwendet, um die Anzahl der zugeordneten Qubits abzurufen, sowie die Anzahl der Qubits, die der `Controlled X` Vorgang als Eingabe empfangen hat. 

Zum Schluss können Sie alle durch den Wert "width" gesammelten Statistiken im CSV-Format im CSV-Format ausgeben, indem Sie Folgendes verwenden:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Weitere Informationen

- Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API-Referenz.
