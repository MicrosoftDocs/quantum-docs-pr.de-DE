---
title: Aktualisieren des quantumentwicklungskit (QDK)
description: 'Hier wird beschrieben, wie Sie die f #-Projekte und die Microsoft Quantum Development Kit auf die aktuelle Version aktualisieren.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 53f72f1d49ae32a5a8572a1cf68a66a1d9b45e4a
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426910"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="75e2d-103">Aktualisieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="75e2d-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="75e2d-104">Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="75e2d-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="75e2d-105">In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben.</span><span class="sxs-lookup"><span data-stu-id="75e2d-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="75e2d-106">Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="75e2d-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="75e2d-107">Es wird empfohlen, mit der neuesten QDK-Version auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="75e2d-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="75e2d-108">Führen Sie dieses Update Handbuch aus, um ein Upgrade auf die neueste Version des QDK auszuführen.</span><span class="sxs-lookup"><span data-stu-id="75e2d-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="75e2d-109">Der Prozess besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="75e2d-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="75e2d-110">Aktualisieren vorhandener Q #-Dateien und-Projekte, um Ihren Code mit einer beliebigen aktualisierten Syntax auszurichten</span><span class="sxs-lookup"><span data-stu-id="75e2d-110">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="75e2d-111">Das QDK selbst für die ausgewählte Entwicklungsumgebung wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75e2d-111">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="75e2d-112">Aktualisieren von f #-Projekten</span><span class="sxs-lookup"><span data-stu-id="75e2d-112">Updating Q# Projects</span></span> 

<span data-ttu-id="75e2d-113">Unabhängig davon, ob Sie c# oder python zum Hosten von q #-Vorgängen verwenden, befolgen Sie diese Anweisungen, um Ihre q #-Projekte zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="75e2d-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="75e2d-114">Überprüfen Sie zunächst, ob Sie über die neueste Version des [.net Core SDK 3,1](https://dotnet.microsoft.com/download)verfügen.</span><span class="sxs-lookup"><span data-stu-id="75e2d-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="75e2d-115">Führen Sie den folgenden Befehl an der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="75e2d-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="75e2d-116">Überprüfen Sie, ob die Ausgabe `3.1.100` oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="75e2d-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="75e2d-117">Falls nicht, installieren Sie die [neueste Version](https://dotnet.microsoft.com/download) , und überprüfen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="75e2d-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="75e2d-118">Befolgen Sie dann die Anweisungen unten abhängig von Ihrem Setup (Visual Studio, Visual Studio Code oder direkt über die Befehlszeile).</span><span class="sxs-lookup"><span data-stu-id="75e2d-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="75e2d-119">Aktualisieren von f #-Projekten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75e2d-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="75e2d-120">Ein Update auf die neueste Version von Visual Studio 2019 finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="75e2d-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="75e2d-121">Öffnen Sie die Projekt Mappe in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75e2d-121">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="75e2d-122">Wählen Sie im Menü Projekt Mappe **Erstellen**  ->  **Bereinigen** aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-122">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="75e2d-123">Aktualisieren Sie in jeder ihrer csproj-Dateien das Ziel Framework auf `netcoreapp3.1` (oder, `netstandard2.1` Wenn es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="75e2d-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="75e2d-124">Das heißt, Sie bearbeiten die Zeilen in der Form:</span><span class="sxs-lookup"><span data-stu-id="75e2d-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="75e2d-125">Weitere Informationen zum Angeben von Ziel Frameworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="75e2d-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="75e2d-126">Speichern und schließen Sie alle Dateien in der Projekt Mappe.</span><span class="sxs-lookup"><span data-stu-id="75e2d-126">Save and close all files in your solution</span></span>
6. <span data-ttu-id="75e2d-127">**Tools**  ->  **Befehlszeile**für Tools auswählen  ->  **Developer-Eingabeaufforderung**</span><span class="sxs-lookup"><span data-stu-id="75e2d-127">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="75e2d-128">Führen Sie für jedes Projekt in der Projekt Mappe den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="75e2d-128">For each project in the solution, run the following command:</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="75e2d-129">Wenn Ihre Projekte andere Microsoft. Quantum-Pakete (z. b. Microsoft. Quantum. Numerics) verwenden, führen Sie den Befehl ebenfalls für diese aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-129">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="75e2d-130">Schließen Sie die Eingabeaufforderung, und wählen Sie Buildprojektmappe **Erstellen**  ->  **Build Solution** (Projekt Mappe neu erstellen) *not* aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-130">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution)</span></span>

<span data-ttu-id="75e2d-131">Nun können Sie mit [Aktualisieren Ihrer Visual Studio-QDK-Erweiterung](#update-visual-studio-qdk-extension)fortfahren.</span><span class="sxs-lookup"><span data-stu-id="75e2d-131">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="75e2d-132">Aktualisieren von f #-Projekten in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="75e2d-132">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="75e2d-133">Öffnen Sie in Visual Studio Code den Ordner mit dem zu Aktualisier nenden Projekt.</span><span class="sxs-lookup"><span data-stu-id="75e2d-133">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="75e2d-134">Wählen Sie **Terminal**  ->  **neues Terminal** aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-134">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="75e2d-135">Befolgen Sie die Anweisungen zum Aktualisieren mithilfe der Befehlszeile (direkt unten).</span><span class="sxs-lookup"><span data-stu-id="75e2d-135">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="75e2d-136">Aktualisieren von f #-Projekten mithilfe der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="75e2d-136">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="75e2d-137">Navigieren Sie zu dem Ordner, der die Projektdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="75e2d-137">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="75e2d-138">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="75e2d-138">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="75e2d-139">Aktualisieren Sie in jeder ihrer csproj-Dateien das Ziel Framework auf `netcoreapp3.1` (oder, `netstandard2.1` Wenn es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="75e2d-139">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="75e2d-140">Das heißt, Sie bearbeiten die Zeilen in der Form:</span><span class="sxs-lookup"><span data-stu-id="75e2d-140">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="75e2d-141">Weitere Informationen zum Angeben von Ziel Frameworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="75e2d-141">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="75e2d-142">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="75e2d-142">Run the following command:</span></span>

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    <span data-ttu-id="75e2d-143">Wenn das Projekt andere Microsoft. Quantum-Pakete (z. b. Microsoft. Quantum. Numerics) verwendet, führen Sie den Befehl ebenfalls für diese aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-143">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="75e2d-144">Speichern und schließen Sie alle Dateien.</span><span class="sxs-lookup"><span data-stu-id="75e2d-144">Save and close all files.</span></span>
6. <span data-ttu-id="75e2d-145">Wiederholen Sie 1-4 für jede Projekt Abhängigkeit, und navigieren Sie dann zurück zu dem Ordner, der das Hauptprojekt enthält, und führen Sie aus</span><span class="sxs-lookup"><span data-stu-id="75e2d-145">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="75e2d-146">Nachdem Sie Ihre Q #-Projekte aktualisiert haben, befolgen Sie die nachfolgenden Anweisungen, um das QDK selbst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="75e2d-146">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="75e2d-147">Aktualisieren des QDK</span><span class="sxs-lookup"><span data-stu-id="75e2d-147">Updating the QDK</span></span>

<span data-ttu-id="75e2d-148">Der Aktualisierungsprozess für das QDK hängt von der Entwicklungssprache und-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="75e2d-148">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="75e2d-149">Wählen Sie unten Ihre Entwicklungsumgebung aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-149">Select your development environment below.</span></span>

* [<span data-ttu-id="75e2d-150">Python: Aktualisieren der IQ #-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-150">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="75e2d-151">Jupyter-Notebooks: Aktualisieren der IQ #-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-151">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="75e2d-152">Visual Studio: Aktualisieren der QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-152">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="75e2d-153">VS Code: Aktualisieren der QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-153">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="75e2d-154">Befehlszeile und c#: Aktualisieren von Projektvorlagen</span><span class="sxs-lookup"><span data-stu-id="75e2d-154">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="75e2d-155">Aktualisieren von IQ # für python</span><span class="sxs-lookup"><span data-stu-id="75e2d-155">Update IQ# for Python</span></span>

1. <span data-ttu-id="75e2d-156">Aktualisieren des `iqsharp` Kernels</span><span class="sxs-lookup"><span data-stu-id="75e2d-156">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="75e2d-157">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="75e2d-157">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="75e2d-158">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75e2d-158">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="75e2d-159">Machen Sie sich keine Sorgen, wenn Ihre `iqsharp` Version höher ist, sollte Sie der [neuesten](xref:microsoft.quantum.relnotes)Version entsprechen.</span><span class="sxs-lookup"><span data-stu-id="75e2d-159">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="75e2d-160">Aktualisieren des `qsharp` Pakets</span><span class="sxs-lookup"><span data-stu-id="75e2d-160">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="75e2d-161">Überprüfen der `qsharp` Version</span><span class="sxs-lookup"><span data-stu-id="75e2d-161">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="75e2d-162">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="75e2d-162">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="75e2d-163">Führen Sie den folgenden Befehl am Speicherort der `.qs` Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="75e2d-163">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="75e2d-164">Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.</span><span class="sxs-lookup"><span data-stu-id="75e2d-164">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="75e2d-165">Aktualisieren von IQ # für jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="75e2d-165">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="75e2d-166">Aktualisieren des `iqsharp` Kernels</span><span class="sxs-lookup"><span data-stu-id="75e2d-166">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="75e2d-167">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="75e2d-167">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="75e2d-168">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="75e2d-168">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="75e2d-169">Machen Sie sich keine Sorgen, wenn Ihre `iqsharp` Version höher ist, sollte Sie der [neuesten](xref:microsoft.quantum.relnotes)Version entsprechen.</span><span class="sxs-lookup"><span data-stu-id="75e2d-169">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="75e2d-170">Führen Sie den folgenden Befehl aus einer Zelle im Jupyter Notebook aus:</span><span class="sxs-lookup"><span data-stu-id="75e2d-170">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="75e2d-171">Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="75e2d-171">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="75e2d-172">Visual Studio-QDK-Erweiterung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="75e2d-172">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="75e2d-173">Aktualisieren der f # Visual Studio-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-173">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="75e2d-174">Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="75e2d-174">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="75e2d-175">Akzeptieren des Updates</span><span class="sxs-lookup"><span data-stu-id="75e2d-175">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="75e2d-176">Die Projektvorlagen werden mit der Erweiterung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="75e2d-176">The project templates are updated with the extension.</span></span> <span data-ttu-id="75e2d-177">Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte.</span><span class="sxs-lookup"><span data-stu-id="75e2d-177">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="75e2d-178">Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="75e2d-178">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="75e2d-179">Update vs Code QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-179">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="75e2d-180">Aktualisieren der Quantum-vs Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="75e2d-180">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="75e2d-181">Neustart vs Code</span><span class="sxs-lookup"><span data-stu-id="75e2d-181">Restart VS Code</span></span>
    - <span data-ttu-id="75e2d-182">Navigieren Sie zur Registerkarte **Erweiterungen** .</span><span class="sxs-lookup"><span data-stu-id="75e2d-182">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="75e2d-183">Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .</span><span class="sxs-lookup"><span data-stu-id="75e2d-183">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="75e2d-184">Erweiterung erneut laden</span><span class="sxs-lookup"><span data-stu-id="75e2d-184">Reload the extension</span></span>

2. <span data-ttu-id="75e2d-185">Aktualisieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="75e2d-185">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="75e2d-186">Gehe zu **Anzeige**-  ->  **Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="75e2d-186">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="75e2d-187">Auswählen von " **Q #: Install Project Templates** "</span><span class="sxs-lookup"><span data-stu-id="75e2d-187">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="75e2d-188">Nach wenigen Sekunden sollte ein Popup mit der Bestätigung angezeigt werden, dass die Projektvorlagen erfolgreich installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="75e2d-188">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="75e2d-189">C# mit dem `dotnet` Befehlszeilen Tool</span><span class="sxs-lookup"><span data-stu-id="75e2d-189">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="75e2d-190">Aktualisieren der Quantum-Projektvorlagen für .net</span><span class="sxs-lookup"><span data-stu-id="75e2d-190">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```