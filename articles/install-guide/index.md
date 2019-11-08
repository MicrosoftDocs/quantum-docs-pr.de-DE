---
title: Installieren des Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 580ac14f2e839d723884a96e9c5fd336ebcb5da0
ms.sourcegitcommit: 30fcb35986b43388ad65dfb876eb3ad8ad0533ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2019
ms.locfileid: "73799161"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="81b00-102">Installieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="81b00-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="81b00-103">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können.</span><span class="sxs-lookup"><span data-stu-id="81b00-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="81b00-104">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="81b00-104">The QDK consists of:</span></span>

- <span data-ttu-id="81b00-105">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="81b00-105">the Q# programming language</span></span>
- <span data-ttu-id="81b00-106">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="81b00-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="81b00-107">Hostanwendung (in Python oder einer .NET-Sprache geschrieben), mit der in Q# geschriebene Quantenvorgänge ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="81b00-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="81b00-108">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="81b00-108">tools to facilitate your development</span></span>

<span data-ttu-id="81b00-109">Je nach ausgewählter Entwicklungsumgebung müssen unterschiedliche Installationsschritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="81b00-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="81b00-110">Wählen Sie Ihre Umgebung in den Abschnitten unten aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="81b00-111">Entwickeln mit Python</span><span class="sxs-lookup"><span data-stu-id="81b00-111">Develop with Python</span></span>

<span data-ttu-id="81b00-112">Das qsharp-Paket für Python vereinfacht das Simulieren von Q#-Vorgängen und -Funktionen in Python.</span><span class="sxs-lookup"><span data-stu-id="81b00-112">The qsharp package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="81b00-113">IQ# (ausgesprochen „aɪ-kjuː-ʃɑrp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="81b00-113">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python that provides the core functionality for compiling and simulating Q# operations.</span></span>

1. <span data-ttu-id="81b00-114">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="81b00-114">Pre-requisites</span></span>

    - <span data-ttu-id="81b00-115">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="81b00-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="81b00-116">Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="81b00-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="81b00-117">.NET Core SDK 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="81b00-117">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="81b00-118">Installieren Sie das Paket `qsharp`.</span><span class="sxs-lookup"><span data-stu-id="81b00-118">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="81b00-119">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="81b00-119">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="81b00-120">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-120">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="81b00-121">Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="81b00-121">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - <span data-ttu-id="81b00-122">Erstellen Sie ein Python-Programm mit dem Namen `hello_world.py`, um den Q#-Vorgang `SayHello()` aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="81b00-122">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="81b00-123">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="81b00-123">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="81b00-124">Überprüfen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="81b00-124">Verify the output.</span></span> <span data-ttu-id="81b00-125">Ihr Programm sollte die folgenden Zeilen ausgeben:</span><span class="sxs-lookup"><span data-stu-id="81b00-125">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="81b00-126">Entwickeln mit Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="81b00-126">Develop with Jupyter notebooks</span></span>

<span data-ttu-id="81b00-127">Jupyter Notebook ist ein beliebtes Tool in der Wissenschaft und Forschung sowie bei der onlinebasierten kollaborativen Programmierung, das sich durch direkte Codeausführung (jetzt auch für Q#-Code) auszeichnet sowie Anweisungen, Hinweise und andere Inhalte bietet.</span><span class="sxs-lookup"><span data-stu-id="81b00-127">A favorite of academic settings, scientific labs, and online-based collaborative programming, Jupyter Notebooks offer in-place code execution—now including Q# code—along with instructions, notes, and other content.</span></span>  <span data-ttu-id="81b00-128">Hier sind die Schritte aufgeführt, die Sie zum Erstellen eigener Q#-Notebooks ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="81b00-128">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="81b00-129">IQ# (ausgesprochen „i-q-sharp“) ist eine hauptsächlich von Jupyter und Python genutzte Erweiterung für das .NET Core SDK, die die Kernfunktionen für das Kompilieren und Simulieren von Q#-Vorgängen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="81b00-129">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>


1. <span data-ttu-id="81b00-130">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="81b00-130">Pre-requisites</span></span>

    - <span data-ttu-id="81b00-131">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="81b00-131">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="81b00-132">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="81b00-132">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="81b00-133">.NET Core SDK 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="81b00-133">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="81b00-134">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="81b00-134">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="81b00-135">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-135">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="81b00-136">Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:</span><span class="sxs-lookup"><span data-stu-id="81b00-136">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="81b00-137">Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="81b00-137">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="81b00-138">Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="81b00-138">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="81b00-139">Erstellen Sie ein Jupyter-Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="81b00-139">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="81b00-140">Führen Sie diese Zelle des Notebooks aus:</span><span class="sxs-lookup"><span data-stu-id="81b00-140">Run this cell of the notebook:</span></span>

        ![Zelle im Jupyter-Notebook mit Q#-Code](~/media/install-guide-jupyter.png)

        <span data-ttu-id="81b00-142">In der Ausgabe der Zelle sollte `SayHello` angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="81b00-142">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="81b00-143">Bei der Ausführung in Jupyter-Notebooks wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-143">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="81b00-144">Simulieren Sie auf einem Quantencomputer in einer neuen Zelle die Ausführung des gerade erstellten Vorgangs mithilfe der `%simulate`-Magic:</span><span class="sxs-lookup"><span data-stu-id="81b00-144">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

        ![Zelle im Jupyter-Notebook mit %simulate-Magic](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="81b00-146">Auf dem Bildschirm sollte die Nachricht zusammen mit dem Ergebnis des von Ihnen aufgerufenen Vorgangs angezeigt werden (in diesem Fall: leer).</span><span class="sxs-lookup"><span data-stu-id="81b00-146">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>


## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="81b00-147">Entwickeln mit C# unter Windows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81b00-147">Develop with C# on Windows, using Visual Studio</span></span>

<span data-ttu-id="81b00-148">Visual Studio bietet eine umfangreiche Umgebung für die Entwicklung von Q#-Programmen sowie großartige Features wie Codevervollständigung und Syntaxhervorhebung, die Entwickler bei der Erstellung von Anwendungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="81b00-148">Visual Studio offers a rich environment for developing Q# programs, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="81b00-149">Die Q#-Erweiterung für Visual Studio enthält Vorlagen für Q#-Dateien und -Projekte sowie Syntaxhervorhebung und IntelliSense-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="81b00-149">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting and IntelliSense support.</span></span>


1. <span data-ttu-id="81b00-150">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="81b00-150">Pre-requisites</span></span>

    - <span data-ttu-id="81b00-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload</span><span class="sxs-lookup"><span data-stu-id="81b00-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="81b00-152">Installieren der Q#-Erweiterung für Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81b00-152">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="81b00-153">Herunterladen der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="81b00-153">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="81b00-154">Hinzufügen der Erweiterung zu Visual Studio</span><span class="sxs-lookup"><span data-stu-id="81b00-154">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="81b00-155">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-155">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="81b00-156">Erstellen einer neuen Q#-Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-156">Create a new Q# application</span></span>

        - <span data-ttu-id="81b00-157">Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="81b00-157">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="81b00-158">Geben Sie im Suchfeld als Suchbegriff `Q#` ein.</span><span class="sxs-lookup"><span data-stu-id="81b00-158">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="81b00-159">Wählen Sie **Q#-Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-159">Select **Q# Application**</span></span>
        - <span data-ttu-id="81b00-160">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-160">Select **Next**</span></span>
        - <span data-ttu-id="81b00-161">Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-161">Choose a name and location for your application</span></span>
        - <span data-ttu-id="81b00-162">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="81b00-162">Select **Create**</span></span>

    - <span data-ttu-id="81b00-163">Untersuchen des Projekts</span><span class="sxs-lookup"><span data-stu-id="81b00-163">Inspect the project</span></span>

        <span data-ttu-id="81b00-164">Es sollten zwei Dateien erstellt worden sein: `Driver.cs` (C#-Hostanwendung) und `Operation.qs` (Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung auf der Konsole definiert wird).</span><span class="sxs-lookup"><span data-stu-id="81b00-164">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="81b00-165">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-165">Run the application</span></span>

        - <span data-ttu-id="81b00-166">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-166">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="81b00-167">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="81b00-167">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="81b00-168">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="81b00-168">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-visual-studio-code"></a><span data-ttu-id="81b00-169">Entwickeln mit C# und Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="81b00-169">Develop with C#, using Visual Studio Code</span></span>

<span data-ttu-id="81b00-170">Visual Studio Code (VS Code) bietet eine umfangreiche Umgebung für die Entwicklung von Q#-Programmen in zahlreichen verschiedenen Computerumgebungen (einschließlich Windows, Linux und Mac) sowie großartige Features wie Codevervollständigung und Syntaxhervorhebung, die Entwickler bei der Erstellung von Anwendungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="81b00-170">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs across many multiple computer environments, including Windows, Linux and Mac, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="81b00-171">Die Q#-VS Code-Erweiterung beinhaltet Syntaxhervorhebung und Q#-Codeausschnitte.</span><span class="sxs-lookup"><span data-stu-id="81b00-171">The Q# VS Code extension contains syntax highlighting, and Q# code snippets.</span></span>

1. <span data-ttu-id="81b00-172">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="81b00-172">Pre-requisites</span></span>

   - [<span data-ttu-id="81b00-173">VS-Code</span><span class="sxs-lookup"><span data-stu-id="81b00-173">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="81b00-174">.NET Core SDK 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="81b00-174">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="81b00-175">Installieren der VS Code-Erweiterung für Quantum</span><span class="sxs-lookup"><span data-stu-id="81b00-175">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="81b00-176">Installieren Sie die [VS Code-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="81b00-176">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="81b00-177">Installieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="81b00-177">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="81b00-178">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="81b00-178">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="81b00-179">Wählen Sie **Q#: Install project templates** (Q#: Projektvorlagen installieren) aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-179">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="81b00-180">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="81b00-180">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="81b00-181">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-181">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="81b00-182">Erstellen eines neuen Projekts:</span><span class="sxs-lookup"><span data-stu-id="81b00-182">Create a new project:</span></span>

        - <span data-ttu-id="81b00-183">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="81b00-183">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="81b00-184">Wählen Sie **Q#: Create New Project** (Q#: Neues Projekt erstellen) aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-184">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="81b00-185">Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="81b00-185">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="81b00-186">Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).</span><span class="sxs-lookup"><span data-stu-id="81b00-186">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="81b00-187">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="81b00-187">Run the application:</span></span>

        - <span data-ttu-id="81b00-188">Navigieren Sie zu **Debuggen** -> **Ohne Debuggen starten**.</span><span class="sxs-lookup"><span data-stu-id="81b00-188">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="81b00-189">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="81b00-189">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="81b00-190">Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81b00-190">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="81b00-191">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="81b00-191">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="81b00-192">Entwickeln mit C# per Befehlszeilentool `dotnet`</span><span class="sxs-lookup"><span data-stu-id="81b00-192">Develop with C#, using the `dotnet` command-line tool</span></span>

<span data-ttu-id="81b00-193">Natürlich können Sie Q#-Programme auch über die Befehlszeile erstellen und ausführen, indem Sie einfach das .NET Core SDK und die QDK-Projektvorlagen installieren.</span><span class="sxs-lookup"><span data-stu-id="81b00-193">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="81b00-194">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="81b00-194">Pre-requisites</span></span>

    - [<span data-ttu-id="81b00-195">.NET Core SDK 3.0 oder höher</span><span class="sxs-lookup"><span data-stu-id="81b00-195">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="81b00-196">Installieren der Quantum-Projektvorlagen für .NET</span><span class="sxs-lookup"><span data-stu-id="81b00-196">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="81b00-197">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="81b00-197">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="81b00-198">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-198">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="81b00-199">Erstellen einer neuen Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-199">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="81b00-200">Navigieren Sie zum neuen Anwendungsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="81b00-200">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="81b00-201">Es sollten zwei Dateien und die Projektdateien der Anwendung erstellt worden sein: eine Q#-Datei (`Operation.qs`) und eine C#-Hostdatei (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="81b00-201">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="81b00-202">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="81b00-202">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="81b00-203">Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="81b00-203">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="81b00-204">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="81b00-204">What's next?</span></span>

<span data-ttu-id="81b00-205">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="81b00-205">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
