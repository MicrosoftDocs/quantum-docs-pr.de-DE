---
title: Quantenorakel
description: Erfahren Sie, wie Sie mithilfe von Quantum-Oracles, Black Box-Vorgängen, die als Eingabe für einen anderen Algorithmus verwendet werden, arbeiten und definieren.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
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
ms.openlocfilehash: 31e43940fc0607b15ccefcfae6be7122227b3d64
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630317"
---
# <a name="quantum-oracles"></a><span data-ttu-id="f5c13-103">Quantum-Oracles</span><span class="sxs-lookup"><span data-stu-id="f5c13-103">Quantum Oracles</span></span>

<span data-ttu-id="f5c13-104">Bei einem Oracle-$O $ handelt es sich um einen "Blackbox"-Vorgang, der als Eingabe für einen anderen Algorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5c13-104">An oracle $O$ is a "black box" operation that is used as input to another algorithm.</span></span>
<span data-ttu-id="f5c13-105">Häufig werden solche Vorgänge mithilfe eines klassischen Funktions $f definiert: \\ {0, 1 \\ } ^ n \to \\ {0, 1 \\ } ^ m, $ der eine binäre $n $ -Bit-Eingabe annimmt und eine binäre $m $ -Bit-Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="f5c13-105">Often, such operations are defined using a classical function $f : \\{0, 1\\}^n \to \\{0, 1\\}^m$ which takes an $n$-bit binary input and produces an $m$-bit binary output.</span></span>
<span data-ttu-id="f5c13-106">Beachten Sie hierzu eine bestimmte binäre Eingabe $x = (x_ {0 } , x_ {1 } , \dots, x_ {n-1 } ) $.</span><span class="sxs-lookup"><span data-stu-id="f5c13-106">To do so, consider a particular binary input $x = (x_{0}, x_{1}, \dots, x_{n-1})$.</span></span>
<span data-ttu-id="f5c13-107">Wir können Qubit-Zustände als "$ \ket { \vec{x } } = \ket{x_ {0 } } \otimes \ket{x_ {1 } } \otimes \cdots \otimes \ket{x_ {n-1 } } $" bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="f5c13-107">We can label qubit states as $\ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_{n-1}}$.</span></span>

<span data-ttu-id="f5c13-108">Wir könnten zuerst versuchen, $O zu definieren, $ sodass $O \ket {x } = \ket{f (x)} $, aber dies hat einige Probleme.</span><span class="sxs-lookup"><span data-stu-id="f5c13-108">We may first attempt to define $O$ so that $O\ket{x} = \ket{f(x)}$, but this has a couple problems.</span></span>
<span data-ttu-id="f5c13-109">Erstens können $f $ eine andere Größe von Eingabe und Ausgabe haben ($n \nE m $ ), sodass beim Anwenden von $O $ die Anzahl der Qubits im Register geändert würde.</span><span class="sxs-lookup"><span data-stu-id="f5c13-109">First, $f$ may have a different size of input and output ($n \ne m$), such that applying $O$ would change the number of qubits in the register.</span></span>
<span data-ttu-id="f5c13-110">Zweitens: auch wenn $n = m $ ist, ist die Funktion möglicherweise nicht invertierbar: Wenn $f (x) = f (y) $ für einige $x \nE y $ , $O \ket {x } = O \ket {y $, } aber $O ^ \dagger o \ket {x } \nE o ^ \dagger o \ket {y } $.</span><span class="sxs-lookup"><span data-stu-id="f5c13-110">Second, even if $n = m$, the function may not be invertible: if $f(x) = f(y)$ for some $x \ne y$, then $O\ket{x} = O\ket{y}$ but $O^\dagger O\ket{x} \ne O^\dagger O\ket{y}$.</span></span>
<span data-ttu-id="f5c13-111">Dies bedeutet, dass wir den Adjoint-Vorgang nicht erstellen können $O ^ \dagger $ , und für Oracles muss ein Adjoint-Element definiert sein.</span><span class="sxs-lookup"><span data-stu-id="f5c13-111">This means we won't be able to construct the adjoint operation $O^\dagger$, and oracles have to have an adjoint defined for them.</span></span>

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a><span data-ttu-id="f5c13-112">Definieren eines Oracle-Effekts durch seine Auswirkung auf den Berechnungsbasis Status</span><span class="sxs-lookup"><span data-stu-id="f5c13-112">Defining an oracle by its effect on computational basis states</span></span>
<span data-ttu-id="f5c13-113">Wir können diese beiden Probleme behandeln, indem wir ein zweites Register $m $ Qubits einführen, um unsere Antwort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f5c13-113">We can deal with both of these problems by introducing a second register of $m$ qubits to hold our answer.</span></span>
<span data-ttu-id="f5c13-114">Anschließend definieren wir die Auswirkung des Oracle auf alle Berechnungs Status Zustände: für alle $x \in \\ {0, 1 \\ } ^ n $ und $y \in \\ {0, 1 \\ } ^ m $ ,</span><span class="sxs-lookup"><span data-stu-id="f5c13-114">Then we will define the effect of the oracle on all computational basis states: for all $x \in \\{0, 1\\}^n$ and $y \in \\{0, 1\\}^m$,</span></span>

<span data-ttu-id="f5c13-115">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-115">$$ \begin{align}</span></span>
    <span data-ttu-id="f5c13-116">O (\ket{x } \otimes \ket{y } ) = \ket{x } \otimes \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="f5c13-116">O(\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="f5c13-117">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-117">\end{align}</span></span>
$$

<span data-ttu-id="f5c13-118">Nun $O = O ^ \dagger $ by Construction, daher haben wir beide früheren Probleme gelöst.</span><span class="sxs-lookup"><span data-stu-id="f5c13-118">Now $O = O^\dagger$ by construction, thus we have resolved both of the earlier problems.</span></span>

> [!TIP]
> <span data-ttu-id="f5c13-119">Um zu sehen, dass $O = O ^ {\dagger } $ lautet, beachten Sie, dass $O ^ 2 = \boldone $ seit $a \oplus b \oplus b = a $ für alle $a, b \in \{ 0, 1 \} $.</span><span class="sxs-lookup"><span data-stu-id="f5c13-119">To see that $O = O^{\dagger}$, note that $O^2 = \boldone$ since $a \oplus b \oplus b = a$ for all $a, b \in \{0, 1\}$.</span></span>
> <span data-ttu-id="f5c13-120">Folglich $O \ket{x } \ket{y \oplus f (x)} = \ket{x } \ket{y \oplus f (x) \oplus f (x)} = \ket{x } \ket{y } $.</span><span class="sxs-lookup"><span data-stu-id="f5c13-120">As a result, $O \ket{x} \ket{y \oplus f(x)} = \ket{x} \ket{y \oplus f(x) \oplus f(x)} = \ket{x} \ket{y}$.</span></span>

<span data-ttu-id="f5c13-121">Wichtig: die Definition eines Oracle auf diese Weise für jeden Berechnungsbasis Status $ \ket{x } \ket{y } $ definiert auch, wie $O $ für jeden anderen Zustand agiert.</span><span class="sxs-lookup"><span data-stu-id="f5c13-121">Importantly, defining an oracle this way for each computational basis state $\ket{x}\ket{y}$ also defines how $O$ acts for any other state.</span></span>
<span data-ttu-id="f5c13-122">Dies folgt unmittelbar daran, dass $O $ , wie alle Quantum-Vorgänge, in dem Zustand, auf den er angewendet wird, linear ist.</span><span class="sxs-lookup"><span data-stu-id="f5c13-122">This follows immediately from the fact that $O$, like all quantum operations, is linear in the state that it acts on.</span></span>
<span data-ttu-id="f5c13-123">Stellen Sie sich beispielsweise den Hadamard-Vorgang vor, der durch $H \ket{0 } = \ket { +} $ und $H \ket{1= } \ket { -} $ definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f5c13-123">Consider the Hadamard operation, for instance, which is defined by $H \ket{0} = \ket{+}$ and $H \ket{1} = \ket{-}$.</span></span>
<span data-ttu-id="f5c13-124">Wenn Sie wissen möchten, wie $H $ mit "$ \ket { +} $" funktioniert, können wir diese $H linear verwenden. $</span><span class="sxs-lookup"><span data-stu-id="f5c13-124">If we wish to know how $H$ acts on $\ket{+}$, we can use that $H$ is linear,</span></span>

<span data-ttu-id="f5c13-125">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-125">$$ \begin{align}</span></span>
<span data-ttu-id="f5c13-126">H \ket { +} & = \bruchteil {1 } {\sqrt{2} } H (\ket{0+ } \ket{1 } ) = \bruchteil {1 } {\sqrt{2 } } (H \ket {0 } + H \ket {1 } ) \\ \\ & = \bruch } {1{\sqrt{2} } (\ket { +} + \ket { -}) = \bruch12 (\ket{0+ } \ket{1+ } \ket{0 } -\ket{1 } ) = \ket{0. }</span><span class="sxs-lookup"><span data-stu-id="f5c13-126">H\ket{+} & = \frac{1}{\sqrt{2}} H(\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (H\ket{0} + H\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \frac12 (\ket{0} + \ket{1} + \ket{0} - \ket{1}) = \ket{0}.</span></span>
<span data-ttu-id="f5c13-127">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-127">\end{align}</span></span>
$$

<span data-ttu-id="f5c13-128">Wenn wir unsere Oracle-$O definieren $ , können wir auf ähnliche Weise den Status $ \ket { \psi } $ auf $n + m- $ Qubits schreiben als</span><span class="sxs-lookup"><span data-stu-id="f5c13-128">In the case of defining our oracle $O$, we can similarly use that any state $\ket{\psi}$ on $n + m$ qubits can be written as</span></span>

<span data-ttu-id="f5c13-129">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-129">$$ \begin{align}</span></span>
<span data-ttu-id="f5c13-130">\ket { \psi } & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y}</span><span class="sxs-lookup"><span data-stu-id="f5c13-130">\ket{\psi} & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y}</span></span>
<span data-ttu-id="f5c13-131">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-131">\end{align}</span></span>
$$

<span data-ttu-id="f5c13-132">wobei $ \alpha: \\ {0, 1 \\ } ^ n \times \\ {0, 1 \\ } ^ m \to \mathbb{c } $ die Koeffizienten des Zustands $ \ket { \psi } $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="f5c13-132">where $\alpha : \\{0, 1\\}^n \times \\{0, 1\\}^m \to \mathbb{C}$ represents the coefficients of the state $\ket{\psi}$.</span></span> <span data-ttu-id="f5c13-133">Demnach sind</span><span class="sxs-lookup"><span data-stu-id="f5c13-133">Thus,</span></span>

<span data-ttu-id="f5c13-134">$ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-134">$$ \begin{align}</span></span>
<span data-ttu-id="f5c13-135">O \ket { \psi } & = o \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y } \\ \\ & = \ sum_ {x \in \\ {0, 1 \\ } ^ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) O \ket{x } \ket{y } \\ \\ & = \ sum_ {x \in \\ {0, 1} ^ \\ n, y \in \\ {0, 1 \\ } ^ m } \alpha (x, y) \ket{x } \ket{y \oplus f (x)}.</span><span class="sxs-lookup"><span data-stu-id="f5c13-135">O \ket{\psi} & = O \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) O \ket{x} \ket{y} \\\\ & = \sum_{x \in \\{0, 1\\}^n, y \in \\{0, 1\\}^m} \alpha(x, y) \ket{x} \ket{y \oplus f(x)}.</span></span>
<span data-ttu-id="f5c13-136">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-136">\end{align}</span></span>
$$

## <a name="phase-oracles"></a><span data-ttu-id="f5c13-137">Phasen-Oracles</span><span class="sxs-lookup"><span data-stu-id="f5c13-137">Phase oracles</span></span>
<span data-ttu-id="f5c13-138">Alternativ $ dazu können Sie $f in eine Oracle-$O codieren, $ indem Sie eine _Phase_ auf der Grundlage der Eingabe für $O anwenden $ .</span><span class="sxs-lookup"><span data-stu-id="f5c13-138">Alternatively, we can encode $f$ into an oracle $O$ by applying a _phase_ based on the input to $O$.</span></span>
<span data-ttu-id="f5c13-139">Beispielsweise können wir $O so definieren $ , dass $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-139">For instance, we might define $O$ such that $$ \begin{align}</span></span>
    <span data-ttu-id="f5c13-140">O \ket{x } = (-1) ^ {f (x)} \ket{x } .</span><span class="sxs-lookup"><span data-stu-id="f5c13-140">O \ket{x} = (-1)^{f(x)} \ket{x}.</span></span>
<span data-ttu-id="f5c13-141">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-141">\end{align}</span></span>
<span data-ttu-id="f5c13-142">$ $ Wenn eine Phase-Oracle zuerst in einem Compute-Status $ \ket{x $ auf ein Register angewendet wird } , ist diese Phase eine globale Phase und daher nicht Observable.</span><span class="sxs-lookup"><span data-stu-id="f5c13-142">$$ If a phase oracle acts on a register initially in a computational basis state $\ket{x}$, then this phase is a global phase and hence not observable.</span></span>
<span data-ttu-id="f5c13-143">Ein solches Oracle kann jedoch eine sehr leistungsfähige Ressource sein, wenn Sie auf eine übergeordnete Position oder einen kontrollierten Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5c13-143">But such an oracle can be a very powerful resource if applied to a superposition or as a controlled operation.</span></span>
<span data-ttu-id="f5c13-144">Stellen Sie sich z. b. einen Phasen-Orcale $O _F $ für eine Single-Qubit-Funktion $f dar $ .</span><span class="sxs-lookup"><span data-stu-id="f5c13-144">For example, consider a phase orcale $O_f$ for a single-qubit function $f$.</span></span>
<span data-ttu-id="f5c13-145">Dann $ $ \begin{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-145">Then, $$ \begin{align}</span></span>
    <span data-ttu-id="f5c13-146">O_f \ket { +} & = O_f (\ket{0+ } \ket{1 } )/\sqrt{2 } \\ \\ & = ((-1) ^ {f (0)} \ket{0+ } (-1) ^ {f (1)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} (\ket{0+ } (-1) ^ {f (1)-f (0)} \ket{1 } )/\sqrt{2 } \\ \\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket { +}.</span><span class="sxs-lookup"><span data-stu-id="f5c13-146">O_f \ket{+} & = O_f (\ket{0} + \ket{1}) / \sqrt{2} \\\\ & = ((-1)^{f(0)} \ket{0} + (-1)^{f(1)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} (\ket{0} + (-1)^{f(1) - f(0)} \ket{1}) / \sqrt{2} \\\\ & = (-1)^{f(0)} Z^{f(0) - f(1)} \ket{+}.</span></span>
<span data-ttu-id="f5c13-147">\end{align}</span><span class="sxs-lookup"><span data-stu-id="f5c13-147">\end{align}</span></span>
$$

<span data-ttu-id="f5c13-148">Im Allgemeinen können beide Sichten von Oracles erweitert werden, um klassische Funktionen darzustellen, die anstelle eines einzelnen Bits reelle Zahlen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f5c13-148">More generally, both views of oracles can be broadened to represent classical functions which return real numbers instead of only a single bit.</span></span>

<span data-ttu-id="f5c13-149">Das Auswählen der besten Methode zum Implementieren eines Oracle hängt stark davon ab, wie dieses Oracle innerhalb eines bestimmten Algorithmus verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5c13-149">Choosing the best way to implement an oracle depends heavily on how this oracle will be used within a given algorithm.</span></span>
<span data-ttu-id="f5c13-150">Der " [Deutsch-Jozsa"-Algorithmus](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) basiert z. b. auf dem Oracle, der auf die erste Weise implementiert ist, während der [-Algorithmus von Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) auf die zweite Weise implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="f5c13-150">For example, [Deutsch-Jozsa algorithm](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) relies on the oracle implemented in the first way, while [Grover's algorithm](https://en.wikipedia.org/wiki/Grover's_algorithm) relies on the oracle implemented in the second way.</span></span>


<span data-ttu-id="f5c13-151">Weitere Informationen finden Sie unter [gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).</span><span class="sxs-lookup"><span data-stu-id="f5c13-151">For more details, we suggest the discussion in [Gilyén *et al*. 1711.00465](https://arxiv.org/abs/1711.00465).</span></span>
