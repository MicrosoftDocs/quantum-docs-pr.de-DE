---
title: Erweiterte Matrixkonzepte
description: Erfahren Sie mehr über Eigenvektoren, Eigenwerte und Matrix exponentiale, die grundlegenden Tools, die zum beschreiben und Simulieren von Quantum-Algorithmen verwendet werden.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: a83911e01ad758bbcb7f701000fd58b4f1c91cd2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907578"
---
# <a name="advanced-matrix-concepts"></a>Erweiterte Matrix Konzepte #

Wir erweitern nun unsere Manipulation von Matrizen auf [*Eigenwerte, Eigenvektoren*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) und [*exponentiale*](https://en.wikipedia.org/wiki/Matrix_exponential) , die einen grundlegenden Satz von Tools bilden, die wir zum beschreiben und Implementieren von Quantum-Algorithmen benötigen.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenwerte und Eigenvektoren ##

Lassen Sie $M $ eine quadratische Matrix und $v $ ein Vektor sein, der nicht der NULL-Vektor ist (d. h. der Vektor mit allen Einträgen gleich $0 $).

Wir sagen $v $ ist ein [*eigen Vektor*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $M $, wenn $MV = CV $ für eine bestimmte Zahl $c $ ist. Wir sagen $c $ ist der [*eigen Wert*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) , der dem Eigen Vektor $v $ entspricht. Im Allgemeinen kann eine Matrix $M $ einen Vektor in einen anderen Vektor umwandeln, aber ein eigen Vektor ist ein besonderes Zeichen, da er unverändert bleibt, außer dass er mit einer Zahl multipliziert wird. Beachten Sie Folgendes: Wenn $v $ ein eigen Vektor mit einem eigen Wert $c $ ist, dann ist $AV $ auch ein eigen Vektor (für alle nicht-NULL-$a $) mit demselben eigen Wert.

Beispielsweise ist für die Identitätsmatrix jeder Vektor $v $ ein eigen Vektor mit dem Eigen Wert $1 $.

Ein weiteres Beispiel ist eine [*diagonale Matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D $, die nur Einträge ungleich 0 (null) auf der Diagonal aufweist:

$ $ \begin{bmatrix} d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & D_3 \end{bmatrix}.
$$

Die Vektoren

$ $ \begin{bmatrix}1 \\\\ 0 \\\\ 0 \ End{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0 \ Ende {bmatrix} und \begin{bmatrix}0 \\\\ 0 \\\\ 1 \ Ende {bmatrix} $ $

sind Eigenvektoren dieser Matrix mit eigen Werten $d _1 $, $d _2 $, bzw. $d _3 $. Wenn $d _1 $, $d _2 $ und $d _3 $ unterschiedliche Zahlen sind, sind diese Vektoren (und ihre vielfache) die einzigen Eigenvektoren der Matrix $D $. Im Allgemeinen ist es für eine diagonal Matrix leicht, die Eigenwerte und Eigenvektoren zu lesen. Die Eigenwerte sind alle Zahlen, die auf der diagonalen angezeigt werden, und ihre jeweiligen Eigenvektoren sind die Einheits Vektoren, bei denen ein Eintrag gleich $1 $ und die restlichen Einträge gleich $0 $ sind.

Beachten Sie im obigen Beispiel, dass die Eigenvektoren von $D $ eine Grundlage für $3 $-dimensionale Vektoren bilden. Eine Basis ist ein Satz von Vektoren, sodass jeder Vektor als lineare Kombination von Ihnen geschrieben werden kann. Explizitere, $v _1 $, $v _2 $ und $v _3 $ bilden eine Grundlage, wenn ein Vektor $v $ als $v = A_1 V_1 + a_2 V_2 + a_3 V_3 $ für einige Zahlen $a _1 $, $a _2 $ und $a _3 $ geschrieben werden kann.

Beachten Sie, dass eine hermitische Matrix (auch als selbst Adjoint bezeichnet) eine komplexe quadratische Matrix ist, die mit ihrer eigenen komplexen konjugierung identisch ist, während eine einheitliche Matrix eine komplexe Quadrat Matrix ist, deren Umkehrung gleich der komplexen konjugierung ist.
Bei hermitian-und einheitlichen Matrizen, bei denen es sich im Wesentlichen um die einzigen Matrizen in Quantum Computing handelt, gibt es ein allgemeines Ergebnis, das als " [*Spektral Theorem*](https://en.wikipedia.org/wiki/Spectral_theorem)" bezeichnet wird, das Folgendes bestätigt: für jede hermitische oder einheitliche Matrix $M $ gibt es eine einheitliche $U $, sodass $M = u ^ \dagger D U $ für eine diagonale Matrix $D $ Außerdem sind die diagonalen Einträge von $D $ die Eigenwerte $M $.

Wir wissen bereits, wie die Eigenwerte und Eigenvektoren einer Diagonalen Matrix $D $ berechnet werden. Bei Verwendung dieses Theorem wissen wir, dass $U ^ \dagger v $ ein eigen Vektor von $M $ mit dem Eigen Wert $c $ ist, wenn $v $ ein eigen Vektor von $D $ mit dem Eigen Wert $c $ ist, d. h. $DV = CV $. Dies liegt daran, dass

$ $M (u ^ \dagger v) = u ^ \dagger d U (U ^ \dagger v) = u ^ \dagger D (u u ^ \dagger) v = u ^ \dagger d v = c U ^ \dagger v. $ $

## <a name="matrix-exponentials"></a>Matrix exponentiale
Eine [*Matrix Exponentialwert*](https://en.wikipedia.org/wiki/Matrix_exponential) kann auch exakt mit der Exponentialfunktion definiert werden.  Das exponentielle Matrix einer Matrix $A $ kann als

$ $ e ^ A = \boldone + A + \bruchteil {a ^ 2} {2!} + \bruchteil {a ^ 3} {3!} + \cdots $ $

Dies ist wichtig, da die Weiterentwicklung von Quantum-mechanischer Zeit durch eine einheitliche Matrix der Form $e ^ {IB} $ für hermitian Matrix $B $ beschrieben wird.  Aus diesem Grund ist das Durchführen von Matrix Exponentialzahlen ein wesentlicher Bestandteil von Quantum Computing, da Q# systeminterne Routinen zum Beschreiben dieser Vorgänge bietet.
In der Praxis gibt es viele Möglichkeiten, eine Matrix auf einem klassischen Computer exponentiell zu berechnen, und in der Regel wird eine solche exponentialweise mit der Peril in Bezug gesetzt.  Weitere Informationen finden Sie unter [*Cleve Moler und Charles Van Loan. "Neun zweifelhafte Möglichkeiten, den Exponentialwert einer Matrix zu berechnen." Siam Review 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) , um weitere Informationen zu den beteiligten Problemen zu finden.

Die einfachste Möglichkeit, um zu verstehen, wie die exponentielle einer Matrix berechnet werden kann, ist die Eigenwerte und Eigenvektoren dieser Matrix.  Insbesondere das oben beschriebene Spektral Theorem besagt, dass für jede hermitische oder einheitliche Matrix $A $ eine einheitliche Matrix $U $ und eine diagonale Matrix $D $, sodass $A = U ^ \dagger D U $ vorhanden ist.  Aufgrund der Eigenschaften von Unitarity haben wir diese $A ^ 2 = u ^ \dagger d ^ 2 U $ und auf ähnliche Weise bei allen Power $p $ $A ^ p = u ^ \dagger d ^ p U $.  Wenn wir dies in die Operator Definition des Operator exponentiell ersetzen, erhalten wir Folgendes:

$ $ e ^ A = U ^ \dagger \left (\boldone + D + \bruchteil {d ^ 2} {2!} + \cdots \right) u = u ^ \dagger \begin{bmatrix}\exp (D_{11}) & 0 & \cdots & 0\\\\ 0 & \exp (D_{22}) & \cdots & 0\\\\ \vdots & \vdots & \ddots & \vdots\\\\ 0 & 0 & \cdots & \exp (D_ {NN}) \end{bmatrix} U. $ $

Anders ausgedrückt: Wenn Sie in die eigenständige Matrix der Matrix umwandeln $A $, entspricht das Berechnen der Matrix exponentiell dem Berechnen des normalen exponentiellen Werts der Eigenwerte der Matrix.  Wie viele Vorgänge in Quantum Computing das Durchführen von Matrix Exponentialzahlen umfassen, wird dieser Trick der Umwandlung in die eigenständige Basis einer Matrix, um die Ausführung des Operator exponentialmäßig zu vereinfachen, häufig angezeigt und ist die Grundlage für viele Quantum-Algorithmen wie Trotter – im weiteren Verlauf dieses Handbuchs erörterte Quantum-Simulationsmethoden im Suzuki-Stil.

Eine weitere nützliche Eigenschaft ist, wenn $B $ sowohl einheitlich als auch hermitian ist, d. h. $B = b ^{-1}= b ^ \dagger $ then $B ^ 2 = \boldone $. Durch Anwenden dieser Regel auf die oben genannte Erweiterung der Matrix und durch Gruppierung von $ \boldone $ und der $B $-Begriffe können Sie sehen, dass für jeden echten Wert $x $ der Identität

$ $e ^ {IBX} = \boldone \cos (x) + ib\sin (x) $ $


bestand. Dieser Trick ist besonders nützlich, da er es in Bezug auf die exponentialaktionen der Aktionen gibt, auch wenn die Dimension von $B $ exponentiell groß ist, für den Sonderfall, wenn $B $ sowohl einheitlich als auch hermitian ist.
