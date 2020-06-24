---
title: Vollständiger Zustands Simulator
description: 'Erfahren Sie, wie Sie Ihre Q #-Programme auf dem Microsoft Quantum Development Kit vollständigen Status Simulator ausführen.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274946"
---
# <a name="quantum-development-kit-full-state-simulator"></a><span data-ttu-id="c69c2-103">Vollständiger Status Simulator für das Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="c69c2-103">Quantum Development Kit Full State Simulator</span></span>

<span data-ttu-id="c69c2-104">Das Quantum Development Kit bietet einen vollständigen Quantum-Simulator ähnlich dem [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) von Microsoft Research.</span><span class="sxs-lookup"><span data-stu-id="c69c2-104">The Quantum Development Kit provides a full state quantum simulator similar to [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) from Microsoft Research.</span></span>
<span data-ttu-id="c69c2-105">Dieser Simulator kann zum Ausführen und Debuggen von in Q # geschriebenen Quantenalgorithmen auf dem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c69c2-105">This simulator can be used to execute and debug quantum algorithms written in Q# on your computer.</span></span>

<span data-ttu-id="c69c2-106">Dieser Quantum-Simulator wird über die-Klasse verfügbar gemacht `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="c69c2-106">This quantum simulator is exposed via the `QuantumSimulator` class.</span></span> <span data-ttu-id="c69c2-107">Um den Simulator zu verwenden, erstellen Sie einfach eine Instanz dieser Klasse, und übergeben Sie Sie an die- `Run` Methode des Quantum-Vorgangs, den Sie zusammen mit den restlichen Parametern ausführen möchten:</span><span class="sxs-lookup"><span data-stu-id="c69c2-107">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a><span data-ttu-id="c69c2-108">IDisposable</span><span class="sxs-lookup"><span data-stu-id="c69c2-108">IDisposable</span></span>

<span data-ttu-id="c69c2-109">Die- `QuantumSimulator` Klasse implementiert <xref:System.IDisposable> . daher `Dispose` sollte die-Methode aufgerufen werden, sobald die Instanz des Simulators nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c69c2-109">The `QuantumSimulator` class implements <xref:System.IDisposable>, thus the `Dispose` method should be called once the instance of the simulator is not used anymore.</span></span> <span data-ttu-id="c69c2-110">Die beste Möglichkeit hierfür ist das Einschließen des Simulators innerhalb einer- `using` Anweisung, wie im obigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c69c2-110">The best way to do this is to wrap the simulator within a `using` statement, as in the example above.</span></span>

## <a name="seed"></a><span data-ttu-id="c69c2-111">Seed</span><span class="sxs-lookup"><span data-stu-id="c69c2-111">Seed</span></span>

<span data-ttu-id="c69c2-112">`QuantumSimulator`Verwendet einen Zufallszahlengenerator, um die Quantum-Zufälligkeit zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="c69c2-112">The `QuantumSimulator` uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="c69c2-113">Zu Testzwecken ist es manchmal sinnvoll, deterministische Ergebnisse zu haben.</span><span class="sxs-lookup"><span data-stu-id="c69c2-113">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="c69c2-114">Dies kann erreicht werden, indem ein Ausgangswert für den Zufallszahlengenerator im `QuantumSimulator` Konstruktor des Konstruktors über den-Parameter bereitgestellt wird `randomNumberGeneratorSeed` :</span><span class="sxs-lookup"><span data-stu-id="c69c2-114">This can be accomplished by providing a seed for the random number generator in the `QuantumSimulator`'s constructor via the `randomNumberGeneratorSeed` parameter:</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a><span data-ttu-id="c69c2-115">Threads</span><span class="sxs-lookup"><span data-stu-id="c69c2-115">Threads</span></span>

<span data-ttu-id="c69c2-116">`QuantumSimulator`Verwendet [OpenMP](http://www.openmp.org/) , um die erforderliche lineare Algebra zu parallelisieren.</span><span class="sxs-lookup"><span data-stu-id="c69c2-116">The `QuantumSimulator` uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="c69c2-117">OpenMP verwendet standardmäßig alle verfügbaren Hardwarethreads, weshalb Programme mit wenigen Qubits häufig langsam ausgeführt werden, stellt die Koordination die tatsächliche Arbeit in den Schatten.</span><span class="sxs-lookup"><span data-stu-id="c69c2-117">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="c69c2-118">Dies kann korrigiert werden, indem die Umgebungsvariable `OMP_NUM_THREADS` auf eine kleine Zahl festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c69c2-118">This can be fixed by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="c69c2-119">Als grobe Faustregel gilt, dass 1 Thread für etwa 4 Qubits genügt und dann für jeden weiteren Qubit ein weiterer Thread benötigt wird. Dies hängt jedoch stark von Ihrem Algorithmus ab.</span><span class="sxs-lookup"><span data-stu-id="c69c2-119">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

