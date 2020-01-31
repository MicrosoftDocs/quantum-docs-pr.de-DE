---
title: 'Weitere Schritte: f #-Techniken | Microsoft-Dokumentation'
description: 'Weitere Schritte: Q #-Techniken'
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.techniques.going-further
ms.openlocfilehash: bd2b799d4001e280baccb04158247891b9cbb5bc
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820197"
---
# <a name="going-further"></a><span data-ttu-id="fdbd1-103">Weiter</span><span class="sxs-lookup"><span data-stu-id="fdbd1-103">Going Further</span></span> #

<span data-ttu-id="fdbd1-104">Nachdem Sie nun erfahren haben, wie Sie interessante Quantum-Programme in Q # schreiben, werden in diesem Abschnitt noch einige erweiterte Themen vorgestellt, die sich in Zukunft als nützlich erweisen sollten.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-104">Now that you've seen how to write interesting quantum programs in Q#, this section goes further by introducing a few more advanced topics that should prove useful going forward.</span></span>


## <a name="generic-operations-and-functions"></a><span data-ttu-id="fdbd1-105">Generische Vorgänge und Funktionen</span><span class="sxs-lookup"><span data-stu-id="fdbd1-105">Generic Operations and Functions</span></span> ##

> [!TIP]
> <span data-ttu-id="fdbd1-106">In diesem Abschnitt wird die grundlegende Vertrautheit mit [Generika C#in ](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [Generika in F# ](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [ C++ Vorlagen](https://docs.microsoft.com/cpp/cpp/templates-cpp)oder ähnlichen Ansätzen für die Metaprogrammierung in anderen Sprachen vorausgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-106">This section assumes some basic familiarity with [generics in C#](https://docs.microsoft.com/dotnet/csharp/programming-guide/generics/introduction-to-generics), [generics in F#](https://docs.microsoft.com/dotnet/fsharp/language-reference/generics/), [C++ templates](https://docs.microsoft.com/cpp/cpp/templates-cpp), or similar approaches to metaprogramming in other languages.</span></span>

<span data-ttu-id="fdbd1-107">Viele Funktionen und Vorgänge, die wir möglicherweise definieren möchten, sind nicht wirklich stark von den Typen Ihrer Eingaben abhängig, sondern verwenden nur implizit ihre Typen über eine andere Funktion oder einen anderen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-107">Many functions and operations that we might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="fdbd1-108">Sehen Sie sich beispielsweise das *Karten* Konzept an, das vielen funktionalen Sprachen gemeinsam ist. bei Angabe einer Funktion $f (x) $ und einer Auflistung von Werten $\{x_1, x_2, \dots, x_n\}$ gibt MAP eine neue Auflistung $\{f (x_1), f (x_2), \dots, f (x_n)\}$ zurück.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-108">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="fdbd1-109">Um dies in Q # zu implementieren, können wir diese Funktionen als erste Klasse nutzen.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-109">To implement this in Q#, we can take advantage of that functions are first class.</span></span>
<span data-ttu-id="fdbd1-110">Sehen wir uns ein kurzes Beispiel für `Map`an, indem wir ★ als Platzhalter verwenden, während wir herausfinden, welche Typen wir benötigen.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-110">Let's write out a quick example of `Map`, using ★ as a placeholder while we figure out what types we need.</span></span>

```qsharp
function Map(fn : ★ -> ★, values : ★[]) : ★[] {
    mutable mappedValues = new ★[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="fdbd1-111">Beachten Sie, dass diese Funktion unabhängig von den tatsächlichen Typen, die wir ersetzen, sehr gut aussieht.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-111">Note this function looks very much the same no matter what actual types we substitute in.</span></span>
<span data-ttu-id="fdbd1-112">Eine Zuordnung von Ganzzahlen zu Paulis sieht beispielsweise genauso wie eine Zuordnung von Gleit Komma Zahlen zu Zeichen folgen aus:</span><span class="sxs-lookup"><span data-stu-id="fdbd1-112">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : Int -> Pauli, values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : Double -> String, values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="fdbd1-113">Im Prinzip könnten wir eine Version von `Map` für jedes Paar von Typen schreiben, auf die wir stoßen, aber dies führt zu einer Reihe von Schwierigkeiten.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-113">In principle, we could write a version of `Map` for every pair of types that we encounter, but this introduces a number of difficulties.</span></span>
<span data-ttu-id="fdbd1-114">Wenn beispielsweise in `Map`ein Fehler gefunden wird, müssen wir sicherstellen, dass die Korrektur in allen Versionen von `Map`einheitlich angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-114">For instance, if we find a bug in `Map`, then we must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="fdbd1-115">Wenn ein neues Tupel oder ein neues UDT erstellt wird, muss nun auch eine neue `Map` erstellt werden, um zusammen mit dem neuen Typ zu gelangen.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-115">Moreover, if we construct a new tuple or UDT, then we must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="fdbd1-116">Obwohl dies für eine kleine Anzahl solcher Funktionen überlastet ist, da wir mehr und mehr Funktionen derselben Form wie `Map`erfassen, werden die Kosten für die Einführung neuer Typen in relativ kurzer Reihenfolge zu groß.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-116">While this is tractable for a small number of such functions, as we collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="fdbd1-117">Ein Großteil dieser Schwierigkeiten ergibt sich jedoch darin, dass wir dem Compiler nicht die Informationen gegeben haben, die er benötigt, um zu erkennen, wie die verschiedenen Versionen von `Map` verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-117">Much of this difficulty results, however, from that the we have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="fdbd1-118">Effektiv möchten wir, dass der Compiler `Map` als eine mathematische Funktion von q #- *Typen* zu q #-Funktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-118">Effectively, we want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>
<span data-ttu-id="fdbd1-119">Dieses Konzept wird formalisiert, indem Funktionen und Vorgänge *Typparameter*sowie ihre normalen tupelparameter enthalten können.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-119">This notion is formalized by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="fdbd1-120">In den obigen Beispielen möchten wir `Map`, dass im ersten Fall Typparameter `Int, Pauli` und im zweiten Fall `Double, String` werden.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-120">In the examples above, we wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="fdbd1-121">In den meisten Fällen können diese Typparameter so verwendet werden, als wären Sie normale Typen: Wir verwenden Werte von Typparametern, um Arrays und Tupel zu erstellen, Funktionen und Vorgänge aufzurufen und gewöhnliche oder änderbare Variablen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-121">For the most part, these type parameters can then be used as though they were ordinary types: we use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="fdbd1-122">Der extremste Fall der indirekten Abhängigkeit ist die von Qubits, bei denen ein Q #-Programm nicht direkt auf die Struktur des `Qubit` Typs zurückgreifen kann, sondern solche Typen an andere Vorgänge und Funktionen übergeben **muss** .</span><span class="sxs-lookup"><span data-stu-id="fdbd1-122">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type, but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="fdbd1-123">Wenn Sie zum obigen Beispiel zurückkehren, sehen Sie, dass `Map` über Typparameter verfügen müssen, eine zum Darstellen der Eingabe für `fn` und eine, die die Ausgabe von `fn`darstellen soll.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-123">Returning to the example above, then, we can see that we need `Map` to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="fdbd1-124">In f # wird dies durch Hinzufügen von spitzen Klammern (das `<>`, nicht von Klammern $ \braket{}$!) nach dem Namen einer Funktion oder eines Vorgangs in der Deklaration und durch Auflisten der einzelnen Typparameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-124">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="fdbd1-125">Der Name jedes Typparameters muss mit einem Tick-`'`beginnen, was darauf hinweist, dass es sich um einen Typparameter handelt und nicht um einen normalen Typ (auch als *konkreter* Typ bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="fdbd1-125">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="fdbd1-126">Für `Map`schreiben wir daher Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdbd1-126">For `Map`, we thus write:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : 'Input -> 'Output, values : 'Input[]) : 'Output {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="fdbd1-127">Beachten Sie, dass die Definition von `Map<'Input, 'Output>` den Versionen, die wir zuvor geschrieben haben, sehr ähnlich aussieht.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-127">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the versions we wrote out before.</span></span>
<span data-ttu-id="fdbd1-128">Der einzige Unterschied besteht darin, dass der Compiler explizit informiert hat, dass `Map` nicht direkt von der `'Input` und `'Output` abhängig ist, sondern für zwei Typen funktioniert, indem Sie Sie indirekt über `fn`verwenden.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-128">The only difference is that we have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="fdbd1-129">Nachdem wir `Map<'Input, 'Output>` auf diese Weise definiert haben, können wir es so nennen, als wäre es eine gewöhnliche Funktion:</span><span class="sxs-lookup"><span data-stu-id="fdbd1-129">Once we have defined `Map<'Input, 'Output>` in this way, we can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, we assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="fdbd1-130">Das Schreiben von generischen Funktionen und Vorgängen ist eine Stelle, an der "Tupel-in-Tupel-out" eine sehr nützliche Methode für den Umgang mit Q #-Funktionen und-Vorgängen ist.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-130">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="fdbd1-131">Da jede Funktion genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt, entspricht eine Eingabe des Typs `'T -> 'U` *jeder beliebigen* Q #-Funktion.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-131">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="fdbd1-132">Ebenso kann jeder Vorgang an eine Eingabe des Typs `'T => 'U`übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-132">Similarly, any operation can be passed to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="fdbd1-133">Sehen Sie sich als zweites Beispiel die Herausforderung an, eine Funktion zu schreiben, die die Komposition zweier anderer Funktionen zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="fdbd1-133">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="fdbd1-134">Hier müssen Sie genau angeben, welche `A`, `B`und `C` sind, und so das Dienstprogramm der neuen `Compose` Funktion stark einschränken.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-134">Here, we must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="fdbd1-135">Schließlich ist `Compose` nur über `innerFn` und `outerFn`von `A`, `B`und *`C` abhängig* .</span><span class="sxs-lookup"><span data-stu-id="fdbd1-135">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="fdbd1-136">Als Alternative können wir Typparameter zu `Compose` hinzufügen, die angeben, dass Sie für *alle* `A`, `B`und `C`funktioniert, solange diese Parameter den von `innerFn` und `outerFn`erwarteten entsprechen:</span><span class="sxs-lookup"><span data-stu-id="fdbd1-136">As an alternative, then, we can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="fdbd1-137">Die Q #-Standardbibliotheken stellen eine Reihe von Typen parametrisierten Vorgängen und Funktionen bereit, um die Express-Ablauf Steuerung leichter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-137">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="fdbd1-138">Diese werden im [Leitfaden der Q #-Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro)erläutert.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-138">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>

## <a name="borrowing-qubits"></a><span data-ttu-id="fdbd1-139">Ausleihen von Qubits</span><span class="sxs-lookup"><span data-stu-id="fdbd1-139">Borrowing Qubits</span></span> ##

<span data-ttu-id="fdbd1-140">Der Mechanismus zum ableihen ermöglicht die Zuordnung von Qubits, die während einer Berechnung als Scratch-Speicherplatz verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-140">The borrowing mechanism allows the allocation of qubits that can be used as scratch space during a computation.</span></span> <span data-ttu-id="fdbd1-141">Diese Qubits befinden sich in der Regel nicht in einem sauberen Zustand, d. h., Sie werden nicht notwendigerweise in einem bekannten Zustand initialisiert, wie z. b. $ \ket{0}$.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-141">These qubits are generally not in a clean state, i.e., they are not necessarily initialized in a known state such as $\ket{0}$.</span></span> <span data-ttu-id="fdbd1-142">Außerdem spricht man von "Dirty"-Qubits, weil ihr Zustand unbekannt ist, und kann sogar mit anderen Teilen des Arbeitsspeichers des Quantums Computers entkoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-142">One also speaks of "dirty" qubits as their state is unknown and can even be entangled with other parts of the quantum computer's memory.</span></span> <span data-ttu-id="fdbd1-143">Zu den bekannten Anwendungsfällen von Dirty Qubits zählen Implementierungen von multigesteuerten CNOT Gates, die nur sehr wenige Qubits und die Implementierung von inkrementern erfordern.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-143">Among the known use cases of dirty qubits are implementations of multi-controlled CNOT gates that require only very few qubits and implementation of incrementers.</span></span>

<span data-ttu-id="fdbd1-144">Im Kanon finden Sie Beispiele, in denen das `borrowing`-Schlüsselwort verwendet wird, z. `MultiControlledXBorrow`. die Funktion, die unten definiert ist.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-144">In the canon there are examples that use the `borrowing` keyword, for instance the function `MultiControlledXBorrow` defined below.</span></span>
<span data-ttu-id="fdbd1-145">Wenn `controls` die Steuerungs Qubits angibt, die einem `X` Vorgang hinzugefügt werden sollen, wird eine Gesamtzahl von `Length(controls)-2` vielen Dirty ancillas durch diese Implementierung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-145">If `controls` denotes the control qubits that should be added to an `X` operation, then an overall of `Length(controls)-2` many dirty ancillas will be added by this implementation.</span></span>

```qsharp
operation MultiControlledXBorrow ( controls : Qubit[] , target : Qubit ) : Unit
is Adj + Ctl {

    body (...) {
        ... // skipping some case handling here
        let numberOfDirtyQubits = numberOfControls - 2;
        borrowing( dirtyQubits = Qubit[ numberOfDirtyQubits ] ) {

            let allQubits = [ target ] + dirtyQubits + controls;
            let lastDirtyQubit = numberOfDirtyQubits;
            let totalNumberOfQubits = Length(allQubits);

            let outerOperation1 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 1, 1, 0, numberOfDirtyQubits , _ );
            
            let innerOperation = 
                CCNOTByIndex(
                    totalNumberOfQubits - 1, totalNumberOfQubits - 2, lastDirtyQubit, _ );
            
            WithA(outerOperation1, innerOperation, allQubits);
            
            let outerOperation2 = 
                CCNOTByIndexLadder(
                    numberOfDirtyQubits + 2, 2, 1, numberOfDirtyQubits - 1 , _ );
            
            WithA(outerOperation2, innerOperation, allQubits);
        }
    }

    controlled(extraControls, ...) {
        MultiControlledXBorrow( extraControls + controls, target );
    }
}
```

<span data-ttu-id="fdbd1-146">Beachten Sie, dass die umfangreiche Verwendung des `With` Combinator in seinem Formular---, das für Vorgänge anwendbar ist, die Adjoint unterstützen, d. h., `WithA`---in diesem Beispiel erstellt wurde. Dies ist ein guter Programmierstil, als das Steuerelement zu Strukturen hinzuzufügen, die `With` nur Steuerelemente an den inneren Vorgang weitergibt</span><span class="sxs-lookup"><span data-stu-id="fdbd1-146">Note that extensive use of the `With` combinator---in its form that is applicable for operations that support adjoint, i.e., `WithA`---was made in this example which is good programming style as adding control to structures involving `With` only propagates control to the inner operation.</span></span> <span data-ttu-id="fdbd1-147">Beachten Sie, dass hier zusätzlich zum `body` des Vorgangs eine Implementierung des `controlled` Texts des Vorgangs explizit bereitgestellt wurde, anstatt auf eine `controlled auto`-Anweisung zurückgreifen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-147">Further note that here in addition to the `body` of the operation an implementation of the `controlled` body of the operation was explicitly provided, rather than resorting to a `controlled auto` statement.</span></span> <span data-ttu-id="fdbd1-148">Der Grund hierfür ist, dass wir aus der Struktur der Verbindung wissen, wie Sie ganz einfach weitere Steuerelemente hinzufügen können, die im Vergleich zum Hinzufügen von Steuerelementen zu jedem und jedem einzelnen Gate im `body`von Vorteil sind.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-148">The reason for this is that we know from the structure of the circuit how to easily add further controls which is beneficial compared to adding control to each and every individual gate in the `body`.</span></span> 

<span data-ttu-id="fdbd1-149">Es ist aufschlussreich, diesen Code mit einer anderen Funktion von `MultiControlledXClean` zu vergleichen, die das gleiche Ziel erreicht, eine mehrfach gesteuerte `X` Operation zu implementieren, bei der jedoch mithilfe des `using` Mechanismus mehrere Clean Qubits verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdbd1-149">It is instructive to compare this code with another canon function `MultiControlledXClean` which achieves the same goal of implementing a multiply-controlled `X` operation, however, which uses several clean qubits using the `using` mechanism.</span></span> 
