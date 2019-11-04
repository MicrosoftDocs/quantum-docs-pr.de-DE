---
title: Quantum-Leitungen | Microsoft-Dokumentation
description: Quantum-Verbindungen
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 7c2afa58fd70d893529cf794ae07df480466aaec
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2019
ms.locfileid: "73210675"
---
# <a name="quantum-circuits"></a><span data-ttu-id="64351-103">Quantum-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="64351-103">Quantum Circuits</span></span>
<span data-ttu-id="64351-104">Beachten Sie für einen Moment die einheitliche Transformation $ \text{CNOT} _{01}(h\otimes 1) $.</span><span class="sxs-lookup"><span data-stu-id="64351-104">Consider for a moment the unitary transformation $\text{ CNOT}_{01}(H\otimes 1)$.</span></span>
<span data-ttu-id="64351-105">Diese Gate-Sequenz ist von grundlegender Bedeutung für das Quantum Computing, da Sie einen maximalen entbickten zwei-Qubit-Zustand erstellt:</span><span class="sxs-lookup"><span data-stu-id="64351-105">This gate sequence is of fundamental significance to quantum computing because it creates a maximally entangled two-qubit state:</span></span>

<span data-ttu-id="64351-106">$ $ \mathrm{CNOT}_{01}(h\otimes 1) \ket{00} = \frac{1}{\sqrt{2}} \left (\ket{00} + \ket{11} \right), $ $</span><span class="sxs-lookup"><span data-stu-id="64351-106">$$\mathrm{CNOT}_{01}(H\otimes 1)\ket{00} = \frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right),$$</span></span>

<span data-ttu-id="64351-107">Vorgänge mit dieser oder einer größeren Komplexität sind bei Quantum-Algorithmen und der Quantum-Fehlerkorrektur universell. Daher sollte Sie als eine einfache Methode für die Visualisierung bezeichnet werden, die als *Quantum*-Verbindungs Diagramm bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="64351-107">Operations with this or greater complexity are ubiquitous in quantum algorithms and quantum error correction, so it should come as a great relief that there is a simple method for their visualization called a *quantum circuit diagram*.</span></span>
<span data-ttu-id="64351-108">Das Verbindungs Diagramm zum Vorbereiten dieses maximale entkoppelt Quantum-Zustands lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="64351-108">The circuit diagram for preparing this maximally entangled quantum state is:</span></span>

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/Concepts1.png)

## <a name="quantum-circuit-diagram-conventions"></a><span data-ttu-id="64351-109">Konventionen für das Quantum Circuit-Diagramm</span><span class="sxs-lookup"><span data-stu-id="64351-109">Quantum circuit diagram conventions</span></span>
<span data-ttu-id="64351-110">Diese visuelle Sprache für Quantum-Vorgänge kann leichter verdaulich sein als das Schreiben der äquivalenten Matrix, sobald Sie die Konventionen zum Ausdrücken einer Quantum-Verbindung verstanden haben.</span><span class="sxs-lookup"><span data-stu-id="64351-110">This visual language for quantum operations can be more readily digestible than writing down its equivalent matrix once you understand the conventions for expressing a quantum circuit.</span></span>
<span data-ttu-id="64351-111">Wir überprüfen die folgenden Konventionen.</span><span class="sxs-lookup"><span data-stu-id="64351-111">We review these conventions below.</span></span>

<span data-ttu-id="64351-112">In einem Verbindungs Diagramm zeigt jede voll solide Linie ein Qubit oder mehr im Allgemeinen ein Qubit-Register an.</span><span class="sxs-lookup"><span data-stu-id="64351-112">In a circuit diagram, each solid line depicts a qubit or more generally a qubit register.</span></span>
<span data-ttu-id="64351-113">Gemäß der Konvention ist die oberste Zeile Qubit-Register $0 $, und der Rest wird sequenziell beschriftet.</span><span class="sxs-lookup"><span data-stu-id="64351-113">By convention, the top line is qubit register $0$ and the remainder are labeled sequentially.</span></span> <span data-ttu-id="64351-114">Die obige Beispiel Verbindung wird als agieren auf zwei Qubits (oder gleichmäßig zwei Register, bestehend aus einem Qubit) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="64351-114">The above example circuit is depicted as acting on two qubits (or equivalently two registers consisting of one qubit).</span></span>
<span data-ttu-id="64351-115">Gates, die für ein oder mehrere Qubit-Register agieren, werden als Box bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="64351-115">Gates acting on one or more qubit registers are denoted as a box.</span></span>
<span data-ttu-id="64351-116">Beispielsweise das Symbol</span><span class="sxs-lookup"><span data-stu-id="64351-116">For example, the symbol</span></span>

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/concepts_2.png)

<span data-ttu-id="64351-117">Das [Hadamard](xref:microsoft.quantum.primitive.h) -Gate, das für ein Single-Qubit-Register fungiert.</span><span class="sxs-lookup"><span data-stu-id="64351-117">is the [Hadamard](xref:microsoft.quantum.primitive.h) gate acting on a single-qubit register.</span></span>

<span data-ttu-id="64351-118">Quantum-Gates werden in chronologischer Reihenfolge mit dem am weitesten links gerichteten Tor sortiert, wenn das Gate zuerst auf die Qubits angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="64351-118">Quantum gates are ordered in chronological order with the left-most gate as the gate first applied to the qubits.</span></span>
<span data-ttu-id="64351-119">Mit anderen Worten: Wenn Sie die Drähte mit dem Quantum-Zustand betrachten, bringen die Drähte den Quantenzustand durch die einzelnen Gates im Diagramm von links nach rechts.</span><span class="sxs-lookup"><span data-stu-id="64351-119">In other words, if you picture the wires as holding the quantum state, the wires bring the quantum state through each of the gates in the diagram from left to right.</span></span>
<span data-ttu-id="64351-120">Das heißt,</span><span class="sxs-lookup"><span data-stu-id="64351-120">That is to say</span></span> 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/concepts_3.png)

<span data-ttu-id="64351-121">ist die einheitliche Matrix $CBA $.</span><span class="sxs-lookup"><span data-stu-id="64351-121">is the unitary matrix $CBA$.</span></span>
<span data-ttu-id="64351-122">Die Matrix Multiplikation befolgt die gegenteilige Konvention: die ganz rechts gerichtete Matrix wird zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="64351-122">Matrix multiplication obeys the opposite convention: the right-most matrix is applied first.</span></span> <span data-ttu-id="64351-123">In Quantum-Verbindungs Diagrammen wird jedoch das am weitesten links öffnende Gate zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="64351-123">In quantum circuit diagrams, however, the left-most gate is applied first.</span></span>
<span data-ttu-id="64351-124">Dieser Unterschied kann zu Verwirrung führen. Daher ist es wichtig, dass Sie diesen signifikanten Unterschied zwischen der linearen algebraischen Notation und den quantumleitungs Diagrammen beachten.</span><span class="sxs-lookup"><span data-stu-id="64351-124">This difference can at times lead to confusion, so it is important to note this significant difference between the linear algebraic notation and quantum circuit diagrams.</span></span>

## <a name="inputs-and-outputs-of-quantum-circuits"></a><span data-ttu-id="64351-125">Eingaben und Ausgaben von Quantum-Verbindungen</span><span class="sxs-lookup"><span data-stu-id="64351-125">Inputs and outputs of quantum circuits</span></span>
<span data-ttu-id="64351-126">Alle vorherigen Beispiele haben genau dieselbe Anzahl von Drähten (Qubits) für ein Quantum Gate als die Anzahl von Drähten aus dem Quantum-Gate.</span><span class="sxs-lookup"><span data-stu-id="64351-126">All previous examples given have had precisely the same number of wires (qubits) input to a quantum gate as the number of wires out from the quantum gate.</span></span>
<span data-ttu-id="64351-127">Es scheint sinnvoll zu sein, dass Quantum-Verbindungen mehr oder weniger Ausgaben als Eingaben im Allgemeinen haben können.</span><span class="sxs-lookup"><span data-stu-id="64351-127">It may at first seem reasonable that quantum circuits could have more, or fewer, outputs than inputs in general.</span></span>
<span data-ttu-id="64351-128">Dies ist jedoch nicht möglich, da alle Quantum-Vorgänge, das Speichern von Messungen, einheitlich und somit umkehrbar sind.</span><span class="sxs-lookup"><span data-stu-id="64351-128">This is impossible, however, because all quantum operations, save measurement, are unitary and hence reversible.</span></span>
<span data-ttu-id="64351-129">Wenn Sie nicht über die gleiche Anzahl von Ausgaben wie Eingaben verfügen, sind Sie nicht umkehrbar und somit nicht einheitlich, was ein Widerspruch ist.</span><span class="sxs-lookup"><span data-stu-id="64351-129">If they did not have the same number of outputs as inputs they would not be reversible and hence not unitary, which is a contradiction.</span></span>
<span data-ttu-id="64351-130">Aus diesem Grund muss jedes in einem Verbindungs Diagramm gezeichnete Feld genau die gleiche Anzahl von Drähten aufweisen, die es als beendet eingeben.</span><span class="sxs-lookup"><span data-stu-id="64351-130">For this reason any box drawn in a circuit diagram must have precisely the same number of wires entering it as exiting it.</span></span>

<span data-ttu-id="64351-131">Multiqubit-Leitungs Diagramme folgen ähnlichen Konventionen wie Single-Qubit.</span><span class="sxs-lookup"><span data-stu-id="64351-131">Multi-qubit circuit diagrams follow similar conventions to single-qubit ones.</span></span>
<span data-ttu-id="64351-132">Als Verdeutlichung können wir eine zwei-Qubit-einheitliche Operation definieren, $B $ bis $ (H s\otimes X) $ ist, und die Leitung gleichwertig Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="64351-132">As a clarifying example, we can define a two-qubit unitary operation $B$ to be $(H S\otimes X)$ and express the circuit equivalently as</span></span>

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/concepts_4.png)

<span data-ttu-id="64351-133">Wir können $B $ auch anzeigen, wenn eine Aktion in einem einzigen zwei-Qubit-Register statt 2 1-Qubit registriert ist, je nachdem, in welchem Kontext die Verbindung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64351-133">We can also view $B$ as having an action on a single two-qubit register rather than two one-qubit registers depending on the context in which the circuit is used.</span></span> <span data-ttu-id="64351-134">Vielleicht ist die nützlichste Eigenschaft von solchen abstrakten Verbindungs Diagrammen, dass Sie komplizierte Quantum-Algorithmen auf hoher Ebene beschreiben können, ohne Sie in grundlegende Gates kompilieren zu müssen.</span><span class="sxs-lookup"><span data-stu-id="64351-134">Perhaps the most useful property of such abstract circuit diagrams is that they allow complicated quantum algorithms to be described at a high level without having to compile them down to fundamental gates.</span></span>
<span data-ttu-id="64351-135">Dies bedeutet, dass Sie eine intuitions Informationen über den Datenfluss für einen großen Quantum-Algorithmus erhalten können, ohne alle Details zu verstehen, wie die einzelnen Unterroutinen innerhalb des Algorithmus funktionieren.</span><span class="sxs-lookup"><span data-stu-id="64351-135">This means that you can get an intuition about the data flow for a large quantum algorithm without needing to understand all the details of how each of the subroutines within the algorithm work.</span></span>

## <a name="controlled-gates"></a><span data-ttu-id="64351-136">Kontrollierte Gates</span><span class="sxs-lookup"><span data-stu-id="64351-136">Controlled gates</span></span>
<span data-ttu-id="64351-137">Das andere Konstrukt, das in Multi-Qubit-Quantum-Verbindungs Diagramme integriert ist, ist Control.</span><span class="sxs-lookup"><span data-stu-id="64351-137">The other construct that is built into multi-qubit quantum circuit diagrams is control.</span></span>
<span data-ttu-id="64351-138">Die Aktion eines durch eine quot;-Steuerelement gesteuerten Tors, die den Wert $ \lambda (g) $ bezeichnet, wobei der Wert eines einzelnen Qubits die Anwendung von $G $ steuert, kann durch betrachten des folgenden Beispiels einer Product State Input $ \lambda (g) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} g\ket {\ psi} $.</span><span class="sxs-lookup"><span data-stu-id="64351-138">The action of a quantum singly controlled gate, denoted $\Lambda(G)$, where a single qubit's value controls the application of $G$, can be understood by looking at the following example of a product state input $\Lambda(G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket{\psi}$.</span></span>
<span data-ttu-id="64351-139">Dies heißt, dass das gesteuerte Gate $G $ auf das Register anwendet, das $ \psi $ if enthält, und nur, wenn das Steuerelement Qubit den Wert $1 $ annimmt.</span><span class="sxs-lookup"><span data-stu-id="64351-139">That is to say, the controlled gate applies $G$ to the register containing $\psi$ if and only if the control qubit takes the value $1$.</span></span>
<span data-ttu-id="64351-140">Im Allgemeinen werden solche kontrollierten Vorgänge in Leitungs Diagrammen als</span><span class="sxs-lookup"><span data-stu-id="64351-140">In general, we describe such controlled operations in circuit diagrams as</span></span>

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/concepts_5.png)

<span data-ttu-id="64351-141">Hier gibt der schwarze Kreis das Quantum-Bit an, auf dem das Gate gesteuert wird, und ein vertikales Netzwerk bezeichnet die einheitliche, die angewendet wird, wenn das Steuerelement-Qubit den Wert $1 $ annimmt.</span><span class="sxs-lookup"><span data-stu-id="64351-141">Here the black circle denotes the quantum bit on which the gate is controlled and a vertical wire denotes the unitary that is applied when the control qubit takes the value $1$.</span></span>
<span data-ttu-id="64351-142">In den Sonderfällen, in denen $G = X $ und $G = Z $ steht, wird die folgende Notation eingeführt, um die kontrollierte Version der Gates zu beschreiben (Beachten Sie, dass das gesteuerte X-Gate der [$CNOT $ Gate](xref:microsoft.quantum.primitive.cnot)ist):</span><span class="sxs-lookup"><span data-stu-id="64351-142">For the special cases where $G=X$ and $G=Z$ we introduce the following notation to describe the controlled version of the gates (note that the controlled-X gate is the [$CNOT$ gate](xref:microsoft.quantum.primitive.cnot)):</span></span>

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/concepts_6.png)

<span data-ttu-id="64351-143">Q # stellt Methoden bereit, mit denen die gesteuerte Version eines Vorgangs automatisch generiert werden kann. Dadurch wird der Programmierer daran bewahrt, diese Vorgänge zu codieren.</span><span class="sxs-lookup"><span data-stu-id="64351-143">Q# provides methods to automatically generate the controlled version of an operation, which saves the programmer from having to hand code these operations.</span></span> <span data-ttu-id="64351-144">Ein Beispiel hierfür finden Sie unten:</span><span class="sxs-lookup"><span data-stu-id="64351-144">An example of this is shown below:</span></span>

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a><span data-ttu-id="64351-145">Mess Operator</span><span class="sxs-lookup"><span data-stu-id="64351-145">Measurement operator</span></span>
<span data-ttu-id="64351-146">Der verbleibende Vorgang für die Visualisierung in Verbindungs Diagrammen ist Maßeinheit.</span><span class="sxs-lookup"><span data-stu-id="64351-146">The remaining operation to visualize in circuit diagrams is measurement.</span></span>
<span data-ttu-id="64351-147">Die Messung nimmt eine Qubit-Registrierung an, misst Sie und gibt das Ergebnis als klassische Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="64351-147">Measurement takes a qubit register, measures it, and outputs the result as classical information.</span></span>
<span data-ttu-id="64351-148">Ein Messungs Vorgang wird durch ein Messungs Symbol bezeichnet und übernimmt immer als Eingabe ein Qubit-Register (gekennzeichnet durch eine durch Strichlinie) und gibt klassische Informationen (gekennzeichnet durch eine doppelte Linie) aus.</span><span class="sxs-lookup"><span data-stu-id="64351-148">A measurement operation is denoted by a meter symbol and always takes as input a qubit register (denoted by a solid line) and outputs classical information (denoted by a double line).</span></span>
<span data-ttu-id="64351-149">Eine solche unter Leitung sieht insbesondere wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="64351-149">Specifically, such a subcircuit looks like:</span></span>

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
<span data-ttu-id="64351-150">![Messungs Verbindung](~/media/concepts_7.png)</span><span class="sxs-lookup"><span data-stu-id="64351-150">![Measurement circuit](~/media/concepts_7.png)</span></span>

<span data-ttu-id="64351-151">F # implementiert zu diesem Zweck einen [Measure-Operator](xref:microsoft.quantum.primitive.measure) .</span><span class="sxs-lookup"><span data-stu-id="64351-151">Q# implements a [Measure operator](xref:microsoft.quantum.primitive.measure) for this purpose.</span></span>
<span data-ttu-id="64351-152">Weitere Informationen finden Sie im [Abschnitt zu Messungen](xref:microsoft.quantum.libraries.standard.prelude#measurements) .</span><span class="sxs-lookup"><span data-stu-id="64351-152">See the [section on measurements](xref:microsoft.quantum.libraries.standard.prelude#measurements) for more information.</span></span>

<span data-ttu-id="64351-153">Ebenso wird die unter Leitung</span><span class="sxs-lookup"><span data-stu-id="64351-153">Similarly, the subcircuit</span></span>

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![](~/media/concepts_8.png)

<span data-ttu-id="64351-154">bietet ein klassisch kontrolliertes Gate, bei dem $G $ auf das klassische Steuerungs Bit angewendet wird, das den Wert $1 $ hat.</span><span class="sxs-lookup"><span data-stu-id="64351-154">gives a classically controlled gate, where $G$ is applied conditioned on the classical control bit being value $1$.</span></span>

## <a name="teleportation-circuit-diagram"></a><span data-ttu-id="64351-155">Teleportations-Verbindungs Diagramm</span><span class="sxs-lookup"><span data-stu-id="64351-155">Teleportation circuit diagram</span></span>
<span data-ttu-id="64351-156">[Quantum-Teleportation](xref:microsoft.quantum.techniques.puttingittogether) ist möglicherweise der beste Quantum-Algorithmus für die Veranschaulichung dieser Komponenten.</span><span class="sxs-lookup"><span data-stu-id="64351-156">[Quantum teleportation](xref:microsoft.quantum.techniques.puttingittogether) is perhaps the best quantum algorithm for illustrating these components.</span></span>
<span data-ttu-id="64351-157">Die Quantum-Teleportation ist eine Methode zum Verschieben von Daten innerhalb eines Quantum-Computers (oder sogar zwischen entfernten Quantum-Computern in einem Quantum-Netzwerk) durch die Verwendung von jede Verflechtungen und Messungen.</span><span class="sxs-lookup"><span data-stu-id="64351-157">Quantum teleportation is a method for moving data within a quantum computer (or even between distant quantum computers in a quantum network) through the use of entanglement and measurement.</span></span>
<span data-ttu-id="64351-158">Interessanterweise ist es in der Lage, einen Quantenzustand, z. b. den Wert in einem bestimmten Qubit, von einem Qubit zu einem anderen zu verschieben, ohne dass Sie wissen, was der Qubit-Wert ist.</span><span class="sxs-lookup"><span data-stu-id="64351-158">Interestingly, it is actually capable of moving a quantum state, say the value in a given qubit, from one qubit to another, without even knowing what the qubit's value is!</span></span>
<span data-ttu-id="64351-159">Dies ist erforderlich, damit das Protokoll gemäß den Gesetzen der Quantum-Mechanik funktioniert.</span><span class="sxs-lookup"><span data-stu-id="64351-159">This is necessary for the protocol to work according to the laws of quantum mechanics.</span></span>
<span data-ttu-id="64351-160">Die Verbindung mit der Quantum-Teleportation ist unten angegeben. Außerdem wird eine Version der Verbindung mit Anmerkungen bereitgestellt, um zu veranschaulichen, wie die Quantum-Verbindung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="64351-160">The quantum teleportation circuit is given below; we also provide an annotated version of the circuit to illustrate how to read the quantum circuit.</span></span>

<!--- ![](.\media\tp2.svg){ width=50% } --->
![](~/media/concepts_tp2.png)
