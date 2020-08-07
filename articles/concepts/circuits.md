---
<span data-ttu-id="61d7c-101">Title: Quantum-Verbindungs Beschreibung: erfahren Sie, wie Sie einfache und komplexe Quantum-Vorgänge mithilfe von Quantum-Verbindungs Diagrammen visuell darstellen.</span><span class="sxs-lookup"><span data-stu-id="61d7c-101">title: Quantum circuits description: Learn how to visually represent simple and complex quantum operations with quantum circuit diagrams.</span></span>
<span data-ttu-id="61d7c-102">Autor: quantumwriter UID: Microsoft. Quantum. Concepts. Circuits ms. Author: nawiebe@microsoft.com ms. Date: 12/11/2017 ms. Topic: article NO-LOC:</span><span class="sxs-lookup"><span data-stu-id="61d7c-102">author: QuantumWriter uid: microsoft.quantum.concepts.circuits ms.author: nawiebe@microsoft.com ms.date: 12/11/2017 ms.topic: article no-loc:</span></span>
- <span data-ttu-id="61d7c-103">"Q#"</span><span class="sxs-lookup"><span data-stu-id="61d7c-103">"Q#"</span></span>
- <span data-ttu-id="61d7c-104">"$$v"</span><span class="sxs-lookup"><span data-stu-id="61d7c-104">"$$v"</span></span>
- <span data-ttu-id="61d7c-105">"$$"</span><span class="sxs-lookup"><span data-stu-id="61d7c-105">"$$"</span></span>
- <span data-ttu-id="61d7c-106">"$$"</span><span class="sxs-lookup"><span data-stu-id="61d7c-106">"$$"</span></span>
- <span data-ttu-id="61d7c-107">"$"</span><span class="sxs-lookup"><span data-stu-id="61d7c-107">"$"</span></span>
- <span data-ttu-id="61d7c-108">"$"</span><span class="sxs-lookup"><span data-stu-id="61d7c-108">"$"</span></span>
- <span data-ttu-id="61d7c-109">"$"</span><span class="sxs-lookup"><span data-stu-id="61d7c-109">"$"</span></span>
- <span data-ttu-id="61d7c-110">"$$"</span><span class="sxs-lookup"><span data-stu-id="61d7c-110">"$$"</span></span>
- <span data-ttu-id="61d7c-111">"\cdots"</span><span class="sxs-lookup"><span data-stu-id="61d7c-111">"\cdots"</span></span>
- <span data-ttu-id="61d7c-112">"bmatrix"</span><span class="sxs-lookup"><span data-stu-id="61d7c-112">"bmatrix"</span></span>
- <span data-ttu-id="61d7c-113">"\ddots"</span><span class="sxs-lookup"><span data-stu-id="61d7c-113">"\ddots"</span></span>
- <span data-ttu-id="61d7c-114">"\equiv"</span><span class="sxs-lookup"><span data-stu-id="61d7c-114">"\equiv"</span></span>
- <span data-ttu-id="61d7c-115">"\sum"</span><span class="sxs-lookup"><span data-stu-id="61d7c-115">"\sum"</span></span>
- <span data-ttu-id="61d7c-116">"\begin"</span><span class="sxs-lookup"><span data-stu-id="61d7c-116">"\begin"</span></span>
- <span data-ttu-id="61d7c-117">"\end"</span><span class="sxs-lookup"><span data-stu-id="61d7c-117">"\end"</span></span>
- <span data-ttu-id="61d7c-118">"\sqrt"</span><span class="sxs-lookup"><span data-stu-id="61d7c-118">"\sqrt"</span></span>
- <span data-ttu-id="61d7c-119">"\otimes"</span><span class="sxs-lookup"><span data-stu-id="61d7c-119">"\otimes"</span></span>
- <span data-ttu-id="61d7c-120">"{"</span><span class="sxs-lookup"><span data-stu-id="61d7c-120">"{"</span></span>
- <span data-ttu-id="61d7c-121">"}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-121">"}"</span></span>
- <span data-ttu-id="61d7c-122">"\text"</span><span class="sxs-lookup"><span data-stu-id="61d7c-122">"\text"</span></span>
- <span data-ttu-id="61d7c-123">"\phi"</span><span class="sxs-lookup"><span data-stu-id="61d7c-123">"\phi"</span></span>
- <span data-ttu-id="61d7c-124">"\kappa"</span><span class="sxs-lookup"><span data-stu-id="61d7c-124">"\kappa"</span></span>
- <span data-ttu-id="61d7c-125">"\psi"</span><span class="sxs-lookup"><span data-stu-id="61d7c-125">"\psi"</span></span>
- <span data-ttu-id="61d7c-126">"\alpha"</span><span class="sxs-lookup"><span data-stu-id="61d7c-126">"\alpha"</span></span>
- <span data-ttu-id="61d7c-127">"\beta"</span><span class="sxs-lookup"><span data-stu-id="61d7c-127">"\beta"</span></span>
- <span data-ttu-id="61d7c-128">"\gamma"</span><span class="sxs-lookup"><span data-stu-id="61d7c-128">"\gamma"</span></span>
- <span data-ttu-id="61d7c-129">"\delta"</span><span class="sxs-lookup"><span data-stu-id="61d7c-129">"\delta"</span></span>
- <span data-ttu-id="61d7c-130">"\omega"</span><span class="sxs-lookup"><span data-stu-id="61d7c-130">"\omega"</span></span>
- <span data-ttu-id="61d7c-131">"\bra"</span><span class="sxs-lookup"><span data-stu-id="61d7c-131">"\bra"</span></span>
- <span data-ttu-id="61d7c-132">"\ket"</span><span class="sxs-lookup"><span data-stu-id="61d7c-132">"\ket"</span></span>
- <span data-ttu-id="61d7c-133">"\boldone"</span><span class="sxs-lookup"><span data-stu-id="61d7c-133">"\boldone"</span></span>
- <span data-ttu-id="61d7c-134">"\\\\"</span><span class="sxs-lookup"><span data-stu-id="61d7c-134">"\\\\"</span></span>
- <span data-ttu-id="61d7c-135">"\\"</span><span class="sxs-lookup"><span data-stu-id="61d7c-135">"\\"</span></span>
- <span data-ttu-id="61d7c-136">"="</span><span class="sxs-lookup"><span data-stu-id="61d7c-136">"="</span></span>
- <span data-ttu-id="61d7c-137">"\frac"</span><span class="sxs-lookup"><span data-stu-id="61d7c-137">"\frac"</span></span>
- <span data-ttu-id="61d7c-138">"\text"</span><span class="sxs-lookup"><span data-stu-id="61d7c-138">"\text"</span></span>
- <span data-ttu-id="61d7c-139">"\mapsto"</span><span class="sxs-lookup"><span data-stu-id="61d7c-139">"\mapsto"</span></span>
- <span data-ttu-id="61d7c-140">"\dagger"</span><span class="sxs-lookup"><span data-stu-id="61d7c-140">"\dagger"</span></span>
- <span data-ttu-id="61d7c-141">"\to"</span><span class="sxs-lookup"><span data-stu-id="61d7c-141">"\to"</span></span>
- <span data-ttu-id="61d7c-142">"\begin{cases}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-142">"\begin{cases}"</span></span>
- <span data-ttu-id="61d7c-143">"\end{cases}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-143">"\end{cases}"</span></span>
- <span data-ttu-id="61d7c-144">"\operatorname"</span><span class="sxs-lookup"><span data-stu-id="61d7c-144">"\operatorname"</span></span>
- <span data-ttu-id="61d7c-145">"\braket"</span><span class="sxs-lookup"><span data-stu-id="61d7c-145">"\braket"</span></span>
- <span data-ttu-id="61d7c-146">"\id"</span><span class="sxs-lookup"><span data-stu-id="61d7c-146">"\id"</span></span>
- <span data-ttu-id="61d7c-147">"\expect"</span><span class="sxs-lookup"><span data-stu-id="61d7c-147">"\expect"</span></span>
- <span data-ttu-id="61d7c-148">"\defeq"</span><span class="sxs-lookup"><span data-stu-id="61d7c-148">"\defeq"</span></span>
- <span data-ttu-id="61d7c-149">"\variance"</span><span class="sxs-lookup"><span data-stu-id="61d7c-149">"\variance"</span></span>
- <span data-ttu-id="61d7c-150">"\dd"</span><span class="sxs-lookup"><span data-stu-id="61d7c-150">"\dd"</span></span>
- <span data-ttu-id="61d7c-151">"&"</span><span class="sxs-lookup"><span data-stu-id="61d7c-151">"&"</span></span>
- <span data-ttu-id="61d7c-152">"\begin{align}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-152">"\begin{align}"</span></span>
- <span data-ttu-id="61d7c-153">"\end{align}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-153">"\end{align}"</span></span>
- <span data-ttu-id="61d7c-154">"\Lambda"</span><span class="sxs-lookup"><span data-stu-id="61d7c-154">"\Lambda"</span></span>
- <span data-ttu-id="61d7c-155">"\lambda"</span><span class="sxs-lookup"><span data-stu-id="61d7c-155">"\lambda"</span></span>
- <span data-ttu-id="61d7c-156">"\Omega"</span><span class="sxs-lookup"><span data-stu-id="61d7c-156">"\Omega"</span></span>
- <span data-ttu-id="61d7c-157">"\mathrm"</span><span class="sxs-lookup"><span data-stu-id="61d7c-157">"\mathrm"</span></span>
- <span data-ttu-id="61d7c-158">"\left"</span><span class="sxs-lookup"><span data-stu-id="61d7c-158">"\left"</span></span>
- <span data-ttu-id="61d7c-159">"\right"</span><span class="sxs-lookup"><span data-stu-id="61d7c-159">"\right"</span></span>
- <span data-ttu-id="61d7c-160">"\qquad"</span><span class="sxs-lookup"><span data-stu-id="61d7c-160">"\qquad"</span></span>
- <span data-ttu-id="61d7c-161">"\times"</span><span class="sxs-lookup"><span data-stu-id="61d7c-161">"\times"</span></span>
- <span data-ttu-id="61d7c-162">"\big"</span><span class="sxs-lookup"><span data-stu-id="61d7c-162">"\big"</span></span>
- <span data-ttu-id="61d7c-163">"\langle"</span><span class="sxs-lookup"><span data-stu-id="61d7c-163">"\langle"</span></span>
- <span data-ttu-id="61d7c-164">"\rangle"</span><span class="sxs-lookup"><span data-stu-id="61d7c-164">"\rangle"</span></span>
- <span data-ttu-id="61d7c-165">"\bigg"</span><span class="sxs-lookup"><span data-stu-id="61d7c-165">"\bigg"</span></span>
- <span data-ttu-id="61d7c-166">"\Big"</span><span class="sxs-lookup"><span data-stu-id="61d7c-166">"\Big"</span></span>
- <span data-ttu-id="61d7c-167">"|"</span><span class="sxs-lookup"><span data-stu-id="61d7c-167">"|"</span></span>
- <span data-ttu-id="61d7c-168">"\mathbb"</span><span class="sxs-lookup"><span data-stu-id="61d7c-168">"\mathbb"</span></span>
- <span data-ttu-id="61d7c-169">"\vec"</span><span class="sxs-lookup"><span data-stu-id="61d7c-169">"\vec"</span></span>
- <span data-ttu-id="61d7c-170">"\in"</span><span class="sxs-lookup"><span data-stu-id="61d7c-170">"\in"</span></span>
- <span data-ttu-id="61d7c-171">"\texttt"</span><span class="sxs-lookup"><span data-stu-id="61d7c-171">"\texttt"</span></span>
- <span data-ttu-id="61d7c-172">"\ne"</span><span class="sxs-lookup"><span data-stu-id="61d7c-172">"\ne"</span></span>
- <span data-ttu-id="61d7c-173">"<"</span><span class="sxs-lookup"><span data-stu-id="61d7c-173">"<"</span></span>
- <span data-ttu-id="61d7c-174">">"</span><span class="sxs-lookup"><span data-stu-id="61d7c-174">">"</span></span>
- <span data-ttu-id="61d7c-175">"\leq"</span><span class="sxs-lookup"><span data-stu-id="61d7c-175">"\leq"</span></span>
- <span data-ttu-id="61d7c-176">"\geq"</span><span class="sxs-lookup"><span data-stu-id="61d7c-176">"\geq"</span></span>
- <span data-ttu-id="61d7c-177">"~~"</span><span class="sxs-lookup"><span data-stu-id="61d7c-177">"~~"</span></span>
- <span data-ttu-id="61d7c-178">"~"</span><span class="sxs-lookup"><span data-stu-id="61d7c-178">"~"</span></span>
- <span data-ttu-id="61d7c-179">"\begin{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-179">"\begin{bmatrix}"</span></span>
- <span data-ttu-id="61d7c-180">"\end{bmatrix}"</span><span class="sxs-lookup"><span data-stu-id="61d7c-180">"\end{bmatrix}"</span></span>
- <span data-ttu-id="61d7c-181">"\_"</span><span class="sxs-lookup"><span data-stu-id="61d7c-181">"\_"</span></span>

---

# <a name="quantum-circuits"></a><span data-ttu-id="61d7c-182">Quantum-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="61d7c-182">Quantum Circuits</span></span>
<span data-ttu-id="61d7c-183">Stellen Sie sich einen Moment für die einheitliche Transformation $ \text { CNOT } _ { 01 } (H \otimes 1) vor $ .</span><span class="sxs-lookup"><span data-stu-id="61d7c-183">Consider for a moment the unitary transformation $\text{ CNOT}_{01}(H\otimes 1)$.</span></span>
<span data-ttu-id="61d7c-184">Diese Gate-Sequenz ist von grundlegender Bedeutung für das Quantum Computing, da Sie einen maximalen entbickten zwei-Qubit-Zustand erstellt:</span><span class="sxs-lookup"><span data-stu-id="61d7c-184">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="61d7c-185">$$\mathrm{CNOT } _ { 01 } (H \otimes 1) \ket { 00 } = \frac { 1 } { \sqrt { 2 } } \left ( \ket { 00 }  +  \ket { 11 } \right ),$$</span><span class="sxs-lookup"><span data-stu-id="61d7c-185">$$\mathrm{CNOT}_{01}(H\otimes 1)\ket{00} = \frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right),$$</span></span>

<span data-ttu-id="61d7c-186">Vorgänge mit dieser oder einer größeren Komplexität sind bei Quantum-Algorithmen und der Quantum-Fehlerkorrektur universell. Daher sollte Sie als eine einfache Methode für die Visualisierung bezeichnet werden, die als *Quantum*-Verbindungs Diagramm bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="61d7c-186">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram*.</span></span>
<span data-ttu-id="61d7c-187">Das Verbindungs Diagramm zum Vorbereiten dieses maximale entkoppelt Quantum-Zustands lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="61d7c-187">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<span data-ttu-id="61d7c-188"><!--- ![](.\media\1.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-188"><!--- ![](.\media\1.svg) ---></span></span>
<span data-ttu-id="61d7c-189"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-189"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-190">![Leitungs Diagramm für einen maximalen entzweitigen zwei-Qubit-Zustand](~/media/1.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-190">![Circuit diagram for a maximally entangled two-qubit state](~/media/1.svg)</span></span>

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="61d7c-191">Konventionen für das Quantum Circuit-Diagramm</span><span class="sxs-lookup"><span data-stu-id="61d7c-191">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="61d7c-192">Diese visuelle Sprache für Quantum-Vorgänge kann leichter verdaulich sein als das Schreiben der äquivalenten Matrix, sobald Sie die Konventionen zum Ausdrücken einer Quantum-Verbindung verstanden haben.</span><span class="sxs-lookup"><span data-stu-id="61d7c-192">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="61d7c-193">Wir überprüfen die folgenden Konventionen.</span><span class="sxs-lookup"><span data-stu-id="61d7c-193">We review these conventions below.</span></span>

<span data-ttu-id="61d7c-194">In einem Verbindungs Diagramm zeigt jede voll solide Linie ein Qubit oder mehr im Allgemeinen ein Qubit-Register an.</span><span class="sxs-lookup"><span data-stu-id="61d7c-194">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="61d7c-195">Gemäß der Konvention ist die oberste Zeile Qubit Register $ 0, $ und der Rest wird sequenziell beschriftet.</span><span class="sxs-lookup"><span data-stu-id="61d7c-195">By convention, the top line is qubit register $0$ and the remainder are labeled sequentially.</span></span> <span data-ttu-id="61d7c-196">Die obige Beispiel Verbindung wird als agieren auf zwei Qubits (oder gleichmäßig zwei Register, bestehend aus einem Qubit) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="61d7c-196">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="61d7c-197">Gates, die für ein oder mehrere Qubit-Register agieren, werden als Box bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="61d7c-197">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="61d7c-198">Beispielsweise das Symbol</span><span class="sxs-lookup"><span data-stu-id="61d7c-198">For example, the symbol</span></span>

<span data-ttu-id="61d7c-199"><!--- ![](.\media\2.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-199"><!--- ![](.\media\2.svg) ---></span></span>
<span data-ttu-id="61d7c-200"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-200"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-201">![Symbol für einen Hadamard-Vorgang, der auf einem Single-Qubit-Register agiert](~/media/2.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-201">![Symbol for a Hadamard operation acting on a single-qubit register](~/media/2.svg)</span></span>

<span data-ttu-id="61d7c-202">ist ein [Hadamard](xref:microsoft.quantum.intrinsic.h) -Vorgang, der auf einem Single-Qubit-Register agiert.</span><span class="sxs-lookup"><span data-stu-id="61d7c-202">is a [Hadamard](xref:microsoft.quantum.intrinsic.h) operation acting on a single-qubit register.</span></span>

<span data-ttu-id="61d7c-203">Quantum-Gates werden in chronologischer Reihenfolge mit dem am weitesten links gerichteten Tor sortiert, wenn das Gate zuerst auf die Qubits angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="61d7c-203">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="61d7c-204">Mit anderen Worten: Wenn Sie die Drähte mit dem Quantum-Zustand betrachten, bringen die Drähte den Quantenzustand durch die einzelnen Gates im Diagramm von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="61d7c-204">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="61d7c-205">Das heißt,</span><span class="sxs-lookup"><span data-stu-id="61d7c-205">That is to say</span></span> 

<span data-ttu-id="61d7c-206"><!--- ![](.\media\3.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-206"><!--- ![](.\media\3.svg) ---></span></span>
<span data-ttu-id="61d7c-207"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-207"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-208">![Diagramm der von links nach rechts angewendeten Quantum-Gates](~/media/3.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-208">![Diagram of quantum gates being applied left-to-right](~/media/3.svg)</span></span>

<span data-ttu-id="61d7c-209">ist der einheitliche Matrix- $ CBA $ .</span><span class="sxs-lookup"><span data-stu-id="61d7c-209">is the unitary matrix $CBA$.</span></span>
<span data-ttu-id="61d7c-210">Die Matrix Multiplikation befolgt die gegenteilige Konvention: die ganz rechts gerichtete Matrix wird zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="61d7c-210">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="61d7c-211">In Quantum-Verbindungs Diagrammen wird jedoch das am weitesten links öffnende Gate zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="61d7c-211">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="61d7c-212">Dieser Unterschied kann zu Verwirrung führen. Daher ist es wichtig, dass Sie diesen signifikanten Unterschied zwischen der linearen algebraischen Notation und den quantumleitungs Diagrammen beachten.</span><span class="sxs-lookup"><span data-stu-id="61d7c-212">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="61d7c-213">Eingaben und Ausgaben von Quantum-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="61d7c-213">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="61d7c-214">Alle vorherigen Beispiele haben genau dieselbe Anzahl von Drähten (Qubits) für ein Quantum Gate als die Anzahl von Drähten aus dem Quantum-Gate.</span><span class="sxs-lookup"><span data-stu-id="61d7c-214">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="61d7c-215">Es scheint sinnvoll zu sein, dass Quantum-Verbindungen mehr oder weniger Ausgaben als Eingaben im Allgemeinen haben können.</span><span class="sxs-lookup"><span data-stu-id="61d7c-215">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="61d7c-216">Dies ist jedoch nicht möglich, da alle Quantum-Vorgänge, das Speichern von Messungen, einheitlich und somit umkehrbar sind.</span><span class="sxs-lookup"><span data-stu-id="61d7c-216">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="61d7c-217">Wenn Sie nicht über die gleiche Anzahl von Ausgaben wie Eingaben verfügen, sind Sie nicht umkehrbar und somit nicht einheitlich, was ein Widerspruch ist.</span><span class="sxs-lookup"><span data-stu-id="61d7c-217">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="61d7c-218">Aus diesem Grund muss jedes in einem Verbindungs Diagramm gezeichnete Feld genau die gleiche Anzahl von Drähten aufweisen, die es als beendet eingeben.</span><span class="sxs-lookup"><span data-stu-id="61d7c-218">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="61d7c-219">Multiqubit-Leitungs Diagramme folgen ähnlichen Konventionen wie Single-Qubit.</span><span class="sxs-lookup"><span data-stu-id="61d7c-219">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="61d7c-220">Als Verdeutlichung können wir eine zwei-Qubit-einheitliche Operation B als $ $ $ (H S \otimes X) definieren $ und die Leitung gleichwertig Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="61d7c-220">As a clarifying example, we can define a two-qubit unitary operation $B$ to be $(H S\otimes X)$ and express the circuit equivalently as</span></span>

<span data-ttu-id="61d7c-221"><!--- ![](.\media\4.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-221"><!--- ![](.\media\4.svg) ---></span></span>
<span data-ttu-id="61d7c-222"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-222"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-223">![Leitungs Diagramm eines zwei-Qubit-einheitlichen Vorgangs](~/media/4.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-223">![Circuit diagram of a two-qubit unitary operation](~/media/4.svg)</span></span>

<span data-ttu-id="61d7c-224">Sie können B auch anzeigen, $ $ Wenn eine Aktion für ein einzelnes zwei-Qubit-Register statt 2 1-Qubit registriert ist, je nachdem, in welchem Kontext die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61d7c-224">We can also view $B$ as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="61d7c-225">Vielleicht ist die nützlichste Eigenschaft von solchen abstrakten Verbindungs Diagrammen, dass Sie komplizierte Quantum-Algorithmen auf hoher Ebene beschreiben können, ohne Sie in grundlegende Gates kompilieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="61d7c-225">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="61d7c-226">Dies bedeutet, dass Sie eine intuitions Informationen über den Datenfluss für einen großen Quantum-Algorithmus erhalten können, ohne alle Details zu verstehen, wie die einzelnen Unterroutinen innerhalb des Algorithmus funktionieren.</span><span class="sxs-lookup"><span data-stu-id="61d7c-226">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="61d7c-227">Kontrollierte Gates</span><span class="sxs-lookup"><span data-stu-id="61d7c-227">Controlled gates</span></span>
<span data-ttu-id="61d7c-228">Das andere Konstrukt, das in Multi-Qubit-Quantum-Verbindungs Diagramme integriert ist, ist Control.</span><span class="sxs-lookup"><span data-stu-id="61d7c-228">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="61d7c-229">Die Aktion eines Quorums, das einzeln gesteuert wird $ \Lambda (d), $ wobei der Wert eines einzelnen Qubits die Anwendung von G steuert, $ $ kann durch betrachten des folgenden Beispiels einer Product State input $ \Lambda (g) ( \alpha \ket { 0 }  +  \beta \ket { 1 } ) \ket { \psi } = \alpha \ket { 0 } \ket { \psi }  +  \beta \ket { 1 } G \ket { \psi } $ interpretiert werden. Dies heißt, dass das kontrollierte Gate $ G $ auf das Register anwendet, das nur dann enthält, wenn $ \psi $ das Steuerelement-Qubit den Wert $ 1 annimmt $ .</span><span class="sxs-lookup"><span data-stu-id="61d7c-229">The action of a quantum singly controlled gate, denoted $\Lambda(G)$, where a single qubit's value controls the application of $G$, can be understood by looking at the following example of a product state input $\Lambda(G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket{\psi}$. That is to say, the controlled gate applies $G$ to the register containing $\psi$ if and only if the control qubit takes the value $1$.</span></span>
<span data-ttu-id="61d7c-230">Im Allgemeinen werden solche kontrollierten Vorgänge in Leitungs Diagrammen als</span><span class="sxs-lookup"><span data-stu-id="61d7c-230">In general, we describe such controlled operations in circuit diagrams as</span></span>

<span data-ttu-id="61d7c-231"><!--- ![](.\media\5.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-231"><!--- ![](.\media\5.svg) ---></span></span>
<span data-ttu-id="61d7c-232"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-232"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-233">![Leitungs Diagramm eines einzeln kontrollierten Gates](~/media/5.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-233">![Circuit diagram of a singly controlled gate](~/media/5.svg)</span></span>

<span data-ttu-id="61d7c-234">Hier gibt der schwarze Kreis das Quantum-Bit an, auf dem das Gate gesteuert wird, und ein vertikales Netzwerk gibt den einheitlichen an, der angewendet wird, wenn das Steuerelement-Qubit den Wert $ 1 annimmt $ .</span><span class="sxs-lookup"><span data-stu-id="61d7c-234">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value $1$.</span></span>
<span data-ttu-id="61d7c-235">In den Sonderfällen, in denen $ g = X $ und $ g = Z enthalten $ sind, wird die folgende Notation eingeführt, um die kontrollierte Version der Gates zu beschreiben (Beachten Sie, dass das gesteuerte X-Gate das [ $ CNOT $ Gate](xref:microsoft.quantum.intrinsic.cnot)ist):</span><span class="sxs-lookup"><span data-stu-id="61d7c-235">For the special cases where $G=X$ and $G=Z$ we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [$CNOT$ gate](xref:microsoft.quantum.intrinsic.cnot)):</span></span>

<span data-ttu-id="61d7c-236"><!--- ![](.\media\6.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-236"><!--- ![](.\media\6.svg) ---></span></span>
<span data-ttu-id="61d7c-237"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-237"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-238">![Leitungs Diagramm für Sonderfälle kontrollierter Gates](~/media/6.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-238">![Circuit diagram for special cases of controlled gates](~/media/6.svg)</span></span>

<span data-ttu-id="61d7c-239">Q#stellt Methoden bereit, mit denen die gesteuerte Version eines Vorgangs automatisch generiert werden kann. Dadurch wird der Programmierer daran bewahrt, diese Vorgänge zu codieren.</span><span class="sxs-lookup"><span data-stu-id="61d7c-239">Q# provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="61d7c-240">Ein Beispiel hierfür finden Sie unten:</span><span class="sxs-lookup"><span data-stu-id="61d7c-240">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a><span data-ttu-id="61d7c-241">Mess Operator</span><span class="sxs-lookup"><span data-stu-id="61d7c-241">Measurement operator</span></span>
<span data-ttu-id="61d7c-242">Der verbleibende Vorgang für die Visualisierung in Verbindungs Diagrammen ist Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="61d7c-242">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="61d7c-243">Die Messung nimmt eine Qubit-Registrierung an, misst Sie und gibt das Ergebnis als klassische Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="61d7c-243">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="61d7c-244">Ein Messungs Vorgang wird durch ein Messungs Symbol bezeichnet und übernimmt immer als Eingabe ein Qubit-Register (gekennzeichnet durch eine durch Strichlinie) und gibt klassische Informationen (gekennzeichnet durch eine doppelte Linie) aus.</span><span class="sxs-lookup"><span data-stu-id="61d7c-244">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="61d7c-245">Eine solche unter Leitung sieht insbesondere wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="61d7c-245">Specifically, such a subcircuit looks like:</span></span>

<span data-ttu-id="61d7c-246"><!--- ![](.\media\7.svg) ----></span><span class="sxs-lookup"><span data-stu-id="61d7c-246"><!--- ![](.\media\7.svg) ----></span></span>
<span data-ttu-id="61d7c-247"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-247"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-248">![Symbol, das einen Messungs Vorgang darstellt](~/media/7.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-248">![Symbol representing a measurement operation](~/media/7.svg)</span></span>

<span data-ttu-id="61d7c-249">Q#implementiert zu diesem Zweck einen [Measure-Operator](xref:microsoft.quantum.intrinsic.measure) .</span><span class="sxs-lookup"><span data-stu-id="61d7c-249">Q# implements a [Measure operator](xref:microsoft.quantum.intrinsic.measure) for this purpose.</span></span>
<span data-ttu-id="61d7c-250">Weitere Informationen finden Sie im [Abschnitt zu Messungen](xref:microsoft.quantum.libraries.standard.prelude#measurements) .</span><span class="sxs-lookup"><span data-stu-id="61d7c-250">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="61d7c-251">Ebenso wird die unter Leitung</span><span class="sxs-lookup"><span data-stu-id="61d7c-251">Similarly, the subcircuit</span></span>

<span data-ttu-id="61d7c-252"><!--- ![](.\media\8.svg) ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-252"><!--- ![](.\media\8.svg) ---></span></span>
<span data-ttu-id="61d7c-253"><!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:--></span><span class="sxs-lookup"><span data-stu-id="61d7c-253"><!-- Can't find a way to easily center this... probably an extension needed:  --></span></span>
<span data-ttu-id="61d7c-254">![Leitungs Diagramm, das einen kontrollierten Vorgang darstellt](~/media/8.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-254">![Circuit diagram representing a controlled operation](~/media/8.svg)</span></span>

<span data-ttu-id="61d7c-255">bietet ein klassisch kontrolliertes Gate, wobei $ G $ auf das klassische Steuerelement Bit, das Wert 1 ist, angewendet wird $ $ .</span><span class="sxs-lookup"><span data-stu-id="61d7c-255">gives a classically controlled gate, where $G$ is applied conditioned on the classical control bit being value $1$.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="61d7c-256">Teleportations-Verbindungs Diagramm</span><span class="sxs-lookup"><span data-stu-id="61d7c-256">Teleportation circuit diagram</span></span>
<span data-ttu-id="61d7c-257">Quantum-Teleportation ist möglicherweise der beste Quantum-Algorithmus für die Veranschaulichung dieser Komponenten.</span><span class="sxs-lookup"><span data-stu-id="61d7c-257">Quantum teleportation is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="61d7c-258">Sie können sich mit der entsprechenden [quanturequantum](xref:microsoft.quantum.overview.katas) -Teleportation vertraut machen. Dies ist eine Methode zum Verschieben von Daten innerhalb eines Quantum-Computers (oder sogar zwischen entfernten Quantum-Computern in einem Quantum-Netzwerk) durch die Verwendung von jede Verflechtungen und Messungen.</span><span class="sxs-lookup"><span data-stu-id="61d7c-258">You can learn hands-on with the corresponding [Quantum Kata](xref:microsoft.quantum.overview.katas) Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="61d7c-259">Interessanterweise ist es in der Lage, einen Quantenzustand, z. b. den Wert in einem bestimmten Qubit, von einem Qubit zu einem anderen zu verschieben, ohne dass Sie wissen, was der Qubit-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="61d7c-259">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="61d7c-260">Dies ist erforderlich, damit das Protokoll gemäß den Gesetzen der Quantum-Mechanik funktioniert.</span><span class="sxs-lookup"><span data-stu-id="61d7c-260">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="61d7c-261">Die Verbindung mit der Quantum-Teleportation ist unten angegeben. Außerdem wird eine Version der Verbindung mit Anmerkungen bereitgestellt, um zu veranschaulichen, wie die Quantum-Verbindung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="61d7c-261">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<span data-ttu-id="61d7c-262"><!--- ![](.\media\tp2.svg) { Breite = 50%} ---></span><span class="sxs-lookup"><span data-stu-id="61d7c-262"><!--- ![](.\media\tp2.svg){ width=50% } ---></span></span>
<span data-ttu-id="61d7c-263">![Quantum-Teleportations-Leitung](~/media/tp2.svg)</span><span class="sxs-lookup"><span data-stu-id="61d7c-263">![Quantum teleportation circuit](~/media/tp2.svg)</span></span>
