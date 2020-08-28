---
title: Möglichkeiten zum Ausführen eines Q# Programms
description: Übersicht über die verschiedenen Möglichkeiten zum Ausführen von Q# Programmen. An der Eingabeaufforderung, Q# jupyter Notebooks und klassischen Host Programmen in Python oder einer .NET-Sprache.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: f1eca44dabd72cd107d72d3b9e3ad1081c19c27d
ms.sourcegitcommit: 11bd357baeb6ab53a402882979e75964d0869b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2020
ms.locfileid: "88992189"
---
# <a name="ways-to-run-a-no-locq-program"></a>Möglichkeiten zum Ausführen eines Q# Programms

Eines der größten Stärken des quantumentwicklungskit ist seine Flexibilität über Plattformen und Entwicklungsumgebungen hinweg.
Dies bedeutet jedoch auch, dass Q# sich neue Benutzer möglicherweise nicht mit den zahlreichen Optionen im [Installationshandbuch](xref:microsoft.quantum.install)verwechselt haben.
Auf dieser Seite erläutern wir, was geschieht, wenn ein Q# Programm ausgeführt wird, und vergleichen die verschiedenen Möglichkeiten, wie Benutzer dies tun können.

Ein primärer Unterschied besteht darin, dass Q# ausgeführt werden kann:
- als eigenständige Anwendung, bei Q# der die einzige beteiligte Sprache ist und das Programm direkt aufgerufen wird. Zwei Methoden fallen tatsächlich in diese Kategorie:
  - die Befehlszeilenschnittstelle
  - Q# Jupyter-Notebooks
- mit einem zusätzlichen *Host Programm*, das in Python oder einer .NET-Sprache (z. b. c# oder F #) geschrieben ist, die dann das Programm aufruft und die zurückgegebenen Ergebnisse weiterverarbeiten kann.

Um diese Prozesse und deren Unterschiede zu verstehen, wird ein einfaches Q# Programm angenommen, und es wird erläutert, wie es ausgeführt werden kann.

## <a name="basic-no-locq-program"></a>Einfaches Q# Programm

Ein grundlegendes Quantum-Programm besteht möglicherweise aus der Vorbereitung eines Qubit in derselben Superposition in den Zuständen $ \ket {0} $ und $ \ket {1} $, wobei es gemessen wird und das Ergebnis zurückgegeben wird. dabei wird entweder einer dieser beiden Zustände mit gleicher Wahrscheinlichkeit nach dem Zufallsprinzip verwendet.
Tatsächlich ist dieser Prozess der Kern des Schnellstarts des [Quantum-Zufallszahlen-Generators](xref:microsoft.quantum.quickstarts.qrng) .

In wird Q# dies durch den folgenden Code ausgeführt:

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

Dieser Code allein kann jedoch nicht von ausgeführt werden Q# .
Dafür muss der Text eines [Vorgangs](xref:microsoft.quantum.guide.basics#q-operations-and-functions), der dann ausgeführt wird, wenn er---direkt oder durch einen anderen Vorgang aufgerufen wird, ausgeführt werden. Daher können Sie einen Vorgang der folgenden Form schreiben:
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
Sie haben einen Vorgang definiert, `MeasureSuperposition` der keine Eingaben annimmt und einen Wert vom Typ [Result](xref:microsoft.quantum.guide.types)zurückgibt.

Obwohl die Beispiele auf dieser Seite nur aus Q# *Vorgängen*bestehen, werden alle Konzepte, die wir erörtern werden, gleichermaßen für Q# *Funktionen*verwendet. daher bezeichnen wir Sie zusammen als *callables*. Die Unterschiede werden in den [ Q# Grundlagen erläutert: Vorgänge und Funktionen](xref:microsoft.quantum.guide.basics#q-operations-and-functions)und weitere Details zur Definition finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).

### <a name="callable-defined-in-a-no-locq-file"></a>In einer Datei definierte Aufruf Bare Q# Datei

Die Aufruf Bare ist genau das, was von aufgerufen und ausgeführt wird Q# .
Allerdings sind einige weitere Ergänzungen erforderlich, um eine vollständige Datei zu bilden `*.qs` Q# .

Alle Q# Typen und callables (sowohl die, die Sie definieren, als auch die in der Sprache intrinsisch) werden innerhalb von *Namespaces*definiert, die jeweils einen vollständigen Namen bereitstellen, auf den dann verwiesen werden kann.

Beispielsweise werden die [`H`](xref:microsoft.quantum.intrinsic.h) [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) Vorgänge und in den [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) Namespaces und (Teil der [ Q# Standard Bibliotheken](xref:microsoft.quantum.qsharplibintro)) gefunden.
Daher können Sie immer über die *vollständigen* Namen und aufgerufen werden `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` . Dies führt jedoch zu einem sehr überlasteten Code.

Stattdessen `open` ermöglichen-Anweisungen, dass auf Aufruf Bare Elemente mit präziseren Kurzform verwiesen wird, wie dies im obigen Vorgangs Text geschehen ist.
Die vollständige Q# Datei, die den Vorgang enthält, besteht daher darin, einen eigenen Namespace zu definieren, die Namespaces für die von unserem Vorgang verwendeten callables zu öffnen, und dann den Vorgang:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> Namespaces können auch beim Öffnen einen *Alias* aufweisen. Dies kann hilfreich sein, wenn Aufruf Bare/Typnamen in zwei Namespaces in Konflikt stehen.
> Beispielsweise könnten wir stattdessen oben verwenden `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` und dann `H` via anrufen `NamespaceWithH.H(<qubit>)` .

> [!NOTE]
> Eine Ausnahme ist der [`Microsoft.Quantum.Core`](xref:microsoft.quantum.core) Namespace, der immer automatisch geöffnet wird.
> Daher können callables wie [`Length`](xref:microsoft.quantum.core.length) immer direkt verwendet werden.

### <a name="execution-on-target-machines"></a>Ausführung auf Ziel Computern

Nun wird das allgemeine Ausführungs Modell eines Q# Programms deutlich.

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

Zum einen hat die spezifische Aufruf Bare, die ausgeführt werden kann, Zugriff auf alle anderen callables und Typen, die im selben Namespace definiert sind.
Außerdem greift er auf die Bibliotheken aus einer der [ Q# Bibliotheken](xref:microsoft.quantum.libraries)zu, aber auf diese müssen entweder über den vollständigen Namen oder über die `open` oben beschriebenen Anweisungen verwiesen werden.

Die Aufruf Bare selbst wird dann auf einem *[Zielcomputer](xref:microsoft.quantum.machines)* ausgeführt.
Bei solchen Ziel Computern kann es sich um tatsächliche Quantum-Hardware oder mehrere Simulatoren handeln, die als Teil des QDK verfügbar sind.
Zu diesem Zweck ist der nützlichste Zielcomputer eine Instanz des [vollständigen Simulators](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , der das Verhalten des Programms so berechnet, als ob es auf einem Rausch freien Quantum-Computer ausgeführt würde.

Bisher haben wir beschrieben, was geschieht, wenn eine bestimmte Q# Aufruf Bare ausgeführt wird.
Unabhängig davon Q# , ob in einer eigenständigen Anwendung oder einem Host Programm verwendet wird, ist dieser allgemeine Prozess mehr oder weniger identisch---daher die Flexibilität des QDK.
Die Unterschiede zwischen den verschiedenen Methoden zum Aufrufen von Quantum Development Kit zeigen sich daher selbst, *wie* diese Aufruf Q# Bare aufgerufen wird und wie alle Ergebnisse zurückgegeben werden.
Genauer gesagt werden die Unterschiede im Zusammenhang mit 
1. die Angabe Q# , welche Aufruf Bare ausgeführt werden soll.
2. Gibt an, wie potenzielle Aufruf Bare Argumente bereitgestellt werden.
3. Angeben des Ziel Computers, auf dem der Computer ausgeführt werden soll, und
4. Gibt an, wie alle Ergebnisse zurückgegeben werden.

Zuerst wird erläutert, wie dies mit der Q# eigenständigen Anwendung an der Eingabeaufforderung erfolgt, und anschließend können Sie mit der Verwendung von Python-und c#-Host Programmen fortfahren.
Wir reservieren die eigenständige Anwendung von Q# jupyter-Notebooks für das letzte, da die primäre Funktionalität im Gegensatz zu den ersten drei nicht um eine lokale Datei zentriert ist Q# .

> [!NOTE]
> Obwohl wir dies in diesen Beispielen nicht veranschaulichen, besteht eine Gemeinsamkeit zwischen den Ausführungsmethoden darin, dass alle Nachrichten, die aus dem Programm gedruckt werden (z. b. über Q# [`Message`](xref:microsoft.quantum.intrinsic.message) oder [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), in der Regel immer an die jeweilige Konsole ausgegeben werden.

## <a name="no-locq-from-the-command-prompt"></a>Q# an der Eingabeaufforderung
Eine der einfachsten Möglichkeiten, Programme zu schreiben Q# , besteht darin, die Gedanken über separate Dateien und eine zweite Sprache vollständig zu vermeiden.
Die Verwendung von Visual Studio Code oder Visual Studio mit der QDK-Erweiterung ermöglicht einen nahtlosen Workflow, bei dem Q# nur callables aus einer einzelnen Q# Datei ausgeführt werden.

Hierzu wird die Ausführung des Programms letztendlich aufgerufen, indem Sie Folgendes eingeben:
```dotnetcli
dotnet run
```
an der Eingabeaufforderung ein.
Der einfachste Workflow ist, wenn der Verzeichnis Speicherort des Terminals mit der Datei identisch ist Q# , die mit Q# der Dateibearbeitung problemlos über das integrierte Terminal in vs Code behandelt werden kann, z. b..
Der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) akzeptiert jedoch zahlreiche Optionen, und das Programm kann auch an einem anderen Speicherort ausgeführt werden, indem einfach `--project <PATH>` der Speicherort der Datei bereitgestellt wird Q# .


### <a name="add-entry-point-to-no-locq-file"></a>Einstiegspunkt zu Datei hinzufügen Q#

Die meisten Q# Dateien enthalten mehr als eine Aufruf Bare Funktion. Daher müssen wir dem Compiler natürlich mitteilen, *welche* Callable beim Bereitstellen des Befehls ausgeführt werden soll `dotnet run` .
Dies erfolgt mit einer einfachen Änderung an der Q# Datei selbst: 
    - Fügen Sie eine Zeile hinzu, `@EntryPoint()` die direkt vor dem Aufruf baren steht.

Unsere Datei von oben wird daher
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

Nun `dotnet run` führt ein-Befehl von der Eingabeaufforderung aus `MeasureSuperposition` , und der zurückgegebene Wert wird dann direkt in das Terminal gedruckt.
Daher wird entweder `One` oder `Zero` gedruckt angezeigt. 

Beachten Sie, dass es keine Rolle spielt, ob weitere Aufruf Bare aufruben definiert sind, sondern nur `MeasureSuperposition` ausgeführt wird.
Außerdem ist es kein Problem, wenn die Aufruf Bare-Datei vor der Deklaration [Dokumentations Kommentare](xref:microsoft.quantum.guide.filestructure#documentation-comments) enthält `@EntryPoint()` .

### <a name="callable-arguments"></a>Aufruf Bare Argumente

Bisher haben wir nur einen Vorgang in Erwägung gezogen, der keine Eingaben annimmt.
Angenommen, wir wollten einen ähnlichen Vorgang durchführen, aber auf mehreren Qubits---die Zahl als Argument bereitgestellt.
Ein solcher Vorgang könnte als
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
Dabei ist der zurückgegebene Wert ein Array der Messergebnisse.
Beachten Sie, dass [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) und [`ForEach`](xref:microsoft.quantum.arrays.foreach) sich im [`Microsoft.Quantum.Canon`](xref:microsoft.quantum.canon) -Namespace und im- [`Microsoft.Quantum.Arrays`](xref:microsoft.quantum.arrays) Namespace befinden, `open` wobei jeweils zusätzliche Anweisungen erforderlich sind.

Wenn Sie das `@EntryPoint()` Attribut vor diesem neuen Vorgang verschieben (Beachten Sie, dass es nur eine Zeile in einer Datei geben kann), und wenn Sie versuchen, es mit einfach auszuführen, führt dies zu `dotnet run` einer Fehlermeldung, die angibt, welche zusätzlichen Befehlszeilenoptionen erforderlich sind, und wie Sie Sie Ausdrücken.

Das allgemeine Format für die Befehlszeile ist tatsächlich `dotnet run [options]` , und es werden Aufruf Bare Argumente dort bereitgestellt.
In diesem Fall fehlt das Argument `n` , und es wird angezeigt, dass die Option bereitgestellt werden muss `-n <n>` . Zum Ausführen `MeasureSuperpositionArray` von for `n=4` Qubits verwenden wir daher

```dotnetcli
dotnet run -n 4
```

Ausgabe ähnlich

```output
[Zero,One,One,One]
```

Dies reicht natürlich auf mehrere Argumente aus.

> [!NOTE]
> In definierte Argument Namen `camelCase` werden vom Compiler leicht geändert, damit Sie als Eingaben akzeptiert werden Q# . Wenn z. b. anstelle von `n` der oben genannte Name verwendet wird `numQubits` , wird diese Eingabe in der Befehlszeile über `--num-qubits 4` anstelle von bereitgestellt `-n 4` .

Die Fehlermeldung enthält auch weitere Optionen, die verwendet werden können, einschließlich Informationen zum Ändern des Ziel Computers.

### <a name="different-target-machines"></a>Verschiedene Zielcomputer

Da die Ausgaben unserer Vorgänge bisher die erwarteten Ergebnisse ihrer Aktion in echten Qubits waren, ist klar, dass der Standardziel Computer von der Befehlszeile aus der vollzustandsquantum-Simulator ist `QuantumSimulator` .
Wir können jedoch Aufruf Bare Aufrufe anweisen, die auf einem bestimmten Zielcomputer mit der Option `--simulator` (oder der kurzseite `-s` ) ausgeführt werden.

Beispielsweise können wir die Anwendung unter Ausführen [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

Die gedruckte Ausgabe lautet dann

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

Ausführliche Informationen dazu, was diese Metriken angeben, finden Sie unter [Ressourcenschätzung: gemeldete Metriken](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).

### <a name="command-line-execution-summary"></a>Zusammenfassung der Befehlszeilen Ausführung
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a>Nicht- Q# `dotnet run` Optionen

Wie bereits kurz erwähnt `--project` , akzeptiert der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) auch Optionen, die nicht mit den Q# Aufruf baren Argumenten verknüpft sind.
Wenn beide Arten von Optionen bereit `dotnet` gestellt werden, müssen zuerst die-spezifischen Optionen, gefolgt von einem Trennzeichen `--` , und dann die Q# -spezifischen Optionen bereitgestellt werden.
Beispielsweise würde die Angabe eines Pfads zusammen mit einer Zahlen-Qubits für den obigen Vorgang über ausgeführt werden `dotnet run --project <PATH> -- -n <n>` .

## <a name="no-locq-with-host-programs"></a>Q# mit Host Programmen

Mit unserer Q# Datei ist eine Alternative zum Aufrufen eines Vorgangs oder einer Funktion direkt über die Eingabeaufforderung die Verwendung eines *Host Programms* in einer anderen klassischen Sprache. Dies kann insbesondere mit Python oder einer .NET-Sprache (z. b. c# oder F #) erfolgen (aus Gründen der Kürze wird c# hier nur ausführlich erläutert).
Zum Aktivieren der Interoperabilität ist ein wenig mehr Setup erforderlich. diese Details finden Sie jedoch in den [Installations](xref:microsoft.quantum.install)Handbüchern.

Kurz gesagt, enthält die Situation nun eine Host Programmdatei (z. b. `*.py` oder `*.cs` ) am gleichen Speicherort wie die Q# Datei.
Es ist jetzt das *Host* Programm, das ausgeführt wird, und im Verlauf der Ausführung kann es bestimmte Q# Vorgänge und Funktionen aus der Datei abrufen Q# .
Der Kern der Interoperabilität basiert auf dem Compiler, der Q# den Inhalt der Q# Datei für das Host Programm zugänglich macht, sodass Sie aufgerufen werden können.

Einer der Hauptvorteile der Verwendung eines Host Programms besteht darin, dass die vom Programm zurückgegebenen klassischen Daten Q# dann in der Host Sprache weiterverarbeitet werden können.
Dies kann aus einer erweiterten Datenverarbeitung bestehen (z. b. etwas, das nicht intern in ausgeführt werden kann Q# ). Anschließend werden weitere Aktionen auf der Q# Grundlage dieser Ergebnisse aufgerufen, oder es kann etwas so einfach sein, wie die Ergebnisse gezeichnet werden Q# .

Das allgemeine Schema wird hier angezeigt, und wir erörtern die spezifischen Implementierungen für python und c# weiter unten. Ein Beispiel für die Verwendung eines F #-Host Programms finden Sie unter [.net-Interoperabilitäts Beispiele](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> Das `@EntryPoint()` für-Anwendungen verwendete Attribut Q# kann nicht mit Host Programmen verwendet werden.
> Wenn Sie in der Datei vorhanden ist Q# , die von einem Host aufgerufen wird, wird ein Fehler ausgelöst. 

Um mit unterschiedlichen Host Programmen arbeiten zu können, sind keine Änderungen an einer `*.qs` Q# Datei erforderlich.
Die folgenden Host Programm Implementierungen funktionieren alle mit derselben Q# Datei:

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

Wählen Sie die Registerkarte aus, die der gewünschten Host Sprache entspricht.

### <a name="python"></a>[Python](#tab/tabid-python)
Ein python-Host Programm wird wie folgt erstellt:
1. Importieren Sie das- `qsharp` Modul, mit dem das Modul Lade Modul für die Interoperabilität registriert wird Q# . 
    Dadurch Q# können Namespaces als Python-Module angezeigt werden, aus denen Sie Q# callables importieren können.
    Beachten Sie, dass es sich nicht um die Q# selbst importierbaren, sondern vielmehr um python-Stubdateien handelt, die das Aufrufen von Dateien ermöglichen.
    Diese werden dann als Objekte von python-Klassen verwendet, auf denen Methoden zum Angeben der Zielcomputer verwendet werden, an die der Vorgang zur Ausführung gesendet wird.

2. Importieren Sie diese Q# callables, die wir direkt aufrufen---in diesem Fall `MeasureSuperposition` und `MeasureSuperpositionArray` .
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    Wenn `qsharp` Sie das Modul importiert haben, können Sie auch callables direkt aus den Q# Bibliotheks Namespaces importieren.

3. Unter jedem anderen Python-Code können Sie jetzt diese callables auf bestimmten Ziel Computern aufrufen und ihre Rückgaben den Variablen (wenn Sie einen Wert zurückgeben) zur weiteren Verwendung zuweisen.

#### <a name="specifying-target-machines"></a>Angeben von Ziel Computern
Das Aufrufen eines Vorgangs, der auf einem bestimmten Zielcomputer ausgeführt werden soll, erfolgt über verschiedene python-Methoden auf dem importierten Objekt.
Beispielsweise `.simulate(<args>)` verwendet die `QuantumSimulator` zum Ausführen des Vorgangs, während `.estimate_resources(<args>)` dies in der erfolgt `ResourcesEstimator` .

#### <a name="passing-inputs-to-q"></a>Übergeben von Eingaben an Q\#
Argumente für die Q# Aufruf Bare-Datei sollten in Form eines Schlüsselwort Arguments bereitgestellt werden, wobei das-Schlüsselwort der Argument Name in der Q# Aufruf baren Definition ist.
Das heißt, `MeasureSuperpositionArray.simulate(n=4)` ist gültig, während `MeasureSuperpositionArray.simulate(4)` einen Fehler auslöst.

Daher ist das python-Host Programm 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

ergibt eine Ausgabe wie die folgende:

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a>Verwenden Q# von Code aus anderen Projekten oder Paketen

Standardmäßig lädt der `import qsharp` Befehl alle `.qs` Dateien im aktuellen Ordner und macht Ihre Q# Vorgänge und Funktionen für die Verwendung innerhalb des python-Skripts verfügbar.

Zum Laden Q# von Code aus einem anderen Ordner kann die [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) verwendet werden, um einen Verweis auf eine `.csproj` Datei für ein Q# Projekt (d. h. ein Projekt, das auf verweist) hinzuzufügen `Microsoft.Quantum.Sdk` .
Mit diesem Befehl werden alle `.qs` Dateien im Ordner kompiliert, die die `.csproj` und deren Unterordner enthalten. Außerdem werden alle Pakete rekursiv geladen `PackageReference` Q# `ProjectReference` , auf die über-oder-Projekte verwiesen wird `.csproj`

Der folgende Python-Code importiert z. b. ein externes Projekt, das auf seinen Pfad relativ zum aktuellen Ordner verweist und einen seiner Vorgänge aufruft Q# :

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

Dies führt zu einer Ausgabe wie der folgenden:

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

Q#Verwenden Sie die- [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages), um externe Pakete mit Code zu laden.

Wenn der Q# Code im aktuellen Ordner von externen Projekten oder Paketen abhängt, werden bei der Ausführung möglicherweise Fehler angezeigt `import qsharp` , da die Abhängigkeiten noch nicht geladen wurden.
Wenn Sie erforderliche externe Pakete oder Q# Projekte während des `import qsharp` Befehls laden möchten, stellen Sie sicher, dass der Ordner mit dem Python-Skript eine Datei enthält, auf `.csproj` die verweist `Microsoft.Quantum.Sdk` . Fügen Sie der-Eigenschaft die- `.csproj` Eigenschaft hinzu `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` . Dies weist Q# darauf hin, `ProjectReference` `PackageReference` dass `.csproj` während des Befehls rekursiv alle-oder-Elemente geladen werden `import qsharp` .

Hier ist beispielsweise eine einfache Datei, die `.csproj` bewirkt, dass Q# das Paket automatisch geladen wird `Microsoft.Quantum.Chemistry` :

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> Diese benutzerdefinierte `<IQSharpLoadAutomatically>` Eigenschaft ist derzeit für python-Hosts erforderlich. in Zukunft kann dies jedoch das Standardverhalten für eine Datei sein, die `.csproj` sich im gleichen Ordner wie das Python-Skript befindet.

> [!NOTE]
> Die `<QsharpCompile>` -Einstellung in `.csproj` wird derzeit von python-Hosts ignoriert, und alle `.qs` Dateien im-Ordner der `.csproj` (einschließlich der Unterordner) werden geladen und kompiliert. Die Unterstützung für `.csproj` Einstellungen wird in Zukunft verbessert (Weitere Informationen finden Sie unter [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) ).


### <a name="c"></a>[C#](#tab/tabid-csharp)

Ein c#-Host Programm verfügt über mehrere Komponenten, die eng mit einigen Komponenten des QDK funktionieren, z. b. die Simulatoren, die selbst auf c# basieren.

Der Q# Compiler arbeitet hier, indem er einen gleichwertig benannten c#-Namespace aus dem Q# Namespace in der Q# Datei erzeugt.
Außerdem wird eine gleichwertig benannte c#-Klasse für jede der Q# darin definierten callables oder Typen generiert.

Zuerst werden alle Klassen, die in unserem Host Programm verwendet werden, mit-Anweisungen zur Verfügung gestellt `using` , die ungefähr mit den `open` Anweisungen in der Datei zusammengefügt werden Q# :

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

Als nächstes deklarieren wir unseren c#-Namespace, einige andere Bits und Teile (siehe den vollständigen Codeblock unten) und dann eine beliebige klassische Programmierung (z. b. das Berechnen von Argumenten für die Q# callables).
Letzteres ist in diesem Fall nicht erforderlich, aber ein Beispiel für eine solche Verwendung finden Sie unter  [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet)Beispiel.

#### <a name="target-machines"></a>Zielcomputer

Bei der Rückkehr zu Q# müssen wir eine Instanz eines beliebigen Ziel Computers erstellen, auf dem wir unsere Vorgänge ausführen werden.

```csharp
            using var sim = new QuantumSimulator();
```

Die Verwendung anderer Zielcomputer ist so einfach wie das Instanziieren eines anderen Ziel Computers, obwohl die Art und Weise der Rückgabe geringfügig abweichen kann.
Aus Gründen der Kürze bleiben wir an der [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) für die Zeit und fügen die [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [folgenden](#including-the-resources-estimator)Informationen ein.

Jede aus den Vorgängen generierte c#-Klasse Q# verfügt über eine- `Run` Methode, wobei das erste Argument, das die Zielcomputer Instanz sein muss.
Daher `MeasureSuperposition` verwenden wir, um auf dem auszuführen `QuantumSimulator` `MeasureSuperposition.Run(sim)` .
Die zurückgegebenen Ergebnisse können dann Variablen in c# zugewiesen werden:

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> Die `Run` -Methode wird asynchron ausgeführt, da dies die Groß-und Kleinschreibung für echte Quantum-Hardware ist. Daher blockiert das- `await` Schlüsselwort die weitere Ausführung, bis die Aufgabe abgeschlossen ist.

Wenn die Q# Aufruf Bare-Datei keine Rückgaben aufweist (d. h. den Rückgabetyp aufweist `Unit` ), kann die Ausführung weiterhin auf dieselbe Weise erfolgen, ohne Sie einer Variablen zuzuweisen.
In diesem Fall würde die gesamte Zeile einfach aus 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a>Argumente

Alle Argumente für die Q# Aufruf baren werden einfach als zusätzliche Argumente an den Zielcomputer weitergeleitet.
Daher werden die Ergebnisse von `MeasureSuperpositionArray` in `n=4` Qubits über 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

Ein vollständiges c#-Host Programm könnte daher wie folgt aussehen.

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

Am Speicherort der c#-Datei kann das Host Programm von der Eingabeaufforderung aus ausgeführt werden, indem Sie Folgendes eingeben:
```dotnetcli
dotnet run
```
in diesem Fall wird die Ausgabe in die Konsole geschrieben, ähnlich wie 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> Aufgrund der Interoperabilität des Compilers mit Namespaces könnten wir unsere Q# callables ohne die-Anweisung verfügbar machen `using NamespaceName;` und den c#-Namespace Titel einfach zuordnen.
> Das heißt, indem durch ersetzt wird `namespace host` `namespace NamespaceName` .

#### <a name="including-the-resources-estimator"></a>Einschließen der Ressourcenschätzung

[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Erfordert eine etwas andere Implementierung zum Abrufen der Ausgabe.

Anstatt Sie als Variable mit einer-Anweisung zu instanziieren `using` (wie dies bei der der Fall ist `QuantumSimulator` ), können wir die Objekte der Klasse über

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

Beachten Sie, dass anstelle eines einzelnen Ziel Simulators, der von mehreren Vorgängen verwendet werden soll Q# , jeweils eine instanziiert wird. Dies liegt daran, dass die Objekte selbst geändert werden, wenn Sie als Zielcomputer verwendet werden, und ihre Ergebnisse anschließend mit der-Klassenmethode abgerufen werden können `.ToTSV()` .

Zum Ausführen der Vorgänge für die Ressourcenschätzung verwenden wir

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
und dann die Ergebnisse als durch Tabstopps getrennte Werte (TSV) mit `estimatorSingleQ.ToTSV()` und Abrufen `estimatorMultiQ.ToTSV()` .

Ein vollständiges c#-Host Programm, das sowohl den als auch den verwendet, könnte das folgende Format haben `QuantumSimulator` `ResourcesEstimator` :

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


Dies ergibt eine Ausgabe ähnlich der

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a>Q# Jupyter-Notebooks
Q# Jupyter-Notebooks verwenden den I Q# -Kernel, mit dem Sie callables in einem einzigen Notebook definieren, kompilieren und ausführen können, Q# ---alle neben Anweisungen, Notizen und anderem Inhalt.
Dies bedeutet, dass es zwar möglich ist, den Inhalt von Dateien zu importieren und zu verwenden `*.qs` Q# , aber im Ausführungs Modell nicht erforderlich sind.

Hier wird ausführlich erläutert, wie die Q# oben definierten Vorgänge ausgeführt werden, aber eine umfassendere Einführung in die Verwendung Q# von jupyter Notebooks finden Sie unter Einführung [in Q# und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).

### <a name="defining-operations"></a>Definieren von Vorgängen

In einem Q# Jupyter Notebook geben Sie den Q# Code genau so ein, wie er im Namespace einer Q# Datei gespeichert wird.

Daher können wir den Zugriff auf callables aus den [ Q# Standardbibliotheken](xref:microsoft.quantum.qsharplibintro) mit `open` Anweisungen für die jeweiligen Namespaces aktivieren.
Wenn eine Zelle mit einer solchen Anweisung ausgeführt wird, sind die Definitionen aus diesen Namespaces im gesamten Arbeitsbereich verfügbar.

> [!NOTE]
> Callables von [Microsoft. Quantum. intrinsisch](xref:microsoft.quantum.intrinsic) und [Microsoft. Quantum. Canon](xref:microsoft.quantum.canon) (z. b. [`H`](xref:microsoft.quantum.intrinsic.h) und [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) stehen automatisch für Vorgänge zur Verfügung, die in Zellen in Q# jupyter-Notebooks definiert sind.
> Dies gilt jedoch nicht für Code, der aus externen Q# Quelldateien eingefügt wurde (ein Prozess, der bei Einführung [zu Q# und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)angezeigt wird). 
> 

Ebenso erfordert die Definition von Vorgängen lediglich das Schreiben des Q# Codes und das Ausführen der Zelle.

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

In der Ausgabe werden dann diese Vorgänge aufgelistet, die aus zukünftigen Zellen aufgerufen werden können.

### <a name="target-machines"></a>Zielcomputer

Die Funktionen zum Ausführen von Vorgängen auf bestimmten Ziel Computern werden über [I Q# Magic-Befehle](xref:microsoft.quantum.guide.quickref.iqsharp)bereitgestellt.
Beispielsweise `%simulate` verwendet die `QuantumSimulator` , und `%estimate` verwendet Folgendes `ResourcesEstimator` :

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a>Übergeben von Eingaben an Funktionen und Vorgänge

Um Eingaben an die Vorgänge zu übergeben Q# , können die Argumente als `key=value` Paare an den Befehl für die Ausführung Magic übergeben werden.
Um also `MeasureSuperpositionArray` mit vier Qubits auszuführen, können wir Folgendes ausführen `%simulate MeasureSuperpositionArray n=4` :

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

Dieses Muster kann auf ähnliche Weise mit `%estimate` und anderen Ausführungs Befehlen verwendet werden.

### <a name="using-no-locq-code-from-other-projects-or-packages"></a>Verwenden Q# von Code aus anderen Projekten oder Paketen

Standardmäßig lädt eine Q# Jupyter Notebook alle `.qs` Dateien im aktuellen Ordner und macht Ihre Q# Vorgänge und Funktionen für die Verwendung im Notebook verfügbar. Der [ `%who` Magic-Befehl](xref:microsoft.quantum.iqsharp.magic-ref.who) listet alle zurzeit verfügbaren Q# Vorgänge und Funktionen auf.

Zum Laden Q# von Code aus einem anderen Ordner kann der [ `%project` Magic-Befehl](xref:microsoft.quantum.iqsharp.magic-ref.project) verwendet werden, um einen Verweis auf eine `.csproj` Datei für ein Q# Projekt (d. h. ein Projekt, das auf verweist) hinzuzufügen `Microsoft.Quantum.Sdk` . Mit diesem Befehl werden alle `.qs` Dateien im Ordner kompiliert, die die `.csproj` (und Unterordner) enthalten. Außerdem werden alle Pakete rekursiv geladen `PackageReference` Q# `ProjectReference` , auf die über-oder-Projekte verwiesen wird `.csproj` 

Beispielsweise simulieren die folgenden Zellen einen- Q# Vorgang aus einem externen Projekt, bei dem auf den Projektpfad relativ zum aktuellen Ordner verwiesen wird:

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

Q#Verwenden Sie den [ `%package` Magic-Befehl](xref:microsoft.quantum.iqsharp.magic-ref.package), um externe Pakete mit Code zu laden.
Durch das Laden eines Pakets werden auch alle benutzerdefinierten Magic-Befehle oder Anzeige Encoder verfügbar gemacht, die in Assemblys enthalten sind, die Teil des Pakets sind.

Stellen Sie zum Laden externer Pakete oder Q# Projekte bei der Notebook-Initialisierung sicher, dass der Notebook-Ordner eine Datei enthält, auf `.csproj` die verweist `Microsoft.Quantum.Sdk` . Fügen Sie der-Eigenschaft die- `.csproj` Eigenschaft hinzu `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` `<PropertyGroup>` . Dies weist Q# darauf hin, `ProjectReference` dass alle `PackageReference` Elemente in der `.csproj` Ladezeit des Notebooks rekursiv geladen werden.

Hier ist beispielsweise eine einfache Datei, die `.csproj` bewirkt, dass Q# das Paket automatisch geladen wird `Microsoft.Quantum.Chemistry` :

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> Diese benutzerdefinierte `<IQSharpLoadAutomatically>` Eigenschaft wird derzeit von Q# Jupyter Notebook Hosts benötigt, aber in Zukunft kann dies das Standardverhalten für eine Datei sein, die `.csproj` sich im selben Ordner wie die Notebook-Datei befindet.

> [!NOTE]
> Die `<QsharpCompile>` -Einstellung in `.csproj` wird derzeit von Q# Jupyter Notebook Hosts ignoriert, und alle `.qs` Dateien im-Ordner der `.csproj` (einschließlich der Unterordner) werden geladen und kompiliert. Die Unterstützung für `.csproj` Einstellungen wird in Zukunft verbessert (Weitere Informationen finden Sie unter [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) ).
