---
title: Testen und Debuggen von Q-Programmen
description: Erfahren Sie, wie Sie Komponententests, Fakten und Assertionen verwenden und Funktionen zum Testen und Debuggen von Quantenprogrammen absetzen.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030581"
---
# <a name="testing-and-debugging"></a>Testen und Debuggen

Wie bei der klassischen Programmierung ist es wichtig, in der Lage zu sein, zu überprüfen, ob Quantenprogramme wie beabsichtigt wirken, und in der Lage zu sein, ein Quantenprogramm zu diagnostizieren, das falsch ist.
In diesem Abschnitt behandeln wir die Tools, die von Q- zum Testen und Debuggen von Quantenprogrammen angeboten werden.

## <a name="unit-tests"></a>Komponententests

Ein gängiger Ansatz zum Testen klassischer Programme besteht darin, kleine Programme zu schreiben, die *als Komponententests* bezeichnet werden und Code in einer Bibliothek ausführen, und die Ausgabe mit einer erwarteten Ausgabe zu vergleichen.
Zum Beispiel können wir sicherstellen, dass `Square(2)` die Rückgabe, `4`da wir von *vornherein* wissen, dass 2 , 2 = 4 .

Die Q-Datei unterstützt das Erstellen von Komponententests für Quantenprogramme, die als Tests innerhalb des xUnit-Komponententestframeworks ausgeführt werden können. [xUnit](https://xunit.github.io/)

### <a name="creating-a-test-project"></a>Erstellen eines Testprojekts

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Öffnen Sie Visual Studio 2019. Gehen Sie `File` zum `New`  >  `Project...`Menü und wählen Sie .
Suchen Sie in der `Q#`oberen rechten `Q# Test Project` Ecke nach , und wählen Sie die Vorlage aus.

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Führen Sie in Ihrer bevorzugten Befehlszeile den folgenden Befehl aus:
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

Das neue Projekt verfügt `Tests.qs`über eine einzelne Datei , die einen bequemen Ort zum Definieren neuer Q-Komponententests bietet.
Zunächst enthält diese Datei `AllocateQubit` einen Beispielkomponententest, der überprüft, ob{0}sich ein neu zugewiesenes Qubit im Zustand .'ket' befindet, und eine Meldung ausgibt:

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:neu: Jede Operation oder Funktion von Qa, die ein Argument des Typs `Unit` und die Rückgaben `Unit` annimmt, kann über das `@Test("...")` Attribut als Komponententest markiert werden. Das Argument für `"QuantumSimulator"` dieses Attribut oben gibt das Ziel an, auf dem der Test ausgeführt wird. Ein einzelner Test kann auf mehreren Zielen ausgeführt werden. Fügen Sie z. `@Test("ResourcesEstimator")` `AllocateQubit`B. ein Attribut oben hinzu. 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
Speichern Sie die Datei, und führen Sie alle Tests aus. Es sollte nun zwei Komponententests geben, einen, bei dem AllocateQubit auf dem QuantumSimulator ausgeführt wird, und einen, bei dem es im ResourceEstimator ausgeführt wird. 

Die integrierten Ziele "QuantumSimulator", "ToffoliSimulator" und "ResourcesEstimator" werden als gültige Ausführungsziele für Komponententests erkannt. Es ist auch möglich, einen vollqualifizierten Namen anzugeben, um ein benutzerdefiniertes Ausführungsziel zu definieren. 

### <a name="running-q-unit-tests"></a>Ausführen von Q-Unit-Tests

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Gehen Sie als einmaliges Setup pro `Test` Lösung `Test Settings`  >  `Default Processor Architecture`  > zum Menü und wählen Sie `X64`aus.

> [!TIP]
> Die Standardeinstellung für die Prozessorarchitektur für Visual`.suo`Studio wird in der Projektmappenoptionendatei ( ) für jede Projektmappe gespeichert.
> Wenn Sie diese Datei löschen, müssen `X64` Sie die Prozessorarchitektur erneut auswählen.

Erstellen Sie das Projekt, gehen Sie zum `Test` Menü und wählen Sie `Windows`  >  `Test Explorer`. `AllocateQubit`wird in der Liste der `Not Run Tests` Tests in der Gruppe angezeigt. Wählen `Run All` oder führen Sie diesen individuellen Test aus, und er sollte bestehen!

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Um Tests auszuführen, navigieren Sie zum Projektordner (dem Ordner, der enthält `Tests.csproj`), und führen Sie den Befehl aus:

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

Komponententests können nach ihrem Namen und/oder dem Ausführungsziel gefiltert werden:

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

Die intrinsische Funktion <xref:microsoft.quantum.intrinsic.message> hat den Typ `(String -> Unit)` und ermöglicht die Erstellung von Diagnosemeldungen.

#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

Nachdem Sie einen Test im Test-Explorer ausgeführt und auf den Test geklickt haben, wird ein Bereich mit Informationen zur Testausführung angezeigt: Status "Übergeben/fehlgeschlagen", verstrichene Zeit und ein "Output"-Link. Wenn Sie auf den Link "Ausgabe" klicken, wird die Testausgabe in einem neuen Fenster geöffnet.

![Testausgabe](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

Der Status "Pass/Fail" für jeden `dotnet test`Test wird von auf der Konsole gedruckt.
Bei fehlerhaften Tests werden die Ausgaben auch auf die Konsole gedruckt, um den Fehler zu diagnostizieren.

***

## <a name="facts-and-assertions"></a>Fakten und Behauptungen

Da Funktionen in Q-A keine _logischen_ Nebenwirkungen haben, können alle _anderen Arten_ von `()` Effekten der Ausführung einer Funktion, deren Ausgabetyp das leere Tupel ist, niemals innerhalb eines Q-Programms beobachtet werden.
Das heißt, ein Zielcomputer kann keine Funktion `()` ausführen, die mit der Garantie zurückkehrt, dass diese Auslassung das Verhalten eines nachfolgenden Q-Codes nicht ändert.
Dies macht `()` die Rückgabe `Unit`von Funktionen (d. h. ) zu einem nützlichen Werkzeug zum Einbetten von Assertionen und Debuggen von Logik in Q-Programme. 

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

Hier gibt `fail` das Schlüsselwort an, dass die Berechnung nicht fortgesetzt werden soll, wodurch eine Ausnahme auf dem Zielcomputer ausgelöst wird, auf dem das Q-Programm ausgeführt wird.
Definitionsgemäß kann ein solcher Fehler nicht innerhalb von Q- und -Code `fail` beobachtet werden, da nach dem Erreichen einer Anweisung kein weiterer Q-Code ausgeführt wird.
Wenn wir also über einen `PositivityFact`Aufruf zu gehen, können wir sicher sein, dass sein Input positiv war.

Beachten Sie, dass wir `PositivityFact` das [`Fact`](xref:microsoft.quantum.diagnostics.fact) gleiche Verhalten <xref:microsoft.quantum.diagnostics> wie die Verwendung der Funktion aus dem Namespace implementieren können:

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

*Assertionen*hingegen werden ähnlich wie Fakten verwendet, können jedoch vom Status der Zielmaschine abhängen. Entsprechend werden sie als Vorgänge definiert, während Fakten als Funktionen definiert werden (wie oben).
Um die Unterscheidung zu verstehen, betrachten Sie die folgende Verwendung einer Tatsache innerhalb einer Behauptung:

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

Hier verwenden wir den <xref:microsoft.quantum.environment.getqubitsavailabletouse> Vorgang, um die Anzahl der qubits zurückzugeben, die zur Verfügung stehen.
Da dies eindeutig vom globalen Zustand des Programms und `AssertQubitsAreAvailable` seiner Ausführungsumgebung abhängt, muss unsere Definition von auch eine Operation sein.
Wir können diesen globalen Zustand jedoch `Bool` verwenden, um `Fact` einen einfachen Wert als Eingabe für die Funktion zu liefern.

Aufbauend auf diesen Ideen bietet [das Präludium](xref:microsoft.quantum.libraries.standard.prelude) zwei besonders nützliche Behauptungen, <xref:microsoft.quantum.intrinsic.assert> die <xref:microsoft.quantum.intrinsic.assertprob> beide als Operationen auf `()`modelliert werden. Diese Behauptungen nehmen jeweils einen Pauli-Operator, der eine bestimmte Messung des Interesses beschreibt, ein Quantenregister, an dem eine Messung durchgeführt werden soll, und ein hypothetisches Ergebnis.
Auf Zielmaschinen, die durch Simulation arbeiten, sind wir nicht an [den no-cloning Theorem](https://en.wikipedia.org/wiki/No-cloning_theorem)gebunden und können solche Messungen durchführen, ohne das Register zu stören, das an solche Behauptungen übergeben wird.
Ein Simulator kann dann, `PositivityFact` ähnlich wie die obige Funktion, die Berechnung abbrechen, wenn das hypothetische Ergebnis in der Praxis nicht beobachtet würde:

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

Auf physikalischer Quantenhardware, bei der der No-Cloning-Theorem die Untersuchung des Quantenzustands verhindert, kehren die `Assert` und `AssertProb` Operationen einfach ohne andere Wirkung zurück. `()`

Der <xref:microsoft.quantum.diagnostics> Namespace bietet mehrere `Assert` weitere Funktionen der Familie, die es uns ermöglichen, fortgeschrittenere Bedingungen zu überprüfen. 

## <a name="dump-functions"></a>Dump-Funktionen

Zur Fehlerbehebung bei <xref:microsoft.quantum.diagnostics> Quantenprogrammen bietet der Namespace zwei Funktionen, die <xref:microsoft.quantum.diagnostics.dumpmachine> den <xref:microsoft.quantum.diagnostics.dumpregister>aktuellen Status des Zielcomputers in eine Datei einlassen können: und . Die generierte Ausgabe der einzelnen abhängig enthatonen hängt von der Zielmaschine ab.

### <a name="dumpmachine"></a>DumpMachine

Der vollstaatliche Quantensimulator, der als Teil des Quantum Development Kit verteilt ist, schreibt in die Datei die [Wellenfunktion](https://en.wikipedia.org/wiki/Wave_function) des gesamten Quantensystems, als eindimensionales Array komplexer Zahlen, in dem jedes Element die Amplitude der Wahrscheinlichkeit darstellt, den Berechnungsbasiszustand zu messen, wobei "Ket" = "ket"b_.n-1" b_1b_0 für Bits\{b_i\}. Auf einem Computer mit nur zwei zugeordneten Qubits und im Quantenzustand wird z. B. die{1}Ausgabe des{2}Aufrufs <xref:microsoft.quantum.diagnostics.dumpmachine> {00} von "end" (""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""{2} {10}"""" """""""" """""""" """""""

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer signifikanten Reihenfolge.
Der Rest der Zeilen beschreibt die Wahrscheinlichkeitsamplitude der Messung des Basiszustandsvektors in kartesischen und polaren Formaten. Im Detail für die erste Zeile:

* **`∣0❭:`** Diese Zeile entspricht `0` dem Berechnungsbasiszustand
* **`0.707107 +  0.000000 i`**: die Wahrscheinlichkeitsamplitude im kartesischen Format.
* **` == `**: `equal` Das Zeichen trennt beide gleichwertigen Darstellungen.
* **`**********  `**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustandsvektor zu messen.
* **`[ 0.500000 ]`**: der numerische Wert der Magnitude
* **`    ---`**: Eine grafische Darstellung der Amplitudenphase (siehe unten).
* **`[ 0.0000 rad ]`**: der numerische Wert der Phase (in Radianten).

Sowohl die Größe als auch die Phase werden mit einer grafischen Darstellung dargestellt. Die Größendarstellung ist geradlinig: `*`Sie zeigt einen Balken von , je größer die Wahrscheinlichkeit, je größer der Balken wird. Für die Phase zeigen wir die folgenden Symbole, um den Winkel basierend auf Bereichen darzustellen:

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

Die folgenden `DumpMachine` Beispiele zeigen für einige allgemeine Zustände:

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
  > Die ID eines Qubits wird zur Laufzeit zugewiesen und ist nicht unbedingt an der Reihenfolge ausgerichtet, in der das Qubit zugewiesen wurde, oder seiner Position innerhalb eines Qubit-Registers.


#### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

  > [!TIP]
  > Sie können eine Qubit-ID in Visual Studio ermitteln, indem Sie einen Haltepunkt in Ihren Code eingeben und den Wert einer qubit-Variablen überprüfen, z. B.:
  > 
  > ![Qubit-ID in Visual Studio anzeigen](~/media/qubit_id.png)
  >
  > der qubit `0` mit `register2` dem`3`Index auf hat `1` id=`2`, das qubit mit index hat id= .

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-vscode)

  > [!TIP]
  > Sie können eine qubit-ID <xref:microsoft.quantum.intrinsic.message> herausfinden, indem Sie die Funktion verwenden und die qubit-Variable in der Nachricht übergeben, z. B.:
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > die diese Ausgabe generieren könnte:
  >```
  > 0=q:3; 1=q:2
  >```
  > was bedeutet, dass das `0` `register2` qubit`3`mit dem Index `1` auf id= hat, hat das qubit mit index id=`2`.


***

<xref:microsoft.quantum.diagnostics.dumpmachine>ist Teil <xref:microsoft.quantum.diagnostics> des Namespace, daher müssen Sie eine `open` Anweisung hinzufügen, um ihn verwenden zu können:

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

<xref:microsoft.quantum.diagnostics.dumpregister>funktioniert <xref:microsoft.quantum.diagnostics.dumpmachine>wie , außer es benötigt auch ein Array von Qubits, um die Menge an Informationen auf die für die entsprechenden Qubits relevanten zu beschränken.

Wie <xref:microsoft.quantum.diagnostics.dumpmachine>bei hängt die <xref:microsoft.quantum.diagnostics.dumpregister> von generierten Informationen vom Zielcomputer ab. Für den Vollzustands-Quantensimulator schreibt er die Wellenfunktion bis zu einer globalen Phase des Quantensubsystems <xref:microsoft.quantum.diagnostics.dumpmachine>in die Datei, die von den bereitgestellten Qubits im gleichen Format wie erzeugt wird.  Zum Beispiel, Nehmen Sie erneut einen Computer mit nur zwei zugeordneten Qubits und im Quantenzustand ,{1},,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""({2}{00} {2} {10} {1}(sqrt{2}{0} {2} {1} {2}{0} <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[0]` , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , , ,

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

und <xref:microsoft.quantum.diagnostics.dumpregister> `qubit[1]` aufrufen erzeugt diese Ausgabe:

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

Im Allgemeinen ist der Zustand eines Registers, das mit einem anderen Register verstrickt ist, ein gemischter Zustand und kein reiner Zustand. Gibt in <xref:microsoft.quantum.diagnostics.dumpregister> diesem Fall die folgende Meldung aus:

```
Qubits provided (0;) are entangled with some other qubit.
```

Das folgende Beispiel zeigt Ihnen, <xref:microsoft.quantum.diagnostics.dumpregister> <xref:microsoft.quantum.diagnostics.dumpmachine> wie Sie beides und in Ihrem Q-Code verwenden können:

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

Zusätzlich zu `Assert` `Dump` den Funktionen und Vorgängen unterstützt Qa eine Teilmenge der standardmäßigen Visual Studio-Debugfunktionen: [Festlegen von Zeilenhaltepunkten,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [Schrittweiseieren von Code mit F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) und [Überprüfen von Werten klassischer Variablen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) sind während der Codeausführung im Simulator möglich.

Das Debuggen in Visual Studio Code nutzt die Debugfunktionen, die von der von OmniSharp unterstützten Erweiterung "C" für Visual Studio-Code bereitgestellt werden, und erfordert die Installation der [neuesten Version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp). 
