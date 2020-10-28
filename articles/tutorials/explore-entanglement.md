---
title: Entdecken Sie jede Verflechtungen mit Q#
description: Erfahren Sie, wie Sie ein Quantum-Programm in schreiben Q# . Entwickeln Sie eine Bell-Zustandsanwendung mithilfe des Quantum Development Kit (QDK)
author: geduardo
ms.author: v-edsanc
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
no-loc:
- Q#
- $$v
ms.openlocfilehash: 7a1a49e18ac9330ca6e3cc89b3e58c96eccb91db
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691669"
---
# <a name="tutorial-explore-entanglement-with-q"></a>Tutorial: Erkunden der Verschränkung mit Q\#

In diesem Tutorial zeigen wir Ihnen, wie Sie ein Q# Programm schreiben, das Qubits manipuliert und misst und die Auswirkungen von Superposition und entanglement veranschaulicht.

Sie schreiben eine Anwendung mit dem Namen „Bell“, um die Quantenverschränkung zu veranschaulichen.
Der Name „Bell“ bezieht sich auf die Bell-Zustände. Hierbei handelt es sich um spezifische Quantenzustände von zwei Qubits, die zum Darstellen der einfachsten Beispiele für Überlagerungen und Quantenverschränkungen verwendet werden.

## <a name="pre-requisites"></a>Voraussetzungen

Führen Sie zunächst diese Schritte aus, wenn Sie bereit zum Codieren sind: 

* [Installieren](xref:microsoft.quantum.install) Sie das Quantum Development Kit mit Ihrer bevorzugten Sprache und Entwicklungsumgebung.
* Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde

Sie können auch mit der Erzählung arbeiten, ohne das QDK zu installieren, indem Sie die Übersichten der Q# Programmiersprache und die ersten Konzepte von Quantum Computing überprüfen.

## <a name="in-this-tutorial-youll-learn-how-to"></a>In diesem Tutorial lernen Sie Folgendes:

> [!div class="checklist"]
> * Erstellen und Kombinieren von Vorgängen in Q\#
> * Erstellen Sie Vorgänge zum Platzieren von Qubits in der superposition, entangle und messen.
> * Veranschaulichen von Quantum jede Verflechtungen mit einem Programm, das Q# in einem Simulator ausgeführt wird. 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a>Demonstrieren des Qubit-Verhaltens mit dem QDK

Klassische Bits enthalten einen einzelnen binären Wert (0 oder 1). Der Zustand eines [Qubits](xref:microsoft.quantum.glossary#qubit) kann dagegen eine **Superposition** sein (also 0 und 1).  Konzeptionell kann der Zustand eines Qubit als Richtung in einem abstrakten Raum (auch als Vektor bezeichnet) betrachtet werden.  Ein Qubit-Zustand kann sich in einer der möglichen Richtungen befinden. Die beiden **klassischen Zustände** sind die beiden Richtungen, die für die einhundertprozentige Chance einer Messung von 0 und die einhundertprozentige Chance einer Messung von 1 stehen.

Mit dem Messvorgang wird ein binäres Ergebnis erzeugt und ein Qubit-Zustand geändert.
Die Messung erzeugt einen binären Wert, entweder 0 oder 1.  Das Qubit geht von einem Überlagerungszustand (beliebige Richtung) in einen der klassischen Zustände über.  Danach führt die Wiederholung der gleichen Messung ohne Eingriff zu demselben binären Ergebnis.  

Mehrere Qubits können [**verschränkt**](xref:microsoft.quantum.glossary#entanglement) sein.  Bei der Messung eines verschränkten Qubits wird unsere Kenntnis des Zustands der anderen Qubits ebenfalls aktualisiert.

Nun können wir veranschaulichen, wie Q# dieses Verhalten ausdrückt.  Sie beginnen mit dem einfachsten möglichen Programm und erweitern es anschließend, um die Quantenüberlagerung und -verschränkung zu demonstrieren.

## <a name="creating-a-no-locq-project"></a>Erstellen eines Q# Projekts

Als erstes müssen Sie ein neues Q# Projekt erstellen. In diesem Tutorial verwenden wir die Umgebung auf der Grundlage von [ Q# Anwendungen mit vs Code](xref:microsoft.quantum.install.standalone).

So erstellen Sie ein neues Projekt in vs Code: 

1. Klicken Sie auf **Ansicht** -> **Befehlspalette** , und wählen Sie **Q#: Neues Projekt erstellen** aus.
2. Klicken Sie auf **Standalone console application** (Eigenständige Konsolenanwendung).
3. Navigieren Sie zum Speicherort für die Speicherung des Projekts, und klicken Sie auf **Projekt erstellen** .
4. Klicken Sie nach der erfolgreichen Erstellung des Projekts unten rechts auf **Open new project...** (Neues Projekt öffnen...).

In diesem Fall haben wir das Projekt aufgerufen `Bell` . Hierdurch werden zwei Dateien generiert: `Bell.csproj` , die Projektdatei und `Program.qs` , eine Vorlage einer-Anwendung, die Q# wir zum Schreiben der Anwendung verwenden. Der Inhalt von `Program.qs` sollte wie folgt lauten:

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a>Schreiben der Q- \# Anwendung
 
Unser Ziel ist es, zwei Qubits in einem bestimmten Quantum-Zustand vorzubereiten. Dies veranschaulicht, wie Sie mit Qubits in arbeiten, Q# um ihren Zustand zu ändern und die Auswirkungen von Superposition und entanglement zu veranschaulichen. Wir erstellen Dies Stück für Stück, um Qubit-Zustände,-Vorgänge und-Messungen vorzustellen.

### <a name="initialize-qubit-using-measurement"></a>Initialisieren von Qubit mithilfe von Messungen

Im ersten Code Ausschnitt unten wird gezeigt, wie Sie in mit Qubits arbeiten Q# .  Wir führen zwei Vorgänge ein, [`M`](xref:Microsoft.Quantum.Intrinsic.m) die [`X`](xref:Microsoft.Quantum.Intrinsic.X) den Zustand eines Qubit transformieren. In diesem Codeausschnitt wird der Vorgang `SetQubitState` definiert, für den als Parameter ein Qubit verwendet wird, sowie ein weiterer Parameter `desired`, mit dem der gewünschte Zustand für das Qubit dargestellt wird.  Der Vorgang `SetQubitState` führt eine Messung für das Qubit durch, indem der Vorgang `M` verwendet wird.  In Q# gibt eine Qubit-Messung immer entweder `Zero` oder zurück `One` .  Wenn die Messung einen Wert zurückgibt, der nicht gleich dem gewünschten Wert ist, wird `SetQubitState` das Qubit geflippt, d. h., es wird ein `X` Vorgang ausgeführt, der den Qubit-Zustand in einen neuen Zustand ändert, in dem die Wahrscheinlichkeiten eines Messwerts, der zurück `Zero` gibt, und `One` umgekehrt werden. Auf diese Weise wird `SetQubitState` das Ziel-Qubit immer in den gewünschten Zustand versetzt.

Ersetzen Sie den Inhalt von `Program.qs` durch den folgenden Code:


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

Dieser Vorgang kann jetzt aufgerufen werden, um ein Qubit auf einen klassischen Zustand festzulegen, indem entweder immer `Zero` oder immer `One` zurückgegeben wird.
`Zero` und `One` sind Konstanten, die die beiden einzigen möglichen Ergebnisse der Messung eines Qubits darstellen.

Mit dem Vorgang `SetQubitState` wird das Qubit gemessen. Wenn sich das Qubit im gewünschten Zustand befindet, `SetQubitState` bleibt es unverändert `X` . andernfalls ändern wir den Qubit-Zustand in den gewünschten Zustand, wenn der Vorgang ausgeführt wird.

#### <a name="about-no-locq-operations"></a>Informationen zu Q# Vorgängen

Ein- Q# Vorgang ist eine Quantum-Unterroutine. Das heißt, es handelt sich um eine Aufruf Bare Routine, die Aufrufe von anderen Quantum-Vorgängen enthält.

Die Argumente für eine Operation werden als Tupel angegeben, in Klammern eingeschlossen.

Der Rückgabetyp der Operation wird nach einem Doppelpunkt angegeben. In diesem Fall weist der `SetQubitState` Vorgang keinen Rückgabetyp auf, sodass er als zurückgegeben gekennzeichnet ist `Unit` . Dies Q# entspricht `unit` in F #, das ungefähr analog zu `void` in c# ist, und ein leeres Tupel in python ( `()` , dargestellt durch den Typhinweis `Tuple[()]` ).

Sie haben im ersten Vorgang zwei Quantum-Vorgänge verwendet Q# :

* Der [`M`](xref:Microsoft.Quantum.Intrinsic.m) Vorgang, der den Zustand des Qubit misst.
* Der [`X`](xref:Microsoft.Quantum.Intrinsic.X) Vorgang, der den Zustand eines Qubit kippt.

Mit einem Quantenvorgang wird der Zustand eines Qubits transformiert. Analog zu klassischen Logikgattern wird anstelle von Vorgängen auch von Quantengattern gesprochen. Diese Bezeichnung stammt aus den Anfängen des Quantencomputings, als Algorithmen lediglich ein theoretisches Konstrukt waren und in Form von Diagrammen visualisiert wurden – ähnlich wie bei einem Schaltplan im Bereich des klassischen Computings.

### <a name="counting-measurement-outcomes"></a>Zählen der Messergebnisse

Zur Veranschaulichung der Auswirkungen des Vorgangs `SetQubitState` wird dann der Vorgang `TestBellState` hinzugefügt. Für diesen Vorgang wird `Zero` oder `One` als Eingabe verwendet, und der Vorgang `SetQubitState` wird einige Male mit dieser Eingabe aufgerufen. Es wird gezählt, wie oft bei der Messung des Qubits `Zero` und wie oft `One` zurückgegeben wird. Bei der ersten Simulation des Vorgangs `TestBellState` erwarten wir natürlich, dass in der Ausgabe für alle Messungen des Qubits mit `Zero` als Parametereingabe `Zero` und für alle Messungen eines Qubits mit `One` als Parametereingabe `One` zurückgegeben wird. Im weiteren Verlauf fügen wir Code hinzu, `TestBellState` um Superposition und entanglement zu veranschaulichen.

Fügen Sie der `Program.qs`-Datei die folgende Operation hinzu, innerhalb des Namespaces, nach dem Ende der `SetQubitState`-Operation:

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
Beachten Sie, dass wir eine Zeile vor hinzugefügt haben `return` , um eine erklärende Nachricht in der-Konsole mit der-Funktion ( `Message` ) [Microsoft. Quantum. intrinsi. Message] zu drucken.

Diese Operation (`TestBellState`) iteriert `count` Iterationen lang in einer Schleife, legt einen angegebenen `initial`-Wert für ein Qubit fest, und misst (`M`) dann das Ergebnis. Sie führt eine Statistik zur Anzahl der gemessenen Nullen und Einsen und gibt diese an den Aufrufer zurück. Sie führt eine weitere erforderliche Operation aus. Sie setzt das Qubit auf einen bekannten Zustand (`Zero`) zurück, bevor sie es zurückgibt, was es anderen ermöglicht, dieses Qubit in einem bekannten Zustand zuzuweisen. Dies ist aufgrund der `using`-Anweisung erforderlich.

#### <a name="about-variables-in-q"></a>Informationen zu Variablen in Q\#

Standardmäßig sind Variablen in Q# unveränderlich; ihr Wert kann nicht geändert werden, nachdem Sie gebunden wurden. Das `let`-Schlüsselwort wird verwendet, um die Bindung einer unveränderlichen Variable anzugeben. Operationsargumente sind immer unveränderlich.

Wenn Sie eine Variable benötigen, deren Wert geändert werden kann, wie etwa `numOnes` im Beispiel, können Sie die Variable mit dem Schlüsselwort `mutable` deklarieren. Der Wert einer veränderlichen Variable kann mithilfe einer `set`-Anweisung geändert werden.

In beiden Fällen wird der Typ einer Variablen vom Compiler abgeleitet. Q# Es sind keine Typanmerkungen für Variablen erforderlich.

#### <a name="about-using-statements-in-q"></a>Informationen zu `using` Anweisungen in Q\#

Die- `using` Anweisung ist auch speziell für Q# . Sie wird verwendet, um Qubits für die Verwendung in einem Codeblock zuzuweisen. In Q# werden alle Qubits dynamisch zugeordnet und freigegeben, anstatt fixierte Ressourcen zu sein, die für die gesamte Lebensdauer eines komplexen Algorithmus vorhanden sind. Eine `using`-Anweisung weist eine Reihe Qubits am Anfang zu und gibt diese Qubits am Ende des Blocks wieder frei.

## <a name="run-the-code-from-the-command-prompt"></a>Ausführen des Codes an der Eingabeaufforderung

Um den Code ausführen zu können, müssen Sie den Compiler anweisen *, welche* Funktion beim Bereitstellen des Befehls ausgeführt werden kann `dotnet run` . Dies erfolgt mit einer einfachen Änderung in der Q# Datei, indem eine Zeile hinzugefügt wird, die `@EntryPoint()` direkt vor der Aufruf baren Zeile steht: der `TestBellState` Vorgang in diesem Fall. Der vollständige Code sollte wie folgt lauten:

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

Um das Programm auszuführen, müssen Sie die `count` Argumente und an `initial` der Eingabeaufforderung angeben. Wählen Sie z. b `count = 1000` . und aus `initial = One` . Geben Sie den folgenden Befehl ein:

```dotnetcli
dotnet run --count 1000 --initial One
```

Und Sie sollten die folgende Ausgabe beachten:

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

Wenn Sie mit versuchen, `initial = Zero` sollten Sie Folgendes beachten:

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a>Vorbereiten von Überlagerung

Sehen wir uns nun an, wie die Q# Methoden zum Platzieren von Qubits in der superposition ausdrückt.  Sie wissen bereits, dass der Zustand eines Qubits den Überlagerungswert 0 und 1 aufweisen kann.  Wir verwenden den Vorgang `Hadamard`, um dies zu erreichen. Wenn das Qubit einen der klassischen Zustände aufweist (bei dem für eine Messung immer `Zero` oder immer `One` zurückgegeben wird), versetzt der Vorgang `Hadamard` bzw. `H` das Qubit in einen Zustand, in dem für eine Messung des Qubits in 50 % der Fälle `Zero` und in 50 % der Fälle `One` zurückgegeben wird.  Sie können sich das Qubit als Mischung von `Zero` und `One` vorstellen.  Wenn wir nun den Vorgang `TestBellState` simulieren, sehen wir nach der Messung, dass ungefähr mit der gleichen Häufigkeit `Zero` und `One` als Ergebnis zurückgegeben wird.  

### <a name="x-flips-qubit-state"></a>`X` kippt-Qubit-Status

Zuerst versuchen wir, das Qubit zu kippen (wenn sich das Qubit im `Zero` Zustand befindet, wird es zu `One` und umgekehrt). Dies wird dadurch erreicht, dass wir den Vorgang `X` durchführen, bevor die Messung in `TestBellState` erfolgt:

```qsharp
X(qubit);
let res = M(qubit);
```

Nun werden die Ergebnisse umgekehrt:

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

Sehen wir uns nun die Quantum-Eigenschaften der Qubits an.

### <a name="h-prepares-superposition"></a>`H` bereitet die Superposition vor

Hierfür müssen wir lediglich den Vorgang `X` in der vorherigen Ausführung durch den Vorgang `H` (Hadamard-Vorgang) ersetzen. Statt das Qubit ganz von 0 in 1 umzukehren, kehren wir es nur halb um. Die ersetzten Zeilen in `TestBellState` sehen jetzt so aus:

```qsharp
H(qubit);
let res = M(qubit);
```

Jetzt werden die Ergebnisse interessanter:

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

Jedes Mal, wenn wir messen, fragen wir nach einem klassischen Wert, aber das Qubit befindet sich auf halbem Weg zwischen 0 und 1, also erhalten wir (statistisch) die Hälfte der Zeit 0 und die Hälfte der Zeit 1.
Dies wird als **Überlagerung** bezeichnet und gibt uns unseren ersten echten Einblick in einen Quantenzustand.

## <a name="prepare-entanglement"></a>Vorbereiten von Verschränkung

Sehen wir uns nun an Q# , wie Methoden zum entangle-Qubits ausdrückt.
Zuerst legen wir das erste Qubit auf den Anfangszustand fest und verwenden dann den Vorgang `H`, um die Überlagerung zu erzielen.  Bevor wir das erste Qubit Messen, verwenden wir dann einen neuen Vorgang ( `CNOT` ), der für " *kontrolliert-not* " steht.  Das Ergebnis der Ausführung dieses Vorgangs auf zwei Qubits besteht darin, das zweite Qubit auszuklappen, wenn das erste Qubit ist `One` .  Die beiden Qubits sind nun verschränkt.  Unsere Statistiken für das erste Qubit haben sich nicht geändert (50:50-Wahrscheinlichkeit für `Zero` oder `One` nach der Messung), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits. Unser `CNOT` hat die zwei Qubits verschränkt, sodass was immer mit dem einen von ihnen geschieht, auch mit dem anderen geschieht. Wenn Sie die Messungen umkehrten (das zweite Qubit vor dem ersten messen), würde das Gleiche passieren. Die erste Messung wäre zufällig, und die zweite wäre im Gleichschritt mit dem, was bei der ersten herausgefunden wurde.

Als erstes müssen wir zwei Qubits anstelle eines in zuordnen `TestBellState` :

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

Dies ermöglicht es uns, einen neuen Vorgang (`CNOT`) hinzuzufügen, bevor wir in `TestBellState` die Messung (`M`) durchführen:

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

Wir haben eine weitere `SetQubitState`-Operation hinzugefügt, um das erste Qubit zu initialisieren, um sicherzustellen, dass es sich anfangs immer im `Zero`-Zustand befindet.

Wir müssen außerdem das zweite Qubit zurücksetzen, bevor wir es freigeben.

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

Die vollständige Routine sieht jetzt so aus:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

Wenn wir dies ausführen, erhalten wir exakt das gleiche 50-50-Ergebnis, das wir zuvor erhalten haben. Woran wir interessiert sind, ist aber die Reaktion des zweiten Qubits auf die Messung des ersten. Wir fügen diese Statistik mit einer neuen Version der `TestBellState`-Operation hinzu:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

Der neue Rückgabewert (`agree`) hält fest, wenn die Messung des ersten Qubits mit der Messung des zweiten Qubits übereinstimmt.

Der folgende Code wird ausgeführt:

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

Wie in der Übersicht beschrieben, haben sich unsere Statistiken für das erste Qubit nicht geändert (50:50-Wahrscheinlichkeit für 0 oder 1), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits, weil sie verschränkt sind.

## <a name="next-steps"></a>Nächste Schritte

Im Lernprogramm [Grover](xref:microsoft.quantum.quickstarts.search) finden Sie Informationen zum Erstellen und Ausführen der Grover-Suche, einer der gängigsten Quantum Computing-Algorithmen und bietet ein gutes Beispiel für ein Q# Programm, das verwendet werden kann, um reale Probleme mit Quantum Computing zu lösen.  

In den ersten Schritten [mit dem Quantum Development Kit werden](xref:microsoft.quantum.welcome) weitere Möglichkeiten zum Erlernen Q# und der quantumprogrammierung empfohlen.
