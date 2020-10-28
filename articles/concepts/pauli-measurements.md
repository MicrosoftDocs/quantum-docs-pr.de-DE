---
Title: Pauli Messungen Description: erfahren Sie, wie Sie mit Einzel-und multiqubit-Pauli-Mess Vorgängen arbeiten.
Autor: bradben UID: Microsoft. Quantum. Concepts. Pauli ms. Author: v-benbra ms. Date: 12/11/2017 ms. Topic: article NO-LOC:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="pauli-measurements"></a>Pauli-Messungen

In den vorherigen Diskussionen haben wir uns auf Berechnungsbasis Messungen konzentriert.
Tatsächlich gibt es weitere allgemeine Messungen, die bei der Quantum-Berechnung auftreten, die aus Sicht der Sicht bequem in Bezug auf Berechnungsbasis Messungen ausgedrückt werden können.
Wenn Sie mit Arbeiten Q# , sind die gängigsten Arten von Messungen wahrscheinlich *Pauli-Messungen* , die Berechnungsbasis Messungen verallgemeinern, um Messungen in anderen Basen und die Parität zwischen verschiedenen Qubits zu berücksichtigen.
In solchen Fällen ist es üblich, das Messen eines Pauli-Operators zu erörtern, im Allgemeinen ein Operator wie $ x, Y, z $ oder $ z \otimes z, x \otimes x, x \otimes Y $ usw.

> [!TIP]
> In Q# werden multiqubit-Pauli-Operatoren in der Regel durch Arrays des Typs dargestellt `Pauli[]` .
> Wenn $ \otimes Sie z. b. X Z Y darstellen möchten \otimes $ , können Sie das Array verwenden `[PauliX, PauliZ, PauliY]` .

Die Erörterung von Messungen in Form von Pauli-Operatoren ist vor allem im Unterfeld der Quantum-Fehlerkorrektur üblich.
In Q# wird eine ähnliche Konvention befolgt. wir erläutern nun diese Alternative Ansicht der Messungen.

Bevor wir uns mit den Details der Bedeutung einer Pauli-Messung beschäftigen, ist es sinnvoll, sich Gedanken darüber zu machen, was ein einzelnes Qubit innerhalb eines Quantum-Computers in den Quantum-Zustand versetzt.
Stellen Sie sich vor, dass wir einen $ n $ -Qubit-Quantum-Status haben. Anschließend wird ein Qubit sofort mit der Hälfte der $ 2 ^ n- $ Möglichkeiten gemessen, in denen sich der Zustand befinden könnte.
Mit anderen Worten: die Messung projiziert den Quantum-Zustand auf einen von zwei halben Leerzeichen.
Wir können die Art und Weise verallgemeinern, in der Messungen für diese Intuition durchdacht werden.

Um diese Teilbereiche zu beschreiben, benötigen wir eine Sprache für die Beschreibung.
Eine Möglichkeit, die beiden Teilbereiche zu beschreiben, besteht darin, Sie durch eine Matrix anzugeben, die nur zwei eindeutige Eigenwerte aufweist, die von der Konvention als $ \pm 1 angenommen werden $ .
Um ein einfaches Beispiel für das Beschreiben von Teilbereichen auf diese Weise zu beschreiben, sollten Sie $ Z $ :

$$
\begin{align}
  Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} .
\end{align}
$$

Wenn Sie die diagonalen Elemente der Pauli- $ Z- $ Matrix lesen, sehen Sie, dass $ Z $ zwei Eigenvektoren ( $ \ket { 0 } $ und $ \ket { 1) } $ mit den entsprechenden eigen Werten $ \pm 1 hat $ .
Wenn wir also das Qubit Messen und Abrufen `Zero` (entsprechend dem Status $ \ket { 0 } $ ), wissen wir, dass der Zustand unseres Qubit ein $ + 1- $ eigen Zustand des $ Z-Operators ist $ .
Entsprechend `One` wissen wir, dass der Zustand unseres Qubit ein $ -1- $ eigen Zustand von Z ist, $ Wenn wir erhalten $ . Dieser Prozess wird in der Sprache von Pauli-Messungen als "Messen von Pauli $ Z" bezeichnet $ und ist vollständig mit der Durchführung einer Berechnungsbasis Messung identisch.

Jede $ 2- \times 2- $ Matrix, die eine einheitliche Transformation von Z ist, $ $ erfüllt diese Kriterien ebenfalls.
Das heißt, wir könnten auch eine Matrix $ a = u ^ \dagger Z U verwenden $ , wobei $ u eine $ beliebige andere einheitliche Matrix ist, um eine Matrix zu erstellen, die die beiden Ergebnisse einer Messung in den $ \pm 1- $ Eigenvektoren definiert.
Die Notation von Pauli-Messungen verweist auf diese einheitliche Äquivalenz $ , indem X-, Y-und Z- $ Messungen als gleichwertige Messungen identifiziert werden, die zur Gewinnung von Informationen aus einem Qubit führen können.
Diese Messungen werden zur einfacheren Verwendung unten angegeben.


|Die Pauli  | -Maßeinheit  |
|-------------------|------------------------|
|$ $ Z |               $\boldone$             |
|$ $ X | $H               $                    |
|$ $ J | $HS ^               {\dagger}$         |

Das heißt, dass mit dieser Sprache "Measure $ Y $ " dem Anwenden $ von HS ^ \dagger $ und der anschließenden Messung der Berechnungsbasis entspricht, wobei [`S`](xref:Microsoft.Quantum.Intrinsic.S) ein System interner Quantum-Vorgang ist, der manchmal als "Phasen Gate" bezeichnet wird, und durch die einheitliche Matrix simuliert werden kann.

$$
\begin{align}
    S =\begin{bmatrix}
        1 & 0 \\\\ 0 & i \end{bmatrix} .
\end{align}
$$

Dies entspricht auch dem Anwenden von $ HS ^ \dagger $ auf den Quanten Zustands Vektor und dem anschließenden Messen von $ Z $ , sodass der folgende Vorgang folgendem entspricht `Measure([PauliY], [q])` :

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        Adjoint S(q);
        H(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

Der richtige Zustand wird dann durch umwandeln auf die Berechnungsbasis gefunden, was das Anwenden von $ SH $ auf den Quanten Zustands Vektor bedeutet. im obigen Code Ausschnitt wird die Transformation zurück zur Berechnungsbasis automatisch durch die Verwendung des- `within … apply` Blocks verarbeitet.

In wird Q# das Ergebnis---, d. h., die klassischen Informationen, die aus der Interaktion mit dem State---extrahiert werden, werden durch einen `Result` Wert $ j NULL angegeben, der \in \\ { \texttt { } angibt, \texttt { } \\ } $ ob sich das Ergebnis im $ (-1) ^ j- $ eigen Raum des Pauli-Operators gemessen hat.


## <a name="multiple-qubit-measurements"></a>Multiple-Qubit-Messungen

Die Messungen von multiqubit-Pauli-Operatoren sind ähnlich definiert, wie in:

$$
Z \otimes z 1 0 0 0 0 = \begin{bmatrix} & & -1 0 0 0 0 & \\\\ & & & \\\\ & & -1 & 0 \\\\ & & & \end{bmatrix} 0 0 0 1.
$$

Daher bilden die tensorflow-Produkte zweier Pauli- $ Z- $ Operatoren eine Matrix, die aus zwei Leerzeichen besteht, die aus $ + 1 $ und $ -1 $ eigen Werten bestehen.
Wie bei einem Single-Qubit-Fall bilden beide einen halben Leerraum, was bedeutet, dass die Hälfte des zugänglichen Vektor Raums zum $ + 1 $ -eigen Raum und die verbleibende Hälfte des $ eigen Raums-1 gehört $ .
Im Allgemeinen ist es einfach, aus der Definition des tensorflow-Produkts zu erkennen, dass ein beliebiges tensorflow-Produkt von Pauli- $ Z- $ Operatoren und die Identität auch dies unterliegt.
Ein auf ein Objekt angewendeter

$$
\begin{align}
    \otimes \boldone Z =\begin{bmatrix}
        1 &  0 &  0 &  0 \\\\
        0 &  1 &  0 &  0 \\\\
        0 &  0 & -1 &  0 \\\\
        0 &  0 &  0 & -1 \end{bmatrix} .
\end{align}
$$

Wie zuvor beschreibt jede einheitliche Transformation dieser Matrizen auch zwei halb Bereiche mit der Bezeichnung $ \pm 1 $ Eigenwerte.
Beispiel: $ x \otimes x = h \otimes h (z \otimes z) h \otimes h $  von der Identität, die $ Z = HXH ist $ .
Ähnlich wie der One-Qubit-Fall können alle zwei-Qubit-Pauli-Messungen als $ u ^ \dagger (Z \otimes \id ) u $ für $ 4 \times 4 $ einheitliche Matrizen u $ $ geschrieben werden. Die Transformationen in der folgenden Tabelle werden aufgelistet.

> [!NOTE]
>In der Tabelle unten verwenden wir $ \operatorname { Swap } $ , um die Matrix > anzugeben.$$
> \begin{align}
>     \operatorname{Austauschen } &=
>     \left( \begin { Matrix}
>         1 & 0 & 0 & 0 \\\\
>         0 & 0 & 1 & 0 \\\\
>         0 & 1 & 0 & 0 \\\\
>0 & 0 & 0 & 1 > \end { Matrix } \right ) >     \end{align}
> $$
> wird verwendet, um den systeminternen Vorgang zu simulieren [`SWAP`](xref:Microsoft.Quantum.Intrinsic) .

|Die Pauli     | -Maßeinheit  |
|----------------------|------------------------|
|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|
|$ \otimes \boldone X $ | $ \otimes \boldone H $|
|$ \otimes \boldone J $ | $ HS \dagger \otimes \boldone ^ $|
|$\boldone \otimes Z- $ | $ \operatorname { Swap } $|
|$\boldone \otimes X $ | $ (H \otimes \boldone ) \operatorname { - } Swap $|
|$\boldone \otimes j $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { - } Swap $|
|$Z \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } $|
|$X \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes \boldone ) $|
|$J \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|
|$Z \otimes X $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes H) $|
|$X \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (h \otimes h) $|
|$J \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes H) $|
|$Z \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|
|$X \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes HS ^ \dagger ) $|
|$J \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes HS ^ \dagger ) $|

Hier wird der [`CNOT`](xref:Microsoft.Quantum.Intrinsic.CNOT) Vorgang aus folgendem Grund angezeigt.
Jede Pauli-Messung, bei der die Matrix nicht enthalten $ \boldone $ ist, ist gleichbedeutend $ mit \otimes $ der oben beschriebenen Argumentation.
Die Eigenwerte von $ z \otimes z $ hängen nur von der Parität der Qubits ab, aus denen die einzelnen Berechnungsbasis Vektor bestehen, und die kontrollierten Vorgänge dienen dazu, diese Parität zu berechnen und im ersten Bit zu speichern.
Nachdem das erste Bit gemessen wurde, können wir die Identität des resultierenden halb Raums wiederherstellen, was dem Messen des Pauli-Operators entspricht.

Ein weiterer Hinweis: Obwohl es möglicherweise verlockend ist, zu übernehmen, dass die Messung von $ z \otimes z mit $ der sequenziellen Messung von $ z \otimes \mathbb { 1 } $ und dann $ \mathbb { 1 Z übereinstimmt } \otimes $ , wäre diese Annahme falsch.
Der Grund hierfür ist, $ dass \otimes die Messung von z z $ den Quantum-Zustand entweder in den $ + 1 $ $ -oder-1- $ eigen Zustand dieser Operatoren projiziert.
Messung $ \otimes \mathbb { von z 1 } $ und dann $ \mathbb { 1 } \otimes z $ projiziert den Quantum-Status Vektor zuerst auf einen halben Leerraum von $ Z \otimes \mathbb { 1 } $ und dann auf einen halben Bereich von $ \mathbb { 1 } \otimes z $ . Da es vier Berechnungsbasis Vektoren gibt, verringert die Durchführung beider Messungen den Zustand auf einen Viertel Raum und reduziert ihn somit auf einen einzelnen Berechnungsbasis Vektor.

## <a name="correlations-between-qubits"></a>Korrelationen zwischen Qubits
Eine weitere Möglichkeit zum Messen von tensorflow-Produkten von Pauli-Matrizen, wie z. b. $ x \otimes x $ oder $ z \otimes z $ , besteht darin, dass mit diesen Messungen Informationen in den Korrelationen zwischen den beiden Qubits angezeigt werden.
Durch $ Messen \otimes \id $ von X können Sie Informationen überprüfen, die lokal im ersten Qubit gespeichert sind.
Obwohl beide Arten von Messungen in Quantum Computing gleichermaßen wertvoll sind, beleuchtet das erste die Leistungsfähigkeit von Quantum Computing.
Es ist offensichtlich, dass die Informationen, die Sie erlernen möchten, bei der Quantum-Verarbeitung nicht in einem einzigen Qubit gespeichert werden, sondern nicht lokal in allen Qubits gespeichert werden $ \otimes . Daher werden diese Informationen nur durch eine gemeinsame Messung (z. b. z z. b. z z $ ) als Manifest angezeigt.

Beispielsweise möchten wir bei der Fehlerkorrektur häufig ermitteln, welche Fehler aufgetreten sind, wenn Sie nichts über den Zustand erfahren möchten, den wir zu schützen versuchen.
Das Beispiel für [bitflip-Code](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code) zeigt ein Beispiel dafür, wie Sie dies mithilfe von Messungen wie $ z \otimes z \otimes \id $ und $ \id \otimes z \otimes z $ < erreichen können. --TODO: Ändern Sie dies in einen Link zum Beispiel Browser, sobald das bitflip-Codebeispiel integriert ist. -->

Beliebige Pauli-Operatoren $ wie \otimes \otimes z. b. X Y Z \otimes \boldone $ können ebenfalls gemessen werden.
Alle derartigen tensorflow-Produkte von Pauli-Operatoren verfügen nur über zwei Eigenwerte $ \pm 1, $ und beide eigen Räume bilden halbräume des gesamten Vektor Bereichs.
Daher stimmen Sie mit den oben genannten Anforderungen überein.

In Q# geben solche Messungen j zurück, $ $ Wenn die Messung ein Ergebnis im Eigen Raum des Zeichens $ (-1) ^ j ergibt $ .
Die Verwendung von Pauli-Messungen als integrierte Funktion in Q# ist hilfreich, da die Messung solcher Operatoren lange Ketten von gesteuerten und nicht-Transformationen und Basis Transformationen erfordert, um das diagonalisieren des U-Gates zu beschreiben, $ $ das erforderlich ist, um den Vorgang als tensorflow-Produkt von $ Z $ und auszudrücken $ \id $ .
Wenn Sie festlegen können, dass Sie eine dieser vordefinierten Messungen durchführen möchten, müssen Sie sich keine Gedanken darüber machen, wie Sie Ihre Basis so transformieren, dass eine Berechnungsbasis Messung die erforderlichen Informationen bereitstellt.
Q# behandelt alle notwendigen Basis Transformationen automatisch.
Weitere Informationen finden Sie unter den [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) -und- [`MeasurePaulis`](xref:Microsoft.Quantum.Measurement.MeasurePaulis) Vorgängen.

## <a name="the-no-cloning-theorem"></a>Das No-Cloning-Theorem

Quantum-Informationen sind leistungsstark.
Dadurch können wir beeindruckende Dinge, wie z. b. die Faktor Zahlen, exponentiell beschleunigen als die besten bekannten klassischen Algorithmen, oder korrelierte Elektronen Systeme effizient simulieren, die für eine genaue Simulation exponentialkosten benötigen.
Es gibt jedoch Einschränkungen hinsichtlich der Leistungsfähigkeit von Quantum Computing.
Eine solche Einschränkung wird durch das *No-Klon-Theorem* angegeben.

Der No-Cloning Theorem hat einen passenden Namen.
Sie lässt das Klonen generischer Quantenzustände durch einen Quantum-Computer nicht zu.
Der Beweis für das Theorem ist erstaunlich einfach.
Obwohl ein vollständiger Nachweis für das No-Klon-Theorem für unsere Erörterung etwas zu technisch ist, liegt der Nachweis im Fall von zusätzlichen Qubits in unserem Bereich. (zusätzliche Qubits sind für den temporären Speicherplatz während einer Berechnung verwendeter Qubits und können problemlos verwendet und verwaltet werden ( Q# Siehe [geliehene Qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).

Bei solch einem Quantum-Computer muss der Klon Vorgang durch eine einheitliche Matrix beschrieben werden.
Die Messung wird nicht zugelassen, da der Quantum-Zustand beschädigt wird, den wir klonen wollen.
Um den Klon Vorgang zu simulieren, soll die einheitliche Matrix die Eigenschaft verwenden, die $$
  U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}
$$
für jeden Zustand $ \ket { \psi } $ .
Die Linearität-Eigenschaft der Matrix Multiplikation impliziert dann, dass für jeden zweiten Quantum $ -Zustand \ket { \phi } $

$$
\begin{align}
    U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}
    &= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}
      + \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\
    &= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}
        \right) \\\\
    &\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right )) \right .
\end{align}
$$

Dadurch wird die grundlegende Intuition hinter dem No-Cloning-Theorem bereitstellt: jedes Gerät, das einen unbekannten Quantum-Zustand kopiert, muss Fehler in mindestens einigen der von ihm kopierte Zustände auslösen.
Während die Hauptannahme, dass der Cloner den Eingabe Status linear verarbeitet, durch Hinzufügen und Messen von hilfssbits verletzt werden kann, können solche Interaktionen auch Informationen über das System durch die maßstatistik und das exakte Klonen in solchen Fällen vermeiden.
Einen ausführlicheren Nachweis des No-Cloning [Theorem finden Sie](xref:microsoft.quantum.more-information)unter.

Das No-Cloning-Theorem ist wichtig für ein qualitativ hochwertiges Verständnis von Quantum Computing, denn wenn Sie Quantum-Zustände ingünstig Klonen könnten, erhalten Sie eine nahezu magische Möglichkeit, aus den Quantum-Zuständen zu lernen.
Tatsächlich könnten Sie das Prinzip der geunten Unsicherheit von Heisenberg verletzen.
Alternativ können Sie einen optimalen Cloner verwenden, um ein einzelnes Beispiel aus einer komplexen Quantum-Distribution zu erstellen und alles zu erlernen, was Sie möglicherweise über die Verteilung von nur einem Beispiel erfahren.
Dies würden Sie tun, wenn Sie eine Münze kippen und Köpfe beobachten und dann einen Freund über das Ergebnis informieren, dass er antwortet, dass die Verteilung der Münze Bernoulli mit $ p = 0.512643 \ ldots $ ! "lauten muss.  Eine solche Anweisung wäre nicht unsinnig, weil ein Teil der Informationen (das Heads-Ergebnis) einfach nicht die vielen Informationen bereitstellen kann, die erforderlich sind, um die Verteilung ohne wesentliche vorherige Informationen zu codieren.
Ebenso wie ohne vorherige Informationen können wir einen quantumstatus nicht ganz genau so Klonen, wie wir ein Ensemble dieser Münzen nicht vorbereiten können, ohne dass Sie $ p kennen $ .

Informationen sind in Quantum Computing nicht kostenlos.
Jedes gemessene Qubit liefert ein einzelnes Bit an Informationen, und das No-Cloning-Theorem zeigt, dass es keine Hintertür gibt, die ausgenutzt werden kann, um den grundlegenden Kompromiss zwischen den Informationen, die über das System gewonnen wurden, und der darauf aufgerufenen Störung zu umgehen.
