---
title: 'F #-Dateistruktur'
description: 'Beschreibt die Struktur und die Syntax einer Q #-Datei.'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide.filestructure
ms.openlocfilehash: 54efc2b9d6b7f1956cdf9a335c88620b29f7729d
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884178"
---
# <a name="q-file-structure"></a><span data-ttu-id="29363-103">F #-Dateistruktur</span><span class="sxs-lookup"><span data-stu-id="29363-103">Q# File Structure</span></span>

<span data-ttu-id="29363-104">Eine Q #-Datei besteht aus einer Sequenz von *Namespace Deklarationen*.</span><span class="sxs-lookup"><span data-stu-id="29363-104">A Q# file consists of a sequence of *namespace declarations*.</span></span>
<span data-ttu-id="29363-105">Jede Namespace Deklaration enthält Deklarationen für benutzerdefinierte Typen, Vorgänge und Funktionen und kann jede beliebige Anzahl von Deklarationen und in beliebiger Reihenfolge enthalten.</span><span class="sxs-lookup"><span data-stu-id="29363-105">Each namespace declaration contains declarations for user-defined types, operations, and functions, and can contain any number of each type of declaration and in any order.</span></span>
<span data-ttu-id="29363-106">Weitere Informationen zu Deklarationen in einem Namespace finden Sie unter [benutzerdefinierte Typen](xref:microsoft.quantum.guide.types#user-defined-types), [Vorgänge](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations)und [Funktionen](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span><span class="sxs-lookup"><span data-stu-id="29363-106">For more information on declarations within a namespace, see [user-defined types](xref:microsoft.quantum.guide.types#user-defined-types), [operations](xref:microsoft.quantum.guide.operationsfunctions#defining-new-operations), and [functions](xref:microsoft.quantum.guide.operationsfunctions#defining-new-functions).</span></span>

<span data-ttu-id="29363-107">Der einzige Text, der außerhalb einer Namespace Deklaration angezeigt werden kann, sind Kommentare.</span><span class="sxs-lookup"><span data-stu-id="29363-107">The only text that can appear outside of a namespace declaration is comments.</span></span>
<span data-ttu-id="29363-108">Insbesondere Dokumentations Kommentare für einen Namespace vor der Deklaration.</span><span class="sxs-lookup"><span data-stu-id="29363-108">In particular, documentation comments for a namespace precede the declaration.</span></span> <span data-ttu-id="29363-109">Weitere Informationen finden Sie in den [Dokumentations Kommentaren](#documentation-comments) in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="29363-109">For more information, see [Documentation comments](#documentation-comments) in this article.</span></span> 

## <a name="namespace-declarations"></a><span data-ttu-id="29363-110">Namespacedeklarationen</span><span class="sxs-lookup"><span data-stu-id="29363-110">Namespace Declarations</span></span>

<span data-ttu-id="29363-111">Eine Q #-Datei besitzt in der Regel nur eine Namespace Deklaration, kann jedoch keine (und leer sein oder nur Kommentare enthalten) oder mehrere Namespaces enthalten.</span><span class="sxs-lookup"><span data-stu-id="29363-111">A Q# file typically has just one namespace declaration, but could have none (and be empty or just contain comments) or could contain multiple namespaces.</span></span>
<span data-ttu-id="29363-112">Namespace Deklarationen können nicht eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="29363-112">Namespace declarations can not be nested.</span></span>

<span data-ttu-id="29363-113">In mehreren Q #-Dateien, die zusammen kompiliert werden, können Sie denselben Namespace deklarieren, solange keine Typen-, Vorgangs-oder Funktions Deklarationen mit demselben Namen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="29363-113">You can declare the same namespace in multiple Q# files that are compiled together, as long as there are no type, operation, or function declarations with the same name.</span></span>
<span data-ttu-id="29363-114">Es ist insbesondere ungültig, denselben Typ im gleichen Namespace in mehreren Dateien zu definieren, auch wenn die Deklarationen identisch sind.</span><span class="sxs-lookup"><span data-stu-id="29363-114">In particular, it is invalid to define the same type in the same namespace in multiple files, even if the declarations are identical.</span></span>

<span data-ttu-id="29363-115">Eine Namespace Deklaration besteht aus dem Schlüsselwort `namespace` , gefolgt vom Namen des Namespace und den Deklarationen im Namespace, die in geschweifte Klammern eingeschlossen sind `{ }` .</span><span class="sxs-lookup"><span data-stu-id="29363-115">A namespace declaration consists of the keyword `namespace`, followed by the name of the namespace, and the declarations contained in the namespace enclosed in braces `{ }`.</span></span>
<span data-ttu-id="29363-116">Namespace Namen folgen dem .net-Muster einer Sequenz von mindestens einem zulässigen Symbol, das durch Zeiträume getrennt ist `.` .</span><span class="sxs-lookup"><span data-stu-id="29363-116">Namespace names follow the .NET pattern of a sequence of one or more legal symbols separated by periods `.`.</span></span>
<span data-ttu-id="29363-117">Beispielsweise `MyQuantumStuff` sind und `Microsoft.Quantum.Intrinsic` gültige Namespace Namen.</span><span class="sxs-lookup"><span data-stu-id="29363-117">For example, `MyQuantumStuff` and `Microsoft.Quantum.Intrinsic` are valid namespace names.</span></span>
<span data-ttu-id="29363-118">Gemäß der Konvention werden die Symbole in einem Namespace Namen groß geschrieben, dies ist jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="29363-118">By convention, capitalize the symbols in a namespace name, however, this is not required.</span></span>

<span data-ttu-id="29363-119">Verweise auf Typen oder Aufruf Bare Elemente, die weiter unten in einer Datei deklariert sind, werden ordnungsgemäß aufgelöst. Es ist nicht erforderlich, dass der Typ, der Vorgang oder die Funktionsdeklaration einem Verweis darauf vorangestellt wird.</span><span class="sxs-lookup"><span data-stu-id="29363-119">References to types or callables declared further down in a file resolve properly; there is no need for the type, operation, or function declaration to precede a reference to it.</span></span>

## <a name="open-directives"></a><span data-ttu-id="29363-120">Open-Direktiven</span><span class="sxs-lookup"><span data-stu-id="29363-120">Open Directives</span></span>

<span data-ttu-id="29363-121">Verwenden Sie in einem Namespace Block die- `open` Direktive, um alle Typen und callables zu importieren, die in einem bestimmten Namespace deklariert sind, und verweisen Sie anhand ihres nicht qualifizierten Namens darauf.</span><span class="sxs-lookup"><span data-stu-id="29363-121">Within a namespace block, use the `open` directive to import all types and callables declared in a certain namespace and refer to them by their unqualified name.</span></span>
<span data-ttu-id="29363-122">Eine solche `open` Direktive besteht aus dem `open` Schlüsselwort, gefolgt vom zu öffnenden Namespace und einem abschließenden Semikolon.</span><span class="sxs-lookup"><span data-stu-id="29363-122">Such an `open` directive consists of the `open` keyword, followed by the namespace to be opened and a terminating semicolon.</span></span>

> [!NOTE] 
> <span data-ttu-id="29363-123">Alle- `open` Direktiven müssen vor allen- `function` ,-oder- `operation` `newtype` Deklarationen im-Namespace Block angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="29363-123">All `open` directives must appear before any `function`, `operation`, or `newtype` declarations in the namespace block.</span></span>

<span data-ttu-id="29363-124">Optional können Sie einen Kurznamen für den geöffneten Namespace definieren.</span><span class="sxs-lookup"><span data-stu-id="29363-124">Optionally, you can define a short name for the opened namespace.</span></span> <span data-ttu-id="29363-125">Wenn ein Kurzname definiert ist, müssen Sie alle Elemente aus diesem Namespace mit dem definierten Kurznamen qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="29363-125">If a short name is defined, you must qualify all elements from that namespace by the defined short name.</span></span> <span data-ttu-id="29363-126">Wenn z. b. die folgende Namespace Deklaration und Open-Direktiven angegeben sind,</span><span class="sxs-lookup"><span data-stu-id="29363-126">For example, given the following namespace declaration and open directives,</span></span>

```qsharp
namespace NS {
    open Microsoft.Quantum.Intrinsic; // opens the namespace
    open Microsoft.Quantum.Math as Math; // defines a short name for the namespace

    // operation, function, and newtype declarations

}
```

<span data-ttu-id="29363-127">Wenn ein deklarierter Vorgang einen Vorgang `Op` aus verwendet `Microsoft.Quantum.Intrinsic` , wird er durch einfaches Verwenden von aufgerufen `Op` .</span><span class="sxs-lookup"><span data-stu-id="29363-127">if a declared operation uses an operation `Op` from `Microsoft.Quantum.Intrinsic`, you call it by simply using `Op`.</span></span>
<span data-ttu-id="29363-128">Um jedoch eine bestimmte Funktion `Fn` von aufzurufen `Microsoft.Quantum.Math` , müssen Sie Sie mithilfe von aufzurufen `Math.Fn` .</span><span class="sxs-lookup"><span data-stu-id="29363-128">However, to call a certain function `Fn` from `Microsoft.Quantum.Math`, you must call it using `Math.Fn`.</span></span>

<span data-ttu-id="29363-129">Die- `open` Direktive gilt für den gesamten Namespace Block in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="29363-129">The `open` directive applies to the entire namespace block within a file.</span></span>
<span data-ttu-id="29363-130">Wenn Sie also einen zusätzlichen Namespace in derselben Q #-Datei wie zuvor definieren `NS` , haben alle im zweiten Namespace definierten Vorgänge/Funktionen/Typen keinen Zugriff auf etwas von `Microsoft.Quantum.Intrinsic` oder, `Microsoft.Quantum.Math` es sei denn, Sie haben die Open-Direktiven darin wiederholt.</span><span class="sxs-lookup"><span data-stu-id="29363-130">Hence, if you define an additional namespace in the same Q# file as `NS` earlier, then any operations/functions/types defined in the second namespace would not have access to anything from `Microsoft.Quantum.Intrinsic` or `Microsoft.Quantum.Math` unless you repeated the open directives therein.</span></span> 

<span data-ttu-id="29363-131">Um auf einen Typ oder Aufruf baren Wert zu verweisen, der in einem anderen Namespace definiert ist, der *nicht* im aktuellen Namespace geöffnet ist, müssen Sie ihn mit seinem voll qualifizierten Namen referenzieren.</span><span class="sxs-lookup"><span data-stu-id="29363-131">To reference a type or callable defined in another namespace that is *not* opened in the current namespace, you must reference it by its fully-qualified name.</span></span>
<span data-ttu-id="29363-132">Angenommen, Sie verfügen über einen Vorgang mit `Op` dem Namen aus dem- `X.Y` Namespace:</span><span class="sxs-lookup"><span data-stu-id="29363-132">For example, given an operation named `Op` from the `X.Y` namespace:</span></span>

* <span data-ttu-id="29363-133">Sie müssen mit dem voll qualifizierten Namen referenzieren `X.Y.Op` , es sei denn, der `X.Y` Namespace wurde zuvor im aktuellen Block geöffnet.</span><span class="sxs-lookup"><span data-stu-id="29363-133">You must reference it by its fully-qualified name `X.Y.Op`, unless the `X.Y` namespace has been opened earlier in the current block.</span></span> 
* <span data-ttu-id="29363-134">Auch wenn der `X` Namespace geöffnet ist, ist es nicht möglich, auf den Vorgang als zu verweisen `Y.Op` .</span><span class="sxs-lookup"><span data-stu-id="29363-134">Even if the `X` namespace is opened, it is not possible to reference the operation as `Y.Op`.</span></span>
* <span data-ttu-id="29363-135">Wenn Sie den Kurznamen `Z` für `X.Y` in diesem Namespace und dieser Datei definiert haben, müssen Sie auf `Op` als verweisen `Z.Op` .</span><span class="sxs-lookup"><span data-stu-id="29363-135">If you defined the short name `Z` for `X.Y` in that namespace and file, you must reference `Op` as `Z.Op`.</span></span> 

<span data-ttu-id="29363-136">Es ist in der Regel besser, einen Namespace mit einer- `open` Direktive einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="29363-136">It is usually better to include a namespace by using an `open` directive.</span></span>
<span data-ttu-id="29363-137">Die Verwendung eines voll qualifizierten Namens ist erforderlich, wenn zwei Namespaces Konstrukte mit dem gleichen Namen definieren und die aktuelle Quelle Konstrukte aus beidem verwendet.</span><span class="sxs-lookup"><span data-stu-id="29363-137">Using a fully-qualified name is required if two namespaces define constructs with the same name, and the current source uses constructs from both.</span></span>

<span data-ttu-id="29363-138">F # befolgt die gleichen Regeln für die Benennung wie andere .NET-Sprachen.</span><span class="sxs-lookup"><span data-stu-id="29363-138">Q# follows the same rules for naming as other .NET languages.</span></span>
<span data-ttu-id="29363-139">F # unterstützt jedoch keine relativen Verweise auf Namespaces.</span><span class="sxs-lookup"><span data-stu-id="29363-139">However, Q# does not support relative references to namespaces.</span></span>
<span data-ttu-id="29363-140">Wenn der Namespace beispielsweise `a.b` geöffnet ist, wird ein Verweis auf einen Vorgang mit dem Namen `c.d` *nicht* in einen Vorgang mit dem vollständigen Namen aufgelöst `a.b.c.d` .</span><span class="sxs-lookup"><span data-stu-id="29363-140">For example, if the namespace `a.b` is open, a reference to an operation named `c.d` does *not* resolve to an operation with full name `a.b.c.d`.</span></span>

## <a name="formatting"></a><span data-ttu-id="29363-141">Formatierung</span><span class="sxs-lookup"><span data-stu-id="29363-141">Formatting</span></span>

<span data-ttu-id="29363-142">Die meisten Q #-Anweisungen und-Direktiven enden mit einem abschließenden Semikolon, `;` .</span><span class="sxs-lookup"><span data-stu-id="29363-142">Most Q# statements and directives end with a terminating semicolon, `;`.</span></span>
<span data-ttu-id="29363-143">-Anweisungen und-Deklarationen, wie z. b. `for` und `operation` , die mit einem Anweisungsblock enden (siehe folgender Abschnitt), erfordern kein abschließendes Semikolon.</span><span class="sxs-lookup"><span data-stu-id="29363-143">Statements and declarations such as `for` and `operation` that end with a statement block (see the following section) do not require a terminating semicolon.</span></span>
<span data-ttu-id="29363-144">Jede Anweisungs Beschreibung gibt an, ob das abschließende Semikolon erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="29363-144">Each statement description notes whether the terminating semicolon is required.</span></span>

<span data-ttu-id="29363-145">Anweisungen, wie Ausdrücke, Deklarationen und Direktiven, können über mehrere Zeilen hinweg aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="29363-145">Statements, like expressions, declarations, and directives, can be broken out across multiple lines.</span></span>
<span data-ttu-id="29363-146">Vermeiden Sie es, mehrere Anweisungen in einer einzelnen Zeile zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="29363-146">Avoid putting multiple statements on a single line.</span></span>

## <a name="statement-blocks"></a><span data-ttu-id="29363-147">Anweisungsblöcke</span><span class="sxs-lookup"><span data-stu-id="29363-147">Statement Blocks</span></span>

<span data-ttu-id="29363-148">Q #-Anweisungen werden in Anweisungsblöcke gruppiert, die in geschweiften Klammern eingeschlossen sind `{ }` .</span><span class="sxs-lookup"><span data-stu-id="29363-148">Q# statements are grouped into statement blocks, which are contained with braces `{ }`.</span></span> <span data-ttu-id="29363-149">Ein Anweisungsblock beginnt mit einem öffnenden `{` und endet mit einem schließenden `}` .</span><span class="sxs-lookup"><span data-stu-id="29363-149">A statement block starts with an opening `{` and ends with a closing `}`.</span></span>

<span data-ttu-id="29363-150">Ein Anweisungsblock, der lexikalisch in einem anderen-Block eingeschlossen ist, wird als Teil Block des enthaltenden Blocks angesehen; enthaltende-und-Unterblöcke werden auch als äußere und innere Blöcke bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="29363-150">A statement block that is lexically enclosed within another block is considered to be a sub-block of the containing block; containing and sub-blocks are also called outer and inner blocks.</span></span>

## <a name="comments"></a><span data-ttu-id="29363-151">Kommentare</span><span class="sxs-lookup"><span data-stu-id="29363-151">Comments</span></span>

<span data-ttu-id="29363-152">Kommentare beginnen mit zwei Schrägstrichen, `//` und werden bis zum Ende der Zeile fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="29363-152">Comments begin with two forward slashes, `//`, and continue until the end of the line.</span></span>
<span data-ttu-id="29363-153">Ein Kommentar kann an beliebiger Stelle in einer Q #-Quelldatei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="29363-153">A comment can appear anywhere in a Q# source file.</span></span>

## <a name="documentation-comments"></a><span data-ttu-id="29363-154">Dokumentationskommentare</span><span class="sxs-lookup"><span data-stu-id="29363-154">Documentation Comments</span></span>

<span data-ttu-id="29363-155">Kommentare, die mit drei Schrägstrichen beginnen, `///` werden vom Compiler speziell behandelt, wenn Sie unmittelbar vor einem Namespace, einem Vorgang, einer Spezialisierung, einer Funktion oder einer Typdefinition erscheinen.</span><span class="sxs-lookup"><span data-stu-id="29363-155">Comments that begin with three forward slashes, `///`, are treated specially by the compiler when they appear immediately before a namespace, operation, specialization, function, or type definition.</span></span>
<span data-ttu-id="29363-156">In diesem Fall behandelt der Compiler Sie als Dokumentation für den definierten Aufruf baren oder benutzerdefinierten Typ, der mit anderen .NET-Sprachen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="29363-156">In that case, the compiler treats them as documentation for the defined callable or user-defined type, the same as other .NET languages.</span></span>

<span data-ttu-id="29363-157">Innerhalb von `///` Kommentaren wird Text, der als Teil der API-Dokumentation angezeigt wird, als [markdown](https://daringfireball.net/projects/markdown/syntax)formatiert, wobei verschiedene Teile der Dokumentation durch speziell benannte Header angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="29363-157">Within `///` comments, text to appear as a part of API documentation is formatted as [Markdown](https://daringfireball.net/projects/markdown/syntax), with different parts of the documentation indicated by specially-named headers.</span></span>
<span data-ttu-id="29363-158">Verwenden Sie in markdown die `@"<ref target>"` Erweiterung für Querverweise auf Vorgänge, Funktionen und benutzerdefinierte Typen in f #.</span><span class="sxs-lookup"><span data-stu-id="29363-158">In Markdown, use the `@"<ref target>"` extension to cross-reference operations, functions, and user-defined types in Q#.</span></span> <span data-ttu-id="29363-159">Ersetzen Sie dies `<ref target>` durch den voll qualifizierten Namen des Code Objekts, auf das verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="29363-159">Replace `<ref target>` with the fully qualified name of the referenced code object.</span></span>
<span data-ttu-id="29363-160">Unterschiedliche Dokumentations-Engines unterstützen möglicherweise zusätzliche markdownerweiterungen.</span><span class="sxs-lookup"><span data-stu-id="29363-160">Different documentation engines may also support additional Markdown extensions.</span></span>

<span data-ttu-id="29363-161">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="29363-161">For example:</span></span>

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

<span data-ttu-id="29363-162">Die folgenden Namen sind als Dokumentations Kommentar Header gültig.</span><span class="sxs-lookup"><span data-stu-id="29363-162">The following names are valid as documentation comment headers.</span></span>

- <span data-ttu-id="29363-163">**Zusammenfassung**: eine kurze Zusammenfassung des Verhaltens einer Funktion oder eines Vorgangs oder des Zwecks eines Typs.</span><span class="sxs-lookup"><span data-stu-id="29363-163">**Summary**: A short summary of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="29363-164">Der erste Absatz der Zusammenfassung wird für Hover-Informationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="29363-164">The first paragraph of the summary is used for hover information.</span></span> <span data-ttu-id="29363-165">Es sollte nur Text sein.</span><span class="sxs-lookup"><span data-stu-id="29363-165">It should be plain text.</span></span>
- <span data-ttu-id="29363-166">**Beschreibung**: eine Beschreibung des Verhaltens einer Funktion oder eines Vorgangs oder der Zweck eines Typs.</span><span class="sxs-lookup"><span data-stu-id="29363-166">**Description**: A description of the behavior of a function or operation, or the purpose of a type.</span></span> <span data-ttu-id="29363-167">Zusammenfassung und Beschreibung bilden die generierte Dokumentations Datei für die Funktion, den Vorgang oder den Typ.</span><span class="sxs-lookup"><span data-stu-id="29363-167">Together, the summary and description form the generated documentation file for the function, operation, or type.</span></span>
  <span data-ttu-id="29363-168">Die Beschreibung unterstützt die in-line-Symbole und-Gleichungen, die in-line-</span><span class="sxs-lookup"><span data-stu-id="29363-168">The description supports in-line LaTeX-formatted symbols and equations.</span></span>
- <span data-ttu-id="29363-169">**Input**: eine Beschreibung des eingabetupels für einen Vorgang oder eine Funktion.</span><span class="sxs-lookup"><span data-stu-id="29363-169">**Input**: A description of the input tuple for an operation or function.</span></span>
  <span data-ttu-id="29363-170">Kann zusätzliche markdown-Unterabschnitte enthalten, die jedes Element des eingabetupels angeben.</span><span class="sxs-lookup"><span data-stu-id="29363-170">Can contain additional Markdown subsections indicating each element of the input tuple.</span></span>
- <span data-ttu-id="29363-171">**Output**: eine Beschreibung des Tupels, das von einem Vorgang oder einer Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="29363-171">**Output**: A description of the tuple returned by an operation or function.</span></span>
- <span data-ttu-id="29363-172">**Typparameter**: ein leerer Abschnitt, der einen zusätzlichen unter Abschnitt für jeden generischen Typparameter enthält.</span><span class="sxs-lookup"><span data-stu-id="29363-172">**Type Parameters**: An empty section that contains one additional subsection for each generic type parameter.</span></span>
- <span data-ttu-id="29363-173">**Beispiel**: ein kurzes Beispiel für den Vorgang, die Funktion oder den Typ, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="29363-173">**Example**: A short example of the operation, function, or type in use.</span></span>
- <span data-ttu-id="29363-174">**Hinweise**: verschiedene Prosa, die einen Aspekt des Vorgangs, der Funktion oder des Typs beschreibt.</span><span class="sxs-lookup"><span data-stu-id="29363-174">**Remarks**: Miscellaneous prose describing some aspect of the operation, function, or type.</span></span>
- <span data-ttu-id="29363-175">**Siehe auch**: eine Liste der voll qualifizierten Namen, die verwandte Funktionen, Vorgänge oder benutzerdefinierte Typen angeben.</span><span class="sxs-lookup"><span data-stu-id="29363-175">**See Also**: A list of fully qualified names indicating related functions, operations, or user-defined types.</span></span>
- <span data-ttu-id="29363-176">**Verweise**: eine Liste von verweisen und citationen für das dokumentierte Element.</span><span class="sxs-lookup"><span data-stu-id="29363-176">**References**: A list of references and citations for the documented item.</span></span>

## <a name="next-steps"></a><span data-ttu-id="29363-177">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="29363-177">Next steps</span></span>

<span data-ttu-id="29363-178">Weitere Informationen zu [Vorgängen und Funktionen](xref:microsoft.quantum.guide.operationsfunctions) in f #.</span><span class="sxs-lookup"><span data-stu-id="29363-178">Learn about [Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions) in Q#.</span></span>