---
title: 'Installation und Validierung der Microsoft Q #-Chemie Bibliothek'
description: Erfahren Sie, wie Sie die Microsoft Quantum Chemistry-Bibliothek installieren und mit der nwchem-Berechnungs-Chemie-Plattform verwenden.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: 48bf7bc980e238e622053f5c2bdd09604c572596
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907357"
---
# <a name="chemistry-library-installation-and-validation"></a><span data-ttu-id="3f6ee-103">Installation und Validierung der Chemie Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3f6ee-103">Chemistry Library Installation and Validation</span></span>

<span data-ttu-id="3f6ee-104">Das Quantum Development Kit bietet Unterstützung für Quantum-Chemie-Anwendungen über das [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) nuget-Paket.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-104">The Quantum Development Kit provides support for quantum chemistry applications through the [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) NuGet package.</span></span>
<span data-ttu-id="3f6ee-105">Wie bei anderen nuget-Paketen ist es einfach, die Chemie Bibliothek zu Ihrem Projekt hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-105">As with other NuGet packages, it's straightforward to add the chemistry library to your project.</span></span>

<span data-ttu-id="3f6ee-106">**Visual Studio 2019:** Wenn Sie Visual Studio 2019 verwenden, können Sie die Quantum-Chemie Pakete mit dem nuget-Paket-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-106">**Visual Studio 2019:** If you are using Visual Studio 2019, you can add the quantum chemistry packages by using the NuGet Package Manager.</span></span>
<span data-ttu-id="3f6ee-107">Um den Paket-Manager zu öffnen, klicken Sie mit der rechten Maustaste auf das Projekt, dem Sie die Chemie Bibliothek hinzufügen möchten, und wählen Sie "nuget-Pakete verwalten..." aus, wie im folgenden Screenshot gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-107">To open the Package Manager, right-click on the project you'd like to add the chemistry library to and select "Manage NuGet Packages...," as in the screenshot below.</span></span>

![Verwenden des nuget-Paket-Managers in Visual Studio 2019](~/media/vs2017-nuget-manage-packages.png)

<span data-ttu-id="3f6ee-109">Suchen Sie auf der Registerkarte Durchsuchen nach dem Paketnamen "Microsoft. Quantum. Chemistry".</span><span class="sxs-lookup"><span data-stu-id="3f6ee-109">From the Browse tab, search for the package name "Microsoft.Quantum.Chemistry."</span></span>

> [!NOTE]
> <span data-ttu-id="3f6ee-110">Stellen Sie sicher, dass "incluelease einschließen" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-110">Make sure to tick "Include prerelease."</span></span>

![Kontrollkästchen "Vorabversion einschließen"](~/media/vs2017-nuget-package-search.png)

<span data-ttu-id="3f6ee-112">Dadurch werden die Pakete aufgelistet, die zum Herunterladen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-112">This will list the packages available for download.</span></span>
<span data-ttu-id="3f6ee-113">Klicken Sie im linken Bereich auf "Microsoft. Quantum. Chemistry", wählen Sie im rechten Bereich die neueste Vorabversion aus, und klicken Sie auf "Install" (installieren):</span><span class="sxs-lookup"><span data-stu-id="3f6ee-113">Click on the "Microsoft.Quantum.Chemistry on the left-hand pane, select the latest pre-release version on the right-hand pane, and click "Install":</span></span>

![Installieren Sie das neueste Microsoft. Quantum. Chemistry-Paket.](~/media/vs2017-nuget-select-chem.png)

<span data-ttu-id="3f6ee-115">Weitere Informationen finden Sie im Leitfaden für die [Benutzeroberfläche des Paket-Managers](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span><span class="sxs-lookup"><span data-stu-id="3f6ee-115">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="3f6ee-116">Alternativ können Sie die-Paket-Manager-Konsole verwenden, um dem Projekt die Quantum-Bibliothek mit einer Befehlszeilenschnittstelle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-116">Alternatively, you can use the Package Manager Console to add the quantum chemistry library to your project with a command line interface.</span></span>

![Verwenden der Paket-Manager-Konsole über die Befehlszeile](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="3f6ee-118">Führen Sie in der Paket-Manager-Konsole Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-118">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Chemistry
```

<span data-ttu-id="3f6ee-119">Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).</span><span class="sxs-lookup"><span data-stu-id="3f6ee-119">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="3f6ee-120">**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie den `dotnet`-Befehl verwenden, um dem Projekt einen nuget-Paket Verweis hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-120">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a><span data-ttu-id="3f6ee-121">Überprüfen der Installation</span><span class="sxs-lookup"><span data-stu-id="3f6ee-121">Verifying Your Installation</span></span> 

<span data-ttu-id="3f6ee-122">Wie der Rest des quantumentwicklungskit enthält die Quantum-Bibliothek eine Reihe von vollständig dokumentierten Beispielen, mit deren Hilfe Sie schnell loslegen können.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-122">Like the rest of the Quantum Development Kit, the quantum chemistry library comes with a number of fully documented samples to help you get up and running quickly.</span></span>
<span data-ttu-id="3f6ee-123">Zum Testen Ihrer Installation mithilfe dieser Beispiele Klonen Sie das [hauptbeispielrepository](https://github.com/Microsoft/Quantum), und führen Sie dann eines der Beispiele aus.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-123">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum), then run one of the samples.</span></span>  <span data-ttu-id="3f6ee-124">So führen Sie z. b. das [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-124">For example, to run the [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

<span data-ttu-id="3f6ee-125">So überprüfen Sie die Installation der Quantum-Chemie Bibliothek mithilfe von Microsoft Visual Studio nach dem Klonen des Repository:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-125">To verify the installation of the quantum chemistry library using Microsoft Visual Studio after cloning the repository:</span></span>
    1. <span data-ttu-id="3f6ee-126">Öffnen Sie die Projekt Mappe "chemistrysamples. sln" im Ordner "Chemistry".</span><span class="sxs-lookup"><span data-stu-id="3f6ee-126">Open the ChemistrySamples.sln solution in the Chemistry folder.</span></span>  
    2. <span data-ttu-id="3f6ee-127">Wählen Sie Samples/1 aus.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-127">Select Samples/1.</span></span> <span data-ttu-id="3f6ee-128">Einfache Moleküle/molecularhydrogen als Startprojekt.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-128">Simple Molecules/MolecularHydrogen as the StartUp project.</span></span>
    3. <span data-ttu-id="3f6ee-129">Drücken Sie F5, um die Demo der Molekular Wasserstoff-Quantum-Phasen Schätzung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-129">Press F5 to run the molecular Hydrogen quantum phase estimation demo.</span></span>

<span data-ttu-id="3f6ee-130">Weitere Informationen zum Schätzen der Werte von Energie Stufen finden Sie unter Abrufen von [Energie Stufen Schätzungen](xref:microsoft.quantum.chemistry.examples.energyestimate) .</span><span class="sxs-lookup"><span data-stu-id="3f6ee-130">See [Obtaining energy level estimates](xref:microsoft.quantum.chemistry.examples.energyestimate) for more information on estimating the values of energy levels.</span></span>   


## <a name="using-the-quantum-development-kit-with-nwchem"></a><span data-ttu-id="3f6ee-131">Verwenden des quantumentwicklungskit mit nwchem</span><span class="sxs-lookup"><span data-stu-id="3f6ee-131">Using the Quantum Development Kit with NWChem</span></span> ##

<span data-ttu-id="3f6ee-132">Das Beispiel "molecularhydrogen" verwendet Molekulare Eingabedaten, die manuell konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-132">The MolecularHydrogen sample uses molecular input data that is manually configured.</span></span>  <span data-ttu-id="3f6ee-133">Obwohl dies für kleine Beispiele in Ordnung ist, erfordert die Skalierung von Quantum-Chemie eine hamiltonation mit Millionen oder Milliarden von Begriffen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-133">While this is fine for small examples, quantum chemistry at scale require Hamiltonians with millions or billions of terms.</span></span> <span data-ttu-id="3f6ee-134">Solche von skalierbaren Berechnungs-Chemie-Paketen generierten hamiltoner sind zu groß, um per Hand zu importieren.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-134">Such Hamiltonians, generated by scalable computational chemistry packages are too large to import by hand.</span></span> 

<span data-ttu-id="3f6ee-135">Die Quantum-Bibliothek für das Quantum Development Kit ist so konzipiert, dass Sie gut mit COMPUTE-Chemie Paketen funktioniert. Dies ist insbesondere die von der Umgebung für das Umwelt Molekulare Labor (EMSL) im Pacific Nordwest National-Labor entwickelte [**nwchem**](http://www.nwchem-sw.org/) -Berechnungs Plattform.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-135">The quantum chemistry library for the Quantum Development Kit is designed to work well with computational chemistry packages, most notably the [**NWChem**](http://www.nwchem-sw.org/) computational chemistry platform developed by the Environmental Molecular Sciences Laboratory (EMSL) at Pacific Northwest National Laboratory.</span></span>
<span data-ttu-id="3f6ee-136">Insbesondere das `Microsoft.Quantum.Chemistry`-Paket bietet Tools zum Laden von Instanzen von Problemen mit der Quantum-Chemie Simulation, die im [broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)dargestellt werden. Dies wird auch für den Export von neueren Versionen von nwchem unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-136">In particular, the `Microsoft.Quantum.Chemistry` package provides tools for loading instances of quantum chemistry simulation problems represented in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), also supported for export by recent versions of NWChem.</span></span>

<span data-ttu-id="3f6ee-137">Wir empfehlen eine der folgenden Methoden, um die Verwendung von nwchem in Verbindung mit dem Quantum Development Kit zu erreichen:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-137">To get up and running using NWChem together with the Quantum Development Kit, we suggest one of the following methods:</span></span>
- <span data-ttu-id="3f6ee-138">Beginnen Sie mit der Verwendung vorhandener broombridge-Dateien, die mit den Beispielen unter [integraldata/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-138">Get started using existing Broombridge files provided with the samples at [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML).</span></span>
- <span data-ttu-id="3f6ee-139">Verwenden Sie den [EMSL-Pfeile-Generator für den Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) der ein webbasiertes Front-End für nwchem ist, um neue, mit broombridge formatierte Molekulare Eingabedateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-139">Use the [EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) which is a web-based frontend to NWChem, to generate new Broombridge-formated molecular input files.</span></span>  
- <span data-ttu-id="3f6ee-140">Verwenden Sie das von pnnl bereitgestellte [docker-Image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) , um nwchem auszuführen, oder</span><span class="sxs-lookup"><span data-stu-id="3f6ee-140">Use the [Docker image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) provided by PNNL to run NWChem, or</span></span>
- <span data-ttu-id="3f6ee-141">[Kompilieren Sie nwchem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) für Ihre Plattform.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-141">[Compile NWChem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) for your platform.</span></span>

<span data-ttu-id="3f6ee-142">Weitere Informationen zum Arbeiten mit nwchem für chemische Modelle finden Sie unter [End-to-End mit nwchem](xref:microsoft.quantum.chemistry.examples.endtoend) , um mit der Chemie Bibliothek von Quantum Developmen Kit zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-142">See [End-to-end with NWChem](xref:microsoft.quantum.chemistry.examples.endtoend) for more information on how to work with NWChem to chemical models to analyze with the Quantum Developmen Kit chemistry library.</span></span>

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a><span data-ttu-id="3f6ee-143">Die ersten Schritte mit den in den Beispielen bereitgestellten broombridge-Dateien</span><span class="sxs-lookup"><span data-stu-id="3f6ee-143">Getting started using Broombridge files provided with the samples</span></span>

<span data-ttu-id="3f6ee-144">Der Ordner [integraldata/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) im beispielrepository für das Quantum Development Kit enthält broombridge-formierte Molekül-Datendateien.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-144">The [IntegralData/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) folder in the Quantum Development Kit Samples repository contains Broombridge-formated molecule data files.</span></span>  

<span data-ttu-id="3f6ee-145">Verwenden Sie als einfaches Beispiel das Beispiel für die Chemie-Bibliothek, [getgatecount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) , um die hamiltonan aus einer der broombridge-Dateien zu laden und Gate-Schätzwerte für Quantum Simulation algorigthms auszuführen:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-145">As a simple example, use the chemistry library sample, [GetGateCount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) to load the Hamiltonian from one of Broombridge files and perform gate estimates of quantum simulation algorigthms:</span></span>

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

<span data-ttu-id="3f6ee-146">Weitere Informationen zum Eingeben von durch das broombridge-Schema dargestellten Molekülen finden Sie unter [Laden einer Datei aus einer Datei](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) .</span><span class="sxs-lookup"><span data-stu-id="3f6ee-146">See [Loading a Hamiltonian from file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) for more information on how to input molecules represented by the Broombridge schema.</span></span>  

<span data-ttu-id="3f6ee-147">Weitere Informationen zur Ressourcenschätzung finden Sie unter Abrufen der [Ressourcen Anzahl](xref:microsoft.quantum.chemistry.examples.resourcecounts) .</span><span class="sxs-lookup"><span data-stu-id="3f6ee-147">See [Obtaining resource counts](xref:microsoft.quantum.chemistry.examples.resourcecounts) for more information on resource estimation.</span></span>  

### <a name="getting-started-using-the-emsl-arrows-builder"></a><span data-ttu-id="3f6ee-148">Einstieg in die Verwendung des EMSL-Pfeile-Generators</span><span class="sxs-lookup"><span data-stu-id="3f6ee-148">Getting started using the EMSL Arrows Builder</span></span>

<span data-ttu-id="3f6ee-149">EMSL-Pfeile ist ein Tool, das nwchem-und chemische Rechen Datenbanken verwendet, um Molekül Daten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-149">EMSL Arrows is a tool that uses NWChem and chemical computational databases to generate molecule data.</span></span>  <span data-ttu-id="3f6ee-150">[Der EMSL-pfeilergenerator für den Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) ermöglicht Ihnen das Eingeben des Modells mit mehreren Modellen für den molekularen Modell und das Generieren der broombridge-Datendatei, die vom Quantum Development Kit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-150">[EMSL Arrows Builder for the Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) allows you to enter your model using multiple molecular model builders and generate the Broombridge datafile to be used by the Quantum Development Kit.</span></span>  

<span data-ttu-id="3f6ee-151">Klicken Sie auf der Seite EMSL auf die Registerkarte [' instuctions '], und befolgen Sie die Anweisungen [' Simple examples '], um broombridge-Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-151">From the EMSL page, click on the ['Instuctions'] tab, and follow the ['Simple Examples'] instructions to generate Broombridge files.</span></span>  <span data-ttu-id="3f6ee-152">Versuchen Sie dann, [' getgatecount '] auszuführen, um die Quantum-Ressourcenschätzungen für diese Moleküle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-152">Then try running the ['GetGateCount'] to see the quantum resource estimates for these molecules.</span></span>

### <a name="installing-nwchem-from-source"></a><span data-ttu-id="3f6ee-153">Installieren von nwchem aus der Quelle</span><span class="sxs-lookup"><span data-stu-id="3f6ee-153">Installing NWChem from Source</span></span>

<span data-ttu-id="3f6ee-154">Vollständige Anweisungen zum Installieren von nwchem aus der Quelle [werden von pnnl bereitgestellt](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span><span class="sxs-lookup"><span data-stu-id="3f6ee-154">Full instructions on how to install NWChem from source [are provided by PNNL](http://www.nwchem-sw.org/index.php/Compiling_NWChem).</span></span>

> [!TIP]
> <span data-ttu-id="3f6ee-155">Wenn Sie nwchem von Windows 10 verwenden möchten, ist das Windows-Subsystem für Linux eine gute Option.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-155">If you wish to use NWChem from Windows 10, the Windows Subsystem for Linux is a great option.</span></span>
> <span data-ttu-id="3f6ee-156">Nachdem Sie [Ubuntu 18,04 LTS für Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)installiert haben, führen Sie `ubuntu18.04` über Ihr bevorzugtes Terminal aus, und befolgen Sie die obigen Anweisungen, um nwchem aus der Quelle zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-156">Once you have installed [Ubuntu 18.04 LTS for Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab), run `ubuntu18.04` from your favorite terminal and follow the instructions above to install NWChem from source.</span></span>

<span data-ttu-id="3f6ee-157">Nachdem Sie nwchem aus der Quelle kompiliert haben, können Sie das `yaml_driver` Skript ausführen, das mit nwchem bereitgestellt wird, um die broombridge-Instanzen schnell aus nwchem-Eingabe Karten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-157">Once you have compiled NWChem from source, you can run the `yaml_driver` script provided with NWChem to quickly produce Broombridge instances from NWChem input decks:</span></span>

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

<span data-ttu-id="3f6ee-158">Mit diesem Befehl wird eine neue `input.yaml` Datei im broombridge-Format innerhalb Ihres aktuellen Verzeichnisses erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-158">This command will create a new `input.yaml` file in the Broombridge format within your current directory.</span></span>

### <a name="using-nwchem-with-docker"></a><span data-ttu-id="3f6ee-159">Verwenden von nwchem mit docker</span><span class="sxs-lookup"><span data-stu-id="3f6ee-159">Using NWChem with Docker</span></span>

<span data-ttu-id="3f6ee-160">Vorgefertigte Images für die Verwendung von nwchem sind plattformübergreifend über [docker Hub](https://hub.docker.com)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-160">Pre-built images for using NWChem are available cross-platform via [Docker Hub](https://hub.docker.com).</span></span>
<span data-ttu-id="3f6ee-161">Befolgen Sie für den Einstieg die Docker-Installationsanweisungen für Ihre Plattform:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-161">To get started, follow the Docker installation instructions for your platform:</span></span>

- [<span data-ttu-id="3f6ee-162">Installieren von Docker für Ubuntu</span><span class="sxs-lookup"><span data-stu-id="3f6ee-162">Install Docker for Ubuntu</span></span>](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [<span data-ttu-id="3f6ee-163">Installieren von Docker für macOS</span><span class="sxs-lookup"><span data-stu-id="3f6ee-163">Install Docker for macOS</span></span>](https://docs.docker.com/docker-for-mac/install/)
- [<span data-ttu-id="3f6ee-164">Installieren von Docker für Windows 10</span><span class="sxs-lookup"><span data-stu-id="3f6ee-164">Install Docker for Windows 10</span></span>](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> <span data-ttu-id="3f6ee-165">Wenn Sie docker für Windows verwenden, müssen Sie das Laufwerk mit dem temporären Verzeichnis (in der Regel das `C:\` Laufwerk) mit dem docker-Daemon freigeben.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-165">If you are using Docker for Windows, you will need to share the drive containing your temporary directory (usually this is the `C:\` drive) with the Docker daemon.</span></span> <span data-ttu-id="3f6ee-166">Weitere Informationen finden Sie in der [docker-Dokumentation](https://docs.docker.com/docker-for-windows/#shared-drives) .</span><span class="sxs-lookup"><span data-stu-id="3f6ee-166">See the [Docker documentation](https://docs.docker.com/docker-for-windows/#shared-drives) for more details.</span></span>

<span data-ttu-id="3f6ee-167">Nachdem Sie docker installiert haben, können Sie entweder das PowerShell-Modul verwenden, das mit den Beispielen für das Quantum Development Kit bereitgestellt wurde, um das Abbild auszuführen, oder Sie können es manuell ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-167">Once you have Docker installed, you can either use the PowerShell module provided with the Quantum Development Kit samples to run the image, or you can run the image manually.</span></span>
<span data-ttu-id="3f6ee-168">Wir erläutern hier die Verwendung von PowerShell. Wenn Sie das docker-Image manuell verwenden möchten, finden Sie weitere Informationen in der [Dokumentation des Images](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span><span class="sxs-lookup"><span data-stu-id="3f6ee-168">We detail using PowerShell here; if you would like to use the Docker image manually, please see the [documentation provided with the image](https://hub.docker.com/r/nwchemorg/nwchem-qc/).</span></span>

#### <a name="running-nwchem-through-powershell-core"></a><span data-ttu-id="3f6ee-169">Ausführen von nwchem mithilfe von PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="3f6ee-169">Running NWChem through PowerShell Core</span></span>

<span data-ttu-id="3f6ee-170">Um das nwchem docker-Image mit dem Quantum Development Kit zu verwenden, wird ein kleines PowerShell-Modul bereitgestellt, das das Verschieben von Dateien in und aus nwchem für Sie behandelt.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-170">To use the NWChem Docker image with the Quantum Development Kit, we provide a small PowerShell module that handles moving files in and out of NWChem for you.</span></span>
<span data-ttu-id="3f6ee-171">Wenn Sie PowerShell Core noch nicht installiert haben, können Sie Sie plattformübergreifend [über das PowerShell-Repository auf GitHub](https://github.com/PowerShell/PowerShell#get-powershell)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-171">If you don't already have PowerShell Core installed, you can download it cross-platform from the [PowerShell repository on GitHub](https://github.com/PowerShell/PowerShell#get-powershell).</span></span>

> [!NOTE]
> <span data-ttu-id="3f6ee-172">PowerShell Core wird auch für einige Beispiele verwendet, um die Interoperabilität mit Data Science und Business Analytics-Workflows zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-172">PowerShell Core is also used for some samples to demonstrate interoperability with data science and business analytics workflows.</span></span>

<span data-ttu-id="3f6ee-173">Nachdem Sie PowerShell Core installiert haben, importieren Sie `InvokeNWChem.psm1`, um nwchem-Befehle in Ihrer aktuellen Sitzung verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-173">Once you have PowerShell Core installed, import `InvokeNWChem.psm1` to make NWChem commands available in your current session:</span></span>

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

<span data-ttu-id="3f6ee-174">Dadurch wird der `Convert-NWChemToBroombridge` Befehl in Ihrer aktuellen PowerShell-Sitzung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-174">This will make the `Convert-NWChemToBroombridge` command available in your current PowerShell session.</span></span>
<span data-ttu-id="3f6ee-175">Wenn Sie alle benötigten Images von docker herunterladen und verwenden möchten, um nwchem-Eingabe Karten auszuführen und die Ausgabe in broombridge zu erfassen, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-175">To download any needed images from Docker and use them to run NWChem input decks and capture output to Broombridge, run the following:</span></span>

```powershell
Convert-NWChemToBroombridge ./input.nw
```

<span data-ttu-id="3f6ee-176">Dadurch wird eine broombridge-Datei erstellt, indem nwchem auf `input.nw`ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-176">This will create a Broombridge file by running NWChem on `input.nw`.</span></span>
<span data-ttu-id="3f6ee-177">Standardmäßig hat die broombridge-Ausgabe denselben Namen und Pfad wie das Eingabe Stapel, wobei die `.nw` Erweiterung durch `.yaml`ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-177">By default, the Broombridge output will have the same name and path as the input deck, with the `.nw` extension replaced by `.yaml`.</span></span>
<span data-ttu-id="3f6ee-178">Dies kann überschrieben werden, indem der `-DestinationPath`-Parameter verwendet wird, um `Convert-NWChemToBroombridge`.</span><span class="sxs-lookup"><span data-stu-id="3f6ee-178">This can be overridden by using the `-DestinationPath` parameter to `Convert-NWChemToBroombridge`.</span></span>
<span data-ttu-id="3f6ee-179">Weitere Informationen finden Sie unter Verwendung der integrierten PowerShell-Funktionen:</span><span class="sxs-lookup"><span data-stu-id="3f6ee-179">More information can be obtained by using PowerShell's built-in help functionality:</span></span>

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
