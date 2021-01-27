---
title: Width Counter-Quantum Development Kit
description: Erfahren Sie mehr über den Microsoft QDK Width-Zähler, der den Quantum-Ablauf Verfolgungs Simulator verwendet, um die Anzahl der von Vorgängen in einem Programm zugewiesenen und zugeordneten Qubits zu zählen Q# .
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: e9a526ee1440544aace922bd83c6ea39cb83c1ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858578"
---
# <a name="quantum-trace-simulator-width-counter"></a><span data-ttu-id="b199e-103">Quantum-Ablauf Verfolgungs Simulator: width-Counter</span><span class="sxs-lookup"><span data-stu-id="b199e-103">Quantum trace simulator: width counter</span></span>

<span data-ttu-id="b199e-104">Der Width-Counter ist Teil des Quantum Development Kit- [quantumlaufverfolgungssimulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="b199e-104">The width counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="b199e-105">Damit können Sie die Anzahl von Qubits zählen, die von den einzelnen Vorgängen in einem Programm zugeordnet und abgerufen werden Q# .</span><span class="sxs-lookup"><span data-stu-id="b199e-105">You can use it to count the number of qubits allocated and borrowed by each operation in a Q# program.</span></span> <span data-ttu-id="b199e-106">Einige primitive Vorgänge können zusätzliche Qubits zuordnen, z. b. durch Multiplizieren von kontrollierten `X` Vorgängen oder kontrollierten `T` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="b199e-106">Some primitive operations can allocate extra qubits, for example, multiply controlled `X` operations or controlled `T` operations.</span></span>

## <a name="invoking-the-width-counter"></a><span data-ttu-id="b199e-107">Aufrufen des breiten Zählers</span><span class="sxs-lookup"><span data-stu-id="b199e-107">Invoking the width counter</span></span>

<span data-ttu-id="b199e-108">Zum Ausführen des Quantum-Ablauf Verfolgungs Simulators mit dem width-Wert müssen Sie eine <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> -Instanz erstellen, die `UseWidthCounter` -Eigenschaft auf **true** festlegen und dann eine neue- <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> Instanz mit `QCTraceSimulatorConfiguration` als Parameter erstellen.</span><span class="sxs-lookup"><span data-stu-id="b199e-108">To run the quantum trace simulator with the width counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseWidthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a><span data-ttu-id="b199e-109">Verwenden des Width-Zählers in einem c#-Host Programm</span><span class="sxs-lookup"><span data-stu-id="b199e-109">Using the width counter in a C# host program</span></span>

<span data-ttu-id="b199e-110">Das c#-Beispiel, das in diesem Abschnitt folgt, berechnet die Anzahl der zusätzlichen Qubits, die von der Implementierung eines Multiplikations gesteuerten Vorgangs zugeordnet werden <xref:Microsoft.Quantum.Intrinsic.X> , basierend auf dem folgenden Q# Beispielcode:</span><span class="sxs-lookup"><span data-stu-id="b199e-110">The C# example that follows in this section computes the number of extra qubits allocated by the implementation of a multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

<span data-ttu-id="b199e-111">Der Vorgang zum Multiplizieren <xref:Microsoft.Quantum.Intrinsic.X> von Aktionen wirkt sich auf insgesamt fünf Qubits aus, ordnet zwei [hilfskbits](xref:microsoft.quantum.glossary#ancilla)zu und hat eine Eingabe Breite von **5**.</span><span class="sxs-lookup"><span data-stu-id="b199e-111">The multiply controlled <xref:Microsoft.Quantum.Intrinsic.X> operation acts on a total of five qubits, allocates two [ancillary qubits](xref:microsoft.quantum.glossary#ancilla), and has an input width of **5**.</span></span> <span data-ttu-id="b199e-112">Verwenden Sie das folgende c#-Programm, um die Anzahl zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="b199e-112">Use the following C# program to verify the counts:</span></span>

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

<span data-ttu-id="b199e-113">Der erste Teil des Programms führt den `ApplyMultiControlledX` Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="b199e-113">The first part of the program runs the `ApplyMultiControlledX` operation.</span></span> <span data-ttu-id="b199e-114">Im zweiten Teil wird die- [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) Methode verwendet, um die Anzahl der zugeordneten Qubits abzurufen, sowie die Anzahl der Qubits, die der `Controlled X` Vorgang als Eingabe empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="b199e-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of allocated qubits as well as the number of qubits that the `Controlled X` operation received as input.</span></span> 

<span data-ttu-id="b199e-115">Zum Schluss können Sie alle durch den Wert "width" gesammelten Statistiken im CSV-Format im CSV-Format ausgeben, indem Sie Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="b199e-115">Finally, you can output all the statistics collected by the width counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="b199e-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b199e-116">See also</span></span>

- <span data-ttu-id="b199e-117">Übersicht über den Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="b199e-117">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="b199e-118">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="b199e-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="b199e-119">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="b199e-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="b199e-120">Die <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="b199e-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API reference.</span></span>
