---
title: 'Schreiben und Simulieren von Programmen auf Qubit-Ebene in Q #'
description: Schritt-für-Schritt-Tutorial zum Schreiben und Simulieren eines Quantum-Programms, das auf der einzelnen Qubit-Ebene funktioniert
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
ms.openlocfilehash: f0b87936c9baf07555e76f295da58c0a6b9ecd17
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84328594"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a>Tutorial: schreiben und Simulieren von Programmen auf Qubit-Ebene in Q\#

Willkommen beim Quantum Development Kit-Tutorial zum Schreiben und Simulieren eines grundlegenden quantumprogramms, das auf einzelnen Qubits funktioniert. 

Obwohl Q # primär als allgemeine Programmiersprache für große Quantum-Programme erstellt wurde, kann es genauso einfach verwendet werden, um die niedrigere Ebene der Quantum-Programme zu untersuchen: direktes adressieren spezifischer Qubits.
Die Flexibilität von Q # ermöglicht es Benutzern, Quantum-Systeme von einer beliebigen Art von Abstraktion anzugehen, und in diesem Tutorial werden die Qubits selbst beleuchtet.
Insbesondere betrachten wir die [Dynamik der Quantum Fourier-Transformation](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), eine Unterroutine, die für viele größere Quantum-Algorithmen von wesentlicher Bedeutung ist.

Beachten Sie, dass dieser Low-Level-Überblick über die Verarbeitung von Quantum-Informationen häufig in Bezug auf "[Quantum](xref:microsoft.quantum.concepts.circuits)-Verbindungen" beschrieben wird, die die sequenzielle Anwendung von Gates auf bestimmte Qubits eines Systems darstellen.

Folglich können die von uns sequenziell angewendenden Single-und Multi-Qubit-Vorgänge in einem "Verbindungs Diagramm" dargestellt werden.
In unserem Fall definieren wir einen Q #-Vorgang, um die vollständige drei-Qubit-Quantum Fourier-Transformation durchzuführen, die die folgende Darstellung als Verbindung aufweist:

<br/>
<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a>Voraussetzungen

* [Installieren](xref:microsoft.quantum.install) Sie das Quantum Development Kit mit Ihrer bevorzugten Sprache und Entwicklungsumgebung.
* Wenn das QDK bereits installiert ist, vergewissern Sie sich, dass es auf die neueste Version [geupdated](xref:microsoft.quantum.update) wurde


## <a name="in-this-tutorial-youll-learn-how-to"></a>In diesem Tutorial lernen Sie Folgendes:

> [!div class="checklist"]
> * Definieren von Quantum-Vorgängen in Q #
> * F #-Vorgänge direkt über die Befehlszeile oder ein klassisches Host Programm abrufen
> * Simulieren eines Quantum-Vorgangs von der Qubit-Zuordnung zur Mess Ausgabe
> * Beobachten Sie, wie sich die simulierte wavefunction des Quantum-Systems während des Vorgangs weiterentwickelt

Das Ausführen eines Quantum-Programms mit dem Quantum Development Kit von Microsoft besteht in der Regel aus zwei Teilen:
1. Das Programm selbst, das mithilfe der Programmiersprache Q # Quantum implementiert wird und dann aufgerufen wird, um auf einem Quantum-Computer oder einem Quantum-Simulator ausgeführt zu werden. Diese bestehen aus 
    - F #-Vorgänge: Unterroutinen, die in quantatenregistern agieren, und 
    - F #-Funktionen: klassische Unterroutinen, die innerhalb des Quantum-Algorithmus verwendet werden.
2. Der Einstiegspunkt, der verwendet wird, um das Quantum-Programm aufzurufen und den Zielcomputer anzugeben, auf dem er ausgeführt werden soll.
    Dies kann direkt über die Befehlszeile oder über ein Host Programm erfolgen, das in einer klassischen Programmiersprache wie Python oder c# geschrieben ist.
    Dieses Tutorial enthält Anweisungen für die gewünschte Methode.

## <a name="allocate-qubits-and-define-quantum-operations"></a>Zuordnen von Qubits und Definieren von Quantum-Vorgängen

Der erste Teil dieses Tutorials besteht darin, den Q #-Vorgang `Perform3qubitQFT` zu definieren, der die Quantum Fourier-Transformation auf drei Qubits ausführt. 

Außerdem verwenden wir die- [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) Funktion, um zu beobachten, wie sich die simulierte wavefunction unseres drei Qubit-Systems über den gesamten Vorgang hinweg weiterentwickelt.

Der erste Schritt besteht darin, das Q #-Projekt und die-Datei zu erstellen.
Die Schritte hierfür hängen von der Umgebung ab, die Sie zum Anrufen des Programms verwenden, und Sie finden die Details in den entsprechenden [Installations](xref:microsoft.quantum.install)Handbüchern.

Wir führen Sie Schritt für Schritt durch die Komponenten der Datei. der Code ist jedoch auch als vollständige Block weiter unten verfügbar.

### <a name="namespaces-to-access-other-q-operations"></a>Namespaces für den Zugriff auf andere Q #-Vorgänge
Innerhalb der Datei wird zunächst der Namespace definiert, `NamespaceQFT` auf den der Compiler zugreift.
Damit der Vorgang vorhandene Q #-Vorgänge nutzen kann, öffnen wir die relevanten `Microsoft.Quantum.<>` Namespaces.

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a>Definieren von Vorgängen mit Argumenten und Rückgabe
Als nächstes definieren wir den `Perform3qubitQFT` Vorgang:

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

Der Vorgang nimmt vorerst keine Argumente an und gibt nichts zurück---in diesem Fall schreiben wir, dass Sie ein-Objekt zurückgibt `Unit` , das `void` in c# oder in einem leeren Tupel `Tuple[()]` in python ähnelt.
Später werden wir Sie ändern, um ein Array von Messergebnissen zurückzugeben, an dem der Punkt `Unit` durch ersetzt wird `Result[]` . 

### <a name="allocate-qubits-with-using"></a>Zuordnen von Qubits mit`using`
In unserem Q #-Vorgang weisen wir zuerst ein Register von drei Qubits mit der- `using` Anweisung zu:

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

Bei `using` werden die Qubits automatisch im $ \ket {0} $-Status zugeordnet. Wir können dies mithilfe von und überprüfen [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , wodurch eine Zeichenfolge und der aktuelle Zustand des Systems auf der Konsole gedruckt werden.

> [!NOTE]
> Die `Message(<string>)` -Funktion und die- `DumpMachine()` Funktion (von [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) bzw.) werden beide direkt in der Konsole gedruckt. Genau wie bei einer echten Quantum-Berechnung lässt Q # den direkten Zugriff auf Qubit-Zustände nicht zu.
> `DumpMachine`Wenn jedoch den aktuellen Zustand des Ziel Computers ausgibt, kann er wertvolle Einblicke in das Debuggen und Erlernen von Informationen liefern, wenn er in Verbindung mit dem vollständigen Zustands Simulator verwendet wird.


### <a name="applying-single-qubit-and-controlled-gates"></a>Anwenden von Single-Qubit und kontrollierten Gates

Als nächstes wenden wir die Gates an, aus denen der Vorgang besteht.
Q # enthält bereits viele grundlegende Quantum-Gates als Vorgänge im [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) -Namespace, und dies ist keine Ausnahme. 

In einem Q #-Vorgang werden die Anweisungen, die callables aufrufen, natürlich in sequenzieller Reihenfolge ausgeführt.
Daher ist das erste anzuwendende Gate der [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) zum ersten Qubit:

<br/>
<img src="./qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

Um einen Vorgang auf ein bestimmtes Qubit aus einem Register (d. h. einem einzelnen `Qubit` aus einem Array) anzuwenden, `Qubit[]` verwenden wir die standardmäßige Index Notation.
Daher hat das Anwenden [`H`](xref:microsoft.quantum.intrinsic.h) von auf das erste Qubit des Registers folgendes Format `qs` :

```qsharp
            H(qs[0]);
```

Neben dem Anwenden des- `H` Tors (Hadamard) auf einzelne Qubits besteht die QFT-Leitung hauptsächlich aus kontrollierten [`R1`](xref:microsoft.quantum.intrinsic.r1) Rotationen.
`R1(θ, <qubit>)`Bei einem Vorgang im Allgemeinen bleibt die $ \ket {0} $-Komponente des Qubit unverändert, während eine Rotation $e ^ {i\orta} $ auf die $ \ket $-Komponente angewendet wird {1} .

#### <a name="controlled-operations"></a>Kontrollierte Vorgänge

F # macht es äußerst einfach, die Ausführung eines Vorgangs auf ein oder mehrere Steuerelement-Qubits zu bedinieren.
Im Allgemeinen wird dem-Befehl lediglich `Controlled` vorangestellt, und die Vorgangs Argumente ändern sich wie folgt:

 `Op(<normal args>)`$ \bis $ `Controlled Op([<control qubits>], (<normal args>))` .

Beachten Sie, dass die Steuerelement-Qubits als Array bereitgestellt werden müssen, selbst wenn es sich um ein einzelnes Qubit handelt.

Nach dem `H` sehen wir, dass es sich bei den nächsten Gates um die Gates handelt, die `R1` auf dem ersten Qubit agieren (und durch das zweite/dritte gesteuert werden):

<br/>
<img src="./qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

Wir nennen diese mit

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

Beachten Sie, dass die- [`PI()`](xref:microsoft.quantum.math.pi) Funktion aus dem- [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) Namespace verwendet wird, um die Rotationen in Bezug auf Pi-radiane zu definieren.
Darüber hinaus dividieren wir durch einen `Double` (z. b. `2.0` ), da die Division durch eine ganze Zahl `2` einen Typfehler auslösen würde. 

> [!TIP]
> `R1(π/2)`und `R1(π/4)` sind äquivalent zu den `S` -und- `T` Vorgängen (auch in `Microsoft.Quantum.Intrinsic` ).


Nach dem Anwenden der relevanten `H` Vorgänge und der kontrollierten Rotationen auf das zweite und dritte Qubits:

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

Wir müssen nur ein [`SWAP`](xref:microsoft.quantum.intrinsic.swap) Gate anwenden, um die Verbindung abzuschließen:

```qsharp
            SWAP(qs[2], qs[0]);
```

Dies ist erforderlich, da die Natur der Quantum Fourier-Transformation die Qubits in umgekehrter Reihenfolge ausgibt, sodass die Austausch Vorgängen eine nahtlose Integration der Unterroutine in größere Algorithmen ermöglichen.

Daher haben wir das Schreiben der Qubit-Level-Vorgänge der Quantum Fourier-Transformation in unseren f #-Vorgang abgeschlossen:

<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

Wir können ihn jedoch noch nicht an einem Tag anrufen.
Unsere Qubits befanden sich im Status "$ \ket {0} $", als wir Sie zugewiesen haben, und ähnlich wie im Leben sollten wir in Q # die Dinge auf dieselbe Weise wie Sie gefunden haben (oder besser!).

### <a name="deallocate-qubits"></a>Freigabe von Qubits aufgehoben

Wir [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) werden erneut aufgerufen, um den Zustand nach dem Betrieb anzuzeigen, und schließlich [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) auf das Qubit-Register angewendet, um die Qubits auf "$ \ket $" zurückzusetzen, {0} bevor der Vorgang abgeschlossen wird:

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

Das festlegen, dass alle zugeordneten Qubits explizit auf "$ \ket $" festgelegt werden müssen {0} , ist eine grundlegende Funktion von Q #, da andere Vorgänge ihren Zustand genau erkennen können, wenn Sie mit der Verwendung der gleichen Qubits (knappe Ressource) beginnen.
Außerdem wird dadurch sichergestellt, dass Sie nicht mit anderen Qubits im System entkoppelt werden.
Wenn die zurück setzung am Ende eines `using` Zuordnungs Blocks nicht ausgeführt wird, wird ein Laufzeitfehler ausgelöst.

Ihre vollständige f #-Datei sollte nun wie folgt aussehen:

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


Wenn die f #-Datei und der Vorgang abgeschlossen sind, kann unser Quantum-Programm aufgerufen und simuliert werden.

## <a name="execute-the-program"></a>Programm ausführen

Nachdem wir den Q #-Vorgang in einer Datei definiert haben `.qs` , müssen wir diesen Vorgang jetzt aufrufen und alle zurückgegebenen klassischen Daten beobachten.
Zurzeit gibt es nichts zurückgegeben (Beachten Sie, dass der oben definierte Vorgang zurückgibt `Unit` ), doch wenn wir später den Q #-Vorgang ändern, um ein Array von Messergebnissen () zurückzugeben `Result[]` , wird dies behandelt.

Wenngleich das Q #-Programm in den Umgebungen, in denen es aufgerufen wird, universell ist, ist die Vorgehensweise natürlich unterschiedlich. Befolgen Sie daher einfach die Anweisungen auf der Registerkarte, die dem Setup entspricht: Arbeiten Sie mit der Befehlszeilen Anwendung "Q #" oder mit einem Host Programm in Python oder c#.

#### <a name="command-line"></a>[Befehlszeile](#tab/tabid-cmdline)

Wenn das q #-Programm über die Befehlszeile ausgeführt wird, ist nur eine kleine Änderung an der q #-Datei erforderlich.

Fügen Sie einfach `@EntryPoint()` zu einer Zeile vor der Vorgangs Definition hinzu:

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

Um das Programm auszuführen, öffnen Sie das Terminal im Ordner des Projekts, und geben Sie ein.

```dotnetcli
dotnet run
```

Bei der Ausführung sollten die `Message` `DumpMachine` Ausgaben und unten in der Konsole gedruckt angezeigt werden.


#### <a name="python"></a>[Python](#tab/tabid-python)

Erstellen Sie eine python-Hostdatei: `host.py` .

Die Hostdatei wird wie folgt erstellt: 
1. Zuerst importieren wir das `qsharp` Modul, das das Modul Lade Modul für die Q #-Interoperabilität registriert. 
    Dadurch können q #-Namespaces (z. b. die `NamespaceQFT` in der Q #-Datei definierten) als Python-Module angezeigt werden, von denen wir q #-Vorgänge importieren können.
2. Importieren Sie dann die f #-Vorgänge, die wir direkt aufrufen---in diesem Fall `Perform3qubitQFT` .
    Wir müssen den Einstiegspunkt nur in ein Q #-Programm importieren (d. h. _keine_ Vorgänge wie `H` und `R1` , die von anderen Q #-Vorgängen, aber nie vom klassischen Host aufgerufen werden).
3. Verwenden Sie beim Simulieren von f #-Vorgängen oder-Funktionen das Formular, `<Q#callable>.simulate(<args>)` um Sie auf dem `QuantumSimulator()` Zielcomputer auszuführen. 

> [!NOTE]
> Wenn der Vorgang auf einem anderen Computer aufgerufen werden soll, z `ResourceEstimator()` . b., verwenden wir einfach `<Q#callable>.estimate_resources(<args>)` .
> Im Allgemeinen sind Q #-Vorgänge auf den Computern, auf denen Sie ausgeführt werden, agnostisch, einige Features wie können sich jedoch unter `DumpMachine` schiedlich Verhalten.

4. Beim Ausführen der Simulation gibt der Vorgangs Aufrufwert Werte zurück, die in der Q #-Datei definiert sind.
    Vorerst wird nichts zurückgegeben, aber später wird ein Beispiel für das zuweisen und Verarbeiten dieser Werte angezeigt.
    Wenn sich die resultierenden Daten in unserer Praxis und ganz klassisch befinden, können wir mit Ihnen alles tun, was wir wollen.

Die vollständige `host.py` Datei sollte wie folgt lauten:

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

Wenn Sie die python-Datei ausführen und in der Konsole gedruckt werden, sollten die `Message` Ausgaben und unten angezeigt werden `DumpMachine` . 


#### <a name="c"></a>[C#](#tab/tabid-csharp)

Befolgen Sie die Anweisungen im [Installationshandbuch](xref:microsoft.quantum.install.cs), erstellen Sie eine c#-Hostdatei, und benennen Sie Sie in um `host.cs` .

Der c#-Host besteht aus vier Teilen:
1. Konstruieren eines Quantensimulators.
    Im folgenden Code ist dies die Variable `qsim` .
2. Berechnen aller Argumente, die für den Quantenalgorithmus erforderlich sind.
    In diesem Beispiel gibt es keine.
3. Ausführen des Quantenalgorithmus. 
    Jede Q#-Operation generiert eine C#-Klasse gleichen Namens. 
    Diese Klasse weist eine `Run`-Methode auf, die die Operation **asynchron** ausführt.
    Die Ausführung ist asynchron, weil die Ausführung auf realer Hardware asynchron ist. 
    Da die- `Run` Methode asynchron ist, wird die- `Wait()` Methode aufgerufen. Dadurch wird die Ausführung blockiert, bis die Aufgabe abgeschlossen ist, und das Ergebnis synchron zurückgegeben wird. 
4. Verarbeiten Sie das zurückgegebene Ergebnis des Vorgangs.
    Vorerst gibt der Vorgang nichts zurück.


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
Führen Sie die Anwendung aus, und die Ausgabe sollte der folgenden Abbildung entsprechen.
Das Programm wird beendet, nachdem Sie eine Taste drücken.
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

Wenn Sie im vollständigen Simulator aufgerufen wird, `DumpMachine()` stellt diese ungendarstellungen der wavefunction des Quantum State bereit. Die möglichen Zustände eines $n $-Qubit-Systems können durch die Zustände "$ 2 ^ n $ Compute" dargestellt werden, die jeweils über einen entsprechenden komplexen Koeffizienten verfügen (einfach eine Amplitude und eine Phase).
Die Berechnungs Zustände entsprechen allen möglichen binären Zeichen folgen der Länge $n $---d. h. alle möglichen Kombinationen aus Qubit-Zuständen $ \ket {0} $ und $ \ket {1} $, wobei jede binäre Ziffer einem einzelnen Qubit entspricht.

Die erste Zeile enthält einen Kommentar mit den IDs der entsprechenden Qubits in ihrer großen Reihenfolge.
Qubit `2` ist die "größte Bedeutung", d. h., dass in der binären Darstellung von "Basis Zustands Vektor $ \ket{i} $" der Status von Qubit `2` der äußersten linken Ziffer entspricht. Beispiel: $ \ket {6} = \ket {110} $ umfasst Qubits `2` und in `1` $ \ket {1} $ und Qubit `0` in $ \ket {0} $.


In den restlichen Zeilen wird die Wahrscheinlichkeits Amplitude der Messung des Basis Zustands Vektors $ \ket{i} $ im kartesischen und Polar Format beschrieben.
Im Detail für die erste Zeile des Eingabe Zustands $ \ket {000} $:
* **`|0>:`** Diese Zeile entspricht dem `0` Status "computebasis" (da der anfängliche Status nach der Zuordnung "$ \ket $" war {000} , erwartet wir, dass dies der einzige Zustand mit Wahrscheinlichkeits Amplitude an diesem Punkt ist).
* **`1.000000 +  0.000000 i`**: die Wahrscheinlichkeits Amplitude im kartesischen Format.
* **` == `**: das `equal` Vorzeichen trennt beide äquivalente Darstellungen.
* **`********************`**: Eine grafische Darstellung der Größe, die Anzahl von `*` ist proportional zur Wahrscheinlichkeit, diesen Zustands Vektor zu messen. 
* **`[ 1.000000 ]`**: der numerische Wert der Größe.
* **`    ---`**: Eine grafische Darstellung der Amplitude-Phase.
* **`[ 0.0000 rad ]`**: der numerische Wert der Phase (im Bogenmaße).

Sowohl die Größe als auch die Phase werden mit grafischer Darstellung angezeigt. Die Größen Darstellung ist einfach: Sie zeigt einen Balken an `*` , und je höher die Wahrscheinlichkeit ist, desto größer ist der Balken. Informationen zu den möglichen Symbol Darstellungen auf der Grundlage von Winkel Bereichen finden Sie [im Abschnitt](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions) dumpmachine.


Die gedruckte Ausgabe zeigt also, dass unsere programmierten Gates unseren Zustand von

$ $ \ket{\psi} \_ {Initial} = \ket {000} $ $

zu 

$ $ \begin{align} \ket{\psi} \_ {Final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $

Dabei handelt es sich genau um das Verhalten der 3-Qubit-Fourier-Transformation. 

Wenn Sie neugierig sind, wie andere Eingabe Zustände betroffen sind, empfehlen wir Ihnen, mit der Anwendung von Qubit-Vorgängen vor der Transformation zu experimentieren.

## <a name="adding-measurements"></a>Hinzufügen von Messungen

Leider weist ein Eckpfeiler der Quantum-Mechanik darauf hin, dass ein reales Quantum-System nicht über eine solche Funktion verfügen kann `DumpMachine` . Stattdessen sind wir gezwungen, Informationen durch Messungen zu extrahieren, was im Allgemeinen nicht nur den vollständigen Quantum-Status bereitstellt, sondern auch das System selbst drastisch verändern kann.
Es gibt viele Arten von Quantum-Messungen, aber wir konzentrieren uns auf die grundlegendsten: Projective Messungen in einzelnen Qubits.
Bei der Messung (z. b. der Berechnungsbasis $ \{ \ket {0} , \ket {1} \} $) wird der Qubit-Zustand auf den jeweiligen Basisstatus projiziert,---daher jede übergeordnete Position zwischen den beiden zerstört.

Zum Implementieren von Messungen in einem Q #-Programm verwenden wir den- `M` Vorgang (from `Microsoft.Quantum.Intrinsic` ), der einen-Typ zurückgibt `Result` .

Zuerst wird der Vorgang so geändert, dass `Perform3QubitQFT` ein Array von Messergebnissen, `Result[]` , anstelle von zurückgegeben wird `Unit` .

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a>Array definieren und initialisieren `Result[]`

Vor der Zuweisung von Qubits (d.h. vor der- `using` Anweisung) deklarieren und binden wir dieses length-3-Array (eines `Result` für jedes Qubit): 

```qsharp
        mutable resultArray = new Result[3];
```

Mit dem- `mutable` Schlüsselwort, das mit der vorangestellt `resultArray` ist, kann die Variable später im Code wieder aufgefüllt werden---beispielsweise beim Hinzufügen unserer Messergebnisse.

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a>Ausführen von Messungen in einer `for` Schleife und Hinzufügen von Ergebnissen zu einem Array

Fügen Sie nach den Fourier Transform-Vorgängen innerhalb des- `using` Blocks den folgenden Code ein:

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
Die [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) Funktion, die für ein Array (z. b. unser Array von Qubits) aufgerufen wird, `qs` gibt einen Bereich über die Indizes des Arrays zurück. Hier verwenden wir Sie in unserer `for` Schleife, um jedes Qubit mithilfe der-Anweisung sequenziell zu messen `M(qs[i])` .
Jeder gemessene `Result` Typ (entweder `Zero` oder `One` ) wird dann der entsprechenden Indexposition in `resultArray` mit einer Update-and-REASSIGN-Anweisung hinzugefügt.

> [!NOTE]
> Die Syntax dieser Anweisung ist für Q # eindeutig, entspricht jedoch der ähnlichen Variablen Neuzuweisung `resultArray[i] <- M(qs[i])` in anderen Sprachen, wie z. b. F # und R.

Das-Schlüsselwort `set` wird immer zum erneuten Zuweisen von Variablen verwendet, die mit gebunden sind `mutable` .

#### <a name="return-resultarray"></a>Hre`resultArray`

Wenn alle drei Qubits gemessen werden und die Ergebnisse zu hinzugefügt `resultArray` wurden, ist es sicher, die Qubits wie zuvor zurückzusetzen und deren Zuteilung aufzuheben.
Fügen Sie nach dem Schließen des Blocks ein. `using`

```qsharp
        return resultArray;
```
, wenn die Ausgabe des Vorgangs letztendlich zurückgegeben werden soll. 

### <a name="understanding-the-effects-of-measurement"></a>Grundlegendes zu den Auswirkungen der Messung

Ändern wir nun die Platzierung unserer `DumpMachine` Funktionen, um den Zustand vor und nach den Messungen auszugeben.
Der endgültige Vorgangs Code sollte wie folgt aussehen: 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

Wenn Sie von der Befehlszeile aus arbeiten, wird das zurückgegebene Array am Ende der Ausführung einfach direkt in der Konsole gedruckt.
Aktualisieren Sie andernfalls das Host Programm, um das zurückgegebene Array zu verarbeiten.

#### <a name="command-line"></a>[Befehlszeile](#tab/tabid-cmdline)

Um mehr über das zurückgegebene Array zu erfahren, das in der Konsole gedruckt wird, können wir eine weitere `Message` in der Q #-Datei direkt vor der-Anweisung hinzufügen `return` :

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

Führen Sie das Projekt aus, und die Ausgabe sollte in etwa wie folgt aussehen:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[Python](#tab/tabid-python)

Aktualisieren Sie das Python-Programm wie folgt:

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

Führen Sie die Datei aus, und die Ausgabe sollte in etwa wie folgt aussehen:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[C#](#tab/tabid-csharp)

Nachdem der Vorgang nun ein Ergebnis zurückgegeben hat, ersetzen Sie den-Methodenaufrufe `Wait()` durch Abrufen der- `Result` Eigenschaft. Dadurch wird immer noch die gleiche Synchronisierung erzielt, die bereits erläutert wurde, und wir können diesen Wert direkt an die Variable binden `measurementResult` .

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

Führen Sie das Projekt aus, und die Ausgabe sollte in etwa wie folgt aussehen:

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

Diese Ausgabe veranschaulicht einige verschiedene Dinge:
1. Wenn Sie das zurückgegebene Ergebnis mit der prämessung vergleichen `DumpMachine` , wird die Post-QFT-Superposition in den Basis Zuständen eindeutig _nicht_ veranschaulicht.
    Eine Messung gibt nur einen einzelnen Basiszustand zurück, wobei eine Wahrscheinlichkeit von der Amplitude dieses Zustands in der wavefunction des Systems bestimmt wird.
2. Aus dem nach Maß der Messung `DumpMachine` sehen wir, dass die Messung den Zustand selbst _ändert_ und ihn von der anfänglichen übergeordneten Position über die Basiszustände in den einzelnen Basisstatus projiziert, der dem gemessenen Wert entspricht.

Wenn wir diesen Vorgang mehrmals wiederholen, sehen wir, dass die Ergebnis Statistik beginnt, um die gleich gewichtete Superposition des postqft-Zustands zu veranschaulichen, die zu einem zufälligen Ergebnis bei jedem Screenshot führt.
Da es _jedoch_nicht ineffizient und immer noch unvollständig ist, würde dies trotzdem nur die relativen Verstärkung der Basiszustände reproduzieren, nicht die relativen Phasen zwischen diesen.
Letzteres stellt in diesem Beispiel kein Problem dar. es werden jedoch relative Phasen angezeigt, wenn eine komplexere Eingabe für die QFT als $ \ket {000} $ vorliegt.

#### <a name="partial-measurements"></a>Partielle Messungen 
Wenn Sie untersuchen möchten, wie sich die Messung nur einiger Qubits des Registers auf den Zustand des Systems auswirken kann, versuchen Sie `for` , nach der Maßeinheit Folgendes in der Schleife hinzuzufügen:
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

Beachten Sie, dass Sie für den Zugriff auf die `IntAsString` Funktion Folgendes hinzufügen müssen: 
```qsharp
    open Microsoft.Quantum.Convert;
```
mit den restlichen Namespace- `open` Anweisungen.

In der resultierenden Ausgabe wird die schrittweise Projektion in Teilbereiche angezeigt, wenn jedes Qubit gemessen wird.


## <a name="use-the-q-libraries"></a>Verwenden der Q #-Bibliotheken
Wie in der Einführung erwähnt, liegt viel von den f #-Leistungsfähigkeit darin, dass es Ihnen ermöglicht, die sorgen für den Umgang mit einzelnen Qubits zu abstrahieren.
Wenn Sie vollständige, anwendbare Quantum-Programme entwickeln möchten, müssen Sie sich Gedanken darüber machen, ob ein `H` Vorgang vor oder nach einer bestimmten Drehung erfolgt. 

Die Q #-Bibliotheken enthalten den [QFT](xref:microsoft.quantum.canon.qft) -Vorgang, den Sie einfach ausführen und auf eine beliebige Anzahl von Qubits anwenden können.
Um es auszuprobieren, definieren Sie einen neuen Vorgang in der Q #-Datei, der denselben Inhalt von aufweist. `Perform3QubitQFT` allerdings ist alles vom ersten `H` bis zum `SWAP` Ersetzen durch zwei einfache Zeilen:
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
In der ersten Zeile wird einfach ein- [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) Ausdruck des zugeordneten Arrays von Qubits erstellt, `qs` was der [QFT](xref:microsoft.quantum.canon.qft) -Vorgang als Argument annimmt.
Dies entspricht der Index Reihenfolge der Qubits im Register.

Um Zugriff auf diese Vorgänge zu erhalten, fügen Sie `open` am Anfang der Q #-Datei-Anweisungen für ihre jeweiligen Namespaces hinzu:
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

Passen Sie nun das Host Programm so an, dass der Name des neuen Vorgangs (z. b. `PerformIntrinsicQFT` ) aufgerufen wird, und fügen Sie ihm einen Leerraum hinzu.

Um den tatsächlichen Vorteil der Verwendung der Q #-Bibliotheks Vorgänge anzuzeigen, ändern Sie die Anzahl der Qubits in einen anderen Wert als `3` :
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
Auf diese Weise können Sie den richtigen QFT für eine beliebige Anzahl von Qubits anwenden, ohne sich Gedanken über das Durcheinander neuer `H` Vorgänge und Rotationen für jedes Qubit machen zu müssen.

Beachten Sie, dass der Quantum-Simulator exponentiell mehr Zeit benötigt, wenn Sie die Anzahl der Qubits erhöhen---genau warum wir uns auf echte Quantum-Hardware freuen!













