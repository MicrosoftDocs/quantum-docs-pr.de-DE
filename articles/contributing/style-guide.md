---
title: 'F #-Stil Handbuch | Microsoft-Dokumentation'
description: 'F #-Stil Handbuch'
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
ms.openlocfilehash: 4050e2ee9e516aed7a8ba1398792562926808ee0
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463324"
---
# <a name="q-style-guide"></a><span data-ttu-id="6890e-103">F #-Stil Handbuch</span><span class="sxs-lookup"><span data-stu-id="6890e-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="6890e-104">Allgemeine Konventionen</span><span class="sxs-lookup"><span data-stu-id="6890e-104">General Conventions</span></span> ##

<span data-ttu-id="6890e-105">Die in diesem Handbuch empfohlenen Konventionen dienen dazu, Programme und Bibliotheken, die in Q # geschrieben wurden, einfacher zu lesen und zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="6890e-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="6890e-106">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-106">Guidance</span></span>

<span data-ttu-id="6890e-107">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-107">We suggest:</span></span>

- <span data-ttu-id="6890e-108">Ignorieren Sie niemals eine Konvention, wenn Sie dies nicht absichtlich tun, um für Ihre Benutzer besser lesbaren und verständlichen Code bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6890e-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="6890e-109">Namenskonventionen</span><span class="sxs-lookup"><span data-stu-id="6890e-109">Naming Conventions</span></span> ##

<span data-ttu-id="6890e-110">Beim anbieten des quantumentwicklungskit werden Funktions-und Vorgangs Namen unterstützt, mit denen Quantum-Entwickler Programme schreiben können, die leicht lesbar sind und die überraschen.</span><span class="sxs-lookup"><span data-stu-id="6890e-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="6890e-111">Ein wichtiger Aspekt dabei ist, dass wir bei der Auswahl von Namen für Funktionen, Vorgänge und Typen das *Vokabular* einrichten, mit dem Programmierer Quantum-Konzepte Ausdrücken. mit unseren Optionen können wir Sie bei der klaren Kommunikation unterstützen oder behindern.</span><span class="sxs-lookup"><span data-stu-id="6890e-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="6890e-112">Dies liegt in der Verantwortung für uns, sicherzustellen, dass die Namen, die wir einführen, eher Klarheit bieten als Verschleierung.</span><span class="sxs-lookup"><span data-stu-id="6890e-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="6890e-113">In diesem Abschnitt erfahren Sie, wie wir diese Verpflichtung in Bezug auf eine explizite Anleitung erfüllen, mit der wir am besten von der Q #-Entwicklungs Community unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="6890e-114">Vorgänge und Funktionen</span><span class="sxs-lookup"><span data-stu-id="6890e-114">Operations and Functions</span></span> ###

<span data-ttu-id="6890e-115">Eines der ersten Dinge, die ein Name einrichten sollte, ist, ob ein bestimmtes Symbol eine Funktion oder einen Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="6890e-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="6890e-116">Der Unterschied zwischen Funktionen und Vorgängen ist wichtig, um zu verstehen, wie sich ein Codeblock verhält.</span><span class="sxs-lookup"><span data-stu-id="6890e-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="6890e-117">Um den Unterschied zwischen Funktionen und Vorgängen an Benutzer zu übermitteln, basieren wir auf der Verwendung von Nebeneffekten darauf, dass die f #-Modelle Quantum-Vorgänge verwenden.</span><span class="sxs-lookup"><span data-stu-id="6890e-117">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="6890e-118">Dies *bedeutet* , dass ein Vorgang etwas bewirkt.</span><span class="sxs-lookup"><span data-stu-id="6890e-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="6890e-119">Im Gegensatz dazu beschreiben Funktionen die mathematischen Beziehungen zwischen den Daten.</span><span class="sxs-lookup"><span data-stu-id="6890e-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="6890e-120">Der Ausdrucks `Sin(PI() / 2.0)` *ist* `1.0`und impliziert nichts über den Zustand eines Programms oder seiner Qubits.</span><span class="sxs-lookup"><span data-stu-id="6890e-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="6890e-121">Durch die Zusammenfassung werden Vorgänge ausgeführt, während Functions Dinge sind.</span><span class="sxs-lookup"><span data-stu-id="6890e-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="6890e-122">Dieser Unterschied schlägt vor, dass wir Vorgänge als Verben und Funktionen als Nomen benennen.</span><span class="sxs-lookup"><span data-stu-id="6890e-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="6890e-123">Wenn ein benutzerdefinierter Typ deklariert wird, wird eine neue Funktion, die Instanzen dieses Typs erstellt, gleichzeitig implizit definiert.</span><span class="sxs-lookup"><span data-stu-id="6890e-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="6890e-124">Aus dieser Sicht sollten benutzerdefinierte Typen als Nomen benannt werden, damit der Typ selbst und die Konstruktorfunktion konsistente Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6890e-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="6890e-125">Stellen Sie in angemessener Weise sicher, dass Vorgangs Namen mit Verben beginnen, die die Auswirkungen des Vorgangs eindeutig angeben.</span><span class="sxs-lookup"><span data-stu-id="6890e-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="6890e-126">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6890e-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="6890e-127">Ein Fall, der besondere Erwähnung verdient, ist, wenn ein Vorgang einen anderen Vorgang als Eingabe annimmt und ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="6890e-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="6890e-128">In solchen Fällen ist die vom Eingabevorgang ausgeführte Aktion nicht klar, wenn der äußere Vorgang definiert ist, sodass das Rechte Verb nicht sofort gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6890e-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="6890e-129">Wir empfehlen das Verb `Apply`, wie in `ApplyIf`, `ApplyToEach`und `ApplyToFirst`.</span><span class="sxs-lookup"><span data-stu-id="6890e-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="6890e-130">Andere Verben können auch in diesem Fall nützlich sein, wie in `IterateThroughCartesianPower`.</span><span class="sxs-lookup"><span data-stu-id="6890e-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="6890e-131">Verb</span><span class="sxs-lookup"><span data-stu-id="6890e-131">Verb</span></span> | <span data-ttu-id="6890e-132">Erwarteter Effekt</span><span class="sxs-lookup"><span data-stu-id="6890e-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="6890e-133">Anwenden</span><span class="sxs-lookup"><span data-stu-id="6890e-133">Apply</span></span> | <span data-ttu-id="6890e-134">Ein als Eingabe bereitgestellter Vorgang wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6890e-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="6890e-135">Assert</span><span class="sxs-lookup"><span data-stu-id="6890e-135">Assert</span></span> | <span data-ttu-id="6890e-136">Eine Hypothese über das Ergebnis einer möglichen Quantum-Messung wird von einem Simulator geprüft.</span><span class="sxs-lookup"><span data-stu-id="6890e-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="6890e-137">Schätzung</span><span class="sxs-lookup"><span data-stu-id="6890e-137">Estimate</span></span> | <span data-ttu-id="6890e-138">Ein klassischer Wert wird zurückgegeben, der eine Schätzung darstellt, die aus einer oder mehreren Messungen gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="6890e-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="6890e-139">"Measure"</span><span class="sxs-lookup"><span data-stu-id="6890e-139">Measure</span></span> | <span data-ttu-id="6890e-140">Eine Quantum-Messung wird ausgeführt, und das Ergebnis wird an den Benutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6890e-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="6890e-141">Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="6890e-141">Prepare</span></span> | <span data-ttu-id="6890e-142">Ein bestimmtes Register von Qubits wird in einem bestimmten Zustand initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6890e-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="6890e-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6890e-143">Sample</span></span> | <span data-ttu-id="6890e-144">Ein klassischer Wert wird nach dem Zufallsprinzip aus einer Verteilung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6890e-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="6890e-145">Bei Functions empfiehlt es sich, die Verwendung von Verben anstelle von gängigen Substantiven zu vermeiden (siehe Anleitungen zu den richtigen Nomen unten) oder Adjektive:</span><span class="sxs-lookup"><span data-stu-id="6890e-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="6890e-146">Vor allem empfiehlt es sich in fast allen Fällen, frühere Partizipationen zu verwenden, wenn dies angebracht ist, um anzugeben, dass ein Funktionsname an anderer Stelle in einem Quantum-Programm mit einer Aktion oder einem Nebeneffekt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="6890e-147">`ControlledOnInt` verwendet beispielsweise die Form teilnehmen des Verbs "Control", um anzugeben, dass die Funktion als Adjektiv fungiert, um das Argument zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6890e-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="6890e-148">Dieser Name hat den zusätzlichen Vorteil, dass die Semantik des integrierten `Controlled`-funktors übereinstimmt, wie weiter unten erläutert.</span><span class="sxs-lookup"><span data-stu-id="6890e-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="6890e-149">Ebenso können- _Agent-Nomen_ verwendet werden, um Funktions-und UDT-Namen aus Vorgangs Namen zu erstellen, wie im Fall des Namens `Encoder` für einen UDT, der stark mit `Encode`verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-150">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-151">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-151">We suggest:</span></span>

- <span data-ttu-id="6890e-152">Verwenden Sie Verben für Vorgangs Namen.</span><span class="sxs-lookup"><span data-stu-id="6890e-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="6890e-153">Verwenden Sie Nomen oder Adjektive für Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="6890e-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="6890e-154">Verwenden Sie Nomen für benutzerdefinierte Typen und Attribute.</span><span class="sxs-lookup"><span data-stu-id="6890e-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="6890e-155">Verwenden Sie für alle Aufruf baren Namen `CamelCase` `pascalCase`, `snake_case`oder `ANGRY_CASE`.</span><span class="sxs-lookup"><span data-stu-id="6890e-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="6890e-156">Stellen Sie insbesondere sicher, dass Aufruf Bare Namen mit Großbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="6890e-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="6890e-157">Verwenden Sie für alle lokalen Variablen `pascalCase` unter starker Priorität für `CamelCase`, `snake_case`oder `ANGRY_CASE`.</span><span class="sxs-lookup"><span data-stu-id="6890e-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="6890e-158">Stellen Sie insbesondere sicher, dass lokale Variablen mit Kleinbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="6890e-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="6890e-159">Vermeiden Sie die Verwendung von unterstrichen `_` in Funktions-und Vorgangs Namen; Wenn weitere Hierarchieebenen benötigt werden, verwenden Sie Namespaces und Namespace Aliase.</span><span class="sxs-lookup"><span data-stu-id="6890e-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-160">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="6890e-161">name</span><span class="sxs-lookup"><span data-stu-id="6890e-161">Name</span></span> | <span data-ttu-id="6890e-162">description</span><span class="sxs-lookup"><span data-stu-id="6890e-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="6890e-163">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="6890e-164">Löschen Sie die Verwendung eines Verbs ("reflektieren"), um die Auswirkung des Vorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6890e-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="6890e-165">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="6890e-166">Die Verwendung von Substantiv Phrase schlägt eine Funktion anstelle von Operation vor.</span><span class="sxs-lookup"><span data-stu-id="6890e-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="6890e-167">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="6890e-168">Die Verwendung von `snake_case` verstößt gegen die Q #-Notation.</span><span class="sxs-lookup"><span data-stu-id="6890e-168">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="6890e-169">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="6890e-170">Die Verwendung von unterstrichen im internen Namen für den Vorgangs Namen verstößt gegen die Q #-Notation</span><span class="sxs-lookup"><span data-stu-id="6890e-170">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="6890e-171">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="6890e-172">Die Verwendung des Substantiv Ausdrucks deutet darauf hin, dass die Funktion einen Vorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6890e-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="6890e-173">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="6890e-174">Löschen Sie die Verwendung von Substantiv ("Fakt"), um anzugeben, dass es sich hierbei um eine Funktion handelt, während das Adjektiv ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="6890e-175">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="6890e-176">Die Verwendung von Verb ("Get") deutet darauf hin, dass es sich hierbei um einen Vorgang handelt.</span><span class="sxs-lookup"><span data-stu-id="6890e-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="6890e-177">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="6890e-178">Die Verwendung des Substantiv Ausdrucks verweist eindeutig auf das Ergebnis des Aufrufs des UDT-Konstruktors.</span><span class="sxs-lookup"><span data-stu-id="6890e-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="6890e-179">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="6890e-180">Die Verwendung des Verb Ausdrucks deutet darauf hin, dass der UDT-Konstruktor ein Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="6890e-181">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="6890e-182">Die Verwendung des nominalen Ausdrucks kommuniziert mit der Verwendung des-Attributs.</span><span class="sxs-lookup"><span data-stu-id="6890e-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="6890e-183">Kurzformen und Abkürzungen</span><span class="sxs-lookup"><span data-stu-id="6890e-183">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="6890e-184">Ungeachtet der obigen Ratschläge gibt es eine Vielzahl von kurz Informationen, die die allgemeine und weit verbreitete Verwendung von Quantum Computing sehen.</span><span class="sxs-lookup"><span data-stu-id="6890e-184">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="6890e-185">Es wird empfohlen, vorhandene und allgemeine kurzwerte zu verwenden, und wo Sie vorhanden sind, insbesondere bei Vorgängen, die für den Betrieb eines Ziel Computers intrinsisch sind.</span><span class="sxs-lookup"><span data-stu-id="6890e-185">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="6890e-186">Wir wählen z. b. den Namen `X` anstelle von `ApplyX`und `Rz` anstelle von `RotateAboutZ`.</span><span class="sxs-lookup"><span data-stu-id="6890e-186">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="6890e-187">Wenn Sie diese Kurznamen verwenden, sollten Vorgangs Namen Großbuchstaben sein (z. b.: `MAJ`).</span><span class="sxs-lookup"><span data-stu-id="6890e-187">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="6890e-188">Im Fall von häufig verwendeten Akronymen und Initialisierungen, wie z. b. "QFT" für "Quantum Fourier Transform", ist Vorsicht geboten.</span><span class="sxs-lookup"><span data-stu-id="6890e-188">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="6890e-189">Es empfiehlt sich, allgemeine .net-Konventionen für die Verwendung von Akronymen und initialismen in vollständigen Namen zu befolgen, die Folgendes vorschreiben:</span><span class="sxs-lookup"><span data-stu-id="6890e-189">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="6890e-190">Akronyme mit zwei Buchstaben und initialisierernamen werden in Großbuchstaben benannt (z. b. `BE` für "Big-erdian").</span><span class="sxs-lookup"><span data-stu-id="6890e-190">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="6890e-191">Alle längeren Akronyme und Initialisierer werden in `CamelCase` benannt (z. b.: `Qft` für "Quantum Fourier Transform").</span><span class="sxs-lookup"><span data-stu-id="6890e-191">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="6890e-192">Folglich kann ein Vorgang, der den QFT implementiert, entweder als Kurzform `QFT` aufgerufen oder als `ApplyQft`ausgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-192">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="6890e-193">Bei besonders häufig verwendeten Vorgängen und Funktionen ist es möglicherweise wünschenswert, einen Kurznamen als _Alias_ für eine längere Form bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="6890e-193">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-194">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-194">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-195">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-195">We suggest:</span></span>

- <span data-ttu-id="6890e-196">Beachten Sie ggf. häufig akzeptierte und häufig verwendete Kurznamen.</span><span class="sxs-lookup"><span data-stu-id="6890e-196">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="6890e-197">Verwenden Sie Großbuchstaben für Kurzformen.</span><span class="sxs-lookup"><span data-stu-id="6890e-197">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="6890e-198">Verwenden Sie für kurze (aus zwei Buchstaben bestehende) Akronyme und Initialisierungen Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="6890e-198">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="6890e-199">Verwenden Sie `CamelCase` für längere Akronyme und Initialisierungen (drei oder mehr Buchstabe).</span><span class="sxs-lookup"><span data-stu-id="6890e-199">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-200">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-200">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="6890e-201">name</span><span class="sxs-lookup"><span data-stu-id="6890e-201">Name</span></span> | <span data-ttu-id="6890e-202">description</span><span class="sxs-lookup"><span data-stu-id="6890e-202">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="6890e-203">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-203">☑</span></span> | `X` | <span data-ttu-id="6890e-204">Wohl verständliche Kurzformen für "Apply a $X $ Transformation"</span><span class="sxs-lookup"><span data-stu-id="6890e-204">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="6890e-205">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-205">☑</span></span> | `CNOT` | <span data-ttu-id="6890e-206">Wohl verständliche Kurzformen für "kontrolliert-not"</span><span class="sxs-lookup"><span data-stu-id="6890e-206">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="6890e-207">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-207">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="6890e-208">Die Kurzweile sollte nicht in `CamelCase`sein.</span><span class="sxs-lookup"><span data-stu-id="6890e-208">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="6890e-209">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-209">☑</span></span> | `ApplyQft` | <span data-ttu-id="6890e-210">Der allgemeine initialismus "QFT" wird als Teil eines langen Namens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6890e-210">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="6890e-211">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-211">☑</span></span> | `QFT` | <span data-ttu-id="6890e-212">Allgemeine Initialisierung "QFT" wird als Teil einer Kurzform angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6890e-212">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="6890e-213">Richtige Nomen in Namen</span><span class="sxs-lookup"><span data-stu-id="6890e-213">Proper Nouns in Names</span></span> ###

<span data-ttu-id="6890e-214">In der Physik ist es üblich, die Dinge nach der ersten Person zu benennen, um Sie zu veröffentlichen. die meisten nicht-Physikern sind nicht mit den Namen aller Benutzer und dem gesamten Verlauf vertraut.</span><span class="sxs-lookup"><span data-stu-id="6890e-214">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="6890e-215">Wenn Sie sich zu stark auf Benennungs Konventionen der Physik verlassen, kann dies zu einer beträchtlichen Barriere für die Eingabe führen, da Benutzer aus anderen Hintergründen eine große Anzahl scheinbar undurchsichtiger Namen erlernen müssen, um allgemeine Vorgänge und Konzepte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6890e-215">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="6890e-216">Daher wird empfohlen, dass, soweit sinnvoll, gängige Nomen, die ein Konzept beschreiben, für die richtigen Nomen, die den Veröffentlichungs Verlauf eines Konzepts beschreiben, eine starke Bevorzugung annehmen.</span><span class="sxs-lookup"><span data-stu-id="6890e-216">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="6890e-217">Ein bestimmtes Beispiel ist, dass die einzeln kontrollierten Swap-und doppelt kontrollierten not-Vorgänge in Academic Literatur oft als "Fredkin"-und "to-do"-Vorgänge bezeichnet werden, aber in Q # primär als `CSWAP` und `CCNOT`identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-217">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="6890e-218">In beiden Fällen enthalten die API-Dokumentations Kommentare Synonyme, die auf den richtigen Substantiven basieren, sowie alle entsprechenden citierungen.</span><span class="sxs-lookup"><span data-stu-id="6890e-218">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="6890e-219">Diese Einstellung ist besonders wichtig, da eine bestimmte Verwendung von richtigen Nomen immer erforderlich ist – f # folgt der Tradition, die von vielen klassischen Sprachen festgelegt wird, und bezieht sich auf `Bool` Typen in Bezug auf die boolesche Logik, die wiederum in Bezug genommen wird. von George Boole.</span><span class="sxs-lookup"><span data-stu-id="6890e-219">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="6890e-220">Einige Quantum-Konzepte werden ähnlich benannt, einschließlich des in der Sprache Q # integrierten `Pauli` Typs.</span><span class="sxs-lookup"><span data-stu-id="6890e-220">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="6890e-221">Wenn Sie die Verwendung von richtigen Nomen minimieren, bei denen eine solche Verwendung nicht wesentlich ist, verringern wir die Auswirkungen, bei denen die richtigen Nomen nicht vernünftig vermieden werden können.</span><span class="sxs-lookup"><span data-stu-id="6890e-221">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-222">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-222">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="6890e-223">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-223">We suggest:</span></span>

- <span data-ttu-id="6890e-224">Vermeiden Sie die Verwendung von richtigen Substantiven in Namen.</span><span class="sxs-lookup"><span data-stu-id="6890e-224">Avoid the use of proper nouns in names.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-225">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-225">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="6890e-226">Typkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="6890e-226">Type Conversions</span></span> ###

<span data-ttu-id="6890e-227">Da Q # eine stark und statisch typisierte Sprache ist, kann ein Wert eines Typs nur als Wert eines anderen Typs verwendet werden, indem ein expliziter Rückruf einer Typkonvertierungs Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6890e-227">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="6890e-228">Dies steht im Gegensatz zu Sprachen, die es ermöglichen, Typen implizit (z. b. typherauf Stufung) oder durch Umwandlung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6890e-228">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="6890e-229">Typkonvertierungs Funktionen spielen daher eine wichtige Rolle bei der Entwicklung der Q #-Bibliothek und bilden eine der gängigsten Entscheidungen zum benennen.</span><span class="sxs-lookup"><span data-stu-id="6890e-229">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="6890e-230">Es ist jedoch zu beachten, dass Typkonvertierungen immer _deterministisch_sind. Sie können als Funktionen geschrieben werden und fallen daher unter den obigen Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="6890e-230">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="6890e-231">Insbesondere wird empfohlen, dass Typkonvertierungs Funktionen nie als Verben (z. b.: `ConvertToX`) oder adverbfilter-präpositional-Ausdrücke (`ToX`) benannt werden. Sie sollten jedoch als Adjektiv-Ausdrücke mit präpositional bezeichnet werden, die die Quell-und Zieltypen angeben (`XAsY`).</span><span class="sxs-lookup"><span data-stu-id="6890e-231">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="6890e-232">Beim Auflisten von Array Typen in Namen der Typkonvertierungs Funktion wird die Kurzform `Arr`empfohlen.</span><span class="sxs-lookup"><span data-stu-id="6890e-232">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="6890e-233">Abgesehen von Ausnahmefällen wird empfohlen, dass alle Typkonvertierungs Funktionen mit `As` benannt werden, damit Sie schnell identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="6890e-233">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-234">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-234">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-235">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-235">We suggest:</span></span>

- <span data-ttu-id="6890e-236">Wenn eine Funktion einen Wert vom Typ `X` in einen Wert vom Typ `Y`konvertiert, verwenden Sie entweder den Namen `AsY` oder `XAsY`.</span><span class="sxs-lookup"><span data-stu-id="6890e-236">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-237">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-237">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="6890e-238">name</span><span class="sxs-lookup"><span data-stu-id="6890e-238">Name</span></span> | <span data-ttu-id="6890e-239">description</span><span class="sxs-lookup"><span data-stu-id="6890e-239">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="6890e-240">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-240">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="6890e-241">Die Vorposition "to" führt zu einem Verb Ausdruck, der einen Vorgang und keine Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="6890e-241">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="6890e-242">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-242">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="6890e-243">Der Eingabetyp ist aus dem Funktionsnamen nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6890e-243">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="6890e-244">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-244">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="6890e-245">Die Eingabe-und Ausgabetypen werden in der falschen Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6890e-245">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="6890e-246">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-246">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="6890e-247">Die Eingabe-und Ausgabetypen sind eindeutig.</span><span class="sxs-lookup"><span data-stu-id="6890e-247">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="6890e-248">Private oder interne Namen</span><span class="sxs-lookup"><span data-stu-id="6890e-248">Private or Internal Names</span></span> ###

<span data-ttu-id="6890e-249">In vielen Fällen ist ein Name ausschließlich für die interne Verwendung in einer Bibliothek oder einem Projekt vorgesehen und ist kein garantierter Teil der API, die von einer Bibliothek angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="6890e-249">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="6890e-250">Es ist hilfreich, eindeutig anzugeben, dass dies der Fall ist, wenn Funktionen und Vorgänge benannt werden, damit versehentlich Abhängigkeiten von internem Code offensichtlich werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-250">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="6890e-251">Wenn ein Vorgang oder eine Funktion nicht für die direkte Verwendung vorgesehen ist, sondern stattdessen von einer übereinstimmenden Aufruf baren Funktion verwendet werden soll, die von einer partiellen Anwendung verwendet wird, empfiehlt es sich, einen Namen zu verwenden, der mit `_` für die teilweise angewendete Aufruf Bare</span><span class="sxs-lookup"><span data-stu-id="6890e-251">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with `_` for the callable that is partially applied.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-252">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-252">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-253">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-253">We suggest:</span></span>

- <span data-ttu-id="6890e-254">Wenn eine Funktion, ein Vorgang oder ein benutzerdefinierter Typ nicht Teil der öffentlichen API für eine Q #-Bibliothek oder ein Programm ist, müssen Sie sicherstellen, dass der Name mit einem führenden Unterstrich (`_`) beginnt.</span><span class="sxs-lookup"><span data-stu-id="6890e-254">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that its name begins with a leading underscore (`_`).</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-255">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-255">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="6890e-256">name</span><span class="sxs-lookup"><span data-stu-id="6890e-256">Name</span></span> | <span data-ttu-id="6890e-257">description</span><span class="sxs-lookup"><span data-stu-id="6890e-257">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="6890e-258">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-258">☒</span></span> | <s>`ApplyDecomposedOperation_`</s> | <span data-ttu-id="6890e-259">Der Unterstrich `_` sollte nicht am Ende des Namens angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-259">The underscore `_` should not appear at the end of the name.</span></span> |
| <span data-ttu-id="6890e-260">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-260">☑</span></span> | `_ApplyDecomposedOperation` | <span data-ttu-id="6890e-261">Der Unterstrich `_` am Anfang weist eindeutig darauf hin, dass dieser Vorgang nur für die interne Verwendung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-261">The underscore `_` at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***

### <a name="variants"></a><span data-ttu-id="6890e-262">HI</span><span class="sxs-lookup"><span data-stu-id="6890e-262">Variants</span></span> ###

<span data-ttu-id="6890e-263">Obwohl diese Einschränkung in zukünftigen Versionen von Q # nicht beibehalten werden kann, ist es aktuell der Fall, dass häufig Gruppen verwandter Vorgänge oder Funktionen vorhanden sind, die durch die von Ihnen unterstützten Funktoren unterschieden werden, oder durch die konkreten Typen ihrer Argumente.</span><span class="sxs-lookup"><span data-stu-id="6890e-263">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="6890e-264">Diese Gruppen können unterschieden werden, indem der gleiche Stamm Name verwendet wird, gefolgt von einem oder zwei Buchstaben, die die Variante angeben.</span><span class="sxs-lookup"><span data-stu-id="6890e-264">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="6890e-265">Suffix</span><span class="sxs-lookup"><span data-stu-id="6890e-265">Suffix</span></span> | <span data-ttu-id="6890e-266">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="6890e-266">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="6890e-267">Die Eingabe erwartet `Adjoint`</span><span class="sxs-lookup"><span data-stu-id="6890e-267">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="6890e-268">Die Eingabe erwartet `Controlled`</span><span class="sxs-lookup"><span data-stu-id="6890e-268">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="6890e-269">Es wurde erwartet, dass `Controlled` und `Adjoint` unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-269">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="6890e-270">Eingabe oder Eingaben sind vom Typ `Int`</span><span class="sxs-lookup"><span data-stu-id="6890e-270">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="6890e-271">Eingabe oder Eingaben sind vom Typ `Double`</span><span class="sxs-lookup"><span data-stu-id="6890e-271">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="6890e-272">Eingabe oder Eingaben sind vom Typ `BigInt`</span><span class="sxs-lookup"><span data-stu-id="6890e-272">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-273">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-273">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-274">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-274">We suggest:</span></span>

- <span data-ttu-id="6890e-275">Wenn eine Funktion oder ein Vorgang nicht mit ähnlichen Funktionen oder Vorgängen durch die Typen und die Funktions Unterstützung Ihrer Eingaben verknüpft ist, verwenden Sie kein Suffix.</span><span class="sxs-lookup"><span data-stu-id="6890e-275">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="6890e-276">Wenn eine Funktion oder ein Vorgang mit ähnlichen Funktionen oder Vorgängen verknüpft ist, die von den Typen und der funktorunterstützung Ihrer Eingaben verwendet werden, verwenden Sie Suffixe wie in der obigen Tabelle, um Varianten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6890e-276">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-277">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-277">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="6890e-278">Argumente und Variablen</span><span class="sxs-lookup"><span data-stu-id="6890e-278">Arguments and Variables</span></span> ###

<span data-ttu-id="6890e-279">Ein wichtiges Ziel des Q #-Codes für eine Funktion oder einen Vorgang besteht darin, dass es leicht lesbar und verständlich ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-279">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="6890e-280">Ebenso sollten die Namen von Eingaben und Typargumenten kommunizieren, wie eine Funktion oder ein Argument nach der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6890e-280">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-281">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-281">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-282">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-282">We suggest:</span></span>

- <span data-ttu-id="6890e-283">Verwenden Sie für alle Variablen-und Eingabe Namen `pascalCase` mit starker Bevorzugung `CamelCase`, `snake_case`oder `ANGRY_CASE`.</span><span class="sxs-lookup"><span data-stu-id="6890e-283">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="6890e-284">Eingabe Namen sollten beschreibend sein. vermeiden Sie, wenn möglich, einen oder zwei Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="6890e-284">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="6890e-285">Vorgänge und Funktionen, die genau ein Typargument akzeptieren, sollten dieses Typargument durch `T` bezeichnen, wenn die Rolle offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-285">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="6890e-286">Wenn eine Funktion oder ein Vorgang mehrere Typargumente annimmt oder wenn die Rolle eines einzelnen Typarguments nicht offensichtlich ist, sollten Sie ein kurzes groß geschritztes Wort verwenden, das `T` (z. b. `TOutput`) für jeden Typ vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-286">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="6890e-287">Geben Sie keine Typnamen in Argument-und Variablennamen ein. Diese Informationen können von Ihrer Entwicklungsumgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-287">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="6890e-288">Kennzeichnen Sie skalare Typen nach Ihren Literalnamen (`flagQubit`) und Array Typen durch einen Plural (`measResults`).</span><span class="sxs-lookup"><span data-stu-id="6890e-288">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="6890e-289">Vor allem bei Arrays von Qubits sollten diese Typen durch `Register` gekennzeichnet werden, wobei der Name auf eine Sequenz von Qubits verweist, die in irgendeiner Weise eng miteinander verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6890e-289">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="6890e-290">Variablen, die als Indizes in Arrays verwendet werden, sollten mit `idx` beginnen und als Singular (z. b. `things[idxThing]`) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-290">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="6890e-291">Vermeiden Sie insbesondere die Verwendung von Variablennamen mit nur einem Buchstaben als Indizes. Verwenden Sie ggf. `idx`.</span><span class="sxs-lookup"><span data-stu-id="6890e-291">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="6890e-292">Variablen, die zum Speichern der Längen von Arrays verwendet werden, sollten mit `n` beginnen und pluralisiert werden (z. b.: `nThings`).</span><span class="sxs-lookup"><span data-stu-id="6890e-292">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-293">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-293">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="6890e-294">Benutzerdefinierter Typ benannte Elemente</span><span class="sxs-lookup"><span data-stu-id="6890e-294">User Defined Type Named Items</span></span> ###

<span data-ttu-id="6890e-295">Benannte Elemente in benutzerdefinierten Typen sollten als `CamelCase`benannt werden, auch als Eingabe für UDT-Konstruktoren.</span><span class="sxs-lookup"><span data-stu-id="6890e-295">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="6890e-296">Dadurch können benannte Elemente bei Verwendung der accessornotation (z. b.: `callable::Apply`) oder der Copy-and-Update-Notation (`set arr w/= Data <- newData`) eindeutig von Verweisen auf lokale Variablen getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-296">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-297">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-297">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-298">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-298">We suggest:</span></span>

- <span data-ttu-id="6890e-299">Benannte Elemente in UDT-Konstruktoren sollten als `CamelCase`benannt werden. Das heißt, Sie sollten mit einem anfänglichen Großbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="6890e-299">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="6890e-300">Benannte Elemente, die in Vorgänge aufgelöst werden, sollten als Verb Phasen benannt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-300">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="6890e-301">Benannte Elemente, die nicht in Vorgänge aufgelöst werden, sollten als nominale Ausdrücke benannt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-301">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="6890e-302">Für UDTs, die Vorgänge einschließen, sollte ein einzelnes benanntes Element namens "`Apply`" definiert werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-302">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-303">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-303">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="6890e-304">Ausschnitt</span><span class="sxs-lookup"><span data-stu-id="6890e-304">Snippet</span></span> | <span data-ttu-id="6890e-305">description</span><span class="sxs-lookup"><span data-stu-id="6890e-305">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="6890e-306">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-306">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="6890e-307">Der Name `Apply` ist ein `CamelCase`formatierter Verb Ausdruck, der darauf hinweist, dass das benannte Element ein Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-307">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="6890e-308">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-308">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="6890e-309">Benannte Elemente sollten mit einem ersten Großbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="6890e-309">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="6890e-310">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-310">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="6890e-311">Benannte Elemente, die in Functions aufgelöst werden, sollten als nominale Ausdrücke und nicht als Verb Ausdrücke benannt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-311">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="6890e-312">Eingabe Konventionen</span><span class="sxs-lookup"><span data-stu-id="6890e-312">Input Conventions</span></span> ##

<span data-ttu-id="6890e-313">Wenn ein Entwickler einen Vorgang oder eine Funktion aufruft, müssen die verschiedenen Eingaben für diesen Vorgang bzw. diese Funktion in einer bestimmten Reihenfolge angegeben werden. dadurch erhöht sich die kognitive Auslastung eines Entwicklers, um eine Bibliothek verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="6890e-313">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="6890e-314">Vor allem ist die Aufgabe des hintergabeorderings häufig eine Ablenkungs Maßnahme von der Aufgabe, die eine Implementierung eines Quantum-Algorithmus zu programmieren.</span><span class="sxs-lookup"><span data-stu-id="6890e-314">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="6890e-315">Obwohl die Unterstützung für umfangreiche IDE dies sehr stark mindern kann, kann ein guter Entwurf und die Einhaltung allgemeiner Konventionen dazu beitragen, die durch eine API erzwungene kognitive Auslastung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="6890e-315">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="6890e-316">Wenn möglich, kann es hilfreich sein, die Anzahl der Eingaben zu verringern, die von einem Vorgang oder einer Funktion erwartet werden, damit die Rolle der einzelnen Eingaben sowohl für Entwickler, die diesen Vorgang oder diese Funktion aufrufen, als auch für Entwickler, die diesen Code später lesen, gleichzeitig offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-316">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="6890e-317">Besonders wenn es nicht möglich oder sinnvoll ist, die Anzahl der Argumente für einen Vorgang oder eine Funktion zu reduzieren, ist es wichtig, dass eine konsistente Reihenfolge vorhanden ist, die die Überraschung des Benutzers beim Vorhersagen der Reihenfolge der Eingaben minimiert.</span><span class="sxs-lookup"><span data-stu-id="6890e-317">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="6890e-318">Wir empfehlen eine Eingabe Reihenfolge Konventionen, die größtenteils von der Betrachtung einer partiellen Anwendung als Generalisierung von f (x, y) ≡ f (x) (y) abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-318">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="6890e-319">Folglich sollte das partielle anwenden der ersten Argumente zu einem Aufruf baren Ergebnis führen, das immer nützlich ist, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-319">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="6890e-320">Nach diesem Prinzip sollten Sie die folgende Reihenfolge von Argumenten verwenden:</span><span class="sxs-lookup"><span data-stu-id="6890e-320">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="6890e-321">Klassische, nicht Aufruf Bare Argumente, wie z. b. Winkel, Vektoren von Mächten usw.</span><span class="sxs-lookup"><span data-stu-id="6890e-321">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="6890e-322">Aufruf Bare Argumente (Funktionen und Argumente).</span><span class="sxs-lookup"><span data-stu-id="6890e-322">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="6890e-323">Wenn sowohl Funktionen als auch Vorgänge als Argumente verwendet werden, erwägen Sie das Platzieren von Vorgängen nach Funktionen.</span><span class="sxs-lookup"><span data-stu-id="6890e-323">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="6890e-324">Auflistungen, auf die durch Aufruf Bare Argumente in ähnlicher Weise wie `Map`, `Iter`, `Enumerate`und `Fold`agiert werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-324">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="6890e-325">Als Steuerelemente verwendete Qubit-Argumente.</span><span class="sxs-lookup"><span data-stu-id="6890e-325">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="6890e-326">Als Ziele verwendete Qubit-Argumente.</span><span class="sxs-lookup"><span data-stu-id="6890e-326">Qubit arguments used as targets.</span></span>

<span data-ttu-id="6890e-327">Angenommen, ein Vorgang `ApplyPhaseEstimationIteration` für die Verwendung in der Phasen Schätzung mit einem Winkel und einem Oracle, übergibt den Winkel an `Rz`, der von einem Array mit unterschiedlichen Skalierungsfaktoren geändert wurde, und steuert dann Anwendungen des Oracle.</span><span class="sxs-lookup"><span data-stu-id="6890e-327">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="6890e-328">Die Eingaben werden auf folgende Weise `ApplyPhaseEstimationIteration` sortiert:</span><span class="sxs-lookup"><span data-stu-id="6890e-328">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

```qsharp
operation ApplyPhaseEstimationIteration(
    angle : Double,
    callable : (Qubit => () is Ctl),
    scaleFactors : Double[],
    controlQubit : Qubit,
    targetQubits : Qubit[]
)
: Unit
...
```
<span data-ttu-id="6890e-329">Im besonderen Fall, dass eine Überraschung minimiert wird, imitieren einige Funktionen und Vorgänge das Verhalten der integrierten Funktoren `Adjoint` und `Controlled`.</span><span class="sxs-lookup"><span data-stu-id="6890e-329">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="6890e-330">`ControlledOnInt<'T>` z. b. den Typ `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, sodass `ControlledOnInt<Qubit[]>(5, _)` wie das `Controlled`-Funktor verhält, aber auf der Bedingung, dass das Steuerelement registriert den Status $ \ket{5} = \ket{101}$ darstellt.</span><span class="sxs-lookup"><span data-stu-id="6890e-330">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="6890e-331">Folglich erwartet ein Entwickler, dass die Eingaben, die die zu transformierende Aufruf Bare `ControlledOnInt` platzieren, und dass der resultierende Vorgang als Eingabe `(Qubit[], 'T)`---dieselbe Reihenfolge wie die Ausgabe des `Controlled`-funktors annimmt.</span><span class="sxs-lookup"><span data-stu-id="6890e-331">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-332">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-332">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-333">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-333">We suggest:</span></span>

- <span data-ttu-id="6890e-334">Verwenden Sie Eingabe Sortierungen in Übereinstimmung mit der Verwendung der partiellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6890e-334">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="6890e-335">Verwenden Sie Eingabe Sortierungen, die mit integrierten Funktoren konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="6890e-335">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="6890e-336">Platzieren Sie alle klassischen Eingaben vor allen Quantum-Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6890e-336">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-337">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-337">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="6890e-338">Dokumentations Konventionen</span><span class="sxs-lookup"><span data-stu-id="6890e-338">Documentation Conventions</span></span> ##

<span data-ttu-id="6890e-339">Die Q #-Sprache ermöglicht das Anfügen von Dokumentationen an Vorgänge, Funktionen und benutzerdefinierte Typen durch die Verwendung von speziell formatierten Dokumentations Kommentaren.</span><span class="sxs-lookup"><span data-stu-id="6890e-339">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="6890e-340">Diese Dokumentations Kommentare sind durch Triple-Schrägstriche (`///`) gekennzeichnet und enthalten kleine, mit [docfx optimierte markdown-](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) Dokumente, mit denen der Zweck der einzelnen Vorgänge, Funktionen und benutzerdefinierten Typen beschrieben werden kann, welche Eingaben jeweils erwartet werden usw.</span><span class="sxs-lookup"><span data-stu-id="6890e-340">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="6890e-341">Der mit dem Quantum Development Kit bereitgestellte Compiler extrahiert diese Kommentare und verwendet diese, um die besitzen-Dokumentation in https://docs.microsoft.com/quantum zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6890e-341">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="6890e-342">Entsprechend verwendet der mit dem Quantum Development Kit bereitgestellte Sprachserver diese Kommentare, um Benutzern Hilfe zu bieten, wenn Sie mit dem Mauszeiger auf Symbole in Ihrem Q #-Code zeigen.</span><span class="sxs-lookup"><span data-stu-id="6890e-342">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="6890e-343">Durch die Verwendung von Dokumentations Kommentaren können Benutzer den Code sinnvoll machen, indem Sie einen nützlichen Verweis auf Details bereitstellen, die nicht ohne weiteres mit den anderen Konventionen in diesem Dokument ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-343">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

<div class="nextstepaction"><span data-ttu-id="6890e-344">
    [Syntax Referenz für Dokumentations Kommentare](xref:microsoft.quantum.language.statements#documentation-comments)
</span><span class="sxs-lookup"><span data-stu-id="6890e-344">
    [Documentation comment syntax reference](xref:microsoft.quantum.language.statements#documentation-comments)
</span></span></div>

<span data-ttu-id="6890e-345">Um diese Funktionalität für Benutzer effektiv nutzen zu können, empfiehlt es sich, beim Schreiben von Dokumentations Kommentaren einige Punkte zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="6890e-345">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-346">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-346">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="6890e-347">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-347">We suggest:</span></span>

- <span data-ttu-id="6890e-348">Jeder öffentlichen Funktion, jedem Vorgang und jedem benutzerdefinierten Typ sollte unmittelbar ein Dokumentations Kommentar vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-348">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="6890e-349">Jeder Dokumentations Kommentar sollte mindestens die folgenden Abschnitte enthalten:</span><span class="sxs-lookup"><span data-stu-id="6890e-349">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="6890e-350">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6890e-350">Summary</span></span>
    - <span data-ttu-id="6890e-351">Eingabe</span><span class="sxs-lookup"><span data-stu-id="6890e-351">Input</span></span>
    - <span data-ttu-id="6890e-352">Ausgabe (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="6890e-352">Output (if applicable)</span></span>
- <span data-ttu-id="6890e-353">Stellen Sie sicher, dass alle Zusammenfassungen zwei oder weniger Sätze sind.</span><span class="sxs-lookup"><span data-stu-id="6890e-353">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="6890e-354">Wenn mehr Platz benötigt wird, stellen Sie einen `# Description` Abschnitt direkt nach `# Summary` mit umfassenden Details bereit.</span><span class="sxs-lookup"><span data-stu-id="6890e-354">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="6890e-355">Wenn Sie vernünftig Vorgehen, sollten Sie mathematische nicht in Zusammenfassungen einschließen, da nicht alle Clients eine TeX-Notation in Zusammenfassungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6890e-355">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="6890e-356">Beachten Sie, dass beim Schreiben von Prosa Dokumenten (z. b. tex oder markdown) die Verwendung längerer Zeilenlängen vorzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="6890e-356">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="6890e-357">Stellen Sie im Abschnitt "`# Description`" alle relevanten mathematischen Ausdrücke bereit.</span><span class="sxs-lookup"><span data-stu-id="6890e-357">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="6890e-358">Wenn Sie Eingaben beschreiben, wiederholen Sie nicht die Typen der einzelnen Eingaben, da diese vom Compiler abgeleitet werden können, und das Risiko der Inkonsistenz.</span><span class="sxs-lookup"><span data-stu-id="6890e-358">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="6890e-359">Geben Sie nach Bedarf Beispiele an, die jeweils in Ihrem eigenen `# Example` Abschnitt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6890e-359">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="6890e-360">Beschreiben Sie kurz die einzelnen Beispiele, bevor Sie Code auflisten.</span><span class="sxs-lookup"><span data-stu-id="6890e-360">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="6890e-361">Nennen Sie alle relevanten akademischen Veröffentlichungen (z. b. Beiträge, Verfahren, Blogbeiträge und alternative Implementierungen) in einem `# References` Abschnitt als Auflistungs Liste mit Links.</span><span class="sxs-lookup"><span data-stu-id="6890e-361">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="6890e-362">Stellen Sie sicher, dass, sofern möglich, alle anfügelinks zu permanenten und unveränderlichen bezeichmern (Dois-oder versionierte arXiv-Nummern) gehören.</span><span class="sxs-lookup"><span data-stu-id="6890e-362">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="6890e-363">Wenn ein Vorgang oder eine Funktion mit anderen Vorgängen oder Funktionen verknüpft ist, können Sie im `# See Also` Abschnitt andere Varianten als Aufzählungs Zeichen auflisten.</span><span class="sxs-lookup"><span data-stu-id="6890e-363">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="6890e-364">Belassen Sie eine leere Kommentar Linie zwischen den Abschnitten der Ebene 1 (`/// #`), aber lassen Sie keine Leerzeile zwischen den Abschnitten der Ebene 2 (`/// ##`).</span><span class="sxs-lookup"><span data-stu-id="6890e-364">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-365">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-365">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="6890e-366">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-366">☑</span></span> ####

```
/// # Summary
/// Applies a rotation about the X-axis by a given angle.
///
///
/// # Description
/// This operation rotates a single qubit by the unitary operation
/// \begin{align}
///     R_x(\theta) \mathrel{:=} e^{-i \theta \sigma_x / 2}.
/// \end{align}
///
/// # Input
/// ## theta
/// Angle about which the qubit is to be rotated.
/// ## qubit
/// Qubit to which the gate should be applied.
///
/// # Remarks
/// Equivalent to:
/// ```qsharp
/// R(PauliX, theta, qubit);
/// ```
///
/// # See Also
/// - Ry
/// - Rz
operation Rx(theta : Double, qubit : Qubit) : Unit
is Adj + Ctl {
    body (...) { R(PauliX, theta, qubit); }
    adjoint (...) { R(PauliX, -theta, qubit); }
}
```

***

## <a name="formatting-conventions"></a><span data-ttu-id="6890e-367">Formatierungs Konventionen</span><span class="sxs-lookup"><span data-stu-id="6890e-367">Formatting Conventions</span></span> ##

<span data-ttu-id="6890e-368">Zusätzlich zu den oben genannten Vorschlägen ist es hilfreich, den Code so lesbar wie möglich zu machen, um konsistente Formatierungs Regeln zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6890e-368">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="6890e-369">Diese Formatierungs Regeln sind eher willkürlich und stark bis zur persönlichen Ästhetik.</span><span class="sxs-lookup"><span data-stu-id="6890e-369">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="6890e-370">Trotzdem empfiehlt es sich, einen konsistenten Satz von Formatierungs Konventionen innerhalb einer Gruppe von Projektmitarbeitern zu verwalten, insbesondere für große Q #-Projekte wie das Quantum Development Kit selbst.</span><span class="sxs-lookup"><span data-stu-id="6890e-370">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="6890e-371">Diese Regeln können automatisch mithilfe des in den f #-Compiler integrierten Formatierungs Tools angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-371">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidancetabguidance"></a>[<span data-ttu-id="6890e-372">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="6890e-372">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="6890e-373">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6890e-373">We suggest:</span></span>

- <span data-ttu-id="6890e-374">Verwenden Sie vier Leerzeichen anstelle von Registerkarten für die Portabilität.</span><span class="sxs-lookup"><span data-stu-id="6890e-374">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="6890e-375">Beispielsweise in vs Code:</span><span class="sxs-lookup"><span data-stu-id="6890e-375">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="6890e-376">Zeilenumbruch um 79 Zeichen, soweit angemessen.</span><span class="sxs-lookup"><span data-stu-id="6890e-376">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="6890e-377">Verwenden Sie Leerzeichen um binäre Operatoren.</span><span class="sxs-lookup"><span data-stu-id="6890e-377">Use spaces around binary operators.</span></span>
- <span data-ttu-id="6890e-378">Verwenden Sie Leerzeichen auf beiden Seiten von Doppelpunkten, die für Typanmerkungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-378">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="6890e-379">Verwenden Sie ein einzelnes Leerzeichen nach Kommas, das in Array-und tupelliteralen verwendet wird (z. b. in Eingaben für Funktionen und Vorgänge).</span><span class="sxs-lookup"><span data-stu-id="6890e-379">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="6890e-380">Verwenden Sie keine Leerzeichen nach Funktions-, Vorgangs-oder UDT-Namen oder nach dem `@` in Attribut Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="6890e-380">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="6890e-381">Jede Attribut Deklaration sollte sich in einer eigenen Zeile befinden.</span><span class="sxs-lookup"><span data-stu-id="6890e-381">Each attribute declaration should be on its own line.</span></span>

# <a name="examplestabexamples"></a>[<span data-ttu-id="6890e-382">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6890e-382">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="6890e-383">Ausschnitt</span><span class="sxs-lookup"><span data-stu-id="6890e-383">Snippet</span></span> | <span data-ttu-id="6890e-384">description</span><span class="sxs-lookup"><span data-stu-id="6890e-384">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="6890e-385">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-385">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="6890e-386">Verwenden Sie Leerzeichen um binäre Operatoren.</span><span class="sxs-lookup"><span data-stu-id="6890e-386">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="6890e-387">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-387">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="6890e-388">Verwenden Sie Leerzeichen um Doppelpunkte der Typanmerkung.</span><span class="sxs-lookup"><span data-stu-id="6890e-388">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="6890e-389">☑</span><span class="sxs-lookup"><span data-stu-id="6890e-389">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="6890e-390">Elemente im eingabetupel sind zur besseren Lesbarkeit ordnungsgemäß verteilt.</span><span class="sxs-lookup"><span data-stu-id="6890e-390">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="6890e-391">☒</span><span class="sxs-lookup"><span data-stu-id="6890e-391">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="6890e-392">Leerzeichen sollten nach Funktions-, Vorgangs-oder UDT-Namen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="6890e-392">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***
