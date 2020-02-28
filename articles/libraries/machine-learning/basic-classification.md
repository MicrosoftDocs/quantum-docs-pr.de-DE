---
title: Einfache Klassifizierung mit der Quantum-Machine Learning Bibliothek
description: 'Erfahren Sie, wie Sie mithilfe der Quantum-Machine Learning Bibliothek von Microsoft QDK einen in Q # geschriebenen Quantum-Klassifizierer ausführen.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: f42e3e4492f934d7a8f03d4fec6fa0de765401d7
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909924"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="8e574-103">Basic-Klassifizierung: klassifizieren von Daten mit dem QDK</span><span class="sxs-lookup"><span data-stu-id="8e574-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="8e574-104">In dieser Schnellstartanleitung erfahren Sie, wie Sie mithilfe der Quantum-Machine Learning Bibliothek des QDK einen in Q # geschriebenen quantesequenziellen Klassifizierer ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e574-104">In this Quickstart, you will learn how to execute a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="8e574-105">In dieser Anleitung verwenden wir das Halbmond-DataSet mit einer in Q # definierten Klassifizierungs Struktur.</span><span class="sxs-lookup"><span data-stu-id="8e574-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8e574-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="8e574-106">Prerequisites</span></span>

- <span data-ttu-id="8e574-107">Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="8e574-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- [<span data-ttu-id="8e574-108">Erstellen eines Q#-Projekts</span><span class="sxs-lookup"><span data-stu-id="8e574-108">Create a Q# Project</span></span>](xref:microsoft.quantum.howto.createproject)

## <a name="host-program"></a><span data-ttu-id="8e574-109">Host Programm</span><span class="sxs-lookup"><span data-stu-id="8e574-109">Host program</span></span>

<span data-ttu-id="8e574-110">Ihr Host Programm besteht aus drei Teilen:</span><span class="sxs-lookup"><span data-stu-id="8e574-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="8e574-111">Laden Sie das DataSet, und wählen Sie einen Satz von Start Parametern für das Modell aus.</span><span class="sxs-lookup"><span data-stu-id="8e574-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="8e574-112">Führen Sie Schulungen aus, um die Parameter und die Verschiebung des Modells zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8e574-112">Execute training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="8e574-113">Überprüfen des Modells zur Bestimmung der Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="8e574-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="8e574-114">Python mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="8e574-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="8e574-115">Wenn Sie den Q #-Klassifizierer aus python ausführen möchten, speichern Sie den folgenden Code als `host.py`.</span><span class="sxs-lookup"><span data-stu-id="8e574-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="8e574-116">Beachten Sie, dass Sie auch das Q #-Datei `Training.qs` benötigen, das weiter unten in diesem Tutorial erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="8e574-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="8e574-117">Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="8e574-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="8e574-118">C# mit Visual Studio Code oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="8e574-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="8e574-119">Wenn Sie den Q #-Klassifizierer ausführen C#möchten, speichern Sie den folgenden Code als `Host.cs`.</span><span class="sxs-lookup"><span data-stu-id="8e574-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="8e574-120">Beachten Sie, dass Sie auch das Q #-Datei `Training.qs` benötigen, das weiter unten in diesem Tutorial erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="8e574-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="8e574-121">Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="8e574-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="8e574-122">C# mit Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="8e574-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="8e574-123">Um das neue Q #-Programm C# in Visual Studio auszuführen, ändern Sie `Host.cs`, um den C# folgenden Code einzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e574-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="8e574-124">Beachten Sie, dass Sie auch das Q #-Datei `Training.qs` benötigen, das weiter unten in diesem Tutorial erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="8e574-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="8e574-125">Drücken Sie dann F5. Das Programm wird gestartet, und ein neues Fenster mit den folgenden Ergebnissen wird angezeigt:</span><span class="sxs-lookup"><span data-stu-id="8e574-125">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="8e574-126">F\# klassifizierercode</span><span class="sxs-lookup"><span data-stu-id="8e574-126">Q\# classifier code</span></span>

<span data-ttu-id="8e574-127">Sehen wir uns nun an, wie die vom Host Programm aufgerufenen Vorgänge in f # definiert werden.</span><span class="sxs-lookup"><span data-stu-id="8e574-127">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="8e574-128">Der folgende Code wird in einer Datei mit dem Namen `Training.qs`gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8e574-128">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="8e574-129">Die wichtigsten im obigen Code definierten Funktionen und Vorgänge sind:</span><span class="sxs-lookup"><span data-stu-id="8e574-129">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="8e574-130">`ClassifierStructure() : ControlledRotation[]`: in dieser Funktion wird die Struktur unseres Verbindungs Modells durch Hinzufügen der Ebenen der kontrollierten Gates festgelegt, die berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e574-130">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="8e574-131">Dieser Schritt entspricht der Deklaration von Neuronen-Ebenen in einem sequenziellen Deep Learning-Modell.</span><span class="sxs-lookup"><span data-stu-id="8e574-131">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="8e574-132">`TrainHalfMoonModel() : TrainWineModel() : (Double[], Double)`: dieser Vorgang ist der Kernteil des Codes und definiert das Training.</span><span class="sxs-lookup"><span data-stu-id="8e574-132">`TrainHalfMoonModel() : TrainWineModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="8e574-133">Hier laden wir die Beispiele aus dem DataSet, das in der Bibliothek enthalten ist, legen die Hyperparameter und die ursprünglichen Parameter für das Training fest und beginnen mit dem Training, indem wir den in der Bibliothek enthaltenen Vorgang `TrainSequentialClassifier` aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8e574-133">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="8e574-134">Es gibt die Parameter und die Verschiebung aus, die den Klassifizierer bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8e574-134">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="8e574-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: dieser Vorgang definiert den Validierungsprozess zum Auswerten des Modells.</span><span class="sxs-lookup"><span data-stu-id="8e574-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="8e574-136">Hier laden wir die Beispiele für die Überprüfung, die Anzahl der Messungen pro Stichprobe und die Toleranz.</span><span class="sxs-lookup"><span data-stu-id="8e574-136">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="8e574-137">Er gibt die Anzahl der fehl Klassifizierungen für den ausgewählten Batch von Beispielen für die Validierung aus.</span><span class="sxs-lookup"><span data-stu-id="8e574-137">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8e574-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8e574-138">Next steps</span></span>

<span data-ttu-id="8e574-139">Zuerst können Sie mit dem Code experimentieren und versuchen, einige Parameter zu ändern, um zu sehen, wie sich dies auf das Training auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8e574-139">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="8e574-140">Im nächsten Tutorial entwerfen Sie dann [ihren eigenen Klassifizierer](xref:microsoft.quantum.libraries.machine-learning.design). Sie erfahren, wie Sie die Struktur des Klassifizierers definieren.</span><span class="sxs-lookup"><span data-stu-id="8e574-140">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
