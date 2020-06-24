---
title: Breiten-Counter
description: Erfahren Sie mehr über den Microsoft QDK Width-Zähler, der die Anzahl der von jedem Vorgang in einem Quantum-Programm zugeordneten und zugeordneten Qubits zählt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274896"
---
# <a name="width-counter"></a>Breiten-Counter

Der `Width Counter` zählt die Anzahl der von jedem Vorgang zugeordneten und zugeordneten Qubits.
Alle Vorgänge aus dem- `Microsoft.Quantum.Intrinsic` Namespace werden in Form einzelner Qubit-Drehungen, T Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt. Einige der primitiven Vorgänge können zusätzliche Qubits zuordnen. Multiplizieren Sie z `X` . b. gesteuerte Gates oder kontrollierte `T` Gates. Wir berechnen die Anzahl zusätzlicher Qubits, die durch die Implementierung eines mehrfach gesteuerten Tors zugeordnet werden `X` :

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Verwenden des Width-Zählers innerhalb eines c#-Programms

Die Multiplikation, `X` die auf insgesamt 5 Qubits durchführt, weist 2 hilfskbits zu, und die Eingabe Breite ist 5. Um zu überprüfen, ob dies der Fall ist, können wir das folgende c#-Programm verwenden:

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

Der erste Teil des Programms wird ausgeführt `ApplyMultiControlledX` . Im zweiten Teil wird die-Methode verwendet `QCTraceSimulator.GetMetric` , um die Anzahl der zugeordneten Qubits sowie die Anzahl von Qubits abzurufen, die von `X` als Eingabe gesteuert werden. 

Zum Schluss können Sie die folgenden Informationen verwenden, um alle Statistiken auszugeben, die von der Width-Zahl im CSV-Format erfasst wurden:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Weitere Informationen ##

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
