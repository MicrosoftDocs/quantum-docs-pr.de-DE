---
title: Erstellen eines Quanten-Zufallszahlengenerators
description: Enthält eine Beschreibung der Erstellung eines Q#-Projekts, mit dem grundlegende Quantenkonzepte wie die Überlagerung veranschaulicht werden, indem ein Quanten-Zufallszahlengenerator erstellt wird.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 134617455b720cc755b9ee9fb68fb59e624d3f1a
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820912"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="529af-103">Schnellstart: Implementieren eines Quanten-Zufallszahlengenerators in Q#</span><span class="sxs-lookup"><span data-stu-id="529af-103">Quickstart: Implement a Quantum Random Number Generator in Q#</span></span>
<span data-ttu-id="529af-104">Ein einfaches Beispiel für einen Quantenalgorithmus, der in Q# geschrieben ist, ist ein Quanten-Zufallszahlengenerator.</span><span class="sxs-lookup"><span data-stu-id="529af-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="529af-105">Für diesen Algorithmus wird das Prinzip der Quantenmechanik genutzt, um eine Zufallszahl zu generieren.</span><span class="sxs-lookup"><span data-stu-id="529af-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="529af-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="529af-106">Prerequisites</span></span>

- <span data-ttu-id="529af-107">Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="529af-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="529af-108">Erstellen eines Q#-Projekts</span><span class="sxs-lookup"><span data-stu-id="529af-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a><span data-ttu-id="529af-109">Schreiben einer Q#-Operation</span><span class="sxs-lookup"><span data-stu-id="529af-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="529af-110">Q#-Operationscode</span><span class="sxs-lookup"><span data-stu-id="529af-110">Q# operation code</span></span>

1. <span data-ttu-id="529af-111">Ersetzen Sie den Inhalt der Datei „Operation.qs“ durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="529af-111">Replace the contents of the Operation.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(qubit = Qubit())  { // Allocate a qubit.
                H(qubit);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(v);     // Measure the qubit value.
                Reset(qubit);
                return r;
            }
        }
    }
    ```

<span data-ttu-id="529af-112">Wie im Artikel [Was ist Quantencomputing?](xref:microsoft.quantum.overview.what) erwähnt, stellt ein Qubit eine Einheit mit Quanteninformationen dar, für die eine Überlagerung vorliegen kann.</span><span class="sxs-lookup"><span data-stu-id="529af-112">As mentioned in our [What is Quantum Computing?](xref:microsoft.quantum.overview.what) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="529af-113">Für ein Qubit kann sich bei einer Messung nur 0 oder 1 ergeben.</span><span class="sxs-lookup"><span data-stu-id="529af-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="529af-114">Während der Ausführung steht der Zustand des Qubits aber für die Wahrscheinlichkeit, dass sich für eine Messung entweder 0 oder 1 ergibt.</span><span class="sxs-lookup"><span data-stu-id="529af-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="529af-115">Dieser Wahrscheinlichkeitszustand wird als Überlagerung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="529af-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="529af-116">Wir können diese Wahrscheinlichkeit verwenden, um Zufallszahlen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="529af-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="529af-117">In unserer Q#-Operation führen wir den nativen Q#-Datentyp `Qubit` ein.</span><span class="sxs-lookup"><span data-stu-id="529af-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="529af-118">Wir können `Qubit` nur mit einer `using`-Anweisung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="529af-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="529af-119">Nach der Zuordnung befindet sich ein Qubit immer im Zustand `Zero`.</span><span class="sxs-lookup"><span data-stu-id="529af-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="529af-120">Mit der Operation `H` können wir das `Qubit` in den Zustand der Überlagerung versetzen.</span><span class="sxs-lookup"><span data-stu-id="529af-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="529af-121">Zum Messen eines Qubits und Lesen seines Werts verwenden Sie die intrinsische Operation `M`.</span><span class="sxs-lookup"><span data-stu-id="529af-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="529af-122">Indem wir das `Qubit` in den Zustand der Überlagerung versetzen und die Messung durchführen, ergibt sich bei jedem Codeaufruf ein anderer Wert als Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="529af-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span> 

<span data-ttu-id="529af-123">Wenn die Zuordnung für ein `Qubit` aufgehoben wird, muss es explizit zurück in den Zustand `Zero` versetzt werden. Andernfalls wird vom Simulator ein Laufzeitfehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="529af-123">When a `Qubit` is de-allocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="529af-124">Eine einfache Möglichkeit, dies zu erreichen, ist das Aufrufen von `Reset`.</span><span class="sxs-lookup"><span data-stu-id="529af-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="529af-125">Visualisieren des Codes mit der Bloch-Kugel</span><span class="sxs-lookup"><span data-stu-id="529af-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="529af-126">Bei der Bloch-Kugel steht der Nordpol für den klassischen Wert **0** und der Südpol für den klassischen Wert **1**.</span><span class="sxs-lookup"><span data-stu-id="529af-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="529af-127">Jede Überlagerung kann durch einen Punkt auf der Kugel dargestellt werden (per Pfeil).</span><span class="sxs-lookup"><span data-stu-id="529af-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="529af-128">Je näher sich das Ende des Pfeils an einem der Pole befindet, desto höher ist die Wahrscheinlichkeit, dass das Qubit bei einer Messung auf den klassischen Wert zurückfällt, der dem Pol zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="529af-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="529af-129">Der unten durch den roten Pfeil dargestellte Qubit-Zustand verfügt beispielsweise über eine höhere Wahrscheinlichkeit, dass sich bei einer Messung der Wert **0** ergibt.</span><span class="sxs-lookup"><span data-stu-id="529af-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175">

<span data-ttu-id="529af-130">Wir können diese Darstellung verwenden, um die Aktivitäten des Codes zu visualisieren:</span><span class="sxs-lookup"><span data-stu-id="529af-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="529af-131">Wir beginnen mit einem im Zustand **0** initialisierten Qubit und wenden `H` an, um eine Überlagerung zu erstellen, bei der die Wahrscheinlichkeiten für **0** und **1** gleich hoch sind.</span><span class="sxs-lookup"><span data-stu-id="529af-131">First we start with a qubit initalizated in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450">

* <span data-ttu-id="529af-132">Anschließend messen wir das Qubit und speichern die Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="529af-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450">

<span data-ttu-id="529af-133">Da das Ergebnis der Messung völlig zufällig ist, erhalten wir ein zufälliges Bit.</span><span class="sxs-lookup"><span data-stu-id="529af-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="529af-134">Wir können diesen Vorgang mehrmals aufrufen, um ganze Zahlen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="529af-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="529af-135">Wenn wir den Vorgang beispielsweise dreimal aufrufen, um drei zufällige Bits zu erhalten, können wir zufällige 3-Bit-Zahlen erstellen (also eine Zufallszahl zwischen 0 und 7).</span><span class="sxs-lookup"><span data-stu-id="529af-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>

## <a name="creating-a-complete-random-number-generator-using-a-host-program"></a><span data-ttu-id="529af-136">Erstellen eines vollständigen Zufallszahlengenerators mithilfe eines Hostprogramms</span><span class="sxs-lookup"><span data-stu-id="529af-136">Creating a complete random number generator using a host program</span></span>

<span data-ttu-id="529af-137">Sie besitzen nun einen Q#-Vorgang, der zufällige Bits generiert, und können damit einen vollständigen Quanten-Zufallszahlengenerator mit einem Hostprogramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="529af-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator with a host program.</span></span>

 ### <a name="python-with-visual-studio-code-or-the-command-linetabtabid-python"></a>[<span data-ttu-id="529af-138">Python mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="529af-138">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)
 
 <span data-ttu-id="529af-139">Um Ihr neues Q#-Programm aus Python auszuführen, speichern Sie den folgenden Code als `host.py`:</span><span class="sxs-lookup"><span data-stu-id="529af-139">To run your new Q# program from Python, save the following code as `host.py`:</span></span>
 
:::code language="python" source="~/quantum/samples/getting-started/qrng/host.py" range="11-30":::

 <span data-ttu-id="529af-140">Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="529af-140">You can then run your Python host program from the command line:</span></span>
 ```bash
 $ python host.py
 Preparing Q# environment...
 ..The random number generated is 42
 ```
 ### <a name="c-with-visual-studio-code-or-the-command-linetabtabid-csharp"></a>[<span data-ttu-id="529af-141">C# mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="529af-141">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)
 
 <span data-ttu-id="529af-142">Um Ihr neues Q#-Programm aus C# auszuführen, ändern Sie `Driver.cs`, so dass es den folgenden C#-Code beinhaltet:</span><span class="sxs-lookup"><span data-stu-id="529af-142">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>
 
 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::
 
 <span data-ttu-id="529af-143">Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="529af-143">You can then run your C# host program from the command line:</span></span>
 
 ```bash
 $ dotnet run
 The random number generated is 42
 ```

 ### <a name="c-with-visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="529af-144">C# mit Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="529af-144">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

 <span data-ttu-id="529af-145">Ändern Sie zum Ausführen Ihres neuen Q#-Programms aus C# in Visual Studio `Driver.cs`, sodass der folgende C#-Code enthalten ist:</span><span class="sxs-lookup"><span data-stu-id="529af-145">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::

 <span data-ttu-id="529af-146">Drücken Sie dann F5. Das Programm wird gestartet, und ein neues Fenster mit der generierten Zufallszahl wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="529af-146">Then press F5, the program will start execution and a new window will pop up with the random number generated:</span></span> 

 ```bash
 $ dotnet run
 The random number generated is 42
 ```
 ***
