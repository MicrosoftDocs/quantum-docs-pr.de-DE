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
# <a name="vectors-and-matrices"></a><span data-ttu-id="27ee8-103">Vektoren und Matrizen</span><span class="sxs-lookup"><span data-stu-id="27ee8-103">Vectors and Matrices</span></span>

<span data-ttu-id="27ee8-104">Eine Vertrautheit mit Vektoren und Matrizen ist für das Verständnis von Quantum Computing von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="27ee8-104">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="27ee8-105">Im folgenden finden Sie eine kurze Einführung, und interessierte Leser werden empfohlen, einen Standard Verweis auf lineare Algebra zu lesen, z. b. für die Tabelle *, G. (1993). Einführung in lineare Algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* oder eine Online Referenz, wie z. b. [lineare Algebra](http://joshua.smcvt.edu/linearalgebra/).</span><span class="sxs-lookup"><span data-stu-id="27ee8-105">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="27ee8-106">Ein Spalten Vektor (oder ein einfaches [*Vektor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v $ der Dimension (oder Größe) $n $ eine Auflistung $n $ komplexer Zahlen $ (V_1, V_2, \ldots, v_n) $ ist, die als Spalte angeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="27ee8-106">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="27ee8-107">$ $v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-107">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-108">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-108">v_1\\\\</span></span>
<span data-ttu-id="27ee8-109">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-109">v_2\\\\</span></span>
<span data-ttu-id="27ee8-110">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-110">\vdots\\\\</span></span>
<span data-ttu-id="27ee8-111">v_n \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="27ee8-111">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="27ee8-112">Die Norm eines Vektor $v $ wird als $ \sqrt { \sum \_ i | v \_ i | ^ 2 $ definiert } .</span><span class="sxs-lookup"><span data-stu-id="27ee8-112">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="27ee8-113">Ein Vektor wird als Einheits Norm bezeichnet (oder alternativ als [*Einheits Vektor*](https://en.wikipedia.org/wiki/Unit_vector)bezeichnet), wenn seine Norm $1 ist $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-113">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="27ee8-114">Das [*Adjoint eines Vektor*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v $ wird $v ^ \dagger bezeichnet und als $ folgender Zeilen Vektor definiert, wobei $ \* $ die komplexe konjugierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="27ee8-114">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="27ee8-115">$ $ \begin{ bmatrix } V_1 \\ \\ \vdots \\ \\ v_n \end{ bmatrix } ^ \dagger = \begin{ bmatrix } V_1 ^ \* & \cdots & v_n ^ \* \end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="27ee8-115">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="27ee8-116">Die gängigste Methode, zwei Vektoren zu multiplizieren, ist das [*innere Produkt*](https://en.wikipedia.org/wiki/Inner_product_space), das auch als "Punktprodukt" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="27ee8-116">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="27ee8-117">Das innere Produkt liefert die Projektion eines Vektors auf einen anderen und ist äußerst nützlich, um zu beschreiben, wie ein Vektor als Summe aus anderen einfacheren Vektoren ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="27ee8-117">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="27ee8-118">Das innere Produkt zwischen $u $ und $v $ , angegeben als "$ \left \langle u", v \right \rangle $ ist definiert als</span><span class="sxs-lookup"><span data-stu-id="27ee8-118">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

<span data-ttu-id="27ee8-119">$ $ \langle u, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } V_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="27ee8-119">$$ \langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="27ee8-120">Diese Notation ermöglicht außerdem, dass die Norm eines Vector-$v $ als $ \sqrt { \langle v, v $ geschrieben wird \rangle } .</span><span class="sxs-lookup"><span data-stu-id="27ee8-120">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="27ee8-121">Ein Vektor kann mit einer Zahl $c multipliziert $ werden, um einen neuen Vektor zu bilden, dessen Einträge mit $c multipliziert werden $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-121">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="27ee8-122">Wir können auch zwei Vektoren $u $ und $v hinzufügen $ , um einen neuen Vektor zu bilden, dessen Einträge die Summe der Einträge von $u $ und $v sind $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-122">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="27ee8-123">Diese Vorgänge werden im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="27ee8-123">These operations are depicted below:</span></span>

<span data-ttu-id="27ee8-124">$ $ \mathrm{if } ~ u = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-124">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-125">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-125">u_1\\\\</span></span>
<span data-ttu-id="27ee8-126">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-126">u_2\\\\</span></span>
<span data-ttu-id="27ee8-127">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-127">\vdots\\\\</span></span>
<span data-ttu-id="27ee8-128">u_n \end{ bmatrix } ~ \mathrm{und } ~ v = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-128">u_n \end{bmatrix}~\mathrm{and}~ v =\begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-129">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-129">v_1\\\\</span></span>
    <span data-ttu-id="27ee8-130">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-130">v_2\\\\</span></span>
    <span data-ttu-id="27ee8-131">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-131">\vdots\\\\</span></span>
    <span data-ttu-id="27ee8-132">v_n \end{ bmatrix } , ~ \mathrm{then } ~ au + BV = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-132">v_n \end{bmatrix},~\mathrm{then}~ au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-133">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-133">au_1+bv_1\\\\</span></span>
<span data-ttu-id="27ee8-134">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-134">au_2+bv_2\\\\</span></span>
<span data-ttu-id="27ee8-135">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-135">\vdots\\\\</span></span>
<span data-ttu-id="27ee8-136">au_n + bv_n \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="27ee8-136">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="27ee8-137">Eine [*Matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) der Größe $m \times n $ ist eine Auflistung von $MN $ komplexen Zahlen, die in $m $ Zeilen und $n Spalten angeordnet sind, $ wie unten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="27ee8-137">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="27ee8-138">$ $M = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-138">$$M = \begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-139">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2N } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-139">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="27ee8-140">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {MN } \\ \\ \end{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="27ee8-140">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\ \end{bmatrix}.$$</span></span>

<span data-ttu-id="27ee8-141">Beachten Sie, dass es sich bei einem Vektor mit Dimensions $n $ einfach um eine Matrix der Größe handelt $n \times 1 $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-141">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="27ee8-142">Wie bei Vektoren können wir eine Matrix mit einer Zahl $c multiplizieren, $ um eine neue Matrix zu erhalten, in der jeder Eintrag mit $c multipliziert ist $ , und wir können zwei Matrizen derselben Größe hinzufügen, um eine neue Matrix zu generieren, deren Einträge die Summe der entsprechenden Einträge der beiden Matrizen sind.</span><span class="sxs-lookup"><span data-stu-id="27ee8-142">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="27ee8-143">Matrix Multiplikation und Tensor-Produkte</span><span class="sxs-lookup"><span data-stu-id="27ee8-143">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="27ee8-144">Wir können auch zwei Matrizen $M $ der Dimension $m \times n $ und $N $ der Dimension $n \time p multiplizieren $ , um wie folgt eine neue Matrix $P $ der Dimension $m "\time p" zu erhalten $ :</span><span class="sxs-lookup"><span data-stu-id="27ee8-144">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

<span data-ttu-id="27ee8-145">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="27ee8-145">\begin{align}</span></span>
<span data-ttu-id="27ee8-146">& \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-146">&\begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-147">M_ {11 } ~ ~ M_ {12 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ M_ {21 } ~ ~ M_ {22 } ~ ~ \cdots ~ ~ M_ {2N } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-147">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\ M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\ \ddots\\\\</span></span>
    <span data-ttu-id="27ee8-148">M_ {M1 } ~ ~ M_ {m2 } ~ ~ \cdots ~ ~ M_ {MN}</span><span class="sxs-lookup"><span data-stu-id="27ee8-148">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
<span data-ttu-id="27ee8-149">Schließlichbmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-149">\end{bmatrix}</span></span>
<span data-ttu-id="27ee8-150">beginnenbmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-150">\begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-151">N_ {11 } ~ ~ N_ {12 } ~ ~ \cdots ~ ~ N_ {1P } \\ \\ N_ {21 } ~ ~ N_ {22 } ~ ~ \cdots ~ ~ N_ {2P } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-151">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\ N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="27ee8-152">N_ {N1 } ~ ~ N_ {N2 } ~ ~ \cdots ~ ~ N_ {NP}</span><span class="sxs-lookup"><span data-stu-id="27ee8-152">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
<span data-ttu-id="27ee8-153">\end{ bmatrix } = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-153">\end{bmatrix}=\begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-154">P_ {11 } ~ ~ P_ {12 } ~ ~ \cdots ~ ~ P_ {1P } \\ \\ P_ {21 } ~ ~ P_ {22 } ~ ~ \cdots ~ ~ P_ {2P } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-154">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\ P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\ \ddots\\\\</span></span>
<span data-ttu-id="27ee8-155">P_ {M1 } ~ ~ P_ {m2 } ~ ~ \cdots ~ ~ P_ {MP}</span><span class="sxs-lookup"><span data-stu-id="27ee8-155">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
<span data-ttu-id="27ee8-156">Schließlichbmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-156">\end{bmatrix}</span></span>
<span data-ttu-id="27ee8-157">\end{align}</span><span class="sxs-lookup"><span data-stu-id="27ee8-157">\end{align}</span></span>

<span data-ttu-id="27ee8-158">Wenn die Einträge $P $ $P _ {IK } = \ sum_j M_ {IJ} N_ {JK } $.</span><span class="sxs-lookup"><span data-stu-id="27ee8-158">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="27ee8-159">Der Eintrag $P _ {11 } $ ist beispielsweise das innere Produkt der ersten Zeile $M $ mit der ersten Spalte $N $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-159">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$.</span></span> <span data-ttu-id="27ee8-160">Beachten Sie, dass sich diese Definition auf die Matrix Vektor Multiplikation erstreckt, da ein Vektor einfach ein Sonderfall einer Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="27ee8-160">Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="27ee8-161">Alle Matrizen, die wir in Erwägung haben, sind entweder quadratische Matrizen, bei denen die Anzahl der Zeilen und Spalten gleich ist, oder Vektoren, die nur $1- $ Spalten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="27ee8-161">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="27ee8-162">Eine spezielle quadratische Matrix ist die [*Identitätsmatrix*](https://en.wikipedia.org/wiki/Identity_matrix), die "$ \boldone" bezeichnet $ , die alle diagonal Elemente gleich $1 $ und die restlichen Elemente gleich $0 sind $ :</span><span class="sxs-lookup"><span data-stu-id="27ee8-162">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

<span data-ttu-id="27ee8-163">$ $ \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-163">$$\boldone=\begin{bmatrix}</span></span>
<span data-ttu-id="27ee8-164">1 ~ ~ 0 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-164">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="27ee8-165">0 ~ ~ 1 ~ ~ \cdots ~ ~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-165">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="27ee8-166">~ ~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-166">~~ \ddots\\\\</span></span>
<span data-ttu-id="27ee8-167">0 ~ ~ 0 ~ ~ \cdots ~ ~ 1 \end{ bmatrix } . $ $</span><span class="sxs-lookup"><span data-stu-id="27ee8-167">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="27ee8-168">Für eine quadratische Matrix $A $ sagen wir, dass eine Matrix $B $ Ihre [*Umkehrung*](https://en.wikipedia.org/wiki/Invertible_matrix) ist, wenn $ab = BA = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-168">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="27ee8-169">Die Umkehrung einer Matrix muss nicht vorhanden sein. Wenn Sie jedoch vorhanden ist, ist sie eindeutig, und wir bezeichnen Sie $A ^ {-1 } $.</span><span class="sxs-lookup"><span data-stu-id="27ee8-169">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="27ee8-170">Bei allen Matrizen $M $ ist die Adjoint-oder konjugierte $M $ eine Matrix $N, die $ $N _ {IJ } = M_ {JI } ^ \* $ ist.</span><span class="sxs-lookup"><span data-stu-id="27ee8-170">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="27ee8-171">Das Adjoint von $M $ wird normalerweise $M ^ \dagger bezeichnet $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-171">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="27ee8-172">Wir sagen, dass eine Matrix $U $ [*einheitlich*](https://en.wikipedia.org/wiki/Unitary_matrix) ist, wenn $UU ^ \dagger = u ^ \dagger U = \boldone $ oder gleichwertig $U ^ {-1 } = u ^ \dagger ist $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-172">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="27ee8-173">Die wichtigste Eigenschaft der einheitlichen Matrizen ist, dass Sie die Norm eines Vektors erhalten.</span><span class="sxs-lookup"><span data-stu-id="27ee8-173">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="27ee8-174">Dies liegt daran, dass</span><span class="sxs-lookup"><span data-stu-id="27ee8-174">This happens because</span></span> 

<span data-ttu-id="27ee8-175">$ $ \langle v, v \rangle = v ^ \dagger v = v ^ \dagger u ^ {-1 } U v = v ^ \dagger u ^ \dagger u v = \langle u v, u v \rangle . $ $</span><span class="sxs-lookup"><span data-stu-id="27ee8-175">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="27ee8-176">Eine Matrix $M als $ [*hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) bezeichnet, wenn $M = M ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="27ee8-176">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="27ee8-177">Zum Schluss ist das [*tensorflow-Produkt*](https://en.wikipedia.org/wiki/Tensor_product) (oder Kronecker-Produkt) mit zwei Matrizen $M $ der Größe $m \times n $ und $N $ der Größe $p \times q $ eine größere Matrix $P = M \otimes n $ der Größe $MP \times NQ " $ und wird von $M $ und $N $ wie folgt abgerufen:</span><span class="sxs-lookup"><span data-stu-id="27ee8-177">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

<span data-ttu-id="27ee8-178">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="27ee8-178">\begin{align}</span></span>
    <span data-ttu-id="27ee8-179">M \otimes N &= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-179">M \otimes N &= \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-180">M_ {11 } ~ ~ \cdots ~ ~ M_ {1N } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-180">M_{11} ~~ \cdots ~~ M_{1n} \\\\ \ddots\\\\</span></span>
        <span data-ttu-id="27ee8-181">M_ {M1 } ~ ~ \cdots ~ ~ M_ {MN}</span><span class="sxs-lookup"><span data-stu-id="27ee8-181">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    <span data-ttu-id="27ee8-182">Schließlichbmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-182">\end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-183">\otimes \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-183">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-184">N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-184">N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="27ee8-185">N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ}</span><span class="sxs-lookup"><span data-stu-id="27ee8-185">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    <span data-ttu-id="27ee8-186">\end{ bmatrix } \\ \\ &= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-186">\end{bmatrix}\\\\ &= \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-187">M_ {11 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{ bmatrix } ~ ~ \cdots ~ ~ M_ {1N } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{ bmatrix } \\ \\ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="27ee8-187">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\ \ddots\\\\</span></span>
        <span data-ttu-id="27ee8-188">M_ {M1 } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{ bmatrix } ~ ~ \cpunkte ~ ~ M_ {MN } \begin{ bmatrix } N_ {11 } ~ ~ \cdots ~ ~ N_ {1Q } \\ \\ \ddots \\\\ N_ {P1 } ~ ~ \cdots ~ ~ N_ {PQ } \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-188">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~ M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-189">\end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="27ee8-189">\end{bmatrix}.</span></span>
<span data-ttu-id="27ee8-190">\end{align}</span><span class="sxs-lookup"><span data-stu-id="27ee8-190">\end{align}</span></span>

<span data-ttu-id="27ee8-191">Dies wird in einigen Beispielen besser veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="27ee8-191">This is better demonstrated with some examples:</span></span>

<span data-ttu-id="27ee8-192">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-192">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-193">a \\ \\ b \end{ bmatrix } \otimes \begin{ bmatrix } c \\ \\ d \\ \\ e \end{ bmatrix } = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-193">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} = \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-194">a \begin{ bmatrix } c \\ \\ d \\ \\ e \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-194">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="27ee8-195">\\\\[1.5 em] b \begin{ bmatrix } c \\ \\ d \\ \\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-195">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-196">Schließlichbmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-196">\end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-197">= \begin{ bmatrix } a c \\ \\ a d \\ \\ a e \\ \\ b c \\ \\ b d \\ \\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-197">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="27ee8-198">und</span><span class="sxs-lookup"><span data-stu-id="27ee8-198">and</span></span>

<span data-ttu-id="27ee8-199">$ $ \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-199">$$ \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-200">a \ b \\ \\ c \ d \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-200">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-201">\otimes \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-201">\otimes \begin{bmatrix}</span></span>
        <span data-ttu-id="27ee8-202">e \ f \\ \\ \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-202">e\ f\\\\g\ h \end{bmatrix}</span></span>
     <span data-ttu-id="27ee8-203">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-203">= \begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-204">ein\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-204">a\begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-205">e \ f \\\\ \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-205">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-206">b\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-206">b\begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-207">e \ f \\\\ \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-207">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-208">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-208">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-209">e \ f \\\\ \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-209">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-210">d\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-210">d\begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-211">e \ f \\\\ \ h \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-211">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-212">Schließlichbmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-212">\end{bmatrix}</span></span>
    <span data-ttu-id="27ee8-213">= \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="27ee8-213">= \begin{bmatrix}</span></span>
    <span data-ttu-id="27ee8-214">AE \ AF \ be \ BF \\ \\ AG \ AH \ BG \ BH \\ \\ CE \ CF \ de \ DF \\ \\ CG \ ch \ DG \ dh \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="27ee8-214">ae\ af\ be\ bf \\\\ ag\ ah\ bg\ bh \\\\ ce\ cf\ de\ df \\\\ cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="27ee8-215">Eine abschließende, nützliche, in Bezug auf die tensorflow-Produkte für alle Vektor $v $ oder Matrix $M $ $v ^ {\otimes n } $ oder $M ^ {\otimes n } $ ist für ein $n $ wiederholten tensorflow-Produkt eine kurze Hand.</span><span class="sxs-lookup"><span data-stu-id="27ee8-215">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="27ee8-216">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="27ee8-216">For example:</span></span>

<span data-ttu-id="27ee8-217">\begin{align}</span><span class="sxs-lookup"><span data-stu-id="27ee8-217">\begin{align}</span></span>
<span data-ttu-id="27ee8-218">& \begin{ bmatrix } 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 1 \\ \\ 0 \ End{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ 0 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ 0 0 \\ \\ \\ \\ 0 \ End{ bmatrix } , \qquad \begin{bmatrix} 1 \\ \\ -1 \end{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 1 \\ \\ -1 \\ \\ -1 \\ \\ 1 \ End{ bmatrix } , \\ \\ & \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } ^ {\otimes 1 } = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } , \qquad \begin{bmatrix} 0 & 1 \\ \\ 1 & 0 \ End{ bmatrix } ^ {\otimes 2 } = \begin{ bmatrix } 0 #b4 0&0&1 \\ \\ 0 &0&1&0 \\ \\ 0 &1&0&0 \\\\ 1 &0&0&0 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="27ee8-218">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\ &\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}    0& 1 \\\\ 1& 0  \end{bmatrix},  \qquad\begin{bmatrix} 0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
<span data-ttu-id="27ee8-219">\end{align}</span><span class="sxs-lookup"><span data-stu-id="27ee8-219">\end{align}</span></span>
