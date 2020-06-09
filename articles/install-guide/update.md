---
title: Aktualisieren des quantumentwicklungskit (QDK)
description: 'Hier wird beschrieben, wie Sie die f #-Projekte und die Microsoft Quantum Development Kit auf die aktuelle Version aktualisieren.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 89db1a671767b0cc083a251918bbeeed2b39b883
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578180"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="55f70-103">Aktualisieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="55f70-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="55f70-104">Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55f70-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="55f70-105">In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben.</span><span class="sxs-lookup"><span data-stu-id="55f70-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="55f70-106">Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="55f70-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="55f70-107">Es wird empfohlen, mit der neuesten QDK-Version auf dem neuesten Stand zu bleiben.</span><span class="sxs-lookup"><span data-stu-id="55f70-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="55f70-108">Führen Sie dieses Update Handbuch aus, um ein Upgrade auf die neueste Version des QDK auszuführen.</span><span class="sxs-lookup"><span data-stu-id="55f70-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="55f70-109">Der Prozess besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="55f70-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="55f70-110">Aktualisieren vorhandener Q #-Dateien und-Projekte, um den Code mit einer beliebigen aktualisierten Syntax auszurichten.</span><span class="sxs-lookup"><span data-stu-id="55f70-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="55f70-111">Das QDK selbst für die ausgewählte Entwicklungsumgebung wird aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="55f70-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="55f70-112">Aktualisieren von f #-Projekten</span><span class="sxs-lookup"><span data-stu-id="55f70-112">Updating Q# Projects</span></span> 

<span data-ttu-id="55f70-113">Unabhängig davon, ob Sie c# oder python zum Hosten von q #-Vorgängen verwenden, befolgen Sie diese Anweisungen, um Ihre q #-Projekte zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55f70-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="55f70-114">Überprüfen Sie zunächst, ob Sie über die neueste Version des [.net Core SDK 3,1](https://dotnet.microsoft.com/download)verfügen.</span><span class="sxs-lookup"><span data-stu-id="55f70-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="55f70-115">Führen Sie den folgenden Befehl an der Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="55f70-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="55f70-116">Überprüfen Sie, ob die Ausgabe `3.1.100` oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="55f70-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="55f70-117">Falls nicht, installieren Sie die [neueste Version](https://dotnet.microsoft.com/download) , und überprüfen Sie Sie erneut.</span><span class="sxs-lookup"><span data-stu-id="55f70-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="55f70-118">Befolgen Sie dann die Anweisungen unten abhängig von Ihrem Setup (Visual Studio, Visual Studio Code oder direkt über die Befehlszeile).</span><span class="sxs-lookup"><span data-stu-id="55f70-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="55f70-119">Aktualisieren von f #-Projekten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="55f70-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="55f70-120">Ein Update auf die neueste Version von Visual Studio 2019 finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) .</span><span class="sxs-lookup"><span data-stu-id="55f70-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="55f70-121">Öffnen Sie Ihre Projektmappe in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="55f70-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="55f70-122">Wählen Sie im Menü Projekt Mappe **Erstellen**  ->  **Bereinigen**aus.</span><span class="sxs-lookup"><span data-stu-id="55f70-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="55f70-123">Aktualisieren Sie in jeder ihrer csproj-Dateien das Ziel Framework auf `netcoreapp3.1` (oder, `netstandard2.1` Wenn es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="55f70-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="55f70-124">Das heißt, Sie bearbeiten die Zeilen in der Form:</span><span class="sxs-lookup"><span data-stu-id="55f70-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="55f70-125">Weitere Informationen zum Angeben von Ziel Frameworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="55f70-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="55f70-126">Legen Sie in jeder der csproj-Dateien das SDK auf fest `Microsoft.Quantum.Sdk` , wie in der folgenden Zeile angegeben.</span><span class="sxs-lookup"><span data-stu-id="55f70-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="55f70-127">Beachten Sie, dass die Versionsnummer die neueste verfügbare Version sein sollte, und Sie können Sie ermitteln, indem Sie die [Anmerkungen](https://docs.microsoft.com/quantum/relnotes/)zu dieser Version überprüfen.</span><span class="sxs-lookup"><span data-stu-id="55f70-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="55f70-128">Speichern und schließen Sie alle Dateien in der Projekt Mappe.</span><span class="sxs-lookup"><span data-stu-id="55f70-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="55f70-129">Wählen Sie **Tools**  ->  **Befehlszeile**  ->  **Developer-Eingabeaufforderung**aus.</span><span class="sxs-lookup"><span data-stu-id="55f70-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="55f70-130">Alternativ können Sie die Paket Verwaltungskonsole in Visual Studio verwenden.</span><span class="sxs-lookup"><span data-stu-id="55f70-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="55f70-131">Führen Sie für jedes Projekt in der Projekt Mappe den folgenden Befehl aus, um dieses Paket zu **Entfernen** :</span><span class="sxs-lookup"><span data-stu-id="55f70-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="55f70-132">Wenn Ihre Projekte andere Microsoft. Quantum-oder Microsoft. Azure. Quantum-Pakete (z. b. Microsoft. Quantum. Numerics) verwenden, führen Sie den Befehl **Hinzufügen** aus, um die verwendete Version zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55f70-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="55f70-133">Schließen Sie die Eingabeaufforderung, und wählen Sie Buildprojektmappe **Erstellen**aus  ->  (Wählen Sie *nicht* neu erstellen).**Build Solution**</span><span class="sxs-lookup"><span data-stu-id="55f70-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="55f70-134">Nun können Sie mit [Aktualisieren Ihrer Visual Studio-QDK-Erweiterung](#update-visual-studio-qdk-extension)fortfahren.</span><span class="sxs-lookup"><span data-stu-id="55f70-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="55f70-135">Aktualisieren von f #-Projekten in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="55f70-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="55f70-136">Öffnen Sie in Visual Studio Code den Ordner mit dem zu Aktualisier nenden Projekt.</span><span class="sxs-lookup"><span data-stu-id="55f70-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="55f70-137">Wählen Sie **Terminal**  ->  **neues Terminal**aus.</span><span class="sxs-lookup"><span data-stu-id="55f70-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="55f70-138">Befolgen Sie die Anweisungen zum Aktualisieren mithilfe der Befehlszeile (direkt unten).</span><span class="sxs-lookup"><span data-stu-id="55f70-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="55f70-139">Aktualisieren von f #-Projekten mithilfe der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="55f70-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="55f70-140">Navigieren Sie zu dem Ordner, der die Hauptprojekt Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="55f70-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="55f70-141">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="55f70-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="55f70-142">Legen Sie die aktuelle Version des QDK fest.</span><span class="sxs-lookup"><span data-stu-id="55f70-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="55f70-143">Um es zu finden, können Sie die [Anmerkungen](https://docs.microsoft.com/quantum/relnotes/)zu dieser Version lesen.</span><span class="sxs-lookup"><span data-stu-id="55f70-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="55f70-144">Die Version weist ein ähnliches Format auf `0.11.2006.207` .</span><span class="sxs-lookup"><span data-stu-id="55f70-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="55f70-145">Durchlaufen Sie in jeder Ihrer `.csproj` Dateien die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="55f70-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="55f70-146">Aktualisieren Sie das Ziel Framework auf `netcoreapp3.1` (oder, `netstandard2.1` Wenn es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="55f70-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="55f70-147">Das heißt, Sie bearbeiten die Zeilen in der Form:</span><span class="sxs-lookup"><span data-stu-id="55f70-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="55f70-148">Weitere Informationen zum Angeben von Ziel Frameworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="55f70-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="55f70-149">Ersetzen Sie den Verweis auf das SDK in der Projektdefinition.</span><span class="sxs-lookup"><span data-stu-id="55f70-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="55f70-150">Stellen Sie sicher, dass die Versionsnummer dem in **Schritt 3**ermittelten Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="55f70-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="55f70-151">Entfernen Sie den Verweis auf das Paket `Microsoft.Quantum.Development.Kit` , falls vorhanden. dieser wird im folgenden Eintrag angegeben:</span><span class="sxs-lookup"><span data-stu-id="55f70-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="55f70-152">Aktualisieren Sie die Version der Microsoft Quantum-Pakete auf die zuletzt veröffentlichte Version des QDK (in **Schritt 3**ermittelt).</span><span class="sxs-lookup"><span data-stu-id="55f70-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="55f70-153">Diese Pakete werden mit den folgenden Mustern benannt:</span><span class="sxs-lookup"><span data-stu-id="55f70-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="55f70-154">Verweise auf Pakete haben das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="55f70-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="55f70-155">Speichern Sie die aktualisierte Datei.</span><span class="sxs-lookup"><span data-stu-id="55f70-155">Save the updated file.</span></span>

    - <span data-ttu-id="55f70-156">Stellen Sie die Abhängigkeiten des Projekts wieder her, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="55f70-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="55f70-157">Navigieren Sie zurück zum Ordner, der das Hauptprojekt enthält, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="55f70-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="55f70-158">Nachdem Sie Ihre Q #-Projekte aktualisiert haben, befolgen Sie die nachfolgenden Anweisungen, um das QDK selbst zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="55f70-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="55f70-159">Aktualisieren des QDK</span><span class="sxs-lookup"><span data-stu-id="55f70-159">Updating the QDK</span></span>

<span data-ttu-id="55f70-160">Der Aktualisierungsprozess für das QDK hängt von der Entwicklungssprache und-Umgebung ab.</span><span class="sxs-lookup"><span data-stu-id="55f70-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="55f70-161">Wählen Sie unten Ihre Entwicklungsumgebung aus.</span><span class="sxs-lookup"><span data-stu-id="55f70-161">Select your development environment below.</span></span>

* [<span data-ttu-id="55f70-162">Python: Aktualisieren der IQ #-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="55f70-163">Jupyter-Notebooks: Aktualisieren der IQ #-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="55f70-164">Visual Studio: Aktualisieren der QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="55f70-165">VS Code: Aktualisieren der QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="55f70-166">Befehlszeile und c#: Aktualisieren von Projektvorlagen</span><span class="sxs-lookup"><span data-stu-id="55f70-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="55f70-167">Aktualisieren von IQ # für python</span><span class="sxs-lookup"><span data-stu-id="55f70-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="55f70-168">Aktualisieren des `iqsharp` Kernels</span><span class="sxs-lookup"><span data-stu-id="55f70-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="55f70-169">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="55f70-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="55f70-170">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55f70-170">You should see the following output:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="55f70-171">Machen Sie sich keine Sorgen, wenn Ihre `iqsharp` Version höher ist, sollte Sie der [neuesten](xref:microsoft.quantum.relnotes)Version entsprechen.</span><span class="sxs-lookup"><span data-stu-id="55f70-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="55f70-172">Aktualisieren des `qsharp` Pakets</span><span class="sxs-lookup"><span data-stu-id="55f70-172">Update the `qsharp` package</span></span>

    ```
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="55f70-173">Überprüfen der `qsharp` Version</span><span class="sxs-lookup"><span data-stu-id="55f70-173">Verify the `qsharp` version</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="55f70-174">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="55f70-174">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="55f70-175">Führen Sie den folgenden Befehl am Speicherort der `.qs` Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="55f70-175">Run the following command from the location of your `.qs` files</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="55f70-176">Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.</span><span class="sxs-lookup"><span data-stu-id="55f70-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="55f70-177">Aktualisieren von IQ # für jupyter-Notebooks</span><span class="sxs-lookup"><span data-stu-id="55f70-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="55f70-178">Aktualisieren des `iqsharp` Kernels</span><span class="sxs-lookup"><span data-stu-id="55f70-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="55f70-179">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="55f70-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="55f70-180">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="55f70-180">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="55f70-181">Machen Sie sich keine Sorgen, wenn Ihre `iqsharp` Version höher ist, sollte Sie der [neuesten](xref:microsoft.quantum.relnotes)Version entsprechen.</span><span class="sxs-lookup"><span data-stu-id="55f70-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="55f70-182">Führen Sie den folgenden Befehl aus einer Zelle im Jupyter Notebook aus:</span><span class="sxs-lookup"><span data-stu-id="55f70-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="55f70-183">Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="55f70-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="55f70-184">Visual Studio-QDK-Erweiterung aktualisieren</span><span class="sxs-lookup"><span data-stu-id="55f70-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="55f70-185">Aktualisieren der f # Visual Studio-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="55f70-186">Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="55f70-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="55f70-187">Akzeptieren des Updates</span><span class="sxs-lookup"><span data-stu-id="55f70-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="55f70-188">Die Projektvorlagen werden mit der Erweiterung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="55f70-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="55f70-189">Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte.</span><span class="sxs-lookup"><span data-stu-id="55f70-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="55f70-190">Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="55f70-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="55f70-191">Update vs Code QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="55f70-192">Aktualisieren der Quantum-vs Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="55f70-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="55f70-193">Neustart vs Code</span><span class="sxs-lookup"><span data-stu-id="55f70-193">Restart VS Code</span></span>
    - <span data-ttu-id="55f70-194">Navigieren Sie zur Registerkarte **Erweiterungen** .</span><span class="sxs-lookup"><span data-stu-id="55f70-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="55f70-195">Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .</span><span class="sxs-lookup"><span data-stu-id="55f70-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="55f70-196">Erweiterung erneut laden</span><span class="sxs-lookup"><span data-stu-id="55f70-196">Reload the extension</span></span>

2. <span data-ttu-id="55f70-197">Aktualisieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="55f70-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="55f70-198">Gehe zu **Anzeige**-  ->  **Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="55f70-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="55f70-199">Auswählen von " **Q #: Install Project Templates** "</span><span class="sxs-lookup"><span data-stu-id="55f70-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="55f70-200">Nach wenigen Sekunden sollte ein Popup mit der Bestätigung angezeigt werden, dass die Projektvorlagen erfolgreich installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="55f70-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="55f70-201">C# mit dem `dotnet` Befehlszeilen Tool</span><span class="sxs-lookup"><span data-stu-id="55f70-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="55f70-202">Aktualisieren der Quantum-Projektvorlagen für .net</span><span class="sxs-lookup"><span data-stu-id="55f70-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
