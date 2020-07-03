---
title: 'Möglichkeiten zum Ausführen eines Q #-Programms'
description: 'Übersicht über die verschiedenen Möglichkeiten zum Ausführen von Q #-Programmen. Über die Befehlszeile, Q # jupyter Notebooks und klassische Host Programme in Python oder einer .NET-Sprache.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
ms.openlocfilehash: 132c138d7c392ed2b4bd3d0079180b68adae4cfc
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85887683"
---
# <a name="ways-to-run-a-q-program"></a>Möglichkeiten zum Ausführen eines Q #-Programms

Eines der größten Stärken des quantumentwicklungskit ist seine Flexibilität über Plattformen und Entwicklungsumgebungen hinweg.
Dies bedeutet jedoch auch, dass neue Q #-Benutzer von den zahlreichen Optionen im [Installationshandbuch](xref:microsoft.quantum.install)möglicherweise verwirrt oder überlastet werden.
Auf dieser Seite erklären wir, was geschieht, wenn ein Q #-Programm ausgeführt wird, und vergleichen die verschiedenen Möglichkeiten, wie Benutzer dies tun können.

Ein primärer Unterschied besteht darin, dass Q # ausgeführt werden kann:
- als eigenständige Anwendung, bei der Q # die einzige beteiligte Sprache ist und das Programm direkt aufgerufen wird. Zwei Methoden fallen tatsächlich in diese Kategorie:
  - die Befehlszeilenschnittstelle
  - Jupyter Notebook-Instanzen in Q#
- mit einem zusätzlichen *Host Programm*, das in Python oder einer .NET-Sprache (z. b. c# oder F #) geschrieben ist, die dann das Programm aufruft und die zurückgegebenen Ergebnisse weiterverarbeiten kann.

Um diese Prozesse und deren Unterschiede zu verstehen, wird ein einfaches Q #-Programm berücksichtigt und die Art und Weise erläutert, wie Sie ausgeführt werden kann.

## <a name="basic-q-program"></a>Einfaches Q #-Programm

Ein grundlegendes Quantum-Programm besteht möglicherweise aus der Vorbereitung eines Qubit in derselben Superposition in den Zuständen $ \ket {0} $ und $ \ket {1} $, wobei es gemessen wird und das Ergebnis zurückgegeben wird. dabei wird entweder einer dieser beiden Zustände mit gleicher Wahrscheinlichkeit nach dem Zufallsprinzip verwendet.
Tatsächlich ist dieser Prozess der Kern des Schnellstarts des [Quantum-Zufallszahlen-Generators](xref:microsoft.quantum.quickstarts.qrng) .

In f # wird dies durch den folgenden Code durchgeführt:

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

Dieser Code allein kann jedoch nicht von Q # ausgeführt werden.
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

Obwohl die Beispiele auf dieser Seite nur aus q #- *Vorgängen*bestehen, werden alle Konzepte, die wir erörtern werden, gleichermaßen für die f #- *Funktionen*verwendet. daher bezeichnen wir Sie zusammen als *callables*. Die Unterschiede werden unter [Q # Basics: Vorgänge und Funktionen](xref:microsoft.quantum.guide.basics#q-operations-and-functions)erläutert. Weitere Informationen zur Definition finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).

### <a name="callable-defined-in-a-q-file"></a>In einer Q #-Datei definierte Aufruf Bare Datei

Die Aufruf Bare ist genau das, was von Q # aufgerufen und ausgeführt wird.
Allerdings sind einige weitere Ergänzungen erforderlich, um eine vollständige `*.qs` Q #-Datei zu bilden.

Alle Q #-Typen und callables (sowohl die, die Sie definieren, als auch die in der Sprache intrinsisch) werden innerhalb von *Namespaces*definiert, die jeweils einen vollständigen Namen bereitstellen, auf den dann verwiesen werden kann.

Beispielsweise befinden sich die [`H`](xref:microsoft.quantum.intrinsic.h) -und- [`MResetZ`](xref:microsoft.quantum.measurement.mresetz) Vorgänge im [`Microsoft.Quantum.Instrinsic`](xref:microsoft.quantum.intrinsic) - [`Microsoft.Quantum.Measurement`](xref:microsoft.quantum.measurement) Namespace und im-Namespace (Teil der [Q # Standard-Bibliotheken](xref:microsoft.quantum.qsharplibintro)).
Daher können Sie immer über die *vollständigen* Namen und aufgerufen werden `Microsoft.Quantum.Intrinsic.H(<qubit>)` `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` . Dies führt jedoch zu einem sehr überlasteten Code.

Stattdessen `open` ermöglichen-Anweisungen, dass auf Aufruf Bare Elemente mit präziseren Kurzform verwiesen wird, wie dies im obigen Vorgangs Text geschehen ist.
Die vollständige f #-Datei, die den Vorgang enthält, besteht daher darin, einen eigenen Namespace zu definieren, die Namespaces für die von unserem Vorgang verwendeten callables zu öffnen, und dann den Vorgang:

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

Nun wird das allgemeine Ausführungs Modell eines f #-Programms deutlich.

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

Zum einen hat die spezifische Aufruf Bare, die ausgeführt werden kann, Zugriff auf alle anderen callables und Typen, die im selben Namespace definiert sind.
Außerdem greifen Sie auf die Bibliotheken aus einer der [Q #-Bibliotheken](xref:microsoft.quantum.libraries)zu, aber auf diese muss entweder über den vollständigen Namen oder über die `open` oben beschriebenen Anweisungen verwiesen werden.

Die Aufruf Bare selbst wird dann auf einem *[Zielcomputer](xref:microsoft.quantum.machines)* ausgeführt.
Bei solchen Ziel Computern kann es sich um tatsächliche Quantum-Hardware oder mehrere Simulatoren handeln, die als Teil des QDK verfügbar sind.
Zu diesem Zweck ist der nützlichste Zielcomputer eine Instanz des [vollständigen Simulators](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` , der das Verhalten des Programms so berechnet, als ob es auf einem Rausch freien Quantum-Computer ausgeführt würde.

Bisher haben wir beschrieben, was geschieht, wenn ein bestimmtes Q # Callable-Element ausgeführt wird.
Unabhängig davon, ob Q # in einer eigenständigen Anwendung oder einem Host Programm verwendet wird, ist dieser allgemeine Prozess mehr oder weniger identisch---daher die Flexibilität des QDK.
Die Unterschiede zwischen den verschiedenen Methoden zum Aufrufen von Quantum Development Kit zeigen sich daher selbst, wie die Ausführung von Q # Callable aufgerufen wird und *wie* alle Ergebnisse zurückgegeben werden.
Genauer gesagt werden die Unterschiede im Zusammenhang mit 
1. Es wird angegeben, welche Q # Callable ausgeführt werden soll.
2. Gibt an, wie potenzielle Aufruf Bare Argumente bereitgestellt werden.
3. Angeben des Ziel Computers, auf dem der Computer ausgeführt werden soll, und
4. Gibt an, wie alle Ergebnisse zurückgegeben werden.

Zuerst wird erläutert, wie dies mit der eigenständigen f #-Anwendung über die Befehlszeile erfolgt, und anschließend können Sie mit der Verwendung von Python-und c#-Host Programmen fortfahren.
Wir reservieren die eigenständige Anwendung der q # jupyter-Notebooks für das letzte, da die primäre Funktionalität im Gegensatz zu den ersten drei nicht in einer lokalen q #-Datei liegt.

> [!NOTE]
> Obwohl wir dies in diesen Beispielen nicht veranschaulichen, besteht eine Gemeinsamkeit zwischen den Ausführungsmethoden darin, dass alle Nachrichten, die aus dem Q #-Programm gedruckt werden (z. b. über [`Message`](xref:microsoft.quantum.intrinsic.message) oder [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) ), in der Regel immer in der jeweiligen Konsole gedruckt werden.

## <a name="q-from-the-command-line"></a>F # von der Befehlszeile aus
Eine der einfachsten Möglichkeiten, Q #-Programme zu schreiben, besteht darin, die Gedanken über separate Dateien und eine zweite Sprache vollständig zu vermeiden.
Die Verwendung von Visual Studio Code oder Visual Studio mit der QDK-Erweiterung ermöglicht einen nahtlosen Workflow, bei dem wir q #-callables nur aus einer einzelnen q #-Datei ausführen.

Hierzu wird die Ausführung des Programms letztendlich aufgerufen, indem Sie Folgendes eingeben:
```dotnetcli
dotnet run
```
in der Befehlszeile.
Der einfachste Workflow ist, wenn der Verzeichnis Speicherort des Terminals mit der q #-Datei identisch ist, die mit der q #-Dateibearbeitung problemlos über das integrierte Terminal in vs Code behandelt werden kann, z. b..
Der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) akzeptiert jedoch zahlreiche Optionen, und das Programm kann auch an einem anderen Speicherort ausgeführt werden, indem einfach `--project <PATH>` der Speicherort der Q #-Datei bereitgestellt wird.


### <a name="add-entry-point-to-q-file"></a>Einstiegspunkt zu Q #-Datei hinzufügen

Die meisten Q #-Dateien enthalten mehr als eine Aufruf Bare Funktion. Daher muss der Compiler wissen, *welche* Callable ausgeführt werden soll, wenn der Befehl bereitgestellt wird `dotnet run` .
Dies erfolgt mit einer einfachen Änderung an der Q #-Datei selbst: 
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

Nun `dotnet run` führt ein-Befehl von der Befehlszeile aus `MeasureSuperposition` , um ausgeführt zu werden, und der zurückgegebene Wert wird dann direkt in das Terminal gedruckt.
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
> In definierte Argument Namen `camelCase` werden vom Compiler leicht geändert, damit Sie als f #-Eingaben akzeptiert werden. Wenn z. b. anstelle von `n` der oben genannte Name verwendet wird `numQubits` , wird diese Eingabe in der Befehlszeile über `--num-qubits 4` anstelle von bereitgestellt `-n 4` .

Die Fehlermeldung enthält auch weitere Optionen, die verwendet werden können, einschließlich Informationen zum Ändern des Ziel Computers.

### <a name="different-target-machines"></a>Verschiedene Zielcomputer

Da die Ausgaben unserer Vorgänge bisher die erwarteten Ergebnisse ihrer Aktion in echten Qubits waren, ist es klar, dass der Standardziel Computer von der Befehlszeile aus der vollständige quauntum-Simulator ist `QuantumSimulator` .
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

### <a name="non-q-dotnet-run-options"></a>Nicht-Q #- `dotnet run` Optionen

Wie bereits kurz erwähnt `--project` , akzeptiert der [ `dotnet run` Befehl](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) auch Optionen, die nicht mit den Q # Callable-Argumenten verknüpft sind.
Wenn beide Arten von Optionen bereit `dotnet` gestellt werden, müssen zuerst die-spezifischen Optionen, gefolgt von einem Trennzeichen `--` , und dann die Q #-spezifischen Optionen bereitgestellt werden.
Beispielsweise würde die Angabe eines Pfads zusammen mit einer Zahlen-Qubits für den obigen Vorgang über ausgeführt werden `dotnet run --project <PATH> -- -n <n>` .

## <a name="q-with-host-programs"></a>Q # mit Host Programmen

Mit unserer f #-Datei besteht eine Alternative zum Aufrufen eines Vorgangs oder einer Funktion direkt über die Befehlszeile darin, ein *Host Programm* in einer anderen klassischen Sprache zu verwenden. Dies kann insbesondere mit Python oder einer .NET-Sprache (z. b. c# oder F #) erfolgen (aus Gründen der Kürze wird c# hier nur ausführlich erläutert).
Zum Aktivieren der Interoperabilität ist ein wenig mehr Setup erforderlich. diese Details finden Sie jedoch in den [Installations](xref:microsoft.quantum.install)Handbüchern.

Kurz gesagt, enthält die Situation nun eine Host Programmdatei (z. b. `*.py` oder `*.cs` ) am gleichen Speicherort wie unsere Q #-Datei.
Es ist jetzt das *Host* Programm, das ausgeführt wird, und im Verlauf seiner Ausführung kann es bestimmte q #-Vorgänge und-Funktionen aus der q #-Datei abrufen.
Der Kern der Interoperabilität basiert auf dem f #-Compiler, der den Inhalt der q #-Datei für das Host Programm zugänglich macht, sodass Sie aufgerufen werden können.

Einer der Hauptvorteile der Verwendung eines Host Programms besteht darin, dass die vom Q #-Programm zurückgegebenen klassischen Daten dann in der Host Sprache weiterverarbeitet werden können.
Dies kann aus einer erweiterten Datenverarbeitung bestehen (z. b. etwas, das nicht intern in Q # ausgeführt werden kann), und anschließend weitere Q #-Aktionen auf der Grundlage dieser Ergebnisse oder etwas so einfach wie das Zeichnen der q #-Ergebnisse.

Das allgemeine Schema wird hier angezeigt, und wir erörtern die spezifischen Implementierungen für python und c# weiter unten. Ein Beispiel für die Verwendung eines F #-Host Programms finden Sie unter [.net-Interoperabilitäts Beispiele](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet).

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> Das `@EntryPoint()` für Q #-Befehlszeilen Anwendungen verwendete Attribut kann nicht mit Host Programmen verwendet werden.
> Wenn Sie in der von einem Host aufgerufenen Q #-Datei vorhanden ist, wird ein Fehler ausgelöst. 

Um mit unterschiedlichen Host Programmen arbeiten zu können, sind keine Änderungen an einer `*.qs` Q #-Datei erforderlich.
Die folgenden Host Programm Implementierungen funktionieren alle mit derselben Q #-Datei:

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
1. Importieren Sie das- `qsharp` Modul, das das Modul Lade Modul für die Q #-Interoperabilität registriert. 
    Dadurch können q #-Namespaces als Python-Module angezeigt werden, aus denen Sie q #-callables importieren können.
    Beachten Sie, dass es sich nicht um die selbst importierenden Q #-callables handelt, sondern um die python-stubweise, die das Aufrufen in Sie ermöglicht.
    Diese werden dann als Objekte von python-Klassen verwendet, auf denen Methoden zum Angeben der Zielcomputer verwendet werden, an die der Vorgang zur Ausführung gesendet wird.

2. Importieren Sie die f #-callables, die wir direkt aufrufen---in diesem Fall `MeasureSuperposition` und `MeasureSuperpositionArray` .
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    Wenn `qsharp` Sie das Modul importiert haben, können Sie auch callables direkt aus den Q # Library-Namespaces importieren.

3. Unter jedem anderen Python-Code können Sie jetzt diese callables auf bestimmten Ziel Computern aufrufen und ihre Rückgaben den Variablen (wenn Sie einen Wert zurückgeben) zur weiteren Verwendung zuweisen.

#### <a name="specifying-target-machines"></a>Angeben von Ziel Computern
Das Aufrufen eines Vorgangs, der auf einem bestimmten Zielcomputer ausgeführt werden soll, erfolgt über verschiedene python-Methoden auf dem importierten Objekt.
Beispielsweise `.simulate(<args>)` verwendet die `QuantumSimulator` zum Ausführen des Vorgangs, während `.estimate_resources(<args>)` dies in der erfolgt `ResourcesEstimator` .

#### <a name="passing-inputs-to-q"></a>Übergeben von Eingaben an Q\#
Argumente für q # Callable sollten in Form eines Schlüsselwort Arguments bereitgestellt werden, wobei das Schlüsselwort der Argument Name in der Q # Callable-Definition ist.
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

```python
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

### <a name="c"></a>[C#](#tab/tabid-csharp)

Ein c#-Host Programm verfügt über mehrere Komponenten, die eng mit einigen Komponenten des QDK funktionieren, z. b. die Simulatoren, die selbst auf c# basieren.

Der f #-Compiler funktioniert hier, indem er einen gleichwertig benannten c#-Namespace aus dem q #-Namespace in unserer q #-Datei erzeugt.
Außerdem wird eine gleichwertig benannte c#-Klasse für jeden der Q #-callables oder-Typen generiert, die darin definiert sind.

Zuerst werden alle Klassen, die in unserem Host Programm verwendet werden, mit-Anweisungen zur Verfügung gestellt `using` , die ungefähr mit den `open` Anweisungen in unserer Q #-Datei zu tun haben:

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (e.g. QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

Als nächstes deklarieren wir den c#-Namespace, einige andere Bits und Teile (siehe den vollständigen Codeblock unten) und dann eine beliebige klassische Programmierung (z. b. das Berechnen von Argumenten für die Q # callables).
Letzteres ist in diesem Fall nicht erforderlich, aber ein Beispiel für eine solche Verwendung finden Sie unter [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet)Beispiel.

#### <a name="target-machines"></a>Zielcomputer

Bei der Rückkehr zu f # müssen wir eine Instanz eines beliebigen Ziel Computers erstellen, auf dem wir unsere Vorgänge ausführen werden.

```csharp
            using var sim = new QuantumSimulator();
```

Die Verwendung anderer Zielcomputer ist so einfach wie das Instanziieren eines anderen Ziel Computers, obwohl die Art und Weise der Rückgabe geringfügig abweichen kann.
Aus Gründen der Kürze bleiben wir an der [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) für die Zeit und fügen die [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [folgenden](#including-the-resources-estimator)Informationen ein.

Jede c#-Klasse, die aus den Q #-Vorgängen generiert wird, verfügt über eine- `Run` Methode, deren erstes Argument die Zielcomputer Instanz sein muss.
Daher `MeasureSuperposition` verwenden wir, um auf dem auszuführen `QuantumSimulator` `MeasureSuperposition.Run(sim)` .
Die zurückgegebenen Ergebnisse können dann Variablen in c# zugewiesen werden:

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> Die `Run` -Methode wird asynchron ausgeführt, da dies die Groß-und Kleinschreibung für echte Quantum-Hardware ist. Daher blockiert das- `await` Schlüsselwort die weitere Ausführung, bis die Aufgabe abgeschlossen ist.

Wenn das Q # Callable-Element keine Rückgaben aufweist (d. h. den Rückgabetyp aufweist `Unit` ), kann die Ausführung weiterhin auf dieselbe Weise erfolgen, ohne Sie einer Variablen zuzuweisen.
In diesem Fall würde die gesamte Zeile einfach aus 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a>Argumente

Alle Argumente für Q # Callable werden einfach als zusätzliche Argumente an den Zielcomputer weitergeleitet.
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

Am Speicherort der c#-Datei kann das Host Programm von der Befehlszeile aus ausgeführt werden, indem Sie eingeben.
```dotnetcli
dotnet run
```
in diesem Fall wird die Ausgabe in die Konsole geschrieben, ähnlich wie 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> Aufgrund der Interoperabilität des Compilers mit Namespaces könnten wir unsere Q #-callables ohne die `using NamespaceName;` -Anweisung verfügbar machen und den c#-Namespace Titel einfach zuordnen.
> Das heißt, indem durch ersetzt wird `namespace host` `namespace NamespaceName` .

#### <a name="including-the-resources-estimator"></a>Einschließen der Ressourcenschätzung

[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Erfordert eine etwas andere Implementierung zum Abrufen der Ausgabe.

Anstatt Sie als Variable mit einer-Anweisung zu instanziieren `using` (wie dies bei der der Fall ist `QuantumSimulator` ), können wir die Objekte der Klasse über

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

Beachten Sie, dass anstelle eines einzelnen Ziel Simulators, der von mehreren Q #-Vorgängen verwendet werden soll, jeweils eine instanziiert wird. Dies liegt daran, dass die Objekte selbst geändert werden, wenn Sie als Zielcomputer verwendet werden, und ihre Ergebnisse anschließend mit der-Klassenmethode abgerufen werden können `.ToTSV()` .

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

## <a name="q-jupyter-notebooks"></a>Jupyter Notebook-Instanzen in Q#
Q # jupyter Notebooks nutzen den IQ #-Kernel, mit dem Sie q #-callables in einem einzigen Notebook definieren, kompilieren und ausführen können---zusammen mit Anweisungen, Notizen und anderem Inhalt.
Dies bedeutet, dass es zwar möglich ist, den Inhalt von Q #-Dateien zu importieren und zu verwenden `*.qs` , aber im Ausführungs Modell nicht erforderlich sind.

Hier wird ausführlich erläutert, wie die oben beschriebenen q #-Vorgänge ausgeführt werden, aber eine umfassendere Einführung in die Verwendung von q # jupyter Notebooks finden Sie unter Einführung [in q # und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).

### <a name="defining-operations"></a>Definieren von Vorgängen

In einem q #-Jupyter Notebook geben Sie f #-Code genau so ein, wie es im Namespace einer q #-Datei der Fall wäre.

Daher können wir den Zugriff auf callables aus den [Q # Standard-Bibliotheken](xref:microsoft.quantum.qsharplibintro) mit `open` Anweisungen für die jeweiligen Namespaces aktivieren.
Wenn eine Zelle mit einer solchen Anweisung ausgeführt wird, sind die Definitionen aus diesen Namespaces im gesamten Arbeitsbereich verfügbar.

> [!NOTE]
> Callables von [Microsoft. Quantum. intrinsisch](xref:microsoft.quantum.intrinsic) und [Microsoft. Quantum. Canon](xref:microsoft.quantum.canon) (z. b. [`H`](xref:microsoft.quantum.intrinsic.h) und [`ApplyToEach`](xref:microsoft.quantum.canon.applytoeach) ) stehen automatisch für Vorgänge zur Verfügung, die in Zellen in Q # jupyter-Notebooks definiert sind.
> Dies gilt jedoch nicht für Code, der aus externen Q #-Quelldateien eingefügt wurde (ein Prozess, der unter Einführung [in q # und jupyter Notebooks](https://github.com/microsoft/Quantum/blob/master/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)angezeigt wird). 
> 

Ebenso erfordert das Definieren von Vorgängen lediglich den Q #-Code und die Ausführung der Zelle.

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="600">

In der Ausgabe werden dann diese Vorgänge aufgelistet, die aus zukünftigen Zellen aufgerufen werden können.

### <a name="target-machines"></a>Zielcomputer

Die Funktionen zum Ausführen von Vorgängen auf bestimmten Ziel Computern werden über die [Befehle "IQ # Magic](xref:microsoft.quantum.guide.quickref.iqsharp)" bereitgestellt.
Beispielsweise `%simulate` verwendet die `QuantumSimulator` , und `%estimate` verwendet Folgendes `ResourcesEstimator` :

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Simulate and estimate resources Jupyter cell" width="500">

### <a name="passing-inputs-to-functions-and-operations"></a>Übergeben von Eingaben an Funktionen und Vorgänge

Derzeit können die Befehle zum Ausführen von Magic nur mit Vorgängen verwendet werden, die keine Argumente annehmen. Zum Ausführen von `MeasureSuperpositionArray` müssen wir also einen Wrapper Vorgang definieren, der dann den Vorgang mit den Argumenten aufruft:

<img src="../media/hostprograms_jupyter_wrapper_def_sim_crop.png" alt="Wrapper function and simulate Jupyter cell" width="550">

Dieser Vorgang kann natürlich auch mit `%estimate` und anderen Ausführungs Befehlen verwendet werden.
