---
title: Erkunden der Verschränkung mit Q#
description: Erfahren Sie, wie Sie ein Quantenprogramm in Q# schreiben. Entwickeln Sie eine Bell-Zustandsanwendung mithilfe des Quantum Development Kit (QDK)
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 16c93b3dd17363c06602529cb34e8fc84aadc7a8
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415421"
---
# <a name="tutorial-explore-entanglement-with-q"></a>Tutorial: Erkunden der Verschränkung mit Q\#

In diesem Tutorial erfahren Sie, wie Sie ein Q#-Programm schreiben, mit dem Qubits bearbeitet und gemessen werden können. Darüber hinaus werden die Auswirkungen von Superposition und Verschränkung veranschaulicht.

Sie schreiben eine Anwendung mit dem Namen „Bell“, um die Quantenverschränkung zu veranschaulichen.
Der Name „Bell“ bezieht sich auf die Bell-Zustände. Hierbei handelt es sich um spezifische Quantenzustände von zwei Qubits, die zum Darstellen der einfachsten Beispiele für Überlagerungen und Quantenverschränkungen verwendet werden.

## <a name="pre-requisites"></a>Voraussetzungen

Führen Sie zunächst diese Schritte aus, wenn Sie bereit zum Codieren sind: 

* [Installieren](xref:microsoft.quantum.install) Sie das Quantum Development Kit mit Ihrer bevorzugten Sprache und Entwicklungsumgebung.
* Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde

Sie können auch mit der Erzählung arbeiten, ohne das QDK zu installieren, indem Sie die Übersichten der Programmiersprache Q # und die ersten Konzepte von Quantum Computing überprüfen.

## <a name="in-this-tutorial-youll-learn-how-to"></a>In diesem Tutorial lernen Sie, wie die folgenden Aufgaben ausgeführt werden:

> [!div class="checklist"]
> * Erstellen und Kombinieren von Vorgängen in Q\#
> * Erstellen Sie Vorgänge zum Platzieren von Qubits in der superposition, entangle und messen.
> * Veranschaulichen von Quantum jede Verflechtungen mit einem f #-Programm, das in einem Simulator ausgeführt wird. 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a>Demonstrieren des Qubit-Verhaltens mit dem QDK

Klassische Bits enthalten einen einzelnen binären Wert (0 oder 1). Der Zustand eines [Qubits](xref:microsoft.quantum.glossary#qubit) kann dagegen eine **Superposition** sein (also 0 und 1).  Konzeptionell kann der Zustand eines Qubit als Richtung in einem abstrakten Raum (auch als Vektor bezeichnet) betrachtet werden.  Ein Qubit-Zustand kann sich in einer der möglichen Richtungen befinden. Die beiden **klassischen Zustände** sind die beiden Richtungen, die für die einhundertprozentige Chance einer Messung von 0 und die einhundertprozentige Chance einer Messung von 1 stehen.

Mit dem Messvorgang wird ein binäres Ergebnis erzeugt und ein Qubit-Zustand geändert.
Die Messung erzeugt einen binären Wert, entweder 0 oder 1.  Das Qubit geht von einem Überlagerungszustand (beliebige Richtung) in einen der klassischen Zustände über.  Danach führt die Wiederholung der gleichen Messung ohne Eingriff zu demselben binären Ergebnis.  

Mehrere Qubits können [**verschränkt**](xref:microsoft.quantum.glossary#entanglement) sein.  Bei der Messung eines verschränkten Qubits wird unsere Kenntnis des Zustands der anderen Qubits ebenfalls aktualisiert.

Nun können wir veranschaulichen, wie dieses Verhalten von Q# ausgedrückt wird.  Sie beginnen mit dem einfachsten möglichen Programm und erweitern es anschließend, um die Quantenüberlagerung und -verschränkung zu demonstrieren.

## <a name="creating-a-q-project"></a>Erstellen eines Q #-Projekts

Zuerst muss ein neues Q #-Projekt erstellt werden. In diesem Tutorial verwenden wir die Umgebung, die auf [Befehlszeilen Anwendungen mit vs Code](xref:microsoft.quantum.install.standalone)basiert.

So erstellen Sie ein neues Projekt in vs Code: 

1. Klicken **View**Sie auf  ->  **Befehls Palette** anzeigen, und wählen Sie **Q #: Neues Projekt erstellen**aus.
2. Klicken Sie auf **eigenständige Konsolenanwendung**.
3. Navigieren Sie zum Speicherort, um das Projekt zu speichern, und klicken Sie auf **Projekt erstellen**.
4. Wenn das Projekt erfolgreich erstellt wurde, klicken Sie auf **Neues Projekt öffnen...** in der unteren rechten Ecke.

In diesem Fall haben wir das Projekt aufgerufen `Bell` . Hierdurch werden zwei Dateien generiert: `Bell.csproj` , die Projektdatei und `Program.qs` , eine Vorlage einer Q #-Anwendung, die wir zum Schreiben der Anwendung verwenden. Der Inhalt von `Program.qs` sollte wie folgt lauten:

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
 
Unser Ziel ist die Festlegung eines spezifischen Quantenzustands für zwei Qubits. Hiermit soll demonstriert werden, wie Sie mit Q# bei Qubits vorgehen, um den Zustand zu ändern und die Auswirkungen von Überlagerung und Verschränkung zu veranschaulichen. Wir erstellen Dies Stück für Stück, um Qubit-Zustände,-Vorgänge und-Messungen vorzustellen.

### <a name="initialize-qubit-using-measurement"></a>Initialisieren von Qubit mithilfe von Messungen

Im ersten unten aufgeführten Code wird gezeigt, wie Sie in Q# mit Qubits arbeiten.  Wir führen zwei Vorgänge ein, [`M`](xref:microsoft.quantum.intrinsic.m) die [`X`](xref:microsoft.quantum.intrinsic.x) den Zustand eines Qubit transformieren. In diesem Codeausschnitt wird der Vorgang `SetQubitState` definiert, für den als Parameter ein Qubit verwendet wird, sowie ein weiterer Parameter `desired`, mit dem der gewünschte Zustand für das Qubit dargestellt wird.  Der Vorgang `SetQubitState` führt eine Messung für das Qubit durch, indem der Vorgang `M` verwendet wird.  In Q # gibt eine Qubit-Messung immer entweder `Zero` oder zurück `One` .  Wenn die Messung einen Wert zurückgibt, der nicht gleich dem gewünschten Wert ist, wird `SetQubitState` das Qubit geflippt, d. h., es wird ein `X` Vorgang ausgeführt, der den Qubit-Zustand in einen neuen Zustand ändert, in dem die Wahrscheinlichkeiten eines Messwerts, der zurück `Zero` gibt, und `One` umgekehrt werden. Auf diese Weise wird `SetQubitState` das Ziel-Qubit immer in den gewünschten Zustand versetzt.

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

Mit dem Vorgang `SetQubitState` wird das Qubit gemessen. Falls sich das Qubit im gewünschten Zustand befindet, wird es von `SetQubitState` unverändert gelassen. Andernfalls ändern wir den Qubit-Zustand in den gewünschten Zustand, indem wir den Vorgang `X` ausführen.

#### <a name="about-q-operations"></a>Informationen zu Q#-Vorgängen

Ein Q#-Vorgang ist eine Quantenunterroutine. Das heißt, es handelt sich um eine Aufruf Bare Routine, die Aufrufe von anderen Quantum-Vorgängen enthält.

Die Argumente für eine Operation werden als Tupel angegeben, in Klammern eingeschlossen.

Der Rückgabetyp der Operation wird nach einem Doppelpunkt angegeben. In diesem Fall hat die Operation `SetQubitState` keinen Rückgabewert, daher ist sie als `Unit` zurückgebend markiert. Dies ist die Q#-Entsprechung von `unit` in F#, das in etwa analog zu `void` in C# und einem leeren Tupel (`Tuple[()]`) in Python ist.

Sie haben in Ihrem ersten Q#-Vorgang zwei Quantenvorgänge verwendet:

* Der [`M`](xref:microsoft.quantum.intrinsic.m) Vorgang, der den Zustand des Qubit misst.
* Der [`X`](xref:microsoft.quantum.intrinsic.x) Vorgang, der den Zustand eines Qubit kippt.

Mit einem Quantenvorgang wird der Zustand eines Qubits transformiert. Analog zu klassischen Logikgattern wird anstelle von Vorgängen auch von Quantengattern gesprochen. Diese Bezeichnung stammt aus den Anfängen des Quantencomputings, als Algorithmen lediglich ein theoretisches Konstrukt waren und in Form von Diagrammen visualisiert wurden – ähnlich wie bei einem Schaltplan im Bereich des klassischen Computings.

### <a name="counting-measurement-outcomes"></a>Zählen der Messergebnisse

Zur Veranschaulichung der Auswirkungen des Vorgangs `SetQubitState` wird dann der Vorgang `TestBellState` hinzugefügt. Für diesen Vorgang wird `Zero` oder `One` als Eingabe verwendet, und der Vorgang `SetQubitState` wird einige Male mit dieser Eingabe aufgerufen. Es wird gezählt, wie oft bei der Messung des Qubits `Zero` und wie oft `One` zurückgegeben wird. Bei der ersten Simulation des Vorgangs `TestBellState` erwarten wir natürlich, dass in der Ausgabe für alle Messungen des Qubits mit `Zero` als Parametereingabe `Zero` und für alle Messungen eines Qubits mit `One` als Parametereingabe `One` zurückgegeben wird. Im weiteren Verlauf fügen wir Code hinzu, `TestBellState` um Superposition und entanglement zu veranschaulichen.

Fügen Sie der `Bell.qs`-Datei die folgende Operation hinzu, innerhalb des Namespaces, nach dem Ende der `SetQubitState`-Operation:

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

Standardmäßig sind Variablen in Q# unveränderlich; ihr Wert kann nach der Bindung nicht geändert werden. Das `let`-Schlüsselwort wird verwendet, um die Bindung einer unveränderlichen Variable anzugeben. Operationsargumente sind immer unveränderlich.

Wenn Sie eine Variable benötigen, deren Wert geändert werden kann, wie etwa `numOnes` im Beispiel, können Sie die Variable mit dem Schlüsselwort `mutable` deklarieren. Der Wert einer veränderlichen Variable kann mithilfe einer `setQubitState`-Anweisung geändert werden.

In beiden Fällen wird der Typ einer Variablen vom Compiler abgeleitet. Q# erfordert keine Typanmerkungen für Variablen.

#### <a name="about-using-statements-in-q"></a>Informationen zu `using` Anweisungen in Q\#

Die `using`-Anweisung ist eine weitere Besonderheit in Q#. Sie wird verwendet, um Qubits für die Verwendung in einem Codeblock zuzuweisen. In Q# werden alle Qubits dynamisch zugewiesen und freigegeben, sie stellen also keine festen Ressourcen dar, die für die gesamte Lebensdauer eines komplexen Algorithmus vorhanden sind. Eine `using`-Anweisung weist eine Reihe Qubits am Anfang zu und gibt diese Qubits am Ende des Blocks wieder frei.

## <a name="execute-the-code-from-the-command-line"></a>Ausführen des Codes über die Befehlszeile

Um den Code auszuführen, muss der Compiler angegeben werden *, der* beim Bereitstellen des Befehls aufgerufen werden kann `dotnet run` . Dies erfolgt mit einer einfachen Änderung in der Q #-Datei, indem eine Zeile hinzugefügt wird, die `@EntryPoint()` direkt vor der Aufruf baren Zeile steht: der `TestBellState` Vorgang in diesem Fall. Der vollständige Code sollte wie folgt lauten:

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

Um das Programm auszuführen, müssen Sie die `count` Argumente und in `initial` der Befehlszeile angeben. Wählen Sie z. b `count = 1000` . und aus `initial = One` . Geben Sie den folgenden Befehl ein:

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

Sehen wir uns nun an, wie f # die Möglichkeiten zum Platzieren von Qubits in der superposition ausdrückt.  Sie wissen bereits, dass der Zustand eines Qubits den Überlagerungswert 0 und 1 aufweisen kann.  Wir verwenden den Vorgang `Hadamard`, um dies zu erreichen. Wenn das Qubit einen der klassischen Zustände aufweist (bei dem für eine Messung immer `Zero` oder immer `One` zurückgegeben wird), versetzt der Vorgang `Hadamard` bzw. `H` das Qubit in einen Zustand, in dem für eine Messung des Qubits in 50 % der Fälle `Zero` und in 50 % der Fälle `One` zurückgegeben wird.  Sie können sich das Qubit als Mischung von `Zero` und `One` vorstellen.  Wenn wir nun den Vorgang `TestBellState` simulieren, sehen wir nach der Messung, dass ungefähr mit der gleichen Häufigkeit `Zero` und `One` als Ergebnis zurückgegeben wird.  

### <a name="x-flips-qubit-state"></a>`X`kippt-Qubit-Status

Zuerst versuchen wir, das Qubit umzukehren (wenn das Qubit den Zustand `Zero` aufweist, wird in `One` umgekehrt (bzw. andersherum)). Dies wird dadurch erreicht, dass wir den Vorgang `X` durchführen, bevor die Messung in `TestBellState` erfolgt:

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

### <a name="h-prepares-superposition"></a>`H`bereitet die Superposition vor

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

Als Nächstes sehen wir uns an, wie Qubits in Q# verschränkt werden.
Zuerst legen wir das erste Qubit auf den Anfangszustand fest und verwenden dann den Vorgang `H`, um die Überlagerung zu erzielen.  Bevor wir das erste Qubit Messen, verwenden wir dann einen neuen Vorgang ( `CNOT` ), der für "kontrolliert-not" steht.  Das Ergebnis der Ausführung dieses Vorgangs für zwei Qubits ist, dass das zweite Qubit umgekehrt wird, wenn das erste Qubit `One` ist.  Die beiden Qubits sind nun verschränkt.  Unsere Statistiken für das erste Qubit haben sich nicht geändert (50:50-Wahrscheinlichkeit für `Zero` oder `One` nach der Messung), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits. Unser `CNOT` hat die zwei Qubits verschränkt, sodass was immer mit dem einen von ihnen geschieht, auch mit dem anderen geschieht. Wenn Sie die Messungen umkehrten (das zweite Qubit vor dem ersten messen), würde das Gleiche passieren. Die erste Messung wäre zufällig, und die zweite wäre im Gleichschritt mit dem, was bei der ersten herausgefunden wurde.

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

Im Tutorial zur [Grover-Suche](xref:microsoft.quantum.quickstarts.search) wird veranschaulicht, wie Sie die Grover-Suche erstellen und ausführen. Dies ist einer der beliebtesten Algorithmen des Quantencomputings und ein schönes Beispiel für ein Q#-Programm, das zum Lösen echter Probleme im Bereich des Quantencomputings eingesetzt werden kann.  

Der [Artikel zum Einstieg in das Quantum Development Kit](xref:microsoft.quantum.welcome) enthält Informationen zu weiteren Möglichkeiten, wie Sie Q# und die Quantenprogrammierung erlernen können.
