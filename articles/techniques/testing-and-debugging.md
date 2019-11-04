---
title: 'F #-Techniken, testen und Debuggen | Microsoft-Dokumentation'
description: 'F #-Techniken, testen und Debuggen'
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 25679331f1bed9f98b86c6eb20f511c891bac1af
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183487"
---
# <a name="testing-and-debugging"></a>Testen und Debuggen

Wie bei der klassischen Programmierung ist es von entscheidender Bedeutung, zu überprüfen, ob Quantum-Programme erwartungsgemäß agieren, und ein ungültiges Quantum-Programm diagnostizieren zu können.
In diesem Abschnitt werden die Tools beschrieben, die von Q # zum Testen und Debuggen von Quantum-Programmen angeboten werden.

## <a name="unit-tests"></a>Komponenten Tests

Ein gängiger Ansatz zum Testen klassischer Programme ist das Schreiben von kleinen Programmen namens Komponenten *Tests* , die Code in einer Bibliothek ausführen und die Ausgabe mit einer erwarteten Ausgabe vergleichen.
Beispielsweise möchten wir möglicherweise sicherstellen, dass `Square(2)` `4`zurückgibt, da wir *ein* -Wert von "$ 2 ^ 2 = $4" kennen.

Q # unterstützt das Erstellen von Komponententests für Quantum-Programme und kann als Tests innerhalb des [xUnit](https://xunit.github.io/) -Komponenten Test-Frameworks ausgeführt werden.

### <a name="creating-a-test-project"></a>Erstellen eines Test Projekts

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Öffnen Sie Visual Studio 2019. Wechseln Sie zum Menü `File`, und wählen Sie `New` > `Project...`aus.
Wählen Sie im Projektvorlagen-Explorer unter `Installed` > `Visual C#`die `Q# Test Project` Vorlage aus.

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

In beiden Fällen werden für das neue Projekt zwei Dateien geöffnet.
Die erste Datei, `Tests.qs`, bietet einen geeigneten Ort zum Definieren neuer Q #-Komponententests.
Diese Datei enthält anfänglich einen Beispiel-Komponenten Test `AllocateQubitTest` der überprüft, ob sich ein neu zugewiesenes Qubit im $ \ket{0}$ State befindet und eine Meldung ausgibt:

```qsharp
    operation AllocateQubitTest () : Unit {
        using (q = Qubit()) {
            Assert([PauliZ], [q], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

Jeder Q #-Vorgang, der mit dem Typ `(Unit => Unit)` oder mit `(Unit -> Unit)` kompatiblen Funktion kompatibel ist, kann als Komponenten Test ausgeführt werden. 

Die zweite Datei, `TestSuiteRunner.cs` enthält eine Methode, die Q #-Komponententests ermittelt und ausführt. Dies ist die Methode, `TestTarget` mit `OperationDriver` Attribut kommentiert wird.
Das `OperationDriver`-Attribut ist ein Teil der xUnit-Erweiterungs Bibliothek Microsoft. Quantum. Simulation. xUnit.
Das Komponenten Test-Framework ruft `TestTarget` Methode für jeden erkannten Q #-Komponenten Test auf.
Das Framework übergibt die Komponenten Testbeschreibung über `op` Argument an die-Methode. Die folgende Codezeile:
```csharp
op.TestOperationRunner(sim);
```
führt den Komponenten Test auf `QuantumSimulator`aus.

Standardmäßig sucht der Mechanismus für die Komponenten Test Ermittlung nach allen Q #-Funktionen oder-Vorgängen mit kompatiblem Typ, die die folgenden Eigenschaften erfüllen:
* Befindet sich in der gleichen Assembly wie die Methode, die mit dem `OperationDriver`-Attribut kommentiert wird.
* Befindet sich im gleichen Namespace wie die Methode, die mit dem `OperationDriver`-Attribut kommentiert wird.
* Hat einen Namen, der mit `Test`endet.

Eine Assembly, ein Namespace und ein Suffix für Komponenten Testfunktionen und-Vorgänge können mithilfe optionaler Parameter des `OperationDriver` Attributs festgelegt werden:
* `AssemblyName` Parameter legt den Namen der Assembly fest, die nach Tests durchsucht wird.
* `TestNamespace` Parameter legt den Namen des Namespace fest, der nach Tests durchsucht wird.
* `Suffix` legt das Suffix von Vorgangs-oder Funktionsnamen fest, die als Unittests betrachtet werden.

Außerdem können Sie mit dem `TestCasePrefix` optionalen-Parameter ein Präfix für den Namen des Testfalls festlegen. Das Präfix vor dem Vorgangs Namen wird in der Liste der Testfälle angezeigt. Beispielsweise führt `TestCasePrefix = "QSim:"` dazu, dass `AllocateQubitTest` in der Liste der gefundenen Tests als `QSim:AllocateQubitTest` angezeigt wird. Dies kann beispielsweise hilfreich sein, um anzugeben, welcher Simulator zum Ausführen eines Tests verwendet wird.

### <a name="running-q-unit-tests"></a>Ausführen von f #-Komponenten Tests

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Wechseln Sie als einmalige Einrichtung pro Lösung zu `Test` Menü, und wählen Sie `Test Settings` > `Default Processor Architecture` > `X64`aus.

> [!TIP]
> Die Standardeinstellung für die Prozessorarchitektur für Visual Studio wird in der Projektmappen-Optionsdatei (`.suo`) für jede Lösung gespeichert.
> Wenn Sie diese Datei löschen, müssen Sie `X64` als Prozessorarchitektur erneut auswählen.

Erstellen Sie das Projekt, wechseln Sie zum Menü `Test`, und wählen Sie `Windows` > `Test Explorer`aus. `AllocateQubitTest` wird in der Liste der Tests in der `Not Run Tests` Gruppe angezeigt. Wählen Sie `Run All` aus, oder führen Sie den einzelnen Test aus, und es sollte bestanden werden!

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Navigieren Sie zum Ausführen von Tests zum Projektordner (dem Ordner, der `Tests.csproj`enthält), und führen Sie den folgenden Befehl aus:

```bash
$ dotnet restore
$ dotnet test
```

Die Ausgabe sollte in etwa wie folgt aussehen:

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

***

## <a name="logging-and-assertions"></a>Protokollierung und Assertionen

Eine wichtige Folge der Tatsache, dass Funktionen in Q # keine Nebeneffekte haben, besteht darin, dass alle Auswirkungen der Ausführung einer Funktion, deren Ausgabetyp das leere Tupel ist `()` nicht innerhalb eines Q #-Programms beobachtet werden können.
Das heißt, ein Zielcomputer kann keine Funktion ausführen, die `()` zurückgibt, wobei sichergestellt wird, dass diese Auslassung das Verhalten eines nachfolgenden f #-Codes nicht ändert.
Dadurch werden Funktionen `()` ein nützliches Tool zum Einbetten von Assertionen und zum Debuggen von Logik in Q #-Programme. 

### <a name="logging"></a>Protokollierung

Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> hat den Typ `(String -> Unit)` und ermöglicht die Erstellung von Diagnose Nachrichten.

Die `onLog` Aktion `QuantumSimulator` kann verwendet werden, um Aktionen zu definieren, die ausgeführt werden, wenn f #-Code `Message`aufruft. Standardmäßig werden protokollierte Nachrichten in der Standardausgabe ausgegeben.

Beim Definieren einer Komponenten Test Sammlung können die protokollierten Nachrichten an die Test Ausgabe weitergeleitet werden. Wenn ein Projekt aus einer f #-Test Projektvorlage erstellt wird, wird diese Umleitung für die Suite vorkonfiguriert und wie folgt standardmäßig erstellt:

```qsharp
using (var sim = new QuantumSimulator())
{
    // OnLog defines action(s) performed when Q# test calls operation Message
    sim.OnLog += (msg) => { output.WriteLine(msg); };
    op.TestOperationRunner(sim);
}
```

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test klicken, wird ein Panel mit Informationen zur Testausführung angezeigt: Status "erfolgreich"/"Fehler", verstrichene Zeit und "Ausgabe". Wenn Sie auf den Link "Output" klicken, wird die Test Ausgabe in einem neuen Fenster geöffnet.

![Test Ausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Der Status "erfolgreich/fehlgeschlagen" für jeden Test wird von `dotnet test`in der Konsole gedruckt.
Bei fehlgeschlagenen Tests werden die Ausgaben, die als Ergebnis des obigen `output.WriteLine(msg)` Aufrufens protokolliert werden, auch in der Konsole gedruckt, um die Diagnose des Fehlers zu erleichtern.

***

### <a name="assertions"></a>TeilI

Die gleiche Logik kann auch für die Implementierung von Assertionen verwendet werden. Betrachten wir ein einfaches Beispiel:

```qsharp
function AssertPositive(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

Hier gibt das Schlüsselwort `fail` an, dass die Berechnung nicht fortgesetzt werden soll, wodurch eine Ausnahme auf dem Zielcomputer ausgelöst wird, der das Q #-Programm ausführt.
Definitionsgemäß kann ein Fehler dieser Art nicht innerhalb von q # beobachtet werden, da kein weiterer Q #-Code ausgeführt wird, nachdem eine `fail`-Anweisung erreicht wurde.
Wenn wir also einen `AssertPositive`-Aufrufvorgang fortsetzen, können wir sicher sein, dass die Eingabe positiv ist.

Wenn Sie auf diese Ideen aufbauen, bietet [das präspiel](xref:microsoft.quantum.libraries.standard.prelude) zwei besonders nützliche Assertionen, <xref:microsoft.quantum.intrinsic.assert> und <xref:microsoft.quantum.intrinsic.assertprob> beide als Vorgänge auf `()`modelliert werden. Diese Assertionen akzeptieren jeweils einen Pauli-Operator, der ein bestimmtes Maß an Interesse beschreibt, ein Quantum-Register, für das eine Messung durchgeführt werden soll, und ein hypothetisches Ergebnis.
Auf Ziel Computern, die bei der Simulation funktionieren, werden wir nicht durch [das No-Klon-Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen durchführen, ohne dass das an diese Assertionen weiter gegebene Register gestört wird.
Ein Simulator kann dann, ähnlich wie in der obigen `AssertPositive`-Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beachtet wird:

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

Bei physischer Quantum-Hardware, bei der das No-Klon-Theorem die Prüfung des Quantums verhindert, werden die `Assert`-und `AssertProb` Vorgänge einfach `()` zurückgegeben.

Der <xref:microsoft.quantum.diagnostics>-Namespace stellt mehrere weitere Funktionen der `Assert`-Familie bereit, die es uns ermöglichen, erweiterte Bedingungen zu überprüfen. 

## <a name="dump-functions"></a>Dumpfunktionen

Zur Unterstützung der Problembehandlung von Quantum-Programmen bietet der <xref:microsoft.quantum.diagnostics>-Namespace zwei Funktionen, mit denen der aktuelle Status des Ziel Computers in einer Datei gespeichert werden kann: <xref:microsoft.quantum.diagnostics.dumpmachine> und <xref:microsoft.quantum.diagnostics.dumpregister>. Die generierte Ausgabe hängt von dem Zielcomputer ab.

### <a name="dumpmachine"></a>Dumpmachine

Der als Teil des Quantum Development Kit verteilte Volltext-Quantum-Simulator schreibt die [Wellenfunktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantum-Systems als eindimensionales Array komplexer Zahlen in die Datei, in der jedes Element die Amplitude der Wahrscheinlichkeit für die Messung des Berechnungsbasis Zustands $ \ket{n} $, wobei $ \ket{n} = \ket{b_{n-1}... b_1b_0} $ für Bits $\{b_i\}$. Beispielsweise auf einem Computer, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\bruchteil {(1 + i)}{2} \ket{10}, \end{align} $ $ Call <xref:microsoft.quantum.diagnostics.dumpmachine> generiert diese Ausgabe. :

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.
In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{n} $ im kartesischen und Polar Format beschrieben. Im Detail für die erste Zeile:

* **`∣0❭:`** diese Zeile dem Status der `0` Berechnungsbasis entspricht.
* **`0.707107 +  0.000000 i`** : die Wahrscheinlichkeits Amplitude im kartesischen Format.
* **` == `** : das `equal` Vorzeichen trennt beide äquivalente Darstellungen.
* **`**********  `** : eine grafische Darstellung der Größe, die Anzahl der `*` proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.
* **`[ 0.500000 ]`** : der numerische Wert der Größe.
* **`    ---`** : eine grafische Darstellung der Amplitude-Phase (siehe unten).
* **`[ 0.0000 rad ]`** : der numerische Wert der Phase (im Bogenmaße).

Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt. Die Größen Darstellung ist geradlinig: Sie zeigt einen Balken `*`an, je größer die Wahrscheinlichkeit, mit der die Leiste größer wird. In der Phase zeigen wir die folgenden Symbole zur Darstellung des Winkels basierend auf Bereichen:

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

In den folgenden Beispielen werden `DumpMachine` für einige gängige Zustände veranschaulicht:

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > Die ID eines Qubit wird zur Laufzeit zugewiesen und ist nicht notwendigerweise an die Reihenfolge ausgerichtet, in der das Qubit zugeordnet wurde, oder an seine Position in einem Qubit-Register.


#### <a name="visual-studio-2019tabtabid-vs2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Sie können eine Qubit-ID in Visual Studio ermitteln, indem Sie einen Haltepunkt in Ihrem Code platzieren und den Wert einer Qubit-Variablen untersuchen, z. b.:
  > 
  > ![Anzeigen der Qubit-ID in Visual Studio](~/media/qubit_id.png)
  >
  > Das Qubit mit Index `0` auf `register2` hat ID =`3`, das Qubit mit Index `1` hat ID =`2`.

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Sie können eine Qubit-ID ermitteln, indem Sie die <xref:microsoft.quantum.intrinsic.message>-Funktion verwenden und die Qubit-Variable in der Nachricht übergeben, z. b.:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > Dies könnte folgende Ausgabe generieren:
  >```
  > 0=q:3; 1=q:2
  >```
  > Dies bedeutet, dass das Qubit mit Index `0` auf `register2` ID =`3`, das Qubit mit Index `1` ID =`2`aufweist.


***

<xref:microsoft.quantum.diagnostics.dumpmachine> ist Teil des <xref:microsoft.quantum.diagnostics>-Namespace. damit Sie ihn verwenden können, müssen Sie eine `open`-Anweisung hinzufügen:

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a>Dumpregiester

<xref:microsoft.quantum.diagnostics.dumpregister> funktioniert wie <xref:microsoft.quantum.diagnostics.dumpmachine>, mit dem Unterschied, dass es auch ein Array von Qubits verwendet, um die Menge der Informationen auf die für die entsprechenden Qubits relevanten Informationen einzuschränken.

Wie bei <xref:microsoft.quantum.diagnostics.dumpmachine>hängt die von <xref:microsoft.quantum.diagnostics.dumpregister> generierten Informationen vom Zielcomputer ab. Für den vollständigen Quantum-Simulator schreibt er in die Datei, die von der Wave-Funktion bis zu einer globalen Phase des von den bereitgestellten Qubits generierten Quantums in demselben Format wie <xref:microsoft.quantum.diagnostics.dumpmachine>generiert wird.  Beispiel: Wiederholen Sie einen Computer, auf dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\bruchteil {(1 + i)}{2} \ket{10} =-e ^ {-i \ pi/4} ((\frac{1}{\sqrt{2}} \ Ket{0}-\bruch{(1 + i)}{2} \ket{1}) \otimes \bruchteil {-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ aufrufen <xref:microsoft.quantum.diagnostics.dumpregister> für `qubit[0]` generiert diese Ausgabe:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

Wenn Sie <xref:microsoft.quantum.diagnostics.dumpregister> für `qubit[1]` aufrufen, wird diese Ausgabe generiert:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Im Allgemeinen ist der Status eines Registers, das mit einem anderen Register entkoppelt ist, ein gemischter Zustand und kein reiner Zustand. In diesem Fall gibt <xref:microsoft.quantum.diagnostics.dumpregister> die folgende Meldung aus:

```
Qubits provided (0;) are entangled with some other qubit.
```

Im folgenden Beispiel wird gezeigt, wie Sie sowohl <xref:microsoft.quantum.diagnostics.dumpregister> als auch <xref:microsoft.quantum.diagnostics.dumpmachine> in Ihrem Q #-Code verwenden können:

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a>Debuggen

Zusätzlich zu den Funktionen und Vorgängen von `Assert` und `Dump` unterstützt Q # eine Teilmenge der standardmäßigen Visual Studio-Debugfunktionen: [Festlegen von Zeilen Haltepunkten](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), schrittweise [durchlaufen von Code mithilfe von F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) und überprüfen [von Werten klassischer Variablen ](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows)sind während der Codeausführung im Simulator möglich.

Das Debuggen in Visual Studio Code wird noch nicht unterstützt.

