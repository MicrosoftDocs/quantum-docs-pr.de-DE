---
title: 'Typen in Q#'
description: 'Erfahren Sie mehr über die verschiedenen Typen, die in der Q# Programmiersprache verwendet werden.'
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.types
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 349138984387cc564cca18ea09c7bf161524b0b6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691622"
---
# <a name="types-in-no-locq"></a><span data-ttu-id="a58b7-103">Typen in Q#</span><span class="sxs-lookup"><span data-stu-id="a58b7-103">Types in Q#</span></span>

<span data-ttu-id="a58b7-104">In diesem Artikel werden das Q# Typmodell und die Syntax zum Angeben von und arbeiten mit Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a58b7-104">This article describes the Q# type model and the syntax for specifying and working with types.</span></span> <span data-ttu-id="a58b7-105">Ausführliche Informationen zum Erstellen und Verarbeiten von Ausdrücken dieser Typen finden Sie unter [typausdrücke](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="a58b7-105">For details on how to create and operate on expressions of these types, see [Type Expressions](xref:microsoft.quantum.guide.expressions).</span></span>

<span data-ttu-id="a58b7-106">Beachten Sie, dass Q# eine *stark typisierte* Sprache ist, sodass der Compiler durch eine sorgfältige Verwendung dieser Typen bei der Kompilierung starke Garantien für Programme bereitstellen kann Q# .</span><span class="sxs-lookup"><span data-stu-id="a58b7-106">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>
<span data-ttu-id="a58b7-107">Um die bestmöglichen Garantien zu gewährleisten, müssen Konvertierungen zwischen Typen in Q# explizit mithilfe von Aufrufen von Funktionen erfolgen, die diese Konvertierung Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="a58b7-107">To provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> 
<span data-ttu-id="a58b7-108">Q# stellt eine Vielzahl solcher Funktionen als Teil des- <xref:Microsoft.Quantum.Convert> Namespace bereit.</span><span class="sxs-lookup"><span data-stu-id="a58b7-108">Q# provides a variety of such functions as a part of the <xref:Microsoft.Quantum.Convert> namespace.</span></span>
<span data-ttu-id="a58b7-109">Auf der anderen Seite werden Upcasts in kompatible Typen implizit durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-109">Upcasts to compatible types, on the other hand, happen implicitly.</span></span> 

<span data-ttu-id="a58b7-110">Q# stellt beide primitiven Typen bereit, die direkt verwendet werden, und eine Vielzahl von Möglichkeiten, um neue Typen aus anderen Typen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="a58b7-110">Q# provides both primitive types, which are used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="a58b7-111">Wir beschreiben alle in den restlichen Abschnitten dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="a58b7-111">We describe each in the rest of this article.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="a58b7-112">Primitive Typen</span><span class="sxs-lookup"><span data-stu-id="a58b7-112">Primitive Types</span></span>

<span data-ttu-id="a58b7-113">Die Q# Sprache stellt die folgenden *primitiven Typen* bereit, die Sie alle direkt in Programmen verwenden können Q# .</span><span class="sxs-lookup"><span data-stu-id="a58b7-113">The Q# language provides the following *primitive types* , all of which you can use directly in Q# programs.</span></span> <span data-ttu-id="a58b7-114">Sie können diese primitiven Typen auch verwenden, um neue Typen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-114">You can also use these primitive types to construct new types.</span></span>

- <span data-ttu-id="a58b7-115">Der- `Int` Typ stellt eine 64-Bit-Ganzzahl mit Vorzeichen dar, z `2` . b., `107` , `-5` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-115">The `Int` type represents a 64-bit signed integer, for example, `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="a58b7-116">Der- `BigInt` Typ stellt eine Ganzzahl mit Vorzeichen beliebiger Größe dar, z `2L` . b., `107L` , `-5L` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-116">The `BigInt` type represents a signed integer of arbitrary size, for example, `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="a58b7-117">Dieser Typ basiert auf .net. <xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="a58b7-117">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="a58b7-118">umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-118">type.</span></span>

- <span data-ttu-id="a58b7-119">Der `Double` -Typ stellt eine Gleit Komma Zahl mit doppelter Genauigkeit dar, z `0.0` . b `-1.3` .,, `4e-7` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-119">The `Double` type represents a double-precision floating-point number, for example, `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="a58b7-120">Der- `Bool` Typ stellt einen booleschen Wert von `true` oder dar `false` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-120">The `Bool` type represents a Boolean value of either `true` or `false`.</span></span>
- <span data-ttu-id="a58b7-121">Der- `Range` Typ stellt eine Sequenz von ganzen Zahlen dar, die durch angegeben wird, `start..step..stop` wobei der Schritt optional ist.</span><span class="sxs-lookup"><span data-stu-id="a58b7-121">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is optional.</span></span> 
   <span data-ttu-id="a58b7-122">Beispielsweise `start .. stop` entspricht `start..1..stop` , und `1..2..7` stellt die Sequenz $ \{ 1, 3, 5, 7 $ dar \} .</span><span class="sxs-lookup"><span data-stu-id="a58b7-122">For example, `start .. stop` corresponds to `start..1..stop`, and `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="a58b7-123">Der- `String` Typ ist eine Sequenz von Unicode-Zeichen, die für den Benutzer nach der Erstellung nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="a58b7-123">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="a58b7-124">Verwenden Sie den- `string` Typ, um Meldungen bei einem Fehler oder einem Diagnose Ereignis an einen klassischen Host zu melden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-124">Use the `string` type to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="a58b7-125">Der- `Unit` Typ kann nur einen Wert,, aufweisen `()` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-125">The `Unit` type can have only one value, `()`.</span></span> 
  <span data-ttu-id="a58b7-126">Verwenden Sie diesen Typ, um anzugeben, dass eine Q# Funktion oder ein Vorgang keine Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-126">Use this type to indicate that a Q# function or operation returns no information.</span></span> 
- <span data-ttu-id="a58b7-127">Der- `Qubit` Typ stellt ein Quantum-Bit oder Qubit dar.</span><span class="sxs-lookup"><span data-stu-id="a58b7-127">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="a58b7-128">`Qubit`e sind für den Benutzer nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="a58b7-128">`Qubit`s are opaque to the user.</span></span> <span data-ttu-id="a58b7-129">Der einzige Vorgang, der mit Ihnen möglich ist, und nicht an einen anderen Vorgang zu übergeben, besteht darin, auf Identity (Gleichheit) zu testen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-129">The only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="a58b7-130">Letztendlich implementieren Sie Aktionen in, indem Sie systeminterne `Qubit` Anweisungen für einen Quantum-Prozessor (oder einen Quantum-Simulator) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-130">Ultimately, you implement actions on `Qubit`s by calling intrinsic instructions on a quantum processor (or a quantum simulator).</span></span>
- <span data-ttu-id="a58b7-131">Der- `Pauli` Typ stellt einen der vier Single-Qubit-Pauli-Operatoren dar.</span><span class="sxs-lookup"><span data-stu-id="a58b7-131">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="a58b7-132">Verwenden Sie diesen Typ, um den Basis Vorgang für Drehungen anzugeben und um die zu messende Observable anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a58b7-132">Use this type to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="a58b7-133">Dabei handelt es sich um einen enumerierten Typ, der über vier mögliche Werte verfügt: `PauliI` , `PauliX` , `PauliY` und `PauliZ` , bei denen es sich um Konstanten des Typs handelt `Pauli` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-133">It is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="a58b7-134">Der- `Result` Typ stellt das Ergebnis einer Messung dar.</span><span class="sxs-lookup"><span data-stu-id="a58b7-134">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="a58b7-135">Dabei handelt es sich um einen enumerierten Typ mit zwei möglichen Werten: und, bei denen es sich um `One` `Zero` Konstanten vom Typ handelt `Result` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-135">It is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="a58b7-136">`Zero` Gibt an, dass der Eigen Wert + 1 gemessen wurde. Gibt an, dass `One` der Eigen Wert-1 gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="a58b7-136">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue was measured.</span></span>

<span data-ttu-id="a58b7-137">Die Konstanten `true` , `false` , `PauliI` ,,, `PauliX` `PauliY` `PauliZ` , `One` und `Zero` sind reservierte Symbole in Q# .</span><span class="sxs-lookup"><span data-stu-id="a58b7-137">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="a58b7-138">Arraytypen</span><span class="sxs-lookup"><span data-stu-id="a58b7-138">Array Types</span></span>

* <span data-ttu-id="a58b7-139">Für jeden gültigen Q# Typ gibt es einen Typ, der ein Array von Werten dieses Typs darstellt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-139">For any valid Q# type, there is a type that represents an array of values of that type.</span></span>
    <span data-ttu-id="a58b7-140">Beispielsweise `Qubit[]` stellen und Werte `(Bool, Pauli)[]` Arrays `Qubit` und `(Bool, Pauli)` Tupelwerte dar.</span><span class="sxs-lookup"><span data-stu-id="a58b7-140">For example, `Qubit[]` and `(Bool, Pauli)[]` represent arrays of `Qubit` values and `(Bool, Pauli)` tuple values.</span></span>

* <span data-ttu-id="a58b7-141">Ein Array von Arrays ist ebenfalls gültig.</span><span class="sxs-lookup"><span data-stu-id="a58b7-141">An array of arrays is also valid.</span></span> <span data-ttu-id="a58b7-142">Im vorherigen Beispiel wird ein Array von `(Bool, Pauli)` Arrays bezeichnet `(Bool, Pauli)[][]` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-142">Expanding on the previous example, an array of `(Bool, Pauli)` arrays is denoted `(Bool, Pauli)[][]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="a58b7-143">Dieses Beispiel `(Bool, Pauli)[][]` stellt eine potenziell Jagged Array von Arrays und kein rechteckiges zweidimensionales Array dar.</span><span class="sxs-lookup"><span data-stu-id="a58b7-143">This example, `(Bool, Pauli)[][]`, represents a potentially jagged array of arrays and not a rectangular two-dimensional array.</span></span> <span data-ttu-id="a58b7-144">Q# unterstützt keine rechteckigen mehrdimensionalen Arrays.</span><span class="sxs-lookup"><span data-stu-id="a58b7-144">Q# does not support rectangular multi-dimensional arrays.</span></span>

* <span data-ttu-id="a58b7-145">Ein Arraywert kann im Q# Quellcode mithilfe von eckigen Klammern um die Elemente eines Arrays geschrieben werden, wie in `[PauliI, PauliX, PauliY, PauliZ]` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-145">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="a58b7-146">Der allgemeine Basistyp aller Elemente im Array bestimmt den Typ eines Arrayliterals.</span><span class="sxs-lookup"><span data-stu-id="a58b7-146">The common base type of all items in the array determines the type of an array literal.</span></span> <span data-ttu-id="a58b7-147">Daher löst das Erstellen eines Arrays mit Elementen, die keinen gemeinsamen Basistyp aufweisen, einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="a58b7-147">Hence, constructing an array with elements that have no common base type raises an error.</span></span>  
<span data-ttu-id="a58b7-148">Ein Beispiel finden Sie unter [Arrays von callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span><span class="sxs-lookup"><span data-stu-id="a58b7-148">For an example, see [arrays of callables](xref:microsoft.quantum.guide.expressions#arrays-of-callables).</span></span>

    > [!WARNING]
    > <span data-ttu-id="a58b7-149">Nachdem die Elemente eines Arrays erstellt wurden, können Sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-149">Once created, the elements of an array cannot be changed.</span></span>
    > <span data-ttu-id="a58b7-150">Verwenden Sie zum Erstellen eines geänderten Arrays die [Anweisungen Update-und-REASSIGN](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) oder [Copy-and-Update-Ausdrücke](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span><span class="sxs-lookup"><span data-stu-id="a58b7-150">To construct a modified array, use [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements) or [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span>

* <span data-ttu-id="a58b7-151">Alternativ kann ein Array mit dem-Schlüsselwort aus seiner Größe erstellt werden `new` :</span><span class="sxs-lookup"><span data-stu-id="a58b7-151">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

    ```qsharp
    let zeros = new Int[13];
    // you can also use new for creating empty arrays:
    let emptyRegister = new Qubit[0];
    ```

* <span data-ttu-id="a58b7-152">Verwenden Sie die Core-Funktion `Length` , um die Anzahl der Elemente aus einem Array als abzurufen `Int` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-152">Use the core function `Length` to obtain the number of elements from an array as an `Int`.</span></span>
* <span data-ttu-id="a58b7-153">Arrays können abonniert werden, um entweder einzelne Elemente oder neue Arrays zu erhalten, die eine Teilmenge der Elemente eines Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="a58b7-153">Arrays can be subscripted to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="a58b7-154">Die Indexwerte von Arrays sind NULL basiert und müssen vom Typ `Int` oder vom Typ sein `Range` :</span><span class="sxs-lookup"><span data-stu-id="a58b7-154">The subscripts of arrays are zero-based and must be type `Int` or type `Range`:</span></span>

    ```qsharp
    let arr = [10, 11, 36, 49];
    let ten = arr[0]; // 10
    let odds = arr[1..2..4]; // [11, 49]
    ```

## <a name="tuple-types"></a><span data-ttu-id="a58b7-155">Tupeltypen</span><span class="sxs-lookup"><span data-stu-id="a58b7-155">Tuple Types</span></span>

<span data-ttu-id="a58b7-156">Tupel sind ein leistungsstarkes Konzept, das in der gesamten verwendet wird Q# , um Werte in einem einzelnen Wert zusammenzufassen, sodass es einfacher ist, Sie zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="a58b7-156">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="a58b7-157">Insbesondere mithilfe von tupelnotation können Sie Ausdrücken, dass jeder Vorgang und Callable genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-157">In particular, using tuple notation, you can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

* <span data-ttu-id="a58b7-158">Wenn 0 (null) oder mehr unterschiedliche Typen,,..., angezeigt wird, `T0` `T1` `Tn` können Sie einen neuen  *tupeltyp* als angeben `(T0, T1, ..., Tn)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-158">Given zero or more different types `T0`, `T1`, ..., `Tn`, you can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="a58b7-159">Die Typen, die zum Erstellen eines neuen tupeltyps verwendet werden, können selbst Tupel sein, wie in `(Int, (Qubit, Qubit))` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-159">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="a58b7-160">Eine solche Schachtelung ist jedoch immer begrenzt, da Tupeltypen unter keinen Umständen selbst enthalten.</span><span class="sxs-lookup"><span data-stu-id="a58b7-160">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

* <span data-ttu-id="a58b7-161">Die Werte des neuen tupeltyps sind Tupel, die durch Sequenz von Werten aus jedem Typ im Tupel gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-161">The values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="a58b7-162">Beispielsweise `(3, false)` ist ein Tupel, dessen Typ der tupeltyp ist `(Int, Bool)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-162">For example, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="a58b7-163">Es ist möglich, Arrays von Tupeln, Tupeln von Arrays, Tupeln von subtupeln usw. zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-163">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, and so on.</span></span>

* <span data-ttu-id="a58b7-164">Ab Q# 0,3 ist `Unit` der Name des *Typs* des leeren Tupels; `()` wird für den *Wert* des leeren Tupels verwendet.</span><span class="sxs-lookup"><span data-stu-id="a58b7-164">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the *value* of the empty tuple.</span></span>

* <span data-ttu-id="a58b7-165">Tupelinstanzen sind unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="a58b7-165">Tuple instances are immutable.</span></span>
<span data-ttu-id="a58b7-166">Q# bietet keinen Mechanismus zum Ändern des Inhalts eines Tupels, nachdem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a58b7-166">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>



### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="a58b7-167">Äquivalenz für Singleton-Tupel</span><span class="sxs-lookup"><span data-stu-id="a58b7-167">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="a58b7-168">Es ist möglich, ein Singleton-Tupel (Einzelelement) zu erstellen `('T1)` , z `(5)` `([1,2,3])` . b. oder.</span><span class="sxs-lookup"><span data-stu-id="a58b7-168">It is possible to create a singleton (single-element) tuple `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="a58b7-169">Behandelt jedoch Q# ein Singleton-Tupel als äquivalent zu einem Wert des eingeschlossenen Typs.</span><span class="sxs-lookup"><span data-stu-id="a58b7-169">However, Q# treats a singleton tuple as equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="a58b7-170">Das heißt, es gibt keinen Unterschied zwischen `5` und `(5)` bzw `5` . zwischen und `(((5)))` oder zwischen `(5, (6))` und `(5, 6)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-170">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>
<span data-ttu-id="a58b7-171">Es ist ebenso gültig, wie geschrieben zu werden, `(5)+3` da `5+3` beide Ausdrücke als ausgewertet werden `8` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-171">It is just as valid to write `(5)+3` as it is to write `5+3`; both expressions evaluate to `8`.</span></span>

<span data-ttu-id="a58b7-172">Diese Äquivalenz gilt für alle Zwecke, einschließlich Zuweisung und Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="a58b7-172">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="a58b7-173">Bei jedem Ausdruck ist derselbe Ausdruck, der in Klammern eingeschlossen ist, ein Ausdruck desselben Typs.</span><span class="sxs-lookup"><span data-stu-id="a58b7-173">Given any expression, that same expression enclosed in parentheses is an expression of the same type.</span></span>
<span data-ttu-id="a58b7-174">Beispielsweise `(7)` ist ein Ausdruck vom Typ `Int` , `([1,2,3])` ist ein Ausdruck vom Typ `Int[]` , und `((1,2))` ist ein Ausdruck vom Typ `(Int, Int)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-174">For example, `(7)` is an expression of type `Int`, `([1,2,3])` is an expression of type `Int[]`, and `((1,2))` is an expression of type `(Int, Int)`.</span></span>

<span data-ttu-id="a58b7-175">Dies bedeutet insbesondere, dass Sie einen Vorgang oder eine Funktion anzeigen können, deren Eingabe-Tupel oder ausgabetupeltyp ein Feld hat, das ein einzelnes Argument annimmt oder einen einzelnen Wert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-175">In particular, this means that you can view an operation or function whose input tuple or output tuple type has one field as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="a58b7-176">Diese Eigenschaft wird als Übereinstimmung mit einem _Singleton-Tupel_ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a58b7-176">We refer to this property as _singleton tuple equivalence_ .</span></span>


## <a name="user-defined-types"></a><span data-ttu-id="a58b7-177">Benutzerdefinierte Typen</span><span class="sxs-lookup"><span data-stu-id="a58b7-177">User-Defined Types</span></span>

<span data-ttu-id="a58b7-178">Eine benutzerdefinierte Typdeklaration besteht aus dem Schlüsselwort `newtype` , gefolgt vom Namen des benutzerdefinierten Typs, einer `=` , einer gültigen Typspezifikation und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="a58b7-178">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="a58b7-179">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a58b7-179">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```
    
* <span data-ttu-id="a58b7-180">Jede Q# Quelldatei kann eine beliebige Anzahl benutzerdefinierter Typen deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a58b7-180">Each Q# source file may declare any number of user-defined types.</span></span>
* <span data-ttu-id="a58b7-181">Typnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-und Funktionsnamen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-181">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>
* <span data-ttu-id="a58b7-182">Benutzerdefinierte Typen sind unterschiedlich, auch wenn die Basis Typen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a58b7-182">User-defined types are distinct, even if the base types are identical.</span></span>
<span data-ttu-id="a58b7-183">Vor allem gibt es keine automatische Konvertierung zwischen den Werten von zwei benutzerdefinierten Typen, auch wenn die zugrunde liegenden Typen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="a58b7-183">In particular, there is no automatic conversion between the values of two user-defined types, even if the underlying types are identical.</span></span>

### <a name="named-vs-anonymous-items"></a><span data-ttu-id="a58b7-184">Benannte und anonyme Elemente</span><span class="sxs-lookup"><span data-stu-id="a58b7-184">Named vs. anonymous items</span></span>

<span data-ttu-id="a58b7-185">Eine Q# Datei kann einen neuen benannten Typ definieren, der einen einzelnen Wert eines beliebigen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="a58b7-185">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="a58b7-186">Für jeden tupeltyp `T` können Sie einen neuen benutzerdefinierten Typ deklarieren, bei dem es sich um einen Untertyp von `T` mit der- `newtype` Anweisung handelt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-186">For any tuple type `T`, you can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="a58b7-187">Im- @"microsoft.quantum.math" Namespace werden z. b. komplexe Zahlen als benutzerdefinierter Typ definiert:</span><span class="sxs-lookup"><span data-stu-id="a58b7-187">In the @"microsoft.quantum.math" namespace, for example, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```
<span data-ttu-id="a58b7-188">Diese Anweisung erstellt einen neuen Typ mit zwei anonymen Elementen vom Typ `Double` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-188">This statement creates a new type with two anonymous items of type `Double`.</span></span>   

<span data-ttu-id="a58b7-189">Abgesehen von anonymen Elementen unterstützen benutzerdefinierte Typen auch *benannte Elemente* ab Q# Version 0,7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a58b7-189">Aside from anonymous items, user-defined types also support *named items* as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="a58b7-190">Beispielsweise können Sie die Elemente `Real` für das Double benennen, das den Realteil einer komplexen Zahl und `Imag` für den imaginären Teil darstellt:</span><span class="sxs-lookup"><span data-stu-id="a58b7-190">For example, you could name the items to `Real` for the double representing the real part of a complex number and `Imag` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Real : Double, Imag : Double);
```
<span data-ttu-id="a58b7-191">Das Benennen eines Elements in einem benutzerdefinierten Typ impliziert nicht, dass alle Elemente benannt werden müssen. eine beliebige Kombination aus benannten und unbenannten Elementen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-191">Naming one item in a user-defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="a58b7-192">Außerdem können innere Elemente ebenfalls benannt werden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-192">Furthermore, inner items may also be named.</span></span>
<span data-ttu-id="a58b7-193">Der Typ `Nested` , wie unten definiert, verfügt beispielsweise über einen zugrunde liegenden Typ `(Double, (Int, String))` , von dem nur das Element des Typs `Int` benannt wird und alle anderen Elemente anonym sind.</span><span class="sxs-lookup"><span data-stu-id="a58b7-193">The type `Nested`, as defined below for example, has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named, and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```

<span data-ttu-id="a58b7-194">Benannte Elemente haben den Vorteil, dass Sie direkt über den *Zugriffs Operator* darauf zugreifen können `::` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-194">Named items have the advantage that they can be accessed directly via the *access operator* `::`.</span></span> 

```qsharp
function ComplexAddition(c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Real + c2::Real, c1::Imag + c2::Imag);
}
```

<span data-ttu-id="a58b7-195">Zusätzlich zur Bereitstellung kurzer Aliase für potenziell komplizierte Tupeltypen ist ein wichtiger Vorteil beim Definieren solcher Typen, dass Sie die Absicht eines bestimmten Werts dokumentieren können.</span><span class="sxs-lookup"><span data-stu-id="a58b7-195">In addition to providing short aliases for potentially complicated tuple types, a significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="a58b7-196">Wenn Sie zum Beispiel zurückkehren `Complex` , können Sie auch eine Polar Koordinate-Neudarstellung als benutzerdefinierten Typ definieren:</span><span class="sxs-lookup"><span data-stu-id="a58b7-196">Returning to the example of `Complex`, one could have also defined a polar coordinate represenation as a user-defined type:</span></span>

```qsharp
newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```

<span data-ttu-id="a58b7-197">Obwohl sowohl `Complex` als auch `ComplexPolar` beide über einen zugrunde liegenden Typ verfügen `(Double, Double)` , sind die beiden Typen in vollständig inkompatibel Q# , wodurch das Risiko minimiert wird, dass versehentlich eine komplexe mathematische Funktion mit Polarkoordinaten aufgerufen wird und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-197">Even though both `Complex` and `ComplexPolar` both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>

#### <a name="access-anonymous-items-with-the-unwrap-operator"></a><span data-ttu-id="a58b7-198">Auf anonyme Elemente mit dem Unwrap-Operator zugreifen</span><span class="sxs-lookup"><span data-stu-id="a58b7-198">Access anonymous items with the unwrap operator</span></span>

<span data-ttu-id="a58b7-199">Wenn Sie auf anonyme Elemente zugreifen möchten, extrahieren Sie zuerst den umschließenden Wert mithilfe des Postfix-Operators `!` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-199">To access anonymous items, first extract the wrapped value using the postfix operator `!`.</span></span>
<span data-ttu-id="a58b7-200">Mit dem Operator "Unwrap" `!` können Sie den Wert extrahieren, der in einem benutzerdefinierten Typ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a58b7-200">With the "unwrap" operator, `!`, you can extract the value contained in a user-defined type.</span></span>
<span data-ttu-id="a58b7-201">Der Typ eines solchen "Unwrap"-Ausdrucks ist der zugrunde liegende Typ des benutzerdefinierten Typs.</span><span class="sxs-lookup"><span data-stu-id="a58b7-201">The type of such an "unwrap" expression is the underlying type of the user-defined type.</span></span> 

```qsharp
function PrintedMessage(value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="a58b7-202">Ein einzelner Unwrap-Operator entpackt eine umschließende Schicht.</span><span class="sxs-lookup"><span data-stu-id="a58b7-202">A single unwrap operator unwraps one layer of wrapping.</span></span> <span data-ttu-id="a58b7-203">Verwenden Sie mehrere Unwrap-Operatoren, um auf einen multipliziert umschließenden Wert zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-203">Use multiple unwrap operators to access a multiply-wrapped value.</span></span>

<span data-ttu-id="a58b7-204">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a58b7-204">For example:</span></span>

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

<span data-ttu-id="a58b7-205">Weitere Informationen zum Unwrap-Operator finden Sie unter [typausdrücke in Q# ](xref:microsoft.quantum.guide.expressions).</span><span class="sxs-lookup"><span data-stu-id="a58b7-205">For more details on the unwrap operator, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions).</span></span>

### <a name="creating-values-of-user-defined-types"></a><span data-ttu-id="a58b7-206">Erstellen von Werten für benutzerdefinierte Typen</span><span class="sxs-lookup"><span data-stu-id="a58b7-206">Creating values of user-defined types</span></span>

<span data-ttu-id="a58b7-207">Erstellen Sie Werte eines benutzerdefinierten Typs, indem Sie den entsprechenden Typkonstruktor aufrufen:</span><span class="sxs-lookup"><span data-stu-id="a58b7-207">Create values of a user-defined type by calling the corresponding type constructor:</span></span>

```qsharp
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="a58b7-208">Alternativ können Sie mithilfe von [Ausdrücken zum Kopieren und aktualisieren](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions)neue Werte aus vorhandenen Werten erstellen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-208">Alternatively, you can create new values from existing ones using [copy-and-update expressions](xref:microsoft.quantum.guide.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="a58b7-209">Ebenso wie bei Arrays kopieren Copy-und-Update-Ausdrücke alle Element Werte des ursprünglichen Ausdrucks, mit Ausnahme der angegebenen benannten Elemente.</span><span class="sxs-lookup"><span data-stu-id="a58b7-209">Just as they do with arrays, copy-and-update expressions copy all item values of the original expression, except for the specified named items.</span></span> <span data-ttu-id="a58b7-210">Für diese Ausnahmen sind die Werte dieser Elemente die Werte, die auf der rechten Seite des Ausdrucks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="a58b7-210">For these exceptions, the values of these items are the values defined on the right-hand side of the expression.</span></span> <span data-ttu-id="a58b7-211">Alle anderen Sprachkonstrukte, die für Array Elemente verfügbar sind, z. b. [Update-und-REASSIGN-Anweisungen](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), sind auch für benannte Elemente in benutzerdefinierten Typen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-211">Any other language constructs that are available for array items, for example [update-and-reassign statements](xref:microsoft.quantum.guide.variables#update-and-reassign-statements), exist for named-items in user-defined types as well.</span></span>

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

* <span data-ttu-id="a58b7-212">Sie können benutzerdefinierte Typen überall dort verwenden, wo Sie beliebige andere Typen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-212">You can use user-defined types anywhere you use any other types.</span></span>
<span data-ttu-id="a58b7-213">Insbesondere ist es möglich, ein Array eines benutzerdefinierten Typs zu definieren und einen benutzerdefinierten Typ als Element eines tupeltyps einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-213">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

* <span data-ttu-id="a58b7-214">Es ist nicht möglich, rekursive Typstrukturen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-214">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="a58b7-215">Das heißt, dass der Typ, der einen benutzerdefinierten Typ definiert, kein tupeltyp sein kann, der ein Element des benutzerdefinierten Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="a58b7-215">That is, the type that defines a user-defined type cannot be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="a58b7-216">Im Allgemeinen haben benutzerdefinierte Typen möglicherweise keine zyklischen Abhängigkeiten, sodass der folgende Satz von Typdefinitionen ungültig ist:</span><span class="sxs-lookup"><span data-stu-id="a58b7-216">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions are invalid:</span></span>

    ```qsharp
    newtype TypeA = (Int, TypeB);
    newtype TypeB = (Double, TypeC);
    newtype TypeC = (TypeA, Range);
    ```


## <a name="operation-and-function-types"></a><span data-ttu-id="a58b7-217">Vorgangs-und Funktionstypen</span><span class="sxs-lookup"><span data-stu-id="a58b7-217">Operation and Function Types</span></span>

<span data-ttu-id="a58b7-218">Mit den Typen `'Tinput` und `'Tresult` :</span><span class="sxs-lookup"><span data-stu-id="a58b7-218">Given the types `'Tinput` and `'Tresult`:</span></span>

* <span data-ttu-id="a58b7-219">`('Tinput => 'Tresult)` ist der Basistyp für jeden *Vorgang* , z `((Qubit, Pauli) => Result)` . b..</span><span class="sxs-lookup"><span data-stu-id="a58b7-219">`('Tinput => 'Tresult)` is the basic type for any *operation* , for example `((Qubit, Pauli) => Result)`.</span></span>
* <span data-ttu-id="a58b7-220">`('Tinput -> 'Tresult)` ist der Basistyp für jede *Funktion* , z `(Int -> Int)` . b..</span><span class="sxs-lookup"><span data-stu-id="a58b7-220">`('Tinput -> 'Tresult)` is the basic type for any *function* , for example `(Int -> Int)`.</span></span> 

<span data-ttu-id="a58b7-221">Diese werden als *Signatur* der aufrufenden bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a58b7-221">These are called the *signature* of the callable.</span></span>

* <span data-ttu-id="a58b7-222">Alle Q# callables nehmen einen einzelnen Wert als Eingabe an und geben einen einzelnen Wert als Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="a58b7-222">All Q# callables take a single value as input and return a single value as output.</span></span>
* <span data-ttu-id="a58b7-223">Sie können Tupel sowohl für die Eingabe-als auch für die Ausgabewerte verwenden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-223">You can use tuples for both the input and output values.</span></span>
* <span data-ttu-id="a58b7-224">Callables ohne Ergebnis geben zurück `Unit` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-224">Callables that have no result, return `Unit`.</span></span>
* <span data-ttu-id="a58b7-225">Callables ohne Eingabe nehmen das leere Tupel als Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="a58b7-225">Callables that have no input take the empty tuple as input.</span></span>

### <a name="functors"></a><span data-ttu-id="a58b7-226">Funktionselemente</span><span class="sxs-lookup"><span data-stu-id="a58b7-226">Functors</span></span>

<span data-ttu-id="a58b7-227">*Funktions* Typen werden vollständig durch ihre Signatur angegeben.</span><span class="sxs-lookup"><span data-stu-id="a58b7-227">*Function* types are completely specified by their signature.</span></span> <span data-ttu-id="a58b7-228">Eine Funktion, die den Sinus eines Winkels berechnet, hätte z. b. den Typ `(Double -> Double)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-228">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span> 

<span data-ttu-id="a58b7-229">*Vorgänge* weisen bestimmte zusätzliche Eigenschaften auf, die als Teil des Vorgangs Typs ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="a58b7-229">*Operations* have certain additional characteristics that are expressed as part of the operation type.</span></span> <span data-ttu-id="a58b7-230">Zu diesen Merkmalen zählen Informationen darüber, welche Funktions *tüktoren* der Vorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-230">Such characteristics include information about which *functors* the operation supports.</span></span>
<span data-ttu-id="a58b7-231">Wenn z. b. die Ausführung des Vorgangs auf dem Zustand anderer Qubits basiert, sollte er das `Controlled` Funktor unterstützen. wenn der Vorgang eine Umkehrung hat, sollte er das `Adjoint` Funktor unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-231">For example, if the running of the operation relies on the state of other qubits, then it should support the `Controlled` functor; if the operation has an inverse, then it should support the `Adjoint` functor.</span></span>

> [!NOTE]
> <span data-ttu-id="a58b7-232">In diesem Artikel wird nur erläutert, wie Funktoren die Vorgangs Signatur ändern.</span><span class="sxs-lookup"><span data-stu-id="a58b7-232">This article only discuss how functors alter the operation signature.</span></span> <span data-ttu-id="a58b7-233">Weitere Informationen zu Funktions tüktoren und Vorgängen finden Sie unter [Vorgänge und Q# Funktionen in ](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="a58b7-233">For more details about functors and operations, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions).</span></span> 

<span data-ttu-id="a58b7-234">Um Unterstützung für den `Controlled` -und/oder- `Adjoint` Funktions tüktor in einem Vorgangstyp zu benötigen, müssen Sie eine Anmerkung hinzufügen, die die entsprechenden Merkmale angibt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-234">To require support for the `Controlled` and/or `Adjoint` functor in an operation type, you need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="a58b7-235">Die-Anmerkung `is Ctl` (z. b. `(Qubit => Unit is Ctl)` ) gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="a58b7-235">The annotation `is Ctl` (for example, `(Qubit => Unit is Ctl)`) indicates that the operation is controllable.</span></span> <span data-ttu-id="a58b7-236">Das heißt, der Run basiert auf dem Zustand eines anderen Qubit oder Qubits.</span><span class="sxs-lookup"><span data-stu-id="a58b7-236">That is, its run relies on the state of another qubit or qubits.</span></span> <span data-ttu-id="a58b7-237">Entsprechend gibt die-Anmerkung `is Adj` an, dass der Vorgang über ein Adjoint-Zeichen verfügt, d. h., es kann "invertiert" werden, sodass das Fortsetzen eines Vorgangs und dessen Adjoint in einen Zustand den Zustand unverändert lässt.</span><span class="sxs-lookup"><span data-stu-id="a58b7-237">Similarly, the annotation `is Adj` indicates that the operation has an adjoint, that is, it can be "inverted" such that successively applying an operation and then its adjoint to a state leaves the state unchanged.</span></span> 

<span data-ttu-id="a58b7-238">Wenn Sie festlegen möchten, dass ein Vorgang dieses Typs sowohl das-als `Adjoint` auch das-Funktor unterstützt, `Controlled` können Sie dies als Ausdrücken `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-238">If you want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor you can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="a58b7-239">Der integrierte Pauli- <xref:Microsoft.Quantum.Intrinsic.X> Vorgang hat z. b. den-Typ `(Qubit => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-239">For example, the built-in Pauli <xref:Microsoft.Quantum.Intrinsic.X> operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span> 

<span data-ttu-id="a58b7-240">Ein Vorgangstyp, der keine Funktions tüktoren unterstützt, wird von seinem Eingabe-und Ausgabetyp allein angegeben, ohne dass zusätzliche Anmerkungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a58b7-240">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>

### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="a58b7-241">Type-Parameterized Funktionen und Vorgänge</span><span class="sxs-lookup"><span data-stu-id="a58b7-241">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="a58b7-242">Aufruf Bare Typen können *Typparameter* enthalten.</span><span class="sxs-lookup"><span data-stu-id="a58b7-242">Callable types may contain *type parameters* .</span></span>
<span data-ttu-id="a58b7-243">Verwenden Sie ein Symbol, das mit einem einfachen Anführungszeichen versehen ist, um einen Typparameter anzugeben. beispielsweise `'A` ist ein gültiger Typparameter.</span><span class="sxs-lookup"><span data-stu-id="a58b7-243">Use a symbol prefixed by a single quote to indicated a type parameter; for example, `'A` is a legal type parameter.</span></span>
<span data-ttu-id="a58b7-244">Weitere Informationen und Details zum Definieren von typparametrisierten Aufruf baren aufrufen finden Sie unter [Vorgänge und Funktionen in Q# ](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span><span class="sxs-lookup"><span data-stu-id="a58b7-244">For more information and details on how to define type-parameterized callables, see [Operations and Functions in Q#](xref:microsoft.quantum.guide.operationsfunctions#generic-type-parameterized-callables).</span></span>

<span data-ttu-id="a58b7-245">Ein Typparameter kann in einer einzigen Signatur mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-245">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="a58b7-246">Eine Funktion, die eine andere Funktion auf jedes Element eines Arrays anwendet und die gesammelten Ergebnisse zurückgibt, hat z. b. die Signatur `(('A[], 'A->'A) -> 'A[])` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-246">For example, a function that applies another function to each element of an array and returns the collected results has the signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="a58b7-247">Ebenso hat eine Funktion, die die Komposition von zwei Vorgängen zurückgibt, die Signatur `((('A=>'B), ('B=>'C)) -> ('A=>'C))` .</span><span class="sxs-lookup"><span data-stu-id="a58b7-247">Similarly, a function that returns the composition of two operations has the signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="a58b7-248">Wenn Sie eine typparametrisierte Aufruf Bare Aufruf Liste aufrufen, müssen alle Argumente, die denselben Typparameter aufweisen, denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-248">When you invoke a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="a58b7-249">Q# stellt keinen Mechanismus zum Einschränken der möglichen Typen bereit, die ein Benutzer für einen Typparameter ersetzen kann.</span><span class="sxs-lookup"><span data-stu-id="a58b7-249">Q# does not provide a mechanism for constraining the possible types that a user might substitute for a type parameter.</span></span>

## <a name="next-steps"></a><span data-ttu-id="a58b7-250">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="a58b7-250">Next steps</span></span>

<span data-ttu-id="a58b7-251">Nachdem Sie alle Typen gesehen haben, die die Sprache enthalten Q# , finden Sie unter [typausdrücke Q# in](xref:microsoft.quantum.guide.expressions) Informationen zum Erstellen und Bearbeiten von Ausdrücken dieser verschiedenen Typen.</span><span class="sxs-lookup"><span data-stu-id="a58b7-251">Now that you've seen all the types which comprise the Q# language, see [Type Expressions in Q#](xref:microsoft.quantum.guide.expressions) to learn how to create and manipulate expressions of these various types.</span></span>
