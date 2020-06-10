---
title: 'Entwickeln mit f #-Befehlszeilen Anwendungen'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630271"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="1fe17-102">Entwickeln mit f #-Befehlszeilen Anwendungen</span><span class="sxs-lookup"><span data-stu-id="1fe17-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="1fe17-103">F #-Programme können eigenständig, ohne Treiber in einer Host Sprache wie c#, F # oder python ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1fe17-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1fe17-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="1fe17-104">Prerequisites</span></span>

- [<span data-ttu-id="1fe17-105">.NET Core SDK 3.1 oder höher</span><span class="sxs-lookup"><span data-stu-id="1fe17-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="1fe17-106">Installation</span><span class="sxs-lookup"><span data-stu-id="1fe17-106">Installation</span></span>

<span data-ttu-id="1fe17-107">Obwohl Sie in jeder IDE q #-Befehlszeilen Anwendungen erstellen können, empfiehlt es sich, für Ihre Q #-Anwendungen Visual Studio Code (vs Code) oder die Visual Studio-IDE zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1fe17-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="1fe17-108">Die Entwicklung in diesen Tools ermöglicht den Zugriff auf umfangreiche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="1fe17-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="1fe17-109">So konfigurieren Sie vs Code:</span><span class="sxs-lookup"><span data-stu-id="1fe17-109">To configure VS Code:</span></span>

1. <span data-ttu-id="1fe17-110">Herunterladen und Installieren von [vs Code](https://code.visualstudio.com/download) (Windows, Linux und Mac).</span><span class="sxs-lookup"><span data-stu-id="1fe17-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="1fe17-111">Installieren Sie das [Microsoft QDK für vs Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="1fe17-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="1fe17-112">So konfigurieren Sie Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="1fe17-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="1fe17-113">Laden Sie [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 oder höher herunter, und installieren Sie es, wenn die Arbeitsauslastung der plattformübergreifenden .net Core-Entwicklung aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="1fe17-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="1fe17-114">Laden Sie [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)herunter, und installieren Sie es.</span><span class="sxs-lookup"><span data-stu-id="1fe17-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="1fe17-115">Entwickeln mit Q # mithilfe von vs Code</span><span class="sxs-lookup"><span data-stu-id="1fe17-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="1fe17-116">Installieren Sie die f #-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="1fe17-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="1fe17-117">Öffnen Sie Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="1fe17-117">Open VS Code.</span></span>
2. <span data-ttu-id="1fe17-118">Klicken **View**Sie auf  ->  **Befehls Palette**anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1fe17-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="1fe17-119">Wählen Sie **Q #: Projektvorlagen installieren**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="1fe17-120">Wenn die **Projektvorlagen erfolgreich installiert** wurden, kann das QDK mit ihren eigenen Anwendungen und Bibliotheken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fe17-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="1fe17-121">So erstellen Sie ein neues Projekt:</span><span class="sxs-lookup"><span data-stu-id="1fe17-121">To create a new project:</span></span>

1. <span data-ttu-id="1fe17-122">Klicken **View**Sie auf  ->  **Befehls Palette** anzeigen, und wählen Sie **Q #: Neues Projekt erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="1fe17-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="1fe17-123">Klicken Sie auf **eigenständige Konsolenanwendung**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="1fe17-124">Navigieren Sie zum Speicherort, um das Projekt zu speichern, und klicken Sie auf **Projekt erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="1fe17-125">Wenn das Projekt erfolgreich erstellt wurde, klicken Sie auf **Neues Projekt öffnen...** in der unteren rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="1fe17-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="1fe17-126">Überprüfen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1fe17-126">Inspect the project.</span></span> <span data-ttu-id="1fe17-127">Es sollte eine Quelldatei mit dem Namen angezeigt `Program.qs` werden, bei der es sich um ein Q #-Programm handelt, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.</span><span class="sxs-lookup"><span data-stu-id="1fe17-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1fe17-128">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="1fe17-128">To run the application:</span></span>
1. <span data-ttu-id="1fe17-129">Klicken Sie auf **Terminal**  ->  **neues Terminal**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="1fe17-130">Geben Sie an der Eingabeaufforderung ein `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="1fe17-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="1fe17-131">Im Ausgabefenster sollte der folgende Text angezeigt werden: `Hello quantum world!`.</span><span class="sxs-lookup"><span data-stu-id="1fe17-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="1fe17-132">Arbeitsbereiche mit mehreren Stamm Ordnern werden zurzeit von der vs Code Q #-Erweiterung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fe17-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="1fe17-133">Wenn Sie innerhalb eines VS Code-Arbeitsbereichs über mehrere Projekte verfügen, müssen alle Projekte in demselben Stammordner enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1fe17-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="1fe17-134">Entwickeln mit Q # mithilfe von Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1fe17-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="1fe17-135">Überprüfen Sie die Visual Studio-Installation, indem Sie eine Q #- `Hello World` Anwendung erstellen.</span><span class="sxs-lookup"><span data-stu-id="1fe17-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="1fe17-136">So erstellen Sie eine neue f #-Anwendung:</span><span class="sxs-lookup"><span data-stu-id="1fe17-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="1fe17-137">Öffnen Sie Visual Studio, und klicken Sie auf **Datei**  ->  **neu**  ->  **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="1fe17-138">Geben `Q#` Sie in das Suchfeld ein, wählen Sie **Q # Application** aus, und klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="1fe17-139">Geben Sie einen Namen und Speicherort für die Anwendung ein, und klicken Sie auf **Erstellen**.</span><span class="sxs-lookup"><span data-stu-id="1fe17-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="1fe17-140">Überprüfen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="1fe17-140">Inspect the project.</span></span> <span data-ttu-id="1fe17-141">Es sollte eine Quelldatei mit dem Namen angezeigt `Program.qs` werden, bei der es sich um ein Q #-Programm handelt, das einen einfachen Vorgang zum Drucken einer Meldung an die Konsole definiert.</span><span class="sxs-lookup"><span data-stu-id="1fe17-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="1fe17-142">So führen Sie die Anwendung aus:</span><span class="sxs-lookup"><span data-stu-id="1fe17-142">To run the application:</span></span>
1. <span data-ttu-id="1fe17-143">Wählen Sie **Debuggen**  ->  **Starten ohne Debugging**aus.</span><span class="sxs-lookup"><span data-stu-id="1fe17-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="1fe17-144">Der Text `Hello quantum world!` sollte in einem Konsolenfenster ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1fe17-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="1fe17-145">Wenn Sie mehrere Projekte in einer Visual Studio-Projekt Mappe haben, müssen sich alle in der Projekt Mappe enthaltenen Projekte im selben Ordner wie die Projekt Mappe oder in einem ihrer Unterordner befinden.</span><span class="sxs-lookup"><span data-stu-id="1fe17-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="1fe17-146">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="1fe17-146">Next steps</span></span>

<span data-ttu-id="1fe17-147">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung installiert haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fe17-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
