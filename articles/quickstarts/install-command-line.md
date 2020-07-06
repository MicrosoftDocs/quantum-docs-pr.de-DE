---
title: Entwickeln mit Q#-Befehlszeilenanwendungen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 15015d1673f47faf5a13dde516f834916b4319d6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884287"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="1e889-102">Entwickeln mit Q#-Befehlszeilenanwendungen</span><span class="sxs-lookup"><span data-stu-id="1e889-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="1e889-103">Q#-Programme können allein ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1e889-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1e889-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1e889-104">Prerequisites</span></span>

- [<span data-ttu-id="1e889-105">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="1e889-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="1e889-106">Installation</span><span class="sxs-lookup"><span data-stu-id="1e889-106">Installation</span></span>

<span data-ttu-id="1e889-107">Sie können Q#-Befehlszeilenanwendungen zwar in einer beliebigen IDE erstellen, aber wir empfehlen Ihnen, für Ihre Q#-Anwendungen Visual Studio Code (VS Code) oder Visual Studio als IDE zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="1e889-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="1e889-108">Die Entwicklung in diesen Umgebungen umfasst die umfangreichen Funktionen der QDK-Erweiterung, einschließlich Warnungen, Syntaxhervorhebung, Projektvorlagen und mehr.</span><span class="sxs-lookup"><span data-stu-id="1e889-108">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="1e889-109">Gehen Sie zum Konfigurieren von VS Code wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="1e889-109">To configure VS Code:</span></span>

1. <span data-ttu-id="1e889-110">Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="1e889-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="1e889-111">Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="1e889-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="1e889-112">Gehen Sie zum Konfigurieren von Visual Studio wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="1e889-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="1e889-113">Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.</span><span class="sxs-lookup"><span data-stu-id="1e889-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="1e889-114">Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="1e889-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="1e889-115">Geben Sie Folgendes in die Befehlszeile ein, um das QDK für eine andere Umgebung zu installieren:</span><span class="sxs-lookup"><span data-stu-id="1e889-115">To install the QDK for another environment, enter in the command line:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-q"></a><span data-ttu-id="1e889-116">Entwickeln mit Q#</span><span class="sxs-lookup"><span data-stu-id="1e889-116">Develop with Q#</span></span>

<span data-ttu-id="1e889-117">Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Umgebung entspricht.</span><span class="sxs-lookup"><span data-stu-id="1e889-117">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="1e889-118">VS-Code</span><span class="sxs-lookup"><span data-stu-id="1e889-118">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="1e889-119">Installieren Sie die Q#-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="1e889-119">Install the Q# project templates:</span></span>

1. <span data-ttu-id="1e889-120">Öffnen Sie Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="1e889-120">Open VS Code.</span></span>
2. <span data-ttu-id="1e889-121">Klicken Sie auf **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="1e889-121">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="1e889-122">Wählen Sie **Q#: Projektvorlagen installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="1e889-122">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="1e889-123">Wenn die Meldung mit dem Hinweis angezeigt wird, dass die **Installation der Projektvorlagen erfolgreich war**, ist das QDK für die Verwendung mit Ihren eigenen Anwendungen und Bibliotheken bereit.</span><span class="sxs-lookup"><span data-stu-id="1e889-123">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="1e889-124">Erstellen Sie wie folgt ein neues Projekt:</span><span class="sxs-lookup"><span data-stu-id="1e889-124">To create a new project:</span></span>

1. <span data-ttu-id="1e889-125">Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="1e889-125">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="1e889-126">Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).</span><span class="sxs-lookup"><span data-stu-id="1e889-126">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="1e889-127">Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1e889-127">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="1e889-128">Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).</span><span class="sxs-lookup"><span data-stu-id="1e889-128">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="1e889-129">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1e889-129">Inspect the project.</span></span> <span data-ttu-id="1e889-130">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1e889-130">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1e889-131">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="1e889-131">To run the application:</span></span>
1. <span data-ttu-id="1e889-132">Klicken Sie auf **Terminal** -> **Neues Terminal**.</span><span class="sxs-lookup"><span data-stu-id="1e889-132">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="1e889-133">Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="1e889-133">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="1e889-134">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="1e889-134">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="1e889-135">Arbeitsbereiche mit mehreren Stammordnern werden von der VS Code-Q#-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1e889-135">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="1e889-136">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1e889-136">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="1e889-137">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1e889-137">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="1e889-138">Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e889-138">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="1e889-139">Erstellen Sie wie folgt eine neue Q#-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="1e889-139">To create a new Q# application:</span></span>
1. <span data-ttu-id="1e889-140">Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1e889-140">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="1e889-141">Geben Sie im Suchfeld den Begriff `Q#` ein, wählen Sie **Q#-Anwendung** aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="1e889-141">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="1e889-142">Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1e889-142">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="1e889-143">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1e889-143">Inspect the project.</span></span> <span data-ttu-id="1e889-144">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1e889-144">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1e889-145">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="1e889-145">To run the application:</span></span>
1. <span data-ttu-id="1e889-146">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="1e889-146">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="1e889-147">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1e889-147">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="1e889-148">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="1e889-148">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-line"></a>[<span data-ttu-id="1e889-149">Andere Editoren mit der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="1e889-149">Other editors with the command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="1e889-150">Überprüfen Sie Ihre Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e889-150">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="1e889-151">Erstellen einer neuen Anwendung:</span><span class="sxs-lookup"><span data-stu-id="1e889-151">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

2. <span data-ttu-id="1e889-152">Navigieren Sie zum Anwendungsverzeichnis:</span><span class="sxs-lookup"><span data-stu-id="1e889-152">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="1e889-153">Dieses Verzeichnis sollte nun eine Datei namens `Program.qs` enthalten. Dabei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="1e889-153">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="1e889-154">Sie können diese Vorlage mit einem Text-Editor ändern und mit ihren eigenen Quantum-Anwendungen überschreiben.</span><span class="sxs-lookup"><span data-stu-id="1e889-154">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

3. <span data-ttu-id="1e889-155">Führen Sie das Programm aus:</span><span class="sxs-lookup"><span data-stu-id="1e889-155">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

4. <span data-ttu-id="1e889-156">Der folgende Text sollte angezeigt werden: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="1e889-156">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="1e889-157">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1e889-157">Next steps</span></span>

<span data-ttu-id="1e889-158">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e889-158">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
