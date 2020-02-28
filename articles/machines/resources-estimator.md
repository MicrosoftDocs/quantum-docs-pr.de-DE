---
title: Ressourcenschätzung für Quantum Development Kit
description: 'Erfahren Sie mehr über die Ressourcenschätzung, mit der die Ressourcen geschätzt werden, die zum Ausführen einer bestimmten Instanz eines Q #-Vorgangs auf einem Quantum-Computer erforderlich sind.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 37c901e5a861f0e8a10cdc911ad1d84ddd3e6e00
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907051"
---
# <a name="the-resourcesestimator-target-machine"></a><span data-ttu-id="e4b81-103">Der resourcesestimator-Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="e4b81-103">The ResourcesEstimator Target Machine</span></span>

<span data-ttu-id="e4b81-104">Wie der Name schon sagt, schätzt der `ResourcesEstimator` die Ressourcen, die erforderlich sind, um eine bestimmte Instanz eines Q #-Vorgangs auf einem Quantum-Computer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e4b81-104">As the name implies, the `ResourcesEstimator` estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>
<span data-ttu-id="e4b81-105">Dies wird erreicht, indem der Quantum-Vorgang ausgeführt wird, ohne den Zustand eines Quantum-Computers zu simulieren. aus diesem Grund können Ressourcen für Q #-Vorgänge geschätzt werden, die Tausende von Qubits verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4b81-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it can estimate resources for Q# operations that use thousands of qubits.</span></span>

## <a name="usage"></a><span data-ttu-id="e4b81-106">Verwendung</span><span class="sxs-lookup"><span data-stu-id="e4b81-106">Usage</span></span>

<span data-ttu-id="e4b81-107">Der `ResourcesEstimator` ist nur ein anderer Typ von Zielcomputer und kann daher verwendet werden, um einen beliebigen Q #-Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e4b81-107">The `ResourcesEstimator` is just another type of target machine, thus it can be used to run any Q# operation.</span></span> 

<span data-ttu-id="e4b81-108">Erstellen Sie wie andere Zielcomputer eine-Instanz, C# um Sie auf einem Host Programm zu verwenden, und übergeben Sie Sie als ersten Parameter der `Run`-Methode des Vorgangs:</span><span class="sxs-lookup"><span data-stu-id="e4b81-108">As other target machines, to use it on a C# host program create an instance and pass it as the first parameter of the operation's `Run` method:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

<span data-ttu-id="e4b81-109">Wie das Beispiel zeigt, stellt die `ResourcesEstimator` eine `ToTSV()` Methode zum Generieren einer Tabelle mit "Tabulator getrennten Werten" (TSV) bereit, die in einer Datei gespeichert oder zur Analyse in die Konsole geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4b81-109">As the example shows, the `ResourcesEstimator` provides a `ToTSV()` method to generate a table with tab-seperated-values (TSV) that can be saved into a file or written to the console for analysis.</span></span> <span data-ttu-id="e4b81-110">Die Ausgabe des obigen Programms sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="e4b81-110">The output of the above program should look something like this:</span></span>

```Output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> <span data-ttu-id="e4b81-111">Der `ResourcesEstimator` setzt seine Berechnungen bei jeder Ausführung nicht zurück. wenn dieselbe Instanz verwendet wird, um einen anderen Vorgang auszuführen, wird die Aggregation der Anzahl vorhandener Ergebnisse beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e4b81-111">The `ResourcesEstimator` does not reset its calculations on every run, if the same instance is used to execute another operation it will keep aggregating counts on top of existing results.</span></span>
> <span data-ttu-id="e4b81-112">Wenn Sie Berechnungen zwischen den Ausführungen zurücksetzen müssen, erstellen Sie für jede Ausführung eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="e4b81-112">If you need to reset calculations between runs, create a new instance for every execution.</span></span>


## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="e4b81-113">Programm gesteuertes Abrufen der geschätzten Daten</span><span class="sxs-lookup"><span data-stu-id="e4b81-113">Programmatically Retrieving the Estimated Data</span></span>

<span data-ttu-id="e4b81-114">Zusätzlich zu einer TSV-Tabelle können die geschätzten Ressourcen Programm gesteuert über die `Data`-Eigenschaft des `ResourcesEstimator`abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e4b81-114">In addition to a TSV table, the resources estimated can be retrieved programmatically via the `ResourcesEstimator`'s `Data` property.</span></span> <span data-ttu-id="e4b81-115">`Data` stellt eine `System.DataTable` Instanz mit zwei Spalten bereit: `Metric` und `Sum`, indiziert durch die metriknamen.</span><span class="sxs-lookup"><span data-stu-id="e4b81-115">`Data` provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics names.</span></span>

<span data-ttu-id="e4b81-116">Der folgende Code zeigt, wie Sie die Gesamtzahl der `QubitClifford`, `T` und `CNOT` Gates abrufen und ausdrucken, die von einem Q #-Vorgang verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="e4b81-116">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` gates used by a Q# operation:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a><span data-ttu-id="e4b81-117">Gemeldete Metriken</span><span class="sxs-lookup"><span data-stu-id="e4b81-117">Metrics Reported</span></span>

<span data-ttu-id="e4b81-118">Im folgenden finden Sie eine Liste der Metriken, die vom `ResourcesEstimator`geschätzt werden:</span><span class="sxs-lookup"><span data-stu-id="e4b81-118">The following is the list of metrics estimated by the `ResourcesEstimator`:</span></span>

* <span data-ttu-id="e4b81-119">__CNOT__: die Anzahl der ausgeführten Gates (auch als kontrollierte Pauli X Gate bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="e4b81-119">__CNOT__: The count of CNOT (also known as the Controlled Pauli X gate) gates executed.</span></span>
* <span data-ttu-id="e4b81-120">__Qubitclifford__: die Anzahl der einzelnen Qubit Clifford-und Pauli-Gates, die ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="e4b81-120">__QubitClifford__: The count of any single qubit Clifford and Pauli gates executed.</span></span>
* <span data-ttu-id="e4b81-121">__Measure__: die Anzahl der ausgeführten Messungen.</span><span class="sxs-lookup"><span data-stu-id="e4b81-121">__Measure__:  The count of any measurements executed.</span></span>
* <span data-ttu-id="e4b81-122">__R__: die Anzahl der ausgeführten einzelnen Qubit-Drehungen, ausgenommen T, Clifford und Pauli Gates.</span><span class="sxs-lookup"><span data-stu-id="e4b81-122">__R__: The count of any single qubit rotations executed, excluding T, Clifford and Pauli gates.</span></span>
* <span data-ttu-id="e4b81-123">__T__: die Anzahl der t-Gates und ihre konjugierte, einschließlich t Gate, T_x = h. T. h und T_y = HY. T. HY, ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e4b81-123">__T__: The count of T gates and their conjugates, including the T gate, T_x = H.T.H, and T_y = Hy.T.Hy, executed.</span></span>
* <span data-ttu-id="e4b81-124">__Tiefe__: Tiefe der vom Q #-Vorgang ausgeführten Quantum-Leitung.</span><span class="sxs-lookup"><span data-stu-id="e4b81-124">__Depth__: Depth of the quantum circuit executed by the Q# operation.</span></span> <span data-ttu-id="e4b81-125">Standardmäßig werden nur T Gates in der Tiefe gezählt. Weitere Informationen finden Sie unter [tiefen Zähler](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) .</span><span class="sxs-lookup"><span data-stu-id="e4b81-125">By default, only T gates are counted in the depth, see [depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) for details.</span></span>
* <span data-ttu-id="e4b81-126">__Width__: maximale Anzahl von Qubits, die während der Ausführung des Q #-Vorgangs zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e4b81-126">__Width__: Maximum number of qubits allocated during the execution of the Q# operation.</span></span>
* <span data-ttu-id="e4b81-127">__Borrowedwidth__: maximale Anzahl von im Q #-Vorgang geliehenen Qubits.</span><span class="sxs-lookup"><span data-stu-id="e4b81-127">__BorrowedWidth__: Maximum number of qubits borrowed inside the Q# operation.</span></span>


## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="e4b81-128">Angeben der Wahrscheinlichkeit für Ergebnisse von Messungen</span><span class="sxs-lookup"><span data-stu-id="e4b81-128">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="e4b81-129"><xref:microsoft.quantum.intrinsic.assertprob> aus dem <xref:microsoft.quantum.intrinsic>-Namespace kann verwendet werden, um Informationen über die erwartete Wahrscheinlichkeit einer Messung bereitzustellen, um die Ausführung des Q #-Programms zu fördern.</span><span class="sxs-lookup"><span data-stu-id="e4b81-129"><xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace can be used to provide information about the expected probability of a measurement to help drive the execution of the Q# program.</span></span> <span data-ttu-id="e4b81-130">Das folgende Beispiel veranschaulicht dies:</span><span class="sxs-lookup"><span data-stu-id="e4b81-130">The following example illustrates this:</span></span>

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

<span data-ttu-id="e4b81-131">Wenn die `ResourcesEstimator` `AssertProb`, wird festgestellt, dass das Messen `PauliZ` auf `source` und `q` das Ergebnis `Zero` mit der Wahrscheinlichkeit 0,5 erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="e4b81-131">When the `ResourcesEstimator` encounters `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="e4b81-132">Wenn Sie später `M` ausgeführt wird, werden die aufgezeichneten Werte der Ergebnis Wahrscheinlichkeiten gefunden, und `M` gibt `Zero` oder `One` mit der Wahrscheinlichkeit 0,5 zurück.</span><span class="sxs-lookup"><span data-stu-id="e4b81-132">When it executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span>


## <a name="see-also"></a><span data-ttu-id="e4b81-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4b81-133">See also</span></span>

<span data-ttu-id="e4b81-134">Der `ResourcesEstimator` basiert auf dem Quantum-Computer-Ablauf [Verfolgungs Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), der einen umfassenderen Satz an Metriken, die Möglichkeit zum Melden von Metriken für das vollständige Aufruf Diagramm und Features wie die unter [schiedliche Eingabe](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) Prüfung bereitstellt, um Fehler in Q #-Programmen zu finden.</span><span class="sxs-lookup"><span data-stu-id="e4b81-134">The `ResourcesEstimator` is built on top of the quantum computer [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics, the ability to report metrics on the full call-graph, and features like [distinct inputs checker](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) to help find bugs on Q# programs.</span></span> <span data-ttu-id="e4b81-135">Weitere Informationen finden Sie in der Dokumentation des Ablauf [Verfolgungs Simulators](xref:microsoft.quantum.machines.qc-trace-simulator.intro) .</span><span class="sxs-lookup"><span data-stu-id="e4b81-135">Please refer to the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) documentation for more information.</span></span>

