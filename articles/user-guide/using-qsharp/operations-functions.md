---
title: Vorgänge und Funktionen inQ#
description: Definieren und aufzurufen von Vorgängen und Funktionen sowie der kontrollierten und der Adjoint-Vorgangs Spezialisierung.
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.operationsfunctions
no-loc:
- Q#
- $$v
ms.openlocfilehash: 76437c83df894fa86409e680f961d97e267c6869
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867878"
---
# <a name="operations-and-functions-in-no-locq"></a><span data-ttu-id="ba218-103">Vorgänge und Funktionen inQ#</span><span class="sxs-lookup"><span data-stu-id="ba218-103">Operations and Functions in Q#</span></span>

## <a name="defining-new-operations"></a><span data-ttu-id="ba218-104">Definieren von neuen Vorgängen</span><span class="sxs-lookup"><span data-stu-id="ba218-104">Defining New Operations</span></span>

<span data-ttu-id="ba218-105">Vorgänge sind der Kern von Q# .</span><span class="sxs-lookup"><span data-stu-id="ba218-105">Operations are the core of Q#.</span></span>
<span data-ttu-id="ba218-106">Nach der Deklaration können Sie entweder von klassischen .NET-Anwendungen aus aufgerufen werden, z. b. durch die Verwendung eines Simulators oder durch andere Vorgänge in Q# .</span><span class="sxs-lookup"><span data-stu-id="ba218-106">Once declared, they can either be called from classical .NET applications, for example, using a simulator or by other operations within Q#.</span></span>
<span data-ttu-id="ba218-107">Jeder in definierte Vorgang Q# kann eine beliebige Anzahl anderer Vorgänge, einschließlich der integrierten systeminternen Vorgänge, die von der Sprache definiert sind, aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba218-107">Each operation defined in Q# can call any number of other operations, including the built-in intrinsic operations defined by the language.</span></span> <span data-ttu-id="ba218-108">Die spezielle Methode, mit der diese systeminternen Q# Vorgänge definiert werden, hängt vom Zielcomputer ab.</span><span class="sxs-lookup"><span data-stu-id="ba218-108">The particular way in which Q# defines these intrinsic operations depends on the target machine.</span></span>
<span data-ttu-id="ba218-109">Bei der Kompilierung wird jeder Vorgang als .NET-Klassentyp dargestellt, der den Ziel Computern bereitgestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba218-109">When compiled, each operation is represented as a .NET class type that can be provided to target machines.</span></span>

<span data-ttu-id="ba218-110">Jede Q# Quelldatei kann eine beliebige Anzahl von Vorgängen definieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-110">Each Q# source file can define any number of operations.</span></span>
<span data-ttu-id="ba218-111">Vorgangs Namen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit Typ-oder Funktionsnamen verursachen.</span><span class="sxs-lookup"><span data-stu-id="ba218-111">Operation names must be unique within a namespace and can not conflict with type or function names.</span></span>

<span data-ttu-id="ba218-112">Eine Vorgangs Deklaration besteht aus dem Schlüsselwort `operation` , gefolgt von dem Symbol, das den Namen des Vorgangs enthält, einem typisierten bezeichnertupel, das die Argumente für den Vorgang definiert, einem Doppelpunkt `:` , einer Typanmerkung, die den Ergebnistyp des Vorgangs beschreibt, optional einer Anmerkung mit den Vorgangs Merkmalen, einer geöffneten geschweiften Klammer und dem Text der Vorgangs Deklaration in geschweiften `{ }`</span><span class="sxs-lookup"><span data-stu-id="ba218-112">An operation declaration consists of the keyword `operation`, followed by the symbol that is the operation's name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation's result type, optionally an annotation with the operation characteristics, an open brace, and then the body of the operation declaration, enclosed in braces `{ }`.</span></span>

<span data-ttu-id="ba218-113">Jeder Vorgang nimmt eine Eingabe an, erzeugt eine Ausgabe und gibt die Implementierung für eine oder mehrere Vorgangs Spezialisierungs Vorgänge an.</span><span class="sxs-lookup"><span data-stu-id="ba218-113">Each operation takes an input, produces an output, and specifies the implementation for one or more operation specializations.</span></span>
<span data-ttu-id="ba218-114">Die möglichen Spezialisierungsmöglichkeiten und die Vorgehensweise zum Definieren und anrufen werden in den verschiedenen Abschnitten dieses Artikels beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ba218-114">The possible specializations, and how to define and call them, are detailed in the different sections of this article.</span></span>
<span data-ttu-id="ba218-115">Sehen Sie sich den folgenden Vorgang an, der nur eine Standard Textzeile definiert und ein einzelnes Qubit als Eingabe annimmt und dann den integrierten <xref:microsoft.quantum.intrinsic.x> Vorgang für diese Eingabe aufruft:</span><span class="sxs-lookup"><span data-stu-id="ba218-115">For now, consider the following operation, which defines only a default body specialization and takes a single qubit as its input, then calls the built-in <xref:microsoft.quantum.intrinsic.x> operation on that input:</span></span>

```qsharp
operation BitFlip(target : Qubit) : Unit {
    X(target);
}
```

<span data-ttu-id="ba218-116">Das Schlüsselwort `operation` beginnt mit der Vorgangs Definition, gefolgt vom Namen; hier, `BitFlip` .</span><span class="sxs-lookup"><span data-stu-id="ba218-116">The keyword `operation` begins the operation definition, followed by the name; here, `BitFlip`.</span></span>
<span data-ttu-id="ba218-117">Als nächstes wird der Typ der Eingabe definiert ( `Qubit` ), zusammen mit einem Namen, `target` , um auf die Eingabe innerhalb des neuen Vorgangs zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="ba218-117">Next, the type of input is defined (`Qubit`), along with a name, `target`, for referring to the input within the new operation.</span></span>
<span data-ttu-id="ba218-118">Schließlich `Unit` definiert, dass die Ausgabe des Vorgangs leer ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-118">Lastly, `Unit` defines that the operation's output is empty.</span></span>
<span data-ttu-id="ba218-119">`Unit`wird ähnlich wie `void` in c# und anderen imperativen Sprachen verwendet und entspricht `unit` in F # und anderen funktionalen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="ba218-119">`Unit` is used similarly to `void` in C# and other imperative languages and is equivalent to `unit` in F# and other functional languages.</span></span>

<span data-ttu-id="ba218-120">Vorgänge können auch interessantere Typen als zurückgeben `Unit` .</span><span class="sxs-lookup"><span data-stu-id="ba218-120">Operations can also return more interesting types than `Unit`.</span></span>
<span data-ttu-id="ba218-121">Der- <xref:microsoft.quantum.intrinsic.m> Vorgang gibt beispielsweise eine Ausgabe vom Typ zurück `Result` , die angibt, dass eine Messung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba218-121">For instance, the <xref:microsoft.quantum.intrinsic.m> operation returns an output of type `Result`, representing having performed a measurement.</span></span>  <span data-ttu-id="ba218-122">Sie können Sie von einem Vorgang an einen anderen Vorgang übergeben oder mit dem- `let` Schlüsselwort verwenden, um eine neue Variable zu definieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-122">You can pass it from an operation to another operation or use it with the `let` keyword to define a new variable.</span></span>

<span data-ttu-id="ba218-123">Mit diesem Ansatz können Sie die klassische Berechnung darstellen, die mit Quantum-Vorgängen auf niedriger Ebene interagiert, wie z. b. in einer über [geordneten Codierung](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span><span class="sxs-lookup"><span data-stu-id="ba218-123">This approach allows for representing classical computation that interacts with quantum operations at a low level, such as in [superdense coding](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding):</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {

    CNOT(there, here);
    H(there);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

> [!NOTE]
> <span data-ttu-id="ba218-124">Jeder Vorgang in Q# erfordert genau eine Eingabe und gibt genau eine Ausgabe zurück.</span><span class="sxs-lookup"><span data-stu-id="ba218-124">Each operation in Q# takes exactly one input and returns exactly one output.</span></span>
> <span data-ttu-id="ba218-125">Mehrere Eingaben und Ausgaben werden mithilfe von *Tupeln*dargestellt, die mehrere Werte in einem einzelnen Wert zusammenfassen.</span><span class="sxs-lookup"><span data-stu-id="ba218-125">Multiple inputs and outputs are represented using *tuples*, which collect multiple values together into a single value.</span></span>
> <span data-ttu-id="ba218-126">In dieser Hinsicht Q# ist eine "Tupel-in-tupelout"-Sprache.</span><span class="sxs-lookup"><span data-stu-id="ba218-126">In this regard, Q# is a "tuple-in tuple-out" language.</span></span>
> <span data-ttu-id="ba218-127">Im Anschluss an dieses Konzept sollte ein Satz leerer Klammern, `()` , als leeres Tupel mit dem-Typ gelesen werden `Unit` .</span><span class="sxs-lookup"><span data-stu-id="ba218-127">Following this concept, a set of empty parentheses, `()`, should then be read as the "empty" tuple, which has the type `Unit`.</span></span>

## <a name="controlled-and-adjoint-operations"></a><span data-ttu-id="ba218-128">Kontrollierte und Adjoint-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="ba218-128">Controlled and Adjoint Operations</span></span>

<span data-ttu-id="ba218-129">Wenn ein Vorgang eine einheitliche Transformation implementiert, wie dies bei vielen Vorgängen in der Fall ist Q# , ist es möglich, zu definieren, wie der *adjointed* Vorgang bei Anfügevorgang oder *Kontrolle*agiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-129">If an operation implements a unitary transformation, as is the case for many operations in Q#, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span> <span data-ttu-id="ba218-130">Eine *Adjoint* -Spezialisierung eines Vorgangs gibt an, wie die "Umkehrung" des Vorgangs agiert, während eine *kontrollierte* Spezialisierung angibt, wie ein Vorgang funktioniert, wenn die Anwendung auf den Zustand eines bestimmten Quantum-Registers angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-130">An *adjoint* specialization of an operation specifies how the "inverse" of the operation acts, while a *controlled* specialization specifies how an operation acts when its application is conditioned on the state of a particular quantum register.</span></span>

<span data-ttu-id="ba218-131">Adjoints von Quantum-Vorgängen sind für viele Aspekte von Quantum Computing von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="ba218-131">Adjoints of quantum operations are crucial to many aspects of quantum computing.</span></span> <span data-ttu-id="ba218-132">Ein Beispiel für eine solche Situation, die zusammen mit einem nützlichen Programmierverfahren erläutert Q# wird, finden Sie unter " [Konjugationen](#conjugations) " in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="ba218-132">For an example of one such situation discussed alongside a useful Q# programming technique, see [Conjugations](#conjugations) in this article.</span></span> 

<span data-ttu-id="ba218-133">Bei der kontrollierten Version eines Vorgangs handelt es sich um einen neuen Vorgang, der den Basis Vorgang effektiv anwendet, wenn sich alle Steuerelement-Qubits in einem angegebenen Zustand befinden.</span><span class="sxs-lookup"><span data-stu-id="ba218-133">The controlled version of an operation is a new operation that effectively applies the base operation only if all of the control qubits are in a specified state.</span></span>
<span data-ttu-id="ba218-134">Wenn sich die Steuerelement-Qubits in der superposition befinden, wird der Basis Vorgang einheitlich auf den entsprechenden Teil der superposition angewendet.</span><span class="sxs-lookup"><span data-stu-id="ba218-134">If the control qubits are in superposition, then the base operation is applied coherently to the appropriate part of the superposition.</span></span>
<span data-ttu-id="ba218-135">Folglich werden kontrollierte Vorgänge häufig zum Generieren von entanglement verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba218-135">Thus, controlled operations are often used to generate entanglement.</span></span>

<span data-ttu-id="ba218-136">Natürlich könnte auch eine *kontrollierte Adjoint* -Spezialisierung vorhanden sein, die die kontrollierte Anwendung des Adjoint eines Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="ba218-136">Naturally, a *controlled adjoint* specialization could exist as well, specifying the controlled application of an operation's adjoint.</span></span>

> [!NOTE]
> <span data-ttu-id="ba218-137">Wenn $U $ die von einem Vorgang implementierte einheitliche Transformation ist `U` , `Adjoint U` stellt die einheitliche Transformation $U ^ \dagger $ dar, die die komplexe konjugierte Transformation ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-137">If $U$ is the unitary transformation implemented by an operation `U`, then `Adjoint U` represents the unitary transformation $U^\dagger$, which is the complex conjugate transpose.</span></span>
> <span data-ttu-id="ba218-138">Wenn Sie einen Vorgang nacheinander anwenden und dessen Adjoint in einen Zustand versetzt wird, bleibt der Zustand unverändert, wie in der Tatsache veranschaulicht, dass $UU ^ \dagger = U ^ \dagger U = \id $ die Identitätsmatrix ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-138">Successively applying an operation and then its adjoint to a state leaves the state unchanged, as illustrated by the fact that $UU^\dagger = U^\dagger U = \id$, the identity matrix.</span></span>
> <span data-ttu-id="ba218-139">Die einheitliche Darstellung eines kontrollierten Vorgangs ist etwas flexibler, aber weitere Informationen finden Sie unter [Quantum Computing Concepts: Multiple Qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span><span class="sxs-lookup"><span data-stu-id="ba218-139">The unitary representation of a controlled operation is slightly more nuanced, but you can find more details at [Quantum computing concepts: multiple qubits](xref:microsoft.quantum.concepts.multiple-qubits).</span></span>

<span data-ttu-id="ba218-140">Im folgenden Abschnitt wird beschrieben, wie Sie diese verschiedenen Spezialisierungs Informationen in Ihrem Code aufzurufen Q# und wie Sie Vorgänge zur Unterstützung definieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-140">The following section describes how to call these various specializations in your Q# code, and how to define operations to support them.</span></span>

### <a name="calling-operation-specializations"></a><span data-ttu-id="ba218-141">Aufrufen von Vorgangs Spezialisierungs Vorgängen</span><span class="sxs-lookup"><span data-stu-id="ba218-141">Calling operation specializations</span></span>

<span data-ttu-id="ba218-142">Ein *Funktor* in Q# ist eine Factory, die einen neuen Vorgang aus einem anderen Vorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-142">A *functor* in Q# is a factory that defines a new operation from another operation.</span></span>
<span data-ttu-id="ba218-143">Die beiden standardfunktoren in Q# sind `Adjoint` und `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="ba218-143">The two standard functors in Q# are `Adjoint` and `Controlled`.</span></span>

<span data-ttu-id="ba218-144">Funktoren haben Zugriff auf die Implementierung des Basis Vorgangs, wenn die Implementierung des neuen Vorgangs definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-144">Functors have access to the implementation of the base operation when defining the implementation of the new operation.</span></span>
<span data-ttu-id="ba218-145">Daher können Funktoren komplexere Funktionen als herkömmliche Funktionen höherer Ebene ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba218-145">Thus, functors can perform more complex functions than traditional higher-level functions.</span></span> <span data-ttu-id="ba218-146">Funktoren haben keine Darstellung im Q# Typsystem.</span><span class="sxs-lookup"><span data-stu-id="ba218-146">Functors do not have a representation in the Q# type system.</span></span> <span data-ttu-id="ba218-147">Daher ist es derzeit nicht möglich, Sie an eine Variable zu binden oder Sie als Argumente zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ba218-147">It is thus currently not possible to bind them to a variable or pass them as arguments.</span></span> 

<span data-ttu-id="ba218-148">Verwenden Sie ein Funktor, indem Sie es auf einen Vorgang anwenden, der einen neuen Vorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ba218-148">Use a functor by applying it to an operation, which returns a new operation.</span></span>
<span data-ttu-id="ba218-149">Wenn Sie das Funktor beispielsweise auf den-Vorgang anwenden, wird `Adjoint` `Y` der neue-Vorgang zurückgegeben `Adjoint Y` .</span><span class="sxs-lookup"><span data-stu-id="ba218-149">For example, applying the `Adjoint` functor to the `Y` operation returns the new operation `Adjoint Y`.</span></span> <span data-ttu-id="ba218-150">Sie können den neuen Vorgang wie jeden anderen Vorgang aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ba218-150">You can invoke the new operation like any other operation.</span></span>
<span data-ttu-id="ba218-151">Damit ein Vorgang die Anwendung des-oder- `Adjoint` `Controlled` funktors unterstützt, muss der Rückgabetyp notwendigerweise sein `Unit` .</span><span class="sxs-lookup"><span data-stu-id="ba218-151">For an operation to support the application of the `Adjoint` or `Controlled` functors, its return type necessarily needs to be `Unit`.</span></span> 

#### <a name="adjoint-functor"></a><span data-ttu-id="ba218-152">`Adjoint`Funktionselement</span><span class="sxs-lookup"><span data-stu-id="ba218-152">`Adjoint` functor</span></span>

<span data-ttu-id="ba218-153">Folglich `Adjoint Y(q1)` wendet das `Adjoint` Funktor auf den `Y` Vorgang an, um einen neuen Vorgang zu generieren, und wendet diesen neuen Vorgang auf an `q1` .</span><span class="sxs-lookup"><span data-stu-id="ba218-153">Thus, `Adjoint Y(q1)` applies the `Adjoint` functor to the `Y` operation to generate a new operation, and applies that new operation to `q1`.</span></span>
<span data-ttu-id="ba218-154">Der neue Vorgang hat dieselbe Signatur und denselben Typ wie der Basis Vorgang `Y` .</span><span class="sxs-lookup"><span data-stu-id="ba218-154">The new operation has the same signature and type as the base operation `Y`.</span></span>
<span data-ttu-id="ba218-155">Insbesondere unterstützt der neue-Vorgang auch `Adjoint` , und unterstützt nur dann, wenn `Controlled` der Basis Vorgang durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba218-155">In particular, the new operation also supports `Adjoint`, and supports `Controlled` if and only if the base operation did.</span></span>
<span data-ttu-id="ba218-156">Das `Adjoint` Funktor ist eine eigene Umkehrung, d. h `Adjoint Adjoint Op` ., ist immer identisch mit `Op` .</span><span class="sxs-lookup"><span data-stu-id="ba218-156">The `Adjoint` functor is its own inverse; that is, `Adjoint Adjoint Op` is always the same as `Op`.</span></span>

#### <a name="controlled-functor"></a><span data-ttu-id="ba218-157">`Controlled`Funktionselement</span><span class="sxs-lookup"><span data-stu-id="ba218-157">`Controlled` functor</span></span>

<span data-ttu-id="ba218-158">Ebenso `Controlled X(controls, target)` wendet das `Controlled` Funktor auf den `X` -Vorgang an, um einen neuen-Vorgang zu generieren, und wendet diesen neuen-Vorgang auf `controls` und an `target` .</span><span class="sxs-lookup"><span data-stu-id="ba218-158">Similarly, `Controlled X(controls, target)` applies the `Controlled` functor to the `X` operation to generate a new operation, and applies that new operation to `controls` and `target`.</span></span>

> [!NOTE]
> <span data-ttu-id="ba218-159">In Q# werden von kontrollierten Versionen immer ein Array von Steuerelement-Qubits übernommen, und die Steuerung basiert immer auf allen Steuerelement-Qubits, die sich im Status "Compu()" befinden ( `PauliZ` `One` $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="ba218-159">In Q#, controlled versions always take an array of control qubits, and the controlling is always based on all of the control qubits being in the computational (`PauliZ`) `One` state, $\ket{1}$.</span></span>
> <span data-ttu-id="ba218-160">Das Steuern auf der Grundlage anderer Zustände wird erreicht, indem der entsprechende einheitliche Vorgang auf die Steuerungs Qubits vor dem kontrollierten Vorgang angewendet und dann die Umkehrung des einheitlichen Vorgangs nach dem kontrollierten Vorgang angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-160">Controlling based on other states is achieved by applying the appropriate unitary operation to the control qubits before the controlled operation, and then applying the inverses of the unitary operation after the controlled operation.</span></span>
> <span data-ttu-id="ba218-161">Wenn Sie z. b `X` . einen Vorgang vor und nach einer kontrollierten Operation auf ein Steuerelement-Qubit anwenden, steuert der Vorgang den `Zero` Zustand ($ \ket {0} $) für dieses Qubit. Anwenden eines `H` Vorgangs vor und nach der Steuerung des `PauliX` `One` Zustands, d. h.-1 eigen Wert von Pauli X, $ \ket {-} \mathrel{: =} (\ket {0} -\ket {1} )/\sqrt {2} $ anstelle des- `PauliZ` `One` Zustands.</span><span class="sxs-lookup"><span data-stu-id="ba218-161">For example, applying an `X` operation to a control qubit before and after a controlled operation causes the operation to control on the `Zero` state ($\ket{0}$) for that qubit; applying an `H` operation before and after controls on the `PauliX` `One` state, that is -1 eigenvalue of Pauli X, $\ket{-} \mathrel{:=} (\ket{0} - \ket{1}) / \sqrt{2}$ rather than the `PauliZ` `One` state.</span></span>

<span data-ttu-id="ba218-162">Bei Angabe eines Vorgangs Ausdrucks können Sie mithilfe des-funktors einen neuen Vorgangs Ausdruck bilden `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="ba218-162">Given an operation expression, you can form a new operation expression by using the `Controlled` functor.</span></span>
<span data-ttu-id="ba218-163">Die Signatur des neuen Vorgangs basiert auf der Signatur des ursprünglichen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ba218-163">The signature of the new operation is based on the signature of the original operation.</span></span>
<span data-ttu-id="ba218-164">Der Ergebnistyp ist identisch, aber der Eingabetyp ist ein zwei Tupel mit einem Qubit-Array, das die Steuerelement-Qubit (s) als erstes Element und die Argumente des ursprünglichen Vorgangs als zweites Element enthält.</span><span class="sxs-lookup"><span data-stu-id="ba218-164">The result type is the same, but the input type is a two-tuple with a qubit array that holds the control qubit(s) as the first element and the arguments of the original operation as the second element.</span></span>
<span data-ttu-id="ba218-165">Der neue-Vorgang unterstützt `Controlled` , und unterstützt `Adjoint` nur dann, wenn der ursprüngliche Vorgang durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ba218-165">The new operation supports `Controlled`, and will support `Adjoint` if and only if the original operation did.</span></span>

<span data-ttu-id="ba218-166">Wenn für den ursprünglichen Vorgang nur ein einzelnes Argument benötigt wurde, wird hier die [entsprechgabe von Singleton-Tupeln](xref:microsoft.quantum.guide.types) berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ba218-166">If the original operation took only a single argument, then [singleton tuple equivalence](xref:microsoft.quantum.guide.types) comes into play here.</span></span>
<span data-ttu-id="ba218-167">Beispiels `Controlled X` Weise ist die gesteuerte Version des `X` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ba218-167">For instance, `Controlled X` is the controlled version of the `X` operation.</span></span> 
<span data-ttu-id="ba218-168">`X`weist den Typ auf `(Qubit => Unit is Adj + Ctl)` , `Controlled X` hat also `((Qubit[], (Qubit)) => Unit is Adj + Ctl)` den Typ; aufgrund der Äquivalenz von Singleton-Tupeln ist dies identisch mit `((Qubit[], Qubit) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="ba218-168">`X` has type `(Qubit => Unit is Adj + Ctl)`, so `Controlled X` has type `((Qubit[], (Qubit)) => Unit is Adj + Ctl)`; because of singleton tuple equivalence, this is the same as `((Qubit[], Qubit) => Unit is Adj + Ctl)`.</span></span>

<span data-ttu-id="ba218-169">Wenn der Basis Vorgang mehrere Argumente benötigt hat, denken Sie daran, die entsprechenden Argumente der kontrollierten Version des Vorgangs in Klammern einzuschließen, um Sie in ein Tupel zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-169">If the base operation took several arguments, remember to enclose the corresponding arguments of the controlled version of the operation in parentheses to convert them into a tuple.</span></span>
<span data-ttu-id="ba218-170">Beispiels `Controlled Rz` Weise ist die gesteuerte Version des `Rz` Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="ba218-170">For instance, `Controlled Rz` is the controlled version of the `Rz` operation.</span></span> 
<span data-ttu-id="ba218-171">`Rz`weist den Typ auf `((Double, Qubit) => Unit is Adj + Ctl)` , hat also den `Controlled Rz` Typ `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="ba218-171">`Rz` has type `((Double, Qubit) => Unit is Adj + Ctl)`, so `Controlled Rz` has type `((Qubit[], (Double, Qubit)) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="ba218-172">Daher ist `Controlled Rz(controls, (0.1, target))` ein gültiger Aufruf von `Controlled Rz` (Beachten Sie die Klammern `0.1, target` ).</span><span class="sxs-lookup"><span data-stu-id="ba218-172">Thus, `Controlled Rz(controls, (0.1, target))` would be a valid invocation of `Controlled Rz` (note the parentheses around `0.1, target`).</span></span>

<span data-ttu-id="ba218-173">Als weiteres Beispiel `CNOT(control, target)` kann als implementiert werden `Controlled X([control], target)` .</span><span class="sxs-lookup"><span data-stu-id="ba218-173">As another example, `CNOT(control, target)` can be implemented as `Controlled X([control], target)`.</span></span> <span data-ttu-id="ba218-174">Wenn ein Ziel von zwei Steuerungs Qubits (ccnot) gesteuert werden soll, verwenden Sie eine- `Controlled X([control1, control2], target)` Anweisung.</span><span class="sxs-lookup"><span data-stu-id="ba218-174">If a target should be controlled by two control qubits (CCNOT), use a `Controlled X([control1, control2], target)` statement.</span></span>

#### `Controlled Adjoint` 

<span data-ttu-id="ba218-175">Das `Controlled` -und das- `Adjoint` funktorin werden angewendet, sodass es keinen Unterschied zwischen dem Anwenden von `Controlled Adjoint Op` oder gibt `Adjoint Controlled Op`</span><span class="sxs-lookup"><span data-stu-id="ba218-175">The `Controlled` and `Adjoint` functors commute, so there is no difference between applying `Controlled Adjoint Op` or `Adjoint Controlled Op`.</span></span>


## <a name="defining-controlled-and-adjoint-implementations"></a><span data-ttu-id="ba218-176">Definieren von kontrollierten und Adjoint-Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ba218-176">Defining Controlled and Adjoint Implementations</span></span>

<span data-ttu-id="ba218-177">In der ersten Vorgangs Deklaration in den vorherigen Beispielen wurden die Vorgänge `BitFlip` und `DecodeSuperdense` mit Signaturen `(Qubit => Unit)` `((Qubit, Qubit) => (Result, Result))` bzw. definiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-177">In the first operation declaration in the previous examples, the operations `BitFlip` and `DecodeSuperdense` were defined with signatures `(Qubit => Unit)` and `((Qubit, Qubit) => (Result, Result))`, respectively.</span></span>
<span data-ttu-id="ba218-178">Wie z. b. `DecodeSuperdense` Messungen, ist es kein einheitlicher Vorgang. Daher könnten weder die kontrollierten noch die nicht zusammenhängenden Spezialisierungs Maßnahmen vorhanden sein `Unit` .</span><span class="sxs-lookup"><span data-stu-id="ba218-178">As `DecodeSuperdense` includes measurements, it is not a unitary operation, and therefore neither controlled not adjoint specializations could exist (recall the related requirement that such an operation return `Unit`).</span></span>
<span data-ttu-id="ba218-179">Wenn Sie jedoch `BitFlip` einfach den einheitlichen <xref:microsoft.quantum.intrinsic.x> Vorgang ausführen, können Sie ihn mit beiden Spezialisierungs Vorgängen definieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-179">However, as `BitFlip` simply performs the unitary <xref:microsoft.quantum.intrinsic.x> operation, you could have defined it with both specializations.</span></span>

<span data-ttu-id="ba218-180">In diesem Abschnitt wird erläutert, wie Sie das vorhanden sein von Spezialisierungs Funktionen in die Q# Vorgangs Deklarationen einschließen und somit die Möglichkeit haben, in Verbindung mit dem-oder dem- `Adjoint` `Controlled` funktors aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ba218-180">This section details how to include the existence of specializations in your Q# operation declarations, hence giving them the ability to called in conjunction with the `Adjoint` or `Controlled` functors.</span></span>
<span data-ttu-id="ba218-181">Weitere Informationen zu einigen Situationen, in denen es entweder gültig oder nicht zulässig ist, bestimmte Spezialisierungs Informationen zu deklarieren, finden Sie unter Umstände für die Überprüfung [von Spezialisierungs](#circumstances-for-validly-defining-specializations) Informationen in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="ba218-181">For more information about some of the situations in which it is either valid or not valid to declare certain specializations, see [Circumstances for validly defining specializations](#circumstances-for-validly-defining-specializations) in this article.</span></span>

<span data-ttu-id="ba218-182">Vorgangs Merkmale definieren, welche Arten von Funktions tüktoren Sie auf den deklarierten Vorgang anwenden können und welche Auswirkungen Sie haben.</span><span class="sxs-lookup"><span data-stu-id="ba218-182">Operation characteristics define what kinds of functors you can apply to the declared operation, and what effect they have.</span></span> <span data-ttu-id="ba218-183">Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur deklariert werden, insbesondere über eine Anmerkung mit den Vorgangs Merkmalen: entweder `is Adj` , `is Ctl` oder `is Adj + Ctl` .</span><span class="sxs-lookup"><span data-stu-id="ba218-183">The existence of these specializations can be declared as part of the operation signature, specifically through an annotation with the operation characteristics: either `is Adj`, `is Ctl`, or `is Adj + Ctl`.</span></span>
<span data-ttu-id="ba218-184">Die tatsächliche Implementierung jeder Spezialisierung kann entweder *implizit* oder *explizit* definiert werden.</span><span class="sxs-lookup"><span data-stu-id="ba218-184">The actual implementation of each specialization can either be *implicitly* or *explicitly* defined.</span></span>

### <a name="implicitly-specifying-implementations"></a><span data-ttu-id="ba218-185">Implizit angeben von Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ba218-185">Implicitly specifying implementations</span></span>

<span data-ttu-id="ba218-186">In diesem Fall besteht der Text der Vorgangs Deklaration ausschließlich aus der Standard Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ba218-186">In this case, the body of the operation declaration consists solely of the default implementation.</span></span> <span data-ttu-id="ba218-187">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ba218-187">For example:</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```
<span data-ttu-id="ba218-188">Hier wird die entsprechende Implementierung für jede solche implizit deklarierte Spezialisierung automatisch vom Compiler generiert, die ausgeführt werden soll, wenn `Adjoint` die `Controlled` Funktoren oder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba218-188">Here, the corresponding implementation for each such implicitly declared specialization is automatically generated by the compiler, to be performed if the `Adjoint` or `Controlled` functors are used.</span></span>

<span data-ttu-id="ba218-189">Ein-Rückruf würde also dazu führen, dass `Adjoint PrepareEntangledPair` der Compiler das Adjoint von `CNOT` und dann das Adjoint von implementiert `H` .</span><span class="sxs-lookup"><span data-stu-id="ba218-189">So, a call of `Adjoint PrepareEntangledPair` would result in the compiler implementing the adjoint of `CNOT` and then the adjoint of `H`.</span></span>
<span data-ttu-id="ba218-190">Diese einzelnen Vorgänge sind beide selbst Adjoint, sodass der resultierende `Adjoint PrepareEntangledPair` Vorgang einfach aus der Anwendung `CNOT(here, there)` und dann besteht `H(here)` .</span><span class="sxs-lookup"><span data-stu-id="ba218-190">These individual operations are both self-adjoint, so the resulting `Adjoint PrepareEntangledPair` operation would simply consist of applying `CNOT(here, there)` and then `H(here)`.</span></span>
<span data-ttu-id="ba218-191">Daher können Sie das `DecodeSuperdense` im vorherigen Beispiel mit einem kompakteren schreiben, indem Sie das Adjoint von verwenden, `PrepareEntangledPair` um den entzickten Zustand wieder in ein nicht verwinkelter Qubits-paar umzuwandeln:</span><span class="sxs-lookup"><span data-stu-id="ba218-191">Hence you can use this to write the `DecodeSuperdense` in the previous example more compactly, by using the adjoint of `PrepareEntangledPair` to transform the entangled state back into an unentangled pair of qubits:</span></span>

```qsharp
operation DecodeSuperdense(here : Qubit, there : Qubit) : (Result, Result) {
    Adjoint PrepareEntangledPair(there, here);

    let firstBit = M(there);
    let secondBit = M(here);

    return (firstBit, secondBit);
}
```

<span data-ttu-id="ba218-192">Die-Anmerkung mit den Vorgangs Merkmalen in der Deklaration ist hilfreich, um sicherzustellen, dass der Compiler automatisch andere Spezialisierungs Vorgänge auf der Grundlage der Standard Implementierung generiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-192">The annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="ba218-193">Beim Entwerfen von Vorgängen für die Verwendung mit Funktoren sind einige wichtige Einschränkungen zu beachten.</span><span class="sxs-lookup"><span data-stu-id="ba218-193">There are several important limitations to consider when designing operations for use with functors.</span></span>
<span data-ttu-id="ba218-194">In den meisten Fällen können Spezialisierungs Vorgänge für einen Vorgang, der den Ausgabewert eines beliebigen anderen Vorgangs verwendet, nicht automatisch vom Compiler generiert werden, da er *nicht* eindeutig ist, wie die Anweisungen in einem solchen Vorgang neu angeordnet werden, um denselben Effekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ba218-194">Most critically, specializations for an operation that uses the output value of any other operation *cannot* be auto-generated by the compiler, as it is ambiguous how to reorder the statements in such an operation to obtain the same effect.</span></span>

<span data-ttu-id="ba218-195">Daher ist es häufig hilfreich, die verschiedenen Implementierungen explizit anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ba218-195">Therefore, it is often useful to explicitly specify the various implementations.</span></span>

### <a name="explicitly-specifying-implementations"></a><span data-ttu-id="ba218-196">Explizite Angabe von Implementierungen</span><span class="sxs-lookup"><span data-stu-id="ba218-196">Explicitly specifying implementations</span></span>

<span data-ttu-id="ba218-197">Wenn der Compiler die Implementierung nicht generieren kann, können Sie ihn explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="ba218-197">In the case where the compiler cannot generate the implementation, you can specify it explicitly.</span></span> <span data-ttu-id="ba218-198">Solche expliziten Spezialisierungs Deklarationen können aus einer geeigneten *Generierungs Direktive* oder einer benutzerdefinierten Implementierung bestehen.</span><span class="sxs-lookup"><span data-stu-id="ba218-198">Such explicit specialization declarations can consist of a suitable *generation directive* or a user-defined implementation.</span></span>
<span data-ttu-id="ba218-199">Im folgenden finden Sie die vollständige Palette der Möglichkeiten mit einigen Beispielen für eine explizite Spezialisierung.</span><span class="sxs-lookup"><span data-stu-id="ba218-199">Following are the full range of possibilities, with some examples of explicit specialization.</span></span> 


#### <a name="explicit-specialization-declarations"></a><span data-ttu-id="ba218-200">Explizite Spezialisierungs Deklarationen</span><span class="sxs-lookup"><span data-stu-id="ba218-200">Explicit specialization declarations</span></span>

<span data-ttu-id="ba218-201">Q#Vorgänge können die folgenden expliziten Spezialisierungs Deklarationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="ba218-201">Q# operations can contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="ba218-202">Die `body` Spezialisierung gibt die Implementierung des Vorgangs ohne angewendete Funktoren an.</span><span class="sxs-lookup"><span data-stu-id="ba218-202">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="ba218-203">Die `adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit `Adjoint` angewendetem Funktionselement an.</span><span class="sxs-lookup"><span data-stu-id="ba218-203">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="ba218-204">Die `controlled` Spezialisierung gibt die Implementierung des Vorgangs mit `Controlled` angewendetem Funktionselement an.</span><span class="sxs-lookup"><span data-stu-id="ba218-204">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="ba218-205">Die `controlled adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit den `Adjoint` `Controlled` angewendeten-und-Funktoren an.</span><span class="sxs-lookup"><span data-stu-id="ba218-205">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="ba218-206">Diese Spezialisierung kann auch benannt werden `adjoint controlled` , da die beiden Funktoren in den Weg gehen.</span><span class="sxs-lookup"><span data-stu-id="ba218-206">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="ba218-207">Eine Vorgangs Spezialisierung besteht aus dem Spezialisierungs Kennzeichen (z. b. `body` oder `adjoint` ), gefolgt von einem der folgenden:</span><span class="sxs-lookup"><span data-stu-id="ba218-207">An operation specialization consists of the specialization tag (for example, `body` or `adjoint`) followed by one of:</span></span>

- <span data-ttu-id="ba218-208">Eine explizite Deklaration, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ba218-208">An explicit declaration as described in the following.</span></span>
- <span data-ttu-id="ba218-209">Eine- *Direktive* , die dem Compiler mitteilt, *wie* die Spezialisierung generiert werden soll, einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="ba218-209">A *directive* that tells the compiler *how* to generate the specialization, one of:</span></span>
  - <span data-ttu-id="ba218-210">`intrinsic`Gibt an, dass der Zielcomputer die Spezialisierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ba218-210">`intrinsic`, which indicates that the target machine provides the specialization.</span></span>
  - <span data-ttu-id="ba218-211">`distribute`wird mit den `controlled` -und- `controlled adjoint` Spezialisierungs-verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba218-211">`distribute`, used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="ba218-212">Bei Verwendung mit `controlled` wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in angewendet wird `body` .</span><span class="sxs-lookup"><span data-stu-id="ba218-212">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="ba218-213">Bei Verwendung mit `controlled adjoint` wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in der Spezialisierung anwendet `adjoint` .</span><span class="sxs-lookup"><span data-stu-id="ba218-213">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="ba218-214">`invert`Gibt an, dass der Compiler die `adjoint` Spezialisierung durch Umkehren von berechnen soll, indem `body` z. b. die Reihenfolge der Vorgänge umkehren und das Adjoint-Attribut auf jedes angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-214">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, for example, reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="ba218-215">Wenn Sie mit verwendet `adjoint controlled` wird, gibt dies an, dass der Compiler die Spezialisierung durch Umkehren der `controlled` Spezialisierung berechnen soll.</span><span class="sxs-lookup"><span data-stu-id="ba218-215">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="ba218-216">`self`, um anzugeben, dass die Adjoint-Spezialisierung mit der Spezialisierung identisch ist `body` .</span><span class="sxs-lookup"><span data-stu-id="ba218-216">`self`, to indicate that the adjoint specialization is the same as the `body` specialization.</span></span>
    <span data-ttu-id="ba218-217">`self`Die Verwendung von ist für die `adjoint` -und- `adjoint controlled` Spezialisierung zulässig.</span><span class="sxs-lookup"><span data-stu-id="ba218-217">Using `self` is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="ba218-218">Für `adjoint controlled` `self` impliziert, dass die `adjoint controlled` Spezialisierung mit der Spezialisierung identisch ist `controlled` .</span><span class="sxs-lookup"><span data-stu-id="ba218-218">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="ba218-219">`auto`, um anzugeben, dass der Compiler eine entsprechende anzuwendende Direktive auswählen soll.</span><span class="sxs-lookup"><span data-stu-id="ba218-219">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="ba218-220">Sie können `auto` für die Spezialisierung nicht verwenden `body` .</span><span class="sxs-lookup"><span data-stu-id="ba218-220">You cannot use`auto` for the `body` specialization.</span></span>

<span data-ttu-id="ba218-221">Die-Direktiven und `auto` alle erfordern ein Schließ Endes Semikolon `;` .</span><span class="sxs-lookup"><span data-stu-id="ba218-221">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="ba218-222">Die- `auto` Direktive wird in die folgende generierte-Direktive aufgelöst, wenn eine explizite Deklaration von `body` bereitgestellt wird:</span><span class="sxs-lookup"><span data-stu-id="ba218-222">The `auto` directive resolves to the following generated directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="ba218-223">Die `adjoint` Spezialisierung wird gemäß der-Direktive generiert `invert` .</span><span class="sxs-lookup"><span data-stu-id="ba218-223">The `adjoint` specialization generates according to the directive `invert`.</span></span>
- <span data-ttu-id="ba218-224">Die `controlled` Spezialisierung wird gemäß der-Direktive generiert `distribute` .</span><span class="sxs-lookup"><span data-stu-id="ba218-224">The `controlled` specialization generates according to the directive `distribute`.</span></span>
- <span data-ttu-id="ba218-225">Die `adjoint controlled` Spezialisierung wird gemäß der-Direktive generiert `invert` , wenn eine explizite Deklaration für `controlled` angegeben ist, aber nicht für `adjoint` , und `distribute` andernfalls.</span><span class="sxs-lookup"><span data-stu-id="ba218-225">The `adjoint controlled` specialization  generates according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="ba218-226">Wenn es sich um einen eigenständigen Vorgang handelt, geben Sie entweder die Adjoint-oder die kontrollierte Adjoint-Spezialisierung mithilfe der Generations Direktive explizit `self` an, damit der Compiler diese Informationen für Optimierungszwecke nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="ba218-226">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="ba218-227">Eine Spezialisierungs Deklaration, die eine benutzerdefinierte Implementierung enthält, besteht aus einem argumenttupel, gefolgt von einem Anweisungsblock mit dem Q# Code, der die Spezialisierung implementiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-227">A specialization declaration containing a user-defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="ba218-228">In der Argumentliste `...` wird verwendet, um die Argumente darzustellen, die für den Vorgang als Ganzes deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="ba218-228">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="ba218-229">Für `body` und `adjoint` sollte die Argumentliste immer sein `(...)` . bei `controlled` und `adjoint controlled` sollte die Argumentliste ein Symbol sein, das das Array von Steuerelement-Qubits, gefolgt von `...` , in Klammern darstellt, z. b `(controls,...)` ..</span><span class="sxs-lookup"><span data-stu-id="ba218-229">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

### <a name="examples"></a><span data-ttu-id="ba218-230">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba218-230">Examples</span></span>

<span data-ttu-id="ba218-231">Eine Vorgangs Deklaration kann so einfach wie die folgende sein, die den primitiven Pauli X-Vorgang definiert:</span><span class="sxs-lookup"><span data-stu-id="ba218-231">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```
<span data-ttu-id="ba218-232">Beachten Sie, dass das Adjoint des Pauli X-Vorgangs mit der-Direktive definiert ist, `self` da definitionsgemäß `X` eine eigene Umkehrung ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-232">Note that the adjoint of the Pauli X operation is defined with the directive `self` because by definition `X` is its own inverse.</span></span>

<span data-ttu-id="ba218-233">Im vorherigen `PrepareEntangledPair` Beispiel entspricht der Code dem folgenden Code, der explizite Spezialisierungs Deklarationen enthält:</span><span class="sxs-lookup"><span data-stu-id="ba218-233">In the earlier `PrepareEntangledPair` example, the code is equivalent to the following code containing explicit specialization declarations:</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    adjoint auto; // auto-generate adjoint specialization
    controlled auto; // auto-generate controlled specialization
    controlled adjoint auto; // auto-generate controlled adjoint specialization
}
```
<span data-ttu-id="ba218-234">Das Schlüsselwort `auto` gibt an, dass der Compiler bestimmen soll, wie die Spezialisierungs Implementierung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba218-234">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>

#### <a name="user-defined-specialization-implementation"></a><span data-ttu-id="ba218-235">Implementierung benutzerdefinierter Spezialisierungen</span><span class="sxs-lookup"><span data-stu-id="ba218-235">User-defined specialization implementation</span></span>

<span data-ttu-id="ba218-236">Wenn der Compiler die Implementierung für eine bestimmte Spezialisierung nicht automatisch generieren kann oder wenn eine effizientere Implementierung angegeben werden kann, können Sie die Implementierung manuell definieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-236">If the compiler cannot generate the implementation for a certain specialization automatically, or if a more efficient implementation can be given, then you can manually define the implementation.</span></span>

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit
is Ctl + Adj {
    body (...) { // default body specialization
        H(here);
        CNOT(here, there);
    }

    controlled (cs, ...) { // user-defined implementation for the controlled specialization
        Controlled H(cs, here);
        Controlled X(cs + [here], there);
    }

    adjoint invert; 
    controlled adjoint invert; 
}
```
<span data-ttu-id="ba218-237">Im vorherigen Beispiel gibt an, `adjoint invert;` dass die Adjoint-Spezialisierung durch das Umkehren der Text Implementierung generiert werden soll, und `controlled adjoint invert;` gibt an, dass die kontrollierte Adjoint-Spezialisierung generiert werden soll, indem die angegebene Implementierung der kontrollierten Spezialisierung umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-237">In the previous example, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="ba218-238">Wenn eine oder mehrere Spezialisierungen neben dem Standardtext explizit deklariert werden müssen, muss die Implementierung für den Standardtext ebenfalls in eine passende Spezialisierungs Deklaration integriert werden:</span><span class="sxs-lookup"><span data-stu-id="ba218-238">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

```qsharp
operation CountOnes(qubits: Qubit[]) : Int {

    body (...) // default body specialization
    {
        mutable n = 0;
        for (qubit in qubits) {
            set n += M(q) == One ? 1 | 0;
        }
        return n;
    }

    ...
```

### <a name="circumstances-for-validly-defining-specializations"></a><span data-ttu-id="ba218-239">Umstände für das valide definieren von Spezialisierungs Informationen</span><span class="sxs-lookup"><span data-stu-id="ba218-239">Circumstances for validly defining specializations</span></span>

#### <a name="operation-declarations-with-adjointcontrolled"></a><span data-ttu-id="ba218-240">Vorgangs Deklarationen mit Adjoint/kontrolliertem</span><span class="sxs-lookup"><span data-stu-id="ba218-240">Operation declarations with adjoint/controlled</span></span>

<span data-ttu-id="ba218-241">Es ist zulässig, einen Vorgang ohne Adjoint oder kontrollierte Versionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ba218-241">It is legal to specify an operation with no adjoint or controlled versions.</span></span> <span data-ttu-id="ba218-242">Beispielsweise haben Messungs Vorgänge keinen, weil Sie nicht invertierbar oder steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="ba218-242">For instance, measurement operations have neither because they are not invertible or controllable.</span></span>

<span data-ttu-id="ba218-243">Ein-Vorgang unterstützt die `Adjoint` -und- `Controlled` Funktoren, wenn seine Deklaration eine implizite oder explizite Deklaration der jeweiligen Spezialisierungs Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="ba218-243">An operation supports the `Adjoint` and `Controlled` functors if its declaration contains an implicit or explicit declaration of the respective specializations.</span></span>

<span data-ttu-id="ba218-244">Eine explizit deklarierte Adjoint/gesteuerte Spezialisierung impliziert das vorhanden sein einer Adjoint/kontrollierten Spezialisierung.</span><span class="sxs-lookup"><span data-stu-id="ba218-244">An explicitly declared adjoint/controlled specialization implies the existence of an adjoint/controlled specialization.</span></span> 

<span data-ttu-id="ba218-245">Bei einem Vorgang, dessen Text Wiederholungs-bis-Erfolg-Schleifen, Set-Anweisungen, Messungen, Rückgabe Anweisungen oder Aufrufe von anderen Vorgängen enthält, die das Funktor nicht unterstützen `Adjoint` , ist das automatische Erstellen einer Adjoint-Spezialisierung nach der- `invert` oder- `auto` Direktive nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="ba218-245">For an operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

<span data-ttu-id="ba218-246">Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die das `Controlled` Funktor nicht unterstützen, ist das automatische Erstellen einer kontrollierten Spezialisierung nach der- `distribute` oder- `auto` Direktive nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="ba218-246">For an operation whose body contains calls to other operations that do not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

#### <a name="controlled-adjoint"></a><span data-ttu-id="ba218-247">Kontrollierter Adjoint</span><span class="sxs-lookup"><span data-stu-id="ba218-247">Controlled Adjoint</span></span>

<span data-ttu-id="ba218-248">Die kontrollierte Adjoint-Version eines Vorgangs gibt an, wie eine durch eine Quantum gesteuerte Version des Adjoint-Vorgangs des Vorgangs implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-248">The controlled adjoint version of an operation specifies how to implement a quantum-controlled version of the adjoint of the operation.</span></span>
<span data-ttu-id="ba218-249">Es ist zulässig, einen Vorgang ohne kontrollierte Adjoint-Version anzugeben. Messvorgänge haben beispielsweise keine kontrollierte Adjoint-Version, da Sie weder steuerbar noch invertierbar sind.</span><span class="sxs-lookup"><span data-stu-id="ba218-249">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="ba218-250">Eine kontrollierte Adjoint-Spezialisierung für einen Vorgang muss nur dann vorhanden sein, wenn sowohl ein Adjoint-als auch eine gesteuerte Spezialisierung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ba218-250">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="ba218-251">In diesem Fall wird das vorhanden sein der kontrollierten Adjoint-Spezialisierung abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="ba218-251">In that case, the existence of the controlled adjoint specialization is inferred.</span></span> <span data-ttu-id="ba218-252">Wenn keine Implementierung explizit definiert ist, generiert die Kompilierung eine entsprechende Spezialisierung.</span><span class="sxs-lookup"><span data-stu-id="ba218-252">If no implementation is explicitly defined, the compile generates an appropriate specialization.</span></span>

<span data-ttu-id="ba218-253">Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die nicht über eine kontrollierte Adjoint-Version verfügen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach der- `invert` ,- `distribute` oder- `auto` Direktive nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="ba218-253">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute`, or `auto` directive is not possible.</span></span>


### <a name="type-compatibility"></a><span data-ttu-id="ba218-254">Typkompatibilität</span><span class="sxs-lookup"><span data-stu-id="ba218-254">Type Compatibility</span></span>

<span data-ttu-id="ba218-255">Verwenden Sie einen Vorgang mit zusätzlichen Funktoren, die überall unterstützt werden, wenn Sie einen Vorgang mit weniger Funktoren, aber derselben Signatur verwenden.</span><span class="sxs-lookup"><span data-stu-id="ba218-255">Use an operation with additional functors supported anywhere you use an operation with fewer functors but the same signature.</span></span> <span data-ttu-id="ba218-256">Verwenden Sie beispielsweise einen Vorgang des Typs an einer beliebigen Stelle, an `(Qubit => Unit is Adj)` der Sie einen Vorgang des Typs verwenden `(Qubit => Unit)` .</span><span class="sxs-lookup"><span data-stu-id="ba218-256">For instance, use an operation of type `(Qubit => Unit is Adj)` anywhere you use an operation of type `(Qubit => Unit)`.</span></span>

<span data-ttu-id="ba218-257">Q#ist *kovariant* in Bezug auf Aufruf Bare Rückgabe Typen: ein Aufruf barer, der einen-Typ zurückgibt, `'A` ist mit einem Aufruf baren-Element mit demselben Eingabetyp und einem Ergebnistyp kompatibel, der mit kompatibel ist `'A` .</span><span class="sxs-lookup"><span data-stu-id="ba218-257">Q# is *covariant* with respect to callable return types: a callable that returns a type `'A` is compatible with a callable with the same input type and a result type that is compatible with `'A` .</span></span>

<span data-ttu-id="ba218-258">Q#ist *kontra Variant* in Bezug auf Eingabetypen: ein Aufruf bares Element, das einen Typ `'A` als Eingabe annimmt, ist mit einem Aufruf baren mit dem gleichen Ergebnistyp und einem Eingabetyp kompatibel, der mit kompatibel ist `'A` .</span><span class="sxs-lookup"><span data-stu-id="ba218-258">Q# is *contravariant* with respect to input types: a callable that takes a type `'A` as input is compatible with a callable with the same result type and an input type that is compatible with `'A`.</span></span>

<span data-ttu-id="ba218-259">Das heißt, wenn die folgenden Definitionen definiert sind,</span><span class="sxs-lookup"><span data-stu-id="ba218-259">That is, given the following definitions,</span></span>

```qsharp
operation Invert(qubits : Qubit[]) : Unit 
is Adj {...} 

operation ApplyUnitary(qubits : Qubit[]) : Unit 
is Adj + Ctl {...} 

function ConjugateInvertWith(
    inner : (Qubit[] => Unit is Adj),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj) {...}

function ConjugateUnitaryWith(
    inner : (Qubit[] => Unit is Adj + Ctl),
    outer : (Qubit[] => Unit is Adj))
: (Qubit[] => Unit is Adj + Ctl) {...}
```

<span data-ttu-id="ba218-260">Sie können</span><span class="sxs-lookup"><span data-stu-id="ba218-260">you can</span></span>

- <span data-ttu-id="ba218-261">Rufen Sie die Funktion `ConjugateInvertWith` mit einem `inner` Argument von `Invert` oder auf `ApplyUnitary` .</span><span class="sxs-lookup"><span data-stu-id="ba218-261">Invoke the function `ConjugateInvertWith` with an `inner` argument of either `Invert` or `ApplyUnitary`.</span></span>
- <span data-ttu-id="ba218-262">Rufen Sie die Funktion `ConjugateUnitaryWith` mit einem `inner` Argument von auf `ApplyUnitary` , jedoch nicht `Invert` .</span><span class="sxs-lookup"><span data-stu-id="ba218-262">Invoke the function `ConjugateUnitaryWith` with an `inner` argument of `ApplyUnitary`, but not `Invert`.</span></span>
- <span data-ttu-id="ba218-263">Gibt einen Wert vom Typ `(Qubit[] => Unit is Adj + Ctl)` aus zurück `ConjugateInvertWith` .</span><span class="sxs-lookup"><span data-stu-id="ba218-263">Return a value of type `(Qubit[] => Unit is Adj + Ctl)` from `ConjugateInvertWith`.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba218-264">Q#0,3 hat einen signifikanten Unterschied im Verhalten von benutzerdefinierten Typen eingeführt.</span><span class="sxs-lookup"><span data-stu-id="ba218-264">Q# 0.3 introduced a significant difference in the behavior of user-defined types.</span></span>

<span data-ttu-id="ba218-265">Benutzerdefinierte Typen werden als umschließende Version des zugrunde liegenden Typs und nicht als Untertyp behandelt.</span><span class="sxs-lookup"><span data-stu-id="ba218-265">User-defined types are treated as a wrapped version of the underlying type, rather than as a subtype.</span></span>
<span data-ttu-id="ba218-266">Dies bedeutet, dass ein Wert eines benutzerdefinierten Typs nicht verwendbar ist, wenn Sie erwarten, dass ein Wert des zugrunde liegenden Typs ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-266">This means that a value of a user-defined type is not usable where you expect a value of the underlying type is.</span></span>


### <a name="conjugations"></a><span data-ttu-id="ba218-267">Konjugationen</span><span class="sxs-lookup"><span data-stu-id="ba218-267">Conjugations</span></span>

<span data-ttu-id="ba218-268">Im Gegensatz zu klassischen Bits ist das Freigeben von Quantum-Speicher etwas komplizierter, da das Blind Zurücksetzen von Qubits unerwünschte Auswirkungen auf die verbleibende Berechnung haben kann, wenn die Qubits noch entkoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="ba218-268">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="ba218-269">Diese Auswirkungen können vermieden werden, indem Berechnungen vor der Freigabe des Arbeitsspeichers ordnungsgemäß durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ba218-269">These effects can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="ba218-270">Ein gängiges Muster in Quantum Computing ist daher Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ba218-270">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="ba218-271">Ab Version 0,9 Q# unterstützt eine Konjugations Anweisung, die die vorherige Transformation implementiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-271">Starting with our 0.9 release, Q# supports a conjugation statement that implements the preceding transformation.</span></span> <span data-ttu-id="ba218-272">Mit dieser Anweisung kann der Vorgang `ApplyWith` folgendermaßen implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="ba218-272">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="ba218-273">Eine solche Konjugations Anweisung ist weitaus nützlicher, wenn die äußeren und inneren Transformationen nicht als Vorgänge verfügbar sind, sondern eher durch einen Block, der aus mehreren Anweisungen besteht, beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-273">Such a conjugation statement becomes far more useful if the outer and inner transformations are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="ba218-274">Die umgekehrte Transformation für die-Anweisungen, die im-Block innerhalb von definiert sind, wird automatisch vom Compiler generiert und nach Abschluss von Apply-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba218-274">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and run after the apply-block completes.</span></span>
<span data-ttu-id="ba218-275">Da alle änderbaren Variablen, die als Teil des Blocks innerhalb von verwendet werden, im Apply-Block nicht wieder hergestellt werden können, ist die generierte Transformation garantiert das Adjoint der Berechnung im within-Block.</span><span class="sxs-lookup"><span data-stu-id="ba218-275">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 


## <a name="defining-new-functions"></a><span data-ttu-id="ba218-276">Definieren neuer Funktionen</span><span class="sxs-lookup"><span data-stu-id="ba218-276">Defining New Functions</span></span>

<span data-ttu-id="ba218-277">Funktionen sind rein deterministische, klassische Routinen in Q# , die sich von Vorgängen unterscheiden, da Sie keine Auswirkungen auf die Berechnung eines Ausgabe Werts haben dürfen.</span><span class="sxs-lookup"><span data-stu-id="ba218-277">Functions are purely deterministic, classical routines in Q#, which are distinct from operations in that they are not allowed to have any effects beyond calculating an output value.</span></span>
<span data-ttu-id="ba218-278">Insbesondere können Funktionen keine Vorgänge aufzurufen. reagieren, zuordnen oder ausleihen von Qubits Stichproben von Zufallszahlen oder hängt anderweitig von dem Zustand ab, der über den Eingabe Wert zu einer Funktion hinausgeht.</span><span class="sxs-lookup"><span data-stu-id="ba218-278">In particular, functions cannot call operations; act on, allocate, or borrow qubits; sample random numbers; or otherwise depend on state beyond the input value to a function.</span></span>
<span data-ttu-id="ba218-279">Folglich Q# sind Funktionen *rein*, da Sie die gleichen Eingabewerte immer denselben Ausgabe Werten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ba218-279">As a consequence, Q# functions are *pure*, in that they always map the same input values to the same output values.</span></span>
<span data-ttu-id="ba218-280">Dieses Verhalten ermöglicht es dem Q# Compiler, sicherzustellen, wie und wann Funktionen beim Erzeugen von Vorgangs speziationen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ba218-280">This behavior allows the Q# compiler to safely reorder how and when to call functions when generating operation specializations.</span></span>

<span data-ttu-id="ba218-281">Jede Q# Quelldatei kann eine beliebige Anzahl von Funktionen definieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-281">Each Q# source file can define any number of functions.</span></span>
<span data-ttu-id="ba218-282">Funktionsnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-oder Typnamen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="ba218-282">Function names must be unique within a namespace and cannot conflict with operation or type names.</span></span>

<span data-ttu-id="ba218-283">Das Definieren einer Funktion funktioniert ähnlich wie ein Vorgang, mit dem Unterschied, dass für eine Funktion keine Adjoint-oder kontrollierten Spezialisierungs Funktionen definiert werden können.</span><span class="sxs-lookup"><span data-stu-id="ba218-283">Defining a function works similarly to defining an operation, except that no adjoint or controlled specializations can be defined for a function.</span></span>
<span data-ttu-id="ba218-284">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ba218-284">For instance:</span></span>

```qsharp
function Square(x : Double) : (Double) {
    return x * x;
}
```

<span data-ttu-id="ba218-285">oder</span><span class="sxs-lookup"><span data-stu-id="ba218-285">or</span></span> 

```qsharp
function DotProduct(a : Double[], b : Double[]) : Double {
    if (Length(a) != Length(b)) {
        fail "Arrays are not compatible";
    }

    mutable accum = 0.0;
    for (i in 0..Length(a)-1) {
        set accum += a[i] * b[i];
    }
    return accum;
}
```

### <a name="classical-logic-in-functions--good"></a><span data-ttu-id="ba218-286">Klassische Logik in Functions = = Good</span><span class="sxs-lookup"><span data-stu-id="ba218-286">Classical logic in functions == good</span></span>

<span data-ttu-id="ba218-287">Wenn dies möglich ist, ist es hilfreich, Klassische Logik in Bezug auf Funktionen anstelle von Vorgängen zu schreiben, damit Vorgänge Sie leichter verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ba218-287">Whenever it is possible to do so, it is helpful to write out classical logic in terms of functions rather than operations so that operations can more readily use it.</span></span> <span data-ttu-id="ba218-288">Wenn Sie z. b. die vorherige `Square` Deklaration als *Vorgang*geschrieben haben, konnte der Compiler nicht garantieren, dass der Aufruf mit derselben Eingabe konstant die gleichen Ausgaben erzeugt.</span><span class="sxs-lookup"><span data-stu-id="ba218-288">For example, if you had written the earlier `Square` declaration as an *operation*, then the compiler would not have been able to guarantee that calling it with the same input would consistently produce the same outputs.</span></span>

<span data-ttu-id="ba218-289">Um den Unterschied zwischen Funktionen und Vorgängen zu unterstreichen, sollten Sie das Problem der klassischen Stichprobenentnahme für eine Zufallszahl innerhalb eines- Q# Vorgangs beachten:</span><span class="sxs-lookup"><span data-stu-id="ba218-289">To underscore the difference between functions and operations, consider the problem of classically sampling a random number from within a Q# operation:</span></span>

```qsharp
operation U(target : Qubit) : Unit {

    let angle = RandomReal()
    Rz(angle, target)
}
```

<span data-ttu-id="ba218-290">Jedes Mal `U` , wenn aufgerufen wird, wird eine andere Aktion für ausgeführt `target` .</span><span class="sxs-lookup"><span data-stu-id="ba218-290">Each time that `U` is called, it has a different action on `target`.</span></span>
<span data-ttu-id="ba218-291">Insbesondere kann der Compiler nicht garantieren, dass, wenn Sie eine `adjoint auto` Spezialisierung-Deklaration hinzufügen `U` , `U(target); Adjoint U(target);` als Identität agiert (d. h. als No-OP).</span><span class="sxs-lookup"><span data-stu-id="ba218-291">In particular, the compiler cannot guarantee that if you add an `adjoint auto` specialization declaration to `U`, then `U(target); Adjoint U(target);` acts as identity (that is, as a no-op).</span></span>
<span data-ttu-id="ba218-292">Dies verstößt gegen die Definition des in [Vektoren und Matrizen](xref:microsoft.quantum.concepts.vectors)definierten Adjoint, sodass der Compiler die automatische Generierung einer Adjoint-Spezialisierung in einem Vorgang gestattet, bei dem Sie den Vorgang aufzurufen, <xref:microsoft.quantum.math.randomreal> die vom Compiler bereitgestellten Garantien sprengen würde <xref:microsoft.quantum.math.randomreal> . ist ein Vorgang, für den keine Adjoint-oder kontrollierte Version vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-292">This violates the definition of the adjoint defined in [Vectors and Matrices](xref:microsoft.quantum.concepts.vectors), such that allowing the compiler to auto-generate an adjoint specialization in an operation where you call the operation <xref:microsoft.quantum.math.randomreal> would break the guarantees provided by the compiler; <xref:microsoft.quantum.math.randomreal> is an operation for which no adjoint or controlled version exists.</span></span>

<span data-ttu-id="ba218-293">Auf der anderen Seite können Funktionsaufrufe wie z. b. `Square` sicher sein, und der Compiler wird sichergestellt, dass nur die Eingabe in beibehalten werden muss, damit die `Square` Ausgabe stabil bleibt.</span><span class="sxs-lookup"><span data-stu-id="ba218-293">On the other hand, allowing function calls such as `Square` is safe, and assures the compiler that it only needs to preserve the input to `Square` to keep its output stable.</span></span>
<span data-ttu-id="ba218-294">Daher ist es einfach, diese Logik in anderen Funktionen und Vorgängen zu verwenden, damit Sie so viel Klassische Logik wie möglich in Functions isolieren kann.</span><span class="sxs-lookup"><span data-stu-id="ba218-294">Thus, isolating as much classical logic as possible into functions makes it easy to reuse that logic in other functions and operations alike.</span></span>


## <a name="generic-type-parameterized-callables"></a><span data-ttu-id="ba218-295">Generische (typparametrisierte) callables</span><span class="sxs-lookup"><span data-stu-id="ba218-295">Generic (Type-Parameterized) Callables</span></span>

<span data-ttu-id="ba218-296">Viele Funktionen und Vorgänge, die Sie möglicherweise definieren möchten, sind nicht wirklich stark von den Typen Ihrer Eingaben abhängig, sondern verwenden nur implizit ihre Typen über eine andere Funktion oder einen anderen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ba218-296">Many functions and operations that you might wish to define do not actually heavily rely on the types of their inputs, but rather only implicitly use their types via some other function or operation.</span></span>
<span data-ttu-id="ba218-297">Sehen Sie sich beispielsweise das *Karten* Konzept an, das vielen funktionalen Sprachen gemeinsam ist. bei Angabe einer Funktion $f (x) $ und einer Auflistung von Werten $ \{ x_1, x_2, \dots, x_n \} $ gibt MAP eine neue Auflistung $ \{ f (x_1), f (x_2), \dots, f (x_n) \} $ zurück.</span><span class="sxs-lookup"><span data-stu-id="ba218-297">For example, consider the *map* concept common to many functional languages; given a function $f(x)$ and a collection of values $\{x_1, x_2, \dots, x_n\}$, map returns a new collection $\{f(x_1), f(x_2), \dots, f(x_n)\}$.</span></span>
<span data-ttu-id="ba218-298">Um dies in zu implementieren Q# , nutzen Sie die Tatsache, dass Functions die erste Klasse ist.</span><span class="sxs-lookup"><span data-stu-id="ba218-298">To implement this in Q#, take advantage of the fact that functions are first class.</span></span>
<span data-ttu-id="ba218-299">Im folgenden finden Sie ein kurzes Beispiel für die `Map` Verwendung von `T` als Platzhalter, während Sie herausfinden, welche Typen Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="ba218-299">Here is a quick example of `Map`, using `T` as a placeholder while you figure out what types you need.</span></span>

```qsharp
function Map(fn : (T -> T), values : T[]) : T[] {
    mutable mappedValues = new T[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="ba218-300">Beachten Sie, dass diese Funktion unabhängig von den tatsächlichen Typen, in denen Sie ersetzen, sehr ähnlich aussieht.</span><span class="sxs-lookup"><span data-stu-id="ba218-300">Note that this function looks very much the same no matter what actual types you substitute in.</span></span>
<span data-ttu-id="ba218-301">Eine Zuordnung von Ganzzahlen zu Paulis sieht beispielsweise genauso wie eine Zuordnung von Gleit Komma Zahlen zu Zeichen folgen aus:</span><span class="sxs-lookup"><span data-stu-id="ba218-301">A map from integers to Paulis, for instance, looks much the same as a map from floating-point numbers to strings:</span></span>

```qsharp
function MapIntsToPaulis(fn : (Int -> Pauli), values : Int[]) : Pauli[] {
    mutable mappedValues = new Pauli[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}

function MapDoublesToStrings(fn : (Double -> String), values : Double[]) : String[] {
    mutable mappedValues = new String[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="ba218-302">Im Prinzip können Sie eine Version von `Map` für jedes Paar von Typen schreiben, das auftreten, aber dies führt zu mehreren Schwierigkeiten.</span><span class="sxs-lookup"><span data-stu-id="ba218-302">In principle, you could write a version of `Map` for every pair of types that you encounter, but this introduces several difficulties.</span></span>
<span data-ttu-id="ba218-303">Wenn Sie beispielsweise einen Fehler in feststellen `Map` , müssen Sie sicherstellen, dass die Korrektur in allen Versionen von einheitlich angewendet wird `Map` .</span><span class="sxs-lookup"><span data-stu-id="ba218-303">For instance, if you find a bug in `Map`, then you must ensure that the fix is applied uniformly across all versions of `Map`.</span></span>
<span data-ttu-id="ba218-304">Wenn Sie ein neues Tupel oder einen neuen UDT erstellen, müssen Sie nun auch ein neues erstellen, `Map` um zusammen mit dem neuen Typ zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="ba218-304">Moreover, if you construct a new tuple or UDT, then you must now also construct a new `Map` to go along with the new type.</span></span>
<span data-ttu-id="ba218-305">Diese Funktion ist zwar für eine kleine Anzahl solcher Funktionen übertragbar, da Sie jedoch mehr und mehr Funktionen der gleichen Form wie erfassen `Map` , werden die Kosten für die Einführung neuer Typen in einer relativ kurzen Reihenfolge nicht sehr groß.</span><span class="sxs-lookup"><span data-stu-id="ba218-305">While this is tractable for a small number of such functions, as you collect more and more functions of the same form as `Map`, the cost of introducing new types becomes unreasonably large in fairly short order.</span></span>

<span data-ttu-id="ba218-306">Ein Großteil dieser Schwierigkeit ergibt sich jedoch aus der Tatsache, dass Sie dem Compiler nicht die erforderlichen Informationen zur Erkennung der verschiedenen Versionen von erhalten haben `Map` .</span><span class="sxs-lookup"><span data-stu-id="ba218-306">However, much of this difficulty results from the fact that you have not given the compiler the information it needs to recognize how the different versions of `Map` are related.</span></span>
<span data-ttu-id="ba218-307">Effektiv möchten Sie, dass der Compiler `Map` als eine mathematische Funktion von Q# *Typen* zu Q# Funktionen behandelt.</span><span class="sxs-lookup"><span data-stu-id="ba218-307">Effectively, you want the compiler to treat `Map` as some kind of mathematical function from Q# *types* to Q# functions.</span></span>

<span data-ttu-id="ba218-308">Q#formalisiert dieses Konzept, indem Funktionen und Vorgänge sowohl *Typparameter*als auch Ihre normalen tupelparameter aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="ba218-308">Q# formalizes this notion by allowing functions and operations to have *type parameters*, as well as their ordinary tuple parameters.</span></span>
<span data-ttu-id="ba218-309">In den vorherigen Beispielen möchten Sie sich vorstellen, `Map` dass im `Int, Pauli` ersten Fall Typparameter und `Double, String` im zweiten Fall vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="ba218-309">In the previous examples, you wish to think of `Map` as having type parameters `Int, Pauli` in the first case and `Double, String` in the second case.</span></span>
<span data-ttu-id="ba218-310">Verwenden Sie zum größten Teil diese Typparameter, als wären Sie normale Typen.</span><span class="sxs-lookup"><span data-stu-id="ba218-310">For the most part, use these type parameters as though they were ordinary types.</span></span> <span data-ttu-id="ba218-311">Verwenden Sie Werte von Typparametern, um Arrays und Tupel zu erstellen, Funktionen und Vorgänge aufzurufen und gewöhnliche oder änderbare Variablen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ba218-311">Use values of type parameters to make arrays and tuples, call functions and operations, and assign to ordinary or mutable variables.</span></span>

> [!NOTE]
> <span data-ttu-id="ba218-312">Der extremste Fall der indirekten Abhängigkeit ist die von Qubits, bei denen sich ein Q# Programm nicht direkt auf die Struktur des Typs verlassen kann, `Qubit` sondern solche Typen an andere Vorgänge und Funktionen übergeben **muss** .</span><span class="sxs-lookup"><span data-stu-id="ba218-312">The most extreme case of indirect dependence is that of qubits, where a Q# program cannot directly rely on the structure of the `Qubit` type but **must** pass such types to other operations and functions.</span></span>

<span data-ttu-id="ba218-313">Wenn Sie zum vorherigen Beispiel zurückkehren, sehen Sie, dass `Map` über Typparameter verfügen muss, eines für die Darstellung der Eingabe `fn` und eines zum Darstellen der Ausgabe `fn` .</span><span class="sxs-lookup"><span data-stu-id="ba218-313">Returning to the earlier example, then, you see that `Map` needs to have type parameters, one to represent the input to `fn` and one to represent the output from `fn`.</span></span>
<span data-ttu-id="ba218-314">In Q# wird dies durch Hinzufügen von spitzen Klammern (d `<>` . h. nicht Klammer $ \braket {} $!) nach dem Namen einer Funktion oder eines Vorgangs in der Deklaration und durch Auflisten der einzelnen Typparameter geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ba218-314">In Q#, this is written by adding angle brackets (that's `<>`, not brakets $\braket{}$!) after the name of a function or operation in its declaration, and by listing each type parameter.</span></span>
<span data-ttu-id="ba218-315">Der Name jedes Typparameters muss mit einem Tick beginnen `'` , was darauf hinweist, dass es sich um einen Typparameter handelt und nicht um einen normalen Typ (auch als *konkreter* Typ bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="ba218-315">The name of each type parameter must start with a tick `'`, indicating that it is a type parameter and not a ordinary type (also known as a *concrete* type).</span></span>
<span data-ttu-id="ba218-316">Daher `Map` wird geschrieben:</span><span class="sxs-lookup"><span data-stu-id="ba218-316">Thus, `Map`, is written:</span></span>

```qsharp
function Map<'Input, 'Output>(fn : ('Input -> 'Output), values : 'Input[]) : 'Output[] {
    mutable mappedValues = new 'Output[Length(values)];
    for (idx in 0..Length(values) - 1) {
        set mappedValues w/= idx <- fn(values[idx]);
    }
    return mappedValues;
}
```

<span data-ttu-id="ba218-317">Beachten Sie, dass die Definition von `Map<'Input, 'Output>` den previoius-Versionen sehr ähnlich aussieht.</span><span class="sxs-lookup"><span data-stu-id="ba218-317">Note that the definition of `Map<'Input, 'Output>` looks extremely similar to the previoius versions.</span></span>
<span data-ttu-id="ba218-318">Der einzige Unterschied besteht darin, dass Sie den Compiler explizit informiert haben, der `Map` nicht direkt davon abhängt `'Input` , was und `'Output` sind, sondern für alle zwei Typen funktionieren, indem Sie Sie indirekt durch verwenden `fn` .</span><span class="sxs-lookup"><span data-stu-id="ba218-318">The only difference is that you have explicitly informed the compiler that `Map` doesn't directly depend on what `'Input` and `'Output` are, but works for any two types by using them indirectly through `fn`.</span></span>
<span data-ttu-id="ba218-319">Wenn Sie `Map<'Input, 'Output>` auf diese Weise definiert haben, können Sie Sie wie eine normale Funktion nennen:</span><span class="sxs-lookup"><span data-stu-id="ba218-319">Once you have defined `Map<'Input, 'Output>` in this way, you can call it as though it was an ordinary function:</span></span>

```qsharp
// Represent Z₀ Z₁ X₂ Y₃ as a list of ints.
let ints = [3, 3, 1, 2];
// Here, assume IntToPauli : Int -> Pauli
// looks up PauliI by 0, PauliX by 1, so forth.
let paulis = Map(IntToPauli, ints);
```

> [!TIP]
> <span data-ttu-id="ba218-320">Das Schreiben von generischen Funktionen und Vorgängen ist eine Stelle, an der "Tupel-in-tupelout" eine sehr nützliche Methode ist, um Q# Funktionen und Vorgänge zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="ba218-320">Writing generic functions and operations is one place where "tuple-in tuple-out" is a very useful way to think about Q# functions and operations.</span></span>
> <span data-ttu-id="ba218-321">Da jede Funktion genau eine Eingabe annimmt und genau eine Ausgabe zurückgibt, gleicht eine Eingabe vom Typ `'T -> 'U` *jede beliebige* Q# Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="ba218-321">Since every function takes exactly one input and returns exactly one output, an input of type `'T -> 'U` matches *any* Q# function whatsoever.</span></span>
> <span data-ttu-id="ba218-322">Entsprechend können Sie jeden Vorgang an eine Eingabe vom Typ übergeben `'T => 'U` .</span><span class="sxs-lookup"><span data-stu-id="ba218-322">Similarly, you can pass any operation to an input of type `'T => 'U`.</span></span>

<span data-ttu-id="ba218-323">Sehen Sie sich als zweites Beispiel die Herausforderung an, eine Funktion zu schreiben, die die Komposition zweier anderer Funktionen zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="ba218-323">As a second example, consider the challenge of writing a function that returns the composition of two other functions:</span></span>

```qsharp
function ComposeImpl(outerFn : (B -> C), innerFn : (A -> B), input : A) : C {
    return outerFn(innerFn(input));
}

function Compose(outerFn : (B -> C), innerFn : (A -> B)) : (A -> C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="ba218-324">Hier müssen Sie genau angeben, was `A` , `B` und `C` sind, und so das Dienstprogramm der neuen Funktion stark einschränken `Compose` .</span><span class="sxs-lookup"><span data-stu-id="ba218-324">Here, you must specify exactly what `A`, `B`, and `C` are, hence severely limiting the utility of our new `Compose` function.</span></span>
<span data-ttu-id="ba218-325">Schließlich ist `Compose` nur von `A` , `B` und `C` *über* `innerFn` und abhängig `outerFn` .</span><span class="sxs-lookup"><span data-stu-id="ba218-325">After all, `Compose` only depends on `A`, `B`, and `C` *via* `innerFn` and `outerFn`.</span></span>
<span data-ttu-id="ba218-326">Als Alternative können Sie auch Typparameter hinzufügen, `Compose` die angeben, dass Sie für *alle* `A` , und funktioniert `B` , solange `C` diese Parameter den von und erwarteten entsprechen `innerFn` `outerFn` :</span><span class="sxs-lookup"><span data-stu-id="ba218-326">As an alternative, then, you can add type parameters to `Compose` that indicate that it works for *any* `A`, `B`, and `C`, so long as these parameters match those expected by `innerFn` and `outerFn`:</span></span>

```qsharp
function ComposeImpl<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B), input : 'A) : 'C {
    return outerFn(innerFn(input));
}

function Compose<'A, 'B, 'C>(outerFn : ('B -> 'C), innerFn : ('A -> 'B)) : ('A -> 'C) {
    return ComposeImpl(outerFn, innerFn, _);
}
```

<span data-ttu-id="ba218-327">Die Q# Standardbibliotheken stellen einen Bereich von Typen parametrisierten Vorgängen und Funktionen bereit, um die Express-Ablauf Steuerung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="ba218-327">The Q# standard libraries provide a range of such type-parameterized operations and functions to make higher-order control flow easier to express.</span></span>
<span data-ttu-id="ba218-328">Diese werden im [ Q# Handbuch zur Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro)erläutert.</span><span class="sxs-lookup"><span data-stu-id="ba218-328">These are discussed further in the [Q# standard library guide](xref:microsoft.quantum.libraries.standard.intro).</span></span>


## <a name="callables-as-first-class-values"></a><span data-ttu-id="ba218-329">Callables als First-Class-Werte</span><span class="sxs-lookup"><span data-stu-id="ba218-329">Callables as First-Class Values</span></span>

<span data-ttu-id="ba218-330">Ein wichtiges Verfahren, um die Ablauf Steuerung und die klassische Logik mithilfe von Funktionen anstelle von Vorgängen zu überdenken, besteht darin, diese Vorgänge und Funktionen in als Q# *erste Klasse*zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ba218-330">One critical technique for reasoning about control flow and classical logic using functions rather than operations is to utilize that operations and functions in Q# are *first-class*.</span></span>
<span data-ttu-id="ba218-331">Das heißt, Sie sind jeweils die einzelnen Werte in der Sprache.</span><span class="sxs-lookup"><span data-stu-id="ba218-331">That is, they are each values in the language in their own right.</span></span>
<span data-ttu-id="ba218-332">Beispielsweise ist der folgende vollständig gültige Q# Code, wenn ein wenig indirekt:</span><span class="sxs-lookup"><span data-stu-id="ba218-332">For instance, the following is perfectly valid Q# code, if a little indirect:</span></span>

```qsharp
operation FirstClassExample(target : Qubit) : Unit {
    let ourH = H;
    ourH(target);
}
```

<span data-ttu-id="ba218-333">Der Wert der Variablen `ourH` im vorherigen Code Ausschnitt ist dann der Vorgang <xref:microsoft.quantum.intrinsic.h> , sodass Sie diesen Wert wie jeder andere Vorgang abrufen können.</span><span class="sxs-lookup"><span data-stu-id="ba218-333">The value of the variable `ourH` in the previous snippet is then the operation <xref:microsoft.quantum.intrinsic.h>, such that you can call that value like any other operation.</span></span>
<span data-ttu-id="ba218-334">Mit dieser Fähigkeit können Sie Vorgänge schreiben, die Vorgänge als Teil Ihrer Eingabe ausführen und so die Konzepte der Ablauf Steuerung in höherer Ordnung bilden.</span><span class="sxs-lookup"><span data-stu-id="ba218-334">With this ability, you can write operations that take operations as a part of their input, forming higher-order control flow concepts.</span></span>
<span data-ttu-id="ba218-335">Beispielsweise können Sie sich vorstellen, einen Vorgang zu "quadrieren", indem Sie ihn zweimal auf das gleiche Ziel-Qubit anwenden.</span><span class="sxs-lookup"><span data-stu-id="ba218-335">For instance, you could imagine wanting to "square" an operation by applying it twice to the same target qubit.</span></span>

```qsharp
operation ApplyTwice(op : (Qubit => Unit), target : Qubit) : Unit {
    op(target);
    op(target);
}
```

### <a name="returning-operations-from-a-function"></a><span data-ttu-id="ba218-336">Zurückgeben von Vorgängen aus einer Funktion</span><span class="sxs-lookup"><span data-stu-id="ba218-336">Returning operations from a function</span></span>

<span data-ttu-id="ba218-337">Es ist wichtig zu betonen, dass Sie auch Vorgänge als Teil der Ausgaben zurückgeben können, sodass Sie einige Arten von klassischer bedingter Logik als klassische Funktion isolieren können, die eine Beschreibung eines Quantum-Programms in Form eines Vorgangs zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ba218-337">It's important to emphasize that you can also return operations as a part of outputs, such that you can isolate some kinds of classical conditional logic as a classical function, which returns a description of a quantum program in the form of an operation.</span></span>
<span data-ttu-id="ba218-338">Als einfaches Beispiel sehen Sie sich das Beispiel für die teleportung an, in dem die Partei, die eine zwei-Bit-klassische Nachricht empfängt, die Nachricht verwenden muss, um Ihr Qubit in den richtigen teleportierten Zustand zu decodieren.</span><span class="sxs-lookup"><span data-stu-id="ba218-338">As a simple example, consider the teleportation example, in which the party receiving a two-bit classical message needs to use the message to decode their qubit into the proper teleported state.</span></span>
<span data-ttu-id="ba218-339">Sie könnten dies im Hinblick auf eine Funktion schreiben, die diese beiden klassischen Bits annimmt und den richtigen Decodierungs Vorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ba218-339">You could write this in terms of a function that takes those two classical bits and returns the proper decoding operation.</span></span>

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

<span data-ttu-id="ba218-340">Diese neue Funktion ist tatsächlich eine Funktion, wenn Sie Sie mit den gleichen Werten von und aufzurufen `hereBit` `thereBit` , und Sie erhalten immer denselben Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ba218-340">This new function is indeed a function, in that if you call it with the same values of `hereBit` and `thereBit`, you always get back the same operation.</span></span>
<span data-ttu-id="ba218-341">Daher kann der Decoder sicher innerhalb von Vorgängen ausgeführt werden, ohne dass es darum geht, zu bedenken, wie die Decodierungs Logik mit den Definitionen der verschiedenen Vorgangs Spezialisierungs Maßnahmen interagiert.</span><span class="sxs-lookup"><span data-stu-id="ba218-341">Thus, the decoder can safely run inside operations without having to reason about how the decoding logic interacts with the definitions of the different operation specializations.</span></span>
<span data-ttu-id="ba218-342">Das heißt, die klassische Logik innerhalb einer Funktion ist isoliert, sodass dem Compiler gewährleistet wird, dass der Funktions aufrufbedarf mit Straffreiheit neu angeordnet werden kann, solange die Eingabe beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="ba218-342">That is, the classical logic inside a function is isolated, guaranteeing to the compiler that the function call can be reordered with impunity so long as the input is preserved.</span></span>


## <a name="partial-application"></a><span data-ttu-id="ba218-343">Partielle Anwendung</span><span class="sxs-lookup"><span data-stu-id="ba218-343">Partial Application</span></span>

<span data-ttu-id="ba218-344">Sie können mit Funktionen, die Vorgänge mithilfe einer *partiellen Anwendung*zurückgeben, wesentlich mehr tun, bei der Sie einen oder mehrere Teile der Eingabe für eine Funktion oder einen Vorgang bereitstellen, ohne Sie tatsächlich aufrufen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="ba218-344">You can do significantly more with functions that return operations by using *partial application*, in which you provide one or more parts of the input to a function or operation without actually calling it.</span></span> <span data-ttu-id="ba218-345">Im vorherigen `ApplyTwice` Beispiel können Sie angeben, dass Sie nicht sofort angeben möchten, auf welchem Qubit der Eingabevorgang angewendet werden soll:</span><span class="sxs-lookup"><span data-stu-id="ba218-345">In the earlier `ApplyTwice` example, you can indicate that you don't want to specify, right away, to which qubit the input operation should apply:</span></span>

```qsharp
operation PartialApplicationExample(op : (Qubit => Unit), target : Qubit) : Unit {
    let twiceOp = ApplyTwice(op, _);
    twiceOp(target);
}
```

<span data-ttu-id="ba218-346">In diesem Fall enthält die lokale Variable `twiceOp` den teilweise angewendeten Vorgang `ApplyTwice(op, _)` , wobei `_` Teile der Eingabe angibt, die noch nicht angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="ba218-346">In this case, the local variable `twiceOp` holds the partially applied operation `ApplyTwice(op, _)`, where `_` indicates parts of the input that have not yet been specified.</span></span>
<span data-ttu-id="ba218-347">Wenn Sie `twiceOp` in der nächsten Zeile aufzurufen, übergeben Sie als Eingabe an den teilweise angewendeten Vorgang alle verbleibenden Teile der Eingabe für den ursprünglichen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ba218-347">When you call `twiceOp` in the next line, you pass as input to the partially applied operation all of the remaining parts of the input to the original operation.</span></span>
<span data-ttu-id="ba218-348">Folglich ist der vorherige Code Ausschnitt tatsächlich identisch mit dem `ApplyTwice(op, target)` direkten Aufruf von, da Sie eine neue lokale Variable eingeführt haben, damit Sie den Aufruf bei der Bereitstellung einiger Teile der Eingabe verzögern können.</span><span class="sxs-lookup"><span data-stu-id="ba218-348">Thus, the previous snippet is effectively identical to having called `ApplyTwice(op, target)` directly, save for that you have introduced a new local variable so you can delay the call while providing some parts of the input.</span></span>

<span data-ttu-id="ba218-349">Da ein Vorgang, der teilweise angewendet wurde, erst aufgerufen wird, wenn die gesamte Eingabe bereitgestellt wurde, können Sie Vorgänge auf sichere Weise sogar aus Funktionen anwenden.</span><span class="sxs-lookup"><span data-stu-id="ba218-349">Since an operation that has been partially applied is not actually called until its entire input has been provided, you can safely partially apply operations even from within functions.</span></span>

```qsharp
function SquareOperation(op : (Qubit => Unit)) : (Qubit => Unit) {
    return ApplyTwice(op, _);
}
```

<span data-ttu-id="ba218-350">Im Prinzip könnte die klassische Logik in `SquareOperation` viel stärker einbezogen werden, aber Sie ist weiterhin vom Rest eines Vorgangs isoliert, indem die Garantien, die der Compiler über Funktionen bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="ba218-350">In principle, the classical logic within `SquareOperation` could have been much more involved, but it is still isolated from the rest of an operation by the guarantees that the compiler can offer about functions.</span></span> <span data-ttu-id="ba218-351">Die Q# Standardbibliothek verwendet diesen Ansatz, um die klassische Ablauf Steuerung so auszudrücken, dass Quantum-Programme Sie problemlos verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ba218-351">The Q# standard library uses this approach throughout for expressing classical control flow in a way that quantum programs can readily use.</span></span>


## <a name="recursion"></a><span data-ttu-id="ba218-352">Rekursion</span><span class="sxs-lookup"><span data-stu-id="ba218-352">Recursion</span></span>

<span data-ttu-id="ba218-353">Q#callables dürfen direkt oder indirekt rekursiv sein.</span><span class="sxs-lookup"><span data-stu-id="ba218-353">Q# callables are allowed to be directly or indirectly recursive.</span></span>
<span data-ttu-id="ba218-354">Das heißt, ein Vorgang oder eine Funktion kann sich selbst aufrufen, oder Sie kann eine andere Aufruf Bare aufrufen, die den Aufruf baren Vorgang direkt oder indirekt aufruft.</span><span class="sxs-lookup"><span data-stu-id="ba218-354">That is, an operation or function can call itself, or it can call another callable that directly or indirectly calls the callable operation.</span></span>

<span data-ttu-id="ba218-355">Es gibt jedoch zwei wichtige Kommentare zur Verwendung der Rekursion:</span><span class="sxs-lookup"><span data-stu-id="ba218-355">There are two important comments about the use of recursion, however:</span></span>

- <span data-ttu-id="ba218-356">Die Verwendung von Rekursion bei Vorgängen beeinträchtigt wahrscheinlich bestimmte Optimierungen.</span><span class="sxs-lookup"><span data-stu-id="ba218-356">The use of recursion in operations is likely to interfere with certain optimizations.</span></span>
  <span data-ttu-id="ba218-357">Diese Störungen können erhebliche Auswirkungen auf die Ausführungszeit des Algorithmus haben.</span><span class="sxs-lookup"><span data-stu-id="ba218-357">This interference can have a substantial impact on the execution time of the algorithm.</span></span>
- <span data-ttu-id="ba218-358">Bei der Ausführung auf einem eigentlichen Quantum-Gerät ist der Stapel Speicherplatz möglicherweise eingeschränkt, sodass die Tiefe Rekursion zu einem Laufzeitfehler führen kann.</span><span class="sxs-lookup"><span data-stu-id="ba218-358">When running on an actual quantum device, stack space might be limited, and so deep recursion can lead to a runtime error.</span></span>
  <span data-ttu-id="ba218-359">Der Q# Compiler und die Laufzeit identifizieren und optimieren die Endrekursion insbesondere nicht.</span><span class="sxs-lookup"><span data-stu-id="ba218-359">In particular, the Q# compiler and runtime do not identify and optimize tail recursion.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ba218-360">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ba218-360">Next steps</span></span>

<span data-ttu-id="ba218-361">Erfahren Sie mehr über [Variablen](xref:microsoft.quantum.guide.variables) in Q# .</span><span class="sxs-lookup"><span data-stu-id="ba218-361">Learn about [Variables](xref:microsoft.quantum.guide.variables) in Q#.</span></span>