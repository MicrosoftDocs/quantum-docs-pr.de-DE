---
Title: Erweiterte Matrix Konzepte Description: erfahren Sie mehr über Eigenvektoren, Eigenwerte und Matrix exponentiale, die grundlegenden Tools, die zum beschreiben und Simulieren von Quantum-Algorithmen verwendet werden.
Autor: quantumwriter UID: Microsoft. Quantum. Concepts. Matrix-Advanced ms. Author: v-benbra ms. Date: 12/11/2017 ms. Topic: konzeptionelle NO-LOC:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "$$$"
- "$$$"
- "$$$"
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
# <a name="advanced-matrix-concepts"></a>Erweiterte Matrix Konzepte #

Wir erweitern nun unsere Manipulation von Matrizen auf [*Eigenwerte, Eigenvektoren*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) und [*exponentiale*](https://en.wikipedia.org/wiki/Matrix_exponential) , die einen grundlegenden Satz von Tools bilden, die wir zum beschreiben und Implementieren von Quantum-Algorithmen benötigen.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenwerte und Eigenvektoren ##

Let $ M $ ist eine quadratische Matrix $ , und v $ ist ein Vektor, der nicht der Nullen aller Nullen ist (d. h. der Vektor mit allen Einträgen gleich $ 0 $ ).

Wir sagen $ , $ dass v ein [*eigen Vektor*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) von M ist,  $ $ Wenn $ mv = CV $ für eine bestimmte Zahl $ c $ . Wir sagen $ , dass c $ der [*eigen Wert*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) ist, der dem Eigen Vektor $ v entspricht $ . Im Allgemeinen kann eine Matrix $ M $ einen Vektor in einen anderen Vektor umwandeln, aber ein eigen Vektor ist ein besonderes Zeichen, da er unverändert bleibt, außer dass er mit einer Zahl multipliziert wird. Beachten Sie Folgendes: Wenn $ v $ ein eigen Vektor mit dem Eigen Wert $ c ist $ , dann $ $ ist AV auch ein eigenständiger Vektor (bei jedem Wert ungleich 0 (NULL $ $ )) mit demselben eigen Wert.

Beispielsweise ist für die Identitätsmatrix jeder Vektor $ v $ ein eigen Vektor mit dem Eigen Wert $ 1 $ .

Sehen Sie sich als weiteres Beispiel eine [*diagonale Matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ D $ an, die nur Einträge ungleich 0 (null) auf der Diagonal aufweist:

$$
\begin{bmatrix}
d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & D_3 \end{bmatrix} .
$$

Die Vektoren

$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} und \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$

sind Eigenvektoren dieser Matrix mit eigen Werten  $ d_1 $ , $ d_2 $ und $ D_3 $ . Wenn $ d_1 $ , $ d_2 $ und $ D_3 unter $ schiedliche Zahlen sind, sind diese Vektoren (und ihre vielfache) die einzigen Eigenvektoren der Matrix $ d $ . Im Allgemeinen ist es für eine diagonal Matrix leicht, die Eigenwerte und Eigenvektoren zu lesen. Die Eigenwerte sind alle Zahlen, die auf der Diagonal angezeigt werden, und ihre jeweiligen Eigenvektoren sind die Einheits Vektoren, bei denen ein Eintrag gleich $ 1 $ und die restlichen Einträge gleich $ 0 sind $ .

Beachten Sie im obigen Beispiel, dass die Eigenvektoren von $ D $ eine Grundlage für $ drei $ dimensionale Vektoren bilden. Eine Basis ist ein Satz von Vektoren, sodass jeder Vektor als lineare Kombination von Ihnen geschrieben werden kann. Explizitere, $ V_1 $ , $ V_2 $ und $ V_3 $ bilden eine Grundlage, wenn ein Vektor $ v $ als $ v = A_1 V_1 + a_2 V_2 + a_3 V_3 geschrieben werden kann A_1 $ $ $ , $ a_2 $ und $ a_3 $ .

Denken Sie daran, dass es sich bei einer hermischen Matrix (auch als "selbst Adjoint" bezeichnet) um eine komplexe quadratische Matrix handelt, die der eigenen komplexen konjugierung entspricht, während eine einheitliche Matrix eine komplexe Quadrat Matrix ist, deren Umkehrung gleich der zugehörigen Adjoint-oder komplexen konjugierte ist.
Für hermitian-und einheitliche Matrizen, die im Grunde die einzigen Matrizen bei der Quantenberechnung sind, gibt es ein allgemeines Ergebnis, das als "Spectral"- [*Theorem*](https://en.wikipedia.org/wiki/Spectral_theorem)bezeichnet wird, das Folgendes bestätigt: für jede hermitische oder einheitliche Matrix $ m gibt $ es eine einheitliche $ U, bei der $ $ m = u ^ \dagger d U $ für eine diagonale Matrix $ D ist $ . Außerdem sind die diagonalen Einträge von $ D $ die Eigenwerte von $ M $ .

Wir wissen bereits, wie Sie die Eigenwerte und Eigenvektoren einer Diagonalen Matrix D berechnen können $ $ . Bei Verwendung dieses Theorem wissen wir, dass bei $ v $ ein eigen Vektor von $ D $ mit dem Eigen Wert $ c $ , d. h. $ DV = CV $ , $ U ^ \dagger v $ ein eigen Vektor von $ M $ mit dem Eigen Wert $ c ist $ . Dies liegt daran, dass

$$M (u ^ \dagger v) = u ^ \dagger d U (u ^ \dagger v) = u ^ \dagger d (u u ^ \dagger ) v = U ^ \dagger d v = c U ^ \dagger v.$$

## <a name="matrix-exponentials"></a>Matrix exponentiale
Eine [*Matrix Exponentialwert*](https://en.wikipedia.org/wiki/Matrix_exponential) kann auch exakt mit der Exponentialfunktion definiert werden.  Die Matrix Exponentialwert einer Matrix $ a $ kann als

$$
e ^ A = \boldone + a + \frac { a ^ 2 } { 2! } + \frac { A ^ 3 } { 3!}+\cdots
$$

Dies ist wichtig, da die Evolution für die Quantum-mechanische Zeit durch eine einheitliche Matrix der Form $ e ^ { IB } $ für hermitian Matrix $ B $ beschrieben wird.  Aus diesem Grund ist das Durchführen von Matrix Exponentialzahlen ein wesentlicher Bestandteil von Quantum Computing und bietet systeminterne Q# Routinen zum Beschreiben dieser Vorgänge.
In der Praxis gibt es viele Möglichkeiten, eine Matrix auf einem klassischen Computer exponentiell zu berechnen, und in der Regel wird eine solche exponentialweise mit der Peril in Bezug gesetzt.  Weitere Informationen finden Sie unter [*Cleve Moler und Charles Van Loan. "Neun zweifelhafte Möglichkeiten, den Exponentialwert einer Matrix zu berechnen." Siam Review 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) , um weitere Informationen zu den beteiligten Problemen zu finden.

Die einfachste Möglichkeit, um zu verstehen, wie die exponentielle einer Matrix berechnet werden kann, ist die Eigenwerte und Eigenvektoren dieser Matrix.  Insbesondere das oben beschriebene Spektral Theorem besagt, dass für jede hermitische oder einheitliche Matrix $ a $ eine einheitliche Matrix $ U $ und eine diagonale Matrix D vorhanden ist, die u $ $ $ = ^ \dagger d u ist $ .  Aufgrund der Eigenschaften von Unitarity haben wir $ eine ^ 2 = u ^ \dagger d ^ 2 u $ und ebenso für alle Power $ p $ $ A ^ p = u ^ \dagger d ^ p u $ .  Wenn wir dies in die Operator Definition des Operator exponentiell ersetzen, erhalten wir Folgendes:

$$
e ^ A = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \exp (D_ { 11 } ) & 0 & \cdots & 0 \\\\ 0 & \exp (D_ { 22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0 & 0 & \cdots & \exp (D_ { NN } ) \end{bmatrix} U.$$

Anders ausgedrückt: Wenn Sie in die eigenständige Matrix der Matrix umwandeln, $ $ entspricht das Berechnen der Matrix exponentiell dem Berechnen des normalen exponentiellen Werts der Eigenwerte der Matrix.  Wie viele Vorgänge in Quantum Computing das Durchführen von Matrix Exponentialzahlen umfassen, wird dieser Trick der Transformation in die eigenständige Basis einer Matrix, um die Ausführung des Operator exponentialmäßig zu vereinfachen, häufig angezeigt und ist die Grundlage für viele Quantum-Algorithmen, wie z. b. Trotter – Quantum-Simulationsmethoden, die später in diesem Handbuch

Eine weitere nützliche Eigenschaft ist $ , wenn b $ sowohl einheitlich als auch hermitian ist, d. h. $ b = b ^ { -1 } = b ^, \dagger $ dann $ b ^ 2 = \boldone $ . Durch Anwenden dieser Regel auf die oben genannte Erweiterung der Matrix und durch Gruppierung der $ \boldone $ und der $ B- $ Begriffe können Sie sehen, dass für jeden echten Wert $ x $ die Identität vorhanden ist.

$$e ^ { IBX } = \boldone \cos (x) + ib\sin (x)$$


bestand. Dieser Trick ist besonders nützlich, weil er die in den Aktions Matrix exponentialweise vorhandenen Aktionen zulässt, auch wenn die Dimension von $ B $ exponentiell groß ist, für den Sonderfall, wenn $ b $ sowohl einheitlich als auch hermitian ist.
