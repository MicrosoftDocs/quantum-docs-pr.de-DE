---
title: Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) aktualisieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ebf1f15d65a12c921cd3f04e4111d463d1060f8e
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463284"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="2dc3b-102">Aktualisieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="2dc3b-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="2dc3b-103">Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="2dc3b-104">In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="2dc3b-105">Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="2dc3b-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>


## <a name="updating-q-projects"></a><span data-ttu-id="2dc3b-106">Aktualisieren von f #-Projekten</span><span class="sxs-lookup"><span data-stu-id="2dc3b-106">Updating Q# Projects</span></span> 

1. <span data-ttu-id="2dc3b-107">Installieren Sie zunächst die neueste Version des [.net Core SDK 3,0](https://dotnet.microsoft.com/download) , und führen Sie den folgenden Befehl an der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="2dc3b-107">First, install the latest version of the [.NET Core SDK 3.0](https://dotnet.microsoft.com/download) and run the following command in the command prompt:</span></span>
```bash
dotnet --version
```
 <span data-ttu-id="2dc3b-108">Überprüfen Sie, ob die Ausgabe 3.0.100 oder höher ist, und befolgen Sie dann die Anweisungen unten abhängig von Ihrem Setup.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-108">Verify the output is 3.0.100 or higher, then follow the instructions below depending on your setup.</span></span>

### <a name="in-visual-studio"></a><span data-ttu-id="2dc3b-109">In Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2dc3b-109">In Visual Studio</span></span>
 
 1. <span data-ttu-id="2dc3b-110">Ein Update auf die neueste Version von Visual Studio 2019 finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="2dc3b-110">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
 2. <span data-ttu-id="2dc3b-111">Öffnen Sie die Projekt Mappe in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2dc3b-111">Open your solution in Visual Studio</span></span>
 3. <span data-ttu-id="2dc3b-112">Wählen Sie im Menü > Projekt Mappe bereinigen erstellen aus.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-112">From the menu, select Build > Clean Solution</span></span> 
 4. <span data-ttu-id="2dc3b-113">[Aktualisieren Sie das Ziel Framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in jeder ihrer csproj-Dateien auf netcoreapp 3.0 (oder netstandard 2.1, wenn es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="2dc3b-113">[Update the target framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
 5. <span data-ttu-id="2dc3b-114">Speichern und schließen Sie alle Dateien in der Projekt Mappe.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-114">Save and close all files in your solution</span></span>
 6. <span data-ttu-id="2dc3b-115">Wählen Sie Tools > Befehlszeile > aus Developer-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="2dc3b-115">Select Tools > Command Line > Developer Command Prompt</span></span>
 7. <span data-ttu-id="2dc3b-116">Führen Sie für jedes Projekt in der Projekt Mappe den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="2dc3b-116">For each project in the solution, run the following command:</span></span>
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
<span data-ttu-id="2dc3b-117">Wenn in Ihren Projekten andere Microsoft. Quantum-Pakete verwendet werden, führen Sie den Befehl ebenfalls für diese aus.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-117">If your projects use any other Microsoft.Quantum packages, run the command for these too.</span></span> 
 8. <span data-ttu-id="2dc3b-118">Schließen Sie die Eingabeaufforderung, und wählen Sie > Projekt Mappe erstellen aus (Wählen Sie *nicht* neu erstellen aus, da die Neuerstellung anfänglich fehlschlägt).</span><span class="sxs-lookup"><span data-stu-id="2dc3b-118">Close the command prompt and select Build > Build Solution (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

### <a name="in-visual-studio-code"></a><span data-ttu-id="2dc3b-119">In Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2dc3b-119">In Visual Studio Code</span></span>

1. <span data-ttu-id="2dc3b-120">Öffnen Sie in Visual Studio Code den Ordner mit dem zu Aktualisier nenden Projekt.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-120">In Visual Studio Code, open the folder containing the project to update</span></span>
1. <span data-ttu-id="2dc3b-121">Terminal > neues Terminal auswählen</span><span class="sxs-lookup"><span data-stu-id="2dc3b-121">Select Terminal > New Terminal</span></span>
1. <span data-ttu-id="2dc3b-122">Befolgen Sie die Anweisungen zum Aktualisieren mithilfe der Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-122">Follow the instructions for updating using the command line</span></span>

### <a name="using-the-command-line"></a><span data-ttu-id="2dc3b-123">Verwenden der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="2dc3b-123">Using the command line</span></span>

1. <span data-ttu-id="2dc3b-124">Navigieren Sie zu dem Ordner, der die Projektdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-124">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="2dc3b-125">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="2dc3b-125">Run the following command:</span></span>
```bash
dotnet clean [project_name].csproj
```

3. <span data-ttu-id="2dc3b-126">[Aktualisieren Sie das Ziel Framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in jeder ihrer csproj-Dateien auf netcoreapp 3.0 (oder netstandard 2.1, wenn es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="2dc3b-126">[Update the target framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
4. <span data-ttu-id="2dc3b-127">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="2dc3b-127">Run the following command:</span></span>
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
<span data-ttu-id="2dc3b-128">Wenn das Projekt andere Microsoft. Quantum-Pakete verwendet, führen Sie den Befehl ebenfalls für diese aus.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-128">if your project uses any other Microsoft.Quantum packages, run the command for these too.</span></span>

5. <span data-ttu-id="2dc3b-129">Alle Dateien speichern und schließen</span><span class="sxs-lookup"><span data-stu-id="2dc3b-129">Save and close all files</span></span>
6. <span data-ttu-id="2dc3b-130">Wiederholen Sie 1-4 für jede Projekt Abhängigkeit, und navigieren Sie dann zurück zu dem Ordner, der das Hauptprojekt enthält, und führen Sie aus</span><span class="sxs-lookup"><span data-stu-id="2dc3b-130">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a><span data-ttu-id="2dc3b-131">Aktualisieren von IQ # für python</span><span class="sxs-lookup"><span data-stu-id="2dc3b-131">Update IQ# for Python</span></span>

1. <span data-ttu-id="2dc3b-132">Aktualisieren des `iqsharp` Kernel</span><span class="sxs-lookup"><span data-stu-id="2dc3b-132">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="2dc3b-133">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="2dc3b-133">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="2dc3b-134">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-134">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```

1. <span data-ttu-id="2dc3b-135">Aktualisieren des `qsharp` Pakets</span><span class="sxs-lookup"><span data-stu-id="2dc3b-135">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="2dc3b-136">Überprüfen der `qsharp` Version</span><span class="sxs-lookup"><span data-stu-id="2dc3b-136">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="2dc3b-137">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-137">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. <span data-ttu-id="2dc3b-138">Führen Sie den folgenden Befehl am Speicherort Ihrer `.qs` Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-138">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. <span data-ttu-id="2dc3b-139">Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-139">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="2dc3b-140">Aktualisieren von IQ # für jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="2dc3b-140">Update IQ# for Jupyter notebooks</span></span>

1. <span data-ttu-id="2dc3b-141">Aktualisieren des `iqsharp` Kernel</span><span class="sxs-lookup"><span data-stu-id="2dc3b-141">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="2dc3b-142">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="2dc3b-142">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="2dc3b-143">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-143">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. <span data-ttu-id="2dc3b-144">Führen Sie den folgenden Befehl aus einer Zelle im Jupyter Notebook aus:</span><span class="sxs-lookup"><span data-stu-id="2dc3b-144">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

1. <span data-ttu-id="2dc3b-145">Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-145">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="2dc3b-146">Visual Studio-QDK-Erweiterung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="2dc3b-146">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="2dc3b-147">Aktualisieren der f # Visual Studio-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2dc3b-147">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="2dc3b-148">Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-148">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="2dc3b-149">Akzeptieren des Updates</span><span class="sxs-lookup"><span data-stu-id="2dc3b-149">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="2dc3b-150">Die Projektvorlagen werden mit der Erweiterung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-150">The project templates are updated with the extension.</span></span> <span data-ttu-id="2dc3b-151">Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-151">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="2dc3b-152">Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-152">The code for your existing projects is not updated when the extension is updated.</span></span>

## <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="2dc3b-153">Update vs Code QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2dc3b-153">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="2dc3b-154">Aktualisieren der Quantum-vs Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="2dc3b-154">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="2dc3b-155">Neustart vs Code</span><span class="sxs-lookup"><span data-stu-id="2dc3b-155">Restart VS Code</span></span>
    - <span data-ttu-id="2dc3b-156">Navigieren Sie zur Registerkarte **Erweiterungen** .</span><span class="sxs-lookup"><span data-stu-id="2dc3b-156">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="2dc3b-157">Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .</span><span class="sxs-lookup"><span data-stu-id="2dc3b-157">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="2dc3b-158">Erweiterung erneut laden</span><span class="sxs-lookup"><span data-stu-id="2dc3b-158">Reload the extension</span></span>

1. <span data-ttu-id="2dc3b-159">Aktualisieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="2dc3b-159">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="2dc3b-160">Gehe zu **Ansicht** -> **Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="2dc3b-160">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="2dc3b-161">Auswählen von " **Q #: Install Project Templates** "</span><span class="sxs-lookup"><span data-stu-id="2dc3b-161">Select **Q#: Install project templates**</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="2dc3b-162">C#mit dem Befehlszeilen Tool "`dotnet`"</span><span class="sxs-lookup"><span data-stu-id="2dc3b-162">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="2dc3b-163">Aktualisieren der Quantum-Projektvorlagen für .net</span><span class="sxs-lookup"><span data-stu-id="2dc3b-163">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="2dc3b-164">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="2dc3b-164">What's next?</span></span>

<span data-ttu-id="2dc3b-165">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung aktualisiert haben, können Sie weiterhin ihre Quantum-Programme entwickeln und ausführen.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-165">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="2dc3b-166">Wenn Sie noch kein Programm geschrieben haben, können Sie mit [Ihrem ersten Quantum-Programm](xref:microsoft.quantum.write-program)beginnen.</span><span class="sxs-lookup"><span data-stu-id="2dc3b-166">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
