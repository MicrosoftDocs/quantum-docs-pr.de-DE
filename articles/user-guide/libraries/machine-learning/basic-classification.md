---
title: Einfache Klassifizierung mit der Quantum-Machine Learning Bibliothek
description: Erfahren Sie, wie Sie Q# mithilfe der Quantum-Machine Learning Bibliothek von Microsoft QDK einen in geschriebenen Quantum-Klassifizierungs Klassifizierer ausführen.
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: conceptual
uid: microsoft.quantum.libraries.machine-learning.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4fe686a87fbdc610badc0bbcbc0bf7b065e0bce9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854041"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="f2f68-103">Basic-Klassifizierung: klassifizieren von Daten mit dem QDK</span><span class="sxs-lookup"><span data-stu-id="f2f68-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="f2f68-104">In dieser Schnellstartanleitung erfahren Sie, wie Sie Q# mithilfe der Quantum-Machine Learning-Bibliothek des QDK einen in geschriebenen quantumziellen Klassifizierungs-Klassifizierer ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2f68-104">In this Quickstart, you will learn how to run a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="f2f68-105">In diesem Handbuch verwenden wir das Halbmond-DataSet, indem wir eine Klassifizierungs Struktur verwenden, die in definiert ist Q# .</span><span class="sxs-lookup"><span data-stu-id="f2f68-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2f68-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f2f68-106">Prerequisites</span></span>

- <span data-ttu-id="f2f68-107">Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="f2f68-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="f2f68-108">Erstellen Sie ein Q# Projekt für ein [python-Host Programm](xref:microsoft.quantum.install.python) oder ein [c#-Host Programm](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="f2f68-108">Create a Q# project for either a [Python host program](xref:microsoft.quantum.install.python) or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="host-program"></a><span data-ttu-id="f2f68-109">Host Programm</span><span class="sxs-lookup"><span data-stu-id="f2f68-109">Host program</span></span>

<span data-ttu-id="f2f68-110">Ihr Host Programm besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="f2f68-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="f2f68-111">Laden Sie das DataSet, und wählen Sie einen Satz von Start Parametern für das Modell aus.</span><span class="sxs-lookup"><span data-stu-id="f2f68-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="f2f68-112">Führen Sie Schulungen aus, um die Parameter und die Verschiebung des Modells zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f2f68-112">Run training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="f2f68-113">Überprüfen des Modells zur Bestimmung der Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="f2f68-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="f2f68-114">Python mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="f2f68-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="f2f68-115">Um die Q# Klassifizierung aus python auszuführen, speichern Sie den folgenden Code als `host.py` .</span><span class="sxs-lookup"><span data-stu-id="f2f68-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="f2f68-116">Beachten Sie, dass Sie auch die Q# Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="f2f68-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="f2f68-117">Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="f2f68-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="f2f68-118">C# mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="f2f68-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="f2f68-119">Um die Q# Klassifizierung aus c# auszuführen, speichern Sie den folgenden Code als `Host.cs` .</span><span class="sxs-lookup"><span data-stu-id="f2f68-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="f2f68-120">Beachten Sie, dass Sie auch die Q# Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="f2f68-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="f2f68-121">Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="f2f68-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="f2f68-122">C# mit Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="f2f68-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="f2f68-123">Um Q# das neue Programm aus c# in Visual Studio auszuführen, ändern `Host.cs` Sie, um den folgenden c#-Code einzufügen.</span><span class="sxs-lookup"><span data-stu-id="f2f68-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="f2f68-124">Beachten Sie, dass Sie auch die Q# Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="f2f68-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="f2f68-125">Drücken Sie F5, damit das Programm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2f68-125">Press F5, and the program will start to run.</span></span> <span data-ttu-id="f2f68-126">Die folgenden Ergebnisse werden in einem neuen Fenster angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f2f68-126">A new window will display the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="f2f68-127">Q- \# Klassifizierungs Code</span><span class="sxs-lookup"><span data-stu-id="f2f68-127">Q\# classifier code</span></span>

<span data-ttu-id="f2f68-128">Nun sehen wir uns an, wie die vom Host Programm aufgerufenen Vorgänge in definiert werden Q# .</span><span class="sxs-lookup"><span data-stu-id="f2f68-128">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="f2f68-129">Der folgende Code wird in einer Datei mit dem Namen gespeichert `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="f2f68-129">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="f2f68-130">Die wichtigsten im obigen Code definierten Funktionen und Vorgänge sind:</span><span class="sxs-lookup"><span data-stu-id="f2f68-130">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="f2f68-131">`ClassifierStructure() : ControlledRotation[]` : in dieser Funktion legen wir die Struktur unseres Verbindungs Modells fest, indem wir die Ebenen der kontrollierten Gates hinzufügen, die wir in Erwägung gezogen haben.</span><span class="sxs-lookup"><span data-stu-id="f2f68-131">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="f2f68-132">Dieser Schritt entspricht der Deklaration von Neuronen-Ebenen in einem sequenziellen Deep Learning-Modell.</span><span class="sxs-lookup"><span data-stu-id="f2f68-132">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="f2f68-133">`TrainHalfMoonModel() : (Double[], Double)` : dieser Vorgang ist der Kernteil des Codes und definiert das Training.</span><span class="sxs-lookup"><span data-stu-id="f2f68-133">`TrainHalfMoonModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="f2f68-134">Hier laden wir die Beispiele aus dem DataSet, das in der Bibliothek enthalten ist, legen die Hyperparameter und die ursprünglichen Parameter für das Training fest und beginnen mit dem Training, indem wir den `TrainSequentialClassifier` in der Bibliothek enthaltenen Vorgang aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2f68-134">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="f2f68-135">Es gibt die Parameter und die Verschiebung aus, die den Klassifizierer bestimmen.</span><span class="sxs-lookup"><span data-stu-id="f2f68-135">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="f2f68-136">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : dieser Vorgang definiert den Validierungsprozess zum Auswerten des Modells.</span><span class="sxs-lookup"><span data-stu-id="f2f68-136">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="f2f68-137">Hier laden wir die Beispiele für die Überprüfung, die Anzahl der Messungen pro Stichprobe und die Toleranz.</span><span class="sxs-lookup"><span data-stu-id="f2f68-137">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="f2f68-138">Er gibt die Anzahl der fehl Klassifizierungen für den ausgewählten Batch von Beispielen für die Validierung aus.</span><span class="sxs-lookup"><span data-stu-id="f2f68-138">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f2f68-139">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="f2f68-139">Next steps</span></span>

<span data-ttu-id="f2f68-140">Zuerst können Sie mit dem Code experimentieren und versuchen, einige Parameter zu ändern, um zu sehen, wie sich dies auf das Training auswirkt.</span><span class="sxs-lookup"><span data-stu-id="f2f68-140">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="f2f68-141">Im nächsten Tutorial entwerfen Sie dann [ihren eigenen Klassifizierer](xref:microsoft.quantum.libraries.machine-learning.design). Sie erfahren, wie Sie die Struktur des Klassifizierers definieren.</span><span class="sxs-lookup"><span data-stu-id="f2f68-141">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
