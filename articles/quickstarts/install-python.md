---
title: Entwickeln mit Q# und Python
description: Hier erfahren Sie, wie Sie mithilfe von Python eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: f6a2a7d1888cfe458fa3989a27d71fcdeed0f01f
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834158"
---
# <a name="develop-with-no-locq-and-python"></a><span data-ttu-id="9e966-103">Entwickeln mit Q# und Python</span><span class="sxs-lookup"><span data-stu-id="9e966-103">Develop with Q# and Python</span></span>

<span data-ttu-id="9e966-104">Installieren Sie das QDK, um Python-Hostprogramme zum Aufrufen von Q#-Vorgängen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="9e966-104">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="9e966-105">Installieren des `qsharp`-Python-Pakets</span><span class="sxs-lookup"><span data-stu-id="9e966-105">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="9e966-106">Installation mithilfe von Conda (empfohlen)</span><span class="sxs-lookup"><span data-stu-id="9e966-106">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="9e966-107">Installieren Sie [Miniconda](https://docs.conda.io/en/latest/miniconda.html) oder [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="9e966-107">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="9e966-108">**Hinweis:** Eine 64-Bit-Installation ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e966-108">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="9e966-109">Öffnen Sie eine Anaconda-Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="9e966-109">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="9e966-110">Wenn Sie PowerShell oder pwsh verwenden möchten: Öffnen Sie eine Shell, führen Sie `conda init powershell`aus, schließen Sie die Shell, und öffnen Sie sie erneut.</span><span class="sxs-lookup"><span data-stu-id="9e966-110">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="9e966-111">Erstellen und aktivieren Sie eine neue Conda-Umgebung namens `qsharp-env` mit den erforderlichen Paketen (einschließlich Jupyter Notebook und IQ#). Führen Sie dazu die folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="9e966-111">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="9e966-112">Führen Sie `python -c "import qsharp"` über das gleiche Terminal aus, um die Installation zu überprüfen und den lokalen Paketcache mit allen erforderlichen QDK-Komponenten aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="9e966-112">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="9e966-113">Installieren mit der .NET-CLI und PIP (erweitert)</span><span class="sxs-lookup"><span data-stu-id="9e966-113">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="9e966-114">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="9e966-114">Prerequisites:</span></span>

    - <span data-ttu-id="9e966-115">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="9e966-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="9e966-116">Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="9e966-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="9e966-117">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="9e966-117">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="9e966-118">Installieren Sie das `qsharp`-Paket. Hierbei handelt es sich um ein Python-Paket, das die Interoperabilität zwischen Q# und Python ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="9e966-118">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="9e966-119">Installieren Sie IQ#. Dies ist ein von Jupyter und Python verwendeter Kernel, der die Kernfunktionen zum Kompilieren und Ausführen von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="9e966-119">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and running Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="9e966-120">Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.</span><span class="sxs-lookup"><span data-stu-id="9e966-120">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="9e966-121">Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="9e966-121">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="9e966-122">Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="9e966-122">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="9e966-123">Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.</span><span class="sxs-lookup"><span data-stu-id="9e966-123">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="9e966-124">Das ist alles!</span><span class="sxs-lookup"><span data-stu-id="9e966-124">That's it!</span></span> <span data-ttu-id="9e966-125">Sie verfügen nun sowohl über das `qsharp`-Python-Paket als auch über den IQ#-Kernel für Jupyter, der die Kernfunktionen für das Kompilieren und Ausführen von Q#-Vorgängen in Python bereitstellt und die Verwendung von Q#-Jupyter Notebook-Instanzen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="9e966-125">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provide the core functionality for compiling and running Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="9e966-126">Auswählen Ihrer IDE</span><span class="sxs-lookup"><span data-stu-id="9e966-126">Choose your IDE</span></span>

<span data-ttu-id="9e966-127">Q# mit Python kann zwar in einer beliebigen IDE verwendet werden, wir empfehlen jedoch Visual Studio Code (VS Code) als IDE für Ihre Q#- und Python-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="9e966-127">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="9e966-128">Mit der QDK-Erweiterung für Visual Studio Code erhalten Sie Zugriff auf umfangreichere Funktionen wie Warnungen, Syntaxhervorhebung, Projektvorlagen usw.</span><span class="sxs-lookup"><span data-stu-id="9e966-128">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="9e966-129">Wenn Sie VS Code verwenden möchten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="9e966-129">If you would like to use VS Code:</span></span>

- <span data-ttu-id="9e966-130">Führen Sie die Installation von [VS Code](https://code.visualstudio.com/download) durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="9e966-130">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="9e966-131">Installieren Sie die [QDK-Erweiterung für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="9e966-131">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="9e966-132">Wenn Sie einen anderen Editor verwenden möchten, sind Sie nach Ausführung der obigen Anweisungen dafür bereit.</span><span class="sxs-lookup"><span data-stu-id="9e966-132">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-no-locq-program"></a><span data-ttu-id="9e966-133">Schreiben Ihres ersten Q#-Programms</span><span class="sxs-lookup"><span data-stu-id="9e966-133">Write your first Q# program</span></span>

<span data-ttu-id="9e966-134">Nun können Sie Ihre Installation des `qsharp`-Python-Pakets überprüfen, indem Sie ein einfaches Q#-Programm schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e966-134">Now you are ready to verify your `qsharp` Python package installation by writing and running a simple Q# program.</span></span>

1. <span data-ttu-id="9e966-135">Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="9e966-135">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="9e966-136">Erstellen Sie im gleichen Ordner wie `Operation.qs` ein Python-Programm namens `host.py`, um den Q#-Vorgang `SampleQuantumRandomNumberGenerator()` zu simulieren:</span><span class="sxs-lookup"><span data-stu-id="9e966-136">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. <span data-ttu-id="9e966-137">Führen Sie das Programm in der Umgebung aus, die Sie während der Installation erstellt haben (d. h. in der Conda- oder Python-Umgebung, in der Sie `qsharp` installiert haben):</span><span class="sxs-lookup"><span data-stu-id="9e966-137">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="9e966-138">Das Ergebnis des von Ihnen aufgerufenen Vorgangs sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e966-138">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="9e966-139">Da in diesem Fall ein zufälliges Ergebnis durch den Vorgang generiert wird, wird entweder `0` oder `1` auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9e966-139">In this case, because your operation generates a random result, you will see either `0` or `1` printed on the screen.</span></span> <span data-ttu-id="9e966-140">Wenn Sie das Programm wiederholt ausführen, sollte jedes Ergebnis ungefähr die Hälfte der Zeit angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="9e966-140">If you run the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> * <span data-ttu-id="9e966-141">Beim Python-Code handelt es sich nur um ein normales Python-Programm.</span><span class="sxs-lookup"><span data-stu-id="9e966-141">The Python code is just a normal Python program.</span></span> <span data-ttu-id="9e966-142">Sie können eine beliebige Python-Umgebung verwenden, einschließlich Python-basierter Jupyter Notebook-Instanzen, um das Python-Programm zu schreiben und Q#-Vorgänge aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9e966-142">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="9e966-143">Das Python-Programm kann Q#-Vorgänge aus allen QS-Dateien importieren, die sich im gleichen Ordner befinden wie der Python-Code.</span><span class="sxs-lookup"><span data-stu-id="9e966-143">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="9e966-144">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9e966-144">Next steps</span></span>

<span data-ttu-id="9e966-145">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung getestet haben, können Sie dieses Tutorial durchführen, um [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) zu schreiben und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9e966-145">Now that you have tested the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
