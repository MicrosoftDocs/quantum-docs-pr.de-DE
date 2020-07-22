---
title: Full State Quantum Simulator-Quantum Development Kit
description: 'Erfahren Sie, wie Sie Ihre Q #-Programme auf dem Microsoft Quantum Development Kit vollständigen Status Simulator ausführen.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: 563fdbd2a45461d112e4c46651eddd75c6fc3db2
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871177"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a><span data-ttu-id="75da0-103">Vollständiger Status Simulator für das Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="75da0-103">Quantum Development Kit (QDK) full state simulator</span></span>

<span data-ttu-id="75da0-104">Das QDK bietet einen vollständigen Status Simulator, der einen Quantum-Computer auf dem lokalen Computer simuliert.</span><span class="sxs-lookup"><span data-stu-id="75da0-104">The QDK provides a full state simulator that simulates a quantum machine on your local computer.</span></span> <span data-ttu-id="75da0-105">Mithilfe des vollständigen Zustands Simulators können Sie in f # geschriebene Quantum-Algorithmen ausführen und Debuggen, wobei bis zu 30 Qubits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="75da0-105">You can use the full state simulator to run and debug quantum algorithms written in Q#, utilizing up to 30 qubits.</span></span> <span data-ttu-id="75da0-106">Der vollständige Zustands Simulator ähnelt dem Quantum-Simulator, der in der [Liq $ UI | \rangle $](http://stationq.github.io/Liquid/) Platform von Microsoft Research verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75da0-106">The full state simulator is similar to the quantum simulator used in the  [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) platform from Microsoft Research.</span></span>

## <a name="invoking-and-running-the-full-state-simulator"></a><span data-ttu-id="75da0-107">Aufrufen und Ausführen des vollständigen Zustands Simulators</span><span class="sxs-lookup"><span data-stu-id="75da0-107">Invoking and running the full state simulator</span></span>

<span data-ttu-id="75da0-108">Sie machen den vollständigen Zustands Simulator über die- `QuantumSimulator` Klasse verfügbar.</span><span class="sxs-lookup"><span data-stu-id="75da0-108">You expose the full state simulator via the `QuantumSimulator` class.</span></span> <span data-ttu-id="75da0-109">Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q #-Programms](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="75da0-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-simulator-from-c"></a><span data-ttu-id="75da0-110">Aufrufen des Simulators von C #</span><span class="sxs-lookup"><span data-stu-id="75da0-110">Invoking the simulator from C#</span></span>

<span data-ttu-id="75da0-111">Erstellen Sie eine Instanz der `QuantumSimulator` -Klasse, und übergeben Sie Sie dann an die- `Run` Methode eines Quantum-Vorgangs zusammen mit allen weiteren Parametern.</span><span class="sxs-lookup"><span data-stu-id="75da0-111">Create an instance of the `QuantumSimulator` class and then pass it to the `Run` method of a quantum operation, along with any additional parameters.</span></span>
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

<span data-ttu-id="75da0-112">Da die- `QuantumSimulator` Klasse die- <xref:System.IDisposable> Schnittstelle implementiert, muss die-Methode aufgerufen werden, `Dispose` Wenn die Instanz des Simulators nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="75da0-112">Because the `QuantumSimulator` class implements the <xref:System.IDisposable> interface, you must call the `Dispose` method once you do not need the instance of the simulator anymore.</span></span> <span data-ttu-id="75da0-113">Die beste Möglichkeit hierfür ist das Einschließen der simulatordeklaration und der Vorgänge in einer [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) -Anweisung, die automatisch die- `Dispose` Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="75da0-113">The best way to do this is to wrap the simulator declaration and operations within a [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) statement, which automatically calls the `Dispose` method.</span></span>

### <a name="invoking-the-simulator-from-python"></a><span data-ttu-id="75da0-114">Aufrufen des Simulators aus python</span><span class="sxs-lookup"><span data-stu-id="75da0-114">Invoking the simulator from Python</span></span>

<span data-ttu-id="75da0-115">Verwenden Sie die Methode " [simulieren ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) " aus der q #-Python-Bibliothek mit dem importierten q #-Vorgang:</span><span class="sxs-lookup"><span data-stu-id="75da0-115">Use the [simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Q# Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a><span data-ttu-id="75da0-116">Aufrufen des Simulators über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="75da0-116">Invoking the simulator from the command line</span></span>

<span data-ttu-id="75da0-117">Wenn ein Q #-Programm über die Befehlszeile ausgeführt wird, ist der vollständige Zustands Simulator der Standardziel Computer.</span><span class="sxs-lookup"><span data-stu-id="75da0-117">When running a Q# program from the command line, the full state simulator is the default target machine.</span></span> <span data-ttu-id="75da0-118">Optional können Sie den Parameter **--Simulator** (oder **-s** ) verwenden, um den gewünschten Zielcomputer anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75da0-118">Optionally, you can use the **--simulator** (or **-s** shortcut) parameter to specify the desired target machine.</span></span> <span data-ttu-id="75da0-119">Beide der folgenden Befehle führen ein Programm mithilfe des vollständigen Zustands Simulators aus.</span><span class="sxs-lookup"><span data-stu-id="75da0-119">Both of the following commands run a program using the full state simulator.</span></span> 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a><span data-ttu-id="75da0-120">Aufrufen des Simulators aus juptyer Notebooks</span><span class="sxs-lookup"><span data-stu-id="75da0-120">Invoking the simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="75da0-121">Verwenden [Sie den](xref:microsoft.quantum.iqsharp.magic-ref.simulate) Befehl "IQ # Magic", um den Q #-Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="75da0-121">Use the IQ# magic command [%simulate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a><span data-ttu-id="75da0-122">Seeding des Simulators</span><span class="sxs-lookup"><span data-stu-id="75da0-122">Seeding the simulator</span></span>

<span data-ttu-id="75da0-123">Standardmäßig verwendet der vollständige Zustands Simulator einen Zufallszahlengenerator, um die Quantum-Zufälligkeit zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="75da0-123">By default, the full state simulator uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="75da0-124">Zu Testzwecken ist es manchmal sinnvoll, deterministische Ergebnisse zu haben.</span><span class="sxs-lookup"><span data-stu-id="75da0-124">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="75da0-125">In einem c#-Programm können Sie dies erreichen, indem Sie über den-Parameter einen Ausgangswert für den Zufallszahlengenerator im `QuantumSimulator` Konstruktor bereitstellen `randomNumberGeneratorSeed` .</span><span class="sxs-lookup"><span data-stu-id="75da0-125">In a C# program, you can accomplish this by providing a seed for the random number generator in the `QuantumSimulator` constructor via the `randomNumberGeneratorSeed` parameter.</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a><span data-ttu-id="75da0-126">Konfigurieren von Threads</span><span class="sxs-lookup"><span data-stu-id="75da0-126">Configuring threads</span></span>

<span data-ttu-id="75da0-127">Der vollständige Zustands Simulator verwendet [OpenMP](http://www.openmp.org/) , um die erforderliche lineare Algebra zu parallelisieren.</span><span class="sxs-lookup"><span data-stu-id="75da0-127">The full state simulator uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="75da0-128">Standardmäßig verwendet OpenMP alle verfügbaren Hardwarethreads, was bedeutet, dass Programme mit einer kleinen Anzahl von Qubits häufig langsam ausgeführt werden, da die erforderliche Koordination die eigentliche Arbeit vergrenzt.</span><span class="sxs-lookup"><span data-stu-id="75da0-128">By default, OpenMP uses all available hardware threads, which means that programs with small numbers of qubits often runs slowly because the coordination that is required dwarfs the actual work.</span></span> <span data-ttu-id="75da0-129">Sie können dieses Problem beheben, indem Sie die Umgebungsvariable `OMP_NUM_THREADS` auf eine kleine Zahl festlegen.</span><span class="sxs-lookup"><span data-stu-id="75da0-129">You can fix this by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="75da0-130">Konfigurieren Sie als Faustregel einen Thread für bis zu vier Qubits und dann einen zusätzlichen Thread pro Qubit.</span><span class="sxs-lookup"><span data-stu-id="75da0-130">As a rule of thumb, configure one thread for up to four qubits, and then one additional thread per qubit.</span></span> <span data-ttu-id="75da0-131">Möglicherweise müssen Sie die Variable abhängig von Ihrem Algorithmus anpassen.</span><span class="sxs-lookup"><span data-stu-id="75da0-131">You might need to adjust the variable depending on your algorithm.</span></span>

## <a name="see-also"></a><span data-ttu-id="75da0-132">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="75da0-132">See also</span></span>

- [<span data-ttu-id="75da0-133">Quantum-Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="75da0-133">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="75da0-134">Quantum-zu-ffoli-Simulator</span><span class="sxs-lookup"><span data-stu-id="75da0-134">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="75da0-135">Quantum-Ablauf Verfolgungs Simulator</span><span class="sxs-lookup"><span data-stu-id="75da0-135">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)