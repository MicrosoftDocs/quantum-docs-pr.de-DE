---
title: 'F #-Typmodell | Microsoft-Dokumentation'
description: Q#-Typmodell
author: QuantumWriter
uid: microsoft.quantum.language.type-model
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 4e251053d1b8306bf8956314d8099e95c56bce55
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184745"
---
# <a name="the-type-model"></a><span data-ttu-id="0d6a5-103">Das Typmodell</span><span class="sxs-lookup"><span data-stu-id="0d6a5-103">The Type Model</span></span>

<span data-ttu-id="0d6a5-104">In diesem Abschnitt wird das Q # Type-Modell erläutert und die Syntax zum Angeben von und arbeiten mit Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-104">This section lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>
<span data-ttu-id="0d6a5-105">Beachten Sie, dass Q # eine *stark typisierte* Sprache ist, sodass der Compiler durch eine sorgfältige Verwendung dieser Typen bei der Kompilierung starke Garantien für Q #-Programme bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-105">We note that Q# is a *strongly-typed* language, such that careful use of these types can help the compiler to provide strong guarantees about Q# programs at compile time.</span></span>

<span data-ttu-id="0d6a5-106">Um die bestmögliche Garantie bereitzustellen, müssen Konvertierungen zwischen Typen in Q # explizit mithilfe von Aufrufen von Funktionen erfolgen, die diese Konvertierung Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-106">In order to provide the strongest guarantees possible, conversions between types in Q# must be explicit using calls to functions which express that conversion.</span></span> <span data-ttu-id="0d6a5-107">Eine Vielzahl solcher Funktionen werden als Teil des <xref:microsoft.quantum.convert>-Namespace bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-107">A variety of such functions are provided as a part of the <xref:microsoft.quantum.convert> namespace.</span></span>
<span data-ttu-id="0d6a5-108">Auf der anderen Seite werden Upcasts zu kompatiblen Typen implizit durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-108">Upcasts to compatible types on the other hand happen implicitly.</span></span> 

<span data-ttu-id="0d6a5-109">Q # stellt beide primitiven Typen bereit, die direkt verwendet werden können, und eine Vielzahl von Möglichkeiten, um neue Typen aus anderen Typen zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-109">Q# provides both primitive types, which can be used directly, and a variety of ways to produce new types from other types.</span></span>
<span data-ttu-id="0d6a5-110">Diese werden im restlichen Teil dieses Abschnitts beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-110">We describe each in the rest of this section.</span></span>

## <a name="primitive-types"></a><span data-ttu-id="0d6a5-111">Primitive Typen</span><span class="sxs-lookup"><span data-stu-id="0d6a5-111">Primitive Types</span></span>

<span data-ttu-id="0d6a5-112">Die Sprache Q # stellt mehrere *primitive Typen*bereit, von denen andere Typen erstellt werden können:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-112">The Q# language provides several *primitive types*, from which other types can be constructed:</span></span>

- <span data-ttu-id="0d6a5-113">Der `Int`-Typ stellt eine 64-Bit-Ganzzahl mit Vorzeichen dar, z. b.: `2`, `107`, `-5`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-113">The `Int` type represents a 64-bit signed integer, e.g.: `2`, `107`, `-5`.</span></span>
- <span data-ttu-id="0d6a5-114">Der `BigInt`-Typ stellt eine Ganzzahl mit Vorzeichen beliebiger Größe dar, z. b. `2L`, `107L``-5L`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-114">The `BigInt` type represents a signed integer of arbitrary size, e.g. `2L`, `107L`, `-5L`.</span></span>
   <span data-ttu-id="0d6a5-115">Dieser Typ basiert auf der .net-<xref:System.Numerics.BigInteger></span><span class="sxs-lookup"><span data-stu-id="0d6a5-115">This type is based on the .NET <xref:System.Numerics.BigInteger></span></span>
   <span data-ttu-id="0d6a5-116">Sorte.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-116">type.</span></span>
- <span data-ttu-id="0d6a5-117">Der `Double`-Typ stellt eine Gleit Komma Zahl mit doppelter Genauigkeit dar, z. b.: `0.0`, `-1.3`, `4e-7`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-117">The `Double` type represents a double-precision floating-point number, e.g.: `0.0`, `-1.3`, `4e-7`.</span></span>
- <span data-ttu-id="0d6a5-118">Der `Bool`-Typ stellt einen booleschen Wert dar, der entweder `true` oder `false`sein kann.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-118">The `Bool` type represents a Boolean value which can either be `true` or `false`.</span></span>
- <span data-ttu-id="0d6a5-119">Der `Qubit` Typ stellt ein Quantum-Bit oder ein Qubit dar.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-119">The `Qubit` type represents a quantum bit or qubit.</span></span>
   <span data-ttu-id="0d6a5-120">`Qubit`s sind für den Benutzer nicht transparent. der einzige Vorgang, der mit Ihnen möglich ist, und nicht an einen anderen Vorgang zu übergeben, besteht darin, auf Identity (Gleichheit) zu testen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-120">`Qubit`s are opaque to the user; the only operation possible with them, other than passing them to another operation, is to test for identity (equality).</span></span>
   <span data-ttu-id="0d6a5-121">Letztendlich werden Aktionen auf `Qubit`s implementiert, indem systeminterne Anweisungen für einen Quantum-Prozessor (oder eine Simulation) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-121">Ultimately, actions on `Qubit`s are implemented by calling intrinsic instructions on a quantum processor (or a simulation thereof).</span></span>
- <span data-ttu-id="0d6a5-122">Der `Pauli`-Typ stellt einen der vier Single-Qubit-Pauli-Operatoren dar.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-122">The `Pauli` type represents one of the four single-qubit Pauli operators.</span></span>
   <span data-ttu-id="0d6a5-123">Dieser Typ wird verwendet, um den Basis Vorgang für Drehungen anzugeben und um die zu messende Observable anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-123">This type is used to denote the base operation for rotations and to specify the observable being measured.</span></span>
   <span data-ttu-id="0d6a5-124">Dabei handelt es sich um einen enumerierten Typ, der über vier mögliche Werte verfügt: `PauliI`, `PauliX`, `PauliY`und `PauliZ`, bei denen es sich um Konstanten vom Typ `Pauli`handelt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-124">This is an enumerated type that has four possible values: `PauliI`, `PauliX`, `PauliY`, and `PauliZ`, which are constants of type `Pauli`.</span></span>
- <span data-ttu-id="0d6a5-125">Der `Result` Typ stellt das Ergebnis einer Messung dar.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-125">The `Result` type represents the result of a measurement.</span></span>
   <span data-ttu-id="0d6a5-126">Dabei handelt es sich um einen enumerierten Typ mit zwei möglichen Werten: `One` und `Zero`, bei denen es sich um Konstanten vom Typ `Result`handelt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-126">This is an enumerated type with two possible values: `One` and `Zero`, which are constants of type `Result`.</span></span>
   <span data-ttu-id="0d6a5-127">`Zero` gibt an, dass der Eigen Wert + 1 gemessen wurde. `One` gibt den eigen Wert-1 an.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-127">`Zero` indicates that the +1 eigenvalue was measured; `One` indicates the -1 eigenvalue.</span></span>
- <span data-ttu-id="0d6a5-128">Der `Range`-Typ stellt eine Sequenz von ganzen Zahlen dar, die durch `start.step.stop`bezeichnet wird, wobei der Schritt "Optionen" angibt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-128">The `Range` type represents a sequence of integers, denoted by `start..step..stop`, where denoting the step is options.</span></span> 
   <span data-ttu-id="0d6a5-129">Dies ist `start . stop` der `start.1.stop`entspricht, und z. b. `1.2.7` die Sequenz $\{1, 3, 5, 7\}$ darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-129">That is `start .. stop` corresponds to `start..1..stop`, and e.g. `1..2..7` represents the sequence $\{1, 3, 5, 7\}$.</span></span>
- <span data-ttu-id="0d6a5-130">Der `String`-Typ ist eine Sequenz von Unicode-Zeichen, die für den Benutzer nach der Erstellung nicht transparent ist.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-130">The `String` type is a sequence of Unicode characters that is opaque to the user once created.</span></span>
  <span data-ttu-id="0d6a5-131">Dieser Typ wird verwendet, um Nachrichten an einen klassischen Host zu melden, wenn ein Fehler oder ein Diagnose Ereignis vorliegt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-131">This type is used to report messages to a classical host in the case of an error or diagnostic event.</span></span>
- <span data-ttu-id="0d6a5-132">Der `Unit` Typ ist der Typ, der nur einen Wert `()`zulässt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-132">The `Unit` type is the type that allows only one value `()`.</span></span> 
  <span data-ttu-id="0d6a5-133">Dieser Typ wird verwendet, um anzugeben, dass die Q #-Funktion oder der-Vorgang keine Informationen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-133">This type is used to indicate that Q# function or operation returns no information.</span></span> 

<span data-ttu-id="0d6a5-134">Die Konstanten `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`und `Zero` sind alle reservierten Symbole in f #.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-134">The constants `true`, `false`, `PauliI`, `PauliX`, `PauliY`, `PauliZ`, `One`, and `Zero` are all reserved symbols in Q#.</span></span>

## <a name="array-types"></a><span data-ttu-id="0d6a5-135">Array Typen</span><span class="sxs-lookup"><span data-stu-id="0d6a5-135">Array Types</span></span>

<span data-ttu-id="0d6a5-136">Bei jedem gültigen Q #-`'T`gibt es einen Typ, der ein Array von Werten des Typs "`'T`" darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-136">Given any valid Q# type `'T`, there is a type that represents an array of values of type `'T`.</span></span>
<span data-ttu-id="0d6a5-137">Dieser Arraytyp wird als `'T[]`dargestellt. beispielsweise `Qubit[]` oder `Int[][]`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-137">This array type is represented as `'T[]`; for example, `Qubit[]` or `Int[][]`.</span></span>
<span data-ttu-id="0d6a5-138">Beispielsweise wird eine Auflistung von ganzen Zahlen als `Int[]`bezeichnet, während ein Array von Arrays mit `(Bool, Pauli)` Werten `(Bool, Pauli)[][]`angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-138">For instance, a collection of integers is denoted `Int[]`, while an array of arrays of `(Bool, Pauli)` values is denoted `(Bool, Pauli)[][]`.</span></span>

<span data-ttu-id="0d6a5-139">Beachten Sie im zweiten Beispiel, dass dies eine potenziell Jagged Array von Arrays und kein rechteckiges zweidimensionales Array darstellt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-139">In the second example, note that this represents a potentially jagged array of arrays, and not a rectangular two-dimensional array.</span></span>
<span data-ttu-id="0d6a5-140">Q # bietet keine Unterstützung für rechteckige mehrdimensionale Arrays.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-140">Q# does not provide support for rectangular multi-dimensional arrays.</span></span>

<span data-ttu-id="0d6a5-141">Ein Arraywert kann in Q #-Quellcode mithilfe von eckigen Klammern um die Elemente eines Arrays geschrieben werden, wie in `[PauliI, PauliX, PauliY, PauliZ]`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-141">An array value can be written in Q# source code by using square brackets around the elements of an array, as in `[PauliI, PauliX, PauliY, PauliZ]`.</span></span>
<span data-ttu-id="0d6a5-142">Der Typ eines Arrayliterals hängt von dem allgemeinen Basistyp aller Elemente im Array ab.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-142">The type of an array literal is determined by the common base type of all items in the array.</span></span> 

> [!WARNING]
> <span data-ttu-id="0d6a5-143">Die Elemente eines Arrays können nicht geändert werden, nachdem das Array erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-143">The elements of an array cannot be changed after the array has been created.</span></span>
> <span data-ttu-id="0d6a5-144">Die Anweisungen Update-und-REASSIGN und/oder Copy-und-Update-Ausdrücke können zum Erstellen eines geänderten Arrays verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-144">Update-and-reassign statements and/or copy-and-update expressions can be used to construct a modified array.</span></span>

<span data-ttu-id="0d6a5-145">Alternativ kann ein Array mit dem `new`-Schlüsselwort aus seiner Größe erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-145">Alternatively, an array can be created from its size using the `new` keyword:</span></span>

```qsharp
let zeros = new Int[13];
// new also allows for creating empty arrays:
let emptyRegister = new Qubit[0];
```

<span data-ttu-id="0d6a5-146">Wenn ein Array erstellt wurde, kann in beiden Fällen die Core-Funktion `Length` zum Abrufen der Anzahl von Elementen als `Int`verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-146">In either case, once an array has been constructed, the core function `Length` can be used to obtain the number of elements as an `Int`.</span></span>
<span data-ttu-id="0d6a5-147">Arrays können mithilfe von eckigen Klammern abonniert werden, wobei entweder der Typ `Int` oder der Typ `Range`ist, um entweder einzelne Elemente oder neue Arrays zu erhalten, die eine Teilmenge der Elemente eines Arrays enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-147">Arrays can be subscripted using square brackets, with subscripts either having type `Int` or type `Range`, to obtain either single elements or new arrays containing a subset of the elements of an array.</span></span>
<span data-ttu-id="0d6a5-148">Die Indizes von Arrays sind NULL basiert:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-148">The subscripts of arrays are zero-based:</span></span>

```qsharp
let arr = [10, 11, 36, 49];
let ten = arr[0]; // 10
let odds = arr[1..2..4]; // [11, 49]
```

## <a name="tuple-types"></a><span data-ttu-id="0d6a5-149">Tupeltypen</span><span class="sxs-lookup"><span data-stu-id="0d6a5-149">Tuple Types</span></span>

<span data-ttu-id="0d6a5-150">Wenn 0 (null) oder mehr unterschiedliche Typen `T0`, `T1`,..., `Tn`, kann ein neuer *tupeltyp* als `(T0, T1, ..., Tn)`bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-150">Given zero or more different types `T0`, `T1`, ..., `Tn`, we can denote a new  *tuple type* as `(T0, T1, ..., Tn)`.</span></span>
<span data-ttu-id="0d6a5-151">Die Typen, die zum Erstellen eines neuen tupeltyps verwendet werden, können selbst Tupel sein, wie in `(Int, (Qubit, Qubit))`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-151">The types used to construct a new tuple type can themselves be tuples, as in `(Int, (Qubit, Qubit))`.</span></span>
<span data-ttu-id="0d6a5-152">Eine solche Schachtelung ist jedoch immer begrenzt, da Tupeltypen unter keinen Umständen selbst enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-152">Such nesting is always finite, however, as tuple types cannot under any circumstances contain themselves.</span></span>

<span data-ttu-id="0d6a5-153">Werte des neuen tupeltyps sind Tupel, die durch Sequenz von Werten aus jedem Typ im Tupel gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-153">Values of the new tuple type are tuples formed by sequences of values from each type in the tuple.</span></span>
<span data-ttu-id="0d6a5-154">`(3, false)` ist beispielsweise ein Tupel, dessen Typ der tupeltyp `(Int, Bool)`ist.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-154">For instance, `(3, false)` is a tuple whose type is the tuple type `(Int, Bool)`.</span></span>
<span data-ttu-id="0d6a5-155">Es ist möglich, Arrays von Tupeln, Tupeln von Arrays, Tupeln von subtupeln usw. zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-155">It is possible to create arrays of tuples, tuples of arrays, tuples of sub-tuples, etc.</span></span>

<span data-ttu-id="0d6a5-156">Ab Q # 0,3 ist `Unit` der Name des *Typs* des leeren Tupels. `()` wird für den leeren *tupelwert*verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-156">As of Q# 0.3, `Unit` is the name of the *type* of the empty tuple; `()` is used for the empty tuple *value*.</span></span>

<span data-ttu-id="0d6a5-157">Tupelinstanzen sind unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-157">Tuple instances are immutable.</span></span>
<span data-ttu-id="0d6a5-158">Q # stellt keinen Mechanismus zum Ändern des Inhalts eines Tupels bereit, nachdem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-158">Q# does not provide a mechanism to change the contents of a tuple once created.</span></span>

<span data-ttu-id="0d6a5-159">Tupel sind ein leistungsfähiges Konzept, das in Q # verwendet wird, um Werte in einem einzelnen Wert zusammenzufassen, sodass Sie einfacher zu übergeben sind.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-159">Tuples are a powerful concept used throughout Q# to collect values together into a single value, making it easier to pass them around.</span></span>
<span data-ttu-id="0d6a5-160">Insbesondere mithilfe von tupelnotation können wir ausdrücken, dass jeder Vorgang und Callable genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-160">In particular, using tuple notation, we can express that every operation and callable takes exactly one input and returns exactly one output.</span></span>

### <a name="singleton-tuple-equivalence"></a><span data-ttu-id="0d6a5-161">Äquivalenz für Singleton-Tupel</span><span class="sxs-lookup"><span data-stu-id="0d6a5-161">Singleton Tuple Equivalence</span></span>

<span data-ttu-id="0d6a5-162">Es ist möglich, ein Singleton-Tupel (Single-Element) zu erstellen, `('T1)`, z. b. `(5)` oder `([1,2,3])`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-162">It is possible to create a singleton (single-element) tuple, `('T1)`, such as `(5)` or `([1,2,3])`.</span></span>
<span data-ttu-id="0d6a5-163">Q # behandelt jedoch ein Singleton-Tupel als vollständig Äquivalent zu einem Wert des eingeschlossenen Typs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-163">However, Q# treats a singleton tuple as completely equivalent to a value of the enclosed type.</span></span>
<span data-ttu-id="0d6a5-164">Das heißt, es gibt keinen Unterschied zwischen `5` und `(5)`bzw. zwischen `5` und `(((5)))`oder zwischen `(5, (6))` und `(5, 6)`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-164">That is, there is no difference between `5` and `(5)`, or between `5` and `(((5)))`, or between `(5, (6))` and `(5, 6)`.</span></span>

<span data-ttu-id="0d6a5-165">Diese Äquivalenz gilt für alle Zwecke, einschließlich Zuweisung und Ausdrücke.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-165">This equivalence applies for all purposes, including assignment and expressions.</span></span>
<span data-ttu-id="0d6a5-166">Es ist ebenso gültig, `(5)+3` als zu schreiben, um `5+3`zu schreiben, und beide Ausdrücke werden zu `8`ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-166">It is just as valid to write `(5)+3` as to write `5+3`, and both expressions will evaluate to `8`.</span></span>
<span data-ttu-id="0d6a5-167">Dies bedeutet insbesondere, dass ein Vorgang oder eine Funktion, deren Eingabetyp oder Ausgabetyp ein Feld hat, sich als ein einzelnes Argument oder einen einzelnen Wert vorstellen kann.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-167">In particular, this means that an operation or function whose input tuple or output tuple type has one field can be thought of as taking a single argument or returning a single value.</span></span>

<span data-ttu-id="0d6a5-168">Diese Eigenschaft wird als Übereinstimmung mit einem _Singleton-Tupel_bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-168">We refer to this property as _singleton tuple equivalence_.</span></span>

## <a name="user-defined-types"></a><span data-ttu-id="0d6a5-169">Benutzerdefinierte Typen</span><span class="sxs-lookup"><span data-stu-id="0d6a5-169">User-Defined Types</span></span>

<span data-ttu-id="0d6a5-170">Eine Q #-Datei kann einen neuen benannten Typ definieren, der einen einzelnen Wert eines beliebigen Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-170">A Q# file may define a new named type containing a single value of any legal type.</span></span>
<span data-ttu-id="0d6a5-171">Für jeden tupeltyp `T`können wir einen neuen benutzerdefinierten Typ deklarieren, bei dem es sich um einen Untertyp von `T` mit der `newtype`-Anweisung handelt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-171">For any tuple type `T`, we can declare a new user-defined type that is a subtype of `T` with the `newtype` statement.</span></span>
<span data-ttu-id="0d6a5-172">Im @"microsoft.quantum.canon" Namespace sind komplexe Zahlen beispielsweise als benutzerdefinierter Typ definiert:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-172">In the @"microsoft.quantum.canon" namespace, for instance, complex numbers are defined as a user-defined type:</span></span>

```qsharp
newtype Complex = (Double, Double);
```

<span data-ttu-id="0d6a5-173">Mit dieser Anweisung wird ein neuer Typ mit zwei anonymen Elementen vom Typ "`Double`" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-173">This statement creates a new type with two anonymous items of type `Double`.</span></span>   
<span data-ttu-id="0d6a5-174">Abgesehen von anonymen Elementen unterstützen benutzerdefinierte Typen auch benannte Elemente ab Q # Version 0,7 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-174">Aside from anonymous items, user defined types also support named items as of Q# version 0.7 or higher.</span></span> <span data-ttu-id="0d6a5-175">Beispielsweise könnten wir den `Re` für das Double benennen, das den Realteil einer komplexen Zahl darstellt, und `Im` für den imaginären Teil:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-175">For example, we could have named the to items `Re` for the double representing the real part of a complex number and `Im` for the imaginary part:</span></span> 

```qsharp
newtype Complex = (Re : Double, Im : Double);
```
<span data-ttu-id="0d6a5-176">Das Benennen eines Elements in einem benutzerdefinierten Typ impliziert nicht, dass alle Elemente benannt werden müssen. eine beliebige Kombination aus benannten und unbenannten Elementen wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-176">Naming one item in a user defined type does not imply that all items need to be named - any combination of named and unnamed items is supported.</span></span> <span data-ttu-id="0d6a5-177">Darüber hinaus können auch innere Elemente benannt werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-177">Furthermore, also inner items may be named.</span></span>
<span data-ttu-id="0d6a5-178">Der Typ `Nested`, wie unten definiert, verfügt über einen zugrunde liegenden Typ `(Double, (Int, String))`, von dem nur das Element des Typs `Int` benannt wird und alle anderen Elemente anonym sind.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-178">The type `Nested` as defined below for example has an underlying type `(Double, (Int, String))`, of which only the item of type `Int` is named and all other items are anonymous.</span></span> 

```qsharp
newtype Nested = (Double, (ItemName : Int, String)); 
```
<span data-ttu-id="0d6a5-179">Benannte Elemente haben den Vorteil, dass direkt über den Zugriffs Operator `::`auf Sie zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-179">Named items have the advantage that they can be accessed directly via the access operator `::`.</span></span> 

```qsharp
function Addition (c1 : Complex, c2 : Complex) : Complex {
    return Complex(c1::Re + c2::Re, c1::Im + c2::Im);
}
```

<span data-ttu-id="0d6a5-180">Um auf anonyme Elemente zugreifen zu können, muss der umschließende Wert zuerst mithilfe des Postfix-Operators `!`extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-180">In order to access anonymous items on the other hand, the wrapped value first needs to be extracted using the postfix operator `!`.</span></span>
<span data-ttu-id="0d6a5-181">Der Unwrap-Operator (`!`) ermöglicht das Extrahieren des Werts, der in einem benutzerdefinierten Typ enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-181">The "unwrap" operator, `!`, allows to extract the value contained in a user defined type.</span></span>
<span data-ttu-id="0d6a5-182">Der Typ eines solchen "Unwrap"-Ausdrucks ist der zugrunde liegende Typ des benutzerdefinierten Typs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-182">The type of such an "unwrap" expression is the underlying type of the user defined type.</span></span> 

```qsharp
function PrintMsg (value : Nested) : Unit {
    let (d, (_, str)) = value!;
    Message ($"{str}, value: {d}");
}
```

<span data-ttu-id="0d6a5-183">Der Unwrap-Operator entpackt genau eine Ebene der Umbruch.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-183">The unwrap operator unwraps exactly one layer of wrapping.</span></span>
<span data-ttu-id="0d6a5-184">Mehrere Unwrap-Operatoren können verwendet werden, um auf einen multipliziert-umschließenden Wert zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-184">Multiple unwrap operators may be used to access a multiply-wrapped value.</span></span>

<span data-ttu-id="0d6a5-185">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-185">For instance:</span></span>

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

<span data-ttu-id="0d6a5-186">Weitere Informationen finden Sie im Abschnitt über die [Unwrap-Ausdrücke](xref:microsoft.quantum.language.expressions#unwrap-expressions) und die [Operatorrangfolge](xref:microsoft.quantum.language.expressions#operator-precedence) .</span><span class="sxs-lookup"><span data-stu-id="0d6a5-186">Take a look at the section on [unwrap expressions](xref:microsoft.quantum.language.expressions#unwrap-expressions) and [operators precedence](xref:microsoft.quantum.language.expressions#operator-precedence) for more details.</span></span>

<span data-ttu-id="0d6a5-187">Werte eines benutzerdefinierten Typs können erstellt werden, indem der entsprechende Typkonstruktor aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-187">Values of a user defined type can be created by calling the corresponding type constructor:</span></span>

```
let realUnit = Complex(1.0, 0.0);
let imaginaryUnit = Complex(0.0, 1.0);
```

<span data-ttu-id="0d6a5-188">Alternativ können neue Werte mithilfe von [Ausdrücken zum Kopieren und aktualisieren](xref:microsoft.quantum.language.expressions#copy-and-update-expressions)aus vorhandenen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-188">Alternatively, new values can be created from existing ones using [copy-and-update expressions](xref:microsoft.quantum.language.expressions#copy-and-update-expressions).</span></span> <span data-ttu-id="0d6a5-189">Wie bei Arrays Kopieren solche Ausdrücke alle Element Werte des ursprünglichen Ausdrucks, mit Ausnahme der angegebenen benannten Elemente.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-189">Like for arrays, such expressions copy all item values of the original expression, with the exception of the specified named items.</span></span> <span data-ttu-id="0d6a5-190">Für diese werden die Werte auf die Werte festgelegt, die auf der rechten Seite des Ausdrucks definiert sind.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-190">For these the values are set to the ones defined on the right hand side of the expression.</span></span> <span data-ttu-id="0d6a5-191">Alle anderen Sprachkonstrukte, wie z. b. [Update-und-REASSIGN-Anweisungen](xref:microsoft.quantum.language.statements#update-and-reassign-statement), die für Array Elemente verfügbar sind, sind auch für benannte Elemente in benutzerdefinierten Typen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-191">Any other language constructs, like for example [update-and-reassign statements](xref:microsoft.quantum.language.statements#update-and-reassign-statement), that are available for array items exist for named-items in user defined types as well.</span></span>

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

<span data-ttu-id="0d6a5-192">Benutzerdefinierte Typen können überall dort verwendet werden, wo jeder andere Typ verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-192">User-defined types may be used anywhere any other type may be used.</span></span>
<span data-ttu-id="0d6a5-193">Insbesondere ist es möglich, ein Array eines benutzerdefinierten Typs zu definieren und einen benutzerdefinierten Typ als Element eines tupeltyps einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-193">In particular, it is possible to define an array of a user-defined type and to include a user-defined type as an element of a tuple type.</span></span>

<span data-ttu-id="0d6a5-194">Es ist nicht möglich, rekursive Typstrukturen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-194">It is not possible to create recursive type structures.</span></span>
<span data-ttu-id="0d6a5-195">Das heißt, der Typ, der einen benutzerdefinierten Typ definiert, darf kein tupeltyp sein, der ein Element des benutzerdefinierten Typs enthält.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-195">That is, the type that defines a user-defined type may not be a tuple type that includes an element of the user-defined type.</span></span>
<span data-ttu-id="0d6a5-196">Im Allgemeinen haben benutzerdefinierte Typen möglicherweise keine zyklischen Abhängigkeiten, sodass der folgende Satz von Typdefinitionen unzulässig wäre:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-196">More generally, user-defined types may not have cyclic dependencies on each other, so the following set of type definitions would be illegal:</span></span>

```qsharp
newtype TypeA = (Int, TypeB);
newtype TypeB = (Double, TypeC);
newtype TypeC = (TypeA, Range);
```

<span data-ttu-id="0d6a5-197">Zusätzlich zur Bereitstellung kurzer Aliase für potenziell komplizierte Tupeltypen ist ein wesentlicher Vorteil der Definition solcher Typen, dass Sie die Absicht eines bestimmten Werts dokumentieren können.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-197">In addition to providing short aliases for potentially complicated tuple types, one significant advantage of defining such types is that they can document the intent of a particular value.</span></span>
<span data-ttu-id="0d6a5-198">Wenn Sie zum Beispiel `Complex`zurückkehren, können Sie auch 2D-Polarkoordinaten als benutzerdefinierten Typ definieren:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-198">Returning to the example of `Complex`, one could have also defined 2D polar coordinates as a user-defined type:</span></span>

```qsharp
newtype Polar = (Radius : Double, Phase : Double);
```

<span data-ttu-id="0d6a5-199">Obwohl sowohl `Complex` als auch `Polar` beide über einen zugrunde liegenden Typ `(Double, Double)`verfügen, sind die beiden Typen in f # vollständig inkompatibel. Dadurch wird das Risiko minimiert, dass versehentlich eine komplexe mathematische Funktion mit Polarkoordinaten aufgerufen wird und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-199">Even though both `Complex` and `Polar` are both have an underlying type `(Double, Double)`, the two types are wholly incompatible in Q#, minimizing the risk of accidentally calling a complex math function with polar coordinates and vice versa.</span></span>
<span data-ttu-id="0d6a5-200">Auf diese Weise haben benutzerdefinierte Typen eine ähnliche Rolle wie Datensätze in F# z. b.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-200">In this way, user-defined types have a similar role as Records in F# for example.</span></span> 


## <a name="operation-and-function-types"></a><span data-ttu-id="0d6a5-201">Vorgangs-und Funktionstypen</span><span class="sxs-lookup"><span data-stu-id="0d6a5-201">Operation and Function Types</span></span>

<span data-ttu-id="0d6a5-202">Ein f #- _Vorgang_ ist eine Quantum-Unterroutine.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-202">A Q# _operation_ is a quantum subroutine.</span></span>
<span data-ttu-id="0d6a5-203">Dies bedeutet, dass es sich um eine aufrufbare Routine handelt, die Quantenvorgänge enthält.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-203">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="0d6a5-204">Eine Q #- _Funktion_ ist eine klassische Unterroutine, die innerhalb eines Quantum-Algorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-204">A Q# _function_ is a classical subroutine used within a quantum algorithm.</span></span>
<span data-ttu-id="0d6a5-205">Sie kann klassischen Code, aber keine Quantum-Vorgänge enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-205">It may contain classical code but no quantum operations.</span></span>
<span data-ttu-id="0d6a5-206">Insbesondere können Funktionen keine Qubits zuordnen oder ausleihen, und Sie können auch keine Vorgänge aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-206">Specifically, functions may not allocate or borrow qubits, nor may they call operations.</span></span>
<span data-ttu-id="0d6a5-207">Es ist jedoch möglich, dass Sie Vorgänge oder Qubits für die Verarbeitung übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-207">It is possible, however, to pass them operations or qubits for processing.</span></span>
<span data-ttu-id="0d6a5-208">Funktionen sind daher vollständig deterministisch, da der Aufruf mit denselben Argumenten immer dasselbe Ergebnis erzeugt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-208">Functions are thus entirely deterministic in the sense that calling them with the same arguments will always produce the same result.</span></span> 

<span data-ttu-id="0d6a5-209">Vorgänge und Funktionen werden kombiniert als _callables_bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-209">Together, operations and functions are called _callables_.</span></span>  <span data-ttu-id="0d6a5-210">Einige [Beispiele hierfür](#examples) finden Sie unten.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-210">You can see some [examples](#examples) of these below.</span></span>

<span data-ttu-id="0d6a5-211">Alle f #-callables werden als Eingabe betrachtet und geben einen einzelnen Wert als Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-211">All Q# callables are considered to take a single value as input and return a single value as output.</span></span>
<span data-ttu-id="0d6a5-212">Sowohl der Eingabe-als auch der Ausgabewert können Tupel sein.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-212">Both the input and output values may be tuples.</span></span>
<span data-ttu-id="0d6a5-213">Callables ohne Ergebnis Rückgabe `Unit`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-213">Callables that have no result return `Unit`.</span></span>
<span data-ttu-id="0d6a5-214">Callables ohne Eingabe nehmen das leere Tupel als Eingabe auf.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-214">Callables that have no input take the empty tuple as input.</span></span>

<span data-ttu-id="0d6a5-215">Der Basistyp für beliebige Callable wird als `('Tinput => 'Tresult)` oder `('Tinput -> 'Tresult)`geschrieben, wobei sowohl `'Tinput` als auch `'Tresult` Typen sind.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-215">The basic type for any callable is written as `('Tinput => 'Tresult)` or `('Tinput -> 'Tresult)`, where both `'Tinput` and `'Tresult` are types.</span></span>
<span data-ttu-id="0d6a5-216">Das erste Formular, mit `=>`, wird für-Vorgänge verwendet. Das zweite Formular mit `->`für Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-216">The first form, with `=>`, is used for operations; the second form, with `->`, for functions.</span></span>
<span data-ttu-id="0d6a5-217">`((Qubit, Pauli) => Result)` stellt z. b. die Signatur für einen möglichen Single-Qubit-Messvorgang dar.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-217">For example, `((Qubit, Pauli) => Result)` represents the signature for a possible single-qubit measurement operation.</span></span>

<span data-ttu-id="0d6a5-218">Funktionstypen werden vollständig durch ihre Signatur angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-218">Function types are completely specified by their signature.</span></span>
<span data-ttu-id="0d6a5-219">Eine Funktion, die den Sinus eines Winkels berechnet, hätte z. b. den Typ `(Double -> Double)`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-219">For example, a function that computes the sine of an angle would have type `(Double -> Double)`.</span></span>

<span data-ttu-id="0d6a5-220">Vorgänge – aber keine Funktionen – verfügen über bestimmte zusätzliche _Eigenschaften_ , die als Teil des Vorgangs Typs ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-220">Operations—but not functions—have certain additional _characteristics_ that are expressed as part of the operation type.</span></span> <span data-ttu-id="0d6a5-221">Zu diesen Merkmalen zählen Informationen darüber, welche Funktions tüktoren der Vorgang unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-221">Such characteristics include information about what functors the operation supports.</span></span>
<span data-ttu-id="0d6a5-222">Funktoren sind metaoperationen, die eine Spezialisierung eines Basis Vorgangs generieren. Weitere Informationen finden Sie [unten unter.](#functors)</span><span class="sxs-lookup"><span data-stu-id="0d6a5-222">Functors are meta-operations that generate a specialization of a base operation; see [Functors](#functors), below.</span></span>

<span data-ttu-id="0d6a5-223">Vorgangs Typen werden durch den Eingabetyp, den Ausgabetyp und deren Merkmale angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-223">Operation types are specified by the their input type, output type, and their characteristics.</span></span>    
<span data-ttu-id="0d6a5-224">Um Unterstützung für den `Controlled`-und/oder `Adjoint`-Funktions tüktor in einem Vorgangstyp zu benötigen, müssen wir eine Anmerkung hinzufügen, die die entsprechenden Merkmale angibt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-224">In order to require support for the `Controlled` and/or `Adjoint` functor in an operation type, we need to add an annotation indicating the corresponding characteristics.</span></span>
<span data-ttu-id="0d6a5-225">Eine Anmerkung `is Ctl` z. b. gibt an, dass der Vorgang steuerbar ist.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-225">An annotation `is Ctl` for example indicates that the operation is controllable.</span></span> <span data-ttu-id="0d6a5-226">Wenn Sie festlegen möchten, dass ein Vorgang dieses Typs sowohl das `Adjoint`-als auch das `Controlled`-Funktor unterstützt, können wir dies als `(Qubit => Unit is Adj + Ctl)`Ausdrücken.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-226">If we want to require that an operation of that type supports both the `Adjoint` and `Controlled` functor we can express this as `(Qubit => Unit is Adj + Ctl)`.</span></span> <span data-ttu-id="0d6a5-227">Die verwendeten Vorgangs Merkmale `Adj` und `Ctl` streng genommen sind zwei vordefinierte Sätze von Bezeichnungen, wobei jede Bezeichnung eine bestimmte Vorgangs Merkmale angibt, z. b. Unterstützung für ein bestimmtes Funktor.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-227">The used operation characteristics `Adj` and `Ctl` strictly speaking are two pre-defined sets of labels, where each label indicates a particular operation characteristics like e.g. support for a particular functor.</span></span>
<span data-ttu-id="0d6a5-228">Daher wird `+` verwendet, um die Kombination dieser beiden Mengen anzugeben, und `*` verwendet, um die Schnittmenge anzugeben, d. h. die Bezeichnungen, die beide Sätze gemeinsam haben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-228">Hence, `+` is used to indicate the union of those two sets, and `*` is used to indicate the intersection - i.e. the labels that are common to both sets.</span></span>  

<span data-ttu-id="0d6a5-229">Der Pauli-`X` Vorgang hat z. b. den Typ `(Qubit => Unit is Adj + Ctl)`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-229">For example, the Pauli `X` operation has type `(Qubit => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="0d6a5-230">Ein Vorgangstyp, der keine Funktions tüktoren unterstützt, wird von seinem Eingabe-und Ausgabetyp allein angegeben, ohne dass zusätzliche Anmerkungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-230">An operation type that does not support any functors is specified by its input and output type alone, with no additional annotation.</span></span>


### <a name="type-parameterized-functions-and-operations"></a><span data-ttu-id="0d6a5-231">Typparametrisierte Funktionen und Vorgänge</span><span class="sxs-lookup"><span data-stu-id="0d6a5-231">Type-Parameterized Functions and Operations</span></span>

<span data-ttu-id="0d6a5-232">Aufruf Bare Typen können Typparameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-232">Callable types may contain type parameters.</span></span>
<span data-ttu-id="0d6a5-233">Typparameter werden durch ein Symbol angegeben, das ein einzelnes Anführungszeichen als Präfix hat. Beispielsweise ist `'A` ein gültiger Typparameter.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-233">Type parameters are indicated by a symbol prefixed by a single quote; for example, `'A` is a legal type parameter.</span></span>

<span data-ttu-id="0d6a5-234">Ein Typparameter kann in einer einzigen Signatur mehrmals vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-234">A type parameter may appear more than once in a single signature.</span></span>
<span data-ttu-id="0d6a5-235">Eine Funktion, die eine andere Funktion auf jedes Element eines Arrays anwendet und die gesammelten Ergebnisse zurückgibt, hätte z. b. eine Signatur `(('A[], 'A->'A) -> 'A[])`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-235">For example, a function that applies another function to each element of an array and returns the collected results would have signature `(('A[], 'A->'A) -> 'A[])`.</span></span>
<span data-ttu-id="0d6a5-236">Ebenso kann eine Funktion, die die Komposition von zwei Vorgängen zurückgibt, über Signatur `((('A=>'B), ('B=>'C)) -> ('A=>'C))`verfügen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-236">Similarly, a function that returns the composition of two operations might have signature `((('A=>'B), ('B=>'C)) -> ('A=>'C))`.</span></span>

<span data-ttu-id="0d6a5-237">Beim Aufrufen eines typparametrisierten Aufruf baren Typs müssen alle Argumente, die denselben Typparameter aufweisen, denselben Typ aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-237">When invoking a type-parameterized callable, all arguments that have the same type parameter must be of the same type.</span></span>

<span data-ttu-id="0d6a5-238">Q # stellt keinen Mechanismus zum Einschränken der möglichen Typen bereit, die durch einen Typparameter ersetzt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-238">Q# does not provide a mechanism for constraining the possible types that might be substituted for a type parameter.</span></span>

### <a name="type-compatibility"></a><span data-ttu-id="0d6a5-239">Typkompatibilität</span><span class="sxs-lookup"><span data-stu-id="0d6a5-239">Type Compatibility</span></span>

<span data-ttu-id="0d6a5-240">Ein Vorgang mit zusätzlichen Funktoren, die unterstützt werden, kann überall dort verwendet werden, wo ein Vorgang mit weniger Funktoren, jedoch mit derselben Signatur erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-240">An operation with additional functors supported may be used anywhere an operation with fewer functors but the same signature is expected.</span></span>
<span data-ttu-id="0d6a5-241">Beispielsweise kann ein Vorgang des Typs `(Qubit => Unit is Adj)` überall dort verwendet werden, wo ein Vorgang des Typs `(Qubit => Unit)` erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-241">For instance, an operation of type `(Qubit => Unit is Adj)` may be used anywhere an operation of type `(Qubit => Unit)` is expected.</span></span>

<span data-ttu-id="0d6a5-242">Q # ist kovariant in Bezug auf Aufruf Bare Rückgabe Typen: ein Aufruf bares Element, das einen Typ zurückgibt `'A` ist mit einem Aufruf baren mit dem gleichen Eingabetyp und einem Ergebnistyp kompatibel, mit dem `'A` kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-242">Q# is covariant with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that `'A` is compatible with.</span></span>

<span data-ttu-id="0d6a5-243">Q # ist in Bezug auf Eingabetypen kontra Variant: ein Aufruf barer, der einen Typ `'A` als Eingabe annimmt, ist mit einem Aufruf baren mit demselben Ergebnistyp und einem Eingabetyp kompatibel, der mit `'A`kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-243">Q# is contravariant with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="0d6a5-244">Das heißt, dass die folgenden Definitionen gegeben sind:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-244">That is, given the following definitions:</span></span>

```qsharp
operation Invertible (qs : Qubit[]) : Unit 
is Adj {...} 
operation Unitary (qs : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertibleWith (
   inner: (Qubit[] => Unit is Adj),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith (
   inner: (Qubit[] => Unit is Adj + Ctl),
   outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="0d6a5-245">Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-245">the following are true:</span></span>

- <span data-ttu-id="0d6a5-246">Der Vorgang `ConjugateInvertibleWith` kann mit einem `inner`-Argument entweder `Invertible` oder `Unitary`aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-246">The operation `ConjugateInvertibleWith` may be invoked with an `inner` argument of either `Invertible` or `Unitary`.</span></span>
- <span data-ttu-id="0d6a5-247">Der Vorgang `ConjugateUnitaryWith` kann mit einem `inner`-Argument `Unitary`aufgerufen werden, jedoch nicht mit `Invertible`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-247">The operation `ConjugateUnitaryWith` may be invoked with an `inner` argument of `Unitary`, but not `Invertible`.</span></span>
- <span data-ttu-id="0d6a5-248">Ein Wert vom Typ "`(Qubit[] => Unit is Adj + Ctl)`" kann von `ConjugateInvertibleWith`zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-248">A value of type `(Qubit[] => Unit is Adj + Ctl)` may be returned from `ConjugateInvertibleWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d6a5-249">F # 0,3 führt einen signifikanten Unterschied im Verhalten von benutzerdefinierten Typen ein.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-249">Q# 0.3 introduces a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="0d6a5-250">Benutzerdefinierte Typen werden als umschließende Version des zugrunde liegenden Typs und nicht als Untertyp behandelt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-250">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="0d6a5-251">Dies bedeutet, dass ein Wert eines benutzerdefinierten Typs nicht verwendbar ist, wenn ein Wert des zugrunde liegenden Typs erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-251">This means that a value of a user-defined type is not usable where a value of the underlying type is expected.</span></span>

### <a name="functors"></a><span data-ttu-id="0d6a5-252">Funktionselemente</span><span class="sxs-lookup"><span data-stu-id="0d6a5-252">Functors</span></span>

<span data-ttu-id="0d6a5-253">Ein Funktor in Q # ist eine Factory, die einen neuen Vorgang aus einem anderen Vorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-253">A functor in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="0d6a5-254">Funktoren haben Zugriff auf die Implementierung des Basis Vorgangs, wenn die Implementierung des neuen Vorgangs definiert wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-254">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="0d6a5-255">Daher können Funktoren komplexere Funktionen als herkömmliche Funktionen höherer Ebene ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-255">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span>

<span data-ttu-id="0d6a5-256">Funktoren haben keine Darstellung im Q #-Typsystem.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-256">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="0d6a5-257">Daher ist es derzeit nicht möglich, Sie an eine Variable zu binden oder Sie als Argumente zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-257">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="0d6a5-258">Ein Funktor wird verwendet, indem er auf einen Vorgang angewendet und ein neuer Vorgang zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-258">A functor is used by applying it to an operation, returning a new operation.</span></span>
<span data-ttu-id="0d6a5-259">Beispielsweise wird der Vorgang, der sich aus der Anwendung des `Adjoint`-funktors auf den `Y` Vorgang ergibt, als `Adjoint Y`geschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-259">For example, the operation that results from applying the `Adjoint` functor to the `Y` operation is written as `Adjoint Y`.</span></span>
<span data-ttu-id="0d6a5-260">Der neue Vorgang kann dann wie jeder andere Vorgang aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-260">The new operation may then be invoked like any other operation.</span></span>
<span data-ttu-id="0d6a5-261">Folglich wendet `Adjoint Y(q1)` das Adjoint-Funktor auf den `Y` Vorgang an, um einen neuen Vorgang zu generieren, und wendet diesen neuen Vorgang auf `q1`an.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-261">Thus, `Adjoint Y(q1)` applies the Adjoint functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>

<span data-ttu-id="0d6a5-262">Entsprechend wendet `Controlled X(controls, target)` den gesteuerten Funktor auf den `X` Vorgang an, um einen neuen Vorgang zu generieren, und wendet diesen neuen Vorgang auf `controls` und `target`an.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-262">Similarly, `Controlled X(controls, target)` applies the Controlled functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

<span data-ttu-id="0d6a5-263">Die zwei standardfunktoren in Q # sind `Adjoint` und `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-263">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

#### <a name="adjoint"></a><span data-ttu-id="0d6a5-264">Adjoint</span><span class="sxs-lookup"><span data-stu-id="0d6a5-264">Adjoint</span></span>

<span data-ttu-id="0d6a5-265">Bei Quantum Computing ist das Adjoint eines Vorgangs die komplexe konjugierte Operation des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-265">In quantum computing, the adjoint of an operation is the complex conjugate transpose of the operation.</span></span>
<span data-ttu-id="0d6a5-266">Bei Vorgängen, die einen einheitlichen Operator implementieren, ist das Adjoint das Gegenteil des Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-266">For operations that implement a unitary operator, the adjoint is the inverse of the operation.</span></span>
<span data-ttu-id="0d6a5-267">Bei einem einfachen Vorgang, bei dem nur eine Sequenz anderer einheitlicher Vorgänge für einen Satz von Qubits aufgerufen wird, kann das Adjoint durch Anwenden der adjoints der unter Vorgänge auf die gleichen Qubits in umgekehrter Reihenfolge berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-267">For a simple operation that just invokes a sequence of other unitary operations on a set of qubits, the adjoint may be computed by applying the adjoints of the sub-operations on the same qubits, in the reverse sequence.</span></span>

<span data-ttu-id="0d6a5-268">Bei einem Vorgangs Ausdruck kann ein neuer Vorgangs Ausdruck mithilfe des `Adjoint`-funktors gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-268">Given an operation expression, a new operation expression may be formed using the `Adjoint` functor.</span></span>
<span data-ttu-id="0d6a5-269">Beispielsweise `Adjoint QFT` den Adjoint-Vorgang des `QFT` Vorgangs fest.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-269">For instance, `Adjoint QFT` designates the adjoint of the `QFT` operation.</span></span>
<span data-ttu-id="0d6a5-270">Der neue Vorgang hat dieselbe Signatur und denselben Typ wie der Basis Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-270">The new operation has the same signature and type as the base operation.</span></span>
<span data-ttu-id="0d6a5-271">Insbesondere ermöglicht der neue Vorgang auch das `Adjoint`und lässt `Controlled` nur dann zu, wenn der Basis Vorgang durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-271">In particular, the new operation also allows `Adjoint`, and will allow `Controlled` if and only if the base operation did.</span></span>

<span data-ttu-id="0d6a5-272">Der Adjoint-Funktor ist eine eigene Umkehrung. Das heißt, `Adjoint Adjoint Op` ist immer identisch mit `Op`.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-272">The Adjoint functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled"></a><span data-ttu-id="0d6a5-273">Klimatisiert</span><span class="sxs-lookup"><span data-stu-id="0d6a5-273">Controlled</span></span>

<span data-ttu-id="0d6a5-274">Bei der kontrollierten Version eines Vorgangs handelt es sich um einen neuen Vorgang, der den Basis Vorgang effektiv anwendet, wenn sich alle Steuerelement-Qubits in einem angegebenen Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-274">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="0d6a5-275">Wenn sich die Steuerelement-Qubits in der superposition befinden, wird der Basis Vorgang einheitlich auf den entsprechenden Teil der superposition angewendet.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-275">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="0d6a5-276">Folglich werden kontrollierte Vorgänge häufig zum Generieren von entanglement verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-276">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="0d6a5-277">In Q # nehmen kontrollierte Versionen immer ein Array von Steuerelement-Qubits auf, und der angegebene Status ist immer, damit alle Steuerelement-Qubits im Berechnungs Zustand (`PauliZ`) `One`, $ \ket{1}$.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-277">In Q#, controlled versions always take an array of control qubits, and the specified state is always for all of the control qubits to be in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
<span data-ttu-id="0d6a5-278">Das Steuern auf der Grundlage anderer Zustände kann erreicht werden, indem der entsprechende einheitliche Vorgang auf die Steuerungs Qubits vor dem kontrollierten Vorgang angewendet und dann nach dem kontrollierten Vorgang die Umkehrung des einheitlichen Vorgangs angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-278">Controlling based on other states may be achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
<span data-ttu-id="0d6a5-279">Wenn Sie z. b. einen `X` Vorgang auf ein Steuerelement Qubit vor und nach einer kontrollierten Operation anwenden, bewirkt dies, dass der Vorgang den `Zero` Zustand ($ \ket{0}$) für dieses Qubit steuert. Wenn Sie einen `H` Vorgang vor und nach anwenden, wird die `PauliX` `One` Status gesteuert, d. h.-1 eigen Wert von Pauli X, $ \ket{-} \mathrel{: =} (\ket{0}-\ket{1})/\sqrt{2}$ und nicht der `PauliZ` `One` Status.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-279">For example, applying an `X` operation to a control qubit before and after a controlled operation will cause the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after will control on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="0d6a5-280">Bei einem Vorgangs Ausdruck kann ein neuer Vorgangs Ausdruck mithilfe des `Controlled`-funktors gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-280">Given an operation expression, a new operation expression may be formed using the `Controlled` functor.</span></span>
<span data-ttu-id="0d6a5-281">Die Signatur des neuen Vorgangs basiert auf der Signatur des ursprünglichen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-281">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="0d6a5-282">Der Ergebnistyp ist identisch, aber der Eingabetyp ist ein zwei Tupel mit einem Qubit-Array, das die Steuerelement-Qubit (s) als erstes Element und die Argumente des ursprünglichen Vorgangs als zweites Element enthält.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-282">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="0d6a5-283">Der neue-Vorgang unterstützt `Controlled`und unterstützt `Adjoint` nur dann, wenn der ursprüngliche Vorgang durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-283">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="0d6a5-284">Wenn für den ursprünglichen Vorgang nur ein einzelnes Argument verwendet wurde, wird hier die entsprechgabe von Singleton-Tupeln berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-284">If the original operation took only a single argument, then singleton tuple equivalence will come into play here.</span></span>
<span data-ttu-id="0d6a5-285">Beispielsweise ist `Controlled X` die gesteuerte Version des `X` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-285">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span>
<span data-ttu-id="0d6a5-286">`X` hat den Typ `(Qubit => Unit is Adj + Ctl)`, sodass `Controlled X` den Typ `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`hat. aufgrund der Übereinstimmung mit einem Singleton-Tupel ist dies mit `((Qubit[], Qubit) => Unit is Adj + Ctl)`identisch.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-286">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="0d6a5-287">Wenn der Basis Vorgang mehrere Argumente benötigt hat, denken Sie daran, die entsprechenden Argumente der kontrollierten Version des Vorgangs in Klammern einzuschließen, um Sie in ein Tupel zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-287">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="0d6a5-288">Beispielsweise ist `Controlled Rz` die gesteuerte Version des `Rz` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-288">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span>
<span data-ttu-id="0d6a5-289">`Rz` hat den Typ `((Double, Qubit) => Unit is Adj + Ctl)`, sodass `Controlled Rz` den Typ `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`hat.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-289">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="0d6a5-290">Daher ist `Controlled Rz(controls, (0.1, target))` ein gültiger Aufruf `Controlled Rz` (Beachten Sie die Klammern um `0.1, target`).</span><span class="sxs-lookup"><span data-stu-id="0d6a5-290">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="0d6a5-291">Als weiteres Beispiel können `CNOT(control, target)` als `Controlled X([control], target)`implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-291">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="0d6a5-292">Wenn ein Ziel von 2 Steuerungs Qubits (ccnot) gesteuert werden soll, können wir `Controlled X([control1, control2], target)`-Anweisung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-292">If a target should be controlled by 2 control qubits (CCNOT), we can use `Controlled X([control1, control2], target)` statement.</span></span>

### <a name="examples"></a><span data-ttu-id="0d6a5-293">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d6a5-293">Examples</span></span>

<span data-ttu-id="0d6a5-294">Dieses Beispiel für einen Q #-Vorgang stammt aus dem [Mess](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-294">This example of a Q# operation comes from the [Measurement](https://github.com/microsoft/Quantum/tree/master/samples/getting-started/measurement) sample.</span></span> <span data-ttu-id="0d6a5-295">Innerhalb von Vorgängen können wir Qubits zuordnen und Quantum-Vorgänge für diese Qubits verwenden, wie z. b. `H` und `X`:</span><span class="sxs-lookup"><span data-stu-id="0d6a5-295">Within operations, we can allocate qubits and use quantum operations on those qubits such as `H` and `X`:</span></span>

```qsharp
/// # Summary
/// Prepares a state and measures it in the Pauli-Z basis.
operation MeasureOneQubit () : Result {
        mutable result = Zero;

        using (qubit = Qubit()) { // Allocate a qubit
            H(qubit);               // Use a quantum operation on that qubit

            set result = M(qubit);      // Measure the qubit

            if (result == One) {    // Reset the qubit so that it can be released
                X(qubit);
            }

            return result;
        }
 }
```

<span data-ttu-id="0d6a5-296">Dieses Beispiel für eine Funktion stammt aus dem [phaseschätzungsbeispiel](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) .</span><span class="sxs-lookup"><span data-stu-id="0d6a5-296">This example of a function comes from the [PhaseEstimation](https://github.com/microsoft/Quantum/tree/master/samples/characterization/phase-estimation) sample.</span></span> <span data-ttu-id="0d6a5-297">Sie enthält reinen klassischen Code.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-297">It contains purely classical code.</span></span> <span data-ttu-id="0d6a5-298">Sie können sehen, dass im Gegensatz zum obigen Beispiel keine Qubits zugeordnet sind und keine Quantum-Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-298">You can see that, unlike the example above, no qubits are allocated, and no quantum operations are used.</span></span>


```qsharp
/// # Summary
/// Given two arrays, returns a new array that is the pointwise product
/// of each of the given arrays.
function MultiplyPointwise (left : Double[], right : Double[]) : Double[] {
    mutable product = new Double[Length(left)];

    for (idxElement in IndexRange(left)) {
        set product w/= idxElement <- left[idxElement] * right[idxElement];
    }
    return product;
}
```

<span data-ttu-id="0d6a5-299">Es ist auch möglich, dass für eine Funktion Qubits für die Verarbeitung übergeben werden, wie in diesem Beispiel aus dem Beispiel " [reversiblelogicsynthese](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) ".</span><span class="sxs-lookup"><span data-stu-id="0d6a5-299">It is also possible for a function to be passed qubits for processing, as in this example from the [ReversibleLogicSynthesis](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/reversible-logic-synthesis) sample.</span></span> <span data-ttu-id="0d6a5-300">Qubits werden an die Funktion geleitet und zur Verarbeitung verwendet, obwohl die Qubit-Zustände zu keinem Zeitpunkt geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0d6a5-300">Qubits are passed to the function and used for processing, although at no point are the qubit states themselves modified.</span></span>

```qsharp
/// # Summary
/// Translate MCT masks into multiple-controlled Toffoli gates (with single
/// targets).
function GateMasksToToffoliGates (qubits : Qubit[], masks : MCMTMask[]) : MCTGate[] {

    mutable result = new MCTGate[0];
    let n = Length(qubits);

    for (i in 0 .. Length(masks) - 1) {
        let (controls, targets) = (masks[i])!;
        let controlBits = IntegerBits(controls, n);
        let targetBits = IntegerBits(targets, n);
        let cQubits = Subarray(controlBits, qubits);
        let tQubits = Subarray(targetBits, qubits);

        for (target in tQubits) {
            set result += [MCTGate(cQubits, target)];
        }
    }

    return result;
}
```
