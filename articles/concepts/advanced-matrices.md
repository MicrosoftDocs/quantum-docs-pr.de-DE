---
title: Erweiterte Matrixkonzepte
description: Erfahren Sie mehr über Eigenvektoren, Eigenwerte und Matrix exponentiale, die grundlegenden Tools, die zum beschreiben und Simulieren von Quantum-Algorithmen verwendet werden.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
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
ms.openlocfilehash: 8d3c646715f13c454e51b9295cbfdabf6a236ffc
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630148"
---
# <a name="advanced-matrix-concepts"></a><span data-ttu-id="f008e-103">Erweiterte Matrix Konzepte</span><span class="sxs-lookup"><span data-stu-id="f008e-103">Advanced Matrix Concepts</span></span> #

<span data-ttu-id="f008e-104">Wir erweitern nun unsere Manipulation von Matrizen auf [*Eigenwerte, Eigenvektoren*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) und [*exponentiale*](https://en.wikipedia.org/wiki/Matrix_exponential) , die einen grundlegenden Satz von Tools bilden, die wir zum beschreiben und Implementieren von Quantum-Algorithmen benötigen.</span><span class="sxs-lookup"><span data-stu-id="f008e-104">We now extend our manipulation of Matrices to [*Eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) and [*Exponentials*](https://en.wikipedia.org/wiki/Matrix_exponential) which form a fundamental set of tools we need to describe and implement quantum algorithms.</span></span>

## <a name="eigenvalues-and-eigenvectors"></a><span data-ttu-id="f008e-105">Eigenwerte und Eigenvektoren</span><span class="sxs-lookup"><span data-stu-id="f008e-105">Eigenvalues and Eigenvectors</span></span> ##

<span data-ttu-id="f008e-106">Let $M $ eine quadratische Matrix und $v $ ein Vektor sein, der nicht der NULL-Vektor ist (d. h. der Vektor, der alle Einträge gleich $0 ist $ ).</span><span class="sxs-lookup"><span data-stu-id="f008e-106">Let $M$ be a square matrix and $v$ be a vector that is not the all zeros vector (i.e., the vector with all entries equal to $0$).</span></span>

<span data-ttu-id="f008e-107">Wir sagen $v $ einen [*eigen Vektor*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) $M, $ wenn $MV = CV $ für eine bestimmte Anzahl $c ist $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-107">We say $v$ is an [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) of  $M$ if $Mv = cv$ for some number $c$.</span></span> <span data-ttu-id="f008e-108">Wir sagen $c $ der [*eigen Wert*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) , der dem Eigen Vektor $v entspricht $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-108">We say $c$ is the [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) corresponding to the eigenvector $v$.</span></span> <span data-ttu-id="f008e-109">Im Allgemeinen kann eine Matrix $M $ einen Vektor in einen anderen Vektor umwandeln, aber ein eigen Vektor ist ein besonderes Zeichen, da er unverändert bleibt, außer dass er mit einer Zahl multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="f008e-109">In general a matrix $M$ may transform a vector into any other vector, but an eigenvector is special because it is left unchanged except for being multiplied by a number.</span></span> <span data-ttu-id="f008e-110">Beachten Sie Folgendes: Wenn $v $ ein eigen Vektor mit einem eigen Wert $c ist $ , dann $ ist $AV auch ein eigenständiger Vektor (für alle nicht-NULL-$a $ ) mit demselben eigen Wert.</span><span class="sxs-lookup"><span data-stu-id="f008e-110">Note that if $v$ is an eigenvector with eigenvalue $c$, then $av$ is also an eigenvector (for any nonzero $a$) with the same eigenvalue.</span></span>

<span data-ttu-id="f008e-111">Beispielsweise ist für die Identitätsmatrix jeder Vektor $v $ ein eigen Vektor mit dem Eigen Wert $1 $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-111">For example, for the identity matrix, every vector $v$ is an eigenvector with eigenvalue $1$.</span></span>

<span data-ttu-id="f008e-112">Nehmen Sie als weiteres Beispiel eine [*diagonale Matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D $ , die nur Einträge ungleich 0 (null) auf der Diagonal aufweist:</span><span class="sxs-lookup"><span data-stu-id="f008e-112">As another example, consider a [*diagonal matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D$ which only has nonzero entries on the diagonal:</span></span>

<span data-ttu-id="f008e-113">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="f008e-113">$$ \begin{bmatrix}</span></span>
<span data-ttu-id="f008e-114">d_1 & 0 & 0 \\ \\ 0 & d_2 & 0 \\ \\ 0 & 0 & D_3 \ End{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="f008e-114">d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & d_3 \end{bmatrix}.</span></span>
$$

<span data-ttu-id="f008e-115">Die Vektoren</span><span class="sxs-lookup"><span data-stu-id="f008e-115">The vectors</span></span>

<span data-ttu-id="f008e-116">$ $ \begin{ bmatrix } 1 \\ \\ 0 \\ \\ 0 \end{ bmatrix } , \begin{ bmatrix } 0 \\ \\ 1 \\ \\ 0 \end { bmatrix } und \begin{ bmatrix } 0 \\ \\ 0 \\ \\ 1 \end {bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="f008e-116">$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix}, \begin{bmatrix}0 \\\\ 1 \\\\ 0\end{bmatrix} and \begin{bmatrix}0 \\\\ 0 \\\\ 1\end{bmatrix}$$</span></span>

<span data-ttu-id="f008e-117">sind Eigenvektoren dieser Matrix mit eigen Werten $d _1 $ , $d _2 $ , bzw. $d _3 $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-117">are eigenvectors of this matrix with eigenvalues  $d_1$, $d_2$, and $d_3$, respectively.</span></span> <span data-ttu-id="f008e-118">Wenn $d _1 $ , $d _2 $ und $d _3 unter $ schiedliche Zahlen sind, sind diese Vektoren (und ihre vielfache) die einzigen Eigenvektoren der Matrix $D $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-118">If $d_1$, $d_2$, and $d_3$ are distinct numbers, then these vectors (and their multiples) are the only eigenvectors of the matrix $D$.</span></span> <span data-ttu-id="f008e-119">Im Allgemeinen ist es für eine diagonal Matrix leicht, die Eigenwerte und Eigenvektoren zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f008e-119">In general, for a diagonal matrix it is easy to read off the eigenvalues and eigenvectors.</span></span> <span data-ttu-id="f008e-120">Bei den eigen Werten handelt es sich um alle Zahlen, die auf der Diagonal angezeigt werden, und ihre jeweiligen Eigenvektoren sind die Einheits Vektoren, bei denen ein Eintrag gleich $1 $ und die restlichen Einträge gleich $0 sind $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-120">The eigenvalues are all the numbers appearing on the diagonal, and their respective eigenvectors are the unit vectors with one entry equal to $1$ and the remaining entries equal to $0$.</span></span>

<span data-ttu-id="f008e-121">Beachten Sie im obigen Beispiel, dass die Eigenvektoren von $D $ eine Grundlage für $3 $ -dimensionale Vektoren bilden.</span><span class="sxs-lookup"><span data-stu-id="f008e-121">Note in the above example that the eigenvectors of $D$ form a basis for $3$-dimensional vectors.</span></span> <span data-ttu-id="f008e-122">Eine Basis ist ein Satz von Vektoren, sodass jeder Vektor als lineare Kombination von Ihnen geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="f008e-122">A basis is a set of vectors such that any vector can be written as a linear combination of them.</span></span> <span data-ttu-id="f008e-123">Die expliziten $v _1 $ , $v _2 $ und $v _3 $ bilden eine Grundlage, wenn ein Vektor $v $ als $v = A_1 V_1 + a_2 V_2 + a_3 V_3 $a $a $ _1 $ , $a _2 $ und _3 geschrieben werden kann $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-123">More explicitly, $v_1$, $v_2$, and $v_3$ form a basis if any vector $v$ can be written as $v=a_1 v_1 + a_2 v_2 + a_3 v_3$ for some numbers $a_1$, $a_2$, and $a_3$.</span></span>

<span data-ttu-id="f008e-124">Beachten Sie, dass eine hermitische Matrix (auch als selbst Adjoint bezeichnet) eine komplexe quadratische Matrix ist, die mit ihrer eigenen komplexen konjugierung identisch ist, während eine einheitliche Matrix eine komplexe Quadrat Matrix ist, deren Umkehrung gleich der komplexen konjugierung ist.</span><span class="sxs-lookup"><span data-stu-id="f008e-124">Recall that a Hermitian matrix (also called self-adjoint) is a complex square matrix equal to its own complex conjugate, while a unitary matrix is a complex square matrix whose inverse is equal to its complex conjugate.</span></span>
<span data-ttu-id="f008e-125">Bei hermischen und einheitlichen Matrizen, bei denen es sich im Wesentlichen um die einzigen Matrizen in Quantum Computing handelt, gibt es ein allgemeines Ergebnis, das als " [*Spectral Theorem*](https://en.wikipedia.org/wiki/Spectral_theorem)" bezeichnet wird, das Folgendes bestätigt: für jede hermitische oder einheitliche Matrix $M gibt $ es eine einheitliche $U, $ sodass $M = U ^ \dagger D U $ für einige diagonal Matrix $D $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-125">For Hermitian and unitary matrices, which are essentially the only matrices encountered in quantum computing, there is a general result known as the [*spectral theorem*](https://en.wikipedia.org/wiki/Spectral_theorem), which asserts the following: For any Hermitian or unitary matrix $M$, there exists a unitary $U$ such that $M=U^\dagger D U$ for some diagonal matrix $D$.</span></span> <span data-ttu-id="f008e-126">Außerdem sind die diagonalen Einträge von $D $ die Eigenwerte $M $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-126">Furthermore, the diagonal entries of $D$ will be the eigenvalues of $M$.</span></span>

<span data-ttu-id="f008e-127">Wir wissen bereits, wie die Eigenwerte und Eigenvektoren einer Diagonalen Matrix $D berechnet werden $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-127">We already know how to compute the eigenvalues and eigenvectors of a diagonal matrix $D$.</span></span> <span data-ttu-id="f008e-128">Bei Verwendung dieses Theorem wissen wir, dass $ $ $ $ $U ^ \dagger v ein eigenständiger Vektor von $ $M $ mit einem eigen Wert $c $ ist, wenn $v ein $D eigen Wert $c ist, d. h. $DV = CV.</span><span class="sxs-lookup"><span data-stu-id="f008e-128">Using this theorem we know that if $v$ is an eigenvector of $D$ with eigenvalue $c$, i.e., $Dv = cv$, then $U^\dagger v$ will be an eigenvector of $M$ with eigenvalue $c$.</span></span> <span data-ttu-id="f008e-129">Dies liegt daran, dass</span><span class="sxs-lookup"><span data-stu-id="f008e-129">This is because</span></span>

<span data-ttu-id="f008e-130">$ $M (u ^ \dagger v) = u ^ \dagger d U (U ^ \dagger v) = u ^ \dagger D (u u ^ \dagger) v = u ^ \dagger d v = c U ^ \dagger v. $ $</span><span class="sxs-lookup"><span data-stu-id="f008e-130">$$M(U^\dagger v) = U^\dagger D U  (U^\dagger v) =U^\dagger D (U  U^\dagger) v = U^\dagger D v = c U^\dagger v.$$</span></span>

## <a name="matrix-exponentials"></a><span data-ttu-id="f008e-131">Matrix exponentiale</span><span class="sxs-lookup"><span data-stu-id="f008e-131">Matrix Exponentials</span></span>
<span data-ttu-id="f008e-132">Eine [*Matrix Exponentialwert*](https://en.wikipedia.org/wiki/Matrix_exponential) kann auch exakt mit der Exponentialfunktion definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f008e-132">A [*matrix exponential*](https://en.wikipedia.org/wiki/Matrix_exponential) can also be defined in exact analogy to the exponential function.</span></span>  <span data-ttu-id="f008e-133">Das exponentielle Matrix einer Matrix $A $ kann als</span><span class="sxs-lookup"><span data-stu-id="f008e-133">The matrix exponential of a matrix $A$ can be expressed as</span></span>

<span data-ttu-id="f008e-134">$ $ e ^ A = \boldone + A + \bruchteil {a ^ 2 } {2!} + \bruchteil {a ^ 3 } {3!} + \cdots $ $</span><span class="sxs-lookup"><span data-stu-id="f008e-134">$$ e^A=\boldone + A + \frac{A^2}{2!}+\frac{A^3}{3!}+\cdots $$</span></span>

<span data-ttu-id="f008e-135">Dies ist wichtig, da die Evolution für die Quantum-mechanische Zeit durch eine einheitliche Matrix der Form $e ^ {IB } $ für hermitian Matrix $B beschrieben wird $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-135">This is important because quantum mechanical time evolution is described by a unitary matrix of the form $e^{iB}$ for Hermitian matrix $B$.</span></span>  <span data-ttu-id="f008e-136">Aus diesem Grund ist das Durchführen von Matrix Exponentialzahlen ein wesentlicher Bestandteil von Quantum Computing, da f # systeminterne Routinen zum Beschreiben dieser Vorgänge bietet.</span><span class="sxs-lookup"><span data-stu-id="f008e-136">For this reason, performing matrix exponentials is a fundamental part of quantum computing and as such Q# offers intrinsic routines for describing these operations.</span></span>
<span data-ttu-id="f008e-137">In der Praxis gibt es viele Möglichkeiten, eine Matrix auf einem klassischen Computer exponentiell zu berechnen, und in der Regel wird eine solche exponentialweise mit der Peril in Bezug gesetzt.</span><span class="sxs-lookup"><span data-stu-id="f008e-137">There are many ways in practice to compute a matrix exponential on a classical computer, and in general numerically approximating such an exponential is fraught with peril.</span></span>  <span data-ttu-id="f008e-138">Weitere Informationen finden Sie unter [*Cleve Moler und Charles Van Loan. "Neun zweifelhafte Möglichkeiten, den Exponentialwert einer Matrix zu berechnen." Siam Review 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) , um weitere Informationen zu den beteiligten Problemen zu finden.</span><span class="sxs-lookup"><span data-stu-id="f008e-138">See [*Cleve Moler and Charles Van Loan. "Nineteen dubious ways to compute the exponential of a matrix." SIAM review 20.4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) for more information about the challenges involved.</span></span>

<span data-ttu-id="f008e-139">Die einfachste Möglichkeit, um zu verstehen, wie die exponentielle einer Matrix berechnet werden kann, ist die Eigenwerte und Eigenvektoren dieser Matrix.</span><span class="sxs-lookup"><span data-stu-id="f008e-139">The easiest way to understand how to compute the exponential of a matrix is through the eigenvalues and eigenvectors of that matrix.</span></span>  <span data-ttu-id="f008e-140">Insbesondere das oben beschriebene Spektral Theorem besagt, dass für jede hermitische oder einheitliche Matrix $A $ eine einheitliche Matrix $U $ und eine diagonale Matrix $D $ , dass $A = U ^ \dagger D U ist $ .  Aufgrund der Eigenschaften von Unitarity haben wir diese $A ^ 2 = u ^ \dagger d ^ 2 U $ und ebenso für alle Power $p $ $A ^ p = u ^ \dagger d ^ p u $ .  Wenn wir dies in die Operator Definition des Operator exponentiell ersetzen, erhalten wir Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f008e-140">Specifically, the spectral theorem discussed above says that for every Hermitian or unitary matrix $A$ there exists a unitary matrix $U$ and a diagonal matrix $D$ such that $A=U^\dagger D U$.  Because of the properties of unitarity we have that $A^2 = U^\dagger D^2 U$ and similarly for any power $p$ $A^p = U^\dagger D^p U$.  If we substitute this into the operator definition of the operator exponential we obtain:</span></span>

<span data-ttu-id="f008e-141">$ $ e ^ A = U ^ \dagger \left (\boldone + D + \bruchteil {d ^ 2 } {2!} + \cdots \right) U = u ^ \dagger \begin{ bmatrix } \exp (D_ {11 } ) & 0 & \cdots &0 \\\\ 0 & \exp (D_ {22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0&0 & \cdots & \exp (D_ {NN } ) \end{ bmatrix } U. $ $</span><span class="sxs-lookup"><span data-stu-id="f008e-141">$$ e^A= U^\dagger \left(\boldone +D +\frac{D^2}{2!}+\cdots \right)U= U^\dagger \begin{bmatrix}\exp(D_{11}) & 0 &\cdots &0\\\\ 0 & \exp(D_{22})&\cdots& 0\\\\ \vdots &\vdots &\ddots &\vdots\\\\ 0&0&\cdots&\exp(D_{NN}) \end{bmatrix} U. $$</span></span>

<span data-ttu-id="f008e-142">Anders ausgedrückt: Wenn Sie in die eigenständige Matrix der Matrix umwandeln $A $ dann entspricht das Berechnen der Matrix exponentiell dem Berechnen des normalen exponentiellen Werts der Eigenwerte der Matrix.</span><span class="sxs-lookup"><span data-stu-id="f008e-142">In other words, if you transform to the eigenbasis of the matrix $A$ then computing the matrix exponential is equivalent to computing the ordinary exponential of the eigenvalues of the matrix.</span></span>  <span data-ttu-id="f008e-143">Wie viele Vorgänge in Quantum Computing das Durchführen von Matrix Exponentialzahlen umfassen, wird dieser Trick der Transformation in die eigenständige Basis einer Matrix, um die Ausführung des Operator exponentialmäßig zu vereinfachen, häufig angezeigt und ist die Grundlage für viele Quantum-Algorithmen, wie z. b. Trotter – Quantum-Simulationsmethoden, die später in diesem Handbuch</span><span class="sxs-lookup"><span data-stu-id="f008e-143">As many operations in quantum computing involve performing matrix exponentials, this trick of transforming into the eigenbasis of a matrix to simplify performing the operator exponential appears frequently and is the basis behind many quantum algorithms such as Trotter–Suzuki-style quantum simulation methods discussed later in this guide.</span></span>

<span data-ttu-id="f008e-144">Eine weitere nützliche Eigenschaft ist, wenn $B $ sowohl einheitlich als auch hermitian ist, d. h. $B = b ^ {-1 } = b ^ \dagger, $ dann $B ^ 2 = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="f008e-144">Another useful property is if $B$ is both unitary and Hermitian, i.e., $B=B^{-1}=B^\dagger$ then $B^2=\boldone$.</span></span> <span data-ttu-id="f008e-145">Durch Anwenden dieser Regel auf die oben genannte Erweiterung der Matrix und durch Gruppierung der $ \boldone $ -und $B $ Begriffe werden die Werte für jeden echten Wert $x $ der Identität angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f008e-145">By applying this rule to the above expansion of the matrix exponential and by grouping the $\boldone$ and the $B$ terms together, it can be see that for any real value $x$ the identity</span></span>

<span data-ttu-id="f008e-146">$ $e ^ {IBX } = \boldone \cos (x) + ib\sin (x) $ $</span><span class="sxs-lookup"><span data-stu-id="f008e-146">$$e^{iBx}=\boldone \cos(x)+ iB\sin(x)$$</span></span>


<span data-ttu-id="f008e-147">bestand.</span><span class="sxs-lookup"><span data-stu-id="f008e-147">holds.</span></span> <span data-ttu-id="f008e-148">Dieser Trick ist besonders nützlich, da er es in Bezug auf die in den Aktionen vorhandenen Aktions Matrix gibt, selbst wenn die Dimension von $B $ exponentiell groß ist, für den Sonderfall, wenn $B $ sowohl einheitlich als auch hermitian ist.</span><span class="sxs-lookup"><span data-stu-id="f008e-148">This trick is especially useful because it allows to reason about the actions matrix exponentials have, even if the dimension of $B$ is exponentially large, for the special case when $B$ is both unitary and Hermitian.</span></span>
