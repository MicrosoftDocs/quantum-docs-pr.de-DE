---
Title: Quantum Oracles Description: Hier erfahren Sie, wie Sie mit Quantum-Oracles, Black Box-Vorgängen, die als Eingabe für einen anderen Algorithmus verwendet werden, arbeiten und definieren.
Autor: cgranade UID: Microsoft. Quantum. Concepts. Oracles ms. Author: chgranad ms. Date: 07/11/2018 ms. Topic: article NO-LOC:
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
# <a name="quantum-oracles"></a>Quantum-Oracles

Ein Oracle $ O $ ist ein "Blackbox"-Vorgang, der als Eingabe für einen anderen Algorithmus verwendet wird.
Häufig werden solche Vorgänge mithilfe der klassischen Funktion $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m definiert, $ die eine $ n $ -Bit-Binär Eingabe annimmt und eine $ m $ -Bit-Binär Ausgabe erzeugt.
Beachten Sie hierzu eine bestimmte binäre Eingabe $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1 } ) $ .
Wir können Qubit-Zustände als $ \ket { \vec { x } } = \ket { x_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 bezeichnen } } $ .

Wir könnten zuerst versuchen, $ o so zu definieren $ $ , dass o \ket { x } = \ket { f (x) } $ , aber dies hat einige Probleme.
Erstens hat $ f $ möglicherweise eine andere Größe von Eingabe und Ausgabe ( $ n \ne m $ ), sodass $ $ durch das Anwenden von O die Anzahl der Qubits im Register geändert würde.
Zweitens: auch wenn $ n = m $ , ist die Funktion möglicherweise nicht invertierbar: Wenn $ f (x) = f (y) $ für einige $ x \ne y $ , dann $ o \ket { x } = o y, \ket { } $ aber $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .
Dies bedeutet, dass wir den Adjoint-Vorgang O ^ nicht erstellen können $ \dagger $ , und für Oracles muss ein Adjoint-Element definiert sein.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>Definieren eines Oracle-Effekts durch seine Auswirkung auf den Berechnungsbasis Status
Wir können diese beiden Probleme behandeln, indem wir ein zweites Register von $ m $ Qubits zum Speichern unserer Antwort einführen.
Anschließend definieren wir die Auswirkung des Oracle auf alle Berechnungs Status Zustände: für alle $ x \in \\ { 0, 1 \\ } ^ n $ und $ y \in \\ { 0, 1 \\ } ^ m $ ,

$$
\begin{align}
    O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .
\end{align}
$$

$ = \dagger $ Wir haben nun die Erstellung durch die Erstellung der beiden früheren Probleme gelöst.

> [!TIP]
>Beachten Sie, dass o $ = { \dagger } $ $ ^ 2 = \boldone $ seit $ a \oplus b \oplus b = a $ für alle $ a, b \in \: :: NO-LOC ({)::: 0, 1 \: :: NO-LOC (})::: $ .
>Folglich ist $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ .

Wichtig: die Definition eines Oracle auf diese Weise für jeden Berechnungsbasis Status $ \ket { x } \ket { y } $ definiert auch, wie $ O $ für einen beliebigen anderen Zustand agiert.
Dies folgt unmittelbar daran, dass $ O $ , wie alle Quantum-Vorgänge, linear in dem Zustand ist, auf den es angewendet wird.
Stellen Sie sich beispielsweise den Hadamard-Vorgang vor, der durch $ h \ket { 0 } = \ket { + } $ und $ h \ket { 1 } = \ket { - } $ definiert ist.
Wenn Sie wissen möchten, wie $ h $ funktioniert $ \ket { + } $ , können wir dieses h verwenden, wenn es $ $ linear ist,

$$
\begin{align}
H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\
           &= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .
\end{align}
$$

Bei der Definition von Oracle $ O $ kann auf ähnliche Weise festgelegt werden, dass jeder Zustand $ \ket { \psi } $ auf $ n + m- $ Qubits als

$$
\begin{align}
\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}
\end{align}
$$

wobei $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ die Koeffizienten des Zustands darstellt $ \ket { \psi } $ . Demnach sind

$$
\begin{align}
O \ket { \psi } & = o \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\
             &= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .
\end{align}
$$

## <a name="phase-oracles"></a>Phasen-Oracles
Alternativ $ $ dazu können Sie f in ein Oracle O codieren, $ $ indem Sie eine _Phase_ auf der Grundlage der Eingabe für $ O anwenden $ . Beispielsweise können wir $ O so definieren $ , dass $$
\begin{align}
    O \ket { x } = (-1) ^ { f (x) } \ket { x } .
\end{align}
$$
Wenn eine Phase, die Oracle für ein Register anfänglich in einem Compute-Status x anwendet, eine Phase $ \ket { } $ ist, ist diese Phase eine globale Phase und daher nicht Observable.
Ein solches Oracle kann jedoch eine sehr leistungsfähige Ressource sein, wenn Sie auf eine übergeordnete Position oder einen kontrollierten Vorgang angewendet wird.
Stellen Sie sich z $ . b. einen Phase-Oracle-O_f $ für eine Single-Qubit-Funktion $ f vor $ .
Seitdem $$
\begin{align}
    O_f \ket{+}
        &=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\
        &=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .
\end{align}
$$

Im Allgemeinen können beide Sichten von Oracles erweitert werden, um klassische Funktionen darzustellen, die anstelle eines einzelnen Bits reelle Zahlen zurückgeben.

Das Auswählen der besten Methode zum Implementieren eines Oracle hängt stark davon ab, wie dieses Oracle innerhalb eines bestimmten Algorithmus verwendet werden soll.
Der " [Deutsch-Jozsa"-Algorithmus](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) basiert z. b. auf dem Oracle, der auf die erste Weise implementiert ist, während der [-Algorithmus von Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) auf die zweite Weise implementiert ist.


Weitere Informationen finden Sie unter [gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).
