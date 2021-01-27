---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Debug-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855529"
---
# <a name="decomposedon-function"></a><span data-ttu-id="f1d09-102">Debug-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1d09-102">DecomposedOn function</span></span>

<span data-ttu-id="f1d09-103">Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="f1d09-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="f1d09-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f1d09-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f1d09-105">Zerlegt eine permutations für eine Variable.</span><span class="sxs-lookup"><span data-stu-id="f1d09-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="f1d09-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1d09-106">Description</span></span>

<span data-ttu-id="f1d09-107">Bei Angabe einer permutations $ \pi $ ( `perm` ) und eines Index $i $ ( `index` ), diese Methode gibt drei Permutationen $ ((\ pi_l, \ pi_r), \pi ') $ so zurück, dass die Bilder von $ \ pi_l $ und $ \ pi_r $ Bits in ihren Elementen bei anderen Indizes als $i $ und Bilder von $ \pi ' $ do not Change Bit $i $ in ihren Elementen nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="f1d09-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="f1d09-108">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f1d09-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="f1d09-109">Perm: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f1d09-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="f1d09-110">Index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f1d09-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="f1d09-111">Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="f1d09-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>



## <a name="example"></a><span data-ttu-id="f1d09-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f1d09-112">Example</span></span>

<span data-ttu-id="f1d09-113">Angenommen, die Eingabe ist "Perm = [0, 2, 3, 5, 7, 1, 4, 6]" und "Index = 0". dann berechnet diese Funktion drei Permutationen basierend auf der folgenden Tabelle, in der die permutations `perm` in Binär Notation mit Elementen in Gruppe A und Bilder in Gruppe D aufgelistet ist.  In den Spalten werden die bitindizes aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f1d09-113">Assume that the input is perm = [0, 2, 3, 5, 7, 1, 4, 6] and index = 0, then this function computes three permutations based on the following table, which lists the permutation `perm` in binary notation with elements in group A and images in group D.  The columns list the bit indices.</span></span>

<span data-ttu-id="f1d09-114">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="f1d09-114">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="f1d09-115">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-115">2 1 0</span></span> | <span data-ttu-id="f1d09-116">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-116">2 1 0</span></span> | <span data-ttu-id="f1d09-117">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-117">2 1 0</span></span> | <span data-ttu-id="f1d09-118">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-118">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="f1d09-119">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-119">0 0 0</span></span> |       |       | <span data-ttu-id="f1d09-120">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-120">0 0 0</span></span> | <span data-ttu-id="f1d09-121">0</span><span class="sxs-lookup"><span data-stu-id="f1d09-121">0</span></span>
| <span data-ttu-id="f1d09-122">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-122">0 0 1</span></span> |       |       | <span data-ttu-id="f1d09-123">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-123">0 1 0</span></span> | <span data-ttu-id="f1d09-124">2</span><span class="sxs-lookup"><span data-stu-id="f1d09-124">2</span></span>
| <span data-ttu-id="f1d09-125">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-125">0 1 0</span></span> |       |       | <span data-ttu-id="f1d09-126">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-126">0 1 1</span></span> | <span data-ttu-id="f1d09-127">3</span><span class="sxs-lookup"><span data-stu-id="f1d09-127">3</span></span>
| <span data-ttu-id="f1d09-128">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-128">0 1 1</span></span> |       |       | <span data-ttu-id="f1d09-129">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-129">1 0 1</span></span> | <span data-ttu-id="f1d09-130">5</span><span class="sxs-lookup"><span data-stu-id="f1d09-130">5</span></span>
| <span data-ttu-id="f1d09-131">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-131">1 0 0</span></span> |       |       | <span data-ttu-id="f1d09-132">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-132">1 1 1</span></span> | <span data-ttu-id="f1d09-133">7</span><span class="sxs-lookup"><span data-stu-id="f1d09-133">7</span></span>
| <span data-ttu-id="f1d09-134">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-134">1 0 1</span></span> |       |       | <span data-ttu-id="f1d09-135">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-135">0 0 1</span></span> | <span data-ttu-id="f1d09-136">1</span><span class="sxs-lookup"><span data-stu-id="f1d09-136">1</span></span>
| <span data-ttu-id="f1d09-137">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-137">1 1 0</span></span> |       |       | <span data-ttu-id="f1d09-138">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-138">1 0 0</span></span> | <span data-ttu-id="f1d09-139">4</span><span class="sxs-lookup"><span data-stu-id="f1d09-139">4</span></span>
| <span data-ttu-id="f1d09-140">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-140">1 1 1</span></span> |       |       | <span data-ttu-id="f1d09-141">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-141">1 1 0</span></span> | <span data-ttu-id="f1d09-142">6</span><span class="sxs-lookup"><span data-stu-id="f1d09-142">6</span></span>

<span data-ttu-id="f1d09-143">Alle Werte für Indizes ungleich 0 (= Index) werden von A nach B und von D in C kopiert.</span><span class="sxs-lookup"><span data-stu-id="f1d09-143">All values for indices not equal to 0 (= index) are copied from A to B and from D to C.</span></span>

<span data-ttu-id="f1d09-144">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="f1d09-144">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="f1d09-145">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-145">2 1 0</span></span> | <span data-ttu-id="f1d09-146">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-146">2 1 0</span></span> | <span data-ttu-id="f1d09-147">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-147">2 1 0</span></span> | <span data-ttu-id="f1d09-148">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-148">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="f1d09-149">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-149">0 0 0</span></span> | <span data-ttu-id="f1d09-150">0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-150">0 0</span></span>   | <span data-ttu-id="f1d09-151">0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-151">0 0</span></span>   | <span data-ttu-id="f1d09-152">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-152">0 0 0</span></span> |
| <span data-ttu-id="f1d09-153">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-153">0 0 1</span></span> | <span data-ttu-id="f1d09-154">0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-154">0 0</span></span>   | <span data-ttu-id="f1d09-155">0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-155">0 1</span></span>   | <span data-ttu-id="f1d09-156">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-156">0 1 0</span></span> |
| <span data-ttu-id="f1d09-157">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-157">0 1 0</span></span> | <span data-ttu-id="f1d09-158">0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-158">0 1</span></span>   | <span data-ttu-id="f1d09-159">0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-159">0 1</span></span>   | <span data-ttu-id="f1d09-160">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-160">0 1 1</span></span> |
| <span data-ttu-id="f1d09-161">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-161">0 1 1</span></span> | <span data-ttu-id="f1d09-162">0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-162">0 1</span></span>   | <span data-ttu-id="f1d09-163">1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-163">1 0</span></span>   | <span data-ttu-id="f1d09-164">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-164">1 0 1</span></span> |
| <span data-ttu-id="f1d09-165">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-165">1 0 0</span></span> | <span data-ttu-id="f1d09-166">1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-166">1 0</span></span>   | <span data-ttu-id="f1d09-167">1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-167">1 1</span></span>   | <span data-ttu-id="f1d09-168">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-168">1 1 1</span></span> |
| <span data-ttu-id="f1d09-169">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-169">1 0 1</span></span> | <span data-ttu-id="f1d09-170">1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-170">1 0</span></span>   | <span data-ttu-id="f1d09-171">0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-171">0 0</span></span>   | <span data-ttu-id="f1d09-172">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-172">0 0 1</span></span> |
| <span data-ttu-id="f1d09-173">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-173">1 1 0</span></span> | <span data-ttu-id="f1d09-174">1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-174">1 1</span></span>   | <span data-ttu-id="f1d09-175">1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-175">1 0</span></span>   | <span data-ttu-id="f1d09-176">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-176">1 0 0</span></span> |
| <span data-ttu-id="f1d09-177">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-177">1 1 1</span></span> | <span data-ttu-id="f1d09-178">1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-178">1 1</span></span>   | <span data-ttu-id="f1d09-179">1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-179">1 1</span></span>   | <span data-ttu-id="f1d09-180">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-180">1 1 0</span></span> |

<span data-ttu-id="f1d09-181">Im nächsten Schritt wird ein Wert von 0 für das erste Element mit einem leeren Index in der Spalte 0 in Block B eingefügt. Anschließend wird 1 in B eingefügt, wobei das Präfix übereinstimmt (im ersten Fall die andere Zeile mit den Indizes 0 0).</span><span class="sxs-lookup"><span data-stu-id="f1d09-181">Next a 0 is placed for the first element with an empty index at column 0 in block B and then a 1 is placed in B where the prefix matches (in the first case the other row with indices 0 0).</span></span>
<span data-ttu-id="f1d09-182">Anschließend wird ein 1 in der gleichen Zeile in Block c und dann ein 0 für das entsprechende Präfix in Block c hinzugefügt.  Dieser Prozess wird wiederholt, bis alle Indizes in den Blöcken B und C in Spalte 0 platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="f1d09-182">Afterwards, a 1 is added in the same row in block C, and then a 0 for the corresponding prefix in block C.  This process is repeated, until all indices have been placed in column 0 in blocks B and C.</span></span>

<span data-ttu-id="f1d09-183">|   A |   B |   C |   D |</span><span class="sxs-lookup"><span data-stu-id="f1d09-183">|   A   |   B   |   C   |   D   |</span></span>
| <span data-ttu-id="f1d09-184">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-184">2 1 0</span></span> | <span data-ttu-id="f1d09-185">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-185">2 1 0</span></span> | <span data-ttu-id="f1d09-186">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-186">2 1 0</span></span> | <span data-ttu-id="f1d09-187">2 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-187">2 1 0</span></span> |
|-------|-------|-------|-------|
| <span data-ttu-id="f1d09-188">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-188">0 0 0</span></span> | <span data-ttu-id="f1d09-189">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-189">0 0 0</span></span> | <span data-ttu-id="f1d09-190">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-190">0 0 0</span></span> | <span data-ttu-id="f1d09-191">0 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-191">0 0 0</span></span> |
| <span data-ttu-id="f1d09-192">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-192">0 0 1</span></span> | <span data-ttu-id="f1d09-193">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-193">0 0 1</span></span> | <span data-ttu-id="f1d09-194">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-194">0 1 1</span></span> | <span data-ttu-id="f1d09-195">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-195">0 1 0</span></span> |
| <span data-ttu-id="f1d09-196">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-196">0 1 0</span></span> | <span data-ttu-id="f1d09-197">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-197">0 1 0</span></span> | <span data-ttu-id="f1d09-198">0 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-198">0 1 0</span></span> | <span data-ttu-id="f1d09-199">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-199">0 1 1</span></span> |
| <span data-ttu-id="f1d09-200">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-200">0 1 1</span></span> | <span data-ttu-id="f1d09-201">0 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-201">0 1 1</span></span> | <span data-ttu-id="f1d09-202">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-202">1 0 1</span></span> | <span data-ttu-id="f1d09-203">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-203">1 0 1</span></span> |
| <span data-ttu-id="f1d09-204">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-204">1 0 0</span></span> | <span data-ttu-id="f1d09-205">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-205">1 0 0</span></span> | <span data-ttu-id="f1d09-206">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-206">1 1 0</span></span> | <span data-ttu-id="f1d09-207">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-207">1 1 1</span></span> |
| <span data-ttu-id="f1d09-208">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-208">1 0 1</span></span> | <span data-ttu-id="f1d09-209">1 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-209">1 0 1</span></span> | <span data-ttu-id="f1d09-210">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-210">0 0 1</span></span> | <span data-ttu-id="f1d09-211">0 0 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-211">0 0 1</span></span> |
| <span data-ttu-id="f1d09-212">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-212">1 1 0</span></span> | <span data-ttu-id="f1d09-213">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-213">1 1 0</span></span> | <span data-ttu-id="f1d09-214">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-214">1 0 0</span></span> | <span data-ttu-id="f1d09-215">1 0 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-215">1 0 0</span></span> |
| <span data-ttu-id="f1d09-216">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-216">1 1 1</span></span> | <span data-ttu-id="f1d09-217">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-217">1 1 1</span></span> | <span data-ttu-id="f1d09-218">1 1 1</span><span class="sxs-lookup"><span data-stu-id="f1d09-218">1 1 1</span></span> | <span data-ttu-id="f1d09-219">1 1 0</span><span class="sxs-lookup"><span data-stu-id="f1d09-219">1 1 0</span></span> |

<span data-ttu-id="f1d09-220">Wir können drei neue Permutationen aus der Tabelle lesen:</span><span class="sxs-lookup"><span data-stu-id="f1d09-220">We can read three new permutations from the table:</span></span>

- <span data-ttu-id="f1d09-221">$ \ pi_l $ mit Elementen in a, Bilder in B (links)</span><span class="sxs-lookup"><span data-stu-id="f1d09-221">$\pi_l$ with elements in A, images in B (left)</span></span>
- <span data-ttu-id="f1d09-222">$ \ pi_r $ mit Elementen in D, Bilder in C (right)</span><span class="sxs-lookup"><span data-stu-id="f1d09-222">$\pi_r$ with elements in D, images in C (right)</span></span>
- <span data-ttu-id="f1d09-223">$ \pi ' $ with Elements in B, Bilder in C (Rest)</span><span class="sxs-lookup"><span data-stu-id="f1d09-223">$\pi'$  with elements in B, images in C (remainder)</span></span>

<span data-ttu-id="f1d09-224">Beachten Sie, dass die Bitwerte in $ \ pi_l $ und $ \ pi_r $ für die Indizes 1 und 2 nicht geändert werden, und die Bitwerte für in $ \ pi_ ' $ für Index 0 nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f1d09-224">Note that by design bit values do not change in $\pi_l$ and $\pi_r$ for indices 1 and 2, and bit values do not change for in $\pi_'$ for index 0.</span></span>  <span data-ttu-id="f1d09-225">Beachten Sie außerdem, dass $ \ pi_l $ und $ \ pi_r $ selbst inversen müssen.</span><span class="sxs-lookup"><span data-stu-id="f1d09-225">Also note that $\pi_l$ and $\pi_r$ must be self-inverse.</span></span>

<span data-ttu-id="f1d09-226">Die abgeleiteten und zurückgegebenen Permutationen lauten: Left = [0, 1, 2, 3, 4, 5, 6, 7] right = [0, 1, 3, 2, 4, 5, 7, 6] Restwert = [0, 3, 2, 5, 6, 1, 4, 7]</span><span class="sxs-lookup"><span data-stu-id="f1d09-226">The derived and returned permutations are: left      = [0, 1, 2, 3, 4, 5, 6, 7] right     = [0, 1, 3, 2, 4, 5, 7, 6] remainder = [0, 3, 2, 5, 6, 1, 4, 7]</span></span>