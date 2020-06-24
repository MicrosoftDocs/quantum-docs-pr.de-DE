---
title: Quantum Development Kit-Simulator
description: Erfahren Sie mehr über den Microsoft QDK-Simulator für den Einsatz von Microsoft QDK, einen speziellen Zweck-Quantum-Simulator, der mit Millionen von Qubits verwendet werden kann
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275145"
---
# <a name="quantum-development-kit-toffoli-simulator"></a><span data-ttu-id="19f27-103">Quantum Development Kit-Simulator</span><span class="sxs-lookup"><span data-stu-id="19f27-103">Quantum Development Kit Toffoli Simulator</span></span>

<span data-ttu-id="19f27-104">Das Quantum Development Kit bietet einen deffoli-Simulator, bei dem es sich um einen Zweck Simulator handelt, mit dem Quantum-Algorithmen simuliert werden können, die auf x-, CNOT-und multigesteuerte X-Quantum-Vorgänge beschränkt sind (alle klassischen Logik und Berechnungen sind verfügbar).</span><span class="sxs-lookup"><span data-stu-id="19f27-104">The Quantum Development Kit provides a Toffoli simulator, which is a special-purpose simulator that can simulate quantum algorithms that are limited to X, CNOT, and multi-controlled X quantum operations (all classical logic and computations are available).</span></span>

<span data-ttu-id="19f27-105">Während der Vorgang "deffoli" in der Operation wesentlich eingeschränkter ist als der [vollständige Zustands Simulator](xref:microsoft.quantum.machines.full-state-simulator), kann er weitaus mehr Qubits simulieren.</span><span class="sxs-lookup"><span data-stu-id="19f27-105">While the Toffoli simulator is much more restricted in operation than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it can simulate far more qubits.</span></span>
<span data-ttu-id="19f27-106">Der-Simulator kann mit Millionen von Qubits verwendet werden, während der vollständige Zustands Simulator im Allgemeinen auf ungefähr 30 beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="19f27-106">The Toffoli simulator can be used with millions of qubits, while the full state simulator is generally limited to about 30.</span></span>
<span data-ttu-id="19f27-107">Es kann einen begrenzten Satz von Quantum-Algorithmen ausführen und Debuggen, die in Q # auf dem Computer geschrieben wurden. Beispielsweise können Oracles, die Boolesche Funktionen evaluieren, mithilfe dieser Gates implementiert werden. Diese werden daher bei einer großen Anzahl von Qubits mit diesem Simulator getestet.</span><span class="sxs-lookup"><span data-stu-id="19f27-107">It can execute and debug a limited set of quantum algorithms written in Q# on your computer; for instance, oracles that evaluate Boolean functions can be implemented using these gates and so tested on vary large numbers of qubits using this simulator.</span></span>

<span data-ttu-id="19f27-108">Dieser Quantum-Simulator wird über die-Klasse verfügbar gemacht `ToffoliSimulator` .</span><span class="sxs-lookup"><span data-stu-id="19f27-108">This quantum simulator is exposed via the `ToffoliSimulator` class.</span></span>
<span data-ttu-id="19f27-109">Um den Simulator zu verwenden, erstellen Sie einfach eine Instanz dieser Klasse, und übergeben Sie Sie an die- `Run` Methode des Quantum-Vorgangs, den Sie zusammen mit den restlichen Parametern ausführen möchten:</span><span class="sxs-lookup"><span data-stu-id="19f27-109">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a><span data-ttu-id="19f27-110">Weitere Vorgänge</span><span class="sxs-lookup"><span data-stu-id="19f27-110">Other Operations</span></span>

<span data-ttu-id="19f27-111">`ToffoliSimulator`Unterstützt Drehungen und exponentiierte Paulis, z. b. `R` und `Exp` , wenn der resultierende Vorgang gleich `X` oder der Identität entspricht.</span><span class="sxs-lookup"><span data-stu-id="19f27-111">The `ToffoliSimulator` supports rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation is equal to `X` or to the identity.</span></span>

<span data-ttu-id="19f27-112">Messungen und Assert werden unterstützt, aber nur in der Pauli- `Z` Basis.</span><span class="sxs-lookup"><span data-stu-id="19f27-112">Measurement and assert are supported, but only in the Pauli `Z` basis.</span></span>
<span data-ttu-id="19f27-113">Beachten Sie, dass die Wahrscheinlichkeit einer Messung immer entweder 0 oder 1 ist. Es gibt keine Zufälligkeit im-Simulator von "".</span><span class="sxs-lookup"><span data-stu-id="19f27-113">Note that the probability of some measurement is always either 0 or 1; there is no randomness in the Toffoli simulator.</span></span>

<span data-ttu-id="19f27-114">`DumpMachine` und `DumpRegister` werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19f27-114">`DumpMachine` and `DumpRegister` are supported.</span></span>
<span data-ttu-id="19f27-115">Beide geben den aktuellen `Z` Status jedes Qubit aus, ein Qubit pro Zeile.</span><span class="sxs-lookup"><span data-stu-id="19f27-115">They both output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="qubitcount"></a><span data-ttu-id="19f27-116">Qubitcount</span><span class="sxs-lookup"><span data-stu-id="19f27-116">QubitCount</span></span>

<span data-ttu-id="19f27-117">Standardmäßig ordnet der `ToffoliSimulator` Speicherplatz für 65.536 Qubits zu.</span><span class="sxs-lookup"><span data-stu-id="19f27-117">By default, the `ToffoliSimulator` allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="19f27-118">Wenn der Algorithmus mehr als diesen Wert erfordert, können Sie die Anzahl der Qubits ändern, indem Sie dem Konstruktor einen Wert für den Parameter bereitstellen `qubitCount` .</span><span class="sxs-lookup"><span data-stu-id="19f27-118">If your algorithm requires more than this, you can change the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="19f27-119">Jedes zusätzliche Qubit erfordert ein zusätzliches Byte Arbeitsspeicher, sodass die Anzahl der benötigten Qubits nicht signifikant ist.</span><span class="sxs-lookup"><span data-stu-id="19f27-119">Each additional qubit requires an additional byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="19f27-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="19f27-120">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
