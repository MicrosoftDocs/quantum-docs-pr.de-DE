---
title: Versionshinweise für das Quantum Development Kit
description: Enthält Informationen zu den neuesten Aktualisierungen für das Microsoft Quantum Development Kit (Vorschauversion).
author: natke
ms.author: nakersha
ms.date: 09/30/2019
ms.topic: article
uid: microsoft.quantum.relnotes
ms.openlocfilehash: 4fbb740568ff6cdc99e4f6a813802ed8d4234ab4
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "81269385"
---
# <a name="microsoft-quantum-development-kit-release-notes"></a>Versionshinweise für das Microsoft Quantum Development Kit

Dieser Artikel enthält Informationen zu den einzelnen Releases des Microsoft Quantum Development Kit.

Installationsanweisungen finden Sie im [Installationshandbuch](xref:microsoft.quantum.install).

Updateanweisungen finden Sie im [Updatehandbuch](xref:microsoft.quantum.update).


## <a name="version-01120032506"></a>Version 0.11.2003.2506

*Veröffentlichungsdatum: 26. März 2020*

Dieses Release enthält Folgendes:

- Neue Unterstützung für Zugriffsmodifizierer in Q#. Weitere Informationen finden Sie unter [Dateistrukturen](xref:microsoft.quantum.language.file-structure).
- Aktualisiert auf .NET Core SDK 3.1

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020022610"></a>Version 0.10.2002.2610

*Veröffentlichungsdatum: 27. Februar 2020*

Dieses Release enthält Folgendes:

- Neue Quantum Machine Learning-Bibliothek. Weitere Informationen finden Sie auf unserer [QML-Seite](https://docs.microsoft.com/quantum/libraries/machine-learning/?view=qsharp-preview).
- Fehlerbehebungen für IQ# haben zu einer Leistungssteigerung um das Zehn- bis Zwanzigfache beim Laden von NuGet-Paketen geführt

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01020012831"></a>Version 0.10.2001.2831

*Veröffentlichungsdatum: 29. Januar 2020*

Dieses Release enthält Folgendes:

- Neues NuGet-Paket „Microsoft.Quantum.SDK“, mit dem das NuGet-Paket „Microsoft.Quantum.Development.Kit“ bei der Erstellung neuer Projekte ersetzt wird. Das NuGet-Paket „Microsoft.Quantum.Development.Kit“ wird für vorhandene Projekte weiter unterstützt. 
- Unterstützung für Q#-Compilererweiterungen basierend auf dem neuen NuGet-Paket „Microsoft.Quantum.SDK“. Weitere Informationen finden Sie in der [Dokumentation auf GitHub](https://github.com/microsoft/qsharp-compiler/tree/master/src/QuantumSdk#extending-the-q-compiler), im [Beispiel für Compilererweiterungen](https://github.com/microsoft/qsharp-compiler/tree/master/examples/CompilerExtensions) und im [Blog zur Q#-Entwicklung](https://devblogs.microsoft.com/qsharp/extending-the-q-compiler/).
- Unterstützung für .NET Core 3.1 hinzugefügt. Wir empfehlen Ihnen dringend, Version 3.1.100 zu installieren, da es bei Buildvorgängen mit früheren .NET Core SDK-Versionen zu Problemen kommen kann.
- Neue Compilertransformationen verfügbar unter „Microsoft.Quantum.QsCompiler.Experimental“.
- Neue Funktionalität zum Verfügbarmachen von Ausgabezustandsvektoren als HTML-Code in IQ#.
- EstimateFrequencyA-Unterstützung zu Microsoft.Quantum.Characterization für Hadamard- und SWAP-Tests hinzugefügt.
- Für den Namespace „AmplitudeAmplification“ wird jetzt der Q#-Styleguide verwendet.

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019120501"></a>Version 0.10.1912.0501

*Veröffentlichungsdatum: 5. Dezember 2019*

Dieses Release enthält Folgendes:

- Neues Testattribut für Q#-Komponententests. Informationen finden Sie in der aktualisierten [API-Dokumentation](https://docs.microsoft.com/qsharp/api/qsharp/microsoft.quantum.diagnostics.test) und im aktualisierten [Leitfaden zum Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging).
- Stapelüberwachung im Fall eines Q#-Programmausführungsfehlers hinzugefügt
- Unterstützung für Breakpoints in Visual Studio Code aufgrund einer Aktualisierung der [OmniSharp-C#-Erweiterung für Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-01019111607"></a>Version 0.10.1911.1607

*Veröffentlichungsdatum: 17. November 2019*

Dieses Release enthält Folgendes:

- Behebung von Leistungsproblemen für [Quanten-Katas](https://github.com/Microsoft/QuantumKatas) und Jupyter Notebook-Instanzen

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  


## <a name="version-0101911307"></a>Version 0.10.1911.307

*Veröffentlichungsdatum: 1. November 2019*

Dieses Release enthält Folgendes:

- Updates für Visual Studio Code- und Visual Studio-Erweiterungen zur Bereitstellung des Sprachservers als eigenständige ausführbare Datei, wodurch sich die Abhängigkeit von .NET Core SDK-Versionen erübrigt  
- Migration zu .NET Core 3.0
- Breaking Change an Microsoft.Quantum.Simulation.Core.IOperationFactory mit Einführung der neuen `Fail`-Methode. Dies betrifft nur benutzerdefinierte Simulatoren, die SimulatorBase nicht erweitern. Weitere Informationen finden Sie im [Pull Request auf GitHub](https://github.com/microsoft/qsharp-runtime/pull/59).
- Neue Unterstützung für veraltete Attribute

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-0919093002"></a>Version 0.9.1909.3002

*Veröffentlichungsdatum: 30. September 2019*

Dieses Release enthält Folgendes:

- Unterstützung für die Q#-Codevervollständigung in Visual Studio 2019 (Versionen 16.3 und höher) und Visual Studio Code
- neues [Quantum Kata](https://github.com/Microsoft/QuantumKatas) für Quantenaddierer

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-09-packagereference-0919082902"></a>Version 0.9 (*PackageReference 0.9.1908.2902*)

*Veröffentlichungsdatum: 29. August 2019*

Dieses Release enthält Folgendes:

- Unterstützung für [Konjugationsanweisungen](xref:microsoft.quantum.language.statements#conjugations) in Q#
- neue Codeaktionen im Compiler wie beispielsweise „Ersetzen durch“, „Add documentation“ (Dokumentation hinzufügen) und Updates für einfache Arrayelemente
- Installationsvorlagen und neue Projektbefehle für die Visual Studio Code-Erweiterung
- neue Varianten des ApplyIf-Kombinators wie beispielsweise [Microsoft.Quantum.Canon.ApplyIfOne](xref:microsoft.quantum.canon.applyifone)
- zusätzliche in Jupyter Notebook konvertierte [Quantum Katas](https://github.com/Microsoft/QuantumKatas)
- Für die Visual Studio-Erweiterung ist jetzt Visual Studio 2019 erforderlich.

Hier finden Sie die vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed), [Compiler](https://github.com/microsoft/qsharp-compiler/pulls?q=is%3Apr+is%3Aclosed), [Runtime](https://github.com/microsoft/qsharp-runtime/pulls?q=is%3Apr+is%3Aclosed), [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed) und [Katas](https://github.com/microsoft/QuantumKatas/pulls?q=is%3Apr+is%3Aclosed).  

Hier werden die Änderungen sowie Anweisungen zum Aktualisieren vorhandener Programme beschrieben.  Weitere Informationen zu diesen Änderungen finden Sie im [Q#-Entwicklerblog](https://devblogs.microsoft.com/qsharp).

## <a name="version-08-packagereference-0819071701"></a>Version 0.8 (*PackageReference 0.8.1907.1701*)

*Veröffentlichungsdatum: 12. Juli 2019*

Dieses Release enthält Folgendes:

- neue Indizierungsspeicherorte für das Aufteilen von Arrays (weitere Informationen in der [Sprachreferenz](xref:microsoft.quantum.language.expressions#array-slices))
- Dockerfiles, die über die [Microsoft-Containerregistrierung](https://github.com/microsoft/ContainerRegistry) gehostet werden (weitere Informationen unter [IQ#-Repository](https://github.com/microsoft/iqsharp/blob/master/README.md))
- wichtige Änderungen für den [Ablaufverfolgungssimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), Updates für Konfigurationseinstellungen und Namensänderungen (siehe [.NET-API-Browser für die aktualisierten Namen](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulatorconfiguration))

Hier finden Sie eine vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) und [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

## <a name="version-07-packagereference-0719053109"></a>Version 0.7 (*PackageReference 0.7.1905.3109*)

*Veröffentlichungsdatum: 31. Mai 2019*

Dieses Release enthält Folgendes:
- Ergänzungen der Q#-Sprache 
- Aktualisierungen der Quantum Chemistry Library (Quantenchemiebibliothek) 
- neue numerische Bibliothek

Hier finden Sie eine vollständige Liste geschlossener Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) und [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed).  

Hier werden die Änderungen sowie Anweisungen zum Aktualisieren vorhandener Programme beschrieben.  Weitere Informationen zu diesen Änderungen finden Sie im [Q#-Entwicklerblog](https://devblogs.microsoft.com/qsharp).

### <a name="q-language-syntax"></a>Q#-Sprachsyntax
Mit diesem Release wird eine neue Q#-Sprachsyntax hinzugefügt:
* benannte Elemente für [benutzerdefinierte Typen](xref:microsoft.quantum.language.type-model#user-defined-types)  
* benutzerdefinierte Typkonstruktoren für die Verwendung als Funktionen
* Unterstützung für [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions) und [apply-and-reassign]((xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols)) in benutzerdefinierten Typen
* optionales Blockieren von Fehlerbehebungen im Zusammenhang mit [repeat-until-success](xref:microsoft.quantum.language.statements#repeat-until-success-loop)-Schleifen
* Unterstützung für while-Schleifen in Funktionen (nicht in Vorgängen)

### <a name="library"></a>Bibliothek 

Mit diesem Release wird eine numerische Bibliothek hinzugefügt: Informieren Sie sich über die [Verwendung der numerischen Bibliothek](xref:microsoft.quantum.numerics.usage), und probieren Sie die [neuen Beispiele](https://github.com/microsoft/quantum/tree/master/Numerics) aus.  [PR #102](https://github.com/Microsoft/QuantumLibraries/pull/102).  

Mit diesem Release werden Erweiterungen neu organisiert, und die Chemiebibliothek wird aktualisiert:
* verbesserte Modularität von Komponenten, der Erweiterbarkeit und allgemeine Codebereinigung  [PR #58](https://github.com/microsoft/QuantumLibraries/pull/58).
* Unterstützung für [Multireferenz-Wellenfunktionen](xref:microsoft.quantum.chemistry.concepts.multireference) (sowohl für Multireferenz-Wellenfunktionen als auch für einheitlich verbundene Cluster).  [PR #110](https://github.com/Microsoft/QuantumLibraries/pull/110).
* (Vielen Dank!) [1QBit](https://1qbit.com)-Mitwirkender ([@valentinS4t1qbit](https://github.com/ValentinS4t1qbit)): Energieauswertung mithilfe eines variablen Ansatzes. [PR #120](https://github.com/Microsoft/QuantumLibraries/pull/120).
* Aktualisieren des [Broombridge](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)-Schemas auf die neue [Version 0.2](xref:microsoft.quantum.libraries.chemistry.schema.spec_v_0_2) und Hinzufügen einer einheitlichen gekoppelten Clusterspezifikation. [Issue #65](https://github.com/microsoft/QuantumLibraries/issues/65).
* Hinzufügen der Python-Interoperabilität zu Chemiebibliothekfunktionen Testen Sie dieses [Beispiel](https://github.com/microsoft/Quantum/tree/master/Chemistry/PythonIntegration). [Problem 53](https://github.com/microsoft/QuantumLibraries/issues/53) [PR 110](https://github.com/Microsoft/QuantumLibraries/pull/110).

## <a name="version-061905"></a>Version 0.6.1905

*Veröffentlichungsdatum: 3. Mai 2019*

Dieses Release enthält Folgendes:
- Änderungen der Q#-Sprache 
- Neustrukturierung der Bibliotheken des Quantum Development Kit 
- neue Beispiele 
- Fehlerbehebungen  (sämtliche geschlossene Pull Requests für [Bibliotheken](https://github.com/Microsoft/QuantumLibraries/pulls?q=is%3Apr+is%3Aclosed) und [Beispiele](https://github.com/Microsoft/Quantum/pulls?q=is%3Apr+is%3Aclosed))  

Hier werden die Änderungen sowie Anweisungen zum Aktualisieren vorhandener Programme beschrieben.  Weitere Informationen zu diesen Änderungen finden Sie unter devblogs.microsoft.com/qsharp.

### <a name="q-language-syntax"></a>Q#-Sprachsyntax
Mit diesem Release wird eine neue Q#-Sprachsyntax hinzugefügt:
* Fügen Sie eine [schnelle Methode zum Ausdrücken von Spezialisierungen von Quantenvorgängen](xref:microsoft.quantum.language.type-model#functors) (Steuerelement und Adjunkte) mit `+`-Operatoren hinzu.  Die frühere Syntax ist veraltet.  Programme, die die alte Syntax verwenden (z. B. `: adjoint`), funktionieren auch weiterhin, es wird jedoch eine Warnung zur Kompilierzeit generiert.  
* Fügen Sie einen neuen Operator für [copy-and-update](xref:microsoft.quantum.language.expressions#copy-and-update-expressions) hinzu. `w/` kann zum Ausdrücken von Arrayerstellungen als Änderung eines vorhandenen Arrays verwendet werden.
* Fügen Sie die allgemeine [apply-and-update](xref:microsoft.quantum.language.statements#rebinding-of-mutable-symbols)-Anweisung hinzu (z. B. `+=`/`w/=`).
* Fügen Sie eine Methode zum Angeben eines kurzen Namens für Namespaces in [offenen Direktiven](xref:microsoft.quantum.language.file-structure#open-directives) hinzu.

Mit diesem Release ist es nicht mehr möglich, ein Arrayelement auf der linken Seite einer set-Anweisung anzugeben.  Dies liegt daran, dass diese Syntax impliziert, dass Arrays veränderbar sind, wenn das Ergebnis des Vorgangs tatsächlich immer das Erstellen eines neuen Arrays mit der Änderung war.  Stattdessen wird ein Compilerfehler mit dem Vorschlag generiert, den neuen copy-and-update-Operator (`w/`) zu verwenden, um das gleiche Ergebnis zu erzielen.  

### <a name="library-restructuring"></a>Umstrukturierung der Bibliothek
Mit diesem Release werden die Bibliotheken neu organisiert, um ein konsistentes Wachstum zu ermöglichen:
* Der Namespace Microsoft.Quantum.Primitive wird in Microsoft.Quantum.Intrinsic umbenannt.  Diese Vorgänge werden vom Zielcomputer implementiert.  Der Namespace Microsoft.Quantum.Primitive ist veraltet.  Eine Runtimewarnung informiert Sie darüber, wann Programme mithilfe von veralteten Namen Vorgänge und Funktionen aufrufen.

* Das Paket Microsoft.Quantum.Canon wird in Microsoft.Quantum.Standard umbenannt.  Dieses Paket enthält Namespaces, die für die meisten Q#-Programme verwendet werden.  Dies schließt Folgendes ein:  
    - Microsoft.Quantum.Canon-Paket für allgemeine Vorgänge
    - Microsoft.Quantum.Arithmetic für universelle arithmetische Operationen
    - Microsoft.Quantum.Preparation für Vorgänge zum Vorbereiten des Qubit-Zustands.
    - Microsoft.Quantum.Simulation für die Simulationsfunktionalität

Durch diese Änderung treten bei Programmen, die eine einzelne „Open“-Anweisung für den Namespace Microsoft.Quatum.Canon enthalten, möglicherweise Buildfehler auf, wenn das Programm auf Vorgänge verweist, die in die anderen drei neuen Namespaces verschoben wurden.  Das Hinzufügen zusätzlicher „Open“-Anweisungen für die drei neuen Namespaces ist eine einfache Möglichkeit, dieses Problem zu beheben.  

* Mehrere Namespaces sind veraltet, da die Vorgänge in anderen Namespaces neu organisiert wurden. Programme, die diese Namespaces verwenden, funktionieren weiterhin. Eine Warnung zur Kompilierzeit bezeichnet den Namespace, in dem der Vorgang definiert ist.  

* Das Namespace Microsoft.Quantum.Arithmetic wurde normalisiert, um den benutzerdefinierten <xref:microsoft.quantum.arithmetic.littleendian>-Typ zu verwenden. Verwenden Sie bei Bedarf die Funktion [BigEndianAsLittleEndian](xref:microsoft.quantum.arithmetic.bigendianaslittleendian) für die Konvertierung zu Little-Endian.  

* Die Namen mehrerer Callable-Funktionen und -Vorgänge wurden so geändert, dass sie den Vorgaben im [Q#-Styleguide](xref:microsoft.quantum.contributing.style) entsprechen.  Die alten Callable-Namen sind veraltet.  Programme, die die alten Callables-Namen verwenden, funktionieren weiterhin. Es wird eine Warnung zur Kompilierzeit generiert. 

### <a name="new-samples"></a>Neue Beispiele

Wir haben ein [Beispiel für die Verwendung von Q# mit F#-Treibern](https://github.com/Microsoft/Quantum/pull/164) hinzugefügt.  

**Besonderer Dank** gilt dem folgenden Mitwirkenden an der offenen Codebasis unter http://github.com/Microsoft/Quantum. Diese Beiträge ergänzen die umfangreichen Beispiele von Q#-Code:

* Mathias Soeken ([@msoeken](https://github.com/msoeken)): Oracle-Funktionssynthese. [PR #135](https://github.com/Microsoft/Quantum/pull/135).

### <a name="migrating-existing-projects-to-061905"></a>Migrieren vorhandener Projekte zu Version 0.6.1905

Informationen zum Aktualisieren des Microsoft Quantum Development Kit finden Sie im [Installationshandbuch](xref:microsoft.quantum.install).
  
Wenn Sie über vorhandene Q#-Projekte der Version 0.5 des Quantum Development Kit verfügen, können Sie diese Projekte mit den folgenden Schritten zur neuesten Version migrieren.

    1. Projekte müssen in der richtigen Reihenfolge aktualisiert werden.  Wenn Sie über eine Projektmappe mit mehreren Projekten verfügen, sollten Sie jedes Projekt in der Reihenfolge aktualisieren, in der darauf verwiesen wird.
    2. Führen Sie in der Befehlszeile `dotnet clean` aus, um alle vorhandenen Binärdateien und Zwischendateien zu entfernen.
    3. Bearbeiten Sie in einem Text-Editor die CSPROJ-Datei, um die Version von den Microsoft.Quantum-`PackageReference`-Paketen auf Version 0.6.1904 zu ändern. Ändern Sie außerdem den Paketnamen „Microsoft.Quantum.Canon“ in „Microsoft.Quantum.Standard“. Beispiel:

         ```xml
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.6.1905.301" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.6.1905.301" />
        ```
    4. Führen Sie über die Befehlszeile den folgenden Befehl aus: `dotnet msbuild`.  
    5. Aufgrund der oben aufgeführten Änderungen müssen Sie die Fehler danach möglicherweise dennoch manuell beheben.  In vielen Fällen werden diese Fehler auch von IntelliSense in Visual Studio oder Visual Studio Code gemeldet.
        - Öffnen Sie den Stammordner des Projekts oder die entsprechende Projektmappe in Visual Studio 2019 oder Visual Studio Code.
        - Nachdem Sie eine QS-Datei im Editor geöffnet haben, sollte im Ausgabefenster die Ausgabe der Q#-Spracherweiterung angezeigt werden.
        - Öffnen Sie nach dem erfolgreichen Laden des Projekts (im Ausgabefenster angegeben) jede Datei, um alle verbleibenden Probleme manuell zu beheben.

> [!NOTE]
> * Bei Version 0.6 unterstützt der im Quantum Development Kit enthaltene Sprachserver nur einen Arbeitsbereich.
> * Öffnen Sie den Stammordner, der das Projekt selbst und alle verwiesene Projekte enthält, um mit einem Projekt in Visual Studio Code arbeiten zu können.   
> * Damit Sie mit einer Projektmappe in Visual Studio arbeiten können, müssen sich alle in der Projektmappe enthaltenen Projekte im selben Ordner wie die Projektmappe oder in einem ihrer Unterordner befinden.  
> * Verweise zwischen Projekten, die zu Version 0.6 oder höher migriert wurden, und Projekte, die ältere Paketversionen verwenden, werden **nicht** unterstützt.

## <a name="version-051904"></a>Version 0.5.1904

*Veröffentlichungsdatum: 15. April 2019*

Dieses Release enthält Fehlerbehebungen.


## <a name="version-051903"></a>Version 0.5.1903

*Veröffentlichungsdatum: 27. März 2019*

Dieses Release enthält Folgendes:

- Unterstützung für Jupyter Notebook und somit einer hervorragenden Möglichkeit, sich mit Q# vertraut zu machen.  [Sehen Sie sich die neuen Jupyter Notebook-Beispiele an, und lernen Sie, wie Sie eigene Notebooks schreiben](xref:microsoft.quantum.install). 

- Hinzufügen der ganzzahligen Addiererarithmetik zur Quantum Canon-Bibliothek.  Befassen Sie sich mit einem Jupyter Notebook, in dem [beschrieben wird, wie die neuen ganzzahligen Addierer verwendet werden](https://github.com/microsoft/Quantum/blob/master/samples/arithmetic/AdderExample.ipynb).

- Problembehebung für das von der Community gemeldete DumpRegister-Issue ([#148](https://github.com/Microsoft/Quantum/issues/148))

- Möglichkeit, innerhalb einer [using-Anweisung](xref:microsoft.quantum.language.statements) zurückzukehren

- überarbeiteter [Leitfaden zu den ersten Schritten](xref:microsoft.quantum.install)


## <a name="version-051902"></a>Version 0.5.1902

*Veröffentlichungsdatum: 27. Februar 2019*

Dieses Release enthält Folgendes:

- Es wurde die Unterstützung für einen plattformübergreifenden Python-Host hinzugefügt.  Das `qsharp`-Paket für Python vereinfacht das Simulieren von Q#-Vorgängen und -Funktionen in Python. Hier finden Sie weitere Informationen zur [Python-Interoperabilität](xref:microsoft.quantum.install). 

- Die Visual Studio- und Visual Studio Code-Erweiterungen unterstützen jetzt das Umbenennen von Symbolen (z. B. Funktionen und Vorgänge).

- Die Visual Studio-Erweiterung kann jetzt in Visual Studio 2019 installiert werden.

## <a name="version-041901"></a>Version 0.4.1901

*Veröffentlichungsdatum: 30. Januar 2019*

Dieses Release enthält Folgendes:

- Unterstützung für den neuen primitiven Typ „BigInt“, der eine ganze Zahl mit Vorzeichen beliebiger Größe darstellt.  Weitere Informationen zum [BigInt-Typ](xref:microsoft.quantum.language.type-model) finden Sie hier.
- neuer spezieller und schneller Toffoli-Simulator, mit dem X-, CNOT- und mehrfach gesteuerte X-Quantenvorgänge mit einer großen Anzahl von Qubits simuliert werden können.  Weitere Informationen zum [Toffoli-Simulator](xref:microsoft.quantum.machines.toffoli-simulator) finden Sie hier.
- einfache Ressourcenschätzung zum Schätzen der erforderlichen Ressourcen für das Ausführen einer bestimmten Instanz eines Q#-Vorgangs auf einem Quantencomputer.  Weitere Informationen zur [Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator) finden Sie hier.


## <a name="version-0318112802"></a>Version 0.3.1811.2802

*Veröffentlichungsdatum: 28. November 2018*

Obwohl diese Version bei der Visual Studio Code-Erweiterung nicht verwendet wurde, wurde sie gekennzeichnet und im Rahmen der [Bereinigung der Erweiterungen](https://code.visualstudio.com/blogs/2018/11/26/event-stream) im Zusammenhang mit dem NPM-Paket `event-stream` aus dem Marketplace entfernt. Diese Version entfernt alle Runtimeabhängigkeiten, die dazu führen könnten, dass die Erweiterung rote Flags auslöst.

Wenn Sie die Erweiterung zuvor installiert haben, müssen Sie sie noch mal installieren, indem Sie im Visual Studio Marketplace die [Microsoft Quantum Development Kit for Visual Studio Code](vscode:extension/quantum.quantum-devkit-vscode)-Erweiterung aufrufen und auf „Installieren“ klicken. Wir entschuldigen uns für die Unannehmlichkeiten.


## <a name="version-0318111511"></a>Version 0.3.1811.1511

*Veröffentlichungsdatum: 20. November 2018*

Mit diesem Release wird ein Fehler behoben, der verhindert hat, dass einige Benutzer die Visual Studio-Erweiterung erfolgreich herunterladen können.

Für den Fall, dass Sie ein Upgrade von Version 0.2 des Quantum Development Kit auf eine andere Version durchführen, erhalten Sie unter [Q#-Sprachänderungen und Migrieren des Q#Programms](xref:microsoft.quantum.relnotes.migration-0-3) weitere Informationen.

## <a name="version-031811203"></a>Version 0.3.1811.203

*Veröffentlichungsdatum: 2. November 2018*

Dieses Release enthält unter anderem folgende Fehlerbehebungen:

* Durch das Aufrufen von `DumpMachine` kann der Zustand des Simulators in bestimmten Situationen geändert werden.
* Beim Entwickeln von Projekten mithilfe einer Version von .NET Core (vor Version 2.1.403) wurden Warnungen zur Kompilierzeit entfernt.
* Die Dokumentation wurde besonders hinsichtlich der QuickInfos überarbeitet, die während des Bewegens des Mauszeigers in Visual Studio Code oder Visual Studio angezeigt werden.

Für den Fall, dass Sie ein Upgrade von Version 0.2 des Quantum Development Kit auf eine andere Version durchführen, erhalten Sie unter [Q#-Sprachänderungen und Migrieren des Q#Programms](xref:microsoft.quantum.relnotes.migration-0-3) weitere Informationen.

## <a name="version-0318102508"></a>Version 0.3.1810.2508

*Veröffentlichungsdatum: 29. Oktober 2018*

Dieses Release enthält neue Sprachfeatures und bietet eine verbesserte Entwicklerumgebung:

* Dieses Release enthält einen Sprachserver für Q# sowie die Clientintegrationen für Visual Studio und Visual Studio Code. Dies ermöglicht die Nutzung einer ganzen Reihe neuer IntelliSense-Features sowie Livefeedback beim Schreiben in Form von gewellten Unterstreichungen von Fehlern und Warnungen. 
* Durch die einfache Navigation zu und präzise Bereiche für Diagnosen sowie zusätzliche Details in den angezeigten Informationsfeldern werden die Diagnosemeldungen mit diesem Update im Allgemeinen verbessert.
* Die Q#-Sprache wurde so erweitert, dass die Art und Weise, wie Entwickler zum Ausdruck eines leistungsstarken Cloudcomputings häufige Vorgänge durchführen und Verbesserungen an den Sprachfeatures vornehmen können, einheitlich ist.  In diesem Release gibt es einige wichtige Änderungen an der Q#-Sprache.   

Weitere Informationen hierzu erhalten Sie unter [Q#-Sprachänderungen und Migrieren des Q#Programms](xref:microsoft.quantum.relnotes.migration-0-3).

Dieses Release umfasst auch eine neue Quantum Chemistry Library (Quantenchemiebibliothek):

* Die Chemiebibliothek enthält neue Hamilton-Simulationsfeatures einschließlich der folgenden:
    - Trotter-Suzuki-Integratoren in beliebiger, gleichmäßiger Reihenfolge für verbesserte Simulationsgenauigkeit
    - Qubit-Simulationstechnik mit chemiespezifischen Optimierungen zum Reduzieren der Komplexität des $T$-Gates
* neu eingeführtes Open-Source-Schema namens Broombridge-Schema (bezugnehmend auf ein als Geburtsort der Hamiltonians gefeiertes [Wahrzeichen](https://en.wikipedia.org/wiki/Broom_Bridge)) zum Importieren von Darstellungen von Molekülen und deren Simulation
* mehrere mithilfe des Broombridge-Schemas definierte chemische Darstellungen.  Diese Modelle wurden von [NWChem](http://www.nwchem-sw.org/), einem leistungsstarken Open-Source-Tool für computergestützte Chemie, generiert.
* Tutorials und Beispiele zur Erklärung der Verwendung der Chemiebibliothek und der Broombridge-Datenmodelle für Folgendes:
    - Konstruieren einfacher Hamilton-Funktionen mithilfe der Chemiebibliothek
    - Visualisieren des Bodens und angeregter Energiezustände von Lithiumhybrid mithilfe der Phasenschätzung
    - Ausführen von Ressourcenschätzungen der Quantenchemiesimulation
    - Schätzen des Energieniveaus von Molekülen, die vom Broombridge-Schema dargestellt werden
* Dokumentation zur Verwendung von NWChem zum Generieren zusätzlicher chemischer Modelle für Quantensimulationen mit Q#

Hier erhalten Sie weitere Informationen zur [Quantum Development Kit-Chemiebibliothek](xref:microsoft.quantum.chemistry.concepts.intro).

Mit der neuen Chemiebibliothek verschieben wir die Bibliotheken in das neue GitHub-Repository [Microsoft/QuantumLibraries](https://github.com/Microsoft/QuantumLibraries).  Die Beispiele befinden sich im Repository [Microsoft/Quantum](https://github.com/Microsoft/Quantum).  Wir freuen uns über Beiträge zu beiden Repositorys.

Dieses Release enthält Fehlerbehebungen und Features zu Problemen, die von der Community gemeldet wurden:

* IntelliSense für Q#? ([UserVoice](https://quantum.uservoice.com/forums/906943/suggestions/32656918))
* QS-Dateien ([UserVoice](https://quantum.uservoice.com/forums/906097/suggestions/32593049))
* Verbesserung der Fehlermeldung bei abgekürzten geschweiften Klammern in if-Anweisungen ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/34718518))
* Unterstützung der Tupeldekonstruktion bei veränderlicher (nochmaliger) Bindung ([UserVoice](https://quantum.uservoice.com/forums/906208/suggestions/35020444))
* Fehler bei Ausführung des bereitgestellten Beispiels „BitFlipCode“ ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546))
* H2SimulationGUI zeigt manchmal große Spitzen an ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34668370)).

### <a name="community-contributions"></a>Beiträge der Community

**Besonderer Dank** gilt den folgenden Mitwirkenden an der offenen Codebasis unter http://github.com/Microsoft/Quantum. Diese Beiträge ergänzen die umfangreichen Beispiele von Q#-Code:

* Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)): verbesserte die Benutzerfreundlichkeit für QASM/Q#-Entwickler, indem er einen Konvertierer von QASM zu Q# erstellt hat. [PR #58](https://github.com/Microsoft/Quantum/pull/58).

* Andrew Helwer ([@ahelwer](https://github.com/ahelwer)):  implementierte das CHSH-Spiel als Beispiel. Dies ist ein Quantenspiel zur Nichtlokalität.  [PR #84](https://github.com/Microsoft/Quantum/pull/84).

Außerdem danken wir Rohit Gupta ([@guptarohit](https://github.com/guptarohit),[PR #90](https://github.com/Microsoft/quantum/pull/90)), Tanaka Takayoshi ([@tanaka-takayoshi](https://github.com/tanaka-takayoshi),[PR #289](https://github.com/MicrosoftDocs/quantum-docs-pr/pull/289)) und Lee James O'Riordan ([@mlxd](https://github.com/mlxd),[PR #96](https://github.com/Microsoft/Quantum/pull/96)) für ihre Beiträge zur Verbesserung der Inhalte durch Korrekturen an der Dokumentation, Rechtschreibung und Tippfehlern. 

## <a name="version-021809701"></a>Version 0.2.1809.701

*Veröffentlichungsdatum: 10. September 2018*

Dieses Release enthält Fehlerbehebungen zu Problemen, die von der Community gemeldet wurden. Zu diesen Problemen gehören:

* Schiebeoperator kann nicht verwendet werden ([GitHub](https://github.com/Microsoft/Quantum/issues/75)).
* `DumpMachine` / `DumpRegister` schlägt bei der Ausgabe in der Konsole für `QCTraceSimulator` fehl ([UserVoice](https://quantum.uservoice.com/forums/906946/suggestions/34709680)).
* Zulassen der Zuweisung von 0 Qubits ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34768069-allow-allocating-0-qubits)).
* `AssertQubitState` erfordert expliziten Aufruf von „Complex()“ ([UserVoice](https://quantum.uservoice.com/forums/906208-q-language/suggestions/34713733-assertqubitstate-requires-explicit-complex-call)).
* `Measure`-Vorgang gibt unter macOS immer `One` zurück ([UserVoice](https://quantum.uservoice.com/forums/906940/suggestions/35008546)).

Vielen Dank! 

## <a name="version-0218063001"></a>Version 0.2.1806.3001

*Veröffentlichungsdatum: 30. Juni 2018*

Dieses Release umfasst lediglich eine schnelle Behebung von [Problem #48 auf GitHub](https://github.com/Microsoft/Quantum/issues/48) (Q#-Kompilierung schlägt fehl, wenn der Benutzername ein Leerzeichen enthält). Für die entsprechende neue Version `0.2.1806.3001-preview` gelten dieselben Updateanweisungen wie für Version `0.2.1806.1503`.

## <a name="version-0218061503"></a>Version 0.2.1806.1503

*Veröffentlichungsdatum: 22. Juni 2018*

Dieses Release enthält mehrere Beiträge der Community sowie eine verbesserte Debugfunktionen und Leistungsverbesserungen.  Dies gilt insbesondere in folgenden Fällen:

* Leistungsverbesserungen für kleine und große Simulationen für den QuantumSimulator-Zielcomputer
* Verbesserte Debugfunktionen
* Communitybeiträge zu Problembehebungen, Hilfsfunktionen, Vorgängen und neue Beispiele

### <a name="performance-improvements"></a>Leistungsverbesserungen

Dieses Update umfasst bedeutende Leistungsverbesserungen für die Simulation einer kleinen oder großen Anzahl von Qubits für alle Zielcomputer.  Diese Verbesserung ist bei der H<sub>2</sub>-Simulation besonders sichtbar. Dies ist ein Standardbeispiel im Quantum Development Kit.

### <a name="improved-debugging-functionality"></a>Verbesserte Debugfunktionen

In diesem Update wurden neue Debugfunktionen hinzugefügt:
* Die zwei neuen Vorgänge @"microsoft.quantum.extensions.diagnostics.dumpmachine" und @"microsoft.quantum.extensions.diagnostics.dumpregister" wurden hinzugefügt, die Wave-Funktionsinformationen über den Zielquantencomputer zu einem bestimmten Zeitpunkt zurückgeben.  
* Die Wahrscheinlichkeit zum Messen von $\ket{1}$ für ein einzelnes Qubit wird in Visual Studio nun automatisch im Debugfenster für den QuantumSimulator-Zielcomputer angezeigt.
* In Visual Studio wurde die Anzeige von Variableneigenschaften in den Debugfenstern **Auto** und **Lokal** verbessert. 

Erfahren Sie mehr über das [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging).

### <a name="community-contributions"></a>Beiträge der Community

Die Programmierercommunity für Q# wächst stetig, und wir freuen uns über die ersten Bibliotheken und Beispiele, die Benutzer zu unserer öffentlichen Codebasis unter http://github.com/Microsoft/quantum beitragen.  **Vielen Dank** an die folgenden Mitwirkenden:
* Mathias Soeken ([@msoeken](https://github.com/msoeken)) hat ein Beispiel zum Definieren einer transformationsbasierter Logiksynthesemethode beigesteuert, die Toffoli-Netzwerke zum Implementieren einer gegebenen Permutation erstellt. Der gesamte Code wurde in Q#-Funktionen und -Vorgängen geschrieben.  [PR #41](https://github.com/Microsoft/Quantum/pull/41).
* Rolf Huisman ([@RolfHuisman](https://github.com/RolfHuisman)), Microsoft MVP, hat ein Beispiel beigetragen, das zweckgemäßen QASM-Code aus Q#-Code für eingeschränkte Programmklassen erstellt, für die keine herkömmliche Ablaufsteuerung und eingeschränkte Quantenvorgänge vorliegen. [PR #59](https://github.com/Microsoft/Quantum/pull/59).
* Sarah Kasier ([@crazy4pi314](https://github.com/crazy4pi314)) verbesserte unsere Codebasis mit einer Bibliotheksfunktion für gesteuerte Vorgänge. [PR #53](https://github.com/Microsoft/Quantum/pull/53).
* Jessica Lemieux ([@Lemj3111](https://github.com/Lemj3111)) behob @"microsoft.quantum.canon.quantumphaseestimation" und erstellte neue Komponententests.  [PR #54](https://github.com/Microsoft/Quantum/pull/54).
* Tama McGlinn ([@TamaHobbit](https://github.com/TamaHobbit)) bereinigte das Beispiel „Teleportation“, indem sichergestellt wird, dass die QuantumSimulator-Instanz verworfen wird. [PR #20](https://github.com/Microsoft/Quantum/pull/20).

Außerdem **danken** wir den folgenden mitwirkenden Microsoft Software Engineers des Commercial Engineering Services-Teams, die während ihres Hackathons wertvolle Änderungen an unserer Dokumentation vorgenommen haben.  Ihre Änderungen sorgten für deutliche Verbesserungen an der Verständlichkeit und dem Onboarding für uns alle:
* Sascha Corti
* Mihaela Curmei
* John Donnelly
* Kirill Logachev
* Jan Pospisil
* Anita Ramanan
* Frances Tibble
* Alessandro Vozza

### <a name="update-existing-projects"></a>Update für vorhandene Projekte

Dieses Release ist vollständig abwärtskompatibel. Sie können einfach Updates für die NuGet-Pakete in Ihren Projekten auf Version `0.2.1806.1503-preview` und eine **vollständige Neuerstellung** durchführen, um sicherzustellen, dass alle Zwischendateien wiederhergestellt werden.

Befolgen Sie die normalen Anweisungen zum Durchführen eines [Paketupdates](https://docs.microsoft.com/nuget/tools/package-manager-ui#updating-a-package) über Visual Studio.

Führen Sie den folgenden Befehl aus, um Updates für Projektvorlagen über die Befehlszeile durchzuführen.
```
dotnet new -i "Microsoft.Quantum.ProjectTemplates::0.2.1806.1503-preview"
```

Nachdem Sie diesen Befehl ausgeführt haben, nutzen alle neuen Projekte, die mithilfe von `dotnet new <project-type> -lang Q#` erstellt werden, automatisch diese Version des Quantum Development Kit.

Führen Sie den folgenden Befehl innerhalb des Verzeichnisses eines jeweiligen Projekts aus, um ein Update für ein vorhandenes Projekt durchzuführen, damit es die neueste Version nutzt:

```
dotnet add package Microsoft.Quantum.Development.Kit -v "0.2.1806.1503-preview"
dotnet add package Microsoft.Quantum.Canon -v "0.2.1806.1503-preview"
```

Wenn ein vorhandenes Projekt auch die XUnit-Integration für Komponententests verwenden, kann ein ähnlicher Befehl auch zum Durchführen eines Updates für dieses Paket verwendet werden.
```
dotnet add package Microsoft.Quantum.Xunit -v "0.2.1806.1503-preview"
```

Je nachdem, welche Version von XUnit in Ihrem Testprojekt verwendet wird, müssen Sie möglicherweise ein Update auf XUnit 2.3.1 durchführen:
```
dotnet add package xunit -v "2.3.1" 
```

Stellen Sie nach dem Update sicher, dass Sie alle temporären Dateien entfernen, die von der vorherigen Version erstellt wurden, indem Sie folgenden Befehl ausführen:
```
dotnet clean 
```

### <a name="known-issues"></a>Bekannte Probleme

Es sind keine weiteren Probleme bekannt.


## <a name="version-0218022202"></a>Version 0.2.1802.2202

*Veröffentlichungsdatum: 26. Februar 2018*

In diesem Release wurde Unterstützung für die Entwicklung auf mehr Plattformen, die Interoperabilität von Sprachen sowie Leistungsverbesserungen eingeführt. Dies gilt insbesondere in folgenden Fällen:

- Unterstützung für die Entwicklung basierend auf macOS und Linux 
- .NET Core-Kompatibilität, einschließlich plattformübergreifender Unterstützung von Visual Studio Code
- eine vollständige Open-Source-Lizenz für Bibliotheken des Quantum Development Kit
- Verbesserung der Simulatorleistung bei Projekten mit 20 oder mehr Qubits
- Interoperabilität mit der Programmiersprache Python (Preview Release für Windows ist verfügbar)

### <a name="net-editions"></a>.NET-Editionen

Die .NET-Plattform ist in zwei verschiedenen Editionen verfügbar. Das mit Windows bereitgestellte .NET Framework und die Open-Source-Plattform .NET Core, die unter Windows, macOS und Linux verfügbar ist.
In diesem Release werden die meisten Bestandteile des Quantum Development Kit als Bibliotheken für .NET Standard bereitgestellt, was die Klassen umfasst, die .NET Framework und .NET Core gemein haben.
Diese Bibliotheken sind daher mit den aktuellen Versionen von .NET Framework und .NET Core kompatibel.

Damit also sichergestellt werden kann, dass mithilfe des Quantum Development Kit geschriebene Projekte möglichst portabel sind, wird empfohlen, mit dem Quantum Development Kit geschriebene Bibliotheksprojekte für .NET Standard zu schreiben, während Konsolenanwendungen für .NET Core geschrieben werden.
Da die vorherigen Releases des Quantum Development Kit nur .NET Framework unterstützt haben, müssen Sie Ihre vorhandenen Projekte möglicherweise migrieren. Weitere Informationen hierzu finden Sie unten.

### <a name="project-migration"></a>Projektmigration

Projekte, die mit vorherigen Versionen des Quantum Development Kit erstellt wurden, funktionieren weiterhin, solange Sie keine Updates für die enthaltenen NuGet-Pakete durchführen. Führen Sie die folgenden Schritte durch, um vorhandenen Code zur neuen Version zu migrieren:
1. Erstellen Sie ein neues .NET Core-Projekt mithilfe des entsprechenden Q#-Projektvorlagentyps (Anwendung, Bibliothek oder Testprojekt).
2. Kopieren Sie vorhandene QS- und CS/FS-Dateien aus dem alten Projekt in das neue Projekt (über „Hinzufügen > Vorhandenes Element“). Kopieren Sie nicht die Datei „AssemblyInfo.cs“.
3. Erstellen Sie das Projekt, und führen Sie es aus.

Beachten Sie, dass der Vorgang „RandomWalkPhaseEstimation“ aus dem Namespace „Microsoft.Quantum.Canon“ in den Namespace „Microsoft.Research.Quantum.RandomWalkPhaseEstimation“ im Repository [Microsoft/Quantum-NC](https://github.com/microsoft/quantum-nc) verschoben wurde.

### <a name="known-issues"></a>Bekannte Probleme

- Die `--filter`-Option für `dotnet test` funktioniert für in Q# geschriebene Tests nicht ordnungsgemäß.
  Daher können individuelle Komponententests nicht in Visual Studio Code ausgeführt werden. Stattdessen wird empfohlen, `dotnet test` in der Befehlszeile zu verwenden, um alle Tests noch mal auszuführen.

## <a name="version-0118011707"></a>Version 0.1.1801.1707

*Veröffentlichungsdatum: 18. Januar 2018*

In diesem Release wurden einige Probleme behoben, die von der Community gemeldet wurden. Die folgenden Probleme wurden behoben:

- Der Simulator funktioniert nun mit altem CPUs, die nicht AVX-fähig sind.
- Regionale Dezimaleinstellungen führen nicht mehr zu einem Fehler beim Q#-Parser.
- Der primitive Vorgang `SignD` gibt nun `Int` anstelle von `Double` zurück.


## <a name="version-011712901"></a>Version 0.1.1712.901

*Veröffentlichungsdatum: 11. Dezember 2017*

### <a name="known-issues"></a>Bekannte Probleme

#### <a name="hardware-and-software-requirements"></a>Hardware- und Softwareanforderungen

- Die Ausführung des im Quantum Development Kit enthaltenen Simulators erfordert eine 64-Bit-Installation von Windows.
- Der Quantensimulator von Microsoft, der mit dem Quantum Development Kit installiert wird, nutzt AVX (Advanced Vector Extensions) und erfordert eine AVX-fähige CPU. Im ersten Quartal von 2011 ausgelieferte Intel-Prozessoren („Sandy Bridge“) oder höher unterstützen AVX. Die Unterstützung früherer CPUs wird noch ausgewertet. Weitere Informationen werden möglicherweise noch angekündigt.

#### <a name="project-creation"></a>Projekterstellung

- Beim Erstellen einer Projektmappe (.sln), die Q# nutzt, muss sich die Projektmappe in einem den in der Projektmappe enthaltenen Projekte (.csproj) übergeordnetem Verzeichnis befinden. Beim Erstellen einer neuen Projektmappe können Sie dies sicherstellen, indem Sie sich vergewissern, dass das Kontrollkästchen „Projektmappenverzeichnis erstellen“ im Dialogfeld „Neues Projekt“ aktiviert ist. Wenn das nicht der Fall ist, müssen die NuGet-Pakete für das Quantum Development Kit manuell installiert werden.

#### <a name="q"></a>Q#

- IntelliSense zeigt keine richtigen Fehler für Q#-Code an. Stellen Sie sicher, dass Sie Buildfehler in der Visual Studio-Fehlerliste anzeigen, um die richtigen Q#-Fehler zu sehen. Beachten Sie außerdem, dass Q#-Fehler nicht angezeigt werden, bevor der Buildvorgang abgeschlossen wurde.
- Die Verwendung eines veränderlichen Arrays in einer Teilanwendung kann zu unerwartetem Verhalten führen.
- Die Bindung eines nicht veränderlichen Arrays an ein veränderliches Array (angenommen a = b, wobei „b“ ein veränderliches Array ist) kann zu unerwartetem Verhalten führen.
- Profilerstellung, Code Coverage und andere Visual Studio-Plug-Ins erkennen Q#-Zeilen und -Blöcke möglicherweise nicht genau.
- Der Q#-Compiler validiert interpolierte Zeichenfolgen nicht. Es ist möglich, C#-Kompilierungsfehler zu erstellen, indem Variablennamen falsch geschrieben oder Ausdrücke in interpolierten Q#-Zeichenfolgen verwendet werden.

#### <a name="simulation"></a>Simulation

- Der Quantensimulator nutzt OpenMP, um die lineare Algebra zu parallelisieren. OpenMP verwendet standardmäßig alle verfügbaren Hardwarethreads, weshalb Programme mit wenigen Qubits häufig langsam ausgeführt werden, stellt die Koordination die tatsächliche Arbeit in den Schatten. Dies kann behoben werden, indem eine kleine Zahl für die Umgebungsvariable OMP_NUM_THREADS festgelegt wird. Als grobe Faustregel gilt, dass 1 Thread für etwa 4 Qubits genügt und dann für jeden weiteren Qubit ein weiterer Thread benötigt wird. Dies hängt jedoch stark von Ihrem Algorithmus ab.

#### <a name="debugging"></a>Debuggen

- F11 (Einzelschritt) funktioniert in Q#-Code nicht.
- Die Codehervorhebung in Q#-Code an einem Breakpoint oder einer Einzelschrittpause ist manchmal ungenau. Es wird zwar die richtige Zeile hervorgehoben, jedoch werden Anfang und Ende manchmal an den falschen Spalten auf der Zeile hervorgehoben.

#### <a name="testing"></a>Testen

- Tests müssen im 64-Bit-Modus ausgeführt werden. Wenn Ihre Tests mit der Ausnahme „BadImageFormatException“ fehlschlagen, öffnen Sie das Testmenü, und klicken Sie auf „Testeinstellungen“ > Standardmäßige Prozessorarchitektur > X64“.
- Die Ausführung einiger Tests dauert länger (abhängig von Ihrem Computer bis zu 5 Minuten). Das ist normal, da einige mehr als 20 Qubits nutzen. Der größte Test nutzt aktuell 23 Qubits.

#### <a name="samples"></a>Beispiele

- Auf einigen Computern werden kleine Beispiele möglicherweise langsam ausgeführt, es sei denn, für die Umgebungsvariable OMP_NUM_THREADS ist der Wert „1“ festgelegt. Weitere Informationen finden Sie in der Anmerkung unter „Simulation“.

#### <a name="libraries"></a>Bibliotheken

- Es gibt eine implizite Annahme, dass die Qubits, die in verschiedenen Argumenten an einen Vorgang übergeben werden, sich voneinander unterscheiden. Beispielsweise gehen alle Bibliotheksvorgänge (und alle Simulatoren) davon aus, dass zwei Qubits, die an einen gesteuerten Vorgang übergeben werden, KEINE unterschiedlichen Qubits sind. Verstöße gegen diese Annahme können zu unvorhersehbarem und unerwartetem Verhalten führen. Es ist möglich, dies mithilfe des Quantenablaufverfolgungssimulators zu testen.
- Die Funktion „Microsoft.Quantum.Bind“ funktioniert in allen Fällen möglicherweise nicht erwartungsgemäß.
- Im Namespace „Microsoft.Quantum.Extensions.Math“ gibt die SignD-Funktion einen Double-Wert anstelle eines Int-Werts zurück, obwohl die zugrunde liegende Funktion „System.Math.Sign“ immer einen Integer zurückgibt. Das Ergebnis kann mit „1,0“, „-1,0“ und „0,0“ verglichen werden, da für diese Double-Werte exakte Binärdarstellungen vorliegen.
