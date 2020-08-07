---
title: Anwendungen in den Q# Standardbibliotheken
description: 'Erfahren Sie mehr über zwei grundlegende Anwendungen in Quantum Computing: hamiltonan Simulation und Shor-Suchalgorithmus.'
author: QuantumWriter
uid: microsoft.quantum.libraries.applications
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4caacaad127f8a4d3b6f77efe35ebe7d3b97cacf
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868762"
---
# <a name="applications"></a>Applications #

## <a name="hamiltonian-simulation"></a>Hamilton-Simulation ##

Die Simulation von Quantum-Systemen ist eine der aufregendsten Anwendungen der Quantum-Berechnung.
Auf einem klassischen Computer wird die Schwierigkeit, die Quantum-Mechanismen zu simulieren, im Allgemeinen mit der Dimension $N $ der zugehörigen Zustands Vektordarstellung skaliert.
Wenn diese Darstellung exponentiell mit der Anzahl von $n $ Qubits $N = 2 ^ n $ wächst, ist das Merkmal, das auch als [Fluch der Dimensionalität](xref:microsoft.quantum.concepts.multiple-qubits)bezeichnet wird, nicht mehr in die Quantum-Simulation der klassischen Hardware integriert.

Allerdings kann die Situation auf der Quantum-Hardware sehr unterschiedlich sein. Die häufigste Variation der Quantum-Simulation ist das zeitunabhängige hamiltona-Simulations Problem. Dort wird eine Beschreibung der System-hamiltonan $H $, eine hermitian-Matrix und ein anfänglicher Quantum-Status $ \ket{\psi (0)} $ bereitgestellt, der in gewisser Weise auf $n $ Qubits auf einem Quantum-Computer codiert wird. Die Quantum-Zustände in geschlossenen Systemen werden unter der Schrödinger-Gleichung $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = H \ket{\psi (t)} weiterentwickelt, \end{align} $ $ das Ziel ist die Implementierung des einheitlichen Time-Evolution-Operators $U (t) = e ^ {-IHT} $ zu einer festgelegten Zeit $t $, wobei $ \ket{\psi (t)} = U (t) \ket{\psi (0)} $ die Schrödinger-Gleichung löst.
Analog dazu löst das zeitabhängige hamiltona-Simulations Problem dieselbe Gleichung, aber mit $H (t) $ Now-Funktion.

Die hamiltona-Simulation ist eine wesentliche Komponente vieler anderer Probleme bei der Quantum-Simulation, und Lösungen für hamiltonein Simulations Problem sind Algorithmen, die eine Sequenz primitiver Quantum-Gates für die Zusammenstellung eines Näherungs Einheits-"$ \tilde{u} $" mit dem Fehler "$ \\ | \tilde{u}-U \\ [spectral norm](xref:microsoft.quantum.concepts.matrix-advanced) Die Komplexität dieser Algorithmen hängt stark davon ab, wie eine Beschreibung der hamiltona von Interesse für einen Quantum-Computer zugänglich gemacht wird. Wenn beispielsweise im ungünstigsten Fall $H $-$n $ Qubits als Liste von $2 ^ n \times 2 ^ n $-Nummern bereitgestellt werden soll, eine für jedes Matrixelement, ist das einfache Lesen der Daten bereits exponentiell Zeit erforderlich. Im besten Fall könnte der Zugriff auf eine Blackbox-einheitlich angenommen werden, die $O \ket{t}\ket{\psi (0)} = \ket{t}U (t) \ket{\psi (0)} $ triviale das Problem löst. Keines dieser Eingabe Modelle ist besonders interessant: das erste ist nicht besser als klassisches Verfahren, und das zweite als das schwarze Feld verbirgt die primitive Gate-Komplexität der Implementierung, die in der Anzahl der Qubits exponentiell sein könnte.

### <a name="descriptions-of-hamiltonians"></a>Beschreibungen der hamiltonane ###

Daher sind zusätzliche Annahmen des Formats der Eingabe erforderlich. Zwischen den Eingabe Modellen, die ausreichend aussagekräftig sind, müssen interessante hamiltonane berücksichtigt werden, wie z. b. jene für realistische physische Systeme oder interessante Berechnungs Probleme, und Eingabe Modelle, die ausreichend restriktiv sind, um auf einem Quantum-Computer effizient implementiert werden zu können. In der Literatur ist möglicherweise eine Vielzahl von nicht trivialen Eingabe Modellen enthalten, und Sie reichen von Quantum bis Classic. 

Als Beispiele für Quantum-Eingabe Modelle geht die [Beispiel basierte hamiltona-Simulation](http://www.nature.com/articles/s41534-017-0013-7) von einem Blackbox-Zugriff auf Quantum-Vorgänge aus, die Kopien der Dichte Matrix $ \rho $ erzeugen, die als hamiltona-$H $ verwendet werden. Beim Modell für den [einheitlichen Zugriff](https://arxiv.org/abs/1202.5822) unterliegt das, dass die hamiltona stattdessen in eine Summe von uniflüssen $ $ \begin{align} H & = \sum ^ {d-1} \_ {j = 0} a \_ j \hat{u} \_ j zerlegt wird. \end{align} $ $ WHERE $a \_ j>$0 sind Koeffizienten, und $ \hat{u} \_ j $ sind Uni-. Dann wird davon ausgegangen, dass eine über einen Blackbox-Zugriff auf die einheitliche Oracle-$V = \sum ^ {d-1} \_ {j = 0} \ket{j}\bra{j}\otimes \hat{u} \_ j $ verfügt, der das gewünschte $ \hat{u} j $ auswählt. \_ und die Oracle-$A \ket {0} = \sum ^ {d-1} \_ {j = 0} \sqrt{a \_ j/\ Sum ^ {d-1} \_ {k = 0} \alpha \_ j} \ket{j} $, die einen Quantum-Status zum Codieren dieser Koeffizienten erstellen. Im Fall von [hamiltonan-Simulation](https://arxiv.org/abs/quant-ph/0301023)mit geringer Dichte geht davon aus, dass es sich bei der hamiltonan um eine SparseMatrix mit nur $d = \mathcal{o} (\text{polylog} (N)) $ nicht-NULL-Element in jeder Zeile handelt. Außerdem wird davon ausgegangen, dass effiziente Quantum-Leitungen vorhanden sind, die den Speicherort dieser Elemente ungleich 0 (null) sowie die zugehörigen Werte ausgeben. Die Komplexität von [hamiltona-Simulations Algorithmen](xref:microsoft.quantum.more-information) wird in Bezug auf die Anzahl von Abfragen für diese schwarzen Felder ausgewertet. die Komplexität des primitiven Tors hängt dann sehr stark von der Schwierigkeit der Implementierung dieser schwarzen Felder ab.

> [!NOTE]
> Die Big-O-Notation wird häufig verwendet, um die Komplexitäts Skalierung von Algorithmen zu beschreiben. Bei zwei echten Funktionen $f g $ bedeutet der Ausdruck $g (x) = \mathcal{o} (f (x)) $, dass es eine absolute positive Konstante gibt $x \_ 0, c>$0, sodass $g (x) \le c f (x) $ für alle $x \ge x \_ $0. 

In den meisten praktischen Anwendungen, die auf einem Quantum-Computer implementiert werden müssen, müssen diese schwarzen Felder effizient implementiert werden, d. h. mit $ \mathcal{o} (\text{polylog} (N)) $ primitive quantgates. Stärker ist es erforderlich, dass eine effiziente simulier Bare, äußerst geringe, klassische Beschreibung vorhanden ist. In einer solchen Formulierung wird davon ausgegangen, dass die hamiltona in eine Summe von hermitian-Teilen $ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} H_j zerlegt wird.
\end{align} $ $ darüber hinaus wird davon ausgegangen, dass jeder Teil, ein hamiltonan $H \_ j $, leicht simuliert werden kann. Dies bedeutet, dass der einheitliche $e ^ {-IH \_ j t} $ für jede Zeit $t $ möglicherweise genau mithilfe von $ \mathcal{o} (1) $ primitiver Quantum-Gates implementiert wird. Dies gilt z. b. für den Sonderfall, dass jede $H \_ j $ lokale Pauli-Operatoren ist, d. h., Sie sind tensorflow-Produkte von $ \mathcal{o} (1) $ Non-Identity-Pauli-Operatoren, die auf räumlich schließende Qubits reagieren. Dieses Modell gilt besonders für physische Systeme mit begrenzter und lokaler Interaktion, da die Anzahl der Begriffe $d = \mathcal{o} (\text{polylog} (N)) $ ist und möglicherweise eindeutig geschrieben ist, d. h. in polynomzeit klassisch beschrieben.

> [!TIP]
> Hamiltonane, die in eine Summe von Teilen zerlegt werden, können mithilfe der Dynamical Generator-Darstellungs Bibliothek beschrieben werden. Weitere Informationen finden Sie im Abschnitt Dynamical Generator-Darstellung in [Datenstrukturen](xref:microsoft.quantum.libraries.data-structures).

### <a name="simulation-algorithms"></a>Simulations Algorithmen ###

Ein Quantum-Simulations Algorithmus konvertiert eine gegebene Beschreibung eines hamiltonins in eine Sequenz primitiver Quantum-Gates, die als Ganzes eine ungefähre Zeit-Evolution durch den Aufruf von hamiltonan bewirken.

Im besonderen Fall, in dem die hamiltona in eine Summe von hermischen Teilen zerlegt wird, ist die Trotter-Suzuki-Zerlegung ein besonders einfacher und intuitiver Algorithmus zum Simulieren von hamiltonen, die in eine Summe von hermitian-Komponenten zerlegt werden. Beispielsweise ein Integrator der ersten Bestellung dieser Familie entspricht $ $ \begin{align} U (t) & = \left (e ^ {-IH \_ 0 t/r} e ^ {-IH \_ 1 t/r} \cdots e ^ {-IH \_ {d-1} t/r} \right) ^ {r} + \mathcal{o} (d ^ 2 \ max_j \\ | H \_ j \\ | ^ 2 t ^ 2/r), \end{align} $ $ mithilfe eines Produkts von $r d $-Begriffen. 

> [!TIP]
> Anwendungen des Trotter-Suzuki-Simulations Algorithmus werden in den Beispielen behandelt.
> Das Erstellungs Modell, das nur die systeminternen Vorgänge verwendet, die von den einzelnen Ziel Computern bereitgestellt werden, finden Sie im [Beispiel **simpleising** ](https://github.com/microsoft/Quantum/blob/master/samples/simulation/ising/simple).
> Informationen zum Strukturierung von Modellen, die die Struktur der Trotter-Suzuki-Bibliothek verwenden, finden Sie im [Beispiel **isingtrotterbeispiel** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/trotter-evolution).
> Informationen zu molekularem Wasserstoff mithilfe der Struktur der Struktur von Trotter-Suzuki finden Sie im Beispiel für die [ **H2-Simulation** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/h2/command-line).

In vielen Fällen möchten wir den Simulations Algorithmus implementieren, sind jedoch nicht an den Details der Implementierung interessiert. Beispielsweise der Second-order Integrator entspricht $ $ \begin{align} U (t) & = \left (e ^ {-IH \_ 0 t/2R} e ^ {-IH \_ 1 t/2R} \cdots e ^ {-IH \_ {d-1} t/2R} e ^ {-IH \_ {d-1} t/2R} \cdots e ^ {-IH \_ 1 t/2R} e ^ {-IH \_ 0 t/2R} \right) ^ {r} + \mathcal{o} (d ^ 3 \ max_j \\ | H \_ j \\ | ^ 3 t ^ 3/r ^ 2), \end{align} $ $ unter Verwendung eines Produkts von $2RD $ Terms. Größere Bestellungen umfassen noch mehr Begriffe, und optimierte Varianten erfordern möglicherweise sehr untriviale Ordnungen in den Exponentialzahlen. Andere erweiterte Algorithmen können auch die Verwendung von "Ancilla Qubits" in Zwischenschritten einschließen. Daher verpacken wir Simulations Algorithmen im Kanon als benutzerdefinierten Typ.

```qsharp
newtype SimulationAlgorithm = ((Double, EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl);
```

Der erste Parameter `Double` ist die Simulationszeit, der zweite Parameter `EvolutionGenerator` , der im Abschnitt "Dynamical Generator Darstellung" der [Datenstrukturen](xref:microsoft.quantum.libraries.data-structures)abgedeckt ist, ist eine klassische Beschreibung einer zeitunabhängigen hamiltona, die eine Anleitung dazu gibt, wie die einzelnen Begriffe in der hamiltonan durch eine Quantum-Verbindung simuliert werden können. Die Typen dieses Formulars nähern sich dem einheitlichen Vorgang $e ^ {-IHT} $ für den dritten Parameter, bei dem es `Qubit[]` sich um das Register handelt, das den Quantenzustand des simulierten Systems speichert. Entsprechend definieren wir bei zeitabhängigen Fällen einen benutzerdefinierten Typ mit einem `EvolutionSchedule` Typ, der eine klassische Beschreibung eines zeitabhängigen hamiltones ist.

```qsharp
newtype TimeDependentSimulationAlgorithm = ((Double, EvolutionSchedule, Qubit[]) => Unit : Adjoint, Controlled);
```

Beispielsweise kann die Trotter-Suzuki-Zerlegung mithilfe der folgenden Funktionen von Canon aufgerufen werden, mit Parametern, `trotterStepSize` die die Dauer der Simulation in den einzelnen exponentialwerte ändern, und `trotterOrder` für die Reihenfolge des gewünschten Integrator.

```qsharp
function TrotterSimulationAlgorithm(
    trotterStepSize : Double, 
    trotterOrder : Int) 
: SimulationAlgorithm {
    ...
}

function TimeDependentTrotterSimulationAlgorithm(
    trotterStepSize : Double, 
    trotterOrder : Int) 
: TimeDependentSimulationAlgorithm {
    ...
}
```

> [!TIP]
> Anwendungen der Simulations Bibliothek werden in den Beispielen behandelt. Informationen zur Phasen Schätzung im ersierenden Modell mithilfe von finden `SimulationAlgorithm` Sie im [Beispiel **isingphaseschätz.** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/phase-estimation)
> Informationen zur Vorbereitung des adiabatischen Zustands im ersierenden Modell mithilfe von finden `TimeDependentSimulationAlgorithm` Sie im Beispiel " [ **adiabaticising** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/adiabatic)".


### <a name="adiabatic-state-preparation--phase-estimation"></a>Schätzung der adiabatischen Zustands Vorbereitung & Phasen ###

Eine gängige Anwendung der hamiltonan-Simulation ist die adiabatische Zustands Vorbereitung. Hier wird eine der beiden hamiltonane $H \_ {\text{Start}} $ und $H \_ {\text{End}} $ und der Quantum State $ \ket{\psi (0)} $ bereitgestellt, der den Grundzustand der Start-hamiltona $H \_ {\text{Start}} $ ist. In der Regel wird $H \_ {\text{Start}} $ ausgewählt, sodass $ \ket{\psi (0)} $ leicht aus dem Berechnungsbasis Status $ \ket{0\cdots 0} $ vorbereitet werden kann. Durch die gleich lange Interpolation zwischen diesen hamiltonoren im zeitabhängigen Simulations Problem ist es möglich, mit hoher Wahrscheinlichkeit in einem Grundzustand der abschließenden hamiltonan $H \_ {\text{End}} $ zu enden. Obwohl das Vorbereiten von guten Näherungen an den hamiltona-Boden Status auf diese Weise fortgesetzt werden kann, indem für zeitabhängige hamiltonalgorithmen-Simulations Algorithmen als Unterroutine aufgerufen werden, sind andere konzeptionell unterschiedliche Ansätze wie z. b. die Variational Quantum eigen Solver möglich.

Eine andere Anwendung, die in der Quantum-Chemie universell ist, schätzt jedoch die Grund Zustands Energie der hamiltonane, die die Zwischenschritte der chemischen Reaktion darstellen. Ein solches Schema könnte z. b. auf der Vorbereitung des Adiabatic-Zustands basieren, um den Bodenzustand zu erzeugen, und dann zeitunabhängige hamiltoneine Simulation als Unterroutine in der Zeit der Phasen Schätzung einbeziehen, um diese Energie mit einem begrenzten Fehler und einer Erfolgswahrscheinlichkeit zu extrahieren. 

Abstrahieren von Simulations Algorithmen als benutzerdefinierte Typen `SimulationAlgorithm` und `TimeDependentSimulationAlgorithm` ermöglichen es uns, ihre Funktionalität bequem in komplexere Quantum-Algorithmen einzubinden. Dies hat zur Folge, dass wir für diese häufig verwendeten Unterroutinen dasselbe tun müssen.

Daher wird die bequeme Funktion definiert.

```qsharp
function InterpolatedEvolution(
        interpolationTime : Double, 
        evolutionGeneratorStart : EvolutionGenerator,
        evolutionGeneratorEnd : EvolutionGenerator,
        timeDependentSimulationAlgorithm : TimeDependentSimulationAlgorithm)
: (Qubit[] => Unit is Adj + Ctl) {
        ...
}
 
```

Dadurch wird ein einheitlicher Vorgang zurückgegeben, der alle Schritte der adiabatischen Zustands Vorbereitung implementiert. Der erste Parameter `interpolatedTime` definiert die Zeit, zu der wir eine lineare interpolieren zwischen der vom zweiten Parameter beschriebenen Start-hamiltona `evolutionGeneratorStart` und dem End hamiltona durch den dritten Parameter durchgeführt haben `evolutionGeneratorEnd` . Der vierte Parameter `timeDependentSimulationAlgorithm` ist die Wahl des Simulations Algorithmus. Beachten Sie, dass `interpolatedTime` , wenn lang genug ist, ein ursprünglicher Ausgangszustand für die gesamte Dauer der zeitabhängigen Simulation ein sofortiger Grundzustand der hamiltona ist und somit den Grundzustand des enden hamiltones endet.

Außerdem wird ein hilfreicher Vorgang definiert, der automatisch alle Schritte eines typischen quantumchemie-Experiments ausführt. Zum Beispiel verfügen wir über Folgendes, das eine Energie Schätzung des von der Adiabatic-Zustands Vorbereitung erzeugten Zustands zurückgibt:

```qsharp
operation EstimateAdiabaticStateEnergy(
    nQubits : Int,
    statePrepUnitary : (Qubit[] => Unit),
    adiabaticUnitary : (Qubit[] => Unit),
    qpeUnitary: (Qubit[] => Unit is Adj + Ctl),
    phaseEstAlgorithm : ((DiscreteOracle, Qubit[]) => Double))
: Double {
...
}
```

`nQubits`die Anzahl der Qubits, die zum Codieren des anfänglichen Quantums verwendet werden. `statePrepUnitary`bereitet den Startstatus von der Berechnungsbasis $ \ket{0\cdots 0} $ vor. `adiabaticUnitary`ist der einheitliche Vorgang, der die adiabatische Zustands Vorbereitung implementiert, z. b. durch die- `InterpolatedEvolution` Funktion erzeugt. `qpeUnitary`der einheitliche Vorgang, der verwendet wird, um die Phasen Schätzung für den resultierenden Quantum-Zustand auszuführen. `phaseEstAlgorithm`ist die Wahl des Algorithmus zur Phasen Schätzung.

> [!TIP]
> In den Beispielen werden Anwendungen der Adiabatic-Zustands Vorbereitung behandelt. Informationen zum Erstellungsmodell, das eine manuelle Implementierung der adiabatischen Zustands Vorbereitung und der Verwendung der- `AdiabaticEvolution` Funktion verwendet, finden Sie im Beispiel " [ **adiabaticising** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/adiabatic)".
> Informationen zur Phasen-und adiabatischen Zustands Vorbereitung im ersierungsmodell finden Sie im [Beispiel **isingphaseschätz.** ](https://github.com/microsoft/Quantum/tree/master/samples/simulation/ising/phase-estimation)

> [!TIP]
> Die [Simulation von molekularer Wasserstoff](https://github.com/microsoft/Quantum/tree/master/samples/simulation/h2/command-line) ist ein interessantes und kurzes Beispiel. Das Modell und die experimentellen Ergebnisse, die in der Datei "" [.](https://arxiv.org/abs/1512.06860) erfordert nur die Pauli-Matrizen und hat das Format $ \hat H = g \_ {0} I \_ 0i \_ 1 + g \_ 1 {Z \_ 0} + g \_ 2 {z \_ 1} + g \_ 3 {z \_ 0} {z \_ 1} + g \_ 4 {y \_ 0} {y \_ 1} + g \_ 5 {x \_ 0} {x \_ 1} $. Dabei handelt es sich um eine effektive hamiltona, die nur 2 Qubits erfordert, bei denen die Konstanten $g $ aus der Entfernung $R $ zwischen den beiden Wasserstoffatomen berechnet werden. Mithilfe von kanonischen Funktionen werden die Paulis in Uni-und dann über kurze Zeiträume mithilfe der Trotter-Suzuki-Zerlegung weiterentwickelt. Eine gute Näherung für den $H _2 $ Ground State kann ohne Verwendung der Adiabatic-Zustands Vorbereitung erstellt werden. Daher kann die Grund Zustands Energie direkt durch die Verwendung der Phasen Schätzung vom Kanon gefunden werden.

## <a name="shors-algorithm"></a>Shor-Algorithmus ##
Der Shor-Algorithmus ist eine der wichtigsten Entwicklungen bei der quantumberechnung, da er zeigte, dass Quantum-Computer verwendet werden könnten, um wichtige, zurzeit klassisch unlösbare Probleme zu lösen.
Der Shor-Algorithmus bietet eine schnelle Möglichkeit, um große Zahlen mithilfe eines Quantum-Computers zu berücksichtigen, ein Problem, das als *Factoring*bezeichnet wird.
Die Sicherheit vieler vorhandener Kryptosysteme basiert auf der Annahme, dass kein schneller Algorithmus für das Factoring vorhanden ist.
Daher hat der Shor-Algorithmus einen tiefgreifenden Einfluss auf die Sicherheit in einer Post-Quantum-Welt.

Der Shor-Algorithmus kann als Hybrid Algorithmus betrachtet werden.
Der Quantum-Computer wird verwendet, um eine Rechen harte Aufgabe auszuführen, die als Zeitraum der Suche bezeichnet wird.
Die Ergebnisse aus der Zeitraum Suche werden dann klassisch verarbeitet, um die Faktoren einzuschätzen.
Wir überprüfen diese beiden Schritte unten.

### <a name="period-finding"></a>Suche nach Zeitraum ###

Nachdem Sie gesehen haben, wie die Quantum Fourier-Transformation und-Phasen Schätzung funktionieren (siehe [Quantum-Algorithmen](xref:microsoft.quantum.libraries.standard.algorithms)), können wir diese Tools verwenden, um ein klassisches, schwer wiesendes Problem mit dem Namen " *Zeit Suche*"  Im nächsten Abschnitt erfahren Sie, wie Sie die Zeitspanne für das Factoring anwenden.

Bei zwei Ganzzahlen $a $ und $N $, bei denen $a<N $, das Ziel der Zeit Steuerungs Suche (auch als Bestellsuche bezeichnet) ist, die _Reihenfolge_ $r $ of $a $ modulo $N $ zu finden, wobei $r $ als die geringste positive Ganzzahl definiert ist, die $a ^ r \equiv 1 \text{mod} N $.  

Zum Ermitteln der Bestellung mithilfe eines Quantum-Computers wir können den Phasen Schätz Algorithmus verwenden, der auf den folgenden einheitlichen Operator angewendet wird $U _A $: $ $ U_a \ket{x} \equiv \ket{(AX) \text{mod} N}. $ $ die Eigenvektoren $U _A $ gelten für Integer $s $ und $0 \ Leq s \leq r-$1, $ $ \ket{x_s} \equiv 1/\sqrt{r} \sum \_ {k = 0} ^ {r-1} e ^ {\bruchteil {-2\pi i SK} {r}} \ket{a ^ k\text {mod} N}, $ $ sind _eigen Zustände_ der $U _A $.
Die Eigenwerte $U _A $ sind $ $ U \_ a \ket{x \_ s} = e ^ {2 \ Pi i s/r} \ket{x \_ s}. $$

Bei der Phasen Schätzung werden daher die Eigenwerte $e ^ {2 \ Pi i s/r} $ ausgegeben, aus denen $r $ mithilfe der [fortgesetzten Bruch](https://en.wikipedia.org/wiki/Continued_fraction) Zahlen von $s/r $ effizient erlernt werden kann.

Das Verbindungs Diagramm für das Auffinden von Quantum-Perioden lautet:

![Verbindungs Diagramm für die Suche nach Quantum-Zeit](~/media/QPE.svg)

Hier werden $2N $ Qubits mit "$ \ket $" initialisiert, {0} und $n $ Qubits werden mit "$ \ket $" initialisiert {1} .
Der Reader kann sich vielleicht Fragen, warum das Quantum-Register zum Speichern der Eigen Zustände mit "$ \ket $" initialisiert wird {1} .
Da die Reihenfolge $r $ im Voraus nicht bekannt ist, können wir $ \ket{x_s} $ States nicht direkt vorbereiten.
Glücklicherweise hat sich herausstellt, dass $1/\ sqrt {r} \sum \_ {s = 0} ^ {r-1} \ket{x \_ s} = \ket {1} $ ist.
Wir müssen $ \ket{x} $! nicht tatsächlich vorbereiten.
Wir können einfach ein Quantum-Register von $n $ Qubits im Status $ \ket {1} $ vorbereiten. 

Die Verbindung enthält den QFT und mehrere kontrollierte Gates.
Das QFT-Gate wurde [zuvor](xref:microsoft.quantum.libraries.standard.algorithms)beschrieben.
Der gesteuerte $U _A $ Gate ordnet $ \ket{x} $ zu $ \ket{(AX) \text{mod} N} $ zu, wenn das Steuerelement-Qubit $ \ket {1} $ ist, und ordnet $ \ket{x} $ auf $ \ket{x} $ zu.

Um $ (a ^ NX) \text{mod} n $ zu erreichen, können wir einfach "gesteuerte-$U _ {a ^ n} $" anwenden, wobei wir $a ^ N \text{mod} n $ klassisch berechnen, um in die Quantum-Leitung zu gelangen.  
Die Verbindungen, um eine solche Modulare Arithmetik zu erzielen, wurden in der Dokumentation für die [Quantum-Arithmetik](./algorithms.md#arithmetic)beschrieben. insbesondere benötigen wir eine modulare exponentiations Verbindung, um die kontrollierten $U \_ {a ^ i} $-Vorgänge zu implementieren.

Die obige Verbindung entspricht der [Quantum-Phasen-Schätzung](xref:microsoft.quantum.characterization.quantumphaseestimation) und ermöglicht das explizite Sortieren der Reihenfolge. die Anzahl der benötigten Qubits kann reduziert werden. Wir können die-Methode von Beauregard für die Bestellsuche befolgen, wie [auf Seite 8 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=8)beschrieben, oder Sie können eine der Phasen Schätz Routinen verwenden, die in Microsoft. Quantum. Charakterisierung verfügbar sind. Beispielsweise wird bei der [robusten Phasen Schätzung](xref:microsoft.quantum.characterization.robustphaseestimation) auch ein zusätzliches Qubit verwendet.
 
### <a name="factoring"></a>Berücksichtigung ###
Das Ziel der Factoring besteht darin, die beiden Hauptfaktoren der ganzzahligen $N $ zu ermitteln, wobei $N $ eine $n $-Bit-Zahl ist.  
Das Factoring besteht aus den unten beschriebenen Schritten. Die Schritte sind in drei Teile unterteilt: eine klassische Vorverarbeitungs Routine (1-4); eine Quantum Computing-Routine zum Ermitteln der Reihenfolge $a \text{mod} N $ (5); und eine klassische nachträglich verarbeitetes-Routine zur Ableitung der Prim Faktoren aus der Reihenfolge (6-9).

Die klassische Vorverarbeitungs Routine besteht aus den folgenden Schritten:
1. Wenn $N $ gleich ist, wird der Primfaktor $2 $ zurückgegeben.
2. Wenn $N = p ^ q $ for $p \geq1 $, $q \geq2 $, wird der Primfaktor $p $ zurückgegeben.  Dieser Schritt wird klassisch ausgeführt.
3. Wählen Sie eine Zufallszahl $a $ aus, sodass $1 < ein < N-$1.
4. Wenn $ \text{GCD} (a, n) >$1, wird der Prim Faktor $ \text{GCD} (a, N) zurückgegeben. Dieser Schritt wird mit dem Algorithmus von Euclid berechnet.
Wenn kein Prim Faktor zurückgegeben wurde, fahren wir mit der Quantum-Routine fort:
5. Aufrufen des Algorithmus zum Ermitteln der Quantum-Zeitspanne, um die Reihenfolge $r $ of $a \text{mod} N $ zu berechnen. Verwenden Sie $r $ in der klassischen nachträglich verarbeitetes-Routine, um die wichtigsten Faktoren zu ermitteln:
6. Wenn $r $ ungerade ist, wechseln Sie zurück zum Vorverarbeitungs Schritt (3).
7. Wenn $r $ gleich ist, und $a ^ {r/2} =-1 \ Text {mod} N $, gehen Sie zurück zum Vorverarbeitungs Schritt (3).
8. Wenn $ \text{GCD} (a ^ {r/2} + 1, n) $ ein nicht trivialer Faktor $N $ ist, wird $ \text{GCD} (a ^ {r/2} + 1, n) $ zurückgegeben.
9. Wenn $ \text{GCD} (a ^ {r/2}-1, n) $ ein nicht trivialer Faktor $N $ ist, wird $ \text{GCD} (a ^ {r/2}-1, n) $ zurückgegeben.


Der Factoring-Algorithmus ist probabilistisch: Es kann angezeigt werden, dass die Wahrscheinlichkeit mindestens eine Hälfte ist, dass $r $ gleich ist, und $a ^ {r/2} \netq-1 \text{mod} N $, wodurch ein Prim Faktor erzeugt wird.  ( [Weitere Informationen](xref:microsoft.quantum.more-information)finden Sie im [Originalartikel von Shor](https://doi.org/10.1109/SFCS.1994.365700) oder einem der *grundlegenden Quantum Computing* -Texte in.)
Wenn kein Prim Faktor zurückgegeben wird, wiederholen Sie einfach den Algorithmus aus Schritt (1).  Nach $n $ tries beträgt die Wahrscheinlichkeit, dass jeder Versuch fehlgeschlagen ist, höchstens $2 ^ {-n} $.
Daher ist es nach dem Wiederholen des Algorithmus sehr gering, dass der Erfolg praktisch sicher ist.
