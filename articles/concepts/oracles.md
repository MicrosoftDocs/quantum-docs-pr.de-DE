---
<span data-ttu-id="dc94d-101">Title: Quantum Oracles Description: Hier erfahren Sie, wie Sie mit Quantum-Oracles, Black Box-Vorgängen, die als Eingabe für einen anderen Algorithmus verwendet werden, arbeiten und definieren.</span><span class="sxs-lookup"><span data-stu-id="dc94d-101">title: Quantum oracles description: Learn how to work with and define quantum oracles, black box operations that are used as input to another algorithm.</span></span>
<span data-ttu-id="dc94d-102">Autor: cgranade UID: Microsoft. Quantum. Concepts. Oracles ms. Author: chgranad ms. Date: 07/11/2018 ms. Topic: konzeptionelle NO-LOC:</span><span class="sxs-lookup"><span data-stu-id="dc94d-102">author: cgranade uid: microsoft.quantum.concepts.oracles ms.author: chgranad ms.date: 07/11/2018 ms.topic: conceptual no-loc:</span></span>
- <span data-ttu-id="dc94d-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="dc94d-103">"Q#"</span></span>
- <span data-ttu-id="dc94d-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="dc94d-104">"$$v"</span></span>
- <span data-ttu-id="dc94d-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="dc94d-105">"$$"</span></span>
- <span data-ttu-id="dc94d-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="dc94d-106">"$$"</span></span>
- <span data-ttu-id="dc94d-107">"$"</span><span class="sxs-lookup"><span data-stu-id="dc94d-107">"$"</span></span>
- <span data-ttu-id="dc94d-108">"$"</span><span class="sxs-lookup"><span data-stu-id="dc94d-108">"$"</span></span>
- <span data-ttu-id="dc94d-109">"$"</span><span class="sxs-lookup"><span data-stu-id="dc94d-109">"$"</span></span>
- <span data-ttu-id="dc94d-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="dc94d-110">"$$"</span></span>
- <span data-ttu-id="dc94d-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="dc94d-111">"\cdots"</span></span>
- <span data-ttu-id="dc94d-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="dc94d-112">"bmatrix"</span></span>
- <span data-ttu-id="dc94d-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="dc94d-113">"\ddots"</span></span>
- <span data-ttu-id="dc94d-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="dc94d-114">"\equiv"</span></span>
- <span data-ttu-id="dc94d-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="dc94d-115">"\sum"</span></span>
- <span data-ttu-id="dc94d-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="dc94d-116">"\begin"</span></span>
- <span data-ttu-id="dc94d-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="dc94d-117">"\end"</span></span>
- <span data-ttu-id="dc94d-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="dc94d-118">"\sqrt"</span></span>
- <span data-ttu-id="dc94d-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="dc94d-119">"\otimes"</span></span>
- <span data-ttu-id="dc94d-120">"{"</span><span class="sxs-lookup"><span data-stu-id="dc94d-120">"{"</span></span>
- <span data-ttu-id="dc94d-121">"}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-121">"}"</span></span>
- <span data-ttu-id="dc94d-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="dc94d-122">"\text"</span></span>
- <span data-ttu-id="dc94d-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="dc94d-123">"\phi"</span></span>
- <span data-ttu-id="dc94d-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="dc94d-124">"\kappa"</span></span>
- <span data-ttu-id="dc94d-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="dc94d-125">"\psi"</span></span>
- <span data-ttu-id="dc94d-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="dc94d-126">"\alpha"</span></span>
- <span data-ttu-id="dc94d-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="dc94d-127">"\beta"</span></span>
- <span data-ttu-id="dc94d-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="dc94d-128">"\gamma"</span></span>
- <span data-ttu-id="dc94d-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="dc94d-129">"\delta"</span></span>
- <span data-ttu-id="dc94d-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="dc94d-130">"\omega"</span></span>
- <span data-ttu-id="dc94d-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="dc94d-131">"\bra"</span></span>
- <span data-ttu-id="dc94d-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="dc94d-132">"\ket"</span></span>
- <span data-ttu-id="dc94d-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="dc94d-133">"\boldone"</span></span>
- <span data-ttu-id="dc94d-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="dc94d-134">"\\\\"</span></span>
- <span data-ttu-id="dc94d-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="dc94d-135">"\\"</span></span>
- <span data-ttu-id="dc94d-136">"="</span><span class="sxs-lookup"><span data-stu-id="dc94d-136">"="</span></span>
- <span data-ttu-id="dc94d-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="dc94d-137">"\frac"</span></span>
- <span data-ttu-id="dc94d-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="dc94d-138">"\text"</span></span>
- <span data-ttu-id="dc94d-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="dc94d-139">"\mapsto"</span></span>
- <span data-ttu-id="dc94d-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="dc94d-140">"\dagger"</span></span>
- <span data-ttu-id="dc94d-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="dc94d-141">"\to"</span></span>
- <span data-ttu-id="dc94d-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-142">"\begin{cases}"</span></span>
- <span data-ttu-id="dc94d-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-143">"\end{cases}"</span></span>
- <span data-ttu-id="dc94d-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="dc94d-144">"\operatorname"</span></span>
- <span data-ttu-id="dc94d-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="dc94d-145">"\braket"</span></span>
- <span data-ttu-id="dc94d-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="dc94d-146">"\id"</span></span>
- <span data-ttu-id="dc94d-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="dc94d-147">"\expect"</span></span>
- <span data-ttu-id="dc94d-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="dc94d-148">"\defeq"</span></span>
- <span data-ttu-id="dc94d-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="dc94d-149">"\variance"</span></span>
- <span data-ttu-id="dc94d-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="dc94d-150">"\dd"</span></span>
- <span data-ttu-id="dc94d-151">"&"</span><span class="sxs-lookup"><span data-stu-id="dc94d-151">"&"</span></span>
- <span data-ttu-id="dc94d-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-152">"\begin{align}"</span></span>
- <span data-ttu-id="dc94d-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-153">"\end{align}"</span></span>
- <span data-ttu-id="dc94d-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="dc94d-154">"\Lambda"</span></span>
- <span data-ttu-id="dc94d-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="dc94d-155">"\lambda"</span></span>
- <span data-ttu-id="dc94d-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="dc94d-156">"\Omega"</span></span>
- <span data-ttu-id="dc94d-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="dc94d-157">"\mathrm"</span></span>
- <span data-ttu-id="dc94d-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="dc94d-158">"\left"</span></span>
- <span data-ttu-id="dc94d-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="dc94d-159">"\right"</span></span>
- <span data-ttu-id="dc94d-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="dc94d-160">"\qquad"</span></span>
- <span data-ttu-id="dc94d-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="dc94d-161">"\times"</span></span>
- <span data-ttu-id="dc94d-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="dc94d-162">"\big"</span></span>
- <span data-ttu-id="dc94d-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="dc94d-163">"\langle"</span></span>
- <span data-ttu-id="dc94d-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="dc94d-164">"\rangle"</span></span>
- <span data-ttu-id="dc94d-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="dc94d-165">"\bigg"</span></span>
- <span data-ttu-id="dc94d-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="dc94d-166">"\Big"</span></span>
- <span data-ttu-id="dc94d-167">"|"</span><span class="sxs-lookup"><span data-stu-id="dc94d-167">"|"</span></span>
- <span data-ttu-id="dc94d-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="dc94d-168">"\mathbb"</span></span>
- <span data-ttu-id="dc94d-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="dc94d-169">"\vec"</span></span>
- <span data-ttu-id="dc94d-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="dc94d-170">"\in"</span></span>
- <span data-ttu-id="dc94d-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="dc94d-171">"\texttt"</span></span>
- <span data-ttu-id="dc94d-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="dc94d-172">"\ne"</span></span>
- <span data-ttu-id="dc94d-173">"<"</span><span class="sxs-lookup"><span data-stu-id="dc94d-173">"<"</span></span>
- <span data-ttu-id="dc94d-174">">"</span><span class="sxs-lookup"><span data-stu-id="dc94d-174">">"</span></span>
- <span data-ttu-id="dc94d-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="dc94d-175">"\leq"</span></span>
- <span data-ttu-id="dc94d-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="dc94d-176">"\geq"</span></span>
- <span data-ttu-id="dc94d-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="dc94d-177">"~~"</span></span>
- <span data-ttu-id="dc94d-178">"~"</span><span class="sxs-lookup"><span data-stu-id="dc94d-178">"~"</span></span>
- <span data-ttu-id="dc94d-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="dc94d-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="dc94d-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="dc94d-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="dc94d-181">"\_"</span></span>

---
# <a name="quantum-oracles"></a><span data-ttu-id="dc94d-182">Quantum-Oracles</span><span class="sxs-lookup"><span data-stu-id="dc94d-182">Quantum Oracles</span></span>

<span data-ttu-id="dc94d-183">Ein Oracle $ O $ ist ein "Blackbox"-Vorgang, der als Eingabe für einen anderen Algorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc94d-183">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="dc94d-184">Häufig werden solche Vorgänge mithilfe der klassischen Funktion $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m definiert, $ die eine $ n $ -Bit-Binär Eingabe annimmt und eine $ m $ -Bit-Binär Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="dc94d-184">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="dc94d-185">Beachten Sie hierzu eine bestimmte binäre Eingabe $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1 } ) $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-185">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="dc94d-186">Wir können Qubit-Zustände als $ \ket { \vec { x } } = \ket { x_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 bezeichnen } } $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-186">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="dc94d-187">Wir könnten zuerst versuchen, $ o so zu definieren $ $ , dass o \ket { x } = \ket { f (x) } $ , aber dies hat einige Probleme.</span><span class="sxs-lookup"><span data-stu-id="dc94d-187">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="dc94d-188">Erstens hat $ f $ möglicherweise eine andere Größe von Eingabe und Ausgabe ( $ n \ne m $ ), sodass $ $ durch das Anwenden von O die Anzahl der Qubits im Register geändert würde.</span><span class="sxs-lookup"><span data-stu-id="dc94d-188">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="dc94d-189">Zweitens: auch wenn $ n = m $ , ist die Funktion möglicherweise nicht invertierbar: Wenn $ f (x) = f (y) $ für einige $ x \ne y $ , dann $ o \ket { x } = o y, \ket { } $ aber $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-189">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="dc94d-190">Dies bedeutet, dass wir den Adjoint-Vorgang O ^ nicht erstellen können $ \dagger $ , und für Oracles muss ein Adjoint-Element definiert sein.</span><span class="sxs-lookup"><span data-stu-id="dc94d-190">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="dc94d-191">Definieren eines Oracle-Effekts durch seine Auswirkung auf den Berechnungsbasis Status</span><span class="sxs-lookup"><span data-stu-id="dc94d-191">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="dc94d-192">Wir können diese beiden Probleme behandeln, indem wir ein zweites Register von $ m $ Qubits zum Speichern unserer Antwort einführen.</span><span class="sxs-lookup"><span data-stu-id="dc94d-192">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="dc94d-193">Anschließend definieren wir die Auswirkung des Oracle auf alle Berechnungs Status Zustände: für alle $ x \in \\ { 0, 1 \\ } ^ n $ und $ y \in \\ { 0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="dc94d-193">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

$$
\begin{align}
    <span data-ttu-id="dc94d-194">O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="dc94d-194">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

<span data-ttu-id="dc94d-195">$ = \dagger $ Wir haben nun die Erstellung durch die Erstellung der beiden früheren Probleme gelöst.</span><span class="sxs-lookup"><span data-stu-id="dc94d-195">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
<span data-ttu-id="dc94d-196">>Beachten Sie, dass o $ = { \dagger } $ $ ^ 2 = \boldone $ seit $ a \oplus b \oplus b = a $ für alle $ a, b \in \: :: NO-LOC ({)::: 0, 1 \: :: NO-LOC (})::: $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-196">> To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
<span data-ttu-id="dc94d-197">>Folglich ist $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-197">> As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="dc94d-198">Wichtig: die Definition eines Oracle auf diese Weise für jeden Berechnungsbasis Status $ \ket { x } \ket { y } $ definiert auch, wie $ O $ für einen beliebigen anderen Zustand agiert.</span><span class="sxs-lookup"><span data-stu-id="dc94d-198">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="dc94d-199">Dies folgt unmittelbar daran, dass $ O $ , wie alle Quantum-Vorgänge, linear in dem Zustand ist, auf den es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc94d-199">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="dc94d-200">Stellen Sie sich beispielsweise den Hadamard-Vorgang vor, der durch $ h \ket { 0 } = \ket { + } $ und $ h \ket { 1 } = \ket { - } $ definiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc94d-200">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="dc94d-201">Wenn Sie wissen möchten, wie $ h $ funktioniert $ \ket { + } $ , können wir dieses h verwenden, wenn es $ $ linear ist,</span><span class="sxs-lookup"><span data-stu-id="dc94d-201">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

$$
\begin{align}
<span data-ttu-id="dc94d-202">H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\</span><span class="sxs-lookup"><span data-stu-id="dc94d-202">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\</span></span>
           <span data-ttu-id="dc94d-203">&= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .</span><span class="sxs-lookup"><span data-stu-id="dc94d-203">& = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
\end{align}
$$

<span data-ttu-id="dc94d-204">Bei der Definition von Oracle $ O $ kann auf ähnliche Weise festgelegt werden, dass jeder Zustand $ \ket { \psi } $ auf $ n + m- $ Qubits als</span><span class="sxs-lookup"><span data-stu-id="dc94d-204">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

$$
\begin{align}
<span data-ttu-id="dc94d-205">\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}</span><span class="sxs-lookup"><span data-stu-id="dc94d-205">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
\end{align}
$$

<span data-ttu-id="dc94d-206">wobei $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ die Koeffizienten des Zustands darstellt $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-206">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="dc94d-207">Demnach sind</span><span class="sxs-lookup"><span data-stu-id="dc94d-207">Thus,</span></span>

$$
\begin{align}
<span data-ttu-id="dc94d-208">O \ket { \psi } & = o \sum _{ x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum_ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\</span><span class="sxs-lookup"><span data-stu-id="dc94d-208">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\</span></span>
             <span data-ttu-id="dc94d-209">&= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="dc94d-209">& = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

## <a name="phase-oracles"></a><span data-ttu-id="dc94d-210">Phasen-Oracles</span><span class="sxs-lookup"><span data-stu-id="dc94d-210">Phase oracles</span></span>
<span data-ttu-id="dc94d-211">Alternativ $ $ dazu können Sie f in ein Oracle O codieren, $ $ indem Sie eine _Phase_ auf der Grundlage der Eingabe für $ O anwenden $ . Beispielsweise können wir $ O so definieren $ , dass $$</span><span class="sxs-lookup"><span data-stu-id="dc94d-211">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$. For instance, we might define $O$ such that $$</span></span>
\begin{align}
    <span data-ttu-id="dc94d-212">O \ket { x } = (-1) ^ { f (x) } \ket { x } .</span><span class="sxs-lookup"><span data-stu-id="dc94d-212">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
\end{align}
$$
<span data-ttu-id="dc94d-213">Wenn eine Phase, die Oracle für ein Register anfänglich in einem Compute-Status x anwendet, eine Phase $ \ket { } $ ist, ist diese Phase eine globale Phase und daher nicht Observable.</span><span class="sxs-lookup"><span data-stu-id="dc94d-213">If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="dc94d-214">Ein solches Oracle kann jedoch eine sehr leistungsfähige Ressource sein, wenn Sie auf eine übergeordnete Position oder einen kontrollierten Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc94d-214">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="dc94d-215">Stellen Sie sich z $ . b. einen Phase-Oracle-O_f $ für eine Single-Qubit-Funktion $ f vor $ .</span><span class="sxs-lookup"><span data-stu-id="dc94d-215">For example, consider a phase oracle $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="dc94d-216">Seitdem $$</span><span class="sxs-lookup"><span data-stu-id="dc94d-216">Then, $$</span></span>
\begin{align}
    <span data-ttu-id="dc94d-217">O_f \ket{+}</span><span class="sxs-lookup"><span data-stu-id="dc94d-217">O_f \ket{+}</span></span>
        <span data-ttu-id="dc94d-218">&=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="dc94d-218">& = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="dc94d-219">&=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="dc94d-219">& = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="dc94d-220">&=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="dc94d-220">& = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\</span></span>
        <span data-ttu-id="dc94d-221">&=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .</span><span class="sxs-lookup"><span data-stu-id="dc94d-221">& = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
\end{align}
$$

> [!NOTE]
<span data-ttu-id="dc94d-222">>Beachten Sie, dass $ z ^ { -1 } = Z ^ { \dagger } = Z $ und somit $ z ^ { f (0)-f (1) } = Z ^ { f (1)-f (0) ist } .$</span><span class="sxs-lookup"><span data-stu-id="dc94d-222">> Note that $Z^{-1}=Z^{\dagger}=Z$ and therefore $Z^{f(0)-f(1)}=Z^{f(1)-f(0)}.$</span></span>

<span data-ttu-id="dc94d-223">Im Allgemeinen können beide Sichten von Oracles erweitert werden, um klassische Funktionen darzustellen, die anstelle eines einzelnen Bits reelle Zahlen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dc94d-223">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="dc94d-224">Das Auswählen der besten Methode zum Implementieren eines Oracle hängt stark davon ab, wie dieses Oracle innerhalb eines bestimmten Algorithmus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc94d-224">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="dc94d-225">Der " [Deutsch-Jozsa"-Algorithmus](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) basiert z. b. auf dem Oracle, der auf die erste Weise implementiert ist, während der [-Algorithmus von Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) auf die zweite Weise implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc94d-225">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="dc94d-226">Weitere Informationen finden Sie unter [gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="dc94d-226">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
