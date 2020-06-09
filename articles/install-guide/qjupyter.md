---
title: Entwickeln mit Q#-Jupyter-Notebooks
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 9117794d6cf6f05fa34e05c21fad8977d0e76505
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577819"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="2e39d-102">Entwickeln mit Q#-Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="2e39d-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="2e39d-103">Installieren Sie das QDK zum Entwickeln von q #-Vorgängen für q # jupyter-Notebooks.</span><span class="sxs-lookup"><span data-stu-id="2e39d-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="2e39d-104">Jupyter-Notebooks ermöglichen die direkte Codeausführung neben Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="2e39d-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="2e39d-105">Diese Umgebung eignet sich ideal zum Schreiben von f #-Code mit eingebetteten Erläuterungen oder interaktiven Lernprogrammen für Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="2e39d-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="2e39d-106">Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="2e39d-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="2e39d-107">IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="2e39d-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="2e39d-108">In q # jupyter Notebooks können Sie nur q #-Code ausführen, und die Vorgänge können nicht von externen Host Programmen (z. b. python-oder c#-Dateien) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2e39d-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="2e39d-109">Diese Umgebung ist nicht geeignet, wenn Sie ein externes klassisches Host Programm mit dem Quantum-Programm kombinieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2e39d-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="2e39d-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2e39d-110">Pre-requisites</span></span>

    - <span data-ttu-id="2e39d-111">[Python](https://www.python.org/downloads/) 3,6 oder höher</span><span class="sxs-lookup"><span data-stu-id="2e39d-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="2e39d-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="2e39d-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="2e39d-113">.Net Core SDK 3,1</span><span class="sxs-lookup"><span data-stu-id="2e39d-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="2e39d-114">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="2e39d-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="2e39d-115">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2e39d-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="2e39d-116">Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:</span><span class="sxs-lookup"><span data-stu-id="2e39d-116">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="2e39d-117">Um das Jupyter Notebook zu öffnen, kopieren Sie die von der Befehlszeile bereitgestellte URL in Ihren Browser, und fügen Sie Sie ein.</span><span class="sxs-lookup"><span data-stu-id="2e39d-117">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="2e39d-118">Erstellen Sie eine Jupyter Notebook mit einem Q #-Kernel, und fügen Sie der ersten Notebook-Zelle den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="2e39d-118">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="2e39d-119">Führen Sie diese Zelle des Notebooks aus:</span><span class="sxs-lookup"><span data-stu-id="2e39d-119">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook Zelle mit Q #-Code](~/media/install-guide-jupyter.png)

        <span data-ttu-id="2e39d-121">In der Ausgabe der Zelle sollte `SayHello` angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2e39d-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="2e39d-122">Bei Ausführung in Jupyter Notebook wird der Q #-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="2e39d-122">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="2e39d-123">Führen Sie in einer neuen Zelle den soeben erstellten Vorgang (in einem Simulator) mithilfe des Befehls aus `%simulate` :</span><span class="sxs-lookup"><span data-stu-id="2e39d-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook Zelle mit "% simulieren" Magic](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="2e39d-125">Die Meldung sollte zusammen mit dem Ergebnis des aufgerufenen Vorgangs auf dem Bildschirm angezeigt werden (hier sehen wir das leere Tupel, `()` da der Vorgang einfach einen Typ zurückgibt `Unit` ).</span><span class="sxs-lookup"><span data-stu-id="2e39d-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="2e39d-126">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="2e39d-126">Next steps</span></span>

<span data-ttu-id="2e39d-127">Nachdem Sie das QDK für Q # jupyter Notebooks installiert haben, können Sie [Ihr erstes Quantum-Programm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen, indem Sie den Q #-Code direkt in die Jupyter Notebook Umgebung schreiben.</span><span class="sxs-lookup"><span data-stu-id="2e39d-127">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="2e39d-128">Weitere Beispiele für das, was Sie mit Q # jupyter-Notebooks tun können, finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="2e39d-128">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="2e39d-129">Einführung [in Q # und Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="2e39d-129">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="2e39d-130">Dort finden Sie eine q #-Jupyter Notebook, die zeigt, wie q # in dieser Umgebung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2e39d-130">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="2e39d-131">[Quantum Katas](xref:microsoft.quantum.overview.katas), eine Open Source-Sammlung von Lernprogrammen für das Selbststudium und Sätze von programmierübungen in Form von Q # jupyter-Notebooks.</span><span class="sxs-lookup"><span data-stu-id="2e39d-131">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="2e39d-132">Das [Quantum Katas Tutorial](https://github.com/microsoft/QuantumKatas#tutorial-topics) ist ein guter Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="2e39d-132">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="2e39d-133">Die Quantum-Katas sind darauf ausgerichtet, Ihnen Elemente von Quantum Computing und Q #-Programmierung gleichzeitig zu vermitteln.</span><span class="sxs-lookup"><span data-stu-id="2e39d-133">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="2e39d-134">Sie sind ein gutes Beispiel für die Art von Inhalten, die Sie mit Q # jupyter Notebooks erstellen können.</span><span class="sxs-lookup"><span data-stu-id="2e39d-134">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
