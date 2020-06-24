---
title: Quantum-Charakterisierung und-Statistiken
description: Erfahren Sie, wie Sie mithilfe von Mess Statistiken aus Phasen Schätzungen die Ergebnis Werte in der Quantum-Programmierung schätzen.
author: QuantumWriter
uid: microsoft.quantum.libraries.characterization
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 7ed92c29020ccf389faa099f5bd80516af525578
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275021"
---
# <a name="quantum-characterization-and-statistics"></a>Quantum-Charakterisierung und-Statistiken #

Es ist wichtig, dass Sie die Auswirkungen von Vorgängen charakterisieren können, um nützliche Quantum-Algorithmen zu entwickeln.
Dies ist eine Herausforderung, da jede Messung eines Quantum-Systems höchstens ein Bit von Informationen ergibt.
Zum Erlernen eines Eigenwerts müssen die Ergebnisse von vielen Messungen zusammengefasst werden, damit der Benutzer die vielen Informationen, die für die Darstellung dieser Konzepte erforderlich sind, ggf. in die Lage versetzt.
Quantum-Zustände sind besonders ärgerlich, da das [No-Klon-Theorem](xref:microsoft.quantum.concepts.pauli#the-no-cloning-theorem) besagt, dass es keine Möglichkeit gibt, einen beliebigen Quantum-Zustand von einer einzelnen Kopie des Zustands zu erlernen, da Sie dadurch Kopien des Zustands erstellen können.
Diese Verschleierung des Quantums gibt an, dass Q # *den Zustand für* Quantum-Programme nicht verfügbar macht oder überhaupt nicht definiert.
Wir nähern uns daher der Quantum-Charakterisierung, indem wir Vorgänge und Zustände als Blackbox behandeln. Dieser Ansatz ist gemeinsam mit der experimentellen Praxis von Quantum-Charakterisierung, Verifizierung und Validierung (qcvv) gemeinsam.

Die Charakterisierung unterscheidet sich von vielen der anderen Bibliotheken, die bereits erläutert wurden.
Das Ziel hierbei ist weniger, klassische Informationen über das System zu erlernen, anstatt eine einheitliche Transformation für einen Zustands Vektor durchzuführen.
Diese Bibliotheken müssen daher sowohl die klassische als auch die Quantum-Informationsverarbeitung kombinieren.


## <a name="iterative-phase-estimation"></a>Iterative Phasen Schätzung ##

Das Anzeigen der Quantum-Programmierung in Bezug auf die Quantum-Darstellung schlägt eine sinnvolle Alternative zur Quantum-Phasen Schätzung vor.
Das heißt, anstelle einer $n $-Qubit-Registrierung, die eine binäre Darstellung der Phase wie in der Quantum-Phasen-Schätzung enthalten soll, können wir die Phasen Schätzung als den Prozess anzeigen, mit dem ein *klassischer* Agent mithilfe von Messungen Eigenschaften eines Quantum-Systems erfährt.
Wir gehen wie im Quantum-Fall vor, indem wir den Phasen-Kickback verwenden, um die Anwendungen eines Blackbox-Vorgangs in Drehung um einen unbekannten Winkel umzuwandeln. Sie messen jedoch das Ancilla-Qubit, das bei jedem Schritt unmittelbar nach der Drehung gedreht wird.
Dies hat den Vorteil, dass wir nur ein einzelnes zusätzliches Qubit benötigen, um das in der Quantum-Fall beschriebene Phasen Rückschreiben auszuführen, da wir dann die Phase der Messergebnisse bei jedem Schritt iterativ erlernen.  
Jede der unten vorgeschlagenen Methoden verwendet eine andere Strategie für das Entwerfen von Experimenten und verschiedene Datenverarbeitungsmethoden, um die Phase zu erlernen.  Sie verfügen jeweils über einen einzigartigen Vorteil, der von strengen Fehler Grenzen bis hin zu den Möglichkeiten zum einbeziehen vorheriger Informationen, zum tolerieren von Fehlern oder zur Verwendung von klassischen Computern mit Arbeitsspeicher verfügt.

Bei der Erörterung der iterativen Phasen Schätzung wird ein einheitlicher $U $ als schwarzer-Box-Vorgang berücksichtigt.
Wie im Abschnitt zu Oracles in [Datenstrukturen](xref:microsoft.quantum.libraries.data-structures)beschrieben, modelliert das Q #-Canon solche Vorgänge nach dem <xref:microsoft.quantum.oracles.discreteoracle> benutzerdefinierten Typ, der durch den tupeltyp definiert wird `((Int, Qubit[]) => Unit : Adjoint, Controlled)` .
Wenn `U : DiscreteOracle` , dann wird `U(m)` $U ^ m $ für implementiert `m : Int` .

Wenn diese Definition vorhanden ist, wird jeder Schritt der iterativen Phasen Schätzung fortgesetzt, indem ein zusätzliches Qubit im $ \ket{+} $-Status zusammen mit dem ursprünglichen Zustand $ \ket{\phi} $ vorbereitet wird. wir gehen davon aus, dass es sich um einen [eigen Vektor](xref:microsoft.quantum.concepts.matrix-advanced) von $U (m) $, d. h. $U (m) \ket{\phi} = e ^ {im\phi} \ Ket {\ Phi} $.  
Anschließend wird eine kontrollierte Anwendung von `U(m)` verwendet, die den Status $ \left (R \_ 1 (m \phi) \ket{+} \right) \ket{\phi} $ vorbereitet.
Wie im Fall von Quantum ist die Auswirkung einer kontrollierten Oracle-Anwendung exakt mit `U(m)` der Auswirkung von $R _1 $ für die unbekannte Phase auf $ \ket{+} $ identisch, sodass wir die Auswirkungen von $U $ auf diese einfachere Weise beschreiben können.
Optional dreht der Algorithmus das Steuerelement Qubit durch Anwenden von $R _1 (-m\erta) $, um den Status $ \ket{\psi} = \left (R \_ 1 (m [\phi-\erta]) \ket{+} \right) \ket{\phi} $ $ abzurufen.
Das zusätzliche Qubit, das als Steuerelement für verwendet `U(m)` wird, wird dann in der $X $-Basis gemessen, um eine einzelne klassische zu erhalten `Result` .

An diesem Punkt ist das erneute Erstellen der Phase aus den Werten, die `Result` durch die iterative Phasen Schätzung abgerufen werden, ein klassisches Statistisches Typrückschluss-Problem.
Das Auffinden des Werts $m $, der die gesammelten Informationen mit einer festgelegten Rückschluss Methode maximiert, ist einfach ein Problem in den Statistiken.
Wir betonen dies, indem wir die iterative Phasen Schätzung auf der theoretischen Ebene im bayyesian-parameterschätzungsformalismus kurz beschreiben, bevor wir mit der Beschreibung der statistischen Algorithmen in Q # Canon zum lösen dieses klassischen Inferenz Problems fortfahren.

### <a name="iterative-phase-estimation-without-eigenstates"></a>Iterative Phasen Schätzung ohne eigen Status ###

Wenn ein Eingabe Status angegeben wird, der kein eigen Status ist, was heißt, dass bei $U (m) \ket{\phi \_ j} = e ^ {im\phi \_ j} $ der Prozess der Phasen Schätzung nicht deterministisch zu einem einzelnen Energiezustand führt.  Der eigenständige Zustand, mit dem er letztendlich konvergiert, ist der Eigen Zustand, der höchstwahrscheinlich den beobachteten Wert erzeugt `Result` .

Der einzige Schritt von PE führt die folgende nicht einheitliche Transformation auf dem Status "\begin{align} \ sum_j \sqrt{\pr (\phi \_ j)} \ket{\phi \_ j} \mapsto \sum \_ j\frac {\ sqrt {\ PR (\phi)" aus. \_ j)} \sqrt{\pr (\text{result} | \phi \_ j)} \ket{\phi \_ j}} {\sqrt{\pr (\phi \_ j) \sum \_ j \pr (\text{result} | \phi \_ j)}}.
\end{align} wenn dieser Prozess über mehrere `Result` Werte durchlaufen wird, werden eigen Zustände, die keine maximalen Werte von $ \ prod_k \pr (\text{Result} \_ k | \phi \_ j) $ aufweisen, exponentiell unterdrückt.
Folglich wird der Rückschluss Prozess in der Regel mit einem einzelnen eigen Wert zusammengeführt, wenn die Experimente ordnungsgemäß ausgewählt werden.

Bayes ' Theorem gibt weiter an, dass der Zustand, der sich aus der Phasen Schätzung ergibt, in der Form \begin{align} \bruchteil {\sqrt{\pr (\phi \_ j)} \sqrt{\pr (\text{result} | \phi \_ j)} \ket{\phi j geschrieben wird. \_ }} {\sqrt{\pr (\phi \_ j) \sum \_ j \pr (\text{result} | \phi \_ j)}} = \ sum_j \sqrt{\pr (\phi \_ j | \text{result})} \ket{\phi \_ j}.
\end{align} hier $ \pr (\phi \_ j | \text{result}) $ kann als die Wahrscheinlichkeit interpretiert werden, die für jede Hypothese über die angegebenen Eigenwerte festgestellt wird:

1. Kenntnis des Quanten Zustands vor der Messung
2. Kenntnis der Eigen Zustände von $U $ und,
3. Kenntnis der Eigenwerte von $U $.

Das Erlernen dieser drei Dinge ist oft exponentiell auf einem klassischen Computer schwierig.
Das Hilfsprogramm der Phasen Schätzung ergibt sich aus der Tatsache, dass es eine solche Quantum Learning-Aufgabe ausführen kann, ohne dass Sie eine dieser Funktionen kennen.
Die Phasen Schätzung wird für diesen Grund innerhalb einer Reihe von Quantum-Algorithmen angezeigt, die exponentielle Beschleunigung bereitstellen.

### <a name="bayesian-phase-estimation"></a>Schätzung der bayesschen Phase ###

> [!TIP]
> Ausführlichere Informationen zur bayesschen Phasen Schätzung in der Praxis finden Sie im Beispiel für eine [**phaseschätzungsschätzung**](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) .

Die Idee der bayesschen Phasen Schätzung ist einfach.
Sie erfassen Mess Statistiken aus dem Phasen Schätz Protokoll und verarbeiten dann die Ergebnisse mit bayesschen Inferenz und geben eine Schätzung des Parameters an.
Diese Verarbeitung gibt Ihnen eine Schätzung des Eigenwerts und der Ungewissheit in dieser Schätzung.
Außerdem können Sie Adaptive Experimente durchführen und vorherige Informationen verwenden.
Der prinzipielle Nachteil der Methode ist, dass Sie Rechen technisch anspruchsvoll ist.

Um zu verstehen, wie dieser Bayessche Rückschluss Prozess funktioniert, sollten Sie den Fall der Verarbeitung eines einzelnen Ergebnisses in Erwägung gezogen `Zero` .
Beachten Sie, dass $X = \ket{+} \bra{+}-\ket {-} \bra {-} $ ist, sodass $ \ket{+} $ der einzige positive eigen Zustand von $X $ ist, der entspricht `Zero` .
Die Wahrscheinlichkeit, `Zero` dass eine [ `PauliX` Messung](xref:microsoft.quantum.concepts.pauli) auf dem ersten Qubit mit dem Eingabe Status $ \ket{\psi}\ket{\phi} $ beobachtet wird, ist folglich \begin{Equation} \pr (\texttt{Zero} | \psi) = \left | \braket{+ | \psi} \right | ^ 2.
\end{Equation} bei iterativer Phasen Schätzung, wir haben das $ \ket{\psi} = R_1 (m [\phi-\urta]) \ket{+} $, sodass \begin{align} \pr (\texttt{Zero} | \phi; m, \orta) & = \left | \braket{+ | R_1 (m [\phi-\orta]) | +} \right | ^ 2 \\ \\ & = \left | \bruchteil 12 \left (\bra {0} + \bra {1} \right) \left (\ket {0} + e ^ {i m [\phi-\erta]} \ket {1} \right) \right | ^ 2 \\ \\ & = \left | \bruchteil {1+ e ^ {i m [\phi-\teta]}} {2} \right | ^ 2 \\ \\ & = \cos ^ 2 (m [\phi-\teta]/2) \tag{★} \label{EQ: Phase-EST-Wahrscheinlichkeit}.
\end{align} das heißt, die iterative Phasen Schätzung besteht aus dem Erlernen der Schwingungs Häufigkeit einer Sinus förmigem-Funktion, wobei die Möglichkeit besteht, eine Münze mit einer von dieser Sinusoid angegebenen Abweichung zu kippen.
Nach der herkömmlichen klassischen Terminologie wird $ \eqref{EQ: Phase-EST-Wahrscheinlichkeit} $ die *Wahrscheinlichkeitsfunktion* für die iterative Phasen Schätzung aufgerufen.

Nachdem ein `Result` aus der Wahrscheinlichkeits Wahrscheinlichkeits-Funktion für iterative Phasen beobachtet wurde, können wir die Bayes-Regel verwenden, um vorzuschreiben, was in der Phase der Betrachtung folgen soll.
Konkret: \begin{Equation} \pr (\phi | d) = \bruchteil {\pr (d | \phi) \pr (\phi)} {\int \pr (d | \phi) \pr (\phi) {\mathrm d} \phi} \pr (\phi), \end{Equation} WHERE $d \in \\ {\texttt{Zero}, \texttt{One} \\ } $ ist `Result` , und WHERE $ \pr (\phi) $ beschreibt unsere früheren Überzeugungen zu $ \phi $.
Dadurch wird die iterative Phasen Schätzung explizit durchlaufen, da der Wert der nachfolgenden Distribution $ \pr (\phi | d) $ unsere Überzeugungen vor der Betrachtung der nächsten beschreibt `Result` .

Zu einem beliebigen Zeitpunkt während dieses Verfahrens können wir die Phase $ \hat{\phi} $, die vom klassischen Controller abgeleitet wurde, als "\begin{Equation} \hat{\phi} \mathrel{" melden: =} \erwartet [\phi | \text{Data}] = \int \phi \pr (\phi | \text{Data}) {\mathrm d} \phi, \end{Equation}, wobei $ \text{Data} $ für den gesamten Datensatz aller `Result` erhaltenen Werte steht.

Der genaue Bayessche Rückschluss ist in der Praxis unlösbar.
Um dies zu sehen, möchten wir eine $n $-Bit-Variable $x $ erlernen.
Die vorherige Distribution $ \pr (x) $ unterstützt mehr als $2 ^ n $ hypothetische Werte von $x $.
Dies bedeutet Folgendes: Wenn wir eine sehr genaue Schätzung $x $ benötigen, ist für die Bayes-Phasen Schätzung möglicherweise eine nicht benötigte Arbeitsspeicher-und Verarbeitungszeit erforderlich.
Während einige Anwendungen, wie z. b. die Quantum-Simulation, die erforderliche Genauigkeit nicht ausschließt, schließt andere Anwendungen, wie z. b. der Shor-Algorithmus, nicht den exakten bayesschen Rückschluss innerhalb des Phasen Schätz Schritts aus.  Aus diesem Grund werden auch Implementierungen für ungefähre Bayes-Methoden bereitgestellt, wie z. b. die [Random Walk-Phasen Schätzung (rwpe)](xref:microsoft.quantum.research.randomwalkphaseestimation.randomwalkphaseestimation) und auch nicht-Bayes-Ansätze, wie z. b. eine [robuste Phasen Schätzung](xref:microsoft.quantum.characterization.robustphaseestimation).

### <a name="robust-phase-estimation"></a>Stabile Phasen Schätzung ###

*Eine maximale nach* haltige Bayes-Wiederherstellung einer Phasen Schätzung von Messergebnissen ist im schlimmsten Fall exponentiell schwierig. Daher Opfern die meisten praktischen Phasen Schätz Algorithmen eine gewisse Qualität bei der Wiederherstellung, in Exchange für eine Menge klassischer Nachbearbeitung, die stattdessen Polynomisch mit der Anzahl der durchgeführten Messungen skaliert.

Ein Beispiel mit einem effizienten klassischen Nachbearbeitungsschritt ist der [robuste Phasen Schätz Algorithmus](https://arxiv.org/abs/1502.02677)mit der oben erwähnten Signatur und den oben erwähnten Eingaben. Dabei wird davon ausgegangen, dass Eingabe-einheitliche schwarze Felder $U $ als Typ verpackt werden `DiscreteOracle` und daher nur ganzzahlige Kräfte von kontrollierten $U $ Abfragen. Wenn der Eingabe Status im `Qubit[]` Register ein eigen Status $U \ket{\psi} = e ^ {i\phi} \ Ket {\ PSI} $ ist, gibt der robuste Algorithmus der Phasen Schätzung eine Schätzung $ \hat{\phi}\in [-\pi, \pi) $ von $ \phi $ als zurück `Double` .

Das wichtigste Feature der robusten Phasen Schätzung, das gemeinsam mit den meisten anderen nützlichen Varianten verwendet wird, besteht darin, dass die Erfolgs Qualität von $ \hat{\phi} $ in gewisser Weise Heisenberg-Limited ist. Dies bedeutet Folgendes: Wenn die Abweichung von $ \hat{\phi} $ von dem Wert "true" den Wert $ \sigma $ hat, wird "$ \sigma $" umgekehrt proportional zur Gesamtanzahl der Abfragen $Q $ an "kontrolliert-$U $" durchgeführt, d. h. $ \sigma = \mathcal{o} (1/Q) $. Nun variiert die Definition der Abweichung zwischen unterschiedlichen Schätz Algorithmen. In einigen Fällen kann dies bedeuten, dass bei mindestens $ \mathcal{o} (1) $ Wahrscheinlichkeit der Schätz Fehler $ | \hat{\phi}-\phi | \_ \circ\le \sigma $ bei einem Zirkel Measure $ \circ $. Bei einer robusten Phasen Schätzung ist die Abweichung genau die Varianz $ \sigma ^ 2 = \mathbb{e} \_ \hat{\phi} [(\Mod \_ {2 \ PI} (\hat{\phi}-\phi + \pi)-\pi) ^ 2] $, wenn wir die Zusammenfassung der periodischen Phasen in einem einzelnen begrenzten Intervall von $ (-\pi, \pi] $) ent Genauer: die Standardabweichung in der robusten Phasen Schätzung erfüllt die Ungleichheiten $ $ \begin{align} 2,0 \pi/q \le \sigma \le 2 \ Pi/2 ^ {n} \le 10.7 \ Pi/q, \end{align} $ $, wobei die untere Grenze im Limit von asympmearg Large $Q $ erreicht wird, und die obere Grenze ist auch bei kleinen Stichprobengrößen garantiert.  Beachten Sie, dass $n $ von der `bitsPrecision` Eingabe ausgewählt wurde, die implizit $Q $ definiert.

Weitere relevante Details sind z. a. der kleine Speicherplatz, der nur $1 $ Ancilla Qubit ist, oder, wenn die Prozedur nicht Adaptive ist, d. h. die erforderliche Sequenz von Quantum-Experimenten ist unabhängig von den zwischen Messergebnissen. In diesem und bevorstehenden Beispielen, in denen der Algorithmus der Phasen Schätzung von Bedeutung ist, sollten Sie in der Dokumentation wie @"microsoft.quantum.characterization.robustphaseestimation" und den referenzierten Veröffentlichungen darauf verweisen, um weitere Informationen und deren Implementierung zu erhalten.

> [!TIP]
> Es gibt viele Beispiele, in denen eine robuste Phasen Schätzung verwendet wird. Die Phasen Schätzung zum Extrahieren der Grund Zustands Energie des unterschiedlichen physischen Systems finden Sie im Beispiel für die [ **H2-Simulation** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/h2/command-line), das [ **simpleising** -Beispiel](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/simple)und das Beispiel für das Hubbard- [ **Modell** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/hubbard).


### <a name="continuous-oracles"></a>Kontinuierliche Oracles ###

Wir können auch aus dem oben verwendeten Oracle-Modell generalisieren, um fortlaufende Oracles zu ermöglichen, die nach dem Kanatyp modelliert werden <xref:microsoft.quantum.oracles.continuousoracle> .
Angenommen, anstelle eines einzelnen einheitlichen Operators $U $ haben wir eine Familie einheitlicher Operatoren $U (t) $ für $t \in \mathbb{r} $, sodass $U (t) U (s) $ = $U (t + s) $.
Dabei handelt es sich um eine schwächere Anweisung als im diskreten Fall, da wir einen erstellen können, <xref:microsoft.quantum.oracles.discreteoracle> indem wir $t = m \, \delta t $ für einige festgelegte $ \delta t $ einschränken.
Nach dem [Theorem des Steins](https://en.wikipedia.org/wiki/Stone%27s_theorem_on_one-parameter_unitary_groups), $U (t) = \exp (i H t) $ für einen Operator $H $, wobei $ \exp $ die Matrix exponentialweise ist, wie in [Advanced Matrizen](xref:microsoft.quantum.concepts.matrix-advanced)beschrieben.
Der Eigen Status $ \ket{\phi} $ von $H $, sodass $H \ket{\phi} = \phi \ket{\phi} $ auch der Eigen Status $U (t) $ für alle $t $, \begin{Equation} U (t) \ket{\phi} = e ^ {i \phi t} \ket{\phi}.
\end{equation}

Genau dieselbe Analyse, die für die Bayes- [Phasen Schätzung](#bayesian-phase-estimation) erläutert wurde, kann angewendet werden. und die Wahrscheinlichkeitsfunktion ist für dieses allgemeinere Oracle-Modell exakt identisch: $ $ \pr (\texttt{Zero} | \phi; t, \orta) = \cos ^ 2 \ Left (\bruchteil {t [\phi-\urta]} {2} \right).
Außerdem gilt: Wenn $U $ eine Simulation eines dynamischen Generators ist, wie es bei der [hamiltona-Simulation](xref:microsoft.quantum.libraries.applications#hamiltonian-simulation)der Fall ist, wird $ \phi $ als Strom interpretiert.
Durch die Verwendung der Phasen Schätzung mit kontinuierlichen Abfragen können wir also das simulierte [Strom Spektrum von Molekülen](https://arxiv.org/abs/quant-ph/0604193), [Materialien](https://arxiv.org/abs/1510.03859) oder [Feldtheorien](https://arxiv.org/abs/1111.3633v2) erlernen, ohne unsere Auswahl von Experimenten kompromittieren zu müssen, da $t $ eine ganze Zahl sein muss.

### <a name="random-walk-phase-estimation"></a>Schätzung der Zufalls Durchlauf Phase ###

Q # bietet eine hilfreiche Näherung der bayyesian-Phasen Schätzung, die für die Verwendung in der Nähe von Quantum-Geräten entwickelt wurde
Diese Methode ist sowohl adaptiv als auch vollständig deterministisch und ermöglicht eine nahezu optimale Skalierung von Fehlern in der geschätzten Phase $ \hat{\phi} $ mit sehr geringem Arbeitsspeicher Aufwand.

Das Protokoll verwendet eine ungefähre Bayessche Typrückschluss-Methode, die annimmt, dass die vorherige Verteilung Gaußsch ist.
Diese gausische Annahme ermöglicht es uns, eine analytische Formel für das Experiment zu verwenden, das die hintere Abweichung minimiert.
Der Algorithmus verschiebt dann basierend auf dem Ergebnis dieses Experiments die Schätzung von $ \phi $ nach links oder rechts um einen vorab festgelegten Betrag und verkleinert die Varianz um einen vordefinierten Betrag.
Dieser Mittelwert und die Varianz geben alle Informationen an, die erforderlich sind, um eine gausische vor $ \phi $ für das nächste Experiment anzugeben.
Unerwartete Messfehler oder das tatsächliche Ergebnis, das sich aus dem anfänglichen früheren Ergebnis ergibt, können dazu führen, dass diese Methode fehlschlägt.
Es wird nach einem Ausfall wieder hergestellt, um zu testen, ob der aktuelle Mittelwert und die Standardabweichung für das System geeignet sind.
Wenn dies nicht der Fall ist, führt der Algorithmus einen umgekehrten Schritt der exemplarischen Vorgehensweise aus, und der Prozess wird fortgesetzt.
Die Möglichkeit, rückwärts zu wechseln, ermöglicht es dem Algorithmus auch, zu lernen, auch wenn die anfängliche vorherige Standardabweichung nicht sehr klein ist.

## <a name="calling-phase-estimation-algorithms"></a>Algorithmen zur Aufruf Phasen Schätzung ##

Jeder Phasen Schätz Vorgang, der mit Q # Canon bereitgestellt wird, erfordert einen anderen Satz von Eingaben, der die Qualität parametrisiert, die wir für die abschließende Schätzung $ \hat{\phi} $ verlangen.
In diesen unterschiedlichen Eingaben werden allerdings mehrere allgemeine Eingaben gemeinsam genutzt, sodass die partielle Anwendung über den Qualitätsparametern eine gängige Signatur zur Folge hat.
Der <xref:microsoft.quantum.characterization.robustphaseestimation> im nächsten Abschnitt erörterte Vorgang hat z. b. die folgende Signatur:

```qsharp
operation RobustPhaseEstimation(bitsPrecision : Int, oracle : DiscreteOracle, eigenstate : Qubit[])  : Double
```

Die `bitsPrecision` Eingabe ist eindeutig für `RobustPhaseEstimation` , während `oracle` und `eigenstate` gemeinsam sind.
So kann ein Vorgang, wie in **H2Sample**gezeigt, einen iterativen Phasen Schätz Algorithmus mit einer Eingabe des Formulars akzeptieren, damit `(DiscreteOracle, Qubit[]) => Unit` ein Benutzer beliebige Phasen Schätz Algorithmen angeben kann:

```qsharp
operation H2EstimateEnergy(
    idxBondLength : Int,
    trotterStepSize : Double,
    phaseEstAlgorithm : ((DiscreteOracle, Qubit[]) => Double))
: Double
```

Diese unzähligen Phasen Schätz Algorithmen sind für verschiedene Eigenschaften und Eingabeparameter optimiert, die verstanden werden müssen, um die beste Wahl für die Zielanwendung zu treffen. Beispielsweise sind einige Phasen Schätz Algorithmen adaptiv, was bedeutet, dass zukünftige Schritte durch die Messergebnisse der vorherigen Schritte klassisch gesteuert werden. Für einige ist es erforderlich, dass das in der Lage ist, das in der Blackbox einheitliche Oracle-Element von beliebigen echten Kräften zu exponentiell zu machen, und andere benötigen nur ganzzahlige Kräfte, aber nur eine Phasen Schätzung von Modulo $2 \ Pi $ auflösen Einige erfordern viele zusätzliche Qubits, und andere erfordern nur eine.

Analog dazu verläuft die Verwendung der zufälligen walkphasen-Schätzung auf die gleiche Weise wie für andere Algorithmen, die mit dem Kanon bereitgestellt werden:

```qsharp
operation ApplyExampleOracle(
    eigenphase : Double,
    time : Double,
    register : Qubit[])
: Unit is Adj + Ctl {
    Rz(2.0 * eigenphase * time, register[0]);
}

operation EstimateBayesianPhase(eigenphase : Double) : Double {
    let oracle = ContinuousOracle(ApplyExampleOracle(eigenphase, _, _));
    using (eigenstate = Qubit()) {
        X(eigenstate);
        // The additional inputs here specify the mean and variance of the prior, the number of
        // iterations to perform, how many iterations to perform as a maximum, and how many
        // steps to roll back on an approximation failure.
        let est = RandomWalkPhaseEstimation(0.0, 1.0, 61, 100000, 1, oracle, [eigenstate]);
        Reset(eigenstate);
        return est;
    }
}
```
