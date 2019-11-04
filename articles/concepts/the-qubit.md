---
title: Das Qubit | Microsoft-Dokumentation
description: Das Qubit
author: QuantumWriter
uid: microsoft.quantum.concepts.qubit
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: f29319c3ec19fecc45f5a9f7c16061b9aa9f71ec
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183640"
---
# <a name="the-qubit"></a>Das Qubit

Ebenso wie Bits das grundlegende Objekt der Informationen in klassischem Computing sind, sind [*Qubits*](https://en.wikipedia.org/wiki/Qubit) (Quantum Bits) das grundlegende Objekt der Informationen in Quantum Computing.  Um diese Entsprechung zu verstehen, betrachten wir das einfachste Beispiel: ein einzelnes Qubit.

## <a name="representing-a-qubit"></a>Darstellen eines Qubit

Obwohl ein Bit oder eine binäre Ziffer entweder den Wert "$0 $" oder "$1 $" aufweisen kann, kann ein Qubit einen Wert aufweisen, der entweder eine dieser oder eine Quantum-Superposition von $0 $ und $1 $ ist.

Der Zustand eines einzelnen Qubit kann durch einen zweidimensionalen Spalten Vektor der Einheits Norm beschrieben werden, d. h. die Größe des Quadrats der zugehörigen Einträge muss auf $1 $ summiert werden. Dieser Vektor, der als Quantum State Vector bezeichnet wird, enthält alle Informationen, die erforderlich sind, um das One-Qubit-Quantum-System so zu beschreiben, wie ein einzelnes Bit alle Informationen enthält, die erforderlich sind, um den Status einer binären Variablen zu beschreiben.

Ein zweidimensionaler Spalten Vektor von reellen oder komplexen Zahlen mit Norm $1 $ stellt einen möglichen Quantum-Zustand dar, der von einem Qubit gehalten wird. Daher stellt "$ \begin{bmatrix} \alpha \\\\ \beta \ End{bmatrix} $" einen Qubit-Status dar, wenn "$ \alpha $" und "$ \beta $" komplexe Zahlen sind, die "$ | \alpha | ^ 2 + | \beta | ^ 2 = $1" erfüllen. Einige Beispiele für gültige Quantum State Vektoren, die Qubits darstellen, sind include

$ $ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix}, \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}, \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{1}{\sqrt{2}} \end{bmatrix} , \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{-1}{\sqrt{2}} \end{bmatrix}, \text{und} \begin{bmatrix} \frac{1}{\sqrt{2}} \\\\ \frac{i}{\sqrt{2}} \end{ bmatrix}. $ $

Die Quantum State Vektoren $ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} $ und $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ nehmen eine besondere Rolle. Diese beiden Vektoren bilden eine Grundlage für den Vektorraum, der den Qubit-Zustand beschreibt. Dies bedeutet, dass jeder Quanten Zustands Vektor als Summe dieser Basis Vektoren geschrieben werden kann. Insbesondere kann der Vektor $ \begin{bmatrix} x \\\\ y \end{bmatrix} $ als $x \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} + y \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $ geschrieben werden. Obwohl jede Drehung dieser Vektoren als vollständig gültige Basis für das Qubit fungieren würde, wählen wir diese Berechtigung aus, indem wir Sie als *Berechnungsgrundlage*aufrufen.

Wir verwenden diese beiden Quantum-Zustände, damit Sie den zwei Zuständen eines klassischen Bits entsprechen, nämlich $0 $ und $1 $. Die Standard Konvention besteht darin,

$ $0 \ equiv \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad 1 \equiv \begin{bmatrix} 0 \\\\ 1 \end{bmatrix}, $ $

Obwohl die entgegengesetzte Auswahl gleichermaßen gut wäre. Folglich entsprechen nur zwei der unendlichen Zahl der möglichen Single-Qubit Quantum State Vectors den Zuständen klassischer Bits. nicht alle anderen Quantum-Zustände.

## <a name="measuring-a-qubit"></a>Messen eines Qubit

Nachdem wir nun wissen, wie Sie ein Qubit darstellen, können wir eine gewisse intuitions Bedeutung für diese Zustände erzielen, indem wir das Konzept der [*Messung*](https://en.wikipedia.org/wiki/Measurement_in_quantum_mechanics)erörtern. Eine Maßeinheit entspricht dem informellen Konzept der "Betrachtung" bei einem Qubit, das den Quantenzustand sofort auf einen der beiden klassischen Zustände "$ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} $" oder "$ \begin{bmatrix} 0 \\\\ 1 \ End{ bmatrix} $. Wenn ein durch den quantenvektor $ \begin{bmatrix} \alpha \\\\ \beta \end{bmatrix} $ gegebenes Qubit gemessen wird, wird das Ergebnis $0 $ mit der Wahrscheinlichkeit $ | \alpha | ^ 2 $ und das Ergebnis $1 $ mit der Wahrscheinlichkeit $ | \beta | ^ 2 $ abgerufen. Bei Ergebnis $0 $ lautet der neue Status des Qubits "$ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} $;". bei Ergebnis $1 $ lautet der Status $ \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $. Beachten Sie, dass diese Wahrscheinlichkeiten aufgrund der normalisierungs Bedingung $ | \alpha | ^ 2 + | \beta | ^ 2 = $1 bis zu $1 $ summiert werden.

Die Eigenschaften der Messung bedeuten auch, dass das Gesamt Vorzeichen des quantenvektoren irrelevant ist. Das neinieren eines Vektors entspricht $ \alpha \rightarrow-\alpha $ und $ \beta \rightarrow-\beta $. Da die Wahrscheinlichkeit, $0 $ und $1 $ zu messen, von der Größenordnung der Bedingungen abhängt, ändert das Einfügen dieser Zeichen nicht die Wahrscheinlichkeiten. Solche Phasen werden üblicherweise [``*globalen Phasen*""](https://en.wikipedia.org/wiki/Phase_factor) genannt, und im Allgemeinen kann die Form $e ^ {i \phi} $ anstelle von "$ \pm $1" sein.

Eine letzte wichtige Eigenschaft der Messung ist, dass Sie nicht notwendigerweise alle quantenvektoren beschädigt. Wenn wir mit einem Qubit im Status $ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} $ beginnen, was dem klassischen Zustand $0 $ entspricht, ergibt das Messen dieses Zustands immer das Ergebnis $0 $ und lässt den Quantum-Status unverändert. Wenn nur klassische Bits vorhanden sind (d. h. Qubits, die entweder $ \begin{bmatrix}1 \\\\ 0 \ End{bmatrix} $ oder $ \begin{bmatrix}0 \\\\ 1 \ End{bmatrix} $), wird das System durch die Messung nicht beeinträchtigt. Dies bedeutet, dass wir klassische Daten replizieren und auf einem Quantum-Computer genauso wie auf einem klassischen Computer bearbeiten können. Die Möglichkeit, Informationen in beiden Zuständen gleichzeitig zu speichern, liegt jedoch in der herauf Setzung von Quantum Computing über das, was klassisch ist, und durch das verbessern von Quantum-Computern mit der Möglichkeit zum willkürlichen Kopieren von Quantum-Daten. Siehe auch [das No-Klon-Theorem. ](https://en.wikipedia.org/wiki/No-cloning_theorem).

## <a name="visualizing-qubits-and-transformations-using-the-bloch-sphere"></a>Visualisieren von Qubits und Transformationen mithilfe der Bloch-Kugel

Qubits können auch in "$ 3 $ D" mithilfe der [*Bloch Sphere*](https://en.wikipedia.org/wiki/Bloch_sphere) -Darstellung dargestellt werden.  Die Bloch-Kugel bietet eine Möglichkeit zum Beschreiben eines Single-Qubit-Quantum-Zustands (bei dem es sich um einen zweidimensionalen komplexen Vektor handelt) als dreidimensionaler echt Wert Vektor.  Dies ist wichtig, da es uns ermöglicht, Single-Qubit-Zustände visuell darzustellen und auf diese Weise Argumente zu entwickeln, die für das Verständnis von multiqubit-Zuständen von Bedeutung sein können  Die Bloch-Kugel kann wie folgt visualisiert werden:

<!--- ![](.\media\bloch.svg){ width=50% } --->
![Bloch-Kugel](~/media/concepts_bloch.png)

Die Pfeile in diesem Diagramm zeigen die Richtung an, in der der Quantum-Status Vektor zeigt, und jede Transformation des Pfeils kann als Drehung zu einer der Hauptachsen betrachtet werden.
Obwohl eine Quantum-Berechnung als Folge von Rotationen eine leistungsstarke Intuition darstellt, ist es schwierig, diese intuienz zu verwenden, um Algorithmen zu entwerfen und zu beschreiben. F # verringert dieses Problem, indem es eine Sprache zum beschreiben solcher Drehungen bereitstellt.

## <a name="single-qubit-operations"></a>Single-Qubit-Vorgänge

Quantum-Computer verarbeiten Daten, indem Sie einen universellen Satz von Quantum-Gates anwenden, mit dem jede Drehung des quantalen Zustands Vektors emuliert werden kann.
Dieses Konzept der Universalität ähnelt dem Konzept der Universalität für traditionelles (d.h. klassisches) Computing, bei dem ein Gate-Satz als universell betrachtet wird, wenn jede Transformation der Eingabe Bits mithilfe einer begrenzten Längen Verbindung ausgeführt werden kann.
Bei der Quantenberechnung sind die gültigen Transformationen, die wir für ein Qubit ausführen dürfen, einheitliche Transformationen und Messungen.
Der *Adjoint-Vorgang* oder das komplexe konjugierte austauschen ist für das Quantum Computing von entscheidender Bedeutung, da es für das Umkehren von Quantum-Transformationen erforderlich ist.
F # reflektiert dies durch die Bereitstellung von Methoden zum automatischen Kompilieren von Gate-Sequenzen in ihren Adjoint-Code, der es dem Programmierer erspart, Code-adjoints in vielen Fällen zu übergeben. Ein Beispiel hierfür finden Sie unten:

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Adj { // Auto-generate the adjoint of the operation
    H(qubit);
}
```

Obwohl es sich hierbei um ein sehr einfaches Beispiel handelt (da es sich um einen eigenständigen <xref:microsoft.quantum.intrinsic.h> Vorgang handelt), können Sie sehen, wie dies für kompliziertere Qubit-Vorgänge von Bedeutung wird.
Weitere Informationen finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.techniques.opsandfunctions).

Es gibt nur vier Funktionen, die einem Bit auf einem klassischen Computer ein Bit zuordnen. Im Gegensatz dazu gibt es eine unendliche Anzahl einheitlicher Transformationen auf einem einzigen Qubit auf einem Quantum-Computer. Daher kann kein endlicher Satz primitiver Quantum-Vorgänge, sogenannte [*Gates*](https://en.wikipedia.org/wiki/Quantum_logic_gate), den unendlichen Satz einheitlicher Transformationen, die in Quantum Computing zulässig sind, exakt replizieren. Dies bedeutet, dass es im Gegensatz zu klassischem Computing nicht möglich ist, dass ein Quantum-Computer jedes mögliche Quantum-Programm genau mit einer begrenzten Anzahl von Gates implementiert. Daher können Quantum-Computer nicht im gleichen Sinne von klassischen Computern universell sein. Wenn wir sagen, dass ein Satz von Gates für das Quantum Computing *universell* ist, bedeutet dies, dass etwas schwächer ist als bei klassischem Computing.
Bei der Universalität ist es erforderlich, dass ein Quantum-Computer *nur jede einheitliche* Matrix innerhalb eines begrenzten Fehlers mithilfe einer endlichen Längen Gate-Sequenz anfordert.
Anders ausgedrückt: ein Satz von Gates ist ein universelles Gate, wenn eine einheitliche Transformation ungefähr als ein Produkt von Gates aus dieser Menge geschrieben werden kann. Wir verlangen, dass für jede vorgeschriebene Fehlergrenze Gates $G _{1}, g_{2}, \ldots, G_N $ aus dem Gate-Satz vorhanden ist, sodass

$ $ G_N g_ {N-1} \cdots G_2 G_1 \ca. $ $

Beachten Sie Folgendes: da die Konvention für die Matrix Multiplikation von rechts nach links multipliziert werden muss, ist der erste Gate-Vorgang in dieser Sequenz, $G _N $, tatsächlich der letzte, der auf den Quantum-Status Vektor angewendet wird. Formal gesagt, dass ein solcher Gate-Satz universell ist, wenn für jede Fehlertoleranz $ \epsilon > 0 $ vorhanden ist $G _1, \ldots, G_N $, sodass der Abstand zwischen $G _N \ ldots G_1 $ und $U $ höchstens $ \epsilon $ liegt. Im Idealfall sollte der Wert von $N $, der diese Distanz von $ \epsilon $ erreichen muss, polylogarithmisch mit $1/\ Epsilon $ skalieren.

Wie sieht eine solche universelle Gate-Menge in der Praxis aus?  Das einfachste solche universelle Gate für Single-Qubit-Gates besteht nur aus zwei Gates: dem Hadamard-Gate $H $ und dem sogenannten $T $-Gate (auch als "$ \ PI/8 $ Gate" bezeichnet):

$ $ H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 &-1 \end{bmatrix}, \qquad t = \begin{bmatrix} 1 & 0 \\\\ 0 & e ^ {i \ pi/4} \end{bmatrix}.
$$

Aus praktischen Gründen im Zusammenhang mit der Quantum-Fehlerkorrektur kann es jedoch bequemer sein, einen größeren Gate-Satz in Erwägung zu nehmen, nämlich einen, der mit $H $ und $T $ generiert werden kann.
Wir können die Quantum-Gates in zwei Kategorien klassifizieren: Clifford Gates und die $T $-Gate.
Diese Unterteilung ist nützlich, da die so genannten Clifford-Gates in vielen Quantum-Fehlerkorrekturen leicht implementiert werden können, sodass Sie nur wenige Ressourcen in Bezug auf Vorgänge und Qubits benötigen, um fehlertoleranter zu implementieren, wohingegen nicht-Clifford Gates sehr kostspielig, wenn Fehlertoleranz erforderlich ist. Der Standardsatz von Single-Qubit Clifford Gates, der [standardmäßig in Q # enthalten](xref:microsoft.quantum.libraries.standard.prelude)ist, umfasst

$ $ H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\ 1 &-1 \end{bmatrix}, \qquad S = \begin{bmatrix} 1 & 0 \\\\ 0 & i \end{bmatrix} = t ^ 2, \qquad X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} = HT ^ 4H, $ $

$ $ Y = \begin{bmatrix} 0 &-i \\\\ i & 0 \ End{bmatrix} = t ^ 2HT ^ 4 HT ^ 6, \qquad Z = \begin{bmatrix}1 & 0\\\\ 0 &-1 \end{bmatrix} = t ^ 4.
$$

Hier werden die Vorgänge $X $, $Y $ und $Z $ besonders häufig verwendet und nach dem Ersteller Wolfgang Pauli als [*Pauli-Operatoren*](https://en.wikipedia.org/wiki/Pauli_matrices) bezeichnet.
Zusammen mit dem nicht-Clifford-Gate (der $T $-Gate) können diese Vorgänge so zusammengesetzt werden, dass jede einheitliche Transformation auf einem einzelnen Qubit ungefähre ist.

Weitere Informationen zu diesen Vorgängen, ihren Bloch Sphere-Darstellungen und f #-Implementierungen finden Sie unter systeminterne [Vorgänge und Funktionen](xref:microsoft.quantum.libraries.standard.prelude#intrinsic-operations-and-functions).

Als Beispiel für die Erstellung einheitlicher Transformationen aus diesen primitiven entsprechen die drei Transformationen, die in den Bloch-Bereichen oben dargestellt werden, der Gate-Sequenz $ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} \mapsto hzh \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} = \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} $.

Während der vorherige die beliebtesten primitiven Gates zum Beschreiben von Vorgängen auf der logischen Ebene des Stapels bilden (denken Sie an die logische Ebene als die Ebene des Quantum-Algorithmus), ist es häufig sinnvoll, weniger grundlegende Vorgänge bei algorithmische zu betrachten. Ebene, z. b. Vorgänge, die näher an einer Funktions Beschreibungs Ebene liegen. Glücklicherweise stehen in Q # auch Methoden zur Verfügung, die für die Implementierung von unidirektionalebenen verfügbar sind, die wiederum Algorithmen auf hoher Ebene implementieren können, ohne dass alle Elemente explizit in Clifford und $T $-Gates zerlegt werden.

Die einfachste solche primitive ist die einzelne Qubit-Rotation. In der Regel werden drei Single-Qubit-Drehungen berücksichtigt: $R _x $, $R _y $ und $R _Z $. Um die Aktion der Drehung $R _x (\urta) zu visualisieren, stellen Sie sich z. b. vor, dass Sie auf die Richtung der $x $-Achse der Bloch-Kugel zeigen und den Vektor mit der Hand durch einen Winkel von $ \ der TA/2 $ radiane drehen. Dieser verwirrende Faktor von $2 $ ergibt sich aus der Tatsache, dass orthogonale Vektoren $180 ^ \circ $ auseinander liegen, wenn Sie in der Bloch-Kugel gezeichnet werden, aber tatsächlich $90 ^ \circ $ Grad gleichmäßig voneinander entfernt sind. Die entsprechenden einheitlichen Matrizen lauten:

\begin{align *} & R_z (\orta) = e ^ {-i\theita z/2} = \begin{bmatrix} e ^ {-i \ der TA/2} & 0\\\\ 0 & e ^ {i \ der TA/2} \end{bmatrix}, \\\\ & R_x (\orta) = e ^ {-i\der Ta x/2} = HR_z (\orta) H = \begin{bmatrix} \cos (\ der TA/2) &-i\sin (\ der TA/2)\\\\-i\sin (\ der TA/2) & \cos (\ der TA/2) \end{bmatrix}, \\\\ & R_y (\urta) = e ^ {-i\der ta y/2} = SHR_z (\orta) HS ^ \dagger = \begin{bmatrix} \cos (\ der TA/2) &-\sin (\-Ta/2) @no__ t_9_ \\ \sin (\ der TA/2) & \cos (\ der TA/2) \end{bmatrix}. \end{align*}

Ebenso wie jede beliebige drei Drehung kombiniert werden kann, um eine willkürliche Drehung in drei Dimensionen auszuführen, kann Sie aus der Bloch Sphere-Darstellung ersichtlich werden, dass jede einheitliche Matrix auch als Sequenz von drei Umdrehungen geschrieben werden kann. Insbesondere für jede einheitliche Matrix $U $ gibt $ \alpha, \beta, \gamma, \delta $ so aus, dass $U = e ^ {i\alpha} R_x (\beta) R_z (\gamma) R_x (\delta) $ vorhanden ist. Daher $R _Z (\teta) $ und $H $ auch einen universellen Gate-Satz bilden, obwohl es sich nicht um eine diskrete Menge handelt, da $ \teta $ einen beliebigen Wert annehmen kann. Aus diesem Grund und aufgrund von Anwendungen in der Quantum-Simulation sind solche kontinuierlichen Gates für die Quantum-Berechnung wichtig, insbesondere auf der Entwurfs Ebene des Quantum-Algorithmus. Um eine fehlertolerante Hardware Implementierung zu erreichen, werden Sie letztendlich in diskrete Gate-Sequenzen kompiliert, die diesen Rotationen sehr ähnlich sind.
