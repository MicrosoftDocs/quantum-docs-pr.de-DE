---
title: 'F #-Programme ohne Treiber und Host Sprache ausführen'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706800"
---
# <a name="q-command-line-applications"></a><span data-ttu-id="af00b-102">F #-Befehlszeilen Anwendungen</span><span class="sxs-lookup"><span data-stu-id="af00b-102">Q# Command Line Applications</span></span>

<span data-ttu-id="af00b-103">F #-Programme können eigenständig, ohne Treiber in einer Host Sprache wie c#, F # oder python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="af00b-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="af00b-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="af00b-104">Pre-requisites</span></span>

- [<span data-ttu-id="af00b-105">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="af00b-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="af00b-106">Installation</span><span class="sxs-lookup"><span data-stu-id="af00b-106">Installation</span></span>

<span data-ttu-id="af00b-107">Obwohl Sie in jeder IDE q #-Befehlszeilen Anwendungen erstellen können, wird dringend empfohlen, Visual Studio Code (vs Code) oder die Visual Studio-IDE für Ihre Q #-Anwendungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="af00b-107">While you can build Q# command line applications in any IDE, we highly recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="af00b-108">Wenn Sie vs Code oder Visual Studio und die QDK-Visual Studio Code Erweiterung verwenden, erhalten Sie Zugriff auf umfangreichere Funktionen.</span><span class="sxs-lookup"><span data-stu-id="af00b-108">By using VS Code or Visual Studio and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

- <span data-ttu-id="af00b-109">Installieren von [vs Code](https://code.visualstudio.com/download) (Windows, Linux und Mac)</span><span class="sxs-lookup"><span data-stu-id="af00b-109">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
- <span data-ttu-id="af00b-110">Installieren Sie die [QDK-Erweiterung für vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) oder</span><span class="sxs-lookup"><span data-stu-id="af00b-110">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) OR</span></span>
- <span data-ttu-id="af00b-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 mit aktivierter plattformübergreifender .NET Core-Entwicklungsworkload</span><span class="sxs-lookup"><span data-stu-id="af00b-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>
- <span data-ttu-id="af00b-112">Herunterladen und Installieren der [Visual Studio-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="af00b-112">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="af00b-113">Entwickeln mit Q # mithilfe von vs Code</span><span class="sxs-lookup"><span data-stu-id="af00b-113">Develop with Q# using VS Code</span></span>

<span data-ttu-id="af00b-114">Installieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="af00b-114">Install the Quantum project templates:</span></span>

- <span data-ttu-id="af00b-115">Gehe zu **Anzeige** -> -**Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="af00b-115">Go to **View** -> **Command Palette**</span></span>
- <span data-ttu-id="af00b-116">Auswählen von " **Q #: Install Project Templates** "</span><span class="sxs-lookup"><span data-stu-id="af00b-116">Select **Q#: Install project templates**</span></span>

<span data-ttu-id="af00b-117">Sie haben das Quantum Development Kit jetzt installiert und können es in Ihren eigenen Anwendungen und Bibliotheken verwenden.</span><span class="sxs-lookup"><span data-stu-id="af00b-117">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>
- <span data-ttu-id="af00b-118">Erstellen eines neuen Projekts:</span><span class="sxs-lookup"><span data-stu-id="af00b-118">Create a new project:</span></span>
  - <span data-ttu-id="af00b-119">Gehe zu **Anzeige** -> -**Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="af00b-119">Go to **View** -> **Command Palette**</span></span>
  - <span data-ttu-id="af00b-120">Wählen Sie **Q #: Neues Projekt erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="af00b-120">Select **Q#: Create New Project**</span></span>
  - <span data-ttu-id="af00b-121">**Eigenständige Konsolenanwendung** auswählen</span><span class="sxs-lookup"><span data-stu-id="af00b-121">Select **Standalone console application**</span></span>
  - <span data-ttu-id="af00b-122">Navigieren Sie im Dateisystem zu dem Speicherort, an dem Sie die Anwendung erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="af00b-122">Navigate to the location on the file system where you would like to create the application</span></span>
  - <span data-ttu-id="af00b-123">Klicken Sie nach Abschluss der Projekterstellung auf die Schaltfläche **Open new project...** (Neues Projekt öffnen).</span><span class="sxs-lookup"><span data-stu-id="af00b-123">Click on the **Open new project...** button, once the project has been created</span></span>
        
- <span data-ttu-id="af00b-124">Untersuchen des Projekts</span><span class="sxs-lookup"><span data-stu-id="af00b-124">Inspect the project</span></span>
  - <span data-ttu-id="af00b-125">Sie sollten sehen, dass eine Datei `Program.qs` mit dem Namen created erstellt wurde. Hierbei handelt es sich um ein Q #-Programm, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.</span><span class="sxs-lookup"><span data-stu-id="af00b-125">You should see that a file called `Program.qs` created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="af00b-126">Führen Sie die Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="af00b-126">Run the application:</span></span>
  - <span data-ttu-id="af00b-127">Zum **Terminal** -> **neuen Terminal** wechseln</span><span class="sxs-lookup"><span data-stu-id="af00b-127">Go to **Terminal** -> **New Terminal**</span></span>
  - <span data-ttu-id="af00b-128">Geben Sie `dotnet run` ein.</span><span class="sxs-lookup"><span data-stu-id="af00b-128">Enter `dotnet run`</span></span>
  - <span data-ttu-id="af00b-129">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="af00b-129">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="af00b-130">Arbeitsbereiche mit mehreren Stammordnern werden von der Visual Studio Code-Erweiterung derzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="af00b-130">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="af00b-131">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="af00b-131">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="af00b-132">Entwickeln mit Q # mithilfe von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af00b-132">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="af00b-133">Überprüfen der Installation durch die Erstellung einer `Hello World`-Anwendung</span><span class="sxs-lookup"><span data-stu-id="af00b-133">Verify the installation by creating a `Hello World` application</span></span>

- <span data-ttu-id="af00b-134">Erstellen einer neuen Q#-Anwendung</span><span class="sxs-lookup"><span data-stu-id="af00b-134">Create a new Q# application</span></span>
  - <span data-ttu-id="af00b-135">Wechseln Sie zu **Datei** -> **Neues** -> **Projekt** .</span><span class="sxs-lookup"><span data-stu-id="af00b-135">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="af00b-136">Geben Sie im Suchfeld als Suchbegriff `Q#` ein.</span><span class="sxs-lookup"><span data-stu-id="af00b-136">Type `Q#` in the search box</span></span>
  - <span data-ttu-id="af00b-137">Wählen Sie **Q#-Anwendung** aus.</span><span class="sxs-lookup"><span data-stu-id="af00b-137">Select **Q# Application**</span></span>
  - <span data-ttu-id="af00b-138">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="af00b-138">Select **Next**</span></span>
  - <span data-ttu-id="af00b-139">Wählen Sie einen Namen und Speicherort für Ihre Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="af00b-139">Choose a name and location for your application</span></span>
  - <span data-ttu-id="af00b-140">Klicken Sie auf **Erstellen**</span><span class="sxs-lookup"><span data-stu-id="af00b-140">Select **Create**</span></span>

- <span data-ttu-id="af00b-141">Untersuchen des Projekts</span><span class="sxs-lookup"><span data-stu-id="af00b-141">Inspect the project</span></span>
  - <span data-ttu-id="af00b-142">Sie sollten sehen, dass eine Datei `Program.qs` mit dem Namen erstellt wurde. Hierbei handelt es sich um ein Q #-Programm, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.</span><span class="sxs-lookup"><span data-stu-id="af00b-142">You should see that a file called `Program.qs` has been created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="af00b-143">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="af00b-143">Run the application</span></span>
  - <span data-ttu-id="af00b-144">**Debuggen** -> **Starten ohne Debugging** auswählen</span><span class="sxs-lookup"><span data-stu-id="af00b-144">Select **Debug** -> **Start Without Debugging**</span></span>
  - <span data-ttu-id="af00b-145">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="af00b-145">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="af00b-146">Falls Sie über mehrere Projekte innerhalb einer Visual Studio-Projektmappe verfügen, müssen sich alle darin enthaltenen Projekte in demselben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="af00b-146">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  


## <a name="whats-next"></a><span data-ttu-id="af00b-147">Ausblick</span><span class="sxs-lookup"><span data-stu-id="af00b-147">What's next?</span></span>

<span data-ttu-id="af00b-148">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.write-program) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="af00b-148">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
