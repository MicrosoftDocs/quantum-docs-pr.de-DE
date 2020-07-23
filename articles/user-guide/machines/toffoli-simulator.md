---
title: Quantum-zu-ffoli-Simulator-Quantum Development Kit
description: Erfahren Sie mehr über den Microsoft QDK-Simulator für den Einsatz von Microsoft QDK, einen speziellen Zweck-Quantum-Simulator, der mit Millionen von Qubits verwendet werden kann
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: a6ceee592e628215511ec83475d9e25bf54674f7
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870616"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a><span data-ttu-id="d3493-103">Quantum Development Kit (QDK)-Simulator (QDK)</span><span class="sxs-lookup"><span data-stu-id="d3493-103">Quantum Development Kit (QDK) Toffoli simulator</span></span>

<span data-ttu-id="d3493-104">Der simulatorqdk-Simulator ist ein Zweck gesteuerter Simulator mit eingeschränktem Bereich und unterstützt nur `X` , `CNOT` und mehr gesteuerte `X` Quantum-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d3493-104">The QDK Toffoli simulator is a special-purpose simulator with a limited scope and only supports `X`, `CNOT`, and multi-controlled `X` quantum operations.</span></span> <span data-ttu-id="d3493-105">Alle klassischen Logik und Berechnungen sind verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d3493-105">All classical logic and computations are available.</span></span>

<span data-ttu-id="d3493-106">Während der ""-und "deffoli"-Simulator mehr Funktionen als der [vollständige Zustands Simulator](xref:microsoft.quantum.machines.full-state-simulator)bietet, hat dies den Vorteil, dass viel mehr Qubits simuliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3493-106">While the Toffoli simulator is more restricted in functionality than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it has the advantage of being able to simulate far more qubits.</span></span> <span data-ttu-id="d3493-107">Der-Simulator kann mit Millionen von Qubits verwendet werden, während der vollständige Zustands Simulator auf ungefähr 30 Qubits beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="d3493-107">The Toffoli simulator can be used with millions of qubits, while the full state simulator is limited to about 30 qubits.</span></span> <span data-ttu-id="d3493-108">Dies ist beispielsweise bei Oracles nützlich, die Boolesche Funktionen auswerten. Sie können mit dem begrenzten Satz unterstützter Algorithmen implementiert und auf einer großen Anzahl von Qubits getestet werden.</span><span class="sxs-lookup"><span data-stu-id="d3493-108">This is useful, for example, with oracles that evaluate Boolean functions - they can be implemented using the limited set of supported algorithms and tested on a large number of qubits.</span></span>

## <a name="invoking-the-toffoli-simulator"></a><span data-ttu-id="d3493-109">Aufrufen des-Simulators "tyffoli"</span><span class="sxs-lookup"><span data-stu-id="d3493-109">Invoking the Toffoli simulator</span></span>

<span data-ttu-id="d3493-110">Der-Simulator wird über die-Klasse verfügbar gemacht `ToffoliSimulator` .</span><span class="sxs-lookup"><span data-stu-id="d3493-110">You expose the Toffoli simulator via the `ToffoliSimulator` class.</span></span> <span data-ttu-id="d3493-111">Weitere Informationen finden Sie unter [Möglichkeiten zum Ausführen eines Q #-Programms](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="d3493-111">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-toffoli-simulator-from-c"></a><span data-ttu-id="d3493-112">Aufrufen des-Simulators von C #</span><span class="sxs-lookup"><span data-stu-id="d3493-112">Invoking the Toffoli simulator from C#</span></span>

<span data-ttu-id="d3493-113">Wie bei anderen Ziel Computern erstellen Sie zunächst eine Instanz der `ToffoliSimulator` -Klasse und übergeben Sie dann als ersten Parameter der-Methode eines Vorgangs `Run` .</span><span class="sxs-lookup"><span data-stu-id="d3493-113">As with other target machines, you first create an instance of the `ToffoliSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="d3493-114">Beachten Sie, dass die-Klasse im Gegensatz zur- `QuantumSimulator` Klasse `ToffoliSimulator` die <xref:System.IDisposable> -Schnittstelle nicht implementiert, sodass Sie Sie nicht in eine-Anweisung einschließen müssen `using` .</span><span class="sxs-lookup"><span data-stu-id="d3493-114">Note that, unlike the `QuantumSimulator` class, the `ToffoliSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a><span data-ttu-id="d3493-115">Aufrufen des atffoli-Simulators aus python</span><span class="sxs-lookup"><span data-stu-id="d3493-115">Invoking the Toffoli simulator from Python</span></span>

<span data-ttu-id="d3493-116">Verwenden Sie die [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) -Methode aus der Python-Bibliothek mit dem importierten Q #-Vorgang:</span><span class="sxs-lookup"><span data-stu-id="d3493-116">Use the [toffoli_simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a><span data-ttu-id="d3493-117">Aufrufen des-Simulators von der Befehlszeile aus</span><span class="sxs-lookup"><span data-stu-id="d3493-117">Invoking the Toffoli simulator from the command line</span></span>

<span data-ttu-id="d3493-118">Wenn Sie ein Q #-Programm über die Befehlszeile ausführen, verwenden Sie den Parameter **--Simulator** (oder **-s** ), um den Bereitstellungs Zielcomputer für den ""-Simulator anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d3493-118">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the Toffoli simulator target machine.</span></span> <span data-ttu-id="d3493-119">Der folgende Befehl führt ein Programm mit der Ressourcenschätzung aus:</span><span class="sxs-lookup"><span data-stu-id="d3493-119">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a><span data-ttu-id="d3493-120">Aufrufen des-Simulators von juptyer Notebooks</span><span class="sxs-lookup"><span data-stu-id="d3493-120">Invoking the Toffoli simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="d3493-121">Verwenden [Sie den](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) Befehl "IQ # Magic", um den Q #-Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d3493-121">Use the IQ# magic command [%toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) to run the Q# operation.</span></span>

```
%toffoli myOperation
```

## <a name="supported-operations"></a><span data-ttu-id="d3493-122">Unterstützte Vorgänge</span><span class="sxs-lookup"><span data-stu-id="d3493-122">Supported operations</span></span>

<span data-ttu-id="d3493-123">Der Schalter "-Schalter" unterstützt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d3493-123">The Toffoli simulator supports:</span></span>

* <span data-ttu-id="d3493-124">Drehungen und exponentialweise, z. b. `R` und `Exp` , wenn der resultierende Vorgang `X` oder die Identitätsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="d3493-124">Rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation equals `X` or the identity matrix.</span></span>
* <span data-ttu-id="d3493-125">Messungen und [Assert](xref:microsoft.quantum.diagnostics.assertmeasurement) -Vorgänge, aber nur in der Pauli- `Z` Basis.</span><span class="sxs-lookup"><span data-stu-id="d3493-125">Measurement and [assert](xref:microsoft.quantum.diagnostics.assertmeasurement) operations, but only in the Pauli `Z` basis.</span></span> <span data-ttu-id="d3493-126">Beachten Sie, dass die Wahrscheinlichkeit eines Messvorgangs immer entweder **0** oder **1**ist. Es gibt keine Zufälligkeit im-Simulator von "".</span><span class="sxs-lookup"><span data-stu-id="d3493-126">Note that a measurement operation's probability is always either **0** or **1**; there is no randomness in the Toffoli simulator.</span></span>
* <span data-ttu-id="d3493-127">`DumpMachine`-und- `DumpRegister` Funktionen.</span><span class="sxs-lookup"><span data-stu-id="d3493-127">`DumpMachine` and `DumpRegister` functions.</span></span>
<span data-ttu-id="d3493-128">Beide Funktionen geben den aktuellen `Z` Status jedes Qubit aus, ein Qubit pro Zeile.</span><span class="sxs-lookup"><span data-stu-id="d3493-128">Both functions output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="specifying-the-number-of-qubits"></a><span data-ttu-id="d3493-129">Angeben der Anzahl von Qubits</span><span class="sxs-lookup"><span data-stu-id="d3493-129">Specifying the number of qubits</span></span>

<span data-ttu-id="d3493-130">Standardmäßig ordnet eine- `ToffoliSimulator` Instanz Speicherplatz für 65.536 Qubits zu.</span><span class="sxs-lookup"><span data-stu-id="d3493-130">By default, a `ToffoliSimulator` instance allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="d3493-131">Wenn für Ihren Algorithmus mehr Qubits erforderlich sind, können Sie die Qubit-Anzahl angeben, indem Sie dem Konstruktor einen Wert für den Parameter bereitstellen `qubitCount` .</span><span class="sxs-lookup"><span data-stu-id="d3493-131">If your algorithm requires more qubits than this, you can specify the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="d3493-132">Für jedes zusätzliche Qubit ist nur ein Byte Arbeitsspeicher erforderlich, sodass die Anzahl der benötigten Qubits nicht signifikant ist.</span><span class="sxs-lookup"><span data-stu-id="d3493-132">Each additional qubit requires only one byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="d3493-133">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d3493-133">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a><span data-ttu-id="d3493-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d3493-134">See also</span></span>

- [<span data-ttu-id="d3493-135">Quantum-Ressourcenschätzung</span><span class="sxs-lookup"><span data-stu-id="d3493-135">Quantum Resources Estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="d3493-136">Quantum-Ablauf Verfolgungs Simulator</span><span class="sxs-lookup"><span data-stu-id="d3493-136">Quantum Trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="d3493-137">Quantum-vollständiger Zustands Simulator</span><span class="sxs-lookup"><span data-stu-id="d3493-137">Quantum Full State simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 