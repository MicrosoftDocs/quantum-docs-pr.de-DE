---
title: 'Erfahren Sie, wie Sie ein Q #-Projekt mit dem Quantum Development Kit (QDK) erstellen.'
description: 'Initialisieren eines Projekts für die Quantum-Entwicklung mit dem QDK und f # in der von Ihnen ausgewählten Entwicklungsumgebung'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: 8019b32a3290e2d45124ebb1eb75395f6cb758db
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327525"
---
# <a name="create-a-q-project-in-your-development-environment"></a><span data-ttu-id="503dc-103">Erstellen eines Q #-Projekts in Ihrer Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="503dc-103">Create a Q# project in your development environment</span></span>

<span data-ttu-id="503dc-104">Erfahren Sie, wie Sie ein Q #-Projekt mit dem QDK erstellen.</span><span class="sxs-lookup"><span data-stu-id="503dc-104">Learn how to create a Q# project with the QDK.</span></span>

<span data-ttu-id="503dc-105">Ein q #-Projekt enthält q #-Dateien, die den Quantum-Code enthalten, sowie ein Host Programm zum Ausführen des Quantum-Programms.</span><span class="sxs-lookup"><span data-stu-id="503dc-105">A Q# project contains Q# files containing quantum code, as well as a host program to run the quantum program.</span></span> <span data-ttu-id="503dc-106">Sie können das Host Programm in .NET-Sprachen schreiben, z. b. in c# oder in Python.</span><span class="sxs-lookup"><span data-stu-id="503dc-106">You can write the host program in .NET languages such as C#, or in Python.</span></span> <span data-ttu-id="503dc-107">Sie können auch Q #-Code in einer Jupyter Notebook ausführen, indem Sie den IQ #-Kernel verwenden.</span><span class="sxs-lookup"><span data-stu-id="503dc-107">You can also run Q# code in a Jupyter Notebook using the IQ# kernel.</span></span>

<span data-ttu-id="503dc-108">Wählen Sie in den folgenden Abschnitten Ihre Entwicklungsumgebung und Sprache aus:</span><span class="sxs-lookup"><span data-stu-id="503dc-108">Choose your development environment and language from the sections below:</span></span>

* [<span data-ttu-id="503dc-109">Python</span><span class="sxs-lookup"><span data-stu-id="503dc-109">Python</span></span>](#create-a-python-project)
* [<span data-ttu-id="503dc-110">Jupyter Notebook-Instanzen in Q#</span><span class="sxs-lookup"><span data-stu-id="503dc-110">Q# Jupyter Notebooks</span></span>](#create-a-q-jupyter-notebook-project)
* [<span data-ttu-id="503dc-111">C# mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="503dc-111">C# with Visual Studio</span></span>](#create-a-c-project-on-windows-using-visual-studio)
* [<span data-ttu-id="503dc-112">C# mit vs Code</span><span class="sxs-lookup"><span data-stu-id="503dc-112">C# with VS Code</span></span>](#create-a-c-project-using-vs-code)
* [<span data-ttu-id="503dc-113">C# mit der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="503dc-113">C# with the command line</span></span>](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a><span data-ttu-id="503dc-114">Erstellen eines Python-Projekts</span><span class="sxs-lookup"><span data-stu-id="503dc-114">Create a Python project</span></span>

1. <span data-ttu-id="503dc-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="503dc-115">Pre-requisites</span></span>

     * <span data-ttu-id="503dc-116">Installieren des [quantumentwicklungskit für python](xref:microsoft.quantum.install.python)</span><span class="sxs-lookup"><span data-stu-id="503dc-116">Install the [Quantum Development Kit for Python](xref:microsoft.quantum.install.python)</span></span>

1. <span data-ttu-id="503dc-117">Erstellen Sie einen Ordner für das Projekt, und navigieren Sie zu diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="503dc-117">Create a folder for your project, and navigate to that folder</span></span>

1. <span data-ttu-id="503dc-118">Erstellen Sie eine q #-Datei mit dem Namen `Operation.qs` , und fügen Sie Ihr den q #-Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="503dc-118">Create a Q# file called `Operation.qs`, and add your Q# code to it.</span></span> <span data-ttu-id="503dc-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503dc-119">For example:</span></span>

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. <span data-ttu-id="503dc-120">Erstellen Sie eine python-Hostdatei namens `host.py` , um den Q #-Vorgang aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="503dc-120">Create a python host file called `host.py` to call your Q# operation.</span></span> <span data-ttu-id="503dc-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="503dc-121">For example:</span></span>

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. <span data-ttu-id="503dc-122">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="503dc-122">Run the program:</span></span>

    ```bash
    python host.py
    ```

1. <span data-ttu-id="503dc-123">Überprüfen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="503dc-123">Verify the output.</span></span> <span data-ttu-id="503dc-124">Ihr Programm sollte die folgenden Zeilen ausgeben:</span><span class="sxs-lookup"><span data-stu-id="503dc-124">Your program should output the following lines:</span></span>

    ```bash
    Hello from quantum world!
    0
    ```

<span data-ttu-id="503dc-125">Sie können nun mit der Entwicklung des Quantums Programm fortfahren.</span><span class="sxs-lookup"><span data-stu-id="503dc-125">You can now continue to develop your quantum program.</span></span>

## <a name="create-a-q-jupyter-notebook-project"></a><span data-ttu-id="503dc-126">Erstellen eines Q # Jupyter Notebook-Projekts</span><span class="sxs-lookup"><span data-stu-id="503dc-126">Create a Q# Jupyter Notebook project</span></span>

1. <span data-ttu-id="503dc-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="503dc-127">Pre-requisites</span></span>

    * <span data-ttu-id="503dc-128">Installieren des [quantumentwicklungskit für jupyter-Notebooks](xref:microsoft.quantum.install.jupyter)</span><span class="sxs-lookup"><span data-stu-id="503dc-128">Install the [Quantum Development Kit for Jupyter Notebooks](xref:microsoft.quantum.install.jupyter)</span></span>

1. <span data-ttu-id="503dc-129">Führen Sie den folgenden Befehl aus, um den Notebookserver zu starten:</span><span class="sxs-lookup"><span data-stu-id="503dc-129">Run the following command to start the notebook server:</span></span>

    ```bash
    jupyter notebook
    ```

1. <span data-ttu-id="503dc-130">Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="503dc-130">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="503dc-131">Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span><span class="sxs-lookup"><span data-stu-id="503dc-131">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

1. <span data-ttu-id="503dc-132">Eine jupyter-Seite wird im Browser angezeigt.</span><span class="sxs-lookup"><span data-stu-id="503dc-132">A Jupyter page appears in the browser.</span></span> <span data-ttu-id="503dc-133">Wählen Sie auf der Registerkarte **Dateien** die Option **New**  >  **Q #** aus, um eine Jupyter Notebook mit einem Q #-Kernel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="503dc-133">On the **Files** tab, select **New** > **Q#** to create a Jupyter Notebook with a Q# kernel.</span></span> <span data-ttu-id="503dc-134">Fügen Sie den folgenden Code in die erste Notebook-Zelle ein:</span><span class="sxs-lookup"><span data-stu-id="503dc-134">Add the following code to the first notebook cell:</span></span>

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. <span data-ttu-id="503dc-135">Wählen Sie **Zelle**Zellen  >  **Ausführen** aus, um das Notebook auszuführen.</span><span class="sxs-lookup"><span data-stu-id="503dc-135">Select **Cell** > **Run Cells** to run the notebook.</span></span> <span data-ttu-id="503dc-136">`SayHello`wird in Kürze in der Zellen Ausgabe angezeigt:</span><span class="sxs-lookup"><span data-stu-id="503dc-136">`SayHello` will soon appear in the cell output:</span></span>

    ![Jupyter Notebook Zelle mit Q #-Code](~/media/install-guide-jupyter.png)

    <span data-ttu-id="503dc-138">Bei der Ausführung in jupyter-Notebooks wird der Q #-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="503dc-138">When running in Jupyter Notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

1. <span data-ttu-id="503dc-139">Simulieren Sie auf einem Quantencomputer in einer neuen Zelle die Ausführung des gerade erstellten Vorgangs mithilfe der `%simulate`-Magic:</span><span class="sxs-lookup"><span data-stu-id="503dc-139">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

    ![Jupyter Notebook Zelle mit "% simulieren" Magic](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="503dc-141">Auf dem Bildschirm sollte die Nachricht zusammen mit dem Ergebnis des von Ihnen aufgerufenen Vorgangs angezeigt werden (in diesem Fall: leer).</span><span class="sxs-lookup"><span data-stu-id="503dc-141">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>

<span data-ttu-id="503dc-142">Sie können jetzt weitere Q #-Vorgänge hinzufügen, um die Quantum-Entwicklung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="503dc-142">You can now add other Q# operations to continue your quantum development.</span></span>

## <a name="create-a-c-project-on-windows-using-visual-studio"></a><span data-ttu-id="503dc-143">Erstellen eines c#-Projekts unter Windows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="503dc-143">Create a C# project on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="503dc-144">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="503dc-144">Pre-requisites</span></span>

    * <span data-ttu-id="503dc-145">Installieren der [Quantum Development Kit-Erweiterung für Visual Studio](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="503dc-145">Install the [Quantum Development Kit extension for Visual Studio](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="503dc-146">Erstellen einer neuen Q#-Anwendung</span><span class="sxs-lookup"><span data-stu-id="503dc-146">Create a new Q# application</span></span>

    * <span data-ttu-id="503dc-147">Wechseln Sie zu **Datei**  ->  **Neues**  ->  **Projekt** .</span><span class="sxs-lookup"><span data-stu-id="503dc-147">Go to **File** -> **New** -> **Project**</span></span>
    * <span data-ttu-id="503dc-148">Geben Sie im Suchfeld als Suchbegriff `Q#` ein.</span><span class="sxs-lookup"><span data-stu-id="503dc-148">Type `Q#` in the search box</span></span>
    * <span data-ttu-id="503dc-149">Wählen Sie **Q#-Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="503dc-149">Select **Q# Application**</span></span>
    * <span data-ttu-id="503dc-150">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="503dc-150">Select **Next**</span></span>
    * <span data-ttu-id="503dc-151">Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="503dc-151">Choose a name and location for your application</span></span>
    * <span data-ttu-id="503dc-152">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="503dc-152">Select **Create**</span></span>

1. <span data-ttu-id="503dc-153">Untersuchen des Projekts</span><span class="sxs-lookup"><span data-stu-id="503dc-153">Inspect the project</span></span>

    <span data-ttu-id="503dc-154">Es sollten zwei Dateien erstellt worden sein: `Driver.cs` (C#-Hostanwendung) und `Operation.qs` (Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung auf der Konsole definiert wird).</span><span class="sxs-lookup"><span data-stu-id="503dc-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

1. <span data-ttu-id="503dc-155">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="503dc-155">Run the application</span></span>

    * <span data-ttu-id="503dc-156">**Debuggen**  ->  **Starten ohne Debugging** auswählen</span><span class="sxs-lookup"><span data-stu-id="503dc-156">Select **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="503dc-157">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="503dc-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

<span data-ttu-id="503dc-158">Sie können jetzt die Quantum-Entwicklung mit Visual Studio fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="503dc-158">You can now continue your quantum development using Visual Studio</span></span>

> [!NOTE]
> * <span data-ttu-id="503dc-159">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="503dc-159">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="create-a-c-project-using-vs-code"></a><span data-ttu-id="503dc-160">Erstellen eines c#-Projekts mit vs Code</span><span class="sxs-lookup"><span data-stu-id="503dc-160">Create a C# project, using VS Code</span></span>

1. <span data-ttu-id="503dc-161">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="503dc-161">Pre-requisites</span></span>

    * <span data-ttu-id="503dc-162">Installieren Sie die [Quantum Development Kit-Erweiterung für vs Code](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="503dc-162">Install the [Quantum Development Kit extension for VS Code](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="503dc-163">Erstellen eines neuen Projekts:</span><span class="sxs-lookup"><span data-stu-id="503dc-163">Create a new project:</span></span>

    * <span data-ttu-id="503dc-164">Gehe zu **Anzeige**-  ->  **Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="503dc-164">Go to **View** -> **Command Palette**</span></span>
    * <span data-ttu-id="503dc-165">Wählen Sie **Q #: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="503dc-165">Select **Q#: Create New Project**</span></span>
    * <span data-ttu-id="503dc-166">**Eigenständige Konsolenanwendung** auswählen</span><span class="sxs-lookup"><span data-stu-id="503dc-166">Select **Standalone console application**</span></span>
    * <span data-ttu-id="503dc-167">Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="503dc-167">Navigate to the location on the file system where you would like to create the application</span></span>
    * <span data-ttu-id="503dc-168">Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).</span><span class="sxs-lookup"><span data-stu-id="503dc-168">Click on the **Open new project...** button, once the project has been created</span></span>

1. <span data-ttu-id="503dc-169">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="503dc-169">Run the application:</span></span>

    * <span data-ttu-id="503dc-170">Zum **Terminal**  ->  **neuen Terminal** wechseln</span><span class="sxs-lookup"><span data-stu-id="503dc-170">Go to **Terminal** -> **New Terminal**</span></span>
    * <span data-ttu-id="503dc-171">Geben Sie `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="503dc-171">Enter `dotnet run`</span></span>
    * <span data-ttu-id="503dc-172">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="503dc-172">You should see the following text in the output window `Hello quantum world!`</span></span>

<span data-ttu-id="503dc-173">Nun können Sie die Quantum-Entwicklung mit Visual Studio Code fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="503dc-173">You can now continue your quantum development using Visual Studio Code.</span></span>

> [!NOTE]
> * <span data-ttu-id="503dc-174">Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="503dc-174">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="503dc-175">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="503dc-175">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a><span data-ttu-id="503dc-176">Erstellen eines c#-Projekts mit dem `dotnet` Befehlszeilen Tool</span><span class="sxs-lookup"><span data-stu-id="503dc-176">Create a C# project, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="503dc-177">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="503dc-177">Pre-requisites</span></span>

    * <span data-ttu-id="503dc-178">Installieren des [quantumentwicklungskit für die Befehlszeile](xref:microsoft.quantum.install.standalone)</span><span class="sxs-lookup"><span data-stu-id="503dc-178">Install the [Quantum Development Kit for the command line](xref:microsoft.quantum.install.standalone)</span></span>

1. <span data-ttu-id="503dc-179">Erstellen einer neuen Anwendung</span><span class="sxs-lookup"><span data-stu-id="503dc-179">Create a new application</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o <project name>
    ```

1. <span data-ttu-id="503dc-180">Navigieren Sie zum neuen Anwendungsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="503dc-180">Navigate to the new application directory</span></span>

    ```bash
    cd <project name>
    ```

    <span data-ttu-id="503dc-181">Es sollten zwei Dateien und die Projektdateien der Anwendung erstellt worden sein: eine Q#-Datei (`Operation.qs`) und eine C#-Hostdatei (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="503dc-181">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

1. <span data-ttu-id="503dc-182">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="503dc-182">Run the application</span></span>

    ```dotnetcli
    dotnet run
    ```

    <span data-ttu-id="503dc-183">Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="503dc-183">You should see the following output: `Hello quantum world!`</span></span>

<span data-ttu-id="503dc-184">Mit Befehlszeilen Tools können Sie nun die Quantum-Entwicklung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="503dc-184">You now continue your quantum development, using command line tools.</span></span>

## <a name="next-steps"></a><span data-ttu-id="503dc-185">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="503dc-185">Next steps</span></span>

<span data-ttu-id="503dc-186">Nachdem Sie ein Projekt in Ihrer bevorzugten Umgebung erstellt haben, können Sie die Quantum-Entwicklung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="503dc-186">Now that you have created a project in your preferred environment, you can continue your quantum development.</span></span>
