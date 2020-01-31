---
title: Primitiver Vorgangs-Counter | Ablauf Verfolgungs Simulator für Quantum-Computer | Microsoft-Dokumentation
description: Übersicht über Ablaufverfolgungssimulator für Quantencomputer
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 1f554c0a1b92c8f6b59be3a9d9965e0e25bd074f
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820418"
---
# <a name="primitive-operations-counter"></a>Primitiver Vorgangs-Counter  

Der `Primitive Operations Counter` ist Teil des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro)für Quantum-Computer. Sie zählt die Anzahl primitiver Ausführungen, die von jedem in einem Quantum-Programm aufgerufenen Vorgang verwendet werden. Alle Vorgänge aus `Microsoft.Quantum.Intrinsic` werden in Form einzelner Qubit-Drehungen, t Gates, einzelner Qubit Clifford Gates, CNOT Gates und Messungen von Multi-Qubit Pauli Observables ausgedrückt. Gesammelte Statistiken werden über die Ränder des Vorgangs Aufruf Diagramms aggregiert. Wir zählen nun, wie viele `T` Gates zum Implementieren des `CCNOT` Vorgangs benötigt werden. 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Verwenden des "primitive"-Vorgangs C# Zählers innerhalb eines Programms

Um zu überprüfen, ob `CCNOT` tatsächlich 7 `T` Gates erfordert und `ApplySampleWithCCNOT` 8 `T` Gates ausführt, können wir C# den folgenden Code verwenden:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Der erste Teil des Programms führt `ApplySampleWithCCNOT`aus. Im zweiten Teil verwenden wir die-Methode `QCTraceSimulator.GetMetric`, um die Anzahl von t Gates zu erhalten, die von `ApplySampleWithCCNOT`ausgeführt werden: 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Wenn `GetMetric` mit zwei Typparametern aufgerufen wird, wird der Wert der Metrik zurückgegeben, die einem angegebenen Aufruf Diagramm Rand zugeordnet ist. In unserem Beispiel Vorgang wird `Primitive.CCNOT` in `ApplySampleWithCCNOT` aufgerufen, und das Aufruf Diagramm enthält daher die Edge-`<Primitive.CCNOT, ApplySampleWithCCNOT>`. 

Um die Anzahl der verwendeten `CNOT` Gates zu erhalten, können Sie die folgende Zeile hinzufügen:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Schließlich können Sie Folgendes verwenden, um alle Statistiken auszugeben, die vom Gate-Counter im CSV-Format erfasst wurden:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Siehe auch ##

- Übersicht über den Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) für Quantum-Computer
