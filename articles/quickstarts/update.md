---
title: Aktualisieren des Quantum Development Kit (QDK)
description: Es wird beschrieben, wie Sie Ihre Q#-Projekte und das Microsoft Quantum Development Kit auf die aktuelle Version aktualisieren.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 8d39716c4d4c96ad87862b4b185895aab66cd210
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274076"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="497aa-103">Aktualisieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="497aa-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="497aa-104">Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) auf die aktuelle Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="497aa-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="497aa-105">In diesem Artikel wird vorausgesetzt, dass Sie das QDK bereits installiert haben.</span><span class="sxs-lookup"><span data-stu-id="497aa-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="497aa-106">Bei der erstmaligen Installation hilft Ihnen das [Installationshandbuch](xref:microsoft.quantum.install) weiter.</span><span class="sxs-lookup"><span data-stu-id="497aa-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="497aa-107">Wir empfehlen Ihnen, immer das neueste QDK-Release zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="497aa-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="497aa-108">Befolgen Sie diesen Aktualisierungsleitfaden, um das Upgrade auf die aktuelle QDK-Version durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="497aa-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="497aa-109">Der Prozess besteht aus zwei Teilen:</span><span class="sxs-lookup"><span data-stu-id="497aa-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="497aa-110">Aktualisieren Ihrer vorhandenen Q#-Dateien und -Projekte zur Ausrichtung Ihres Codes auf aktualisierte Syntax</span><span class="sxs-lookup"><span data-stu-id="497aa-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="497aa-111">Aktualisieren des eigentlichen QDK für die von Ihnen gewählte Entwicklungsumgebung</span><span class="sxs-lookup"><span data-stu-id="497aa-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="497aa-112">Aktualisieren von Q#-Projekten</span><span class="sxs-lookup"><span data-stu-id="497aa-112">Updating Q# Projects</span></span> 

<span data-ttu-id="497aa-113">Unabhängig davon, ob Sie C# oder Python zum Hosten von Q#-Vorgängen nutzen, können Sie die unten angegebene Anleitung zum Aktualisieren Ihrer Q#-Projekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="497aa-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="497aa-114">Überprüfen Sie zunächst, ob Sie die neueste Version des [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) nutzen.</span><span class="sxs-lookup"><span data-stu-id="497aa-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="497aa-115">Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="497aa-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="497aa-116">Überprüfen Sie, ob `3.1.100` oder höher ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="497aa-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="497aa-117">Falls nicht, sollten Sie die [aktuelle Version](https://dotnet.microsoft.com/download) installieren und die Überprüfung dann erneut durchführen.</span><span class="sxs-lookup"><span data-stu-id="497aa-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="497aa-118">Befolgen Sie anschließend unten die Anleitung je nach Ihrem Setup (Visual Studio, Visual Studio Code oder direkt über die Befehlszeile).</span><span class="sxs-lookup"><span data-stu-id="497aa-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="497aa-119">Aktualisieren von Q#-Projekten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="497aa-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="497aa-120">Führen Sie ein Update auf die aktuelle Version von Visual Studio 2019 durch. Eine entsprechende Anleitung finden Sie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="497aa-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="497aa-121">Öffnen Sie Ihre Projektmappe in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="497aa-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="497aa-122">Wählen Sie im Menü die Option **Erstellen** -> **Projektmappe bereinigen** aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="497aa-123">Aktualisieren Sie in Ihren CSPROJ-Dateien jeweils das Zielframework auf `netcoreapp3.1` (bzw. `netstandard2.1`, falls es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="497aa-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="497aa-124">Bearbeiten Sie hierfür Zeilen der folgenden Art:</span><span class="sxs-lookup"><span data-stu-id="497aa-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="497aa-125">Ausführlichere Informationen zum Angeben von Zielframeworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="497aa-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="497aa-126">Legen Sie in allen CSPROJ-Dateien das SDK auf `Microsoft.Quantum.Sdk` fest (wie in der Zeile unten angegeben).</span><span class="sxs-lookup"><span data-stu-id="497aa-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="497aa-127">Beachten Sie, dass die Versionsnummer der neuesten verfügbaren Version entsprechen sollte. Sie können dies ermitteln, indem Sie in den [Versionshinweisen](https://docs.microsoft.com/quantum/relnotes/) nachsehen.</span><span class="sxs-lookup"><span data-stu-id="497aa-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="497aa-128">Speichern und schließen Sie alle Dateien in Ihrer Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="497aa-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="497aa-129">Wählen Sie **Extras** -> **Befehlszeile** -> **Developer-Eingabeaufforderung** aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="497aa-130">Alternativ können Sie auch die Paketverwaltungskonsole in Visual Studio verwenden.</span><span class="sxs-lookup"><span data-stu-id="497aa-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="497aa-131">Führen Sie für jedes Projekt der Projektmappe den folgenden Befehl aus, um dieses Paket zu **entfernen**:</span><span class="sxs-lookup"><span data-stu-id="497aa-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="497aa-132">Gehen Sie wie folgt vor, falls für Ihre Projekte noch andere Microsoft.Quantum- oder Microsoft.Azure.Quantum-Pakete (z. B. Microsoft.Quantum.Numerics) genutzt werden: Führen Sie den Befehl **add** für diese Pakete aus, um die genutzte Version zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="497aa-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="497aa-133">Schließen Sie die Eingabeaufforderung, und wählen Sie **Erstellen** -> **Projektmappe erstellen** aus (*nicht* die Option „Projektmappe neu erstellen“).</span><span class="sxs-lookup"><span data-stu-id="497aa-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="497aa-134">Sie können nun zu [Aktualisieren Ihrer Visual Studio-QDK-Erweiterung](#update-visual-studio-qdk-extension) springen.</span><span class="sxs-lookup"><span data-stu-id="497aa-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="497aa-135">Aktualisieren von Q#-Projekten in Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="497aa-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="497aa-136">Öffnen Sie in Visual Studio Code den Ordner, der das zu aktualisierende Projekt enthält.</span><span class="sxs-lookup"><span data-stu-id="497aa-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="497aa-137">Wählen Sie **Terminal** -> **Neues Terminal** aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="497aa-138">Befolgen Sie die Anleitung für die Aktualisierung über die Befehlszeile (unten angegeben).</span><span class="sxs-lookup"><span data-stu-id="497aa-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="497aa-139">Aktualisieren von Q#-Projekten über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="497aa-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="497aa-140">Navigieren Sie zu dem Ordner, der Ihre Hauptprojektdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="497aa-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="497aa-141">Führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="497aa-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="497aa-142">Bestimmen Sie die aktuelle Version des QDK.</span><span class="sxs-lookup"><span data-stu-id="497aa-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="497aa-143">Informationen hierzu finden Sie in den [Versionshinweisen](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="497aa-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="497aa-144">Die Versionsangabe hat in etwa das folgende Format: `0.11.2006.207`.</span><span class="sxs-lookup"><span data-stu-id="497aa-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="497aa-145">Führen Sie in Ihren `.csproj`-Dateien jeweils die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="497aa-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="497aa-146">Aktualisieren Sie das Zielframework auf `netcoreapp3.1` (bzw. `netstandard2.1`, falls es sich um ein Bibliotheksprojekt handelt).</span><span class="sxs-lookup"><span data-stu-id="497aa-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="497aa-147">Bearbeiten Sie hierfür Zeilen der folgenden Art:</span><span class="sxs-lookup"><span data-stu-id="497aa-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="497aa-148">Ausführlichere Informationen zum Angeben von Zielframeworks finden Sie [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span><span class="sxs-lookup"><span data-stu-id="497aa-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="497aa-149">Ersetzen Sie in der Projektdefinition den Verweis auf das SDK.</span><span class="sxs-lookup"><span data-stu-id="497aa-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="497aa-150">Stellen Sie sicher, dass die Versionsnummer dem Wert entspricht, den Sie in **Schritt 3** ermittelt haben.</span><span class="sxs-lookup"><span data-stu-id="497aa-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="497aa-151">Entfernen Sie den Verweis auf das Paket `Microsoft.Quantum.Development.Kit` (falls vorhanden), der im folgenden Eintrag angegeben ist:</span><span class="sxs-lookup"><span data-stu-id="497aa-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="497aa-152">Aktualisieren Sie die Version aller Microsoft Quantum-Pakete auf die letzte veröffentlichte Version des QDK (in **Schritt 3** ermittelt).</span><span class="sxs-lookup"><span data-stu-id="497aa-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="497aa-153">Für die Benennung dieser Pakete wird das folgende Muster genutzt:</span><span class="sxs-lookup"><span data-stu-id="497aa-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="497aa-154">Verweise auf Pakete haben das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="497aa-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="497aa-155">Speichern Sie die aktualisierte Datei.</span><span class="sxs-lookup"><span data-stu-id="497aa-155">Save the updated file.</span></span>

    - <span data-ttu-id="497aa-156">Stellen Sie die Abhängigkeiten des Projekts wieder her, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="497aa-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="497aa-157">Navigieren Sie zurück zum Ordner, der Ihr Hauptprojekt enthält, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="497aa-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="497aa-158">Nachdem Ihre Q#-Projekte nun aktualisiert wurden, sollten Sie die Anleitung unten befolgen, um das eigentliche QDK zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="497aa-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="497aa-159">Aktualisieren des QDK</span><span class="sxs-lookup"><span data-stu-id="497aa-159">Updating the QDK</span></span>

<span data-ttu-id="497aa-160">Der Prozess zur Aktualisierung des QDK variiert je nach Entwicklungssprache und -umgebung.</span><span class="sxs-lookup"><span data-stu-id="497aa-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="497aa-161">Wählen Sie unten Ihre Entwicklungsumgebung aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-161">Select your development environment below.</span></span>

* [<span data-ttu-id="497aa-162">Python: Aktualisieren der IQ#-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="497aa-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="497aa-163">Jupyter Notebooks: Aktualisieren der IQ#-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="497aa-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="497aa-164">Visual Studio: Aktualisieren der QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="497aa-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="497aa-165">VS Code: Aktualisieren der QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="497aa-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="497aa-166">Befehlszeile und C# : Aktualisieren der Projektvorlagen</span><span class="sxs-lookup"><span data-stu-id="497aa-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="497aa-167">Aktualisieren von IQ# für Python</span><span class="sxs-lookup"><span data-stu-id="497aa-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="497aa-168">Aktualisieren Sie den `iqsharp`-Kernel.</span><span class="sxs-lookup"><span data-stu-id="497aa-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="497aa-169">Überprüfen Sie die `iqsharp`-Version.</span><span class="sxs-lookup"><span data-stu-id="497aa-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="497aa-170">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497aa-170">You should see the following output:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="497aa-171">Es ist kein Problem, wenn Ihre `iqsharp`-Version höher ist. Dies sollte dem [aktuellen Release](xref:microsoft.quantum.relnotes) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="497aa-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="497aa-172">Aktualisieren Sie das `qsharp`-Paket.</span><span class="sxs-lookup"><span data-stu-id="497aa-172">Update the `qsharp` package</span></span>

    ```
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="497aa-173">Überprüfen Sie die `qsharp`-Version.</span><span class="sxs-lookup"><span data-stu-id="497aa-173">Verify the `qsharp` version</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="497aa-174">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497aa-174">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="497aa-175">Führen Sie am Speicherort Ihrer `.qs`-Dateien den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-175">Run the following command from the location of your `.qs` files</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="497aa-176">Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantenprogramme auszuführen.</span><span class="sxs-lookup"><span data-stu-id="497aa-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="497aa-177">Aktualisieren von IQ# für Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="497aa-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="497aa-178">Aktualisieren Sie den `iqsharp`-Kernel.</span><span class="sxs-lookup"><span data-stu-id="497aa-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="497aa-179">Überprüfen Sie die `iqsharp`-Version.</span><span class="sxs-lookup"><span data-stu-id="497aa-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="497aa-180">Die Ausgabe sollte in etwa wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="497aa-180">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="497aa-181">Es ist kein Problem, wenn Ihre `iqsharp`-Version höher ist. Dies sollte dem [aktuellen Release](xref:microsoft.quantum.relnotes) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="497aa-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="497aa-182">Führen Sie den folgenden Befehl in einer Zelle im Jupyter Notebook aus:</span><span class="sxs-lookup"><span data-stu-id="497aa-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="497aa-183">Sie können jetzt ein vorhandenes Jupyter Notebook öffnen und mit dem aktualisierten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="497aa-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="497aa-184">Aktualisieren der Visual Studio-QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="497aa-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="497aa-185">Aktualisieren Sie die Q#-Visual Studio-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="497aa-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="497aa-186">In Visual Studio wird eine Aufforderung zum Akzeptieren der Updates für die [Visual Studio-Quantum-Erweiterung](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497aa-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="497aa-187">Akzeptieren Sie das Update.</span><span class="sxs-lookup"><span data-stu-id="497aa-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="497aa-188">Die Projektvorlagen werden mit der Erweiterung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="497aa-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="497aa-189">Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte.</span><span class="sxs-lookup"><span data-stu-id="497aa-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="497aa-190">Der Code für Ihre vorhandenen Projekte wird bei der Aktualisierung der Erweiterung nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="497aa-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="497aa-191">Aktualisieren der VS Code-QDK-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="497aa-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="497aa-192">Aktualisieren Sie die Quantum-Erweiterung für VS Code.</span><span class="sxs-lookup"><span data-stu-id="497aa-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="497aa-193">Starten Sie VS Code neu.</span><span class="sxs-lookup"><span data-stu-id="497aa-193">Restart VS Code</span></span>
    - <span data-ttu-id="497aa-194">Navigieren Sie zur Registerkarte **Erweiterungen**.</span><span class="sxs-lookup"><span data-stu-id="497aa-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="497aa-195">Wählen Sie die Erweiterung **Microsoft Quantum Development Kit for Visual Studio Code** aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="497aa-196">Laden Sie die Erweiterung neu.</span><span class="sxs-lookup"><span data-stu-id="497aa-196">Reload the extension</span></span>

2. <span data-ttu-id="497aa-197">Aktualisieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="497aa-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="497aa-198">Navigieren Sie zu **Ansicht** -> **Befehlspalette**.</span><span class="sxs-lookup"><span data-stu-id="497aa-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="497aa-199">Wählen Sie **Q#: Install project templates** (Q#: Projektvorlagen installieren) aus.</span><span class="sxs-lookup"><span data-stu-id="497aa-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="497aa-200">Nach wenigen Sekunden sollte ein Popupfenster mit der Bestätigung angezeigt werden, dass die „Projektvorlagen erfolgreich installiert wurden“.</span><span class="sxs-lookup"><span data-stu-id="497aa-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="497aa-201">C#: `dotnet`-Befehlszeilentool</span><span class="sxs-lookup"><span data-stu-id="497aa-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="497aa-202">Aktualisieren Sie die Quantum-Projektvorlagen für .NET.</span><span class="sxs-lookup"><span data-stu-id="497aa-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
