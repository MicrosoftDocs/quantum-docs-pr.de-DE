---
title: Entwickeln mit Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 8a878e8f930f4b898f4de35751e4a39cc8716cec
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884251"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="87169-102">Entwickeln mit Q#-Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="87169-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="87169-103">Installieren Sie das QDK für die Entwicklung von Q#-Vorgängen auf Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="87169-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="87169-104">Jupyter Notebooks ermöglichen die direkte Codeausführung parallel zu Anweisungen, Notizen und anderem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="87169-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="87169-105">Diese Umgebung eignet sich ideal zum Schreiben von Q#-Code mit eingebetteten Erläuterungen oder interaktiven Tutorials zum Quantencomputing.</span><span class="sxs-lookup"><span data-stu-id="87169-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="87169-106">Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="87169-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

> [!NOTE]
> * <span data-ttu-id="87169-107">In Q#-Jupyter Notebooks können Sie nur Q#-Code ausführen, und die Vorgänge können nicht über externe Hostprogramme (z. B. Python- oder C#-Dateien) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="87169-107">In Q# Jupyter Notebooks, you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="87169-108">Diese Umgebung ist nicht geeignet, wenn Ihr Ziel die Kombination eines externen klassischen Hostprogramms mit dem Quantenprogramm ist.</span><span class="sxs-lookup"><span data-stu-id="87169-108">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

## <a name="install-the-iq-jupyter-kernel"></a><span data-ttu-id="87169-109">Installieren des IQ#-Jupyter-Kernels</span><span class="sxs-lookup"><span data-stu-id="87169-109">Install the IQ# Jupyter kernel</span></span>

<span data-ttu-id="87169-110">IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="87169-110">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="87169-111">Installation mithilfe von Conda (empfohlen)</span><span class="sxs-lookup"><span data-stu-id="87169-111">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="87169-112">Installieren Sie [Miniconda](https://docs.conda.io/en/latest/miniconda.html) oder [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="87169-112">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span>

1. <span data-ttu-id="87169-113">Öffnen Sie eine Anaconda-Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="87169-113">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="87169-114">Wenn Sie PowerShell oder pwsh verwenden möchten: Öffnen Sie eine Shell, führen Sie `conda init powershell`aus, schließen Sie die Shell, und öffnen Sie sie erneut.</span><span class="sxs-lookup"><span data-stu-id="87169-114">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="87169-115">Erstellen und aktivieren Sie eine neue Conda-Umgebung namens `qsharp-env` mit den erforderlichen Paketen (einschließlich Jupyter Notebook und IQ#), indem Sie die folgenden Befehle ausführen:</span><span class="sxs-lookup"><span data-stu-id="87169-115">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="87169-116">Führen Sie `python -c "import qsharp"` über das gleiche Terminal aus, um die Installation zu überprüfen und den lokalen Paketcache mit allen erforderlichen QDK-Komponenten aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="87169-116">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-advanced"></a>[<span data-ttu-id="87169-117">Installieren mithilfe der .NET-CLI (erweitert)</span><span class="sxs-lookup"><span data-stu-id="87169-117">Install using .NET CLI (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="87169-118">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="87169-118">Prerequisites:</span></span>

    - <span data-ttu-id="87169-119">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="87169-119">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="87169-120">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="87169-120">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="87169-121">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="87169-121">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="87169-122">Installieren Sie das `Microsoft.Quantum.IQSharp`-Paket.</span><span class="sxs-lookup"><span data-stu-id="87169-122">Install the `Microsoft.Quantum.IQSharp` package.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="87169-123">Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.</span><span class="sxs-lookup"><span data-stu-id="87169-123">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="87169-124">Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="87169-124">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="87169-125">Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="87169-125">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="87169-126">Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.</span><span class="sxs-lookup"><span data-stu-id="87169-126">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="87169-127">Das ist alles!</span><span class="sxs-lookup"><span data-stu-id="87169-127">That's it!</span></span> <span data-ttu-id="87169-128">Sie verfügen nun über den IQ#-Kernel für Jupyter, der die Kernfunktionen für das Kompilieren und Ausführen von Q#-Vorgängen in Jupyter Notebook-Instanzen in Q# bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="87169-128">You now have the IQ# kernel for Jupyter, which provides the core functionality for compiling and executing Q# operations from Q# Jupyter Notebooks.</span></span>

## <a name="create-your-first-q-notebook"></a><span data-ttu-id="87169-129">Erstellen Ihres ersten Q#-Notebooks</span><span class="sxs-lookup"><span data-stu-id="87169-129">Create your first Q# notebook</span></span>

<span data-ttu-id="87169-130">Nun können Sie Ihre Q#-Jupyter Notebook-Installation überprüfen, indem Sie einen einfachen Q#-Vorgang schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="87169-130">Now you are ready to verify your Q# Jupyter Notebook installation by writing and executing a simple Q# operation.</span></span>

1. <span data-ttu-id="87169-131">Führen Sie in der bei der Installation erstellten Umgebung (d. h. entweder in der von Ihnen erstellten Conda-Umgebung oder in der Python-Umgebung, in der Sie Jupyter installiert haben) den folgenden Befehl aus, um den Jupyter Notebook-Server zu starten:</span><span class="sxs-lookup"><span data-stu-id="87169-131">From the environment you created during installation (i.e., either the conda environment you created, or the Python environment where you installed Jupyter), run the following command to start the Jupyter Notebook server:</span></span>

    ```
    jupyter notebook
    ```

    - <span data-ttu-id="87169-132">Wenn Jupyter Notebook nicht automatisch in Ihrem Browser geöffnet wird, kopieren Sie die URL aus der Befehlszeile in den Browser.</span><span class="sxs-lookup"><span data-stu-id="87169-132">If the Jupyter Notebook doesn't open automatically in your browser, copy and paste the URL provided by the command line into your browser.</span></span>

1. <span data-ttu-id="87169-133">Wählen Sie „Neu“ → „Q#“, um ein Jupyter Notebook mit einem Q#-Kernel zu erstellen, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="87169-133">Choose "New" → "Q#" to create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. <span data-ttu-id="87169-134">Führen Sie diese Zelle des Notebooks aus:</span><span class="sxs-lookup"><span data-stu-id="87169-134">Run this cell of the notebook:</span></span>

    ![Zelle im Jupyter Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

    <span data-ttu-id="87169-136">In der Ausgabe der Zelle sollte `SampleQuantumRandomNumberGenerator` angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="87169-136">You should see `SampleQuantumRandomNumberGenerator` in the output of the cell.</span></span> <span data-ttu-id="87169-137">Bei der Ausführung im Jupyter Notebook wird der Q#-Code kompiliert, und die Zelle gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="87169-137">When running in Jupyter Notebook, the Q# code is compiled, and the cell outputs the name of any operations that it finds.</span></span>

1. <span data-ttu-id="87169-138">Führen Sie in einer neuen Zelle den soeben erstellten Vorgang aus (in einem Simulator), indem Sie den Befehl `%simulate` verwenden:</span><span class="sxs-lookup"><span data-stu-id="87169-138">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

    ![Jupyter Notebook-Zelle mit %simulate-Magic-Befehl](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="87169-140">Das Ergebnis des von Ihnen aufgerufenen Vorgangs sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="87169-140">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="87169-141">Da in diesem Fall ein zufälliges Ergebnis durch den Vorgang generiert wird, wird entweder `Zero` oder `One` auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="87169-141">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="87169-142">Wenn Sie die Zelle wiederholt ausführen, sollte jedes Ergebnis ungefähr die Hälfte der Zeit angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="87169-142">If you execute the cell repeatedly, you should see each result approximately half the time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="87169-143">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="87169-143">Next steps</span></span>

<span data-ttu-id="87169-144">Nachdem Sie das QDK für Q#-Jupyter Notebooks nun installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen. Schreiben Sie Q#-Code hierfür direkt in der Jupyter Notebook-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="87169-144">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="87169-145">Weitere Beispiele für die Nutzung von Q#-Jupyter Notebooks finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="87169-145">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>

- <span data-ttu-id="87169-146">[Einführung in Q# und Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="87169-146">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="87169-147">Enthält ein Q#-Jupyter Notebook mit weiteren Details zur Verwendung von Q# in der Jupyter-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="87169-147">There you will find a Q# Jupyter Notebook that provides more details on how to use Q# in the Jupyter environment.</span></span>
- <span data-ttu-id="87169-148">[Quanten-Katas](xref:microsoft.quantum.overview.katas), eine Open-Source-Sammlung mit eigenverantwortlich zu absolvierenden Tutorials und Programmierübungen in Form von Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="87169-148">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="87169-149">Die [Tutorial-Notebooks der Quanten-Katas](https://github.com/microsoft/QuantumKatas#tutorial-topics) sind ein guter Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="87169-149">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="87169-150">Die Quanten-Katas sind so ausgelegt, dass Ihnen gleichzeitig Elemente des Quantencomputings und der Q#-Programmierung vermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="87169-150">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="87169-151">Sie sind ein hervorragendes Beispiel dafür, welche Arten von Inhalt Sie mit Q#-Jupyter Notebooks erstellen können.</span><span class="sxs-lookup"><span data-stu-id="87169-151">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>