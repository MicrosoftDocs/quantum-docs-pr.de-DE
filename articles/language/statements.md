---
title: 'Q #-Anweisungen | Microsoft-Dokumentation'
description: 'Q #-Anweisungen'
author: QuantumWriter
uid: microsoft.quantum.language.statements
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 9a6f5d53ec21090d0c13f4369e0270d264cd1e9b
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036490"
---
# <a name="statements-and-other-constructs"></a><span data-ttu-id="8f6eb-103">Anweisungen und andere Konstrukte</span><span class="sxs-lookup"><span data-stu-id="8f6eb-103">Statements and Other Constructs</span></span>

## <a name="comments"></a><span data-ttu-id="8f6eb-104">Kommentare</span><span class="sxs-lookup"><span data-stu-id="8f6eb-104">Comments</span></span>

<span data-ttu-id="8f6eb-105">Kommentare beginnen mit zwei Schrägstrichen, `//`und werden bis zum Ende der Zeile fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-105">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="8f6eb-106">Ein Kommentar kann an beliebiger Stelle in einer f #-Quelldatei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-106">A comment may appear anywhere in a Q# source file.</span></span>

### <a name="documentation-comments"></a><span data-ttu-id="8f6eb-107">Dokumentations Kommentare</span><span class="sxs-lookup"><span data-stu-id="8f6eb-107">Documentation Comments</span></span>

<span data-ttu-id="8f6eb-108">Kommentare, die mit drei Schrägstrichen (`///`) beginnen, werden vom Compiler speziell behandelt, wenn Sie unmittelbar vor einem Namespace, einem Vorgang, einer Spezialisierung, einer Funktion oder einer Typdefinition erscheinen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-108">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="8f6eb-109">In diesem Fall wird der Inhalt als Dokumentation für den definierten Aufruf baren oder benutzerdefinierten Typ, wie für andere .NET-Sprachen, übernommen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-109">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="8f6eb-110">In `///` Kommentaren wird Text, der als Teil der API-Dokumentation angezeigt wird, als [markdown](https://daringfireball.net/projects/markdown/syntax)formatiert, wobei verschiedene Teile der Dokumentation durch speziell benannte Header angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-110">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="8f6eb-111">Als Erweiterung von markdown können Querverweise auf Vorgänge, Funktionen und benutzerdefinierte Typen in Q # mithilfe des `@"<ref target>"`eingeschlossen werden, wobei `<ref target>` durch den voll qualifizierten Namen des Code Objekts ersetzt wird, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-111">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="8f6eb-112">Optional kann eine Dokumentations-Engine auch zusätzliche markdownerweiterungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-112">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="8f6eb-113">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-113">For example:</span></span>

```qsharp
/// # Summary
/// Given an operation and a target for that operation,
/// applies the given operation twice.
///
/// # Input
/// ## op
/// The operation to be applied.
/// ## target
/// The target to which the operation is to be applied.
///
/// # Type Parameters
/// ## 'T
/// The type expected by the given operation as its input.
///
/// # Example
/// ```Q#
/// // Should be equivalent to the identity.
/// ApplyTwice(H, qubit);
/// ```
///
/// # See Also
/// - Microsoft.Quantum.Intrinsic.H
operation ApplyTwice<'T>(op : ('T => Unit), target : 'T) : Unit {
    op(target);
    op(target);
}
```

<span data-ttu-id="8f6eb-114">Die folgenden Namen werden als Dokumentations Kommentar Header erkannt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-114">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="8f6eb-115">**Zusammenfassung**: eine kurze Zusammenfassung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-115">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="8f6eb-116">Der erste Absatz der Zusammenfassung wird für Hover-Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-116">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="8f6eb-117">Es sollte nur Text sein.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-117">It should be plain text.</span></span>
- <span data-ttu-id="8f6eb-118">**Beschreibung**: eine Beschreibung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-118">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="8f6eb-119">Die Zusammenfassung und Beschreibung werden verkettet, um die generierte Dokumentations Datei für die Funktion, den Vorgang oder den Typ zu bilden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-119">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="8f6eb-120">Die Beschreibung enthält möglicherweise in-line-Symbole und-Gleichungen in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-120">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="8f6eb-121">**Input**: eine Beschreibung des eingabetupels für einen Vorgang oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-121">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="8f6eb-122">Kann zusätzliche markdown-Unterabschnitte enthalten, die jedes einzelne Element des eingabetupels angeben.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-122">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="8f6eb-123">**Output**: eine Beschreibung des Tupels, das von einem Vorgang oder einer Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-123">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="8f6eb-124">**Typparameter**: ein leerer Abschnitt, der einen zusätzlichen unter Abschnitt für jeden generischen Typparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-124">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="8f6eb-125">**Beispiel**: ein kurzes Beispiel für den Vorgang, die Funktion oder den Typ, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-125">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="8f6eb-126">**Hinweise**: verschiedene Prosa, die einen Aspekt des Vorgangs, der Funktion oder des Typs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-126">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="8f6eb-127">**Siehe auch**: eine Liste der voll qualifizierten Namen, die verwandte Funktionen, Vorgänge oder benutzerdefinierte Typen angeben.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-127">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="8f6eb-128">**Verweise**: eine Liste von verweisen und citationen für das Element, das dokumentiert wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-128">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="namespaces"></a><span data-ttu-id="8f6eb-129">Namespaces</span><span class="sxs-lookup"><span data-stu-id="8f6eb-129">Namespaces</span></span>

<span data-ttu-id="8f6eb-130">Jeder Q #-Vorgang, jede Funktion und jeder benutzerdefinierte Typ wird in einem Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-130">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>
<span data-ttu-id="8f6eb-131">F # befolgt die gleichen Regeln für die Benennung wie andere .NET-Sprachen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-131">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="8f6eb-132">F # unterstützt jedoch keine relativen Verweise auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-132">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="8f6eb-133">Das heißt, wenn der Namespace `a.b` geöffnet wurde, wird ein Verweis auf die Vorgangs Namen `c.d` nicht in einen Vorgang mit vollständigem Namen `a.b.c.d`aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-133">That is, if the namespace `a.b` has been opened, a reference to an operation names `c.d` will not be resolved to an operation with full name `a.b.c.d`.</span></span>

<span data-ttu-id="8f6eb-134">Innerhalb eines Namespace Blocks kann die `open` Direktive verwendet werden, um alle Typen und callables zu importieren, die in einem bestimmten Namespace deklariert sind, und auf diese mit Ihrem nicht qualifizierten Namen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-134">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span> <span data-ttu-id="8f6eb-135">Optional kann ein Kurzname für den geöffneten Namespace definiert werden, sodass alle Elemente aus diesem Namespace durch den definierten Kurznamen qualifiziert werden können (und müssen).</span><span class="sxs-lookup"><span data-stu-id="8f6eb-135">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="8f6eb-136">Die `open`-Direktive gilt für den gesamten Namespace Block in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-136">The `open` directive applies to the entire namespace block within a file.</span></span>

<span data-ttu-id="8f6eb-137">Auf einen Typ oder Aufruf baren Wert, der in einem anderen Namespace definiert ist, der nicht im aktuellen Namespace geöffnet ist, muss mit seinem voll qualifizierten Namen darauf verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-137">A type or callable defined in another namespace that is not opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="8f6eb-138">Beispielsweise muss ein Vorgang mit dem Namen `Op` im `X.Y`-Namespace mit dem voll qualifizierten Namen `X.Y.Op`referenziert werden, es sei denn, der `X.Y`-Namespace wurde zuvor im aktuellen Block geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-138">For example, an operation named `Op` in the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="8f6eb-139">Wie bereits erwähnt, ist es nicht möglich, auf den Vorgang als `Y.Op`zu verweisen, auch wenn der `X` Namespace geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-139">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="8f6eb-140">Wenn ein Kurzname `Z` für `X.Y` in diesem Namespace und in der Datei definiert ist, muss `Op` als `Z.Op`bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-140">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace
}
```

<span data-ttu-id="8f6eb-141">Es ist in der Regel besser, einen Namespace mit einer `open`-Direktive einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-141">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="8f6eb-142">Die Verwendung eines voll qualifizierten Namens ist erforderlich, wenn zwei Namespaces Konstrukte mit dem gleichen Namen definieren und die aktuelle Quelle Konstrukte aus beidem verwendet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-142">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

## <a name="formatting"></a><span data-ttu-id="8f6eb-143">Formatierung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-143">Formatting</span></span>

<span data-ttu-id="8f6eb-144">Die meisten Q #-Anweisungen und-Direktiven enden mit einem abschließenden Semikolon, `;`.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-144">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="8f6eb-145">-Anweisungen und-Deklarationen wie `for` und `operation`, die mit einem-Anweisungsblock enden, erfordern kein abschließendes Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-145">Statements and declarations such as `for` and `operation` that end with a statement block do not require a terminating semicolon.</span></span>
<span data-ttu-id="8f6eb-146">Jede Anweisungs Beschreibung gibt an, ob das abschließende Semikolon erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-146">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="8f6eb-147">Anweisungen, wie Ausdrücke, Deklarationen und Direktiven, werden möglicherweise über mehrere Zeilen hinweg aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-147">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="8f6eb-148">Das vorhanden sein mehrerer Anweisungen in einer einzelnen Zeile sollte vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-148">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="8f6eb-149">Anweisungsblöcke</span><span class="sxs-lookup"><span data-stu-id="8f6eb-149">Statement Blocks</span></span>

<span data-ttu-id="8f6eb-150">Q #-Anweisungen werden in Anweisungsblöcke gruppiert.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-150">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="8f6eb-151">Ein Anweisungsblock beginnt mit einem öffnenden `{` und endet mit einem schließenden `}`.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-151">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="8f6eb-152">Ein Anweisungsblock, der lexikalisch in einem anderen-Block eingeschlossen ist, wird als Teil Block des enthaltenden Blocks angesehen; enthaltende-und-Unterblöcke werden auch als äußere und innere Blöcke bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-152">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="symbol-binding-and-assignment"></a><span data-ttu-id="8f6eb-153">Symbol Bindung und-Zuweisung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-153">Symbol Binding and Assignment</span></span>

<span data-ttu-id="8f6eb-154">Q # unterscheidet zwischen veränderbaren und unveränderlichen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-154">Q# distinguishes between mutable and immutable symbols.</span></span>
<span data-ttu-id="8f6eb-155">Im Allgemeinen wird die Verwendung unveränderlicher Symbole empfohlen, da es dem Compiler ermöglicht, weitere Optimierungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-155">In general, the use of immutable symbols is encouraged because it allows the compiler to perform more optimizations.</span></span>

<span data-ttu-id="8f6eb-156">Die linke Seite der Bindung besteht aus einem symboltupel und der rechten Seite eines Ausdrucks.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-156">The left-hand-side of the binding consists of a symbol tuple, and the right hand side of an expression.</span></span>

<span data-ttu-id="8f6eb-157">Da es sich bei allen Q #-Typen um Werttypen handelt, bei denen die Qubits eine etwas besondere Rolle übernimmt, wird formal eine Kopie erstellt, wenn ein Wert an ein Symbol gebunden ist oder wenn ein Symbol erneut erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-157">Since all Q# types are value types - with the qubits taking a somewhat special role - formally a "copy" is created when a value is bound to a symbol, or when a symbol is rebound.</span></span> <span data-ttu-id="8f6eb-158">Dies heißt, dass das Verhalten von Q # identisch ist, wenn eine Kopie bei der Zuweisung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-158">That is to say, the behavior of Q# is the same as if a copy were created on assignment.</span></span> <span data-ttu-id="8f6eb-159">Dies gilt insbesondere für Arrays.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-159">This in particular also includes arrays.</span></span> <span data-ttu-id="8f6eb-160">Natürlich werden in der Praxis nur die relevanten Teile bei Bedarf neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-160">Of course in practice only the relevant pieces are actually recreated as needed.</span></span> 

### <a name="tuple-deconstruction"></a><span data-ttu-id="8f6eb-161">Tupelerstellung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-161">Tuple Deconstruction</span></span>

<span data-ttu-id="8f6eb-162">Wenn die Rechte Seite der Bindung ein Tupel ist, kann dieses Tupel bei der Zuweisung dekonstruiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-162">If the right-hand side of the binding is a tuple, then that tuple may be deconstructed upon assignment.</span></span>
<span data-ttu-id="8f6eb-163">Solche Dekonstruktionen können geschaltete Tupel einschließen, und jede vollständige oder partielle Dekonstruktion ist gültig, solange die Form des Tupels auf der rechten Seite mit der Form des symboltupels kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-163">Such deconstructions may involve nested tuples, and any full or partial deconstruction is valid as long as the shape of the tuple on the right hand side is compatible with the shape of the symbol tuple.</span></span>
<span data-ttu-id="8f6eb-164">Die Dekonstruktion von Tupeln kann insbesondere dann auch verwendet werden, wenn die Rechte Seite des `=` ein tupelwertausdruck ist.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-164">Tuple deconstruction can in particular also be used when the right-hand side of the `=` is a tuple-valued expression.</span></span>

```qsharp
let (i, f) = (5, 0.1); // i is bound to 5 and f to 0.1
mutable (a, (_, b)) = (1, (2, 3)); // a is bound to 1, b is bound to 3
mutable (x, y) = ((1, 2), [3, 4]); // x is bound to (1,2), y is bound to [3,4]
set (x, _, y) = ((5, 6), 7, [8]);  // x is rebound to (5,6), y is rebound to [8]
let (r1, r2) = MeasureTwice(q1, PauliX, q2, PauliY);
```

### <a name="immutable-symbols"></a><span data-ttu-id="8f6eb-165">Unveränderliche Symbole</span><span class="sxs-lookup"><span data-stu-id="8f6eb-165">Immutable Symbols</span></span>

<span data-ttu-id="8f6eb-166">Unveränderliche Symbole werden mithilfe der `let`-Anweisung gebunden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-166">Immutable symbols are bound using the `let` statement.</span></span>
<span data-ttu-id="8f6eb-167">Dies entspricht ungefähr der Variablen Deklaration und Initialisierung in Sprachen wie C#, mit dem Unterschied, dass Q #-Symbole nach der Bindung möglicherweise nicht geändert werden. `let` Bindungen sind unveränderlich.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-167">This is roughly equivalent to variable declaration and initialization in languages such as C#, except that Q# symbols, once bound, may not be changed; `let` bindings are immutable.</span></span>

<span data-ttu-id="8f6eb-168">Eine unveränderliche Bindung besteht aus dem Schlüsselwort `let`, gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=`, einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-168">An immutable binding consists of the keyword `let`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="8f6eb-169">Der Typ der gebundenen Symbole wird basierend auf dem Ausdruck auf der rechten Seite abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-169">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span>

### <a name="mutable-symbols"></a><span data-ttu-id="8f6eb-170">Änderbare Symbole</span><span class="sxs-lookup"><span data-stu-id="8f6eb-170">Mutable Symbols</span></span>

<span data-ttu-id="8f6eb-171">Änderbare Symbole werden mithilfe der `mutable` Anweisung definiert und initialisiert.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-171">Mutable symbols are defined and initialized using the `mutable` statement.</span></span>
<span data-ttu-id="8f6eb-172">Symbole, die als Teil einer `mutable` Anweisung deklariert und gebunden werden, können später im Code an einen anderen Wert zurückgebunden werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-172">Symbols declared and bound as part of a `mutable` statement may be rebound to a different value later in the code.</span></span> 

<span data-ttu-id="8f6eb-173">Eine änderbare Bindungs Anweisung besteht aus dem Schlüsselwort `mutable`, gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=`, einem Ausdruck, an den die Symbole gebunden werden, und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-173">A mutable binding statement consists of the keyword `mutable`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to bind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="8f6eb-174">Der Typ der gebundenen Symbole wird basierend auf dem Ausdruck auf der rechten Seite abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-174">The type of the bound symbol(s) is inferred based on the expression on the right hand side.</span></span> <span data-ttu-id="8f6eb-175">Wenn ein Symbol später im Code wieder verwendet wird, wird der Typ nicht geändert, und der gebundene Wert muss mit diesem Typ kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-175">If a symbol is rebound later in the code, its type does not change, and the bound value needs to be compatible with that type.</span></span>

### <a name="rebinding-of-mutable-symbols"></a><span data-ttu-id="8f6eb-176">Neubinden von änderbaren Symbolen</span><span class="sxs-lookup"><span data-stu-id="8f6eb-176">Rebinding of Mutable Symbols</span></span>

<span data-ttu-id="8f6eb-177">Eine änderbare Variable kann mit einer `set`-Anweisung erneut gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-177">A mutable variable may be rebound using a `set` statement.</span></span>
<span data-ttu-id="8f6eb-178">Eine solche erneute Bindung besteht aus dem Schlüsselwort `set`, gefolgt von einem Symbol oder einem symboltupel, einem Gleichheitszeichen `=`, einem Ausdruck zum erneuten Binden der Symbole an und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-178">Such a rebinding consists of the keyword `set`, followed by a symbol or symbol tuple, an equals sign `=`, an expression to rebind the symbol(s) to, and a terminating semicolon.</span></span>
<span data-ttu-id="8f6eb-179">Der Wert muss mit den Typen der Symbole kompatibel sein, an die er gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-179">The value must be compatible with the type(s) of the symbol(s) it is bound to.</span></span>

#### <a name="apply-and-reassign-statement"></a><span data-ttu-id="8f6eb-180">Apply-and-REASSIGN-Anweisung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-180">Apply-and-Reassign Statement</span></span>

<span data-ttu-id="8f6eb-181">Eine bestimmte Art von Set-Statement, auf die als Apply-and-REASSIGN-Anweisung verwiesen wird, stellt eine bequeme Methode für die Verkettung dar, wenn die Rechte Seite aus der Anwendung eines binären Operators besteht und das Ergebnis an das linke Argument des Operators zurückgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-181">A particular kind of set-statement we refer to as an apply-and-reassign statement provides a convenient way of concatenation if the right hand side consists of the application of a binary operator and the result is to be rebound to the left argument to the operator.</span></span> <span data-ttu-id="8f6eb-182">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-182">For example,</span></span>
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter += 1;
    // ...
}
```
<span data-ttu-id="8f6eb-183">erhöht den Wert des Zählers `counter` in jeder Iterationen der `for` Schleife.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-183">increments the value of the counter `counter` in each iteration of the `for` loop.</span></span> <span data-ttu-id="8f6eb-184">Der obige Code entspricht</span><span class="sxs-lookup"><span data-stu-id="8f6eb-184">The code above is equivalent to</span></span> 
```qsharp
mutable counter = 0;
for (i in 1 .. 2 .. 10) {
    set counter = counter + 1;
    // ...
}
```
<span data-ttu-id="8f6eb-185">Ähnliche Anweisungen sind für alle binären Operatoren verfügbar, in denen der Typ der linken Seite mit dem Ausdruckstyp übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-185">Similar statements are available for all binary operators in which the type of the left-hand-side matches the expression type.</span></span> <span data-ttu-id="8f6eb-186">Dies stellt beispielsweise eine bequeme Möglichkeit zum Sammeln von Werten dar:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-186">This provides for example a convenient way to accumulate values:</span></span>
```qsharp
mutable results = new Result[0];
for (qubit in qubits) {
    set results += [M(q)];
    // ...
}
```
#### <a name="update-and-reassign-statement"></a><span data-ttu-id="8f6eb-187">Update-and-REASSIGN-Anweisung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-187">Update-and-Reassign Statement</span></span>

<span data-ttu-id="8f6eb-188">Eine ähnliche Verkettung ist für Kopier-und Update Ausdrücke auf der rechten Seite vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-188">A similar concatenation exists for copy-and-update expressions on the right hand side.</span></span> <span data-ttu-id="8f6eb-189">Entsprechend sind Update-und-REASSIGN-Anweisungen für benannte Elemente in benutzerdefinierten Typen sowie für Array Elemente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-189">Correspondingly, update-and-reassign statements exist for named items in user-defined types as well as for array items.</span></span>  

```qsharp
newtype Complex = (Re : Double, Im : Double);

function ComplexSum(reals : Double[], ims : Double[]) : Complex[] {
    mutable res = Complex(0.,0.);

    for (r in reals) {
        set res w/= Re <- res::Re + r; // update-and-reassign statement
    }
    for (i in ims) {
        set res w/= Im <- res::Im + i; // update-and-reassign statement
    }
    return res;
}
```

<span data-ttu-id="8f6eb-190">Im Fall von Arrays enthalten unsere Standardbibliotheken die erforderlichen Tools für viele gängige Anforderungen an die Initialisierung und Bearbeitung von Arrays. dadurch ist es nicht mehr erforderlich, Array Elemente an erster Stelle zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-190">In the case of arrays, our standard libraries contain the necessary tools for many common array initialization and manipulation needs, and thus help avoid having to update array items in the first place.</span></span> <span data-ttu-id="8f6eb-191">Update-und-REASSIGN-Anweisungen stellen bei Bedarf eine Alternative dar:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-191">Update-and-reassign statements provide an alternative if needed:</span></span>

```qsharp
operation GenerateRandomInts(max : Int, nSamples : Int) : Int[] {
    mutable samples = new Double[0];
    for (i in 1 .. nSamples) {
        set samples += [RandomInt(max)];
    }
    return samples;
}

operation SampleUniformDistrbution(nSamples : Int, nSteps : Int) : Double[] {
    let normalization = 1. / IntAsDouble(nSteps);
    mutable samples = GenerateRandomInts(nSteps, nSamples);
    
    for (i in IndexRange(samples) {
        let value = IntAsDouble(samples[i]);
        set samples w/= i <- normalization * value; // update-and-reassign statement
    }
}

```

> [!TIP]   
> <span data-ttu-id="8f6eb-192">Vermeiden Sie unnötige Verwendung von Update-und-REASSIGN-Anweisungen, indem Sie die in <xref:microsoft.quantum.arrays>bereitgestellten Tools nutzen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-192">Avoid unnecessary use of update-and-reassign statements by leveraging the tools provided in <xref:microsoft.quantum.arrays>.</span></span>

<span data-ttu-id="8f6eb-193">Die-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f6eb-193">The function</span></span>
```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    mutable pauliArray = new Pauli[length];
    for (index in 0 .. length - 1) {
        set pauliArray w/= index <- 
            index == location ? pauli | PauliI;
    }    
    return pauliArray;
}
```
<span data-ttu-id="8f6eb-194">kann z. b. einfach mithilfe der in `Microsoft.Quantum.Arrays``ConstantArray` Funktion vereinfacht werden und gibt einen Copy-and-Update-Ausdruck zurück:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-194">for example can simply be simplified using the function `ConstantArray` in `Microsoft.Quantum.Arrays`, and returning a copy-and-update expression:</span></span>

```qsharp
function PauliEmbedding(pauli : Pauli, length : Int, location : Int) : Pauli[] {
    return ConstantArray(length, PauliI) w/ location <- pauli;
}
```

### <a name="binding-scopes"></a><span data-ttu-id="8f6eb-195">Bindungs Bereiche</span><span class="sxs-lookup"><span data-stu-id="8f6eb-195">Binding Scopes</span></span>

<span data-ttu-id="8f6eb-196">Im allgemeinen verlassen Symbol Bindungen den Gültigkeitsbereich und werden am Ende des Anweisungsblocks, in dem Sie auftreten, inaktiv.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-196">In general, symbol bindings go out of scope and become inoperative at the end of the statement block they occur in.</span></span>
<span data-ttu-id="8f6eb-197">Es gibt jedoch zwei Ausnahmen:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-197">There are two exceptions to this rule:</span></span>

- <span data-ttu-id="8f6eb-198">Die Bindung der Schleifen Variablen einer `for`-Schleife liegt im Gültigkeitsbereich des Texts der for-Schleife, aber nicht nach dem Ende der Schleife.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-198">The binding of the loop variable of a `for` loop is in scope for the body of the for loop, but not after the end of the loop.</span></span>
- <span data-ttu-id="8f6eb-199">Alle drei Teile eines `repeat`/`until`-Schleife (der Text, der Test und das Fixup) werden als einzelner Bereich behandelt, sodass im Text gebundene Symbole im Test und im Fixup verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-199">All three portions of a `repeat`/`until` loop (the body, the test, and the fixup) are treated as a single scope, so symbols that are bound in the body are available in the test and in the fixup.</span></span>

<span data-ttu-id="8f6eb-200">Für beide Schleifen Typen wird jeder Durchlauf der Schleife in einem eigenen Bereich ausgeführt, sodass Bindungen aus einem früheren Durchlauf in einem späteren Durchlauf nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-200">For both types of loops, each pass through the loop executes in its own scope, so bindings from an earlier pass are not available in a later pass.</span></span>

<span data-ttu-id="8f6eb-201">Symbol Bindungen aus äußeren Blöcken werden von inneren Blöcken geerbt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-201">Symbol bindings from outer blocks are inherited by inner blocks.</span></span>
<span data-ttu-id="8f6eb-202">Ein Symbol kann nur einmal pro Block gebunden werden. Es ist unzulässig, ein Symbol mit dem gleichen Namen wie ein anderes Symbol zu definieren, das sich im Gültigkeitsbereich befindet (kein "shadodown").</span><span class="sxs-lookup"><span data-stu-id="8f6eb-202">A symbol may only be bound once per block; it is illegal to define a symbol with the same name as another symbol that is within scope (no "shadowing").</span></span>
<span data-ttu-id="8f6eb-203">Die folgenden Sequenzen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-203">The following sequences would be legal:</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
}
let n = 8;
...                 // n is 8
```

<span data-ttu-id="8f6eb-204">and</span><span class="sxs-lookup"><span data-stu-id="8f6eb-204">and</span></span>

```qsharp
if (a == b) {
    ...
    let n = 5;
    ...             // n is 5
} else {
    ...
    let n = 8;
    ...             // n is 8
}
```

<span data-ttu-id="8f6eb-205">Dies wäre jedoch unzulässig:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-205">But this would be illegal:</span></span>

```qsharp
let n = 5;
...                 // n is 5
let n = 8;          // Error!!
...
```

<span data-ttu-id="8f6eb-206">wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-206">as would:</span></span>

```qsharp
let n = 8;
if (a == b) {
    ...             // n is 8
    let n = 5;      // Error!
    ...
}
...
```

## <a name="control-flow"></a><span data-ttu-id="8f6eb-207">Ablaufsteuerung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-207">Control Flow</span></span>

### <a name="for-loop"></a><span data-ttu-id="8f6eb-208">For-Schleife</span><span class="sxs-lookup"><span data-stu-id="8f6eb-208">For Loop</span></span>

<span data-ttu-id="8f6eb-209">Die `for`-Anweisung unterstützt Iterationen über einen ganzzahligen Bereich oder über ein Array.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-209">The `for` statement supports iteration over an integer range or over an array.</span></span>
<span data-ttu-id="8f6eb-210">Die-Anweisung besteht aus dem Schlüsselwort `for`, einer öffnenden Klammer `(`, gefolgt von einem Symbol-oder symboltupel, dem Schlüsselwort `in`, einem Ausdruck vom Typ `Range` oder Array, einer schließenden Klammer `)`und einem Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-210">The statement consists of the keyword `for`, an open parenthesis `(`, followed by a symbol or symbol tuple, the keyword `in`, an expression of type `Range` or array, a close parenthesis `)`, and a statement block.</span></span>

<span data-ttu-id="8f6eb-211">Der Anweisungsblock (der Hauptteil der Schleife) wird wiederholt ausgeführt, wobei die definierten Symbole (die Schleifen Variablen) an jeden Wert im Bereich oder Array gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-211">The statement block (the body of the loop) is executed repeatedly, with the defined symbol(s) (the loop variable(s)) bound to each value in the range or array.</span></span>
<span data-ttu-id="8f6eb-212">Beachten Sie, dass der Text nicht ausgeführt wird, wenn der Bereichs Ausdruck zu einem leeren Bereich oder Array ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-212">Note that if the range expression evaluates to an empty range or array, the body will not be executed at all.</span></span>
<span data-ttu-id="8f6eb-213">Der Ausdruck wird vor der Eingabe der Schleife vollständig ausgewertet und ändert sich nicht, während die Schleife ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-213">The expression is fully evaluated before entering the loop, and will not change while the loop is executing.</span></span>

<span data-ttu-id="8f6eb-214">Die Bindung der deklarierten Symbole ist unveränderlich und folgt denselben Regeln wie andere Variablen Bindungen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-214">The binding of the declared symbol(s) is immutable and follows the same rules as other variable bindings.</span></span> <span data-ttu-id="8f6eb-215">Insbesondere ist es möglich, bei der Zuweisung zu den Schleifen Variablen z. b. Array Elemente für eine Iterationen über ein Array zu strukturieren.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-215">In particular, it is possible to destruct e.g. array items for an iteration over an array upon assignment to the loop variable(s).</span></span>

<span data-ttu-id="8f6eb-216">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-216">For example,</span></span>

```qsharp
// ...
for (qubit in qubits) { // qubits contains a Qubit[]
    H(qubit);
}

mutable results = new (Int, Results)[Length(qubits)];
for (index in 0 .. Length(qubits) - 1) {
    set results w/= index <- (index, M(qubits[index]));
}

mutable accumulated = 0;
for ((index, measured) in results) {
    if (measured == One) {
        set accumulated += 1 <<< index;
    }
}
```

<span data-ttu-id="8f6eb-217">Die Schleifenvariable wird an jedem Eingang an den Schleifen Text gebunden, und die Bindung am Ende des Texts wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-217">The loop variable is bound at each entrance to the loop body, and unbound at the end of the body.</span></span>
<span data-ttu-id="8f6eb-218">Insbesondere wird die Schleifenvariable nicht gebunden, nachdem die for-Schleife abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-218">In particular, the loop variable is not bound after the for loop is completed.</span></span>

### <a name="repeat-until-success-loop"></a><span data-ttu-id="8f6eb-219">Repeat-Until-Success-Schleife</span><span class="sxs-lookup"><span data-stu-id="8f6eb-219">Repeat-Until-Success Loop</span></span>

<span data-ttu-id="8f6eb-220">Die `repeat`-Anweisung unterstützt das Quantum-Muster "Wiederholung bis Erfolg".</span><span class="sxs-lookup"><span data-stu-id="8f6eb-220">The `repeat` statement supports the quantum “repeat until success” pattern.</span></span>
<span data-ttu-id="8f6eb-221">Sie besteht aus dem Schlüsselwort `repeat`, gefolgt von einem Anweisungsblock ( _Schleifen_ Text), dem Schlüsselwort `until`, einem booleschen Ausdruck und einem abschließenden Semikolon oder dem Schlüsselwort `fixup` gefolgt von einem anderen Anweisungsblock (der _Fixup_).</span><span class="sxs-lookup"><span data-stu-id="8f6eb-221">It consists of the keyword `repeat`, followed by a statement block (the _loop_ body), the keyword `until`, a Boolean expression, and either a terminating semicolon or the keyword `fixup` followed by another statement block (the _fixup_).</span></span>
<span data-ttu-id="8f6eb-222">Der Schleifen Text, die Bedingung und das Fixup werden als einzelner Bereich betrachtet, sodass im Text gebundene Symbole in der Bedingung und dem Fixup verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-222">The loop body, condition, and fixup are all considered to be a single scope, so symbols bound in the body are available in the condition and fixup.</span></span>

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

<span data-ttu-id="8f6eb-223">Der Schleifen Text wird ausgeführt, und anschließend wird die Bedingung ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-223">The loop body is executed, and then the condition is evaluated.</span></span>
<span data-ttu-id="8f6eb-224">Wenn die Bedingung true ist, wird die-Anweisung abgeschlossen. Andernfalls wird das Fixup ausgeführt, und die Anweisung wird erneut ausgeführt, beginnend mit dem Schleifen Text.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-224">If the condition is true, then the statement is completed; otherwise, the fixup is executed, and the statement is re-executed starting with the loop body.</span></span>
<span data-ttu-id="8f6eb-225">Beachten Sie, dass das Abschließen der Ausführung des Fixup den Bereich für die-Anweisung beendet, sodass Symbol Bindungen, die während des Texts oder Fixup erstellt werden, in nachfolgenden Wiederholungen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-225">Note that completing the execution of the fixup ends the scope for the statement, so that symbol bindings made during the body or fixup are not available in subsequent repetitions.</span></span>

<span data-ttu-id="8f6eb-226">Der folgende Code ist z. b. eine probabilistische Verbindung, die ein wichtiges Drehungs Gate implementiert $V _3 = (\boldone + 2 i)/\sqrt{5}$ mithilfe von Hadamard und t Gates.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-226">For example, the following code is a probabilistic circuit that implements an important rotation gate $V_3 = (\boldone + 2 i Z) / \sqrt{5}$ using the Hadamard and T gates.</span></span>
<span data-ttu-id="8f6eb-227">Die Schleife wird im Durchschnitt von $ \frac{8}{5}$-Wiederholungen beendet.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-227">The loop terminates in $\frac{8}{5}$ repetitions on average.</span></span>
<span data-ttu-id="8f6eb-228">Weitere Informationen finden Sie [*unter Repeat-Until-Success: nicht deterministische Zerlegung von Single-Qubit-uniflüssen*](https://arxiv.org/abs/1311.1074) ("Petznick" und "svore", 2014).</span><span class="sxs-lookup"><span data-stu-id="8f6eb-228">See [*Repeat-Until-Success: Non-deterministic decomposition of single-qubit unitaries*](https://arxiv.org/abs/1311.1074) (Paetznick and Svore, 2014) for details.</span></span>

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

> [!TIP]   
> <span data-ttu-id="8f6eb-229">Vermeiden Sie die Verwendung von Wiederholungs-bis-Erfolg-Schleifen innerhalb von Funktionen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-229">Avoid using repeat-until-success loops inside functions.</span></span> <span data-ttu-id="8f6eb-230">Die entsprechende Funktionalität wird von while-Schleifen in Funktionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-230">The corresponding functionality is provided by while loops in functions.</span></span> 

### <a name="while-loop"></a><span data-ttu-id="8f6eb-231">While-Schleife</span><span class="sxs-lookup"><span data-stu-id="8f6eb-231">While Loop</span></span>

<span data-ttu-id="8f6eb-232">Wiederholungs-bis-Erfolg-Muster verfügen über eine sehr Quantum-spezifische-Anmerkung.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-232">Repeat-until-success patterns have a very quantum-specific connotation.</span></span> <span data-ttu-id="8f6eb-233">Sie werden häufig in bestimmten Klassen von Quantum-Algorithmen verwendet. Dies ist daher das dedizierte Sprachkonstrukt in f #.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-233">They are widely used in particular classes of quantum algorithms -- hence the dedicated language construct in Q#.</span></span> <span data-ttu-id="8f6eb-234">Allerdings müssen Schleifen, die basierend auf einer Bedingung unterbrechen und deren Ausführungsdauer zur Kompilierzeit nicht bekannt ist, mit bestimmter Sorgfalt in einer Quantum-Laufzeit behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-234">However, loops that break based on a condition and whose execution length is thus unknown at compile time need to be handled with particular care in a quantum runtime.</span></span> <span data-ttu-id="8f6eb-235">Die Verwendung in Funktionen andererseits ist nicht problematisch, da diese nur Code enthalten, der auf herkömmlicher (nicht Quantum-) Hardware ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-235">Their use within functions on the other hand is unproblematic, since these only contain code that will be executed on conventional (non-quantum) hardware.</span></span> 

<span data-ttu-id="8f6eb-236">F # unterstützt daher die Verwendung von while-Schleifen nur innerhalb von Functions.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-236">Q# therefore supports to use of while loops within functions only.</span></span> <span data-ttu-id="8f6eb-237">Eine `while`-Anweisung besteht aus dem Schlüsselwort `while`, einer öffnenden Klammer `(`, einer Bedingung (d. h. einem booleschen Ausdruck), einer schließenden Klammer `)`und einem Anweisungsblock.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-237">A `while` statement consists of the keyword `while`, an open parenthesis `(`, a condition (i.e. a Boolean expression), a close parenthesis `)`, and a statement block.</span></span>
<span data-ttu-id="8f6eb-238">Der Anweisungsblock (der Text der Schleife) wird ausgeführt, solange die Bedingung als `true`ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-238">The statement block (the body of the loop) is executed as long as the condition evaluates to `true`.</span></span>

```qsharp
// ...
mutable (item, index) = (-1, 0);
while (index < Length(arr) && item < 0) { 
    set item = arr[index];
    set index += 1;
}
```

### <a name="conditional-statement"></a><span data-ttu-id="8f6eb-239">Bedingte Anweisung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-239">Conditional Statement</span></span>

<span data-ttu-id="8f6eb-240">Die `if`-Anweisung unterstützt die bedingte Ausführung.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-240">The `if` statement supports conditional execution.</span></span>
<span data-ttu-id="8f6eb-241">Sie besteht aus dem Schlüsselwort `if`, einer öffnenden Klammer `(`, einem booleschen Ausdruck, einer schließenden Klammer `)`und einem Anweisungsblock (der _Then_ -Block).</span><span class="sxs-lookup"><span data-stu-id="8f6eb-241">It consists of the keyword `if`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _then_ block).</span></span>
<span data-ttu-id="8f6eb-242">Auf diese kann eine beliebige Anzahl von else-if-Klauseln folgen, von denen jede aus dem Schlüsselwort `elif`, einer öffnenden Klammer `(`, einem booleschen Ausdruck, einer schließenden Klammer `)`und einem Anweisungsblock (der _else-if-_ Block) besteht.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-242">This may be followed by any number of else-if clauses, each of which consists of the keyword `elif`, an open parenthesis `(`, a Boolean expression, a close parenthesis `)`, and a statement block (the _else-if_ block).</span></span>
<span data-ttu-id="8f6eb-243">Schließlich kann die Anweisung optional mit einer Else-Klausel abgeschlossen werden, die aus dem Schlüsselwort besteht `else` gefolgt von einem anderen Anweisungsblock (der _else_ -Block).</span><span class="sxs-lookup"><span data-stu-id="8f6eb-243">Finally, the statement may optionally finish with an else clause, which consists of the keyword `else` followed by another statement block (the _else_ block).</span></span>
<span data-ttu-id="8f6eb-244">Die Bedingung wird ausgewertet, und wenn der Wert true ist, wird der then-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-244">The condition is evaluated, and if it is true, the then block is executed.</span></span>
<span data-ttu-id="8f6eb-245">Wenn die Bedingung false ist, wird die erste else-if-Bedingung ausgewertet. Wenn der Wert true ist, wird der Else-If-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-245">If the condition is false, then the first else-if condition is evaluated; if it is true, that else-if block is executed.</span></span>
<span data-ttu-id="8f6eb-246">Andernfalls wird der zweite Else-If-Block getestet, dann der dritte, usw., bis entweder eine-Klausel mit einer true-Bedingung gefunden wird oder keine else-if-Klauseln mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-246">Otherwise, the second else-if block is tested, and then the third, and so on until either a clause with a true condition is encountered or there are no more else-if clauses.</span></span>
<span data-ttu-id="8f6eb-247">Wenn die ursprüngliche if-Bedingung und alle else-if-Klauseln als false ausgewertet werden, wird der Else-Block ausgeführt, wenn ein solcher angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-247">If the original if condition and all else-if clauses evaluate to false, the else block is executed if one was provided.</span></span>

<span data-ttu-id="8f6eb-248">Beachten Sie, dass der ausgeführte Block in seinem eigenen Bereich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-248">Note that whichever block is executed is executed in its own scope.</span></span>
<span data-ttu-id="8f6eb-249">Bindungen, die innerhalb eines then-, else-if-oder Else-Blocks erstellt werden, sind nach dem Ende der if-Anweisung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-249">Bindings made inside of a then, else-if, or else block are not visible after the end of the if statement.</span></span>

<span data-ttu-id="8f6eb-250">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-250">For example,</span></span>

```qsharp
if (result == One) {
    X(target);
} 
```

<span data-ttu-id="8f6eb-251">oder</span><span class="sxs-lookup"><span data-stu-id="8f6eb-251">or</span></span>

```qsharp
if (i == 1) {
    X(target);
} elif (i == 2) {
    Y(target);
} else {
    Z(target);
}
```

### <a name="return"></a><span data-ttu-id="8f6eb-252">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f6eb-252">Return</span></span>

<span data-ttu-id="8f6eb-253">Die Return-Anweisung beendet die Ausführung eines Vorgangs oder einer Funktion und gibt einen Wert an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-253">The return statement ends execution of an operation or function and returns a value to the caller.</span></span>
<span data-ttu-id="8f6eb-254">Er besteht aus dem Schlüsselwort `return`, gefolgt von einem Ausdruck des entsprechenden Typs und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-254">It consists of the keyword `return`, followed by an expression of the appropriate type, and a terminating semicolon.</span></span>

<span data-ttu-id="8f6eb-255">Ein Aufruf bares Element, das ein leeres Tupel zurückgibt, `()`, erfordert keine Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-255">A callable that returns an empty tuple, `()`, does not require a return statement.</span></span>
<span data-ttu-id="8f6eb-256">Wenn eine frühe Beendigung gewünscht ist, können `return ()` in diesem Fall verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-256">If an early exit is desired, `return ()` may be used in this case.</span></span>
<span data-ttu-id="8f6eb-257">Aufruf Bare Elemente, die einen beliebigen anderen Typ zurückgeben, erfordern eine abschließende Return-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-257">Callables that return any other type require a final return statement.</span></span>

<span data-ttu-id="8f6eb-258">Es gibt keine maximale Anzahl von Return-Anweisungen innerhalb eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-258">There is no maximum number of return statements within an operation.</span></span>
<span data-ttu-id="8f6eb-259">Der Compiler gibt möglicherweise eine Warnung aus, wenn Anweisungen einer Return-Anweisung in einem-Block folgen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-259">The compiler may emit a warning if statements follow a return statement within a block.</span></span>

<span data-ttu-id="8f6eb-260">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-260">For example,</span></span>

```qsharp
return 1;
```

<span data-ttu-id="8f6eb-261">oder</span><span class="sxs-lookup"><span data-stu-id="8f6eb-261">or</span></span>

```qsharp
return ();
```

<span data-ttu-id="8f6eb-262">oder</span><span class="sxs-lookup"><span data-stu-id="8f6eb-262">or</span></span>

```qsharp
return (results, qubits);
```

### <a name="fail"></a><span data-ttu-id="8f6eb-263">Fehler</span><span class="sxs-lookup"><span data-stu-id="8f6eb-263">Fail</span></span>

<span data-ttu-id="8f6eb-264">Die Fail-Anweisung beendet die Ausführung eines Vorgangs und gibt einen Fehlerwert an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-264">The fail statement ends execution of an operation and returns an error value to the caller.</span></span>
<span data-ttu-id="8f6eb-265">Er besteht aus dem Schlüsselwort `fail`, gefolgt von einer Zeichenfolge und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-265">It consists of the keyword `fail`, followed by a string and a terminating semicolon.</span></span>
<span data-ttu-id="8f6eb-266">Die Zeichenfolge wird als Fehlermeldung an den klassischen Treiber zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-266">The string is returned to the classical driver as the error message.</span></span>

<span data-ttu-id="8f6eb-267">Es gibt keine Einschränkung für die Anzahl der Fail-Anweisungen innerhalb eines Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-267">There is no restriction on the number of fail statements within an operation.</span></span>
<span data-ttu-id="8f6eb-268">Der Compiler gibt möglicherweise eine Warnung aus, wenn-Anweisungen einer Fail-Anweisung innerhalb eines-Blocks folgen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-268">The compiler may emit a warning if statements follow a fail statement within a block.</span></span>

<span data-ttu-id="8f6eb-269">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-269">For example,</span></span>

```qsharp
fail $"Impossible state reached";
```

<span data-ttu-id="8f6eb-270">oder</span><span class="sxs-lookup"><span data-stu-id="8f6eb-270">or</span></span>

```qsharp
fail $"Syndrome {syn} is incorrect";
```

## <a name="qubit-management"></a><span data-ttu-id="8f6eb-271">Qubit-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="8f6eb-271">Qubit Management</span></span>

<span data-ttu-id="8f6eb-272">Beachten Sie, dass keine dieser Anweisungen innerhalb des Texts einer Funktion zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-272">Note that none of these statements are allowed within the body of a function.</span></span>
<span data-ttu-id="8f6eb-273">Sie sind nur innerhalb von Vorgängen gültig.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-273">They are only valid within operations.</span></span>

### <a name="clean-qubits"></a><span data-ttu-id="8f6eb-274">Löschen von Qubits</span><span class="sxs-lookup"><span data-stu-id="8f6eb-274">Clean Qubits</span></span>

<span data-ttu-id="8f6eb-275">Die `using`-Anweisung wird verwendet, um neue Qubits für die Verwendung während eines-Anweisungsblocks abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-275">The `using` statement is used to acquire new qubits for use during a statement block.</span></span>
<span data-ttu-id="8f6eb-276">Es ist garantiert, dass die Qubits mit dem Berechnungs `Zero` Zustand initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-276">The qubits are guaranteed to be initialized to the computational `Zero` state.</span></span>
<span data-ttu-id="8f6eb-277">Die Qubits sollten sich am Ende des Anweisungsblocks im Status der Berechnungs `Zero` befinden. Simulatoren werden empfohlen, dies zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-277">The qubits should be in the computational `Zero` state at the end of the statement block; simulators are encouraged to enforce this.</span></span>

<span data-ttu-id="8f6eb-278">Die-Anweisung besteht aus dem Schlüsselwort `using`, gefolgt von einer öffnenden Klammer `(`, einer Bindung, einer schließenden Klammer `)`und dem Anweisungsblock, in dem die Qubits verfügbar sein werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-278">The statement consists of the keyword `using`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="8f6eb-279">Die Bindung folgt dem gleichen Muster wie `let`-Anweisungen: entweder ein einzelnes Symbol oder ein Tupel von Symbolen, gefolgt von einem Gleichheitszeichen `=`und entweder ein einzelner Wert oder ein entsprechendes Tupel von Initialisierern.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-279">The binding follows the same pattern as `let` statements: either a single symbol or a tuple of symbols, followed by an equals sign `=`, and either a single value or a matching tuple of initializers.</span></span>
<span data-ttu-id="8f6eb-280">Initialisierer sind entweder für ein einzelnes Qubit, das als `Qubit()`angegeben wird, oder ein Array von Qubits verfügbar, das durch `Qubit[`, einen `Int` Ausdruck und `]`angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-280">Initializers are available either for a single qubit, indicated as `Qubit()`, or an array of qubits, indicated by `Qubit[`, an `Int` expression, and `]`.</span></span>

<span data-ttu-id="8f6eb-281">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-281">For example,</span></span>

```qsharp
using (qubit = Qubit()) {
    // ...
}
using ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

### <a name="borrowed-qubits"></a><span data-ttu-id="8f6eb-282">Geliehene Qubits</span><span class="sxs-lookup"><span data-stu-id="8f6eb-282">Borrowed Qubits</span></span>

<span data-ttu-id="8f6eb-283">Die `borrowing`-Anweisung wird verwendet, um Qubits für die temporäre Verwendung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-283">The `borrowing` statement is used to obtain qubits for temporary use.</span></span> <span data-ttu-id="8f6eb-284">Die-Anweisung besteht aus dem Schlüsselwort `borrowing`, gefolgt von einer öffnenden Klammer `(`, einer Bindung, einer schließenden Klammer `)`und dem Anweisungsblock, in dem die Qubits verfügbar sein werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-284">The statement consists of the keyword `borrowing`, followed by an open parenthesis `(`, a binding, a close parenthesis `)`, and the statement block within which the qubits will be available.</span></span>
<span data-ttu-id="8f6eb-285">Die Bindung folgt demselben Muster und denselben Regeln wie in einer `using`-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-285">The binding follows the same pattern and rules as the one in a `using` statement.</span></span>

<span data-ttu-id="8f6eb-286">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-286">For example,</span></span>

```qsharp
borrowing (qubit = Qubit()) {
    // ...
}
borrowing ((auxiliary, qubits) = (Qubit(), Qubit[bits * 2 + 3])) {
    // ...
}
```

<span data-ttu-id="8f6eb-287">Die geliehenen Qubits befinden sich in einem unbekannten Zustand und verlassen den Gültigkeitsbereich am Ende des Anweisungsblocks.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-287">The borrowed qubits are in an unknown state and go out of scope at the end of the statement block.</span></span>
<span data-ttu-id="8f6eb-288">Der Kreditnehmer führt einen Commit aus, um die Qubits in demselben Zustand zu belassen, in dem Sie sich befanden, d. h., ihr Zustand am Anfang und am Ende des Anweisungsblocks ist erwartungsgemäß identisch.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-288">The borrower commits to leaving the qubits in the same state they were in when they were borrowed, i.e. their state at the beginning and at the end of the statement block is expected to be the same.</span></span>
<span data-ttu-id="8f6eb-289">Dabei handelt es sich nicht unbedingt um einen klassischen Zustand, der in den meisten Fällen keine Messungen enthalten sollte.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-289">This state in particular is not necessarily a classical state, such that in most cases, borrowing scopes should not contain measurements.</span></span> 

<span data-ttu-id="8f6eb-290">Ein Beispiel für eine geliehene Qubit-Verwendung finden [*Sie unter Factoring mithilfe von 2N + 2-Qubits mit Toffoli-basierter Modularität*](https://arxiv.org/abs/1611.07995) (Haner, roetteler und svore 2017).</span><span class="sxs-lookup"><span data-stu-id="8f6eb-290">See [*Factoring using 2n+2 qubits with Toffoli based modular multiplication*](https://arxiv.org/abs/1611.07995) (Haner, Roetteler, and Svore 2017) for an example of borrowed qubit use.</span></span>

<span data-ttu-id="8f6eb-291">Beim Abgleich von Qubits versucht das System zunächst, die Anforderung von Qubits auszufüllen, die verwendet werden, auf die jedoch nicht während des Texts der `borrowing` Anweisung zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-291">When borrowing qubits, the system will first try to fill the request from qubits that are in use but that are not accessed during the body of the `borrowing` statement.</span></span>
<span data-ttu-id="8f6eb-292">Wenn nicht genügend derartige Qubits vorhanden sind, werden neue Qubits zum Durchführen der Anforderung zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-292">If there aren't enough such qubits, then it will allocate new qubits to complete the request.</span></span>

## <a name="conjugations"></a><span data-ttu-id="8f6eb-293">Konjugationen</span><span class="sxs-lookup"><span data-stu-id="8f6eb-293">Conjugations</span></span>

<span data-ttu-id="8f6eb-294">Im Gegensatz zu klassischen Bits ist das Freigeben von Quantum-Speicher etwas komplizierter, da das Blind Zurücksetzen von Qubits unerwünschte Auswirkungen auf die verbleibende Berechnung haben kann, wenn die Qubits noch entkoppelt sind.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-294">In contrast to classical bits, releasing quantum memory is slightly more involved since blindly resetting qubits can have undesired effects on the remaining computation if the qubits are still entangled.</span></span> <span data-ttu-id="8f6eb-295">Dies kann vermieden werden, indem Berechnungen vor der Freigabe des Arbeitsspeichers ordnungsgemäß durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-295">This can be avoided by properly "undoing" performed computations prior to releasing the memory.</span></span> <span data-ttu-id="8f6eb-296">Ein gängiges Muster in Quantum Computing ist daher Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-296">A common pattern in quantum computing is hence the following:</span></span> 

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

<span data-ttu-id="8f6eb-297">: neu: ab unserer Version 0,9 wird eine Konjugations Anweisung unterstützt, die die oben beschriebene Transformation implementiert.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-297">:new: Starting with our 0.9 release, we support a conjugation statement that implements the transformation above.</span></span> <span data-ttu-id="8f6eb-298">Mithilfe dieser Anweisung kann der Vorgang `ApplyWith` folgendermaßen implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-298">Using that statement, the operation `ApplyWith` can be implemented in the following way:</span></span>

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
<span data-ttu-id="8f6eb-299">Eine solche Konjugation-Anweisung wird deutlich nützlicher, wenn die äußere und die innere Transformation nicht als Vorgänge verfügbar sind, sondern eher durch einen Block, der aus mehreren Anweisungen besteht, beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-299">Such a conjugation statement obviously becomes far more useful if the outer and inner transformation are not readily available as operations but are instead more convenient to describe by a block consisting of several statements.</span></span> 

<span data-ttu-id="8f6eb-300">Die umgekehrte Transformation für die-Anweisungen, die im-Block innerhalb von definiert sind, wird automatisch vom Compiler generiert und nach Abschluss von Apply-Block ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-300">The inverse transformation for the statements defined in the within-block is automatically generated by the compiler and executed after the apply-block completes.</span></span> <span data-ttu-id="8f6eb-301">Da alle änderbaren Variablen, die als Teil des Blocks innerhalb von verwendet werden, im Apply-Block nicht wieder hergestellt werden können, ist die generierte Transformation garantiert das Adjoint der Berechnung im within-Block.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-301">Since any mutable variables used as part of the within-block cannot be rebound in the apply-block, the generated transformation is guaranteed to be the adjoint of the computation in the within-block.</span></span> 

## <a name="expression-evaluation-statements"></a><span data-ttu-id="8f6eb-302">Ausdrucks Auswertungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="8f6eb-302">Expression Evaluation Statements</span></span>

<span data-ttu-id="8f6eb-303">Jeder aufrufsausdruck vom Typ "`Unit`" kann als Anweisung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-303">Any call expression of type `Unit` may be used as a statement.</span></span>
<span data-ttu-id="8f6eb-304">Dies wird hauptsächlich beim Aufrufen von Vorgängen für Qubits verwendet, die `Unit` zurückgeben, da der Zweck der Anweisung darin besteht, den impliziten Quantum-Zustand zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-304">This is primarily of use when calling operations on qubits that return `Unit` because the purpose of the statement is to modify the implicit quantum state.</span></span>
<span data-ttu-id="8f6eb-305">Ausdrucks Auswertungs Anweisungen erfordern ein abschließendes Semikolon.</span><span class="sxs-lookup"><span data-stu-id="8f6eb-305">Expression evaluation statements require a terminating semicolon.</span></span>

<span data-ttu-id="8f6eb-306">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8f6eb-306">For example,</span></span>

```qsharp
X(q);
CNOT(control, target);
Adjoint T(q);
```
