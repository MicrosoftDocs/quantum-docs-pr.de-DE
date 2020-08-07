---
title: Nwchem Quantum-Beispielprogramm
description: Unter Verwendung eines nwchem-Eingabe Decks finden Sie ein Beispiel für das Aufrufen von Gate-Anzahlen für die Quantum-Chemie-Simulation.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/23/2018
uid: microsoft.quantum.chemistry.examples.endtoend
no-loc:
- Q#
- $$v
ms.openlocfilehash: 78d6488ed5e3972f85f1e6cf1ba2d197596c4cc3
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869306"
---
# <a name="end-to-end-with-nwchem"></a>End-to-End mit NWChem #

In diesem Artikel wird ein Beispiel für das Aufrufen von Gate-Anzahlen für die Quantum-Chemie-Simulation erläutert, beginnend mit einem [nwchem](http://www.nwchem-sw.org/index.php/Main_Page) -Eingabe Stapel.
Bevor Sie mit diesem Beispiel fortfahren, stellen Sie sicher, dass Sie docker installiert haben, und befolgen Sie dabei das [Installations-und Validierungs Handbuch](xref:microsoft.quantum.chemistry.concepts.installation).

Weitere Informationen finden Sie unter:
- [Struktur von nwchem-Eingabe Decks](https://github.com/nwchemgit/nwchem/wiki/Getting-Started#input-file-structure)
    - [Eingabe Karten Befehle für die Verwendung mit dem Quantum Development Kit](https://github.com/nwchemgit/nwchem/tree/master/contrib/quasar)
- [Installieren der Chemie Bibliothek und der Abhängigkeiten](xref:microsoft.quantum.chemistry.concepts.installation)
- [Ressourcen Zählung](xref:microsoft.quantum.chemistry.examples.resourcecounts)

> [!NOTE]
> Für dieses Beispiel muss Windows PowerShell Core ausgeführt werden.
> Laden Sie PowerShell Core für Windows, macOS oder Linux unter herunter https://github.com/PowerShell/PowerShell .

## <a name="importing-required-powershell-modules"></a>Importieren erforderlicher PowerShell-Module ##

Wenn Sie dies noch nicht getan haben, Klonen Sie das [Microsoft/quantum-Repository](https://github.com/Microsoft/Quantum), das Beispiele und Hilfsprogramme zum Arbeiten mit dem Quantum Development Kit enthält:

```powershell
git clone https://github.com/Microsoft/Quantum
```

Nachdem Sie geklont haben `Microsoft/Quantum` , führen Sie `cd` den `utilities/` Ordner aus, und importieren Sie das PowerShell-Modul für die Arbeit mit docker und nwchem:

```powershell
cd utilities
Import-Module InvokeNWChem.psm1
```

> [!NOTE]
> Standardmäßig verhindert Windows die Ausführung von Skripts oder Modulen als sicherheitsmeasure.
> Damit Module wie z `Invoke-NWChem.psm1` . b. unter Windows ausgeführt werden können, müssen Sie ggf. die Ausführungs Richtlinie ändern.
> Führen Sie dazu den folgenden `Set-ExecutionPolicy` Befehl aus:
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope Process
> ```
> Die Ausführungs Richtlinie wird dann wieder hergestellt, wenn Sie PowerShell beenden.
> Wenn Sie die Ausführungs Richtlinie speichern möchten, verwenden Sie einen anderen Wert für `-Scope` :
> ```powershell
> Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
> ```

Nun sollte der `Convert-NWChemToBroombridge` Befehl verfügbar sein:

```powershell
Get-Command -Module InvokeNWChem
```

Als nächstes importieren wir den Befehl, der `Get-GateCount` mit dem **getgatecount** -Beispiel bereitgestellt wird.
Ausführliche Informationen finden Sie in den [Anweisungen für das Beispiel](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/GetGateCount).
Führen Sie als nächstes Folgendes aus, und ersetzen `<runtime>` `win10-x64` Sie dabei `osx-x64` je nach `linux-x64` Betriebssystem entweder durch, oder.

```powershell
cd ../Chemistry/GetGateCount
dotnet publish --self-contained -r <runtime>
Import-Module ./bin/Debug/netcoreapp2.1/<runtime>/publish/get-gatecount.dll
```

Nun sollte der `Get-GateCount` Befehl verfügbar sein:

```powershell
Get-Command Get-GateCount
```

## <a name="input-decks"></a>Eingabe Karten ##

Das nwchem-Paket nimmt eine Textdatei mit dem Namen " _Input Karten_ " an, die ein zu lösendes Problem mit der Quantum-Chemie sowie andere Parameter wie die Speicher Belegungs Einstellungen angibt.
In diesem Beispiel verwenden wir eines der vorgefertigten Eingabe Karten, das in nwchem integriert ist.
Klonen Sie zunächst das [Repository nwchemgit/nwchem](https://github.com/nwchemgit/nwchem):

> [!NOTE]
> Da es sich um ein sehr großes Repository handelt, können wir einen flachen Klon durchführen, um Bandbreite und Speicherplatz zu sparen, indem Sie das- `--depth 1` Argument verwenden.
> Dies ist jedoch optional.
> Das Klonen funktioniert problemlos ohne `--depth 1` .

```powershell
git clone https://github.com/nwchemgit/nwchem --depth 1
```

Das `nwchemgit/nwchem` Repository verfügt über eine Vielzahl von Eingabe Decks, die für die Verwendung mit dem Quantum Development Kit vorgesehen sind, das unter dem [ `QA/chem_library_tests` Ordner](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests)aufgeführt ist.
In diesem Beispiel verwenden wir den Eingabe Stapel `H4` :

```powershell
cd nwchem/QA/chem_library_tests/H4
Get-Content h4_sto6g_0.000.nw
```

Das betreffende Molekül ist ein System von vier Wasserstoff Atomen, die in einer bestimmten Geometrie angeordnet sind, die von einem Winkel abhängt, dem Parameter, `alpha` wie im Namen des Stapels angegeben `h4_sto6g_alpha.nw` . H4 ist seit den 70er Jahren ein bekannter [Molekular Benchmarkwert](https://onlinelibrary.wiley.com/doi/abs/10.1002/qua.560180511) für die Rechen Chemie. Der-Parameter gibt an, `sto6g` dass der Stapel eine Darstellung in Bezug auf eine Slater-typorbital implementiert, insbesondere eine Darstellung in Bezug auf eine [Sto-ng-Basis](https://en.wikipedia.org/wiki/STO-nG_basis_sets) , die sechs gausche Basisfunktionen hat. Dieser Eingabe Stapel enthält außerdem mehrere Anweisungen für das nwchem Tensor-Datenbankmodul (TCE), das nwchem zum Herstellen der für die Zusammenarbeit mit dem Quantum Development Kit benötigten Informationen verwendet:

```
...
set tce:print_integrals T
set tce:qorb 18
set tce:qela  9
set tce:qelb  9
```

## <a name="producing-and-consuming-broombridge-output-from-nwchem"></a>Erstellen und Verarbeiten der broombridge-Ausgabe von nwchem ##

Sie verfügen jetzt über alles, was Sie zum erzeugen und Nutzen von broombridge-Dokumenten benötigen.
Führen Sie Folgendes aus, um nwchem auszuführen und ein broombridge-Dokument für das Eingabe Stapel zu entwickeln `h4_sto6g_0.000.nw` `Convert-NWChemToBroombridge` :

> [!NOTE]
> Wenn Sie diesen Befehl zum ersten Mal ausführen, wird das Image von Docker heruntergeladen `nwchemorg/nwchem-qc` .
> Dies kann einige Zeit in Anspruch nehmen, je nach Verbindungsgeschwindigkeit, die möglicherweise eine Gelegenheit bietet, Kaffee zu erhalten.

```powershell
Convert-NWChemToBroombridge h4_sto6g_0.000.nw 
```

Dadurch wird ein broombridge-Dokument mit dem Namen erstellt `h4_sto6g_0.000.yaml` , das Sie mit verwenden können `Get-GateCount` :

```powershell
Get-GateCount -Format YAML h4_sto6g_0.000.yaml
```

Nun sollte die Konsolenausgabe angezeigt werden, die die Ressourcenschätzung wie z. b. "T-count", "Drehungen count", "CNOT count" usw. enthält

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

Hierfür gibt es viele Dinge: 
- Probieren Sie verschiedene vordefinierte Eingabe Karten aus, z. b. durch Variation des Parameters `alpha` in `h4_sto6g_alpha.nw` , 
- Versuchen Sie, die Karten zu ändern, indem Sie die nwchem-Karten direkt bearbeiten, z. b. Durchsuchen `STO-nG` von Modellen für verschiedene Optionen von n, 
- Probieren Sie weitere vordefinierte nwchem-Eingabe Karten aus, die unter verfügbar sind. `nwchem/qa/chem_library_tests`
- Probieren Sie eine Reihe von vordefinierten broombridge-YAML-Benchmarks aus, die aus nwchem generiert wurden und als Teil des [Microsoft/quantum-Repository](https://github.com/Microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML)verfügbar sind. Diese Benchmarks umfassen Folgendes: 
    - kleine Moleküle, wie z. b. Molekulare Wasserstoff (H2), Beryllium (be), Lithium-Hydride (LIH),
    - größere Moleküle, wie z. b. Ozon (O3), Beta-Carotin, zykosinus und viele mehr. 
- Probieren Sie die grafischen Front-End- [EMSL-Pfeile](https://arrows.emsl.pnnl.gov/api/qsharp_chem) aus, die eine Schnittstelle zum Microsoft Quantum Development Kit enthalten. 


## <a name="producing-broombridge-output-from-emsl-arrows"></a>Erstellen der broombridge-Ausgabe von EMSL-Pfeilen ##

Um mit webbasierten Front-End-EMSL-Pfeilen zu beginnen, navigieren Sie in [einem Browser.](https://arrows.emsl.pnnl.gov/api/qsharp_chem) 

> [!NOTE]
> Für das Ausführen von EMSL-Pfeilen in einem Webbrowser muss JavaScript aktiviert sein. Weitere Informationen zum Aktivieren von JavaScript in Ihrem Browser finden Sie in diesen [Anweisungen](https://www.enable-javascript.com/) . 

Geben Sie zunächst ein Molekül in das Abfragefeld ein, das besagt, dass``Enter an esmiles, esmiles reaction, or other Arrows input, then push the "Run Arrows" button.`` 

Sie können zahlreiche Moleküle nach Ihrem Umgangs Namen eingeben, z. b. "Koffein" anstelle von "1, 3, 7-zanthraxanthine". 

Klicken Sie anschließend auf die Schaltfläche, die besagt ``theory{qsharp_chem}`` . Dadurch wird das Abfragefeld weiter mit einer Anweisung aufgefüllt, die den Testlauf anweist, die Ausgabe im broombridge-YAML-Format zu exportieren. 

Nun, Uhr ``Run Arrows`` . Abhängig von der Größe der Eingabe kann dies einige Zeit in Anspruch nehmen. Für den Fall, dass das jeweilige Modell bereits vorher berechnet wurde, kann es sehr schnell ausgeführt werden, da es nur auf eine Suche in einer Datenbank beschränkt wird. In beiden Fällen werden Sie zu einer neuen Seite geleitet, die eine Vielzahl von Informationen über die jeweilige nwchem-Laufzeit mit dem von Ihrer Eingabe angegebenen Stapel enthält. 

Sie können die Datei broombridge YAML aus dem Abschnitt herunterladen und speichern, der mit folgendem Header beginnt: 
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

Klicken Sie auf ``download`` , wodurch eine lokale Kopie mit einem eindeutigen Dateinamen (z ``qsharp_chem48443.yaml`` . b.) gespeichert wird. (der jeweilige Name ist für jeden Testlauf anders.) Sie können diese Datei wie oben beschrieben weiterverarbeiten, z. b. mit 
```powershell
Get-GateCount -Format YAML qsharp_chem48443.yaml
```
zum erhalten der Ressourcen Anzahl. 

Sie können den 3D-Molekül-Generator nutzen, auf den Sie ``Arrows Entry - 3D Builder`` über die Registerkarte auf der Startseite der EMSL-Pfeile zugreifen können. Wenn Sie auf das [jsmol](http://wiki.jmol.org/index.php/JSmol) 3D-Bild des angezeigten Moleküls klicken, können Sie es bearbeiten. Sie können Atome verschieben, Atome ziehen, sodass sich Ihre zwischen molekularen Abstände ändern, Atome hinzufügen/entfernen usw. Für jede dieser Optionen können Sie, nachdem Sie ``theory{qsharp_chem}`` im Abfragefeld hinzugefügt haben, eine Instanz des broombridge-YAML-Schemas generieren und Sie mithilfe der Quantum-Chemie Bibliothek weiter untersuchen. 
