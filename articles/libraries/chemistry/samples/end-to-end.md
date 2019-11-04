---
title: End-to-End mit nwchem | Microsoft-Dokumentation
description: End-to-End mit nwchem docs
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/23/2018
uid: microsoft.quantum.chemistry.examples.endtoend
ms.openlocfilehash: 8f727ea4599e06b41ced561c624c4e773b9887d9
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185816"
---
# <a name="end-to-end-with-nwchem"></a><span data-ttu-id="788bb-103">End-to-End mit nwchem</span><span class="sxs-lookup"><span data-stu-id="788bb-103">End-to-end with NWChem</span></span> #

<span data-ttu-id="788bb-104">Auf dieser Seite wird ein Beispiel für das Aufrufen von Gate-Anzahlen für die Quantum-Chemie-Simulation erläutert, beginnend mit einem [nwchem](http://www.nwchem-sw.org/index.php/Main_Page) -Eingabe Stapel.</span><span class="sxs-lookup"><span data-stu-id="788bb-104">In this page, we will walk through an example of getting gate counts for quantum chemistry simulation, starting from an [NWChem](http://www.nwchem-sw.org/index.php/Main_Page) input deck.</span></span>
<span data-ttu-id="788bb-105">Bevor Sie mit diesem Beispiel fortfahren, stellen Sie sicher, dass Sie docker installiert haben, und befolgen Sie dabei das [Installations-und Validierungs Handbuch](xref:microsoft.quantum.chemistry.concepts.installation).</span><span class="sxs-lookup"><span data-stu-id="788bb-105">Before proceeding with this example, make sure that you've installed Docker, following the [installation and validation guide](xref:microsoft.quantum.chemistry.concepts.installation).</span></span>

<span data-ttu-id="788bb-106">Weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="788bb-106">For more information:</span></span>
- [<span data-ttu-id="788bb-107">Struktur von nwchem-Eingabe Decks</span><span class="sxs-lookup"><span data-stu-id="788bb-107">Structure of NWChem input decks</span></span>](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [<span data-ttu-id="788bb-108">Eingabe Karten Befehle für die Verwendung mit dem Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="788bb-108">Input deck commands for use with the Quantum Development Kit</span></span>](https://github.com/nwchemgit/nwchem/tree/master/contrib/quasar)
- [<span data-ttu-id="788bb-109">Installieren der Chemie Bibliothek und der Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="788bb-109">Installing the chemistry library and dependencies</span></span>](xref:microsoft.quantum.chemistry.concepts.installation)
- [<span data-ttu-id="788bb-110">Ressourcen Zählung</span><span class="sxs-lookup"><span data-stu-id="788bb-110">Resource counting</span></span>](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> <span data-ttu-id="788bb-111">Für dieses Beispiel muss Windows PowerShell Core ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="788bb-111">This example requires Windows PowerShell Core to run.</span></span>
> <span data-ttu-id="788bb-112">Laden Sie PowerShell Core für Windows, macOS oder Linux unter https://github.com/PowerShell/PowerShell herunter.</span><span class="sxs-lookup"><span data-stu-id="788bb-112">Download PowerShell Core for Windows, macOS, or Linux at https://github.com/PowerShell/PowerShell.</span></span>

## <a name="importing-required-powershell-modules"></a><span data-ttu-id="788bb-113">Importieren erforderlicher PowerShell-Module</span><span class="sxs-lookup"><span data-stu-id="788bb-113">Importing Required PowerShell Modules</span></span> ##

<span data-ttu-id="788bb-114">Wenn Sie dies noch nicht getan haben, Klonen Sie das [Microsoft/quantum-Repository](https://github.com/Microsoft/Quantum), das Beispiele und Hilfsprogramme zum Arbeiten mit dem Quantum Development Kit enthält:</span><span class="sxs-lookup"><span data-stu-id="788bb-114">If you haven't already done so, clone the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum), which contains samples and utilities for working with the Quantum Development Kit:</span></span>

```powershell
git clone https://github.com/Microsoft/Quantum
```

<span data-ttu-id="788bb-115">Nachdem Sie `Microsoft/Quantum`geklont haben, führen Sie `cd` im `utilities/` Ordner aus, und importieren Sie das PowerShell-Modul für die Arbeit mit docker und nwchem:</span><span class="sxs-lookup"><span data-stu-id="788bb-115">Once you've cloned `Microsoft/Quantum`, perform `cd` into the `utilities/` folder and import the PowerShell module for working with Docker and NWChem:</span></span>

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> <span data-ttu-id="788bb-116">Standardmäßig verhindert Windows die Ausführung von Skripts oder Modulen als sicherheitsmeasure.</span><span class="sxs-lookup"><span data-stu-id="788bb-116">By default, Windows prevents the execution of any scripts or modules as a security measure.</span></span>
> <span data-ttu-id="788bb-117">Damit Module wie `Invoke-NWChem.psm1` unter Windows ausgeführt werden können, müssen Sie ggf. die Ausführungs Richtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="788bb-117">To allow modules such as `Invoke-NWChem.psm1` to run on Windows, you may need to change the execution policy.</span></span>
> <span data-ttu-id="788bb-118">Führen Sie dazu den Befehl `Set-ExecutionPolicy` aus:</span><span class="sxs-lookup"><span data-stu-id="788bb-118">To do so, run the `Set-ExecutionPolicy` command:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> <span data-ttu-id="788bb-119">Die Ausführungs Richtlinie wird dann wieder hergestellt, wenn Sie PowerShell beenden.</span><span class="sxs-lookup"><span data-stu-id="788bb-119">The execution policy will then be reverted when you exit PowerShell.</span></span>
> <span data-ttu-id="788bb-120">Wenn Sie die Ausführungs Richtlinie speichern möchten, verwenden Sie einen anderen Wert für `-Scope`:</span><span class="sxs-lookup"><span data-stu-id="788bb-120">If you would like to save the execution policy, use a different value for `-Scope`:</span></span>
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

<span data-ttu-id="788bb-121">Der `Convert-NWChemToBroombridge` Befehl sollte jetzt verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="788bb-121">You should now have the `Convert-NWChemToBroombridge` command available:</span></span>

```powershell
Get-Command -Module InvokeNWChem
```

<span data-ttu-id="788bb-122">Als nächstes importieren wir den `Get-GateCount` Befehl, der mit dem **getgatecount** -Beispiel bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="788bb-122">Next, we'll import the `Get-GateCount` command provided with the **GetGateCount** sample.</span></span>
<span data-ttu-id="788bb-123">Ausführliche Informationen finden Sie in den [Anweisungen für das Beispiel](https://github.com/Microsoft/Quantum/tree/master/Chemistry/GetGateCount).</span><span class="sxs-lookup"><span data-stu-id="788bb-123">For full details, see the [instructions provided with the sample](https://github.com/Microsoft/Quantum/tree/master/Chemistry/GetGateCount).</span></span>
<span data-ttu-id="788bb-124">Führen Sie als nächstes Folgendes aus, und ersetzen Sie `<runtime>` abhängig von Ihrem Betriebssystem entweder durch `win10-x64`, `osx-x64`oder `linux-x64`:</span><span class="sxs-lookup"><span data-stu-id="788bb-124">Next, run the following, substituting `<runtime>` with either `win10-x64`, `osx-x64`, or `linux-x64`, depending on your operating system:</span></span>

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

<span data-ttu-id="788bb-125">Der `Get-GateCount` Befehl sollte jetzt verfügbar sein:</span><span class="sxs-lookup"><span data-stu-id="788bb-125">You should now have the `Get-GateCount` command available:</span></span>

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a><span data-ttu-id="788bb-126">Eingabe Karten</span><span class="sxs-lookup"><span data-stu-id="788bb-126">Input Decks</span></span> ##

<span data-ttu-id="788bb-127">Das nwchem-Paket nimmt eine Textdatei mit dem Namen " _Input Karten_ " an, die ein zu lösendes Problem mit der Quantum-Chemie sowie andere Parameter wie die Speicher Belegungs Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="788bb-127">The NWChem package takes a text file called an _input deck_ which specifies a quantum chemistry problem to be solved, along with other parameters such as memory allocation settings.</span></span>
<span data-ttu-id="788bb-128">In diesem Beispiel verwenden wir eines der vorgefertigten Eingabe Karten, das in nwchem integriert ist.</span><span class="sxs-lookup"><span data-stu-id="788bb-128">For this example, we'll use one of the pre-made input decks that comes with NWChem.</span></span>
<span data-ttu-id="788bb-129">Klonen Sie zunächst das [Repository nwchemgit/nwchem](https://github.com/nwchemgit/nwchem):</span><span class="sxs-lookup"><span data-stu-id="788bb-129">First, clone the [nwchemgit/nwchem repository](https://github.com/nwchemgit/nwchem):</span></span>

> [!NOTE]
> <span data-ttu-id="788bb-130">Da es sich um ein sehr großes Repository handelt, können wir einen flachen Klon durchführen, um Bandbreite und Speicherplatz zu sparen, indem wir das `--depth 1` Argument verwenden.</span><span class="sxs-lookup"><span data-stu-id="788bb-130">Since this is a very large repository, we can do a shallow clone to save some bandwidth and disk space, using the `--depth 1` argument.</span></span>
> <span data-ttu-id="788bb-131">Dies ist jedoch optional.</span><span class="sxs-lookup"><span data-stu-id="788bb-131">This is optional, however.</span></span>
> <span data-ttu-id="788bb-132">Das Klonen funktioniert problemlos ohne `--depth 1`.</span><span class="sxs-lookup"><span data-stu-id="788bb-132">Cloning will work just fine without `--depth 1`.</span></span>

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

<span data-ttu-id="788bb-133">Das `nwchemgit/nwchem`-Repository verfügt über eine Vielzahl von Eingabe Karten, die für die Verwendung mit dem Quantum Development Kit vorgesehen sind, das unter dem [Ordner`QA/chem_library_tests`](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests)aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="788bb-133">The `nwchemgit/nwchem` repository comes with a variety of input decks intended for use with the Quantum Development Kit, listed under the [`QA/chem_library_tests` folder](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests).</span></span>
<span data-ttu-id="788bb-134">In diesem Beispiel verwenden wir den `H4` Eingabe-Karten:</span><span class="sxs-lookup"><span data-stu-id="788bb-134">For this example, we'll use the `H4` input deck:</span></span>

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

<span data-ttu-id="788bb-135">Bei dem fraglichen Molekül handelt es sich um ein System aus vier Wasserstoff Atomen, die in einer bestimmten Geometrie angeordnet sind, die von einem Winkel abhängt. der Parameter `alpha`, wie im Namen `h4_sto6g_alpha.nw` des Stapels angegeben.</span><span class="sxs-lookup"><span data-stu-id="788bb-135">The molecule in question is a system of 4 hydrogen atoms that are arranged in a certain geometry that depends on one angle, the parameter `alpha` as indicated in the name `h4_sto6g_alpha.nw` of the deck.</span></span> <span data-ttu-id="788bb-136">H4 ist seit den 70er Jahren ein bekannter [Molekular Benchmarkwert](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) für die Rechen Chemie.</span><span class="sxs-lookup"><span data-stu-id="788bb-136">H4 is a known [molecular benchmark](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) for computational chemistry since the 1970s.</span></span> <span data-ttu-id="788bb-137">Der Parameter `sto6g` weist darauf hin, dass der Stapel eine Darstellung in Bezug auf eine Slater-typorbital implementiert, insbesondere eine Darstellung in Bezug auf einen [Sto-ng-Basis Satz](https://en.wikipedia.org/wiki/STO-nG_basis_sets) mit 6 gauschen Basisfunktionen.</span><span class="sxs-lookup"><span data-stu-id="788bb-137">The parameter `sto6g` is indicative that the deck implements a representation with respect to a Slater-type orbital, specifically, a representation with respect to an [STO-nG basis set](https://en.wikipedia.org/wiki/STO-nG_basis_sets) with 6 Gaussian basis functions.</span></span> <span data-ttu-id="788bb-138">Dieser Eingabe Stapel enthält außerdem mehrere Anweisungen für das nwchem Tensor-Datenbankmodul (TCE), das nwchem zum Herstellen der für die Zusammenarbeit mit dem Quantum Development Kit benötigten Informationen verwendet:</span><span class="sxs-lookup"><span data-stu-id="788bb-138">This input deck furthermore contains several instructions to the NWChem Tensor Contraction Engine (TCE) that direct NWChem to produce the information needed for interoperating with the Quantum Development Kit:</span></span>

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a><span data-ttu-id="788bb-139">Erstellen und Verarbeiten der broombridge-Ausgabe von nwchem</span><span class="sxs-lookup"><span data-stu-id="788bb-139">Producing and Consuming Broombridge Output from NWChem</span></span> ##

<span data-ttu-id="788bb-140">Wir haben jetzt alles, was wir benötigen, um broombridge-Dokumente zu erzeugen und zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="788bb-140">We now have everything we need to produce and consume Broombridge documents.</span></span>
<span data-ttu-id="788bb-141">Führen Sie `Convert-NWChemToBroombridge`aus, um nwchem auszuführen und ein broombridge-Dokument für die `h4_sto6g_0.000.nw` Eingabe-Karten zu entwickeln:</span><span class="sxs-lookup"><span data-stu-id="788bb-141">To run NWChem and produce a Broombridge document for the `h4_sto6g_0.000.nw` input deck, run `Convert-NWChemToBroombridge`:</span></span>

> [!NOTE]
> <span data-ttu-id="788bb-142">Wenn Sie diesen Befehl zum ersten Mal ausführen, wird das `nwchemorg/nwchem-qc` Abbild von Docker heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="788bb-142">The first time you run this command, Docker will download the `nwchemorg/nwchem-qc` image for you.</span></span>
> <span data-ttu-id="788bb-143">Dies kann einige Zeit in Anspruch nehmen, je nach Verbindungsgeschwindigkeit, die möglicherweise eine Gelegenheit bietet, Kaffee zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="788bb-143">This may take a little while, depending on your connection speed, possibly providing an opportunity to get a cup of coffee.</span></span>

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

<span data-ttu-id="788bb-144">Dadurch wird ein broombridge-Dokument mit dem Namen `h4_sto6g_0.000.yaml` erstellt, das wir mit `Get-GateCount`verwenden können:</span><span class="sxs-lookup"><span data-stu-id="788bb-144">This will produce a Broombridge document called `h4_sto6g_0.000.yaml` that we can use with `Get-GateCount`:</span></span>

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

<span data-ttu-id="788bb-145">Nun sollte die Konsolenausgabe angezeigt werden, die die Ressourcenschätzung wie z. b. "T-count", "Drehungen count", "CNOT count" usw. enthält</span><span class="sxs-lookup"><span data-stu-id="788bb-145">You should now see console output which contains resource estimation such as T-count, rotations count, CNOT count, etc. for various quantum simulation methods:</span></span>

```powershell 
IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Trotter
TCount              : 0
RotationsCount      : 92
CNOTCount           : 520
ElapsedMilliseconds : 327

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Qubitization
TCount              : 438
RotationsCount      : 516
CNOTCount           : 2150
ElapsedMilliseconds : 528

IntegralDataPath    : C:\Users\martinro\REPOS\nwchem\qa\chem_library_tests\h4\h4_sto6g_0.000.yaml
HamiltonianName     : hamiltonian_0
SpinOrbitals        : 8
Method              : Optimized Qubitization
TCount              : 3540
RotationsCount      : 18
CNOTCount           : 7932
ElapsedMilliseconds : 721
```

<span data-ttu-id="788bb-146">Hierfür gibt es viele Dinge:</span><span class="sxs-lookup"><span data-stu-id="788bb-146">There are many things to go do from here:</span></span> 
- <span data-ttu-id="788bb-147">Probieren Sie verschiedene vordefinierte Eingabe Karten aus, z. b. indem Sie den Parameter `alpha` in `h4_sto6g_alpha.nw`verändern.</span><span class="sxs-lookup"><span data-stu-id="788bb-147">Try out different predefined input decks, e.g., by varying the parameter `alpha` in `h4_sto6g_alpha.nw`,</span></span> 
- <span data-ttu-id="788bb-148">Versuchen Sie, die Karten zu ändern, indem Sie die nwchem-Karten direkt bearbeiten, z. b. `STO-nG` Modelle für verschiedene Optionen von n,</span><span class="sxs-lookup"><span data-stu-id="788bb-148">Try modifying the decks by editing the NWChem decks directly, e.g., exploring `STO-nG` models for various choices of n,</span></span> 
- <span data-ttu-id="788bb-149">Probieren Sie weitere vordefinierte nwchem-Eingabe Karten aus, die unter `nwchem/qa/chem_library_tests`verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="788bb-149">Try other predefined NWChem input decks that are available at `nwchem/qa/chem_library_tests`,</span></span>
- <span data-ttu-id="788bb-150">Probieren Sie eine Reihe von vordefinierten broombridge-YAML-Benchmarks aus, die aus nwchem generiert wurden und als Teil des [Microsoft/quantum-Repository](https://github.com/Microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML)verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="788bb-150">Try out a suite of predefined Broombridge YAML benchmarks that were generated from NWChem and are available as part of the [Microsoft/Quantum repository](https://github.com/Microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML).</span></span> <span data-ttu-id="788bb-151">Diese Benchmarks umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="788bb-151">These benchmarks include:</span></span> 
    - <span data-ttu-id="788bb-152">kleine Moleküle, wie z. b. Molekulare Wasserstoff (H2), Beryllium (be), Lithium-Hydride (LIH),</span><span class="sxs-lookup"><span data-stu-id="788bb-152">small molecules such as molecular hydrogen (H2), Beryllium (Be), Lithium hydride (LiH),</span></span>
    - <span data-ttu-id="788bb-153">größere Moleküle, wie z. b. Ozon (O3), Beta-Carotin, zykosinus und viele mehr.</span><span class="sxs-lookup"><span data-stu-id="788bb-153">larger molecules such as ozone (O3), beta-carotene, cytosine, and many more.</span></span> 
- <span data-ttu-id="788bb-154">Probieren Sie die grafischen Front-End- [EMSL-Pfeile](https://arrows.emsl.pnnl.gov/api/qsharp_chem) aus, die eine Schnittstelle zum Microsoft Quantum Development Kit enthalten.</span><span class="sxs-lookup"><span data-stu-id="788bb-154">Try out the graphical front-end [EMSL Arrows](https://arrows.emsl.pnnl.gov/api/qsharp_chem) that features an interface to the Microsoft Quantum Development Kit.</span></span> 


## <a name="producing-broombridge-output-from-emsl-arrows"></a><span data-ttu-id="788bb-155">Erstellen der broombridge-Ausgabe von EMSL-Pfeilen</span><span class="sxs-lookup"><span data-stu-id="788bb-155">Producing Broombridge Output from EMSL Arrows</span></span> ##

<span data-ttu-id="788bb-156">Um mit webbasierten Front-End-EMSL-Pfeilen zu beginnen, navigieren Sie in [einem Browser.](https://arrows.emsl.pnnl.gov/api/qsharp_chem)</span><span class="sxs-lookup"><span data-stu-id="788bb-156">To get started with web-based front end EMSL Arrows, navigate a browser [here](https://arrows.emsl.pnnl.gov/api/qsharp_chem).</span></span> 

> [!NOTE]
> <span data-ttu-id="788bb-157">Für das Ausführen von EMSL-Pfeilen in einem Webbrowser muss JavaScript aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="788bb-157">Running EMSL Arrows in a web browser requires JavaScript to be enabled.</span></span> <span data-ttu-id="788bb-158">Weitere Informationen zum Aktivieren von JavaScript in Ihrem Browser finden Sie in diesen [Anweisungen](https://www.enable-javascript.com/) .</span><span class="sxs-lookup"><span data-stu-id="788bb-158">Please refer to these [instructions](https://www.enable-javascript.com/) on how to enable JavaScript in your browser.</span></span> 

<span data-ttu-id="788bb-159">Geben Sie zunächst ein Molekül in das Abfragefeld ein, das besagt ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span><span class="sxs-lookup"><span data-stu-id="788bb-159">First, enter a molecule in the query box that says ``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.``</span></span> 

<span data-ttu-id="788bb-160">Sie können zahlreiche Moleküle nach Ihrem Umgangs Namen eingeben, z. b. "Koffein" anstelle von "1, 3, 7-zanthraxanthine".</span><span class="sxs-lookup"><span data-stu-id="788bb-160">You can enter many molecules by their colloquial name, such as "caffeine" instead of "1,3,7-Trimethylxanthine".</span></span> 

<span data-ttu-id="788bb-161">Klicken Sie anschließend auf die Schaltfläche ``theory{qsharp_chem}``.</span><span class="sxs-lookup"><span data-stu-id="788bb-161">Next, click the button that says ``theory{qsharp_chem}``.</span></span> <span data-ttu-id="788bb-162">Dadurch wird das Abfragefeld weiter mit einer Anweisung aufgefüllt, die den Testlauf anweist, die Ausgabe im broombridge-YAML-Format zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="788bb-162">This will populate the query box further with an instruction that will tell the run to export output in the Broombridge YAML format.</span></span> 

<span data-ttu-id="788bb-163">Nun, Uhr ``Run Arrows``.</span><span class="sxs-lookup"><span data-stu-id="788bb-163">Now, clock on ``Run Arrows``.</span></span> <span data-ttu-id="788bb-164">Abhängig von der Größe der Eingabe kann dies einige Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="788bb-164">Depending on the size of the input, this might take a while.</span></span> <span data-ttu-id="788bb-165">Für den Fall, dass das jeweilige Modell bereits vorher berechnet wurde, kann es sehr schnell ausgeführt werden, da es nur auf eine Suche in einer Datenbank beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="788bb-165">Or, in case the particular model has already been computed before, it can be done extremely fast as it will only amount to a lookup in a database.</span></span> <span data-ttu-id="788bb-166">In beiden Fällen werden Sie zu einer neuen Seite geleitet, die eine Vielzahl von Informationen über die jeweilige nwchem-Laufzeit mit dem von Ihrer Eingabe angegebenen Stapel enthält.</span><span class="sxs-lookup"><span data-stu-id="788bb-166">In either case, you will be taken to a new page that contains a plethora of information about the particular run of NWChem against the deck specified by your input.</span></span> 

<span data-ttu-id="788bb-167">Sie können die Datei broombridge YAML aus dem Abschnitt herunterladen und speichern, der mit folgendem Header beginnt:</span><span class="sxs-lookup"><span data-stu-id="788bb-167">You can download and save the Broombridge YAML file from the section that starts with the following header:</span></span> 
```powershell
+==================================================+
||              Molecular Calculation             ||
+==================================================+

Id     = 48443

NWOutput = Link to NWChem Output (download)

Datafiles:
qsharp_chem.yaml-2018-10-23-14:37:42 (download)
...
```

<span data-ttu-id="788bb-168">Klicken Sie auf ``download``, wodurch eine lokale Kopie mit einem eindeutigen Dateinamen (z. b. ``qsharp_chem48443.yaml`` gespeichert wird. (der jeweilige Name ist für jeden Testlauf anders.)</span><span class="sxs-lookup"><span data-stu-id="788bb-168">Click on ``download``, which saves a local copy with a unique file name such as ``qsharp_chem48443.yaml`` (the particular name will be different for each run).</span></span> <span data-ttu-id="788bb-169">Sie können diese Datei wie oben beschrieben weiterverarbeiten, z. b. mit</span><span class="sxs-lookup"><span data-stu-id="788bb-169">You can then further process this file as above, e.g., with</span></span> 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
<span data-ttu-id="788bb-170">zum erhalten der Ressourcen Anzahl.</span><span class="sxs-lookup"><span data-stu-id="788bb-170">to get resource counts.</span></span> 

<span data-ttu-id="788bb-171">Sie können den 3D-Molekül-Generator nutzen, auf den Sie über die Registerkarte "``Arrows Entry - 3D Builder``" auf der Seite "EMSL-Pfeile" zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="788bb-171">You might enjoy the 3D molecule builder that can be accessed from the ``Arrows Entry - 3D Builder`` tab on the EMSL Arrows start page.</span></span> <span data-ttu-id="788bb-172">Wenn Sie auf das [jsmol](http://wiki.jmol.org/index.php/JSmol) 3D-Bild des angezeigten Moleküls klicken, können Sie es bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="788bb-172">Clicking the [JSMol](http://wiki.jmol.org/index.php/JSmol) 3D picture of the shown molecule will let you allow to edit it.</span></span> <span data-ttu-id="788bb-173">Sie können Atome verschieben, Atome ziehen, sodass sich Ihre zwischen molekularen Abstände ändern, Atome hinzufügen/entfernen usw. Wenn Sie ``theory{qsharp_chem}`` im Feld Abfrage hinzugefügt haben, können Sie für jede dieser Optionen eine Instanz des broombridge-YAML-Schemas generieren und Sie mithilfe der Quantum-Chemie Bibliothek weiter untersuchen.</span><span class="sxs-lookup"><span data-stu-id="788bb-173">You can move atoms around, drag atoms apart so that their inter-molecular distances change, add/remove atoms, etc. For each of these choices, once you added ``theory{qsharp_chem}`` in the query box, you can then generate an instance of the Broombridge YAML schema and further explore it using the Quantum Chemistry Library.</span></span> 
