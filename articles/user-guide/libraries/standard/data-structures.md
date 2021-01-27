---
title: Datenstrukturen in den Q# Standardbibliotheken
description: Erfahren Sie mehr über Datenstrukturen, Oracles und dynamikalische Generatoren in den Microsoft- Q# Standardbibliotheken.
author: QuantumWriter
uid: microsoft.quantum.libraries.data-structures
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: e9b593ba69ed41a9fb3c1298b5b945a4cbe43d5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858332"
---
# <a name="data-structures-and-modeling"></a>Datenstrukturen und Modellierung #

## <a name="classical-data-structures"></a>Klassische Datenstrukturen ##

Zusammen mit benutzerdefinierten Typen für die Darstellung von Quantum-Konzepten stellt der Kanon auch Vorgänge, Funktionen und Typen für die Arbeit mit klassischen Daten bereit, die bei der Steuerung von Quantum-Systemen verwendet werden.
Beispiels <xref:Microsoft.Quantum.Arrays.Reversed> Weise nimmt die Funktion ein Array als Eingabe an und gibt dasselbe Array in umgekehrter Reihenfolge zurück.
Dies kann dann für ein Array des Typs verwendet werden `Qubit[]` , um zu vermeiden, dass unnötige $ \operatschmue{curap} $ Gates beim Konvertieren zwischen den ganzen Zahlen von ganzen Zahlen angewendet werden müssen.
Ebenso haben wir im vorherigen Abschnitt gesehen, dass Formular Typen für die `(Int, Int -> T)` Darstellung von zufälligen Zugriffs Auflistungen nützlich sein können, sodass die- <xref:Microsoft.Quantum.Arrays.LookupFunction> Funktion eine bequeme Möglichkeit bietet, solche Typen aus Array Typen zu erstellen.

### <a name="pairs"></a>Chen ###

Der Kanon unterstützt die Funktionsweise Notation für Paare, was den Zugriff auf Tupel durch die decoerstellung ergänzt:

```qsharp
let pair = (PauliZ, register); // type (Pauli, Qubit[])
ApplyToEach(H, Snd(pair)); // No need to deconstruct to access the register.
```

### <a name="arrays"></a>Arrays ###

Der Kanon stellt mehrere Funktionen zum Bearbeiten von Arrays bereit.
Diese Funktionen sind typparametrisiert und können daher mit Arrays eines beliebigen Typs verwendet werden Q# .
Beispielsweise gibt die- <xref:Microsoft.Quantum.Arrays.Reversed> Funktion ein neues Array zurück, dessen Elemente in umgekehrter Reihenfolge von der Eingabe zurückgegeben werden.
Dies kann verwendet werden, um zu ändern, wie ein Quantum-Register beim Aufrufen von Vorgängen dargestellt wird:

```qsharp
let leRegister = LittleEndian(register);
// QFT expects a BigEndian, so we can reverse before calling.
QFT(BigEndian(Reversed(leRegister!)));
// This is how the LittleEndianAsBigEndian function is implemented:
QFT(LittleEndianAsBigEndian(leRegister));
```

Ebenso kann die- <xref:Microsoft.Quantum.Arrays.Subarray> Funktion verwendet werden, um die Elemente eines Arrays neu anzuordnen oder Teilmengen zu nehmen:

```qsharp
// Applies H to qubits 2 and 5.
ApplyToEach(H, Subarray([2, 5], register));
```

In Kombination mit der Fluss Steuerung können Array Bearbeitungsfunktionen wie z. b. <xref:Microsoft.Quantum.Arrays.Zipped> eine leistungsstarke Möglichkeit zum Ausdrücken von Quantum-Programmen bieten:

```qsharp
// Applies X₃ Y₁ Z₇ to a register of any size.
ApplyToEach(
    ApplyPauli(_, register),
    Map(
        EmbedPauli(_, _, Length(register)),
        Zipped([PauliX, PauliY, PauliZ], [3, 1, 7])
    )
);
```

## <a name="oracles"></a>Oracles ##

In der Literatur der [Phasen Schätzung](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm) und der [Amplitude-Verstärkung](https://en.wikipedia.org/wiki/Amplitude_amplification) erscheint das Konzept eines Oracle häufig.
Hier bezieht sich der Begriff Oracle auf eine Quantum-Unterroutine, die auf einen Satz von Qubits folgt und die Antwort als Phase zurückgibt.
Diese Unterroutine kann sich oft als Eingabe für einen Quantum-Algorithmus vorstellen, der das Oracle zusätzlich zu einigen anderen Parametern annimmt, und eine Reihe von Quantum-Vorgängen anwendet und einen aufzurufenden aufrufungs Vorgang als grundlegende Gate behandelt.
Um den größeren Algorithmus tatsächlich zu implementieren, muss eine konkrete Zerlegung des Oracle in grundlegende Gates bereitgestellt werden, aber eine solche Zerlegung ist nicht erforderlich, um den Algorithmus zu verstehen, der das Oracle aufruft.
In Q# wird diese Abstraktion durch Verwendung von dargestellt, wobei es sich bei den Vorgängen um erstklassige Werte handelt, sodass Vorgänge in einer Blackbox-Weise an Implementierungen von Quantum-Algorithmen übermittelt werden können.
Darüber hinaus werden benutzerdefinierte Typen verwendet, um die verschiedenen Oracle-Darstellungen auf typsichere Weise zu bezeichnen. dadurch ist es schwierig, unterschiedliche Arten von Black Box-Vorgängen versehentlich zu verscheihen.

Solche Oracles werden in verschiedenen Kontexten angezeigt, einschließlich bekannter Beispiele wie [der Such-und Quantum-Simulations Algorithmen von Grover](https://en.wikipedia.org/wiki/Grover%27s_algorithm) .
Hier konzentrieren wir uns auf die Oracles, die nur für zwei Anwendungen benötigt werden: Amplitude-Verstärkung und Phasen Schätzung.
Zuerst werden Amplitude-Verstärkungs-Oracles erläutert, bevor die Phasen Schätzung fortgesetzt wird.

### <a name="amplitude-amplification-oracles"></a>Amplitude-Verstärkungs-Oracles ###

Der Amplitude-Verstärkungs Algorithmus zielt darauf ab, eine Drehung zwischen einem Anfangszustand und einem Endzustand durch Anwenden einer Sequenz von Reflektionen des Zustands auszuführen.
Damit der Algorithmus funktionsfähig ist, muss er beide Zustände angeben.
Diese Spezifikationen werden durch zwei Oracles angegeben.
Diese Oracles funktionieren durch Aufteilen der Eingaben in zwei Leerzeichen, einem "Ziel"-Teilbereich und einem "ursprünglichen" Teilbereich.
Die Oracles identifizieren solche Teilbereiche, ähnlich wie bei der Verwendung von "Pauli"-Operatoren zwei Leerzeichen, indem Sie eine $ \pm $1-Phase auf diese Leerzeichen anwenden.
Der Hauptunterschied besteht darin, dass diese Leerzeichen in dieser Anwendung keine halben Leerzeichen sein müssen.
Beachten Sie auch, dass diese beiden Teilbereiche sich nicht gegenseitig ausschließen: Es werden Vektoren vorhanden sein, die Mitglieder beider Leerzeichen sind.
Wenn dies nicht der Fall ist, hätte die Amplitude-Verstärkung keine Auswirkung, daher benötigen wir den ursprünglichen Teilbereich, um eine Überschneidung ungleich NULL mit dem Ziel Teilbereich zu erhalten.

Wir bezeichnen das erste Oracle, das wir für die Amplitude-Verstärkung benötigen \_ , $P $0, das für die folgende Aktion definiert ist.  Für alle Zustände $ \ket{x} $ im "ursprünglichen" Teilbereich $P \_ 0 \ket{x} =-\ket{x} $ und für alle Zustände $ \ket{y} $, die sich nicht in diesem Teilbereich befinden, ist $P \_ 0 \ket{y} = \ket{y} $ vorhanden.
Das Oracle, das den Ziel Teilbereich ($P _1 $) kennzeichnet, hat genau dasselbe Formular.
Für alle Zustände $ \ket{x} $ im Ziel Teilbereich (d. h. für alle Zustände, die der Algorithmus ausgeben soll), $P _1 \ Ket {x} =-\ket{x} $.
Gleiches gilt für alle Zustände $ \ket{y} $, die sich nicht im Ziel Teilbereich befinden $P _1 \ Ket {y} = \ket{y} $.
Diese beiden Reflektionen werden dann kombiniert, um einen Operator zu bilden, der einen einzelnen Schritt der Amplitude-Verstärkung $Q =-P_0 P_1 $, wobei das Gesamt Minuszeichen nur in kontrollierten Anwendungen berücksichtigt werden muss.
Die Amplitude-Verstärkung wird dann durchgeführt, indem ein Anfangszustand ($ \ket{\psi} $), der sich im ursprünglichen Teilbereich befindet, übernommen und dann "$ \ket{\psi} \mapsto Q ^ m \ket{\psi} $" durchgeführt wird.
Wenn eine solche Iteration durchgeführt wird, wird sichergestellt, dass bei einem Anfangszustand, der den Wert $ \sin ^ 2 (\urta) $ mit dem markierten Bereich aufweist, nach $m $-Iterationen $ \sin ^ 2 ([2M + 1] \urta) $ geändert wird.
Daher möchten wir in der Regel $m $ auswählen, um einen kostenlosen Parameter zu sein, z. b. $ [2M + 1] \Der Ta = \ Pi/2 $; Diese starren Optionen sind jedoch für einige Formen der Amplitude-Verstärkung nicht so wichtig, wie z. b. die Verstärkung der festen Punkt Amplitude.
Mit diesem Prozess können wir einen Status im markierten Teilbereich vorbereiten, indem Sie quadratisch weniger Abfragen an die Markierungs Funktion und die Zustands Vorbereitungs Funktion als auf einem streng klassischen Gerät durchführt.
Aus diesem Grund ist die Amplitude-Verstärkung ein bedeutender Baustein für viele Anwendungen von Quantum Computing.

Um zu verstehen, wie der Algorithmus verwendet wird, ist es hilfreich, ein Beispiel bereitzustellen, das eine Konstruktion der Oracles ermöglicht.  Sie sollten in dieser Einstellung einen Grover-Algorithmus für Daten Bank Suchvorgänge ausführen.
In der Grover-Suche besteht das Ziel darin, den Status $ \ket{+} ^ {\otimes n} = H ^ {\otimes n} \ket {0} $ in einen der (potenziell) vielen markierten Zustände umzuwandeln.
Um dies zu vereinfachen, sehen wir uns nur den Fall an, in dem der einzige markierte Status $ \ket {0} $ lautet.
Anschließend werden zwei Oracles entworfen: eine, die nur den Anfangszustand $ \ket{+} ^ {\otimes n} $ mit einem Minuszeichen und einen anderen kennzeichnet, der den markierten Zustand $ \ket {0} $ mit einem Minuszeichen markiert.
Das letztere Gate kann mithilfe des folgenden Verarbeitungsvorgangs implementiert werden, indem die Ablauf Steuerungs Vorgänge in der Canon verwendet werden:

```qsharp
operation ReflectAboutAllZeros(register : Qubit[]) : Unit 
is Adj + Ctl {

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);

    // Apply an $n-1$ controlled $Z$-gate to the $n^{\text{th}}$ qubit.
    // This gate will lead to a sign flip if and only if every qubit is
    // $1$, which happens only if each of the qubits were $0$ before step 1.
    Controlled Z(Most(register), Tail(register));

    // Apply $X$ gates to every qubit.
    ApplyToEach(X, register);
}
```

Bei diesem Oracle handelt es sich dann um einen Sonderfall des- <xref:Microsoft.Quantum.Canon.RAll1> Vorgangs, der das Drehen durch eine beliebige Phase anstelle des Reflektionsobjekte $ \phi = \pi $ ermöglicht.
In diesem Fall ähnelt dem aufzurufenden `RAll1` <xref:Microsoft.Quantum.Intrinsic.R1> Vorgang, da er ungefähr $ \ket{11\cdots1} $ anstelle des Single-Qubit-Zustands $ \ket $ rotiert {1} .

Das Oracle, das den ursprünglichen Teilbereich markiert, kann auf ähnliche Weise erstellt werden.
In Pseudocode:

1. Wenden Sie $H $ Gates auf alle Qubits an.
2. Wenden Sie $X $ Gates auf alle Qubits an.
3. Wenden Sie eine $n-$1-gesteuerte $Z $-Gate auf die $n ^ {\text{Th}} $ Qubit an.
4. Wenden Sie $X $ Gates auf alle Qubits an.
5. Wenden Sie $H $ Gates auf alle Qubits an.

Dieses Mal veranschaulichen wir auch die Verwendung <xref:Microsoft.Quantum.Canon.ApplyWith> von mit dem <xref:Microsoft.Quantum.Canon.RAll1> oben beschriebenen Vorgang:

```qsharp
operation ReflectAboutInitial(register : Qubit[]) : Unit
is Adj + Ctl {
    ApplyWithCA(ApplyToEach(H, _), ApplyWith(ApplyToEach(X, _), RAll1(_, PI()), _), register);
}
```

Anschließend können Sie diese beiden Oracles miteinander kombinieren, um zwischen den beiden Zuständen zu wechseln und "$ \ket{+} ^ {\otimes n} $" auf "$ \ket {0} $" mit einer Anzahl von Ebenen von Hadamard Gates zu transformieren, die proportional zu "$ \sqrt{2 ^ n" sind.} $ (IE $m \propto \sqrt{2 ^ n} $) im Vergleich zu den n $2 ^ n $-Ebenen, die für eine nicht deterministische Vorbereitung des $ \ket {0} $-Zustands benötigt werden, indem Sie den anfänglichen Status vorbereiten und Messen, bis das Ergebnis $0 $ beobachtet wird.

### <a name="phase-estimation-oracles"></a>Phasen Schätz-Oracles ###

Bei der Phasen Schätzung sind die Oracles etwas natürlicher.
Das Ziel der Phasen Schätzung ist das Entwerfen einer Unterroutine, die eine Stichprobe aus den eigen Werten einer einheitlichen Matrix erstellen kann.
Diese Methode ist in der Quantum-Simulation unverzichtbar, da diese Eigenwerte für viele physische Probleme in der Chemie und in der Materialwissenschaft die Boden Zustands Energien von Quantum-Systemen liefern, die uns wertvolle Informationen zu den Phasen Diagrammen der Materialien und der Reaktions Dynamik für Moleküle liefern.
Jede Konfiguration der Phasen Schätzung benötigt eine einheitliche Eingabe.
Diese einheitliche wird in der Regel durch einen von zwei Typen von Oracles beschrieben.

> [!TIP]
> Beide unten beschriebenen Oracle-Typen werden in den Beispielen behandelt.
> Weitere Informationen zu kontinuierlichen Abfrage-Oracles finden Sie im Beispiel [ **phaseschätz.**](https://github.com/microsoft/Quantum/tree/main/samples/characterization/phase-estimation)
> Weitere Informationen zu diskreten Abfrage-Oracles finden Sie im Beispiel [ **isingphaseschätz.**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/phase-estimation)

Der erste Oracle-Typ, der als diskretes Abfrage-Oracle bezeichnet wird und mit dem benutzerdefinierten Typ dargestellt <xref:Microsoft.Quantum.Oracles.DiscreteOracle> wird, umfasst einfach eine einheitliche Matrix.
Wenn $U $ die einheitliche ist, deren Eigenwerte wir schätzen möchten, ist das Oracle für $U $ einfach ein eigenständiger Wert für eine Unterroutine, die $U $ implementiert.
Beispielsweise kann $U $ der oben definierte Oracle $Q $ für die Amplitude-Schätzung sein.
Die Eigenwerte dieser Matrix können verwendet werden, um die Überlappung zwischen dem Anfangs-und dem Ziel Status, $ \sin ^ 2 (\teta) $, zu schätzen, wobei quadratisch weniger Stichproben verwendet werden, die andernfalls benötigt werden.
Dadurch wird die Anwendung der Phasen Schätzung mithilfe der Grover-Oracle-$Q $ als Eingabe für den Moniker der Amplitude-Schätzung verdient.
Eine andere gängige Anwendung, die häufig in der Quantum-metroologie verwendet wird, umfasst die Schätzung eines kleinen Drehwinkels.
Mit anderen Worten, wir möchten $ \Der TA $ für ein unbekanntes Drehungs Gate der Form $R _Z (\Der TA) $ schätzen.
In solchen Fällen die Unterroutine, mit der wir interagieren, um diesen festgelegten Wert von $ \teta $ für das Gate zu erlernen, ist $ $ \begin{align} U & = R_z (\teta) \\ \\ & = \begin{bmatrix} e ^ {-i \teta/2} & 0 \\ \\ 0 & e ^ {i \ der TA/2} \end{bmatrix}.
\end{align} $ $

Der zweite in der Phasen Schätzung verwendete Oracle-Typ ist das durch den-Typ dargestellte kontinuierliche Abfrage-Oracle <xref:Microsoft.Quantum.Oracles.ContinuousOracle> .
Ein kontinuierliches Oracle-Abfrage für die Phasen Schätzung hat die Form $U (t) $, wobei $t $ eine klassisch bekannte reelle Zahl ist.
Wenn $U $ eine einheitliche einheitliche ist, übernimmt das Oracle für die kontinuierliche Abfrage das Formular $U (t) = U ^ t $.
Dies ermöglicht es uns, Matrizen, wie z. b. $ \sqrt{u} $, abzufragen, die nicht direkt im diskreten Abfrage Modell implementiert werden konnten.

Diese Art von Oracle ist wertvoll, wenn Sie nicht eine bestimmte einheitliche, sondern die Eigenschaften des Generators der einheitlich erlernen möchten.
Beispielsweise ist in Dynamical Quantum Simulation das Ziel, Quantum-Verbindungen zu entwickeln, die $U (t) = e ^ {-i H t} $ für eine hermitische Matrix $H $ und Evolution time $t $ ähneln.
Die Eigenwerte $U (t) $ sind direkt mit den eigen Werten von $H $ verknüpft.
Um dies zu sehen, betrachten Sie einen eigen Vektor $H $: $H \ket{e} = e\ket {e} $, dann ist es leicht, von der Energie Reihen Definition der Matrix exponentialweise zu sehen, dass $U (t) \ket{e} = e ^ {i\phi} \ Ket {E} = e ^ {-IET} \ket{e} $.
Wenn Sie die eigen Phase von $U (t) $ schätzen, erhält der Eigen Wert $E $, vorausgesetzt, dass der Eigen Vektor $ \ket{e} $ in den Phasen Schätz Algorithmus eingegeben wird.
In diesem Fall kann der Wert $t $ jedoch im Ermessen des Benutzers ausgewählt werden, da für einen ausreichend kleinen Wert $t $ der Eigen Wert $E $ eindeutig durch $E =-\ Phi/t $ uminvertiert werden kann.
Da die Methoden der Quantum-Simulation die Möglichkeit bieten, eine nach Komma Breite auszuführen, werden Phasen Schätz Algorithmen bei der Abfrage der einheitlich als zusätzliche Freiheit gewährt, insbesondere, während das diskrete Abfrage Modell nur unimining der Form zulässt, $U ^ j $ für ganze Zahlen verwendet werden kann $j $ das Oracle-Replikations Modell ermöglicht es uns, die einzelnen unierungen der Form $U ^ t $ $t für
Dies ist wichtig, um die letzte Unze Effizienz von Phasen Schätz Algorithmen zu unterdrücken, da es uns ermöglicht, genau das Experiment auszuwählen, das die meisten Informationen über $E $; Methoden, die auf diskreten Abfragen basieren, müssen jedoch durch die Auswahl der optimalen Anzahl von Abfragen im Algorithmus kompromittiert werden.

Als konkretes Beispiel hierfür sollten Sie das Problem beachten, dass nicht der Drehungs Winkel eines Gates, sondern die Häufigkeit eines rotierenden Quantums geschätzt wird.
Der einheitliche, der diese Quantum Dynamics beschreibt, ist $U (t) = R_z (2 \ Omega t) $ für die Entwicklungszeit $t $ und die unbekannte Häufigkeit $ \omega $.
In diesem Kontext können wir $U (t) $ für beliebige $t $ mithilfe eines einzelnen $R _Z $ Gate simulieren. Daher müssen Sie sich nicht auf einzelne Abfragen auf die einheitliche beschränken.
Ein solches kontinuierliches Modell verfügt auch über die-Eigenschaft, dass Häufigkeits Werte, die größer als $2 \ PI $ sind, von Phasen Schätz Prozessen, die kontinuierliche Abfragen verwenden, erlernt werden können, da Phaseninformationen, die andernfalls durch die Verzweigungen der Logarithmus-Funktion maskiert werden, aus den Ergebnissen von Experimenten angezeigt werden können, die für nicht angemessene Werte $t $ ausgeführt werden.
Aus diesem Grund sind Probleme, wie z. b. diese kontinuierlichen Abfrage Modelle für die Phasen Schätzung, nicht nur angemessen, sondern auch dem diskreten Abfrage Modell vorzuziehen.
Aus diesem Grund Q# verfügt über Funktionen für beide Formen von Abfragen, die es dem Benutzer überlassen, einen Phasen Schätz Algorithmus zu entscheiden, der Ihren Anforderungen entspricht, sowie den verfügbaren Oracle-Typ.

## <a name="dynamical-generator-modeling"></a>Dynamical Generator-Modellierung ##

Generatoren von Time-Evolution beschreiben, wie sich die Zustände im Laufe der Zeit weiterentwickeln. Beispielsweise wird die Dynamics eines Quantum-Zustands $ \ket{\psi} $ von der Schrödinger-Gleichung $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = H \ket{\psi (t)} gesteuert. \end{align} $ $ mit einer hermitian-Matrix $H $ (als "hamiltonan" bezeichnet) als Bewegungs Generator. Bei einem ersten Status von $ \ket{\psi (0)} $ at time $t = $0 ist die formale Lösung dieser Gleichung zum Zeitpunkt $t $ möglicherweise, schreiben Sie im Prinzip $ $ \begin{align} \ket{\psi (t)} = U (t) \ket{\psi (0)}, \end{align} $ $, wobei die Matrix exponentielle $U (t) = e ^ {-i H t} $ als einheitlicher Time-Evolution-Operator bezeichnet wird. Obwohl wir uns auf die Generatoren dieses Formulars konzentrieren, betonen wir, dass das Konzept allgemeiner angewendet wird, z. b. für die Simulation offener Quantum-Systeme oder für abstraktere differenzielle Gleichungen.

Ein primäres Ziel der dynamischen Simulation ist die Implementierung des Time-Evolution-Operators in einem Quantum-Zustand, der in Qubits eines Quantum-Computers codiert ist.  In vielen Fällen kann der hamiltonan in eine Summe aus einigen $d $ einfacheren Begriffen aufgeteilt werden.

$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} H_j, \end{align} $ $

Wenn die Zeit Weiterentwicklung pro Begriff allein auf einem Quantum-Computer leicht zu implementieren ist. Wenn $H _J $ beispielsweise ein $X _1X_2 $-Operator ist, der für das 1. und 2. Element des Qubit-Registers fungiert `qubits` , kann die Zeit Weiterentwicklung durch die IT für jede Zeit $t $ implementiert werden, indem der Vorgang mit der Signatur aufgerufen wird `Exp([PauliX,PauliX], t, qubits[1..2])` `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` . Wie weiter unten in der hamiltona-Simulation erläutert, besteht eine Lösung darin, die Zeit Weiterentwicklung durch $H $ mit einer Sequenz einfacher Vorgänge zu überarbeiten.

$ $ \begin{align} U (t) & = \left (e ^ {-IH \_ 0 t/r} e ^ {-IH \_ 1 t/r} \cdots e ^ {-IH \_ {d-1} t/r} \right) ^ {r} + \mathcal{o} (d ^ 2 \ max_j \\ | H \_ j \\ | ^ 2 t ^ 2/r), \end{align} $ $

Dabei steuert die ganzzahlige $r > $0 den Näherungs Fehler.

Die Dynamical Generator Modeling Library bietet ein Framework für die systematische Codierung komplexer Generatoren in Bezug auf einfachere Generatoren. Eine solche Beschreibung kann dann an die Simulations Bibliothek weitergeleitet werden, um die Zeitentwicklung durch einen Simulations Algorithmus Ihrer Wahl zu implementieren, wobei viele Details automatisch berücksichtigt werden.

> [!TIP]
> Die nachstehend beschriebene Dynamical Generator Library wird in den Beispielen behandelt. Ein Beispiel, das auf dem Modell zum Modellieren von Modellen basiert, finden Sie im Beispiel [ **isinggenerators**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/ising/generators).
> Ein Beispiel, das auf Molekular Wasserstoff basiert, finden Sie in den Beispielen [**H2SimulationCmdLine**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/command-line) und [**H2SimulationGUI**](https://github.com/microsoft/Quantum/tree/main/samples/simulation/h2/gui) .

### <a name="complete-description-of-a-generator"></a>Umfassende Beschreibung eines Generators ###

Auf der obersten Ebene befindet sich eine komplette Beschreibung einer hamiltonan im `EvolutionGenerator` benutzerdefinierten Typ, der über zwei Komponenten verfügt:

```qsharp
newtype EvolutionGenerator = (EvolutionSet, GeneratorSystem);
```

Der `GeneratorSystem` benutzerdefinierte Typ ist eine klassische Beschreibung der hamiltonan.

```qsharp
newtype GeneratorSystem = (Int, (Int -> GeneratorIndex));
```

Das erste Element `Int` des Tupels speichert die Anzahl der Begriffe $d $ in der hamiltonan, und das zweite Element `(Int -> GeneratorIndex)` ist eine Funktion, die einen ganzzahligen Index in $ \{ 0, 1,..., d-1 \} $ einem `GeneratorIndex` benutzerdefinierten Typ zuordnet, der jeden primitiven Begriff in der hamiltonan eindeutig identifiziert. Beachten Sie, dass durch das Ausdrücken der Auflistung von Begriffen in der hamiltona als Funktion anstelle eines Arrays die dynamische `GeneratorIndex[]` Berechnung von ermöglicht `GeneratorIndex` wird. Dies ist besonders nützlich, wenn Sie hamiltonane mit einer großen Anzahl von Begriffen beschreiben.

Entscheidend ist, dass wir keine Konventionen dafür vorsehen, welche primitiven, von identifizierten Begriffe `GeneratorIndex` leicht zu simulieren sind. Primitive Begriffe können z. b. "Pauli"-Operatoren sein, wie oben erläutert, Sie können jedoch auch eine fermionische Zerstörung und Erstellungs Operatoren sein, die häufig in der Quantum-Chemie Simulation Eine `GeneratorIndex` ist selbst bedeutungslos, da Sie nicht beschreibt, wie die Zeit Weiterentwicklung durch den Begriff, auf den Sie verweist, als Quantum-Leitung implementiert werden kann.

Dies wird durch Angabe eines `EvolutionSet` benutzerdefinierten Typs, `GeneratorIndex` der von einer kanonischen Menge gezeichnet wird, zu einem einheitlichen Operator, der `EvolutionUnitary` als Quantum-Leitung ausgedrückt, aufgelöst. `EvolutionSet`Definiert die Konvention, wie eine `GeneratorIndex` strukturiert ist, und definiert auch die Menge möglicher `GeneratorIndex` .

```qsharp
newtype EvolutionSet = (GeneratorIndex -> EvolutionUnitary);
```

### <a name="pauli-operator-generators"></a>Pauli-Operator Generatoren ###

Ein konkretes und nützliches Beispiel für Generatoren ist eine Summe von Pauli-Operatoren, die jeweils über einen anderen Koeffizienten verfügen.
$ $ \begin{align} H & = \sum ^ {d-1} _ {j = 0} a_j H_j, \end{align} $ $, wobei jede $ \hat H_j $ nun von der Gruppe "Pauli" gezeichnet wird. Bei solchen Systemen geben wir den `PauliEvolutionSet()` des Typs an, der `EvolutionSet` eine Konvention definiert, wie ein Element der Gruppe "Pauli" und ein Koeffizienten durch einen identifiziert werden können `GeneratorIndex` , der über die folgende Signatur verfügt.

```qsharp
newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```

In der Codierung gibt der erste Parameter `Int[]` eine Pauli-Zeichenfolge an, wobei "$ \hat i\rightarrow $0", "$ \hat x\rightarrow $1", "$ \hat y\rightarrow $2" und "$ \hat z\rightarrow $3" angegeben wird. Mit dem zweiten Parameter wird `Double[]` der Koeffizient der Pauli-Zeichenfolge in der hamiltonan gespeichert. Beachten Sie, dass nur das erste Element dieses Arrays verwendet wird. Der dritte Parameter `Int[]` indiziert die Qubits, auf die diese Pauli-Zeichenfolge angewendet wird, und darf keine doppelten Elemente aufweisen. Daher kann der hamiltona-Begriff $0,4 \hat x_0 \hat Y_8 \hat I_2 \hat Z_1 $ als

```qsharp
let generatorIndexExample = GeneratorIndex(([1,2,0,3], [0.4]]), [0,8,2,1]);
```

`PauliEvolutionSet()`Ist eine Funktion, die jedes `GeneratorIndex` dieser Formulare einem `EvolutionUnitary` mit der folgenden Signatur zuordnet.

```qsharp
newtype EvolutionUnitary = ((Double, Qubit[]) => Unit is Adj + Ctl);
```

Der erste Parameter stellt eine Zeitdauer dar, die durch den Koeffizienten in der `GeneratorIndex` von einheitlicher Evolution multipliziert wird. Der zweite Parameter ist das Qubit-Register, für das die einheitliche fungiert. 

### <a name="time-dependent-generators"></a>Time-Dependent Generatoren ###

In vielen Fällen sind wir auch daran interessiert, zeitabhängige Generatoren zu modellieren, wie es in der Schrödinger-Gleichung $ $ \begin{align} i\frac {d \ket{\psi (t)}} {d t} & = \hat H (t) \ket{\psi (t)} vorkommen könnte. \end{align} $ $, wobei der Generator $ \hat H (t) $ nun Zeit abhängig ist. Die Erweiterung aus den zeitunabhängigen Generatoren oberhalb dieses Falls ist einfach. Anstatt ein festes zu haben `GeneratorSystem` , das den hamiltona für alle Male $t $ beschreibt, haben wir stattdessen den `GeneratorSystemTimeDependent` benutzerdefinierten Typ.

```qsharp
newtype GeneratorSystemTimeDependent = (Double -> GeneratorSystem);
```

Der erste Parameter ist ein kontinuierlicher Zeit Plan Parameter $s \in [0, 1] $, und Funktionen dieses Typs geben `GeneratorSystem` für diesen Zeitplan einen zurück. Beachten Sie, dass der Zeit Plan Parameter linear mit dem physischen Zeitparameter verknüpft werden kann, z. b. $s = t/t $, für eine Gesamtzeit der Simulation $T $. Im Allgemeinen muss dies jedoch nicht der Fall sein.

Entsprechend ist für eine komplette Beschreibung dieses Generators ein erforderlich `EvolutionSet` . daher definieren wir einen `EvolutionSchedule` benutzerdefinierten Typ.

```qsharp
newtype EvolutionSchedule = (EvolutionSet, GeneratorSystemTimeDependent);
```
