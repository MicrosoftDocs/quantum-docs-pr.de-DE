---
title: Quantum Development Kit-vollständiger Status Simulator | Microsoft-Dokumentation
description: Übersicht über den voll Zustands Simulator von Microsoft Quantum Development Kit
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: ab0e65765d27e301a59948d7c02105a523022e68
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184677"
---
# <a name="quantum-development-kit-full-state-simulator"></a><span data-ttu-id="ebe87-103">Vollständiger Status Simulator für das Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="ebe87-103">Quantum Development Kit Full State Simulator</span></span>

<span data-ttu-id="ebe87-104">Das Quantum Development Kit bietet einen vollständigen Quantum-Simulator ähnlich dem [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) von Microsoft Research.</span><span class="sxs-lookup"><span data-stu-id="ebe87-104">The Quantum Development Kit provides a full state quantum simulator similar to [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) from Microsoft Research.</span></span>
<span data-ttu-id="ebe87-105">Dieser Simulator kann zum Ausführen und Debuggen von in Q # geschriebenen Quantenalgorithmen auf dem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebe87-105">This simulator can be used to execute and debug quantum algorithms written in Q# on your computer.</span></span>

<span data-ttu-id="ebe87-106">Dieser Quantum-Simulator wird über die `QuantumSimulator`-Klasse verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="ebe87-106">This quantum simulator is exposed via the `QuantumSimulator` class.</span></span> <span data-ttu-id="ebe87-107">Um den Simulator zu verwenden, erstellen Sie einfach eine Instanz dieser Klasse, und übergeben Sie Sie an die `Run`-Methode des Quantum-Vorgangs, den Sie zusammen mit den restlichen Parametern ausführen möchten:</span><span class="sxs-lookup"><span data-stu-id="ebe87-107">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a><span data-ttu-id="ebe87-108">IDisposable</span><span class="sxs-lookup"><span data-stu-id="ebe87-108">IDisposable</span></span>

<span data-ttu-id="ebe87-109">Die `QuantumSimulator`-Klasse implementiert <xref:System.IDisposable>. Daher sollte die `Dispose`-Methode aufgerufen werden, sobald die Instanz des Simulators nicht mehr verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ebe87-109">The `QuantumSimulator` class implements <xref:System.IDisposable>, thus the `Dispose` method should be called once the instance of the simulator is not used anymore.</span></span> <span data-ttu-id="ebe87-110">Die beste Möglichkeit hierfür ist das Einschließen des Simulators innerhalb einer `using`-Anweisung, wie im obigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebe87-110">The best way to do this is to wrap the simulator within a `using` statement, as in the example above.</span></span>

## <a name="seed"></a><span data-ttu-id="ebe87-111">säen</span><span class="sxs-lookup"><span data-stu-id="ebe87-111">Seed</span></span>

<span data-ttu-id="ebe87-112">Der `QuantumSimulator` verwendet einen Zufallszahlengenerator, um die Quantum-Zufälligkeit zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="ebe87-112">The `QuantumSimulator` uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="ebe87-113">Zu Testzwecken ist es manchmal sinnvoll, deterministische Ergebnisse zu haben.</span><span class="sxs-lookup"><span data-stu-id="ebe87-113">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="ebe87-114">Dies kann erreicht werden, indem ein Ausgangswert für den Zufallszahlengenerator im Konstruktor der `QuantumSimulator`über den Parameter "`randomNumberGeneratorSeed`" bereitgestellt wird:</span><span class="sxs-lookup"><span data-stu-id="ebe87-114">This can be accomplished by providing a seed for the random number generator in the `QuantumSimulator`'s constructor via the `randomNumberGeneratorSeed` parameter:</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a><span data-ttu-id="ebe87-115">Threads</span><span class="sxs-lookup"><span data-stu-id="ebe87-115">Threads</span></span>

<span data-ttu-id="ebe87-116">Der `QuantumSimulator` verwendet [OpenMP](http://www.openmp.org/) , um die erforderliche lineare Algebra zu parallelisieren.</span><span class="sxs-lookup"><span data-stu-id="ebe87-116">The `QuantumSimulator` uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="ebe87-117">Standardmäßig verwendet OpenMP alle verfügbaren Hardwarethreads, was bedeutet, dass Programme mit einer kleinen Anzahl von Qubits häufig langsam ausgeführt werden, da die eigentliche Arbeit durch die erforderliche Koordination in den Mittelpunkt gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ebe87-117">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="ebe87-118">Dies kann korrigiert werden, indem die Umgebungsvariable `OMP_NUM_THREADS` auf eine kleine Zahl festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="ebe87-118">This can be fixed by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="ebe87-119">Als sehr grobe Faustregel ist 1 Thread für bis zu ungefähr 4 Qubits geeignet, und dann ist ein zusätzlicher Thread pro Qubit gut, obwohl dies stark von Ihrem Algorithmus abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="ebe87-119">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

