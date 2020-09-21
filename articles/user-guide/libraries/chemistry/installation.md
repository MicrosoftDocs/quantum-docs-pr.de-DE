---
title: Installation der Microsoft- Q# Chemie Bibliothek
description: Erfahren Sie, wie Sie die Microsoft Quantum Chemistry-Bibliothek installieren und mit der nwchem-Berechnungs-Chemie-Plattform verwenden.
author: guanghaolow
ms.author: gulow
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.chemistry.concepts.installation
no-loc:
- Q#
- $$v
ms.openlocfilehash: f1a7d1d041dab73980d8debc179d6c79acac6d33
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759798"
---
# <a name="chemistry-library-installation"></a>Installation der Chemie Bibliothek

Das [Beispiel " **molecularhydrogen** ](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogen) " verwendet Molekulare Eingabedaten, die manuell konfiguriert werden.
Obwohl dies für kleine Beispiele in Ordnung ist, erfordert die horizontale Skalierung bei der Skalierung eine Weile mit Millionen oder Milliarden von Begriffen.
Solche von skalierbaren Berechnungs-Chemie-Paketen generierten hamiltonoren sind zu groß für den manuellen Import.

Die Quantum-Bibliothek für das Quantum Development Kit ist so konzipiert, dass Sie gut mit COMPUTE-Chemie Paketen funktioniert. Dies ist insbesondere die von der Umgebung für das Umwelt Molekulare Labor (EMSL) im Pacific Nordwest National-Labor entwickelte [**nwchem**](http://www.nwchem-sw.org/) -Berechnungs Plattform.
Insbesondere das [ **Microsoft. Quantum. Chemistry** -Paket](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) stellt Tools zum Laden von Instanzen von Problemen bei der Quantum-Chemie Simulation dar, die im [broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)dargestellt werden und auch für den Export nach neueren Versionen von nwchem unterstützt werden.

Die Quantum Development Kit-Chemie Bibliothek bietet auch ein Befehlszeilen Tool, `qdk-chem` , für die Typumwandlungen zwischen Legacy Formaten und [broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge).

In diesem Abschnitt wird erläutert, wie das Quantum Development Kit mit nwchem und broombridge oder Legacy Formaten und verwendet wird `qdk-chem` .

## <a name="using-the-quantum-development-kit-with-nwchem"></a>Verwenden des quantumentwicklungskit mit nwchem

Verwenden Sie eine der folgenden Methoden, um die Verwendung von nwchem in Verbindung mit dem Quantum Development Kit zu starten:

- Beginnen Sie mit der Verwendung vorhandener broombridge-Dateien, die mit den Beispielen unter [integraldata/YAML](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML)bereitgestellt werden.
- Verwenden Sie den [EMSL-Pfeile-Generator für den Microsoft Quantum Development Kit](https://arrows.emsl.pnnl.gov/api/qsharp_chem) der ein webbasiertes Front-End für nwchem ist, um neue, mit broombridge formatierte Molekulare Eingabedateien zu generieren.  
- Verwenden Sie das von pnnl bereitgestellte [docker-Image](https://hub.docker.com/r/nwchemorg/nwchem-qc/) , um nwchem auszuführen, oder
- [Kompilieren Sie nwchem](http://www.nwchem-sw.org/index.php/Compiling_NWChem) für Ihre Plattform.

Weitere Informationen zum Arbeiten mit nwchem für chemische Modelle finden Sie unter [End-to-End mit nwchem](xref:microsoft.quantum.chemistry.examples.endtoend) , um mit der Chemie Bibliothek von Quantum Developmen Kit zu analysieren.

### <a name="getting-started-using-broombridge-files-provided-with-the-samples"></a>Die ersten Schritte mit den in den Beispielen bereitgestellten broombridge-Dateien

Der Ordner [integraldata/YAML](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/IntegralData/YAML) im beispielrepository für das Quantum Development Kit enthält broombridge-formierte Molekül-Datendateien.  

Verwenden Sie als einfaches Beispiel das Beispiel für die Chemie-Bibliothek, [getgatecount](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/GetGateCount) , um die hamiltonan aus einer der broombridge-Dateien zu laden und Gate-Schätzwerte für Quantum Simulation algorigthms auszuführen:

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

## <a name="using-the-quantum-development-kit-with-qdk-chem"></a>Verwenden des quantumentwicklungskit mit `qdk-chem`

Zum Installieren `qdk-chem` von können Sie die .net Core SDK in der Befehlszeile verwenden:

```dotnetcli
dotnet tool install --global Microsoft.Quantum.Chemistry.Tools
```

Nachdem Sie installiert haben `qdk-chem` , können Sie die Option verwenden, `--help` um weitere Details über die vom Tool angebotene Funktionalität zu erhalten `qdk-chem` .

Zum Konvertieren in und aus broombridge können Sie den Befehl verwenden `qdk-chem convert` :

```
qdk-chem convert --from fcidump --to broombridge data.fcidump --out data.yml
```

Der `qdk-chem convert` Befehl kann auch seine Daten aus der Standardeingabe akzeptieren und in die Standardausgabe schreiben. Dies ist besonders in Skripts und für die Integration mit Tools möglich, die in Legacy Formate exportieren.
Beispiel in Bash:

```bash
cat data.fcidump | qdk-convert --from fcidump --to broombridge - > data.yml
```
