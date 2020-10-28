---
title: Dokumentation zum Microsoft QDK
description: Erfahren Sie, wie Sie konzeptionelle oder API-Inhalte zum Microsoft Quantum-Dokumentations Satz beitragen.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.docs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2debef858c38b9a8f11264858130ed7cb41543ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691790"
---
# <a name="improving-documentation"></a>Verbessern der Dokumentation

Die Dokumentation für das Quantum Development Kit ist in mehreren unterschiedlichen Formularen verfügbar, sodass die Informationen problemlos für Quantum-Entwickler verfügbar sind.

Gemäß den Prinzipien von [docs als Code](https://www.writethedocs.org/guide/docs-as-code/)wird die gesamte Dokumentation zum Quantum Development Kit als Code formatiert und mit git auf die gleiche Weise wie der Quellcode verwaltet, der zum Erstellen des Quantum Development Kit verwendet wird.
Zum größten Teil besteht die Code Unterstützungs Dokumentation aus verschiedenen Formen von [markdown](https://daringfireball.net/projects/markdown/), einer Sprache zum Schreiben von umfangreichem formatiertem Text in einem nur-Text-Format, das in der Befehlszeile, in IDES und mit der Quell Code Verwaltung einfach zu verwenden ist.
Wir übernehmen auf ähnliche Weise die [mathjax](https://www.mathjax.org/) -Bibliothek, um die Formatierung von Mathematik in der Dokumentation mithilfe der Latex-Sprache zu ermöglichen, wie weiter unten beschrieben.


Dies bedeutet, dass jede Art von Dokumentation in den Details etwas variiert:

- Die **konzeptionelle Dokumentation** besteht aus einer Reihe von Artikeln, die in veröffentlicht werden https://docs.microsoft.com/quantum , und in denen alles von den Grundlagen von Quantum Computing bis hin zu den technischen Spezifikationen für Austauschformate beschrieben wird. Diese Artikel sind in " [docfx-aromatied markdown" (DFM)](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html)geschrieben, einer markdown-Variante, die zum Erstellen umfassender Dokumentations Sätze verwendet wird.
- Die **API-Referenz** besteht aus einem Satz von Seiten für jede Q# Funktion, jeden Vorgang und jeden benutzerdefinierten Typ, der in veröffentlicht wird https://docs.microsoft.com/qsharp/api/ . Diese Seiten dokumentieren die Eingaben und Vorgänge für jede Aufruf Bare Datei sowie Beispiele und Links zu weiteren Informationen. Die API-Referenz wird automatisch aus kleinen DFM-Dokumenten im Q# Quellcode im Rahmen der einzelnen Releases extrahiert.
- Die in den einzelnen Beispielen und in der Datei "Info. MD" enthaltenen "Info **<!----> . MD** "-Dateien beschreiben, wie dieses Beispiel verwendet wird, und wie es verwendet wird, was es behandelt und wie es mit dem Rest des Quantum Development Kit verknüpft ist. Diese Dateien werden mithilfe von [GitHub-debuggermarkdown (GFM)](https://github.github.com/gfm/)geschrieben, eine einfachere Alternative zu DFM, die für die direkte Anfügung von Dokumentation an Coderepositorys beliebt ist.

## <a name="contributing-to-the-conceptual-documentation"></a>Mitwirken an der konzeptionellen Dokumentation

Um an der konzeptionellen oder der Info-Dokumentation weiter zu verbessern, beginnt mit einer Pull Request auf [**microsoftdocs/Quantum-docs-PR**](https://github.com/MicrosoftDocs/quantum-docs-pr/
), [**Microsoft/Quantum**](https://github.com/Microsoft/Quantum)oder [**Microsoft/quantumkatas**](https://github.com/Microsoft/QuantumKatas), wie es geeignet ist.
Im folgenden werden weitere Informationen zu Pull Requests beschrieben. es gibt jedoch einige Dinge, die Sie beim Verbessern der Dokumentation beachten sollten:

- Leser werden aus einer sehr großen Bandbreite von Hintergründen an die Quantum Development Kit-Dokumentation weitergegeben. Alle Personen von Studenten, die sich mit der Arbeit mit Quantum Computing Research vertraut machen, sollten in der Lage sein, die Dokumentation zu lesen. Soweit dies möglich ist, nehmen Sie keine umfassenden Kenntnisse über den Teil ihrer Leser an, da Sie möglicherweise einfach anfangen. Es ist besonders hilfreich, wenn Sie klare und barrierefreie Beschreibungen bereitstellen können, oder Sie können Links zu anderen Ressourcen bereitstellen, um weitere Informationen zu erhalten.
- Dokumentations Sätze werden nicht wie Bücher oder Dokumente angelegt, da Leser in der "mittleren" erscheinen könnten. Suchmaschinen können z. b. den Index nicht vorschlagen, oder es wurde ein Link von einem Freund gesendet, der Sie unterstützt. Versuchen Sie, dem Reader zu helfen, indem Sie immer einen eindeutigen Kontext bereitstellen, und verwenden Sie gegebenenfalls Links.
- Einige Leser finden abstrakte Anweisungen und Definitionen am hilfreichsten, während andere Leser am besten funktionieren, indem Sie aus konkreten Beispielen extrapolieren. Wenn sowohl der allgemeine Fall als auch bestimmte Beispiele bereitgestellt werden, können beide Leser die Quantum-Programmierung optimal nutzen.
- Vor allem, wenn Sie auch den Code geschrieben haben, der dokumentiert wird, können Sie für Sie offensichtlich sein, dass Sie für Ihre Leser nicht offensichtlich sind. Es gibt keine einzigartige Möglichkeit, um Programmieren zu können. unabhängig davon, wie clever oder erfahrener Leser sein könnte, können Sie sich nicht vorstellen, welche Entwurfsmuster Sie am hilfreichsten, um Ihre Ideen im Code auszudrücken. Wenn Sie sich darüber im klaren sein, wie ein Reader die Verwendung des Codes erwarten kann, kann dieser Kontext bereitgestellt werden.
- Viele Mitglieder der Quantum-Programmier Community sind akademische Forscher und werden hauptsächlich durch citate für Ihre Beiträge zur Community erkannt. Zusätzlich zur Unterstützung von Lesern bei der Suche nach zusätzlichen Materialien können Academic-Ausgaben, wie z. b. Zeitungen, Gespräche, Blogbeiträge und Software Tools, den akademischen Mitwirkenden dabei helfen, Ihre bestmögliche Arbeit zu verbessern, um die Community zu verbessern.
- Die Quantum-Programmier Community ist eine Breite und wunderbare Community. Die Verwendung von genten Pronomen in Beispielen für Dritte (z. b. "Wenn ein Benutzer..., er wird...") ausschließen und nicht einschließen. Das Erkennen von Personennamen in citationen und Verknüpfungen und die richtige Einbeziehung von nicht-ASCII-Zeichen können die Vielfalt der Community erfüllen, indem die entsprechenden Elemente berücksichtigt werden. Auf ähnliche Weise werden viele Wörter in englischer Sprache häufig als Hass verwendet, sodass ihre Verwendung in der technischen Dokumentation sowohl für einzelne Leser als auch für die Community in großem Umfang Schaden anrichten kann.

### <a name="referencing-sample-code-from-conceptual-articles"></a>Verweisen auf Beispiel Code aus konzeptionellen Artikeln

Wenn Sie Code aus dem [beispielrepository](https://github.com/Microsoft/Quantum)einschließen möchten, können Sie dazu einen speziellen DocFX-Flavored markdown-Befehl verwenden:

```markdown
:::code language="qsharp" source="~/quantum/samples/algorithms/chsh-game/Game.qs" range="4-8":::
```

Mit diesem Befehl werden die Zeilen 4 in 8 der [ `Game.qs` Datei aus dem `chsh-game` Beispiel](https://github.com/microsoft/Quantum/blob/main/samples/algorithms/chsh-game/Game.qs)importiert und als Q# Code für die Syntax Hervorhebung gekennzeichnet.
Mit diesem Befehl können Sie das Duplizieren von Code zwischen konzeptionellen Artikeln und dem beispielrepository vermeiden, sodass der Beispielcode in der Dokumentation immer so aktuell wie möglich ist.

## <a name="contributing-to-the-api-references"></a>Beitrag zu den API-verweisen

Um die API-Verweise zu verbessern, ist es am hilfreichsten, eine Pull Request direkt auf dem dokumentierten Code zu öffnen.
Jede Funktion, jeder Vorgang oder jeder benutzerdefinierte Typ unterstützt einen Dokumentations Kommentar ( `///` anstelle von `//` ).
Beim Kompilieren der einzelnen Releases des Quantum Development Kit werden diese Kommentare zum Generieren der API-Referenz unter verwendet https://docs.microsoft.com/qsharp/api/ , einschließlich Details zu den Eingaben und Ausgaben aus den einzelnen Aufruf baren, den Annahmen, die die einzelnen Aufrufe durchführen, sowie Beispiele für deren Verwendung.

> [!IMPORTANT]
> Stellen Sie sicher, dass Sie die generierte API-Dokumentation nicht manuell bearbeiten, da diese Dateien mit jeder neuen Version überschrieben werden.
> Wir schätzen ihren Beitrag zur Community und möchten sicherstellen, dass Ihre Änderungen den Benutzern nach der Veröffentlichung weiterhin helfen.

Stellen Sie sich beispielsweise die-Funktion vor `ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)` .
Ein Dokumentations Kommentar sollte einem Benutzer helfen, zu erfahren, wie `bits` und `oracle` wofür die Funktion vorgesehen ist.
Alle diese unterschiedlichen Informationen können dem Q# Compiler von einem speziell benannten markdown-Abschnitt im Dokumentations Kommentar bereitgestellt werden.
Für das Beispiel von `ControlledOnBitString` könnten wir etwas wie das folgende schreiben:

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

Die gerenderte Version des obigen Codes finden Sie in der [API-Dokumentation für die `ControlledOnBitString` Funktion](xref:Microsoft.Quantum.Canon.ControlledOnBitString).

Zusätzlich zur allgemeinen Vorgehensweise bei der Dokumentations Erstellung werden im Artikel Schreiben von API-Dokumentations Kommentaren die folgenden Punkte berücksichtigt:

- Das Format der einzelnen Dokumentations Kommentare muss den Anforderungen entsprechen, die der Q# Compiler erwartet, damit die Dokumentation ordnungsgemäß angezeigt wird. Einige Abschnitte, wie z `/// # Remarks` . b. das Zulassen von frei Hand Inhalten, während Abschnitte wie der- `/// # See Also` Abschnitt restriktiver sind.
- Ein Leser kann Ihre API-Dokumentation auf der Haupt-API-Referenz Website, in der Zusammenfassung für jeden Namespace oder sogar in der IDE durch die Verwendung von Hover-Informationen lesen. Wenn Sie sicherstellen, dass `/// # Summary` nicht länger als ein Satz ist, können Sie den Leser schnell herausfinden, ob Sie einen weiteren Lesevorgang ausführen müssen, und Sie können bei der schnellen Durchführung von Namespace Zusammenfassungen helfen.
- Die Dokumentation kann deutlich länger als der Code selbst sein, aber das ist in Ordnung. Sogar ein kleiner Code Abschnitt kann unerwartete Auswirkungen auf Benutzer haben, die den Kontext, in dem der Code vorhanden ist, nicht kennen. Wenn Sie konkrete Beispiele und Erläuterungen erläutern, können Sie die Benutzer dabei unterstützen, den Code, der für Sie verfügbar ist, optimal zu nutzen.

<!-- ## LaTeX Formatting ##

**TODO** -->
