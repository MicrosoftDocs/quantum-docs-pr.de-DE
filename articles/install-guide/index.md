---
title: Installieren des Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 3ec53934436b47908fd4d794a98933010f6059a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035306"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="4c632-102">Installieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="4c632-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="4c632-103">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können.</span><span class="sxs-lookup"><span data-stu-id="4c632-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="4c632-104">Das QDK umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4c632-104">The QDK consists of:</span></span>

- <span data-ttu-id="4c632-105">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="4c632-105">the Q# programming language</span></span>
- <span data-ttu-id="4c632-106">Bibliotheken zur Abstraktion komplexer Funktionen in Q#</span><span class="sxs-lookup"><span data-stu-id="4c632-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="4c632-107">Hostanwendung (in Python oder einer .NET-Sprache geschrieben), mit der in Q# geschriebene Quantenvorgänge ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="4c632-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="4c632-108">Tools für die Entwicklung</span><span class="sxs-lookup"><span data-stu-id="4c632-108">tools to facilitate your development</span></span>

<span data-ttu-id="4c632-109">Je nach ausgewählter Entwicklungsumgebung müssen unterschiedliche Installationsschritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4c632-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="4c632-110">Wählen Sie Ihre Umgebung in den Abschnitten unten aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="4c632-111">Entwickeln mit Python</span><span class="sxs-lookup"><span data-stu-id="4c632-111">Develop with Python</span></span>

1. <span data-ttu-id="4c632-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4c632-112">Pre-requisites</span></span>

    - <span data-ttu-id="4c632-113">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c632-113">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="4c632-114">Der [PIP](https://pip.pypa.io/en/stable/installing)-Python-Paket-Manager</span><span class="sxs-lookup"><span data-stu-id="4c632-114">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="4c632-115">.NET Core SDK 2.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c632-115">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4c632-116">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="4c632-116">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="4c632-117">Installieren Sie das Paket `qsharp`.</span><span class="sxs-lookup"><span data-stu-id="4c632-117">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="4c632-118">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4c632-119">Erstellen Sie einen minimalen Q#-Vorgang, indem Sie eine Datei mit dem Namen `Operation.qs` erstellen und ihr den folgenden Code hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="4c632-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

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

    - <span data-ttu-id="4c632-120">Erstellen Sie ein Python-Programm mit dem Namen `hello_world.py`, um den Q#-Vorgang `SayHello()` aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="4c632-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="4c632-121">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="4c632-121">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="4c632-122">Überprüfen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4c632-122">Verify the output.</span></span> <span data-ttu-id="4c632-123">Ihr Programm sollte die folgenden Zeilen ausgeben:</span><span class="sxs-lookup"><span data-stu-id="4c632-123">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="4c632-124">Entwickeln mit Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="4c632-124">Develop with Jupyter notebooks</span></span>

1. <span data-ttu-id="4c632-125">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4c632-125">Pre-requisites</span></span>

    - <span data-ttu-id="4c632-126">[Python](https://www.python.org/downloads/) 3.6 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c632-126">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="4c632-127">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="4c632-127">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="4c632-128">.NET Core SDK 2.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c632-128">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4c632-129">Installieren Sie das Paket `iqsharp`.</span><span class="sxs-lookup"><span data-stu-id="4c632-129">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="4c632-130">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-130">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4c632-131">Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:</span><span class="sxs-lookup"><span data-stu-id="4c632-131">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="4c632-132">Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4c632-132">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="4c632-133">Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="4c632-133">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="4c632-134">Erstellen Sie ein Jupyter-Notebook mit einem Q#-Kernel, und fügen Sie in der ersten Notebookzelle den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="4c632-134">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="4c632-135">Führen Sie diese Zelle des Notebooks aus:</span><span class="sxs-lookup"><span data-stu-id="4c632-135">Run this cell of the notebook:</span></span>

        ![Zelle im Jupyter-Notebook](~/media/install-guide-jupyter.png)

        <span data-ttu-id="4c632-137">In der Ausgabe der Zelle sollte `SayHello` angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4c632-137">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="4c632-138">Bei der Ausführung in Jupyter-Notebooks wird der Q#-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-138">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="4c632-139">Entwickeln mit C# unter Windows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4c632-139">Develop with C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="4c632-140">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4c632-140">Pre-requisites</span></span>

    - <span data-ttu-id="4c632-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload</span><span class="sxs-lookup"><span data-stu-id="4c632-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="4c632-142">Installieren der Q#-Erweiterung für Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4c632-142">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="4c632-143">Herunterladen der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="4c632-143">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="4c632-144">Hinzufügen der Erweiterung zu Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4c632-144">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="4c632-145">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-145">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4c632-146">Erstellen einer neuen Q#-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-146">Create a new Q# application</span></span>

        - <span data-ttu-id="4c632-147">Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="4c632-147">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="4c632-148">Geben Sie im Suchfeld als Suchbegriff `Q#` ein.</span><span class="sxs-lookup"><span data-stu-id="4c632-148">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="4c632-149">Wählen Sie **Q#-Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-149">Select **Q# Application**</span></span>
        - <span data-ttu-id="4c632-150">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-150">Select **Next**</span></span>
        - <span data-ttu-id="4c632-151">Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-151">Choose a name and location for your application</span></span>
        - <span data-ttu-id="4c632-152">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="4c632-152">Select **Create**</span></span>

    - <span data-ttu-id="4c632-153">Untersuchen des Projekts</span><span class="sxs-lookup"><span data-stu-id="4c632-153">Inspect the project</span></span>

        <span data-ttu-id="4c632-154">Es sollten zwei Dateien erstellt worden sein: `Driver.cs` (C#-Hostanwendung) und `Operation.qs` (Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung auf der Konsole definiert wird).</span><span class="sxs-lookup"><span data-stu-id="4c632-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="4c632-155">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-155">Run the application</span></span>

        - <span data-ttu-id="4c632-156">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-156">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="4c632-157">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4c632-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="4c632-158">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="4c632-158">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-vs-code"></a><span data-ttu-id="4c632-159">Entwickeln mit C# per VS Code</span><span class="sxs-lookup"><span data-stu-id="4c632-159">Develop with C#, using VS Code</span></span>

1. <span data-ttu-id="4c632-160">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4c632-160">Pre-requisites</span></span>

   - [<span data-ttu-id="4c632-161">VS-Code</span><span class="sxs-lookup"><span data-stu-id="4c632-161">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="4c632-162">.NET Core SDK 2.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c632-162">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4c632-163">Installieren der VS Code-Erweiterung für Quantum</span><span class="sxs-lookup"><span data-stu-id="4c632-163">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="4c632-164">Installieren Sie die [VS Code-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="4c632-164">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="4c632-165">Installieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="4c632-165">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="4c632-166">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="4c632-166">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="4c632-167">Wählen Sie **Q#: Install project templates** (Q#: Projektvorlagen installieren) aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-167">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="4c632-168">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c632-168">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="4c632-169">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-169">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4c632-170">Erstellen eines neuen Projekts:</span><span class="sxs-lookup"><span data-stu-id="4c632-170">Create a new project:</span></span>

        - <span data-ttu-id="4c632-171">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="4c632-171">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="4c632-172">Wählen Sie **Q#: Create New Project** (Q#: Neues Projekt erstellen) aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-172">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="4c632-173">Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="4c632-173">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="4c632-174">Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).</span><span class="sxs-lookup"><span data-stu-id="4c632-174">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="4c632-175">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="4c632-175">Run the application:</span></span>

        - <span data-ttu-id="4c632-176">Navigieren Sie zu **Debuggen** -> **Ohne Debuggen starten**.</span><span class="sxs-lookup"><span data-stu-id="4c632-176">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="4c632-177">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="4c632-177">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="4c632-178">Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c632-178">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="4c632-179">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="4c632-179">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="4c632-180">Entwickeln mit C# per Befehlszeilentool `dotnet`</span><span class="sxs-lookup"><span data-stu-id="4c632-180">Develop with C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="4c632-181">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="4c632-181">Pre-requisites</span></span>

    - [<span data-ttu-id="4c632-182">.NET Core SDK 2.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="4c632-182">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="4c632-183">Installieren der Quantum-Projektvorlagen für .NET</span><span class="sxs-lookup"><span data-stu-id="4c632-183">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="4c632-184">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c632-184">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="4c632-185">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-185">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="4c632-186">Erstellen einer neuen Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-186">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="4c632-187">Navigieren Sie zum neuen Anwendungsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="4c632-187">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="4c632-188">Es sollten zwei Dateien und die Projektdateien der Anwendung erstellt worden sein: eine Q#-Datei (`Operation.qs`) und eine C#-Hostdatei (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="4c632-188">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="4c632-189">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="4c632-189">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="4c632-190">Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="4c632-190">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="4c632-191">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="4c632-191">What's next?</span></span>

<span data-ttu-id="4c632-192">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c632-192">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
