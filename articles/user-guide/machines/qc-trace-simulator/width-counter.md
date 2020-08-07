---
title: Width Counter-Quantum Development Kit
description: Erfahren Sie mehr über den Microsoft QDK Width-Zähler, der den Quantum-Ablauf Verfolgungs Simulator verwendet, um die Anzahl der von Vorgängen in einem Programm zugewiesenen und zugeordneten Qubits zu zählen Q# .
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 02f4937aaccf7bf49d6450355c6b42b273071b2e
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868201"
---
# <a name="quantum-trace-simulator-width-counter"></a>Quantum-Ablauf Verfolgungs Simulator: width-Counter

Der Width-Counter ist Teil des Quantum Development Kit- [quantumlaufverfolgungssimulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Damit können Sie die Anzahl von Qubits zählen, die von den einzelnen Vorgängen in einem Programm zugeordnet und abgerufen werden Q# . Einige primitive Vorgänge können zusätzliche Qubits zuordnen, z. b. durch Multiplizieren von kontrollierten `X` Vorgängen oder kontrollierten `T` Vorgängen.

## <a name="invoking-the-width-counter"></a>Aufrufen des breiten Zählers

Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit dem width-Wert müssen Sie eine <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> -Instanz erstellen, die `UseWidthCounter` -Eigenschaft auf **true**festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a>Verwenden des Width-Zählers in einem c#-Host Programm

Das c#-Beispiel, das in diesem Abschnitt folgt, berechnet die Anzahl der zusätzlichen Qubits, die von der Implementierung eines Multiplikations gesteuerten Vorgangs zugeordnet werden <xref:microsoft.quantum.intrinsic.x> , basierend auf dem folgenden Q# Beispielcode:

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
