---
title: Typen in Q#
description: 'Erfahren Sie mehr über die verschiedenen Typen, die in der Programmiersprache Q # verwendet werden.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
ms.openlocfilehash: f7a3ac3813966c0ef695068297ce4d9949ead554
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327287"
---
# <a name="types-in-q"></a><span data-ttu-id="fa85c-103">Typen in Q#</span><span class="sxs-lookup"><span data-stu-id="fa85c-103">Types in Q#</span></span>

<span data-ttu-id="fa85c-104">Auf dieser Seite wird das Q #-Typmodell und die Syntax zum Angeben von und arbeiten mit Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa85c-104">This page lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="fa85c-105">Auf der nächsten Seite, [typausdrücke](xref:microsoft.quantum.guide.expressions), wird erläutert, wie Ausdrücke dieser Typen erstellt und verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-105">The next page, [Type Expressions](xref:microsoft.quantum.guide.expressions), details how to create and operate on expressions of these types.</span></span>

<span data-ttu-id="fa85c-106">Beachten Sie, dass Q # eine *stark typisierte* Sprache ist, sodass der Compiler durch eine sorgfältige Verwendung dieser Typen bei der Kompilierung starke Garantien für Q #-Programme bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="fa85c-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="fa85c-107">Um die bestmögliche Garantie bereitzustellen, müssen Konvertierungen zwischen Typen in Q # explizit mithilfe von Aufrufen von Funktionen erfolgen, die diese Konvertierung Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="fa85c-107">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="fa85c-108">Eine Vielzahl solcher Funktionen werden als Teil des- <xref:microsoft.quantum.convert> Namespace bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-108">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="fa85c-109">Auf der anderen Seite werden Upcasts zu kompatiblen Typen implizit durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-109">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="fa85c-110">Q # stellt beide primitiven Typen bereit, die direkt verwendet werden können, und eine Vielzahl von Möglichkeiten, um neue Typen aus anderen Typen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="fa85c-110">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="fa85c-111">Diese werden im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa85c-111">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="fa85c-112">Primitive Typen</span><span class="sxs-lookup"><span data-stu-id="fa85c-112">Primitive Types</span></span>

<span data-ttu-id="fa85c-113">Die Sprache Q # stellt mehrere *primitive Typen*bereit, von denen andere Typen erstellt werden können:</span><span class="sxs-lookup"><span data-stu-id="fa85c-113">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="fa85c-114">Der- `Int` Typ stellt eine 64-Bit-Ganzzahl mit Vorzeichen dar, z. b.: `2` , `107` , `-5` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-114">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="fa85c-115">Der- `BigInt` Typ stellt eine Ganzzahl mit Vorzeichen beliebiger Größe dar, z. b., `2L` `107L` , `-5L` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-115">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="fa85c-116">Dieser Typ basiert auf .net.<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="fa85c-116">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="fa85c-117">Sorte.</span><span class="sxs-lookup"><span data-stu-id="fa85c-117">type.</span></span>
- <span data-ttu-id="fa85c-118">Der `Double` -Typ stellt eine Gleit Komma Zahl mit doppelter Genauigkeit dar, z. b.: `0.0` , `-1.3` , `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-118">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="fa85c-119">Der- `Bool` Typ stellt einen booleschen Wert dar, der entweder oder sein kann `true` `false` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-119">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="fa85c-120">Der- `Range` Typ stellt eine Sequenz von ganzen Zahlen dar, die durch angegeben wird, `start..step..stop` wobei der Schritt optional ist.</span><span class="sxs-lookup"><span data-stu-id="fa85c-120">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="fa85c-121">Dies `start .. stop` entspricht `start..1..stop` , und stellt z. b. `1..2..7` die Sequenz $ \{ 1, 3, 5, 7 \} $ dar.</span><span class="sxs-lookup"><span data-stu-id="fa85c-121">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="fa85c-122">Der- `String` Typ ist eine Sequenz von Unicode-Zeichen, die für den Benutzer nach der Erstellung nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="fa85c-122">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="fa85c-123">Dieser Typ wird verwendet, um Nachrichten an einen klassischen Host zu melden, wenn ein Fehler oder ein Diagnose Ereignis vorliegt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-123">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="fa85c-124">Der `Unit` Typ ist der Typ, der nur einen Wert zulässt `()` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-124">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="fa85c-125">Dieser Typ wird verwendet, um anzugeben, dass die Q #-Funktion oder der-Vorgang keine Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-125">This type is used to indicate that Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="fa85c-126">Der- `Qubit` Typ stellt ein Quantum-Bit oder Qubit dar.</span><span class="sxs-lookup"><span data-stu-id="fa85c-126">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="fa85c-127">`Qubit`e sind für den Benutzer nicht transparent. der einzige Vorgang, der mit Ihnen möglich ist, und nicht an einen anderen Vorgang zu übergeben, besteht darin, auf Identity (Gleichheit) zu testen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-127">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="fa85c-128">Letztendlich werden Aktionen für `Qubit` s implementiert, indem systeminterne Anweisungen für einen Quantum-Prozessor (oder eine Simulation) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-128">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="fa85c-129">Der- `Pauli` Typ stellt einen der vier Single-Qubit-Pauli-Operatoren dar.</span><span class="sxs-lookup"><span data-stu-id="fa85c-129">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="fa85c-130">Dieser Typ wird verwendet, um den Basis Vorgang für Drehungen anzugeben und um die zu messende Observable anzugeben.</span><span class="sxs-lookup"><span data-stu-id="fa85c-130">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="fa85c-131">Dies ist ein enumerierter Typ, der über vier mögliche Werte verfügt: `PauliI` , `PauliX` , `PauliY` und `PauliZ` , bei denen es sich um Konstanten des Typs handelt `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-131">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="fa85c-132">Der- `Result` Typ stellt das Ergebnis einer Messung dar.</span><span class="sxs-lookup"><span data-stu-id="fa85c-132">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="fa85c-133">Dabei handelt es sich um einen enumerierten Typ mit zwei möglichen Werten: und, bei denen es sich um `One` `Zero` Konstanten vom Typ handelt `Result` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-133">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="fa85c-134">`Zero`Gibt an, dass der Eigen Wert + 1 gemessen wurde. `One`gibt den eigen Wert-1 an.</span><span class="sxs-lookup"><span data-stu-id="fa85c-134">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>

<span data-ttu-id="fa85c-135">Die Konstanten `true` , `false` , `PauliI` ,,, `PauliX` `PauliY` `PauliZ` , `One` und `Zero` sind reservierte Symbole in Q #.</span><span class="sxs-lookup"><span data-stu-id="fa85c-135">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="fa85c-136">Array Typen</span><span class="sxs-lookup"><span data-stu-id="fa85c-136">Array Types</span></span>

<span data-ttu-id="fa85c-137">Bei jedem gültigen Q #-Typ `'T` gibt es einen Typ, der ein Array von Werten vom Typ darstellt `'T` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-137">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="fa85c-138">Dieser Arraytyp wird als dargestellt `'T[]` , z `Qubit[]` . b `Int[][]` . oder.</span><span class="sxs-lookup"><span data-stu-id="fa85c-138">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="fa85c-139">Beispielsweise ist eine Auflistung von ganzen Zahlen gekennzeichnet `Int[]` , während ein Array von `(Bool, Pauli)` Werten mit Werten gekennzeichnet wird `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-139">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="fa85c-140">Beachten Sie im zweiten Beispiel, dass dies eine potenziell Jagged Array von Arrays und kein rechteckiges zweidimensionales Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-140">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="fa85c-141">Q # bietet keine Unterstützung für rechteckige mehrdimensionale Arrays.</span><span class="sxs-lookup"><span data-stu-id="fa85c-141">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="fa85c-142">Ein Arraywert kann in Q #-Quellcode mithilfe von eckigen Klammern um die Elemente eines Arrays geschrieben werden, wie in `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-142">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="fa85c-143">Der Typ eines Arrayliterals hängt von dem allgemeinen Basistyp aller Elemente im Array ab.</span><span class="sxs-lookup"><span data-stu-id="fa85c-143">The type of an array literal is determined by the common base type of all items in the array.</span></span> <span data-ttu-id="fa85c-144">Daher wird beim Versuch, ein Array mit Elementen zu erstellen, die keinen gemeinsamen Basistyp haben, ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa85c-144">Hence trying to construct an array with elements that have no common base type will raise an error.</span></span>  
<span data-ttu-id="fa85c-145">Ein Beispiel hierfür finden Sie unter [Arrays von callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables) .</span><span class="sxs-lookup"><span data-stu-id="fa85c-145">See [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables) for an example of this.</span></span>

> [!WARNING]
> <span data-ttu-id="fa85c-146">Die Elemente eines Arrays können nicht geändert werden, nachdem das Array erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa85c-146">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="fa85c-147">Die [Anweisungen Update-und-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) und/oder [Copy-und-Update-Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) können zum Erstellen eines geänderten Arrays verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-147">[Update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) and/or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions) can be used to construct a modified array.</span></span>

<span data-ttu-id="fa85c-148">Alternativ kann ein Array mit dem-Schlüsselwort aus seiner Größe erstellt werden `new` :</span><span class="sxs-lookup"><span data-stu-id="fa85c-148">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="fa85c-149">In beiden Fällen kann die Core-Funktion `Length` verwendet werden, um die Anzahl von Elementen als zu erhalten, sobald ein Array erstellt wurde `Int` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-149">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="fa85c-150">Arrays können mithilfe von eckigen Klammern, wobei es sich `Int` um einen Typ oder einen Typ handelt, abonniert werden, `Range` um entweder einzelne Elemente oder neue Arrays zu erhalten, die eine Teilmenge der Elemente eines Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="fa85c-150">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="fa85c-151">Die Indizes von Arrays sind NULL basiert:</span><span class="sxs-lookup"><span data-stu-id="fa85c-151">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="fa85c-152">Tupeltypen</span><span class="sxs-lookup"><span data-stu-id="fa85c-152">Tuple Types</span></span>

<span data-ttu-id="fa85c-153">Wenn 0 (null) oder mehr unterschiedliche Typen `T0` , `T1` ,..., `Tn` , kann ein neuer *tupeltyp* als bezeichnet werden `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-153">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="fa85c-154">Die Typen, die zum Erstellen eines neuen tupeltyps verwendet werden, können selbst Tupel sein, wie in `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-154">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="fa85c-155">Eine solche Schachtelung ist jedoch immer begrenzt, da Tupeltypen unter keinen Umständen selbst enthalten.</span><span class="sxs-lookup"><span data-stu-id="fa85c-155">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="fa85c-156">Werte des neuen tupeltyps sind Tupel, die durch Sequenz von Werten aus jedem Typ im Tupel gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-156">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="fa85c-157">Beispielsweise `(3, false)` ist ein Tupel, dessen Typ der tupeltyp ist `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-157">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="fa85c-158">Es ist möglich, Arrays von Tupeln, Tupeln von Arrays, Tupeln von subtupeln usw. zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-158">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="fa85c-159">Ab Q # 0,3 `Unit` ist der Name des *Typs* des leeren Tupels; `()` wird für den leeren *tupelwert*verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa85c-159">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="fa85c-160">Tupelinstanzen sind unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="fa85c-160">Tuple instances are immutable.</span></span>
<span data-ttu-id="fa85c-161">Q # stellt keinen Mechanismus zum Ändern des Inhalts eines Tupels bereit, nachdem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fa85c-161">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="fa85c-162">Tupel sind ein leistungsfähiges Konzept, das in Q # verwendet wird, um Werte in einem einzelnen Wert zusammenzufassen, sodass Sie einfacher zu übergeben sind.</span><span class="sxs-lookup"><span data-stu-id="fa85c-162">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="fa85c-163">Insbesondere mithilfe von tupelnotation können wir ausdrücken, dass jeder Vorgang und Callable genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-163">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="fa85c-164">Äquivalenz für Singleton-Tupel</span><span class="sxs-lookup"><span data-stu-id="fa85c-164">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="fa85c-165">Es ist möglich, ein Singleton-Tupel (Einzelelement) zu erstellen, `('T1)` z `(5)` . b `([1,2,3])` . oder.</span><span class="sxs-lookup"><span data-stu-id="fa85c-165">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="fa85c-166">Q # behandelt jedoch ein Singleton-Tupel als vollständig Äquivalent zu einem Wert des eingeschlossenen Typs.</span><span class="sxs-lookup"><span data-stu-id="fa85c-166">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="fa85c-167">Das heißt, es gibt keinen Unterschied zwischen `5` und `(5)` bzw `5` . zwischen und `(((5)))` oder zwischen `(5, (6))` und `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-167">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="fa85c-168">Es ist ebenso gültig, wie geschrieben zu `(5)+3` werden, um zu schreiben `5+3` , und beide Ausdrücke werden in ausgewertet `8` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-168">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>

<span data-ttu-id="fa85c-169">Diese Äquivalenz gilt für alle Zwecke, einschließlich Zuweisung und Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="fa85c-169">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="fa85c-170">Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="fa85c-170">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="fa85c-171">Beispielsweise `(7)` ist ein `Int` Ausdruck, `([1,2,3])` ist ein Ausdruck vom Typ Array von `Int` s, und `((1,2))` ist ein Ausdruck vom Typ `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-171">For instance, `(7)` is an `Int` expression, `([1,2,3])` is an expression of type array of `Int`s, and `((1,2))` is an expression with type `(Int, Int)`.</span></span>

<span data-ttu-id="fa85c-172">Dies bedeutet insbesondere, dass ein Vorgang oder eine Funktion, deren Eingabetyp oder Ausgabetyp ein Feld hat, sich als ein einzelnes Argument oder einen einzelnen Wert vorstellen kann.</span><span class="sxs-lookup"><span data-stu-id="fa85c-172">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="fa85c-173">Diese Eigenschaft wird als Übereinstimmung mit einem _Singleton-Tupel_bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fa85c-173">We refer to this property as _singleton tuple equivalence_.</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="fa85c-174">Benutzerdefinierte Typen</span><span class="sxs-lookup"><span data-stu-id="fa85c-174">User-Defined Types</span></span>

<span data-ttu-id="fa85c-175">Eine benutzerdefinierte Typdeklaration besteht aus dem Schlüsselwort `newtype` , gefolgt vom Namen des benutzerdefinierten Typs, einer `=` , einer gültigen Typspezifikation und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="fa85c-175">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="fa85c-176">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fa85c-176">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="fa85c-177">Jede f #-Quelldatei kann eine beliebige Anzahl benutzerdefinierter Typen deklarieren.</span><span class="sxs-lookup"><span data-stu-id="fa85c-177">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="fa85c-178">Typnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-und Funktionsnamen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-178">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="fa85c-179">Benutzerdefinierte Typen sind unterschiedlich, auch wenn die Basis Typen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="fa85c-179">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="fa85c-180">Insbesondere, wenn die zugrunde liegenden Typen identisch sind, gibt es keine automatische Konvertierung zwischen Werten von zwei benutzerdefinierten Typen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-180">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="fa85c-181">Benannte und anonyme Elemente</span><span class="sxs-lookup"><span data-stu-id="fa85c-181">Named vs. anonymous items</span></span>

<span data-ttu-id="fa85c-182">Eine Q #-Datei kann einen neuen benannten Typ definieren, der einen einzelnen Wert eines beliebigen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="fa85c-182">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="fa85c-183">Für jeden tupeltyp `T` können wir einen neuen benutzerdefinierten Typ deklarieren, bei dem es sich um einen Untertyp von `T` mit der- `newtype` Anweisung handelt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-183">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="fa85c-184">Im- @"microsoft.quantum.math" Namespace sind komplexe Zahlen beispielsweise als benutzerdefinierter Typ definiert:</span><span class="sxs-lookup"><span data-stu-id="fa85c-184">In the @"microsoft.quantum.math" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="fa85c-185">Diese Anweisung erstellt einen neuen Typ mit zwei anonymen Elementen vom Typ `Double` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-185">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="fa85c-186">Abgesehen von anonymen Elementen unterstützen benutzerdefinierte Typen auch *benannte Elemente* ab Q # Version 0,7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fa85c-186">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="fa85c-187">Beispielsweise könnten wir den in Elemente `Re` für das Double benennen, das den Realteil einer komplexen Zahl und `Im` für den imaginären Teil darstellt:</span><span class="sxs-lookup"><span data-stu-id="fa85c-187">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="fa85c-188">Das Benennen eines Elements in einem benutzerdefinierten Typ impliziert nicht, dass alle Elemente benannt werden müssen. eine beliebige Kombination aus benannten und unbenannten Elementen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-188">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="fa85c-189">Außerdem können innere Elemente ebenfalls benannt werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-189">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="fa85c-190">Der Typ `Nested` , wie unten definiert, verfügt über einen zugrunde liegenden Typ `(Double, (Int, String))` , von dem nur das Element des Typs `Int` benannt wird und alle anderen Elemente anonym sind.</span><span class="sxs-lookup"><span data-stu-id="fa85c-190">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="fa85c-191">Benannte Elemente haben den Vorteil, dass Sie direkt über den *Zugriffs Operator* darauf zugreifen können `::` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-191">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="fa85c-192">Zusätzlich zur Bereitstellung kurzer Aliase für potenziell komplizierte Tupeltypen ist ein wesentlicher Vorteil der Definition solcher Typen, dass Sie die Absicht eines bestimmten Werts dokumentieren können.</span><span class="sxs-lookup"><span data-stu-id="fa85c-192">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="fa85c-193">Wenn Sie zum Beispiel zurückkehren `Complex` , können Sie auch 2D-Polarkoordinaten als benutzerdefinierten Typ definieren:</span><span class="sxs-lookup"><span data-stu-id="fa85c-193">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="fa85c-194">Obwohl sowohl `Complex` als auch `Polar` beide über einen zugrunde liegenden Typ verfügen `(Double, Double)` , sind die beiden Typen in f # vollständig inkompatibel. Dadurch wird das Risiko minimiert, dass versehentlich eine komplexe mathematische Funktion mit Polarkoordinaten aufgerufen wird und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-194">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="fa85c-195">Auf diese Weise haben benutzerdefinierte Typen eine ähnliche Rolle wie Datensätze in F #.</span><span class="sxs-lookup"><span data-stu-id="fa85c-195">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="fa85c-196">Auf anonyme Elemente mit dem Unwrap-Operator zugreifen</span><span class="sxs-lookup"><span data-stu-id="fa85c-196">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="fa85c-197">Um auf anonyme Elemente zugreifen zu können, muss der umschließende Wert zuerst mithilfe des Postfix-Operators extrahiert werden `!` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-197">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="fa85c-198">Der Unwrap-Operator () `!` ermöglicht, den in einem benutzerdefinierten Typ enthaltenen Wert zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="fa85c-198">The "unwrap" operator, `!`, allows to extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="fa85c-199">Der Typ eines solchen "Unwrap"-Ausdrucks ist der zugrunde liegende Typ des benutzerdefinierten Typs.</span><span class="sxs-lookup"><span data-stu-id="fa85c-199">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="fa85c-200">Der Unwrap-Operator entpackt genau eine Ebene der Umbruch.</span><span class="sxs-lookup"><span data-stu-id="fa85c-200">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="fa85c-201">Mehrere Unwrap-Operatoren können verwendet werden, um auf einen multipliziert-umschließenden Wert zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-201">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="fa85c-202">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fa85c-202">For instance:</span></span>

```qsharp
newtype WrappedInt = Int;
newtype DoublyWrappedInt = WrappedInt;

...
    let x = DoublyWrappedInt(WrappedInt(6));
    let y = x!;       // y is WrappedInt(6)
    let z = x!!;      // z is 6
    let a = x + 5;    // This is an error, a DoublyWrappedInt isn't an Int
    let b = x! + 5;   // Also an error
    let c = x!! + 5;  // This is valid, c will be 11
...
```

<span data-ttu-id="fa85c-203">Weitere Informationen zum Unwrap-Operator finden Sie unter [typanexpressions in f #](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="fa85c-203">More details on the unwrap operator can be found at [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="fa85c-204">Erstellen von Werten für benutzerdefinierte Typen</span><span class="sxs-lookup"><span data-stu-id="fa85c-204">Creating values of user-defined types</span></span>

<span data-ttu-id="fa85c-205">Werte eines benutzerdefinierten Typs können erstellt werden, indem der entsprechende Typkonstruktor aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="fa85c-205">Values of a user-defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="fa85c-206">Alternativ können neue Werte mithilfe von [Ausdrücken zum Kopieren und aktualisieren](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)aus vorhandenen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-206">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="fa85c-207">Wie bei Arrays Kopieren solche Ausdrücke alle Element Werte des ursprünglichen Ausdrucks, mit Ausnahme der angegebenen benannten Elemente.</span><span class="sxs-lookup"><span data-stu-id="fa85c-207">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="fa85c-208">Für diese werden die Werte auf die Werte festgelegt, die auf der rechten Seite des Ausdrucks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="fa85c-208">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="fa85c-209">Alle anderen Sprachkonstrukte, wie z. b. [Update-und-REASSIGN-Anweisungen](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), die für Array Elemente verfügbar sind, sind auch für benannte Elemente in benutzerdefinierten Typen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-209">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), that are available for array items exist for named-items in user-defined types as well.</span></span>

```qsharp
newtype ComplexArray = (Count : Int, Data : Complex[]);

function AsComplexArray (data : Double[]) : ComplexArray {

    mutable res = ComplexArray(0, new Complex[0]);
    for (item in data) {
        set res w/= Data <- res::Data + [Complex(item, 0.)]; // update-and-reassign statement
    }
    return res w/ Count <- Length(res::Data); // returning a copy-and-update expression
}
```

<span data-ttu-id="fa85c-210">Benutzerdefinierte Typen können überall dort verwendet werden, wo jeder andere Typ verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fa85c-210">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="fa85c-211">Insbesondere ist es möglich, ein Array eines benutzerdefinierten Typs zu definieren und einen benutzerdefinierten Typ als Element eines tupeltyps einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-211">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="fa85c-212">Beachten Sie, dass keine rekursiven Typstrukturen erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="fa85c-212">Note is not possible to create recursive type structures.</span></span>
<span data-ttu-id="fa85c-213">Das heißt, der Typ, der einen benutzerdefinierten Typ definiert, darf kein tupeltyp sein, der ein Element des benutzerdefinierten Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="fa85c-213">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="fa85c-214">Im Allgemeinen haben benutzerdefinierte Typen möglicherweise keine zyklischen Abhängigkeiten, sodass der folgende Satz von Typdefinitionen unzulässig wäre:</span><span class="sxs-lookup"><span data-stu-id="fa85c-214">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```


## <a name="operation-and-function-types"></a><span data-ttu-id="fa85c-215">Vorgangs-und Funktionstypen</span><span class="sxs-lookup"><span data-stu-id="fa85c-215">Operation and Function Types</span></span>

<span data-ttu-id="fa85c-216">Der Basistyp für alle Aufruf baren wird als `('Tinput => 'Tresult)` oder geschrieben `('Tinput -> 'Tresult)` , wobei sowohl als `'Tinput` auch- `'Tresult` Typen sind.</span><span class="sxs-lookup"><span data-stu-id="fa85c-216">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="fa85c-217">Diese werden als *Signatur* der aufrufenden bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="fa85c-217">These are called the *signature* of the callable.</span></span>

<span data-ttu-id="fa85c-218">Alle f #-callables werden als Eingabe betrachtet und geben einen einzelnen Wert als Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="fa85c-218">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="fa85c-219">Sowohl der Eingabe-als auch der Ausgabewert können Tupel sein.</span><span class="sxs-lookup"><span data-stu-id="fa85c-219">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="fa85c-220">Callables ohne Ergebnis Rückgabe `Unit` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-220">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="fa85c-221">Callables ohne Eingabe nehmen das leere Tupel als Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="fa85c-221">Callables that have no input take the empty tuple as input.</span></span>

> [!NOTE]
> <span data-ttu-id="fa85c-222">Das erste Formular, mit `=>` wird für-Vorgänge verwendet, das zweite Formular, mit `->` für-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-222">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
> <span data-ttu-id="fa85c-223">`((Qubit, Pauli) => Result)`Stellt z. b. die Signatur für einen möglichen Single-Qubit-Messvorgang dar.</span><span class="sxs-lookup"><span data-stu-id="fa85c-223">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>
<span data-ttu-id="fa85c-224">*Funktions* Typen werden vollständig durch ihre Signatur angegeben.</span><span class="sxs-lookup"><span data-stu-id="fa85c-224">*Function* types are completely specified by their signature.</span></span>
<span data-ttu-id="fa85c-225">Eine Funktion, die den Sinus eines Winkels berechnet, hätte z. b. den Typ `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-225">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="fa85c-226">*Vorgänge*---, aber keine Funktionen---bestimmte zusätzliche Merkmale aufweisen, die als Teil des Vorgangs Typs ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fa85c-226">*Operations*---but not functions---have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="fa85c-227">Zu diesen Merkmalen zählen Informationen darüber, welche Funktions *tüktoren* der Vorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-227">Such characteristics include information about what *functors* the operation supports.</span></span>
<span data-ttu-id="fa85c-228">Wenn die Ausführung des Vorgangs z. b. auf den Zustand anderer Qubits bedingt sein kann, sollte er das `Controlled` Funktor unterstützen. wenn der Vorgang eine Umkehrung hat, sollte er das `Adjoint` Funktor unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-228">For example, if execution of the operation can be conditioned on the state of other qubits, it should support the `Controlled` functor; if the operation has an inverse, it should support the `Adjoint` functor.</span></span> <span data-ttu-id="fa85c-229">Funktoren und Vorgänge werden ausführlich unter [Vorgänge und Funktionen in Q #](xref:microsoft.quantum.guide.operationsfunctions)erläutert, aber hier wird einfach erläutert, wie dies die Vorgangs Signatur verändert.</span><span class="sxs-lookup"><span data-stu-id="fa85c-229">Functors and operations are discussed in detail at [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions), but here we simply discuss how this alters the operation signature.</span></span>

<span data-ttu-id="fa85c-230">Um Unterstützung für den `Controlled` -und/oder- `Adjoint` Funktions tüktor in einem Vorgangstyp zu benötigen, müssen Sie eine Anmerkung hinzufügen, die die entsprechenden Merkmale angibt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-230">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="fa85c-231">Eine Anmerkung `is Ctl` (z. b `(Qubit => Unit is Ctl)` .) gibt an, dass der Vorgang steuerbar ist---d. h., die Ausführung ist für den Zustand eines anderen Qubit oder Qubits bedingt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-231">An annotation `is Ctl` (e.g. `(Qubit => Unit is Ctl)`) indicates that the operation is controllable---that is, it's execution conditioned on the state of another qubit or qubits.</span></span> <span data-ttu-id="fa85c-232">Analog dazu `is Adj` gibt an, dass der Vorgang über ein Adjoint verfügt, oder einfach, dass er "invertiert" werden kann, sodass das Fortsetzen eines Vorgangs und dessen Adjoint auf einen Zustand den Zustand unverändert lässt.</span><span class="sxs-lookup"><span data-stu-id="fa85c-232">Similarly, `is Adj` indicates that the operation has an adjoint; or simply, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="fa85c-233">Wenn Sie festlegen möchten, dass ein Vorgang dieses Typs sowohl das-als `Adjoint` auch das-Funktor unterstützt, `Controlled` können wir dies als Ausdrücken `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-233">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="fa85c-234">Der integrierte Pauli- <xref:microsoft.quantum.intrinsic.x> Vorgang hat z. b. den-Typ `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-234">For example, the built-in Pauli <xref:microsoft.quantum.intrinsic.x> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="fa85c-235">Ein Vorgangstyp, der keine Funktions tüktoren unterstützt, wird von seinem Eingabe-und Ausgabetyp allein angegeben, ohne dass zusätzliche Anmerkungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fa85c-235">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="fa85c-236">Typparametrisierte Funktionen und Vorgänge</span><span class="sxs-lookup"><span data-stu-id="fa85c-236">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="fa85c-237">Aufruf Bare Typen können Typparameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="fa85c-237">Callable types may contain type parameters.</span></span>
<span data-ttu-id="fa85c-238">Typparameter werden durch ein Symbol angegeben, das ein einzelnes Anführungszeichen als Präfix hat. beispielsweise `'A` ist ein gültiger Typparameter.</span><span class="sxs-lookup"><span data-stu-id="fa85c-238">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="fa85c-239">Details zum Definieren von parametrisierten typparametrisierten aufrufen finden Sie auf der Seite [Vorgänge und Funktionen in f #](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) .</span><span class="sxs-lookup"><span data-stu-id="fa85c-239">Details on defining type-parameterized callables are provided on the [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables) page.</span></span>

<span data-ttu-id="fa85c-240">Ein Typparameter kann in einer einzigen Signatur mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-240">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="fa85c-241">Eine Funktion, die eine andere Funktion auf jedes Element eines Arrays anwendet und die gesammelten Ergebnisse zurückgibt, hätte z. b. eine Signatur `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-241">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="fa85c-242">Ebenso kann eine Funktion, die die Komposition von zwei Vorgängen zurückgibt, eine Signatur aufweisen `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="fa85c-242">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="fa85c-243">Beim Aufrufen eines typparametrisierten Aufruf baren Typs müssen alle Argumente, die denselben Typparameter aufweisen, denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fa85c-243">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="fa85c-244">Q # stellt keinen Mechanismus zum Einschränken der möglichen Typen bereit, die durch einen Typparameter ersetzt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="fa85c-244">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="fa85c-245">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="fa85c-245">Next steps</span></span>

<span data-ttu-id="fa85c-246">Nachdem Sie alle Typen gesehen haben, die die Q #-Sprache bilden, können Sie [in q # Ausdrücke eingeben](xref:microsoft.quantum.guide.expressions) , um zu erfahren, wie Sie Ausdrücke dieser verschiedenen Typen erstellen und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fa85c-246">Now that you've seen all the types which comprise the Q# language, you can head to [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to see how to create and manipulate expressions of these various types.</span></span>


