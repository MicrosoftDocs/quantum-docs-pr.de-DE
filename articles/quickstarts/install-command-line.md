---
title: Entwickeln mit :::no-loc(Q#):::-Anwendungen in einer IDE
description: 'Hier erfahren Sie, wie Sie eine Anwendung vom Typ :::no-loc(Q#)::: erstellen, die über die Eingabeaufforderung ausgeführt wird.'
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: a6823888dcbe8cf79f0045d2615fe8b889dcc7c3
ms.sourcegitcommit: a13c7c86fd52a05cbf129b8dd713d6586ca1cc2c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/05/2020
ms.locfileid: "93376421"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a><span data-ttu-id="adedb-103">Entwickeln mit :::no-loc(Q#):::-Anwendungen in einer IDE</span><span class="sxs-lookup"><span data-stu-id="adedb-103">Develop with :::no-loc(Q#)::: applications in an IDE</span></span>

<span data-ttu-id="adedb-104">:::no-loc(Q#):::-Programme können eigenständig ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="adedb-104">:::no-loc(Q#)::: programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span> <span data-ttu-id="adedb-105">Sie können :::no-loc(Q#):::-Anwendungen in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces oder mit einem beliebigen Editor bzw. einer beliebigen IDE entwickeln und Anwendungen über die .NET-Konsole ausführen.</span><span class="sxs-lookup"><span data-stu-id="adedb-105">You can develop :::no-loc(Q#)::: applications in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces, or with any editor/IDE and run applications from the .NET console.</span></span> 

## <a name="prerequisites-for-all-environments"></a><span data-ttu-id="adedb-106">Voraussetzungen für alle Umgebungen</span><span class="sxs-lookup"><span data-stu-id="adedb-106">Prerequisites for all environments</span></span>

- [<span data-ttu-id="adedb-107">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="adedb-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="adedb-108">Installation</span><span class="sxs-lookup"><span data-stu-id="adedb-108">Installation</span></span>

<span data-ttu-id="adedb-109">:::no-loc(Q#):::-Anwendungen können zwar in einer beliebigen IDE erstellt werden, wir empfehlen jedoch, Visual Studio Code (VS Code) oder die Visual Studio-IDE für die lokale Entwicklung Ihrer :::no-loc(Q#):::-Anwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="adedb-109">While you can build :::no-loc(Q#)::: applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your :::no-loc(Q#)::: applications locally.</span></span> <span data-ttu-id="adedb-110">Für die Entwicklung in der Cloud über den Webbrowser wird Visual Studio Codespaces empfohlen.</span><span class="sxs-lookup"><span data-stu-id="adedb-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="adedb-111">Die Entwicklung in diesen Umgebungen umfasst die umfangreichen Funktionen der QDK-Erweiterung, einschließlich Warnungen, Syntaxhervorhebung, Projektvorlagen und mehr.</span><span class="sxs-lookup"><span data-stu-id="adedb-111">Developing in these environments leverages the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

### <a name="to-configure-for-vs-code"></a><span data-ttu-id="adedb-112">Gehen Sie zum Konfigurieren für VS Code wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="adedb-112">To configure for VS Code:</span></span>

1. <span data-ttu-id="adedb-113">Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="adedb-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="adedb-114">Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="adedb-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

### <a name="to-configure-for-visual-studio"></a><span data-ttu-id="adedb-115">Gehen Sie zum Konfigurieren für Visual Studio wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="adedb-115">To configure for Visual Studio:</span></span>

1. <span data-ttu-id="adedb-116">Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.</span><span class="sxs-lookup"><span data-stu-id="adedb-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="adedb-117">Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="adedb-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

### <a name="to-configure-for-another-environment"></a><span data-ttu-id="adedb-118">Gehen Sie zum Konfigurieren für eine andere Umgebung wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="adedb-118">To configure for another environment:</span></span> 

1. <span data-ttu-id="adedb-119">Geben Sie an der Eingabeaufforderung Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="adedb-119">Enter the following at the command prompt</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a><span data-ttu-id="adedb-120">Gehen Sie zum Konfigurieren für Visual Studio Codespaces wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="adedb-120">To configure for Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="adedb-121">[Erstellen eines Azure-Kontos](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="adedb-121">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="adedb-122">Erstellen Sie eine Codespaces-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="adedb-122">Create a Codespaces environment.</span></span> <span data-ttu-id="adedb-123">Führen Sie dazu die Schritte in der [Schnellstartanleitung](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser) aus.</span><span class="sxs-lookup"><span data-stu-id="adedb-123">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="adedb-124">Wir empfehlen, beim Erstellen der Codespaces-Umgebung `microsoft/Quantum` in das Feld „Git-Repository“ einzugeben, um QDK-spezifische Einstellungen zu laden.</span><span class="sxs-lookup"><span data-stu-id="adedb-124">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="adedb-125">Nun können Sie Ihre neue Umgebung starten und mit der Entwicklung im Browser über die [VS Codespaces-Cloud-IDE](https://online.visualstudio.com/environments) beginnen.</span><span class="sxs-lookup"><span data-stu-id="adedb-125">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="adedb-126">Alternativ können Sie die lokale Installation von VS Code und Codespaces als [Remoteumgebung](https://docs.microsoft.com/visualstudio/online/how-to/vscode) verwenden.</span><span class="sxs-lookup"><span data-stu-id="adedb-126">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>

## <a name="develop-with-no-locq"></a><span data-ttu-id="adedb-127">Entwickeln mit :::no-loc(Q#):::</span><span class="sxs-lookup"><span data-stu-id="adedb-127">Develop with :::no-loc(Q#):::</span></span>

<span data-ttu-id="adedb-128">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Entwicklungsumgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="adedb-128">Follow the instructions on the tab corresponding to your development environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="adedb-129">VS-Code</span><span class="sxs-lookup"><span data-stu-id="adedb-129">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="adedb-130">Erstellen Sie wie folgt ein neues Projekt:</span><span class="sxs-lookup"><span data-stu-id="adedb-130">To create a new project:</span></span>

1. <span data-ttu-id="adedb-131">Klicken Sie auf **Ansicht** -> **Befehlspalette** , und wählen Sie **:::no-loc(Q#):::: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="adedb-131">Click **View** -> **Command Palette** and select **:::no-loc(Q#):::: Create New Project**.</span></span>
2. <span data-ttu-id="adedb-132">Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).</span><span class="sxs-lookup"><span data-stu-id="adedb-132">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="adedb-133">Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="adedb-133">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="adedb-134">Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).</span><span class="sxs-lookup"><span data-stu-id="adedb-134">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="adedb-135">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="adedb-135">Inspect the project.</span></span> <span data-ttu-id="adedb-136">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein :::no-loc(Q#):::-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="adedb-136">You should see a source file named `Program.qs`, which is a :::no-loc(Q#)::: program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="adedb-137">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="adedb-137">To run the application:</span></span>

1. <span data-ttu-id="adedb-138">Klicken Sie auf **Terminal** -> **Neues Terminal**.</span><span class="sxs-lookup"><span data-stu-id="adedb-138">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="adedb-139">Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="adedb-139">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="adedb-140">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="adedb-140">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="adedb-141">Arbeitsbereiche mit mehreren Stammordnern werden von der :::no-loc(Q#):::-Erweiterung für VS Code derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="adedb-141">Workspaces with multiple root folders are not currently supported by the VS Code :::no-loc(Q#)::: extension.</span></span> <span data-ttu-id="adedb-142">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="adedb-142">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="adedb-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="adedb-143">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="adedb-144">Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine :::no-loc(Q#):::-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="adedb-144">Verify your Visual Studio installation by creating a :::no-loc(Q#)::: `Hello World` application.</span></span>

<span data-ttu-id="adedb-145">So erstellen Sie eine neue :::no-loc(Q#):::-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="adedb-145">To create a new :::no-loc(Q#)::: application:</span></span>

1. <span data-ttu-id="adedb-146">Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="adedb-146">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="adedb-147">Geben Sie `:::no-loc(Q#):::` in das Suchfeld ein, wählen Sie **:::no-loc(Q#):::-Anwendung** aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="adedb-147">Type `:::no-loc(Q#):::` in the search box, select **:::no-loc(Q#)::: Application** and click **Next**.</span></span>
3. <span data-ttu-id="adedb-148">Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="adedb-148">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="adedb-149">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="adedb-149">Inspect the project.</span></span> <span data-ttu-id="adedb-150">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein :::no-loc(Q#):::-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="adedb-150">You should see a source file named `Program.qs`, which is a :::no-loc(Q#)::: program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="adedb-151">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="adedb-151">To run the application:</span></span>

1. <span data-ttu-id="adedb-152">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="adedb-152">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="adedb-153">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="adedb-153">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="adedb-154">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="adedb-154">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="adedb-155">Andere Editoren mit der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="adedb-155">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="adedb-156">Überprüfen Sie Ihre Installation, indem Sie eine :::no-loc(Q#):::-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="adedb-156">Verify your installation by creating a :::no-loc(Q#)::: `Hello World` application.</span></span>

1. <span data-ttu-id="adedb-157">Erstellen einer neuen Anwendung:</span><span class="sxs-lookup"><span data-stu-id="adedb-157">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang :::no-loc(Q#)::: -o runSayHello
    ```

1. <span data-ttu-id="adedb-158">Navigieren Sie zum Anwendungsverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="adedb-158">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="adedb-159">Dieses Verzeichnis sollte nun eine Datei namens `Program.qs` enthalten. Dabei handelt es sich um ein :::no-loc(Q#):::-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="adedb-159">This directory should now contain a file `Program.qs`, which is a :::no-loc(Q#)::: program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="adedb-160">Sie können diese Vorlage mit einem Text-Editor ändern und mit ihren eigenen Quantum-Anwendungen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="adedb-160">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="adedb-161">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="adedb-161">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="adedb-162">Der folgende Text sollte angezeigt werden: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="adedb-162">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="adedb-163">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="adedb-163">Next steps</span></span>

<span data-ttu-id="adedb-164">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="adedb-164">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
