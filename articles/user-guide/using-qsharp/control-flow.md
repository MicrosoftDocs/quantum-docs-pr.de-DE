---
title: Ablauf Steuerung in Q#
description: Schleifen, Bedingungen usw.
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
no-loc:
- Q#
- $$v
ms.openlocfilehash: 547c57cab67443e8b487bf817eb79fc922b43cdc
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833522"
---
# <a name="control-flow-in-no-locq"></a><span data-ttu-id="16bd9-103">Ablauf Steuerung in Q#</span><span class="sxs-lookup"><span data-stu-id="16bd9-103">Control flow in Q#</span></span>

<span data-ttu-id="16bd9-104">Innerhalb eines Vorgangs oder einer Funktion wird jede Anweisung in der richtigen Reihenfolge ausgeführt, ähnlich wie andere gängige imperative klassische Sprachen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-104">Within an operation or function, each statement runs in order, similar to other common imperative classical languages.</span></span>
<span data-ttu-id="16bd9-105">Allerdings können Sie die Ablauf Steuerung auf drei verschiedene Arten ändern:</span><span class="sxs-lookup"><span data-stu-id="16bd9-105">However, you can modify the flow of control in three distinct ways:</span></span>

* <span data-ttu-id="16bd9-106">`if` Äußerungen</span><span class="sxs-lookup"><span data-stu-id="16bd9-106">`if` statements</span></span>
* <span data-ttu-id="16bd9-107">`for` Loops</span><span class="sxs-lookup"><span data-stu-id="16bd9-107">`for` loops</span></span>
* <span data-ttu-id="16bd9-108">`repeat-until-success` Loops</span><span class="sxs-lookup"><span data-stu-id="16bd9-108">`repeat-until-success` loops</span></span>
* <span data-ttu-id="16bd9-109">Konjugationen ( `apply-within` Anweisungen)</span><span class="sxs-lookup"><span data-stu-id="16bd9-109">conjugations (`apply-within` statements)</span></span>

<span data-ttu-id="16bd9-110">Die `if` `for` Ablaufsteuerungskonstrukte und sind für die meisten klassischen Programmiersprachen vertraut.</span><span class="sxs-lookup"><span data-stu-id="16bd9-110">The `if` and `for` control flow constructs proceed in a familiar sense to most classical programming languages.</span></span> <span data-ttu-id="16bd9-111">[`Repeat-until-success`](#repeat-until-success-loop) Schleifen und [Konjugationen](#conjugations) werden weiter unten in diesem Artikel erläutert.</span><span class="sxs-lookup"><span data-stu-id="16bd9-111">[`Repeat-until-success`](#repeat-until-success-loop) loops and [conjugations](#conjugations) are discussed later in this article.</span></span>

<span data-ttu-id="16bd9-112">Wichtig ist, `for` dass Schleifen und `if` Anweisungen in Vorgängen verwendet werden können, für die [Spezialisierungs](xref:microsoft.quantum.guide.operationsfunctions) Vorgänge automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="16bd9-112">Importantly, `for` loops and `if` statements can be used in operations for which [specializations](xref:microsoft.quantum.guide.operationsfunctions) are auto-generated.</span></span> <span data-ttu-id="16bd9-113">In diesem Szenario kehrt das Adjoint einer `for` Schleife die Richtung um und übernimmt das Adjoint der einzelnen Iterationen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-113">In that scenario, the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="16bd9-114">Diese Aktion folgt dem Prinzip "Schuh-und-SOCKS": Wenn Sie das Einfügen von SOCKS und den Schuhen rückgängig machen möchten, müssen Sie die einfügende Schuhe rückgängig machen und dann auf die SOCKS setzen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-114">This action follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span> 

## <a name="if-else-if-else"></a><span data-ttu-id="16bd9-115">If, else-if, Else</span><span class="sxs-lookup"><span data-stu-id="16bd9-115">If, Else-if, Else</span></span>

<span data-ttu-id="16bd9-116">Die- `if` Anweisung unterstützt die bedingte Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="16bd9-116">The `if` statement supports conditional processing.</span></span>
<span data-ttu-id="16bd9-117">Er besteht aus dem Schlüsselwort `if` , einem booleschen Ausdruck in Klammern und einem Anweisungsblock (der _Then_ -Block).</span><span class="sxs-lookup"><span data-stu-id="16bd9-117">It consists of the keyword `if`, a Boolean expression in parentheses, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="16bd9-118">Optional kann eine beliebige Anzahl von else-if-Klauseln befolgt werden, von denen jeder aus dem Schlüsselwort `elif` , einem booleschen Ausdruck in Klammern und einem Anweisungsblock (der _else-if-_ Block) besteht.</span><span class="sxs-lookup"><span data-stu-id="16bd9-118">Optionally, any number of else-if clauses can follow, each of which consists of the keyword `elif`, a Boolean expression in parentheses, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="16bd9-119">Schließlich kann die Anweisung optional mit einer Else-Klausel abgeschlossen werden, die aus dem Schlüsselwort `else` gefolgt von einem anderen Anweisungsblock (dem _else_ -Block) besteht.</span><span class="sxs-lookup"><span data-stu-id="16bd9-119">Finally, the statement can optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="16bd9-120">Die `if` Bedingung wird ausgewertet, und wenn der Wert *true*ist, wird der *Then* -Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-120">The `if` condition is evaluated, and if it is *true*, the *then* block is run.</span></span>
<span data-ttu-id="16bd9-121">Wenn die Bedingung *false*ist, wird die erste else-if-Bedingung ausgewertet. Wenn dies zutrifft, wird der *else-if-* Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-121">If the condition is *false*, then the first else-if condition is evaluated; if that is true, then the *else-if* block is run.</span></span>
<span data-ttu-id="16bd9-122">Andernfalls wertet der zweite Else-If-Block aus, und dann der dritte, usw., bis entweder eine-Klausel mit einer true-Bedingung gefunden wird oder keine else-if-Klauseln mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="16bd9-122">Otherwise, the second else-if block evaluates, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="16bd9-123">Wenn die ursprüngliche *if* -Bedingung und alle else-if-Klauseln als *false*ausgewertet werden, wird der *else* -Block ausgeführt, falls angegeben.</span><span class="sxs-lookup"><span data-stu-id="16bd9-123">If the original *if* condition and all the else-if clauses evaluate to *false*, the *else* block is run, if provided.</span></span>

<span data-ttu-id="16bd9-124">Beachten Sie, dass der ausgeführte Block in seinem eigenen Bereich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16bd9-124">Note that whichever block runs, it runs within its own scope.</span></span>
<span data-ttu-id="16bd9-125">Bindungen, die innerhalb eines- `if` ,-oder-Blocks erstellt werden, `elif` `else` sind nach Beendigung des-Blocks nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="16bd9-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after the block ends.</span></span>

<span data-ttu-id="16bd9-126">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="16bd9-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="16bd9-127">oder</span><span class="sxs-lookup"><span data-stu-id="16bd9-127">or</span></span>
```qsharp
if (i == 1) {
    X(target);
    let n = 1;
} elif (i == 2) {
    Y(target);
    let m = n + 1; // would cause an error, because n is no longer bound
} else {
    Z(target);
}
```

## <a name="for-loop"></a><span data-ttu-id="16bd9-128">for-Schleifen</span><span class="sxs-lookup"><span data-stu-id="16bd9-128">For loop</span></span>

<span data-ttu-id="16bd9-129">Die- `for` Anweisung unterstützt Iterationen über einen ganzzahligen Bereich oder ein Array.</span><span class="sxs-lookup"><span data-stu-id="16bd9-129">The `for` statement supports iteration over an integer range or an array.</span></span>
<span data-ttu-id="16bd9-130">Die-Anweisung besteht aus dem `for` -Schlüsselwort, gefolgt von einem Symbol-oder Symbol-Tupel, dem-Schlüsselwort `in` und einem Ausdruck vom Typ `Range` oder Array, alle in Klammern und einem Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="16bd9-130">The statement consists of the keyword `for`, followed by a symbol or symbol tuple, the keyword `in`, and an expression of type `Range` or array, all in parentheses, and a statement block.</span></span>

<span data-ttu-id="16bd9-131">Der Anweisungsblock (der Hauptteil der Schleife) wird wiederholt ausgeführt, wobei das definierte Symbol (die Schleifenvariable) an jeden Wert im Bereich oder Array gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="16bd9-131">The statement block (the body of the loop) runs repeatedly, with the defined symbol (the loop variable) bound to each value in the range or array.</span></span>
<span data-ttu-id="16bd9-132">Beachten Sie Folgendes: Wenn der Bereichs Ausdruck einen leeren Bereich oder ein leeres Array ergibt, wird der Text überhaupt nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-132">Note that if the range expression evaluates to an empty range or array, the body does not run at all.</span></span>
<span data-ttu-id="16bd9-133">Der Ausdruck wird vor der Eingabe der Schleife vollständig ausgewertet und ändert sich nicht, während die Schleife ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16bd9-133">The expression is fully evaluated before entering the loop, and does not change while the loop is running.</span></span>

<span data-ttu-id="16bd9-134">Die Schleifenvariable wird an jedem Eingang an den Schleifen Text gebunden, und die Bindung am Ende des Texts wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="16bd9-134">The loop variable is bound at each entrance to the loop body, and is unbound at the end of the body.</span></span>
<span data-ttu-id="16bd9-135">Die Schleifenvariable wird nicht gebunden, nachdem die for-Schleife abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="16bd9-135">The loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="16bd9-136">Die Bindung der Schleifen Variablen ist unveränderlich und folgt denselben Regeln wie andere Variablen Bindungen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-136">The binding of the loop variable is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="16bd9-137">In diesen Beispielen `qubits` ist ein Register von Qubits (d. h. vom Typ `Qubit[]` ).</span><span class="sxs-lookup"><span data-stu-id="16bd9-137">In these examples, `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

```qsharp
// ...
for (qubit in qubits) {  // iterate over each qubit value in the array qubits
    H(qubit);
}
// 'qubit' is no longer bound

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {  // iterates over the integers in the Range 0 .. (Length(qubits) - 1)
    set results w/= index <- (index, M(qubits[index])); // measure each qubit, updates the tuple value in the results array that at index 
}

mutable accumulated = 0;
for ((index, measured) in results) { // iterates over the tuple values in results
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="16bd9-138">Beachten Sie, dass wir am Ende den binären Operator "arithmetischer Shift-Left" () verwendet haben `<<<` .</span><span class="sxs-lookup"><span data-stu-id="16bd9-138">Note that at the end, we utilized the arithmetic-shift-left binary operator, `<<<`.</span></span> <span data-ttu-id="16bd9-139">Weitere Informationen finden Sie unter [numerische Ausdrücke](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span><span class="sxs-lookup"><span data-stu-id="16bd9-139">For more information, see [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions).</span></span>

## <a name="repeat-until-success-loop"></a><span data-ttu-id="16bd9-140">Repeat-Until-Success-Schleife</span><span class="sxs-lookup"><span data-stu-id="16bd9-140">Repeat-until-success loop</span></span>

<span data-ttu-id="16bd9-141">Die Q# Sprache ermöglicht eine klassische Ablauf Steuerung, die von den Ergebnissen der Messung von Qubits abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="16bd9-141">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="16bd9-142">Diese Funktion ermöglicht es wiederum, leistungsstarke probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="16bd9-142">This capability, in turn, enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="16bd9-143">Beispiele hierfür sind die RUS *-Muster (Repeat-Until-Success* ) in Q# .</span><span class="sxs-lookup"><span data-stu-id="16bd9-143">Examples of this are the *repeat-until-success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="16bd9-144">Diese RUS-Muster sind probabilistische Programme, die zu den *erwarteten* niedrigen Kosten in Bezug auf elementare Gates gehören. die anfallenden Kosten hängen von der tatsächlichen Durchführung und der Überführung der zahlreichen möglichen Verzweigungen ab.</span><span class="sxs-lookup"><span data-stu-id="16bd9-144">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates; the incurred cost depends on the actual run and the interleaving of the multiple possible branchings.</span></span>

<span data-ttu-id="16bd9-145">Zum Vereinfachen von Wiederholungs-bis-Erfolg-Mustern (RUS) Q# unterstützt die-Konstrukte.</span><span class="sxs-lookup"><span data-stu-id="16bd9-145">To facilitate repeat-until-success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="16bd9-146">dabei `expression` ist ein beliebiger gültiger Ausdruck, der zu einem Wert vom Typ ausgewertet wird `Bool` .</span><span class="sxs-lookup"><span data-stu-id="16bd9-146">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="16bd9-147">Der Schleifen Text wird ausgeführt, und anschließend wird die Bedingung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="16bd9-147">The loop body runs, and then the condition is evaluated.</span></span>
<span data-ttu-id="16bd9-148">Wenn die Bedingung true ist, wird die-Anweisung abgeschlossen. Andernfalls wird der Fixup ausgeführt, und die Anweisung wird erneut ausgeführt, beginnend mit dem Schleifen Text.</span><span class="sxs-lookup"><span data-stu-id="16bd9-148">If the condition is true, then the statement is completed; otherwise, the fixup runs, and the statement runs again, starting with the loop body.</span></span>

<span data-ttu-id="16bd9-149">Alle drei Teile einer RUS-Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich *für jede Wiederholung*behandelt, sodass im Text gebundene Symbole sowohl im Test als auch im Fixup verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="16bd9-149">All three portions of an RUS loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in both the test and the fixup.</span></span>
<span data-ttu-id="16bd9-150">Wenn Sie die Ausführung des Fixup abschließen, wird der Gültigkeitsbereich für die-Anweisung beendet, sodass im Text-oder Fixup-Bereich vorgenommene Symbol Bindungen in nachfolgenden Wiederholungen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="16bd9-150">However, completing the run of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="16bd9-151">Außerdem ist die- `fixup` Anweisung häufig hilfreich, aber nicht immer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="16bd9-151">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="16bd9-152">In Fällen, in denen er nicht benötigt wird, wird das Konstrukt</span><span class="sxs-lookup"><span data-stu-id="16bd9-152">In cases that it is not needed, the construct</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression);
```

<span data-ttu-id="16bd9-153">ist auch ein gültiges RUS-Muster.</span><span class="sxs-lookup"><span data-stu-id="16bd9-153">is also a valid RUS pattern.</span></span>

<span data-ttu-id="16bd9-154">Weitere Beispiele und Details finden Sie in diesem Artikel unter [Wiederholungs-bis-Erfolg-Beispiele](#repeat-until-success-examples) .</span><span class="sxs-lookup"><span data-stu-id="16bd9-154">For more examples and details, see [Repeat-until-success examples](#repeat-until-success-examples) in this article.</span></span>

> [!TIP]   
> <span data-ttu-id="16bd9-155">Vermeiden Sie die Verwendung von Wiederholungs-bis-Erfolg-Schleifen innerhalb von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-155">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="16bd9-156">Verwenden Sie *while* -Schleifen, um die entsprechende Funktionalität in Funktionen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-156">Use *while* loops to provide the corresponding functionality inside functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="16bd9-157">while-Schleifen</span><span class="sxs-lookup"><span data-stu-id="16bd9-157">While loop</span></span>

<span data-ttu-id="16bd9-158">Wiederholungs-bis-Erfolg-Muster verfügen über eine sehr Quantum-spezifische-Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="16bd9-158">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="16bd9-159">Sie werden häufig in bestimmten Klassen von Quantum-Algorithmen verwendet. Dies ist also das dedizierte Sprachkonstrukt in Q# .</span><span class="sxs-lookup"><span data-stu-id="16bd9-159">They are widely used in particular classes of quantum algorithms - hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="16bd9-160">Schleifen, die basierend auf einer Bedingung unterbrechen und deren Testlauf Länge daher zur Kompilierzeit nicht bekannt ist, werden mit bestimmter Sorgfalt in einer Quantum-Laufzeit behandelt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-160">However, loops that break based on a condition and whose run length is thus unknown at compile-time, are handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="16bd9-161">Die Verwendung innerhalb von Funktionen ist jedoch nicht problematisch, da diese Schleifen nur Code enthalten, der auf herkömmlicher (nicht Quantum-) Hardware ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16bd9-161">However, their use within functions is unproblematic since these loops only contain code that runs on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="16bd9-162">Q#Daher unterstützt die Verwendung von while-Schleifen nur innerhalb von Functions.</span><span class="sxs-lookup"><span data-stu-id="16bd9-162">Q#, therefore, supports to use of while loops within functions only.</span></span>
<span data-ttu-id="16bd9-163">Eine- `while` Anweisung besteht aus dem Schlüsselwort `while` , einem booleschen Ausdruck in Klammern und einem Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="16bd9-163">A `while` statement consists of the keyword `while`, a Boolean expression in parentheses, and a statement block.</span></span>
<span data-ttu-id="16bd9-164">Der Anweisungsblock (der Text der Schleife) wird ausgeführt, solange die Bedingung als ausgewertet wird `true` .</span><span class="sxs-lookup"><span data-stu-id="16bd9-164">The statement block (the body of the loop) runs as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

## <a name="conjugations"></a><span data-ttu-id="16bd9-165">Konjugationen</span><span class="sxs-lookup"><span data-stu-id="16bd9-165">Conjugations</span></span>

<span data-ttu-id="16bd9-166">Im Gegensatz zu klassischen Bits ist das Freigeben von Quantum-Speicher etwas komplizierter, da das Blind Zurücksetzen von Qubits unerwünschte Auswirkungen auf die verbleibende Berechnung haben kann, wenn die Qubits noch entkoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="16bd9-166">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="16bd9-167">Diese Auswirkungen können vermieden werden, indem Berechnungen vor der Freigabe des Arbeitsspeichers ordnungsgemäß durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="16bd9-167">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="16bd9-168">Ein gängiges Muster in Quantum Computing ist daher Folgendes:</span><span class="sxs-lookup"><span data-stu-id="16bd9-168">A common pattern in quantum computing is hence the following:</span></span> 

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    outerOperation(target);
    innerOperation(target);
    Adjoint outerOperation(target);
}
```

<span data-ttu-id="16bd9-169">Q# unterstützt eine Konjugations Anweisung, die die vorherige Transformation implementiert.</span><span class="sxs-lookup"><span data-stu-id="16bd9-169">Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="16bd9-170">Mit dieser Anweisung kann der Vorgang `ApplyWith` folgendermaßen implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="16bd9-170">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

```qsharp
operation ApplyWith<'T>(
    outerOperation : ('T => Unit is Adj), 
    innerOperation : ('T => Unit), 
    target : 'T) 
: Unit {

    within{ 
        outerOperation(target);
    }
    apply {
        innerOperation(target);
    }
}
```
<span data-ttu-id="16bd9-171">Eine solche Konjugations Anweisung erweist sich als nützlich, wenn die äußeren und inneren Transformationen nicht als Vorgänge verfügbar sind, sondern eher durch einen Block, der aus mehreren Anweisungen besteht, beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="16bd9-171">Such a conjugation statement becomes useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="16bd9-172">Die umgekehrte Transformation für die-Anweisungen, die im-Block innerhalb von definiert sind, wird automatisch vom Compiler generiert und nach Abschluss von Apply-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-172">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="16bd9-173">Da alle änderbaren Variablen, die als Teil des Blocks innerhalb von verwendet werden, im Apply-Block nicht wieder hergestellt werden können, ist die generierte Transformation garantiert das Adjoint der Berechnung im within-Block.</span><span class="sxs-lookup"><span data-stu-id="16bd9-173">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="return-statement"></a><span data-ttu-id="16bd9-174">Return-Anweisung</span><span class="sxs-lookup"><span data-stu-id="16bd9-174">Return Statement</span></span>

<span data-ttu-id="16bd9-175">Die Return-Anweisung beendet die Ausführung eines Vorgangs oder einer Funktion und gibt einen Wert an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="16bd9-175">The return statement ends the run of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="16bd9-176">Er besteht aus dem Schlüsselwort `return` , gefolgt von einem Ausdruck des entsprechenden Typs und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="16bd9-176">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="16bd9-177">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="16bd9-177">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="16bd9-178">oder</span><span class="sxs-lookup"><span data-stu-id="16bd9-178">or</span></span>
```qsharp
return (results, qubits);
```

* <span data-ttu-id="16bd9-179">Ein Aufruf bares Element, das ein leeres Tupel zurückgibt, `()` erfordert keine Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="16bd9-179">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
* <span data-ttu-id="16bd9-180">Verwenden Sie, um eine frühe Beendigung des Vorgangs oder der Funktion anzugeben `return ();` .</span><span class="sxs-lookup"><span data-stu-id="16bd9-180">To specify an early exit from the operation or function, use `return ();`.</span></span>
<span data-ttu-id="16bd9-181">Aufruf Bare Elemente, die einen beliebigen anderen Typ zurückgeben, erfordern eine abschließende Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="16bd9-181">Callables that return any other type require a final return statement.</span></span>
* <span data-ttu-id="16bd9-182">Es gibt keine maximale Anzahl von Return-Anweisungen innerhalb eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="16bd9-182">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="16bd9-183">Der Compiler gibt möglicherweise eine Warnung aus, wenn Anweisungen einer Return-Anweisung in einem-Block folgen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-183">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

   
## <a name="fail-statement"></a><span data-ttu-id="16bd9-184">Fail-Anweisung</span><span class="sxs-lookup"><span data-stu-id="16bd9-184">Fail statement</span></span>

<span data-ttu-id="16bd9-185">Die Fail-Anweisung beendet die Ausführung eines Vorgangs und gibt einen Fehlerwert an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="16bd9-185">The fail statement ends the run of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="16bd9-186">Er besteht aus dem Schlüsselwort `fail` , gefolgt von einer Zeichenfolge und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="16bd9-186">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="16bd9-187">Die-Anweisung gibt die Zeichenfolge an den klassischen Treiber als Fehlermeldung zurück.</span><span class="sxs-lookup"><span data-stu-id="16bd9-187">The statement returns the string to the classical driver as the error message.</span></span>

<span data-ttu-id="16bd9-188">Es gibt keine Einschränkung für die Anzahl der Fail-Anweisungen innerhalb eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="16bd9-188">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="16bd9-189">Der Compiler gibt möglicherweise eine Warnung aus, wenn-Anweisungen einer Fail-Anweisung innerhalb eines-Blocks folgen.</span><span class="sxs-lookup"><span data-stu-id="16bd9-189">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="16bd9-190">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="16bd9-190">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="16bd9-191">oder mithilfe von [interpoliert](xref:microsoft.quantum.guide.expressions#interpolated-strings)Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="16bd9-191">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="16bd9-192">Beispiele für Wiederholung bis zum Erfolg</span><span class="sxs-lookup"><span data-stu-id="16bd9-192">Repeat-until-success examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="16bd9-193">RUS-Muster für Single-Qubit-Drehung über eine irrationale Achse</span><span class="sxs-lookup"><span data-stu-id="16bd9-193">RUS pattern for single-qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="16bd9-194">In einem typischen Anwendungsfall implementiert der folgende Q# Vorgang eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt {5} $ in der Bloch-Kugel.</span><span class="sxs-lookup"><span data-stu-id="16bd9-194">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="16bd9-195">Die Implementierung verwendet ein bekanntes RUS-Muster:</span><span class="sxs-lookup"><span data-stu-id="16bd9-195">The implementation uses a known RUS pattern:</span></span>

```qsharp
operation ApplyVRotationUsingRUS(qubit : Qubit) : Unit {
    using (controls = Qubit[2]) {
        ApplyToEachA(H, controls);
        mutable finished = false;
        repeat {
            Controlled X(controls, qubit);
            S(qubit);
            Controlled X(controls, qubit);
            Z(qubit);
        }
        until (finished)
        fixup {
            if (MeasureIfAllQubitsAreZero(controls, PauliX)) {
                set finished = true;
            }
        }
    }
}
```

### <a name="rus-loop-with-a-mutable-variable-in-scope"></a><span data-ttu-id="16bd9-196">RUS-Schleife mit einer änderbaren Variablen im Gültigkeitsbereich</span><span class="sxs-lookup"><span data-stu-id="16bd9-196">RUS loop with a mutable variable in scope</span></span>

<span data-ttu-id="16bd9-197">Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen, `finished` die innerhalb des Gültigkeits Bereichs der gesamten Repeat-Until-Fixup-Schleife liegt und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="16bd9-197">This example shows the use of a mutable variable, `finished`, which is within the scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

```qsharp
mutable iter = 1;
repeat {
    ProbabilisticCircuit(qubits);
    let success = ComputeSuccessIndicator(qubits);
}
until (success || iter > maxIter)
fixup {
    iter += 1;
    ComputeCorrection(qubits);
}
```

### <a name="rus-without-fixup"></a><span data-ttu-id="16bd9-198">RUS ohne `fixup`</span><span class="sxs-lookup"><span data-stu-id="16bd9-198">RUS without `fixup`</span></span>

<span data-ttu-id="16bd9-199">Dieses Beispiel zeigt eine RUS-Schleife ohne den fixupschritt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-199">This example shows an RUS loop without the fixup step.</span></span> <span data-ttu-id="16bd9-200">Der Code ist eine probabilistische Verbindung, die ein wichtiges Drehungs Gate implementiert $V _3 = (\boldone + 2 i)/\sqrt {5} $ mithilfe von `H` und `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="16bd9-200">The code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="16bd9-201">Die Schleife wird im Durchschnitt in $ \frac {8} {5} $ Wiederholungen beendet.</span><span class="sxs-lookup"><span data-stu-id="16bd9-201">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="16bd9-202">Weitere Informationen finden Sie [*unter Repeat-Until-Success: nicht deterministische Zerlegung von Single-Qubit-uniflüssen*](https://arxiv.org/abs/1311.1074) ("Petznick" und "svore", 2014).</span><span class="sxs-lookup"><span data-stu-id="16bd9-202">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

```qsharp
using (qubit = Qubit()) {
    repeat {
        H(qubit);
        T(qubit);
        CNOT(target, qubit);
        H(qubit);
        Adjoint T(qubit);
        H(qubit);
        T(qubit);
        H(qubit);
        CNOT(target, qubit);
        T(qubit);
        Z(target);
        H(qubit);
        let result = M(qubit);
    } until (result == Zero);
}
```

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="16bd9-203">RUS zum Vorbereiten eines Quantum-Zustands</span><span class="sxs-lookup"><span data-stu-id="16bd9-203">RUS to prepare a quantum state</span></span>

<span data-ttu-id="16bd9-204">Im folgenden finden Sie ein Beispiel für ein RUS-Muster zum Vorbereiten des Quantums $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, beginnend mit dem Status $ \ket{+} $.</span><span class="sxs-lookup"><span data-stu-id="16bd9-204">Finally, here is an example of an RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>

<span data-ttu-id="16bd9-205">Wichtige programmgesteuerte Features, die in diesem Vorgang angezeigt werden, sind:</span><span class="sxs-lookup"><span data-stu-id="16bd9-205">Notable programmatic features shown in this operation are:</span></span>

* <span data-ttu-id="16bd9-206">Ein komplexerer `fixup` Teil der Schleife, der Quantum-Vorgänge einschließt.</span><span class="sxs-lookup"><span data-stu-id="16bd9-206">A more complex `fixup` part of the loop, which involves quantum operations.</span></span> 
* <span data-ttu-id="16bd9-207">Die Verwendung von- `AssertMeasurementProbability` Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantenzustand an bestimmten angegebenen Punkten im Programm gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="16bd9-207">The use of `AssertMeasurementProbability` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>

<span data-ttu-id="16bd9-208">Weitere Informationen zu den [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) -und- [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) Vorgängen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging).</span><span class="sxs-lookup"><span data-stu-id="16bd9-208">For more information about the [`AssertMeasurement`](xref:microsoft.quantum.diagnostics.assertmeasurement) and [`AssertMeasurementProbability`](xref:microsoft.quantum.diagnostics.assertmeasurementprobability) operations, see [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging).</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertMeasurementProbability(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertMeasurementProbability(
                [PauliX], [auxiliary], Zero, 3. / 4.,
                "Error: the probability to measure |+> in the first
                auxiliary must be 3/4",
                1e-10);

            // If we get the measurement outcome Zero, we prepare the
            // required state.
            let outcome = Measure([PauliX], [auxiliary]);
        }
        until (outcome == Zero)
        fixup {
            // Bring the auxiliary and target qubits back to |+> state.
            if (outcome == One) {
                Z(auxiliary);
                X(target);
                H(target);
            }
        }
        // Return the auxiliary qubit back to the Zero state.
        H(auxiliary);
    }
}
```

<span data-ttu-id="16bd9-209">Weitere Informationen finden Sie unter [Beispiel für Komponententests mit der Standardbibliothek](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span><span class="sxs-lookup"><span data-stu-id="16bd9-209">For more information, see [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/main/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

## <a name="next-steps"></a><span data-ttu-id="16bd9-210">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="16bd9-210">Next steps</span></span>

<span data-ttu-id="16bd9-211">Erfahren Sie mehr über das [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging) in Q# .</span><span class="sxs-lookup"><span data-stu-id="16bd9-211">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>
