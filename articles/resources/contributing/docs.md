---
title: Dokumentation zum Microsoft QDK
description: Erfahren Sie, wie Sie konzeptionelle oder API-Inhalte zum Microsoft Quantum-Dokumentations Satz beitragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 2debef858c38b9a8f11264858130ed7cb41543ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691790"
---
# <a name="improving-documentation"></a><span data-ttu-id="c5751-103">Verbessern der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c5751-103">Improving Documentation</span></span>

<span data-ttu-id="c5751-104">Die Dokumentation für das Quantum Development Kit ist in mehreren unterschiedlichen Formularen verfügbar, sodass die Informationen problemlos für Quantum-Entwickler verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="c5751-104">The documentation for the Quantum Development Kit takes on several different forms, such that information is readily available to quantum developers.</span></span>

<span data-ttu-id="c5751-105">Gemäß den Prinzipien von [docs als Code](https://www.writethedocs.org/guide/docs-as-code/)wird die gesamte Dokumentation zum Quantum Development Kit als Code formatiert und mit git auf die gleiche Weise wie der Quellcode verwaltet, der zum Erstellen des Quantum Development Kit verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5751-105">Following the principles of [Docs as Code](https://www.writethedocs.org/guide/docs-as-code/), all Quantum Development Kit documentation is formatted as code and is managed using Git in the same way as the source code that is used to build the Quantum Development Kit.</span></span>
<span data-ttu-id="c5751-106">Zum größten Teil besteht die Code Unterstützungs Dokumentation aus verschiedenen Formen von [markdown](https://daringfireball.net/projects/markdown/), einer Sprache zum Schreiben von umfangreichem formatiertem Text in einem nur-Text-Format, das in der Befehlszeile, in IDES und mit der Quell Code Verwaltung einfach zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="c5751-106">For the most part, the code backing documentation consists of various forms of [Markdown](https://daringfireball.net/projects/markdown/), a language for writing out richly formatted text in a plain text format that's easy to use at the command line, in IDEs, and with source control.</span></span>
<span data-ttu-id="c5751-107">Wir übernehmen auf ähnliche Weise die [mathjax](https://www.mathjax.org/) -Bibliothek, um die Formatierung von Mathematik in der Dokumentation mithilfe der Latex-Sprache zu ermöglichen, wie weiter unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c5751-107">We similarly adopt the [MathJax](https://www.mathjax.org/) library to allow for formatting mathematics in documentation using the LaTeX language, as detailed further below.</span></span>


<span data-ttu-id="c5751-108">Dies bedeutet, dass jede Art von Dokumentation in den Details etwas variiert:</span><span class="sxs-lookup"><span data-stu-id="c5751-108">That said, each form of documentation does vary somewhat in the details:</span></span>

- <span data-ttu-id="c5751-109">Die **konzeptionelle Dokumentation** besteht aus einer Reihe von Artikeln, die in veröffentlicht werden https://docs.microsoft.com/quantum , und in denen alles von den Grundlagen von Quantum Computing bis hin zu den technischen Spezifikationen für Austauschformate beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c5751-109">The **conceptual documentation** consists of a set of articles that are published to https://docs.microsoft.com/quantum, and that describe everything from the basics of quantum computing to the technical specifications for interchange formats.</span></span> <span data-ttu-id="c5751-110">Diese Artikel sind in " [docfx-aromatied markdown" (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html)geschrieben, einer markdown-Variante, die zum Erstellen umfassender Dokumentations Sätze verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5751-110">These articles are written in [DocFX-Flavored Markdown (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html), a Markdown variant used for creating rich documentation sets.</span></span>
- <span data-ttu-id="c5751-111">Die **API-Referenz** besteht aus einem Satz von Seiten für jede Q# Funktion, jeden Vorgang und jeden benutzerdefinierten Typ, der in veröffentlicht wird https://docs.microsoft.com/qsharp/api/ .</span><span class="sxs-lookup"><span data-stu-id="c5751-111">The **API reference** is a set of pages for each Q# function, operation, and user-defined type, published to https://docs.microsoft.com/qsharp/api/.</span></span> <span data-ttu-id="c5751-112">Diese Seiten dokumentieren die Eingaben und Vorgänge für jede Aufruf Bare Datei sowie Beispiele und Links zu weiteren Informationen.</span><span class="sxs-lookup"><span data-stu-id="c5751-112">These pages document the inputs and operations to each callable, along with examples and links to more information.</span></span> <span data-ttu-id="c5751-113">Die API-Referenz wird automatisch aus kleinen DFM-Dokumenten im Q# Quellcode im Rahmen der einzelnen Releases extrahiert.</span><span class="sxs-lookup"><span data-stu-id="c5751-113">The API reference is automatically extracted from small DFM documents in Q# source code as a part of each release.</span></span>
- <span data-ttu-id="c5751-114">Die in den einzelnen Beispielen und in der Datei "Info. MD" enthaltenen "Info **<!----> . MD** "-Dateien beschreiben, wie dieses Beispiel verwendet wird, und wie es verwendet wird, was es behandelt und wie es mit dem Rest des Quantum Development Kit verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c5751-114">The **README<!---->.md** files included with each sample and kata describe how to use that sample or kata is used, what it covers, and how it relates to the rest of the Quantum Development Kit.</span></span> <span data-ttu-id="c5751-115">Diese Dateien werden mithilfe von [GitHub-debuggermarkdown (GFM)](https://github.github.com/gfm/)geschrieben, eine einfachere Alternative zu DFM, die für die direkte Anfügung von Dokumentation an Coderepositorys beliebt ist.</span><span class="sxs-lookup"><span data-stu-id="c5751-115">These files are written using [GitHub Flavored Markdown (GFM)](https://github.github.com/gfm/), a more lightweight alternative to DFM that's popular for attaching documentation directly to code repositories.</span></span>

## <a name="contributing-to-the-conceptual-documentation"></a><span data-ttu-id="c5751-116">Mitwirken an der konzeptionellen Dokumentation</span><span class="sxs-lookup"><span data-stu-id="c5751-116">Contributing to the Conceptual Documentation</span></span>

<span data-ttu-id="c5751-117">Um an der konzeptionellen oder der Info-Dokumentation weiter zu verbessern, beginnt mit einer Pull Request auf [**microsoftdocs/Quantum-docs-PR**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/Quantum**](https://github.com/Microsoft/Quantum)oder [**Microsoft/quantumkatas**](https://github.com/Microsoft/QuantumKatas), wie es geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="c5751-117">To contribute an improvement to the conceptual or README documentation, then, starts with a pull request onto either [**MicrosoftDocs/quantum-docs-pr**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/Quantum**](https://github.com/Microsoft/Quantum), or [**Microsoft/QuantumKatas**](https://github.com/Microsoft/QuantumKatas), as is appropriate.</span></span>
<span data-ttu-id="c5751-118">Im folgenden werden weitere Informationen zu Pull Requests beschrieben. es gibt jedoch einige Dinge, die Sie beim Verbessern der Dokumentation beachten sollten:</span><span class="sxs-lookup"><span data-stu-id="c5751-118">We'll describe more about pull requests below, but for now there's a few things that are good to keep in mind as you improve documentation:</span></span>

- <span data-ttu-id="c5751-119">Leser werden aus einer sehr großen Bandbreite von Hintergründen an die Quantum Development Kit-Dokumentation weitergegeben.</span><span class="sxs-lookup"><span data-stu-id="c5751-119">Readers come to the Quantum Development Kit documentation from a very wide range of backgrounds.</span></span> <span data-ttu-id="c5751-120">Alle Personen von Studenten, die sich mit der Arbeit mit Quantum Computing Research vertraut machen, sollten in der Lage sein, die Dokumentation zu lesen.</span><span class="sxs-lookup"><span data-stu-id="c5751-120">Everyone from high school students looking to learn something new and exciting through to tenured faculty performing quantum computing research should be able to get something out of reading the documentation.</span></span> <span data-ttu-id="c5751-121">Soweit dies möglich ist, nehmen Sie keine umfassenden Kenntnisse über den Teil ihrer Leser an, da Sie möglicherweise einfach anfangen. Es ist besonders hilfreich, wenn Sie klare und barrierefreie Beschreibungen bereitstellen können, oder Sie können Links zu anderen Ressourcen bereitstellen, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5751-121">To the extent that's possible, please don't assume extensive knowledge on the part of your readers, as they may just be starting out. It's most helpful if you can provide clear and accessible descriptions, or can provide links to other resources for more information.</span></span>
- <span data-ttu-id="c5751-122">Dokumentations Sätze werden nicht wie Bücher oder Dokumente angelegt, da Leser in der "mittleren" erscheinen könnten.</span><span class="sxs-lookup"><span data-stu-id="c5751-122">Documentation sets aren't laid out like books or papers, in that readers will arrive in what might seem like the "middle."</span></span> <span data-ttu-id="c5751-123">Suchmaschinen können z. b. den Index nicht vorschlagen, oder es wurde ein Link von einem Freund gesendet, der Sie unterstützt. Versuchen Sie, dem Reader zu helfen, indem Sie immer einen eindeutigen Kontext bereitstellen, und verwenden Sie gegebenenfalls Links.</span><span class="sxs-lookup"><span data-stu-id="c5751-123">For example, search engines might not suggest the index, or they might have been sent a link by a friend trying to help them out. Try to help your reader by always providing a clear context, along with links where appropriate.</span></span>
- <span data-ttu-id="c5751-124">Einige Leser finden abstrakte Anweisungen und Definitionen am hilfreichsten, während andere Leser am besten funktionieren, indem Sie aus konkreten Beispielen extrapolieren.</span><span class="sxs-lookup"><span data-stu-id="c5751-124">Some readers will find abstract statements and definitions most helpful, while other readers work best by extrapolating from concrete examples.</span></span> <span data-ttu-id="c5751-125">Wenn sowohl der allgemeine Fall als auch bestimmte Beispiele bereitgestellt werden, können beide Leser die Quantum-Programmierung optimal nutzen.</span><span class="sxs-lookup"><span data-stu-id="c5751-125">Providing both the general case and specific examples can help both readers get the most out of quantum programming.</span></span>
- <span data-ttu-id="c5751-126">Vor allem, wenn Sie auch den Code geschrieben haben, der dokumentiert wird, können Sie für Sie offensichtlich sein, dass Sie für Ihre Leser nicht offensichtlich sind.</span><span class="sxs-lookup"><span data-stu-id="c5751-126">Especially if you also wrote the code being documented, things may be obvious to you that are not at all obvious to your reader.</span></span> <span data-ttu-id="c5751-127">Es gibt keine einzigartige Möglichkeit, um Programmieren zu können. unabhängig davon, wie clever oder erfahrener Leser sein könnte, können Sie sich nicht vorstellen, welche Entwurfsmuster Sie am hilfreichsten, um Ihre Ideen im Code auszudrücken.</span><span class="sxs-lookup"><span data-stu-id="c5751-127">There's no one unique best way to program, so no matter how clever or experienced a reader might be, they can't guess at what design patterns you found the most helpful to express your ideas in code.</span></span> <span data-ttu-id="c5751-128">Wenn Sie sich darüber im klaren sein, wie ein Reader die Verwendung des Codes erwarten kann, kann dieser Kontext bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5751-128">Being clear about how a reader can expect to make use of your code can help provide that context.</span></span>
- <span data-ttu-id="c5751-129">Viele Mitglieder der Quantum-Programmier Community sind akademische Forscher und werden hauptsächlich durch citate für Ihre Beiträge zur Community erkannt.</span><span class="sxs-lookup"><span data-stu-id="c5751-129">Many members of the quantum programming community are academic researchers, and are recognized mainly through citations for their contributions to the community.</span></span> <span data-ttu-id="c5751-130">Zusätzlich zur Unterstützung von Lesern bei der Suche nach zusätzlichen Materialien können Academic-Ausgaben, wie z. b. Zeitungen, Gespräche, Blogbeiträge und Software Tools, den akademischen Mitwirkenden dabei helfen, Ihre bestmögliche Arbeit zu verbessern, um die Community zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="c5751-130">In addition to helping readers find additional materials, making sure to properly cite academic outputs such as papers, talks, blog posts, and software tools can help academic contributors to keep doing their best work to improve the community.</span></span>
- <span data-ttu-id="c5751-131">Die Quantum-Programmier Community ist eine Breite und wunderbare Community.</span><span class="sxs-lookup"><span data-stu-id="c5751-131">The quantum programming community is a broad and wonderfully diverse community.</span></span> <span data-ttu-id="c5751-132">Die Verwendung von genten Pronomen in Beispielen für Dritte (z. b. "Wenn ein Benutzer..., er wird...") ausschließen und nicht einschließen.</span><span class="sxs-lookup"><span data-stu-id="c5751-132">The use of gendered pronouns in third-person examples (e.g.: "if a user ..., he will ...") can work to exclude rather than include.</span></span> <span data-ttu-id="c5751-133">Das Erkennen von Personennamen in citationen und Verknüpfungen und die richtige Einbeziehung von nicht-ASCII-Zeichen können die Vielfalt der Community erfüllen, indem die entsprechenden Elemente berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c5751-133">Being cognizant of people's names in citations and links, and of the correct inclusion of non-ASCII characters can serve the diversity of the community by showing respect to its members.</span></span> <span data-ttu-id="c5751-134">Auf ähnliche Weise werden viele Wörter in englischer Sprache häufig als Hass verwendet, sodass ihre Verwendung in der technischen Dokumentation sowohl für einzelne Leser als auch für die Community in großem Umfang Schaden anrichten kann.</span><span class="sxs-lookup"><span data-stu-id="c5751-134">Similarly, many words in the English language are often used in a hateful manner, such that their use in technical documentation can cause harm both to individual readers and to the community at large.</span></span>

### <a name="referencing-sample-code-from-conceptual-articles"></a><span data-ttu-id="c5751-135">Verweisen auf Beispiel Code aus konzeptionellen Artikeln</span><span class="sxs-lookup"><span data-stu-id="c5751-135">Referencing Sample Code from Conceptual Articles</span></span>

<span data-ttu-id="c5751-136">Wenn Sie Code aus dem [beispielrepository](https://github.com/Microsoft/Quantum)einschließen möchten, können Sie dazu einen speziellen DocFX-Flavored markdown-Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="c5751-136">If you want to include code from the [samples repository](https://github.com/Microsoft/Quantum), you can do so using a special DocFX-Flavored Markdown command:</span></span>

```markdown
:::code language="qsharp" source="~/quantum/samples/algorithms/chsh-game/Game.qs" range="4-8":::
```

<span data-ttu-id="c5751-137">Mit diesem Befehl werden die Zeilen 4 in 8 der [ `Game.qs` Datei aus dem `chsh-game` Beispiel](https://github.com/microsoft/Quantum/blob/main/samples/algorithms/chsh-game/Game.qs)importiert und als Q# Code für die Syntax Hervorhebung gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c5751-137">This command will import lines 4 to 8 of the [`Game.qs` file from the `chsh-game` sample](https://github.com/microsoft/Quantum/blob/main/samples/algorithms/chsh-game/Game.qs), marking them as Q# code for the purpose of syntax highlighting.</span></span>
<span data-ttu-id="c5751-138">Mit diesem Befehl können Sie das Duplizieren von Code zwischen konzeptionellen Artikeln und dem beispielrepository vermeiden, sodass der Beispielcode in der Dokumentation immer so aktuell wie möglich ist.</span><span class="sxs-lookup"><span data-stu-id="c5751-138">Using this command, you can avoid duplicating code between conceptual articles and the samples repository, so that sample code in documentation is always as up to date as possible.</span></span>

## <a name="contributing-to-the-api-references"></a><span data-ttu-id="c5751-139">Beitrag zu den API-verweisen</span><span class="sxs-lookup"><span data-stu-id="c5751-139">Contributing to the API References</span></span>

<span data-ttu-id="c5751-140">Um die API-Verweise zu verbessern, ist es am hilfreichsten, eine Pull Request direkt auf dem dokumentierten Code zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c5751-140">To contribute an improvement to the API references, it's most helpful to open a pull request directly on the code being documented.</span></span>
<span data-ttu-id="c5751-141">Jede Funktion, jeder Vorgang oder jeder benutzerdefinierte Typ unterstützt einen Dokumentations Kommentar ( `///` anstelle von `//` ).</span><span class="sxs-lookup"><span data-stu-id="c5751-141">Each function, operation, or user-defined type supports a documentation comment (denoted with `///` instead of `//`).</span></span>
<span data-ttu-id="c5751-142">Beim Kompilieren der einzelnen Releases des Quantum Development Kit werden diese Kommentare zum Generieren der API-Referenz unter verwendet https://docs.microsoft.com/qsharp/api/ , einschließlich Details zu den Eingaben und Ausgaben aus den einzelnen Aufruf baren, den Annahmen, die die einzelnen Aufrufe durchführen, sowie Beispiele für deren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="c5751-142">When we compile each release of the Quantum Development Kit, these comments are used to generate the API reference at https://docs.microsoft.com/qsharp/api/, including details about the inputs to and outputs from each callable, the assumptions each callable makes, and examples of how to use them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5751-143">Stellen Sie sicher, dass Sie die generierte API-Dokumentation nicht manuell bearbeiten, da diese Dateien mit jeder neuen Version überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c5751-143">Please make sure to not manually edit the generated API documentation, as these files are overwritten with each new release.</span></span>
> <span data-ttu-id="c5751-144">Wir schätzen ihren Beitrag zur Community und möchten sicherstellen, dass Ihre Änderungen den Benutzern nach der Veröffentlichung weiterhin helfen.</span><span class="sxs-lookup"><span data-stu-id="c5751-144">We value your contribution to the community, and want to make sure that your changes continue to help users release after release.</span></span>

<span data-ttu-id="c5751-145">Stellen Sie sich beispielsweise die-Funktion vor `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)` .</span><span class="sxs-lookup"><span data-stu-id="c5751-145">For example, consider the function `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)`.</span></span>
<span data-ttu-id="c5751-146">Ein Dokumentations Kommentar sollte einem Benutzer helfen, zu erfahren, wie `bits` und `oracle` wofür die Funktion vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="c5751-146">A documentation comment should help a user learn how to interpret `bits` and `oracle` and what the function is for.</span></span>
<span data-ttu-id="c5751-147">Alle diese unterschiedlichen Informationen können dem Q# Compiler von einem speziell benannten markdown-Abschnitt im Dokumentations Kommentar bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c5751-147">Each of these different pieces of information can be provided to the Q# compiler by a specially named Markdown section in the documentation comment.</span></span>
<span data-ttu-id="c5751-148">Für das Beispiel von `ControlledOnBitString` könnten wir etwas wie das folgende schreiben:</span><span class="sxs-lookup"><span data-stu-id="c5751-148">For the example of `ControlledOnBitString`, we might write something like the following:</span></span>

```qsharp
 /// # Summary
 /// Returns a unitary operation that applies an oracle on the target register if the 
 /// control register state corresponds to a specified bit mask.
 ///
 /// # Description
 /// The output of this function is an operation that can be represented by a
 /// unitary transformation $U$ such that
 /// \begin{align}
 ///     U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes
 ///     \begin{cases}
 ///         V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\
 ///         \ket{\psi} & \textrm{otherwise}
 ///     \end{cases},
 /// \end{align}
 /// where $V$ is a unitary transformation that represents the action of the
 /// `oracle` operation.
 ///
 /// # Input
 /// ## bits
 /// The bit string to control the given unitary operation on.
 /// ## oracle
 /// The unitary operation to be applied on the target register.
 ///
 /// # Output
 /// A unitary operation that applies `oracle` on the target register if the control 
 /// register state corresponds to the bit mask `bits`.
 ///
 /// # Remarks
 /// The length of `bits` and `controlRegister` must be equal.
 ///
 /// Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function
 /// is an operation that performs the following steps:
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits`;
 /// * apply `Controlled oracle` to the control and target registers;
 /// * apply an `X` operation to each qubit of the control register that corresponds to `false` 
 /// element of the `bits` again to return the control register to the original state.
 ///
 /// The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.
 ///
 /// # Example
 /// The following code snippets are equivalent:
 /// ```qsharp
 /// (ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
 /// ```
 /// and
 /// ```qsharp
 /// within {
 ///     ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
 /// } apply {
 ///     Controlled oracle(controlRegister, targetRegister);
 /// }
 /// ```
 ///
 /// The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:
 /// ```qsharp
 /// using (register = Qubit[2]) {
 ///     ApplyToEach(H, register);
 ///     (ControlledOnBitString([false], Z))(register[0..0], register[1]);
 /// }
 /// ```
 function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
 {
     return ControlledOnBitStringImpl(bits, oracle, _, _);
 }
```

<span data-ttu-id="c5751-149">Die gerenderte Version des obigen Codes finden Sie in der [API-Dokumentation für die `ControlledOnBitString` Funktion](xref:Microsoft.Quantum.Canon.ControlledOnBitString).</span><span class="sxs-lookup"><span data-stu-id="c5751-149">You can see the rendered version of the code above in the [API documentation for the `ControlledOnBitString` function](xref:Microsoft.Quantum.Canon.ControlledOnBitString).</span></span>

<span data-ttu-id="c5751-150">Zusätzlich zur allgemeinen Vorgehensweise bei der Dokumentations Erstellung werden im Artikel Schreiben von API-Dokumentations Kommentaren die folgenden Punkte berücksichtigt:</span><span class="sxs-lookup"><span data-stu-id="c5751-150">In addition to the general practice of documentation writing, in writing API documentation comments it helps to keep a few things in mind:</span></span>

- <span data-ttu-id="c5751-151">Das Format der einzelnen Dokumentations Kommentare muss den Anforderungen entsprechen, die der Q# Compiler erwartet, damit die Dokumentation ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c5751-151">The format of each documentation comment has to match what the Q# compiler expects for your documentation to appear correctly.</span></span> <span data-ttu-id="c5751-152">Einige Abschnitte, wie z `/// # Remarks` . b. das Zulassen von frei Hand Inhalten, während Abschnitte wie der- `/// # See Also` Abschnitt restriktiver sind.</span><span class="sxs-lookup"><span data-stu-id="c5751-152">Some sections, such as `/// # Remarks` allow for freeform content, while sections such as `/// # See Also` section are more restrictive.</span></span>
- <span data-ttu-id="c5751-153">Ein Leser kann Ihre API-Dokumentation auf der Haupt-API-Referenz Website, in der Zusammenfassung für jeden Namespace oder sogar in der IDE durch die Verwendung von Hover-Informationen lesen.</span><span class="sxs-lookup"><span data-stu-id="c5751-153">A reader may read your API documentation on the main API reference site, on the summary for each namespace, or even from within their IDE through the use of hover information.</span></span> <span data-ttu-id="c5751-154">Wenn Sie sicherstellen, dass `/// # Summary` nicht länger als ein Satz ist, können Sie den Leser schnell herausfinden, ob Sie einen weiteren Lesevorgang ausführen müssen, und Sie können bei der schnellen Durchführung von Namespace Zusammenfassungen helfen.</span><span class="sxs-lookup"><span data-stu-id="c5751-154">Making sure that `/// # Summary` isn't longer than about a sentence helps your reader quickly sort out whether they need to read further or look elsewhere, and can help in quickly scanning through namespace summaries.</span></span>
- <span data-ttu-id="c5751-155">Die Dokumentation kann deutlich länger als der Code selbst sein, aber das ist in Ordnung.</span><span class="sxs-lookup"><span data-stu-id="c5751-155">Your documentation may well wind up being much longer than the code itself, but that's OK!</span></span> <span data-ttu-id="c5751-156">Sogar ein kleiner Code Abschnitt kann unerwartete Auswirkungen auf Benutzer haben, die den Kontext, in dem der Code vorhanden ist, nicht kennen.</span><span class="sxs-lookup"><span data-stu-id="c5751-156">Even a small piece of code can have unexpected effects to users that don't know the context in which that code exists.</span></span> <span data-ttu-id="c5751-157">Wenn Sie konkrete Beispiele und Erläuterungen erläutern, können Sie die Benutzer dabei unterstützen, den Code, der für Sie verfügbar ist, optimal zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="c5751-157">By providing concrete examples and clear explanations, you can help users make the best use of the code that's available to them.</span></span>

<!-- ## LaTeX Formatting ##

**TODO** -->
