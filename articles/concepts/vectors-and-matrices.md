---
<span data-ttu-id="3ed1b-101">Title: Vektoren und Matrizen in Quantum Computing Description: Erlernen Sie die Grundlagen der Arbeit mit Vektoren und Matrizen.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-101">title: Vectors and matrices in quantum computing description: Learn the basics of how to work with vectors and matrices.</span></span>
<span data-ttu-id="3ed1b-102">Autor: quantumwriter UID: Microsoft. Quantum. Concepts. Vectors ms. Author: nawiebe@microsoft.com ms. Date: 12/11/2017 ms. Topic: article NO-LOC:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-102">author: QuantumWriter uid: microsoft.quantum.concepts.vectors ms.author: nawiebe@microsoft.com ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="3ed1b-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-103">"Q#"</span></span>
- <span data-ttu-id="3ed1b-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-104">"$$v"</span></span>
- <span data-ttu-id="3ed1b-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-105">"$$"</span></span>
- <span data-ttu-id="3ed1b-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-106">"$$"</span></span>
- <span data-ttu-id="3ed1b-107">"$"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-107">"$"</span></span>
- <span data-ttu-id="3ed1b-108">"$"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-108">"$"</span></span>
- <span data-ttu-id="3ed1b-109">"$"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-109">"$"</span></span>
- <span data-ttu-id="3ed1b-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-110">"$$"</span></span>
- <span data-ttu-id="3ed1b-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-111">"\cdots"</span></span>
- <span data-ttu-id="3ed1b-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-112">"bmatrix"</span></span>
- <span data-ttu-id="3ed1b-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-113">"\ddots"</span></span>
- <span data-ttu-id="3ed1b-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-114">"\equiv"</span></span>
- <span data-ttu-id="3ed1b-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-115">"\sum"</span></span>
- <span data-ttu-id="3ed1b-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-116">"\begin"</span></span>
- <span data-ttu-id="3ed1b-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-117">"\end"</span></span>
- <span data-ttu-id="3ed1b-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-118">"\sqrt"</span></span>
- <span data-ttu-id="3ed1b-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-119">"\otimes"</span></span>
- <span data-ttu-id="3ed1b-120">"{"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-120">"{"</span></span>
- <span data-ttu-id="3ed1b-121">"}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-121">"}"</span></span>
- <span data-ttu-id="3ed1b-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-122">"\text"</span></span>
- <span data-ttu-id="3ed1b-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-123">"\phi"</span></span>
- <span data-ttu-id="3ed1b-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-124">"\kappa"</span></span>
- <span data-ttu-id="3ed1b-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-125">"\psi"</span></span>
- <span data-ttu-id="3ed1b-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-126">"\alpha"</span></span>
- <span data-ttu-id="3ed1b-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-127">"\beta"</span></span>
- <span data-ttu-id="3ed1b-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-128">"\gamma"</span></span>
- <span data-ttu-id="3ed1b-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-129">"\delta"</span></span>
- <span data-ttu-id="3ed1b-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-130">"\omega"</span></span>
- <span data-ttu-id="3ed1b-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-131">"\bra"</span></span>
- <span data-ttu-id="3ed1b-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-132">"\ket"</span></span>
- <span data-ttu-id="3ed1b-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-133">"\boldone"</span></span>
- <span data-ttu-id="3ed1b-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-134">"\\\\"</span></span>
- <span data-ttu-id="3ed1b-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-135">"\\"</span></span>
- <span data-ttu-id="3ed1b-136">"="</span><span class="sxs-lookup"><span data-stu-id="3ed1b-136">"="</span></span>
- <span data-ttu-id="3ed1b-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-137">"\frac"</span></span>
- <span data-ttu-id="3ed1b-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-138">"\text"</span></span>
- <span data-ttu-id="3ed1b-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-139">"\mapsto"</span></span>
- <span data-ttu-id="3ed1b-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-140">"\dagger"</span></span>
- <span data-ttu-id="3ed1b-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-141">"\to"</span></span>
- <span data-ttu-id="3ed1b-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-142">"\begin{cases}"</span></span>
- <span data-ttu-id="3ed1b-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-143">"\end{cases}"</span></span>
- <span data-ttu-id="3ed1b-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-144">"\operatorname"</span></span>
- <span data-ttu-id="3ed1b-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-145">"\braket"</span></span>
- <span data-ttu-id="3ed1b-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-146">"\id"</span></span>
- <span data-ttu-id="3ed1b-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-147">"\expect"</span></span>
- <span data-ttu-id="3ed1b-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-148">"\defeq"</span></span>
- <span data-ttu-id="3ed1b-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-149">"\variance"</span></span>
- <span data-ttu-id="3ed1b-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-150">"\dd"</span></span>
- <span data-ttu-id="3ed1b-151">"&"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-151">"&"</span></span>
- <span data-ttu-id="3ed1b-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-152">"\begin{align}"</span></span>
- <span data-ttu-id="3ed1b-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-153">"\end{align}"</span></span>
- <span data-ttu-id="3ed1b-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-154">"\Lambda"</span></span>
- <span data-ttu-id="3ed1b-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-155">"\lambda"</span></span>
- <span data-ttu-id="3ed1b-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-156">"\Omega"</span></span>
- <span data-ttu-id="3ed1b-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-157">"\mathrm"</span></span>
- <span data-ttu-id="3ed1b-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-158">"\left"</span></span>
- <span data-ttu-id="3ed1b-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-159">"\right"</span></span>
- <span data-ttu-id="3ed1b-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-160">"\qquad"</span></span>
- <span data-ttu-id="3ed1b-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-161">"\times"</span></span>
- <span data-ttu-id="3ed1b-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-162">"\big"</span></span>
- <span data-ttu-id="3ed1b-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-163">"\langle"</span></span>
- <span data-ttu-id="3ed1b-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-164">"\rangle"</span></span>
- <span data-ttu-id="3ed1b-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-165">"\bigg"</span></span>
- <span data-ttu-id="3ed1b-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-166">"\Big"</span></span>
- <span data-ttu-id="3ed1b-167">"|"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-167">"|"</span></span>
- <span data-ttu-id="3ed1b-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-168">"\mathbb"</span></span>
- <span data-ttu-id="3ed1b-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-169">"\vec"</span></span>
- <span data-ttu-id="3ed1b-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-170">"\in"</span></span>
- <span data-ttu-id="3ed1b-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-171">"\texttt"</span></span>
- <span data-ttu-id="3ed1b-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-172">"\ne"</span></span>
- <span data-ttu-id="3ed1b-173">"<"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-173">"<"</span></span>
- <span data-ttu-id="3ed1b-174">">"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-174">">"</span></span>
- <span data-ttu-id="3ed1b-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-175">"\leq"</span></span>
- <span data-ttu-id="3ed1b-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-176">"\geq"</span></span>
- <span data-ttu-id="3ed1b-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-177">"~~"</span></span>
- <span data-ttu-id="3ed1b-178">"~"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-178">"~"</span></span>
- <span data-ttu-id="3ed1b-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="3ed1b-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="3ed1b-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="3ed1b-181">"\_"</span></span>

---

# <a name="vectors-and-matrices"></a><span data-ttu-id="3ed1b-182">Vektoren und Matrizen</span><span class="sxs-lookup"><span data-stu-id="3ed1b-182">Vectors and Matrices</span></span>

<span data-ttu-id="3ed1b-183">Eine Vertrautheit mit Vektoren und Matrizen ist für das Verständnis von Quantum Computing von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-183">Some familiarity with vectors and matrices is essential to understand quantum computing.</span></span> <span data-ttu-id="3ed1b-184">Im folgenden finden Sie eine kurze Einführung, und interessierte Leser werden empfohlen, einen Standard Verweis auf lineare Algebra zu lesen, z. b. für die Tabelle *, G. (1993). Einführung in lineare Algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* oder eine Online Referenz, wie z. b. [lineare Algebra](http://joshua.smcvt.edu/linearalgebra/).</span><span class="sxs-lookup"><span data-stu-id="3ed1b-184">We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as *Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press* or an online reference such as [Linear Algebra](http://joshua.smcvt.edu/linearalgebra/).</span></span>

<span data-ttu-id="3ed1b-185">Ein Spalten Vektor (oder einfach [*Vektor*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ $ der Dimension (oder Größe) $ n $ ist eine Auflistung von $ n $ komplexen Zahlen $ (V_1 V_2, \ldots, v_n), die $ als Spalte angeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-185">A column vector (or simply [*vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1,v_2,\ldots,v_n)$ arranged as a column:</span></span>

<span data-ttu-id="3ed1b-186">$$v =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-186">$$v =\begin{bmatrix}</span></span>
<span data-ttu-id="3ed1b-187">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-187">v_1\\\\</span></span>
<span data-ttu-id="3ed1b-188">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-188">v_2\\\\</span></span>
<span data-ttu-id="3ed1b-189">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-189">\vdots\\\\</span></span>
<span data-ttu-id="3ed1b-190">v_n\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="3ed1b-190">v_n \end{bmatrix}$$</span></span>

<span data-ttu-id="3ed1b-191">Die Norm eines Vector $ v $ ist als $ \sqrt { \sum \_ i | v \_ i | ^ 2 definiert } $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-191">The norm of a vector $v$ is defined as $\sqrt{\sum\_i |v\_i|^2}$.</span></span> <span data-ttu-id="3ed1b-192">Ein Vektor wird als Einheits Norm bezeichnet (oder auch als [*Einheits Vektor*](https://en.wikipedia.org/wiki/Unit_vector)bezeichnet), wenn seine Norm den Wert 1 hat $ $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-192">A vector is said to be of unit norm (or alternatively it is called a [*unit vector*](https://en.wikipedia.org/wiki/Unit_vector)) if its norm is $1$.</span></span> <span data-ttu-id="3ed1b-193">Das [*Adjoint eines Vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ wird als $ v ^ bezeichnet und als \dagger $ folgender Zeilen Vektor definiert $ \* $ , wobei die komplexe konjugierung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-193">The [*adjoint of a vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $v$ is denoted $v^\dagger$ and is defined to be the following row vector where $\*$ denotes the complex conjugate,</span></span>

<span data-ttu-id="3ed1b-194">$$\begin{bmatrix}V_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} V_1 ^ \* & \cdots & v_n ^ \*\end{bmatrix}$$</span><span class="sxs-lookup"><span data-stu-id="3ed1b-194">$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix}^\dagger = \begin{bmatrix}v_1^\* & \cdots & v_n^\* \end{bmatrix}$$</span></span>

<span data-ttu-id="3ed1b-195">Die gängigste Methode, zwei Vektoren zu multiplizieren, ist das [*innere Produkt*](https://en.wikipedia.org/wiki/Inner_product_space), das auch als "Punktprodukt" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-195">The most common way to multiply two vectors together is through the [*inner product*](https://en.wikipedia.org/wiki/Inner_product_space), also known as a dot product.</span></span>  <span data-ttu-id="3ed1b-196">Das innere Produkt liefert die Projektion eines Vektors auf einen anderen und ist äußerst nützlich, um zu beschreiben, wie ein Vektor als Summe aus anderen einfacheren Vektoren ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-196">The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.</span></span>  <span data-ttu-id="3ed1b-197">Das innere Produkt zwischen $ u $ und $ v $ , bezeichnet $ \left \langle u, v \right \rangle $ ist definiert als</span><span class="sxs-lookup"><span data-stu-id="3ed1b-197">The inner product between $u$ and $v$, denoted $\left\langle u, v\right\rangle$ is defined as</span></span>

$$
<span data-ttu-id="3ed1b-198">\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } V_1 + \cdots + u \_ n ^ { \* } v \_ n.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-198">\langle u, v\rangle = u^\dagger v=u\_1^{\*} v_1 + \cdots + u\_n^{\*} v\_n.</span></span>
$$

<span data-ttu-id="3ed1b-199">Diese Notation ermöglicht außerdem das Schreiben der Norm eines Vector $ v $ als $ \sqrt { \langle v, v \rangle } $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-199">This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.</span></span>

<span data-ttu-id="3ed1b-200">Wir können einen Vektor mit einer Zahl c multiplizieren $ $ , um einen neuen Vektor zu bilden, dessen Einträge mit c multipliziert werden $ $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-200">We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$.</span></span> <span data-ttu-id="3ed1b-201">Wir können auch zwei Vektoren $ u $ und v hinzufügen $ $ , um einen neuen Vektor zu bilden, dessen Einträge die Summe der Einträge von $ u $ und v sind $ $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-201">We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$.</span></span> <span data-ttu-id="3ed1b-202">Diese Vorgänge werden im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-202">These operations are depicted below:</span></span>

<span data-ttu-id="3ed1b-203">$$\mathrm{Wenn } ~ u=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-203">$$\mathrm{If}~u =\begin{bmatrix}</span></span>
<span data-ttu-id="3ed1b-204">u_1\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-204">u_1\\\\</span></span>
<span data-ttu-id="3ed1b-205">u_2\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-205">u_2\\\\</span></span>
<span data-ttu-id="3ed1b-206">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-206">\vdots\\\\</span></span>
<span data-ttu-id="3ed1b-207">u_n \end{bmatrix} ~ \mathrm { und}~</span><span class="sxs-lookup"><span data-stu-id="3ed1b-207">u_n \end{bmatrix}~\mathrm{and}~</span></span>
<span data-ttu-id="3ed1b-208">Ramelow=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-208">v =\begin{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-209">v_1\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-209">v_1\\\\</span></span>
    <span data-ttu-id="3ed1b-210">v_2\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-210">v_2\\\\</span></span>
    <span data-ttu-id="3ed1b-211">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-211">\vdots\\\\</span></span>
    <span data-ttu-id="3ed1b-212">v_n \end{bmatrix} , ~ \mathrm {}~</span><span class="sxs-lookup"><span data-stu-id="3ed1b-212">v_n \end{bmatrix},~\mathrm{then}~</span></span>
<span data-ttu-id="3ed1b-213">Au + BV=\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-213">au+bv =\begin{bmatrix}</span></span>
<span data-ttu-id="3ed1b-214">au_1 + bv_1\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-214">au_1+bv_1\\\\</span></span>
<span data-ttu-id="3ed1b-215">au_2 + bv_2\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-215">au_2+bv_2\\\\</span></span>
<span data-ttu-id="3ed1b-216">\vdots\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-216">\vdots\\\\</span></span>
<span data-ttu-id="3ed1b-217">au_n + bv_n \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-217">au_n+bv_n \end{bmatrix}.</span></span>
$$

<span data-ttu-id="3ed1b-218">Eine [*Matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) der Größe $ m \times n $ ist eine Auflistung von $ $ in Mio. Zeilen komplexen Zahlen, die in $ m $ Zeilen und n Spalten angeordnet sind, $ $ wie unten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-218">A [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:</span></span>

<span data-ttu-id="3ed1b-219">$$800=</span><span class="sxs-lookup"><span data-stu-id="3ed1b-219">$$M =</span></span> 
\begin{bmatrix}
<span data-ttu-id="3ed1b-220">M_ { 11 } ~~ m_ { 12 } ~~ \cdots ~~ m_ { 1N}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-220">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
<span data-ttu-id="3ed1b-221">M_ { 21 } ~~ m_ { 22 } ~~ \cdots ~~ m_ { 2N}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-221">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="3ed1b-222">M_ { M1 } ~~ m_ { m2 } ~~ \cdots ~~ m_ { MN}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-222">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\\\</span></span>
<span data-ttu-id="3ed1b-223">\end{bmatrix}.$$</span><span class="sxs-lookup"><span data-stu-id="3ed1b-223">\end{bmatrix}.$$</span></span>

<span data-ttu-id="3ed1b-224">Beachten Sie, dass es sich bei einem Vektor der Dimension $ n $ einfach um eine Matrix der Größe $ n \times 1 handelt $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-224">Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$.</span></span> <span data-ttu-id="3ed1b-225">Wie bei Vektoren können wir eine Matrix mit einer Zahl c multiplizieren, $ $ um eine neue Matrix zu erhalten, in der jeder Eintrag mit c multipliziert wird $ $ . Wir können zwei Matrizen derselben Größe hinzufügen, um eine neue Matrix zu generieren, deren Einträge die Summe der entsprechenden Einträge der beiden Matrizen sind.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-225">As with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices.</span></span> 

## <a name="matrix-multiplication-and-tensor-products"></a><span data-ttu-id="3ed1b-226">Matrix Multiplikation und Tensor-Produkte</span><span class="sxs-lookup"><span data-stu-id="3ed1b-226">Matrix Multiplication and Tensor Products</span></span>

<span data-ttu-id="3ed1b-227">Wir können auch zwei Matrizen $ m $ der Dimension $ m \times n $ und $ n $ der Dimension n p multiplizieren $ \times $ , um eine neue Matrix $ p $ der Dimension $ m \times p $ wie folgt zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-227">We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:</span></span>

\begin{align}
&\begin{bmatrix}
    <span data-ttu-id="3ed1b-228">M_ { 11 } ~~ m_ { 12 } ~~ \cdots ~~ m_ { 1N}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-228">M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\\\</span></span>
    <span data-ttu-id="3ed1b-229">M_ { 21 } ~~ m_ { 22 } ~~ \cdots ~~ m_ { 2N}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-229">M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\\\</span></span>
    \ddots\\\\
    <span data-ttu-id="3ed1b-230">M_ { M1 } ~~ m_ { m2 } ~~ \cdots ~~ m_ { MN}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-230">M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}</span></span>
\end{bmatrix}
\begin{bmatrix}
<span data-ttu-id="3ed1b-231">N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1P}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-231">N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\\\</span></span>
<span data-ttu-id="3ed1b-232">N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2P}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-232">N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="3ed1b-233">N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-233">N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}</span></span>
\end{bmatrix}=\begin{bmatrix}
<span data-ttu-id="3ed1b-234">P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1P}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-234">P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\\\</span></span>
<span data-ttu-id="3ed1b-235">P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2P}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-235">P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\\\</span></span>
\ddots\\\\
<span data-ttu-id="3ed1b-236">P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-236">P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}</span></span>
\end{bmatrix}
\end{align}

<span data-ttu-id="3ed1b-237">Dabei sind die Einträge $ von $ P $ P_ { IK } = \sum _j M_ { IJ } N_ { JK } $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-237">where the entries of $P$ are $P_{ik} = \sum_j M_{ij}N_{jk}$.</span></span> <span data-ttu-id="3ed1b-238">Der Eintrag $ P_ { 11 ist beispielsweise } $ das innere Produkt der ersten Zeile von $ M $ mit der ersten Spalte von $ N $ . Beachten Sie, dass sich diese Definition auf die Matrix Vektor Multiplikation erstreckt, da ein Vektor einfach ein Sonderfall einer Matrix ist.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-238">For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$. Note that since a vector is simply a special case of a matrix, this definition extends to matrix-vector multiplication.</span></span> 

<span data-ttu-id="3ed1b-239">Alle Matrizen, die wir in Erwägung haben, sind entweder quadratische Matrizen, bei denen die Anzahl der Zeilen und Spalten gleich ist, oder Vektoren, die nur $ einer $ Spalte entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-239">All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column.</span></span> <span data-ttu-id="3ed1b-240">Eine spezielle quadratische Matrix ist die [*Identitätsmatrix*](https://en.wikipedia.org/wiki/Identity_matrix), die als bezeichnet wird $ \boldone $ und deren diagonale Elemente gleich $ 1 $ und die übrigen Elemente gleich $ 0 sind $ :</span><span class="sxs-lookup"><span data-stu-id="3ed1b-240">One special square matrix is the [*identity matrix*](https://en.wikipedia.org/wiki/Identity_matrix), denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:</span></span>

$$\boldone=\begin{bmatrix}
<span data-ttu-id="3ed1b-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-241">1 ~~ 0 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="3ed1b-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-242">0 ~~ 1 ~~ \cdots ~~ 0\\\\</span></span>
<span data-ttu-id="3ed1b-243">~~ \ddots\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-243">~~ \ddots\\\\</span></span>
<span data-ttu-id="3ed1b-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$</span><span class="sxs-lookup"><span data-stu-id="3ed1b-244">0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix}.$$</span></span>

<span data-ttu-id="3ed1b-245">Für eine quadratische Matrix $ a $ sagen wir, dass $ die Matrix B $ bei [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) $ ab BA umgekehrt = ist = \boldone $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-245">For a square matrix $A$, we say a matrix $B$ is its [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) if $AB = BA = \boldone$.</span></span> <span data-ttu-id="3ed1b-246">Die Umkehrung einer Matrix muss nicht vorhanden sein. Wenn Sie jedoch vorhanden ist, ist sie eindeutig, und wir bezeichnen Sie $ als ^ { -1 } $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-246">The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$.</span></span> 

<span data-ttu-id="3ed1b-247">Bei allen Matrizen $ m $ ist die Adjoint-oder konjugierte-/konjugierte-Datei $ $ eine Matrix $ N, $ sodass $ N_ { IJ } = m_ { JI ist } ^ \* $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-247">For any matrix $M$, the adjoint or conjugate transpose of $M$ is a matrix $N$ such that $N_{ij} = M_{ji}^\*$.</span></span> <span data-ttu-id="3ed1b-248">Das Adjoint von $ M $ wird normalerweise als $ M ^ bezeichnet \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-248">The adjoint of $M$ is usually denoted $M^\dagger$.</span></span> <span data-ttu-id="3ed1b-249">Wir sagen, eine $ Matrix $ u [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) ist einheitlich $ , wenn UU ^ \dagger = u ^ \dagger u = \boldone $ oder gleichwertig, $ u ^ { -1 } = u ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-249">We say a matrix $U$ is [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) if $UU^\dagger = U^\dagger U = \boldone$ or equivalently, $U^{-1} = U^\dagger$.</span></span>  <span data-ttu-id="3ed1b-250">Die wichtigste Eigenschaft der einheitlichen Matrizen ist, dass Sie die Norm eines Vektors erhalten.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-250">Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.</span></span>  <span data-ttu-id="3ed1b-251">Dies liegt daran, dass</span><span class="sxs-lookup"><span data-stu-id="3ed1b-251">This happens because</span></span> 

<span data-ttu-id="3ed1b-252">$$\langlev, v \rangle = v ^ \dagger v = v ^ \dagger u ^ { -1 } U v = v ^ \dagger u ^ \dagger u v = \langle u v, u v \rangle .$$</span><span class="sxs-lookup"><span data-stu-id="3ed1b-252">$$\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = v^\dagger U^\dagger U v = \langle U v, U v\rangle.$$</span></span>  

<span data-ttu-id="3ed1b-253">Eine Matrix $ m $ wird als [*hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) bezeichnet, wenn $ m = m ^ \dagger $ .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-253">A matrix $M$ is said to be [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) if $M=M^\dagger$.</span></span>

<span data-ttu-id="3ed1b-254">Schließlich ist das [*tensorflow-Produkt*](https://en.wikipedia.org/wiki/Tensor_product) (oder Kronecker-Produkt) von zwei Matrizen $ m $ der Größe $ m \times n $ und $ n $ der Größe $ p \times q $ eine größere Matrix $ p = M \otimes n $ der Größe $ MP \times NQ " $ und wird $ $ $ $ wie folgt von M und n abgerufen:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-254">Finally, the [*tensor product*](https://en.wikipedia.org/wiki/Tensor_product) (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:</span></span>

\begin{align}
    <span data-ttu-id="3ed1b-255">M \otimes N&=</span><span class="sxs-lookup"><span data-stu-id="3ed1b-255">M \otimes N &=</span></span>
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-256">M_ { 11 } ~~ \cdots ~~ m_ { 1N }\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-256">M_{11} ~~ \cdots ~~ M_{1n} \\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="3ed1b-257">M_ { M1 } ~~ \cdots ~~ m_ { MN  }</span><span class="sxs-lookup"><span data-stu-id="3ed1b-257">M_{m1}  ~~ \cdots ~~ M_{mn}</span></span>
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-258">N_ { 11 } ~~ \cdots ~~ N_ { 1Q  }\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-258">N_{11}  ~~ \cdots ~~ N_{1q}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="3ed1b-259">N_ { P1 } ~~ \cdots ~~ N_ { PQ}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-259">N_{p1} ~~ \cdots ~~ N_{pq}</span></span>
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-260">M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="3ed1b-260">M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="3ed1b-261">M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-261">M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}\\\\</span></span>
        \ddots\\\\
        <span data-ttu-id="3ed1b-262">M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ } \end{bmatrix} ~~ \cdots  ~~</span><span class="sxs-lookup"><span data-stu-id="3ed1b-262">M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}~~ \cdots ~~</span></span> 
        <span data-ttu-id="3ed1b-263">M_ { MN } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1Q } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { PQ }  \end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-263">M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\\\ \ddots\\\\ N_{p1} ~~ \cdots ~~ N_{pq} \end{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-264">\end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-264">\end{bmatrix}.</span></span>
\end{align}

<span data-ttu-id="3ed1b-265">Dies wird in einigen Beispielen besser veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-265">This is better demonstrated with some examples:</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-266">a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=</span><span class="sxs-lookup"><span data-stu-id="3ed1b-266">a \\\\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix} =</span></span>
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-267">ein \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-267">a \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}</span></span>
        <span data-ttu-id="3ed1b-268">\\\\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-268">\\\\[1.5em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}</span></span>
    \end{bmatrix}
    <span data-ttu-id="3ed1b-269">=\begin{bmatrix}a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-269">= \begin{bmatrix} a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\ be\end{bmatrix}</span></span>
$$

<span data-ttu-id="3ed1b-270">and</span><span class="sxs-lookup"><span data-stu-id="3ed1b-270">and</span></span>

$$
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-271">a \ b \\\\ c \ d\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-271">a\ b \\\\ c\ d \end{bmatrix}</span></span>
    \otimes 
    \begin{bmatrix}
        <span data-ttu-id="3ed1b-272">e \ f \\\\ \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-272">e\ f\\\\g\ h \end{bmatrix}</span></span>
     =
    \begin{bmatrix}
    <span data-ttu-id="3ed1b-273">ein\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-273">a\begin{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-274">e \ f \\\\ \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-274">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-275">b\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-275">b\begin{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-276">e \ f \\\\ \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-276">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-277">\\\\[1em] c\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-277">\\\\[1em] c\begin{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-278">e \ f \\\\ \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-278">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-279">d\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-279">d\begin{bmatrix}</span></span>
    <span data-ttu-id="3ed1b-280">e \ f \\\\ \ h\end{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="3ed1b-280">e\ f\\\\ g\ h \end{bmatrix}</span></span>
    \end{bmatrix}
    =
    \begin{bmatrix}
    <span data-ttu-id="3ed1b-281">AE \ AF \ be \ BF\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-281">ae\ af\ be\ bf \\\\</span></span>
    <span data-ttu-id="3ed1b-282">AG \ AH \ BG \ BH\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-282">ag\ ah\ bg\ bh \\\\</span></span>
    <span data-ttu-id="3ed1b-283">CE \ CF \ de \ DF\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-283">ce\ cf\ de\ df \\\\</span></span>
    <span data-ttu-id="3ed1b-284">CG \ ch \ DG \ dh \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-284">cg\ ch\ dg\ dh \end{bmatrix}.</span></span>
$$

<span data-ttu-id="3ed1b-285">Eine abschließende, nützliche, in Bezug auf das tensorflow-Produkt verwendete Anmerkung ist, dass für alle Vektor- $ v $ -oder Matrix- $ m $ , $ v ^ { \otimes n } $ oder $ M ^ { \otimes n } $ für ein $ n $ -Fold wiederholtes tensorflow-Produkt kurz Hand ist.</span><span class="sxs-lookup"><span data-stu-id="3ed1b-285">A final useful notational convention surrounding tensor products is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$-fold repeated tensor product.</span></span>  <span data-ttu-id="3ed1b-286">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3ed1b-286">For example:</span></span>

\begin{align}
<span data-ttu-id="3ed1b-287">&\begin{bmatrix}1 \\\\ 0 1 \end{bmatrix} ^ { \otimes } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ -1 \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\</span><span class="sxs-lookup"><span data-stu-id="3ed1b-287">&\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ 0 \\\\0 \\\\0 \end{bmatrix}, \qquad\begin{bmatrix} 1 \\\\ -1 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\\\ -1 \\\\-1 \\\\1 \end{bmatrix}, \\\\</span></span>
  <span data-ttu-id="3ed1b-288">&\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 1 & 0 & 0 & 0 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="3ed1b-288">&\begin{bmatrix}  0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 1}= \begin{bmatrix}  0& 1 \\\\ 1& 0    \end{bmatrix},    \qquad\begin{bmatrix}   0 & 1 \\\\ 1& 0   \end{bmatrix}^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\\\ 0 &0&1&0 \\\\ 0 &1&0&0\\\\ 1 &0&0&0\end{bmatrix}.</span></span>
\end{align}
