---
title: 'F #-Dateistruktur'
description: 'Beschreibt die Struktur und die Syntax einer Q #-Datei.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: b8c24dae6cc8d8f37ad4f1f74017c05cabe3a4b4
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327457"
---
# <a name="q-file-structure"></a><span data-ttu-id="6196e-103">F #-Dateistruktur</span><span class="sxs-lookup"><span data-stu-id="6196e-103">Q# File Structure</span></span>

<span data-ttu-id="6196e-104">Jeder Q #-Vorgang, jede Funktion und jeder benutzerdefinierte Typ wird in einem Namespace definiert.</span><span class="sxs-lookup"><span data-stu-id="6196e-104">Every Q# operation, function, and user-defined type is defined within a namespace.</span></span>

<span data-ttu-id="6196e-105">Eine Q #-Datei besteht aus einer Sequenz von *Namespace Deklarationen*.</span><span class="sxs-lookup"><span data-stu-id="6196e-105">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="6196e-106">Jede Namespace Deklaration enthält Deklarationen für benutzerdefinierte Typen, Vorgänge und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6196e-106">Each namespace declaration contains declarations for user-defined types, operations, and functions.</span></span>
<span data-ttu-id="6196e-107">Eine Namespace Deklaration kann beliebig viele Typen von Deklarationen und in beliebiger Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="6196e-107">A namespace declaration may contain any number of each type of declaration, and in any order.</span></span>
<span data-ttu-id="6196e-108">Befolgen Sie diese Links, um weitere Informationen zum Deklarieren von [benutzerdefinierten Typen](xref:microsoft.quantum.guide.types#user-defined-types), [Vorgängen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)und [Funktionen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) innerhalb eines Namespace zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6196e-108">Follow these links for more details on declaring [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions) within a namespace.</span></span>

<span data-ttu-id="6196e-109">Der einzige Text, der außerhalb einer Namespace Deklaration angezeigt werden kann, sind Kommentare.</span><span class="sxs-lookup"><span data-stu-id="6196e-109">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="6196e-110">Insbesondere Dokumentations Kommentare (weitere Details finden Sie unten) für einen Namespace vor der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="6196e-110">In particular, documentation comments (more details below) for a namespace precede the declaration.</span></span>

## <a name="namespace-declarations"></a><span data-ttu-id="6196e-111">Namespacedeklarationen</span><span class="sxs-lookup"><span data-stu-id="6196e-111">Namespace Declarations</span></span>

<span data-ttu-id="6196e-112">Eine Q #-Datei hat normalerweise genau eine Namespace Deklaration, kann jedoch keine (und leer sein oder nur Kommentare enthalten) oder mehrere Namespaces enthalten.</span><span class="sxs-lookup"><span data-stu-id="6196e-112">A Q# file will typically have exactly one namespace declaration, but may have none (and be empty or just contain comments) or may contain multiple namespaces.</span></span>
<span data-ttu-id="6196e-113">Namespace Deklarationen dürfen nicht eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6196e-113">Namespace declarations may not be nested.</span></span>

<span data-ttu-id="6196e-114">Derselbe Namespace kann in mehreren Q #-Dateien deklariert werden, die zusammen kompiliert werden, solange keine Typen-, Vorgangs-oder Funktions Deklarationen mit demselben Namen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6196e-114">The same namespace may be declared in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="6196e-115">Es ist insbesondere ungültig, denselben Typ im gleichen Namespace in mehreren Dateien zu definieren, auch wenn die Deklarationen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="6196e-115">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="6196e-116">Eine Namespace Deklaration besteht aus dem Schlüsselwort `namespace` , gefolgt vom Namen des Namespace, einer offenen geschweifter Klammer `{` , den im Namespace enthaltenen Deklarationen und einer schließenden geschweifter Klammer `}` .</span><span class="sxs-lookup"><span data-stu-id="6196e-116">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, an open brace `{`, the declarations contained in the namespace, and a close brace `}`.</span></span>
<span data-ttu-id="6196e-117">Namespace Namen folgen dem .net-Muster einer Sequenz von mindestens einem zulässigen Symbol, das durch Zeiträume getrennt ist `.` .</span><span class="sxs-lookup"><span data-stu-id="6196e-117">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="6196e-118">Beispielsweise `MyQuantumStuff` sind und `Microsoft.Quantum.Intrinsic` gültige Namespace Namen.</span><span class="sxs-lookup"><span data-stu-id="6196e-118">For instance, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="6196e-119">Gemäß der Konvention werden die Symbole in einem Namespace Namen groß geschrieben, dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6196e-119">By convention, the symbols in a namespace name are capitalized, but this is not required.</span></span>

<span data-ttu-id="6196e-120">Verweise auf Typen oder Aufruf Bare Dateien, die in einer Datei weiter unten deklariert sind, werden ordnungsgemäß aufgelöst. Es ist nicht erforderlich, dass der Typ, der Vorgang oder die Funktionsdeklaration einem Verweis darauf vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6196e-120">References to types or callables declared further down in a file are resolved properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="6196e-121">Open-Direktiven</span><span class="sxs-lookup"><span data-stu-id="6196e-121">Open Directives</span></span>

<span data-ttu-id="6196e-122">Innerhalb eines Namespace Blocks kann die- `open` Direktive verwendet werden, um alle Typen und callables zu importieren, die in einem bestimmten Namespace deklariert sind, und auf diese mit dem nicht qualifizierten Namen zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6196e-122">Within a namespace block, the `open` directive may be used to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="6196e-123">Eine solche `open` Direktive besteht aus dem `open` Schlüsselwort, gefolgt vom zu öffnenden Namespace und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="6196e-123">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="6196e-124">Alle- `open` Direktiven müssen vor allen- `function` ,-oder- `operation` `newtype` Deklarationen im-Namespace Block angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6196e-124">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="6196e-125">Optional kann ein Kurzname für den geöffneten Namespace definiert werden, sodass alle Elemente aus diesem Namespace durch den definierten Kurznamen qualifiziert werden können (und müssen).</span><span class="sxs-lookup"><span data-stu-id="6196e-125">Optionally, a short name for the opened namespace may be defined such that all elements from that namespace can (and need) to be qualified by the defined short name.</span></span> <span data-ttu-id="6196e-126">Wenn z. b. die folgende Namespace Deklaration und Open-Direktiven angegeben sind,</span><span class="sxs-lookup"><span data-stu-id="6196e-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="6196e-127">Wenn ein von uns deklarierte Vorgang einen Vorgang `Op` aus verwendet `Microsoft.Quantum.Intrinsic` , wird er durch einfaches Verwenden von aufgerufen `Op` .</span><span class="sxs-lookup"><span data-stu-id="6196e-127">if an operation we declare uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, we would call it by simply using `Op`.</span></span>
<span data-ttu-id="6196e-128">Wenn jedoch eine bestimmte Funktion `Fn` von aufgerufen `Microsoft.Quantum.Math` werden soll, muss Sie mit aufgerufen werden `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="6196e-128">However, if we wanted a call a certain function `Fn` from `Microsoft.Quantum.Math`, we would need to call it using `Math.Fn`.</span></span>

<span data-ttu-id="6196e-129">Die- `open` Direktive gilt für den gesamten Namespace Block in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="6196e-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="6196e-130">Wenn wir also einen zusätzlichen Namespace in der gleichen Q #-Datei wie oben definieren würden `NS` , hätten alle im zweiten Namespace definierten Vorgänge/Funktionen/Typen keinen Zugriff auf etwas von `Microsoft.Quantum.Intrinsic` oder, `Microsoft.Quantum.Math` es sei denn, wir haben die Open-Direktiven darin wiederholt.</span><span class="sxs-lookup"><span data-stu-id="6196e-130">Hence, if we were to define an additional namespace in the same Q# file as `NS` above, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless we repeated the open directives therein.</span></span> 

<span data-ttu-id="6196e-131">Auf einen Typ oder Aufruf baren Wert, der in einem anderen Namespace definiert ist, der *nicht* im aktuellen Namespace geöffnet ist, muss mit seinem voll qualifizierten Namen darauf verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="6196e-131">A type or callable defined in another namespace that is *not* opened in the current namespace must be referenced by its fully-qualified name.</span></span>
<span data-ttu-id="6196e-132">Beispielsweise muss auf einen Vorgang `Op` mit dem Namen aus dem- `X.Y` Namespace durch seinen voll qualifizierten Namen verwiesen werden `X.Y.Op` , es sei denn, der `X.Y` Namespace wurde zuvor im aktuellen Block geöffnet.</span><span class="sxs-lookup"><span data-stu-id="6196e-132">For example, an operation named `Op` from the `X.Y` namespace must be referenced by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> <span data-ttu-id="6196e-133">Wie bereits erwähnt, `X` ist es nicht möglich, auf den Vorgang als zu verweisen, auch wenn der Namespace geöffnet wurde `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="6196e-133">As mentioned above, even if the `X` namespace has been opened, it is not possible to reference the operation as `Y.Op`.</span></span>
<span data-ttu-id="6196e-134">Wenn ein Kurzname `Z` für `X.Y` in diesem Namespace und in der Datei definiert wurde, `Op` muss als bezeichnet werden `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="6196e-134">If a short name `Z` for `X.Y` has been defined in that namespace and file, then `Op` needs to be referred to as `Z.Op`.</span></span> 

<span data-ttu-id="6196e-135">Es ist in der Regel besser, einen Namespace mit einer- `open` Direktive einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="6196e-135">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="6196e-136">Die Verwendung eines voll qualifizierten Namens ist erforderlich, wenn zwei Namespaces Konstrukte mit dem gleichen Namen definieren und die aktuelle Quelle Konstrukte aus beidem verwendet.</span><span class="sxs-lookup"><span data-stu-id="6196e-136">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="6196e-137">F # befolgt die gleichen Regeln für die Benennung wie andere .NET-Sprachen.</span><span class="sxs-lookup"><span data-stu-id="6196e-137">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="6196e-138">F # unterstützt jedoch keine relativen Verweise auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="6196e-138">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="6196e-139">Das heißt, wenn der Namespace `a.b` geöffnet wurde, wird ein Verweis auf einen Vorgang mit dem Namen `c.d` *nicht* in einen Vorgang mit dem vollständigen Namen aufgelöst `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="6196e-139">That is, if the namespace `a.b` has been opened, a reference to an operation named `c.d` will *not* be resolved to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="6196e-140">Formatierung</span><span class="sxs-lookup"><span data-stu-id="6196e-140">Formatting</span></span>

<span data-ttu-id="6196e-141">Die meisten Q #-Anweisungen und-Direktiven enden mit einem abschließenden Semikolon, `;` .</span><span class="sxs-lookup"><span data-stu-id="6196e-141">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="6196e-142">-Anweisungen und-Deklarationen, wie z. b. `for` und `operation` , die mit einem Anweisungsblock enden (siehe unten), erfordern kein abschließendes Semikolon</span><span class="sxs-lookup"><span data-stu-id="6196e-142">Statements and declarations such as `for` and `operation` that end with a statement block (see below) do not require a terminating semicolon.</span></span>
<span data-ttu-id="6196e-143">Jede Anweisungs Beschreibung gibt an, ob das abschließende Semikolon erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6196e-143">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="6196e-144">Anweisungen, wie Ausdrücke, Deklarationen und Direktiven, werden möglicherweise über mehrere Zeilen hinweg aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="6196e-144">Statements, like expressions, declarations, and directives, may be broken out across multiple lines.</span></span>
<span data-ttu-id="6196e-145">Das vorhanden sein mehrerer Anweisungen in einer einzelnen Zeile sollte vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="6196e-145">Having multiple statements on a single line should be avoided.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="6196e-146">Anweisungsblöcke</span><span class="sxs-lookup"><span data-stu-id="6196e-146">Statement Blocks</span></span>

<span data-ttu-id="6196e-147">Q #-Anweisungen werden in Anweisungsblöcke gruppiert.</span><span class="sxs-lookup"><span data-stu-id="6196e-147">Q# statements are grouped into statement blocks.</span></span>
<span data-ttu-id="6196e-148">Ein Anweisungsblock beginnt mit einem öffnenden `{` und endet mit einem schließenden `}` .</span><span class="sxs-lookup"><span data-stu-id="6196e-148">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="6196e-149">Ein Anweisungsblock, der lexikalisch in einem anderen-Block eingeschlossen ist, wird als Teil Block des enthaltenden Blocks angesehen; enthaltende-und-Unterblöcke werden auch als äußere und innere Blöcke bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="6196e-149">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="6196e-150">Kommentare</span><span class="sxs-lookup"><span data-stu-id="6196e-150">Comments</span></span>

<span data-ttu-id="6196e-151">Kommentare beginnen mit zwei Schrägstrichen, `//` und werden bis zum Zeilenende fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="6196e-151">Comments begin with two forward slashes, `//`, and continue until the end of line.</span></span>
<span data-ttu-id="6196e-152">Ein Kommentar kann an beliebiger Stelle in einer f #-Quelldatei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6196e-152">A comment may appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="6196e-153">Dokumentationskommentare</span><span class="sxs-lookup"><span data-stu-id="6196e-153">Documentation Comments</span></span>

<span data-ttu-id="6196e-154">Kommentare, die mit drei Schrägstrichen beginnen, `///` werden vom Compiler speziell behandelt, wenn Sie unmittelbar vor einem Namespace, einem Vorgang, einer Spezialisierung, einer Funktion oder einer Typdefinition erscheinen.</span><span class="sxs-lookup"><span data-stu-id="6196e-154">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="6196e-155">In diesem Fall wird der Inhalt als Dokumentation für den definierten Aufruf baren oder benutzerdefinierten Typ, wie für andere .NET-Sprachen, übernommen.</span><span class="sxs-lookup"><span data-stu-id="6196e-155">In that case, their contents are taken as documentation for the defined callable or user-defined type, as for other .NET languages.</span></span>

<span data-ttu-id="6196e-156">Innerhalb von `///` Kommentaren wird Text, der als Teil der API-Dokumentation angezeigt wird, als [markdown](https://daringfireball.net/projects/markdown/syntax)formatiert, wobei verschiedene Teile der Dokumentation durch speziell benannte Header angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6196e-156">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation being indicated by specially-named headers.</span></span>
<span data-ttu-id="6196e-157">Als Erweiterung von markdown können Querverweise auf Vorgänge, Funktionen und benutzerdefinierte Typen in Q # mithilfe von eingeschlossen werden `@"<ref target>"` `<ref target>` . dabei wird durch den voll qualifizierten Namen des Code Objekts ersetzt, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6196e-157">As an extension to Markdown, cross references to operations, functions and user-defined types in Q# can be included using the `@"<ref target>"`, where `<ref target>` is replaced by the fully qualified name of the code object being referenced.</span></span>
<span data-ttu-id="6196e-158">Optional kann eine Dokumentations-Engine auch zusätzliche markdownerweiterungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6196e-158">Optionally, a documentation engine may also support additional Markdown extensions.</span></span>

<span data-ttu-id="6196e-159">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6196e-159">For example:</span></span>

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

<span data-ttu-id="6196e-160">Die folgenden Namen werden als Dokumentations Kommentar Header erkannt.</span><span class="sxs-lookup"><span data-stu-id="6196e-160">The following names are recognized as documentation comment headers.</span></span>

- <span data-ttu-id="6196e-161">**Zusammenfassung**: eine kurze Zusammenfassung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs.</span><span class="sxs-lookup"><span data-stu-id="6196e-161">**Summary**: A short summary of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="6196e-162">Der erste Absatz der Zusammenfassung wird für Hover-Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="6196e-162">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="6196e-163">Es sollte nur Text sein.</span><span class="sxs-lookup"><span data-stu-id="6196e-163">It should be plain text.</span></span>
- <span data-ttu-id="6196e-164">**Beschreibung**: eine Beschreibung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs.</span><span class="sxs-lookup"><span data-stu-id="6196e-164">**Description**: A description of the behavior of a function or operation, or of the purpose of a type.</span></span> <span data-ttu-id="6196e-165">Die Zusammenfassung und Beschreibung werden verkettet, um die generierte Dokumentations Datei für die Funktion, den Vorgang oder den Typ zu bilden.</span><span class="sxs-lookup"><span data-stu-id="6196e-165">The summary and description are concatenated to form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="6196e-166">Die Beschreibung enthält möglicherweise in-line-Symbole und-Gleichungen in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="6196e-166">The description may contain in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="6196e-167">**Input**: eine Beschreibung des eingabetupels für einen Vorgang oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="6196e-167">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="6196e-168">Kann zusätzliche markdown-Unterabschnitte enthalten, die jedes einzelne Element des eingabetupels angeben.</span><span class="sxs-lookup"><span data-stu-id="6196e-168">May contain additional Markdown subsections indicating each individual element of the input tuple.</span></span>
- <span data-ttu-id="6196e-169">**Output**: eine Beschreibung des Tupels, das von einem Vorgang oder einer Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6196e-169">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="6196e-170">**Typparameter**: ein leerer Abschnitt, der einen zusätzlichen unter Abschnitt für jeden generischen Typparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="6196e-170">**Type Parameters**: An empty section which contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="6196e-171">**Beispiel**: ein kurzes Beispiel für den Vorgang, die Funktion oder den Typ, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6196e-171">**Example**: A short example of the operation, function or type in use.</span></span>
- <span data-ttu-id="6196e-172">**Hinweise**: verschiedene Prosa, die einen Aspekt des Vorgangs, der Funktion oder des Typs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="6196e-172">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="6196e-173">**Siehe auch**: eine Liste der voll qualifizierten Namen, die verwandte Funktionen, Vorgänge oder benutzerdefinierte Typen angeben.</span><span class="sxs-lookup"><span data-stu-id="6196e-173">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="6196e-174">**Verweise**: eine Liste von verweisen und citationen für das Element, das dokumentiert wird.</span><span class="sxs-lookup"><span data-stu-id="6196e-174">**References**: A list of references and citations for the item being documented.</span></span>

## <a name="next-steps"></a><span data-ttu-id="6196e-175">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="6196e-175">Next steps</span></span>

<span data-ttu-id="6196e-176">Weitere Informationen zu [Vorgängen und Funktionen](xref:microsoft.quantum.guide.operationsfunctions) in f #.</span><span class="sxs-lookup"><span data-stu-id="6196e-176">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>