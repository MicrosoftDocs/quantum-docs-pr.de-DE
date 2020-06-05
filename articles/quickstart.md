---
title: Erkunden der Verschränkung mit Q#
description: Erfahren Sie, wie Sie ein Quantenprogramm in Q# schreiben. Entwickeln Sie eine Bell-Zustandsanwendung mithilfe des Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 989080e7d9979bb87d14b2580d28732bb1092eb1
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327372"
---
# <a name="tutorial-explore-entanglement-with-q"></a>Tutorial: Erkunden der Verschränkung mit Q\#

In diesem Tutorial erfahren Sie, wie Sie ein Q#-Programm schreiben, mit dem Qubits bearbeitet und gemessen werden können. Darüber hinaus werden die Auswirkungen von Superposition und Verschränkung veranschaulicht.
Es wird beschrieben, wie Sie das QDK installieren und das Programm erstellen und mit einem Quantensimulator ausführen.  

Sie schreiben eine Anwendung mit dem Namen „Bell“, um die Quantenverschränkung zu veranschaulichen.
Der Name „Bell“ bezieht sich auf die Bell-Zustände. Hierbei handelt es sich um spezifische Quantenzustände von zwei Qubits, die zum Darstellen der einfachsten Beispiele für Überlagerungen und Quantenverschränkungen verwendet werden.

## <a name="pre-requisites"></a>Voraussetzungen

Führen Sie zunächst diese Schritte aus, wenn Sie bereit zum Codieren sind: 

* Installieren Sie das Quantum Development Kit für [Python](xref:microsoft.quantum.install.python) oder [.NET](xref:microsoft.quantum.install.cs).
* Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde

Sie können den Vorgang auch ohne Installation des QDK durchführen, indem Sie sich die Übersichten zur Q#-Programmiersprache und die wichtigsten Konzepte des Quantencomputings ansehen.

## <a name="demonstrating-qubit-behavior-with-q"></a>Veranschaulichen des Qubit-Verhaltens mit Q#

Denken Sie an unsere einfache [Qubit-Definition](xref:microsoft.quantum.overview.understanding) zurück.  Klassische Bits enthalten einen einzelnen binären Wert (0 oder 1). Der Zustand eines [Qubits](xref:microsoft.quantum.glossary#qubit) kann dagegen eine **Superposition** sein (also 0 und 1).  Vom Konzept her können Sie sich ein Qubit als eine Richtung im Raum vorstellen (auch als Vektor bezeichnet).  Ein Qubit kann eine beliebige der möglichen Richtungen aufweisen. Die beiden **klassischen Zustände** sind die beiden Richtungen, die für die einhundertprozentige Chance einer Messung von 0 und die einhundertprozentige Chance einer Messung von 1 stehen.  Diese Darstellung wird formal durch die [Bloch-Kugel](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) visualisiert.

Mit dem Messvorgang wird ein binäres Ergebnis erzeugt und ein Qubit-Zustand geändert. Bei der Messung wird ein binärer Wert erzeugt (0 oder 1).  Das Qubit geht von einem Überlagerungszustand (beliebige Richtung) in einen der klassischen Zustände über.  Danach führt die Wiederholung der gleichen Messung ohne Eingriff zu demselben binären Ergebnis.  

Mehrere Qubits können [**verschränkt**](xref:microsoft.quantum.glossary#entanglement) sein. Bei der Messung eines verschränkten Qubits wird unsere Kenntnis des Zustands der anderen Qubits ebenfalls aktualisiert.

Nun können wir veranschaulichen, wie dieses Verhalten von Q# ausgedrückt wird.  Sie beginnen mit dem einfachsten möglichen Programm und erweitern es anschließend, um die Quantenüberlagerung und -verschränkung zu demonstrieren.

## <a name="setup"></a>Einrichten

Dieses Tutorial nutzt Hostprogramme und besteht aus zwei Teilen:

1. Einer Reihe von Quantenalgorithmen, die mithilfe der Quantenprogrammiersprache Q# implementiert wurden
1. Einem in Python oder C# implementierten Hostprogramm, das als Haupteinstiegspunkt dient und Q#-Vorgänge aufruft, um einen Quantenalgorithmus auszuführen

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Wählen Sie einen Speicherort für Ihre Anwendung aus

1. Erstellen Sie eine Datei namens `Bell.qs`. Diese Datei enthält Ihren Q #-Code.

1. Erstellen Sie eine Datei namens `host.py`. Diese Datei enthält Ihren Python-Hostcode.

#### <a name="c-command-line"></a>[C#-Befehlszeile](#tab/tabid-csharp)

1. Erstellen Sie ein neues Q#-Projekt:

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    Sie sollten eine `.csproj`-Datei, eine Q#-Datei mit dem Namen `Operations.qs` und eine Hostprogrammdatei mit dem Namen `Driver.cs` sehen.

1. Benennen Sie die Q#-Datei um.

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. Erstellen eines neuen Projekts

   * Öffnen Sie Visual Studio.
   * Navigieren Sie zum Menü **Datei**, und wählen Sie **Neu** -> **Projekt...** aus.
   * Geben Sie im Projektvorlagen-Explorer `Q#` in das Suchfeld ein, und wählen Sie die Vorlage `Q# Application` aus.
   * Geben Sie dem Projekt den Namen `Bell`.

1. Benennen Sie die Q#-Datei um.

   * Navigieren Sie zum **Projektmappen-Explorer**
   * Klicken Sie mit der rechten Maustaste auf die `Operations.qs`-Datei.
   * Benennen Sie sie in `Bell.qs` um.

* * *

## <a name="write-a-q-operation"></a>Schreiben einer Q#-Operation

Unser Ziel ist die Festlegung eines spezifischen Quantenzustands für zwei Qubits. Hiermit soll demonstriert werden, wie Sie mit Q# bei Qubits vorgehen, um den Zustand zu ändern und die Auswirkungen von Überlagerung und Verschränkung zu veranschaulichen. Wir bauen dies Stück für Stück auf, um Zustände, Vorgänge und Messungen von Qubits zu demonstrieren.

**Übersicht:**  Im ersten unten aufgeführten Code wird gezeigt, wie Sie in Q# mit Qubits arbeiten.  Wir verwenden die beiden Vorgänge `M` und `X`, um den Zustand eines Qubits zu transformieren. 

In diesem Codeausschnitt wird der Vorgang `Set` definiert, für den als Parameter ein Qubit verwendet wird, sowie ein weiterer Parameter `desired`, mit dem der gewünschte Zustand für das Qubit dargestellt wird.  Der Vorgang `Set` führt eine Messung für das Qubit durch, indem der Vorgang `M` verwendet wird.  In Q# wird für eine Qubit-Messung immer entweder `Zero` oder `One` zurückgegeben.  Wenn die Messung einen Wert zurückgibt, der nicht einem gewünschten Wert entspricht, wird das Qubit von „Set“ umgekehrt. Der Vorgang `X` wird ausgeführt, mit dem der Qubit-Zustand in einen neuen Zustand geändert wird, bei dem die Wahrscheinlichkeiten, dass für eine Messung `Zero` und `One` zurückgegeben wird, umgekehrt sind.  Zur Veranschaulichung der Auswirkungen des Vorgangs `Set` wird dann der Vorgang `TestBellState` hinzugefügt.  Für diesen Vorgang wird `Zero` oder `One` als Eingabe verwendet, und der Vorgang `Set` wird einige Male mit dieser Eingabe aufgerufen. Es wird gezählt, wie oft bei der Messung des Qubits `Zero` und wie oft `One` zurückgegeben wird. Bei der ersten Simulation des Vorgangs `TestBellState` erwarten wir natürlich, dass in der Ausgabe für alle Messungen des Qubits mit `Zero` als Parametereingabe `Zero` und für alle Messungen eines Qubits mit `One` als Parametereingabe `One` zurückgegeben wird.  Später fügen wir `TestBellState` Code hinzu, um die Überlagerung und Verschränkung zu demonstrieren.


### <a name="q-operation-code"></a>Q#-Operationscode

1. Ersetzen Sie den Inhalt der Datei „Bell.qs“ durch den folgenden Code:

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    Dieser Vorgang kann jetzt aufgerufen werden, um ein Qubit auf einen klassischen Zustand festzulegen, indem entweder immer `Zero` oder immer `One` zurückgegeben wird.  `Zero` und `One` sind Konstanten, die die beiden einzigen möglichen Ergebnisse der Messung eines Qubits darstellen.

    Mit dem Vorgang `Set` wird das Qubit gemessen.
    Falls sich das Qubit im gewünschten Zustand befindet, wird es von `Set` unverändert gelassen. Andernfalls ändern wir den Qubit-Zustand in den gewünschten Zustand, indem wir den Vorgang `X` ausführen.

### <a name="about-q-operations"></a>Informationen zu Q#-Vorgängen

Ein Q#-Vorgang ist eine Quantenunterroutine. Dies bedeutet, dass es sich um eine aufrufbare Routine handelt, die Quantenvorgänge enthält.

Die Argumente für eine Operation werden als Tupel angegeben, in Klammern eingeschlossen.

Der Rückgabetyp der Operation wird nach einem Doppelpunkt angegeben. In diesem Fall hat die Operation `Set` keinen Rückgabewert, daher ist sie als `Unit` zurückgebend markiert. Dies ist die Q#-Entsprechung von `unit` in F#, das in etwa analog zu `void` in C# und einem leeren Tupel (`Tuple[()]`) in Python ist.

Sie haben in Ihrem ersten Q#-Vorgang zwei Quantenvorgänge verwendet:

* Den Vorgang [M](xref:microsoft.quantum.intrinsic.m), mit dem der Zustand des Qubits gemessen wird
* Den Vorgang [X](xref:microsoft.quantum.intrinsic.x), mit dem der Zustand eines Qubits umgekehrt wird

Mit einem Quantenvorgang wird der Zustand eines Qubits transformiert. Analog zu klassischen Logikgattern wird anstelle von Vorgängen auch von Quantengattern gesprochen. Diese Bezeichnung stammt aus den Anfängen des Quantencomputings, als Algorithmen lediglich ein theoretisches Konstrukt waren und in Form von Diagrammen visualisiert wurden – ähnlich wie bei einem Schaltplan im Bereich des klassischen Computings.

### <a name="add-q-test-code"></a>Hinzufügen von Q#-Testcode

1. Fügen Sie der `Bell.qs`-Datei die folgende Operation hinzu, innerhalb des Namespaces, nach dem Ende der `Set`-Operation:

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    Diese Operation (`TestBellState`) iteriert `count` Iterationen lang in einer Schleife, legt einen angegebenen `initial`-Wert für ein Qubit fest, und misst (`M`) dann das Ergebnis. Sie führt eine Statistik zur Anzahl der gemessenen Nullen und Einsen und gibt diese an den Aufrufer zurück. Sie führt eine weitere erforderliche Operation aus. Sie setzt das Qubit auf einen bekannten Zustand (`Zero`) zurück, bevor sie es zurückgibt, was es anderen ermöglicht, dieses Qubit in einem bekannten Zustand zuzuweisen. Dies ist aufgrund der `using`-Anweisung erforderlich.

### <a name="about-variables-in-q"></a>Informationen zu Variablen in Q#

Standardmäßig sind Variablen in Q# unveränderlich; ihr Wert kann nach der Bindung nicht geändert werden. Das `let`-Schlüsselwort wird verwendet, um die Bindung einer unveränderlichen Variable anzugeben. Operationsargumente sind immer unveränderlich.

Wenn Sie eine Variable benötigen, deren Wert geändert werden kann, wie etwa `numOnes` im Beispiel, können Sie die Variable mit dem Schlüsselwort `mutable` deklarieren. Der Wert einer veränderlichen Variable kann mithilfe einer `set`-Anweisung geändert werden.

In beiden Fällen wird der Typ einer Variablen vom Compiler abgeleitet. Q# erfordert keine Typanmerkungen für Variablen.

### <a name="about-using-statements-in-q"></a>Informationen zu `using`-Anweisungen in Q#

Die `using`-Anweisung ist eine weitere Besonderheit in Q#. Sie wird verwendet, um Qubits für die Verwendung in einem Codeblock zuzuweisen. In Q# werden alle Qubits dynamisch zugewiesen und freigegeben, sie stellen also keine festen Ressourcen dar, die für die gesamte Lebensdauer eines komplexen Algorithmus vorhanden sind. Eine `using`-Anweisung weist eine Reihe Qubits am Anfang zu und gibt diese Qubits am Ende des Blocks wieder frei.

## <a name="create-the-host-application-code"></a>Erstellen des Hostanwendungscodes

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Öffnen Sie die Datei `host.py`, und fügen Sie den folgenden Code hinzu:

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

1. Ersetzen Sie den Inhalt der Datei `Driver.cs` durch den folgenden Code:

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a>Informationen zum Hostanwendungscode

#### <a name="python"></a>[Python](#tab/tabid-python)

Die Python-Hostanwendung weist drei Teile auf:

* Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind. Im Beispiel ist `count` auf 1000 festgelegt, und `initial` ist der Anfangswert des Qubits.
* Ausführen des Quantenalgorithmus durch Aufrufen der `simulate()`-Methode der importierten Q#-Operation.
* Verarbeiten des Ergebnisses der Operation. Im Beispiel empfängt `res` das Ergebnis der Operation. Hier ist das Ergebnis ein Tupel der Anzahl von Nullen (`num_zeros`) und der Anzahl von Einsen (`num_ones`), die vom Simulator gemessen wurden. Wir dekonstruieren das Tupel, um die zwei Felder zu erhalten, und geben die Ergebnisse aus.

#### <a name="c"></a>[C#](#tab/tabid-csharp)

Die C#-Hostanwendung weist vier Teile auf:

* Konstruieren eines Quantensimulators. Im Beispiel ist `qsim` der Simulator.
* Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind. Im Beispiel ist `count` auf 1000 festgelegt, und `initial` ist der Anfangswert des Qubits.
* Ausführen des Quantenalgorithmus. Jede Q#-Operation generiert eine C#-Klasse gleichen Namens. Diese Klasse weist eine `Run`-Methode auf, die die Operation **asynchron** ausführt. Die Ausführung ist asynchron, weil die Ausführung auf realer Hardware asynchron ist. Da die `Run`-Methode asynchron ist, rufen wir die `Result`-Eigenschaft ab; dies blockiert die Ausführung, bis die Aufgabe abgeschlossen ist und das Ergebnis synchron zurückgibt.
* Verarbeiten des Ergebnisses der Operation. Im Beispiel empfängt `res` das Ergebnis der Operation. Hier ist das Ergebnis ein Tupel der Anzahl von Nullen (`numZeros`) und der Anzahl von Einsen (`numOnes`), die vom Simulator gemessen wurden. Dies wird in C# als ein ValueTuple zurückgegeben. Wir dekonstruieren das Tupel, um die zwei Felder zu erhalten, geben die Ergebnisse aus und warten auf einen Tastendruck.

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a>Erstellen und Ausführen

#### <a name="python"></a>[Python](#tab/tabid-python)

1. Führen Sie den folgenden Befehl an Ihrem Terminal aus:

    ```
    python host.py
    ```

    Dieser Befehl führt die Hostanwendung aus, die die Q#-Operation simuliert.

Dies sollten die Ergebnisse sein:

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[Befehlszeile/Visual Studio Code](#tab/tabid-csharp)

1. Führen Sie Folgendes an Ihrem Terminal aus:

    ```bash
    dotnet run
    ```

    Durch diesen Befehl werden alle erforderlichen Pakete automatisch heruntergeladen, die Anwendung erstellt und anschließend an der Befehlszeile ausgeführt.

1. Drücken Sie alternativ **F1**, um die Befehlspalette zu öffnen, und wählen Sie **Debug: Starten ohne Debuggen** aus.
Möglicherweise werden Sie aufgefordert, eine neue ``launch.json``-Datei zu erstellen, die beschreibt, wie das Programm gestartet wird.
Die standardmäßige ``launch.json`` sollte für die meisten Anwendungen gut funktionieren.

Dies sollten die Ergebnisse sein:

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[Visual Studio](#tab/tabid-vs2019)

1. Drücken Sie einfach `F5`, dann sollte Ihr Programm erstellt und ausgeführt werden!

Dies sollten die Ergebnisse sein:

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

Das Programm wird beendet, nachdem Sie eine Taste drücken.

* * *

## <a name="prepare-superposition"></a>Vorbereiten von Überlagerung

**Übersicht** Wir sehen uns nun an, wie in Q# die Überlagerung von Qubits erzielt wird.  Sie wissen bereits, dass der Zustand eines Qubits den Überlagerungswert 0 und 1 aufweisen kann.  Wir verwenden den Vorgang `Hadamard`, um dies zu erreichen. Wenn das Qubit einen der klassischen Zustände aufweist (bei dem für eine Messung immer `Zero` oder immer `One` zurückgegeben wird), versetzt der Vorgang `Hadamard` bzw. `H` das Qubit in einen Zustand, in dem für eine Messung des Qubits in 50 % der Fälle `Zero` und in 50 % der Fälle `One` zurückgegeben wird.  Sie können sich das Qubit als Mischung von `Zero` und `One` vorstellen.  Wenn wir nun den Vorgang `TestBellState` simulieren, sehen wir nach der Messung, dass ungefähr mit der gleichen Häufigkeit `Zero` und `One` als Ergebnis zurückgegeben wird.  

Zuerst versuchen wir, das Qubit umzukehren (wenn das Qubit den Zustand `Zero` aufweist, wird in `One` umgekehrt (bzw. andersherum)). Dies wird dadurch erreicht, dass wir den Vorgang `X` durchführen, bevor die Messung in `TestBellState` erfolgt:

```qsharp
X(qubit);
let res = M(qubit);
```

Jetzt sind die Ergebnisse (nach dem Drücken von `F5`) umgekehrt:

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

Aber alles, was wir bisher gesehen haben, ist klassisch. Rufen wir mal ein Quantenergebnis ab. Hierfür müssen wir lediglich den Vorgang `X` in der vorherigen Ausführung durch den Vorgang `H` (Hadamard-Vorgang) ersetzen. Statt das Qubit ganz von 0 in 1 umzukehren, kehren wir es nur halb um. Die ersetzten Zeilen in `TestBellState` sehen jetzt so aus:

```qsharp
H(qubit);
let res = M(qubit);
```

Jetzt werden die Ergebnisse interessanter:

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

Jedes Mal, wenn wir messen, fragen wir nach einem klassischen Wert, aber das Qubit befindet sich auf halbem Weg zwischen 0 und 1, also erhalten wir (statistisch) die Hälfte der Zeit 0 und die Hälfte der Zeit 1. Dies wird als __Überlagerung__ bezeichnet und gibt uns unseren ersten echten Einblick in einen Quantenzustand.

## <a name="prepare-entanglement"></a>Vorbereiten von Verschränkung

**Übersicht:**  Als Nächstes sehen wir uns an, wie Qubits in Q# verschränkt werden.  Zuerst legen wir das erste Qubit auf den Anfangszustand fest und verwenden dann den Vorgang `H`, um die Überlagerung zu erzielen.  Vor dem Messen des ersten Qubits verwenden wir den neuen Vorgang `CNOT`. Diese Abkürzung steht für „Controlled-Not“.  Das Ergebnis der Ausführung dieses Vorgangs für zwei Qubits ist, dass das zweite Qubit umgekehrt wird, wenn das erste Qubit `One` ist.  Die beiden Qubits sind nun verschränkt.  Unsere Statistiken für das erste Qubit haben sich nicht geändert (50:50-Wahrscheinlichkeit für `Zero` oder `One` nach der Messung), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits. Unser `CNOT` hat die zwei Qubits verschränkt, sodass was immer mit dem einen von ihnen geschieht, auch mit dem anderen geschieht. Wenn Sie die Messungen umkehrten (das zweite Qubit vor dem ersten messen), würde das Gleiche passieren. Die erste Messung wäre zufällig, und die zweite wäre im Gleichschritt mit dem, was bei der ersten herausgefunden wurde.

Im ersten Schritt müssen wir dazu in `TestBellState` 2 Qubits anstelle von einem zuweisen:

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

Dies ermöglicht es uns, einen neuen Vorgang (`CNOT`) hinzuzufügen, bevor wir in `TestBellState` die Messung (`M`) durchführen:

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

Wir haben eine weitere `Set`-Operation hinzugefügt, um das erste Qubit zu initialisieren, um sicherzustellen, dass es sich anfangs immer im `Zero`-Zustand befindet.

Wir müssen außerdem das zweite Qubit zurücksetzen, bevor wir es freigeben.

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

Die vollständige Routine sieht jetzt so aus:

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
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
                Set(initial, q0);
                Set(Zero, q1);

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
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

Der neue Rückgabewert (`agree`) hält fest, wenn die Messung des ersten Qubits mit der Messung des zweiten Qubits übereinstimmt. Außerdem müssen wir die Hostanwendung entsprechend aktualisieren:

#### <a name="python"></a>[Python](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

Bei einer erneuten Ausführung erhalten wir jetzt etwas ziemlich Erstaunliches:

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

Wie in der Übersicht beschrieben, haben sich unsere Statistiken für das erste Qubit nicht geändert (50:50-Wahrscheinlichkeit für 0 oder 1), aber wenn wir jetzt das zweite Qubit messen, erhalten wir __immer__ das gleiche Ergebnis wie bei der Messung des ersten Qubits, weil sie verschränkt sind.

Herzlichen Glückwunsch, Sie haben Ihr erstes Quantenprogramm geschrieben!

## <a name="next-steps"></a>Nächste Schritte

Im Tutorial zur [Grover-Suche](xref:microsoft.quantum.quickstarts.search) wird veranschaulicht, wie Sie die Grover-Suche erstellen und ausführen. Dies ist einer der beliebtesten Algorithmen des Quantencomputings und ein schönes Beispiel für ein Q#-Programm, das zum Lösen echter Probleme im Bereich des Quantencomputings eingesetzt werden kann.  

Der [Artikel zum Einstieg in das Quantum Development Kit](xref:microsoft.quantum.welcome) enthält Informationen zu weiteren Möglichkeiten, wie Sie Q# und die Quantenprogrammierung erlernen können.
