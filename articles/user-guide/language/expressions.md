---
title: 'Ausdrücke in Q#'
description: 'Erfahren Sie, wie Konstanten, Variablen, Operatoren, Vorgänge und Funktionen als Ausdrücke in angegeben, referenziert und kombiniert werden Q# .'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.expressions
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: e95a7cb9b74136ef9a6f51b4bbc32d1d93c43a0d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691606"
---
# <a name="expressions-in-no-locq"></a><span data-ttu-id="42ff7-103">Ausdrücke in Q#</span><span class="sxs-lookup"><span data-stu-id="42ff7-103">Expressions in Q#</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="42ff7-104">Numerische Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-104">Numeric Expressions</span></span>

<span data-ttu-id="42ff7-105">Numerische Ausdrücke sind Ausdrücke vom Typ `Int` , `BigInt` oder `Double` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-105">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="42ff7-106">Das heißt, Sie sind entweder ganzzahlige oder Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-106">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="42ff7-107">`Int` Literale in Q# werden als Sequenz von Ziffern geschrieben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-107">`Int` literals in Q# are written as a sequence of digits.</span></span>
<span data-ttu-id="42ff7-108">Hexadezimale und binäre ganzzahlige Werte werden unterstützt `0x` `0b` bzw. mit dem Präfix und geschrieben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-108">Hexadecimal and binary integers are supported and written with a `0x` and `0b` prefix, respectively.</span></span>

<span data-ttu-id="42ff7-109">`BigInt` Literale in Q# verfügen über ein nach gestelltes- `l` oder- `L` Suffix.</span><span class="sxs-lookup"><span data-stu-id="42ff7-109">`BigInt` literals in Q# have a trailing `l` or `L` suffix.</span></span>
<span data-ttu-id="42ff7-110">Hexadezimale Big Integerwerte werden unterstützt und mit einem Präfix "0x" geschrieben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-110">Hexadecimal big integers are supported and written with a "0x" prefix.</span></span>
<span data-ttu-id="42ff7-111">Daher sind die folgenden alle gültigen Verwendungsmöglichkeiten von `BigInt` Literalen:</span><span class="sxs-lookup"><span data-stu-id="42ff7-111">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="42ff7-112">`Double` Literale in Q# sind Gleit Komma Zahlen, die mithilfe von Dezimalziffern geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-112">`Double` literals in Q# are floating-point numbers written using decimal digits.</span></span>
<span data-ttu-id="42ff7-113">Sie können mit oder ohne Dezimaltrennzeichen, oder mit einem `.` exponentiellen Teil geschrieben werden, der mit "e" oder "e" angegeben wird (nach dem nur ein mögliches negatives Vorzeichen und Dezimalziffern gültig sind).</span><span class="sxs-lookup"><span data-stu-id="42ff7-113">They can be written with or without a decimal point, `.`, or an exponential part indicated with 'e' or 'E' (after which only a possible negative sign and decimal digits are valid).</span></span>
<span data-ttu-id="42ff7-114">Die folgenden `Double` Literale sind gültig: `0.0` , `1.2e5` , `1e-5` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-114">The following are valid `Double` literals: `0.0`, `1.2e5`, `1e-5`.</span></span>

<span data-ttu-id="42ff7-115">Wenn ein Array Ausdruck eines beliebigen Elementtyps vorhanden ist, können Sie `Int` mithilfe der integrierten Funktion einen Ausdruck bilden [`Length`](xref:Microsoft.Quantum.Core.Length) , wobei der Array Ausdruck in Klammern eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-115">Given an array expression of any element type, you can form an `Int` expression using the [`Length`](xref:Microsoft.Quantum.Core.Length) built-in function, with the array expression enclosed in parentheses.</span></span>
<span data-ttu-id="42ff7-116">Wenn z. b `a` . an ein Array gebunden ist, dann `Length(a)` ist ein ganzzahliger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="42ff7-116">For example, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="42ff7-117">Wenn `b` ein Array von Arrays ganzer Zahlen ist, `Int[][]` dann `Length(b)` ist die Anzahl der Unterarrays in `b` , und `Length(b[1])` die Anzahl von ganzen Zahlen im zweiten Unterarray in `b` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-117">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="42ff7-118">Bei zwei numerischen Ausdrücken desselben Typs können die binären Operatoren, `+` , `-` `*` und `/` verwendet werden, um einen neuen numerischen Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-118">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="42ff7-119">Der Typ des neuen Ausdrucks ist mit den Typen der einzelnen Ausdrücke identisch.</span><span class="sxs-lookup"><span data-stu-id="42ff7-119">The type of the new expression is the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="42ff7-120">Verwenden Sie bei zwei ganzzahligen Ausdrücken den binären Operator `^` (Power), um einen neuen ganzzahligen Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-120">Given two integer expressions, use the binary operator `^` (power) to form a new integer expression.</span></span>
<span data-ttu-id="42ff7-121">Auf ähnliche Weise können Sie auch `^` mit zwei doppelten Ausdrücken verwenden, um einen neuen doppelten Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-121">Similarly, you can also use `^` with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="42ff7-122">Schließlich können Sie `^` mit einer großen Ganzzahl auf der linken Seite und einer Ganzzahl auf der rechten Seite verwenden, um einen neuen großen ganzzahligen Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-122">Finally, you can use `^` with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="42ff7-123">In diesem Fall muss der zweite Parameter in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="42ff7-123">In this case, the second parameter must fit into 32 bits; if not, it raises a runtime error.</span></span>

<span data-ttu-id="42ff7-124">Bei zwei ganzzahligen oder großen ganzzahligen Ausdrücken bilden Sie mithilfe der `%` Operatoren (Modulus), `&&&` (Bitweises and), `|||` (bitweiser or) oder `^^^` (Bitweiser XOR) einen neuen Integer-oder Big Integer-Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="42ff7-124">Given two integer or big integer expressions, form a new integer or big integer expression using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="42ff7-125">Verwenden Sie auf der linken Seite entweder einen ganzzahligen Ausdruck oder einen großen ganzzahligen Ausdruck und einen ganzzahligen Ausdruck auf der rechten Seite, `<<<` `>>>` um einen neuen Ausdruck mit dem gleichen Typ wie den linken Ausdruck zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-125">Given either an integer or big integer expression on the left, and an integer expression on the right, use the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="42ff7-126">Der zweite Parameter (die UMSCHALT Menge) in einen Verschiebungs Vorgang muss größer oder gleich 0 (null) sein. das Verhalten für negative Verschiebungs Beträge ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="42ff7-126">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="42ff7-127">Der Verschiebungs Betrag für einen der Verschiebungs Vorgänge muss ebenfalls in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="42ff7-127">The shift amount for either shift operation must also fit into 32 bits; if not, it raises a runtime error.</span></span>
<span data-ttu-id="42ff7-128">Wenn die verschobene Zahl eine ganze Zahl ist, wird der Verschiebungs Betrag interpretiert, d `mod 64` . h. eine Verschiebung von 1 und eine UMSCHALT 65 haben dieselbe Wirkung.</span><span class="sxs-lookup"><span data-stu-id="42ff7-128">If the number shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="42ff7-129">Bei ganzzahligen und großen ganzzahligen Werten sind Verschiebungen arithmetisch.</span><span class="sxs-lookup"><span data-stu-id="42ff7-129">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="42ff7-130">Wenn Sie einen negativen Wert entweder nach links oder nach rechts verschieben, ergibt dies eine negative Zahl.</span><span class="sxs-lookup"><span data-stu-id="42ff7-130">Shifting a negative value either left or right results in a negative number.</span></span>
<span data-ttu-id="42ff7-131">Das heißt, dass ein Schritt nach links oder rechts verschoben wird, entspricht dem multiplizieren bzw. aufteilen durch 2.</span><span class="sxs-lookup"><span data-stu-id="42ff7-131">That is, shifting one step to the left or right is the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="42ff7-132">Die ganzzahlige Division und der ganzzahlige Modulo folgen dem Verhalten für negative Zahlen wie c#.</span><span class="sxs-lookup"><span data-stu-id="42ff7-132">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span> <span data-ttu-id="42ff7-133">Das heißt, dass `a % b` immer das gleiche Vorzeichen wie hat `a` und `b * (a / b) + a % b` immer gleich ist `a` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-133">That is, `a % b` always has the same sign as `a`, and `b * (a / b) + a % b` always equals `a`.</span></span> <span data-ttu-id="42ff7-134">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42ff7-134">For example:</span></span>

|`A` | `B` | `A / B` | `A % B`|
|:---------:|:----------:|:---------:|:---------:|
| <span data-ttu-id="42ff7-135">5</span><span class="sxs-lookup"><span data-stu-id="42ff7-135">5</span></span> | <span data-ttu-id="42ff7-136">2</span><span class="sxs-lookup"><span data-stu-id="42ff7-136">2</span></span> | <span data-ttu-id="42ff7-137">2</span><span class="sxs-lookup"><span data-stu-id="42ff7-137">2</span></span> | <span data-ttu-id="42ff7-138">1</span><span class="sxs-lookup"><span data-stu-id="42ff7-138">1</span></span> |
| <span data-ttu-id="42ff7-139">5</span><span class="sxs-lookup"><span data-stu-id="42ff7-139">5</span></span> | <span data-ttu-id="42ff7-140">-2</span><span class="sxs-lookup"><span data-stu-id="42ff7-140">-2</span></span> | <span data-ttu-id="42ff7-141">-2</span><span class="sxs-lookup"><span data-stu-id="42ff7-141">-2</span></span> | <span data-ttu-id="42ff7-142">1</span><span class="sxs-lookup"><span data-stu-id="42ff7-142">1</span></span> |
| <span data-ttu-id="42ff7-143">-5</span><span class="sxs-lookup"><span data-stu-id="42ff7-143">-5</span></span> | <span data-ttu-id="42ff7-144">2</span><span class="sxs-lookup"><span data-stu-id="42ff7-144">2</span></span> | <span data-ttu-id="42ff7-145">-2</span><span class="sxs-lookup"><span data-stu-id="42ff7-145">-2</span></span> | <span data-ttu-id="42ff7-146">-1</span><span class="sxs-lookup"><span data-stu-id="42ff7-146">-1</span></span> |
| <span data-ttu-id="42ff7-147">-5</span><span class="sxs-lookup"><span data-stu-id="42ff7-147">-5</span></span> | <span data-ttu-id="42ff7-148">-2</span><span class="sxs-lookup"><span data-stu-id="42ff7-148">-2</span></span> | <span data-ttu-id="42ff7-149">2</span><span class="sxs-lookup"><span data-stu-id="42ff7-149">2</span></span> | <span data-ttu-id="42ff7-150">-1</span><span class="sxs-lookup"><span data-stu-id="42ff7-150">-1</span></span> |

<span data-ttu-id="42ff7-151">Die Division von großen ganzzahligen und Modulo funktioniert auf dieselbe Weise.</span><span class="sxs-lookup"><span data-stu-id="42ff7-151">Big integer division and modulus operations work the same way.</span></span>

<span data-ttu-id="42ff7-152">Wenn ein beliebiger numerischer Ausdruck vorhanden ist, können Sie mit dem unären Operator einen neuen Ausdruck bilden `-` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-152">Given any numeric expression, you can form a new expression using the `-` unary operator.</span></span>
<span data-ttu-id="42ff7-153">Der neue Ausdruck ist derselbe Typ wie der konstituierende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="42ff7-153">The new expression is the same type as the constituent expression.</span></span>

<span data-ttu-id="42ff7-154">Wenn Sie einen ganzzahligen Ausdruck oder einen großen ganzzahligen Ausdruck verwenden, können Sie einen neuen Ausdruck desselben Typs mit dem `~~~` unären Operator (bitweiser Komplement) bilden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-154">Given any integer or big integer expression, you can form a new expression of the same type using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="42ff7-155">Boolesche Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-155">Boolean Expressions</span></span>

<span data-ttu-id="42ff7-156">Die beiden `Bool` Literalwerte sind `true` und `false` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-156">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="42ff7-157">Wenn zwei Ausdrücke desselben primitiven Typs vorhanden sind, können die `==` `!=` binären Operatoren und verwendet werden, um einen-Ausdruck zu erstellen `Bool` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-157">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="42ff7-158">Der Ausdruck ist true, wenn die beiden Ausdrücke gleich sind, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="42ff7-158">The expression is true if the two expressions are equal and false if not.</span></span>

<span data-ttu-id="42ff7-159">Werte von benutzerdefinierten Typen können nicht verglichen werden, sondern es können nur Ihre nicht umschließenden Werte verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-159">Values of user-defined types may not be compared, only their unwrapped values can be compared.</span></span> <span data-ttu-id="42ff7-160">Verwenden Sie z. b. den Operator "Unwrap" `!` (ausführlich unter [Typen in Q# ](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)erläutert).</span><span class="sxs-lookup"><span data-stu-id="42ff7-160">For example, using the "unwrap" operator `!` (explained in detail at [Types in Q#](xref:microsoft.quantum.guide.types#access-anonymous-items-with-the-unwrap-operator)),</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="42ff7-161">Der Gleichheits Vergleich für `Qubit` Werte ist die Identitäts Gleichheit, d. h., ob die beiden Ausdrücke dasselbe Qubit identifizieren.</span><span class="sxs-lookup"><span data-stu-id="42ff7-161">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="42ff7-162">Die Zustände der beiden Qubits werden von diesem Vergleich nicht verglichen, auf Sie zugegriffen, gemessen oder geändert.</span><span class="sxs-lookup"><span data-stu-id="42ff7-162">The states of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="42ff7-163">Der Gleichheits Vergleich für `Double` Werte kann aufgrund von Rundungs Effekten irreführend sein.</span><span class="sxs-lookup"><span data-stu-id="42ff7-163">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="42ff7-164">Beispiel: `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="42ff7-164">For example, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="42ff7-165">Bei zwei numerischen Ausdrücken können die binären Operatoren,, `>` `<` `>=` und `<=` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der erste Ausdruck größer als, kleiner als, größer als oder gleich oder kleiner oder gleich dem zweiten Ausdruck ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-165">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="42ff7-166">Verwenden Sie bei zwei booleschen Ausdrücken den `and` binären-Operator, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn beide Ausdrücke True sind.</span><span class="sxs-lookup"><span data-stu-id="42ff7-166">Given any two Boolean expressions, use the `and` binary operator to construct a new Boolean expression that is true if both of the two expressions are true.</span></span> <span data-ttu-id="42ff7-167">Ebenso erstellt die Verwendung des- `or` Operators einen Ausdruck, der true ist, wenn einer der beiden Ausdrücke True ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-167">Likewise, using the `or` operator creates an expression that is true if either of the two expressions is true.</span></span>

<span data-ttu-id="42ff7-168">Bei jedem booleschen Ausdruck kann der `not` unäre Operator verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der konstituierende Ausdruck false ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-168">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="42ff7-169">Zeichenfolgenausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-169">String expressions</span></span>

<span data-ttu-id="42ff7-170">Q# ermöglicht die Verwendung von Zeichen folgen in der `fail` Anweisung (in der [Ablauf Steuerung](xref:microsoft.quantum.guide.controlflow#fail-statement)erläutert) und in der [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) Standardfunktion.</span><span class="sxs-lookup"><span data-stu-id="42ff7-170">Q# allows strings to be used in the `fail` statement (explained in [Control Flow](xref:microsoft.quantum.guide.controlflow#fail-statement)) and in the [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) standard function.</span></span> <span data-ttu-id="42ff7-171">Das spezifische Verhalten der letzteren hängt vom verwendeten Simulator ab, schreibt jedoch in der Regel eine Meldung in die Host Konsole, wenn Sie während eines Programms aufgerufen wird Q# .</span><span class="sxs-lookup"><span data-stu-id="42ff7-171">The specific behavior of the latter depends on the simulator used but typically writes a message to the host console when called during a Q# program.</span></span>

<span data-ttu-id="42ff7-172">Zeichen folgen in Q# sind entweder Literale oder interpoliert Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-172">Strings in Q# are either literals or interpolated strings.</span></span>

<span data-ttu-id="42ff7-173">Zeichenfolgenliterale ähneln in den meisten Sprachen einfachen Zeichenfolgenliteralen: eine Sequenz von Unicode-Zeichen, die in doppelten Anführungszeichen eingeschlossen sind `" "` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-173">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double-quotes `" "`.</span></span>
<span data-ttu-id="42ff7-174">Verwenden Sie innerhalb einer Zeichenfolge den umgekehrten Schrägstrich, `\` um ein doppeltes Anführungszeichen () mit Escapezeichen `\"` zu versehen, oder um eine neue Zeile ( `\n` ), ein Wagen Rücklauf Zeichen ( `\r` ) oder eine Registerkarte ( `\t` ) einzufügen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-174">Inside of a string, use the backslash character `\` to escape a double-quote character (`\"`), or to insert a new-line ( `\n` ), a carriage return (`\r`), or a tab (`\t`).</span></span>
<span data-ttu-id="42ff7-175">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42ff7-175">For example:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```
### <a name="interpolated-strings"></a><span data-ttu-id="42ff7-176">Interpolierte Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="42ff7-176">Interpolated strings</span></span>

<span data-ttu-id="42ff7-177">Die Q# Syntax für Zeichen folgen Interpolationen ist eine Teilmenge der c#-Syntax.</span><span class="sxs-lookup"><span data-stu-id="42ff7-177">The Q# syntax for string interpolations is a subset of the C# syntax.</span></span> <span data-ttu-id="42ff7-178">Im folgenden finden Sie die wichtigsten Punkte, die Sie betreffen Q# :</span><span class="sxs-lookup"><span data-stu-id="42ff7-178">Following are the key points as they pertain to Q#:</span></span>

* <span data-ttu-id="42ff7-179">Wenn Sie ein Zeichenfolgenliteral als interpolierte Zeichenfolge ermitteln möchten, stellen Sie ihm ein `$`-Symbol voran.</span><span class="sxs-lookup"><span data-stu-id="42ff7-179">To identify a string literal as an interpolated string, prepend it with the `$` symbol.</span></span> <span data-ttu-id="42ff7-180">Zwischen dem `$` und dem `"` , das einen zeichenfolgenliteralvorgang startet, darf kein Leerraum vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="42ff7-180">There can be no white space between the `$` and the `"` that starts a string literal.</span></span>

* <span data-ttu-id="42ff7-181">Im folgenden finden Sie ein einfaches Beispiel, in dem die-Funktion verwendet wird [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) , um das Ergebnis einer Maßeinheit zusammen mit anderen Ausdrücken in die Konsole zu schreiben Q# .</span><span class="sxs-lookup"><span data-stu-id="42ff7-181">The following is a basic example using the [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) function to write the result of a measurement to the console, alongside other Q# expressions.</span></span>

```qsharp
    let num = 8;       // some Q# expression
    let res = M(q);
    Message($"Number: {num}, Result: {res}");
```

* <span data-ttu-id="42ff7-182">Jeder gültige Q# Ausdruck wird möglicherweise in einer interinterierten Zeichenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42ff7-182">Any valid Q# expression may appear in an interpolated string.</span></span>

* <span data-ttu-id="42ff7-183">Ausdrücke in einer interinterierten Zeichenfolge Folgen der Q# Syntax, nicht der c#-Syntax.</span><span class="sxs-lookup"><span data-stu-id="42ff7-183">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span> <span data-ttu-id="42ff7-184">Der wichtigste Unterschied besteht darin, dass Q# keine ausführlichen (mehrzeiligen) interpoliert-Zeichen folgen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42ff7-184">The most notable distinction is that Q# does not support verbatim (multi-line) interpolated strings.</span></span>

<span data-ttu-id="42ff7-185">Weitere Informationen zur c#-Syntax finden Sie unter [*interpoliert*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span><span class="sxs-lookup"><span data-stu-id="42ff7-185">For more details about the C# syntax, see [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings).</span></span>

## <a name="range-expressions"></a><span data-ttu-id="42ff7-186">Bereichs Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-186">Range Expressions</span></span>

<span data-ttu-id="42ff7-187">Bei den drei `Int` Ausdrücken `start` , `step` und `stop` ist der Ausdruck `start .. step .. stop` ein Bereichs Ausdruck, dessen erstes Element `start` , zweites Element `start+step` , drittes Element `start+step+step` , usw. ist, bis Sie übergeben werden `stop` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-187">Given any three `Int` expressions `start`, `step`, and `stop`, the expression `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, and so on, until you pass `stop`.</span></span>
<span data-ttu-id="42ff7-188">Ein Bereich kann leer sein, wenn z. b `step` . positiv und ist `stop < start` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-188">A range may be empty if, for example, `step` is positive and `stop < start`.</span></span>

<span data-ttu-id="42ff7-189">Der Bereich ist an beiden Enden inklusiv.</span><span class="sxs-lookup"><span data-stu-id="42ff7-189">The range is inclusive at both ends.</span></span> <span data-ttu-id="42ff7-190">Das heißt, wenn der Unterschied zwischen `start` und `stop` ein ganzzahliges Vielfache von ist `step` , ist das letzte Element des Bereichs `stop` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-190">That is, if the difference between `start` and `stop` is an integer multiple of `step`, the last element of the range will be `stop`.</span></span>

<span data-ttu-id="42ff7-191">`Int`Bei zwei Ausdrücken `start` und `stop` ist der Ausdruck `start .. stop` ein Bereichs Ausdruck, der gleich ist `start .. 1 .. stop` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-191">Given any two `Int` expressions `start` and `stop`, the expression `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="42ff7-192">Beachten Sie, dass der implizierte Wert `step` + 1 ist, auch wenn `stop` kleiner als ist `start` . in einem solchen Fall ist der Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="42ff7-192">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="42ff7-193">Einige Beispiel Bereiche sind:</span><span class="sxs-lookup"><span data-stu-id="42ff7-193">Some example ranges are:</span></span>

- <span data-ttu-id="42ff7-194">`1..3` der Bereich von 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="42ff7-194">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="42ff7-195">`2..2..5` ist der Bereich von 2, 4.</span><span class="sxs-lookup"><span data-stu-id="42ff7-195">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="42ff7-196">`2..2..6` ist der Bereich von 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="42ff7-196">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="42ff7-197">`6..-2..2` der Bereich ist 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="42ff7-197">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="42ff7-198">`2..1` der leere Bereich.</span><span class="sxs-lookup"><span data-stu-id="42ff7-198">`2..1` is the empty range.</span></span>
- <span data-ttu-id="42ff7-199">`2..6..7` der Bereich 2.</span><span class="sxs-lookup"><span data-stu-id="42ff7-199">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="42ff7-200">`2..2..1` der leere Bereich.</span><span class="sxs-lookup"><span data-stu-id="42ff7-200">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="42ff7-201">`1..-1..2` der leere Bereich.</span><span class="sxs-lookup"><span data-stu-id="42ff7-201">`1..-1..2` is the empty range.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="42ff7-202">Qubit-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-202">Qubit Expressions</span></span>

<span data-ttu-id="42ff7-203">Die einzigen `Qubit` Ausdrücke sind Symbole, die an `Qubit` Werte oder Array Elemente von Arrays gebunden sind `Qubit` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-203">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="42ff7-204">Es sind keine `Qubit` Literale vorhanden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-204">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="42ff7-205">Pauli-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-205">Pauli Expressions</span></span>

<span data-ttu-id="42ff7-206">Die vier Werte,,, `Pauli` `PauliI` `PauliX` `PauliY` und `PauliZ` sind gültige `Pauli` Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="42ff7-206">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="42ff7-207">Abgesehen davon sind die einzigen `Pauli` Ausdrücke Symbole, die an `Pauli` Werte oder Array Elemente von Arrays gebunden sind `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-207">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="42ff7-208">Ergebnis Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-208">Result Expressions</span></span>

<span data-ttu-id="42ff7-209">Die beiden `Result` Werte `One` und `Zero` sind gültige `Result` Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="42ff7-209">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="42ff7-210">Abgesehen davon sind die einzigen `Result` Ausdrücke Symbole, die an `Result` Werte oder Array Elemente von Arrays gebunden sind `Result` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-210">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="42ff7-211">Beachten Sie insbesondere, dass `One` nicht mit der ganzen Zahl identisch ist `1` , und es gibt keine direkte Konvertierung zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-211">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="42ff7-212">Das gleiche gilt für `Zero` und `0` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-212">The same is true for `Zero` and `0`.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="42ff7-213">Tupelausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-213">Tuple Expressions</span></span>

<span data-ttu-id="42ff7-214">Ein tupelliteralelement ist eine Sequenz von Element Ausdrücken des entsprechenden Typs, die durch Kommas getrennt sind und in Klammern eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="42ff7-214">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in parentheses.</span></span>
<span data-ttu-id="42ff7-215">Beispielsweise `(1, One)` ist ein `(Int, Result)` Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="42ff7-215">For example, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="42ff7-216">Abgesehen von Literalen sind die einzigen Tupelausdrücke Symbole, die an Tupelwerte, Array Elemente von tupelarrays und Aufruf Bare Aufrufe gebunden sind, die Tupel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-216">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="42ff7-217">User-Defined typausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-217">User-Defined Type Expressions</span></span>

<span data-ttu-id="42ff7-218">Ein Literalwert eines benutzerdefinierten Typs besteht aus dem Typnamen, gefolgt von einem tupelliteraltyp mit dem basistupeltyp des Typs.</span><span class="sxs-lookup"><span data-stu-id="42ff7-218">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="42ff7-219">Wenn z. b. `IntPair` ein benutzerdefinierter Typ ist `(Int, Int)` , der auf basiert, dann `IntPair(2, 3)` ist ein gültiges Literale dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="42ff7-219">For example, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2, 3)` is a valid literal of that type.</span></span>

<span data-ttu-id="42ff7-220">Anders als Literale sind die einzigen Ausdrücke eines benutzerdefinierten Typs Symbole, die an Werte dieses Typs gebunden sind, Array Elemente von Arrays dieses Typs und Aufruf Bare Aufrufe, die diesen Typ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-220">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="42ff7-221">Entpacken von Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="42ff7-221">Unwrap Expressions</span></span>

<span data-ttu-id="42ff7-222">In Q# handelt es sich bei dem Unwrap-Operator um ein nach gestelltes Ausrufezeichen `!` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-222">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="42ff7-223">Wenn z. b `IntPair` . ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ `(Int, Int)` und `s` eine Variable mit Wert ist `IntPair(2, 3)` , dann `s!` ist `(2, 3)` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-223">For example, if `IntPair` is a user-defined type with the underlying type `(Int, Int)` and `s` is a variable with value `IntPair(2, 3)`, then `s!` is `(2, 3)`.</span></span>

<span data-ttu-id="42ff7-224">Bei benutzerdefinierten Typen, die in Bezug auf andere benutzerdefinierte Typen definiert sind, können Sie den Unwrap-Operator wiederholen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-224">For user-defined types defined in terms of other user-defined types, you can repeat the unwrap operator.</span></span> <span data-ttu-id="42ff7-225">`s!!`Gibt z. b. den doppelt entpackten Wert von an `s` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-225">For example, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="42ff7-226">Wenn `WrappedPair` ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ ist `IntPair` und `t` eine Variable mit dem Wert ist, `WrappedPair(IntPair(1,2))` dann `t!!` ist `(1,2)` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-226">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` is `(1,2)`.</span></span>

<span data-ttu-id="42ff7-227">Der `!` Operator hat eine höhere Rangfolge als alle anderen Operatoren, außer `[]` für die Array Indizierung und die Slicing.</span><span class="sxs-lookup"><span data-stu-id="42ff7-227">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="42ff7-228">`!` und `[]` binden Sie Positions bedingt, `a[i]![3]` d. h., wird gelesen als `((a[i])!)[3]` : nehmen Sie das `i` th-Element von `a` , entpacken Sie es, und holen Sie dann das dritte Element des entpackten Werts (der ein Array sein muss).</span><span class="sxs-lookup"><span data-stu-id="42ff7-228">`!` and `[]` bind positionally; that is, `a[i]![3]` is read as `((a[i])!)[3]`: take the `i`th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="42ff7-229">Die Rangfolge des `!` Operators hat eine Beeinträchtigung, die möglicherweise nicht offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-229">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="42ff7-230">Wenn eine Funktion oder ein Vorgang einen Wert zurückgibt, der dann entpackt wird, muss der Funktions-oder Vorgangs Ausdruck in Klammern eingeschlossen werden, damit das Argument Tupel an den-Ausdruck gebunden wird, anstatt an den Unwrap-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="42ff7-230">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="42ff7-231">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42ff7-231">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="42ff7-232">Array Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-232">Array Expressions</span></span>

<span data-ttu-id="42ff7-233">Ein Arrayliteral ist eine Sequenz von einem oder mehreren Element Ausdrücken, die durch Kommas getrennt sind und in eckige Klammern eingeschlossen sind `[]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-233">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in square brackets `[]`.</span></span>
<span data-ttu-id="42ff7-234">Alle-Elemente müssen mit demselben Typ kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="42ff7-234">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="42ff7-235">Verwenden Sie bei zwei Arrays desselben Typs den binären Operator, `+` um ein neues Array zu bilden, das die Verkettung der beiden Arrays ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-235">Given two arrays of the same type, use the binary `+` operator to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="42ff7-236">Beispiel: `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`</span><span class="sxs-lookup"><span data-stu-id="42ff7-236">For example, `[1,2,3] + [4,5,6]` = `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="42ff7-237">Array Erstellung</span><span class="sxs-lookup"><span data-stu-id="42ff7-237">Array Creation</span></span>

<span data-ttu-id="42ff7-238">Verwenden Sie bei Angabe eines Typs und eines `Int` Ausdrucks den- `new` Operator, um ein neues Array mit der angegebenen Größe zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-238">Given a type and an `Int` expression, use the `new` operator to allocate a new array of the given size.</span></span>
<span data-ttu-id="42ff7-239">`new Int[i + 1]`Weist z. b. ein neues `Int` Array mit- `i + 1` Elementen zu.</span><span class="sxs-lookup"><span data-stu-id="42ff7-239">For example, `new Int[i + 1]` allocates a new `Int` array with `i + 1` elements.</span></span>

<span data-ttu-id="42ff7-240">Leere Array Literale, wie z `[]` . b., sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="42ff7-240">Empty array literals, such as `[]`, are not allowed.</span></span>
<span data-ttu-id="42ff7-241">Stattdessen können Sie ein Array der Länge 0 (null) erstellen, indem Sie verwenden `new T[0]` , wobei `T` ein Platzhalter für einen geeigneten Typ ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-241">Instead, you can create an array of length zero by using `new T[0]`, where `T` is a placeholder for a suitable type.</span></span>

<span data-ttu-id="42ff7-242">Die Elemente eines neuen Arrays initialisieren einen typabhängigen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="42ff7-242">The elements of a new array initialize to a type-dependent default value.</span></span>
<span data-ttu-id="42ff7-243">In den meisten Fällen ist dies eine Variation von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="42ff7-243">In most cases, this is some variation of zero.</span></span>

<span data-ttu-id="42ff7-244">Bei Qubits und callables, bei denen es sich um Verweise auf Entitäten handelt, gibt es keinen angemessenen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="42ff7-244">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="42ff7-245">Daher ist für diese Typen der Standardwert ein ungültiger Verweis, den Sie nicht ohne einen Laufzeitfehler verwenden können, ähnlich wie bei einem NULL-Verweis in Sprachen wie c# oder Java.</span><span class="sxs-lookup"><span data-stu-id="42ff7-245">Thus, for these types, the default is an invalid reference that you cannot use without causing a runtime error, similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="42ff7-246">Arrays, die Qubits oder callables enthalten, müssen mit nicht standardmäßigen Werten initialisiert werden, bevor Sie Ihre Elemente sicher verwenden können.</span><span class="sxs-lookup"><span data-stu-id="42ff7-246">Arrays containing qubits or callables must be initialized with non-default values before you can use their elements safely.</span></span> <span data-ttu-id="42ff7-247">Geeignete Initialisierungs Routinen finden Sie unter <xref:Microsoft.Quantum.Arrays> .</span><span class="sxs-lookup"><span data-stu-id="42ff7-247">For suitable initialization routines, see <xref:Microsoft.Quantum.Arrays>.</span></span>

<span data-ttu-id="42ff7-248">Die Standardwerte für jeden Typ lauten:</span><span class="sxs-lookup"><span data-stu-id="42ff7-248">The default values for each type are:</span></span>

<span data-ttu-id="42ff7-249">type</span><span class="sxs-lookup"><span data-stu-id="42ff7-249">Type</span></span> | <span data-ttu-id="42ff7-250">Standard</span><span class="sxs-lookup"><span data-stu-id="42ff7-250">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="42ff7-251">_Ungültiges Qubit_</span><span class="sxs-lookup"><span data-stu-id="42ff7-251">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="42ff7-252">Der leere Bereich, `1..1..0`</span><span class="sxs-lookup"><span data-stu-id="42ff7-252">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="42ff7-253">_Ungültige Aufruf Bare_</span><span class="sxs-lookup"><span data-stu-id="42ff7-253">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="42ff7-254">Tupeltypen initialisieren Element für Element.</span><span class="sxs-lookup"><span data-stu-id="42ff7-254">Tuple types initialize element-by-element.</span></span>


### <a name="array-elements"></a><span data-ttu-id="42ff7-255">Array Elemente</span><span class="sxs-lookup"><span data-stu-id="42ff7-255">Array Elements</span></span>

<span data-ttu-id="42ff7-256">Wenn ein Array Ausdruck und ein `Int` Ausdruck angegeben sind, erstellen Sie einen neuen Ausdruck mit dem Array Element-Operator `[]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-256">Given an array expression and an `Int` expression, form a new expression using the array element operator `[]`.</span></span>
<span data-ttu-id="42ff7-257">Der neue Ausdruck ist derselbe Typ wie der Elementtyp des Arrays.</span><span class="sxs-lookup"><span data-stu-id="42ff7-257">The new expression is the same type as the element type of the array.</span></span>
<span data-ttu-id="42ff7-258">Wenn z. b. `a` an ein Array vom Typ gebunden ist `Double` , dann `a[4]` ist ein- `Double` Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="42ff7-258">For example, if `a` is bound to an array of type `Double`, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="42ff7-259">Wenn es sich bei dem Array Ausdruck nicht um einen einfachen Bezeichner handelt, müssen Sie ihn in Klammern einschließen, um ein Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-259">If the array expression is not a simple identifier, you must enclose it in parentheses to select an element.</span></span>
<span data-ttu-id="42ff7-260">Wenn z. b. `a` und `b` beide Arrays vom Typ sind `Int` , wird ein Element aus der Verkettung folgendermaßen ausgedrückt:</span><span class="sxs-lookup"><span data-stu-id="42ff7-260">For example, if `a` and `b` are both arrays of type `Int`, an element from the concatenation is expressed as:</span></span>

```qsharp
(a + b)[13]
```

<span data-ttu-id="42ff7-261">Alle Arrays in Q# sind NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="42ff7-261">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="42ff7-262">Das heißt, das erste Element eines Arrays `a` ist immer `a[0]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-262">That is, the first element of an array `a` is always `a[0]`.</span></span>


### <a name="array-slices"></a><span data-ttu-id="42ff7-263">Array Slices</span><span class="sxs-lookup"><span data-stu-id="42ff7-263">Array Slices</span></span>

<span data-ttu-id="42ff7-264">Wenn ein Array Ausdruck und ein `Range` Ausdruck angegeben sind, erstellen Sie einen neuen Ausdruck mithilfe des Array Slice-Operators `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-264">Given an array expression and a `Range` expression, form a new expression using the array slice operator `[ ]`.</span></span>
<span data-ttu-id="42ff7-265">Der neue Ausdruck hat denselben Typ wie das Array und enthält die Array Elemente, die von den Elementen des-Elements indiziert `Range` werden, in der Reihenfolge, die von definiert wird `Range` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-265">The new expression is the same type as the array and contains the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="42ff7-266">Wenn z. b. `a` an ein Array vom Typ gebunden ist `Double` , dann `a[3..-1..0]` ist ein-Ausdruck, `Double[]` der die ersten vier Elemente von enthält, `a` jedoch in umgekehrter Reihenfolge, wie Sie in angezeigt werden `a` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-266">For example, if `a` is bound to an array of type `Double`, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="42ff7-267">Wenn das `Range` leer ist, ist das resultierende Array in der Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="42ff7-267">If the `Range` is empty, then the resulting array slice is zero length.</span></span>

<span data-ttu-id="42ff7-268">Ebenso wie beim Verweisen auf Array Elemente müssen Sie, wenn der Array Ausdruck kein einfacher Bezeichner ist, ihn in Klammern einschließen, um ihn in Slices aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-268">Just as with referencing array elements, if the array expression is not a simple identifier, you must enclose it in parentheses to slice it.</span></span>
<span data-ttu-id="42ff7-269">Wenn z. b. `a` und `b` beide Arrays vom Typ sind `Int` , wird ein Slice aus der Verkettung folgendermaßen ausgedrückt:</span><span class="sxs-lookup"><span data-stu-id="42ff7-269">For example, if `a` and `b` are both arrays of type `Int`, a slice from the concatenation is expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

#### <a name="inferred-startend-values"></a><span data-ttu-id="42ff7-270">Abherleitet anfangs-/Endwerte</span><span class="sxs-lookup"><span data-stu-id="42ff7-270">Inferred start/end values</span></span>

<span data-ttu-id="42ff7-271">Ab unserer [Version 0,8](xref:microsoft.quantum.relnotes)unterstützen wir Kontext Ausdrücke für die Bereichs Aufteilung.</span><span class="sxs-lookup"><span data-stu-id="42ff7-271">Starting with our [0.8 release](xref:microsoft.quantum.relnotes), we support contextual expressions for range slicing.</span></span> <span data-ttu-id="42ff7-272">Vor allem können Sie Bereichs Start-und Endwerte im Kontext eines Bereichs aufteilen-Ausdrucks weglassen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-272">In particular, you may omit range start and end values in the context of a range slicing expression.</span></span> <span data-ttu-id="42ff7-273">In diesem Fall wendet der Compiler die folgenden Regeln an, um die vorgesehenen Trennzeichen für den Bereich abzuleiten:</span><span class="sxs-lookup"><span data-stu-id="42ff7-273">In that case, the compiler applies the following rules to infer the intended delimiters for the range:</span></span>

* <span data-ttu-id="42ff7-274">Wenn der Bereichs *Start* Wert weggelassen wird, wird der abherleitet Startwert</span><span class="sxs-lookup"><span data-stu-id="42ff7-274">If the range *start* value is omitted, then the inferred start value</span></span>
  * <span data-ttu-id="42ff7-275">ist 0 (null), wenn kein Schritt angegeben oder der angegebene Schritt positiv ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-275">is zero if no step is specified or the specified step is positive.</span></span>  
  * <span data-ttu-id="42ff7-276">die Länge des aufgeschnittenen Arrays minus 1, wenn der angegebene Schritt negativ ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-276">is the length of the sliced array minus one if the specified step is negative.</span></span>

* <span data-ttu-id="42ff7-277">Wenn der Wert für den Bereichs *Endpunkt* weggelassen wird, wird der abherende Endwert</span><span class="sxs-lookup"><span data-stu-id="42ff7-277">If the range *end* value is omitted, then the inferred end value</span></span>
  * <span data-ttu-id="42ff7-278">die Länge des aufgeschnittenen Arrays minus 1, wenn kein Schritt angegeben oder der angegebene Schritt positiv ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-278">is the length of the sliced array minus one if no step is specified or the specified step is positive.</span></span>
  * <span data-ttu-id="42ff7-279">ist 0 (null), wenn der angegebene Schritt negativ ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-279">is zero if the specified step is negative.</span></span>

<span data-ttu-id="42ff7-280">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="42ff7-280">Some examples are:</span></span>

```qsharp
let arr = [1,2,3,4,5,6];
let slice1  = arr[3...];      // slice1 is [4,5,6];
let slice2  = arr[0..2...];   // slice2 is [1,3,5];
let slice3  = arr[...2];      // slice3 is [1,2,3];
let slice4  = arr[...2..3];   // slice4 is [1,3];
let slice5  = arr[...2...];   // slice5 is [1,3,5];
let slice7  = arr[4..-2...];  // slice7 is [5,3,1];
let slice8  = arr[...-1..3];  // slice8 is [6,5,4];
let slice9  = arr[...-1...];  // slice9 is [6,5,4,3,2,1];
let slice10 = arr[...];       // slice10 is [1,2,3,4,5,6];
```

### <a name="copy-and-update-expressions"></a><span data-ttu-id="42ff7-281">Copy-und Update-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-281">Copy-and-Update Expressions</span></span>

<span data-ttu-id="42ff7-282">Da es Q# sich bei allen Typen um Werttypen handelt (wobei die Qubits eine etwas besondere Rolle einnehmen), wird formal eine "Copy"-Kopie erstellt, wenn ein Wert an ein Symbol gebunden ist oder wenn ein Symbol erneut hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="42ff7-282">Since all Q# types are value types (with the qubits taking a somewhat special role), formally a "copy" is created when a value is bound to a symbol or when a symbol is rebound.</span></span> <span data-ttu-id="42ff7-283">Dies heißt, dass das Verhalten von Q# mit dem identisch ist, wenn eine Kopie mithilfe eines Zuweisungs Operators erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="42ff7-283">That is to say, the behavior of Q# is the same as if a copy were created using an assignment operator.</span></span> 

<span data-ttu-id="42ff7-284">Natürlich werden in der Praxis nur die relevanten Teile nach Bedarf neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="42ff7-284">Of course, in practice, only the relevant pieces are recreated as needed.</span></span> <span data-ttu-id="42ff7-285">Dies wirkt sich darauf aus, wie Arrays kopiert werden, da Array Elemente nicht aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="42ff7-285">This affects how you copy arrays because it is not possible to update array items.</span></span> <span data-ttu-id="42ff7-286">Zum Ändern eines vorhandenen Arrays muss ein *Kopier-und Aktualisierungs* Mechanismus genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-286">To modify an existing array requires leveraging a *copy-and-update* mechanism.</span></span>

<span data-ttu-id="42ff7-287">Sie können ein neues Array aus einem vorhandenen Array mithilfe von *Copy-und Update-* Ausdrücken erstellen, die die Operatoren `w/` und verwenden `<-` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-287">You can create a new array from an existing array via *copy-and-update* expressions, which use the operators `w/` and `<-`.</span></span>
<span data-ttu-id="42ff7-288">Ein Copy-and-Update-Ausdruck ist ein Ausdruck der Form `expression1 w/ expression2 <- expression3` , wobei</span><span class="sxs-lookup"><span data-stu-id="42ff7-288">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where</span></span>

* <span data-ttu-id="42ff7-289">`expression1` muss `T[]` für einen Typ vom Typ sein `T` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-289">`expression1` must be type `T[]` for some type `T`.</span></span>
* <span data-ttu-id="42ff7-290">`expression2` definiert, welche Indizes in dem in angegebenen Array `expression1` geändert werden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-290">`expression2` defines which indices in the array specified in `expression1` to modify.</span></span> <span data-ttu-id="42ff7-291">`expression2` muss entweder vom Typ `Int` oder vom Typ sein `Range` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-291">`expression2` must be either type `Int` or type `Range`.</span></span>
* <span data-ttu-id="42ff7-292">`expression3` der Wert (n), der zum Aktualisieren von Elementen in verwendet wird `expression1` , basierend auf den in angegebenen Indizes `expression2` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-292">`expression3` is the value(s) used to update elements in `expression1`, based on the indices specified in `expression2`.</span></span> <span data-ttu-id="42ff7-293">Wenn `expression2` vom Typ ist `Int` , `expression3` muss vom Typ sein `T` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-293">If `expression2` is type `Int`, `expression3` must be type `T`.</span></span> <span data-ttu-id="42ff7-294">Wenn `expression2` vom Typ ist `Range` , `expression3` muss vom Typ sein `T[]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-294">If `expression2` is type `Range`, `expression3` must be type `T[]`.</span></span>

<span data-ttu-id="42ff7-295">Beispielsweise erstellt der Copy-and-Update-Ausdruck `arr w/ idx <- value` ein neues Array mit allen Elementen, die auf die entsprechenden Elemente in festgelegt sind `arr` , mit Ausnahme der durch angegebenen Elemente `idx` , die auf den Wert (e) in festgelegt ist `value` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-295">For example, the copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding elements in `arr`, except for the element(s) specified by `idx`, which is set to the value(s) in `value`.</span></span> 

<span data-ttu-id="42ff7-296">`arr`Das angegebene enthält das Array. `[0,1,2,3]`</span><span class="sxs-lookup"><span data-stu-id="42ff7-296">Given `arr` contains the array `[0,1,2,3]`, then</span></span> 

- <span data-ttu-id="42ff7-297">`arr w/ 0 <- 10` ist das Array `[10,1,2,3]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-297">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="42ff7-298">`arr w/ 2 <- 10` ist das Array `[0,1,10,3]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-298">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="42ff7-299">`arr w/ 0..2..3 <- [10,12]` ist das Array `[10,1,12,3]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-299">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

#### <a name="copy-and-update-expressions-for-named-items"></a><span data-ttu-id="42ff7-300">Copy-und Update-Ausdrücke für benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="42ff7-300">Copy-and-update expressions for named items</span></span>

<span data-ttu-id="42ff7-301">Ähnliche Ausdrücke sind für benannte Elemente in benutzerdefinierten Typen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-301">Similar expressions exist for named items in user-defined types.</span></span> 

<span data-ttu-id="42ff7-302">Nehmen Sie z. b. den Typ.</span><span class="sxs-lookup"><span data-stu-id="42ff7-302">For example, consider the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="42ff7-303">Wenn `c` den Wert des Typs enthält `Complex(1., -1.)` , dann `c w/ Re <- 0.` ist ein Ausdruck vom Typ, der ergibt `Complex` `Complex(0., -1.)` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-303">If `c` contains the value of type `Complex(1., -1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0., -1.)`.</span></span>

### <a name="jagged-arrays"></a><span data-ttu-id="42ff7-304">Verzweigte Arrays</span><span class="sxs-lookup"><span data-stu-id="42ff7-304">Jagged Arrays</span></span>

<span data-ttu-id="42ff7-305">Eine Jagged Array, manchmal auch als "Array von Arrays" bezeichnet, ist ein Array, dessen Elemente Arrays sind.</span><span class="sxs-lookup"><span data-stu-id="42ff7-305">A jagged array, sometimes called an "array of arrays," is an array whose elements are arrays.</span></span>
<span data-ttu-id="42ff7-306">Die Elemente einer Jagged Array können unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="42ff7-306">The elements of a jagged array can be of different sizes.</span></span>
<span data-ttu-id="42ff7-307">Im folgenden Beispiel wird gezeigt, wie Sie eine Jagged Array deklarieren und initialisieren, die eine Multiplikationstabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="42ff7-307">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

```qsharp
let N = 4;
mutable multiplicationTable = new Int[][N];
for (i in 1..N) {
    mutable row = new Int[i];
    for (j in 1..i) {
        set row w/= j-1 <- i * j;
    }
    set multiplicationTable w/= i-1 <- row;
}
```

### <a name="arrays-of-callables"></a><span data-ttu-id="42ff7-308">Arrays von callables</span><span class="sxs-lookup"><span data-stu-id="42ff7-308">Arrays of callables</span></span> 

<span data-ttu-id="42ff7-309">Sie können auch ein Array von callables erstellen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-309">You can also create an array of callables.</span></span>

* <span data-ttu-id="42ff7-310">Wenn der allgemeine Elementtyp ein Vorgang oder Funktionstyp ist, müssen alle Elemente die gleichen Eingabe-und Ausgabetypen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-310">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
* <span data-ttu-id="42ff7-311">Der Elementtyp des Arrays unterstützt alle [Funktoren](xref:microsoft.quantum.guide.operationsfunctions) , die von allen Elementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-311">The element type of the array supports any [functors](xref:microsoft.quantum.guide.operationsfunctions) that are supported by all of the elements.</span></span>
<span data-ttu-id="42ff7-312">Wenn z. b. `Op1` , `Op2` und `Op3` alle Vorgänge sind, unterstützt, unterstützt und unterstützt jedoch `Qubit[] => Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` beide:</span><span class="sxs-lookup"><span data-stu-id="42ff7-312">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit` operations, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>
  * <span data-ttu-id="42ff7-313">`[Op1, Op2]` ist ein Array von `(Qubit[] => Unit)` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-313">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
  * <span data-ttu-id="42ff7-314">`[Op1, Op3]` ist ein Array von `(Qubit[] => Unit is Adj)` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-314">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
  * <span data-ttu-id="42ff7-315">`[Op2, Op3]` ist ein Array von `(Qubit[] => Unit is Ctl)` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-315">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="42ff7-316">Während die Vorgänge `(Qubit[] => Unit is Adj)` und  `(Qubit[] => Unit is Ctl)` den gemeinsamen Basistyp aufweisen `(Qubit[] => Unit)` , verwenden *Arrays* dieser Vorgänge jedoch keinen gemeinsamen Basistyp.</span><span class="sxs-lookup"><span data-stu-id="42ff7-316">However, while the operations `(Qubit[] => Unit is Adj)` and  `(Qubit[] => Unit is Ctl)` have the common base type of `(Qubit[] => Unit)`, *arrays* of these operations do not share a common base type.</span></span>

<span data-ttu-id="42ff7-317">Beispielsweise gibt `[[Op1], [Op2]]` derzeit einen Fehler aus, da versucht wird, ein Array der beiden inkompatiblen Array Typen und zu erstellen `(Qubit[] => Unit is Adj)[]` `(Qubit[] => Unit is Ctl)[]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-317">For example, `[[Op1], [Op2]]` would currently raise an error because it attempts to create an array of the two incompatible array types `(Qubit[] => Unit is Adj)[]` and `(Qubit[] => Unit is Ctl)[]`.</span></span>

<span data-ttu-id="42ff7-318">Weitere Informationen zu callables finden Sie unter [Aufruf Bare Ausdrücke](#callable-expressions) auf dieser Seite bzw. [in den Vorgängen und Funktionen in Q# ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="42ff7-318">For more information on callables, see [Callable expressions](#callable-expressions)  on this page or [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="42ff7-319">Bedingte Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-319">Conditional Expressions</span></span>

<span data-ttu-id="42ff7-320">Wenn zwei Ausdrücke desselben Typs und ein boolescher Ausdruck verwendet werden, bilden Sie einen Bedingungs Ausdruck mithilfe des Fragezeichens, `?` und des vertikalen Balkens `|` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-320">Given two expressions of the same type and a Boolean expression, form a conditional expression using the question mark, `?`, and the vertical bar `|`.</span></span> <span data-ttu-id="42ff7-321">Gibt `a==b ? c | d` an, dass der Wert des bedingten Ausdrucks ist, wenn den Wert `c` `a==b` true hat und wenn der Wert `d` false ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-321">Given `a==b ? c | d`, the value of the conditional expression is `c` if `a==b` is true and `d` if it is false.</span></span>

### <a name="conditional-expressions-with-callables"></a><span data-ttu-id="42ff7-322">Bedingte Ausdrücke mit callables</span><span class="sxs-lookup"><span data-stu-id="42ff7-322">Conditional expressions with callables</span></span>

<span data-ttu-id="42ff7-323">Bedingte Ausdrücke können zu Vorgängen ausgewertet werden, die über die gleichen Eingaben und Ausgaben verfügen, aber unterschiedliche Funktions tüktoren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-323">Conditional expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span> <span data-ttu-id="42ff7-324">In diesem Fall ist der Typ des bedingten Ausdrucks ein Vorgang mit Eingaben und Ausgaben, die alle von beiden Ausdrücken unterstützten Funktoren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-324">In this case, the type of the conditional expression is an operation with inputs and outputs that support any functors supported by both expressions.</span></span>
<span data-ttu-id="42ff7-325">Wenn z. b. `Op1` , `Op2` und `Op3` alle sind, unterstützt, unterstützt und unterstützt jedoch `Qubit[]=>Unit` `Op1` `Adjoint` `Op2` `Controlled` `Op3` beide:</span><span class="sxs-lookup"><span data-stu-id="42ff7-325">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="42ff7-326">`flag ? Op1 | Op2` ist ein- `(Qubit[] => Unit)` Vorgang.</span><span class="sxs-lookup"><span data-stu-id="42ff7-326">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="42ff7-327">`flag ? Op1 | Op3` ist ein- `(Qubit[] => Unit is Adj)` Vorgang.</span><span class="sxs-lookup"><span data-stu-id="42ff7-327">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="42ff7-328">`flag ? Op2 | Op3` ist ein- `(Qubit[] => Unit is Ctl)` Vorgang.</span><span class="sxs-lookup"><span data-stu-id="42ff7-328">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="42ff7-329">Wenn einer der beiden möglichen Ergebnis Ausdrücke einen Funktions-oder einen Vorgangs aufzurufen enthält, findet dieser Vorgang nur statt, wenn das Ergebnis das Ergebnis ist, das der Wert des Aufrufes ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-329">If either of the two possible result expressions include a function or operation call, that call only takes place if that result is the one that is the value of the call.</span></span> <span data-ttu-id="42ff7-330">Wenn z. b. `a==b ? C(qs) | D(qs)` `a==b` true ist, wird der `C` Vorgang aufgerufen, und wenn false ist, wird nur der `D` Vorgang aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-330">For example, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true, then the `C` operation is invoked, and if it is false then only the `D` operation is invoked.</span></span> <span data-ttu-id="42ff7-331">Diese Vorgehensweise ähnelt der *Kurzschluss* in anderen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-331">This approach is similar to *short-circuiting* in other languages.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="42ff7-332">Aufruf Bare Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-332">Callable Expressions</span></span>

<span data-ttu-id="42ff7-333">Ein Aufruf bares Literalelement ist der Name eines Vorgangs oder einer Funktion, der im Kompilierungs Bereich definiert ist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-333">A callable literal is the name of an operation or function defined in the compilation scope.</span></span> <span data-ttu-id="42ff7-334">Beispielsweise ist ein vorgangsliteral, `X` das auf den `X` -Standard Bibliotheks Vorgang verweist, und `Message` ist ein Funktionsliteral, das auf die Standard Bibliotheks `Message` Funktion verweist.</span><span class="sxs-lookup"><span data-stu-id="42ff7-334">For example, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="42ff7-335">Wenn ein Vorgang das `Adjoint` Funktor unterstützt, `Adjoint op` ist ein Vorgangs Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="42ff7-335">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="42ff7-336">Entsprechend `Controlled` `Controlled op` ist ein Vorgangs Ausdruck, wenn der Vorgang das Funktor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="42ff7-336">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="42ff7-337">Weitere Informationen zu den Typen dieser Ausdrücke finden Sie unter [Aufrufen von Vorgangs Spezialisierungs](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations)Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-337">For more information about the types of these expressions, see [Calling operation specializations](xref:microsoft.quantum.guide.operationsfunctions#calling-operation-specializations).</span></span>

<span data-ttu-id="42ff7-338">Funktoren ( `Adjoint` und `Controlled` ) werden genauer gebunden als alle anderen Operatoren, mit Ausnahme des Unwrap `!` -Operators und der Array Indizierung mit `[ ]` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-338">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[ ]`.</span></span>
<span data-ttu-id="42ff7-339">Daher sind die folgenden Elemente gültig, vorausgesetzt, dass die-Vorgänge die verwendeten Funktoren unterstützen:</span><span class="sxs-lookup"><span data-stu-id="42ff7-339">Thus, the following are all valid, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

### <a name="type-parameterized-callable-expressions"></a><span data-ttu-id="42ff7-340">Typparametrisierte Aufruf Bare Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-340">Type-parameterized callable expressions</span></span>

<span data-ttu-id="42ff7-341">Sie können ein Aufruf bares Literalzeichen als Wert verwenden, um es z. b. einer Variablen zuzuweisen oder es an eine andere Aufruf Bare zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-341">You can use a callable literal as a value, for example, to assign it to a variable or pass it to another callable.</span></span> <span data-ttu-id="42ff7-342">Wenn die Aufruf Bare [Typparameter](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables)enthält, müssen Sie in diesem Fall die Parameter als Teil des Aufruf baren Werts angeben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-342">In this case, if the callable has [type parameters](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables), you must provide the parameters as part of the callable value.</span></span>

<span data-ttu-id="42ff7-343">Ein Aufruf barer Wert darf keine nicht angegebenen Typparameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-343">A callable value cannot have any unspecified type parameters.</span></span> <span data-ttu-id="42ff7-344">Wenn z. b. `Fun` eine Funktion mit der Signatur ist `'T1->Unit` :</span><span class="sxs-lookup"><span data-stu-id="42ff7-344">For example, if `Fun` is a function with the signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is (Int->Unit).
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun<Double>);   // A (Double->Unit) is passed to SomeOtherFun.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="42ff7-345">Aufruf Bare Aufruf Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="42ff7-345">Callable Invocation Expressions</span></span>

<span data-ttu-id="42ff7-346">Wenn ein Aufruf barer Ausdruck (Vorgang oder Funktion) und ein Tupelausdruck des Eingabetyps der Aufruf baren Signatur angegeben werden, können Sie einen *Aufruf Ausdruck* bilden, indem Sie den Tupelausdruck an den Aufruf baren Ausdruck anhängen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-346">Given a callable expression (operation or function) and a tuple expression of the input type of the callable's signature, you can form an *invocation expression* by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="42ff7-347">Der Typ des Aufruf Ausdrucks ist der Ausgabetyp der Signatur des Callable-Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="42ff7-347">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="42ff7-348">Wenn z. b `Op` . ein Vorgang mit der Signatur ist `((Int, Qubit) => Double)` , `Op(3, qubit1)` ist ein Ausdruck vom Typ `Double` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-348">For example, if `Op` is an operation with the signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="42ff7-349">Ebenso ist, wenn `Sin` eine Funktion mit der Signatur ist `(Double -> Double)` , `Sin(0.1)` ein Ausdruck vom Typ `Double` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-349">Similarly, if `Sin` is a function with the signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="42ff7-350">Wenn schließlich `Builder` eine Funktion mit der Signatur ist `(Int -> (Int -> Int))` , dann `Builder(3)` ist eine Funktion von `Int` zu `Int` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-350">Finally, if `Builder` is a function with the signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from `Int` to `Int`.</span></span>

<span data-ttu-id="42ff7-351">Zum Aufrufen des Ergebnisses eines Aufruf baren Ausdrucks ist ein zusätzliches Paar von Klammern um den Aufruf baren Ausdruck erforderlich.</span><span class="sxs-lookup"><span data-stu-id="42ff7-351">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="42ff7-352">Um also das Ergebnis des Aufrufs `Builder` aus dem vorherigen Absatz aufzurufen, ist die korrekte Syntax:</span><span class="sxs-lookup"><span data-stu-id="42ff7-352">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="42ff7-353">Wenn Sie einen [vom Typ parametrisierten](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) Aufruf baren aufrufen, können Sie die tatsächlichen Typparameter innerhalb von spitzen Klammern `< >` nach dem Aufruf baren Ausdruck angeben.</span><span class="sxs-lookup"><span data-stu-id="42ff7-353">When invoking a [type-parameterized](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) callable, you can specify the actual type parameters within angle brackets `< >` after the callable expression.</span></span>
<span data-ttu-id="42ff7-354">Diese Aktion ist in der Regel unnötig, da der Q# Compiler die eigentlichen Typen leitet.</span><span class="sxs-lookup"><span data-stu-id="42ff7-354">This action is usually unnecessary as the Q# compiler infers the actual types.</span></span>
<span data-ttu-id="42ff7-355">Es *ist* jedoch für die [partielle Anwendung](xref:microsoft.quantum.guide.operationsfunctions#partial-application) erforderlich, wenn ein typparametrisiertes Argument nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="42ff7-355">However, it *is* required for [partial application](xref:microsoft.quantum.guide.operationsfunctions#partial-application) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="42ff7-356">Dies ist auch nützlich, wenn die Übergabe von Vorgängen mit unterschiedlichen Funktoren unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="42ff7-356">It is also useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="42ff7-357">Wenn z. b. die Signatur hat und die Signatur und die Signatur aufweisen, muss `Func` `('T1, 'T2, 'T1) -> 'T2` `Op1` `Op2` `(Qubit[] => Unit is Adj)` `Op3` `(Qubit[] => Unit)` `Func` mit `Op1` als erstes Argument, `Op2` als zweites und `Op3` als drittes aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="42ff7-357">For example, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="42ff7-358">Die Typspezifikation ist erforderlich `Op3` , da und `Op1` unterschiedliche Typen aufweisen, sodass der Compiler dies ohne Angabe der Spezifikation als mehrdeutig behandelt.</span><span class="sxs-lookup"><span data-stu-id="42ff7-358">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="42ff7-359">Operatorrangfolge</span><span class="sxs-lookup"><span data-stu-id="42ff7-359">Operator Precedence</span></span>

* <span data-ttu-id="42ff7-360">Alle binären Operatoren sind mit Ausnahme von rechts assoziativ `^` .</span><span class="sxs-lookup"><span data-stu-id="42ff7-360">All binary operators are right-associative, except for `^`.</span></span>

* <span data-ttu-id="42ff7-361">Eckige Klammern (für das Aufteilen `[ ]` und Indizieren von Arrays) werden vor jedem Operator gebunden.</span><span class="sxs-lookup"><span data-stu-id="42ff7-361">Brackets, `[ ]`, for array slicing and indexing, bind before any operator.</span></span>

* <span data-ttu-id="42ff7-362">Die Funktoren `Adjoint` und die `Controlled` Bindung nach der Array Indizierung, aber vor allen anderen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="42ff7-362">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

* <span data-ttu-id="42ff7-363">Klammern für Vorgangs-und Funktionsaufrufe werden auch vor jedem Operator gebunden, aber nach der Array Indizierung und den Funktoren.</span><span class="sxs-lookup"><span data-stu-id="42ff7-363">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="42ff7-364">Q# Operatoren in Rangfolge, vom höchsten zum niedrigsten:</span><span class="sxs-lookup"><span data-stu-id="42ff7-364">Q# operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="42ff7-365">Betreiber</span><span class="sxs-lookup"><span data-stu-id="42ff7-365">Operator</span></span> | <span data-ttu-id="42ff7-366">Ständigkeit</span><span class="sxs-lookup"><span data-stu-id="42ff7-366">Arity</span></span> | <span data-ttu-id="42ff7-367">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42ff7-367">Description</span></span> | <span data-ttu-id="42ff7-368">Operanden Typen</span><span class="sxs-lookup"><span data-stu-id="42ff7-368">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="42ff7-369">nachträ `!`</span><span class="sxs-lookup"><span data-stu-id="42ff7-369">trailing `!`</span></span> | <span data-ttu-id="42ff7-370">Unär</span><span class="sxs-lookup"><span data-stu-id="42ff7-370">Unary</span></span> | <span data-ttu-id="42ff7-371">Aufheben der Umschließung</span><span class="sxs-lookup"><span data-stu-id="42ff7-371">Unwrap</span></span> | <span data-ttu-id="42ff7-372">Ein beliebiger benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="42ff7-372">Any user-defined type</span></span>
 <span data-ttu-id="42ff7-373">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="42ff7-373">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="42ff7-374">Unär</span><span class="sxs-lookup"><span data-stu-id="42ff7-374">Unary</span></span> | <span data-ttu-id="42ff7-375">Numerische negative, bitweise Komplement logische Negation</span><span class="sxs-lookup"><span data-stu-id="42ff7-375">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="42ff7-376">`Int`, `BigInt` oder `Double` für `-` , `Int` `BigInt` `~~~` `Bool` für `not`</span><span class="sxs-lookup"><span data-stu-id="42ff7-376">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="42ff7-377">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-377">Binary</span></span> | <span data-ttu-id="42ff7-378">Ganzzahlige Potenz</span><span class="sxs-lookup"><span data-stu-id="42ff7-378">Integer power</span></span> | <span data-ttu-id="42ff7-379">`Int` oder `BigInt` für die Basisklasse `Int` für den Exponenten</span><span class="sxs-lookup"><span data-stu-id="42ff7-379">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="42ff7-380">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="42ff7-380">`/`, `*`, `%`</span></span> | <span data-ttu-id="42ff7-381">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-381">Binary</span></span> | <span data-ttu-id="42ff7-382">Division, Multiplikation, ganzzahliger Modulo</span><span class="sxs-lookup"><span data-stu-id="42ff7-382">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="42ff7-383">`Int`, `BigInt` oder `Double` für `/` und `*` `Int` oder `BigInt` für `%`</span><span class="sxs-lookup"><span data-stu-id="42ff7-383">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="42ff7-384">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="42ff7-384">`+`, `-`</span></span> | <span data-ttu-id="42ff7-385">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-385">Binary</span></span> | <span data-ttu-id="42ff7-386">Addition oder Zeichenfolge und Array Verkettung, Subtraktion</span><span class="sxs-lookup"><span data-stu-id="42ff7-386">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="42ff7-387">`Int`, `BigInt` oder `Double` , zusätzlich `String` oder ein beliebiger Arraytyp für `+`</span><span class="sxs-lookup"><span data-stu-id="42ff7-387">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="42ff7-388">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="42ff7-388">`<<<`, `>>>`</span></span> | <span data-ttu-id="42ff7-389">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-389">Binary</span></span> | <span data-ttu-id="42ff7-390">Left Shift, Right Shift</span><span class="sxs-lookup"><span data-stu-id="42ff7-390">Left shift, right shift</span></span> | <span data-ttu-id="42ff7-391">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="42ff7-391">`Int` or `BigInt`</span></span>
 <span data-ttu-id="42ff7-392">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="42ff7-392">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="42ff7-393">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-393">Binary</span></span> | <span data-ttu-id="42ff7-394">Kleiner-als-, kleiner-als-oder-gleich-, größer-als-, größer-als-oder-gleich-Vergleiche</span><span class="sxs-lookup"><span data-stu-id="42ff7-394">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="42ff7-395">`Int`, `BigInt` oder `Double`</span><span class="sxs-lookup"><span data-stu-id="42ff7-395">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="42ff7-396">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="42ff7-396">`==`, `!=`</span></span> | <span data-ttu-id="42ff7-397">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-397">Binary</span></span> | <span data-ttu-id="42ff7-398">gleich, nicht gleichmäßige Vergleiche</span><span class="sxs-lookup"><span data-stu-id="42ff7-398">equal, not-equal comparisons</span></span> | <span data-ttu-id="42ff7-399">beliebiger primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="42ff7-399">any primitive type</span></span>
 `&&&` | <span data-ttu-id="42ff7-400">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-400">Binary</span></span> | <span data-ttu-id="42ff7-401">Bitweises AND</span><span class="sxs-lookup"><span data-stu-id="42ff7-401">Bitwise AND</span></span> | <span data-ttu-id="42ff7-402">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="42ff7-402">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="42ff7-403">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-403">Binary</span></span> | <span data-ttu-id="42ff7-404">Bitweises XOR</span><span class="sxs-lookup"><span data-stu-id="42ff7-404">Bitwise XOR</span></span> | <span data-ttu-id="42ff7-405">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="42ff7-405">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="42ff7-406">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-406">Binary</span></span> | <span data-ttu-id="42ff7-407">Bitweises OR</span><span class="sxs-lookup"><span data-stu-id="42ff7-407">Bitwise OR</span></span> | <span data-ttu-id="42ff7-408">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="42ff7-408">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="42ff7-409">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-409">Binary</span></span> | <span data-ttu-id="42ff7-410">Logisches AND</span><span class="sxs-lookup"><span data-stu-id="42ff7-410">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="42ff7-411">Binary</span><span class="sxs-lookup"><span data-stu-id="42ff7-411">Binary</span></span> | <span data-ttu-id="42ff7-412">Logisches OR</span><span class="sxs-lookup"><span data-stu-id="42ff7-412">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="42ff7-413">Binär/Ternär</span><span class="sxs-lookup"><span data-stu-id="42ff7-413">Binary/Ternary</span></span> | <span data-ttu-id="42ff7-414">Bereichs Operator</span><span class="sxs-lookup"><span data-stu-id="42ff7-414">Range operator</span></span> | `Int`
 <span data-ttu-id="42ff7-415">`?` `|`</span><span class="sxs-lookup"><span data-stu-id="42ff7-415">`?` `|`</span></span> | <span data-ttu-id="42ff7-416">TERNÄRE</span><span class="sxs-lookup"><span data-stu-id="42ff7-416">Ternary</span></span> | <span data-ttu-id="42ff7-417">Bedingt</span><span class="sxs-lookup"><span data-stu-id="42ff7-417">Conditional</span></span> | <span data-ttu-id="42ff7-418">`Bool` für die linke Seite</span><span class="sxs-lookup"><span data-stu-id="42ff7-418">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="42ff7-419">`w/` `<-`</span><span class="sxs-lookup"><span data-stu-id="42ff7-419">`w/` `<-`</span></span> | <span data-ttu-id="42ff7-420">TERNÄRE</span><span class="sxs-lookup"><span data-stu-id="42ff7-420">Ternary</span></span> | <span data-ttu-id="42ff7-421">Kopieren und aktualisieren</span><span class="sxs-lookup"><span data-stu-id="42ff7-421">Copy-and-update</span></span> | <span data-ttu-id="42ff7-422">Weitere Informationen finden Sie unter [Copy-and-Update-Ausdrücke](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="42ff7-422">See [Copy-and-update expressions](#copy-and-update-expressions)</span></span>

## <a name="next-steps"></a><span data-ttu-id="42ff7-423">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="42ff7-423">Next steps</span></span>

<span data-ttu-id="42ff7-424">Nachdem Sie nun mit Ausdrücken in arbeiten können Q# , fahren Sie mit den [Vorgängen und Q# Funktionen in](xref:microsoft.quantum.guide.operationsfunctions) fort, um zu erfahren, wie Sie Vorgänge und Funktionen definieren und aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="42ff7-424">Now that you can work with expressions in Q#, move on to [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions) to learn how to define and call operations and functions.</span></span>
