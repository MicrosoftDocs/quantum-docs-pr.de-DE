---
Title: Vektoren und Matrizen in Quantum Computing Description: Erlernen Sie die Grundlagen der Arbeit mit Vektoren und Matrizen.
Autor: quantumwriter UID: Microsoft. Quantum. Concepts. Vectors ms. Author: nawiebe@microsoft.com ms. Date: 12/11/2017 ms. Topic: article NO-LOC:
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

# <a name="vectors-and-matrices"></a>Vektoren und Matrizen

Eine Vertrautheit mit Vektoren und Matrizen ist für das Verständnis von Quantum Computing von entscheidender Bedeutung. Im folgenden finden Sie eine kurze Einführung, und interessierte Leser werden empfohlen, einen Standard Verweis auf lineare Algebra zu lesen, z. b. für die Tabelle *, G. (1993). Einführung in lineare Algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* oder eine Online Referenz, wie z. b. [lineare Algebra](http://joshua.smcvt.edu/linearalgebra/).

Ein Spalten Vektor (oder einfach [*Vektor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ $ der Dimension (oder Größe) $ n $ ist eine Auflistung von $ n $ komplexen Zahlen $ (V_1 V_2, \ldots, v_n), die $ als Spalte angeordnet sind:

$$v =\begin{bmatrix}
v_1\\\\
v_2\\\\
\vdots\\\\
v_n\end{bmatrix}$$

Die Norm eines Vector $ v $ ist als $ \sqrt { \sum \_ i | v \_ i | ^ 2 definiert } $ . Ein Vektor wird als Einheits Norm bezeichnet (oder auch als [*Einheits Vektor*](https://en.wikipedia.org/wiki/Unit_vector)bezeichnet), wenn seine Norm den Wert 1 hat $ $ . Das [*Adjoint eines Vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ wird als $ v ^ bezeichnet und als \dagger $ folgender Zeilen Vektor definiert $ \* $ , wobei die komplexe konjugierung bezeichnet.

$$\begin{bmatrix}V_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} V_1 ^ * & \cdots & v_n ^ *\end{bmatrix}$$

Die gängigste Methode, zwei Vektoren zu multiplizieren, ist das [*innere Produkt*](https://en.wikipedia.org/wiki/Inner_product_space), das auch als "Punktprodukt" bezeichnet wird.  Das innere Produkt liefert die Projektion eines Vektors auf einen anderen und ist äußerst nützlich, um zu beschreiben, wie ein Vektor als Summe aus anderen einfacheren Vektoren ausgedrückt wird.  Das innere Produkt zwischen $ u $ und $ v $ , bezeichnet $ \left \langle u, v \right \rangle $ ist definiert als

$$
\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } V_1 + \cdots + u \_ n ^ { \* } v \_ n.
$$

Diese Notation ermöglicht außerdem das Schreiben der Norm eines Vector $ v $ als $ \sqrt { \langle v, v \rangle } $ .

Wir können einen Vektor mit einer Zahl c multiplizieren $ $ , um einen neuen Vektor zu bilden, dessen Einträge mit c multipliziert werden $ $ . Wir können auch zwei Vektoren $ u $ und v hinzufügen $ $ , um einen neuen Vektor zu bilden, dessen Einträge die Summe der Einträge von $ u $ und v sind $ $ . Diese Vorgänge werden im folgenden dargestellt:

$$\mathrm{Wenn } ~ u=\begin{bmatrix}
u_1\\\\
u_2\\\\
\vdots\\\\
u_n \end{bmatrix} ~ \mathrm { und}~
Ramelow=\begin{bmatrix}
    v_1\\\\
    v_2\\\\
    \vdots\\\\
    v_n \end{bmatrix} , ~ \mathrm {}~
Au + BV=\begin{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\vdots\\\\
au_n + bv_n \end{bmatrix} .
$$

Eine [*Matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) der Größe $ m \times n $ ist eine Auflistung von $ $ in Mio. Zeilen komplexen Zahlen, die in $ m $ Zeilen und n Spalten angeordnet sind, $ $ wie unten dargestellt:

$$800= 
\begin{bmatrix}
M_ { 11 } ~~ m_ { 12 } ~~ \cdots ~~ m_ { 1N}\\\\
M_ { 21 } ~~ m_ { 22 } ~~ \cdots ~~ m_ { 2N}\\\\
\ddots\\\\
M_ { M1 } ~~ m_ { m2 } ~~ \cdots ~~ m_ { MN}\\\\
\end{bmatrix}.$$

Beachten Sie, dass es sich bei einem Vektor der Dimension $ n $ einfach um eine Matrix der Größe $ n \times 1 handelt $ . Wie bei Vektoren können wir eine Matrix mit einer Zahl c multiplizieren, $ $ um eine neue Matrix zu erhalten, in der jeder Eintrag mit c multipliziert wird $ $ . Wir können zwei Matrizen derselben Größe hinzufügen, um eine neue Matrix zu generieren, deren Einträge die Summe der entsprechenden Einträge der beiden Matrizen sind. 

## <a name="matrix-multiplication-and-tensor-products"></a>Matrix Multiplikation und Tensor-Produkte

Wir können auch zwei Matrizen $ m $ der Dimension $ m \times n $ und $ n $ der Dimension n p multiplizieren $ \times $ , um eine neue Matrix $ p $ der Dimension $ m \times p $ wie folgt zu erhalten:

\begin{align}
&\begin{bmatrix}
    M_ { 11 } ~~ m_ { 12 } ~~ \cdots ~~ m_ { 1N}\\\\
    M_ { 21 } ~~ m_ { 22 } ~~ \cdots ~~ m_ { 2N}\\\\
    \ddots\\\\
    M_ { M1 } ~~ m_ { m2 } ~~ \cdots ~~ m_ { MN}
\end{bmatrix}
\begin{bmatrix}
N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1P}\\\\
N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2P}\\\\
\ddots\\\\
N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}
\end{bmatrix}=\begin{bmatrix}
P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1P}\\\\
P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2P}\\\\
\ddots\\\\
P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}
\end{bmatrix}
\end{align}

Dabei sind die Einträge $ von $ P $ P_ { IK } = \sum _j M_ { IJ } N_ { JK } $ . Der Eintrag $ P_ { 11 ist beispielsweise } $ das innere Produkt der ersten Zeile von $ M $ mit der ersten Spalte von $ N $ . Beachten Sie, dass sich diese Definition auf die Matrix Vektor Multiplikation erstreckt, da ein Vektor einfach ein Sonderfall einer Matrix ist. 

Alle Matrizen, die wir in Erwägung haben, sind entweder quadratische Matrizen, bei denen die Anzahl der Zeilen und Spalten gleich ist, oder Vektoren, die nur $ einer $ Spalte entsprechen. Eine spezielle quadratische Matrix ist die [*Identitätsmatrix*](https://en.wikipedia.org/wiki/Identity_matrix), die als bezeichnet wird $ \boldone $ und deren diagonale Elemente gleich $ 1 $ und die übrigen Elemente gleich $ 0 sind $ :

$$\boldone=\begin{bmatrix}
1 ~~ 0 ~~ \cdots ~~ 0\\\\
0 ~~ 1 ~~ \cdots ~~ 0\\\\
~~ \ddots\\\\
0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$

Für eine quadratische Matrix $ a $ sagen wir, dass $ die Matrix B $ bei [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) $ ab BA umgekehrt = ist = \boldone $ . Die Umkehrung einer Matrix muss nicht vorhanden sein. Wenn Sie jedoch vorhanden ist, ist sie eindeutig, und wir bezeichnen Sie $ als ^ { -1 } $ . 

Bei allen Matrizen $ m $ ist die Adjoint-oder konjugierte-/konjugierte-Datei $ $ eine Matrix $ N, $ sodass $ N_ { IJ } = m_ { JI ist } ^ \* $ . Das Adjoint von $ M $ wird normalerweise als $ M ^ bezeichnet \dagger $ . Wir sagen, eine $ Matrix $ u [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) ist einheitlich $ , wenn UU ^ \dagger = u ^ \dagger u = \boldone $ oder gleichwertig, $ u ^ { -1 } = u ^ \dagger $ .  Die wichtigste Eigenschaft der einheitlichen Matrizen ist, dass Sie die Norm eines Vektors erhalten.  Dies liegt daran, dass 

$$\langlev, v \rangle = v ^ \dagger v = v ^ \dagger u ^ { -1 } U v = v ^ \dagger u ^ \dagger u v = \langle u v, u v \rangle .$$  

Eine Matrix $ m $ wird als [*hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) bezeichnet, wenn $ m = m ^ \dagger $ .

Schließlich ist das [*tensorflow-Produkt*](https://en.wikipedia.org/wiki/Tensor_product) (oder Kronecker-Produkt) von zwei Matrizen $ m $ der Größe $ m \times n $ und $ n $ der Größe $ p \times q $ eine größere Matrix $ p = M \otimes n $ der Größe $ MP \times NQ " $ und wird $ $ $ $ wie folgt von M und n abgerufen:

\begin{align}
    M \otimes N&=
    \begin{bmatrix}
        M_ { 11 } ~~ \cdots ~~ m_ { 1N }\\\\
        \ddots\\\\
        M_ { M1 } ~~ \cdots ~~ m_ { MN  }
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        N_ { 11 } ~~ \cdots ~~ N_ { 1Q  }\\\\
        \ddots\\\\
        N_ { P1 } ~~ \cdots ~~ N_ { PQ}
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}\\\\
        \ddots\\\\
        M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { MN } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}
    \end{bmatrix}.
\end{align}

Dies wird in einigen Beispielen besser veranschaulicht:

$$
    \begin{bmatrix}
        a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=
    \begin{bmatrix}
        ein \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
        \\\\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
    \end{bmatrix}
    =\begin{bmatrix}a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}
$$

and

$$
    \begin{bmatrix}
        a \ b \\\\ c \ d\end{bmatrix}
    \otimes 
    \begin{bmatrix}
        e \ f \\\\ \ h\end{bmatrix}
     =
    \begin{bmatrix}
    ein\begin{bmatrix}
    e \ f \\\\ \ h\end{bmatrix}
    b\begin{bmatrix}
    e \ f \\\\ \ h\end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ \ h\end{bmatrix}
    d\begin{bmatrix}
    e \ f \\\\ \ h\end{bmatrix}
    \end{bmatrix}
    =
    \begin{bmatrix}
    AE \ AF \ be \ BF\\\\
    AG \ AH \ BG \ BH\\\\
    CE \ CF \ de \ DF\\\\
    CG \ ch \ DG \ dh \end{bmatrix} .
$$

Eine abschließende, nützliche, in Bezug auf das tensorflow-Produkt verwendete Anmerkung ist, dass für alle Vektor- $ v $ -oder Matrix- $ m $ , $ v ^ { \otimes n } $ oder $ M ^ { \otimes n } $ für ein $ n $ -Fold wiederholtes tensorflow-Produkt kurz Hand ist.  Beispiel:

\begin{align}
&\begin{bmatrix}1 \\\\ 0 1 \end{bmatrix} ^ { \otimes } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1 \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\
  &\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 1 & 0 & 0 & 0 \end{bmatrix} .
\end{align}
