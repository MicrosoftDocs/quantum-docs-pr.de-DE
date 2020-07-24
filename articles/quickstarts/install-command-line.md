---
title: Entwickeln mit Q#-Befehlszeilenanwendungen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 3d70838289e72afdd0a48bbdff0bec407428d125
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871432"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="5beae-102">Entwickeln mit Q#-Befehlszeilenanwendungen</span><span class="sxs-lookup"><span data-stu-id="5beae-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="5beae-103">Q#-Programme können allein ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5beae-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5beae-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="5beae-104">Prerequisites</span></span>

- [<span data-ttu-id="5beae-105">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="5beae-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="5beae-106">Installation</span><span class="sxs-lookup"><span data-stu-id="5beae-106">Installation</span></span>

<span data-ttu-id="5beae-107">Sie können Q#-Befehlszeilenanwendungen zwar in einer beliebigen IDE erstellen, aber wir empfehlen Ihnen, für die lokale Entwicklung Ihrer Q#-Anwendungen Visual Studio Code (VS Code) oder die Visual Studio-IDE zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="5beae-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="5beae-108">Für die Entwicklung in der Cloud über den Webbrowser wird Visual Studio Codespaces empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5beae-108">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="5beae-109">Die Entwicklung in diesen Umgebungen umfasst die umfangreichen Funktionen der QDK-Erweiterung, einschließlich Warnungen, Syntaxhervorhebung, Projektvorlagen und mehr.</span><span class="sxs-lookup"><span data-stu-id="5beae-109">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="5beae-110">Gehen Sie zum Konfigurieren von VS Code wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5beae-110">To configure VS Code:</span></span>

1. <span data-ttu-id="5beae-111">Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="5beae-111">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="5beae-112">Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="5beae-112">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="5beae-113">Gehen Sie zum Konfigurieren von Visual Studio wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="5beae-113">To configure Visual Studio:</span></span>

1. <span data-ttu-id="5beae-114">Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.</span><span class="sxs-lookup"><span data-stu-id="5beae-114">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="5beae-115">Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="5beae-115">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="5beae-116">So konfigurieren Sie Visual Studio Codespaces:</span><span class="sxs-lookup"><span data-stu-id="5beae-116">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="5beae-117">[Erstellen eines Azure-Kontos](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="5beae-117">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="5beae-118">Erstellen Sie eine Codespaces-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="5beae-118">Create a Codespaces environment.</span></span> <span data-ttu-id="5beae-119">Führen Sie dazu die Schritte in der [Schnellstartanleitung](https://docs.microsoft.com/visualstudio/online/quickstarts/browser) aus.</span><span class="sxs-lookup"><span data-stu-id="5beae-119">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span></span> <span data-ttu-id="5beae-120">Wir empfehlen, beim Erstellen der Codespaces-Umgebung `microsoft/Quantum` in das Feld „Git-Repository“ einzugeben, um QDK-spezifische Einstellungen zu laden.</span><span class="sxs-lookup"><span data-stu-id="5beae-120">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="5beae-121">Nun können Sie Ihre neue Umgebung starten und mit der Entwicklung im Browser über die [VS Codespaces-Cloud-IDE](https://online.visualstudio.com/environments) beginnen.</span><span class="sxs-lookup"><span data-stu-id="5beae-121">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="5beae-122">Alternativ können Sie die lokale Installation von VS Code und Codespaces als [Remoteumgebung](https://docs.microsoft.com/visualstudio/online/how-to/vscode) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5beae-122">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="5beae-123">Geben Sie Folgendes in die Befehlszeile ein, um das QDK für eine andere Umgebung zu installieren:</span><span class="sxs-lookup"><span data-stu-id="5beae-123">To install the QDK for another environment, enter in the command line:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a><span data-ttu-id="5beae-124">Entwickeln mit Q#</span><span class="sxs-lookup"><span data-stu-id="5beae-124">Develop with Q#</span></span>

<span data-ttu-id="5beae-125">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Umgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="5beae-125">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="5beae-126">VS-Code</span><span class="sxs-lookup"><span data-stu-id="5beae-126">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="5beae-127">Erstellen Sie wie folgt ein neues Projekt:</span><span class="sxs-lookup"><span data-stu-id="5beae-127">To create a new project:</span></span>

1. <span data-ttu-id="5beae-128">Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="5beae-128">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="5beae-129">Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).</span><span class="sxs-lookup"><span data-stu-id="5beae-129">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="5beae-130">Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5beae-130">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="5beae-131">Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).</span><span class="sxs-lookup"><span data-stu-id="5beae-131">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="5beae-132">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="5beae-132">Inspect the project.</span></span> <span data-ttu-id="5beae-133">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5beae-133">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="5beae-134">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="5beae-134">To run the application:</span></span>
1. <span data-ttu-id="5beae-135">Klicken Sie auf **Terminal** -> **Neues Terminal**.</span><span class="sxs-lookup"><span data-stu-id="5beae-135">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="5beae-136">Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="5beae-136">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="5beae-137">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="5beae-137">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="5beae-138">Arbeitsbereiche mit mehreren Stammordnern werden von der VS Code-Q#-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5beae-138">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="5beae-139">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="5beae-139">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="5beae-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5beae-140">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="5beae-141">Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="5beae-141">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="5beae-142">Erstellen Sie wie folgt eine neue Q#-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="5beae-142">To create a new Q# application:</span></span>
1. <span data-ttu-id="5beae-143">Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="5beae-143">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="5beae-144">Geben Sie im Suchfeld den Begriff `Q#` ein, wählen Sie **Q#-Anwendung** aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="5beae-144">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="5beae-145">Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="5beae-145">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="5beae-146">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="5beae-146">Inspect the project.</span></span> <span data-ttu-id="5beae-147">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5beae-147">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="5beae-148">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="5beae-148">To run the application:</span></span>
1. <span data-ttu-id="5beae-149">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="5beae-149">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="5beae-150">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5beae-150">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="5beae-151">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="5beae-151">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-line"></a>[<span data-ttu-id="5beae-152">Andere Editoren mit der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="5beae-152">Other editors with the command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="5beae-153">Überprüfen Sie Ihre Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="5beae-153">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="5beae-154">Installieren Sie die Projektvorlagen.</span><span class="sxs-lookup"><span data-stu-id="5beae-154">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="5beae-155">Erstellen einer neuen Anwendung:</span><span class="sxs-lookup"><span data-stu-id="5beae-155">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="5beae-156">Navigieren Sie zum Anwendungsverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="5beae-156">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="5beae-157">Dieses Verzeichnis sollte nun eine Datei namens `Program.qs` enthalten. Dabei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="5beae-157">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="5beae-158">Sie können diese Vorlage mit einem Text-Editor ändern und mit ihren eigenen Quantum-Anwendungen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="5beae-158">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="5beae-159">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="5beae-159">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="5beae-160">Der folgende Text sollte angezeigt werden: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="5beae-160">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="5beae-161">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="5beae-161">Next steps</span></span>

<span data-ttu-id="5beae-162">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="5beae-162">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
