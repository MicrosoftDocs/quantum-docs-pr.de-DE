---
title: Erstellen eines Quanten-Zufallszahlengenerators
description: Erstellen Sie ein Q# Projekt, das grundlegende Quantum-Konzepte wie Superposition veranschaulicht, indem Sie einen Quantum-Zufallszahlengenerator erstellen.
author: bromeg
ms.author: megbrow
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: a0e8933e6a77d017db914e4bb969ea05f760a443
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834039"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="83bd4-103">Tutorial: Implementieren eines Quanten-Zufallszahlengenerators in Q\#</span><span class="sxs-lookup"><span data-stu-id="83bd4-103">Tutorial: Implement a Quantum Random Number Generator in Q\#</span></span>

<span data-ttu-id="83bd4-104">Ein einfaches Beispiel für einen in geschriebenen Quantum-Algorithmus Q# ist ein Quantum-Zufallszahlengenerator.</span><span class="sxs-lookup"><span data-stu-id="83bd4-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="83bd4-105">Für diesen Algorithmus wird das Prinzip der Quantenmechanik genutzt, um eine Zufallszahl zu generieren.</span><span class="sxs-lookup"><span data-stu-id="83bd4-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="83bd4-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="83bd4-106">Prerequisites</span></span>

- <span data-ttu-id="83bd4-107">Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="83bd4-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="83bd4-108">Erstellen Sie ein Q# Projekt für eine- [ Q# Anwendung](xref:microsoft.quantum.install.standalone), ein [python-Host Programm](xref:microsoft.quantum.install.python)oder ein [c#-Host Programm](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="83bd4-108">Create a Q# project for either a [Q# application](xref:microsoft.quantum.install.standalone), with a [Python host program](xref:microsoft.quantum.install.python), or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="write-a-no-locq-operation"></a><span data-ttu-id="83bd4-109">Schreiben eines- Q# Vorgangs</span><span class="sxs-lookup"><span data-stu-id="83bd4-109">Write a Q# operation</span></span>

### <a name="no-locq-operation-code"></a><span data-ttu-id="83bd4-110">Q# Vorgangs Code</span><span class="sxs-lookup"><span data-stu-id="83bd4-110">Q# operation code</span></span>

1. <span data-ttu-id="83bd4-111">Ersetzen Sie den Inhalt der Datei „Program.qs“ durch den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="83bd4-111">Replace the contents of the Program.qs file with the following code:</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

<span data-ttu-id="83bd4-112">Wie im Artikel [Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding) erklärt, stellt ein Qubit eine Einheit mit Quanteninformationen dar, die sich in einem Superpositionszustand befinden kann.</span><span class="sxs-lookup"><span data-stu-id="83bd4-112">As mentioned in our [Understanding quantum computing](xref:microsoft.quantum.overview.understanding) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="83bd4-113">Für ein Qubit kann sich bei einer Messung nur 0 oder 1 ergeben.</span><span class="sxs-lookup"><span data-stu-id="83bd4-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="83bd4-114">Wenn jedoch ein Vorgang ausgeführt wird, stellt der Status des Qubit die Wahrscheinlichkeit dar, dass entweder 0 oder 1 mit einer Messung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="83bd4-114">However, when an operation is running, the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="83bd4-115">Dieser Wahrscheinlichkeitszustand wird als Überlagerung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="83bd4-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="83bd4-116">Wir können diese Wahrscheinlichkeit verwenden, um Zufallszahlen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="83bd4-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="83bd4-117">In unserem Q# Vorgang stellen wir den `Qubit` DataType, den systemeigenen, bereit Q# .</span><span class="sxs-lookup"><span data-stu-id="83bd4-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="83bd4-118">Wir können `Qubit` nur mit einer `using`-Anweisung zuordnen.</span><span class="sxs-lookup"><span data-stu-id="83bd4-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="83bd4-119">Nach der Zuordnung befindet sich ein Qubit immer im Zustand `Zero`.</span><span class="sxs-lookup"><span data-stu-id="83bd4-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="83bd4-120">Mit der Operation `H` können wir das `Qubit` in den Zustand der Überlagerung versetzen.</span><span class="sxs-lookup"><span data-stu-id="83bd4-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="83bd4-121">Zum Messen eines Qubits und Lesen seines Werts verwenden Sie die intrinsische Operation `M`.</span><span class="sxs-lookup"><span data-stu-id="83bd4-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="83bd4-122">Indem wir das `Qubit` in den Zustand der Überlagerung versetzen und die Messung durchführen, ergibt sich bei jedem Codeaufruf ein anderer Wert als Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="83bd4-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span>

<span data-ttu-id="83bd4-123">Wenn die Zuordnung für ein `Qubit` aufgehoben wird, muss es explizit zurück in den Zustand `Zero` versetzt werden. Andernfalls wird vom Simulator ein Laufzeitfehler gemeldet.</span><span class="sxs-lookup"><span data-stu-id="83bd4-123">When a `Qubit` is deallocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="83bd4-124">Eine einfache Möglichkeit, dies zu erreichen, ist das Aufrufen von `Reset`.</span><span class="sxs-lookup"><span data-stu-id="83bd4-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="83bd4-125">Visualisieren des Codes mit der Bloch-Kugel</span><span class="sxs-lookup"><span data-stu-id="83bd4-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="83bd4-126">Bei der Bloch-Kugel steht der Nordpol für den klassischen Wert **0** und der Südpol für den klassischen Wert **1**.</span><span class="sxs-lookup"><span data-stu-id="83bd4-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="83bd4-127">Jede Überlagerung kann durch einen Punkt auf der Kugel dargestellt werden (per Pfeil).</span><span class="sxs-lookup"><span data-stu-id="83bd4-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="83bd4-128">Je näher sich das Ende des Pfeils an einem der Pole befindet, desto höher ist die Wahrscheinlichkeit, dass das Qubit bei einer Messung auf den klassischen Wert zurückfällt, der dem Pol zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83bd4-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="83bd4-129">Der unten durch den roten Pfeil dargestellte Qubit-Zustand verfügt beispielsweise über eine höhere Wahrscheinlichkeit, dass sich bei einer Messung der Wert **0** ergibt.</span><span class="sxs-lookup"><span data-stu-id="83bd4-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

<span data-ttu-id="83bd4-130">Wir können diese Darstellung verwenden, um die Aktivitäten des Codes zu visualisieren:</span><span class="sxs-lookup"><span data-stu-id="83bd4-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="83bd4-131">Wir beginnen mit einem im Zustand **0** initialisierten Qubit und wenden `H` an, um eine Überlagerung zu erstellen, bei der die Wahrscheinlichkeiten für **0** und **1** gleich hoch sind.</span><span class="sxs-lookup"><span data-stu-id="83bd4-131">First we start with a qubit initialized in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* <span data-ttu-id="83bd4-132">Anschließend messen wir das Qubit und speichern die Ausgabe:</span><span class="sxs-lookup"><span data-stu-id="83bd4-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

<span data-ttu-id="83bd4-133">Da das Ergebnis der Messung völlig zufällig ist, erhalten wir ein zufälliges Bit.</span><span class="sxs-lookup"><span data-stu-id="83bd4-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="83bd4-134">Wir können diesen Vorgang mehrmals aufrufen, um ganze Zahlen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="83bd4-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="83bd4-135">Wenn wir den Vorgang beispielsweise dreimal aufrufen, um drei zufällige Bits zu erhalten, können wir zufällige 3-Bit-Zahlen erstellen (also eine Zufallszahl zwischen 0 und 7).</span><span class="sxs-lookup"><span data-stu-id="83bd4-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>


## <a name="creating-a-complete-random-number-generator"></a><span data-ttu-id="83bd4-136">Erstellen eines vollständigen Zufallszahlengenerators</span><span class="sxs-lookup"><span data-stu-id="83bd4-136">Creating a complete random number generator</span></span>

<span data-ttu-id="83bd4-137">Nachdem wir nun über einen-Vorgang verfügen, mit Q# dem zufällige Bits generiert werden, können wir damit einen kompletten Quantum-Zufallszahlengenerator erstellen.</span><span class="sxs-lookup"><span data-stu-id="83bd4-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator.</span></span> <span data-ttu-id="83bd4-138">Wir können eine- Q# Anwendung verwenden oder ein Host Programm verwenden.</span><span class="sxs-lookup"><span data-stu-id="83bd4-138">We can use a Q# application or use a host program.</span></span>



### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>[<span data-ttu-id="83bd4-139">Q# Anwendungen mit Visual Studio oder Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="83bd4-139">Q# applications with Visual Studio or Visual Studio Code</span></span>](#tab/tabid-qsharp)

<span data-ttu-id="83bd4-140">Q#Fügen Sie dem Programm den folgenden Einstiegspunkt hinzu, um die vollständige Anwendung zu erstellen Q# :</span><span class="sxs-lookup"><span data-stu-id="83bd4-140">To create the full Q# application, add the following entry point to your Q# program:</span></span> 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

<span data-ttu-id="83bd4-141">Abhängig von der Projekt Konfiguration und den Befehlszeilenoptionen führt das Programm den Vorgang oder die Funktion aus, der mit dem- `@EntryPoint()` Attribut für einen Simulator oder eine Ressourcenschätzung gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="83bd4-141">The program will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

<span data-ttu-id="83bd4-142">Drücken Sie in Visual Studio einfach STRG + F5, um das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="83bd4-142">In Visual Studio, simply press Ctrl + F5 to run the script.</span></span>

<span data-ttu-id="83bd4-143">Erstellen Sie in VS Code erstmalig die Datei „Program.qs“, indem Sie Folgendes im Terminal eingeben:</span><span class="sxs-lookup"><span data-stu-id="83bd4-143">In VS Code, build the Program.qs the first time by typing the below in the terminal:</span></span>

```dotnetcli
dotnet build
```

<span data-ttu-id="83bd4-144">Bei nachfolgenden Ausführungen muss diese Datei nicht erneut erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="83bd4-144">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="83bd4-145">Geben Sie für die Ausführung den folgenden Befehl ein, und drücken Sie die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="83bd4-145">To run it, type the following command and press enter:</span></span>

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-prompt"></a>[<span data-ttu-id="83bd4-146">Python mit Visual Studio Code oder der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="83bd4-146">Python with Visual Studio Code or the command prompt</span></span>](#tab/tabid-python)

<span data-ttu-id="83bd4-147">Um Ihr neues Q# Programm aus python auszuführen, speichern Sie den folgenden Code `host.py` :</span><span class="sxs-lookup"><span data-stu-id="83bd4-147">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

<span data-ttu-id="83bd4-148">Anschließend können Sie Ihr python-Host Programm an der Eingabeaufforderung ausführen:</span><span class="sxs-lookup"><span data-stu-id="83bd4-148">You can then run your Python host program from the command prompt:</span></span>

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[<span data-ttu-id="83bd4-149">C# mit Visual Studio Code oder Visual Studio</span><span class="sxs-lookup"><span data-stu-id="83bd4-149">C# with Visual Studio Code or Visual Studio</span></span>](#tab/tabid-csharp)

<span data-ttu-id="83bd4-150">Um Q# das neue Programm aus c# auszuführen, ändern `Driver.cs` Sie, um den folgenden c#-Code einzuschließen:</span><span class="sxs-lookup"><span data-stu-id="83bd4-150">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

<span data-ttu-id="83bd4-151">Sie können dann Ihr c#-Host Programm von der Eingabeaufforderung aus ausführen (in Visual Studio sollten Sie F5 drücken):</span><span class="sxs-lookup"><span data-stu-id="83bd4-151">You can then run your C# host program from the command prompt (in Visual Studio you should press F5):</span></span>

```bash
$ dotnet run
The random number generated is 42
```

***
