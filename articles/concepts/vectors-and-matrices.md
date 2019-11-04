---
title: Vektoren und Matrizen | Microsoft-Dokumentation
description: Vektoren und Matrizen
author: QuantumWriter
uid: microsoft.quantum.concepts.vectors
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 58c96f9cda22b712e1a408e5566e0a8ee987bd6e
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183742"
---
# <a name="vectors-and-matrices"></a>Vektoren und Matrizen

Eine Vertrautheit mit Vektoren und Matrizen ist für das Verständnis von Quantum Computing von entscheidender Bedeutung. Im folgenden finden Sie eine kurze Einführung, und interessierte Leser werden empfohlen, einen Standard Verweis auf lineare Algebra zu lesen, z. b. für die Tabelle *, G. (1993). Einführung in lineare Algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* oder eine Online Referenz, wie z. b. [lineare Algebra](http://joshua.smcvt.edu/linearalgebra/).

Ein Spalten Vektor (oder einfach [*Vektor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ der Dimension (oder Größe) $n $ ist eine Auflistung von $n $ Complex-Zahlen (V_1, V_2, \ldots, v_n) $, die als Spalte angeordnet sind:

$ $v = \begin{bmatrix} V_1\\\\ V_2\\\\ \vdots\\\\ v_n \end{bmatrix} $ $

Die Norm eines Vector-$v $ ist als $ \sqrt{\sum\_i | v\_i | ^ 2} $ definiert. Ein Vektor wird als Einheits Norm bezeichnet (oder alternativ als [*Einheits Vektor*](https://en.wikipedia.org/wiki/Unit_vector)bezeichnet), wenn seine Norm $1 $ ist. Das [*Adjoint eines Vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) -$v $ wird $v ^ \dagger $ bezeichnet und als folgender Zeilen Vektor definiert, wobei $\*$ die komplexe konjugierung bezeichnet.

$ $ \begin{bmatrix}V_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix}V_1 ^ * & \cdots & v_n ^ * \end{bmatrix} $ $

Die gängigste Methode, zwei Vektoren zu multiplizieren, ist das [*innere Produkt*](https://en.wikipedia.org/wiki/Inner_product_space), das auch als "Punktprodukt" bezeichnet wird.  Das innere Produkt liefert die Projektion eines Vektors auf einen anderen und ist äußerst nützlich, um zu beschreiben, wie ein Vektor als Summe aus anderen einfacheren Vektoren ausgedrückt wird.  Das innere Produkt zwischen $u $ und $v $, bezeichnet $ \left\langle u, v\right\rangle $ ist definiert als

$ $ \langle u, v\rangle = u ^ \dagger v = u\_1 ^ {\*} V_1 + \cdots + u\_n ^ {\*} v\_n.
$$

Diese Notation ermöglicht außerdem das Schreiben der Norm eines Vector-$v $ als $ \sqrt{\langle v, v\rangle} $.

Wir können einen Vektor mit einer Zahl $c $ multiplizieren, um einen neuen Vektor zu bilden, dessen Einträge mit $c $ multipliziert werden. Wir können auch zwei Vektoren $u $ und $v $ hinzufügen, um einen neuen Vektor zu bilden, dessen Einträge die Summe der Einträge von $u $ und $v $ sind. Diese Vorgänge werden im folgenden dargestellt:

$ $ \mathrm{if} ~ u = \begin{bmatrix} u_1\\\\ u_2\\\\ \vdots\\\\ u_n \end{bmatrix} ~ \mathrm{and} ~ v = \begin{bmatrix} V_1\\\\ V_2\\\\ \vdots @no__ t_10_ \\ v_n \end{bmatrix}, ~ \mathrm{then} ~ au + BV = \begin{bmatrix} au_1 + bv_1\\\\ au_2 + bv_2\\\\ \vdots\\\\ au_n + bv_n \end{bmatrix}.
$$

Eine [*Matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) der Größe $m \times n $ ist eine Auflistung von $MN $ komplexen Zahlen, die in $m $ Rows angeordnet sind, und $n $ Columns, wie unten dargestellt:

$ $M = \begin{bmatrix} M_{11} ~ ~ M_{12} ~ ~ \cdots ~ ~ M_ {1N}\\\\ M_{21} ~ ~ M_{22} ~ ~ \cdots ~ ~ M_ {2N}\\\\ \ddots\\\\ M_ {M1} ~ ~ M_ {m2} ~ ~ \cdots ~ ~ M_ {MN}\\@no__ t_11_ \end{bmatrix}. $ $

Beachten Sie, dass ein Vektor von Dimension $n $ einfach eine Matrix der Größe $n \times $1 ist. Wie bei Vektoren können wir eine Matrix mit einer Zahl $c $ multiplizieren, um eine neue Matrix zu erhalten, in der jeder Eintrag mit $c $ multipliziert wird. Wir können zwei Matrizen derselben Größe hinzufügen, um eine neue Matrix zu generieren, deren Einträge die Summe der entsprechenden Einträge der beiden Matrizen sind. 

## <a name="matrix-multiplication-and-tensor-products"></a>Matrix Multiplikation und Tensor-Produkte

Wir können auch zwei Matrizen $M $ of Dimension $m \times n $ und $N $ of Dimension $n \time p $ multiplizieren, um eine neue Matrix $P $ of Dimension $m \times p $ wie folgt zu erhalten:

\begin{align} & \begin{bmatrix} M_{11} ~ ~ M_{12} ~ ~ \cdots ~ ~ M_ {1N}\\\\ M_{21} ~ ~ M_{22} ~ ~ \cdots ~ ~ M_ {2N}\\\\ \ddots\\\\ M_ {M1} ~ ~ M_ {m2} ~ ~ \cdots ~ ~ M_ {MN} \end{bmatrix} \ BEGIN {bmatrix} N_{11} ~ ~ N_{12} ~ ~ \cdots ~ ~ N_ {1P}\\\\ N_{21} ~ ~ N_{22} ~ ~ \cdots ~ ~ N_ {2P}\\\\ \ddots\\\\ N_ {N1} ~ ~ N_ {N2} ~ ~ \cdots ~ ~ N_ {NP} \end{bmatrix} = \begin{bmatrix} P_{11} ~ ~ P_{12} ~ ~ \cdots ~ ~ P_ {1P}\\\\ P_{21} ~ ~ P_{22} ~ ~ \cdots ~ ~ P_ {2P}\\\\ \ddots\\\\ P_ {M1} ~ ~ P_ {m2} ~ ~ \cdots ~ ~ P_ {MP} \end{bmatrix} \end{align}

Wenn die Einträge von $P $ $P _ {IK} = \sum_j M_ {IJ} N_ {JK} $ sind. Beispielsweise ist der Eintrag $P _{11}$ das innere Produkt der ersten Zeile von $M $ mit der ersten Spalte $N $. Beachten Sie, dass sich diese Definition auf die Matrix Vektor Multiplikation erstreckt, da ein Vektor einfach ein Sonderfall einer Matrix ist. 

Alle Matrizen, die wir in Erwägung gezogen, sind entweder quadratische Matrizen, bei denen die Anzahl der Zeilen und Spalten gleich ist, oder Vektoren, die nur $1 $-Spalten entsprechen. Eine spezielle quadratische Matrix ist die [*Identitätsmatrix*](https://en.wikipedia.org/wiki/Identity_matrix), die "$ \boldone $" bezeichnet und deren diagonale Elemente gleich $1 $ und die restlichen Elemente gleich $0 $ sind:

$ $ \boldone = \begin{bmatrix} 1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\ 0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\ ~ ~ \ddots\\\\ 0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \end{bmatrix}. $ $

Für eine quadratische Matrix $A $ sagen wir, dass eine Matrix $B $ die [*umgekehrte*](https://en.wikipedia.org/wiki/Invertible_matrix) ist, wenn $ab = BA = \boldone $ ist. Die Umkehrung einer Matrix muss nicht vorhanden sein. Wenn Sie jedoch vorhanden ist, ist sie eindeutig, und wir bezeichnen Sie $A ^{-1}$. 

Bei allen Matrizen $M $ ist das Adjoint-oder konjugierte $M $ eine Matrix $N $, sodass $N _ {IJ} = M_ {JI} ^\*$ ist. Das Adjoint-$M $ wird normalerweise $M ^ \dagger $ bezeichnet. Wir sagen, dass eine Matrix $U $ [*einheitlich*](https://en.wikipedia.org/wiki/Unitary_matrix) ist, wenn $UU ^ \dagger = u ^ \dagger U = \boldone $ oder gleichwertig $U ^{-1} = u ^ \dagger $.  Die wichtigste Eigenschaft der einheitlichen Matrizen ist, dass Sie die Norm eines Vektors erhalten.  Dies liegt daran, dass 

$ $ \langle v, v \rangle = v ^ \dagger v = v ^ \dagger u ^{-1} U v = v ^ \dagger u ^ \dagger u v = \langle u v, u v\rangle. $ $  

Eine Matrix $M $ heißt [*hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) , wenn $M = M ^ \dagger $.

Schließlich ist das [*tensorflow-Produkt*](https://en.wikipedia.org/wiki/Tensor_product) (oder Kronecker-Produkt) von zwei Matrizen $M $ der Größe $m \times n $ und $N $ der Größe $p \times q $ eine größere Matrix $P = m\otimes n $ der Größe $MP \times NQ $ und wird wie folgt aus $M $ und $N $ abgerufen:

\begin{align} M \otimes N & = \begin{bmatrix} M_{11} ~ ~ \cdots ~ ~ M_ {1N} \\\\ \ddots\\\\ M_ {M1} ~ ~ \cdots ~ ~ M_ {MN} \end{bmatrix} \otimes \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1Q}\\\\ \ddots @no__ t_8_ \\ N_ {P1} ~ ~ \cdots ~ ~ N_ {PQ} \end{bmatrix}\\\\ & = \begin{bmatrix} M_{11} \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1Q}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {PQ} \end{bmatrix} ~ ~ \cdots ~ ~ M_ {1N} \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1Q}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {PQ} \end{bmatrix}\\\\ \ddots\\\\ M_ {M1} \begin{bmatrix} N_{11} ~ ~ \ cdots ~ ~ N_ {1Q}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {PQ} \end{bmatrix} ~ ~ \cdots ~ ~ M_ {MN} \begin{bmatrix} N_{11} ~ ~ \cdots ~ ~ N_ {1Q}\\\\ \ddots\\\\ N_ {P1} ~ ~ \cdots ~ ~ N_ {PQ} \end {bmatrix} \end{bmatrix}.
\end{align}

Dies wird in einigen Beispielen besser veranschaulicht:

$ $ \begin{bmatrix} a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix} a \begin{bmatrix} c \\\\ \\d \\ @no__ e \end{bmatrix} t_10_ \\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end {bmatrix} \end{bmatrix} = \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\ende {bmatrix} $ $

und der

$ $ \begin{bmatrix} a \ b \\\\ c \ d \end{bmatrix} \otimes \begin{bmatrix} e \ f\\\\g \ h \end{bmatrix} = \begin{bmatrix} a\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} b\begin {bmatrix} e \ f\\@no__ t_7_ g \ h \end{bmatrix} \\\\[1em] c\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} d\begin {bmatrix} e \ f\\\\ g \ h \end{bmatrix} \end{bmatrix} = \begin{bmatrix} AE \ AF \ be \ BF \\@no__ t_15_ AG \ AH \ BG \ BH \\\\ CE \ CF \ de \ DF \\\\ CG \ ch \ DG \ dh \end{bmatrix}.
$$

Eine abschließende, nützliche, in Bezug auf die tensorflow-Produkte für alle Vektor $v $ oder Matrix $M $, $v ^ {\otimes n} $ oder $M ^ {\otimes n} $ ist eine kurze Hand für ein $n $-Fold-tensorflow-Produkt.  Beispiel:

\begin{align} & \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} ^ {\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \ End{bmatrix}, \qquad\begin{bmatrix} 1 \\\\-1 \end{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 1 \\\\-1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ & \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ {\otimes 1} = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}, \qquad\begin{bmatrix} 0 & 1 \\@no__ t_27_ 1 & 0 \ End{bmatrix} ^ {\otimes 2} = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0\\\\ 1 & 0 & 0 & 0 \ Ende {bmatrix}.
\end{align}

