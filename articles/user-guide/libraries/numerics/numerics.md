---
title: Verwenden der Microsoft Q# Numerics-Bibliothek
description: Erfahren Sie mehr über die Typen und Vorgänge, die in der Microsoft Quantum-Numerics-Bibliothek verfügbar sind.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.usage
no-loc:
- Q#
- $$v
ms.openlocfilehash: 474fc74b9c92fbf28c0618a3090905d025699d32
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868796"
---
# <a name="using-the-numerics-library"></a><span data-ttu-id="b23c8-103">Verwenden der Numerics-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b23c8-103">Using the Numerics library</span></span>

## <a name="overview"></a><span data-ttu-id="b23c8-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b23c8-104">Overview</span></span>

<span data-ttu-id="b23c8-105">Die Numerics-Bibliothek besteht aus drei Komponenten.</span><span class="sxs-lookup"><span data-stu-id="b23c8-105">The Numerics library consists of three components</span></span>

1. <span data-ttu-id="b23c8-106">**Einfache ganzzahlige Arithmetik** mit ganzzahligen addern und Comparatoren</span><span class="sxs-lookup"><span data-stu-id="b23c8-106">**Basic integer arithmetic** with integer adders and comparators</span></span>
1. <span data-ttu-id="b23c8-107">Allgemeine **ganzzahlige Funktionalität** , die auf Grundlage der grundlegenden Funktionalität basiert. Es umfasst Multiplikation, Division, Inversion usw.  für ganze Zahlen mit und ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b23c8-107">**High-level integer functionality** that is built on top of the basic  functionality; it includes multiplication, division, inversion, etc.  for signed and unsigned integers.</span></span>
1. <span data-ttu-id="b23c8-108">**Arithmetische Funktionalität mit festem Punkt** mit Initialisierung mit festem Punkt, Addition, Multiplikation, gegenseitiger Auswertung, polynomgebung und Messung.</span><span class="sxs-lookup"><span data-stu-id="b23c8-108">**Fixed-point arithmetic functionality** with fixed-point initialization,  addition, multiplication, reciprocal, polynomial evaluation, and measurement.</span></span>

<span data-ttu-id="b23c8-109">Auf alle diese Komponenten kann mit einer einzelnen-Anweisung zugegriffen werden `open` :</span><span class="sxs-lookup"><span data-stu-id="b23c8-109">All of these components can be accessed using a single `open` statement:</span></span>
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a><span data-ttu-id="b23c8-110">Typen</span><span class="sxs-lookup"><span data-stu-id="b23c8-110">Types</span></span>

<span data-ttu-id="b23c8-111">Die Numerics-Bibliothek unterstützt die folgenden Typen:</span><span class="sxs-lookup"><span data-stu-id="b23c8-111">The numerics library supports the following types</span></span>

1. <span data-ttu-id="b23c8-112">**`LittleEndian`**: Ein Qubit-Array `qArr : Qubit[]` , das eine Ganzzahl darstellt, wobei `qArr[0]` das unwichtigste Bit bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b23c8-112">**`LittleEndian`**: A qubit array `qArr : Qubit[]` that represents an integer where `qArr[0]` denotes the least significant bit.</span></span>
1. <span data-ttu-id="b23c8-113">**`SignedLittleEndian`**: Identisch `LittleEndian` mit, mit der Ausnahme, dass es sich um eine ganze Zahl mit Vorzeichen handelt, die in zwei-</span><span class="sxs-lookup"><span data-stu-id="b23c8-113">**`SignedLittleEndian`**: Same as `LittleEndian` except that it represents a signed integer stored in two's complement.</span></span>
1. <span data-ttu-id="b23c8-114">**`FixedPoint`**: Stellt eine reelle Zahl dar, die aus einem Qubit `qArr2 : Qubit[]` -Array und einer binären Punktposition besteht `pos` , die die Anzahl der binären Ziffern links vom binären Punkt zählt.</span><span class="sxs-lookup"><span data-stu-id="b23c8-114">**`FixedPoint`**: Represents a real number consisting of a qubit array `qArr2 : Qubit[]` and a binary point position `pos`, which counts the number of binary digits to the left of the binary point.</span></span> <span data-ttu-id="b23c8-115">`qArr2`wird auf die gleiche Weise wie gespeichert `SignedLittleEndian` .</span><span class="sxs-lookup"><span data-stu-id="b23c8-115">`qArr2` is stored in the same way as `SignedLittleEndian`.</span></span>

## <a name="operations"></a><span data-ttu-id="b23c8-116">Operationen (Operations)</span><span class="sxs-lookup"><span data-stu-id="b23c8-116">Operations</span></span>

<span data-ttu-id="b23c8-117">Für jeden der drei oben genannten Typen stehen eine Vielzahl von Vorgängen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="b23c8-117">For each of the three types above, a variety of operations is available:</span></span>

1. **`LittleEndian`**
    - <span data-ttu-id="b23c8-118">Addition</span><span class="sxs-lookup"><span data-stu-id="b23c8-118">Addition</span></span>
    - <span data-ttu-id="b23c8-119">Vergleich</span><span class="sxs-lookup"><span data-stu-id="b23c8-119">Comparison</span></span>
    - <span data-ttu-id="b23c8-120">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="b23c8-120">Multiplication</span></span>
    - <span data-ttu-id="b23c8-121">Quadrieren</span><span class="sxs-lookup"><span data-stu-id="b23c8-121">Squaring</span></span>
    - <span data-ttu-id="b23c8-122">Division (mit Rest)</span><span class="sxs-lookup"><span data-stu-id="b23c8-122">Division (with remainder)</span></span>

1. **`SignedLittleEndian`**
    - <span data-ttu-id="b23c8-123">Addition</span><span class="sxs-lookup"><span data-stu-id="b23c8-123">Addition</span></span>
    - <span data-ttu-id="b23c8-124">Vergleich</span><span class="sxs-lookup"><span data-stu-id="b23c8-124">Comparison</span></span>
    - <span data-ttu-id="b23c8-125">Inversion von Modulo 2</span><span class="sxs-lookup"><span data-stu-id="b23c8-125">Inversion modulo 2's complement</span></span>
    - <span data-ttu-id="b23c8-126">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="b23c8-126">Multiplication</span></span>
    - <span data-ttu-id="b23c8-127">Quadrieren</span><span class="sxs-lookup"><span data-stu-id="b23c8-127">Squaring</span></span>

1. **`FixedPoint`**
    - <span data-ttu-id="b23c8-128">Vorbereitung/Initialisierung für klassische Werte</span><span class="sxs-lookup"><span data-stu-id="b23c8-128">Preparation / initialization to a classical values</span></span>
    - <span data-ttu-id="b23c8-129">Addition (klassische Konstante oder andere Quantum-Fixpunkte)</span><span class="sxs-lookup"><span data-stu-id="b23c8-129">Addition (classical constant or other quantum fixed-point)</span></span>
    - <span data-ttu-id="b23c8-130">Vergleich</span><span class="sxs-lookup"><span data-stu-id="b23c8-130">Comparison</span></span>
    - <span data-ttu-id="b23c8-131">Multiplikation</span><span class="sxs-lookup"><span data-stu-id="b23c8-131">Multiplication</span></span>
    - <span data-ttu-id="b23c8-132">Quadrieren</span><span class="sxs-lookup"><span data-stu-id="b23c8-132">Squaring</span></span>
    - <span data-ttu-id="b23c8-133">Polynomial Evaluation with Spezialisierung for even and Odd Functions</span><span class="sxs-lookup"><span data-stu-id="b23c8-133">Polynomial evaluation with specialization for even and odd functions</span></span>
    - <span data-ttu-id="b23c8-134">Gegenseitige (1/x)</span><span class="sxs-lookup"><span data-stu-id="b23c8-134">Reciprocal (1/x)</span></span>
    - <span data-ttu-id="b23c8-135">Messung (klassisches Double)</span><span class="sxs-lookup"><span data-stu-id="b23c8-135">Measurement (classical Double)</span></span>

<span data-ttu-id="b23c8-136">Weitere Informationen und eine ausführliche Dokumentation zu den einzelnen Vorgängen finden Sie in der Referenz Dokumentation der Q# Bibliothek unter [docs.Microsoft.com](https://docs.microsoft.com/quantum) .</span><span class="sxs-lookup"><span data-stu-id="b23c8-136">For more information and detailed documentation for each of these operations, see the Q# library reference docs at [docs.microsoft.com](https://docs.microsoft.com/quantum)</span></span>

## <a name="sample-integer-addition"></a><span data-ttu-id="b23c8-137">Beispiel: Hinzufügen einer Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="b23c8-137">Sample: Integer addition</span></span>

<span data-ttu-id="b23c8-138">Als einfaches Beispiel angenommen, der Vorgang ist $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $, d. h. ein Vorgang, der eine n-Qubit-Ganzzahl $x $ und ein n-oder (n + 1)-Qubit-Register $y $ als Eingabe annimmt. letztere wird der Summe $ (x + y)</span><span class="sxs-lookup"><span data-stu-id="b23c8-138">As a basic example, consider the operation $$ \ket x\ket y\mapsto \ket x\ket{x+y} $$ that is, an operation that takes an n-qubit integer $x$ and an n- or (n+1)-qubit register $y$ as input, the latter of which it maps to the sum $(x+y)$.</span></span> <span data-ttu-id="b23c8-139">Beachten Sie, dass die Summe berechnet wird, Modulo $2 ^ n $, wenn $y $ in einem $n $-Bit-Register gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="b23c8-139">Note that the sum is computed modulo $2^n$ if $y$ is stored in an $n$-bit register.</span></span>

<span data-ttu-id="b23c8-140">Mit dem Quantum Development Kit kann dieser Vorgang wie folgt angewendet werden:</span><span class="sxs-lookup"><span data-stu-id="b23c8-140">Using the Quantum Development Kit, this operation can be applied as follows:</span></span>
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a><span data-ttu-id="b23c8-141">Beispiel: Auswerten von Smooth Functions</span><span class="sxs-lookup"><span data-stu-id="b23c8-141">Sample: Evaluating smooth functions</span></span>

<span data-ttu-id="b23c8-142">Zum Auswerten von Smooth-Funktionen wie z. b. $ \sin (x) $ auf einem Quantum-Computer, bei dem $x $ eine Quantum- `FixedPoint` Zahl ist, stellt die-Numerics-Bibliothek des Quantum Development Kits die Vorgänge `EvaluatePolynomialFxP` und bereit `Evaluate[Even/Odd]PolynomialFxP` .</span><span class="sxs-lookup"><span data-stu-id="b23c8-142">To evaluate smooth functions such as $\sin(x)$ on a quantum computer, where $x$ is a quantum `FixedPoint` number, the Quantum Development Kit numerics library provides the operations `EvaluatePolynomialFxP` and `Evaluate[Even/Odd]PolynomialFxP`.</span></span>

<span data-ttu-id="b23c8-143">Mit dem ersten, `EvaluatePolynomialFxP` , kann ein Polynoms der Form $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $ ausgewertet werden, wobei $d $ den *Grad*angibt.</span><span class="sxs-lookup"><span data-stu-id="b23c8-143">The first, `EvaluatePolynomialFxP`, allows to evaluate a polynomial of the form $$ P(x) = a_0 + a_1x + a_2x^2 + \cdots + a_dx^d, $$ where $d$ denotes the *degree*.</span></span> <span data-ttu-id="b23c8-144">Dazu benötigen Sie lediglich die Polynomen `[a_0,..., a_d]` (vom Typ `Double[]` ), die Eingabe `x : FixedPoint` und die Ausgabe `y : FixedPoint` (anfänglich NULL):</span><span class="sxs-lookup"><span data-stu-id="b23c8-144">To do so, all that is needed are the polynomial coefficients `[a_0,..., a_d]` (of type `Double[]`), the input `x : FixedPoint` and the output `y : FixedPoint` (initially zero):</span></span>
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="b23c8-145">Das Ergebnis, $P (x) = 1 + 2x $, wird in gespeichert `yFxP` .</span><span class="sxs-lookup"><span data-stu-id="b23c8-145">The result, $P(x)=1+2x$, will be stored in `yFxP`.</span></span>

<span data-ttu-id="b23c8-146">Die zweite, `EvaluateEvenPolynomialFxP` und der dritte, `EvaluateOddPolynomialFxP` , sind Spezialisierungs Fälle für die Fälle der geraden bzw. ungeraden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b23c8-146">The second, `EvaluateEvenPolynomialFxP`, and the third, `EvaluateOddPolynomialFxP`, are specializations for the cases of even and odd functions, respectively.</span></span> <span data-ttu-id="b23c8-147">Das heißt, bei einer geraden/ungeraden Funktion $f (x) $ und $ $ P_ {even} (x) = a_0 + A_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ ist für $P _ {even} (x) $ oder $P _ {Odd} (x): = x\cdot P_ {even} (x) $ gleich gut.</span><span class="sxs-lookup"><span data-stu-id="b23c8-147">That is, for an even/odd function $f(x)$ and $$ P_{even}(x)=a_0 + a_1 x^2 + a_2 x^4 + \cdots + a_d x^{2d}, $$ $f(x)$ is approximated well by $P_{even}(x)$ or $P_{odd}(x) := x\cdot P_{even}(x)$, respectively.</span></span>
<span data-ttu-id="b23c8-148">In Q# können diese beiden Fälle wie folgt behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="b23c8-148">In Q#, these two cases can be handled as follows:</span></span>
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="b23c8-149">wertet $P _ {even} (x) = 1 + 2x ^ 2 $ aus, und</span><span class="sxs-lookup"><span data-stu-id="b23c8-149">which evaluates $P_{even}(x) = 1 + 2x^2$, and</span></span>
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
<span data-ttu-id="b23c8-150">, der $P _ {Odd} (x) = x + 2X ^ 3 $ auswertet.</span><span class="sxs-lookup"><span data-stu-id="b23c8-150">which evaluates $P_{odd}(x) = x + 2x^3$.</span></span>

## <a name="more-samples"></a><span data-ttu-id="b23c8-151">Weitere Beispiele</span><span class="sxs-lookup"><span data-stu-id="b23c8-151">More samples</span></span>

<span data-ttu-id="b23c8-152">Weitere Beispiele finden Sie im [hauptbeispielrepository](https://github.com/Microsoft/Quantum).</span><span class="sxs-lookup"><span data-stu-id="b23c8-152">You can find more samples in the [main samples repository](https://github.com/Microsoft/Quantum).</span></span>

<span data-ttu-id="b23c8-153">Klonen Sie zunächst das Repository, und öffnen Sie den `Numerics` Unterordner:</span><span class="sxs-lookup"><span data-stu-id="b23c8-153">To get started, clone the repo and open the `Numerics` subfolder:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/Numerics
```

<span data-ttu-id="b23c8-154">`cd`In einem der Beispiel Ordner, und führen Sie das Beispiel über aus.</span><span class="sxs-lookup"><span data-stu-id="b23c8-154">Then, `cd` into one of the sample folders and run the sample via</span></span>

```bash
dotnet run
```
