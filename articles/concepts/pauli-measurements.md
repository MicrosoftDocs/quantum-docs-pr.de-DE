---
<span data-ttu-id="ce0ef-101">Title: Pauli Messungen Description: erfahren Sie, wie Sie mit Einzel-und multiqubit-Pauli-Mess Vorgängen arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-101">title: Pauli Measurements description: Learn how to work with single- and multi-qubit Pauli measurement operations.</span></span>
<span data-ttu-id="ce0ef-102">Autor: bradben UID: Microsoft. Quantum. Concepts. Pauli ms. Author: v-benbra ms. Date: 12/11/2017 ms. Topic: article NO-LOC:</span><span class="sxs-lookup"><span data-stu-id="ce0ef-102">author: bradben uid: microsoft.quantum.concepts.pauli ms.author: v-benbra ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="ce0ef-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-103">"Q#"</span></span>
- <span data-ttu-id="ce0ef-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-104">"$$v"</span></span>
- <span data-ttu-id="ce0ef-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-105">"$$"</span></span>
- <span data-ttu-id="ce0ef-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-106">"$$"</span></span>
- <span data-ttu-id="ce0ef-107">"$"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-107">"$"</span></span>
- <span data-ttu-id="ce0ef-108">"$"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-108">"$"</span></span>
- <span data-ttu-id="ce0ef-109">"$"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-109">"$"</span></span>
- <span data-ttu-id="ce0ef-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-110">"$$"</span></span>
- <span data-ttu-id="ce0ef-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-111">"\cdots"</span></span>
- <span data-ttu-id="ce0ef-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-112">"bmatrix"</span></span>
- <span data-ttu-id="ce0ef-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-113">"\ddots"</span></span>
- <span data-ttu-id="ce0ef-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-114">"\equiv"</span></span>
- <span data-ttu-id="ce0ef-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-115">"\sum"</span></span>
- <span data-ttu-id="ce0ef-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-116">"\begin"</span></span>
- <span data-ttu-id="ce0ef-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-117">"\end"</span></span>
- <span data-ttu-id="ce0ef-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-118">"\sqrt"</span></span>
- <span data-ttu-id="ce0ef-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-119">"\otimes"</span></span>
- <span data-ttu-id="ce0ef-120">"{"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-120">"{"</span></span>
- <span data-ttu-id="ce0ef-121">"}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-121">"}"</span></span>
- <span data-ttu-id="ce0ef-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-122">"\text"</span></span>
- <span data-ttu-id="ce0ef-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-123">"\phi"</span></span>
- <span data-ttu-id="ce0ef-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-124">"\kappa"</span></span>
- <span data-ttu-id="ce0ef-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-125">"\psi"</span></span>
- <span data-ttu-id="ce0ef-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-126">"\alpha"</span></span>
- <span data-ttu-id="ce0ef-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-127">"\beta"</span></span>
- <span data-ttu-id="ce0ef-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-128">"\gamma"</span></span>
- <span data-ttu-id="ce0ef-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-129">"\delta"</span></span>
- <span data-ttu-id="ce0ef-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-130">"\omega"</span></span>
- <span data-ttu-id="ce0ef-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-131">"\bra"</span></span>
- <span data-ttu-id="ce0ef-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-132">"\ket"</span></span>
- <span data-ttu-id="ce0ef-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-133">"\boldone"</span></span>
- <span data-ttu-id="ce0ef-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-134">"\\\\"</span></span>
- <span data-ttu-id="ce0ef-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-135">"\\"</span></span>
- <span data-ttu-id="ce0ef-136">"="</span><span class="sxs-lookup"><span data-stu-id="ce0ef-136">"="</span></span>
- <span data-ttu-id="ce0ef-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-137">"\frac"</span></span>
- <span data-ttu-id="ce0ef-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-138">"\text"</span></span>
- <span data-ttu-id="ce0ef-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-139">"\mapsto"</span></span>
- <span data-ttu-id="ce0ef-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-140">"\dagger"</span></span>
- <span data-ttu-id="ce0ef-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-141">"\to"</span></span>
- <span data-ttu-id="ce0ef-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-142">"\begin{cases}"</span></span>
- <span data-ttu-id="ce0ef-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-143">"\end{cases}"</span></span>
- <span data-ttu-id="ce0ef-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-144">"\operatorname"</span></span>
- <span data-ttu-id="ce0ef-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-145">"\braket"</span></span>
- <span data-ttu-id="ce0ef-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-146">"\id"</span></span>
- <span data-ttu-id="ce0ef-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-147">"\expect"</span></span>
- <span data-ttu-id="ce0ef-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-148">"\defeq"</span></span>
- <span data-ttu-id="ce0ef-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-149">"\variance"</span></span>
- <span data-ttu-id="ce0ef-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-150">"\dd"</span></span>
- <span data-ttu-id="ce0ef-151">"&"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-151">"&"</span></span>
- <span data-ttu-id="ce0ef-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-152">"\begin{align}"</span></span>
- <span data-ttu-id="ce0ef-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-153">"\end{align}"</span></span>
- <span data-ttu-id="ce0ef-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-154">"\Lambda"</span></span>
- <span data-ttu-id="ce0ef-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-155">"\lambda"</span></span>
- <span data-ttu-id="ce0ef-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-156">"\Omega"</span></span>
- <span data-ttu-id="ce0ef-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-157">"\mathrm"</span></span>
- <span data-ttu-id="ce0ef-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-158">"\left"</span></span>
- <span data-ttu-id="ce0ef-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-159">"\right"</span></span>
- <span data-ttu-id="ce0ef-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-160">"\qquad"</span></span>
- <span data-ttu-id="ce0ef-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-161">"\times"</span></span>
- <span data-ttu-id="ce0ef-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-162">"\big"</span></span>
- <span data-ttu-id="ce0ef-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-163">"\langle"</span></span>
- <span data-ttu-id="ce0ef-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-164">"\rangle"</span></span>
- <span data-ttu-id="ce0ef-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-165">"\bigg"</span></span>
- <span data-ttu-id="ce0ef-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-166">"\Big"</span></span>
- <span data-ttu-id="ce0ef-167">"|"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-167">"|"</span></span>
- <span data-ttu-id="ce0ef-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-168">"\mathbb"</span></span>
- <span data-ttu-id="ce0ef-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-169">"\vec"</span></span>
- <span data-ttu-id="ce0ef-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-170">"\in"</span></span>
- <span data-ttu-id="ce0ef-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-171">"\texttt"</span></span>
- <span data-ttu-id="ce0ef-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-172">"\ne"</span></span>
- <span data-ttu-id="ce0ef-173">"<"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-173">"<"</span></span>
- <span data-ttu-id="ce0ef-174">">"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-174">">"</span></span>
- <span data-ttu-id="ce0ef-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-175">"\leq"</span></span>
- <span data-ttu-id="ce0ef-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-176">"\geq"</span></span>
- <span data-ttu-id="ce0ef-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-177">"~~"</span></span>
- <span data-ttu-id="ce0ef-178">"~"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-178">"~"</span></span>
- <span data-ttu-id="ce0ef-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="ce0ef-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="ce0ef-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="ce0ef-181">"\_"</span></span>

---

# <a name="pauli-measurements"></a><span data-ttu-id="ce0ef-182">Pauli-Messungen</span><span class="sxs-lookup"><span data-stu-id="ce0ef-182">Pauli Measurements</span></span>

<span data-ttu-id="ce0ef-183">In den vorherigen Diskussionen haben wir uns auf Berechnungsbasis Messungen konzentriert.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-183">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="ce0ef-184">Tatsächlich gibt es weitere allgemeine Messungen, die bei der Quantum-Berechnung auftreten, die aus Sicht der Sicht bequem in Bezug auf Berechnungsbasis Messungen ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-184">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="ce0ef-185">Wenn Sie mit Arbeiten Q# , sind die gängigsten Arten von Messungen wahrscheinlich *Pauli-Messungen* , die Berechnungsbasis Messungen verallgemeinern, um Messungen in anderen Basen und die Parität zwischen verschiedenen Qubits zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-185">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements* , which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="ce0ef-186">In solchen Fällen ist es üblich, das Messen eines Pauli-Operators zu erörtern, im Allgemeinen ein Operator wie $ x, Y, z $ oder $ z \otimes z, x \otimes x, x \otimes Y $ usw.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-186">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span>

> [!TIP]
<span data-ttu-id="ce0ef-187">> In Q# werden multiqubit-Pauli-Operatoren in der Regel durch Arrays des Typs dargestellt `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-187">> In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
<span data-ttu-id="ce0ef-188">> Wenn $ \otimes Sie z. b. X Z Y darstellen möchten \otimes $ , können Sie das Array verwenden `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-188">> For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="ce0ef-189">Die Erörterung von Messungen in Form von Pauli-Operatoren ist vor allem im Unterfeld der Quantum-Fehlerkorrektur üblich.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-189">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="ce0ef-190">In Q# wird eine ähnliche Konvention befolgt. wir erläutern nun diese Alternative Ansicht der Messungen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-190">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="ce0ef-191">Bevor wir uns mit den Details der Bedeutung einer Pauli-Messung beschäftigen, ist es sinnvoll, sich Gedanken darüber zu machen, was ein einzelnes Qubit innerhalb eines Quantum-Computers in den Quantum-Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-191">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="ce0ef-192">Stellen Sie sich vor, dass wir einen $ n $ -Qubit-Quantum-Status haben. Anschließend wird ein Qubit sofort mit der Hälfte der $ 2 ^ n- $ Möglichkeiten gemessen, in denen sich der Zustand befinden könnte.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-192">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="ce0ef-193">Mit anderen Worten: die Messung projiziert den Quantum-Zustand auf einen von zwei halben Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-193">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="ce0ef-194">Wir können die Art und Weise verallgemeinern, in der Messungen für diese Intuition durchdacht werden.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-194">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="ce0ef-195">Um diese Teilbereiche zu beschreiben, benötigen wir eine Sprache für die Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-195">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="ce0ef-196">Eine Möglichkeit, die beiden Teilbereiche zu beschreiben, besteht darin, Sie durch eine Matrix anzugeben, die nur zwei eindeutige Eigenwerte aufweist, die von der Konvention als $ \pm 1 angenommen werden $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-196">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="ce0ef-197">Um ein einfaches Beispiel für das Beschreiben von Teilbereichen auf diese Weise zu beschreiben, sollten Sie $ Z $ :</span><span class="sxs-lookup"><span data-stu-id="ce0ef-197">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

$$
\begin{align}
  <span data-ttu-id="ce0ef-198">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-198">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="ce0ef-199">Wenn Sie die diagonalen Elemente der Pauli- $ Z- $ Matrix lesen, sehen Sie, dass $ Z $ zwei Eigenvektoren ( $ \ket { 0 } $ und $ \ket { 1) } $ mit den entsprechenden eigen Werten $ \pm 1 hat $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-199">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="ce0ef-200">Wenn wir also das Qubit Messen und Abrufen `Zero` (entsprechend dem Status $ \ket { 0 } $ ), wissen wir, dass der Zustand unseres Qubit ein $ + 1- $ eigen Zustand des $ Z-Operators ist $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-200">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="ce0ef-201">Entsprechend `One` wissen wir, dass der Zustand unseres Qubit ein $ -1- $ eigen Zustand von Z ist, $ Wenn wir erhalten $ . Dieser Prozess wird in der Sprache von Pauli-Messungen als "Messen von Pauli $ Z" bezeichnet $ und ist vollständig mit der Durchführung einer Berechnungsbasis Messung identisch.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-201">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$. This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="ce0ef-202">Jede $ 2- \times 2- $ Matrix, die eine einheitliche Transformation von Z ist, $ $ erfüllt diese Kriterien ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-202">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="ce0ef-203">Das heißt, wir könnten auch eine Matrix $ a = u ^ \dagger Z U verwenden $ , wobei $ u eine $ beliebige andere einheitliche Matrix ist, um eine Matrix zu erstellen, die die beiden Ergebnisse einer Messung in den $ \pm 1- $ Eigenvektoren definiert.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-203">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="ce0ef-204">Die Notation von Pauli-Messungen verweist auf diese einheitliche Äquivalenz $ , indem X-, Y-und Z- $ Messungen als gleichwertige Messungen identifiziert werden, die zur Gewinnung von Informationen aus einem Qubit führen können.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-204">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="ce0ef-205">Diese Messungen werden zur einfacheren Verwendung unten angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-205">These measurements are given below for convenience.</span></span>


<span data-ttu-id="ce0ef-206">|Die Pauli  | -Maßeinheit  |</span><span class="sxs-lookup"><span data-stu-id="ce0ef-206">|Pauli Measurement  |Unitary transformation  |</span></span>
|-------------------|------------------------|
<span data-ttu-id="ce0ef-207">|$ $ Z |               $\boldone$             |</span><span class="sxs-lookup"><span data-stu-id="ce0ef-207">| $Z$               | $\boldone$             |</span></span>
<span data-ttu-id="ce0ef-208">|$ $ X | $H               $                    |</span><span class="sxs-lookup"><span data-stu-id="ce0ef-208">| $X$               | $H$                    |</span></span>
<span data-ttu-id="ce0ef-209">|$ $ J | $HS ^               {\dagger}$         |</span><span class="sxs-lookup"><span data-stu-id="ce0ef-209">| $Y$               | $HS^{\dagger}$         |</span></span>

<span data-ttu-id="ce0ef-210">Das heißt, dass mit dieser Sprache "Measure $ Y $ " dem Anwenden $ von HS ^ \dagger $ und der anschließenden Messung der Berechnungsbasis entspricht, wobei [`S`](xref:Microsoft.Quantum.Intrinsic.S) ein System interner Quantum-Vorgang ist, der manchmal als "Phasen Gate" bezeichnet wird, und durch die einheitliche Matrix simuliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-210">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:Microsoft.Quantum.Intrinsic.S) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

$$
\begin{align}
    <span data-ttu-id="ce0ef-211">S =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-211">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="ce0ef-212">1 & 0 \\\\ 0 & i \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-212">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="ce0ef-213">Dies entspricht auch dem Anwenden von $ HS ^ \dagger $ auf den Quanten Zustands Vektor und dem anschließenden Messen von $ Z $ , sodass der folgende Vorgang folgendem entspricht `Measure([PauliY], [q])` :</span><span class="sxs-lookup"><span data-stu-id="ce0ef-213">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        Adjoint S(q);
        H(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

<span data-ttu-id="ce0ef-214">Der richtige Zustand wird dann durch umwandeln auf die Berechnungsbasis gefunden, was das Anwenden von $ SH $ auf den Quanten Zustands Vektor bedeutet. im obigen Code Ausschnitt wird die Transformation zurück zur Berechnungsbasis automatisch durch die Verwendung des- `within … apply` Blocks verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-214">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="ce0ef-215">In wird Q# das Ergebnis---, d. h., die klassischen Informationen, die aus der Interaktion mit dem State---extrahiert werden, werden durch einen `Result` Wert $ j NULL angegeben, der \in \\ { \texttt { } angibt, \texttt { } \\ } $ ob sich das Ergebnis im $ (-1) ^ j- $ eigen Raum des Pauli-Operators gemessen hat.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-215">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="ce0ef-216">Multiple-Qubit-Messungen</span><span class="sxs-lookup"><span data-stu-id="ce0ef-216">Multiple-qubit measurements</span></span>

<span data-ttu-id="ce0ef-217">Die Messungen von multiqubit-Pauli-Operatoren sind ähnlich definiert, wie in:</span><span class="sxs-lookup"><span data-stu-id="ce0ef-217">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

$$
<span data-ttu-id="ce0ef-218">Z \otimes z 1 0 0 0 0 = \begin{bmatrix} & & -1 0 0 0 0 & \\\\ & & & \\\\ & & -1 & 0 \\\\ & & & \end{bmatrix} 0 0 0 1.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-218">Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="ce0ef-219">Daher bilden die tensorflow-Produkte zweier Pauli- $ Z- $ Operatoren eine Matrix, die aus zwei Leerzeichen besteht, die aus $ + 1 $ und $ -1 $ eigen Werten bestehen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-219">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="ce0ef-220">Wie bei einem Single-Qubit-Fall bilden beide einen halben Leerraum, was bedeutet, dass die Hälfte des zugänglichen Vektor Raums zum $ + 1 $ -eigen Raum und die verbleibende Hälfte des $ eigen Raums-1 gehört $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-220">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="ce0ef-221">Im Allgemeinen ist es einfach, aus der Definition des tensorflow-Produkts zu erkennen, dass ein beliebiges tensorflow-Produkt von Pauli- $ Z- $ Operatoren und die Identität auch dies unterliegt.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-221">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="ce0ef-222">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="ce0ef-222">For example,</span></span>

$$
\begin{align}
    <span data-ttu-id="ce0ef-223">\otimes \boldone Z =\begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-223">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="ce0ef-224">1 &  0 &  0 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-224">1 &  0 &  0 &  0 \\\\</span></span>
        <span data-ttu-id="ce0ef-225">0 &  1 &  0 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-225">0 &  1 &  0 &  0 \\\\</span></span>
        <span data-ttu-id="ce0ef-226">0 &  0 & -1 &  0 \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-226">0 &  0 & -1 &  0 \\\\</span></span>
        <span data-ttu-id="ce0ef-227">0 &  0 &  0 & -1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-227">0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
\end{align}
$$

<span data-ttu-id="ce0ef-228">Wie zuvor beschreibt jede einheitliche Transformation dieser Matrizen auch zwei halb Bereiche mit der Bezeichnung $ \pm 1 $ Eigenwerte.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-228">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="ce0ef-229">Beispiel: $ x \otimes x = h \otimes h (z \otimes z) h \otimes h $  von der Identität, die $ Z = HXH ist $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-229">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="ce0ef-230">Ähnlich wie der One-Qubit-Fall können alle zwei-Qubit-Pauli-Messungen als $ u ^ \dagger (Z \otimes \id ) u $ für $ 4 \times 4 $ einheitliche Matrizen u $ $ geschrieben werden. Die Transformationen in der folgenden Tabelle werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-230">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$. We enumerate the transformations in the following table.</span></span>

> [!NOTE]
<span data-ttu-id="ce0ef-231">>In der Tabelle unten verwenden wir $ \operatorname { Swap } $ , um die Matrix > anzugeben.$$</span><span class="sxs-lookup"><span data-stu-id="ce0ef-231">> In the table below, we use $\operatorname{SWAP}$ to indicate the matrix > $$</span></span>
<span data-ttu-id="ce0ef-232">> \begin{align}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-232">> \begin{align}</span></span>
<span data-ttu-id="ce0ef-233">>     \operatorname{Austauschen } &=</span><span class="sxs-lookup"><span data-stu-id="ce0ef-233">>     \operatorname{SWAP} & =</span></span>
<span data-ttu-id="ce0ef-234">>     \left( \begin { Matrix}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-234">>     \left(\begin{matrix}</span></span>
<span data-ttu-id="ce0ef-235">>         1 & 0 & 0 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-235">>         1 & 0 & 0 & 0 \\\\</span></span>
<span data-ttu-id="ce0ef-236">>         0 & 0 & 1 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-236">>         0 & 0 & 1 & 0 \\\\</span></span>
<span data-ttu-id="ce0ef-237">>         0 & 1 & 0 & 0 \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-237">>         0 & 1 & 0 & 0 \\\\</span></span>
<span data-ttu-id="ce0ef-238">>0 & 0 & 0 & 1 > \end { Matrix } \right ) >     \end{align}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-238">>         0 & 0 & 0 & 1 >     \end{matrix}\right) > \end{align}</span></span>
<span data-ttu-id="ce0ef-239">> $$</span><span class="sxs-lookup"><span data-stu-id="ce0ef-239">> $$</span></span>
<span data-ttu-id="ce0ef-240">> wird verwendet, um den systeminternen Vorgang zu simulieren [`SWAP`](xref:Microsoft.Quantum.Intrinsic) .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-240">> used to simulate the intrinsic operation [`SWAP`](xref:Microsoft.Quantum.Intrinsic).</span></span>

<span data-ttu-id="ce0ef-241">|Die Pauli     | -Maßeinheit  |</span><span class="sxs-lookup"><span data-stu-id="ce0ef-241">|Pauli Measurement     |Unitary transformation  |</span></span>
|----------------------|------------------------|
<span data-ttu-id="ce0ef-242">|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-242">| $Z\otimes \boldone$ | $\boldone\otimes \boldone$ |</span></span>
<span data-ttu-id="ce0ef-243">|$ \otimes \boldone X $ | $ \otimes \boldone H $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-243">| $X\otimes \boldone$ | $H\otimes \boldone$ |</span></span>
<span data-ttu-id="ce0ef-244">|$ \otimes \boldone J $ | $ HS \dagger \otimes \boldone ^ $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-244">| $Y\otimes \boldone$ | $HS^\dagger\otimes \boldone$ |</span></span>
<span data-ttu-id="ce0ef-245">|$\boldone \otimes Z- $ | $ \operatorname { Swap } $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-245">| $\boldone \otimes Z$ | $\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="ce0ef-246">|$\boldone \otimes X $ | $ (H \otimes \boldone ) \operatorname { - } Swap $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-246">| $\boldone \otimes X$ | $(H\otimes \boldone)\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="ce0ef-247">|$\boldone \otimes j $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { - } Swap $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-247">| $\boldone \otimes Y$ | $(HS^\dagger\otimes \boldone)\operatorname{SWAP}$ |</span></span>
<span data-ttu-id="ce0ef-248">|$Z \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-248">| $Z\otimes Z$ | $\operatorname{CNOT}\_{10}$ |</span></span>
<span data-ttu-id="ce0ef-249">|$X \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes \boldone ) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-249">| $X\otimes Z$ | $\operatorname{CNOT}\_{10}(H\otimes \boldone)$ |</span></span>
<span data-ttu-id="ce0ef-250">|$J \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-250">| $Y\otimes Z$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$ |</span></span>
<span data-ttu-id="ce0ef-251">|$Z \otimes X $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes H) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-251">| $Z\otimes X$ | $\operatorname{CNOT}\_{10}(\boldone\otimes H)$ |</span></span>
<span data-ttu-id="ce0ef-252">|$X \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (h \otimes h) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-252">| $X\otimes X$ | $\operatorname{CNOT}\_{10}(H\otimes H)$ |</span></span>
<span data-ttu-id="ce0ef-253">|$J \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes H) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-253">| $Y\otimes X$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$ |</span></span>
<span data-ttu-id="ce0ef-254">|$Z \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-254">| $Z\otimes Y$ | $\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$ |</span></span>
<span data-ttu-id="ce0ef-255">|$X \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-255">| $X\otimes Y$ | $\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$ |</span></span>
<span data-ttu-id="ce0ef-256">|$J \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes HS ^ \dagger ) $|</span><span class="sxs-lookup"><span data-stu-id="ce0ef-256">| $Y\otimes Y$ | $\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$ |</span></span>

<span data-ttu-id="ce0ef-257">Hier wird der [`CNOT`](xref:Microsoft.Quantum.Intrinsic.CNOT) Vorgang aus folgendem Grund angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-257">Here, the [`CNOT`](xref:Microsoft.Quantum.Intrinsic.CNOT) operation appears for the following reason.</span></span>
<span data-ttu-id="ce0ef-258">Jede Pauli-Messung, bei der die Matrix nicht enthalten $ \boldone $ ist, ist gleichbedeutend $ mit \otimes $ der oben beschriebenen Argumentation.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-258">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="ce0ef-259">Die Eigenwerte von $ z \otimes z $ hängen nur von der Parität der Qubits ab, aus denen die einzelnen Berechnungsbasis Vektor bestehen, und die kontrollierten Vorgänge dienen dazu, diese Parität zu berechnen und im ersten Bit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-259">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="ce0ef-260">Nachdem das erste Bit gemessen wurde, können wir die Identität des resultierenden halb Raums wiederherstellen, was dem Messen des Pauli-Operators entspricht.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-260">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="ce0ef-261">Ein weiterer Hinweis: Obwohl es möglicherweise verlockend ist, zu übernehmen, dass die Messung von $ z \otimes z mit $ der sequenziellen Messung von $ z \otimes \mathbb { 1 } $ und dann $ \mathbb { 1 Z übereinstimmt } \otimes $ , wäre diese Annahme falsch.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-261">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="ce0ef-262">Der Grund hierfür ist, $ dass \otimes die Messung von z z $ den Quantum-Zustand entweder in den $ + 1 $ $ -oder-1- $ eigen Zustand dieser Operatoren projiziert.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-262">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="ce0ef-263">Messung $ \otimes \mathbb { von z 1 } $ und dann $ \mathbb { 1 } \otimes z $ projiziert den Quantum-Status Vektor zuerst auf einen halben Leerraum von $ Z \otimes \mathbb { 1 } $ und dann auf einen halben Bereich von $ \mathbb { 1 } \otimes z $ . Da es vier Berechnungsbasis Vektoren gibt, verringert die Durchführung beider Messungen den Zustand auf einen Viertel Raum und reduziert ihn somit auf einen einzelnen Berechnungsbasis Vektor.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-263">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="ce0ef-264">Korrelationen zwischen Qubits</span><span class="sxs-lookup"><span data-stu-id="ce0ef-264">Correlations between qubits</span></span>
<span data-ttu-id="ce0ef-265">Eine weitere Möglichkeit zum Messen von tensorflow-Produkten von Pauli-Matrizen, wie z. b. $ x \otimes x $ oder $ z \otimes z $ , besteht darin, dass mit diesen Messungen Informationen in den Korrelationen zwischen den beiden Qubits angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-265">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="ce0ef-266">Durch $ Messen \otimes \id $ von X können Sie Informationen überprüfen, die lokal im ersten Qubit gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-266">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="ce0ef-267">Obwohl beide Arten von Messungen in Quantum Computing gleichermaßen wertvoll sind, beleuchtet das erste die Leistungsfähigkeit von Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-267">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="ce0ef-268">Es ist offensichtlich, dass die Informationen, die Sie erlernen möchten, bei der Quantum-Verarbeitung nicht in einem einzigen Qubit gespeichert werden, sondern nicht lokal in allen Qubits gespeichert werden $ \otimes . Daher werden diese Informationen nur durch eine gemeinsame Messung (z. b. z z. b. z z $ ) als Manifest angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-268">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="ce0ef-269">Beispielsweise möchten wir bei der Fehlerkorrektur häufig ermitteln, welche Fehler aufgetreten sind, wenn Sie nichts über den Zustand erfahren möchten, den wir zu schützen versuchen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-269">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="ce0ef-270">Das Beispiel für [bitflip-Code](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code) zeigt ein Beispiel dafür, wie Sie dies mithilfe von Messungen wie $ z \otimes z \otimes \id $ und $ \id \otimes z \otimes z $ < erreichen können. --TODO: Ändern Sie dies in einen Link zum Beispiel Browser, sobald das bitflip-Codebeispiel integriert ist.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-270">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/main/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$. <!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded.</span></span> -->

<span data-ttu-id="ce0ef-271">Beliebige Pauli-Operatoren $ wie \otimes \otimes z. b. X Y Z \otimes \boldone $ können ebenfalls gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-271">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="ce0ef-272">Alle derartigen tensorflow-Produkte von Pauli-Operatoren verfügen nur über zwei Eigenwerte $ \pm 1, $ und beide eigen Räume bilden halbräume des gesamten Vektor Bereichs.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-272">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="ce0ef-273">Daher stimmen Sie mit den oben genannten Anforderungen überein.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-273">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="ce0ef-274">In Q# geben solche Messungen j zurück, $ $ Wenn die Messung ein Ergebnis im Eigen Raum des Zeichens $ (-1) ^ j ergibt $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-274">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="ce0ef-275">Die Verwendung von Pauli-Messungen als integrierte Funktion in Q# ist hilfreich, da die Messung solcher Operatoren lange Ketten von gesteuerten und nicht-Transformationen und Basis Transformationen erfordert, um das diagonalisieren des U-Gates zu beschreiben, $ $ das erforderlich ist, um den Vorgang als tensorflow-Produkt von $ Z $ und auszudrücken $ \id $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-275">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$.</span></span>
<span data-ttu-id="ce0ef-276">Wenn Sie festlegen können, dass Sie eine dieser vordefinierten Messungen durchführen möchten, müssen Sie sich keine Gedanken darüber machen, wie Sie Ihre Basis so transformieren, dass eine Berechnungsbasis Messung die erforderlichen Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-276">By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="ce0ef-277">Q# behandelt alle notwendigen Basis Transformationen automatisch.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-277">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="ce0ef-278">Weitere Informationen finden Sie unter den [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) -und- [`MeasurePaulis`](xref:Microsoft.Quantum.Measurement.MeasurePaulis) Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-278">For more information, see the [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) and [`MeasurePaulis`](xref:Microsoft.Quantum.Measurement.MeasurePaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="ce0ef-279">Das No-Cloning-Theorem</span><span class="sxs-lookup"><span data-stu-id="ce0ef-279">The No-Cloning Theorem</span></span>

<span data-ttu-id="ce0ef-280">Quantum-Informationen sind leistungsstark.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-280">Quantum information is powerful.</span></span>
<span data-ttu-id="ce0ef-281">Dadurch können wir beeindruckende Dinge, wie z. b. die Faktor Zahlen, exponentiell beschleunigen als die besten bekannten klassischen Algorithmen, oder korrelierte Elektronen Systeme effizient simulieren, die für eine genaue Simulation exponentialkosten benötigen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-281">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="ce0ef-282">Es gibt jedoch Einschränkungen hinsichtlich der Leistungsfähigkeit von Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-282">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="ce0ef-283">Eine solche Einschränkung wird durch das *No-Klon-Theorem* angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-283">One such limitation is given by the *No-Cloning Theorem* .</span></span>

<span data-ttu-id="ce0ef-284">Der No-Cloning Theorem hat einen passenden Namen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-284">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="ce0ef-285">Sie lässt das Klonen generischer Quantenzustände durch einen Quantum-Computer nicht zu.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-285">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="ce0ef-286">Der Beweis für das Theorem ist erstaunlich einfach.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-286">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="ce0ef-287">Obwohl ein vollständiger Nachweis für das No-Klon-Theorem für unsere Erörterung etwas zu technisch ist, liegt der Nachweis im Fall von zusätzlichen Qubits in unserem Bereich. (zusätzliche Qubits sind für den temporären Speicherplatz während einer Berechnung verwendeter Qubits und können problemlos verwendet und verwaltet werden ( Q# Siehe [geliehene Qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span><span class="sxs-lookup"><span data-stu-id="ce0ef-287">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope (auxiliary qubits are qubits used for scratch space during a computation and are easily used and managed in Q#, see [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span></span>

<span data-ttu-id="ce0ef-288">Bei solch einem Quantum-Computer muss der Klon Vorgang durch eine einheitliche Matrix beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-288">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="ce0ef-289">Die Messung wird nicht zugelassen, da der Quantum-Zustand beschädigt wird, den wir klonen wollen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-289">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="ce0ef-290">Um den Klon Vorgang zu simulieren, soll die einheitliche Matrix die Eigenschaft verwenden, die $$</span><span class="sxs-lookup"><span data-stu-id="ce0ef-290">To simulate the cloning operation, we want the unitary matrix used to have the property that $$</span></span>
  <span data-ttu-id="ce0ef-291">U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-291">U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
$$
<span data-ttu-id="ce0ef-292">für jeden Zustand $ \ket { \psi } $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-292">for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="ce0ef-293">Die Linearität-Eigenschaft der Matrix Multiplikation impliziert dann, dass für jeden zweiten Quantum $ -Zustand \ket { \phi } $</span><span class="sxs-lookup"><span data-stu-id="ce0ef-293">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

$$
\begin{align}
    <span data-ttu-id="ce0ef-294">U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-294">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="ce0ef-295">&= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-295">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="ce0ef-296">+ \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-296">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\</span></span>
    <span data-ttu-id="ce0ef-297">&= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}</span><span class="sxs-lookup"><span data-stu-id="ce0ef-297">& = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="ce0ef-298">\right) \\\\</span><span class="sxs-lookup"><span data-stu-id="ce0ef-298">\right) \\\\</span></span>
    <span data-ttu-id="ce0ef-299">&\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right )) \right .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-299">& \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
\end{align}
$$

<span data-ttu-id="ce0ef-300">Dadurch wird die grundlegende Intuition hinter dem No-Cloning-Theorem bereitstellt: jedes Gerät, das einen unbekannten Quantum-Zustand kopiert, muss Fehler in mindestens einigen der von ihm kopierte Zustände auslösen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-300">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="ce0ef-301">Während die Hauptannahme, dass der Cloner den Eingabe Status linear verarbeitet, durch Hinzufügen und Messen von hilfssbits verletzt werden kann, können solche Interaktionen auch Informationen über das System durch die maßstatistik und das exakte Klonen in solchen Fällen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-301">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="ce0ef-302">Einen ausführlicheren Nachweis des No-Cloning [Theorem finden Sie](xref:microsoft.quantum.more-information)unter.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-302">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="ce0ef-303">Das No-Cloning-Theorem ist wichtig für ein qualitativ hochwertiges Verständnis von Quantum Computing, denn wenn Sie Quantum-Zustände ingünstig Klonen könnten, erhalten Sie eine nahezu magische Möglichkeit, aus den Quantum-Zuständen zu lernen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-303">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="ce0ef-304">Tatsächlich könnten Sie das Prinzip der geunten Unsicherheit von Heisenberg verletzen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-304">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="ce0ef-305">Alternativ können Sie einen optimalen Cloner verwenden, um ein einzelnes Beispiel aus einer komplexen Quantum-Distribution zu erstellen und alles zu erlernen, was Sie möglicherweise über die Verteilung von nur einem Beispiel erfahren.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-305">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="ce0ef-306">Dies würden Sie tun, wenn Sie eine Münze kippen und Köpfe beobachten und dann einen Freund über das Ergebnis informieren, dass er antwortet, dass die Verteilung der Münze Bernoulli mit $ p = 0.512643 \ ldots $ ! "lauten muss.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-306">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="ce0ef-307">Eine solche Anweisung wäre nicht unsinnig, weil ein Teil der Informationen (das Heads-Ergebnis) einfach nicht die vielen Informationen bereitstellen kann, die erforderlich sind, um die Verteilung ohne wesentliche vorherige Informationen zu codieren.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-307">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="ce0ef-308">Ebenso wie ohne vorherige Informationen können wir einen quantumstatus nicht ganz genau so Klonen, wie wir ein Ensemble dieser Münzen nicht vorbereiten können, ohne dass Sie $ p kennen $ .</span><span class="sxs-lookup"><span data-stu-id="ce0ef-308">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="ce0ef-309">Informationen sind in Quantum Computing nicht kostenlos.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-309">Information is not free in quantum computing.</span></span>
<span data-ttu-id="ce0ef-310">Jedes gemessene Qubit liefert ein einzelnes Bit an Informationen, und das No-Cloning-Theorem zeigt, dass es keine Hintertür gibt, die ausgenutzt werden kann, um den grundlegenden Kompromiss zwischen den Informationen, die über das System gewonnen wurden, und der darauf aufgerufenen Störung zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="ce0ef-310">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
