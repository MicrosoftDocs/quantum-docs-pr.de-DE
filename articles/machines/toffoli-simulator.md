---
title: Quantum Development Kit-Simulator | Microsoft-Dokumentation
description: Übersicht über das Quantum Development Kit von Microsoft zum Simulator
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 26940d1a8fe31f1035e2d23a68940cd999517c6b
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442354"
---
# <a name="quantum-development-kit-toffoli-simulator"></a><span data-ttu-id="90a81-103">Quantum Development Kit-Simulator</span><span class="sxs-lookup"><span data-stu-id="90a81-103">Quantum Development Kit Toffoli Simulator</span></span>

<span data-ttu-id="90a81-104">Das Quantum Development Kit bietet einen deffoli-Simulator, bei dem es sich um einen Zweck Simulator handelt, mit dem Quantum-Algorithmen simuliert werden können, die auf x-, CNOT-und multigesteuerte X-Quantum-Vorgänge beschränkt sind (alle klassischen Logik und Berechnungen sind verfügbar).</span><span class="sxs-lookup"><span data-stu-id="90a81-104">The Quantum Development Kit provides a Toffoli simulator, which is a special-purpose simulator that can simulate quantum algorithms that are limited to X, CNOT, and multi-controlled X quantum operations (all classical logic and computations are available).</span></span>

<span data-ttu-id="90a81-105">Während der Vorgang "deffoli" in der Operation wesentlich eingeschränkter ist als der [vollständige Zustands Simulator](xref:microsoft.quantum.machines.full-state-simulator), kann er weitaus mehr Qubits simulieren.</span><span class="sxs-lookup"><span data-stu-id="90a81-105">While the Toffoli simulator is much more restricted in operation than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it can simulate far more qubits.</span></span>
<span data-ttu-id="90a81-106">Der-Simulator kann mit Millionen von Qubits verwendet werden, während der vollständige Zustands Simulator im Allgemeinen auf ungefähr 30 beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="90a81-106">The Toffoli simulator can be used with millions of qubits, while the full state simulator is generally limited to about 30.</span></span>
<span data-ttu-id="90a81-107">Es kann einen begrenzten Satz von Quantum-Algorithmen ausführen und Debuggen, die in Q # auf dem Computer geschrieben wurden. Beispielsweise können Oracles, die Boolesche Funktionen evaluieren, mithilfe dieser Gates implementiert werden. Diese werden daher bei einer großen Anzahl von Qubits mit diesem Simulator getestet.</span><span class="sxs-lookup"><span data-stu-id="90a81-107">It can execute and debug a limited set of quantum algorithms written in Q# on your computer; for instance, oracles that evaluate Boolean functions can be implemented using these gates and so tested on vary large numbers of qubits using this simulator.</span></span>

<span data-ttu-id="90a81-108">Dieser Quantum-Simulator wird über die `ToffoliSimulator`-Klasse verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="90a81-108">This quantum simulator is exposed via the `ToffoliSimulator` class.</span></span>
<span data-ttu-id="90a81-109">Um den Simulator zu verwenden, erstellen Sie einfach eine Instanz dieser Klasse, und übergeben Sie Sie an die `Run`-Methode des Quantum-Vorgangs, den Sie zusammen mit den restlichen Parametern ausführen möchten:</span><span class="sxs-lookup"><span data-stu-id="90a81-109">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a><span data-ttu-id="90a81-110">Weitere Vorgänge</span><span class="sxs-lookup"><span data-stu-id="90a81-110">Other Operations</span></span>

<span data-ttu-id="90a81-111">Der `ToffoliSimulator` unterstützt Drehungen und exponentiierte Paulis, z. b. `R` und `Exp`, wenn der resultierende Vorgang gleich `X` oder der Identität ist.</span><span class="sxs-lookup"><span data-stu-id="90a81-111">The `ToffoliSimulator` supports rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation is equal to `X` or to the identity.</span></span>

<span data-ttu-id="90a81-112">Messungen und Assert werden unterstützt, aber nur in der Pauli-`Z` Basis.</span><span class="sxs-lookup"><span data-stu-id="90a81-112">Measurement and assert are supported, but only in the Pauli `Z` basis.</span></span>
<span data-ttu-id="90a81-113">Beachten Sie, dass die Wahrscheinlichkeit einer Messung immer entweder 0 oder 1 ist. Es gibt keine Zufälligkeit im-Simulator von "".</span><span class="sxs-lookup"><span data-stu-id="90a81-113">Note that the probability of some measurement is always either 0 or 1; there is no randomness in the Toffoli simulator.</span></span>

<span data-ttu-id="90a81-114">`DumpMachine` und `DumpRegister` werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="90a81-114">`DumpMachine` and `DumpRegister` are supported.</span></span>
<span data-ttu-id="90a81-115">Beide geben den aktuellen `Z`basierten Status jedes Qubit, ein Qubit pro Zeile, aus.</span><span class="sxs-lookup"><span data-stu-id="90a81-115">They both output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="qubitcount"></a><span data-ttu-id="90a81-116">Qubitcount</span><span class="sxs-lookup"><span data-stu-id="90a81-116">QubitCount</span></span>

<span data-ttu-id="90a81-117">Standardmäßig wird von der `ToffoliSimulator` Speicherplatz für 65.536 Qubits zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="90a81-117">By default, the `ToffoliSimulator` allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="90a81-118">Wenn der Algorithmus mehr als diesen Wert erfordert, können Sie die Anzahl der Qubits ändern, indem Sie einen Wert für den `qubitCount`-Parameter für den Konstruktor bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="90a81-118">If your algorithm requires more than this, you can change the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="90a81-119">Jedes zusätzliche Qubit erfordert ein zusätzliches Byte Arbeitsspeicher, sodass die Anzahl der benötigten Qubits nicht signifikant ist.</span><span class="sxs-lookup"><span data-stu-id="90a81-119">Each additional qubit requires an additional byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="90a81-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="90a81-120">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
