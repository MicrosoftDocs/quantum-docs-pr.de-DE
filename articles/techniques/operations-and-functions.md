---
title: 'Vorgänge und Funktionen: f #-Techniken | Microsoft-Dokumentation'
description: 'Vorgänge und Funktionen: Q #-Techniken'
uid: microsoft.quantum.techniques.opsandfunctions
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 1fca20bb44cc42008f7d25d2fc71a39b962525c2
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820775"
---
# <a name="q-operations-and-functions"></a><span data-ttu-id="a0673-103">F #-Vorgänge und-Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0673-103">Q# Operations and Functions</span></span>

<span data-ttu-id="a0673-104">Q #-Programme bestehen aus mindestens einem *Vorgang* , bei dem die Nebeneffekte, die Quantum-Vorgänge auf Quantum-Daten haben können, und eine oder mehrere *Funktionen* , die Änderungen an klassischen Daten zulassen, beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-104">Q# programs consist of one or more *operations* that describe side effects quantum operations can have on quantum data, and one or more *functions* that allow modifications to classical data.</span></span> <span data-ttu-id="a0673-105">Im Gegensatz zu Vorgängen werden Funktionen verwendet, um rein klassisches Verhalten zu beschreiben, und Sie haben keine Auswirkungen, außer wenn Sie klassische Ausgabewerte berechnen.</span><span class="sxs-lookup"><span data-stu-id="a0673-105">In contrast to operations, functions are used to describe purely classical behavior and do not have any effects besides computing classical output values.</span></span>

<span data-ttu-id="a0673-106">Jeder in Q # definierte Vorgang kann dann eine beliebige Anzahl anderer Vorgänge aufzurufen, einschließlich der integrierten systeminternen Vorgänge, die von der Sprache definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-106">Each operation defined in Q# may then call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="a0673-107">Die spezielle Methode, mit der diese systeminternen Vorgänge definiert werden, hängt vom Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="a0673-107">The particular way in which these intrinsic operations are defined depends on the target machine.</span></span> <span data-ttu-id="a0673-108">Bei der Kompilierung wird jeder Vorgang als .NET-Klassentyp dargestellt, der den Ziel Computern bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0673-108">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="a0673-109">Definieren von neuen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="a0673-109">Defining New Operations</span></span>

<span data-ttu-id="a0673-110">Wie oben beschrieben, ist der grundlegendste Baustein eines in q # geschriebenen Quantum-Programms ein *Vorgang*, der entweder von klassischen .NET-Anwendungen aus aufgerufen werden kann, z. b. durch die Verwendung eines Simulators oder durch andere Vorgänge in q #.</span><span class="sxs-lookup"><span data-stu-id="a0673-110">As described above, the most basic building block of a quantum program written in Q# is an *operation*, which can either be called from classical .NET applications, e.g., using a simulator, or by other operations within Q#.</span></span>
<span data-ttu-id="a0673-111">Jeder Vorgang nimmt eine Eingabe an, erzeugt eine Ausgabe und gibt die Implementierung für eine oder mehrere Vorgangs Spezialisierungs Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="a0673-111">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="a0673-112">Beispielsweise wird durch den folgenden Vorgang nur eine standardmäßige Text Spezialisierung definiert, und es wird ein einzelnes Qubit als Eingabe benötigt. Anschließend wird der integrierte `X` Vorgang für diese Eingabe aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="a0673-112">For instance, the following operation defines only a default body specialization and takes a single qubit as its input, then calls the built-in `X` operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="a0673-113">Das Schlüsselwort `operation` beginnt die Vorgangs Definition, gefolgt vom Namen. Hier `BitFlip`.</span><span class="sxs-lookup"><span data-stu-id="a0673-113">The keyword `operation` begins the operation definition, and is followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="a0673-114">Als nächstes wird der Typ der Eingabe als `Qubit`definiert, zusammen mit einem Namen `target`, um auf die Eingabe innerhalb des neuen Vorgangs zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a0673-114">Next, the type of the input is defined as `Qubit`, along with a name `target` for referring to the input within the new operation.</span></span>
<span data-ttu-id="a0673-115">Ebenso definiert das `Unit`, dass die Ausgabe des Vorgangs leer ist.</span><span class="sxs-lookup"><span data-stu-id="a0673-115">Similarly, the `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="a0673-116">Dies wird ähnlich wie bei `void` in C# und anderen imperativen Sprachen verwendet und entspricht `unit` in F# und anderen funktionalen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="a0673-116">This is used similarly to `void` in C# and other imperative languages, and is equivalent to `unit` in F# and other functional languages.</span></span>

> [!NOTE]
> <span data-ttu-id="a0673-117">Dies wird im folgenden ausführlicher erläutert, aber jeder Vorgang in Q # nimmt genau eine Eingabe an und gibt genau eine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="a0673-117">We will explore this in more detail below, but each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="a0673-118">Anschließend werden mehrere Eingaben und Ausgaben mithilfe von *Tupeln*dargestellt, die mehrere Werte in einem einzelnen Wert zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="a0673-118">Multiple inputs and outputs are then represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="a0673-119">Informell gesagt, dass Q # eine "tupelin tupelout"-Sprache ist.</span><span class="sxs-lookup"><span data-stu-id="a0673-119">Informally, we say that Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="a0673-120">Nach diesem Konzept sollten `()` als "leeres" Tupel mit dem Typ "`Unit`" gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-120">Following this concept, `()` should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

<span data-ttu-id="a0673-121">Innerhalb des neuen Vorgangs kann die Implementierung direkt innerhalb der-Deklaration angegeben werden, wenn nur die Implementierung der Standardtext Spezialisierung explizit angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="a0673-121">Within the new operation, the implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to be specified explicitly.</span></span> <span data-ttu-id="a0673-122">Außerdem ist es möglich, die Implementierungen von (z. b. eine oder mehrere `functor` Vorgänge) zu definieren, wie unten erläutert.</span><span class="sxs-lookup"><span data-stu-id="a0673-122">Additionally, it is possible to define the implementations of, for example, one or more `functor` operations, as elaborated below.</span></span> <span data-ttu-id="a0673-123">Im obigen Beispiel besteht die einzige Anweisung darin, den integrierten f #-Vorgang <xref:microsoft.quantum.intrinsic.x>aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a0673-123">In the example above, the only statement is to call the built-in Q# operation <xref:microsoft.quantum.intrinsic.x>.</span></span>

<span data-ttu-id="a0673-124">Vorgänge können auch interessantere Typen als `Unit`zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a0673-124">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="a0673-125">Der <xref:microsoft.quantum.intrinsic.m>-Vorgang gibt beispielsweise eine Ausgabe des Typs `Result`zurück, die angibt, dass eine Messung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a0673-125">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span> <span data-ttu-id="a0673-126">Die Ausgabe kann entweder von einem Vorgang an einen anderen Vorgang übergeben werden, oder Sie kann mit dem `let`-Schlüsselwort verwendet werden, um eine neue Variable zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a0673-126">We can either pass the output from an operation to another operation, or can use it with the `let` keyword to define a new variable.</span></span>
<!-- Link to UID for superdense conceptual and example documentation. -->
<span data-ttu-id="a0673-127">Dies ermöglicht die Darstellung der klassischen Berechnung, die mit Quantum-Vorgängen auf niedriger Ebene interagiert, wie z. b. in einer übergeordneten Codierung:</span><span class="sxs-lookup"><span data-stu-id="a0673-127">This allows for representing classical computation that interacts with quantum operations at a low level, such as in superdense coding:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```
### <a name="functors-adjoint-and-controlled"></a><span data-ttu-id="a0673-128">Funktoren, Adjoint und gesteuert</span><span class="sxs-lookup"><span data-stu-id="a0673-128">Functors, adjoint and controlled</span></span>
<span data-ttu-id="a0673-129">Wenn ein Vorgang eine einheitliche Transformation implementiert, ist es möglich, zu definieren, wie der Vorgang beim *angleichen oder* *Steuern*erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a0673-129">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="a0673-130">Eine Adjoint-Spezialisierung eines Vorgangs gibt an, wie er bei umgekehrter Ausführung agiert, während eine kontrollierte Spezialisierung angibt, wie ein Vorgang angewendet wird, wenn er auf den Zustand eines Quantum-Register angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a0673-130">An adjoint specialization of an operation specifies how it acts when run in reverse, while a controlled specialization specifies how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="a0673-131">Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur: `is Adj + Ctl` im folgenden Beispiel deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-131">The existence of these specializations can be declared as part of the operation signature: `is Adj + Ctl` in the following example.</span></span> <span data-ttu-id="a0673-132">Die entsprechende Implementierung für jede solche implizit deklarierte Spezialisierung wird dann vom Compiler generiert.</span><span class="sxs-lookup"><span data-stu-id="a0673-132">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

> [!NOTE]
> <span data-ttu-id="a0673-133">Viele Vorgänge in Q # stellen einheitliche Gates dar.</span><span class="sxs-lookup"><span data-stu-id="a0673-133">Many operations in Q# represent unitary gates.</span></span>
> <span data-ttu-id="a0673-134">Wenn $U $ das einheitliche Gate ist, das durch einen Vorgang `U`dargestellt wird, stellt `Adjoint U` das einheitliche Gate $U ^ \dagger $ dar.</span><span class="sxs-lookup"><span data-stu-id="a0673-134">If $U$ is the unitary gate represented by an operation `U`, then `Adjoint U` represents the unitary gate $U^\dagger$.</span></span>

<span data-ttu-id="a0673-135">Wenn die Implementierung nicht vom Compiler generiert werden kann, kann Sie explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-135">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="a0673-136">Solche expliziten Spezialisierungs Deklarationen können aus einer geeigneten Generierungs Direktive oder einer benutzerdefinierten Implementierung bestehen.</span><span class="sxs-lookup"><span data-stu-id="a0673-136">Such explicit specialization declarations can consist of a suitable generation directive or a user defined implementation.</span></span> <span data-ttu-id="a0673-137">Der oben genannte Code in `PrepareEntangledPair` z. b. Äquivalent zum folgenden Code, der explizite Spezialisierungs Deklarationen enthält:</span><span class="sxs-lookup"><span data-stu-id="a0673-137">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="a0673-138">Das Schlüsselwort `auto` gibt an, dass der Compiler bestimmen soll, wie die Spezialisierungs Implementierung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0673-138">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="a0673-139">Wenn der Compiler die Implementierung für eine bestimmte Spezialisierung nicht automatisch generieren kann oder wenn eine effizientere Implementierung angegeben werden kann, kann die Implementierung auch manuell definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-139">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="a0673-140">Im obigen Beispiel gibt `adjoint invert;` an, dass die Adjoint-Spezialisierung generiert werden soll, indem Sie die Text Implementierung umkehren, und `controlled adjoint invert;` gibt an, dass die kontrollierte Adjoint-Spezialisierung generiert werden soll, indem Sie die angegebene Implementierung der kontrollierten Spezialisierung umkehren.</span><span class="sxs-lookup"><span data-stu-id="a0673-140">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="a0673-141">Weitere Beispiele hierfür finden Sie in der [Ablauf Steuerung in höherer Reihenfolge](xref:microsoft.quantum.concepts.control-flow).</span><span class="sxs-lookup"><span data-stu-id="a0673-141">We will see more examples of this in [Higher-Order Control Flow](xref:microsoft.quantum.concepts.control-flow).</span></span>

<span data-ttu-id="a0673-142">Um eine Spezialisierung eines Vorgangs aufzurufen, verwenden Sie die Schlüsselwörter `Adjoint` oder `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="a0673-142">To call a specialization of an operation, use the `Adjoint` or `Controlled` keywords.</span></span>
<span data-ttu-id="a0673-143">So kann z. b. das oben beschriebene Codierungs Beispiel mit dem Adjoint von `PrepareEntangledPair` kompakter geschrieben werden, um den entzickten Zustand zurück in ein nicht verziges paar von Qubits umzuwandeln:</span><span class="sxs-lookup"><span data-stu-id="a0673-143">For example, the superdense coding example above can be written more compactly by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation Superdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="a0673-144">Beim Entwerfen von Vorgängen für die Verwendung mit Funktoren sind einige wichtige Einschränkungen zu beachten.</span><span class="sxs-lookup"><span data-stu-id="a0673-144">There are a number of important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="a0673-145">In den meisten Fällen können Spezialisierungs Vorgänge für einen Vorgang, der den Ausgabewert eines beliebigen anderen Vorgangs verwendet, nicht automatisch vom Compiler generiert werden, da er nicht eindeutig ist, wie die Anweisungen in einem solchen Vorgang neu angeordnet werden, um denselben Effekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0673-145">Most critically, specializations for an operation that uses the output value of any other operation cannot be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>


## <a name="defining-new-functions"></a><span data-ttu-id="a0673-146">Definieren neuer Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0673-146">Defining New Functions</span></span>

<span data-ttu-id="a0673-147">Q # ermöglicht außerdem das Definieren von *Funktionen*, die sich von Vorgängen unterscheiden, da Sie keine Auswirkungen auf die Berechnung eines Ausgabe Werts haben dürfen.</span><span class="sxs-lookup"><span data-stu-id="a0673-147">Q# also allows for defining *functions*, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="a0673-148">Insbesondere können Funktionen keine Vorgänge aufzurufen, auf Qubits reagieren, Zufallszahlen in Stichproben oder anderweitig abhängig von dem Zustand, der über den Eingabe Wert hinausgeht, auf eine Funktion setzen.</span><span class="sxs-lookup"><span data-stu-id="a0673-148">In particular, functions cannot call operations, act on qubits, sample random numbers, or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="a0673-149">Folglich sind Q #-Funktionen *rein*, da Sie die gleichen Eingabewerte immer denselben Ausgabe Werten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="a0673-149">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="a0673-150">Dadurch kann der Q #-Compiler sicher neu anordnen, wie und wann Funktionen beim Erstellen von Vorgangs speziationen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-150">This allows the Q# compiler to safely reorder how and when functions are called when generating operation specializations.</span></span>

<span data-ttu-id="a0673-151">Das Definieren einer Funktion funktioniert ähnlich wie ein Vorgang, mit dem Unterschied, dass für eine Funktion keine Adjoint-oder kontrollierten Spezialisierungs Funktionen definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a0673-151">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="a0673-152">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a0673-152">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```
<span data-ttu-id="a0673-153">Wenn dies möglich ist, ist es hilfreich, Klassische Logik in Bezug auf Funktionen anstelle von Vorgängen zu schreiben, damit Sie von innerhalb von Vorgängen leichter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0673-153">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations, so that it can be more readily used from within operations.</span></span>
<span data-ttu-id="a0673-154">Wenn wir z. b. `Square` als Vorgang geschrieben hätten, wäre der Compiler nicht in der Lage, zu garantieren, dass der Aufruf mit derselben Eingabe konsistent die gleichen Ausgaben erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a0673-154">If we had written `Square` as an operation, for example, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="a0673-155">Um den Unterschied zwischen Funktionen und Vorgängen zu unterstreichen, sollten Sie das Problem der klassischen Stichprobenentnahme einer Zufallszahl aus einem f #-Vorgang in Erwägung gezogen</span><span class="sxs-lookup"><span data-stu-id="a0673-155">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="a0673-156">Jedes Mal, wenn `U` aufgerufen wird, wird eine andere Aktion auf `target`ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0673-156">Each time that `U` is called, it will have a different action on `target`.</span></span>
<span data-ttu-id="a0673-157">Insbesondere kann der Compiler nicht garantieren, dass beim Hinzufügen einer `adjoint auto`-Spezialisierungs Deklaration zu `U`, `U(target); Adjoint U(target);` als Identität agiert (d. h. als No-OP).</span><span class="sxs-lookup"><span data-stu-id="a0673-157">In particular, the compiler cannot guarantee that if we added an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="a0673-158">Dies verstößt gegen die Definition des Adjoint, das wir in [Vektoren und Matrizen](xref:microsoft.quantum.concepts.vectors)erkannt haben, sodass das automatische Generieren einer Adjoint-Spezialisierung in einem Vorgang möglich ist, bei dem der Vorgang aufgerufen wurde <xref:microsoft.quantum.math.randomreal> die vom Compiler bereitgestellten Garantien unterbrechen würde. <xref:microsoft.quantum.math.randomreal> ist ein Vorgang, für den keine Adjoint-oder kontrollierte Version vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a0673-158">This violates the definition of the adjoint that we saw in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing to auto-generate an adjoint specialization in an operation where we have called the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="a0673-159">Das Zulassen von Funktionsaufrufen, wie z. b. `Square`, ist darin sicherzustellen, dass der Compiler sicher sein kann, dass nur die Eingabe für `Square` beibehalten werden muss, damit die Ausgabe stabil bleibt.</span><span class="sxs-lookup"><span data-stu-id="a0673-159">On the other hand, allowing function calls such as `Square` is safe, in that the compiler can be assured that it only needs to preserve the input to `Square` in order to keep its output stable.</span></span>
<span data-ttu-id="a0673-160">Daher ist es einfach, diese Logik in anderen Funktionen und Vorgängen zu verwenden, damit Sie so viel Klassische Logik wie möglich in Functions isolieren kann.</span><span class="sxs-lookup"><span data-stu-id="a0673-160">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>

## <a name="control-flow"></a><span data-ttu-id="a0673-161">Ablaufsteuerung</span><span class="sxs-lookup"><span data-stu-id="a0673-161">Control Flow</span></span>

<span data-ttu-id="a0673-162">Innerhalb einer Operation oder Funktion wird jede Anweisung in der richtigen Reihenfolge ausgeführt, ähnlich wie bei den gängigsten, imperativen, klassischen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="a0673-162">Within an operation or function, each statement executes in order, similar to most common imperative classical languages.</span></span>
<span data-ttu-id="a0673-163">Diese Ablauf Steuerung kann jedoch auf drei verschiedene Arten geändert werden:</span><span class="sxs-lookup"><span data-stu-id="a0673-163">This flow of control can be modified, however, in three distinct ways:</span></span>

- <span data-ttu-id="a0673-164">`if`-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="a0673-164">`if` Statements</span></span>
- <span data-ttu-id="a0673-165">`for` Schleifen</span><span class="sxs-lookup"><span data-stu-id="a0673-165">`for` Loops</span></span>
- <span data-ttu-id="a0673-166">`repeat`-`until` Schleifen</span><span class="sxs-lookup"><span data-stu-id="a0673-166">`repeat`-`until` Loops</span></span>

<span data-ttu-id="a0673-167">Wir verzögern die Erörterung der letzteren, bis wir eine [Wiederholung von Wiederholungs Läufen (RUS bis Erfolg)](xref:microsoft.quantum.techniques.qubits#measurements) erörtern.</span><span class="sxs-lookup"><span data-stu-id="a0673-167">We defer discussion of the latter until we discuss [Repeat Until Success (RUS)](xref:microsoft.quantum.techniques.qubits#measurements) circuits.</span></span>
<span data-ttu-id="a0673-168">Die `if`-und `for` Ablaufsteuerungskonstrukte werden jedoch in den meisten klassischen Programmiersprachen als vertrauter bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a0673-168">The `if` and `for` control flow constructs, however, proceed in a familiar sense to most classical programming languages.</span></span>
<span data-ttu-id="a0673-169">Vor allem kann eine `if`-Anweisung eine Bedingung annehmen, auf die eine oder mehrere `elif` Anweisungen folgen können und mit einem `else`enden:</span><span class="sxs-lookup"><span data-stu-id="a0673-169">In particular, an `if` statement can take a condition, may be followed by one or more `elif` statements, and may end with an `else`:</span></span>

```qsharp
if (pauli == PauliX) {
    X(qubit);
} elif (pauli == PauliY) {
    Y(qubit);
} elif (pauli == PauliZ) {
    Z(qubit);
} else {
    fail "Cannot use PauliI here.";
}
```

<span data-ttu-id="a0673-170">Auf ähnliche Weise geben `for` Schleifen Iterationen über einen Bereich von ganzen Zahlen oder über die Elemente eines Arrays an:</span><span class="sxs-lookup"><span data-stu-id="a0673-170">Similarly, `for` loops indicate iteration over a range of integers or over the elements of an array:</span></span>

```qsharp
for (idxQubit in 0..nQubits - 1) {
    // Do something to idxQubit...
}
```

<span data-ttu-id="a0673-171">Wichtig ist, dass `for` Schleifen und `if` Anweisungen sogar in Vorgängen verwendet werden können, für die Spezialisierungs Vorgänge automatisch generiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-171">Importantly, `for` loops and `if` statements can even be used in operations for which specializations are auto-generated.</span></span> <span data-ttu-id="a0673-172">In diesem Fall kehrt das Adjoint-Zeichen einer `for`-Schleife die Richtung um und nimmt das Adjoint der einzelnen Iterationen an.</span><span class="sxs-lookup"><span data-stu-id="a0673-172">In that case the adjoint of a `for` loop reverses the direction and takes the adjoint of each iteration.</span></span>
<span data-ttu-id="a0673-173">Dies folgt dem Prinzip "Schuh-und-SOCKS": Wenn Sie das Einfügen von SOCKS und dann auf Schuhe rückgängig machen möchten, müssen Sie die einfügende Schuhe rückgängig machen und dann auf SOCKS setzen.</span><span class="sxs-lookup"><span data-stu-id="a0673-173">This follows the "shoes-and-socks" principle: if you wish to undo putting on socks and then shoes, you must undo putting on shoes and then undo putting on socks.</span></span>
<span data-ttu-id="a0673-174">Es funktioniert ausgesprochen weniger gut, wenn Sie versuchen, die SOCKS zu wiederholen, während Sie Ihre Schuhe noch nicht nutzen!</span><span class="sxs-lookup"><span data-stu-id="a0673-174">It works decidedly less well to try and take your socks off while you're still wearing your shoes!</span></span>

## <a name="operations-and-functions-as-first-class-values"></a><span data-ttu-id="a0673-175">Vorgänge und Funktionen als First-Class-Werte</span><span class="sxs-lookup"><span data-stu-id="a0673-175">Operations and Functions as First-Class Values</span></span>

<span data-ttu-id="a0673-176">Ein wichtiges Verfahren, um die Ablauf Steuerung und die klassische Logik mithilfe von Funktionen anstelle von Vorgängen zu überdenken, besteht darin, diese Vorgänge und Funktionen in Q # als *erste Klasse*zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0673-176">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="a0673-177">Das heißt, Sie sind jeweils die einzelnen Werte in der Sprache.</span><span class="sxs-lookup"><span data-stu-id="a0673-177">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="a0673-178">Beispielsweise ist der folgende vollständig gültige Q #-Code, wenn ein wenig indirekt:</span><span class="sxs-lookup"><span data-stu-id="a0673-178">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="a0673-179">Der Wert der Variablen, die im obigen Code Ausschnitt `ourH` ist, ist der Vorgang <xref:microsoft.quantum.intrinsic.h>, sodass wir diesen Wert wie jeder andere Vorgang abrufen können.</span><span class="sxs-lookup"><span data-stu-id="a0673-179">The value of the variable `ourH` in the snippet above is then the operation <xref:microsoft.quantum.intrinsic.h>, such that we can call that value like any other operation.</span></span>
<span data-ttu-id="a0673-180">Dies ermöglicht es uns, Vorgänge zu schreiben, die Vorgänge als Teil Ihrer Eingabe ausführen und so die Konzepte der Ablauf Steuerung auf höherer Ordnung bilden.</span><span class="sxs-lookup"><span data-stu-id="a0673-180">This allows us to write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="a0673-181">Beispielsweise könnten wir uns vorstellen, einen Vorgang zu "quadrieren", indem wir ihn zweimal auf das gleiche Ziel-Qubit anwenden.</span><span class="sxs-lookup"><span data-stu-id="a0673-181">For instance, we could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="a0673-182">In diesem Beispiel gibt der `=>` Pfeil, der im Typ `(Qubit => Unit)` angezeigt wird, an, dass das Eingabefeld `op` ein Vorgang ist, der als Eingabe den Typ `Qubit` annimmt und ein leeres Tupel als Ausgabe erzeugt.</span><span class="sxs-lookup"><span data-stu-id="a0673-182">In this example, the `=>` arrow that appears in the type `(Qubit => Unit)` denotes that the input field `op` is an operation which takes as its input the type `Qubit` and produces an empty tuple as its output.</span></span>
<span data-ttu-id="a0673-183">Außerdem geben wir die Merkmale dieses Vorgangs Typs an, die die Informationen zu den unterstützten Funktoren enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0673-183">Additionally we specify the characteristics of that operation type, which contain the information about which functors are supported.</span></span>
<span data-ttu-id="a0673-184">Ein Vorgang vom Typ `(Qubit => Unit)` unterstützt weder den `Adjoint` noch den `Controlled`-Funktor.</span><span class="sxs-lookup"><span data-stu-id="a0673-184">An operation of type `(Qubit => Unit)` supports neither the `Adjoint` nor the `Controlled` functor.</span></span> <span data-ttu-id="a0673-185">Wenn Sie angeben möchten, dass ein Vorgang dieses Typs z. b. den `Adjoint`-Funktor unterstützen muss, müssen wir ihn als adjointable deklarieren.</span><span class="sxs-lookup"><span data-stu-id="a0673-185">If we want to indicate that an operation of that type has to support e.g. the `Adjoint` functor, we have to declare it as being adjointable.</span></span> <span data-ttu-id="a0673-186">Dies erfolgt mithilfe der-Anmerkung `is Adj` für den-Typ.</span><span class="sxs-lookup"><span data-stu-id="a0673-186">This is done by using the annotation `is Adj` to the type.</span></span> <span data-ttu-id="a0673-187">Ebenso gibt `(Qubit => Unit is Ctl)` an, dass ein Vorgang dieses Typs den `Controlled`-Funktor unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0673-187">Similarly, `(Qubit => Unit is Ctl)` denotes that an operation of that type supports the `Controlled` functor.</span></span> <span data-ttu-id="a0673-188">Wir werden dies weiter untersuchen, wenn wir [types in Q #] (Xref: Microsoft. Quantum. Language. Type-Model) allgemeiner erörtern.</span><span class="sxs-lookup"><span data-stu-id="a0673-188">We will explore this further when we discuss [types in Q#] (xref:microsoft.quantum.language.type-model) more generally.</span></span>

<span data-ttu-id="a0673-189">Vorerst betonen wir, dass wir auch Vorgänge als Teil der Ausgaben zurückgeben können, sodass wir einige Arten von klassischer bedingter Logik als klassische Funktion isolieren können, die eine Beschreibung eines Quantum-Programms in Form eines Vorgangs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a0673-189">For now, we emphasize that we can also return operations as a part of outputs, such that we can isolate some kinds of classical conditional logic as a classical function which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="a0673-190">Als einfaches Beispiel sehen Sie sich das Beispiel für die teleportung an, in dem die Partei, die eine zwei-Bit-klassische Nachricht empfängt, die Nachricht verwenden muss, um Ihr Qubit in den richtigen teleportierten Zustand zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="a0673-190">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="a0673-191">Wir könnten dies im Hinblick auf eine Funktion schreiben, die diese beiden klassischen Bits annimmt und den richtigen Decodierungs Vorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a0673-191">We could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

```qsharp
function TeleporationDecoderForMessage(hereBit : Result, thereBit : Result)
: (Qubit => Unit is Adj + Ctl) {

    if (hereBit == Zero && thereBit == Zero) {
        return I;
    } elif (hereBit == One && thereBit == Zero) {
        return X;
    } elif (hereBit == Zero && thereBit == One) {
        return Z;
    } else {
        return Y;
    }
}
```

<span data-ttu-id="a0673-192">Diese neue Funktion ist tatsächlich eine Funktion, denn wenn wir Sie mit denselben Werten von `hereBit` und `thereBit`nennen, erhalten wir immer denselben Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a0673-192">This new function is indeed a function, in that if we call it with the same values of `hereBit` and `thereBit`, we will always get back the same operation.</span></span>
<span data-ttu-id="a0673-193">Daher kann der Decoder sicher innerhalb von Vorgängen ausgeführt werden, ohne dass es darum geht, zu bedenken, wie die Decodierungs Logik mit den Definitionen der verschiedenen Vorgangs Spezialisierungs Maßnahmen interagiert.</span><span class="sxs-lookup"><span data-stu-id="a0673-193">Thus, the decoder can be safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="a0673-194">Das heißt, wir haben die klassische Logik innerhalb einer Funktion isoliert und dem Compiler dadurch sichergestellt, dass der Funktions aufrufbedarf mit Straffreiheit neu angeordnet werden kann, solange die Eingabe beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="a0673-194">That is, we have isolated the classical logic inside a function, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>

<span data-ttu-id="a0673-195">Wir können Funktionen auch als First-Class-Werte behandeln, da wir bei der Erörterung von [Vorgängen und Funktionstypen](#operations-and-functions-as-first-class-values)ausführlicher sehen werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-195">We can also treat functions as first-class values, as we will see in more detail when we discuss [operations and function types](#operations-and-functions-as-first-class-values).</span></span>

## <a name="partially-applying-operations-and-functions"></a><span data-ttu-id="a0673-196">Teilweise Anwenden von Vorgängen und Funktionen</span><span class="sxs-lookup"><span data-stu-id="a0673-196">Partially Applying Operations and Functions</span></span>

<span data-ttu-id="a0673-197">Wir können mit Funktionen, die Vorgänge mithilfe einer *partiellen Anwendung*zurückgeben, wesentlich mehr tun, in der wir einen oder mehrere Teile der Eingabe für eine Funktion oder einen Vorgang bereitstellen können, ohne Sie tatsächlich aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="a0673-197">We can do significantly more with functions that return operations by using *partial application*, in which we can provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="a0673-198">Wenn Sie z. b. das obige `ApplyTwice` Beispiel beachten, können wir angeben, dass wir nicht sofort angeben möchten, auf welchem Qubit der Eingabevorgang angewendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="a0673-198">For example, recalling the `ApplyTwice` example above, we can indicate that we don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="a0673-199">In diesem Fall enthält die lokale Variable `twiceOp` den teilweise angewendeten Vorgang `ApplyTwice(op, _)`, bei dem noch nicht angegebene Teile der Eingabe durch `_`angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-199">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where parts of the input that have not yet been specified are indicated by `_`.</span></span>
<span data-ttu-id="a0673-200">Wenn `twiceOp` in der nächsten Zeile aufgerufen wird, übergeben wir als Eingabe an den teilweise angewendeten Vorgang alle verbleibenden Teile der Eingabe für den ursprünglichen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a0673-200">When we actually call `twiceOp` in the next line, we pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="a0673-201">Folglich ist der obige Code Ausschnitt effektiv identisch mit dem Aufruf von `ApplyTwice(op, target)` direkt. speichern Sie, damit wir eine neue lokale Variable eingeführt haben, die es uns ermöglicht, den Aufruf zu verzögern, während einige Teile der Eingabe bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a0673-201">Thus, the above snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that we have introduced a new local variable that allows us to delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="a0673-202">Da ein Vorgang, der teilweise angewendet wurde, erst aufgerufen wird, wenn die gesamte Eingabe bereitgestellt wurde, können wir Vorgänge auf sichere Weise sogar aus Funktionen anwenden.</span><span class="sxs-lookup"><span data-stu-id="a0673-202">Since an operation that has been partially applied is not actually called until its entire input has been provided, we can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="a0673-203">Im Prinzip könnte die klassische Logik in `SquareOperation` viel komplizierter sein, aber Sie ist weiterhin vom Rest eines Vorgangs isoliert, indem die Garantien, die der Compiler über Funktionen bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="a0673-203">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span>
<span data-ttu-id="a0673-204">Diese Vorgehensweise wird in der Q #-Standardbibliothek verwendet, um die klassische Ablauf Steuerung so auszudrücken, dass Sie in quantenprogrammen problemlos verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0673-204">This approach will be used throughout the Q# standard library for expressing classical control flow in a way that can be readily used within quantum programs.</span></span>
