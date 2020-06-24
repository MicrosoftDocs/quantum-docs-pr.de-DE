---
title: Pauli-Messungen
description: Erfahren Sie, wie Sie mit Einzel-und Multi-Qubit-Pauli-Mess Vorgängen arbeiten.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
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
ms.openlocfilehash: 7f10c4ad5eb325da97552d60ff47ea89a699f08d
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269472"
---
# <a name="pauli-measurements"></a><span data-ttu-id="6d043-103">Pauli-Messungen</span><span class="sxs-lookup"><span data-stu-id="6d043-103">Pauli Measurements</span></span>

<span data-ttu-id="6d043-104">In den vorherigen Diskussionen haben wir uns auf Berechnungsbasis Messungen konzentriert.</span><span class="sxs-lookup"><span data-stu-id="6d043-104">In the previous discussions, we have focused on computational basis measurements.</span></span>
<span data-ttu-id="6d043-105">Tatsächlich gibt es weitere allgemeine Messungen, die bei der Quantum-Berechnung auftreten, die aus Sicht der Sicht bequem in Bezug auf Berechnungsbasis Messungen ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="6d043-105">In fact, there are other common measurements that occur in quantum computing that, from a notational perspective, are convenient to express in terms of computational basis measurements.</span></span>
<span data-ttu-id="6d043-106">Bei der Arbeit mit Q # sind die gängigsten Arten von Messungen wahrscheinlich *Pauli-Messungen*, die Berechnungsbasis Messungen verallgemeinern, um Messungen in anderen Basen und die Parität zwischen verschiedenen Qubits zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="6d043-106">As you work with Q#, the most common kind of measurements that you'll run into will likely be *Pauli measurements*, which generalize computational basis measurements to include measurements in other bases, and of parity between different qubits.</span></span>
<span data-ttu-id="6d043-107">In solchen Fällen ist es üblich, das Messen eines Pauli-Operators zu erörtern, im Allgemeinen ein Operator wie $X, Y, Z $ oder $Z \otimes Z, x \otimes x, x \otimes Y $ usw.</span><span class="sxs-lookup"><span data-stu-id="6d043-107">In such cases, it is common to discuss measuring a Pauli operator, in general an operator such as $X,Y,Z$ or $Z\otimes Z, X\otimes X, X\otimes Y$, and so forth.</span></span>

> [!TIP]
> <span data-ttu-id="6d043-108">In Q # werden multiqubit-Pauli-Operatoren in der Regel durch Arrays des Typs dargestellt `Pauli[]` .</span><span class="sxs-lookup"><span data-stu-id="6d043-108">In Q#, multi-qubit Pauli operators are generally represented by arrays of type `Pauli[]`.</span></span>
> <span data-ttu-id="6d043-109">Wenn Sie z. b. $X \otimes Z \otimes Y darstellen möchten $ , können Sie das Array verwenden `[PauliX, PauliZ, PauliY]` .</span><span class="sxs-lookup"><span data-stu-id="6d043-109">For example, to represent $X \otimes Z \otimes Y$, you can use the array `[PauliX, PauliZ, PauliY]`.</span></span>

<span data-ttu-id="6d043-110">Die Erörterung von Messungen in Form von Pauli-Operatoren ist vor allem im Unterfeld der Quantum-Fehlerkorrektur üblich.</span><span class="sxs-lookup"><span data-stu-id="6d043-110">Discussing measurement in terms of Pauli operators is especially common in the subfield of quantum error correction.</span></span>
<span data-ttu-id="6d043-111">In f # wird eine ähnliche Konvention befolgt. Wir erläutern nun diese Alternative Ansicht von Messungen.</span><span class="sxs-lookup"><span data-stu-id="6d043-111">In Q#, we follow a similar convention; we now explain this alternative view of measurements.</span></span>

<span data-ttu-id="6d043-112">Bevor wir uns mit den Details der Bedeutung einer Pauli-Messung beschäftigen, ist es sinnvoll, sich Gedanken darüber zu machen, was ein einzelnes Qubit innerhalb eines Quantum-Computers in den Quantum-Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="6d043-112">Before delving into the details of how to think of a Pauli measurement, it is useful to think about what measuring a single qubit inside a quantum computer does to the quantum state.</span></span>
<span data-ttu-id="6d043-113">Stellen Sie sich vor, dass ein $n $ -Qubit-Quantum-Status vorhanden ist. Anschließend wird ein Qubit sofort mit der Hälfte der $2 ^ n- $ Möglichkeiten, in denen sich der Zustand befindet, fest.</span><span class="sxs-lookup"><span data-stu-id="6d043-113">Imagine that we have an $n$-qubit quantum state; then measuring one qubit immediately rules out half of the $2^n$ possibilities that state could be in.</span></span>
<span data-ttu-id="6d043-114">Mit anderen Worten: die Messung projiziert den Quantum-Zustand auf einen von zwei halben Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="6d043-114">In other words, the measurement projects the quantum state onto one of two half-spaces.</span></span>
<span data-ttu-id="6d043-115">Wir können die Art und Weise verallgemeinern, in der Messungen für diese Intuition durchdacht werden.</span><span class="sxs-lookup"><span data-stu-id="6d043-115">We can generalize the way we think about measurement to reflect this intuition.</span></span>

<span data-ttu-id="6d043-116">Um diese Teilbereiche zu beschreiben, benötigen wir eine Sprache für die Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="6d043-116">In order to concisely identify these subspaces, we need a language for describing them.</span></span>
<span data-ttu-id="6d043-117">Eine Möglichkeit, die beiden Teilbereiche zu beschreiben, besteht darin, Sie durch eine Matrix anzugeben, die nur zwei eindeutige Eigenwerte hat, die gemäß der Konvention $ \pm 1 übernommen werden $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-117">One way to describe the two subspaces is by specifying them through a matrix that just has two unique eigenvalues, taken by convention to be $\pm 1$.</span></span>
<span data-ttu-id="6d043-118">Um ein einfaches Beispiel für das Beschreiben von Teilbereichen auf diese Weise zu beschreiben, sollten Sie $Z beachten $ :</span><span class="sxs-lookup"><span data-stu-id="6d043-118">For a simple example of describing subspaces in this way, consider $Z$:</span></span>

<span data-ttu-id="6d043-119">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-119">$$ \begin{align}</span></span>
  <span data-ttu-id="6d043-120">Z & = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="6d043-120">Z & = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="6d043-121">\end{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-121">\end{align}</span></span>
$$

<span data-ttu-id="6d043-122">Wenn Sie die diagonalen Elemente der Pauli-$Z $ Matrix lesen, sehen Sie, dass $Z $ zwei Eigenvektoren, $ \ket{0$ } und $ \ket{1$ } , mit den entsprechenden eigen Werten $ \pm 1 aufweist $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-122">By reading the diagonal elements of the Pauli-$Z$ matrix, we can see that $Z$ has two eigenvectors, $\ket{0}$ and $\ket{1}$, with corresponding eigenvalues $\pm 1$.</span></span>
<span data-ttu-id="6d043-123">Wenn wir also das Qubit Messen und Abrufen `Zero` (entsprechend dem Status $ \ket{0$ } ), wissen wir, dass der Status des Qubit ein $ + 1-Zustand $ des $Z Operators ist $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-123">Thus, if we measure the qubit and obtain `Zero` (corresponding to the state $\ket{0}$), we know that the state of our qubit is a $+1$ eigenstate of the $Z$ operator.</span></span>
<span data-ttu-id="6d043-124">Ebenso wissen wir, wenn wir `One` , dass der Zustand unseres Qubit ein "$-1"- $ Zustand der $Z ist $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-124">Similarly, if we obtain `One`, we know that the state of our qubit is a $-1$ eigenstate of $Z$.</span></span>
<span data-ttu-id="6d043-125">Dieser Prozess wird in der Sprache von Pauli-Messungen als "Messen von Pauli $Z $ " bezeichnet und ist vollständig mit der Durchführung einer Berechnungsbasis Messung identisch.</span><span class="sxs-lookup"><span data-stu-id="6d043-125">This process is referred to in the language of Pauli measurements as "measuring Pauli $Z$," and is entirely equivalent to performing a computational basis measurement.</span></span>

<span data-ttu-id="6d043-126">Jede $2 \times 2- $ Matrix, die eine einheitliche Transformation von $Z ist, $ erfüllt diese Kriterien ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="6d043-126">Any $2\times 2$ matrix that is a unitary transformation of $Z$ also satisfies this criteria.</span></span>
<span data-ttu-id="6d043-127">Das heißt, wir könnten auch eine Matrix $A = U ^ \dagger Z U verwenden $ , wobei $U eine $ beliebige andere einheitliche Matrix ist, um eine Matrix zu erstellen, die die beiden Ergebnisse einer Messung in den $ \pm 1- $ Eigenvektoren definiert.</span><span class="sxs-lookup"><span data-stu-id="6d043-127">That is, we could also use a matrix $A=U^\dagger Z U$, where $U$ is any other unitary matrix, to give a matrix that defines the two outcomes of a measurement in its $\pm 1$ eigenvectors.</span></span>
<span data-ttu-id="6d043-128">Die Notation von Pauli-Messungen verweist auf diese einheitliche Äquivalenz, indem $X-, Y-und Z- $ Messungen als gleichwertige Messungen identifiziert werden, die zur Gewinnung von Informationen aus einem Qubit führen könnten.</span><span class="sxs-lookup"><span data-stu-id="6d043-128">The notation of Pauli measurements references this unitary equivalence by identifying $X,Y,Z$ measurements as equivalent measurements that one could do to gain information from a qubit.</span></span>
<span data-ttu-id="6d043-129">Diese Messungen werden zur einfacheren Verwendung unten angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d043-129">These measurements are given below for convenience.</span></span>


|<span data-ttu-id="6d043-130">Pauli-Messung</span><span class="sxs-lookup"><span data-stu-id="6d043-130">Pauli Measurement</span></span>  |<span data-ttu-id="6d043-131">Einheitliche Transformation</span><span class="sxs-lookup"><span data-stu-id="6d043-131">Unitary transformation</span></span>  |
|-------------------|------------------------|
| <span data-ttu-id="6d043-132">$Z$</span><span class="sxs-lookup"><span data-stu-id="6d043-132">$Z$</span></span>               | <span data-ttu-id="6d043-133">$ \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-133">$\boldone$</span></span>             |
| <span data-ttu-id="6d043-134">$X$</span><span class="sxs-lookup"><span data-stu-id="6d043-134">$X$</span></span>               | <span data-ttu-id="6d043-135">$H$</span><span class="sxs-lookup"><span data-stu-id="6d043-135">$H$</span></span>                    |
| <span data-ttu-id="6d043-136">$Y$</span><span class="sxs-lookup"><span data-stu-id="6d043-136">$Y$</span></span>               | <span data-ttu-id="6d043-137">$HS ^ {\dagger}$</span><span class="sxs-lookup"><span data-stu-id="6d043-137">$HS^{\dagger}$</span></span>         |

<span data-ttu-id="6d043-138">Das heißt, "Measure $Y $ " entspricht der Anwendung von $HS ^ \dagger $ und der anschließenden Messung, wobei ein System interner [`S`](xref:microsoft.quantum.intrinsic.s) Quantum-Vorgang ist, der manchmal als "Phasen Gate" bezeichnet wird, und durch die einheitliche Matrix simuliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6d043-138">That is, using this language, "measure $Y$" is equivalent to applying $HS^\dagger$ and then measuring in the computational basis, where [`S`](xref:microsoft.quantum.intrinsic.s) is an intrinsic quantum operation sometimes called the "phase gate," and can be simulated by the unitary matrix</span></span>

<span data-ttu-id="6d043-139">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-139">$$ \begin{align}</span></span>
    <span data-ttu-id="6d043-140">S = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="6d043-140">S = \begin{bmatrix}</span></span>
        <span data-ttu-id="6d043-141">1 & 0 \\ \\ 0 & i \end{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="6d043-141">1 & 0 \\\\ 0 & i \end{bmatrix}.</span></span>
<span data-ttu-id="6d043-142">\end{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-142">\end{align}</span></span>
$$

<span data-ttu-id="6d043-143">Dies entspricht auch dem Anwenden von $HS ^ \dagger $ auf den Quantum-Status Vektor und dem anschließenden Messen $Z $ , sodass der folgende Vorgang dem entspricht `Measure([PauliY], [q])` :</span><span class="sxs-lookup"><span data-stu-id="6d043-143">It is also equivalent to applying $HS^\dagger$ to the quantum state vector and then measuring $Z$, such that the following operation is equivalent to `Measure([PauliY], [q])`:</span></span>

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

<span data-ttu-id="6d043-144">Der richtige Zustand wird dann durch umwandeln auf die Berechnungsbasis gefunden, was das Anwenden $ von $SH auf den Quanten Zustands Vektor bedeutet. im obigen Code Ausschnitt wird die Transformation zurück zur Berechnungsbasis automatisch durch die Verwendung des- `within … apply` Blocks verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6d043-144">The correct state would then be found by transforming back to the computational basis, which amounts to applying $SH$ to the quantum state vector; in the above snippet, the transformation back to the computational basis is handled automatically by the use of the `within … apply` block.</span></span>

<span data-ttu-id="6d043-145">In f # wird das Ergebnis---, das heißt, die klassischen Informationen, die aus der Interaktion mit dem Status---extrahiert werden, werden durch einen `Result` Wert $j \in \\ {\texttt{Zero } , \texttt{One} $ angegeben, der } \\ angibt, ob das Ergebnis im $ (-1) ^ j- $ eigen Raum des angehängten Pauli-Operators ist.</span><span class="sxs-lookup"><span data-stu-id="6d043-145">In Q#, we say the outcome---that is, the classical information extracted from interacting with the state---is given by a `Result` value $j \in \\{\texttt{Zero}, \texttt{One}\\}$ indicating if the result is in the $(-1)^j$ eigenspace of the Pauli operator measured.</span></span>


## <a name="multiple-qubit-measurements"></a><span data-ttu-id="6d043-146">Multiple-Qubit-Messungen</span><span class="sxs-lookup"><span data-stu-id="6d043-146">Multiple-qubit measurements</span></span>

<span data-ttu-id="6d043-147">Die Messungen von multiqubit-Pauli-Operatoren sind ähnlich definiert, wie in:</span><span class="sxs-lookup"><span data-stu-id="6d043-147">Measurements of multi-qubit Pauli operators are defined similarly, as seen from:</span></span>

<span data-ttu-id="6d043-148">$ $ Z \otimes z = \begin{ bmatrix } 1 &0 &0&0 \\\\ 0 & -1&0&0 \\\\ 0&0 & -1&0 \\\\ 0&0&0&1 \end{bmatrix} .</span><span class="sxs-lookup"><span data-stu-id="6d043-148">$$ Z\otimes Z = \begin{bmatrix}1 &0 &0&0\\\\  0&-1&0&0\\\\ 0&0&-1&0\\\\ 0&0&0&1\end{bmatrix}.</span></span>
$$

<span data-ttu-id="6d043-149">Daher bilden die tensorflow-Produkte von zwei Pauli-$Z- $ Operatoren eine Matrix, die aus zwei Leerzeichen besteht, die aus $ + 1 $ und $-1 $ eigen Werten bestehen.</span><span class="sxs-lookup"><span data-stu-id="6d043-149">Thus the tensor products of two Pauli-$Z$ operators forms a matrix composed of two spaces consisting of $+1$ and $-1$ eigenvalues.</span></span>
<span data-ttu-id="6d043-150">Wie bei einem Single-Qubit-Fall bilden beide einen halben Leerraum, was bedeutet, dass die Hälfte des zugänglichen Vektor Raums zum $ + 1 $ -eigen Raum und die verbleibende Hälfte des Eigen Raums $-1 gehört $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-150">As with the single-qubit case, both constitute a half-space meaning that half of the accessible vector space belongs to the $+1$ eigenspace and the remaining half to the $-1$ eigenspace.</span></span>
<span data-ttu-id="6d043-151">Im Allgemeinen ist es einfach, aus der Definition des tensorflow-Produkts zu erkennen, dass ein beliebiges tensorflow-Produkt von Pauli-$Z $ -Operatoren und die Identität auch diesem entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d043-151">In general, it is easy to see from the definition of the tensor product that any tensor product of Pauli-$Z$ operators and the identity also obeys this.</span></span>
<span data-ttu-id="6d043-152">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6d043-152">For example,</span></span>

<span data-ttu-id="6d043-153">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-153">$$ \begin{align}</span></span>
    <span data-ttu-id="6d043-154">Z \otimes \boldone = \begin{bmatrix}</span><span class="sxs-lookup"><span data-stu-id="6d043-154">Z \otimes \boldone = \begin{bmatrix}</span></span>
        <span data-ttu-id="6d043-155">1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 &-1 & 0 \\ \\ 0 & 0 & 0 &-1 \ End{ bmatrix } .</span><span class="sxs-lookup"><span data-stu-id="6d043-155">1 &  0 &  0 &  0 \\\\ 0 &  1 &  0 &  0 \\\\ 0 &  0 & -1 &  0 \\\\ 0 &  0 &  0 & -1 \end{bmatrix}.</span></span>
<span data-ttu-id="6d043-156">\end{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-156">\end{align}</span></span>
$$

<span data-ttu-id="6d043-157">Wie zuvor beschreibt jede einheitliche Transformation dieser Matrizen auch zwei halbe Leerzeichen, die durch $ \pm 1 $ Eigenwerte bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="6d043-157">As before, any unitary transformation of such matrices also describes two half-spaces labeled by $\pm 1$ eigenvalues.</span></span>
<span data-ttu-id="6d043-158">Beispielsweise $X \otimes X = h \otimes h (z \otimes z) h \otimes h $ von der Identität, die $Z = HXH ist $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-158">For example, $X\otimes X = H\otimes H(Z\otimes Z)H\otimes H$  from the identity that $Z=HXH$.</span></span>
<span data-ttu-id="6d043-159">Ähnlich wie der One-Qubit-Fall können alle zwei-Qubit-Pauli-Messungen als $U ^ \dagger (Z \otimes \id) U $ für $4 \times 4 $ einheitliche Matrizen $U $ geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6d043-159">Similar to the one-qubit case, all two-qubit Pauli-measurements can be written as $U^\dagger (Z\otimes \id) U$ for $4\times 4$ unitary matrices $U$.</span></span> <span data-ttu-id="6d043-160">Die Transformationen in der folgenden Tabelle werden aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6d043-160">We enumerate the transformations in the following table.</span></span>

> [!NOTE]
> <span data-ttu-id="6d043-161">In der folgenden Tabelle wird $ \operatorname{Swap $ verwendet, } um die Matrix $ $ \begin{align anzugeben.}</span><span class="sxs-lookup"><span data-stu-id="6d043-161">In the table below, we use $\operatorname{SWAP}$ to indicate the matrix $$ \begin{align}</span></span>
>     <span data-ttu-id="6d043-162">\operatschmue{Swap } & = \left (\begin{Matrix}</span><span class="sxs-lookup"><span data-stu-id="6d043-162">\operatorname{SWAP} & = \left(\begin{matrix}</span></span>
>         <span data-ttu-id="6d043-163">1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{Matrix } \right) \end{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-163">1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{matrix}\right) \end{align}</span></span>
> <span data-ttu-id="6d043-164">$ $, mit dem der systeminterne Vorgang simuliert wird [`SWAP`](xref:microsoft.quantum.intrinsic) .</span><span class="sxs-lookup"><span data-stu-id="6d043-164">$$ used to simulate the intrinsic operation [`SWAP`](xref:microsoft.quantum.intrinsic).</span></span>

|<span data-ttu-id="6d043-165">Pauli-Messung</span><span class="sxs-lookup"><span data-stu-id="6d043-165">Pauli Measurement</span></span>     |<span data-ttu-id="6d043-166">Einheitliche Transformation</span><span class="sxs-lookup"><span data-stu-id="6d043-166">Unitary transformation</span></span>  |
|----------------------|------------------------|
| <span data-ttu-id="6d043-167">$Z \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-167">$Z \otimes \boldone$</span></span> | <span data-ttu-id="6d043-168">$ \boldone \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-168">$\boldone \otimes \boldone$</span></span> |
| <span data-ttu-id="6d043-169">$Z \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-169">$Z\otimes \boldone$</span></span> | <span data-ttu-id="6d043-170">$ \boldone \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-170">$\boldone\otimes \boldone$</span></span> |
| <span data-ttu-id="6d043-171">$X \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-171">$X\otimes \boldone$</span></span> | <span data-ttu-id="6d043-172">$H \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-172">$H\otimes \boldone$</span></span> |
| <span data-ttu-id="6d043-173">$Y \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-173">$Y\otimes \boldone$</span></span> | <span data-ttu-id="6d043-174">$HS ^ \dagger \otimes \boldone$</span><span class="sxs-lookup"><span data-stu-id="6d043-174">$HS^\dagger\otimes \boldone$</span></span> |
| <span data-ttu-id="6d043-175">$ \boldone \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="6d043-175">$\boldone \otimes Z$</span></span> | <span data-ttu-id="6d043-176">$ \operatschmue{Swap}$</span><span class="sxs-lookup"><span data-stu-id="6d043-176">$\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="6d043-177">$ \boldone \otimes X$</span><span class="sxs-lookup"><span data-stu-id="6d043-177">$\boldone \otimes X$</span></span> | <span data-ttu-id="6d043-178">$ (H \otimes \boldone) \operatschmue{Swap}$</span><span class="sxs-lookup"><span data-stu-id="6d043-178">$(H\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="6d043-179">$ \boldone \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="6d043-179">$\boldone \otimes Y$</span></span> | <span data-ttu-id="6d043-180">$ (HS ^ \dagger \otimes \boldone) \operatschmue{Swap}$</span><span class="sxs-lookup"><span data-stu-id="6d043-180">$(HS^\dagger\otimes \boldone)\operatorname{SWAP}$</span></span> |
| <span data-ttu-id="6d043-181">$Z \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="6d043-181">$Z\otimes Z$</span></span> | <span data-ttu-id="6d043-182">$ \operatorname{CNOT } \_ {10}$</span><span class="sxs-lookup"><span data-stu-id="6d043-182">$\operatorname{CNOT}\_{10}$</span></span> |
| <span data-ttu-id="6d043-183">$X \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="6d043-183">$X\otimes Z$</span></span> | <span data-ttu-id="6d043-184">$ \operatschmue{CNOT } \_ {10 } (H \otimes \boldone) $</span><span class="sxs-lookup"><span data-stu-id="6d043-184">$\operatorname{CNOT}\_{10}(H\otimes \boldone)$</span></span> |
| <span data-ttu-id="6d043-185">$Y \otimes Z$</span><span class="sxs-lookup"><span data-stu-id="6d043-185">$Y\otimes Z$</span></span> | <span data-ttu-id="6d043-186">$ \operatschmue{CNOT } \_ {10 } (HS ^ \dagger \otimes \boldone) $</span><span class="sxs-lookup"><span data-stu-id="6d043-186">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes \boldone)$</span></span> |
| <span data-ttu-id="6d043-187">$Z \otimes X$</span><span class="sxs-lookup"><span data-stu-id="6d043-187">$Z\otimes X$</span></span> | <span data-ttu-id="6d043-188">$ \operatschmue{CNOT } \_ {10 } (\boldone \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="6d043-188">$\operatorname{CNOT}\_{10}(\boldone\otimes H)$</span></span> |
| <span data-ttu-id="6d043-189">$X \otimes X$</span><span class="sxs-lookup"><span data-stu-id="6d043-189">$X\otimes X$</span></span> | <span data-ttu-id="6d043-190">$ \operatschmue{CNOT } \_ {10 } (h \otimes h) $</span><span class="sxs-lookup"><span data-stu-id="6d043-190">$\operatorname{CNOT}\_{10}(H\otimes H)$</span></span> |
| <span data-ttu-id="6d043-191">$Y \otimes X$</span><span class="sxs-lookup"><span data-stu-id="6d043-191">$Y\otimes X$</span></span> | <span data-ttu-id="6d043-192">$ \operatschmue{CNOT } \_ {10 } (HS ^ \dagger \otimes H) $</span><span class="sxs-lookup"><span data-stu-id="6d043-192">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes H)$</span></span> |
| <span data-ttu-id="6d043-193">$Z \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="6d043-193">$Z\otimes Y$</span></span> | <span data-ttu-id="6d043-194">$ \operatschmue{CNOT } \_ {10 } (\boldone \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="6d043-194">$\operatorname{CNOT}\_{10}(\boldone \otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="6d043-195">$X \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="6d043-195">$X\otimes Y$</span></span> | <span data-ttu-id="6d043-196">$ \operatorname{CNOT } \_ {10 } (H \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="6d043-196">$\operatorname{CNOT}\_{10}(H\otimes HS^\dagger)$</span></span> |
| <span data-ttu-id="6d043-197">$Y \otimes Y$</span><span class="sxs-lookup"><span data-stu-id="6d043-197">$Y\otimes Y$</span></span> | <span data-ttu-id="6d043-198">$ \operatschmue{CNOT } \_ {10 } (HS ^ \dagger \otimes HS ^ \dagger) $</span><span class="sxs-lookup"><span data-stu-id="6d043-198">$\operatorname{CNOT}\_{10}(HS^\dagger\otimes HS^\dagger)$</span></span> |

<span data-ttu-id="6d043-199">Hier wird der [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) Vorgang aus folgendem Grund angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d043-199">Here, the [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) operation appears for the following reason.</span></span>
<span data-ttu-id="6d043-200">Jede Pauli-Messung, die die "$ \boldone"-Matrix nicht enthält, $ entspricht der oben beschriebenen Argumentation einem einheitlichen $Z \otimes Z $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-200">Each Pauli measurement that does not include the $\boldone$ matrix is equivalent up to a unitary to $Z\otimes Z$ by the above reasoning.</span></span>
<span data-ttu-id="6d043-201">Die Eigenwerte von $Z \otimes Z $ hängen nur von der Parität der Qubits ab, aus denen die einzelnen Berechnungsbasis Vektor bestehen, und die kontrollierten Vorgänge dienen dazu, diese Parität zu berechnen und im ersten Bit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6d043-201">The eigenvalues of $Z\otimes Z$ only depend on the parity of the qubits that comprise each computational basis vector, and the controlled-not operations serve to compute this parity and store it in the first bit.</span></span>
<span data-ttu-id="6d043-202">Nachdem das erste Bit gemessen wurde, können wir die Identität des resultierenden halb Raums wiederherstellen, was dem Messen des Pauli-Operators entspricht.</span><span class="sxs-lookup"><span data-stu-id="6d043-202">Then once the first bit is measured, we can recover the identity of the resultant half-space, which is equivalent to measuring the Pauli operator.</span></span>

<span data-ttu-id="6d043-203">Ein weiterer Hinweis: Obwohl es möglicherweise verlockend ist, zu übernehmen, dass die Messung $Z \otimes Z $ identisch mit der sequenziellen Messung $Z \otimes \mathbb{1$ } und dann $ \mathbb{1 } \otimes Z ist $ , wäre diese Annahme falsch.</span><span class="sxs-lookup"><span data-stu-id="6d043-203">One additional note: while it may be tempting to assume that measuring $Z\otimes Z$ is the same as sequentially measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$, this assumption would be false.</span></span>
<span data-ttu-id="6d043-204">Der Grund hierfür ist, dass \otimes die Messung $Z Z $ den Quantum-Zustand entweder in den "$ + 1"- $ oder "$-1"- $ Zustand dieser Operatoren projiziert.</span><span class="sxs-lookup"><span data-stu-id="6d043-204">The reason is that measuring $Z\otimes Z$ projects the quantum state into either the $+1$ or $-1$ eigenstate of these operators.</span></span>
<span data-ttu-id="6d043-205">Wenn Sie $Z \otimes \mathbb{1$ } und dann $ \mathbb{1\otimes z Messen, wird } $ der Quantum-Status Vektor zuerst auf einen halben Bereich $Z \otimes \mathbb{1$ } und dann auf einen halben Bereich von $ \mathbb{1\otimes } z projiziert $ . Da es vier Berechnungsbasis Vektoren gibt, verringert die Durchführung beider Messungen den Zustand auf einen Viertel Raum und reduziert ihn somit auf einen einzelnen Berechnungsbasis Vektor.</span><span class="sxs-lookup"><span data-stu-id="6d043-205">Measuring $Z\otimes \mathbb{1}$ and then $\mathbb{1} \otimes Z$ projects the quantum state vector first onto a half space of $Z\otimes \mathbb{1}$ and then onto a half space of $\mathbb{1} \otimes Z$. As there are four computational basis vectors, performing both measurements reduces the state to a quarter-space and hence reduces it to a single computational basis vector.</span></span>

## <a name="correlations-between-qubits"></a><span data-ttu-id="6d043-206">Korrelationen zwischen Qubits</span><span class="sxs-lookup"><span data-stu-id="6d043-206">Correlations between qubits</span></span>
<span data-ttu-id="6d043-207">Eine weitere Möglichkeit zum Messen von tensorflow-Produkten von Pauli-Matrizen, wie $X \otimes X $ oder $Z \otimes Z $ , besteht darin, dass mit diesen Messungen die in den Korrelationen zwischen den beiden Qubits gespeicherten Informationen untersucht werden können.</span><span class="sxs-lookup"><span data-stu-id="6d043-207">Another way of looking at measuring tensor products of Pauli matrices such as $X\otimes X$ or $Z\otimes Z$ is that these measurements let you look at information stored in the correlations between the two qubits.</span></span>
<span data-ttu-id="6d043-208">\otimesWenn Sie $X \id Messen $ , sehen Sie sich die lokal im ersten Qubit gespeicherten Informationen an.</span><span class="sxs-lookup"><span data-stu-id="6d043-208">Measuring $X\otimes \id$ lets you look at information that is locally stored in the first qubit.</span></span>
<span data-ttu-id="6d043-209">Obwohl beide Arten von Messungen in Quantum Computing gleichermaßen wertvoll sind, beleuchtet das erste die Leistungsfähigkeit von Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="6d043-209">While both types of measurements are equally valuable in quantum computing, the former illuminates the power of quantum computing.</span></span>
<span data-ttu-id="6d043-210">Es ist offensichtlich, dass die Informationen, die Sie erlernen möchten, häufig nicht in einem einzigen Qubit gespeichert werden, sondern nicht lokal in allen Qubits gespeichert werden und daher nur durch eine gemeinsame Messung (z. b. $Z Z), dass \otimes $ diese Informationen zu einem Manifest werden.</span><span class="sxs-lookup"><span data-stu-id="6d043-210">It reveals that in quantum computing, often the information you wish to learn is not stored in any single qubit but rather stored non-locally in all the qubits at once, and therefore only by looking at it through a joint measurement (e.g. $Z\otimes Z$) does this information become manifest.</span></span>

<span data-ttu-id="6d043-211">Beispielsweise möchten wir bei der Fehlerkorrektur häufig ermitteln, welche Fehler aufgetreten sind, wenn Sie nichts über den Zustand erfahren möchten, den wir zu schützen versuchen.</span><span class="sxs-lookup"><span data-stu-id="6d043-211">For example, in error correction, we often wish to learn what error occurred while learning nothing about the state that we're trying to protect.</span></span>
<span data-ttu-id="6d043-212">Das [Bit-Flip-Code](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) Beispiel zeigt ein Beispiel dafür, wie Sie dies mithilfe von Messungen wie $Z \otimes z \otimes \id $ und $ \id \otimes z \ otimes z erreichen können $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-212">The [bit-flip code sample](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) shows an example of how you can do that using measurements like $Z \otimes Z \otimes \id$ and $\id \otimes Z \otimes Z$.</span></span>
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

<span data-ttu-id="6d043-213">Beliebige Pauli-Operatoren wie \otimes Z. b. $X Y \otimes Z \otimes \boldone $ können ebenfalls gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="6d043-213">Arbitrary Pauli operators such as $X\otimes Y \otimes Z \otimes \boldone$ can also be measured.</span></span>
<span data-ttu-id="6d043-214">Alle derartigen tensorflow-Produkte von Pauli-Operatoren haben nur zwei Eigenwerte $ \pm 1, $ und beide eigen Räume bilden halbräume des gesamten Vektor Bereichs.</span><span class="sxs-lookup"><span data-stu-id="6d043-214">All such tensor products of Pauli operators have only two eigenvalues $\pm 1$ and both eigenspaces constitute half-spaces of the entire vector space.</span></span>
<span data-ttu-id="6d043-215">Daher stimmen Sie mit den oben genannten Anforderungen überein.</span><span class="sxs-lookup"><span data-stu-id="6d043-215">Thus they coincide with the requirements stated above.</span></span>

<span data-ttu-id="6d043-216">In Q # geben solche Messungen $j zurück, $ Wenn die Messung ein Ergebnis im Eigen Bereich von Sign $ (-1) ^ j ergibt $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-216">In Q#, such measurements return $j$ if the measurement yields a result in the eigenspace of sign $(-1)^j$.</span></span>
<span data-ttu-id="6d043-217">Die Verwendung von Pauli-Messungen als integriertes Feature in Q # ist hilfreich, da die Messung solcher Operatoren lange Ketten von gesteuerten und nicht-Transformationen und Basis Transformationen erfordert, um die Diagonalisierung $U Gate zu beschreiben, $ die erforderlich ist, um den Vorgang als tensorflow-Produkt $Z $ und $ \id auszudrücken $ . Wenn Sie festlegen können, dass Sie eine dieser vordefinierten Messungen durchführen möchten, müssen Sie sich keine Gedanken darüber machen, wie Sie Ihre Basis so transformieren, dass eine Berechnungsbasis Messung die erforderlichen Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6d043-217">Having Pauli measurements as a built-in feature in Q# is helpful because measuring such operators requires long chains of controlled-NOT gates and basis transformations to describe the diagonalizing $U$ gate needed to express the operation as a tensor product of $Z$ and $\id$. By being able to specify that you wish to do one of these pre-defined measurements, you don't need to worry about how to transform your basis such that a computational basis measurement provides the necessary information.</span></span>
<span data-ttu-id="6d043-218">Q # behandelt alle notwendigen Basis Transformationen automatisch.</span><span class="sxs-lookup"><span data-stu-id="6d043-218">Q# handles all the necessary basis transformations for you automatically.</span></span>
<span data-ttu-id="6d043-219">Weitere Informationen finden Sie unter den [`Measure`](xref:microsoft.quantum.intrinsic.measure) -und- [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="6d043-219">For more information, see the [`Measure`](xref:microsoft.quantum.intrinsic.measure) and [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) operations.</span></span>

## <a name="the-no-cloning-theorem"></a><span data-ttu-id="6d043-220">Das No-Klon-Theorem</span><span class="sxs-lookup"><span data-stu-id="6d043-220">The No-Cloning Theorem</span></span>

<span data-ttu-id="6d043-221">Quantum-Informationen sind leistungsstark.</span><span class="sxs-lookup"><span data-stu-id="6d043-221">Quantum information is powerful.</span></span>
<span data-ttu-id="6d043-222">Dadurch können wir beeindruckende Dinge, wie z. b. die Faktor Zahlen, exponentiell beschleunigen als die besten bekannten klassischen Algorithmen, oder korrelierte Elektronen Systeme effizient simulieren, die für eine genaue Simulation exponentialkosten benötigen.</span><span class="sxs-lookup"><span data-stu-id="6d043-222">It enables us to do amazing things such as factor numbers exponentially faster than the best known classical algorithms, or efficiently simulate correlated electron systems that classically require exponential cost to simulate accurately.</span></span>
<span data-ttu-id="6d043-223">Es gibt jedoch Einschränkungen hinsichtlich der Leistungsfähigkeit von Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="6d043-223">However, there are limitations to the power of quantum computing.</span></span>
<span data-ttu-id="6d043-224">Eine solche Einschränkung wird durch das *No-Klon-Theorem*angegeben.</span><span class="sxs-lookup"><span data-stu-id="6d043-224">One such limitation is given by the *No-Cloning Theorem*.</span></span>

<span data-ttu-id="6d043-225">Das No-Klon-Theorem weist einen passenden Namen auf.</span><span class="sxs-lookup"><span data-stu-id="6d043-225">The No-Cloning Theorem is aptly named.</span></span>
<span data-ttu-id="6d043-226">Sie lässt das Klonen generischer Quantenzustände durch einen Quantum-Computer nicht zu.</span><span class="sxs-lookup"><span data-stu-id="6d043-226">It disallows cloning of generic quantum states by a quantum computer.</span></span>
<span data-ttu-id="6d043-227">Der Beweis für das Theorem ist erstaunlich einfach.</span><span class="sxs-lookup"><span data-stu-id="6d043-227">The proof of the theorem is remarkably straightforward.</span></span>
<span data-ttu-id="6d043-228">Obwohl ein vollständiger Nachweis für das No-Klon-Theorem für unsere Erörterung etwas zu technisch ist, liegt der Nachweis im Fall von zusätzlichen Qubits in unserem Bereich. (zusätzliche Qubits sind für den temporären Speicherplatz während einer Berechnung verwendeter Qubits und können problemlos in Q # verwendet werden, siehe [geliehene Qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span><span class="sxs-lookup"><span data-stu-id="6d043-228">While a full proof of the no-cloning theorem is a little too technical for our discussion here, the proof in the case of no additional auxiliary qubits is within our scope (auxiliary qubits are qubits used for scratch space during a computation and are easily used and managed in Q#, see [borrowed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).</span></span>

<span data-ttu-id="6d043-229">Bei solch einem Quantum-Computer muss der Klon Vorgang durch eine einheitliche Matrix beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6d043-229">For such a quantum computer, the cloning operation must be described by a unitary matrix.</span></span>
<span data-ttu-id="6d043-230">Die Messung wird nicht zugelassen, da der Quantum-Zustand beschädigt wird, den wir klonen wollen.</span><span class="sxs-lookup"><span data-stu-id="6d043-230">We disallow measurement, since it would corrupt the quantum state we are trying to clone.</span></span>
<span data-ttu-id="6d043-231">Um den Klon Vorgang zu simulieren, soll für die einheitliche Matrix die Eigenschaft $ $ U \ket { \psi } \ket{0= } \ket { \psi } \ket { \psi verwendet werden.}</span><span class="sxs-lookup"><span data-stu-id="6d043-231">To simulate the cloning operation, we want the unitary matrix used to have the property that $$ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}</span></span>
<span data-ttu-id="6d043-232">$ $ für einen beliebigen Status $ \ket { \psi } $.</span><span class="sxs-lookup"><span data-stu-id="6d043-232">$$ for any state $\ket{\psi}$.</span></span>
<span data-ttu-id="6d043-233">Die Linearität-Eigenschaft der Matrix Multiplikation impliziert dann, dass für jeden zweiten Quantum-Status $ \ket { \phi } $,</span><span class="sxs-lookup"><span data-stu-id="6d043-233">The linearity property of matrix multiplication then implies that for any second quantum state $\ket{\phi}$,</span></span>

<span data-ttu-id="6d043-234">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-234">$$ \begin{align}</span></span>
    <span data-ttu-id="6d043-235">U \left [\bruchteil {1 } {\sqrt{2} } \left (\ket { \phi } + \ket { \psi } \right) \right] \ket{0}</span><span class="sxs-lookup"><span data-stu-id="6d043-235">U \left[ \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right] \ket{0}</span></span>
    <span data-ttu-id="6d043-236">& = \bruchteil {1 } {\sqrt{2} } U \ket { \phi } \ket{0}</span><span class="sxs-lookup"><span data-stu-id="6d043-236">& = \frac{1}{\sqrt{2}} U\ket{\phi}\ket{0}</span></span>
      <span data-ttu-id="6d043-237">+ \bruchteil {1 } {\sqrt{2} } U \ket { \psi } \ket{0 } \\ \\ & = \bruchteil {1 } {\sqrt{2} } \left (\ket { \phi } \ket { \phi } + \ket { \psi } \ket { \psi}</span><span class="sxs-lookup"><span data-stu-id="6d043-237">+ \frac{1}{\sqrt{2}} U\ket{\psi}\ket{0} \\\\ & = \frac{1}{\sqrt{2}} \left( \ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi}</span></span>
        <span data-ttu-id="6d043-238">\right) \\ \\ & \nE \left (\bruchteil {1 } {\sqrt{2} } \left (\ket { \phi } + \ket { \psi } \right) \right) \otimes \left (\bruchteil {1 } {\sqrt{2 } } \left (\ket { \phi } + \ket { \psi } \right) \right).</span><span class="sxs-lookup"><span data-stu-id="6d043-238">\right) \\\\ & \ne \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right) \otimes \left( \frac{1}{\sqrt{2}}\left(\ket{\phi}+\ket{\psi} \right) \right).</span></span>
<span data-ttu-id="6d043-239">\end{align}</span><span class="sxs-lookup"><span data-stu-id="6d043-239">\end{align}</span></span>
$$

<span data-ttu-id="6d043-240">Dies stellt die grundlegende Intuition hinter dem No-Klon-Theorem bereit: jedes Gerät, das einen unbekannten Quantum-Zustand kopiert, muss Fehler in mindestens einigen der von ihm kopierte Zustände auslösen.</span><span class="sxs-lookup"><span data-stu-id="6d043-240">This provides the fundamental intuition behind the No-Cloning Theorem: any device that copies an unknown quantum state must induce errors on at least some of the states it copies.</span></span>
<span data-ttu-id="6d043-241">Während die Hauptannahme, dass der Cloner den Eingabe Status linear verarbeitet, durch Hinzufügen und Messen von hilfssbits verletzt werden kann, können solche Interaktionen auch Informationen über das System durch die maßstatistik und das exakte Klonen in solchen Fällen vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6d043-241">While the key assumption that the cloner acts linearly on the input state can be violated through the addition and measurement of auxiliary qubits, such interactions also leak information about the system through the measurement statistics and prevent exact cloning in such cases as well.</span></span>
<span data-ttu-id="6d043-242">Einen ausführlicheren Nachweis für das No-Klon-Theorem finden Sie unter, [um weitere Informationen](xref:microsoft.quantum.more-information)zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6d043-242">For a more complete proof of the No-Cloning Theorem see [For more information](xref:microsoft.quantum.more-information).</span></span>

<span data-ttu-id="6d043-243">Das No-Clone-Theorem ist wichtig für ein qualitativ hochwertiges Verständnis von Quantum Computing, denn wenn Sie Quantum-Zustände ingünstig Klonen könnten, erhalten Sie eine nahezu magische Möglichkeit, von Quantum-Zuständen zu lernen.</span><span class="sxs-lookup"><span data-stu-id="6d043-243">The No-Cloning Theorem is important for qualitative understanding of quantum computing because if you could clone quantum states inexpensively then you would be granted a near-magical ability to learn from quantum states.</span></span>
<span data-ttu-id="6d043-244">Tatsächlich könnten Sie das Prinzip der geunten Unsicherheit von Heisenberg verletzen.</span><span class="sxs-lookup"><span data-stu-id="6d043-244">Indeed, you could violate Heisenberg's vaunted uncertainty principle.</span></span>
<span data-ttu-id="6d043-245">Alternativ können Sie einen optimalen Cloner verwenden, um ein einzelnes Beispiel aus einer komplexen Quantum-Distribution zu erstellen und alles zu erlernen, was Sie möglicherweise über die Verteilung von nur einem Beispiel erfahren.</span><span class="sxs-lookup"><span data-stu-id="6d043-245">Alternatively, you could use an optimal cloner to take a single sample from a complex quantum distribution and learn everything you could possibly learn about that distribution from just one sample.</span></span>
<span data-ttu-id="6d043-246">Dies wäre so, als würden Sie eine Münze kippen und Köpfe beobachten und dann einen Freund über das Ergebnis informieren, dass Sie Antworten müssen. "ah die Verteilung der Münze muss Bernoulli mit $p = 0.512643 \ ldots $ !" lauten.</span><span class="sxs-lookup"><span data-stu-id="6d043-246">This would be like you flipping a coin and observing heads and then upon telling a friend about the result having them respond "Ah the distribution of that coin must be Bernoulli with $p=0.512643\ldots$!"</span></span>  <span data-ttu-id="6d043-247">Eine solche Anweisung wäre nicht unsinnig, weil ein Teil der Informationen (das Heads-Ergebnis) einfach nicht die vielen Informationen bereitstellen kann, die erforderlich sind, um die Verteilung ohne wesentliche vorherige Informationen zu codieren.</span><span class="sxs-lookup"><span data-stu-id="6d043-247">Such a statement would be non-sensical because one bit of information (the heads outcome) simply cannot provide the many bits of information needed to encode the distribution without substantial prior information.</span></span>
<span data-ttu-id="6d043-248">Ebenso wie ohne vorherige Informationen können wir einen quantumstatus nicht ganz genau so Klonen, wie wir ein Ensemble dieser Münzen nicht vorbereiten können, ohne $p zu kennen $ .</span><span class="sxs-lookup"><span data-stu-id="6d043-248">Similarly, without prior information we cannot perfectly clone a quantum state just as we cannot prepare an ensemble of such coins without knowing $p$.</span></span>

<span data-ttu-id="6d043-249">Informationen sind in Quantum Computing nicht kostenlos.</span><span class="sxs-lookup"><span data-stu-id="6d043-249">Information is not free in quantum computing.</span></span>
<span data-ttu-id="6d043-250">Jedes gemessene Qubit liefert ein einzelnes Bit an Informationen, und das No-Klon-Theorem zeigt, dass es keine Hintertür gibt, die ausgenutzt werden kann, um den grundlegenden Kompromiss zwischen den Informationen, die über das System gewonnen wurden, und der auf ihm aufgerufenen Störung zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="6d043-250">Each qubit measured gives a single bit of information, and the No-Cloning Theorem shows that there is no backdoor that can be exploited to get around the fundamental tradeoff between information gained about the system and the disturbance invoked upon it.</span></span>
