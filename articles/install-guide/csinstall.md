---
title: 'Entwickeln mit Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 7803846279f230f5fc0ee8424bd39be735a650ca
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036286"
---
# <a name="develop-with-q--c"></a><span data-ttu-id="c3754-102">Entwickeln mit Q # +C#</span><span class="sxs-lookup"><span data-stu-id="c3754-102">Develop with Q# + C#</span></span>

<span data-ttu-id="c3754-103">Installieren Sie das QDK, C# um Host Programme zum Abrufen von Q #-Vorgängen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="c3754-103">Install the QDK to develop C# host programs to call Q# operations.</span></span>

<span data-ttu-id="c3754-104">Q # ist speziell für .NET-Sprachen konzipiert, insbesondere C#.</span><span class="sxs-lookup"><span data-stu-id="c3754-104">Q# is built to play well with .NET languages--specifically C#.</span></span> <span data-ttu-id="c3754-105">Sie können mit dieser Kopplung innerhalb verschiedener Entwicklungsumgebungen arbeiten:</span><span class="sxs-lookup"><span data-stu-id="c3754-105">You can work with this pairing inside different development environments:</span></span>

- [<span data-ttu-id="c3754-106">F # und C# Verwendung von Visual Studio (Windows)</span><span class="sxs-lookup"><span data-stu-id="c3754-106">Q# + C# using Visual Studio (Windows)</span></span>](#VS)
- [<span data-ttu-id="c3754-107">Q # + C# Verwenden von Visual Studio Code (Windows, Linux und Mac)</span><span class="sxs-lookup"><span data-stu-id="c3754-107">Q# + C# using Visual Studio Code (Windows, Linux and Mac)</span></span>](#VSC)
- [<span data-ttu-id="c3754-108">Q # + C# mit dem Befehlszeilen Tool "`dotnet`"</span><span class="sxs-lookup"><span data-stu-id="c3754-108">Q# + C# using the `dotnet` command-line tool</span></span>](#command)

## <span data-ttu-id="c3754-109">Entwickeln mit Q # + C# mithilfe von Visual Studio <a name="VS"></a></span><span class="sxs-lookup"><span data-stu-id="c3754-109">Develop with Q# + C# using Visual Studio <a name="VS"></a></span></span>

<span data-ttu-id="c3754-110">Visual Studio bietet eine umfangreiche Umgebung für die Entwicklung von f #-Programmen.</span><span class="sxs-lookup"><span data-stu-id="c3754-110">Visual Studio offers a rich environment for developing Q# programs.</span></span> <span data-ttu-id="c3754-111">Die f # Visual Studio-Erweiterung enthält Vorlagen für Q #-Dateien und-Projekte sowie Syntax Hervorhebung, Codevervollständigung und IntelliSense-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="c3754-111">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting, code completion and IntelliSense support.</span></span>


1. <span data-ttu-id="c3754-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c3754-112">Pre-requisites</span></span>

    - <span data-ttu-id="c3754-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload</span><span class="sxs-lookup"><span data-stu-id="c3754-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="c3754-114">Installieren der Q#-Erweiterung für Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c3754-114">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="c3754-115">Herunterladen und Installieren der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="c3754-115">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>

1. <span data-ttu-id="c3754-116">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-116">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="c3754-117">Erstellen einer neuen Q#-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-117">Create a new Q# application</span></span>

        - <span data-ttu-id="c3754-118">Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c3754-118">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="c3754-119">Geben Sie im Suchfeld als Suchbegriff `Q#` ein.</span><span class="sxs-lookup"><span data-stu-id="c3754-119">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="c3754-120">Wählen Sie **Q#-Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="c3754-120">Select **Q# Application**</span></span>
        - <span data-ttu-id="c3754-121">Wählen Sie **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="c3754-121">Select **Next**</span></span>
        - <span data-ttu-id="c3754-122">Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="c3754-122">Choose a name and location for your application</span></span>
        - <span data-ttu-id="c3754-123">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="c3754-123">Select **Create**</span></span>

    - <span data-ttu-id="c3754-124">Untersuchen des Projekts</span><span class="sxs-lookup"><span data-stu-id="c3754-124">Inspect the project</span></span>

        <span data-ttu-id="c3754-125">Es sollten zwei Dateien erstellt worden sein: `Driver.cs` (C#-Hostanwendung) und `Operation.qs` (Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung auf der Konsole definiert wird).</span><span class="sxs-lookup"><span data-stu-id="c3754-125">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="c3754-126">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-126">Run the application</span></span>

        - <span data-ttu-id="c3754-127">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="c3754-127">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="c3754-128">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c3754-128">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="c3754-129">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="c3754-129">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <span data-ttu-id="c3754-130">Entwickeln mit Q # + C# mit Visual Studio Code <a name="VSC"></a></span><span class="sxs-lookup"><span data-stu-id="c3754-130">Develop with Q# + C# using Visual Studio Code <a name="VSC"></a></span></span>

<span data-ttu-id="c3754-131">Visual Studio Code (vs Code) bietet eine umfangreiche Umgebung für die Entwicklung von Q #-Programmen unter Windows, Linux und Mac.</span><span class="sxs-lookup"><span data-stu-id="c3754-131">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs on Windows, Linux and Mac.</span></span>  <span data-ttu-id="c3754-132">Die q # vs Code-Erweiterung bietet Unterstützung für die f #-Syntax Hervorhebung, Codevervollständigung und f #-Code Ausschnitte.</span><span class="sxs-lookup"><span data-stu-id="c3754-132">The Q# VS Code extension includes support for Q# syntax highlighting, code completion, and Q# code snippets.</span></span>

1. <span data-ttu-id="c3754-133">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c3754-133">Pre-requisites</span></span>

   - [<span data-ttu-id="c3754-134">VS-Code</span><span class="sxs-lookup"><span data-stu-id="c3754-134">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="c3754-135">.Net Core SDK 3,1 oder höher</span><span class="sxs-lookup"><span data-stu-id="c3754-135">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="c3754-136">Installieren der VS Code-Erweiterung für Quantum</span><span class="sxs-lookup"><span data-stu-id="c3754-136">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="c3754-137">Installieren Sie die [VS Code-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="c3754-137">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="c3754-138">Installieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="c3754-138">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="c3754-139">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="c3754-139">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="c3754-140">Auswählen von " **Q #: Install Project Templates** "</span><span class="sxs-lookup"><span data-stu-id="c3754-140">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="c3754-141">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3754-141">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="c3754-142">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-142">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="c3754-143">Erstellen eines neuen Projekts:</span><span class="sxs-lookup"><span data-stu-id="c3754-143">Create a new project:</span></span>

        - <span data-ttu-id="c3754-144">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="c3754-144">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="c3754-145">Wählen Sie **Q #: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c3754-145">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="c3754-146">**Eigenständige Konsolenanwendung** auswählen</span><span class="sxs-lookup"><span data-stu-id="c3754-146">Select **Standalone console application**</span></span>
        - <span data-ttu-id="c3754-147">Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c3754-147">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="c3754-148">Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).</span><span class="sxs-lookup"><span data-stu-id="c3754-148">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="c3754-149">Wenn Sie die C# Erweiterung für vs Code nicht bereits installiert haben, wird ein Popup Fenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3754-149">If you don't already have the C# extension for VS Code installed, a pop-up will appear.</span></span> <span data-ttu-id="c3754-150">Installieren Sie die Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="c3754-150">Install the extension.</span></span> 

    - <span data-ttu-id="c3754-151">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="c3754-151">Run the application:</span></span>

        - <span data-ttu-id="c3754-152">Zum **Terminal** -> **neuen Terminal** wechseln</span><span class="sxs-lookup"><span data-stu-id="c3754-152">Go to **Terminal** -> **New Terminal**</span></span>
        - <span data-ttu-id="c3754-153">Geben Sie `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="c3754-153">Enter `dotnet run`</span></span>
        - <span data-ttu-id="c3754-154">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="c3754-154">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="c3754-155">Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3754-155">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="c3754-156">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c3754-156">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <span data-ttu-id="c3754-157">Entwickeln mit Q # + C# mit dem `dotnet`-Befehlszeilen Tool<a name="command"></a></span><span class="sxs-lookup"><span data-stu-id="c3754-157">Develop with Q# + C# using the `dotnet` command-line tool <a name="command"></a></span></span>

<span data-ttu-id="c3754-158">Natürlich können Sie Q#-Programme auch über die Befehlszeile erstellen und ausführen, indem Sie einfach das .NET Core SDK und die QDK-Projektvorlagen installieren.</span><span class="sxs-lookup"><span data-stu-id="c3754-158">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="c3754-159">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c3754-159">Pre-requisites</span></span>

    - [<span data-ttu-id="c3754-160">.Net Core SDK 3,1 oder höher</span><span class="sxs-lookup"><span data-stu-id="c3754-160">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="c3754-161">Installieren der Quantum-Projektvorlagen für .NET</span><span class="sxs-lookup"><span data-stu-id="c3754-161">Install the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="c3754-162">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="c3754-162">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="c3754-163">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-163">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="c3754-164">Erstellen einer neuen Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-164">Create a new application</span></span>

       ```dotnetcli
       dotnet new console -lang "Q#" -o runSayHello
       ```

    - <span data-ttu-id="c3754-165">Navigieren Sie zum neuen Anwendungsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="c3754-165">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="c3754-166">Es sollten zwei Dateien und die Projektdateien der Anwendung erstellt worden sein: eine Q#-Datei (`Operation.qs`) und eine C#-Hostdatei (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="c3754-166">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="c3754-167">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="c3754-167">Run the application</span></span>

        ```dotnetcli
        dotnet run
        ```

        <span data-ttu-id="c3754-168">Die folgende Ausgabe sollte angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="c3754-168">You should see the following output: `Hello quantum world!`</span></span>

    
## <a name="whats-next"></a><span data-ttu-id="c3754-169">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="c3754-169">What's next?</span></span>

<span data-ttu-id="c3754-170">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3754-170">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
