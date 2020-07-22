---
<span data-ttu-id="e194a-101">Title: Quantum Oracles Description: Hier erfahren Sie, wie Sie mit Quantum-Oracles, Black Box-Vorgängen, die als Eingabe für einen anderen Algorithmus verwendet werden, arbeiten und definieren.</span><span class="sxs-lookup"><span data-stu-id="e194a-101">title: Quantum oracles description: Learn how to work with and define quantum oracles, black box operations that are used as input to another algorithm.</span></span>
<span data-ttu-id="e194a-102">Autor: cgranade UID: Microsoft. Quantum. Concepts. Oracles ms. Author: Christopher.Granade@microsoft.com ms. Date: 07/11/2018 ms. Topic: article NO-LOC:</span><span class="sxs-lookup"><span data-stu-id="e194a-102">author: cgranade uid: microsoft.quantum.concepts.oracles ms.author: Christopher.Granade@microsoft.com ms.date: 07/11/2018 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="e194a-103">"$$"</span><span class="sxs-lookup"><span data-stu-id="e194a-103">"$$"</span></span>
- <span data-ttu-id="e194a-104">"$$"</span><span class="sxs-lookup"><span data-stu-id="e194a-104">"$$"</span></span>
- <span data-ttu-id="e194a-105">"$"</span><span class="sxs-lookup"><span data-stu-id="e194a-105">"$"</span></span>
- <span data-ttu-id="e194a-106">"$"</span><span class="sxs-lookup"><span data-stu-id="e194a-106">"$"</span></span>
- <span data-ttu-id="e194a-107">"$"</span><span class="sxs-lookup"><span data-stu-id="e194a-107">"$"</span></span>
- <span data-ttu-id="e194a-108">"$$"</span><span class="sxs-lookup"><span data-stu-id="e194a-108">"$$"</span></span>
- <span data-ttu-id="e194a-109">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="e194a-109">"\cdots"</span></span>
- <span data-ttu-id="e194a-110">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="e194a-110">"bmatrix"</span></span>
- <span data-ttu-id="e194a-111">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="e194a-111">"\ddots"</span></span>
- <span data-ttu-id="e194a-112">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="e194a-112">"\equiv"</span></span>
- <span data-ttu-id="e194a-113">"\sum"</span><span class="sxs-lookup"><span data-stu-id="e194a-113">"\sum"</span></span>
- <span data-ttu-id="e194a-114">"\begin"</span><span class="sxs-lookup"><span data-stu-id="e194a-114">"\begin"</span></span>
- <span data-ttu-id="e194a-115">"\end"</span><span class="sxs-lookup"><span data-stu-id="e194a-115">"\end"</span></span>
- <span data-ttu-id="e194a-116">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="e194a-116">"\sqrt"</span></span>
- <span data-ttu-id="e194a-117">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="e194a-117">"\otimes"</span></span>
- <span data-ttu-id="e194a-118">"{"</span><span class="sxs-lookup"><span data-stu-id="e194a-118">"{"</span></span>
- <span data-ttu-id="e194a-119">"}"</span><span class="sxs-lookup"><span data-stu-id="e194a-119">"}"</span></span>
- <span data-ttu-id="e194a-120">"\text"</span><span class="sxs-lookup"><span data-stu-id="e194a-120">"\text"</span></span>
- <span data-ttu-id="e194a-121">"\phi"</span><span class="sxs-lookup"><span data-stu-id="e194a-121">"\phi"</span></span>
- <span data-ttu-id="e194a-122">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="e194a-122">"\kappa"</span></span>
- <span data-ttu-id="e194a-123">"\psi"</span><span class="sxs-lookup"><span data-stu-id="e194a-123">"\psi"</span></span>
- <span data-ttu-id="e194a-124">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="e194a-124">"\alpha"</span></span>
- <span data-ttu-id="e194a-125">"\beta"</span><span class="sxs-lookup"><span data-stu-id="e194a-125">"\beta"</span></span>
- <span data-ttu-id="e194a-126">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="e194a-126">"\gamma"</span></span>
- <span data-ttu-id="e194a-127">"\delta"</span><span class="sxs-lookup"><span data-stu-id="e194a-127">"\delta"</span></span>
- <span data-ttu-id="e194a-128">"\omega"</span><span class="sxs-lookup"><span data-stu-id="e194a-128">"\omega"</span></span>
- <span data-ttu-id="e194a-129">"\bra"</span><span class="sxs-lookup"><span data-stu-id="e194a-129">"\bra"</span></span>
- <span data-ttu-id="e194a-130">"\ket"</span><span class="sxs-lookup"><span data-stu-id="e194a-130">"\ket"</span></span>
- <span data-ttu-id="e194a-131">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="e194a-131">"\boldone"</span></span>
- <span data-ttu-id="e194a-132">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="e194a-132">"\\\\"</span></span>
- <span data-ttu-id="e194a-133">"\\"</span><span class="sxs-lookup"><span data-stu-id="e194a-133">"\\"</span></span>
- <span data-ttu-id="e194a-134">"="</span><span class="sxs-lookup"><span data-stu-id="e194a-134">"="</span></span>
- <span data-ttu-id="e194a-135">"\frac"</span><span class="sxs-lookup"><span data-stu-id="e194a-135">"\frac"</span></span>
- <span data-ttu-id="e194a-136">"\text"</span><span class="sxs-lookup"><span data-stu-id="e194a-136">"\text"</span></span>
- <span data-ttu-id="e194a-137">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="e194a-137">"\mapsto"</span></span>
- <span data-ttu-id="e194a-138">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="e194a-138">"\dagger"</span></span>
- <span data-ttu-id="e194a-139">"\to"</span><span class="sxs-lookup"><span data-stu-id="e194a-139">"\to"</span></span>
- <span data-ttu-id="e194a-140">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="e194a-140">"\begin{cases}"</span></span>
- <span data-ttu-id="e194a-141">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="e194a-141">"\end{cases}"</span></span>
- <span data-ttu-id="e194a-142">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="e194a-142">"\operatorname"</span></span>
- <span data-ttu-id="e194a-143">"\braket"</span><span class="sxs-lookup"><span data-stu-id="e194a-143">"\braket"</span></span>
- <span data-ttu-id="e194a-144">"\id"</span><span class="sxs-lookup"><span data-stu-id="e194a-144">"\id"</span></span>
- <span data-ttu-id="e194a-145">"\expect"</span><span class="sxs-lookup"><span data-stu-id="e194a-145">"\expect"</span></span>
- <span data-ttu-id="e194a-146">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="e194a-146">"\defeq"</span></span>
- <span data-ttu-id="e194a-147">"\variance"</span><span class="sxs-lookup"><span data-stu-id="e194a-147">"\variance"</span></span>
- <span data-ttu-id="e194a-148">"\dd"</span><span class="sxs-lookup"><span data-stu-id="e194a-148">"\dd"</span></span>
- <span data-ttu-id="e194a-149">"&"</span><span class="sxs-lookup"><span data-stu-id="e194a-149">"&"</span></span>
- <span data-ttu-id="e194a-150">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="e194a-150">"\begin{align}"</span></span>
- <span data-ttu-id="e194a-151">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="e194a-151">"\end{align}"</span></span>
- <span data-ttu-id="e194a-152">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="e194a-152">"\Lambda"</span></span>
- <span data-ttu-id="e194a-153">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="e194a-153">"\lambda"</span></span>
- <span data-ttu-id="e194a-154">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="e194a-154">"\Omega"</span></span>
- <span data-ttu-id="e194a-155">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="e194a-155">"\mathrm"</span></span>
- <span data-ttu-id="e194a-156">"\left"</span><span class="sxs-lookup"><span data-stu-id="e194a-156">"\left"</span></span>
- <span data-ttu-id="e194a-157">"\right"</span><span class="sxs-lookup"><span data-stu-id="e194a-157">"\right"</span></span>
- <span data-ttu-id="e194a-158">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="e194a-158">"\qquad"</span></span>
- <span data-ttu-id="e194a-159">"\times"</span><span class="sxs-lookup"><span data-stu-id="e194a-159">"\times"</span></span>
- <span data-ttu-id="e194a-160">"\big"</span><span class="sxs-lookup"><span data-stu-id="e194a-160">"\big"</span></span>
- <span data-ttu-id="e194a-161">"\langle"</span><span class="sxs-lookup"><span data-stu-id="e194a-161">"\langle"</span></span>
- <span data-ttu-id="e194a-162">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="e194a-162">"\rangle"</span></span>
- <span data-ttu-id="e194a-163">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="e194a-163">"\bigg"</span></span>
- <span data-ttu-id="e194a-164">"\Big"</span><span class="sxs-lookup"><span data-stu-id="e194a-164">"\Big"</span></span>
- <span data-ttu-id="e194a-165">"|"</span><span class="sxs-lookup"><span data-stu-id="e194a-165">"|"</span></span>
- <span data-ttu-id="e194a-166">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="e194a-166">"\mathbb"</span></span>
- <span data-ttu-id="e194a-167">"\vec"</span><span class="sxs-lookup"><span data-stu-id="e194a-167">"\vec"</span></span>
- <span data-ttu-id="e194a-168">"\in"</span><span class="sxs-lookup"><span data-stu-id="e194a-168">"\in"</span></span>
- <span data-ttu-id="e194a-169">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="e194a-169">"\texttt"</span></span>
- <span data-ttu-id="e194a-170">"\ne"</span><span class="sxs-lookup"><span data-stu-id="e194a-170">"\ne"</span></span>
- <span data-ttu-id="e194a-171">"<"</span><span class="sxs-lookup"><span data-stu-id="e194a-171">"<"</span></span>
- <span data-ttu-id="e194a-172">">"</span><span class="sxs-lookup"><span data-stu-id="e194a-172">">"</span></span>
- <span data-ttu-id="e194a-173">"\leq"</span><span class="sxs-lookup"><span data-stu-id="e194a-173">"\leq"</span></span>
- <span data-ttu-id="e194a-174">"\geq"</span><span class="sxs-lookup"><span data-stu-id="e194a-174">"\geq"</span></span>
- <span data-ttu-id="e194a-175">"~~"</span><span class="sxs-lookup"><span data-stu-id="e194a-175">"~~"</span></span>
- <span data-ttu-id="e194a-176">"~"</span><span class="sxs-lookup"><span data-stu-id="e194a-176">"~"</span></span>
- <span data-ttu-id="e194a-177">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="e194a-177">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="e194a-178">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="e194a-178">"\end{bmatrix}"</span></span>
- <span data-ttu-id="e194a-179">"\_"</span><span class="sxs-lookup"><span data-stu-id="e194a-179">"\_"</span></span>

---
# <a name="quantum-oracles"></a><span data-ttu-id="e194a-180">Quantum-Oracles</span><span class="sxs-lookup"><span data-stu-id="e194a-180">Quantum Oracles</span></span>

<span data-ttu-id="e194a-181">Ein Oracle $ O $ ist ein "Blackbox"-Vorgang, der als Eingabe für einen anderen Algorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e194a-181">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="e194a-182">Häufig werden solche Vorgänge mithilfe der klassischen Funktion $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m definiert, $ die eine $ n $ -Bit-Binär Eingabe annimmt und eine $ m $ -Bit-Binär Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="e194a-182">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="e194a-183">Beachten Sie hierzu eine bestimmte binäre Eingabe $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1 } ) $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-183">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="e194a-184">Wir können Qubit-Zustände als $ \ket { \vec { x } } = \ket { x_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 bezeichnen } } $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-184">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="e194a-185">Wir könnten zuerst versuchen, $ o so zu definieren $ $ , dass o \ket { x } = \ket { f (x) } $ , aber dies hat einige Probleme.</span><span class="sxs-lookup"><span data-stu-id="e194a-185">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="e194a-186">Erstens hat $ f $ möglicherweise eine andere Größe von Eingabe und Ausgabe ( $ n \ne m $ ), sodass $ $ durch das Anwenden von O die Anzahl der Qubits im Register geändert würde.</span><span class="sxs-lookup"><span data-stu-id="e194a-186">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="e194a-187">Zweitens: auch wenn $ n = m $ , ist die Funktion möglicherweise nicht invertierbar: Wenn $ f (x) = f (y) $ für einige $ x \ne y $ , dann $ o \ket { x } = o y, \ket { } $ aber $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-187">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="e194a-188">Dies bedeutet, dass wir den Adjoint-Vorgang O ^ nicht erstellen können $ \dagger $ , und für Oracles muss ein Adjoint-Element definiert sein.</span><span class="sxs-lookup"><span data-stu-id="e194a-188">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="e194a-189">Definieren eines Oracle-Effekts durch seine Auswirkung auf den Berechnungsbasis Status</span><span class="sxs-lookup"><span data-stu-id="e194a-189">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="e194a-190">Wir können diese beiden Probleme behandeln, indem wir ein zweites Register von $ m $ Qubits zum Speichern unserer Antwort einführen.</span><span class="sxs-lookup"><span data-stu-id="e194a-190">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="e194a-191">Anschließend definieren wir die Auswirkung des Oracle auf alle Berechnungs Status Zustände: für alle $ x \in \\ { 0, 1 \\ } ^ n $ und $ y \in \\ { 0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="e194a-191">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

$$
\begin{align}
    <span data-ttu-id="e194a-192">O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="e194a-192">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

<span data-ttu-id="e194a-193">$ = \dagger $ Wir haben nun die Erstellung durch die Erstellung der beiden früheren Probleme gelöst.</span><span class="sxs-lookup"><span data-stu-id="e194a-193">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
><span data-ttu-id="e194a-194">Beachten Sie, dass o $ = { \dagger } $ $ ^ 2 = \boldone $ seit $ a \oplus b \oplus b = a $ for $ a, b \in \[ ! Schel. No-Loc ({)] 0, 1 \[ ! Schel. No-Loc (})] $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-194"> To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
><span data-ttu-id="e194a-195">Folglich ist $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-195"> As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="e194a-196">Wichtig: die Definition eines Oracle auf diese Weise für jeden Berechnungsbasis Status $ \ket { x } \ket { y } $ definiert auch, wie $ O $ für einen beliebigen anderen Zustand agiert.</span><span class="sxs-lookup"><span data-stu-id="e194a-196">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="e194a-197">Dies folgt unmittelbar daran, dass $ O $ , wie alle Quantum-Vorgänge, linear in dem Zustand ist, auf den es angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e194a-197">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="e194a-198">Stellen Sie sich beispielsweise den Hadamard-Vorgang vor, der durch $ h \ket { 0 } = \ket { + } $ und $ h \ket { 1 } = \ket { - } $ definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e194a-198">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="e194a-199">Wenn Sie wissen möchten, wie $ h $ funktioniert $ \ket { + } $ , können wir dieses h verwenden, wenn es $ $ linear ist,</span><span class="sxs-lookup"><span data-stu-id="e194a-199">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

$$
\begin{align}
<span data-ttu-id="e194a-200">H \ket { + } & = \frac { 1 } { \sqrt { 2 } } h ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + h \ket { 1 } )\\\\</span><span class="sxs-lookup"><span data-stu-id="e194a-200">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\</span></span>
           &<span data-ttu-id="e194a-201">= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .</span><span class="sxs-lookup"><span data-stu-id="e194a-201"> = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
\end{align}
$$

<span data-ttu-id="e194a-202">Bei der Definition von Oracle $ O $ kann auf ähnliche Weise festgelegt werden, dass jeder Zustand $ \ket { \psi } $ auf $ n + m- $ Qubits als</span><span class="sxs-lookup"><span data-stu-id="e194a-202">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

$$
\begin{align}
\ket<span data-ttu-id="e194a-203">{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}</span><span class="sxs-lookup"><span data-stu-id="e194a-203">{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
\end{align}
$$

<span data-ttu-id="e194a-204">wobei $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ die Koeffizienten des Zustands darstellt $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-204">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="e194a-205">Demnach sind</span><span class="sxs-lookup"><span data-stu-id="e194a-205">Thus,</span></span>

$$
\begin{align}
<span data-ttu-id="e194a-206">O \ket { \psi } & = o \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\</span><span class="sxs-lookup"><span data-stu-id="e194a-206">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\</span></span>
             &<span data-ttu-id="e194a-207">= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .</span><span class="sxs-lookup"><span data-stu-id="e194a-207"> = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
\end{align}
$$

## <a name="phase-oracles"></a><span data-ttu-id="e194a-208">Phasen-Oracles</span><span class="sxs-lookup"><span data-stu-id="e194a-208">Phase oracles</span></span>
<span data-ttu-id="e194a-209">Alternativ $ $ dazu können Sie f in ein Oracle O codieren, $ $ indem Sie eine _Phase_ auf der Grundlage der Eingabe für $ O anwenden $ . Beispielsweise können wir $ O so definieren $ , dass$$</span><span class="sxs-lookup"><span data-stu-id="e194a-209">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$. For instance, we might define $O$ such that $$</span></span>
\begin{align}
    <span data-ttu-id="e194a-210">O \ket { x } = (-1) ^ { f (x) } \ket { x } .</span><span class="sxs-lookup"><span data-stu-id="e194a-210">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
\end{align}
$$
<span data-ttu-id="e194a-211">Wenn eine Phase, die Oracle für ein Register anfänglich in einem Compute-Status x anwendet, eine Phase $ \ket { } $ ist, ist diese Phase eine globale Phase und daher nicht Observable.</span><span class="sxs-lookup"><span data-stu-id="e194a-211">If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="e194a-212">Ein solches Oracle kann jedoch eine sehr leistungsfähige Ressource sein, wenn Sie auf eine übergeordnete Position oder einen kontrollierten Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e194a-212">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="e194a-213">Stellen Sie sich z $ . b. einen Phase-Oracle-O_f $ für eine Single-Qubit-Funktion $ f vor $ .</span><span class="sxs-lookup"><span data-stu-id="e194a-213">For example, consider a phase oracle $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="e194a-214">Seitdem$$</span><span class="sxs-lookup"><span data-stu-id="e194a-214">Then, $$</span></span>
\begin{align}
    <span data-ttu-id="e194a-215">O_f\ket{+}</span><span class="sxs-lookup"><span data-stu-id="e194a-215">O_f \ket{+}</span></span>
        &<span data-ttu-id="e194a-216">=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="e194a-216"> = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\</span></span>
        &<span data-ttu-id="e194a-217">=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="e194a-217"> = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\</span></span>
        &<span data-ttu-id="e194a-218">=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\</span><span class="sxs-lookup"><span data-stu-id="e194a-218"> = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\</span></span>
        &<span data-ttu-id="e194a-219">=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .</span><span class="sxs-lookup"><span data-stu-id="e194a-219"> = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
\end{align}
$$

<span data-ttu-id="e194a-220">Im Allgemeinen können beide Sichten von Oracles erweitert werden, um klassische Funktionen darzustellen, die anstelle eines einzelnen Bits reelle Zahlen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e194a-220">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="e194a-221">Das Auswählen der besten Methode zum Implementieren eines Oracle hängt stark davon ab, wie dieses Oracle innerhalb eines bestimmten Algorithmus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e194a-221">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="e194a-222">Der " [Deutsch-Jozsa"-Algorithmus](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) basiert z. b. auf dem Oracle, der auf die erste Weise implementiert ist, während der [-Algorithmus von Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) auf die zweite Weise implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="e194a-222">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="e194a-223">Weitere Informationen finden Sie unter [gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="e194a-223">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
