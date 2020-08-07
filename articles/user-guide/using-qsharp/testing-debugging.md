---
title: Testen und Debuggen
description: Erfahren Sie, wie Sie Komponententests, Fakten und Assertionen sowie Dumpfunktionen zum Testen und Debuggen von Quantum-Programmen verwenden.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2b5276da594ba263177d435c1153f6d96e29c4e8
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867912"
---
# <a name="testing-and-debugging"></a>Testen und Debuggen

Wie bei der klassischen Programmierung ist es von entscheidender Bedeutung, zu überprüfen, ob Quantum-Programme erwartungsgemäß agieren, und das falsche Verhalten diagnostizieren zu können.
In diesem Abschnitt werden die Tools beschrieben, die von Q# zum Testen und Debuggen von Quantum-Programmen angeboten werden.

## <a name="unit-tests"></a>Komponententests

Ein gängiger Ansatz zum Testen klassischer Programme ist das Schreiben von kleinen Programmen namens Komponenten *Tests*, die Code in einer Bibliothek ausführen und die Ausgabe mit einer erwarteten Ausgabe vergleichen.
So können Sie z. b. sicherstellen, dass `Square(2)` zurückgibt, `4` da Sie *eine* mit dem Wert "$ 2 ^ 2 = $4.

Q#unterstützt das Erstellen von Komponententests für Quantum-Programme, die als Tests innerhalb des [xUnit](https://xunit.github.io/) -Komponenten Test-Frameworks ausgeführt werden können.

### <a name="creating-a-test-project"></a>Erstellen eines Test Projekts

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Öffnen Sie Visual Studio 2019. Wechseln Sie zum Menü **Datei** , und wählen Sie **Neu > Projekt...** aus. Suchen Sie in der oberen rechten Ecke nach `Q#` , und wählen Sie die Vorlage ** Q# Test Projekt** aus.

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Das neue Projekt verfügt über eine einzelne Datei `Tests.qs` , die einen geeigneten Ort zum Definieren neuer Komponenten Q# Tests bietet.
Diese Datei enthält zunächst einen Beispiel Komponenten Test, `AllocateQubit` der überprüft, ob sich ein neu zugewiesenes Qubit im Zustand "$ \ket $" befindet {0} und eine Meldung ausgibt:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

Alle Vorgänge Q# oder Funktionen, die ein Argument vom Typ `Unit` und zurück `Unit` geben, können über das-Attribut als Komponenten Test gekennzeichnet werden `@Test("...")` . Im vorherigen Beispiel gibt das-Argument dieses Attributs, `"QuantumSimulator"` , das Ziel an, auf dem der Test ausgeführt wird. Ein einzelner Test kann auf mehreren Zielen ausgeführt werden. Fügen Sie z. b. ein Attribut `@Test("ResourcesEstimator")` vor ein `AllocateQubit` . 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Speichern Sie die Datei, und führen Sie alle Tests aus. Es sollten nun zwei Komponententests vorhanden sein, von denen eine `AllocateQubit` auf dem ausgeführt wird `QuantumSimulator` , und eine, in der Sie ausgeführt wird `ResourcesEstimator` . 

Der Q# Compiler erkennt die integrierten Ziele `"QuantumSimulator"` , `"ToffoliSimulator"` und `"ResourcesEstimator"` als gültige Ausführungs Ziele für Komponententests. Es ist auch möglich, einen voll qualifizierten Namen anzugeben, um ein benutzerdefiniertes Ausführungs Ziel zu definieren. 

### <a name="running-no-locq-unit-tests"></a>Ausführen von Komponenten Q# Tests

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Wechseln Sie als einmalige Einrichtung pro Lösung zum Menü **Test** , und wählen Sie **Testeinstellungen > Standard Prozessorarchitektur > x64**aus.

> [!TIP]
> Die Standardeinstellung für die Prozessorarchitektur für Visual Studio wird in der Projektmappendatei ( `.suo` ) für jede Lösung gespeichert.
> Wenn Sie diese Datei löschen, müssen Sie **x64** als Prozessorarchitektur erneut auswählen.

Erstellen Sie das Projekt, öffnen Sie das Menü " **Test** ", und wählen Sie **Windows > Test-Explorer**aus. " **Zustellungs Zuordnung** " wird in der Liste der Tests in der Gruppe " **nicht ausgeführt Tests** " angezeigt. Wählen Sie **alle ausführen** aus, oder führen Sie den einzelnen Test aus.

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Navigieren Sie zum Ausführen von Tests zum Projektordner (dem Ordner, der enthält `Tests.csproj` ), und führen Sie den folgenden Befehl aus:

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

Komponententests können nach Ihrem Namen oder dem Ausführungs Ziel gefiltert werden:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> weist `(String -> Unit)` den Typ auf und ermöglicht die Erstellung von Diagnosemeldungen.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test klicken, wird ein Panel mit Informationen zur Testausführung angezeigt: Status "erfolgreich/fehlgeschlagen", verstrichene Zeit und ein Link zur Ausgabe. Klicken Sie auf **Ausgabe** , um die Test Ausgabe in einem neuen Fenster zu öffnen.

![Test Ausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Der Status "erfolgreich/fehlgeschlagen" für jeden Test wird von auf der Konsole gedruckt `dotnet test` .
Bei fehlgeschlagenen Tests werden die Ausgaben auch in der Konsole gedruckt, um den Fehler zu diagnostizieren.

***

## <a name="facts-and-assertions"></a>Fakten und Assertionen

Da Funktionen in Q# keine _logischen_ Nebeneffekte haben, können Sie innerhalb eines Programms niemals davon Q# ausgehen, dass eine Funktion, deren Ausgabetyp ein leeres Tupel ist, von einem Programm aus ausgeführt wird `()` .
Das heißt, ein Zielcomputer kann festlegen, dass keine Funktion ausgeführt werden soll, die `()` mit der Garantie zurückgibt, dass diese Auslassung das Verhalten eines nachfolgenden Codes nicht ändert Q# .
Dieses Verhalten bewirkt, dass Funktionen, die zurückgeben `()` (z.b. `Unit` ), ein nützliches Tool zum Einbetten von Assertionen und zum Debuggen von Q# 

Betrachten wir ein einfaches Beispiel:

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

Hier gibt das Schlüsselwort an, `fail` dass die Berechnung nicht fortgesetzt werden soll, und löst eine Ausnahme auf dem Zielcomputer aus, auf dem das Programm ausgeführt wird Q# .
Definitionsgemäß kann ein Fehler dieser Art nicht innerhalb von erkannt werden Q# , da der Zielcomputer den Code nicht mehr ausführt, Q# nachdem eine Anweisung erreicht wurde `fail` .
Wenn wir also einen Rückruf von fortsetzen `PositivityFact` , können wir sicher sein, dass die Eingabe positiv ist.

Beachten Sie, dass das gleiche Verhalten wie die `PositivityFact` Verwendung der- [`Fact`](xref:microsoft.quantum.diagnostics.fact) Funktion aus dem-Namespace implementiert werden kann <xref:microsoft.quantum.diagnostics> :

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

Assertionen werden dagegen ähnlich wie Fakten *verwendet, hängen*jedoch möglicherweise vom Status des Ziel Computers ab. Dementsprechend werden Sie als Vorgänge definiert, wohingegen Fakten als Funktionen definiert werden (wie im vorherigen Beispiel).
Um den Unterschied zu verstehen, sollten Sie die folgende Verwendung eines Fakts innerhalb einer Aussage in Erwägung gezogen haben:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Hier wird der-Vorgang verwendet <xref:microsoft.quantum.environment.getqubitsavailabletouse> , um die Anzahl der zu verwendenden Qubits zurückzugeben.
Da dies von dem globalen Status des Programms und seiner Ausführungsumgebung abhängt, muss unsere Definition von `AssertQubitsAreAvailable` ebenfalls ein Vorgang sein.
Der globale Status kann jedoch verwendet werden, um einen einfachen `Bool` Wert als Eingabe für die Funktion zu erhalten `Fact` .

[Der Auftakt](xref:microsoft.quantum.libraries.standard.prelude), auf dem diese Ideen aufbauen, bietet zwei besonders nützliche Assertionen, die <xref:microsoft.quantum.diagnostics.assertmeasurement> <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> beide als Vorgänge für modelliert werden `()` . Diese Assertionen akzeptieren jeweils einen Pauli-Operator, der ein bestimmtes Maß an Interesse, ein Quantum-Register, für das eine Messung durchgeführt wird, und ein hypothetisches Ergebnis beschreibt.
Zielcomputer, die bei der Simulation arbeiten, werden nicht durch [das No-Klon-Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen ausführen, ohne das Register zu beeinträchtigen, das an solche Assertionen weitergeleitet wird.
Ein Simulator kann dann, ähnlich wie bei der `PositivityFact` vorherigen Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beachtet wird:

```qsharp
using (register = Qubit()) 
{
    H(register);
    AssertMeasurement([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

Bei physischer Quantum-Hardware, bei der das No-Klon-Theorem die Untersuchung eines Quantum-Zustands verhindert, werden die `AssertMeasurement` -und- `AssertMeasurementProbability` Vorgänge einfach `()` ohne andere Auswirkungen zurückgegeben.

Der- <xref:microsoft.quantum.diagnostics> Namespace stellt mehrere weitere Funktionen der- `Assert` Familie bereit, mit denen Sie erweiterte Bedingungen überprüfen können. 

## <a name="dump-functions"></a>Dumpfunktionen

Zur Unterstützung der Problembehandlung von Quantum-Programmen bietet der- <xref:microsoft.quantum.diagnostics> Namespace zwei Funktionen, mit denen der aktuelle Status des Ziel Computers in einer Datei gespeichert werden kann: <xref:microsoft.quantum.diagnostics.dumpmachine> und <xref:microsoft.quantum.diagnostics.dumpregister> . Die generierte Ausgabe hängt von dem Zielcomputer ab.

### <a name="dumpmachine"></a>DumpMachine

Der als Teil des Quantum Development Kit verteilte Volltext-Quantum-Simulator schreibt in die Datei der [Wave-Funktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantum-Systems. als eindimensionales Array komplexer Zahlen, bei dem jedes Element die Amplitude der Wahrscheinlichkeits Wahrscheinlichkeit für die Messung des Berechnungsbasis Zustands $ \ket{n} $ darstellt, wobei $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ für Bits $ \{ b_i \} $. Beispielsweise wird auf einem Computer, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\call{(1 + i)} {2} \ket die folgende {10} <xref:microsoft.quantum.diagnostics.dumpmachine> Ausgabe generiert:

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.
In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{n} $ im kartesischen und Polar Format beschrieben. Im Detail für die erste Zeile:

* **`∣0❭:`** Diese Zeile entspricht dem `0` Status der Berechnungs Ebene.
* **`0.707107 +  0.000000 i`**: die Wahrscheinlichkeits Amplitude im kartesischen Format.
* **` == `**: das `equal` Vorzeichen trennt beide äquivalente Darstellungen.
* **`**********  `**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen.
* **`[ 0.500000 ]`**: der numerische Wert der Größe.
* **`    ---`**: Eine grafische Darstellung der Amplitude-Phase (Weitere Informationen finden Sie in der folgenden Ausgabe).
* **`[ 0.0000 rad ]`**: der numerische Wert der Phase (im Bogenmaße).

Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt. Die Größen Darstellung ist geradlinig: Sie zeigt einen Balken an `*` , je größer die Wahrscheinlichkeit, mit der die Leiste größer wird. In der Phase zeigen wir die folgenden Symbole zur Darstellung des Winkels basierend auf Bereichen:

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

Die folgenden Beispiele zeigen `DumpMachine` einige allgemeine Zustände:

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
  > Die ID eines Qubit wird zur Laufzeit zugewiesen und ist nicht notwendigerweise an die Reihenfolge ausgerichtet, in der das Qubit zugewiesen wurde, oder an seine Position in einem Qubit-Register.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Sie können in Visual Studio eine Qubit-ID suchen, indem Sie einen Haltepunkt in Ihrem Code platzieren und den Wert einer Qubit-Variablen untersuchen, z. b.:
  > 
  > ![Anzeigen der Qubit-ID in Visual Studio](~/media/qubit_id.png)
  >
  > Das Qubit mit Index `0` on `register2` hat ID = `3` , das Qubit mit dem Index `1` hat ID = `2` .

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Sie können eine Qubit-ID suchen, indem Sie die <xref:microsoft.quantum.intrinsic.message> -Funktion verwenden und die Qubit-Variable in der Nachricht übergeben, z. b.:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > Dies könnte folgende Ausgabe generieren:
  >```
  > 0=q:3; 1=q:2
  >```
  > Dies bedeutet, dass das Qubit mit dem Index `0` on `register2` ID = ist `3` , das Qubit mit Index `1` ID = `2` .


***

Da <xref:microsoft.quantum.diagnostics.dumpmachine> Teil des- <xref:microsoft.quantum.diagnostics> Namespace ist, müssen Sie eine-Anweisung hinzufügen, `open` um darauf zugreifen zu können:

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


### <a name="dumpregister"></a>DumpRegister

<xref:microsoft.quantum.diagnostics.dumpregister>funktioniert wie <xref:microsoft.quantum.diagnostics.dumpmachine> , mit der Ausnahme, dass es auch ein Array von Qubits verwendet, um die Menge der Informationen auf die für die entsprechenden Qubits relevanten Informationen einzuschränken.

Wie bei <xref:microsoft.quantum.diagnostics.dumpmachine> hängen die von generierten Informationen vom <xref:microsoft.quantum.diagnostics.dumpregister> Zielcomputer ab. Für den vollständigen Quantum-Simulator schreibt er in die Datei, die von der Wave-Funktion bis zu einer globalen Phase des von den bereitgestellten Qubits generierten Quantums in demselben Format wie angegeben wird <xref:microsoft.quantum.diagnostics.dumpmachine> .  Nehmen Sie z. b. erneut einen Computer an, dem nur zwei Qubits zugeordnet sind, und im Quantum-Status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\bruch {(1 + i)} {2} \ket {10} =-e. ^ {-i \ pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\bruch{(1 + i)} {2} \ket {1} ) \otimes \bruchteil {-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ beim Aufrufen <xref:microsoft.quantum.diagnostics.dumpregister> von wird `qubit[0]` Diese Ausgabe generiert:

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

durch <xref:microsoft.quantum.diagnostics.dumpregister> das Aufrufen von für wird `qubit[1]` Diese Ausgabe generiert:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Im Allgemeinen ist der Status eines Registers, das mit einem anderen Register entkoppelt ist, ein gemischter Zustand und kein reiner Zustand. In diesem Fall wird <xref:microsoft.quantum.diagnostics.dumpregister> die folgende Meldung ausgegeben:

```
Qubits provided (0;) are entangled with some other qubit.
```

Im folgenden Beispiel wird gezeigt, wie Sie sowohl <xref:microsoft.quantum.diagnostics.dumpregister> als auch <xref:microsoft.quantum.diagnostics.dumpmachine> in Ihrem Q# Code verwenden können:

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

Zusätzlich zu den `Assert` `Dump` Funktionen und Vorgängen von und Q# unterstützt eine Teilmenge der standardmäßigen Visual Studio-Debugfunktionen: das [Festlegen von Zeilen Haltepunkten](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), das schrittweise [durchlaufen von Code mit F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)und das Überprüfen [von Werten klassischer Variablen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) ist während der Codeausführung im Simulator möglich.

Beim Debuggen in Visual Studio Code werden die Debuggingfunktionen von c# für Visual Studio Code Erweiterung von omnisharp genutzt, und die [neueste Version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)muss installiert werden. 
