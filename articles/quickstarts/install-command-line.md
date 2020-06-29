---
title: Entwickeln mit Q#-Befehlszeilenanwendungen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274120"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="c1d57-102">Entwickeln mit Q#-Befehlszeilenanwendungen</span><span class="sxs-lookup"><span data-stu-id="c1d57-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="c1d57-103">Q#-Programme können allein ohne Treiber in einer Hostsprache wie C#, F# oder Python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c1d57-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1d57-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c1d57-104">Prerequisites</span></span>

- [<span data-ttu-id="c1d57-105">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="c1d57-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="c1d57-106">Installation</span><span class="sxs-lookup"><span data-stu-id="c1d57-106">Installation</span></span>

<span data-ttu-id="c1d57-107">Sie können Q#-Befehlszeilenanwendungen zwar in einer beliebigen IDE erstellen, aber wir empfehlen Ihnen, für Ihre Q#-Anwendungen Visual Studio Code (VS Code) oder Visual Studio als IDE zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="c1d57-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="c1d57-108">Bei der Entwicklung in diesen Tools haben Sie Zugriff auf einen großen Funktionsumfang.</span><span class="sxs-lookup"><span data-stu-id="c1d57-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="c1d57-109">Gehen Sie zum Konfigurieren von VS Code wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c1d57-109">To configure VS Code:</span></span>

1. <span data-ttu-id="c1d57-110">Laden Sie [VS Code](https://code.visualstudio.com/download) herunter, und führen Sie die Installation durch (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="c1d57-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="c1d57-111">Installieren Sie das [Microsoft QDK für VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="c1d57-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="c1d57-112">Gehen Sie zum Konfigurieren von Visual Studio wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="c1d57-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="c1d57-113">Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 oder höher herunter, und installieren Sie die Anwendung mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload.</span><span class="sxs-lookup"><span data-stu-id="c1d57-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="c1d57-114">Laden Sie das [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="c1d57-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="c1d57-115">Entwickeln mit Q# mithilfe von VS Code</span><span class="sxs-lookup"><span data-stu-id="c1d57-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="c1d57-116">Installieren Sie die Q#-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="c1d57-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="c1d57-117">Öffnen Sie Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="c1d57-117">Open VS Code.</span></span>
2. <span data-ttu-id="c1d57-118">Klicken Sie auf **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="c1d57-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="c1d57-119">Wählen Sie **Q#: Projektvorlagen installieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c1d57-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="c1d57-120">Wenn die Meldung mit dem Hinweis angezeigt wird, dass die **Installation der Projektvorlagen erfolgreich war**, ist das QDK für die Verwendung mit Ihren eigenen Anwendungen und Bibliotheken bereit.</span><span class="sxs-lookup"><span data-stu-id="c1d57-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="c1d57-121">Erstellen Sie wie folgt ein neues Projekt:</span><span class="sxs-lookup"><span data-stu-id="c1d57-121">To create a new project:</span></span>

1. <span data-ttu-id="c1d57-122">Klicken Sie auf **Ansicht** -> **Befehlspalette**, und wählen Sie **Q#: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="c1d57-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="c1d57-123">Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).</span><span class="sxs-lookup"><span data-stu-id="c1d57-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="c1d57-124">Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="c1d57-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="c1d57-125">Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).</span><span class="sxs-lookup"><span data-stu-id="c1d57-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="c1d57-126">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c1d57-126">Inspect the project.</span></span> <span data-ttu-id="c1d57-127">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c1d57-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="c1d57-128">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="c1d57-128">To run the application:</span></span>
1. <span data-ttu-id="c1d57-129">Klicken Sie auf **Terminal** -> **Neues Terminal**.</span><span class="sxs-lookup"><span data-stu-id="c1d57-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="c1d57-130">Geben Sie an der Eingabeaufforderung des Terminals `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="c1d57-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="c1d57-131">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="c1d57-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="c1d57-132">Arbeitsbereiche mit mehreren Stammordnern werden von der VS Code-Q#-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1d57-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="c1d57-133">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c1d57-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="c1d57-134">Entwickeln mit Q# mithilfe von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c1d57-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="c1d57-135">Überprüfen Sie Ihre Visual Studio-Installation, indem Sie eine Q#-Anwendung vom Typ `Hello World` erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1d57-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="c1d57-136">Erstellen Sie wie folgt eine neue Q#-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="c1d57-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="c1d57-137">Öffnen Sie Visual Studio, und klicken Sie auf **Datei** -> **Neu** -> **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c1d57-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="c1d57-138">Geben Sie im Suchfeld den Begriff `Q#` ein, wählen Sie **Q#-Anwendung** aus, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="c1d57-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="c1d57-139">Geben Sie einen Namen und Speicherort für Ihre Anwendung ein, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="c1d57-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="c1d57-140">Untersuchen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="c1d57-140">Inspect the project.</span></span> <span data-ttu-id="c1d57-141">Es sollte eine Quelldatei mit dem Namen `Program.qs` angezeigt werden. Hierbei handelt es sich um ein Q#-Programm, mit dem ein einfacher Vorgang zum Ausgeben einer Meldung in der Konsole definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c1d57-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="c1d57-142">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="c1d57-142">To run the application:</span></span>
1. <span data-ttu-id="c1d57-143">Wählen Sie **Debuggen** -> **Ohne Debuggen starten** aus.</span><span class="sxs-lookup"><span data-stu-id="c1d57-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="c1d57-144">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1d57-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="c1d57-145">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe bzw. in einem der Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="c1d57-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="c1d57-146">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c1d57-146">Next steps</span></span>

<span data-ttu-id="c1d57-147">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1d57-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
