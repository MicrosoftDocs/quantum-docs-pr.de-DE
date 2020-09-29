---
title: Entwickeln mit Q#-Anwendungen
description: Hier erfahren Sie, wie Sie eine Anwendung vom Typ Q# erstellen, die über die Eingabeaufforderung ausgeführt wird.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 68f530d80e5c5f40dc2bcbb185879c3cb6f93f91
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834413"
---
# <a name="develop-with-no-locq-applications"></a><span data-ttu-id="decae-103">Entwickeln mit Q#-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="decae-103">Develop with Q# applications</span></span>

<span data-ttu-id="decae-104">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Umgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="decae-104">Follow the instructions at the tab corresponding to your environment.</span></span>

<span data-ttu-id="decae-105">Q#-Programme können eigenständig ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="decae-105">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="decae-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="decae-106">Prerequisites</span></span>

- [<span data-ttu-id="decae-107">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="decae-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="decae-108">Installation</span><span class="sxs-lookup"><span data-stu-id="decae-108">Installation</span></span>

<span data-ttu-id="decae-109">Q#-Anwendungen können zwar in einer beliebigen IDE erstellt werden, wir empfehlen jedoch, Visual Studio Code (VS Code) oder die Visual Studio-IDE für die lokale Entwicklung Ihrer Q#-Anwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="decae-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="decae-110">Für die Entwicklung in der Cloud über den Webbrowser wird Visual Studio Codespaces empfohlen.</span><span class="sxs-lookup"><span data-stu-id="decae-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="decae-111">Die Entwicklung in diesen Umgebungen umfasst die umfangreichen Funktionen der QDK-Erweiterung, einschließlich Warnungen, Syntaxhervorhebung, Projektvorlagen und mehr.</span><span class="sxs-lookup"><span data-stu-id="decae-111">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="decae-112">Gehen Sie zum Konfigurieren von VS Code wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="decae-112">To configure VS Code:</span></span>

1. <span data-ttu-id="decae-113">Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="decae-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="decae-114">Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="decae-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="decae-115">Gehen Sie zum Konfigurieren von Visual Studio wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="decae-115">To configure Visual Studio:</span></span>

1. <span data-ttu-id="decae-116">Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.</span><span class="sxs-lookup"><span data-stu-id="decae-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="decae-117">Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="decae-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="decae-118">So konfigurieren Sie Visual Studio Codespaces:</span><span class="sxs-lookup"><span data-stu-id="decae-118">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="decae-119">[Erstellen eines Azure-Kontos](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="decae-119">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="decae-120">Erstellen Sie eine Codespaces-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="decae-120">Create a Codespaces environment.</span></span> <span data-ttu-id="decae-121">Führen Sie dazu die Schritte in der [Schnellstartanleitung](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser) aus.</span><span class="sxs-lookup"><span data-stu-id="decae-121">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="decae-122">Wir empfehlen, beim Erstellen der Codespaces-Umgebung `microsoft/Quantum` in das Feld „Git-Repository“ einzugeben, um QDK-spezifische Einstellungen zu laden.</span><span class="sxs-lookup"><span data-stu-id="decae-122">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="decae-123">Nun können Sie Ihre neue Umgebung starten und mit der Entwicklung im Browser über die [VS Codespaces-Cloud-IDE](https://online.visualstudio.com/environments) beginnen.</span><span class="sxs-lookup"><span data-stu-id="decae-123">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="decae-124">Alternativ können Sie die lokale Installation von VS Code und Codespaces als [Remoteumgebung](https://docs.microsoft.com/visualstudio/online/how-to/vscode) verwenden.</span><span class="sxs-lookup"><span data-stu-id="decae-124">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="decae-125">Geben Sie Folgendes an der Eingabeaufforderung ein, um das QDK für eine andere Umgebung zu installieren:</span><span class="sxs-lookup"><span data-stu-id="decae-125">To install the QDK for another environment, enter the following at the command prompt:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="decae-126">Entwickeln mit Q#</span><span class="sxs-lookup"><span data-stu-id="decae-126">Develop with Q#</span></span>

<span data-ttu-id="decae-127">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Umgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="decae-127">Follow the instructions on the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="decae-128">VS-Code</span><span class="sxs-lookup"><span data-stu-id="decae-128">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="decae-129">Erstellen Sie wie folgt ein neues Projekt:</span><span class="sxs-lookup"><span data-stu-id="decae-129">To create a new project:</span></span>

1. <span data-ttu-id="decae-130">Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="decae-130">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="decae-131">Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).</span><span class="sxs-lookup"><span data-stu-id="decae-131">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="decae-132">Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="decae-132">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="decae-133">Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).</span><span class="sxs-lookup"><span data-stu-id="decae-133">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="decae-134">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="decae-134">Inspect the project.</span></span> <span data-ttu-id="decae-135">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="decae-135">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="decae-136">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="decae-136">To run the application:</span></span>

1. <span data-ttu-id="decae-137">Klicken Sie auf **Terminal** -> **Neues Terminal**.</span><span class="sxs-lookup"><span data-stu-id="decae-137">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="decae-138">Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="decae-138">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="decae-139">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="decae-139">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="decae-140">Arbeitsbereiche mit mehreren Stammordnern werden von der Q#-Erweiterung für VS Code derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="decae-140">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="decae-141">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="decae-141">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="decae-142">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="decae-142">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="decae-143">Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="decae-143">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="decae-144">So erstellen Sie eine neue Q#-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="decae-144">To create a new Q# application:</span></span>

1. <span data-ttu-id="decae-145">Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="decae-145">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="decae-146">Geben Sie `Q#` in das Suchfeld ein, wählen Sie **Q#-Anwendung** aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="decae-146">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="decae-147">Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="decae-147">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="decae-148">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="decae-148">Inspect the project.</span></span> <span data-ttu-id="decae-149">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="decae-149">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="decae-150">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="decae-150">To run the application:</span></span>

1. <span data-ttu-id="decae-151">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="decae-151">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="decae-152">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="decae-152">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="decae-153">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="decae-153">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="decae-154">Andere Editoren mit der Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="decae-154">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="decae-155">Überprüfen Sie Ihre Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="decae-155">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="decae-156">Installieren Sie die Projektvorlagen.</span><span class="sxs-lookup"><span data-stu-id="decae-156">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="decae-157">Erstellen einer neuen Anwendung:</span><span class="sxs-lookup"><span data-stu-id="decae-157">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="decae-158">Navigieren Sie zum Anwendungsverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="decae-158">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="decae-159">Dieses Verzeichnis sollte nun eine Datei namens `Program.qs` enthalten. Dabei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="decae-159">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="decae-160">Sie können diese Vorlage mit einem Text-Editor ändern und mit ihren eigenen Quantum-Anwendungen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="decae-160">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="decae-161">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="decae-161">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="decae-162">Der folgende Text sollte angezeigt werden: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="decae-162">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="decae-163">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="decae-163">Next steps</span></span>

<span data-ttu-id="decae-164">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="decae-164">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
