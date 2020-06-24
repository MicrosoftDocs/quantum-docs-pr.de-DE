---
title: 'Installation und Validierung der Microsoft Q #-Chemie Bibliothek'
description: Erfahren Sie, wie Sie die Microsoft Quantum Chemistry-Bibliothek installieren und mit der nwchem-Berechnungs-Chemie-Plattform verwenden.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
ms.openlocfilehash: 48bf7bc980e238e622053f5c2bdd09604c572596
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275177"
---
# <a name="chemistry-library-installation-and-validation"></a>Installation und Validierung der Chemie Bibliothek

Das Quantum Development Kit bietet Unterstützung für Quantum-Chemie-Anwendungen über das [`Microsoft.Quantum.Chemistry`](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) nuget-Paket.
Wie bei anderen nuget-Paketen ist es einfach, die Chemie Bibliothek zu Ihrem Projekt hinzuzufügen.

**Visual Studio 2019:** Wenn Sie Visual Studio 2019 verwenden, können Sie die Quantum-Chemie Pakete mit dem nuget-Paket-Manager hinzufügen.
Um den Paket-Manager zu öffnen, klicken Sie mit der rechten Maustaste auf das Projekt, dem Sie die Chemie Bibliothek hinzufügen möchten, und wählen Sie "nuget-Pakete verwalten..." aus, wie im folgenden Screenshot gezeigt.

![Verwenden des nuget-Paket-Managers in Visual Studio 2019](~/media/vs2017-nuget-manage-packages.png)

Suchen Sie auf der Registerkarte Durchsuchen nach dem Paketnamen "Microsoft. Quantum. Chemistry".

> [!NOTE]
> Stellen Sie sicher, dass "incluelease einschließen" angezeigt wird.

![Kontrollkästchen "Vorabversion einschließen"](~/media/vs2017-nuget-package-search.png)

Dadurch werden die Pakete aufgelistet, die zum Herunterladen zur Verfügung stehen.
Klicken Sie im linken Bereich auf "Microsoft. Quantum. Chemistry", wählen Sie im rechten Bereich die neueste Vorabversion aus, und klicken Sie auf "Install" (installieren):

![Installieren Sie das neueste Microsoft. Quantum. Chemistry-Paket.](~/media/vs2017-nuget-select-chem.png)

Weitere Informationen finden Sie im Leitfaden für die [Benutzeroberfläche des Paket-Managers](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Alternativ können Sie die-Paket-Manager-Konsole verwenden, um dem Projekt die Quantum-Bibliothek mit einer Befehlszeilenschnittstelle hinzuzufügen.

![Verwenden der Paket-Manager-Konsole über die Befehlszeile](~/media/vs2017-nuget-console-menu.png)

Führen Sie in der Paket-Manager-Konsole Folgendes aus:

```
Install-Package Microsoft.Quantum.Chemistry
```

Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).

**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie dem `dotnet` Projekt den nuget-Paket Verweis hinzufügen:

```dotnetcli
dotnet add package Microsoft.Quantum.Chemistry
```

## <a name="verifying-your-installation"></a>Überprüfen der Installation 

Wie der Rest des quantumentwicklungskit enthält die Quantum-Bibliothek eine Reihe von vollständig dokumentierten Beispielen, mit deren Hilfe Sie schnell loslegen können.
Zum Testen Ihrer Installation mithilfe dieser Beispiele Klonen Sie das [hauptbeispielrepository](https://github.com/Microsoft/Quantum), und führen Sie dann eines der Beispiele aus.  So führen Sie z. b. das [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/MolecularHydrogen) Beispiel aus:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/chemistry/MolecularHydrogen
dotnet run
```

So überprüfen Sie die Installation der Quantum-Chemie Bibliothek mithilfe von Microsoft Visual Studio nach dem Klonen des Repository:
    1. Öffnen Sie die Projekt Mappe "chemistrysamples. sln" im Ordner "Chemistry".  
    2. Wählen Sie Samples/1 aus. Einfache Moleküle/molecularhydrogen als Startprojekt.
    3. Drücken Sie F5, um die Demo der Molekular Wasserstoff-Quantum-Phasen Schätzung auszuführen.

Weitere Informationen zum Schätzen der Werte von Energie Stufen finden Sie unter Abrufen von [Energie Stufen Schätzungen](xref:microsoft.quantum.chemistry.examples.energyestimate) .   


## <a name="using-the-quantum-development-kit-with-nwchem"></a>Verwenden des quantumentwicklungskit mit nwchem ##

Das Beispiel "molecularhydrogen" verwendet Molekulare Eingabedaten, die manuell konfiguriert werden.  Obwohl dies für kleine Beispiele in Ordnung ist, erfordert die Skalierung von Quantum-Chemie eine hamiltonation mit Millionen oder Milliarden von Begriffen. Solche von skalierbaren Berechnungs-Chemie-Paketen generierten hamiltoner sind zu groß, um per Hand zu importieren. 

Die Quantum-Bibliothek für das Quantum Development Kit ist so konzipiert, dass Sie gut mit COMPUTE-Chemie Paketen funktioniert. Dies ist insbesondere die von der Umgebung für das Umwelt Molekulare Labor (EMSL) im Pacific Nordwest National-Labor entwickelte [**nwchem**](http://www.nwchem-sw.org/) -Berechnungs Plattform.
Insbesondere `Microsoft.Quantum.Chemistry` stellt das Paket Tools zum Laden von Instanzen von Problemen bei der Quantum-Chemie Simulation dar, die im [broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)dargestellt werden und auch für den Export nach neueren Versionen von nwchem unterstützt werden.

Wir empfehlen eine der folgenden Methoden, um die Verwendung von nwchem in Verbindung mit dem Quantum Development Kit zu erreichen:
- Beginnen Sie mit der Verwendung vorhandener broombridge-Dateien, die mit den Beispielen unter [integraldata/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)bereitgestellt werden.
- Verwenden Sie den [EMSL-Pfeile-Generator für den Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) der ein webbasiertes Front-End für nwchem ist, um neue, mit broombridge formatierte Molekulare Eingabedateien zu generieren.  
- Verwenden Sie das von pnnl bereitgestellte [docker-Image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) , um nwchem auszuführen, oder
- [Kompilieren Sie nwchem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) für Ihre Plattform.

Weitere Informationen zum Arbeiten mit nwchem für chemische Modelle finden Sie unter [End-to-End mit nwchem](xref:microsoft.quantum.chemistry.examples.endtoend) , um mit der Chemie Bibliothek von Quantum Developmen Kit zu analysieren.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Die ersten Schritte mit den in den Beispielen bereitgestellten broombridge-Dateien

Der Ordner [integraldata/YAML](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) im beispielrepository für das Quantum Development Kit enthält broombridge-formierte Molekül-Datendateien.  

Verwenden Sie als einfaches Beispiel das Beispiel für die Chemie-Bibliothek, [getgatecount](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/GetGateCount) , um die hamiltonan aus einer der broombridge-Dateien zu laden und Gate-Schätzwerte für Quantum Simulation algorigthms auszuführen:

```bash
cd Quantum/Chemistry/GetGateCount
dotnet run -- --path=../IntegralData/YAML/h2.yaml --format=YAML
```

Weitere Informationen zum Eingeben von durch das broombridge-Schema dargestellten Molekülen finden Sie unter [Laden einer Datei aus einer Datei](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) .  

Weitere Informationen zur Ressourcenschätzung finden Sie unter Abrufen der [Ressourcen Anzahl](xref:microsoft.quantum.chemistry.examples.resourcecounts) .  

### <a name="getting-started-using-the-emsl-arrows-builder"></a>Einstieg in die Verwendung des EMSL-Pfeile-Generators

EMSL-Pfeile ist ein Tool, das nwchem-und chemische Rechen Datenbanken verwendet, um Molekül Daten zu generieren.  [Der EMSL-pfeilergenerator für den Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) ermöglicht Ihnen das Eingeben des Modells mit mehreren Modellen für den molekularen Modell und das Generieren der broombridge-Datendatei, die vom Quantum Development Kit verwendet werden soll.  

Klicken Sie auf der Seite EMSL auf die Registerkarte [' instuctions '], und befolgen Sie die Anweisungen [' Simple examples '], um broombridge-Dateien zu generieren.  Versuchen Sie dann, [' getgatecount '] auszuführen, um die Quantum-Ressourcenschätzungen für diese Moleküle anzuzeigen.

### <a name="installing-nwchem-from-source"></a>Installieren von nwchem aus der Quelle

Vollständige Anweisungen zum Installieren von nwchem aus der Quelle [werden von pnnl bereitgestellt](http://www.nwchem-sw.org/index.php/Compiling_NWChem).

> [!TIP]
> Wenn Sie nwchem von Windows 10 verwenden möchten, ist das Windows-Subsystem für Linux eine gute Option.
> Nachdem Sie [Ubuntu 18,04 LTS für Windows](https://www.microsoft.com/en-us/p/ubuntu-1804-lts/9n9tngvndl3q#activetab=pivot:overviewtab)installiert haben, führen Sie über `ubuntu18.04` Ihr bevorzugtes Terminal aus, und befolgen Sie die obigen Anweisungen, um nwchem aus der Quelle zu installieren.

Nachdem Sie nwchem aus der Quelle kompiliert haben, können Sie das `yaml_driver` mit nwchem bereitgestellte Skript ausführen, um schnell broombridge-Instanzen aus nwchem-Eingabe Decks zu erstellen:

```bash
$NWCHEM_TOP/contrib/quasar/yaml_driver input.nw
```

Mit diesem Befehl wird eine neue `input.yaml` Datei im broombridge-Format innerhalb Ihres aktuellen Verzeichnisses erstellt.

### <a name="using-nwchem-with-docker"></a>Verwenden von nwchem mit docker

Vorgefertigte Images für die Verwendung von nwchem sind plattformübergreifend über [docker Hub](https://hub.docker.com)verfügbar.
Befolgen Sie für den Einstieg die Docker-Installationsanweisungen für Ihre Plattform:

- [Installieren von Docker für Ubuntu](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Installieren von Docker für macOS](https://docs.docker.com/docker-for-mac/install/)
- [Installieren von Docker für Windows 10](https://docs.docker.com/docker-for-windows/install/)

> [!TIP]
> Wenn Sie docker für Windows verwenden, müssen Sie das Laufwerk mit dem temporären Verzeichnis (in der Regel das `C:\` Laufwerk) mit dem docker-Daemon freigeben. Weitere Informationen finden Sie in der [docker-Dokumentation](https://docs.docker.com/docker-for-windows/#shared-drives) .

Nachdem Sie docker installiert haben, können Sie entweder das PowerShell-Modul verwenden, das mit den Beispielen für das Quantum Development Kit bereitgestellt wurde, um das Abbild auszuführen, oder Sie können es manuell ausführen.
Wir erläutern hier die Verwendung von PowerShell. Wenn Sie das docker-Image manuell verwenden möchten, finden Sie weitere Informationen in der [Dokumentation des Images](https://hub.docker.com/r/nwchemorg/nwchem-qc/).

#### <a name="running-nwchem-through-powershell-core"></a>Ausführen von nwchem mithilfe von PowerShell Core

Um das nwchem docker-Image mit dem Quantum Development Kit zu verwenden, wird ein kleines PowerShell-Modul bereitgestellt, das das Verschieben von Dateien in und aus nwchem für Sie behandelt.
Wenn Sie PowerShell Core noch nicht installiert haben, können Sie Sie plattformübergreifend [über das PowerShell-Repository auf GitHub](https://github.com/PowerShell/PowerShell#get-powershell)herunterladen.

> [!NOTE]
> PowerShell Core wird auch für einige Beispiele verwendet, um die Interoperabilität mit Data Science und Business Analytics-Workflows zu veranschaulichen.

Nachdem Sie PowerShell Core installiert haben, importieren Sie, `InvokeNWChem.psm1` um nwchem-Befehle in Ihrer aktuellen Sitzung verfügbar zu machen:

```powershell
cd Quantum/utilities/
Import-Module ./InvokeNWChem.psm1
```

Dadurch wird der `Convert-NWChemToBroombridge` Befehl in Ihrer aktuellen PowerShell-Sitzung verfügbar.
Wenn Sie alle benötigten Images von docker herunterladen und verwenden möchten, um nwchem-Eingabe Karten auszuführen und die Ausgabe in broombridge zu erfassen, führen Sie Folgendes aus:

```powershell
Convert-NWChemToBroombridge ./input.nw
```

Dadurch wird eine broombridge-Datei erstellt, indem nwchem unter ausgeführt wird `input.nw` .
Standardmäßig hat die broombridge-Ausgabe denselben Namen und Pfad wie das Eingabe Stapel, wobei die `.nw` Erweiterung durch ersetzt wird `.yaml` .
Dies kann überschrieben werden, indem der- `-DestinationPath` Parameter für verwendet wird `Convert-NWChemToBroombridge` .
Weitere Informationen finden Sie unter Verwendung der integrierten PowerShell-Funktionen:

```powershell
Convert-NWChemToBroombridge -?
Get-Help Convert-NWChemToBroombridge -Full
```
