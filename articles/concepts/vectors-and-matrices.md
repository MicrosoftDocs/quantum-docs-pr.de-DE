---
title: Vektoren und Matrizen beim Quantencomputing
description: Erfahren Sie mehr über die Grundlagen der Arbeit mit Vektoren und Matrizen.
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: f9d4e14742b7d06a6e90af0902b31fbdf17aedab
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269540"
---
# <a name="vectors-and-matrices"></a>Vektoren und Matrizen

Eine Vertrautheit mit Vektoren und Matrizen ist für das Verständnis von Quantum Computing von entscheidender Bedeutung. Im folgenden finden Sie eine kurze Einführung, und interessierte Leser werden empfohlen, einen Standard Verweis auf lineare Algebra zu lesen, z. b. für die Tabelle *, G. (1993). Einführung in lineare Algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* oder eine Online Referenz, wie z. b. [lineare Algebra](http://joshua.smcvt.edu/linearalgebra/).

Ein Spalten Vektor (oder ein einfaches [*Vektor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ der Dimension (oder Größe) $n $ eine Auflistung $n $ komplexer Zahlen $ (V_1, V_2, \ldots, v_n) $ ist, die als Spalte angeordnet sind:

$ $v = \begin{bmatrix}
v_1\\\\
v_2\\\\
\vdots\\\\
v_n \end{bmatrix}$$

Die Norm eines Vektor $v $ wird als $ \sqrt { \sum \_ i | v \_ i | ^ 2 $ definiert } . Ein Vektor wird als Einheits Norm bezeichnet (oder alternativ als [*Einheits Vektor*](https://en.wikipedia.org/wiki/Unit_vector)bezeichnet), wenn seine Norm $1 ist $ . Das [*Adjoint eines Vektor*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v $ wird $v ^ \dagger bezeichnet und als $ folgender Zeilen Vektor definiert, wobei $ \* $ die komplexe konjugierung bezeichnet.

$ $ \begin{ bmatrix } V_1 \\ \\ \vdots \\ \\ v_n \end{ bmatrix } ^ \dagger = \begin{ bmatrix } V_1 ^ * & \cdots & v_n ^ * \end{bmatrix}$$

Die gängigste Methode, zwei Vektoren zu multiplizieren, ist das [*innere Produkt*](https://en.wikipedia.org/wiki/Inner_product_space), das auch als "Punktprodukt" bezeichnet wird.  Das innere Produkt liefert die Projektion eines Vektors auf einen anderen und ist äußerst nützlich, um zu beschreiben, wie ein Vektor als Summe aus anderen einfacheren Vektoren ausgedrückt wird.  Das innere Produkt zwischen $u $ und $v $ , angegeben als "$ \left \langle u", v \right \rangle $ ist definiert als

$ $ \langle u, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } V_1 + \cdots + u \_ n ^ { \* } v \_ n.
$$

Diese Notation ermöglicht außerdem, dass die Norm eines Vector-$v $ als $ \sqrt { \langle v, v $ geschrieben wird \rangle } .

Ein Vektor kann mit einer Zahl $c multipliziert $ werden, um einen neuen Vektor zu bilden, dessen Einträge mit $c multipliziert werden $ . Wir können auch zwei Vektoren $u $ und $v hinzufügen $ , um einen neuen Vektor zu bilden, dessen Einträge die Summe der Einträge von $u $ und $v sind $ . Diese Vorgänge werden im folgenden dargestellt:

$ $ \mathrm{if } ~ u = \begin{bmatrix}
u_1\\\\
u_2\\\\
\vdots\\\\
u_n \end{ bmatrix } ~ \mathrm{und } ~ v = \begin{bmatrix}
    v_1\\\\
    v_2\\\\
    \vdots\\\\
    v_n \end{ bmatrix } , ~ \mathrm{then } ~ au + BV = \begin{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\vdots\\\\
au_n + bv_n \end{ bmatrix } .
$$

Eine [*Matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) der Größe $m \times n $ ist eine Auflistung von $MN $ komplexen Zahlen, die in $m $ Zeilen und $n Spalten angeordnet sind, $ wie unten dargestellt:

$ $M = \begin{bmatrix}
M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2N } \\ \\ \ddots\\\\
M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {MN } \\ \\ \end{ bmatrix } . $ $

Beachten Sie, dass es sich bei einem Vektor mit Dimensions $n $ einfach um eine Matrix der Größe handelt $n \times 1 $ . Wie bei Vektoren können wir eine Matrix mit einer Zahl $c multiplizieren, $ um eine neue Matrix zu erhalten, in der jeder Eintrag mit $c multipliziert ist $ , und wir können zwei Matrizen derselben Größe hinzufügen, um eine neue Matrix zu generieren, deren Einträge die Summe der entsprechenden Einträge der beiden Matrizen sind. 

## <a name="matrix-multiplication-and-tensor-products"></a>Matrix Multiplikation und Tensor-Produkte

Wir können auch zwei Matrizen $M $ der Dimension $m \times n $ und $N $ der Dimension $n \time p multiplizieren $ , um wie folgt eine neue Matrix $P $ der Dimension $m "\time p" zu erhalten $ :

\begin{align}
& \begin{bmatrix}
    M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2N } \\ \\ \ddots\\\\
    M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {MN}
Schließlichbmatrix}
beginnenbmatrix}
N_ {11 } ~ ~ N_ {12 } ~ ~ \cdots ~ ~ N_ {1P } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \cdots ~ ~ N_ {2P } \\ \\ \ddots\\\\
N_ {N1 } ~ ~ N_ {N2 } ~ ~ \cdots ~ ~ N_ {NP}
\end{ bmatrix } = \begin{bmatrix}
P_ {11 } ~ ~ P_ {12 } ~ ~ \cdots ~ ~ P_ {1P } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \cdots ~ ~ P_ {2P } \\ \\ \ddots\\\\
P_ {M1 } ~ ~ P_ {m2 } ~ ~ \cdots ~ ~ P_ {MP}
Schließlichbmatrix}
\end{align}

Wenn die Einträge $P $ $P _ {IK } = \ sum_j M_ {IJ} N_ {JK } $. Der Eintrag $P _ {11 } $ ist beispielsweise das innere Produkt der ersten Zeile $M $ mit der ersten Spalte $N $ . Beachten Sie, dass sich diese Definition auf die Matrix Vektor Multiplikation erstreckt, da ein Vektor einfach ein Sonderfall einer Matrix ist. 

Alle Matrizen, die wir in Erwägung haben, sind entweder quadratische Matrizen, bei denen die Anzahl der Zeilen und Spalten gleich ist, oder Vektoren, die nur $1- $ Spalten entsprechen. Eine spezielle quadratische Matrix ist die [*Identitätsmatrix*](https://en.wikipedia.org/wiki/Identity_matrix), die "$ \boldone" bezeichnet $ , die alle diagonal Elemente gleich $1 $ und die restlichen Elemente gleich $0 sind $ :

$ $ \boldone = \begin{bmatrix}
1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\
0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\
~ ~ \ddots\\\\
0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \end{ bmatrix } . $ $

Für eine quadratische Matrix $A $ sagen wir, dass eine Matrix $B $ Ihre [*Umkehrung*](https://en.wikipedia.org/wiki/Invertible_matrix) ist, wenn $ab = BA = \boldone $ . Die Umkehrung einer Matrix muss nicht vorhanden sein. Wenn Sie jedoch vorhanden ist, ist sie eindeutig, und wir bezeichnen Sie $A ^ {-1 } $. 

Bei allen Matrizen $M $ ist die Adjoint-oder konjugierte $M $ eine Matrix $N, die $ $N _ {IJ } = M_ {JI } ^ \* $ ist. Das Adjoint von $M $ wird normalerweise $M ^ \dagger bezeichnet $ . Wir sagen, dass eine Matrix $U $ [*einheitlich*](https://en.wikipedia.org/wiki/Unitary_matrix) ist, wenn $UU ^ \dagger = u ^ \dagger U = \boldone $ oder gleichwertig $U ^ {-1 } = u ^ \dagger ist $ .  Die wichtigste Eigenschaft der einheitlichen Matrizen ist, dass Sie die Norm eines Vektors erhalten.  Dies liegt daran, dass 

$ $ \langle v, v \rangle = v ^ \dagger v = v ^ \dagger u ^ {-1 } U v = v ^ \dagger u ^ \dagger u v = \langle u v, u v \rangle . $ $  

Eine Matrix $M als $ [*hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) bezeichnet, wenn $M = M ^ \dagger $ .

Zum Schluss ist das [*tensorflow-Produkt*](https://en.wikipedia.org/wiki/Tensor_product) (oder Kronecker-Produkt) mit zwei Matrizen $M $ der Größe $m \times n $ und $N $ der Größe $p \times q $ eine größere Matrix $P = M \otimes n $ der Größe $MP \times NQ " $ und wird von $M $ und $N $ wie folgt abgerufen:

\begin{align}
    M \otimes N &= \begin{bmatrix}
        M_ {11 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ \ddots\\\\
        M_ {M1 } ~ ~ \cdots ~ ~ M_ {MN}
    Schließlichbmatrix}
    \otimes \begin{bmatrix}
        N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots\\\\
        N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ}
    \end{ bmatrix } \\ \\ &= \begin{bmatrix}
        M_ {11 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{ bmatrix } ~ ~ \cdots ~ ~ M_ {1N } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{ bmatrix } \\ \\ \ddots\\\\
        M_ {M1 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{ bmatrix } ~ ~ \cpunkte ~ ~ M_ {MN } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{bmatrix}
    \end{ bmatrix } .
\end{align}

Dies wird in einigen Beispielen besser veranschaulicht:

$ $ \begin{bmatrix}
        a \\ \\ b \end{ bmatrix } \otimes \begin{ bmatrix } c \\ \\ d \\ \\ e \end{ bmatrix } = \begin{bmatrix}
        a \begin{ bmatrix } c \\ \\ d \\ \\ e \end{bmatrix}
        \\\\[1.5 em] b \begin{ bmatrix } c \\ \\ d \\ \\ e\end{bmatrix}
    Schließlichbmatrix}
    = \begin{ bmatrix } a c \\ \\ a d \\ \\ a e \\ \\ b c \\ \\ b d \\ \\\end{bmatrix}
$$

und

$ $ \begin{bmatrix}
        a \ b \\ \\ c \ d \end{bmatrix}
    \otimes \begin{bmatrix}
        e \ f \\ \\ \ h \end{bmatrix}
     = \begin{bmatrix}
    ein\begin{bmatrix}
    e \ f \\\\ \ h \end{bmatrix}
    b\begin{bmatrix}
    e \ f \\\\ \ h \end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ \ h \end{bmatrix}
    d\begin{bmatrix}
    e \ f \\\\ \ h \end{bmatrix}
    Schließlichbmatrix}
    = \begin{bmatrix}
    AE \ AF \ be \ BF \\ \\ AG \ AH \ BG \ BH \\ \\ CE \ CF \ de \ DF \\ \\ CG \ ch \ DG \ dh \end{ bmatrix } .
$$

Eine abschließende, nützliche, in Bezug auf die tensorflow-Produkte für alle Vektor $v $ oder Matrix $M $ $v ^ {\otimes n } $ oder $M ^ {\otimes n } $ ist für ein $n $ wiederholten tensorflow-Produkt eine kurze Hand.  Beispiel:

\begin{align}
& \begin{ bmatrix } 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 1 \\ \\ 0 \ End{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ 0 0 \\ \\ \\ \\ 0 \ End{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ -1 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \ End{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } , \qquad \begin{bmatrix} 0 & 1 \\ \\ 1 & 0 \ End{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 0 #b4 0&0&1 \\ \\ 0 &0&1&0 \\ \\ 0 &1&0&0 \\\\ 1 &0&0&0 \end{bmatrix} .
\end{align}
