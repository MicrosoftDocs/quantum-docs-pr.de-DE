---
title: Ausdrücke | Microsoft-Dokumentation
description: Ausdrücke
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.expressions
ms.openlocfilehash: 09d493df4e1178fee1f7a5946cfda2f411111006
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185204"
---
# <a name="expressions"></a><span data-ttu-id="8410c-103">Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-103">Expressions</span></span>

## <a name="grouping"></a><span data-ttu-id="8410c-104">Gruppierung</span><span class="sxs-lookup"><span data-stu-id="8410c-104">Grouping</span></span>

<span data-ttu-id="8410c-105">Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="8410c-105">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="8410c-106">`(7)` ist beispielsweise ein `Int` Ausdruck. `([1,2,3])` ist ein Ausdruck vom Typ Array von `Int`s, und `((1,2))` ist ein Ausdruck vom Typ `(Int, Int)`.</span><span class="sxs-lookup"><span data-stu-id="8410c-106">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="8410c-107">Die Äquivalenz zwischen einfachen Werten und Tupeln mit einem einzelnen Element, die im [Typmodell](xref:microsoft.quantum.language.type-model#tuple-types) beschrieben werden, entfernt die Mehrdeutigkeit zwischen `(6)` als Gruppe und `(6)` als ein Tupel mit einem einzelnen Element.</span><span class="sxs-lookup"><span data-stu-id="8410c-107">The equivalence between simple values and single-element tuples described in [the type model](xref:microsoft.quantum.language.type-model#tuple-types) removes the ambiguity between `(6)` as a group and `(6)` as a single-element tuple.</span></span>

## <a name="symbols"></a><span data-ttu-id="8410c-108">MB</span><span class="sxs-lookup"><span data-stu-id="8410c-108">Symbols</span></span>

<span data-ttu-id="8410c-109">Der Name eines Symbols, das einem Wert des Typs `'T` gebunden oder zugewiesen ist, ist ein Ausdruck vom Typ `'T`.</span><span class="sxs-lookup"><span data-stu-id="8410c-109">The name of a symbol bound or assigned to a value of type `'T` is an expression of type `'T`.</span></span>
<span data-ttu-id="8410c-110">Wenn beispielsweise das Symbol `count` an den ganzzahligen Wert `5`gebunden ist, ist `count` ein ganzzahliger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-110">For instance, if the symbol `count` is bound to the integer value `5`, then `count` is an integer expression.</span></span>

## <a name="numeric-expressions"></a><span data-ttu-id="8410c-111">Numerische Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-111">Numeric Expressions</span></span>

<span data-ttu-id="8410c-112">Numerische Ausdrücke sind Ausdrücke vom Typ `Int`, `BigInt`oder `Double`.</span><span class="sxs-lookup"><span data-stu-id="8410c-112">Numeric expressions are expressions of type `Int`, `BigInt`, or `Double`.</span></span>
<span data-ttu-id="8410c-113">Das heißt, Sie sind entweder ganzzahlige oder Gleit Komma Zahlen.</span><span class="sxs-lookup"><span data-stu-id="8410c-113">That is, they are either integer or floating-point numbers.</span></span>

<span data-ttu-id="8410c-114">`Int` Literale in Q # sind mit ganzzahligen literalen C#in identisch, mit dem Unterschied, dass kein nach gestelltes "l" oder "l" erforderlich (oder zulässig) ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-114">`Int` literals in Q# are identical to integer literals in C#, except that no trailing "l" or "L" is required (or allowed).</span></span>
<span data-ttu-id="8410c-115">Hexadezimale und binäre ganze Zahlen werden mit dem Präfix "0x" bzw. "0B" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8410c-115">Hexadecimal and binary integers are supported with a "0x" and "0b" prefix respectively.</span></span>

<span data-ttu-id="8410c-116">`BigInt` Literale in Q # sind identisch mit großen ganzzahligen Zeichen folgen in .net mit einem nachfolgenden "l" oder "l".</span><span class="sxs-lookup"><span data-stu-id="8410c-116">`BigInt` literals in Q# are identical to big integer strings in .NET, with a trailing "l" or "L".</span></span>
<span data-ttu-id="8410c-117">Hexadezimale große ganze Zahlen werden mit dem Präfix "0x" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8410c-117">Hexadecimal big integers are supported with a "0x" prefix.</span></span>
<span data-ttu-id="8410c-118">Daher sind die folgenden alle gültigen Verwendungsmöglichkeiten von `BigInt` Literalen:</span><span class="sxs-lookup"><span data-stu-id="8410c-118">Thus, the following are all valid uses of `BigInt` literals:</span></span>

```qsharp
let bigZero = 0L;
let bigHex = 0x123456789abcdef123456789abcdefL;
let bigOne = bigZero + 1L;
```

<span data-ttu-id="8410c-119">`Double` Literale in Q # sind mit doppelten Literalen in C#identisch, mit dem Unterschied, dass kein nach gestelltes "d" oder "d" erforderlich (oder zulässig) ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-119">`Double` literals in Q# are identical to double literals in C#, except that no trailing "d" or "D" is required (or allowed).</span></span>

<span data-ttu-id="8410c-120">Wenn ein Array Ausdruck eines beliebigen Elementtyps vorhanden ist, kann ein `Int` Ausdruck mit der integrierten Funktion `Length` gebildet werden, wobei der Array Ausdruck in Klammern, `(` und `)`eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-120">Given an array expression of any element type, an `Int` expression may be formed using the `Length` built-in function, with the array expression enclosed in parentheses, `(` and `)`.</span></span>
<span data-ttu-id="8410c-121">Wenn `a` beispielsweise an ein Array gebunden ist, ist `Length(a)` ein ganzzahliger Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-121">For instance, if `a` is bound to an array, then `Length(a)` is an integer expression.</span></span>
<span data-ttu-id="8410c-122">Wenn `b` ein Array von Arrays mit ganzen Zahlen ist, `Int[][]`, dann ist `Length(b)` die Anzahl der Unterarrays in `b`, und `Length(b[1])` ist die Anzahl von ganzen Zahlen im zweiten Unterarray in `b`.</span><span class="sxs-lookup"><span data-stu-id="8410c-122">If `b` is an array of arrays of integers, `Int[][]`, then `Length(b)` is the number of sub-arrays in `b`, and `Length(b[1])` is the number of integers in the second sub-array in `b`.</span></span>

<span data-ttu-id="8410c-123">Bei zwei numerischen Ausdrücken desselben Typs können die binären Operatoren `+`, `-`, `*`und `/` verwendet werden, um einen neuen numerischen Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="8410c-123">Given two numeric expressions of the same type, the binary operators `+`, `-`, `*`, and `/` may be used to form a new numeric expression.</span></span>
<span data-ttu-id="8410c-124">Der Typ des neuen Ausdrucks ist mit den Typen der einzelnen Ausdrücke identisch.</span><span class="sxs-lookup"><span data-stu-id="8410c-124">The type of the new expression will be the same as the types of the constituent expressions.</span></span>

<span data-ttu-id="8410c-125">Bei zwei ganzzahligen Ausdrücken kann der binäre Operator `^` (Power) verwendet werden, um einen neuen ganzzahligen Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="8410c-125">Given two integer expressions, the binary operator `^` (power) may be used to form a new integer expression.</span></span>
<span data-ttu-id="8410c-126">Ebenso können `^` mit zwei doppelten Ausdrücken verwendet werden, um einen neuen doppelten Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="8410c-126">Similarly, `^` may be used with two double expressions to form a new double expression.</span></span>
<span data-ttu-id="8410c-127">Schließlich können `^` mit einer großen Ganzzahl auf der linken Seite und einer ganzen Zahl auf der rechten Seite verwendet werden, um einen neuen großen ganzzahligen Ausdruck zu bilden.</span><span class="sxs-lookup"><span data-stu-id="8410c-127">Finally, `^` may be used with a big integer on the left and an integer on the right to form a new big integer expression.</span></span>
<span data-ttu-id="8410c-128">In diesem Fall muss der zweite Parameter in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8410c-128">In this case, the second parameter must fit into 32 bits; if not, a runtime error will be raised.</span></span>

<span data-ttu-id="8410c-129">Bei zwei ganzzahligen oder großen ganzzahligen Ausdrücken kann ein neuer Integer-Ausdruck oder ein großer ganzzahliger Ausdruck mithilfe des `%` (Modulus), `&&&` (bitweisen und), `|||` (bitweisen OR) oder `^^^` (bitweisen XOR)-Operatoren gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-129">Given two integer or big integer expressions, a new integer or big integer expression may be formed using the `%` (modulus), `&&&` (bitwise AND), `|||` (bitwise OR), or `^^^` (bitwise XOR) operators.</span></span>

<span data-ttu-id="8410c-130">Wenn auf der linken Seite entweder ein ganzzahliger Ausdruck oder ein großer ganzzahliger Ausdruck und ein ganzzahliger Ausdruck auf der rechten Seite angegeben ist, können die `<<<`-Operatoren (arithmetischer Left Shift) oder `>>>` (arithmetische rechts Schiebe) zum Erstellen eines neuen Ausdrucks mit demselben Typ wie der linke verwendet werden. Begriff.</span><span class="sxs-lookup"><span data-stu-id="8410c-130">Given either an integer or big integer expression on the left, and an integer expression on the right, the `<<<` (arithmetic left shift) or `>>>` (arithmetic right shift) operators may be used to create a new expression with the same type as the left-hand expression.</span></span>

<span data-ttu-id="8410c-131">Der zweite Parameter (die UMSCHALT Menge) in einen Verschiebungs Vorgang muss größer oder gleich 0 (null) sein. das Verhalten für negative Verschiebungs Beträge ist nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="8410c-131">The second parameter (the shift amount) to either shift operation must be greater than or equal to zero; the behavior for negative shift amounts is undefined.</span></span>
<span data-ttu-id="8410c-132">Der Verschiebungs Betrag für einen der Verschiebungs Vorgänge muss ebenfalls in 32 Bits passen. Wenn dies nicht der Fall ist, wird ein Laufzeitfehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="8410c-132">The shift amount for either shift operation must also fit into 32 bits; if not, a runtime error will be raised.</span></span>
<span data-ttu-id="8410c-133">Wenn die zu Verschiebe Zahl eine ganze Zahl ist, wird die UMSCHALT Menge `mod 64`; Das heißt, dass eine Verschiebung von 1 und eine Schicht von 65 denselben Effekt haben.</span><span class="sxs-lookup"><span data-stu-id="8410c-133">If the number to be shifted is an integer, then the shift amount is interpreted `mod 64`; that is, a shift of 1 and a shift of 65 have the same effect.</span></span>

<span data-ttu-id="8410c-134">Bei ganzzahligen und großen ganzzahligen Werten sind Verschiebungen arithmetisch.</span><span class="sxs-lookup"><span data-stu-id="8410c-134">For both integer and big integer values, shifts are arithmetic.</span></span>
<span data-ttu-id="8410c-135">Wenn Sie einen negativen Wert entweder nach links oder rechts verschieben, ergibt dies eine negative Zahl.</span><span class="sxs-lookup"><span data-stu-id="8410c-135">Shifting a negative value either left or right will result in a negative number.</span></span>
<span data-ttu-id="8410c-136">Das heißt, die Verschiebung eines Schritts nach links oder rechts ist identisch mit der Multiplikation bzw. Division durch 2.</span><span class="sxs-lookup"><span data-stu-id="8410c-136">That is, shifting one step to the left or right is exactly the same as multiplying or dividing by 2, respectively.</span></span>

<span data-ttu-id="8410c-137">Die ganzzahlige Division und der ganzzahlige Modulo folgen dem C#Verhalten für negative Zahlen als.</span><span class="sxs-lookup"><span data-stu-id="8410c-137">Integer division and integer modulus follow the same behavior for negative numbers as C#.</span></span>
<span data-ttu-id="8410c-138">Das heißt, `a % b` immer dasselbe Zeichen wie `a`haben, und `b * (a / b) + a % b` immer gleich `a`.</span><span class="sxs-lookup"><span data-stu-id="8410c-138">That is, `a % b` will always have the same sign as `a`, and `b * (a / b) + a % b` will always equal `a`.</span></span>
<span data-ttu-id="8410c-139">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8410c-139">For example:</span></span>

 `A` | `B` | `A / B` | `A % B`
---------|----------|---------|---------
 <span data-ttu-id="8410c-140">5</span><span class="sxs-lookup"><span data-stu-id="8410c-140">5</span></span> | <span data-ttu-id="8410c-141">2</span><span class="sxs-lookup"><span data-stu-id="8410c-141">2</span></span> | <span data-ttu-id="8410c-142">2</span><span class="sxs-lookup"><span data-stu-id="8410c-142">2</span></span> | <span data-ttu-id="8410c-143">1</span><span class="sxs-lookup"><span data-stu-id="8410c-143">1</span></span>
 <span data-ttu-id="8410c-144">5</span><span class="sxs-lookup"><span data-stu-id="8410c-144">5</span></span> | <span data-ttu-id="8410c-145">-2</span><span class="sxs-lookup"><span data-stu-id="8410c-145">-2</span></span> | <span data-ttu-id="8410c-146">-2</span><span class="sxs-lookup"><span data-stu-id="8410c-146">-2</span></span> | <span data-ttu-id="8410c-147">1</span><span class="sxs-lookup"><span data-stu-id="8410c-147">1</span></span>
 <span data-ttu-id="8410c-148">-5</span><span class="sxs-lookup"><span data-stu-id="8410c-148">-5</span></span> | <span data-ttu-id="8410c-149">2</span><span class="sxs-lookup"><span data-stu-id="8410c-149">2</span></span> | <span data-ttu-id="8410c-150">-2</span><span class="sxs-lookup"><span data-stu-id="8410c-150">-2</span></span> | <span data-ttu-id="8410c-151">-1</span><span class="sxs-lookup"><span data-stu-id="8410c-151">-1</span></span>
 <span data-ttu-id="8410c-152">-5</span><span class="sxs-lookup"><span data-stu-id="8410c-152">-5</span></span> | <span data-ttu-id="8410c-153">-2</span><span class="sxs-lookup"><span data-stu-id="8410c-153">-2</span></span> | <span data-ttu-id="8410c-154">2</span><span class="sxs-lookup"><span data-stu-id="8410c-154">2</span></span> | <span data-ttu-id="8410c-155">-1</span><span class="sxs-lookup"><span data-stu-id="8410c-155">-1</span></span>

<span data-ttu-id="8410c-156">Große ganzzahlige Division und Modulo funktionieren auf dieselbe Weise.</span><span class="sxs-lookup"><span data-stu-id="8410c-156">Big integer division and modulus works the same way.</span></span>

<span data-ttu-id="8410c-157">Wenn ein beliebiger numerischer Ausdruck vorhanden ist, kann ein neuer Ausdruck mithilfe des `-` unären Operators gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-157">Given any numeric expression, a new expression may be formed using the `-` unary operator.</span></span>
<span data-ttu-id="8410c-158">Der neue Ausdruck hat denselben Typ wie der konstituierende Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-158">The new expression will be the same type as the constituent expression.</span></span>

<span data-ttu-id="8410c-159">Bei jedem Integer-Ausdruck oder einem Big Integer-Ausdruck kann ein neuer Ausdruck desselben Typs mithilfe des `~~~` (bitweisen Komplement) unären Operators gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-159">Given any integer or big integer expression, a new expression of the same type may be formed using the `~~~` (bitwise complement) unary operator.</span></span>

## <a name="boolean-expressions"></a><span data-ttu-id="8410c-160">Boolesche Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-160">Boolean Expressions</span></span>

<span data-ttu-id="8410c-161">Die beiden `Bool` Literalwerte sind `true` und `false`.</span><span class="sxs-lookup"><span data-stu-id="8410c-161">The two `Bool` literal values are `true` and `false`.</span></span>

<span data-ttu-id="8410c-162">Wenn zwei Ausdrücke desselben primitiven Typs vorhanden sind, können die `==` und `!=` binäre Operatoren verwendet werden, um einen `Bool` Ausdruck zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8410c-162">Given any two expressions of the same primitive type, the `==` and `!=` binary operators may be used to construct a `Bool` expression.</span></span>
<span data-ttu-id="8410c-163">Der Ausdruck ist true, wenn die beiden Ausdrücke (bzw. nicht) gleich sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-163">The expression will be true if the two expressions are (resp. are not) equal.</span></span>

<span data-ttu-id="8410c-164">Werte von benutzerdefinierten Typen können nicht verglichen werden, sondern nur ihre Werte können verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-164">Values of user-defined types may not be compared, only their values can be compared.</span></span> <span data-ttu-id="8410c-165">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8410c-165">For example,</span></span>

```qsharp
newtype WrappedInt = Int;     // Yes, this is a contrived example
let x = WrappedInt(1);
let y = WrappedInt(2);
let z = x! == y!;             // This will compile and yield z = false.
let t = x == y;               // This will cause a compiler error.
```

<span data-ttu-id="8410c-166">Der Gleichheits Vergleich für `Qubit` Werte ist Identitäts Gleichheit. Das heißt, ob die beiden Ausdrücke dasselbe Qubit identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8410c-166">Equality comparison for `Qubit` values is identity equality; that is, whether the two expressions identify the same qubit.</span></span>
<span data-ttu-id="8410c-167">Der Zustand der beiden Qubits wird von diesem Vergleich nicht verglichen, auf Sie zugegriffen, gemessen oder geändert.</span><span class="sxs-lookup"><span data-stu-id="8410c-167">The state of the two qubits are not compared, accessed, measured, or modified by this comparison.</span></span>

<span data-ttu-id="8410c-168">Der Gleichheits Vergleich für `Double` Werte kann aufgrund von Rundungs Effekten irreführend sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-168">Equality comparison for `Double` values may be misleading due to rounding effects.</span></span>
<span data-ttu-id="8410c-169">Beispielsweise `49.0 * (1.0/49.0) != 1.0`.</span><span class="sxs-lookup"><span data-stu-id="8410c-169">For instance, `49.0 * (1.0/49.0) != 1.0`.</span></span>

<span data-ttu-id="8410c-170">Bei zwei numerischen Ausdrücken können die binären Operatoren `>`, `<`, `>=`und `<=` verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der erste Ausdruck größer als, kleiner als, größer als oder gleich ist. oder kleiner oder gleich dem zweiten Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-170">Given any two numeric expressions, the binary operators `>`, `<`, `>=`, and `<=` may be used to construct a new Boolean expression that is true if the first expression is respectively greater than, less than, greater than or equal to, or less than or equal to the second expression.</span></span>

<span data-ttu-id="8410c-171">Bei zwei booleschen Ausdrücken können die `and` und `or` binäre Operatoren verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn die beiden Ausdrücke "true" sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-171">Given any two Boolean expressions, the `and` and `or` binary operators may be used to construct a new Boolean expression that is true if both of (resp. either or both of) the two expressions are true.</span></span>

<span data-ttu-id="8410c-172">Bei jedem booleschen Ausdruck kann der `not` unäre Operator verwendet werden, um einen neuen booleschen Ausdruck zu erstellen, der true ist, wenn der konstituierende Ausdruck false ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-172">Given any Boolean expression, the `not` unary operator may be used to construct a new Boolean expression that is true if the constituent expression is false.</span></span>

## <a name="string-expressions"></a><span data-ttu-id="8410c-173">Zeichen folgen Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-173">String Expressions</span></span>

<span data-ttu-id="8410c-174">Q # ermöglicht die Verwendung von Zeichen folgen in der `fail`-Anweisung und der `Log`-Standardfunktion.</span><span class="sxs-lookup"><span data-stu-id="8410c-174">Q# allows strings to be used in the `fail` statement and the `Log` standard function.</span></span>

<span data-ttu-id="8410c-175">Zeichen folgen in Q # sind entweder Literale oder interpoliert Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="8410c-175">Strings in Q# are either literals or interpolated strings.</span></span>
<span data-ttu-id="8410c-176">Zeichen folgen Literale ähneln in den meisten Sprachen einfachen Zeichenfolgenliteralen: eine Sequenz von Unicode-Zeichen, die in doppelten Anführungszeichen eingeschlossen sind, `"`.</span><span class="sxs-lookup"><span data-stu-id="8410c-176">String literals are similar to simple string literals in most languages: a sequence of Unicode characters enclosed in double quotes, `"`.</span></span>
<span data-ttu-id="8410c-177">Innerhalb einer Zeichenfolge kann der umgekehrte Schrägstrich `\` verwendet werden, um ein doppeltes Anführungszeichen zu versehen und eine neue Zeile als `\n`einzufügen, ein Wagen Rücklauf als `\r`und eine Registerkarte als `\t`.</span><span class="sxs-lookup"><span data-stu-id="8410c-177">Inside of a string, the back-slash character `\` may be used to escape a double quote character, and to insert a new-line as `\n`, a carriage return as `\r`, and a tab as `\t`.</span></span>
<span data-ttu-id="8410c-178">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8410c-178">For instance:</span></span>

```qsharp
"\"Hello world!\", she said.\n"
```

<span data-ttu-id="8410c-179">Die Q #-Syntax für Zeichen folgen Interpolationen ist eine Teilmenge C# der 7,0-Syntax. Q # unterstützt keine ausführlichen (mehrzeiligen) interpoliert Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="8410c-179">The Q# syntax for string interpolations is a subset of the C# 7.0 syntax; Q# does not support verbatim (multi-line) interpolated strings.</span></span>
<span data-ttu-id="8410c-180">Informationen zur Syntax finden Sie unter C# [*interpoliert*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) .</span><span class="sxs-lookup"><span data-stu-id="8410c-180">See [*Interpolated Strings*](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/interpolated-strings) for the C# syntax.</span></span>

<span data-ttu-id="8410c-181">Ausdrücke in einer interinterierten Zeichenfolge Folgen der Q #- C# Syntax, nicht der Syntax.</span><span class="sxs-lookup"><span data-stu-id="8410c-181">Expressions inside of an interpolated string follow Q# syntax, not C# syntax.</span></span>
<span data-ttu-id="8410c-182">Jeder gültige Q #-Ausdruck kann in einer interinterierten Zeichenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-182">Any valid Q# expression may appear in an interpolated string.</span></span>

## <a name="qubit-expressions"></a><span data-ttu-id="8410c-183">Qubit-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-183">Qubit Expressions</span></span>

<span data-ttu-id="8410c-184">Die einzigen `Qubit` Ausdrücke sind Symbole, die an `Qubit` Werte oder Array Elemente `Qubit` Arrays gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-184">The only `Qubit` expressions are symbols that are bound to `Qubit` values or array elements of `Qubit` arrays.</span></span>
<span data-ttu-id="8410c-185">Es sind keine `Qubit` Literale vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8410c-185">There are no `Qubit` literals.</span></span>

## <a name="pauli-expressions"></a><span data-ttu-id="8410c-186">Pauli-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-186">Pauli Expressions</span></span>

<span data-ttu-id="8410c-187">Die vier `Pauli` Werte `PauliI`, `PauliX`, `PauliY`und `PauliZ`sind alle gültigen `Pauli` Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="8410c-187">The four `Pauli` values, `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, are all valid `Pauli` expressions.</span></span>

<span data-ttu-id="8410c-188">Abgesehen davon sind die einzigen `Pauli` Ausdrücke Symbole, die an `Pauli` Werte oder Array Elemente `Pauli` Arrays gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-188">Other than that, the only `Pauli` expressions are symbols that are bound to `Pauli` values or array elements of `Pauli` arrays.</span></span>

## <a name="result-expressions"></a><span data-ttu-id="8410c-189">Ergebnis Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-189">Result Expressions</span></span>

<span data-ttu-id="8410c-190">Die beiden `Result` Werte `One` und `Zero`sind gültige `Result` Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="8410c-190">The two `Result` values, `One` and `Zero`, are valid `Result` expressions.</span></span>

<span data-ttu-id="8410c-191">Abgesehen davon sind die einzigen `Result` Ausdrücke Symbole, die an `Result` Werte oder Array Elemente `Result` Arrays gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-191">Other than that, the only `Result` expressions are symbols that are bound to `Result` values or array elements of `Result` arrays.</span></span>
<span data-ttu-id="8410c-192">Beachten Sie insbesondere, dass `One` nicht mit der ganzzahligen `1`identisch ist, und es gibt keine direkte Konvertierung zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="8410c-192">In particular, note that `One` is not the same as the integer `1`, and there is no direct conversion between them.</span></span>
<span data-ttu-id="8410c-193">Das gleiche gilt für `Zero` und `0`.</span><span class="sxs-lookup"><span data-stu-id="8410c-193">The same is true for `Zero` and `0`.</span></span>

## <a name="range-expressions"></a><span data-ttu-id="8410c-194">Bereichs Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-194">Range Expressions</span></span>

<span data-ttu-id="8410c-195">Bei allen drei `Int` Ausdrücken `start`, `step`und `stop`ist `start .. step .. stop` ein Bereichs Ausdruck, dessen erstes Element `start`ist, das zweite Element `start+step`ist, das dritte Element `start+step+step`ist usw., bis `stop` übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-195">Given any three `Int` expressions `start`, `step`, and `stop`, `start .. step .. stop` is a range expression whose first element is `start`, second element is `start+step`, third element is `start+step+step`, etc., until `stop` is passed.</span></span>
<span data-ttu-id="8410c-196">Ein Bereich kann leer sein, wenn `step` beispielsweise positiv und `stop < start`ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-196">A range may be empty if, for instance, `step` is positive and `stop < start`.</span></span>
<span data-ttu-id="8410c-197">Das letzte Element des Bereichs wird `stop`, wenn der Unterschied zwischen `start` und `stop` ein ganzzahliges Vielfaches von `step`ist. Das heißt, der Bereich ist an beiden Enden inklusiv.</span><span class="sxs-lookup"><span data-stu-id="8410c-197">The last element of the range will be `stop` if the difference between `start` and `stop` is an integral multiple of `step`; that is, the range is inclusive at both ends.</span></span>

<span data-ttu-id="8410c-198">Bei zwei `Int` Ausdrücken `start` und `stop`ist `start .. stop` ein Bereichs Ausdruck, der `start .. 1 .. stop`entspricht.</span><span class="sxs-lookup"><span data-stu-id="8410c-198">Given any two `Int` expressions `start` and `stop`, `start .. stop` is a range expression that is equal to `start .. 1 .. stop`.</span></span>
<span data-ttu-id="8410c-199">Beachten Sie, dass der implizierte `step` gleich + 1 ist, auch wenn `stop` kleiner als `start`ist. in einem solchen Fall ist der Bereich leer.</span><span class="sxs-lookup"><span data-stu-id="8410c-199">Note that the implied `step` is +1 even if `stop` is less than `start`; in such a case, the range is empty.</span></span>

<span data-ttu-id="8410c-200">Einige Beispiel Bereiche sind:</span><span class="sxs-lookup"><span data-stu-id="8410c-200">Some example ranges are:</span></span>

- <span data-ttu-id="8410c-201">`1..3` ist der Bereich von 1, 2, 3.</span><span class="sxs-lookup"><span data-stu-id="8410c-201">`1..3` is the range 1, 2, 3.</span></span>
- <span data-ttu-id="8410c-202">`2..2..5` ist der Bereich von 2, 4.</span><span class="sxs-lookup"><span data-stu-id="8410c-202">`2..2..5` is the range 2, 4.</span></span>
- <span data-ttu-id="8410c-203">`2..2..6` ist der Bereich von 2, 4, 6.</span><span class="sxs-lookup"><span data-stu-id="8410c-203">`2..2..6` is the range 2, 4, 6.</span></span>
- <span data-ttu-id="8410c-204">`6..-2..2` ist der Bereich 6, 4, 2.</span><span class="sxs-lookup"><span data-stu-id="8410c-204">`6..-2..2` is the range 6, 4, 2.</span></span>
- <span data-ttu-id="8410c-205">`2..1` ist der leere Bereich.</span><span class="sxs-lookup"><span data-stu-id="8410c-205">`2..1` is the empty range.</span></span>
- <span data-ttu-id="8410c-206">`2..6..7` ist der Bereich 2.</span><span class="sxs-lookup"><span data-stu-id="8410c-206">`2..6..7` is the range 2.</span></span>
- <span data-ttu-id="8410c-207">`2..2..1` ist der leere Bereich.</span><span class="sxs-lookup"><span data-stu-id="8410c-207">`2..2..1` is the empty range.</span></span>
- <span data-ttu-id="8410c-208">`1..-1..2` ist der leere Bereich.</span><span class="sxs-lookup"><span data-stu-id="8410c-208">`1..-1..2` is the empty range.</span></span>

## <a name="callable-expressions"></a><span data-ttu-id="8410c-209">Aufruf Bare Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-209">Callable Expressions</span></span>

<span data-ttu-id="8410c-210">Ein Aufruf bares Literalelement ist der Name eines Vorgangs oder einer Funktion, der im Kompilierungs Bereich definiert ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-210">A callable literal is the name of an operation or function defined in the compilation scope.</span></span>
<span data-ttu-id="8410c-211">Beispielsweise ist `X` ein vorgangsliteral, das auf den `X` Vorgang der Standardbibliothek verweist, und `Message` ist ein Funktionsliteral, das auf die `Message` Funktion der Standardbibliothek verweist.</span><span class="sxs-lookup"><span data-stu-id="8410c-211">For instance, `X` is an operation literal that refers to the standard library `X` operation, and `Message` is a function literal that refers to the standard library `Message` function.</span></span>

<span data-ttu-id="8410c-212">Wenn ein Vorgang das `Adjoint`-Funktor unterstützt, ist `Adjoint op` ein Vorgangs Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-212">If an operation supports the `Adjoint` functor, then `Adjoint op` is an operation expression.</span></span>
<span data-ttu-id="8410c-213">Wenn der Vorgang das `Controlled`-Funktor unterstützt, ist `Controlled op` ein Vorgangs Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-213">Similarly, if the operation supports the `Controlled` functor, then `Controlled op` is an operation expression.</span></span>
<span data-ttu-id="8410c-214">Die Typen dieser Ausdrücke werden in den [Funktoren](xref:microsoft.quantum.language.type-model#functors)angegeben.</span><span class="sxs-lookup"><span data-stu-id="8410c-214">The types of these expressions are specified in [Functors](xref:microsoft.quantum.language.type-model#functors).</span></span>

<span data-ttu-id="8410c-215">Funktoren (`Adjoint` und `Controlled`) werden genauer gebunden als alle anderen Operatoren, mit Ausnahme des Unwrap-Operators `!` und der Array Indizierung mit `[]`.</span><span class="sxs-lookup"><span data-stu-id="8410c-215">Functors (`Adjoint` and `Controlled`) bind more closely than all other operators, except for the unwrap operator `!` and array indexing with `[]`.</span></span>
<span data-ttu-id="8410c-216">Folglich sind die folgenden Vorgänge zulässig, vorausgesetzt, dass die Vorgänge die verwendeten Funktoren unterstützen:</span><span class="sxs-lookup"><span data-stu-id="8410c-216">Thus, the following are all legal, assuming that the operations support the functors used:</span></span>

```qsharp
Adjoint Op(qs)
Controlled Op(controls, targets)
Controlled Adjoint Op(controls, targets)
Adjoint WrappedOp!(qs)
```

<span data-ttu-id="8410c-217">Ein Aufruf bares Literale kann als Wert verwendet werden, z. b. um einer Variablen zuzuweisen oder um Sie an eine andere Aufruf Bare zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="8410c-217">A callable literal may be used as a value, say to assign to a variable or to pass to another callable.</span></span>
<span data-ttu-id="8410c-218">In diesem Fall müssen Sie, wenn die Aufruf Bare Typparameter aufweist, als Teil des Aufruf baren Werts angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-218">In this case, if the callable has type parameters, they must be provided as part of the callable value.</span></span>
<span data-ttu-id="8410c-219">Ein Aufruf barer Wert darf keine nicht angegebenen Typparameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8410c-219">A callable value cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="8410c-220">Wenn `Fun` beispielsweise eine Funktion mit Signatur `'T1->Unit`ist:</span><span class="sxs-lookup"><span data-stu-id="8410c-220">For instance, if `Fun` is a function with signature `'T1->Unit`:</span></span>

```qsharp
let f = Fun<Int>;            // f is Int->Unit.
SomeOtherFun(Fun<Double>);   // A Double->Unit is passed to SomOtherFun.
let g = Fun;                 // This causes a compilation error.
SomeOtherFun(Fun);           // This also causes a compilation error.
```

## <a name="callable-invocation-expressions"></a><span data-ttu-id="8410c-221">Aufruf Bare Aufruf Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-221">Callable Invocation Expressions</span></span>

<span data-ttu-id="8410c-222">Bei einem Aufruf baren Ausdruck (Operation oder Funktion) und einem Tupelausdruck des Eingabetyps der Aufruf baren Signatur kann ein Aufruf Ausdruck gebildet werden, indem der Tupelausdruck an den Aufruf baren Ausdruck angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-222">Given a callable (operation or function) expression and a tuple expression of the input type of the callable's signature, an invocation expression may be formed by appending the tuple expression to the callable expression.</span></span>
<span data-ttu-id="8410c-223">Der Typ des Aufruf Ausdrucks ist der Ausgabetyp der Signatur des Callable-Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="8410c-223">The type of the invocation expression is the output type of the callable's signature.</span></span>

<span data-ttu-id="8410c-224">Wenn `Op` z. b. ein Vorgang mit Signatur `((Int, Qubit) => Double)`ist, `Op(3, qubit1)` ein Ausdruck vom Typ `Double`ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-224">For example, if `Op` is an operation with signature `((Int, Qubit) => Double)`, `Op(3, qubit1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="8410c-225">Ebenso gilt, wenn `Sin` eine Funktion mit Signatur `(Double -> Double)`ist, `Sin(0.1)` ein Ausdruck vom Typ `Double`ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-225">Similarly, if `Sin` is a function with signature `(Double -> Double)`, `Sin(0.1)` is an expression of type `Double`.</span></span>
<span data-ttu-id="8410c-226">Wenn `Builder` eine Funktion mit Signatur `(Int -> (Int -> Int))`ist, dann ist `Builder(3)` eine Funktion von bis zu int.</span><span class="sxs-lookup"><span data-stu-id="8410c-226">Finally, if `Builder` is a function with signature `(Int -> (Int -> Int))`, then `Builder(3)` is a function from Into to Int.</span></span>

<span data-ttu-id="8410c-227">Zum Aufrufen des Ergebnisses eines Aufruf baren Ausdrucks ist ein zusätzliches Paar von Klammern um den Aufruf baren Ausdruck erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8410c-227">Invoking the result of a callable-valued expression requires an extra pair of parentheses around the callable expression.</span></span>
<span data-ttu-id="8410c-228">Um also das Ergebnis des Aufrufs von `Builder` aus dem vorherigen Absatz aufzurufen, lautet die korrekte Syntax:</span><span class="sxs-lookup"><span data-stu-id="8410c-228">Thus, to invoke the result of calling `Builder` from the previous paragraph, the correct syntax is:</span></span>

```qsharp
(Builder(3))(2)
```

<span data-ttu-id="8410c-229">Beim Aufrufen einer typparametrisierten Aufruf baren kann der tatsächliche Typparameter in spitzen Klammern `<` und nach dem Aufruf baren Ausdruck `>` werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-229">When invoking a type-parameterized callable, the actual type parameters may be specified within angle brackets `<` and `>` after the callable expression.</span></span>
<span data-ttu-id="8410c-230">Dies ist in der Regel unnötig, da der Q #-Compiler die eigentlichen Typen ableiten wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-230">This is usually unnecessary as the Q# compiler will infer the actual types.</span></span>
<span data-ttu-id="8410c-231">Dies ist für die partielle Anwendung erforderlich (siehe unten), wenn ein typparametrisiertes Argument nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-231">It is required for partial application (see below) if a type-parameterized argument is left unspecified.</span></span>
<span data-ttu-id="8410c-232">Dies ist manchmal auch nützlich, wenn die Übergabe von Vorgängen mit unterschiedlichen Funktoren unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-232">It is also sometimes useful when passing operations with different functor supports to a callable.</span></span>

<span data-ttu-id="8410c-233">Wenn `Func` beispielsweise über eine Signatur `('T1, 'T2, 'T1) -> 'T2`verfügt, `Op1` und `Op2` Signatur `(Qubit[] => Unit is Adj)`aufweisen und `Op3` über eine Signatur `(Qubit[] => Unit)`verfügt, um `Func` als erstes Argument aufzurufen `Op1` mit `Op2` als erstes Argument als zweites und `Op3` als drittes:</span><span class="sxs-lookup"><span data-stu-id="8410c-233">For instance, if `Func` has signature `('T1, 'T2, 'T1) -> 'T2`, `Op1` and `Op2` have signature `(Qubit[] => Unit is Adj)`, and `Op3` has signature `(Qubit[] => Unit)`, to invoke `Func` with `Op1` as the first argument, `Op2` as the second, and `Op3` as the third:</span></span>

```qsharp
let combinedOp = Func<(Qubit[] => Unit), (Qubit[] => Unit is Adj)>(Op1, Op2, Op3);
```

<span data-ttu-id="8410c-234">Die Typspezifikation ist erforderlich, da `Op3` und `Op1` unterschiedliche Typen aufweisen, sodass der Compiler dies ohne Angabe der Spezifikation als mehrdeutig behandelt.</span><span class="sxs-lookup"><span data-stu-id="8410c-234">The type specification is required because `Op3` and `Op1` have different types, so the compiler will treat this as ambiguous without the specification.</span></span>

### <a name="partial-application"></a><span data-ttu-id="8410c-235">Partielle Anwendung</span><span class="sxs-lookup"><span data-stu-id="8410c-235">Partial Application</span></span>

<span data-ttu-id="8410c-236">Bei einem Aufruf baren Ausdruck kann ein neuer Aufruf barer Ausdruck erstellt werden, indem eine Teilmenge der Argumente für die Aufruf Bare bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-236">Given a callable expression, a new callable may be created by providing a subset of the arguments to the callable.</span></span>
<span data-ttu-id="8410c-237">Dies wird als _partielle Anwendung_bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8410c-237">This is called _partial application_.</span></span>

<span data-ttu-id="8410c-238">In f # wird eine teilweise angewendete Aufruf Bare-Datei durch Schreiben eines normalen Aufruf Ausdrucks ausgedrückt, wobei jedoch ein Unterstrich, `_`, für die nicht angegebenen Argumente verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-238">In Q#, a partially applied callable is expressed by writing a normal invocation expression, but using an underscore, `_`, for the unspecified arguments.</span></span>
<span data-ttu-id="8410c-239">Die sich ergebende Aufruf Bare hat denselben Ergebnistyp wie die basiscallable und die gleichen Spezialisierungs Vorgänge für Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="8410c-239">The resulting callable has the same result type as the base callable, and the same specializations for operations.</span></span>
<span data-ttu-id="8410c-240">Der Eingabetyp der partiellen Anwendung ist einfach der ursprüngliche Typ mit den angegebenen Argumenten.</span><span class="sxs-lookup"><span data-stu-id="8410c-240">The input type of the partial application is simply the original type with the specified arguments removed.</span></span>

<span data-ttu-id="8410c-241">Wenn beim Erstellen einer partiellen Anwendung eine änderbare Variable als angegebenes Argument angegeben wird, wird der aktuelle Wert der Variablen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8410c-241">If a mutable variable is passed as a specified argument when creating a partial application, the current value of the variable is used.</span></span>
<span data-ttu-id="8410c-242">Wenn Sie den Wert der Variablen anschließend ändern, wirkt sich dies nicht auf die partielle Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="8410c-242">Changing the value of the variable afterward will not impact the partial application.</span></span>

<span data-ttu-id="8410c-243">Wenn `Op` z. b. den Typ `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`hat:</span><span class="sxs-lookup"><span data-stu-id="8410c-243">For example, if `Op` has type `((Int, ((Qubit, Qubit), Double)) => Unit is Adj)`:</span></span>

- <span data-ttu-id="8410c-244">`Op(5,(_,_))` hat den Typ `(((Qubit,Qubit), Double) => Unit is Adj)`und `Op(5,_)`.</span><span class="sxs-lookup"><span data-stu-id="8410c-244">`Op(5,(_,_))` has type `(((Qubit,Qubit), Double) => Unit is Adj)`, and so has `Op(5,_)`.</span></span>
- <span data-ttu-id="8410c-245">`Op(_,(_,1.0))` hat den Typ `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="8410c-245">`Op(_,(_,1.0))` has type `((Int, (Qubit,Qubit)) => Unit is Adj)`.</span></span>
- <span data-ttu-id="8410c-246">`Op(_,((q1,q2),_))` hat den Typ `((Int,Double) => Unit is Adj)`.</span><span class="sxs-lookup"><span data-stu-id="8410c-246">`Op(_,((q1,q2),_))` has type `((Int,Double) => Unit is Adj)`.</span></span>
   <span data-ttu-id="8410c-247">Beachten Sie, dass hier eine Singleton-tupeläquivalenz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8410c-247">Note that we have applied singleton tuple equivalence here.</span></span>

<span data-ttu-id="8410c-248">Wenn das teilweise angewendete Aufruf Bare Typparameter aufweist, die vom Compiler nicht abgeleitet werden können, müssen Sie auf der Aufruf Site bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-248">If the partially-applied callable has type parameters that cannot be inferred by the compiler, they must be provided at the invocation site.</span></span>
<span data-ttu-id="8410c-249">Die partielle Anwendung darf keine nicht angegebenen Typparameter aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8410c-249">The partial application cannot have any unspecified type parameters.</span></span>

<span data-ttu-id="8410c-250">Wenn `Op` z. b. den Typ `(('T1, Qubit, 'T1) => Unit : Adjoint)`hat:</span><span class="sxs-lookup"><span data-stu-id="8410c-250">For example, if `Op` has type `(('T1, Qubit, 'T1) => Unit : Adjoint)`:</span></span>

```qsharp
let f1 = Op<Int>(_, qb, _); // f1 has type ((Int,Int) => Unit is Adj)
let f2 = Op(5, qb, _);      // f2 has type (Int => Unit is Adj)
let f3 = Op(_,qb, _);       // f3 generates a compilation error
```

### <a name="recursion"></a><span data-ttu-id="8410c-251">Rekursion</span><span class="sxs-lookup"><span data-stu-id="8410c-251">Recursion</span></span>

<span data-ttu-id="8410c-252">F #-callables dürfen direkt oder indirekt rekursiv sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-252">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="8410c-253">Das heißt, ein Vorgang oder eine Funktion kann sich selbst aufrufen, oder es kann eine andere Aufruf Bare aufgerufen werden, die den Aufruf baren Vorgang direkt oder indirekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="8410c-253">That is, an operation or function may call itself, or it may call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="8410c-254">Es gibt jedoch zwei wichtige Kommentare zur Verwendung der Rekursion:</span><span class="sxs-lookup"><span data-stu-id="8410c-254">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="8410c-255">Die Verwendung von Rekursion bei Vorgängen beeinträchtigt wahrscheinlich bestimmte Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="8410c-255">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="8410c-256">Dies kann erhebliche Auswirkungen auf die Ausführungszeit des Algorithmus haben.</span><span class="sxs-lookup"><span data-stu-id="8410c-256">This may have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="8410c-257">Bei der Ausführung auf einem eigentlichen Quantum-Gerät kann der Stapel Speicher eingeschränkt sein, sodass die Tiefe Rekursion zu einem Laufzeitfehler führen kann.</span><span class="sxs-lookup"><span data-stu-id="8410c-257">When executing on an actual quantum device, stack space may be limited, and so deep recursion may lead to a runtime error.</span></span>
  <span data-ttu-id="8410c-258">Insbesondere der Q #-Compiler und die Common Language Runtime erkennen und optimieren die Endrekursion nicht.</span><span class="sxs-lookup"><span data-stu-id="8410c-258">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="tuple-expressions"></a><span data-ttu-id="8410c-259">Tupelausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-259">Tuple Expressions</span></span>

<span data-ttu-id="8410c-260">Ein tupelliteral ist eine Sequenz von Element Ausdrücken des entsprechenden Typs, die durch Kommas getrennt sind und in `(` und `)`eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-260">A tuple literal is a sequence of element expressions of the appropriate type, separated by commas, enclosed in `(` and `)`.</span></span>
<span data-ttu-id="8410c-261">Beispielsweise ist `(1, One)` ein `(Int, Result)` Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-261">For instance, `(1, One)` is an `(Int, Result)` expression.</span></span>

<span data-ttu-id="8410c-262">Abgesehen von Literalen sind die einzigen Tupelausdrücke Symbole, die an Tupelwerte, Array Elemente von tupelarrays und Aufruf Bare Aufrufe gebunden sind, die Tupel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8410c-262">Other than literals, the only tuple expressions are symbols that are bound to tuple values, array elements of tuple arrays, and callable invocations that return tuples.</span></span>

## <a name="user-defined-type-expressions"></a><span data-ttu-id="8410c-263">Benutzerdefinierte typausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-263">User-Defined Type Expressions</span></span>

<span data-ttu-id="8410c-264">Ein Literalwert eines benutzerdefinierten Typs besteht aus dem Typnamen, gefolgt von einem tupelliteraltyp mit dem basistupeltyp des Typs.</span><span class="sxs-lookup"><span data-stu-id="8410c-264">A literal of a user-defined type consists of the type name followed by a tuple literal of the type’s base tuple type.</span></span>
<span data-ttu-id="8410c-265">Wenn `IntPair` beispielsweise ein benutzerdefinierter Typ ist, der auf `(Int, Int)`basiert, wäre `IntPair(2,3)` ein gültiges Literale dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="8410c-265">For instance, if `IntPair` is a user-defined type based on `(Int, Int)`, then `IntPair(2,3)` would be a valid literal of that type.</span></span>

<span data-ttu-id="8410c-266">Anders als Literale sind die einzigen Ausdrücke eines benutzerdefinierten Typs Symbole, die an Werte dieses Typs gebunden sind, Array Elemente von Arrays dieses Typs und Aufruf Bare Aufrufe, die diesen Typ zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8410c-266">Other than literals, the only expressions of a user-defined type are symbols that are bound to values of that type, array elements of arrays of that type, and callable invocations that return that type.</span></span>

## <a name="unwrap-expressions"></a><span data-ttu-id="8410c-267">Entpacken von Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="8410c-267">Unwrap Expressions</span></span>

<span data-ttu-id="8410c-268">In Q # ist der Unwrap-Operator ein nach gestelltes Ausrufezeichen `!`.</span><span class="sxs-lookup"><span data-stu-id="8410c-268">In Q#, the unwrap operator is a trailing exclamation mark `!`.</span></span>
<span data-ttu-id="8410c-269">Wenn `IntPair` beispielsweise einen benutzerdefinierten Typ mit dem zugrunde liegenden Typ `(Int, Int)`und `s` eine Variable mit einem Wert `IntPair(2,3)`war, dann `s!` `(2,3)`.</span><span class="sxs-lookup"><span data-stu-id="8410c-269">For instance, if `IntPair` is a user-defined type with underlying type `(Int, Int)`, and `s` was a variable with value `IntPair(2,3)`, then `s!` would be `(2,3)`.</span></span>

<span data-ttu-id="8410c-270">Für benutzerdefinierte Typen, die in Bezug auf andere benutzerdefinierte Typen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-270">For user-defined types defined in terms of other user-defined types.</span></span> <span data-ttu-id="8410c-271">der Unwrap-Operator kann wiederholt werden. Beispielsweise gibt `s!!` den doppelt entpackten Wert `s`an.</span><span class="sxs-lookup"><span data-stu-id="8410c-271">the unwrap operator may be repeated; for instance, `s!!` indicates the doubly-unwrapped value of `s`.</span></span>
<span data-ttu-id="8410c-272">Wenn `WrappedPair` ein benutzerdefinierter Typ mit dem zugrunde liegenden Typ `IntPair`ist und `t` eine Variable mit einem Wert `WrappedPair(IntPair(1,2))`ist, dann wird `t!!` `(1,2)`.</span><span class="sxs-lookup"><span data-stu-id="8410c-272">Thus, if `WrappedPair` is a user-defined type with underlying type `IntPair`, and `t` is a variable with value `WrappedPair(IntPair(1,2))`, then `t!!` would be `(1,2)`.</span></span>

<span data-ttu-id="8410c-273">Der `!` Operator hat eine höhere Rangfolge als alle anderen Operatoren als `[]` für die Array Indizierung und die Slicing.</span><span class="sxs-lookup"><span data-stu-id="8410c-273">The `!` operator has higher precedence than all other operators other than `[]` for array indexing and slicing.</span></span>
<span data-ttu-id="8410c-274">`!` und `[]` Bindung Positions bedingt; Das heißt, `a[i]![3]` als `((a[i])!)[3]`gelesen werden sollen: nehmen Sie das `i`"th-Element `a`, entpacken Sie es, und holen Sie dann das dritte Element des entpackten Werts (der ein Array sein muss).</span><span class="sxs-lookup"><span data-stu-id="8410c-274">`!` and `[]` bind positionally; that is, `a[i]![3]` should be read as `((a[i])!)[3]`: take the `i`'th element of `a`, unwrap it, and then get the 3rd element of the unwrapped value (which must be an array).</span></span>

<span data-ttu-id="8410c-275">Die Rangfolge des `!` Operators hat eine Beeinträchtigung, die möglicherweise nicht offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-275">The precedence of the `!` operator has one impact that might not be obvious.</span></span>
<span data-ttu-id="8410c-276">Wenn eine Funktion oder ein Vorgang einen Wert zurückgibt, der dann entpackt wird, muss der Funktions-oder Vorgangs Ausdruck in Klammern eingeschlossen werden, damit das Argument Tupel an den-Ausdruck gebunden wird, anstatt an den Unwrap-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8410c-276">If a function or operation returns a value that then gets unwrapped, the function or operation call must be enclosed in parentheses so that the argument tuple binds to the call rather than to the unwrap.</span></span>
<span data-ttu-id="8410c-277">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8410c-277">For example:</span></span>

```qsharp
let f = (Foo(arg))!;    // Calls Foo(arg), then unwraps the result
let g = Foo(arg)!;      // Syntax error
```

## <a name="array-expressions"></a><span data-ttu-id="8410c-278">Array Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-278">Array Expressions</span></span>

<span data-ttu-id="8410c-279">Ein Arrayliteral ist eine Sequenz von einem oder mehreren Element Ausdrücken, die durch Kommas getrennt sind und in `[` und `]`eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-279">An array literal is a sequence of one or more element expressions, separated by commas, enclosed in `[` and `]`.</span></span>
<span data-ttu-id="8410c-280">Alle-Elemente müssen mit demselben Typ kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-280">All elements must be compatible with the same type.</span></span>

<span data-ttu-id="8410c-281">Wenn der allgemeine Elementtyp ein Vorgang oder Funktionstyp ist, müssen alle Elemente die gleichen Eingabe-und Ausgabetypen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8410c-281">If the common element type is an operation or function type, all of the elements must have the same input and output types.</span></span>
<span data-ttu-id="8410c-282">Der Elementtyp des Arrays unterstützt alle Funktoren, die von allen Elementen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-282">The element type of the array will support any functors that are supported by all of the elements.</span></span>
<span data-ttu-id="8410c-283">Wenn z. b. `Op1`, `Op2`und `Op3` alle `Qubit[] => Unit`sind, `Op1` aber `Adjoint`unterstützt, unterstützt `Op2` `Controlled`, und `Op3` unterstützt beides:</span><span class="sxs-lookup"><span data-stu-id="8410c-283">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[] => Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="8410c-284">`[Op1, Op2]` ist ein Array von `(Qubit[] => Unit)` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="8410c-284">`[Op1, Op2]` is an array of `(Qubit[] => Unit)` operations.</span></span>
- <span data-ttu-id="8410c-285">`[Op1, Op3]` ist ein Array von `(Qubit[] => Unit is Adj)` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="8410c-285">`[Op1, Op3]` is an array of `(Qubit[] => Unit is Adj)` operations.</span></span>
- <span data-ttu-id="8410c-286">`[Op2, Op3]` ist ein Array von `(Qubit[] => Unit is Ctl)` Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="8410c-286">`[Op2, Op3]` is an array of `(Qubit[] => Unit is Ctl)` operations.</span></span>

<span data-ttu-id="8410c-287">Leere Array Literale, `[]`, sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="8410c-287">Empty array literals, `[]`, are not allowed.</span></span>
<span data-ttu-id="8410c-288">Verwenden Sie stattdessen `new ★[0]`, bei dem `★` als Platzhalter für einen geeigneten Typ dient, das Erstellen des gewünschten Arrays der Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8410c-288">Instead using `new ★[0]`, where `★` is as placeholder for a suitable type, allows to create the desired array of length zero.</span></span>

<span data-ttu-id="8410c-289">Bei zwei Arrays desselben Typs kann der binäre `+`-Operator verwendet werden, um ein neues Array zu bilden, bei dem es sich um die Verkettung der beiden Arrays handelt.</span><span class="sxs-lookup"><span data-stu-id="8410c-289">Given two arrays of the same type, the binary `+` operator may be used to form a new array that is the concatenation of the two arrays.</span></span>
<span data-ttu-id="8410c-290">Beispielsweise ist `[1,2,3] + [4,5,6]` `[1,2,3,4,5,6]`.</span><span class="sxs-lookup"><span data-stu-id="8410c-290">For instance, `[1,2,3] + [4,5,6]` is `[1,2,3,4,5,6]`.</span></span>

### <a name="array-creation"></a><span data-ttu-id="8410c-291">Array Erstellung</span><span class="sxs-lookup"><span data-stu-id="8410c-291">Array Creation</span></span>

<span data-ttu-id="8410c-292">Wenn ein Typ und ein `Int` Ausdruck verwendet werden, kann der `new` Operator verwendet werden, um ein neues Array mit der angegebenen Größe zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8410c-292">Given a type and an `Int` expression, the `new` operator may be used to allocate a new array of the given size.</span></span>
<span data-ttu-id="8410c-293">Beispielsweise wird `new Int[i+1]` ein neues `Int` Array mit `i+1` Elementen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="8410c-293">For instance, `new Int[i+1]` would allocate a new `Int` array with `i+1` elements.</span></span>

<span data-ttu-id="8410c-294">Die Elemente eines neuen Arrays werden mit einem typabhängigen Standardwert initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8410c-294">The elements of a new array are initialized to a type-dependent default value.</span></span>
<span data-ttu-id="8410c-295">In den meisten Fällen ist dies eine Variation von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8410c-295">In most cases this is some variation of zero.</span></span>

<span data-ttu-id="8410c-296">Bei Qubits und callables, bei denen es sich um Verweise auf Entitäten handelt, gibt es keinen angemessenen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="8410c-296">For qubits and callables, which are references to entities, there is no reasonable default value.</span></span>
<span data-ttu-id="8410c-297">Daher ist für diese Typen der Standardwert ein ungültiger Verweis, der nicht verwendet werden kann, ohne dass ein Laufzeitfehler verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-297">Thus, for these types, the default is an invalid reference that cannot be used without causing a runtime error.</span></span>
<span data-ttu-id="8410c-298">Dies ähnelt einem NULL-Verweis in Sprachen wie C# oder Java.</span><span class="sxs-lookup"><span data-stu-id="8410c-298">This is similar to a null reference in languages such as C# or Java.</span></span>
<span data-ttu-id="8410c-299">Arrays, die Qubits oder callables enthalten, müssen ordnungsgemäß mit nicht standardmäßigen Werten initialisiert werden, bevor ihre Elemente problemlos verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8410c-299">Arrays containing qubits or callables must be properly initialized with non-default values before their elements may be safely used.</span></span> <span data-ttu-id="8410c-300">Geeignete Initialisierungs Routinen finden Sie in <xref:microsoft.quantum.arrays>.</span><span class="sxs-lookup"><span data-stu-id="8410c-300">Suitable initialization routines can be found in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="8410c-301">Die Standardwerte für jeden Typ lauten:</span><span class="sxs-lookup"><span data-stu-id="8410c-301">The default values for each type are:</span></span>

<span data-ttu-id="8410c-302">type</span><span class="sxs-lookup"><span data-stu-id="8410c-302">Type</span></span> | <span data-ttu-id="8410c-303">Standard</span><span class="sxs-lookup"><span data-stu-id="8410c-303">Default</span></span>
---------|----------
 `Int` | `0`
 `BigInt` | `0L`
 `Double` | `0.0`
 `Bool` | `false`
 `String` | `""`
 `Qubit` | <span data-ttu-id="8410c-304">_Ungültiges Qubit_</span><span class="sxs-lookup"><span data-stu-id="8410c-304">_invalid qubit_</span></span>
 `Pauli` | `PauliI`
 `Result` | `Zero`
 `Range` | <span data-ttu-id="8410c-305">Der leere Bereich, `1..1..0`</span><span class="sxs-lookup"><span data-stu-id="8410c-305">The empty range, `1..1..0`</span></span>
 `Callable` | <span data-ttu-id="8410c-306">_Ungültige Aufruf Bare_</span><span class="sxs-lookup"><span data-stu-id="8410c-306">_invalid callable_</span></span>
 `Array['T]` | `'T[0]`

<span data-ttu-id="8410c-307">Tupeltypen werden Element für Element initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8410c-307">Tuple types are initialized element-by-element.</span></span>


### <a name="jagged-arrays"></a><span data-ttu-id="8410c-308">Verzweigte Arrays</span><span class="sxs-lookup"><span data-stu-id="8410c-308">Jagged Arrays</span></span>

<span data-ttu-id="8410c-309">Eine Jagged Array, manchmal auch als "Array von Arrays" bezeichnet, ist ein Array, dessen Elemente Arrays sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-309">A jagged array, sometimes called an "array of arrays", is an array whose elements are arrays.</span></span> <span data-ttu-id="8410c-310">Die Elemente einer Jagged Array können unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-310">The elements of a jagged array can be of different sizes.</span></span> <span data-ttu-id="8410c-311">Im folgenden Beispiel wird gezeigt, wie Sie eine Jagged Array deklarieren und initialisieren, die eine Multiplikationstabelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="8410c-311">The following example shows how to declare and initialize a jagged array representing a multiplication table.</span></span>

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


### <a name="array-slices"></a><span data-ttu-id="8410c-312">Array Slices</span><span class="sxs-lookup"><span data-stu-id="8410c-312">Array Slices</span></span>

<span data-ttu-id="8410c-313">Wenn ein Array Ausdruck und ein `Range` Ausdruck vorliegen, kann ein neuer Ausdruck mithilfe des `[`-und `]` Array Slice-Operators gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-313">Given an array expression and a `Range` expression, a new expression may be formed using the `[` and `]` array slice operator.</span></span>
<span data-ttu-id="8410c-314">Der neue Ausdruck hat denselben Typ wie das Array und enthält die Array Elemente, die von den Elementen der `Range`indiziert werden, in der Reihenfolge, die vom `Range`definiert wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-314">The new expression will be the same type as the array and will contain the array items indexed by the elements of the `Range`, in the order defined by the `Range`.</span></span>
<span data-ttu-id="8410c-315">Wenn `a` beispielsweise an ein Array von `Double`s gebunden ist, ist `a[3..-1..0]` ein `Double[]` Ausdruck, der die ersten vier Elemente von `a` enthält, jedoch in umgekehrter Reihenfolge, wie Sie in `a`angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-315">For instance, if `a` is bound to an array of `Double`s, then `a[3..-1..0]` is a `Double[]` expression that contains the first four elements of `a` but in the reverse order as they appear in `a`.</span></span>

<span data-ttu-id="8410c-316">Wenn das `Range` leer ist, ist das resultierende Array in der Länge 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8410c-316">If the `Range` is empty, then the resulting array slice will be zero length.</span></span>

<span data-ttu-id="8410c-317">Wenn es sich bei dem Array Ausdruck nicht um einen einfachen Bezeichner handelt, muss er in Klammern eingeschlossen werden, damit er in einen Slice eingefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8410c-317">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to slice.</span></span>
<span data-ttu-id="8410c-318">Wenn beispielsweise `a` und `b` beide Arrays `Int`s sind, würde ein Slice aus der Verkettung wie folgt ausgedrückt werden:</span><span class="sxs-lookup"><span data-stu-id="8410c-318">For instance, if `a` and `b` are both arrays of `Int`s, a slice from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[1..2..7]
```

<span data-ttu-id="8410c-319">Alle Arrays in Q # sind NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="8410c-319">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="8410c-320">Das heißt, dass das erste Element eines Arrays `a` immer `a[0]`ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-320">That is, the first element of an array `a` is always `a[0]`.</span></span>

<span data-ttu-id="8410c-321">Ab unserer Version 0,8 unterstützen wir Kontext Ausdrücke für die Bereichs Aufteilung.</span><span class="sxs-lookup"><span data-stu-id="8410c-321">Starting with our 0.8 release, we support contextual expressions for range slicing.</span></span> <span data-ttu-id="8410c-322">Insbesondere können Bereichs Start-und Endwerte im Kontext eines Bereichs aufteilen-Ausdrucks weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-322">In particular, range start and end values may be omitted in the context of a range slicing expression.</span></span> <span data-ttu-id="8410c-323">In diesem Fall wendet der Compiler die folgenden Regeln an, um die vorgesehenen Trennzeichen für den Bereich abzuleiten.</span><span class="sxs-lookup"><span data-stu-id="8410c-323">In that case, the compiler will apply the following rules to infer the intended delimiters for the range.</span></span> 

<span data-ttu-id="8410c-324">Wenn z. b. der Bereichs Start Wert weggelassen wird, wird der abherleitet Startwert</span><span class="sxs-lookup"><span data-stu-id="8410c-324">For example, if the range start value is omitted, then the inferred start value</span></span> 
- <span data-ttu-id="8410c-325">ist 0 (null), wenn kein Schritt angegeben oder der angegebene Schritt positiv ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-325">is zero if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="8410c-326">die Länge des aufgeschnittenen Arrays minus 1, wenn der angegebene Schritt negativ ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-326">is the length of sliced array minus one if the specified step is negative.</span></span> 

<span data-ttu-id="8410c-327">Wenn der Wert für den Bereichs Endpunkt weggelassen wird, wird der abherende Endwert</span><span class="sxs-lookup"><span data-stu-id="8410c-327">If the range end value is omitted, then the inferred end value</span></span> 
- <span data-ttu-id="8410c-328">die Länge des aufgeschnittenen Arrays minus 1, wenn kein Schritt angegeben oder der angegebene Schritt positiv ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-328">is the length of sliced array minus one if no step is specified or the specified step is positive, and</span></span> 
- <span data-ttu-id="8410c-329">ist 0 (null), wenn der angegebene Schritt negativ ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-329">is zero if the specified step is negative.</span></span> 

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

## <a name="array-element-expressions"></a><span data-ttu-id="8410c-330">Array Element Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-330">Array Element Expressions</span></span>

<span data-ttu-id="8410c-331">Wenn ein Array Ausdruck und ein `Int` Ausdruck vorliegen, kann ein neuer Ausdruck mithilfe des `[` und `]` Array Element-Operators gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-331">Given an array expression and an `Int` expression, a new expression may be formed using the `[` and `]` array element operator.</span></span>
<span data-ttu-id="8410c-332">Der neue Ausdruck hat denselben Typ wie der Elementtyp des Arrays.</span><span class="sxs-lookup"><span data-stu-id="8410c-332">The new expression will be the same type as the element type of the array.</span></span>
<span data-ttu-id="8410c-333">Wenn `a` beispielsweise an ein Array von `Double`s gebunden ist, ist `a[4]` ein `Double` Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="8410c-333">For instance, if `a` is bound to an array of `Double`s, then `a[4]` is a `Double` expression.</span></span>

<span data-ttu-id="8410c-334">Wenn der Array Ausdruck kein einfacher Bezeichner ist, muss er in Klammern eingeschlossen werden, um ein Element auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="8410c-334">If the array expression is not a simple identifier, it must be enclosed it parentheses in order to select an element.</span></span>
<span data-ttu-id="8410c-335">Wenn beispielsweise `a` und `b` beide Arrays `Int`s sind, würde ein Element aus der Verkettung wie folgt ausgedrückt werden:</span><span class="sxs-lookup"><span data-stu-id="8410c-335">For instance, if `a` and `b` are both arrays of `Int`s, an element from the concatenation would be expressed as:</span></span>

```qsharp
(a+b)[13]
```

<span data-ttu-id="8410c-336">Alle Arrays in Q # sind NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="8410c-336">All arrays in Q# are zero-based.</span></span>
<span data-ttu-id="8410c-337">Das heißt, dass das erste Element eines Arrays `a` immer `a[0]`ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-337">That is, the first element of an array `a` is always `a[0]`.</span></span>


## <a name="copy-and-update-expressions"></a><span data-ttu-id="8410c-338">Copy-und Update-Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-338">Copy-and-Update Expressions</span></span>

<span data-ttu-id="8410c-339">Neue Arrays können über Kopier-und Update Ausdrücke aus vorhandenen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-339">New arrays can be created from existing ones via copy-and-update expressions.</span></span>
<span data-ttu-id="8410c-340">Ein Copy-and-Update-Ausdruck ist ein Ausdruck der Form `expression1 w/ expression2 <- expression3`, bei dem `expression1` für einige Typen `T`vom Typ `T[]` sein muss.</span><span class="sxs-lookup"><span data-stu-id="8410c-340">A copy-and-update expression is an expression of the form `expression1 w/ expression2 <- expression3`, where `expression1` has to be of type `T[]` for some type `T`.</span></span> <span data-ttu-id="8410c-341">Die zweite `expression2` definiert die Indizes der zu ändernden Elemente im Vergleich zum Array in `expression1` und muss entweder vom Typ `Int` oder vom Typ `Range`sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-341">The second `expression2` defines the indices of the element(s) to modify compared to the array in `expression1` and has to be either of type `Int` or of type `Range`.</span></span> <span data-ttu-id="8410c-342">Wenn `expression2` vom Typ `Int`ist, muss `expression3` vom Typ `T`sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-342">If `expression2` is of type `Int`, `expression3` has to be of type `T`.</span></span> <span data-ttu-id="8410c-343">Wenn `expression2` vom Typ `Range`ist, muss `expression3` vom Typ `T[]`sein.</span><span class="sxs-lookup"><span data-stu-id="8410c-343">If `expression2` is of type `Range`, `expression3` has to be of type `T[]`.</span></span>

<span data-ttu-id="8410c-344">Ein Copy-and-Update-Ausdruck `arr w/ idx <- value` erstellt ein neues Array mit allen Elementen, die auf das entsprechende Element in `arr`festgelegt sind, mit Ausnahme der Elemente in `idx`, die in `value`auf das entsprechende Element festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="8410c-344">A copy-and-update expression `arr w/ idx <- value` constructs a new array with all elements set to the corresponding element in `arr`, except for the element(s) at `idx`, which are set to the one(s) in `value`.</span></span> <span data-ttu-id="8410c-345">Wenn `arr` z. b. ein Array `[0,1,2,3]`enthält, dann</span><span class="sxs-lookup"><span data-stu-id="8410c-345">For example, if `arr` contains an array `[0,1,2,3]`, then</span></span> 
- <span data-ttu-id="8410c-346">`arr w/ 0 <- 10` ist das Array `[10,1,2,3]`.</span><span class="sxs-lookup"><span data-stu-id="8410c-346">`arr w/ 0 <- 10` is the array `[10,1,2,3]`.</span></span>
- <span data-ttu-id="8410c-347">`arr w/ 2 <- 10` ist das Array `[0,1,10,3]`.</span><span class="sxs-lookup"><span data-stu-id="8410c-347">`arr w/ 2 <- 10` is the array `[0,1,10,3]`.</span></span>
- <span data-ttu-id="8410c-348">`arr w/ 0..2..3 <- [10,12]` ist das Array `[10,1,12,3]`.</span><span class="sxs-lookup"><span data-stu-id="8410c-348">`arr w/ 0..2..3 <- [10,12]` is the array `[10,1,12,3]`.</span></span>

<span data-ttu-id="8410c-349">Ähnliche Ausdrücke sind für benannte Elemente in benutzerdefinierten Typen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8410c-349">Similar expressions exist for named items in user-defined types.</span></span> <span data-ttu-id="8410c-350">Beachten Sie beispielsweise den-Typ.</span><span class="sxs-lookup"><span data-stu-id="8410c-350">Consider for example the type</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="8410c-351">Wenn `c` den Wert des Typs `Complex(1.,-1.)`enthält, ist `c w/ Re <- 0.` ein Ausdruck vom Typ `Complex`, der als `Complex(0.,-1.)`ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="8410c-351">If `c` contains the value of type `Complex(1.,-1.)`, then `c w/ Re <- 0.` is an expression of type `Complex` that evaluates to `Complex(0.,-1.)`.</span></span>

## <a name="conditional-expressions"></a><span data-ttu-id="8410c-352">Bedingte Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="8410c-352">Conditional Expressions</span></span>

<span data-ttu-id="8410c-353">Bei zwei anderen Ausdrücken desselben Typs und eines booleschen Ausdrucks kann der bedingte Ausdruck mit dem Fragezeichen `?` und der senkrechten Leiste `|`gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="8410c-353">Given two other expressions of the same type and a Boolean expression, the conditional expression may be formed using the question mark `?` and the vertical bar `|`.</span></span>
<span data-ttu-id="8410c-354">Beispielsweise `a==b ? c | d`.</span><span class="sxs-lookup"><span data-stu-id="8410c-354">For instance, `a==b ? c | d`.</span></span>
<span data-ttu-id="8410c-355">In diesem Beispiel wird der Wert des bedingten Ausdrucks `c`, wenn `a==b` true ist, und `d`, wenn er false ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-355">In this example, the value of the conditional expression will be `c` if `a==b` is true and `d` if it is false.</span></span>

<span data-ttu-id="8410c-356">Die beiden Ausdrücke können zu Vorgängen ausgewertet werden, die über die gleichen Eingaben und Ausgaben verfügen, aber unterschiedliche Funktions tüktoren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8410c-356">The two expressions may evaluate to operations that have the same inputs and outputs but support different functors.</span></span>
<span data-ttu-id="8410c-357">In diesem Fall ist der Typ des bedingten Ausdrucks ein Vorgang mit diesen Eingaben und Ausgaben, der alle von beiden Ausdrücken unterstützten Funktoren unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8410c-357">In this case, the type of the conditional expression is an operation with those inputs and outputs that supports any functors supported by both expressions.</span></span>
<span data-ttu-id="8410c-358">Wenn z. b. `Op1`, `Op2`und `Op3` alle `Qubit[]=>Unit`sind, `Op1` aber `Adjoint`unterstützt, unterstützt `Op2` `Controlled`, und `Op3` unterstützt beides:</span><span class="sxs-lookup"><span data-stu-id="8410c-358">For example, if `Op1`, `Op2`, and `Op3` all are `Qubit[]=>Unit`, but `Op1` supports `Adjoint`, `Op2` supports `Controlled`, and `Op3` supports both:</span></span>

- <span data-ttu-id="8410c-359">`flag ? Op1 | Op2` ist ein `(Qubit[] => Unit)` Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8410c-359">`flag ? Op1 | Op2` is a `(Qubit[] => Unit)` operation.</span></span>
- <span data-ttu-id="8410c-360">`flag ? Op1 | Op3` ist ein `(Qubit[] => Unit is Adj)` Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8410c-360">`flag ? Op1 | Op3` is a `(Qubit[] => Unit is Adj)` operation.</span></span>
- <span data-ttu-id="8410c-361">`flag ? Op2 | Op3` ist ein `(Qubit[] => Unit is Ctl)` Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8410c-361">`flag ? Op2 | Op3` is a `(Qubit[] => Unit is Ctl)` operation.</span></span>

<span data-ttu-id="8410c-362">Wenn einer der beiden möglichen Ergebnis Ausdrücke einen Funktions-oder einen Vorgangs aufzurufen enthält, findet dieser Vorgang nur statt, wenn das Ergebnis das Ergebnis ist, das der Wert des Aufrufes ist.</span><span class="sxs-lookup"><span data-stu-id="8410c-362">If either of the two possible result expressions include a function or operation call, that call will only take place if that result is the one that will be the value of the call.</span></span>
<span data-ttu-id="8410c-363">Wenn `a==b` beispielsweise `a==b ? C(qs) | D(qs)`den Wert true hat, wird der `C` Vorgang aufgerufen, wenn er false ist, und wenn er false ist, wird nur `D` aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8410c-363">For instance, in the case `a==b ? C(qs) | D(qs)`, if `a==b` is true then the `C` operation will be invoked, and if it is false then only `D` will be invoked.</span></span>
<span data-ttu-id="8410c-364">Dies ähnelt der Kurzschluss in anderen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="8410c-364">This is similar to short-circuiting in other languages.</span></span>


## <a name="operator-precedence"></a><span data-ttu-id="8410c-365">Operator Rangfolge</span><span class="sxs-lookup"><span data-stu-id="8410c-365">Operator Precedence</span></span>

<span data-ttu-id="8410c-366">Alle binären Operatoren sind mit Ausnahme von `^`rechts assoziativ.</span><span class="sxs-lookup"><span data-stu-id="8410c-366">All binary operators are right-associative, except for `^`.</span></span>

<span data-ttu-id="8410c-367">Eckige Klammern, `[` und `]`für das aufteilen und Indizieren von Arrays werden vor jedem Operator gebunden.</span><span class="sxs-lookup"><span data-stu-id="8410c-367">Brackets, `[` and `]`, for array slicing and indexing, bind before any operator.</span></span>

<span data-ttu-id="8410c-368">Die Funktoren `Adjoint` und `Controlled` nach der Array Indizierung gebunden werden, aber vor allen anderen Operatoren.</span><span class="sxs-lookup"><span data-stu-id="8410c-368">The functors `Adjoint` and `Controlled` bind after array indexing but before all other operators.</span></span>

<span data-ttu-id="8410c-369">Klammern für Vorgangs-und Funktionsaufrufe werden auch vor jedem Operator gebunden, aber nach der Array Indizierung und den Funktoren.</span><span class="sxs-lookup"><span data-stu-id="8410c-369">Parentheses for operation and function invocation also bind before any operator but after array indexing and functors.</span></span>

<span data-ttu-id="8410c-370">Operatoren in Rangfolge, vom höchsten zum niedrigsten:</span><span class="sxs-lookup"><span data-stu-id="8410c-370">Operators in order of precedence, from highest to lowest:</span></span>

<span data-ttu-id="8410c-371">Operators</span><span class="sxs-lookup"><span data-stu-id="8410c-371">Operator</span></span> | <span data-ttu-id="8410c-372">Ständigkeit</span><span class="sxs-lookup"><span data-stu-id="8410c-372">Arity</span></span> | <span data-ttu-id="8410c-373">description</span><span class="sxs-lookup"><span data-stu-id="8410c-373">Description</span></span> | <span data-ttu-id="8410c-374">Operanden Typen</span><span class="sxs-lookup"><span data-stu-id="8410c-374">Operand Types</span></span>
---------|----------|---------|---------------
 <span data-ttu-id="8410c-375">nachfolgende `!`</span><span class="sxs-lookup"><span data-stu-id="8410c-375">trailing `!`</span></span> | <span data-ttu-id="8410c-376">Unären</span><span class="sxs-lookup"><span data-stu-id="8410c-376">Unary</span></span> | <span data-ttu-id="8410c-377">Aufheben der Umschließung</span><span class="sxs-lookup"><span data-stu-id="8410c-377">Unwrap</span></span> | <span data-ttu-id="8410c-378">Ein beliebiger benutzerdefinierter Typ</span><span class="sxs-lookup"><span data-stu-id="8410c-378">Any user-defined type</span></span>
 <span data-ttu-id="8410c-379">`-`, `~~~`, `not`</span><span class="sxs-lookup"><span data-stu-id="8410c-379">`-`, `~~~`, `not`</span></span> | <span data-ttu-id="8410c-380">Unären</span><span class="sxs-lookup"><span data-stu-id="8410c-380">Unary</span></span> | <span data-ttu-id="8410c-381">Numerische negative, bitweise Komplement logische Negation</span><span class="sxs-lookup"><span data-stu-id="8410c-381">Numeric negative, bitwise complement, logical negation</span></span> | <span data-ttu-id="8410c-382">`Int`, `BigInt` oder `Double` für `-`, `Int` oder `BigInt` `~~~`für `Bool`</span><span class="sxs-lookup"><span data-stu-id="8410c-382">`Int`, `BigInt` or `Double` for `-`, `Int` or `BigInt` for `~~~`, `Bool` for `not`</span></span>
 `^` | <span data-ttu-id="8410c-383">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-383">Binary</span></span> | <span data-ttu-id="8410c-384">Ganzzahlige Potenz</span><span class="sxs-lookup"><span data-stu-id="8410c-384">Integer power</span></span> | <span data-ttu-id="8410c-385">`Int` oder `BigInt` für die Basis `Int` für den Exponenten.</span><span class="sxs-lookup"><span data-stu-id="8410c-385">`Int` or `BigInt` for the base, `Int` for the exponent</span></span>
 <span data-ttu-id="8410c-386">`/`, `*`, `%`</span><span class="sxs-lookup"><span data-stu-id="8410c-386">`/`, `*`, `%`</span></span> | <span data-ttu-id="8410c-387">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-387">Binary</span></span> | <span data-ttu-id="8410c-388">Division, Multiplikation, ganzzahliger Modulo</span><span class="sxs-lookup"><span data-stu-id="8410c-388">Division, multiplication, integer modulus</span></span> | <span data-ttu-id="8410c-389">`Int`, `BigInt` oder `Double` für `/` und `*`, `Int` oder `BigInt` für `%`</span><span class="sxs-lookup"><span data-stu-id="8410c-389">`Int`, `BigInt` or `Double` for `/` and `*`, `Int` or `BigInt` for `%`</span></span>
 <span data-ttu-id="8410c-390">`+`, `-`</span><span class="sxs-lookup"><span data-stu-id="8410c-390">`+`, `-`</span></span> | <span data-ttu-id="8410c-391">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-391">Binary</span></span> | <span data-ttu-id="8410c-392">Addition oder Zeichenfolge und Array Verkettung, Subtraktion</span><span class="sxs-lookup"><span data-stu-id="8410c-392">Addition or string and array concatenation, subtraction</span></span> | <span data-ttu-id="8410c-393">`Int`, `BigInt` oder `Double`, zusätzlich `String` oder ein beliebiger Arraytyp für `+`</span><span class="sxs-lookup"><span data-stu-id="8410c-393">`Int`, `BigInt` or `Double`, additionally `String` or any array type for `+`</span></span>
 <span data-ttu-id="8410c-394">`<<<`, `>>>`</span><span class="sxs-lookup"><span data-stu-id="8410c-394">`<<<`, `>>>`</span></span> | <span data-ttu-id="8410c-395">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-395">Binary</span></span> | <span data-ttu-id="8410c-396">Left Shift, Right Shift</span><span class="sxs-lookup"><span data-stu-id="8410c-396">Left shift, right shift</span></span> | <span data-ttu-id="8410c-397">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="8410c-397">`Int` or `BigInt`</span></span>
 <span data-ttu-id="8410c-398">`<`, `<=`, `>`, `>=`</span><span class="sxs-lookup"><span data-stu-id="8410c-398">`<`, `<=`, `>`, `>=`</span></span> | <span data-ttu-id="8410c-399">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-399">Binary</span></span> | <span data-ttu-id="8410c-400">Kleiner-als-, kleiner-als-oder-gleich-, größer-als-, größer-als-oder-gleich-Vergleiche</span><span class="sxs-lookup"><span data-stu-id="8410c-400">Less-than, less-than-or-equal, greater-than, greater-than-or-equal comparisons</span></span> | <span data-ttu-id="8410c-401">`Int`, `BigInt` oder `Double`</span><span class="sxs-lookup"><span data-stu-id="8410c-401">`Int`, `BigInt` or `Double`</span></span>
 <span data-ttu-id="8410c-402">`==`, `!=`</span><span class="sxs-lookup"><span data-stu-id="8410c-402">`==`, `!=`</span></span> | <span data-ttu-id="8410c-403">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-403">Binary</span></span> | <span data-ttu-id="8410c-404">gleich, nicht gleichmäßige Vergleiche</span><span class="sxs-lookup"><span data-stu-id="8410c-404">equal, not-equal comparisons</span></span> | <span data-ttu-id="8410c-405">beliebiger primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="8410c-405">any primitive type</span></span>
 `&&&` | <span data-ttu-id="8410c-406">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-406">Binary</span></span> | <span data-ttu-id="8410c-407">Bitweises and</span><span class="sxs-lookup"><span data-stu-id="8410c-407">Bitwise AND</span></span> | <span data-ttu-id="8410c-408">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="8410c-408">`Int` or `BigInt`</span></span>
 `^^^` | <span data-ttu-id="8410c-409">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-409">Binary</span></span> | <span data-ttu-id="8410c-410">Bitweises XOR</span><span class="sxs-lookup"><span data-stu-id="8410c-410">Bitwise XOR</span></span> | <span data-ttu-id="8410c-411">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="8410c-411">`Int` or `BigInt`</span></span>
 <code>\|\|\|</code> | <span data-ttu-id="8410c-412">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-412">Binary</span></span> | <span data-ttu-id="8410c-413">Bitweises OR</span><span class="sxs-lookup"><span data-stu-id="8410c-413">Bitwise OR</span></span> | <span data-ttu-id="8410c-414">`Int` oder `BigInt`</span><span class="sxs-lookup"><span data-stu-id="8410c-414">`Int` or `BigInt`</span></span>
 `and` | <span data-ttu-id="8410c-415">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-415">Binary</span></span> | <span data-ttu-id="8410c-416">Logisches and</span><span class="sxs-lookup"><span data-stu-id="8410c-416">Logical AND</span></span> | `Bool`
 `or` | <span data-ttu-id="8410c-417">Binär</span><span class="sxs-lookup"><span data-stu-id="8410c-417">Binary</span></span> | <span data-ttu-id="8410c-418">Logisches OR</span><span class="sxs-lookup"><span data-stu-id="8410c-418">Logical OR</span></span> | `Bool`
 `..` | <span data-ttu-id="8410c-419">Binär/Ternär</span><span class="sxs-lookup"><span data-stu-id="8410c-419">Binary/Ternary</span></span> | <span data-ttu-id="8410c-420">Bereichs Operator</span><span class="sxs-lookup"><span data-stu-id="8410c-420">Range operator</span></span> | `Int`
 <span data-ttu-id="8410c-421">`?``|`</span><span class="sxs-lookup"><span data-stu-id="8410c-421">`?` `|`</span></span> | <span data-ttu-id="8410c-422">TERNÄRE</span><span class="sxs-lookup"><span data-stu-id="8410c-422">Ternary</span></span> | <span data-ttu-id="8410c-423">Bedingt</span><span class="sxs-lookup"><span data-stu-id="8410c-423">Conditional</span></span> | <span data-ttu-id="8410c-424">`Bool` für die linke Seite</span><span class="sxs-lookup"><span data-stu-id="8410c-424">`Bool` for the left-hand-side</span></span>
<span data-ttu-id="8410c-425">`w/``<-`</span><span class="sxs-lookup"><span data-stu-id="8410c-425">`w/` `<-`</span></span> | <span data-ttu-id="8410c-426">TERNÄRE</span><span class="sxs-lookup"><span data-stu-id="8410c-426">Ternary</span></span> | <span data-ttu-id="8410c-427">Kopieren und aktualisieren</span><span class="sxs-lookup"><span data-stu-id="8410c-427">Copy-and-update</span></span> | <span data-ttu-id="8410c-428">Weitere Informationen finden Sie unter [Copy-and-Update-Ausdrücke](#copy-and-update-expressions)</span><span class="sxs-lookup"><span data-stu-id="8410c-428">see [copy-and-update expressions](#copy-and-update-expressions)</span></span>
