---
title: Entwickeln mit Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274097"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="a8ac4-102">Entwickeln mit Q#-Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="a8ac4-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="a8ac4-103">Installieren Sie das QDK für die Entwicklung von Q#-Vorgängen auf Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="a8ac4-104">Jupyter Notebooks ermöglichen die direkte Codeausführung parallel zu Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="a8ac4-105">Diese Umgebung eignet sich ideal zum Schreiben von Q#-Code mit eingebetteten Erläuterungen oder interaktiven Tutorials zum Quantencomputing.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="a8ac4-106">Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="a8ac4-107">IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="a8ac4-108">In Q#-Jupyter Notebooks können Sie nur Q#-Code ausführen, und die Vorgänge können nicht über externe Hostprogramme (z. B. Python- oder C#-Dateien) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="a8ac4-109">Diese Umgebung ist nicht geeignet, wenn Ihr Ziel die Kombination eines externen klassischen Hostprogramms mit dem Quantenprogramm ist.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="a8ac4-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="a8ac4-110">Prerequisites</span></span>

    - <span data-ttu-id="a8ac4-111">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="a8ac4-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="a8ac4-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="a8ac4-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="a8ac4-113">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="a8ac4-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="a8ac4-114">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="a8ac4-115">Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="a8ac4-116">Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="a8ac4-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="a8ac4-117">Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="a8ac4-118">Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="a8ac4-119">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="a8ac4-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="a8ac4-120">Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:</span><span class="sxs-lookup"><span data-stu-id="a8ac4-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="a8ac4-121">Kopieren Sie zum Öffnen des Jupyter Notebooks die URL aus der Befehlszeile in Ihren Browser.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="a8ac4-122">Erstellen Sie ein Jupyter Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="a8ac4-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="a8ac4-123">Führen Sie diese Zelle des Notebooks aus:</span><span class="sxs-lookup"><span data-stu-id="a8ac4-123">Run this cell of the notebook:</span></span>

        ![Zelle im Jupyter Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

        <span data-ttu-id="a8ac4-125">In der Ausgabe der Zelle sollte `SayHello` angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="a8ac4-126">Bei der Ausführung im Jupyter Notebook wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="a8ac4-127">Führen Sie in einer neuen Zelle den soeben erstellten Vorgang aus (in einem Simulator), indem Sie den Befehl `%simulate` verwenden:</span><span class="sxs-lookup"><span data-stu-id="a8ac4-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook-Zelle mit %simulate-Magic-Befehl](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="a8ac4-129">Auf dem Bildschirm sollte die Meldung mit dem Ergebnis des von Ihnen aufgerufenen Vorgangs angezeigt werden (hier ist dies das leere Tupel `()`, weil bei unserem Vorgang lediglich der Typ `Unit` zurückgegeben wird).</span><span class="sxs-lookup"><span data-stu-id="a8ac4-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a8ac4-130">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a8ac4-130">Next steps</span></span>

<span data-ttu-id="a8ac4-131">Nachdem Sie das QDK für Q#-Jupyter Notebooks nun installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen. Schreiben Sie Ihren Q#-Code hierfür direkt in der Jupyter Notebook-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="a8ac4-132">Weitere Beispiele für die Nutzung von Q#-Jupyter Notebooks finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a8ac4-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="a8ac4-133">[Einführung in Q# und Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="a8ac4-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="a8ac4-134">Enthält ein Q#-Jupyter Notebook, mit dem veranschaulicht wird, wie Sie Q# in dieser Umgebung verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="a8ac4-135">[Quanten-Katas](xref:microsoft.quantum.overview.katas), eine Open-Source-Sammlung mit eigenverantwortlich zu absolvierenden Tutorials und Programmierübungen in Form von Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="a8ac4-136">Die [Tutorial-Notebooks der Quanten-Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) sind ein guter Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="a8ac4-137">Die Quanten-Katas sind so ausgelegt, dass Ihnen gleichzeitig Elemente des Quantencomputings und der Q#-Programmierung vermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="a8ac4-138">Sie sind ein hervorragendes Beispiel dafür, welche Arten von Inhalt Sie mit Q#-Jupyter Notebooks erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a8ac4-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
