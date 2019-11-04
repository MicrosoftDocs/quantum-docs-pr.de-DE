---
title: Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) aktualisieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185850"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="de532-102">Aktualisieren des Microsoft Quantum Development Kit (QDK)</span><span class="sxs-lookup"><span data-stu-id="de532-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="de532-103">Erfahren Sie, wie Sie die Microsoft Quantum Development Kit (QDK) auf die neueste Version aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="de532-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="de532-104">In diesem Artikel wird davon ausgegangen, dass Sie das QDK bereits installiert haben.</span><span class="sxs-lookup"><span data-stu-id="de532-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="de532-105">Wenn Sie zum ersten Mal installieren, finden Sie weitere Informationen im [Installationshandbuch](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="de532-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="de532-106">Die Aktualisierungs Schritte hängen von Ihrer Entwicklungsumgebung ab.</span><span class="sxs-lookup"><span data-stu-id="de532-106">The update steps depend on your development environment.</span></span> <span data-ttu-id="de532-107">Wählen Sie Ihre Umgebung aus den folgenden Abschnitten aus.</span><span class="sxs-lookup"><span data-stu-id="de532-107">Choose your environment from the following sections.</span></span>

## <a name="python"></a><span data-ttu-id="de532-108">Python</span><span class="sxs-lookup"><span data-stu-id="de532-108">Python</span></span>

1. <span data-ttu-id="de532-109">Aktualisieren des `iqsharp` Kernel</span><span class="sxs-lookup"><span data-stu-id="de532-109">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="de532-110">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="de532-110">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="de532-111">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de532-111">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="de532-112">Aktualisieren des `qsharp` Pakets</span><span class="sxs-lookup"><span data-stu-id="de532-112">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="de532-113">Überprüfen der `qsharp` Version</span><span class="sxs-lookup"><span data-stu-id="de532-113">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="de532-114">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de532-114">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="de532-115">Sie können jetzt die aktualisierte QDK-Version verwenden, um Ihre vorhandenen Quantum-Programme auszuführen.</span><span class="sxs-lookup"><span data-stu-id="de532-115">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="jupyter-notebooks"></a><span data-ttu-id="de532-116">Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="de532-116">Jupyter notebooks</span></span>

1. <span data-ttu-id="de532-117">Aktualisieren des `iqsharp` Kernel</span><span class="sxs-lookup"><span data-stu-id="de532-117">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="de532-118">Überprüfen der `iqsharp` Version</span><span class="sxs-lookup"><span data-stu-id="de532-118">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="de532-119">Die folgende Ausgabe wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="de532-119">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="de532-120">Sie können jetzt ein vorhandenes jupyter Notebook öffnen und es mit dem aktualisierten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="de532-120">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="c-on-windows-using-visual-studio"></a><span data-ttu-id="de532-121">C#unter Windows mit Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de532-121">C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="de532-122">Aktualisieren der f # Visual Studio-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="de532-122">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="de532-123">Visual Studio fordert Sie auf, Aktualisierungen der [Erweiterung von Visual Studio](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit) zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="de532-123">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="de532-124">Akzeptieren des Updates</span><span class="sxs-lookup"><span data-stu-id="de532-124">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="de532-125">Die Projektvorlagen werden mit der Erweiterung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="de532-125">The project templates are updated with the extension.</span></span> <span data-ttu-id="de532-126">Die aktualisierten Vorlagen gelten nur für neu erstellte Projekte.</span><span class="sxs-lookup"><span data-stu-id="de532-126">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="de532-127">Der Code für die vorhandenen Projekte wird nicht aktualisiert, wenn die Erweiterung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="de532-127">The code for your existing projects is not updated when the extension is updated.</span></span>

1. <span data-ttu-id="de532-128">Aktualisieren der QDK-Pakete</span><span class="sxs-lookup"><span data-stu-id="de532-128">Update the QDK packages</span></span>

    - <span data-ttu-id="de532-129">Öffnen einer vorhandenen Anwendung</span><span class="sxs-lookup"><span data-stu-id="de532-129">Open an existing application</span></span>
    - <span data-ttu-id="de532-130">Wählen Sie **Abhängigkeiten** in der Projektmappen-Explorer</span><span class="sxs-lookup"><span data-stu-id="de532-130">Select **Dependencies** in the Solution Explorer</span></span>
    - <span data-ttu-id="de532-131">Wählen Sie **nuget-Pakete verwalten** .</span><span class="sxs-lookup"><span data-stu-id="de532-131">Select **Manage NuGet Packages**</span></span>
    - <span data-ttu-id="de532-132">Aktualisieren Sie die **Microsoft. Quantum** -Pakete auf die neueste Version.</span><span class="sxs-lookup"><span data-stu-id="de532-132">Update the **Microsoft.Quantum** packages to the latest version</span></span>

1. <span data-ttu-id="de532-133">Sie können nun Ihre Anwendung mit dem neuesten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="de532-133">You can now run your application with the latest QDK.</span></span>

## <a name="c-using-vs-code"></a><span data-ttu-id="de532-134">C#mit vs Code</span><span class="sxs-lookup"><span data-stu-id="de532-134">C#, using VS Code</span></span>

1. <span data-ttu-id="de532-135">Aktualisieren der Quantum-vs Code Erweiterung</span><span class="sxs-lookup"><span data-stu-id="de532-135">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="de532-136">Neustart vs Code</span><span class="sxs-lookup"><span data-stu-id="de532-136">Restart VS Code</span></span>
    - <span data-ttu-id="de532-137">Navigieren Sie zur Registerkarte **Erweiterungen** .</span><span class="sxs-lookup"><span data-stu-id="de532-137">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="de532-138">Wählen Sie die **Microsoft Quantum Development Kit für Visual Studio Code Erweiterung aus** .</span><span class="sxs-lookup"><span data-stu-id="de532-138">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="de532-139">Erweiterung erneut laden</span><span class="sxs-lookup"><span data-stu-id="de532-139">Reload the extension</span></span>

1. <span data-ttu-id="de532-140">Aktualisieren Sie die Quantum-Projektvorlagen:</span><span class="sxs-lookup"><span data-stu-id="de532-140">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="de532-141">Gehe zu **Ansicht** -> **Befehls Palette**</span><span class="sxs-lookup"><span data-stu-id="de532-141">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="de532-142">Auswählen von " **Q #: Install Project Templates** "</span><span class="sxs-lookup"><span data-stu-id="de532-142">Select **Q#: Install project templates**</span></span>

1. <span data-ttu-id="de532-143">Öffnen Sie eine vorhandene Anwendung in vs Code</span><span class="sxs-lookup"><span data-stu-id="de532-143">Open an existing application in VS Code</span></span>

   - <span data-ttu-id="de532-144">Bearbeiten Sie die CSPROJ-Datei, um die neuen Paketversionen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="de532-144">Edit the .csproj file to add the new package versions</span></span>

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    <span data-ttu-id="de532-145">Wenn Sie andere `Microsoft.Quantum` Pakete verwenden, aktualisieren Sie diese ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="de532-145">If you use other `Microsoft.Quantum` packages, update these too.</span></span>

1. <span data-ttu-id="de532-146">Sie können Ihre Anwendung jetzt mit dem aktualisierten QDK ausführen.</span><span class="sxs-lookup"><span data-stu-id="de532-146">You can now run your application with the updated QDK</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="de532-147">C#mit dem Befehlszeilen Tool "`dotnet`"</span><span class="sxs-lookup"><span data-stu-id="de532-147">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="de532-148">Aktualisieren der Quantum-Projektvorlagen für .net</span><span class="sxs-lookup"><span data-stu-id="de532-148">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="de532-149">Aktualisieren und Ausführen einer vorhandenen Anwendung</span><span class="sxs-lookup"><span data-stu-id="de532-149">Update and run an existing application</span></span>

    - <span data-ttu-id="de532-150">Aktualisieren der QDK-Paketversionen in der Anwendung</span><span class="sxs-lookup"><span data-stu-id="de532-150">Update the QDK package versions in your application</span></span>

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        <span data-ttu-id="de532-151">Wenn Ihre Anwendung andere `Microsoft.Quantum` Pakete verwendet, aktualisieren Sie diese ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="de532-151">If your application uses any other `Microsoft.Quantum` packages, update these too.</span></span>

    - <span data-ttu-id="de532-152">Ausführen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="de532-152">Run the application</span></span>

        ```bash
        dotnet run
        ```

    - <span data-ttu-id="de532-153">Ihre Anwendung wird mit den neuen Paketversionen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de532-153">Your application will run with the new package versions</span></span>

## <a name="whats-next"></a><span data-ttu-id="de532-154">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="de532-154">What's next?</span></span>

<span data-ttu-id="de532-155">Nachdem Sie das Quantum Development Kit in Ihrer bevorzugten Umgebung aktualisiert haben, können Sie weiterhin ihre Quantum-Programme entwickeln und ausführen.</span><span class="sxs-lookup"><span data-stu-id="de532-155">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="de532-156">Wenn Sie noch kein Programm geschrieben haben, können Sie mit [Ihrem ersten Quantum-Programm](xref:microsoft.quantum.write-program)beginnen.</span><span class="sxs-lookup"><span data-stu-id="de532-156">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
