---
title: Quantum Computing-Glossar
description: Ein Glossar allgemeiner Begriffe, Aktionen und Objekte, die in Quantum Computing verwendet werden.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
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
ms.openlocfilehash: ba4d171d84d808f082b919dcc6156d9c65df7c05
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274790"
---
# <a name="quantum-computing-glossary"></a><span data-ttu-id="6a0e4-103">Quantum Computing-Glossar</span><span class="sxs-lookup"><span data-stu-id="6a0e4-103">Quantum computing glossary</span></span>

## <a name="adjoint"></a><span data-ttu-id="6a0e4-104">Adjoint</span><span class="sxs-lookup"><span data-stu-id="6a0e4-104">Adjoint</span></span>

<span data-ttu-id="6a0e4-105">Die komplexe konjugierte, die einen [Vorgang](xref:microsoft.quantum.glossary#operation)durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-105">The complex conjugate transpose of an [operation](xref:microsoft.quantum.glossary#operation).</span></span> <span data-ttu-id="6a0e4-106">Bei Vorgängen, die einen [einheitlichen](xref:microsoft.quantum.glossary#unitary-operator) Operator implementieren, ist das Adjoint das Gegenteil des Vorgangs und wird durch ein Kreuz-Symbol angegeben.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-106">For operations that implement a [unitary](xref:microsoft.quantum.glossary#unitary-operator) operator, the adjoint is the inverse of the operation and is indicated by a dagger symbol.</span></span> <span data-ttu-id="6a0e4-107">Wenn der Vorgang z. b. `U` den einheitlichen Operator $U darstellt $ , `Adjoint U` stellt $U ^ \dagger dar $ .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-107">For example, if the operation `U` represents the unitary operator $U$, then `Adjoint U` represents $U^\dagger$.</span></span> <span data-ttu-id="6a0e4-108">Weitere Informationen finden Sie unter [Adjoint](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-108">For more information, see [Adjoint](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span></span>

## <a name="ancilla"></a><span data-ttu-id="6a0e4-109">Ancilla</span><span class="sxs-lookup"><span data-stu-id="6a0e4-109">Ancilla</span></span>

<span data-ttu-id="6a0e4-110">Ein [Qubit](xref:microsoft.quantum.glossary#qubit) , das als temporärer Speicher für einen Quantum-Computer fungiert und bei Bedarf zugewiesen und dessen Zuordnung aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-110">A [qubit](xref:microsoft.quantum.glossary#qubit) that serves as temporary memory for a quantum computer and is allocated and de-allocated as needed.</span></span>  <span data-ttu-id="6a0e4-111">Weitere Informationen finden Sie unter [Multiple Qubits (mehrere Qubits](xref:microsoft.quantum.concepts.multiple-qubits)).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-111">For more information, see [Multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

## <a name="bell-state"></a><span data-ttu-id="6a0e4-112">Glocken Zustand</span><span class="sxs-lookup"><span data-stu-id="6a0e4-112">Bell state</span></span>

<span data-ttu-id="6a0e4-113">Einer von vier bestimmten maxitional [entbickten](xref:microsoft.quantum.glossary#entanglement) [Quantum-Zuständen](xref:microsoft.quantum.glossary#quantum-state) mit zwei Qubits.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-113">One of four specific maximally [entangled](xref:microsoft.quantum.glossary#entanglement) [quantum states](xref:microsoft.quantum.glossary#quantum-state) of two qubits.</span></span> <span data-ttu-id="6a0e4-114">Die vier Zustände werden $ \ket { \ beta_ {IJ } } = (\mathbb{i } \otimes X ^ iz ^ j) (\ket{00 } + \ket{11 } )/\sqrt{2 $ definiert } .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-114">The four states are defined $\ket{\beta_{ij}} = (\mathbb{I} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span> <span data-ttu-id="6a0e4-115">Ein Glocken Zustand wird auch als [EPR-paar](xref:microsoft.quantum.glossary#epr-pair)bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-115">A Bell state is also known as an [EPR pair](xref:microsoft.quantum.glossary#epr-pair).</span></span>

## <a name="bloch-sphere"></a><span data-ttu-id="6a0e4-116">Bloch-Kugel</span><span class="sxs-lookup"><span data-stu-id="6a0e4-116">Bloch sphere</span></span>

<span data-ttu-id="6a0e4-117">Eine grafische Darstellung eines Single-[Qubit](xref:microsoft.quantum.glossary#qubit) - [Quantum-Zustands](xref:microsoft.quantum.glossary#quantum-state) als Punkt in einer dreidimensionalen Einheits Kugel.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-117">A graphical representation of a single-[qubit](xref:microsoft.quantum.glossary#qubit) [quantum state](xref:microsoft.quantum.glossary#quantum-state) as a point in a three-dimensional unit sphere.</span></span> <span data-ttu-id="6a0e4-118">Weitere Informationen finden Sie unter [visualisieren von Qubits und Transformationen mithilfe der Bloch-Kugel](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-118">For more information, see  [Visualizing Qubits and Transformations using the Bloch Sphere](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>

## <a name="callable"></a><span data-ttu-id="6a0e4-119">Callable</span><span class="sxs-lookup"><span data-stu-id="6a0e4-119">Callable</span></span>

<span data-ttu-id="6a0e4-120">Ein [Vorgang](xref:microsoft.quantum.glossary#operation) oder eine [Funktion](xref:microsoft.quantum.glossary#function) in der Q #-Sprache.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-120">An [operation](xref:microsoft.quantum.glossary#operation) or [function](xref:microsoft.quantum.glossary#function) in the Q# language.</span></span> <span data-ttu-id="6a0e4-121">Weitere Informationen finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-121">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="clifford-group"></a><span data-ttu-id="6a0e4-122">Clifford-Gruppe</span><span class="sxs-lookup"><span data-stu-id="6a0e4-122">Clifford group</span></span>

<span data-ttu-id="6a0e4-123">Der Satz von Vorgängen, die die oktanten der [Bloch-Kugel](xref:microsoft.quantum.glossary#bloch-sphere) und Auswirkung Permutationen der [Pauli-Operatoren](xref:microsoft.quantum.glossary#pauli-operators)belegen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-123">The set of operations that occupy the octants of the [Bloch sphere](xref:microsoft.quantum.glossary#bloch-sphere) and effect permutations of the [Pauli operators](xref:microsoft.quantum.glossary#pauli-operators).</span></span> <span data-ttu-id="6a0e4-124">Hierzu gehören die Vorgänge [$X $ ](xref:microsoft.quantum.intrinsic.x), [$Y $ ](xref:microsoft.quantum.intrinsic.y), [$Z $ ](xref:microsoft.quantum.intrinsic.z), [$H $ ](xref:microsoft.quantum.intrinsic.h) und [$S $ ](xref:microsoft.quantum.intrinsic.s).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-124">These include the operations [$X$](xref:microsoft.quantum.intrinsic.x), [$Y$](xref:microsoft.quantum.intrinsic.y), [$Z$](xref:microsoft.quantum.intrinsic.z), [$H$](xref:microsoft.quantum.intrinsic.h) and [$S$](xref:microsoft.quantum.intrinsic.s).</span></span>

## <a name="controlled"></a><span data-ttu-id="6a0e4-125">Klimatisiert</span><span class="sxs-lookup"><span data-stu-id="6a0e4-125">Controlled</span></span>

<span data-ttu-id="6a0e4-126">Ein Quantum- [Vorgang](xref:microsoft.quantum.glossary#operation) , der ein oder mehrere [Qubits](xref:microsoft.quantum.glossary#qubit) als Enabler für den Ziel Vorgang annimmt.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-126">A quantum [operation](xref:microsoft.quantum.glossary#operation) that takes one or more [qubits](xref:microsoft.quantum.glossary#qubit) as enablers for the target operation.</span></span> <span data-ttu-id="6a0e4-127">Weitere Informationen finden Sie unter [gesteuerte und Adjoint-Vorgänge](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-127">For more information, see [Controlled and adjoint operations](xref:microsoft.quantum.guide.operationsfunctions#controlled-and-adjoint-operations).</span></span>

## <a name="dirac-notation"></a><span data-ttu-id="6a0e4-128">Dirac-Notation</span><span class="sxs-lookup"><span data-stu-id="6a0e4-128">Dirac Notation</span></span>

<span data-ttu-id="6a0e4-129">Eine symbolische Kurznotiz, die die Darstellung von [Quantum-Zuständen](xref:microsoft.quantum.glossary#quantum-state)vereinfacht, auch als *Bra-Ket-* Notation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-129">A symbolic shorthand that simplifies the representation of [quantum states](xref:microsoft.quantum.glossary#quantum-state), also called *bra-ket* notation.</span></span>  <span data-ttu-id="6a0e4-130">Der *Bra* -Teil stellt einen Zeilen Vektor dar, z. b. $ \bra{a } = \begin{ bmatrix } a {_1 } & a {_2 } \end{ bmatrix } $, und der *Ket* -Teil stellt einen Spalten Vektor ($ \ket{b } = \begin{ bmatrix } b {_1 } \\ \\ B {_2 } \end{ bmatrix } $) dar.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-130">The *bra* portion represents a row vector, for example  $\bra{A} = \begin{bmatrix} A{_1} & A{_2} \end{bmatrix}$ and the *ket* portion represents a column vector, $\ket{B} = \begin{bmatrix} B{_1} \\\\ B{_2} \end{bmatrix}$.</span></span> <span data-ttu-id="6a0e4-131">Weitere Informationen finden Sie unter [Dirac-Notation](xref:microsoft.quantum.concepts.dirac).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-131">For more information, see [Dirac Notation](xref:microsoft.quantum.concepts.dirac).</span></span>

## <a name="eigenvalue"></a><span data-ttu-id="6a0e4-132">Eigen Wert</span><span class="sxs-lookup"><span data-stu-id="6a0e4-132">Eigenvalue</span></span>

<span data-ttu-id="6a0e4-133">Der Faktor, um den die Größe eines [eigen Vektors](xref:microsoft.quantum.glossary#eigenvector) einer bestimmten Transformation von der Anwendung der Transformation geändert wird.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-133">The factor by which the magnitude of an [eigenvector](xref:microsoft.quantum.glossary#eigenvector) of a given transformation is changed by the application of the transformation.</span></span>  <span data-ttu-id="6a0e4-134">Wenn eine quadratische Matrix $M $ und ein eigen Vektor $v $ , dann $MV = CV $ , wobei $c $ der Eigen Wert ist und eine komplexe Zahl beliebiger Argumente sein kann.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-134">Given a square matrix $M$ and an eigenvector $v$, then $Mv = cv$, where $c$ is the eigenvalue and can be a complex number of any argument.</span></span> <span data-ttu-id="6a0e4-135">Weitere Informationen finden Sie unter [Advanced Matrix Concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-135">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="eigenvector"></a><span data-ttu-id="6a0e4-136">Eigen Vektor</span><span class="sxs-lookup"><span data-stu-id="6a0e4-136">Eigenvector</span></span>

<span data-ttu-id="6a0e4-137">Ein Vektor, dessen Richtung durch eine angegebene Transformation unverändert bleibt und dessen Größe durch einen Faktor geändert wird, der dem [eigen Wert](xref:microsoft.quantum.glossary#eigenvalue)dieses Vektors entspricht.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-137">A vector whose direction is unchanged by a given transformation and whose magnitude is changed by a factor corresponding to that vector's [eigenvalue](xref:microsoft.quantum.glossary#eigenvalue).</span></span> <span data-ttu-id="6a0e4-138">Wenn eine quadratische Matrix $M $ und ein eigen Wert $c $ , dann $MV = CV $ , wobei $v $ ein eigen Vektor der Matrix ist und eine komplexe Zahl beliebiger Argumente sein kann.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-138">Given a square matrix $M$ and an eigenvalue $c$, then $Mv = cv$, where $v$ is an eigenvector of the matrix and can be a complex number of any argument.</span></span> <span data-ttu-id="6a0e4-139">Weitere Informationen finden Sie unter [Advanced Matrix Concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-139">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="entanglement"></a><span data-ttu-id="6a0e4-140">Verschränkung</span><span class="sxs-lookup"><span data-stu-id="6a0e4-140">Entanglement</span></span>

<span data-ttu-id="6a0e4-141">Quantum-Partikel (z. b. [Qubits](xref:microsoft.quantum.glossary#qubit)) können verbunden oder *entkoppelt* werden, sodass Sie nicht unabhängig voneinander beschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-141">Quantum particles, such as [qubits](xref:microsoft.quantum.glossary#qubit), can be connected or *entangled* such that they cannot be described independently from each other.</span></span> <span data-ttu-id="6a0e4-142">Die Messergebnisse werden auch dann korreliert, wenn Sie unendlich weit entfernt sind.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-142">Their measurement results are correlated even when they are separated infinitely far away.</span></span> <span data-ttu-id="6a0e4-143">"Entanglement" ist für die [Messung](xref:microsoft.quantum.glossary#measurement) des [Status](xref:microsoft.quantum.glossary#quantum-state) eines Qubit unabdingbar.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-143">Entanglement is essential to [measuring](xref:microsoft.quantum.glossary#measurement) the [state](xref:microsoft.quantum.glossary#quantum-state) of a qubit.</span></span>  <span data-ttu-id="6a0e4-144">Weitere Informationen finden Sie unter [Advanced Matrix Concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-144">For more information, see [Advanced matrix concepts](xref:microsoft.quantum.concepts.matrix-advanced).</span></span>

## <a name="epr-pair"></a><span data-ttu-id="6a0e4-145">EPR-paar</span><span class="sxs-lookup"><span data-stu-id="6a0e4-145">EPR pair</span></span>

<span data-ttu-id="6a0e4-146">Einer von vier bestimmten maxitional entbickten [Quantum-Zuständen](xref:microsoft.quantum.glossary#quantum-state) mit zwei [Qubits](xref:microsoft.quantum.glossary#qubit).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-146">One of four specific maximally entangled [quantum states](xref:microsoft.quantum.glossary#quantum-state) of two [qubits](xref:microsoft.quantum.glossary#qubit).</span></span> <span data-ttu-id="6a0e4-147">Die vier Zustände werden $ \ket { \ beta_ {IJ } } = (\mathbb{1 } \otimes X ^ iz ^ j) (\ket{00 } + \ket{11 } )/\sqrt{2 $ definiert } .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-147">The four states are defined $\ket{\beta_{ij}} = (\mathbb{1} \otimes X^iZ^j) (\ket{00} + \ket{11}) / \sqrt{2}$.</span></span> <span data-ttu-id="6a0e4-148">Ein EPR-Paar wird auch als [Glocken Zustand](xref:microsoft.quantum.glossary#bell-state) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-148">An EPR pair is also known as a [Bell state](xref:microsoft.quantum.glossary#bell-state)</span></span>

## <a name="evolution"></a><span data-ttu-id="6a0e4-149">Entwicklungs</span><span class="sxs-lookup"><span data-stu-id="6a0e4-149">Evolution</span></span>

<span data-ttu-id="6a0e4-150">Die Art und Weise, in der sich ein [Quantum-Zustand](xref:microsoft.quantum.glossary#quantum-state)</span><span class="sxs-lookup"><span data-stu-id="6a0e4-150">How a [quantum state](xref:microsoft.quantum.glossary#quantum-state) changes over time.</span></span> <span data-ttu-id="6a0e4-151">Weitere Informationen finden Sie unter [Matrix exponentiale](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-151">For more information, see [Matrix exponentials](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).</span></span>

## <a name="function"></a><span data-ttu-id="6a0e4-152">Funktion</span><span class="sxs-lookup"><span data-stu-id="6a0e4-152">Function</span></span>
<span data-ttu-id="6a0e4-153">Ein Typ von Unterroutine in der Q #-Sprache, der rein klassisch (nicht Quantum) ist.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-153">A type of subroutine in the Q# language that is purely classical (non-quantum).</span></span> <span data-ttu-id="6a0e4-154">Obwohl Funktionen innerhalb von Quantum-Algorithmen verwendet werden, können Sie nicht auf [Qubits](xref:microsoft.quantum.glossary#qubit) oder Aufrufe von [Vorgängen](xref:microsoft.quantum.glossary#operation)reagieren.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-154">While functions are used within quantum algorithms, they cannot act on [qubits](xref:microsoft.quantum.glossary#qubit) or call [operations](xref:microsoft.quantum.glossary#operation).</span></span> <span data-ttu-id="6a0e4-155">Weitere Informationen finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-155">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="gate"></a><span data-ttu-id="6a0e4-156">Tors</span><span class="sxs-lookup"><span data-stu-id="6a0e4-156">Gate</span></span>

<span data-ttu-id="6a0e4-157">Ein Legacy Begriff für einen Quantum- [Vorgang](xref:microsoft.quantum.glossary#operation), der auf dem Konzept der klassischen Logik Gates basiert.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-157">A legacy term for a quantum [operation](xref:microsoft.quantum.glossary#operation), based on the concept of classical logic gates.</span></span> <span data-ttu-id="6a0e4-158">Eine [Quantum](xref:microsoft.quantum.glossary#quantum-circuit-diagram) -Verbindung ist ein Netzwerk von Gates (oder Vorgängen), das auf dem gleichen Konzept klassischer Logik Leitungen basiert.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-158">A [quantum circuit](xref:microsoft.quantum.glossary#quantum-circuit-diagram) is a network of gates (or operations), based on the similar concept of classical logic circuits.</span></span>

## <a name="global-phase"></a><span data-ttu-id="6a0e4-159">Globale Phase</span><span class="sxs-lookup"><span data-stu-id="6a0e4-159">Global phase</span></span>

<span data-ttu-id="6a0e4-160">Wenn zwei [Zustände](xref:microsoft.quantum.glossary#quantum-state) mit einem Vielfachen einer komplexen Zahl $e ^ {i $ identisch sind \phi } , werden Sie sich bis zu einer globalen Phase unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-160">When two [states](xref:microsoft.quantum.glossary#quantum-state) are identical up to a multiple of a complex number $e^{i\phi}$, they are said to differ up to a global phase.</span></span> <span data-ttu-id="6a0e4-161">Im Gegensatz zu lokalen Phasen können globale Phasen nicht durch eine beliebige [Measurment](xref:microsoft.quantum.glossary#measurement)beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-161">Unlike local phases, global phases cannot be observed through any [measurment](xref:microsoft.quantum.glossary#measurement).</span></span> <span data-ttu-id="6a0e4-162">Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-162">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="hadamard"></a><span data-ttu-id="6a0e4-163">Hadamard</span><span class="sxs-lookup"><span data-stu-id="6a0e4-163">Hadamard</span></span>

<span data-ttu-id="6a0e4-164">Der Hadamard-Vorgang (auch als Hadamard-Gate oder-Transformation bezeichnet) agiert mit einem einzelnen [Qubit](xref:microsoft.quantum.glossary#qubit) und versetzt ihn in eine gerade [Superposition](xref:microsoft.quantum.glossary#superposition) von $ \ket{0$ } oder $ \ket{1$, } Wenn sich das Qubit anfänglich im $ \ket{0$- } Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-164">The Hadamard operation (also referred to as the Hadamard gate or transform) acts on a single [qubit](xref:microsoft.quantum.glossary#qubit) and puts it in an even [superposition](xref:microsoft.quantum.glossary#superposition) of $\ket{0}$ or $\ket{1}$ if the qubit is initially in the $\ket{0}$ state.</span></span> <span data-ttu-id="6a0e4-165">In f # wird dieser Vorgang durch den vordefinierten [`H`](xref:microsoft.quantum.intrinsic.h) Vorgang angewendet.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-165">In Q#, this operation is applied by the pre-defined [`H`](xref:microsoft.quantum.intrinsic.h) operation.</span></span>

## <a name="immutable"></a><span data-ttu-id="6a0e4-166">Unveränderlich</span><span class="sxs-lookup"><span data-stu-id="6a0e4-166">Immutable</span></span>

<span data-ttu-id="6a0e4-167">Eine Variable, deren Wert nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-167">A variable whose value cannot be changed.</span></span> <span data-ttu-id="6a0e4-168">Eine unveränderliche Variable in Q # wird mit dem- `let` Schlüsselwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-168">An immutable variable in Q# is created using the `let` keyword.</span></span> <span data-ttu-id="6a0e4-169">Verwenden Sie zum Deklarieren von Variablen, die geändert werden *können* , das [änderbare](xref:microsoft.quantum.glossary#immutable) -Schlüsselwort, um und das-Schlüsselwort zu deklarieren und den `set` Wert</span><span class="sxs-lookup"><span data-stu-id="6a0e4-169">To declare variables that *can* be changed, use the [mutable](xref:microsoft.quantum.glossary#immutable) keyword to declare and the `set` keyword to modify the value.</span></span> 

## <a name="measurement"></a><span data-ttu-id="6a0e4-170">Messung</span><span class="sxs-lookup"><span data-stu-id="6a0e4-170">Measurement</span></span>

<span data-ttu-id="6a0e4-171">Eine Manipulation eines [Qubits](xref:microsoft.quantum.glossary#qubit) (oder eines Satzes von Qubits), der das Ergebnis einer Beobachtung ergibt, was das Abrufen eines klassischen Bits bewirkt.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-171">A manipulation of a [qubit](xref:microsoft.quantum.glossary#qubit) (or set of qubits) that yields the result of an observation, in effect obtaining a classical bit.</span></span> <span data-ttu-id="6a0e4-172">Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-172">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).</span></span>

## <a name="mutable"></a><span data-ttu-id="6a0e4-173">Veränderlich</span><span class="sxs-lookup"><span data-stu-id="6a0e4-173">Mutable</span></span>

<span data-ttu-id="6a0e4-174">Eine Variable, deren Wert geändert werden kann, nachdem Sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-174">A variable whose value may be changed after it is created.</span></span> <span data-ttu-id="6a0e4-175">Eine änderbare Variable in Q # wird mit dem `mutable` -Schlüsselwort deklariert und mithilfe des- `set` Schlüssel Worts geändert.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-175">A mutable variable in Q# is declared using the `mutable` keyword and modified using the `set` keyword.</span></span> <span data-ttu-id="6a0e4-176">Mit dem `let` -Schlüsselwort erstellte Variablen sind [unveränderlich](xref:microsoft.quantum.glossary#immutable) , und ihr Wert kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-176">Variables created with the `let` keyword are [immutable](xref:microsoft.quantum.glossary#immutable) and their value cannot be changed.</span></span>

## <a name="namespace"></a><span data-ttu-id="6a0e4-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="6a0e4-177">Namespace</span></span>

<span data-ttu-id="6a0e4-178">Eine Bezeichnung für eine Auflistung verwandter Namen (d. h. [Vorgänge](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function)und [benutzerdefinierte Typen](xref:microsoft.quantum.glossary#user-defined-type)).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-178">A label for a collection of related names (i.e., [operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function), and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type)).</span></span> <span data-ttu-id="6a0e4-179">Beispielsweise zeichnet der Namespace [Microsoft. Quantum. Preparation](xref:microsoft.quantum.preparation) alle Symbole auf, die in der Standardbibliothek definiert sind und bei der Vorbereitung von anfänglichen Zuständen helfen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-179">For instance the namespace [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) labels all of the symbols defined in the standard library that help with preparing initial states.</span></span>

## <a name="operation"></a><span data-ttu-id="6a0e4-180">Vorgang</span><span class="sxs-lookup"><span data-stu-id="6a0e4-180">Operation</span></span>

<span data-ttu-id="6a0e4-181">Die grundlegende Einheit der Quantum-Ausführung in Q #.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-181">The basic unit of quantum execution in Q#.</span></span> <span data-ttu-id="6a0e4-182">Dies entspricht ungefähr einer Funktion in C, C++ oder python oder einer statischen Methode in c# oder Java.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-182">It is roughly equivalent to a function in C, C++ or Python, or a static method in C# or Java.</span></span> <span data-ttu-id="6a0e4-183">Weitere Informationen finden Sie unter [Vorgänge und Funktionen](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-183">For more information, see [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="operator-application"></a><span data-ttu-id="6a0e4-184">Operator Anwendung</span><span class="sxs-lookup"><span data-stu-id="6a0e4-184">Operator application</span></span>

<span data-ttu-id="6a0e4-185">Ausführen eines Quantum-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-185">Performing a quantum operation.</span></span> <span data-ttu-id="6a0e4-186">Dadurch wird in der Regel eine einheitliche Matrix auf den aktuellen Quantum-Status Vektor angewendet.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-186">This typically applies a unitary matrix to the current quantum state vector.</span></span>

## <a name="oracle"></a><span data-ttu-id="6a0e4-187">Oracle</span><span class="sxs-lookup"><span data-stu-id="6a0e4-187">Oracle</span></span>

<span data-ttu-id="6a0e4-188">Eine Unterroutine, die zur Laufzeit Daten abhängige Informationen für einen Quantum-Algorithmus bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-188">A subroutine that provides data-dependent information to a quantum algorithm at runtime.</span></span> <span data-ttu-id="6a0e4-189">In der Regel besteht das Ziel darin, eine [Superposition](xref:microsoft.quantum.glossary#superposition) der Ausgaben bereitzustellen, die den Eingaben in der superposition entsprechen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-189">Typically, the goal is to provide a [superposition](xref:microsoft.quantum.glossary#superposition) of outputs corresponding to inputs that are in superposition.</span></span> <span data-ttu-id="6a0e4-190">Weitere Informationen finden Sie unter [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-190">For more information, see [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).</span></span>

## <a name="partial-application"></a><span data-ttu-id="6a0e4-191">Partielle Anwendung</span><span class="sxs-lookup"><span data-stu-id="6a0e4-191">Partial application</span></span>

<span data-ttu-id="6a0e4-192">Aufrufen einer [Funktion](xref:microsoft.quantum.glossary#function) oder eines [Vorgangs](xref:microsoft.quantum.glossary#operation) ohne alle erforderlichen Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-192">Calling a [function](xref:microsoft.quantum.glossary#function) or [operation](xref:microsoft.quantum.glossary#operation) without all the required inputs.</span></span> <span data-ttu-id="6a0e4-193">Dadurch wird eine neue [Aufruf Bare](xref:microsoft.quantum.glossary#callable) zurückgegeben, bei der nur die fehlenden Parameter (die durch einen Unterstrich angegeben werden) während einer zukünftigen Anwendung bereitgestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-193">This returns a new [callable](xref:microsoft.quantum.glossary#callable) that only needs the missing parameters (indicated by an underscore) to be supplied during a future application.</span></span> <span data-ttu-id="6a0e4-194">Beispielsweise können Sie mit der-Funktion Sie `MyFunc(x : int, y : int) : int {return x + y;}` teilweise auf eine neue Funktion anwenden `let NewFunc = MyFunc(_, 3)` .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-194">For example, given the function `MyFunc(x : int, y : int) : int {return x + y;}` you can partially apply it to a new function `let NewFunc = MyFunc(_, 3)`.</span></span> <span data-ttu-id="6a0e4-195">Anschließend können Sie die neue Funktion zu einem späteren Zeitpunkt mit dem fehlenden Parameter aufrufen `NewFunc(2)` , der den Wert *5*zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-195">You can then call the new function at a later time with the missing parameter `NewFunc(2)` which returns the value *5*.</span></span>  <span data-ttu-id="6a0e4-196">Weitere Informationen finden Sie unter [partielle Anwendung](xref:microsoft.quantum.guide.operationsfunctions#partial-application).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-196">For more information, see [Partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application).</span></span>

## <a name="pauli-operators"></a><span data-ttu-id="6a0e4-197">Pauli-Operatoren</span><span class="sxs-lookup"><span data-stu-id="6a0e4-197">Pauli operators</span></span>

<span data-ttu-id="6a0e4-198">Ein Satz von drei einheitlichen Matrizen, die als `X` , `Y` und Quantum-Vorgänge bezeichnet werden `Z` .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-198">A set of three 2 x 2 unitary matrices known as the `X`, `Y` and `Z` quantum operations.</span></span> <span data-ttu-id="6a0e4-199">Die Identitätsmatrix, $I $ , ist häufig auch in der Gruppe enthalten.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-199">The identity matrix, $I$, is often included in the set as well.</span></span>  <span data-ttu-id="6a0e4-200">$I = \begin{ bmatrix } 1 & 0 \\ \\ 0 & 1 \end{ bmatrix } $, $X = \begin{ bmatrix } 0 & 1 \\ \\ 1 & 0 \end{ bmatrix } $, $Y = \begin{ bmatrix } 0 &-i \\ \\ i & 0 \end{ bmatrix } $, $Z = \begin{ bmatrix } 1 & 0 \\ \\ 0 &-1 \end{ bmatrix } $.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-200">$I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix}$, $X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix}$, $Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix}$, $Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix}$.</span></span>   <span data-ttu-id="6a0e4-201">Weitere Informationen finden Sie unter [Single-Qubit-Vorgänge](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-201">For more information, see [Single-qubit operations](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).</span></span>

## <a name="quantum-circuit-diagram"></a><span data-ttu-id="6a0e4-202">Quantum-Verbindungs Diagramm</span><span class="sxs-lookup"><span data-stu-id="6a0e4-202">Quantum circuit diagram</span></span>

<span data-ttu-id="6a0e4-203">Eine Methode zur grafischen Darstellung der Abfolge von [Vorgängen](xref:microsoft.quantum.glossary#operation) (oder [Gates](xref:microsoft.quantum.glossary#gate)) für einfache Quantum-Programme, z. b.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-203">A method to graphically represent the sequence of [operations](xref:microsoft.quantum.glossary#operation) (or [gates](xref:microsoft.quantum.glossary#gate)) for simple quantum programs, for example</span></span> 

![Beispiel für ein Verbindungs Diagramm](~/media/qpe.png)<span data-ttu-id="6a0e4-205">.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-205">.</span></span> 

<span data-ttu-id="6a0e4-206">Weitere Informationen finden Sie unter [Quantum](xref:microsoft.quantum.concepts.circuits)-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-206">For more information, see [Quantum circuits](xref:microsoft.quantum.concepts.circuits).</span></span>

## <a name="quantum-libraries"></a><span data-ttu-id="6a0e4-207">Quantum-Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="6a0e4-207">Quantum libraries</span></span>

<span data-ttu-id="6a0e4-208">Auflistungen von [Vorgängen](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function) und [benutzerdefinierten Typen](xref:microsoft.quantum.glossary#user-defined-type) zum Erstellen von Q #-Programmen.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-208">Collections of [operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function) and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) for creating Q# programs.</span></span> <span data-ttu-id="6a0e4-209">Die [Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro) wird standardmäßig installiert.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-209">The [Standard library](xref:microsoft.quantum.libraries.standard.intro) is installed by default.</span></span> <span data-ttu-id="6a0e4-210">Weitere verfügbare Bibliotheken sind die [Chemie Bibliothek](xref:microsoft.quantum.chemistry.concepts.intro), die [Numerics-Bibliothek](xref:microsoft.quantum.numerics.intro) und die [Machine Learning-Bibliothek](xref:microsoft.quantum.machine-learning.concepts.intro).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-210">Other libraries available are the [Chemistry library](xref:microsoft.quantum.chemistry.concepts.intro), the [Numerics library](xref:microsoft.quantum.numerics.intro) and the [Machine learning library](xref:microsoft.quantum.machine-learning.concepts.intro).</span></span>

## <a name="quantum-state"></a><span data-ttu-id="6a0e4-211">Quantum-Status</span><span class="sxs-lookup"><span data-stu-id="6a0e4-211">Quantum state</span></span>

<span data-ttu-id="6a0e4-212">Der genaue Zustand eines isolierten Quantum-Systems, von dem [Mess](xref:microsoft.quantum.glossary#measurement) Wahrscheinlichkeiten extrahiert werden können.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-212">The precise state of an isolated quantum system, from which [measurement](xref:microsoft.quantum.glossary#measurement) probabilities can be extracted.</span></span> <span data-ttu-id="6a0e4-213">In Quantum Computing verwendet der Quantum-Simulator diese Informationen, um zu simulieren, wie Qubits auf Vorgänge reagieren.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-213">In quantum computing, the quantum simulator uses this information to simulate how qubits respond to operations.</span></span> <span data-ttu-id="6a0e4-214">Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-214">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="qubit"></a><span data-ttu-id="6a0e4-215">Qubit</span><span class="sxs-lookup"><span data-stu-id="6a0e4-215">Qubit</span></span>

<span data-ttu-id="6a0e4-216">Eine grundlegende Einheit von Quantum-Informationen, analog zu einem *Bit* im klassischen Computing.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-216">A basic unit of quantum information, analogous to a *bit* in classical computing.</span></span> <span data-ttu-id="6a0e4-217">Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-217">For more information, see [The Qubit](xref:microsoft.quantum.concepts.qubit).</span></span>

## <a name="repeat-until-success"></a><span data-ttu-id="6a0e4-218">Wiederholung-bis-Erfolg</span><span class="sxs-lookup"><span data-stu-id="6a0e4-218">Repeat-until-success</span></span>

<span data-ttu-id="6a0e4-219">Ein Quantum-Algorithmus, der probabilistisch erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-219">A quantum algorithm that probabilistically succeeds.</span></span> <span data-ttu-id="6a0e4-220">Bei einem Fehler wird die Routine so lange wiederholt, bis Sie erfolgreich ist (oder ein Grenzwert erreicht wurde).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-220">Upon failure, the routine will retry until successful (or a limit has been reached).</span></span> <span data-ttu-id="6a0e4-221">Weitere Informationen finden Sie unter [Wiederholen bis Erfolg (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop) .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-221">For more information, see [Repeat Until Success (RUS)](xref:microsoft.quantum.guide.controlflow#repeat-until-success-loop)</span></span>

## <a name="standard-libraries"></a><span data-ttu-id="6a0e4-222">Standardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="6a0e4-222">Standard libraries</span></span>

<span data-ttu-id="6a0e4-223">[Vorgänge](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function) und [benutzerdefinierte Typen](xref:microsoft.quantum.glossary#user-defined-type) , die während der Installation zusammen mit dem Q #-Compiler installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-223">[Operations](xref:microsoft.quantum.glossary#operation), [functions](xref:microsoft.quantum.glossary#function) and [user-defined types](xref:microsoft.quantum.glossary#user-defined-type) that are installed along with the Q# compiler during installation.</span></span> <span data-ttu-id="6a0e4-224">Die Implementierung der Standardbibliothek ist in Bezug auf die Zielcomputer agnostisch.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-224">The standard library implementation is agnostic with respect to target machines.</span></span> <span data-ttu-id="6a0e4-225">Weitere Informationen finden Sie unter [Standard Bibliotheken](xref:microsoft.quantum.libraries.standard.intro).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-225">For more information, see [Standard libraries](xref:microsoft.quantum.libraries.standard.intro).</span></span>

## <a name="superposition"></a><span data-ttu-id="6a0e4-226">Superposition</span><span class="sxs-lookup"><span data-stu-id="6a0e4-226">Superposition</span></span>

<span data-ttu-id="6a0e4-227">Das Konzept von Quantum Computing, dass ein [Qubit](xref:microsoft.quantum.glossary#qubit) eine lineare Kombination aus zwei Zuständen ist, $ \ket{0$ } und $ \ket{1$ } , bis es [gemessen](xref:microsoft.quantum.glossary#measurement)wird.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-227">The concept in quantum computing that a [qubit](xref:microsoft.quantum.glossary#qubit) is a linear combination of two states, $\ket{0}$ and $\ket{1}$, until it is [measured](xref:microsoft.quantum.glossary#measurement).</span></span>  <span data-ttu-id="6a0e4-228">Weitere Informationen finden Sie Untergrund Legendes zu [Quantum Computing](xref:microsoft.quantum.overview.understanding).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-228">For more information, see [Understanding quantum computing](xref:microsoft.quantum.overview.understanding).</span></span>

## <a name="target-machine"></a><span data-ttu-id="6a0e4-229">Zielcomputer</span><span class="sxs-lookup"><span data-stu-id="6a0e4-229">Target machine</span></span>

<span data-ttu-id="6a0e4-230">Ein Kompilierungs Ziel, das ein abstraktes Quantum-Programm auf Hardware oder Simulation senkt.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-230">A compilation target that lowers an abstract quantum program towards hardware or simulation.</span></span> <span data-ttu-id="6a0e4-231">Dies schließt in der Regel Umschreib Vorgänge für viele Zwecke ein, einschließlich Gate-Ersetzung, Codierung für die Fehlerkorrektur, geometrisches Layout und andere.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-231">This typically include re-writes for many purposes including gate replacement, encoding for error correction, geometric layout and others.</span></span> <span data-ttu-id="6a0e4-232">Weitere Informationen finden Sie unter [Quantum Simulatoren und Host Applications](xref:microsoft.quantum.machines).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-232">For more information, see [Quantum simulators and host applications](xref:microsoft.quantum.machines).</span></span>

## <a name="teleportation"></a><span data-ttu-id="6a0e4-233">Teleportation</span><span class="sxs-lookup"><span data-stu-id="6a0e4-233">Teleportation</span></span>

<span data-ttu-id="6a0e4-234">Eine Methode zum erneuten Generieren von Daten (bzw. des [Quantums](xref:microsoft.quantum.glossary#quantum-state)) von einem [Qubit](xref:microsoft.quantum.glossary#qubit) von einem Ort zu einem anderen, ohne dass das Qubit mithilfe von [jede Verflechtungen](xref:microsoft.quantum.glossary#entanglement) und [Messung](xref:microsoft.quantum.glossary#measurement)physisch verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-234">A method for regenerating data, or the [quantum state](xref:microsoft.quantum.glossary#quantum-state), of one [qubit](xref:microsoft.quantum.glossary#qubit) from one place to another without physically moving the qubit, using [entanglement](xref:microsoft.quantum.glossary#entanglement) and [measurement](xref:microsoft.quantum.glossary#measurement).</span></span>  <span data-ttu-id="6a0e4-235">Weitere Informationen finden Sie unter [Quantum](xref:microsoft.quantum.concepts.circuits) -Verbindungen und die jeweilige Kata bei [Quantum Katas](xref:microsoft.quantum.overview.katas).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-235">For more information, see [Quantum circuits](xref:microsoft.quantum.concepts.circuits) and the respective kata at [Quantum Katas](xref:microsoft.quantum.overview.katas).</span></span>

## <a name="tuple"></a><span data-ttu-id="6a0e4-236">Tupel</span><span class="sxs-lookup"><span data-stu-id="6a0e4-236">Tuple</span></span>

<span data-ttu-id="6a0e4-237">Eine Auflistung von durch Trennzeichen getrennten Werten, die als einzelner Wert fungieren.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-237">A collection of comma-separated values that acts as a single value.</span></span> <span data-ttu-id="6a0e4-238">Der *Typ* eines Tupels wird durch die Typen der darin enthaltenen Werte definiert.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-238">The *type* of a tuple is defined by the types of values it contains.</span></span> <span data-ttu-id="6a0e4-239">In Q # sind Tupel [unveränderlich und können geschmustet](xref:microsoft.quantum.glossary#immutable) werden, Arrays enthalten oder in einem Array verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-239">In Q#, tuples are [immutable](xref:microsoft.quantum.glossary#immutable) and can be nested, contain arrays, or used in an array.</span></span> <span data-ttu-id="6a0e4-240">Weitere Informationen finden Sie unter [Tupeltypen](xref:microsoft.quantum.guide.types#tuple-types).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-240">For more information, see [Tuple types](xref:microsoft.quantum.guide.types#tuple-types).</span></span>

## <a name="unitary-operator"></a><span data-ttu-id="6a0e4-241">Einheitlicher Operator</span><span class="sxs-lookup"><span data-stu-id="6a0e4-241">Unitary operator</span></span>

<span data-ttu-id="6a0e4-242">Ein Operator, dessen Umkehrung gleich dem zugehörigen [Adjoint](xref:microsoft.quantum.glossary#adjoint)ist, d. h. $uu ^ {\dagger } = \id $ .</span><span class="sxs-lookup"><span data-stu-id="6a0e4-242">An operator whose inverse is equal to its [adjoint](xref:microsoft.quantum.glossary#adjoint), i.e., $UU^{\dagger} = \id$.</span></span>

## <a name="user-defined-type"></a><span data-ttu-id="6a0e4-243">Benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="6a0e4-243">User-defined type</span></span>

<span data-ttu-id="6a0e4-244">Eine Auflistung integrierter oder zuvor definierter Typen, auf die als einzelne Einheit verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6a0e4-244">A collection of built-in or previously defined types that may be referred to as a single unit.</span></span> <span data-ttu-id="6a0e4-245">Weitere Informationen finden Sie unter [benutzerdefinierte Typen](xref:microsoft.quantum.guide.types#user-defined-types).</span><span class="sxs-lookup"><span data-stu-id="6a0e4-245">For more information, see [User-defined types](xref:microsoft.quantum.guide.types#user-defined-types).</span></span>