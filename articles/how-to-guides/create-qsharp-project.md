---
title: 'Erfahren Sie, wie Sie ein Q #-Projekt mit dem Quantum Development Kit (QDK) erstellen.'
description: 'Initialisieren eines Projekts für die Quantum-Entwicklung mit dem QDK und f # in der von Ihnen ausgewählten Entwicklungsumgebung'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: b4bec5e7a174b7e2d588331dd2093c7b23a728b0
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73444173"
---
# <a name="create-a-q-project-in-your-development-environment"></a><span data-ttu-id="af0fe-103">Erstellen eines Q #-Projekts in Ihrer Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="af0fe-103">Create a Q# project in your development environment</span></span>

<span data-ttu-id="af0fe-104">Erfahren Sie, wie Sie ein Q #-Projekt mit dem QDK erstellen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-104">Learn how to create a Q# project with the QDK.</span></span>

<span data-ttu-id="af0fe-105">Ein q #-Projekt enthält q #-Dateien, die den Quantum-Code enthalten, sowie ein Host Programm zum Ausführen des Quantum-Programms.</span><span class="sxs-lookup"><span data-stu-id="af0fe-105">A Q# project contains Q# files containing quantum code, as well as a host program to run the quantum program.</span></span> <span data-ttu-id="af0fe-106">Sie können das Host Programm in .NET-Sprachen wie C#oder in Python schreiben.</span><span class="sxs-lookup"><span data-stu-id="af0fe-106">You can write the host program in .NET languages such as C#, or in Python.</span></span> <span data-ttu-id="af0fe-107">Sie können auch Q #-Code in einem jupyter-Notebook mithilfe des IQ #-Kernels ausführen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-107">You can also run Q# code in a Jupyter notebook using the IQ# kernel.</span></span>

<span data-ttu-id="af0fe-108">Wählen Sie in den folgenden Abschnitten Ihre Entwicklungsumgebung und Sprache aus:</span><span class="sxs-lookup"><span data-stu-id="af0fe-108">Choose your development environment and language from the sections below:</span></span>

* [<span data-ttu-id="af0fe-109">Python</span><span class="sxs-lookup"><span data-stu-id="af0fe-109">Python</span></span>](#create-a-python-project)
* [<span data-ttu-id="af0fe-110">Jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="af0fe-110">Jupyter notebooks</span></span>](#create-a-jupyter-notebook-project)
* [<span data-ttu-id="af0fe-111">C#mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af0fe-111">C# with Visual Studio</span></span>](#create-a-c-project-on-windows-using-visual-studio)
* [<span data-ttu-id="af0fe-112">C#mit vs Code</span><span class="sxs-lookup"><span data-stu-id="af0fe-112">C# with VS Code</span></span>](#create-a-c-project-using-vs-code)
* [<span data-ttu-id="af0fe-113">C#mit der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="af0fe-113">C# with the command line</span></span>](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a><span data-ttu-id="af0fe-114">Erstellen eines python-Projekts</span><span class="sxs-lookup"><span data-stu-id="af0fe-114">Create a Python project</span></span>

1. <span data-ttu-id="af0fe-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af0fe-115">Pre-requisites</span></span>

     * <span data-ttu-id="af0fe-116">Das [Quantum Development Kit für python](xref:microsoft.quantum.install#develop-with-python)</span><span class="sxs-lookup"><span data-stu-id="af0fe-116">The [Quantum Development Kit for Python](xref:microsoft.quantum.install#develop-with-python)</span></span>

1. <span data-ttu-id="af0fe-117">Erstellen Sie einen Ordner für das Projekt, und navigieren Sie zu diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="af0fe-117">Create a folder for your project, and navigate to that folder</span></span>

1. <span data-ttu-id="af0fe-118">Erstellen Sie eine q #-Datei mit dem Namen `Operation.qs`, und fügen Sie Ihr den q #-Code hinzu.</span><span class="sxs-lookup"><span data-stu-id="af0fe-118">Create a Q# file called `Operation.qs`, and add your Q# code to it.</span></span> <span data-ttu-id="af0fe-119">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="af0fe-119">For example:</span></span>

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

1. <span data-ttu-id="af0fe-120">Erstellen Sie eine python-Hostdatei mit dem Namen `host.py`, um den Q #-Vorgang aufzurufen</span><span class="sxs-lookup"><span data-stu-id="af0fe-120">Create a python host file called `host.py` to call your Q# operation.</span></span> <span data-ttu-id="af0fe-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="af0fe-121">For example:</span></span>

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. <span data-ttu-id="af0fe-122">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="af0fe-122">Run the program:</span></span>

    ```bash
    python host.py
    ```

1. <span data-ttu-id="af0fe-123">Überprüfen Sie die Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="af0fe-123">Verify the output.</span></span> <span data-ttu-id="af0fe-124">Ihr Programm sollte die folgenden Zeilen ausgeben:</span><span class="sxs-lookup"><span data-stu-id="af0fe-124">Your program should output the following lines:</span></span>

    ```bash
    Hello from quantum world!
    0
    ```

<span data-ttu-id="af0fe-125">Sie können nun mit der Entwicklung des Quantums Programm fortfahren.</span><span class="sxs-lookup"><span data-stu-id="af0fe-125">You can now continue to develop your quantum program.</span></span>

## <a name="create-a-jupyter-notebook-project"></a><span data-ttu-id="af0fe-126">Erstellen eines Jupyter Notebook Projekts</span><span class="sxs-lookup"><span data-stu-id="af0fe-126">Create a Jupyter Notebook project</span></span>

1. <span data-ttu-id="af0fe-127">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af0fe-127">Pre-requisites</span></span>

    * <span data-ttu-id="af0fe-128">Das [Quantum Development Kit für jupyter-Notebooks](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)</span><span class="sxs-lookup"><span data-stu-id="af0fe-128">The [Quantum Development Kit for Jupyter notebooks](xref:microsoft.quantum.install#develop-with-jupyter-notebooks)</span></span>

1. <span data-ttu-id="af0fe-129">Führen Sie den folgenden Befehl aus, um den Notebook-Server zu starten:</span><span class="sxs-lookup"><span data-stu-id="af0fe-129">Run the following command to start the notebook server:</span></span>

    ```bash
    jupyter notebook
    ```

1. <span data-ttu-id="af0fe-130">Navigieren Sie zu der URL, die in der Befehlszeile angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="af0fe-130">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="af0fe-131">Beispiel: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="af0fe-131">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

1. <span data-ttu-id="af0fe-132">Eine jupyter-Seite wird im Browser angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af0fe-132">A Jupyter page appears in the browser.</span></span> <span data-ttu-id="af0fe-133">Wählen Sie auf der Registerkarte **Dateien** die Option **neu** > **Q #** aus, um ein jupyter-Notebook mit einem Q #-Kernel zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-133">On the **Files** tab, select **New** > **Q#** to create a Jupyter notebook with a Q# kernel.</span></span> <span data-ttu-id="af0fe-134">Fügen Sie den folgenden Code in die erste Notebook-Zelle ein:</span><span class="sxs-lookup"><span data-stu-id="af0fe-134">Add the following code to the first notebook cell:</span></span>

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. <span data-ttu-id="af0fe-135">Wählen Sie **Cell** > **Zellen ausführen** aus, um das Notebook auszuführen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-135">Select **Cell** > **Run Cells** to run the notebook.</span></span> <span data-ttu-id="af0fe-136">`SayHello` wird in Kürze in der Zellen Ausgabe angezeigt:</span><span class="sxs-lookup"><span data-stu-id="af0fe-136">`SayHello` will soon appear in the cell output:</span></span>

    ![Jupyter Notebook-Zelle mit Q #-Code](~/media/install-guide-jupyter.png)

    <span data-ttu-id="af0fe-138">Bei der Ausführung in jupyter-Notebooks wird der Q #-Code kompiliert, und das Notebook gibt den Namen der gefundenen Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="af0fe-138">When running in Jupyter Notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

1. <span data-ttu-id="af0fe-139">Simulieren Sie in einer neuen Zelle die Ausführung auf einem Quantum-Computer des gerade erstellten Vorgangs mithilfe der `%simulate` Magic:</span><span class="sxs-lookup"><span data-stu-id="af0fe-139">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

    ![Jupyter Notebook-Zelle mit "% simulieren" Magic](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="af0fe-141">Es sollte angezeigt werden, dass die Meldung auf dem Bildschirm angezeigt wird, und das Ergebnis des Vorgangs, den Sie aufgerufen haben (in diesem Fall leer).</span><span class="sxs-lookup"><span data-stu-id="af0fe-141">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>

<span data-ttu-id="af0fe-142">Sie können jetzt weitere Q #-Vorgänge hinzufügen, um die Quantum-Entwicklung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-142">You can now add other Q# operations to continue your quantum development.</span></span>

## <a name="create-a-c-project-on-windows-using-visual-studio"></a><span data-ttu-id="af0fe-143">Erstellen eines C# Projekts unter Windows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af0fe-143">Create a C# project on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="af0fe-144">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af0fe-144">Pre-requisites</span></span>

    * <span data-ttu-id="af0fe-145">Das [Quantum Development Kit für Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="af0fe-145">The [Quantum Development Kit for Visual Studio](xref:microsoft.quantum.install#develop-with-c-on-windows-using-visual-studio)</span></span>

1. <span data-ttu-id="af0fe-146">Erstellen einer neuen f #-Anwendung</span><span class="sxs-lookup"><span data-stu-id="af0fe-146">Create a new Q# application</span></span>

    * <span data-ttu-id="af0fe-147">Gehe zu **Datei** -> **Neues** -> **Projekt**</span><span class="sxs-lookup"><span data-stu-id="af0fe-147">Go to **File** -> **New** -> **Project**</span></span>
    * <span data-ttu-id="af0fe-148">Geben Sie `Q#` in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="af0fe-148">Type `Q#` in the search box</span></span>
    * <span data-ttu-id="af0fe-149">**F #-Anwendung** auswählen</span><span class="sxs-lookup"><span data-stu-id="af0fe-149">Select **Q# Application**</span></span>
    * <span data-ttu-id="af0fe-150">Wählen Sie **Weiter** aus</span><span class="sxs-lookup"><span data-stu-id="af0fe-150">Select **Next**</span></span>
    * <span data-ttu-id="af0fe-151">Auswählen eines Namens und eines Speicher Orts für die Anwendung</span><span class="sxs-lookup"><span data-stu-id="af0fe-151">Choose a name and location for your application</span></span>
    * <span data-ttu-id="af0fe-152">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="af0fe-152">Select **Create**</span></span>

1. <span data-ttu-id="af0fe-153">Überprüfen des Projekts</span><span class="sxs-lookup"><span data-stu-id="af0fe-153">Inspect the project</span></span>

    <span data-ttu-id="af0fe-154">Sie sollten sehen, dass zwei Dateien erstellt wurden: `Driver.cs`, die die C# Host Anwendung ist. und `Operation.qs`. dabei handelt es sich um ein Q #-Programm, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.</span><span class="sxs-lookup"><span data-stu-id="af0fe-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

1. <span data-ttu-id="af0fe-155">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="af0fe-155">Run the application</span></span>

    * <span data-ttu-id="af0fe-156">Wählen Sie **Debuggen** -> **Starten ohne Debugging**</span><span class="sxs-lookup"><span data-stu-id="af0fe-156">Select **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="af0fe-157">Sie sollten sehen, dass der Text in einem Konsolenfenster gedruckt `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="af0fe-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

<span data-ttu-id="af0fe-158">Sie können jetzt die Quantum-Entwicklung mit Visual Studio fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-158">You can now continue your quantum development using Visual Studio</span></span>

> [!NOTE]
> * <span data-ttu-id="af0fe-159">Wenn Sie mehrere Projekte in einer Visual Studio-Projekt Mappe haben, müssen sich alle in der Projekt Mappe enthaltenen Projekte im selben Ordner wie die Projekt Mappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="af0fe-159">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="create-a-c-project-using-vs-code"></a><span data-ttu-id="af0fe-160">Erstellen eines C# Projekts mit vs Code</span><span class="sxs-lookup"><span data-stu-id="af0fe-160">Create a C# project, using VS Code</span></span>

1. <span data-ttu-id="af0fe-161">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af0fe-161">Pre-requisites</span></span>

    * <span data-ttu-id="af0fe-162">Das [Quantum Development Kit für vs Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)</span><span class="sxs-lookup"><span data-stu-id="af0fe-162">The [Quantum Development Kit for VS Code](xref:microsoft.quantum.install#develop-with-c-using-visual-studio-code)</span></span>

1. <span data-ttu-id="af0fe-163">Erstellen eines neuen Projekts:</span><span class="sxs-lookup"><span data-stu-id="af0fe-163">Create a new project:</span></span>

    * <span data-ttu-id="af0fe-164">Gehe zu **Ansicht** -> **Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="af0fe-164">Go to **View** -> **Command Palette**</span></span>
    * <span data-ttu-id="af0fe-165">Wählen Sie **Q #: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="af0fe-165">Select **Q#: Create New Project**</span></span>
    * <span data-ttu-id="af0fe-166">Navigieren Sie zu dem Speicherort im Dateisystem, in dem Sie die Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="af0fe-166">Navigate to the location on the file system where you would like to create the application</span></span>
    * <span data-ttu-id="af0fe-167">Klicken Sie auf die Schaltfläche **Neues Projekt öffnen...** , nachdem das Projekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="af0fe-167">Click on the **Open new project...** button, once the project has been created</span></span>

1. <span data-ttu-id="af0fe-168">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="af0fe-168">Run the application:</span></span>

    * <span data-ttu-id="af0fe-169">Gehe zu **Debuggen** -> **Starten ohne Debugging**</span><span class="sxs-lookup"><span data-stu-id="af0fe-169">Go to **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="af0fe-170">Der folgende Text sollte im Ausgabefenster angezeigt werden `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="af0fe-170">You should see the following text in the output window `Hello quantum world!`</span></span>

<span data-ttu-id="af0fe-171">Nun können Sie die Quantum-Entwicklung mit Visual Studio Code fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-171">You can now continue your quantum development using Visual Studio Code.</span></span>

> [!NOTE]
> * <span data-ttu-id="af0fe-172">Arbeitsbereiche mit mehreren Stamm Ordnern werden zurzeit von der Visual Studio Code Erweiterung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af0fe-172">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="af0fe-173">Wenn Sie über mehrere Projekte in einem vs Code Arbeitsbereich verfügen, müssen alle Projekte im selben Stamm Ordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="af0fe-173">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a><span data-ttu-id="af0fe-174">Erstellen eines C# Projekts mit dem Befehlszeilen Tool "`dotnet`"</span><span class="sxs-lookup"><span data-stu-id="af0fe-174">Create a C# project, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="af0fe-175">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af0fe-175">Pre-requisites</span></span>

    * <span data-ttu-id="af0fe-176">Das [Quantum Development Kit für die Befehlszeile](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)</span><span class="sxs-lookup"><span data-stu-id="af0fe-176">The [Quantum Development Kit for the Command Line](xref:microsoft.quantum.install#develop-with-c-using-the-dotnet-command-line-tool)</span></span>

1. <span data-ttu-id="af0fe-177">Erstellen einer neuen Anwendung</span><span class="sxs-lookup"><span data-stu-id="af0fe-177">Create a new application</span></span>

    ```bash
    dotnet new console -lang Q# -o <project name>
    ```

1. <span data-ttu-id="af0fe-178">Navigieren Sie zum neuen Anwendungsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="af0fe-178">Navigate to the new application directory</span></span>

    ```bash
    cd <project name>
    ```

    <span data-ttu-id="af0fe-179">Sie sollten sehen, dass zwei Dateien erstellt wurden, zusammen mit den Projektdateien der Anwendung: eine Q #-Datei (`Operation.qs`) und eine C# Hostdatei (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="af0fe-179">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

1. <span data-ttu-id="af0fe-180">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="af0fe-180">Run the application</span></span>

    ```bash
    dotnet run
    ```

    <span data-ttu-id="af0fe-181">Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="af0fe-181">You should see the following output: `Hello quantum world!`</span></span>

<span data-ttu-id="af0fe-182">Mit Befehlszeilen Tools können Sie nun die Quantum-Entwicklung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-182">You now continue your quantum development, using command line tools.</span></span>

## <a name="whats-next"></a><span data-ttu-id="af0fe-183">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="af0fe-183">What's next?</span></span>

<span data-ttu-id="af0fe-184">Nachdem Sie ein Projekt in Ihrer bevorzugten Umgebung erstellt haben, können Sie die Quantum-Entwicklung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="af0fe-184">Now that you have created a project in your preferred environment, you can continue your quantum development.</span></span>
