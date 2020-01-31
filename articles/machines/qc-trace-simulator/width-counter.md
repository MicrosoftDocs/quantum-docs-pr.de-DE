---
title: Breiten-Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: 9c3601e74eec17bd6b463e90f8f3085c959d6f95
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820367"
---
# <a name="width-counter"></a>Breiten-Counter

Der `Width Counter` zählt die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits.
Alle Vorgänge aus dem `Microsoft.Quantum.Intrinsic`-Namespace werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt. Einige der primitiven Vorgänge können zusätzliche Qubits zuordnen. Multiplizieren Sie z. b. die kontrollierten `X` Gates oder kontrollierten `T` Gates. Wir berechnen die Anzahl der zusätzlichen Qubits, die durch die Implementierung eines Multiplikations gesteuerten `X` Gates zugeordnet werden:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Verwenden des Width-Zählers innerhalb eines C# Programms

Bei der multiplizierten `X`, die auf insgesamt 5 Qubits wirkt, werden zwei hilfskbits und die Eingabe Breite 5 verwendet. Um zu überprüfen, ob dies der Fall ist, können wir C# Folgendes Programm verwenden:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
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

Der erste Teil des Programms führt `ApplyMultiControlledX`aus. Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl der zugeordneten Qubits abzurufen, sowie die Anzahl der Qubits, die `X` als Eingabe empfangen haben. 

Zum Schluss können Sie die folgenden Informationen verwenden, um alle Statistiken auszugeben, die von der Width-Zahl im CSV-Format erfasst wurden:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Siehe auch ##

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
