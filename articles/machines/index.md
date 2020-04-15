---
title: Quantensimulatoren und Hostanwendungen | Microsoft-Dokumentation
description: Es wird beschrieben, wie Sie Quantensimulatoren mit einer klassischen .NET-Computingsprache (normalerweise C# oder Q#) betreiben.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 9d1c045cf1a2c3e19030cb38dbc7496dbd24ab58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2020
ms.locfileid: "73442213"
---
# <a name="quantum-simulators-and-host-applications"></a>Quantensimulatoren und Hostanwendungen

## <a name="what-youll-learn"></a>Sie lernen Folgendes

> [!div class="checklist"]
> * Ausführen von Quantenalgorithmen
> * Quantensimulatoren in diesem Release
> * Schreiben eines C#-Treibers für Ihren Quantenalgorithmus

## <a name="the-quantum-development-kit-execution-model"></a>Modell für die Quantum Development Kit-Ausführung

Unter [Schreiben eines Quantenprogramms](xref:microsoft.quantum.write-program) haben wir unseren Quantenalgorithmus ausgeführt, indem wir ein `QuantumSimulator`-Objekt an die `Run`-Methode der Algorithmusklasse übergeben haben.
Die `QuantumSimulator`-Klasse führt den Quantenalgorithmus aus, indem der Quantenzustandsvektor vollständig simuliert wird. Dies ist der perfekte Ansatz für das Ausführen und Testen von `Teleport`.
Weitere Informationen zu Quantenzustandsvektoren finden Sie im [Leitfaden zu den Konzepten](xref:microsoft.quantum.concepts.intro).

Andere Zielcomputer können verwendet werden, um einen Quantenalgorithmus auszuführen.
Der Computer ist für das Bereitstellen der Implementierungen von Quantenprimitiven für den Algorithmus zuständig.
Dies gilt auch für primitive Vorgänge, z. B. H, CNOT und Measure, sowie für die Verwaltung und Nachverfolgung von Qubits.
Verschiedene Klassen von Quantencomputern stehen für unterschiedliche Ausführungsmodelle desselben Quantenalgorithmus.

Mit jeder Art von Quantencomputer können unterschiedliche Implementierungen dieser Primitive bereitgestellt werden.
Mit dem Simulator für die Nachverfolgung von Quantencomputern, der im Development Kit enthalten ist, werden beispielsweise keine Simulationen durchgeführt.
Stattdessen wird hiermit die Nutzung von Gates, Qubits und anderen Ressourcen für den Algorithmus nachverfolgt.

### <a name="quantum-machines"></a>Quantencomputer

Für die Zukunft ist die Definition weiterer Quantencomputerklassen geplant, um andere Arten von Simulationen und die Ausführung auf topologischen Quantencomputern zu unterstützen.
Indem der Algorithmus konstant gehalten wird, während die zugrunde liegende Computerimplementierung variiert, wird das Testen und Debuggen eines simulierten Algorithmus vereinfacht. Anschließend können Sie beim Ausführen auf echter Hardware sicher sein, dass sich der Algorithmus nicht geändert hat.

### <a name="whats-included-in-this-release"></a>Was ist in diesem Release enthalten?

Dieses Release des Quantum Developer Kit umfasst mehrere Quantencomputerklassen.
Diese sind im Namespace `Microsoft.Quantum.Simulation.Simulators` definiert.

* Ein [umfassender Zustandsvektorsimulator](xref:microsoft.quantum.machines.full-state-simulator) (die `QuantumSimulator`-Klasse).
* Eine [einfache Ressourcenschätzung](xref:microsoft.quantum.machines.resources-estimator) (die `ResourcesEstimator`-Klasse). Sie ermöglicht für die Ressourcen, die zum Ausführen eines Quantenalgorithmus benötigt werden, eine Analyse der Ressourcen auf oberster Ebene.
* Eine [auf der Ablaufverfolgung basierende Ressourcenschätzung](xref:microsoft.quantum.machines.qc-trace-simulator.intro) (die `QCTraceSimulator`-Klasse). Sie ermöglicht eine erweiterte Analyse des Ressourcenverbrauchs für das gesamte Aufrufdiagramm des Algorithmus.
* Ein [Toffoli-Simulator](xref:microsoft.quantum.machines.toffoli-simulator) (die `ToffoliSimulator`-Klasse).

## <a name="writing-a-host-application"></a>Schreiben einer Hostanwendung

Unter [Schreiben eines Quantenprogramms](xref:microsoft.quantum.write-program) haben wir einen einfachen C#-Treiber für unseren Teleportalgorithmus geschrieben. Ein C#-Treiber hat vier Hauptaufgaben:

* Erstellen des Zielcomputers
* Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind
* Ausführen des Quantenalgorithmus mit dem Simulator
* Verarbeiten des Vorgangsergebnisses

Hier werden die einzelnen Schritte ausführlicher beschrieben.

### <a name="constructing-the-target-machine"></a>Erstellen des Zielcomputers

Quantencomputer sind Instanzen normaler .NET-Klassen. Sie werden also genauso wie .NET-Klassen erstellt, indem ihr Konstruktor aufgerufen wird.
Da von einigen Simulatoren, z. B. `QuantumSimulator`, die <xref:System.IDisposable?displayProperty=nameWithType>-.NET-Schnittstelle implementiert wird, sollten diese mit einer C#-Anweisung vom Typ `using` umschlossen werden.

### <a name="computing-arguments-for-the-algorithm"></a>Berechnen von Argumenten für den Algorithmus

Im `Teleport`-Beispiel haben wir einige etwas künstliche Argumente für die Übergabe an unseren Quantenalgorithmus berechnet.
Typischer ist aber, dass für den Quantenalgorithmus umfangreiche Daten benötigt werden, die am einfachsten über den klassischen Treiber bereitgestellt werden können.

Beim Durchführen von chemischen Simulationen ist für den Quantenalgorithmus beispielsweise eine umfassende Tabelle mit Molekülorbital-Interaktionsintegralen erforderlich.
Normalerweise werden diese Daten aus einer Datei eingelesen, die beim Ausführen des Algorithmus angegeben wird.
Da Q# nicht über einen Mechanismus für den Zugriff auf das Dateisystem verfügt, ist es am besten, diese Daten über den klassischen Treiber zu erfassen und dann an die `Run`-Methode des Quantenalgorithmus zu übergeben.

Ein weiterer Fall, in dem der klassische Treiber eine wichtige Rolle spielt, sind Variationsmethoden.
Bei dieser Klasse von Algorithmen wird basierend auf einigen klassischen Parametern ein Quantenzustand vorbereitet, der dann zum Berechnen eines benötigten Werts verwendet wird.
Die Parameter werden basierend auf einer Art von Bergsteiger- oder Machine Learning-Algorithmus angepasst, und der Quantenalgorithmus wird erneut ausgeführt.
Bei Algorithmen dieser Art wird der Bergsteigeralgorithmus selbst am besten als reine klassische Funktion implementiert, die vom klassischen Treiber aufgerufen wird. Die Ergebnisse des Bergsteigervorgangs werden dann an die nächste Ausführung des Quantenalgorithmus übergeben.

### <a name="running-the-quantum-algorithm"></a>Ausführen des Quantenalgorithmus

Dieser Teil ist im Allgemeinen nicht sehr kompliziert.
Jeder Q#-Vorgang wird zu einer Klasse kompiliert, die eine statische `Run`-Methode bereitstellt.
Die Argumente für diese Methode werden vom vereinfachten Argumenttupel des Vorgangs selbst bereitgestellt – sowie ein weiteres erstes Argument, bei dem es sich um den Simulator für die Ausführung handelt. Für einen Vorgang, für den das benannte Tupel vom Typ `(a: String, (b: Double, c: Double))` erwartet wird, hat das vereinfachte Gegenstück den Typ `(String a, Double b, Double c)`.


Beim Übergeben von Argumenten an eine `Run`-Methode sind einige Besonderheiten zu beachten:

* Arrays müssen mit einem `Microsoft.Quantum.Simulation.Core.QArray<T>`-Objekt umschlossen sein.
    Eine `QArray`-Klasse verfügt über einen Konstruktor, für den eine beliebige sortierte Sammlung (`IEnumerable<T>`) mit geeigneten Objekten verwendet werden kann.
* Das leere Tupel (`()` in Q#) wird in C# mit `QVoid.Instance` dargestellt.
* Tupel, die nicht leer sind, werden als `ValueTuple`-.NET-Instanzen dargestellt.
* Benutzerdefinierte Q#-Typen werden als Basistyp übergeben.
* Zum Übergeben eines Vorgangs oder einer Funktion an eine `Run`-Methode müssen Sie eine Instanz der Vorgangs- oder Funktionsklasse abrufen, indem Sie die `Get<>`-Methode des Simulators verwenden.

### <a name="processing-the-results"></a>Verarbeiten der Ergebnisse

Die Ergebnisse des Quantenalgorithmus werden von der `Run`-Methode zurückgegeben.
Da die `Run`-Methode asynchron ausgeführt wird, gibt sie eine Instanz von <xref:System.Threading.Tasks.Task`1> zurück.
Es gibt mehrere Möglichkeiten, die Ergebnisse des tatsächlichen Vorgangs zu erhalten. Der einfachste Weg ist die Verwendung der [`Result`-Eigenschaft](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result) der `Task`:

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
Andere Verfahren, z. B. die [`Wait`-Methode](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) oder das C#-Schlüsselwort [`await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await), funktionieren ebenfalls.

Wie auch bei Argumenten, werden Q#-Tupel als `ValueTuple`-Instanzen und Q#-Arrays als `QArray`-Instanzen dargestellt.
Benutzerdefinierte Typen werden als Basistypen zurückgegeben.
Das leere Tupel `()` wird als Instanz der `QVoid`-Klasse zurückgegeben.

Für viele Quantenalgorithmen ist eine umfangreiche Nachbearbeitung erforderlich, um nützliche Antworten zu erhalten.
Der Quantenteil des Shor-Algorithmus ist beispielsweise nur der Anfang einer Berechnung, bei der die Faktoren einer Zahl ermittelt werden.

In den meisten Fällen ist es am einfachsten, diese Art der Nachbearbeitung über den klassischen Treiber durchzuführen.
Nur mit dem klassischen Treiber können Ergebnisse an den Benutzer gemeldet oder auf Datenträger geschrieben werden.
Der klassische Treiber verfügt über Zugriff auf Analysebibliotheken und andere mathematische Funktionen, die in Q# nicht verfügbar gemacht werden.


## <a name="failures"></a>Fehler

Wenn bei der Ausführung eines Vorgangs die Q#-Anweisung `fail` erreicht wird, wird `ExecutionFailException` ausgelöst.

Aufgrund der Verwendung von `System.Task` in der `Run`-Methode ist die Ausnahme, die aufgrund einer `fail`-Anweisung ausgelöst wird, von `System.AggregateException` umschlossen.
Zum Ermitteln der tatsächlichen Ursache des Fehlers müssen Sie eine Iteration in `AggregateException` 
`InnerExceptions` durchführen. Beispiel:

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a>Andere klassische Sprachen

Die bereitgestellten Beispiele gelten für C#, F# und Python, aber das Quantum Development Kit unterstützt auch das Schreiben klassischer Hostprogramme in anderen Sprachen.
Wenn Sie beispielsweise ein Hostprogramm in Visual Basic schreiben möchten, [sollte dies problemlos funktionieren](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).
