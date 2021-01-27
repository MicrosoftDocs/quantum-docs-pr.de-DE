---
title: Primitiver Vorgangs Counter-Quantum Development Kit
description: Erfahren Sie mehr über den "Microsoft QDK primitive Operation"-Vorgang, der mithilfe des Quantum-Ablauf Verfolgungs Simulators primitive Prozesse nachverfolgt, die von Vorgängen in einem Q# Programm
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 19ea3c1f5a91c00de4d3e435318bf4cf8cdd83be
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858599"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a>Quantum-Ablauf Verfolgungs Simulator: primitiver Vorgangs Counter

Der primitive Vorgangs Counter ist Teil des Quantum Development Kit- [quantumlaufverfolgungs-Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Sie zählt die Anzahl primitiver Prozesse, die von jedem in einem Quantum-Programm aufgerufenen Vorgang verwendet werden. 

Alle <xref:Microsoft.Quantum.Intrinsic> Vorgänge werden in Form von Single-Qubit-Drehungen, T-Vorgängen, Single-Qubit-Clifford-Vorgängen, CNOT-Vorgängen und Messungen von Multi-Qubit--Observables ausgedrückt. Der primitive Vorgangs Vergleich aggregiert und sammelt Statistiken über alle Ränder des [Aufruf Diagramms](https://en.wikipedia.org/wiki/Call_graph)des Vorgangs.

## <a name="invoking-the-primitive-operation-counter"></a>Aufruf des primitiven Vorgangs Zählers

Sie müssen eine- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> Instanz erstellen, die `UsePrimitiveOperationsCounter` -Eigenschaft auf **true** festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen, um den Quantum-Ablauf Verfolgungs Simulator mit dem Wert für den primitiven Vorgang auszuführen.

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a>Verwendung des primitiven Vorgangs Zählers in einem c#-Host Programm

Das c#-Beispiel, das in diesem Abschnitt folgt, zählt, wie viele <xref:Microsoft.Quantum.Intrinsic.T> Vorgänge erforderlich sind, um den <xref:Microsoft.Quantum.Intrinsic.CCNOT> Vorgang basierend auf dem folgenden Q# Beispielcode zu implementieren:

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

Verwenden Sie den folgenden c#-Code, um zu überprüfen, ob `CCNOT` sieben `T` Vorgänge erforderlich sind und dass `ApplySampleWithCCNOT` acht `T` Vorgänge ausgeführt werden:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Der erste Teil des Programms wird ausgeführt `ApplySampleWithCCNOT` . Im zweiten Teil wird die- [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) Methode verwendet, um die Anzahl der Vorgänge abzurufen, die `T` von ausgeführt werden `ApplySampleWithCCNOT` : 

Wenn Sie `GetMetric` mit zwei Typparametern aufzurufen, wird der Wert der Metrik zurückgegeben, die einem angegebenen Aufruf Diagramm Rand zugeordnet ist. Im vorherigen Beispiel ruft das Programm den `Primitive.CCNOT` -Vorgang innerhalb von auf `ApplySampleWithCCNOT` . Daher enthält das Aufruf Diagramm den Edge `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

Um die Anzahl der `CNOT` verwendeten Vorgänge abzurufen, fügen Sie die folgende Zeile hinzu:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Zum Schluss können Sie mithilfe der folgenden Daten alle vom primitiven Betriebs Leistungs-Leistungsdaten erfassten Statistiken im CSV-Format ausgeben:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Siehe auch

- Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.
- Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API-Referenz.