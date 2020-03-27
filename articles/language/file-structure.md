---
title: 'F #-Dateistruktur'
description: 'Erfahren Sie, wie Sie Namespaces und Vorgänge, Funktionen und benutzerdefinierte Typdeklarationen in Q #-Programmen und-Bibliotheken strukturieren.'
author: QuantumWriter
uid: microsoft.quantum.language.file-structure
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 96de062bc6ce4edf94520bec449e8d95259c0f5c
ms.sourcegitcommit: a0e50c5f07841b99204c068cf5b5ec8ed087ffea
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2020
ms.locfileid: "80320760"
---
# <a name="file-structure"></a><span data-ttu-id="407e1-103">Dateistruktur</span><span class="sxs-lookup"><span data-stu-id="407e1-103">File Structure</span></span>

<span data-ttu-id="407e1-104">Eine Q #-Datei besteht aus einer Sequenz von Namespace Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="407e1-104">A Q# file consists of a sequence of namespace declarations.</span></span>
<span data-ttu-id="407e1-105">Jede Namespace Deklaration enthält Deklarationen für benutzerdefinierte Typen, Vorgänge und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="407e1-105">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="407e1-106">Eine Namespace Deklaration kann beliebig viele Typen von Deklarationen und in beliebiger Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="407e1-106">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="407e1-107">Der einzige Text, der außerhalb einer Namespace Deklaration angezeigt werden kann, sind Kommentare.</span><span class="sxs-lookup"><span data-stu-id="407e1-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="407e1-108">Insbesondere Dokumentations Kommentare für einen Namespace vor der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="407e1-108">In particular, documentation comments for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="407e1-109">Namespacedeklarationen</span><span class="sxs-lookup"><span data-stu-id="407e1-109">Namespace Declarations</span></span>

<span data-ttu-id="407e1-110">Eine Q #-Datei hat normalerweise genau eine Namespace Deklaration, kann jedoch keine (und leer sein oder nur Kommentare enthalten) oder mehrere Namespaces enthalten.</span><span class="sxs-lookup"><span data-stu-id="407e1-110">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="407e1-111">Namespace Deklarationen dürfen nicht eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-111">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="407e1-112">Derselbe Namespace kann in mehreren Q #-Dateien deklariert werden, die zusammen kompiliert werden, solange keine Typen-, Vorgangs-oder Funktions Deklarationen mit demselben Namen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-112">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="407e1-113">Es ist insbesondere ungültig, denselben Typ im gleichen Namespace in mehreren Dateien zu definieren, auch wenn die Deklarationen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-113">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="407e1-114">Eine Namespace Deklaration besteht aus dem Schlüsselwort `namespace`, gefolgt vom Namen des Namespace, einer geöffneten geschweifter Klammer `{`, den im Namespace enthaltenen Deklarationen und einer schließenden geschweifter Klammer `}`.</span><span class="sxs-lookup"><span data-stu-id="407e1-114">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="407e1-115">Namespace Namen folgen dem .net-Muster einer Sequenz von mindestens einem juristischen Symbol, das durch Zeiträume `.`getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="407e1-115">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="407e1-116">Beispielsweise sind `MyQuantumStuff` und `Microsoft.Quantum.Canon` gültige Namespace Namen.</span><span class="sxs-lookup"><span data-stu-id="407e1-116">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Canon` are valid namespace names.</span></span>
<span data-ttu-id="407e1-117">Gemäß der Konvention werden die Symbole in einem Namespace Namen groß geschrieben, dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="407e1-117">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="407e1-118">Deklarationen werden in einer Namespace Deklaration möglicherweise in beliebiger Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="407e1-118">Declarations may appear in any order in a namespace declaration.</span></span>
<span data-ttu-id="407e1-119">Verweise auf Typen oder Aufruf Bare Dateien, die in einer Datei weiter unten deklariert sind, werden ordnungsgemäß aufgelöst. Es ist nicht erforderlich, dass der Typ, der Vorgang oder die Funktionsdeklaration einem Verweis darauf vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="407e1-119">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="407e1-120">Open-Direktiven</span><span class="sxs-lookup"><span data-stu-id="407e1-120">Open Directives</span></span>

<span data-ttu-id="407e1-121">Innerhalb eines Namespace Blocks kann die `open`-Direktive verwendet werden, um alle Typen und callables zu importieren, die in einem bestimmten Namespace definiert sind, und auf diese über ihren nicht qualifizierten Namen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="407e1-121">Within a namespace block, the `open` directive may be used to import all types and callables defined in a certain namespace and refer to them by their unqualified name.</span></span> 

<span data-ttu-id="407e1-122">Eine solche `open` Direktive besteht aus dem Schlüsselwort `open`, gefolgt vom zu öffnenden Namespace und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="407e1-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

<span data-ttu-id="407e1-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="407e1-123">For instance,</span></span>

```qsharp
open Microsoft.Quantum.Canon;
```

<span data-ttu-id="407e1-124">Optional kann ein Kurzname für den geöffneten Namespace definiert werden, sodass alle Elemente aus diesem Namespace durch den definierten Kurznamen qualifiziert werden können (und müssen).</span><span class="sxs-lookup"><span data-stu-id="407e1-124">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="407e1-125">Ein solcher Kurzname wird definiert, indem das Schlüsselwort `as` gefolgt vom gewünschten Kurznamen vor dem Semikolon in einer `open` Direktive hinzugefügt wird:</span><span class="sxs-lookup"><span data-stu-id="407e1-125">Such a short name is defined by adding the keyword `as` followed by the desired short name before the semicolon in an `open` directive:</span></span>

```qsharp
open Microsoft.Quantum.Math as Math;
```

<span data-ttu-id="407e1-126">Alle `open` Direktiven müssen vor allen `function`-, `operation`-oder `newtype` Deklarationen im-Namespace Block angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-126">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>
<span data-ttu-id="407e1-127">Die `open`-Direktive gilt für den gesamten Namespace Block in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="407e1-127">The `open` directive applies to the entire namespace block within a file.</span></span>

## <a name="user-defined-type-declarations"></a><span data-ttu-id="407e1-128">Deklarationen von benutzerdefinierten Typen</span><span class="sxs-lookup"><span data-stu-id="407e1-128">User-Defined Type Declarations</span></span>

<span data-ttu-id="407e1-129">Q # bietet Benutzern die Möglichkeit, neue benutzerdefinierte Typen zu deklarieren, wie im Abschnitt " [Q # Type Model](xref:microsoft.quantum.language.type-model) " beschrieben.</span><span class="sxs-lookup"><span data-stu-id="407e1-129">Q# provides a way for users to declare new user-defined types, as described in the [Q# type model](xref:microsoft.quantum.language.type-model) section.</span></span>
<span data-ttu-id="407e1-130">Benutzerdefinierte Typen sind unterschiedlich, auch wenn die Basis Typen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-130">User-defined types are distinct even if the base types are identical.</span></span>
<span data-ttu-id="407e1-131">Insbesondere, wenn die zugrunde liegenden Typen identisch sind, gibt es keine automatische Konvertierung zwischen Werten von zwei benutzerdefinierten Typen.</span><span class="sxs-lookup"><span data-stu-id="407e1-131">In particular, there is no automatic conversion between values of two user-defined types even if the underlying types are identical.</span></span>

<span data-ttu-id="407e1-132">Eine benutzerdefinierte Typdeklaration besteht aus dem Schlüsselwort `newtype`, gefolgt vom Namen des benutzerdefinierten Typs, einer `=`, einer gültigen Typspezifikation und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="407e1-132">A user-defined type declaration consists of the keyword `newtype`, followed by the name of the user-defined type, an `=`, a valid type specification, and a terminating semicolon.</span></span>

<span data-ttu-id="407e1-133">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="407e1-133">For example:</span></span>

```qsharp
newtype PairOfInts = (Int, Int);
```

<span data-ttu-id="407e1-134">Jede f #-Quelldatei kann eine beliebige Anzahl benutzerdefinierter Typen deklarieren.</span><span class="sxs-lookup"><span data-stu-id="407e1-134">Each Q# source file may declare any number of user-defined types.</span></span>
<span data-ttu-id="407e1-135">Typnamen müssen innerhalb eines Namespace eindeutig sein und können nicht mit Vorgangs-und Funktionsnamen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="407e1-135">Type names must be unique within a namespace and may not conflict with operation and function names.</span></span>

<span data-ttu-id="407e1-136">Es ist nicht möglich, zirkuläre Abhängigkeiten zwischen benutzerdefinierten Typen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="407e1-136">It is not possible to define circular dependencies between user defined types.</span></span> <span data-ttu-id="407e1-137">Rekursive Typen sind in Q # daher nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="407e1-137">Recursive types are thus not possible within Q#.</span></span>

## <a name="operation-declarations"></a><span data-ttu-id="407e1-138">Vorgangs Deklarationen</span><span class="sxs-lookup"><span data-stu-id="407e1-138">Operation Declarations</span></span>

<span data-ttu-id="407e1-139">Vorgänge sind das Kernstück von Q #, ungefähr analog zu Funktionen in anderen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="407e1-139">Operations are the core of Q#, roughly analogous to functions in other languages.</span></span>
<span data-ttu-id="407e1-140">Jede f #-Quelldatei kann eine beliebige Anzahl von Vorgängen definieren.</span><span class="sxs-lookup"><span data-stu-id="407e1-140">Each Q# source file may define any number of operations.</span></span>

<span data-ttu-id="407e1-141">Vorgangs Namen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit Typ-und Funktionsnamen verursachen.</span><span class="sxs-lookup"><span data-stu-id="407e1-141">Operation names must be unique within a namespace and may not conflict with type and function names.</span></span>

<span data-ttu-id="407e1-142">Eine Vorgangs Deklaration besteht aus dem Schlüsselwort `operation`, gefolgt vom Symbol, das den Namen des Vorgangs, ein typisiertes bezeichnertupel, das die Argumente für den Vorgang definiert, einen Doppelpunkt `:`, eine Typanmerkung, die den Ergebnistyp des Vorgangs beschreibt, optional eine Anmerkung mit den Vorgangs Merkmalen, eine öffnende geschweifte Klammer `{`, den Text der Vorgangs Deklaration und eine abschließende schließende geschweifte Klammer `}`.</span><span class="sxs-lookup"><span data-stu-id="407e1-142">An operation declarations consists of the keyword `operation`, followed by the symbol that is the operation’s name, a typed identifier tuple that defines the arguments to the operation, a colon `:`, a type annotation that describes the operation’s result type, optionally an annotation with the operation characteristics, an open brace `{`, the body of the operation declaration, and a final closing brace `}`.</span></span>

<span data-ttu-id="407e1-143">Der Text der Vorgangs Deklaration besteht entweder aus der Standard Implementierung oder einer Liste von spezialisierer.</span><span class="sxs-lookup"><span data-stu-id="407e1-143">The body of the operation declaration either consists of the default implementation or of a list of specializations.</span></span>
<span data-ttu-id="407e1-144">Die Standard Implementierung kann direkt innerhalb der-Deklaration angegeben werden, wenn nur die Implementierung der Standardtext Spezialisierung explizit angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="407e1-144">The default implementation can be specified directly within the declaration if only the implementation of the default body specialization needs to specified explicitly.</span></span>
<span data-ttu-id="407e1-145">In diesem Fall ist eine Anmerkung mit den Vorgangs Merkmalen in der Deklaration hilfreich, um sicherzustellen, dass der Compiler automatisch andere Spezialisierungs Vorgänge auf der Grundlage der Standard Implementierung generiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-145">In this case, an annotation with the operation characteristics in the declaration is useful to ensure that the compiler auto-generates other specializations based on the default implementation.</span></span> 

<span data-ttu-id="407e1-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="407e1-146">For example</span></span> 

```qsharp
operation PrepareEntangledPair(here : Qubit, there : Qubit) : Unit 
is Adj + Ctl { // implies the existence of an adjoint, a controlled, and a controlled adjoint specialization
    H(here);
    CNOT(here, there);
}
```

<span data-ttu-id="407e1-147">Vorgangs Merkmale definieren, welche Arten von functoren auf den deklarierten Vorgang angewendet werden können und welche Auswirkungen Sie haben.</span><span class="sxs-lookup"><span data-stu-id="407e1-147">Operation characteristics define what kinds of functors can be applied to the declared operation, and what effect they have.</span></span> <span data-ttu-id="407e1-148">Wenn ein Vorgang eine einheitliche Transformation implementiert, ist es möglich, zu definieren, wie der Vorgang beim *angleichen oder* *Steuern*erfolgt.</span><span class="sxs-lookup"><span data-stu-id="407e1-148">If an operation implements a unitary transformation, then it is possible to define how the operation acts when *adjointed* or *controlled*.</span></span>
<span data-ttu-id="407e1-149">Das vorhanden sein dieser Spezialisierungsmöglichkeiten kann als Teil der Vorgangs Signatur deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-149">The existence of these specializations can be declared as part of the operation signature.</span></span> <span data-ttu-id="407e1-150">Die entsprechende Implementierung für jede solche implizit deklarierte Spezialisierung wird dann vom Compiler generiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-150">The corresponding implementation for each such implicitly declared specialization is then generated by the compiler.</span></span> <span data-ttu-id="407e1-151">Im obigen Beispiel werden eine Adjoint-, eine gesteuerte und eine kontrollierte Adjoint-Spezialisierung vom Compiler generiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-151">In the example above, an adjoint, a controlled, and a controlled adjoint specialization are generated by the compiler.</span></span> 

<span data-ttu-id="407e1-152">Wenn die Implementierung nicht vom Compiler generiert werden kann, kann Sie explizit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-152">In the case where the implementation cannot be generated by the compiler, it can be explicitly specified.</span></span> <span data-ttu-id="407e1-153">Solche expliziten Spezialisierungs Deklarationen können entweder aus einer geeigneten Generierungs Direktive bestehen, die verdeutlichen, wie eine bestimmte Spezialisierung erstellt werden soll, oder einer benutzerdefinierten Implementierung.</span><span class="sxs-lookup"><span data-stu-id="407e1-153">Such explicit specialization declarations can either consist of a suitable generation directive that clarify how a certain specialization is to be built, or a user defined implementation.</span></span> <span data-ttu-id="407e1-154">Der oben genannte Code in `PrepareEntangledPair` z. b. Äquivalent zum folgenden Code, der explizite Spezialisierungs Deklarationen enthält:</span><span class="sxs-lookup"><span data-stu-id="407e1-154">The code in `PrepareEntangledPair` above for example is equivalent to the code below containing explicit specialization declarations:</span></span> 

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
<span data-ttu-id="407e1-155">Das Schlüsselwort `auto` gibt an, dass der Compiler bestimmen soll, wie die Spezialisierungs Implementierung generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="407e1-155">The keyword `auto` indicates that the compiler should determine how to generate the specialization implementation.</span></span>
<span data-ttu-id="407e1-156">Wenn der Compiler die Implementierung für eine bestimmte Spezialisierung ohne weitere Anweisungen (z. b. eine präzisere Generierungs Direktive) nicht generieren kann, oder wenn eine effizientere Implementierung angegeben werden kann, kann die Implementierung auch manuell definiert werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-156">If the compiler cannot generate the implementation for a certain specialization without further instructions - like a more precise generation directive -, or if a more efficient implementation can be given, then the implementation may also be manually defined.</span></span>

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

<span data-ttu-id="407e1-157">Im obigen Beispiel gibt `adjoint invert;` an, dass die Adjoint-Spezialisierung generiert werden soll, indem Sie die Text Implementierung umkehren, und `controlled adjoint invert;` gibt an, dass die kontrollierte Adjoint-Spezialisierung generiert werden soll, indem Sie die angegebene Implementierung der kontrollierten Spezialisierung umkehren.</span><span class="sxs-lookup"><span data-stu-id="407e1-157">In the example above, `adjoint invert;` indicates that the adjoint specialization is to be generated by inverting the body implementation, and `controlled adjoint invert;` indicates that the controlled adjoint specialization is to be generated by inverting the given implementation of the controlled specialization.</span></span>

<span data-ttu-id="407e1-158">Damit ein Vorgang die Anwendung des `Adjoint`-und/oder `Controlled`-funktors unterstützt, muss der Rückgabetyp notwendigerweise `Unit`werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-158">For an operation to support application of the `Adjoint` and/or `Controlled` functor, its return type necessarily needs to be `Unit`.</span></span> 


### <a name="explicit-specialization-declarations"></a><span data-ttu-id="407e1-159">Explizite Spezialisierungs Deklarationen</span><span class="sxs-lookup"><span data-stu-id="407e1-159">Explicit Specialization Declarations</span></span>

<span data-ttu-id="407e1-160">F #-Vorgänge können die folgenden expliziten Spezialisierungs Deklarationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="407e1-160">Q# operations may contain the following explicit specialization declarations:</span></span>

- <span data-ttu-id="407e1-161">Die `body` Spezialisierung gibt die Implementierung des Vorgangs ohne angewendete Funktoren an.</span><span class="sxs-lookup"><span data-stu-id="407e1-161">The `body` specialization specifies the implementation of the operation with no functors applied.</span></span>
- <span data-ttu-id="407e1-162">Die `adjoint` Spezialisierung gibt die Implementierung des Vorgangs mit angewendetem `Adjoint`-Funktor an.</span><span class="sxs-lookup"><span data-stu-id="407e1-162">The `adjoint` specialization specifies the implementation of the operation with the `Adjoint` functor applied.</span></span>
- <span data-ttu-id="407e1-163">Die `controlled` Spezialisierung gibt die Implementierung des Vorgangs mit angewendetem `Controlled`-Funktor an.</span><span class="sxs-lookup"><span data-stu-id="407e1-163">The `controlled` specialization specifies the implementation of the operation with the `Controlled` functor applied.</span></span>
- <span data-ttu-id="407e1-164">Die `controlled adjoint` Spezialisierung gibt die Implementierung des Vorgangs an, bei der die `Adjoint`-und `Controlled`-Funktoren angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="407e1-164">The `controlled adjoint` specialization specifies the implementation of the operation with both the `Adjoint` and `Controlled` functors applied.</span></span>
  <span data-ttu-id="407e1-165">Diese Spezialisierung kann auch `adjoint controlled`benannt werden, da die beiden Funktoren in den Weg gehen.</span><span class="sxs-lookup"><span data-stu-id="407e1-165">This specialization can also be named `adjoint controlled`, since the two functors commute.</span></span>


<span data-ttu-id="407e1-166">Eine Vorgangs Spezialisierung besteht aus dem Spezialisierungs Kennzeichen (z. b. `body`oder `adjoint`usw.), gefolgt von einem der folgenden:</span><span class="sxs-lookup"><span data-stu-id="407e1-166">An operation specialization consists of the specialization tag (like e.g. `body`, or `adjoint`, etc.) followed by one of:</span></span>

- <span data-ttu-id="407e1-167">Eine explizite Deklaration, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="407e1-167">An explicit declaration as described below.</span></span>
- <span data-ttu-id="407e1-168">Eine-Direktive, die dem Compiler mitteilt, wie die Spezialisierung generiert werden soll, einer der folgenden:</span><span class="sxs-lookup"><span data-stu-id="407e1-168">A directive that tells the compiler how to generate the specialization, one of:</span></span>
  - <span data-ttu-id="407e1-169">`intrinsic`, das angibt, dass die Spezialisierung vom Zielcomputer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="407e1-169">`intrinsic`, which indicates that the specialization is provided by the target machine.</span></span>
  - <span data-ttu-id="407e1-170">`distribute`, die für die `controlled`-und `controlled adjoint`-Spezialisierung verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="407e1-170">`distribute`, which may be used with the `controlled` and `controlled adjoint` specializations.</span></span>
    <span data-ttu-id="407e1-171">Bei Verwendung mit `controlled`wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge im `body`anwendet.</span><span class="sxs-lookup"><span data-stu-id="407e1-171">When used with `controlled`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `body`.</span></span>
    <span data-ttu-id="407e1-172">Bei Verwendung mit `controlled adjoint`wird angegeben, dass der Compiler die Spezialisierung berechnen soll, indem er `Controlled` auf alle Vorgänge in der `adjoint` Spezialisierung anwendet.</span><span class="sxs-lookup"><span data-stu-id="407e1-172">When used with `controlled adjoint`, it indicates that the compiler should compute the specialization by applying `Controlled` to all of the operations in the `adjoint` specialization.</span></span>
  - <span data-ttu-id="407e1-173">`invert`, das angibt, dass der Compiler die `adjoint` Spezialisierung berechnen soll, indem er die `body`umschließt, d. h. die Reihenfolge der Vorgänge wird umgekehrt und das Adjoint-Attribut auf jeden angewendet.</span><span class="sxs-lookup"><span data-stu-id="407e1-173">`invert`, which indicates that the compiler should compute the `adjoint` specialization by inverting the `body`, i.e. reversing the order of operations and applying the adjoint to each one.</span></span>
    <span data-ttu-id="407e1-174">Bei Verwendung mit `adjoint controlled`gibt dies an, dass der Compiler die Spezialisierung berechnen soll, indem er die `controlled` Spezialisierung umkehrt.</span><span class="sxs-lookup"><span data-stu-id="407e1-174">When used with `adjoint controlled`, this indicates that the compiler should compute the specialization by inverting the `controlled` specialization.</span></span>
  - <span data-ttu-id="407e1-175">`self`, um anzugeben, dass die Adjoint-Spezialisierung mit der `body` Spezialisierung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="407e1-175">`self`, to indicate that the adjoint specialization is the the same as the `body` specialization.</span></span>
    <span data-ttu-id="407e1-176">Dies ist für die `adjoint`-und `adjoint controlled` Spezialisierung zulässig.</span><span class="sxs-lookup"><span data-stu-id="407e1-176">This is legal for the `adjoint` and `adjoint controlled` specializations.</span></span>
    <span data-ttu-id="407e1-177">Bei `adjoint controlled`impliziert `self`, dass die `adjoint controlled` Spezialisierung mit der `controlled` Spezialisierung identisch ist.</span><span class="sxs-lookup"><span data-stu-id="407e1-177">For `adjoint controlled`, `self` implies that the `adjoint controlled` specialization is the same as the `controlled` specialization.</span></span>
  - <span data-ttu-id="407e1-178">`auto`, um anzugeben, dass der Compiler eine geeignete Direktive auswählen soll, die angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="407e1-178">`auto`, to indicate that the compiler should select an appropriate directive to apply.</span></span>
    <span data-ttu-id="407e1-179">`auto` darf nicht für die `body` Spezialisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-179">`auto` may not be used for the `body` specialization.</span></span>

<span data-ttu-id="407e1-180">Die Direktiven und `auto` alle erfordern ein Schließ Endes Semikolon `;`.</span><span class="sxs-lookup"><span data-stu-id="407e1-180">The directives and `auto` all require a closing semi-colon `;`.</span></span>
<span data-ttu-id="407e1-181">Die `auto`-Direktive wird in die folgende Generations Anweisung aufgelöst, wenn eine explizite Deklaration des `body` bereitgestellt wird:</span><span class="sxs-lookup"><span data-stu-id="407e1-181">The `auto` directive resolves to the following generation directive if an explicit declaration of the `body` is provided:</span></span>

- <span data-ttu-id="407e1-182">Die `adjoint` Spezialisierung wird gemäß der-Direktive `invert`generiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-182">The `adjoint` specialization is generated according to the directive `invert`.</span></span>
- <span data-ttu-id="407e1-183">Die `controlled` Spezialisierung wird gemäß der-Direktive `distribute`generiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-183">The `controlled` specialization is generated according to the directive `distribute`.</span></span>
- <span data-ttu-id="407e1-184">Die `adjoint controlled` Spezialisierung wird gemäß der-Direktive generiert `invert` wenn eine explizite Deklaration für `controlled` angegeben ist, aber nicht für `adjoint`, und andernfalls `distribute`.</span><span class="sxs-lookup"><span data-stu-id="407e1-184">The `adjoint controlled` specialization is generated according to the directive `invert` if an explicit declaration for `controlled` is given but not one for `adjoint`, and `distribute` otherwise.</span></span>

> [!TIP]   
> <span data-ttu-id="407e1-185">Wenn es sich um einen eigenständigen Vorgang handelt, geben Sie entweder die Adjoint-oder die kontrollierte Adjoint-Spezialisierung mithilfe der Generations Direktive an `self` um dem Compiler zu ermöglichen, diese Informationen zu Optimierungszwecken zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="407e1-185">If an operation is self-adjoint, explicitly specify either the adjoint or the controlled adjoint specialization via the generation directive `self` to allow the compiler to make use of that information for optimization purposes.</span></span>

<span data-ttu-id="407e1-186">Eine Spezialisierungs Deklaration, die eine benutzerdefinierte Implementierung enthält, besteht aus einem argumenttupel, gefolgt von einem Anweisungsblock mit dem Q #-Code, der die Spezialisierung implementiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-186">A specialization declaration containing a user defined implementation consists of an argument tuple followed by a statement block with the Q# code that implements the specialization.</span></span>
<span data-ttu-id="407e1-187">In der Argumentliste wird `...` verwendet, um die für den Vorgang als Ganzes deklarierten Argumente darzustellen.</span><span class="sxs-lookup"><span data-stu-id="407e1-187">In the argument list, `...` is used to represent the arguments declared for the operation as a whole.</span></span>
<span data-ttu-id="407e1-188">Bei `body` und `adjoint`sollte die Argumentliste immer `(...)`sein. bei `controlled` und `adjoint controlled`sollte die Argumentliste ein Symbol sein, das das Array von Steuerelement-Qubits, gefolgt von `...`, in Klammern eingeschlossen ist. beispielsweise `(controls,...)`.</span><span class="sxs-lookup"><span data-stu-id="407e1-188">For `body` and `adjoint`, the argument list should always be `(...)`; for `controlled` and `adjoint controlled`, the argument list should be a symbol that represents the array of control qubits, followed by `...`, enclosed in parentheses; for example, `(controls,...)`.</span></span>

<span data-ttu-id="407e1-189">Wenn eine oder mehrere Spezialisierungen neben dem Standardtext explizit deklariert werden müssen, muss die Implementierung für den Standardtext ebenfalls in eine passende Spezialisierungs Deklaration integriert werden:</span><span class="sxs-lookup"><span data-stu-id="407e1-189">If one or more specializations besides the default body need to be explicitly declared, then the implementation for the default body needs to be wrapped into a suitable specialization declaration as well:</span></span>

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

### <a name="adjoint"></a><span data-ttu-id="407e1-190">Adjoint</span><span class="sxs-lookup"><span data-stu-id="407e1-190">Adjoint</span></span>

<span data-ttu-id="407e1-191">Das Adjoint eines Vorgangs gibt an, wie die komplexe konjugierte, die den Vorgang implementiert, implementiert wird, d. h., wie der Vorgang bei umgekehrter Ausführung funktioniert.</span><span class="sxs-lookup"><span data-stu-id="407e1-191">The adjoint of an operation specifies how the complex conjugate transpose of the operation is implemented, i.e. how the operation acts when "run in reverse".</span></span>
<span data-ttu-id="407e1-192">Es ist zulässig, einen Vorgang ohne Adjoint anzugeben. Beispielsweise haben Messvorgänge keinen Adjoint, da Sie nicht invertierbar sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-192">It is legal to specify an operation with no adjoint; for instance, measurement operations have no adjoint because they are not invertible.</span></span>
<span data-ttu-id="407e1-193">Ein Vorgang unterstützt das `Adjoint`-Funktor, wenn seine Deklaration eine implizite oder explizite Deklaration einer Adjoint-Spezialisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="407e1-193">An operation supports the `Adjoint` functor if its declaration contains an implicit or explicit declaration of an adjoint specialization.</span></span>
<span data-ttu-id="407e1-194">Eine explizit deklarierte, kontrollierte Adjoint-Spezialisierung impliziert, dass eine Adjoint-Spezialisierung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="407e1-194">An explicitly declared controlled adjoint specialization implies the existence of an adjoint specialization.</span></span> 

<span data-ttu-id="407e1-195">Für einen Vorgang, dessen Text Wiederholungs-bis-Erfolg-Schleifen, Set-Anweisungen, Messungen, Rückgabe Anweisungen oder Aufrufe von anderen Vorgängen enthält, die den `Adjoint`-Funktor nicht unterstützen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach der `invert`-oder `auto`-Direktive nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="407e1-195">For operation whose body contains repeat-until-success loops, set statements, measurements, return statements, or calls to other operations that do not support the `Adjoint` functor, auto-generating an adjoint specialization following the `invert` or `auto` directive is not possible.</span></span>

### <a name="controlled"></a><span data-ttu-id="407e1-196">Klimatisiert</span><span class="sxs-lookup"><span data-stu-id="407e1-196">Controlled</span></span>

<span data-ttu-id="407e1-197">Die kontrollierte Version eines Vorgangs gibt an, wie eine Quantum-gesteuerte Version des Vorgangs implementiert wird, d. h., wie ein Vorgang angewendet wird, wenn er auf den Zustand eines Quantum-Register angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="407e1-197">The controlled version of an operation specifies how a quantum-controlled version of the operation is implemented, i.e. how an operation acts when applied conditioned on the state of a quantum register.</span></span>
<span data-ttu-id="407e1-198">Eine ausführlichere Beschreibung finden Sie im Abschnitt " [gesteuert](xref:microsoft.quantum.language.type-model#controlled) ".</span><span class="sxs-lookup"><span data-stu-id="407e1-198">A more complete description is provided in the [Controlled](xref:microsoft.quantum.language.type-model#controlled) section.</span></span>

<span data-ttu-id="407e1-199">Es ist zulässig, einen Vorgang ohne kontrollierte Version anzugeben. Beispielsweise haben Messvorgänge keine kontrollierte Version, da Sie nicht steuerbar sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-199">It is legal to specify an operation with no controlled version; for instance, measurement operations have no controlled version because they are not controllable.</span></span>
<span data-ttu-id="407e1-200">Ein Vorgang unterstützt den `Controlled`-Funktor nur dann, wenn seine Deklaration eine implizite oder explizite Deklaration einer kontrollierten Spezialisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="407e1-200">An operation supports the `Controlled` functor if and only if its declaration contains an implicit or explicit declaration of a controlled specialization.</span></span>
<span data-ttu-id="407e1-201">Eine explizit deklarierte, kontrollierte Adjoint-Spezialisierung impliziert das vorhanden sein einer kontrollierten Spezialisierung.</span><span class="sxs-lookup"><span data-stu-id="407e1-201">An explicitly declared controlled adjoint specialization implies the existence of a controlled specialization.</span></span> 

<span data-ttu-id="407e1-202">Bei einem Vorgang, dessen Text Aufrufe anderer Vorgänge enthält, die den `Controlled`-Funktor nicht unterstützen, ist das automatische Erstellen einer kontrollierten Spezialisierung nach der `distribute`-oder `auto`-Direktive nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="407e1-202">For an operation whose body contains calls to other operations that does not support the `Controlled` functor, auto-generating a controlled specialization following the `distribute` or `auto` directive is not possible.</span></span>

### <a name="controlled-adjoint"></a><span data-ttu-id="407e1-203">Kontrollierter Adjoint</span><span class="sxs-lookup"><span data-stu-id="407e1-203">Controlled Adjoint</span></span>

<span data-ttu-id="407e1-204">Die kontrollierte Adjoint-Version eines Vorgangs gibt an, wie eine Quantum-gesteuerte Version des Adjoint-Vorgangs des Vorgangs implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="407e1-204">The controlled adjoint version of an operation specifies how a quantum-controlled version of the adjoint of the operation is implemented.</span></span>
<span data-ttu-id="407e1-205">Es ist zulässig, einen Vorgang ohne kontrollierte Adjoint-Version anzugeben. Messvorgänge haben beispielsweise keine kontrollierte Adjoint-Version, da Sie weder steuerbar noch invertierbar sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-205">It is legal to specify an operation with no controlled adjoint version; for instance, measurement operations have no controlled adjoint version because they are neither controllable nor invertible.</span></span>

<span data-ttu-id="407e1-206">Eine kontrollierte Adjoint-Spezialisierung für einen Vorgang muss nur dann vorhanden sein, wenn sowohl ein Adjoint-als auch eine gesteuerte Spezialisierung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="407e1-206">A controlled adjoint specialization for an operation needs to exist if and only if both an adjoint and a controlled specialization exist.</span></span> <span data-ttu-id="407e1-207">In diesem Fall wird das vorhanden sein der kontrollierten Adjoint-Spezialisierung abgeleitet, und vom Compiler wird eine entsprechende Spezialisierung generiert, wenn keine Implementierung explizit definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="407e1-207">In that case, the existence of the controlled adjoint specialization is inferred and an appropriate specialization is generated by the compiler if no implementation has been defined explicitly.</span></span> 

<span data-ttu-id="407e1-208">Bei einem Vorgang, dessen Text Aufrufe von anderen Vorgängen enthält, die nicht über eine kontrollierte Adjoint-Version verfügen, ist das automatische Erstellen einer Adjoint-Spezialisierung nach den `invert``distribute`-oder `auto`-Direktive nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="407e1-208">For an operation whose body contains calls to other operations that do not have a controlled adjoint version, auto-generating an adjoint specialization following the `invert`, `distribute` or `auto` directive is not possible.</span></span>


### <a name="examples"></a><span data-ttu-id="407e1-209">Beispiele</span><span class="sxs-lookup"><span data-stu-id="407e1-209">Examples</span></span>

<span data-ttu-id="407e1-210">Eine Vorgangs Deklaration kann so einfach wie die folgende sein, die den primitiven Pauli X-Vorgang definiert:</span><span class="sxs-lookup"><span data-stu-id="407e1-210">An operation declaration might be as simple as the following, which defines the primitive Pauli X operation:</span></span>

```qsharp
operation X (qubit : Qubit) : Unit
is Adj + Ctl {
    body intrinsic;
    adjoint self;
}
```

<span data-ttu-id="407e1-211">Im folgenden wird der teleportvorgang definiert.</span><span class="sxs-lookup"><span data-stu-id="407e1-211">The following defines the teleport operation.</span></span>

```qsharp
// Entangle two qubits.
// Assumes that both qubits are in the |0> state.
operation PrepareEntangledPair (q1 : Qubit, q2 : Qubit) : Unit 
is Adj + Ctl {
    H(q2);
    CNOT(q2, q1);
}

// Teleport the quantum state of the source to the target.
// Assumes that the target is in the |0> state.
operation Teleport (source : Qubit, target : Qubit) : Unit {

    // Get a temporary for the Bell pair
    using (ancilla = Qubit())
    {
        // Create a Bell pair between the temporary and the target
        PrepareEntangledPair(target, ancilla);

        // Do the teleportation
        Adjoint PrepareEntangledPair(ancilla, source);

        if (MResetZ(source) == One) {
            X(target);
        }
        if (MResetZ(ancilla) == One) {
            Z(target);
        }
    }
}
```

## <a name="function-declarations"></a><span data-ttu-id="407e1-212">Funktionsdeklarationen</span><span class="sxs-lookup"><span data-stu-id="407e1-212">Function Declarations</span></span>

<span data-ttu-id="407e1-213">Funktionen sind rein klassische Routinen in Q #.</span><span class="sxs-lookup"><span data-stu-id="407e1-213">Functions are purely classical routines in Q#.</span></span>
<span data-ttu-id="407e1-214">Jede f #-Quelldatei kann eine beliebige Anzahl von Funktionen definieren.</span><span class="sxs-lookup"><span data-stu-id="407e1-214">Each Q# source file may define any number of functions.</span></span>

<span data-ttu-id="407e1-215">Eine Funktionsdeklaration besteht aus dem Schlüsselwort `function`, gefolgt von dem Symbol, das den Namen der Funktion, ein typisiertes bezeichnertupel, eine Typanmerkung, die den Rückgabetyp der Funktion beschreibt, und einem Anweisungsblock, der die Implementierung der Funktion beschreibt.</span><span class="sxs-lookup"><span data-stu-id="407e1-215">A function declaration consists of the keyword `function`, followed by the symbol that is the function’s name, a typed identifier tuple, a type annotation that describes the function's return type, and a statement block that describes the implementation of the function.</span></span>

<span data-ttu-id="407e1-216">Der Anweisungsblock, der eine Funktion definiert, muss in `{` eingeschlossen und `}` wie jeder andere Anweisungsblock sein.</span><span class="sxs-lookup"><span data-stu-id="407e1-216">The statement block defining a function must be enclosed in `{` and `}` like any other statement block.</span></span>

<span data-ttu-id="407e1-217">Funktionsnamen müssen innerhalb eines Namespace eindeutig sein und können keinen Konflikt mit den Vorgangs-und Typnamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="407e1-217">Function names must be unique within a namespace and may not conflict with operation and type names.</span></span>
<span data-ttu-id="407e1-218">Funktionen dürfen keine Qubits zuordnen oder ausleihen, oder es werden keine Vorgänge aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="407e1-218">Functions may not allocate or borrow qubits, or call operations.</span></span> <span data-ttu-id="407e1-219">Die partielle Anwendung von Vorgängen oder die Übergabe von typisierten Werten ist in Ordnung.</span><span class="sxs-lookup"><span data-stu-id="407e1-219">Partial application of operations or passing around operation typed values is fine.</span></span>

<span data-ttu-id="407e1-220">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="407e1-220">For example,</span></span>

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


## <a name="internal-declarations"></a><span data-ttu-id="407e1-221">Interne Deklarationen</span><span class="sxs-lookup"><span data-stu-id="407e1-221">Internal Declarations</span></span>

<span data-ttu-id="407e1-222">Benutzerdefinierte Typen, Vorgänge und Funktionen können auch als *intern*deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-222">User-defined types, operations, and functions can also be declared as *internal*.</span></span>
<span data-ttu-id="407e1-223">Dies bedeutet, dass nur innerhalb des Q #-Projekts, in dem Sie deklariert sind, auf Sie zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="407e1-223">This means that they can only be accessed from within the Q# project that they are declared in.</span></span>
<span data-ttu-id="407e1-224">Wenn ein Projekt als Verweis verwendet wird, werden alle *öffentlichen* (nicht internen) Deklarationen zur Verfügung gestellt, aber es wird versucht, eine interne Deklaration aus einem anderen Projekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="407e1-224">When a project is used as a reference, all of its *public* (non-internal) declarations are made available, but trying to use an internal declaration from another project will produce an error.</span></span>
<span data-ttu-id="407e1-225">Interne Deklarationen sind nützlich, wenn Sie modularen Code schreiben möchten, der von anderen Teilen des Projekts wieder verwendet werden kann, aber später noch geändert werden kann, ohne andere Projekte zu unterbrechen, die von ihm abhängig sein könnten.</span><span class="sxs-lookup"><span data-stu-id="407e1-225">Internal declarations are useful for writing modular code that can be reused by other parts of your project, but still be changed later without breaking other projects that might depend on it.</span></span>

<span data-ttu-id="407e1-226">Ein interner benutzerdefinierter Typ, Vorgang oder Funktion kann einfach durch Hinzufügen von `internal` am Anfang der Deklaration deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="407e1-226">An internal user-defined type, operation, or function can be declared simply by adding `internal` at the beginning of the declaration.</span></span>
<span data-ttu-id="407e1-227">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="407e1-227">For example,</span></span>

```qsharp
internal newtype PairOfQubits = (Qubit, Qubit);

internal operation PrepareEntangledPair(pair : PairOfQubits) : Unit 
is Adj + Ctl {
    let (q1, q2) = pair!;
    H(q2);
    CNOT(q2, q1);
}

internal function DotProduct(a : Double[], b : Double[]) : Double {
    ...
}
```

> [!WARNING]
> <span data-ttu-id="407e1-228">Interne benutzerdefinierte Typen können nur in Signaturen oder zugrunde liegenden Typen verwendet werden, wenn der entsprechende Aufruf Bare oder benutzerdefinierte Typ ebenfalls intern ist.</span><span class="sxs-lookup"><span data-stu-id="407e1-228">Internal user-defined types can only be used in signatures or underlying types if the corresponding callable or user-defined type is also internal.</span></span>
> <span data-ttu-id="407e1-229">Wenn beispielsweise ein benutzerdefinierter Typ `InternalOptions` der mit dem Schlüsselwort `internal` deklariert wurde, werden die folgenden Deklarationen zu Fehlern führen:</span><span class="sxs-lookup"><span data-stu-id="407e1-229">For example, if there is a user-defined type `InternalOptions` that was declared with the `internal` keyword, then the following declarations will result in errors:</span></span>
>
> ```qsharp
> // Error: Can't use InternalOptions as an output type of a public function.
> function DefaultInternalOptions() : InternalOptions { ... }
>
> // Error: Can't use InternalOptions as an item in a public user-defined type.
> newtype ExtendedOptions = (Internal : InternalOptions);
> ```
