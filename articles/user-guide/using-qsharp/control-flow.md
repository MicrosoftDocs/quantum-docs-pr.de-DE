---
title: 'Ablauf Steuerung in Q #'
description: Schleifen, Bedingungen usw.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.controlflow
ms.openlocfilehash: c534e016fcb8b50e66c11ca29c253ba0512acc6e
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430950"
---
# <a name="control-flow-in-q"></a><span data-ttu-id="efe37-103">Ablauf Steuerung in Q #</span><span class="sxs-lookup"><span data-stu-id="efe37-103">Control Flow in Q#</span></span>

<span data-ttu-id="efe37-104">Innerhalb einer Operation oder Funktion wird jede Anweisung in der richtigen Reihenfolge ausgeführt, ähnlich wie bei den gängigsten, imperativen, klassischen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="efe37-104">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="efe37-105">Diese Ablauf Steuerung kann jedoch auf drei verschiedene Arten geändert werden:</span><span class="sxs-lookup"><span data-stu-id="efe37-105">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="efe37-106">`if`Äußerungen</span><span class="sxs-lookup"><span data-stu-id="efe37-106">`if` statements</span></span>
- <span data-ttu-id="efe37-107">`for`Loops</span><span class="sxs-lookup"><span data-stu-id="efe37-107">`for` loops</span></span>
- <span data-ttu-id="efe37-108">`repeat`-`until`Loops</span><span class="sxs-lookup"><span data-stu-id="efe37-108">`repeat`-`until` loops</span></span>

<span data-ttu-id="efe37-109">Wir verzögern die Erörterung der letzteren weiter [unten](#repeat-until-success-loop).</span><span class="sxs-lookup"><span data-stu-id="efe37-109">We defer discussion of the latter to further [below](#repeat-until-success-loop).</span></span>
<span data-ttu-id="efe37-110">Die `if` `for` Ablaufsteuerungs-Konstrukte und sind jedoch für die meisten klassischen Programmiersprachen in einem vertrauten Sinn.</span><span class="sxs-lookup"><span data-stu-id="efe37-110">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>

<span data-ttu-id="efe37-111">Wichtig ist, `for` dass Schleifen und `if` Anweisungen sogar in Vorgängen verwendet werden können, für die Spezialisierungs Vorgänge automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="efe37-111">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="efe37-112">In diesem Fall kehrt das Adjoint einer `for` Schleife die Richtung um und übernimmt das Adjoint der einzelnen Iterationen.</span><span class="sxs-lookup"><span data-stu-id="efe37-112">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="efe37-113">Dies folgt dem Prinzip "Schuh-und-SOCKS": Wenn Sie das Einfügen von SOCKS und dann auf Schuhe rückgängig machen möchten, müssen Sie die einfügende Schuhe rückgängig machen und dann auf SOCKS setzen.</span><span class="sxs-lookup"><span data-stu-id="efe37-113">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="efe37-114">Es funktioniert ausgesprochen weniger gut, wenn Sie versuchen, die SOCKS zu wiederholen, während Sie Ihre Schuhe noch nicht nutzen!</span><span class="sxs-lookup"><span data-stu-id="efe37-114">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="if-else-if-else"></a><span data-ttu-id="efe37-115">If, else-if, Else</span><span class="sxs-lookup"><span data-stu-id="efe37-115">If, Else-if, Else</span></span>

<span data-ttu-id="efe37-116">Die- `if` Anweisung unterstützt die bedingte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="efe37-116">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="efe37-117">Sie besteht aus dem Schlüsselwort `if` , einer offenen Klammer `(` , einem booleschen Ausdruck, einer schließenden Klammer `)` und einem Anweisungsblock (der _Then_ -Block).</span><span class="sxs-lookup"><span data-stu-id="efe37-117">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="efe37-118">Auf diese kann eine beliebige Anzahl von else-if-Klauseln folgen, von denen jede aus dem Schlüsselwort `elif` , einer offenen Klammer `(` , einem booleschen Ausdruck, einer schließenden Klammer `)` und einem Anweisungsblock besteht (der _else-if-_ Block).</span><span class="sxs-lookup"><span data-stu-id="efe37-118">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="efe37-119">Schließlich kann die Anweisung optional mit einer Else-Klausel abgeschlossen werden, die aus dem Schlüsselwort `else` gefolgt von einem anderen Anweisungsblock (dem _else_ -Block) besteht.</span><span class="sxs-lookup"><span data-stu-id="efe37-119">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>

<span data-ttu-id="efe37-120">Die `if` Bedingung wird ausgewertet, und wenn der Wert true ist, wird der then-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efe37-120">The `if` condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="efe37-121">Wenn die Bedingung false ist, wird die erste else-if-Bedingung ausgewertet. Wenn der Wert true ist, wird der Else-If-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="efe37-121">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="efe37-122">Andernfalls wird der zweite Else-If-Block getestet, dann der dritte, usw., bis entweder eine-Klausel mit einer true-Bedingung gefunden wird oder keine else-if-Klauseln mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="efe37-122">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="efe37-123">Wenn die ursprüngliche if-Bedingung und alle else-if-Klauseln als false ausgewertet werden, wird der Else-Block ausgeführt, wenn ein solcher angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="efe37-123">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="efe37-124">Beachten Sie, dass der ausgeführte Block in seinem eigenen Bereich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efe37-124">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="efe37-125">Bindungen, die innerhalb eines- `if` ,-oder-Blocks erstellt werden, `elif` `else` sind nach dem Ende nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="efe37-125">Bindings made inside of an `if`, `elif`, or `else` block are not visible after its end.</span></span>

<span data-ttu-id="efe37-126">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="efe37-126">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
    let n = 1;
    // n is bound
} 
// n is not bound
```
<span data-ttu-id="efe37-127">oder</span><span class="sxs-lookup"><span data-stu-id="efe37-127">or</span></span>
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

## <a name="for-loop"></a><span data-ttu-id="efe37-128">For-Schleife</span><span class="sxs-lookup"><span data-stu-id="efe37-128">For Loop</span></span>

<span data-ttu-id="efe37-129">Die- `for` Anweisung unterstützt Iterationen über einen ganzzahligen Bereich oder über ein Array.</span><span class="sxs-lookup"><span data-stu-id="efe37-129">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="efe37-130">Die-Anweisung besteht aus dem Schlüsselwort `for` , einer offenen Klammer `(` , gefolgt von einem Symbol oder einem Symbol Tupel, dem Schlüsselwort `in` , einem Ausdruck vom Typ `Range` oder Array, einer schließenden Klammer `)` und einem Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="efe37-130">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="efe37-131">Der Anweisungsblock (der Hauptteil der Schleife) wird wiederholt ausgeführt, wobei die definierten Symbole (die Schleifen Variablen) an jeden Wert im Bereich oder Array gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="efe37-131">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="efe37-132">Beachten Sie, dass der Text nicht ausgeführt wird, wenn der Bereichs Ausdruck zu einem leeren Bereich oder Array ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="efe37-132">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="efe37-133">Der Ausdruck wird vor der Eingabe der Schleife vollständig ausgewertet und ändert sich nicht, während die Schleife ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efe37-133">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="efe37-134">Die Schleifenvariable wird an jedem Eingang an den Schleifen Text gebunden, und die Bindung am Ende des Texts wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="efe37-134">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="efe37-135">Insbesondere wird die Schleifenvariable nicht gebunden, nachdem die for-Schleife abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="efe37-135">In particular, the loop variable is not bound after the for loop is completed.</span></span>
<span data-ttu-id="efe37-136">Die Bindung der deklarierten Symbole ist unveränderlich und folgt denselben Regeln wie andere Variablen Bindungen.</span><span class="sxs-lookup"><span data-stu-id="efe37-136">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> 

<span data-ttu-id="efe37-137">Für einige Beispiele ist das unter `qubits` drücken ein Register von Qubits (d. h. vom Typ `Qubit[]` ).</span><span class="sxs-lookup"><span data-stu-id="efe37-137">For some examples, supposing `qubits` is a register of qubits (i.e. of type `Qubit[]`),</span></span> 

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
<span data-ttu-id="efe37-138">Beachten Sie, dass wir am Ende den binären Operator "arithmetischer Shift-Left", "Details", `<<<` die in [numerischen Ausdrücken](xref:microsoft.quantum.guide.expressions#numeric-expressions) gefunden werden können, verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="efe37-138">Note that at the end we utilized the arithmetic-shift-left binary operator, `<<<`, details of which can be found at [Numeric Expressions](xref:microsoft.quantum.guide.expressions#numeric-expressions)</span></span>


## <a name="repeat-until-success-loop"></a><span data-ttu-id="efe37-139">Repeat-Until-Success-Schleife</span><span class="sxs-lookup"><span data-stu-id="efe37-139">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="efe37-140">Die Q #-Sprache ermöglicht eine klassische Ablauf Steuerung, die von den Ergebnissen der Messung von Qubits abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="efe37-140">The Q# language allows classical control flow to depend on the results of measuring qubits.</span></span>
<span data-ttu-id="efe37-141">Diese Funktion ermöglicht es wiederum, leistungsfähige, probabilistische Mini Anwendungen zu implementieren, die die berechnungskosten für die Implementierung von uniflüssen reduzieren können.</span><span class="sxs-lookup"><span data-stu-id="efe37-141">This capability in turn enables implementing powerful probabilistic gadgets that can reduce the computational cost for implementing unitaries.</span></span>
<span data-ttu-id="efe37-142">Beispielsweise ist es einfach, so genannte *Wiederholungs-bis-Erfolg-* Muster (RUS) in Q # zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="efe37-142">As an example, it is easy to implement so-called *Repeat-Until-Success* (RUS) patterns in Q#.</span></span>
<span data-ttu-id="efe37-143">Diese RUS-Muster sind probabilistische Programme, deren Kosten in Bezug auf elementare Gates *erwartungsgemäß* sind, aber für die die echten Kosten von einem tatsächlichen Testlauf und einem tatsächlichen Austausch der verschiedenen möglichen Verzweigungen abhängen.</span><span class="sxs-lookup"><span data-stu-id="efe37-143">These RUS patterns are probabilistic programs that have an *expected* low cost in terms of elementary gates, but for which the true cost depends on an actual run and an actual interleaving of various possible branchings.</span></span>

<span data-ttu-id="efe37-144">Zum Vereinfachen von Wiederholungs-bis-Erfolg-Mustern (RUS) unterstützt Q # die-Konstrukte.</span><span class="sxs-lookup"><span data-stu-id="efe37-144">To facilitate Repeat-Until-Success (RUS) patterns, Q# supports the constructs</span></span>

```qsharp
repeat {
    // do stuff
}
until (expression)
fixup {
    // do other stuff
}
```

<span data-ttu-id="efe37-145">dabei `expression` ist ein beliebiger gültiger Ausdruck, der zu einem Wert vom Typ ausgewertet wird `Bool` .</span><span class="sxs-lookup"><span data-stu-id="efe37-145">where `expression` is any valid expression that evaluates to a value of type `Bool`.</span></span>
<span data-ttu-id="efe37-146">Der Schleifen Text wird ausgeführt, und anschließend wird die Bedingung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="efe37-146">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="efe37-147">Wenn die Bedingung true ist, wird die-Anweisung abgeschlossen. Andernfalls wird das Fixup ausgeführt, und die Anweisung wird erneut ausgeführt, beginnend mit dem Schleifen Text.</span><span class="sxs-lookup"><span data-stu-id="efe37-147">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>

<span data-ttu-id="efe37-148">Alle drei Teile einer Wiederholung/bis-Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich *für jede Wiederholung*behandelt, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="efe37-148">All three portions of a repeat/until loop (the body, the test, and the fixup) are treated as a single scope *for each repetition*, so symbols that are bound in the body are available in the test and in the fixup.</span></span>
<span data-ttu-id="efe37-149">Wenn die Ausführung der Fixup-Anweisung abgeschlossen ist, wird der Bereich für die-Anweisung beendet, sodass im Text-oder Fixup-Bereich vorgenommene Symbol Bindungen in nachfolgenden Wiederholungen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="efe37-149">However completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="efe37-150">Außerdem ist die- `fixup` Anweisung häufig hilfreich, aber nicht immer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="efe37-150">Further, the `fixup` statement is often useful but not always necessary.</span></span>
<span data-ttu-id="efe37-151">In Fällen, in denen er nicht benötigt wird, wird das Konstrukt</span><span class="sxs-lookup"><span data-stu-id="efe37-151">In cases that it is not needed, the construct</span></span>
```qsharp
repeat {
    // do stuff
}
until (expression);
```
<span data-ttu-id="efe37-152">ist auch ein gültiges RUS-Muster.</span><span class="sxs-lookup"><span data-stu-id="efe37-152">is also a valid RUS pattern.</span></span>

<span data-ttu-id="efe37-153">Am unteren Rand dieser Seite werden einige [Beispiele für RUS-Schleifen](#repeat-until-success-examples)vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="efe37-153">At the bottom of this page we present some [examples of RUS loops](#repeat-until-success-examples).</span></span>

> [!TIP]   
> <span data-ttu-id="efe37-154">Vermeiden Sie die Verwendung von Wiederholungs-bis-Erfolg-Schleifen innerhalb von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="efe37-154">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="efe37-155">Die entsprechende Funktionalität wird von while-Schleifen in Funktionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="efe37-155">The corresponding functionality is provided by while loops in functions.</span></span> 

## <a name="while-loop"></a><span data-ttu-id="efe37-156">While-Schleife</span><span class="sxs-lookup"><span data-stu-id="efe37-156">While Loop</span></span>

<span data-ttu-id="efe37-157">Wiederholungs-bis-Erfolg-Muster verfügen über eine sehr Quantum-spezifische-Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="efe37-157">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="efe37-158">Sie werden häufig in bestimmten Klassen von Quantum-Algorithmen verwendet. Dies ist daher das dedizierte Sprachkonstrukt in f #.</span><span class="sxs-lookup"><span data-stu-id="efe37-158">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="efe37-159">Allerdings müssen Schleifen, die basierend auf einer Bedingung unterbrechen und deren Ausführungsdauer zur Kompilierzeit nicht bekannt ist, mit bestimmter Sorgfalt in einer Quantum-Laufzeit behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="efe37-159">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="efe37-160">Die Verwendung in Funktionen andererseits ist nicht problematisch, da diese nur Code enthalten, der auf herkömmlicher (nicht Quantum-) Hardware ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="efe37-160">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="efe37-161">F # unterstützt daher die Verwendung von while-Schleifen nur innerhalb von Functions.</span><span class="sxs-lookup"><span data-stu-id="efe37-161">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="efe37-162">Eine- `while` Anweisung besteht aus dem Schlüsselwort `while` , einer offenen Klammer `(` , einer Bedingung (d. h. einem booleschen Ausdruck), einer schließenden Klammer `)` und einem Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="efe37-162">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="efe37-163">Der Anweisungsblock (der Text der Schleife) wird ausgeführt, solange die Bedingung als ausgewertet wird `true` .</span><span class="sxs-lookup"><span data-stu-id="efe37-163">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```


## <a name="return-statement"></a><span data-ttu-id="efe37-164">Return-Anweisung</span><span class="sxs-lookup"><span data-stu-id="efe37-164">Return Statement</span></span>

<span data-ttu-id="efe37-165">Die Return-Anweisung beendet die Ausführung eines Vorgangs oder einer Funktion und gibt einen Wert an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="efe37-165">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="efe37-166">Er besteht aus dem Schlüsselwort `return` , gefolgt von einem Ausdruck des entsprechenden Typs und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="efe37-166">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="efe37-167">Ein Aufruf bares Element, das ein leeres Tupel zurückgibt, `()` erfordert keine Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="efe37-167">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="efe37-168">Wenn eine frühe Beendigung gewünscht ist, `return ()` kann in diesem Fall verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efe37-168">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="efe37-169">Aufruf Bare Elemente, die einen beliebigen anderen Typ zurückgeben, erfordern eine abschließende Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="efe37-169">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="efe37-170">Es gibt keine maximale Anzahl von Return-Anweisungen innerhalb eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="efe37-170">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="efe37-171">Der Compiler gibt möglicherweise eine Warnung aus, wenn Anweisungen einer Return-Anweisung in einem-Block folgen.</span><span class="sxs-lookup"><span data-stu-id="efe37-171">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="efe37-172">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="efe37-172">For example,</span></span>
```qsharp
return 1;
```
<span data-ttu-id="efe37-173">oder</span><span class="sxs-lookup"><span data-stu-id="efe37-173">or</span></span>
```qsharp
return ();
```
<span data-ttu-id="efe37-174">oder</span><span class="sxs-lookup"><span data-stu-id="efe37-174">or</span></span>
```qsharp
return (results, qubits);
```

## <a name="fail-statement"></a><span data-ttu-id="efe37-175">Fail-Anweisung</span><span class="sxs-lookup"><span data-stu-id="efe37-175">Fail Statement</span></span>

<span data-ttu-id="efe37-176">Die Fail-Anweisung beendet die Ausführung eines Vorgangs und gibt einen Fehlerwert an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="efe37-176">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="efe37-177">Er besteht aus dem Schlüsselwort `fail` , gefolgt von einer Zeichenfolge und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="efe37-177">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="efe37-178">Die Zeichenfolge wird als Fehlermeldung an den klassischen Treiber zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="efe37-178">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="efe37-179">Es gibt keine Einschränkung für die Anzahl der Fail-Anweisungen innerhalb eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="efe37-179">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="efe37-180">Der Compiler gibt möglicherweise eine Warnung aus, wenn-Anweisungen einer Fail-Anweisung innerhalb eines-Blocks folgen.</span><span class="sxs-lookup"><span data-stu-id="efe37-180">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="efe37-181">Ein auf ein Objekt angewendeter</span><span class="sxs-lookup"><span data-stu-id="efe37-181">For example,</span></span>
```qsharp
fail $"Impossible state reached";
```
<span data-ttu-id="efe37-182">oder mithilfe von [interpoliert](xref:microsoft.quantum.guide.expressions#interpolated-strings)Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="efe37-182">or, using [interpolated strings](xref:microsoft.quantum.guide.expressions#interpolated-strings),</span></span>
```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="repeat-until-success-examples"></a><span data-ttu-id="efe37-183">Beispiele für Wiederholung bis zum Erfolg</span><span class="sxs-lookup"><span data-stu-id="efe37-183">Repeat-Until-Success Examples</span></span>

### <a name="rus-pattern-for-single-qubit-rotation-about-an-irrational-axis"></a><span data-ttu-id="efe37-184">RUS-Muster für einzelne Qubit-Drehung über eine irrationale Achse</span><span class="sxs-lookup"><span data-stu-id="efe37-184">RUS pattern for single qubit rotation about an irrational axis</span></span> 

<span data-ttu-id="efe37-185">In einem typischen Anwendungsfall implementiert der folgende Q #-Vorgang eine Drehung um eine irrationale Achse von $ (I + 2i Z)/\sqrt {5} $ in der Bloch-Kugel.</span><span class="sxs-lookup"><span data-stu-id="efe37-185">In a typical use case, the following Q# operation implements a rotation around an irrational axis of $(I + 2i Z)/\sqrt{5}$ on the Bloch sphere.</span></span> <span data-ttu-id="efe37-186">Dies wird mit einem bekannten RUS-Muster erreicht:</span><span class="sxs-lookup"><span data-stu-id="efe37-186">This is accomplished by using a known RUS pattern:</span></span>

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

### <a name="rus-loop-with-mutable-variable-in-scope"></a><span data-ttu-id="efe37-187">RUS-Schleife mit änderbarer Variable im Gültigkeitsbereich</span><span class="sxs-lookup"><span data-stu-id="efe37-187">RUS loop with mutable variable in scope</span></span>

<span data-ttu-id="efe37-188">Dieses Beispiel zeigt die Verwendung einer änderbaren Variablen `finished` , die sich im Gültigkeitsbereich der gesamten Repeat-Until-Fixup-Schleife befindet und die vor der Schleife initialisiert und im fixupschritt aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="efe37-188">This example shows the use of a mutable variable `finished` which is in scope of the entire repeat-until-fixup loop and which gets initialized before the loop and updated in the fixup step.</span></span>

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

### <a name="rus-without-fixup"></a><span data-ttu-id="efe37-189">RUS ohne`fixup`</span><span class="sxs-lookup"><span data-stu-id="efe37-189">RUS without `fixup`</span></span>

<span data-ttu-id="efe37-190">Der folgende Code ist z. b. eine probabilistische Verbindung, die ein wichtiges Drehungs Gate implementiert $V _3 = (\boldone + 2 i Z)/\sqrt {5} $ mithilfe der `H` -und- `T` Gates.</span><span class="sxs-lookup"><span data-stu-id="efe37-190">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the `H` and `T` gates.</span></span>
<span data-ttu-id="efe37-191">Die Schleife wird im Durchschnitt in $ \frac {8} {5} $ Wiederholungen beendet.</span><span class="sxs-lookup"><span data-stu-id="efe37-191">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="efe37-192">Weitere Informationen finden Sie [*unter Repeat-Until-Success: nicht deterministische Zerlegung von Single-Qubit-uniflüssen*](https://arxiv.org/abs/1311.1074) ("Petznick" und "svore", 2014).</span><span class="sxs-lookup"><span data-stu-id="efe37-192">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for more details.</span></span>

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

### <a name="rus-to-prepare-a-quantum-state"></a><span data-ttu-id="efe37-193">RUS zum Vorbereiten eines Quantum-Zustands</span><span class="sxs-lookup"><span data-stu-id="efe37-193">RUS to prepare a quantum state</span></span>

<span data-ttu-id="efe37-194">Schließlich zeigen wir ein Beispiel für ein RUS-Muster zum Vorbereiten eines Quantum-Zustands $ \frac {1} {\sqrt {3} } \left (\sqrt {2} \ket {0} + \ket {1} \right) $, beginnend ab dem $ \ket{+} $-Status.</span><span class="sxs-lookup"><span data-stu-id="efe37-194">Finally, we show an example of a RUS pattern to prepare a quantum state $\frac{1}{\sqrt{3}}\left(\sqrt{2}\ket{0}+\ket{1}\right)$, starting from the $\ket{+}$ state.</span></span>
<span data-ttu-id="efe37-195">Siehe auch das [Beispiel für Komponententests, das mit der Standardbibliothek bereitgestellt](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs)wird:</span><span class="sxs-lookup"><span data-stu-id="efe37-195">See also the [unit testing sample provided with the standard library](https://github.com/microsoft/Quantum/blob/master/samples/diagnostics/unit-testing/RepeatUntilSuccessCircuits.qs):</span></span>

```qsharp
operation PrepareStateUsingRUS(target : Qubit) : Unit {
    using (auxiliary = Qubit()) {
        H(auxiliary);
        repeat {
            // We expect the target and auxiliary qubits to each be in
            // the |+> state.
            AssertProb(
                [PauliX], [target], Zero, 1.0,
                "target qubit should be in the |+> state", 1e-10 );
            AssertProb(
                [PauliX], [auxiliary], Zero, 1.0,
                "auxiliary qubit should be in the |+> state", 1e-10 );

            Adjoint T(auxiliary);
            CNOT(target, auxiliary);
            T(auxiliary);

            // The probability of measuring |+> state on the auxiliary qubit
            // is 3/4.
            AssertProb(
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

<span data-ttu-id="efe37-196">Wichtige programmgesteuerte Features, die in diesem Vorgang gezeigt werden, sind ein komplexerer `fixup` Teil der-Schleife, der Quantum-Vorgänge einschließt, und die Verwendung von- `AssertProb` Anweisungen, um die Wahrscheinlichkeit zu ermitteln, dass der Quantum-Zustand an bestimmten angegebenen Punkten im Programm gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="efe37-196">Notable programmatic features shown in this operation are a more complex `fixup` part of the loop, which involves quantum operations, and the use of `AssertProb` statements to ascertain the probability of measuring the quantum state at certain specified points in the program.</span></span>
<span data-ttu-id="efe37-197">Weitere Informationen zu den-und-Vorgängen finden Sie unter [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging) [`Assert`](xref:microsoft.quantum.intrinsic.assert) [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) .</span><span class="sxs-lookup"><span data-stu-id="efe37-197">See also [Testing and debugging](xref:microsoft.quantum.guide.testingdebugging) for more information about the [`Assert`](xref:microsoft.quantum.intrinsic.assert) and [`AssertProb`](xref:microsoft.quantum.intrinsic.assertprob) operations.</span></span>


## <a name="whats-next"></a><span data-ttu-id="efe37-198">Wie geht es weiter?</span><span class="sxs-lookup"><span data-stu-id="efe37-198">What's Next?</span></span>
<span data-ttu-id="efe37-199">Erfahren Sie mehr über das [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging) in f #.</span><span class="sxs-lookup"><span data-stu-id="efe37-199">Learn about [Testing and Debugging](xref:microsoft.quantum.guide.testingdebugging) in Q#.</span></span>