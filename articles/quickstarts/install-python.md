---
title: Entwickeln mit Q# und Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: ec5e66e0c85d89888a8ff1e7d6bf18bf89ff44ac
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871585"
---
# <a name="develop-with-q-and-python"></a><span data-ttu-id="6fcbb-102">Entwickeln mit Q# und Python</span><span class="sxs-lookup"><span data-stu-id="6fcbb-102">Develop with Q# and Python</span></span>

<span data-ttu-id="6fcbb-103">Installieren Sie das QDK, um Python-Hostprogramme zum Aufrufen von Q#-Vorgängen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-103">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="6fcbb-104">Installieren des `qsharp`-Python-Pakets</span><span class="sxs-lookup"><span data-stu-id="6fcbb-104">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="6fcbb-105">Installation mithilfe von Conda (empfohlen)</span><span class="sxs-lookup"><span data-stu-id="6fcbb-105">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="6fcbb-106">Installieren Sie [Miniconda](https://docs.conda.io/en/latest/miniconda.html) oder [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="6fcbb-106">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="6fcbb-107">**Hinweis:** Eine 64-Bit-Installation ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-107">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="6fcbb-108">Öffnen Sie eine Anaconda-Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-108">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="6fcbb-109">Wenn Sie PowerShell oder pwsh verwenden möchten: Öffnen Sie eine Shell, führen Sie `conda init powershell`aus, schließen Sie die Shell, und öffnen Sie sie erneut.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-109">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="6fcbb-110">Erstellen und aktivieren Sie eine neue Conda-Umgebung namens `qsharp-env` mit den erforderlichen Paketen (einschließlich Jupyter Notebook und IQ#), indem Sie die folgenden Befehle ausführen:</span><span class="sxs-lookup"><span data-stu-id="6fcbb-110">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="6fcbb-111">Führen Sie `python -c "import qsharp"` über das gleiche Terminal aus, um die Installation zu überprüfen und den lokalen Paketcache mit allen erforderlichen QDK-Komponenten aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-111">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="6fcbb-112">Installieren mit der .NET-CLI und PIP (erweitert)</span><span class="sxs-lookup"><span data-stu-id="6fcbb-112">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="6fcbb-113">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="6fcbb-113">Prerequisites:</span></span>

    - <span data-ttu-id="6fcbb-114">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="6fcbb-114">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="6fcbb-115">Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="6fcbb-115">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="6fcbb-116">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="6fcbb-116">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="6fcbb-117">Installieren Sie das `qsharp`-Paket. Hierbei handelt es sich um ein Python-Paket, das die Interoperabilität zwischen Q# und Python ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-117">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="6fcbb-118">Installieren Sie IQ#. Dies ist ein von Jupyter und Python verwendeter Kernel, der die Kernfunktionen zum Kompilieren und Ausführen von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-118">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and executing Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="6fcbb-119">Wenn Sie während des Schritts `dotnet iqsharp install` einen Fehler erhalten, sollten Sie ein neues Terminalfenster öffnen und den Vorgang dann wiederholen.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-119">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="6fcbb-120">Falls der Vorgang immer noch nicht erfolgreich ist, sollten Sie mit dem installierten Tool `dotnet-iqsharp` (unter Windows `dotnet-iqsharp.exe`) Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="6fcbb-120">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="6fcbb-121">Ersetzen Sie hierbei `/path/to/dotnet-iqsharp` durch den absoluten Pfad zum Tool `dotnet-iqsharp` in Ihrem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-121">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="6fcbb-122">Normalerweise finden Sie dies unter `.dotnet/tools` in Ihrem Benutzerprofilordner.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-122">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="6fcbb-123">Das ist alles!</span><span class="sxs-lookup"><span data-stu-id="6fcbb-123">That's it!</span></span> <span data-ttu-id="6fcbb-124">Sie verfügen nun sowohl über das `qsharp`-Python-Paket als auch den IQ#-Kernel für Jupyter, der die Kernfunktionen für das Kompilieren und Ausführen von Q#-Vorgängen in Python bereitstellt und Ihnen die Verwendung von Q#-Jupyter Notebooks ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-124">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provides the core functionality for compiling and executing Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="6fcbb-125">Auswählen Ihrer IDE</span><span class="sxs-lookup"><span data-stu-id="6fcbb-125">Choose your IDE</span></span>

<span data-ttu-id="6fcbb-126">Sie können Q# mit Python zwar in einer beliebigen IDE verwenden, aber wir empfehlen Ihnen dringend die Nutzung von Visual Studio Code (VS Code) als IDE für Ihre Q#/Python-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-126">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="6fcbb-127">Mit der QDK-Erweiterung für Visual Studio Code erhalten Sie Zugriff auf umfangreichere Funktionen wie Warnungen, Syntaxhervorhebung, Projektvorlagen usw.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-127">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="6fcbb-128">Wenn Sie VS Code verwenden möchten, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="6fcbb-128">If you would like to use VS Code:</span></span>

- <span data-ttu-id="6fcbb-129">Führen Sie die Installation von [VS Code](https://code.visualstudio.com/download) durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="6fcbb-129">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="6fcbb-130">Installieren Sie die [QDK-Erweiterung für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="6fcbb-130">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="6fcbb-131">Wenn Sie einen anderen Editor verwenden möchten, sind Sie nach Ausführung der obigen Anweisungen dafür bereit.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-131">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-q-program"></a><span data-ttu-id="6fcbb-132">Schreiben Ihres ersten Q#-Programms</span><span class="sxs-lookup"><span data-stu-id="6fcbb-132">Write your first Q# program</span></span>

<span data-ttu-id="6fcbb-133">Nun können Sie Ihre Installation des `qsharp`-Python-Pakets überprüfen, indem Sie ein einfaches Q#-Programm schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-133">Now you are ready to verify your `qsharp` Python package installation by writing and executing a simple Q# program.</span></span>

1. <span data-ttu-id="6fcbb-134">Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="6fcbb-134">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="6fcbb-135">Erstellen Sie im gleichen Ordner wie `Operation.qs` ein Python-Programm namens `host.py`, um den Q#-Vorgang `SampleQuantumRandomNumberGenerator()` zu simulieren:</span><span class="sxs-lookup"><span data-stu-id="6fcbb-135">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    SampleQuantumRandomNumberGenerator.simulate()
    ```

1. <span data-ttu-id="6fcbb-136">Führen Sie das Programm in der Umgebung aus, die Sie während der Installation erstellt haben (d. h. in der Conda- oder Python-Umgebung, in der Sie `qsharp` installiert haben):</span><span class="sxs-lookup"><span data-stu-id="6fcbb-136">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="6fcbb-137">Das Ergebnis des von Ihnen aufgerufenen Vorgangs sollte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-137">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="6fcbb-138">Da in diesem Fall ein zufälliges Ergebnis durch den Vorgang generiert wird, wird entweder `Zero` oder `One` auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-138">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="6fcbb-139">Wenn Sie das Programm wiederholt ausführen, sollte jedes Ergebnis ungefähr die Hälfte der Zeit angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-139">If you execute the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> * <span data-ttu-id="6fcbb-140">Beim Python-Code handelt es sich nur um ein normales Python-Programm.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-140">The Python code is just a normal Python program.</span></span> <span data-ttu-id="6fcbb-141">Sie können eine beliebige Python-Umgebung verwenden, einschließlich Python-basierter Jupyter Notebooks, um das Python-Programm zu schreiben und Q#-Vorgänge aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-141">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="6fcbb-142">Das Python-Programm kann Q#-Vorgänge aus allen QS-Dateien importieren, die sich im gleichen Ordner wie der Python-Code selbst befinden.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-142">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6fcbb-143">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="6fcbb-143">Next steps</span></span>

<span data-ttu-id="6fcbb-144">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie dieses Tutorial durchführen, um [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) zu schreiben und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6fcbb-144">Now that you have installed the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
