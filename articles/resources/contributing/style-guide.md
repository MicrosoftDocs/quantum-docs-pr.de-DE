---
title: Microsoft- Q# Styleguide
description: Erlernen Sie die Benennungs-, Eingabe-, Dokumentations-und Formatierungs Konventionen für Q# Programme und Bibliotheken.
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.style
no-loc:
- Q#
- $$v
ms.openlocfilehash: 27a2ae5ae9d00329fc369268edae24228a9a9d0d
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867588"
---
# <a name="no-locq-style-guide"></a><span data-ttu-id="fdd6e-103">Q#Styleguide</span><span class="sxs-lookup"><span data-stu-id="fdd6e-103">Q# Style Guide</span></span> #
## <a name="general-conventions"></a><span data-ttu-id="fdd6e-104">Allgemeine Konventionen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-104">General Conventions</span></span> ##

<span data-ttu-id="fdd6e-105">Die in diesem Handbuch empfohlenen Konventionen sollen Ihnen helfen, Programme und Bibliotheken Q# leichter zu lesen und zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-105">The conventions suggested in this guide are intended to help make programs and libraries written in Q# easier to read and understand.</span></span>

## <a name="guidance"></a><span data-ttu-id="fdd6e-106">Anleitung</span><span class="sxs-lookup"><span data-stu-id="fdd6e-106">Guidance</span></span>

<span data-ttu-id="fdd6e-107">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-107">We suggest:</span></span>

- <span data-ttu-id="fdd6e-108">Ignorieren Sie niemals eine Konvention, wenn Sie dies nicht absichtlich tun, um für Ihre Benutzer besser lesbaren und verständlichen Code bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-108">Never disregard a convention unless you’re doing so intentionally in order to provide more readable and understandable code for your users.</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="fdd6e-109">Namenskonventionen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-109">Naming Conventions</span></span> ##

<span data-ttu-id="fdd6e-110">Beim anbieten des quantumentwicklungskit werden Funktions-und Vorgangs Namen unterstützt, mit denen Quantum-Entwickler Programme schreiben können, die leicht lesbar sind und die überraschen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-110">In offering the Quantum Development Kit, we strive for function and operation names that help quantum developers write programs that are easy to read and that minimize surprise.</span></span>
<span data-ttu-id="fdd6e-111">Ein wichtiger Aspekt dabei ist, dass wir bei der Auswahl von Namen für Funktionen, Vorgänge und Typen das *Vokabular* einrichten, mit dem Programmierer Quantum-Konzepte Ausdrücken. mit unseren Optionen können wir Sie bei der klaren Kommunikation unterstützen oder behindern.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-111">An important part of that is that when we choose names for functions, operations, and types, we are establishing the *vocabulary* that programmers use to express quantum concepts; with our choices, we either help or hinder them in their effort to clearly communicate.</span></span>
<span data-ttu-id="fdd6e-112">Dies liegt in der Verantwortung für uns, sicherzustellen, dass die Namen, die wir einführen, eher Klarheit bieten als Verschleierung.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-112">This places a responsibility on us to make sure that the names we introduce offer clarity rather than obscurity.</span></span>
<span data-ttu-id="fdd6e-113">In diesem Abschnitt erfahren Sie, wie wir diese Verpflichtung in Bezug auf eine explizite Anleitung erfüllen, die uns bei der optimalen Durchführung der Q# Entwicklungs Community unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-113">In this section, we detail how we meet this obligation in terms of explicit guidance that helps us do the best by the Q# development community.</span></span>

### <a name="operations-and-functions"></a><span data-ttu-id="fdd6e-114">Vorgänge und Funktionen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-114">Operations and Functions</span></span> ###

<span data-ttu-id="fdd6e-115">Eines der ersten Dinge, die ein Name einrichten sollte, ist, ob ein bestimmtes Symbol eine Funktion oder einen Vorgang darstellt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-115">One of the first things that a name should establish is whether a given symbol represents a function or an operation.</span></span>
<span data-ttu-id="fdd6e-116">Der Unterschied zwischen Funktionen und Vorgängen ist wichtig, um zu verstehen, wie sich ein Codeblock verhält.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-116">The difference between functions and operations is critical to understanding how a block of code behaves.</span></span>
<span data-ttu-id="fdd6e-117">Um den Unterschied zwischen Funktionen und Vorgängen an Benutzer zu übermitteln, basieren wir auf der Q# Verwendung von Nebeneffekten darauf, dass die Quantum-Vorgänge modelliert werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-117">To communicate the distinction between functions and operations to users, we rely on that Q# models quantum operations through the use of side effects.</span></span>
<span data-ttu-id="fdd6e-118">Dies *bedeutet* , dass ein Vorgang etwas bewirkt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-118">That is, an operation *does* something.</span></span>

<span data-ttu-id="fdd6e-119">Im Gegensatz dazu beschreiben Funktionen die mathematischen Beziehungen zwischen den Daten.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-119">By contrast, functions describe the mathematical relationships between data.</span></span>
<span data-ttu-id="fdd6e-120">Der Ausdruck `Sin(PI() / 2.0)` *ist* `1.0` , und impliziert nichts über den Zustand eines Programms oder seiner Qubits.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-120">The expression `Sin(PI() / 2.0)` *is* `1.0`, and implies nothing about the state of a program or its qubits.</span></span>

<span data-ttu-id="fdd6e-121">Durch die Zusammenfassung werden Vorgänge ausgeführt, während Functions Dinge sind.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-121">Summarizing, operations do things while functions are things.</span></span>
<span data-ttu-id="fdd6e-122">Dieser Unterschied schlägt vor, dass wir Vorgänge als Verben und Funktionen als Nomen benennen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-122">This distinction suggests that we name operations as verbs and functions as nouns.</span></span>

> [!NOTE]
> <span data-ttu-id="fdd6e-123">Wenn ein benutzerdefinierter Typ deklariert wird, wird eine neue Funktion, die Instanzen dieses Typs erstellt, gleichzeitig implizit definiert.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-123">When a user-defined type is declared, a new function that constructs instances of that type is implicitly defined at the same time.</span></span>
> <span data-ttu-id="fdd6e-124">Aus dieser Sicht sollten benutzerdefinierte Typen als Nomen benannt werden, damit der Typ selbst und die Konstruktorfunktion konsistente Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-124">From that perspective, user-defined types should be named as nouns so that both the type itself and the constructor function have consistent names.</span></span>

<span data-ttu-id="fdd6e-125">Stellen Sie in angemessener Weise sicher, dass Vorgangs Namen mit Verben beginnen, die die Auswirkungen des Vorgangs eindeutig angeben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-125">Where reasonable, ensure that operation names begin with verbs that clearly indicate the effect taken by the operation.</span></span>
<span data-ttu-id="fdd6e-126">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-126">For example:</span></span>

- `MeasureInteger`
- `EstimateEnergy`
- `SampleInt`

<span data-ttu-id="fdd6e-127">Ein Fall, der besondere Erwähnung verdient, ist, wenn ein Vorgang einen anderen Vorgang als Eingabe annimmt und ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-127">One case that deserves special mention is when an operation takes another operation as input and calls it.</span></span>
<span data-ttu-id="fdd6e-128">In solchen Fällen ist die vom Eingabevorgang ausgeführte Aktion nicht klar, wenn der äußere Vorgang definiert ist, sodass das Rechte Verb nicht sofort gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-128">In such cases, the action taken by the input operation is not clear when the outer operation is defined, such that the right verb is not immediately clear.</span></span>
<span data-ttu-id="fdd6e-129">Wir empfehlen das Verb `Apply` , wie in `ApplyIf` , `ApplyToEach` und `ApplyToFirst` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-129">We recommend the verb `Apply`, as in `ApplyIf`, `ApplyToEach`, and `ApplyToFirst`.</span></span>
<span data-ttu-id="fdd6e-130">Andere Verben können auch in diesem Fall nützlich sein, wie in `IterateThroughCartesianPower` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-130">Other verbs may be useful in this case as well, as in `IterateThroughCartesianPower`.</span></span>

| <span data-ttu-id="fdd6e-131">Verb</span><span class="sxs-lookup"><span data-stu-id="fdd6e-131">Verb</span></span> | <span data-ttu-id="fdd6e-132">Erwarteter Effekt</span><span class="sxs-lookup"><span data-stu-id="fdd6e-132">Expected Effect</span></span> |
| ---- | ------ |
| <span data-ttu-id="fdd6e-133">Anwenden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-133">Apply</span></span> | <span data-ttu-id="fdd6e-134">Ein als Eingabe bereitgestellter Vorgang wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-134">An operation provided as input is called</span></span> |
| <span data-ttu-id="fdd6e-135">Assert</span><span class="sxs-lookup"><span data-stu-id="fdd6e-135">Assert</span></span> | <span data-ttu-id="fdd6e-136">Eine Hypothese über das Ergebnis einer möglichen Quantum-Messung wird von einem Simulator geprüft.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-136">A hypothesis about the outcome of a possible quantum measurement is checked by a simulator</span></span> |
| <span data-ttu-id="fdd6e-137">Schätzungen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-137">Estimate</span></span> | <span data-ttu-id="fdd6e-138">Ein klassischer Wert wird zurückgegeben, der eine Schätzung darstellt, die aus einer oder mehreren Messungen gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-138">A classical value is returned, representing an estimate drawn from one or more measurements</span></span> |
| <span data-ttu-id="fdd6e-139">"Measure"</span><span class="sxs-lookup"><span data-stu-id="fdd6e-139">Measure</span></span> | <span data-ttu-id="fdd6e-140">Eine Quantum-Messung wird ausgeführt, und das Ergebnis wird an den Benutzer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-140">A quantum measurement is performed, and its result is returned to the user</span></span> |
| <span data-ttu-id="fdd6e-141">Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="fdd6e-141">Prepare</span></span> | <span data-ttu-id="fdd6e-142">Ein bestimmtes Register von Qubits wird in einem bestimmten Zustand initialisiert.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-142">A given register of qubits is initialized into a particular state</span></span> |
| <span data-ttu-id="fdd6e-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fdd6e-143">Sample</span></span> | <span data-ttu-id="fdd6e-144">Ein klassischer Wert wird nach dem Zufallsprinzip aus einer Verteilung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-144">A classical value is returned at random from some distribution</span></span> |

<span data-ttu-id="fdd6e-145">Bei Functions empfiehlt es sich, die Verwendung von Verben anstelle von gängigen Substantiven zu vermeiden (siehe Anleitungen zu den richtigen Nomen unten) oder Adjektive:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-145">For functions, we suggest avoiding the use of verbs in favor of common nouns (see guidance on proper nouns below) or adjectives:</span></span>

- `ConstantArray`
- `Head`
- `LookupFunction`

<span data-ttu-id="fdd6e-146">Vor allem empfiehlt es sich in fast allen Fällen, frühere Partizipationen zu verwenden, wenn dies angebracht ist, um anzugeben, dass ein Funktionsname an anderer Stelle in einem Quantum-Programm mit einer Aktion oder einem Nebeneffekt verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-146">In particular, in almost all cases, we suggest using past participles where appropriate to indicate that a function name is strongly connected to an action or side effect elsewhere in a quantum program.</span></span>
<span data-ttu-id="fdd6e-147">Verwendet beispielsweise `ControlledOnInt` die Form teilnehmen des Verbs "Control", um anzugeben, dass die Funktion als Adjektiv fungiert, um das Argument zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-147">For example,  `ControlledOnInt` uses the part participle form of the verb "control" to indicate that the function acts as an adjective to modify its argument.</span></span>
<span data-ttu-id="fdd6e-148">Dieser Name hat den zusätzlichen Vorteil, dass die Semantik des integrierten `Controlled` funktors übereinstimmt, wie weiter unten erläutert.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-148">This name has the additional benefit of matching the semantics of the built-in `Controlled` functor, as discussed further below.</span></span>
<span data-ttu-id="fdd6e-149">Ebenso können- _Agent-Nomen_ verwendet werden, um Funktions-und UDT-Namen aus Vorgangs Namen zu erstellen, wie im Fall des namens `Encoder` für einen UDT, der stark zugeordnet ist `Encode` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-149">Similarly, _agent nouns_ can be used to construct function and UDT names from operation names, as in the case of the name `Encoder` for a UDT that is strongly associated with `Encode`.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-150">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-150">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-151">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-151">We suggest:</span></span>

- <span data-ttu-id="fdd6e-152">Verwenden Sie Verben für Vorgangs Namen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-152">Use verbs for operation names.</span></span>
- <span data-ttu-id="fdd6e-153">Verwenden Sie Nomen oder Adjektive für Funktionsnamen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-153">Use nouns or adjectives for function names.</span></span>
- <span data-ttu-id="fdd6e-154">Verwenden Sie Nomen für benutzerdefinierte Typen und Attribute.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-154">Use nouns for user-defined types and attributes.</span></span>
- <span data-ttu-id="fdd6e-155">Verwenden Sie für alle Aufruf baren Namen eine `CamelCase` starke Bevorzugung von `pascalCase` , `snake_case` oder `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-155">For all callable names, use `CamelCase` in strong preference to `pascalCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="fdd6e-156">Stellen Sie insbesondere sicher, dass Aufruf Bare Namen mit Großbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-156">In particular, ensure that callable names start with uppercase letters.</span></span>
- <span data-ttu-id="fdd6e-157">Verwenden Sie für alle lokalen Variablen `pascalCase` die starke bevorzugte Einstellung für `CamelCase` , `snake_case` oder `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-157">For all local variables, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span> <span data-ttu-id="fdd6e-158">Stellen Sie insbesondere sicher, dass lokale Variablen mit Kleinbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-158">In particular, ensure that local variables start with lowercase letters.</span></span>
- <span data-ttu-id="fdd6e-159">Vermeiden Sie die Verwendung von unterstrichen `_` in Funktions-und Vorgangs Namen. wenn zusätzliche Ebenen der Hierarchie erforderlich sind, verwenden Sie Namespaces und Namespace Aliase.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-159">Avoid the use of underscores `_` in function and operation names; where additional levels of hierarchy are needed, use namespaces and namespace aliases.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-160">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-160">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-161">Name</span><span class="sxs-lookup"><span data-stu-id="fdd6e-161">Name</span></span> | <span data-ttu-id="fdd6e-162">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-162">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fdd6e-163">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-163">☑</span></span> | `operation ReflectAboutStart` | <span data-ttu-id="fdd6e-164">Löschen Sie die Verwendung eines Verbs ("reflektieren"), um die Auswirkung des Vorgangs anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-164">Clear use of a verb ("reflect") to indicate the effect of the operation.</span></span> |
| <span data-ttu-id="fdd6e-165">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-165">☒</span></span> | <s>`operation XRotation`</s> | <span data-ttu-id="fdd6e-166">Die Verwendung von Substantiv Phrase schlägt eine Funktion anstelle von Operation vor.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-166">Use of noun phrase suggests function, rather than operation.</span></span> |
| <span data-ttu-id="fdd6e-167">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-167">☒</span></span> | <s>`operation search_oracle`</s> | <span data-ttu-id="fdd6e-168">Die Verwendung von verstößt gegen die `snake_case` Q# Notation.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-168">Use of `snake_case` contravenes Q# notation.</span></span> |
| <span data-ttu-id="fdd6e-169">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-169">☒</span></span> | <s>`operation Search_Oracle`</s> | <span data-ttu-id="fdd6e-170">Die Verwendung von unterstrichen, die intern für den Vorgangs Namen verwendet werden, verstößt Q#</span><span class="sxs-lookup"><span data-stu-id="fdd6e-170">Use of underscores internal to operation name contravenes Q# notation.</span></span> |
| <span data-ttu-id="fdd6e-171">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-171">☑</span></span> | `function StatePreparationOracle` | <span data-ttu-id="fdd6e-172">Die Verwendung des Substantiv Ausdrucks deutet darauf hin, dass die Funktion einen Vorgang zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-172">Use of noun phrase suggests that the function returns an operation.</span></span> |
| <span data-ttu-id="fdd6e-173">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-173">☑</span></span> | `function EqualityFact` | <span data-ttu-id="fdd6e-174">Löschen Sie die Verwendung von Substantiv ("Fakt"), um anzugeben, dass es sich hierbei um eine Funktion handelt, während das Adjektiv ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-174">Clear use of noun ("fact") to indicate that this is a function, while the adjective.</span></span> |
| <span data-ttu-id="fdd6e-175">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-175">☒</span></span> | <s>`function GetRotationAngles`</s> | <span data-ttu-id="fdd6e-176">Die Verwendung von Verb ("Get") deutet darauf hin, dass es sich hierbei um einen Vorgang handelt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-176">Use of verb ("get") suggests that this is an operation.</span></span> |
| <span data-ttu-id="fdd6e-177">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-177">☑</span></span> | `newtype GeneratorTerm` | <span data-ttu-id="fdd6e-178">Die Verwendung des Substantiv Ausdrucks verweist eindeutig auf das Ergebnis des Aufrufs des UDT-Konstruktors.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-178">Use of noun phrase clearly refers to the result of calling the UDT constructor.</span></span> |
| <span data-ttu-id="fdd6e-179">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-179">☒</span></span> | <s>`@Attribute() newtype RunOnce()`</s> | <span data-ttu-id="fdd6e-180">Die Verwendung des Verb Ausdrucks deutet darauf hin, dass der UDT-Konstruktor ein Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-180">Use of verb phrase suggests that the UDT constructor is an operation.</span></span> |
| <span data-ttu-id="fdd6e-181">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-181">☑</span></span> | `@Attribute() newtype Deprecated(Reason : String)` | <span data-ttu-id="fdd6e-182">Die Verwendung des nominalen Ausdrucks kommuniziert mit der Verwendung des-Attributs.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-182">Use of noun phrase communicates the use of the attribute.</span></span> |

***

### <a name="entry-points"></a><span data-ttu-id="fdd6e-183">Einstiegspunkte</span><span class="sxs-lookup"><span data-stu-id="fdd6e-183">Entry Points</span></span>

<span data-ttu-id="fdd6e-184">Beim Definieren eines Einstiegs Punkts in ein Q# Programm erkennt der Q# Compiler das- [ `@EntryPoint()` Attribut](xref:microsoft.quantum.core.entrypoint) , sodass die Einstiegspunkte einen bestimmten Namen aufweisen (z. b. `main` , `Main` oder `__main__` ).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-184">When defining an entry point into a Q# program, the Q# compiler recognizes the [`@EntryPoint()` attribute](xref:microsoft.quantum.core.entrypoint) rather requiring that entry points have a particular name (e.g.: `main`, `Main`, or `__main__`).</span></span>
<span data-ttu-id="fdd6e-185">Aus Sicht eines Q# Entwicklers sind Einstiegspunkte also normale Vorgänge, die mit kommentiert werden `@EntryPoint()` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-185">That is, from the perspective of a Q# developer, entry points are ordinary operations annotated with `@EntryPoint()`.</span></span>
<span data-ttu-id="fdd6e-186">Außerdem sind Q# Einstiegspunkte möglicherweise Einstiegspunkte für eine gesamte Anwendung (d. h. in Q# eigenständigen ausführbaren Dateien), oder es kann sich um eine Schnittstelle zwischen einem Q# Programm und dem Host Programm für eine Anwendung handeln (d.h. bei Verwendung Q# von mit Python oder .net), sodass der Name "Main" irreführend sein kann, wenn er auf einen Q# Einstiegspunkt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-186">Moreover, Q# entry points may be entry points for an entire application (i.e.: in Q# standalone executables), or may be an interface between a Q# program and the host program for an application (i.e.: when using Q# with Python or .NET), such that the name "main" could be misleading when applied to a Q# entry point.</span></span>

<span data-ttu-id="fdd6e-187">Wir empfehlen die Verwendung von Benennungs Einstiegspunkten, um die Verwendung des `@EntryPoint()` Attributs anhand der allgemeinen Ratschläge für Benennungs Vorgänge widerzuspiegeln, die oben aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-187">We suggest using naming entry points to reflect the use of the `@EntryPoint()` attribute by using the general advice for naming operations listed above.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="fdd6e-188">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-188">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-189">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-189">We suggest:</span></span>

- <span data-ttu-id="fdd6e-190">Benennen Sie keine Einstiegspunkt Vorgänge als "Main".</span><span class="sxs-lookup"><span data-stu-id="fdd6e-190">Do not name entry point operations as "main."</span></span>
- <span data-ttu-id="fdd6e-191">Name der Einstiegspunkt Vorgänge als normale Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-191">Name entry point operations as ordinary operations.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-192">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-192">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-193">Name</span><span class="sxs-lookup"><span data-stu-id="fdd6e-193">Name</span></span> | <span data-ttu-id="fdd6e-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-194">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fdd6e-195">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-195">☑</span></span> | `@EntryPoint() operation RunSimulation` | <span data-ttu-id="fdd6e-196">Kommuniziert den Zweck des Einstiegs Punkts über den Vorgangs Namen eindeutig.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-196">Clearly communicates purpose of entry point through operation name.</span></span> |
| <span data-ttu-id="fdd6e-197">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-197">☒</span></span> | <s>`@EntryPoint() operation Main`</s> | <span data-ttu-id="fdd6e-198">Die Verwendung von `Main` kommuniziert nicht eindeutig mit dem Zweck des Einstiegs Punkts und ist mit dem- `@EntryPoint()` Attribut redundant.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-198">Use of `Main` doesn't clearly communicate purpose of entry point, and is redundant with `@EntryPoint()` attribute.</span></span> |

***

### <a name="shorthand-and-abbreviations"></a><span data-ttu-id="fdd6e-199">Kurzformen und Abkürzungen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-199">Shorthand and Abbreviations</span></span> ###

<span data-ttu-id="fdd6e-200">Ungeachtet der obigen Ratschläge gibt es eine Vielzahl von kurz Informationen, die die allgemeine und weit verbreitete Verwendung von Quantum Computing sehen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-200">The above advice notwithstanding, there are many forms of shorthand that see common and pervasive use in quantum computing.</span></span>
<span data-ttu-id="fdd6e-201">Es wird empfohlen, vorhandene und allgemeine kurzwerte zu verwenden, und wo Sie vorhanden sind, insbesondere bei Vorgängen, die für den Betrieb eines Ziel Computers intrinsisch sind.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-201">We suggest using existing and common shorthand where it exists, especially for operations that are intrinsic to the operation of a target machine.</span></span>
<span data-ttu-id="fdd6e-202">Wir wählen beispielsweise den Namen `X` anstelle von `ApplyX` und `Rz` anstelle von aus `RotateAboutZ` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-202">For example, we choose the name `X` instead of `ApplyX`, and `Rz` instead of `RotateAboutZ`.</span></span>
<span data-ttu-id="fdd6e-203">Wenn Sie diese Kurznamen verwenden, sollten Vorgangs Namen Großbuchstaben sein (z. b. `MAJ` ).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-203">When using such shorthand, operation names should be all uppercase (e.g.: `MAJ`).</span></span>

<span data-ttu-id="fdd6e-204">Im Fall von häufig verwendeten Akronymen und Initialisierungen, wie z. b. "QFT" für "Quantum Fourier Transform", ist Vorsicht geboten.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-204">Some care is required when applying this convention in the case of commonly used acronyms and initialisms such as "QFT" for "quantum Fourier transform."</span></span>
<span data-ttu-id="fdd6e-205">Es empfiehlt sich, allgemeine .net-Konventionen für die Verwendung von Akronymen und initialismen in vollständigen Namen zu befolgen, die Folgendes vorschreiben:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-205">We suggest following general .NET conventions for the use of acronyms and initialisms in full names, which prescribe that:</span></span>

- <span data-ttu-id="fdd6e-206">Akronyme mit zwei Buchstaben und Initialisierungen werden in Großbuchstaben benannt (z. b. `BE` für "Big-in").</span><span class="sxs-lookup"><span data-stu-id="fdd6e-206">two-letter acronyms and initialisms are named in upper case (e.g.: `BE` for "big-endian"),</span></span>
- <span data-ttu-id="fdd6e-207">Alle längeren Akronyme und Initialisierer werden in benannt `CamelCase` (z. b. `Qft` für "Quantum Fourier Transform").</span><span class="sxs-lookup"><span data-stu-id="fdd6e-207">all longer acronyms and initialisms are named in `CamelCase` (e.g.: `Qft` for "quantum Fourier transform")</span></span>

<span data-ttu-id="fdd6e-208">Folglich kann ein Vorgang, der den QFT implementiert, entweder `QFT` als Kurzform oder als ausgeschrieben bezeichnet werden `ApplyQft` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-208">Thus, an operation implementing the QFT could either be called `QFT` as shorthand, or written out as `ApplyQft`.</span></span>

<span data-ttu-id="fdd6e-209">Bei besonders häufig verwendeten Vorgängen und Funktionen ist es möglicherweise wünschenswert, einen Kurznamen als _Alias_ für eine längere Form bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-209">For particularly commonly used operations and functions, it may be desirable to provide a shorthand name as an _alias_ for a longer form:</span></span>

```qsharp
operation CCNOT(control0 : Qubit, control1 : Qubit, target : Qubit)
is Adj + Ctl {
    Controlled X([control0, control1], target);
}
```

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-210">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-210">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-211">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-211">We suggest:</span></span>

- <span data-ttu-id="fdd6e-212">Beachten Sie ggf. häufig akzeptierte und häufig verwendete Kurznamen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-212">Consider commonly accepted and widely used shorthand names when appropriate.</span></span>
- <span data-ttu-id="fdd6e-213">Verwenden Sie Großbuchstaben für Kurzformen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-213">Use uppercase for shorthand.</span></span>
- <span data-ttu-id="fdd6e-214">Verwenden Sie für kurze (aus zwei Buchstaben bestehende) Akronyme und Initialisierungen Großbuchstaben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-214">Use uppercase for short (two-letter) acronyms and initialisms.</span></span>
- <span data-ttu-id="fdd6e-215">Verwenden Sie `CamelCase` für längere (drei oder mehr Buchstaben) Akronyme und Initialisierer.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-215">Use `CamelCase` for longer (three or more letter) acronyms and initialisms.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-216">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-216">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-217">Name</span><span class="sxs-lookup"><span data-stu-id="fdd6e-217">Name</span></span> | <span data-ttu-id="fdd6e-218">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-218">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fdd6e-219">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-219">☑</span></span> | `X` | <span data-ttu-id="fdd6e-220">Wohl verständliche Kurzformen für "Apply a $X $ Transformation"</span><span class="sxs-lookup"><span data-stu-id="fdd6e-220">Well-understood shorthand for "apply an $X$ transformation"</span></span> |
| <span data-ttu-id="fdd6e-221">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-221">☑</span></span> | `CNOT` | <span data-ttu-id="fdd6e-222">Wohl verständliche Kurzformen für "kontrolliert-not"</span><span class="sxs-lookup"><span data-stu-id="fdd6e-222">Well-understood shorthand for "controlled-NOT"</span></span> |
| <span data-ttu-id="fdd6e-223">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-223">☒</span></span> | <s>`Cnot`</s> | <span data-ttu-id="fdd6e-224">Kurzformen dürfen nicht in sein `CamelCase` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-224">Shorthand should not be in `CamelCase`.</span></span> |
| <span data-ttu-id="fdd6e-225">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-225">☑</span></span> | `ApplyQft` | <span data-ttu-id="fdd6e-226">Der allgemeine initialismus "QFT" wird als Teil eines langen Namens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-226">Common initialism "QFT" appears as a part of a long-form name.</span></span> |
| <span data-ttu-id="fdd6e-227">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-227">☑</span></span> | `QFT` | <span data-ttu-id="fdd6e-228">Allgemeine Initialisierung "QFT" wird als Teil einer Kurzform angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-228">Common initialism "QFT" appears as a part of a shorthand name.</span></span> |



***


### <a name="proper-nouns-in-names"></a><span data-ttu-id="fdd6e-229">Richtige Nomen in Namen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-229">Proper Nouns in Names</span></span> ###

<span data-ttu-id="fdd6e-230">In der Physik ist es üblich, die Dinge nach der ersten Person zu benennen, um Sie zu veröffentlichen. die meisten nicht-Physikern sind nicht mit den Namen aller Benutzer und dem gesamten Verlauf vertraut.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-230">While in physics it is common to name things after the first person to publish about them, most non-physicists aren’t familiar with everyone’s names and all of the history.</span></span>
<span data-ttu-id="fdd6e-231">Wenn Sie sich zu stark auf Benennungs Konventionen der Physik verlassen, kann dies zu einer beträchtlichen Barriere für die Eingabe führen, da Benutzer aus anderen Hintergründen eine große Anzahl scheinbar undurchsichtiger Namen erlernen müssen, um allgemeine Vorgänge und Konzepte zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-231">Relying too heavily on naming conventions from physics can thus put up a substantial barrier to entry, as users from other backgrounds must learn a large number of seemingly opaque names in order to use common operations and concepts.</span></span>
<!-- An important part of the task of reducing confusion is to make code more accessible.
Especially in a field such as quantum computing that is rich with domain expertise, we must at all times be cognizant of the demands we place on that expertise as we design quantum software.
In naming code symbols, one way that this cognizance expresses itself is as an awareness of the convention from physics of adopting as the names of algorithms and operations the names of their original publishers.
While we must maintain the history and intellectual provenance of concepts in quantum computing, demanding that all users be versed in this history to use even the most basic of functions and operations places a barrier to entry that is in most cases severe enough to even present an ethical compromise. -->
<span data-ttu-id="fdd6e-232">Daher wird empfohlen, dass, soweit sinnvoll, gängige Nomen, die ein Konzept beschreiben, für die richtigen Nomen, die den Veröffentlichungs Verlauf eines Konzepts beschreiben, eine starke Bevorzugung annehmen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-232">Thus, we recommend that wherever reasonable, common nouns that describe a concept be adopted in strong preference to proper nouns that describe the publication history of a concept.</span></span>
<span data-ttu-id="fdd6e-233">Ein bestimmtes Beispiel ist, dass der einzeln gesteuerte Swap-Vorgang und der doppelt kontrollierte not-Vorgang in Academic Literatur oft als "Fredkin"-und "deffoli"-Vorgänge bezeichnet werden, die jedoch in Q# erster Linie als und identifiziert werden `CSWAP` `CCNOT` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-233">As a particular example, the singly controlled SWAP and doubly controlled NOT operations are often called the "Fredkin" and "Toffoli" operations in academic literature, but are identified in Q# primarily as `CSWAP` and `CCNOT`.</span></span>
<span data-ttu-id="fdd6e-234">In beiden Fällen enthalten die API-Dokumentations Kommentare Synonyme, die auf den richtigen Substantiven basieren, sowie alle entsprechenden citierungen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-234">In both cases, the API documentation comments provide synonymous names based on proper nouns, along with all appropriate citations.</span></span>

<span data-ttu-id="fdd6e-235">Diese Einstellung ist besonders wichtig, da eine bestimmte Verwendung von richtigen Nomen immer erforderlich ist – Q# folgt der von vielen klassischen Sprachen festgelegten Tradition und bezieht sich auf Typen als `Bool` Verweis auf die boolesche Logik, die wiederum in Bezug auf George Boole benannt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-235">This preference is especially important given that some usage of proper nouns will always be necessary — Q# follows the tradition set by many classical languages, for instance, and refers to `Bool` types in reference to Boolean logic, which is in turn named in honor of George Boole.</span></span>
<span data-ttu-id="fdd6e-236">Einige Quantum-Konzepte werden ähnlich benannt, einschließlich des in `Pauli` die Sprache integrierten Typs Q# .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-236">A few quantum concepts similarly are named in a similar fashion, including the `Pauli` type built-in to the Q# language.</span></span>
<span data-ttu-id="fdd6e-237">Wenn Sie die Verwendung von richtigen Nomen minimieren, bei denen eine solche Verwendung nicht wesentlich ist, verringern wir die Auswirkungen, bei denen die richtigen Nomen nicht vernünftig vermieden werden können.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-237">By minimizing the usage of proper nouns where such usage is not essential, we reduce the impact where proper nouns cannot be reasonably avoided.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-238">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-238">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="fdd6e-239">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-239">We suggest:</span></span>

- <span data-ttu-id="fdd6e-240">Vermeiden Sie die Verwendung von richtigen Substantiven in Namen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-240">Avoid the use of proper nouns in names.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-241">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-241">Examples</span></span>](#tab/examples)

***

### <a name="type-conversions"></a><span data-ttu-id="fdd6e-242">Typkonvertierungen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-242">Type Conversions</span></span> ###

<span data-ttu-id="fdd6e-243">Da Q# eine stark und statisch typisierte Sprache ist, kann ein Wert eines Typs nur als Wert eines anderen Typs mithilfe eines expliziten Aufrufes einer Typkonvertierungs Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-243">Since Q# is a strongly and staticly typed language, a value of one type can only be used as a value of another type by using an explicit call to a type conversion function.</span></span>
<span data-ttu-id="fdd6e-244">Dies steht im Gegensatz zu Sprachen, die es ermöglichen, Typen implizit (z. b. typherauf Stufung) oder durch Umwandlung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-244">This is in contrast to languages which allow for values to change types implicitly (e.g.: type promotion), or through casting.</span></span>
<span data-ttu-id="fdd6e-245">Typkonvertierungs Funktionen spielen daher eine wichtige Rolle bei der Q# Bibliotheksentwicklung und bilden eine der gängigsten Entscheidungen zum benennen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-245">As a result, type conversion functions play an important role in Q# library development, and comprise one of the more commonly encountered decisions about naming.</span></span>
<span data-ttu-id="fdd6e-246">Es ist jedoch zu beachten, dass Typkonvertierungen immer _deterministisch_sind. Sie können als Funktionen geschrieben werden und fallen daher unter den obigen Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-246">We note, however, that since type conversions are always _deterministic_, they can be written as functions and thus fall under the advice above.</span></span>
<span data-ttu-id="fdd6e-247">Insbesondere wird empfohlen, dass Typkonvertierungs Funktionen nie als Verben (z. b. `ConvertToX` ) oder adverbfilter-präpositional-Ausdrücke () benannt werden `ToX` . Sie sollten jedoch als Adjektiv-Ausdrücke mit präpositional bezeichnet werden, die die Quell-und Zieltypen angeben ( `XAsY` ).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-247">In particular, we suggest that type conversion functions should never be named as verbs (e.g.: `ConvertToX`) or adverb prepositional phrases (`ToX`), but should be named as adjective prepositional phrases that indicate the source and destination types (`XAsY`).</span></span>
<span data-ttu-id="fdd6e-248">Beim Auflisten von Array Typen in Namen der Typkonvertierungs Funktion wird die Kurzform empfohlen `Arr` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-248">When listing array types in type conversion function names, we recommend the shorthand `Arr`.</span></span>
<span data-ttu-id="fdd6e-249">Abgesehen von Ausnahmefällen wird empfohlen, dass alle Typkonvertierungs Funktionen mit benannt werden, `As` damit Sie schnell identifiziert werden können.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-249">Barring exceptional circumstances, we recommend that all type conversion functions be named using `As` so that they can be quickly identified.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-250">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-250">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-251">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-251">We suggest:</span></span>

- <span data-ttu-id="fdd6e-252">Wenn eine Funktion einen Wert vom Typ `X` in einen Wert vom Typ konvertiert `Y` , verwenden Sie entweder den Namen `AsY` oder `XAsY` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-252">If a function converts a value of type `X` to a value of type `Y`, use either the name `AsY` or `XAsY`.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-253">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-253">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-254">Name</span><span class="sxs-lookup"><span data-stu-id="fdd6e-254">Name</span></span> | <span data-ttu-id="fdd6e-255">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-255">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fdd6e-256">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-256">☒</span></span> | <s>`ToDouble`</s> | <span data-ttu-id="fdd6e-257">Die Vorposition "to" führt zu einem Verb Ausdruck, der einen Vorgang und keine Funktion angibt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-257">The preposition "to" results in a verb phrase, indicating an operation and not a function.</span></span> |
| <span data-ttu-id="fdd6e-258">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-258">☒</span></span> | <s>`AsDouble`</s> | <span data-ttu-id="fdd6e-259">Der Eingabetyp ist aus dem Funktionsnamen nicht eindeutig.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-259">The input type is not clear from the function name.</span></span> |
| <span data-ttu-id="fdd6e-260">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-260">☒</span></span> | <s>`PauliArrFromBoolArr`</s> | <span data-ttu-id="fdd6e-261">Die Eingabe-und Ausgabetypen werden in der falschen Reihenfolge angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-261">The input and output types appear in the wrong order.</span></span> |
| <span data-ttu-id="fdd6e-262">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-262">☑</span></span> | `ResultArrAsBoolArr` | <span data-ttu-id="fdd6e-263">Die Eingabe-und Ausgabetypen sind eindeutig.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-263">Both the input types and output types are clear.</span></span> |

***

### <a name="private-or-internal-names"></a><span data-ttu-id="fdd6e-264">Private oder interne Namen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-264">Private or Internal Names</span></span> ###

<span data-ttu-id="fdd6e-265">In vielen Fällen ist ein Name ausschließlich für die interne Verwendung in einer Bibliothek oder einem Projekt vorgesehen und ist kein garantierter Teil der API, die von einer Bibliothek angeboten wird.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-265">In many cases, a name is intended strictly for use internal to a library or project, and is not a guaranteed part of the API offered by a library.</span></span>
<span data-ttu-id="fdd6e-266">Es ist hilfreich, eindeutig anzugeben, dass dies der Fall ist, wenn Funktionen und Vorgänge benannt werden, damit versehentlich Abhängigkeiten von internem Code offensichtlich werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-266">It is helpful to clearly indicate that this is the case when naming functions and operations so that accidental dependencies on internal-only code are made obvious.</span></span>
<span data-ttu-id="fdd6e-267">Wenn ein Vorgang oder eine Funktion nicht für die direkte Verwendung vorgesehen ist, sondern stattdessen von einer übereinstimmenden Aufruf baren Funktion verwendet werden soll, die von einer partiellen Anwendung verwendet wird, empfiehlt es sich, einen Namen zu verwenden, der mit dem `internal` Schlüsselwort für die Aufruf Bare-Aktivität beginnt</span><span class="sxs-lookup"><span data-stu-id="fdd6e-267">If an operation or function is not intended for direct use, but rather should be used by a matching callable which acts by partial application, consider using a name starting with the `internal` keyword for the callable that is partially applied.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-268">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-268">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-269">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-269">We suggest:</span></span>

- <span data-ttu-id="fdd6e-270">Wenn eine Funktion, ein Vorgang oder ein benutzerdefinierter Typ nicht Teil der öffentlichen API für eine Q# Bibliothek oder ein Programm ist, stellen Sie sicher, dass Sie als intern gekennzeichnet ist, indem Sie das `internal` Schlüsselwort vor der- `function` ,-oder- `operation` `newtype` Deklaration platzieren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-270">When a function, operation, or user-defined type is not a part of the public API for a Q# library or program, ensure that it is marked as internal by placing the `internal` keyword before the `function`, `operation`, or `newtype` declaration.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-271">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-271">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-272">Name</span><span class="sxs-lookup"><span data-stu-id="fdd6e-272">Name</span></span> | <span data-ttu-id="fdd6e-273">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-273">Description</span></span> |
|---|------|-------------|
| <span data-ttu-id="fdd6e-274">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-274">☒</span></span> | <s>`operation _ApplyDecomposedOperation`</s> | <span data-ttu-id="fdd6e-275">Verwenden Sie keinen Unterstrich `_` , um anzugeben, dass dieser Vorgang nur für die interne Verwendung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-275">Do not use an underscore `_` to indicate that this operation is for internal use only.</span></span> |
| <span data-ttu-id="fdd6e-276">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-276">☑</span></span> | `internal operation ApplyDecomposedOperation` | <span data-ttu-id="fdd6e-277">Das `internal` Schlüsselwort am Anfang weist eindeutig darauf hin, dass dieser Vorgang nur für die interne Verwendung vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-277">The `internal` keyword at the beginning clearly indicates that this operation is for internal use only.</span></span> |

***
### <a name="variants"></a><span data-ttu-id="fdd6e-278">Varianten</span><span class="sxs-lookup"><span data-stu-id="fdd6e-278">Variants</span></span> ###

<span data-ttu-id="fdd6e-279">Obwohl diese Einschränkung in zukünftigen Versionen von möglicherweise nicht beibehalten wird Q# , ist es aktuell, dass häufig Gruppen verwandter Vorgänge oder Funktionen vorhanden sind, die durch die von Ihnen unterstützten Funktoren unterschieden werden, oder durch die konkreten Typen ihrer Argumente.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-279">Though this limitation may not persist in future versions of Q#, it is presently the case that there will often be groups of related operations or functions that are distinguished by which functors their inputs support, or by the concrete types of their arguments.</span></span>
<span data-ttu-id="fdd6e-280">Diese Gruppen können unterschieden werden, indem der gleiche Stamm Name verwendet wird, gefolgt von einem oder zwei Buchstaben, die die Variante angeben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-280">These groups can be distinguished by using the same root name, followed by one or two letters that indicate its variant.</span></span>

| <span data-ttu-id="fdd6e-281">Suffix</span><span class="sxs-lookup"><span data-stu-id="fdd6e-281">Suffix</span></span> | <span data-ttu-id="fdd6e-282">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fdd6e-282">Meaning</span></span> |
|--------|---------|
| `A` | <span data-ttu-id="fdd6e-283">Für die Unterstützung erwartete Eingabe`Adjoint`</span><span class="sxs-lookup"><span data-stu-id="fdd6e-283">Input expected to support `Adjoint`</span></span> |
| `C` | <span data-ttu-id="fdd6e-284">Für die Unterstützung erwartete Eingabe`Controlled`</span><span class="sxs-lookup"><span data-stu-id="fdd6e-284">Input expected to support `Controlled`</span></span> |
| `CA` | <span data-ttu-id="fdd6e-285">Es wurde eine Eingabe erwartet, die `Controlled` und`Adjoint`</span><span class="sxs-lookup"><span data-stu-id="fdd6e-285">Input expected to support `Controlled` and `Adjoint`</span></span> |
| `I` | <span data-ttu-id="fdd6e-286">Eingabe oder Eingaben weisen den Typ auf.`Int`</span><span class="sxs-lookup"><span data-stu-id="fdd6e-286">Input or inputs are of type `Int`</span></span> |
| `D` | <span data-ttu-id="fdd6e-287">Eingabe oder Eingaben weisen den Typ auf.`Double`</span><span class="sxs-lookup"><span data-stu-id="fdd6e-287">Input or inputs are of type `Double`</span></span> |
| `L` | <span data-ttu-id="fdd6e-288">Eingabe oder Eingaben weisen den Typ auf.`BigInt`</span><span class="sxs-lookup"><span data-stu-id="fdd6e-288">Input or inputs are of type `BigInt`</span></span> |

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-289">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-289">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-290">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-290">We suggest:</span></span>

- <span data-ttu-id="fdd6e-291">Wenn eine Funktion oder ein Vorgang nicht mit ähnlichen Funktionen oder Vorgängen durch die Typen und die Funktions Unterstützung Ihrer Eingaben verknüpft ist, verwenden Sie kein Suffix.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-291">If a function or operation is not related to any similar functions or operations by the types and functor support of their inputs, do not use a suffix.</span></span>
- <span data-ttu-id="fdd6e-292">Wenn eine Funktion oder ein Vorgang mit ähnlichen Funktionen oder Vorgängen verknüpft ist, die von den Typen und der funktorunterstützung Ihrer Eingaben verwendet werden, verwenden Sie Suffixe wie in der obigen Tabelle, um Varianten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-292">If a function or operation is related to any similar functions or operations by the types and functor support of their inputs, use suffixes as in the table above to distinguish variants.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-293">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-293">Examples</span></span>](#tab/examples)

***

### <a name="arguments-and-variables"></a><span data-ttu-id="fdd6e-294">Argumente und Variablen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-294">Arguments and Variables</span></span> ###

<span data-ttu-id="fdd6e-295">Ein wichtiges Ziel des Q# Codes für eine Funktion oder einen Vorgang besteht darin, den Code einfach zu lesen und zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-295">A key goal of the Q# code for a function or operation is for it to be easily read and understood.</span></span>
<span data-ttu-id="fdd6e-296">Ebenso sollten die Namen von Eingaben und Typargumenten kommunizieren, wie eine Funktion oder ein Argument nach der Bereitstellung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-296">Similarly, the names of inputs and type arguments should communicate how a function or argument will be used once provided.</span></span>


# <a name="guidance"></a>[<span data-ttu-id="fdd6e-297">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-297">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-298">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-298">We suggest:</span></span>

- <span data-ttu-id="fdd6e-299">Verwenden Sie für alle Variablen-und Eingabe Namen `pascalCase` die starke bevorzugte Einstellung für `CamelCase` , `snake_case` oder `ANGRY_CASE` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-299">For all variable and input names, use `pascalCase` in strong preference to `CamelCase`, `snake_case`, or `ANGRY_CASE`.</span></span>
- <span data-ttu-id="fdd6e-300">Eingabe Namen sollten beschreibend sein. vermeiden Sie, wenn möglich, einen oder zwei Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-300">Input names should be descriptive; avoid one or two letter names where possible.</span></span>
- <span data-ttu-id="fdd6e-301">Vorgänge und Funktionen, die genau ein Typargument akzeptieren, sollten das Typargument von angeben, `T` wenn seine Rolle offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-301">Operations and functions accepting exactly one type argument should denote that type argument by `T` when its role is obvious.</span></span>
- <span data-ttu-id="fdd6e-302">Wenn eine Funktion oder ein Vorgang mehrere Typargumente annimmt oder wenn die Rolle eines einzelnen Typarguments nicht offensichtlich ist, sollten Sie die Verwendung eines kurzen Großbuchstaben mit vorangestelltem Wort `T` (z. b. `TOutput` ) für jeden Typ in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-302">If a function or operation takes multiple type arguments, or if the role of a single type argument is not obvious, consider using a short capitalized word prefaced by `T` (e.g.: `TOutput`) for each type.</span></span>
- <span data-ttu-id="fdd6e-303">Geben Sie keine Typnamen in Argument-und Variablennamen ein. Diese Informationen können von Ihrer Entwicklungsumgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-303">Do not include type names in argument and variable names; this information can and should be provided by your development environment.</span></span>
- <span data-ttu-id="fdd6e-304">Kennzeichnen Sie skalare Typen nach Ihren Literalnamen ( `flagQubit` ) und Array Typen durch einen Plural ( `measResults` ).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-304">Denote scalar types by their literal names (`flagQubit`), and array types by a plural (`measResults`).</span></span>
  <span data-ttu-id="fdd6e-305">Vor allem bei Arrays von Qubits sollten diese Typen in Erwägung gezogen werden, `Register` Wenn der Name auf eine Sequenz von Qubits verweist, die in irgendeiner Weise eng miteinander verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-305">For arrays of qubits in particular, consider denoting such types by `Register` where the name refers to a sequence of qubits that are closely related in some way.</span></span>
- <span data-ttu-id="fdd6e-306">Variablen, die als Indizes in Arrays verwendet werden, sollten mit beginnen `idx` und als Singular (z. b.) verwendet werden `things[idxThing]` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-306">Variables used as indices into arrays should begin with `idx` and should be singular (e.g.: `things[idxThing]`).</span></span>
  <span data-ttu-id="fdd6e-307">Vermeiden Sie insbesondere die Verwendung von Variablennamen mit nur einem Buchstaben als Indizes. Verwenden Sie `idx` ggf. mindestens.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-307">In particular, strongly avoid using single-letter variable names as indices; consider using `idx` at a minimum.</span></span>
- <span data-ttu-id="fdd6e-308">Variablen, die zum Speichern der Längen von Arrays verwendet werden, sollten mit beginnen `n` und pluralisiert werden (z. b. `nThings` ).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-308">Variables used to hold lengths of arrays should begin with `n` and should be pluralized (e.g.: `nThings`).</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-309">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-309">Examples</span></span>](#tab/examples)

***

### <a name="user-defined-type-named-items"></a><span data-ttu-id="fdd6e-310">Benannte Elemente des benutzerdefinierten Typs</span><span class="sxs-lookup"><span data-stu-id="fdd6e-310">User-Defined Type Named Items</span></span> ###

<span data-ttu-id="fdd6e-311">Benannte Elemente in benutzerdefinierten Typen sollten als benannt werden `CamelCase` , auch als Eingabe für UDT-Konstruktoren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-311">Named items in user-defined types should be named as `CamelCase`, even in input to UDT constructors.</span></span>
<span data-ttu-id="fdd6e-312">Dadurch können benannte Elemente bei Verwendung der accessornotation (z. b. `callable::Apply` ) oder der Copy-and-Update-Notation () eindeutig von Verweisen auf lokale Variablen getrennt werden `set arr w/= Data <- newData` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-312">This helps in order to clearly separate named items from references to locally scoped variables when using accessor notation (e.g.: `callable::Apply`) or copy-and-update notation (`set arr w/= Data <- newData`).</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-313">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-313">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-314">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-314">We suggest:</span></span>

- <span data-ttu-id="fdd6e-315">Benannte Elemente in UDT-Konstruktoren sollten als benannt werden, d `CamelCase` . h., Sie sollten mit einem anfänglichen Großbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-315">Named items in UDT constructors should be named as `CamelCase`; that is, they should begin with an initial uppercase.</span></span>
- <span data-ttu-id="fdd6e-316">Benannte Elemente, die in Vorgänge aufgelöst werden, sollten als Verb Phasen benannt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-316">Named items that resolve to operations should be named as verb phases.</span></span>
- <span data-ttu-id="fdd6e-317">Benannte Elemente, die nicht in Vorgänge aufgelöst werden, sollten als nominale Ausdrücke benannt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-317">Named items that do not resolve to operations should be named as noun phrases.</span></span>
- <span data-ttu-id="fdd6e-318">Für UDTs, die Vorgänge einschließen, sollte ein einzelnes benanntes Element mit dem Namen `Apply` definiert werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-318">For UDTs that wrap operations, a single named item called `Apply` should be defined.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-319">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-319">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-320">Codeausschnitt</span><span class="sxs-lookup"><span data-stu-id="fdd6e-320">Snippet</span></span> | <span data-ttu-id="fdd6e-321">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-321">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="fdd6e-322">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-322">☑</span></span> | `newtype Oracle = (Apply : Qubit[] => Unit is Adj + Ctl)` | <span data-ttu-id="fdd6e-323">Der Name `Apply` ist ein `CamelCase` -formatierter Verb Ausdruck, der darauf hinweist, dass das benannte Element ein Vorgang ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-323">The name `Apply` is a `CamelCase`-formatted verb phrase, suggesting that the named item is an operation.</span></span> |
| <span data-ttu-id="fdd6e-324">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-324">☒</span></span> | <s>`newtype Oracle = (apply : Qubit[] => Unit is Adj + Ctl) `</s> | <span data-ttu-id="fdd6e-325">Benannte Elemente sollten mit einem ersten Großbuchstaben beginnen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-325">Named items should begin with an initial uppercase letter.</span></span> |
| <span data-ttu-id="fdd6e-326">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-326">☒</span></span> | <s>`newtype Collection = (Length : Int, Get : Int -> (Qubit => Unit)) `</s> | <span data-ttu-id="fdd6e-327">Benannte Elemente, die in Functions aufgelöst werden, sollten als nominale Ausdrücke und nicht als Verb Ausdrücke benannt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-327">Named items which resolve to functions should be named as noun phrases, not as verb phrases.</span></span> |

***

## <a name="input-conventions"></a><span data-ttu-id="fdd6e-328">Eingabe Konventionen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-328">Input Conventions</span></span> ##

<span data-ttu-id="fdd6e-329">Wenn ein Entwickler einen Vorgang oder eine Funktion aufruft, müssen die verschiedenen Eingaben für diesen Vorgang bzw. diese Funktion in einer bestimmten Reihenfolge angegeben werden. dadurch erhöht sich die kognitive Auslastung eines Entwicklers, um eine Bibliothek verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-329">When a developer calls into an operation or function, the various inputs to that operation or function must be specified in a particular order, increasing the cognitive load that a developer faces in order to make use of a library.</span></span>
<span data-ttu-id="fdd6e-330">Vor allem ist die Aufgabe des hintergabeorderings häufig eine Ablenkungs Maßnahme von der Aufgabe, die eine Implementierung eines Quantum-Algorithmus zu programmieren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-330">In particular, the task of remembering input orderings is often a distraction from the task at hand: programming an implementation of a quantum algorithm.</span></span>
<span data-ttu-id="fdd6e-331">Obwohl die Unterstützung für umfangreiche IDE dies sehr stark mindern kann, kann ein guter Entwurf und die Einhaltung allgemeiner Konventionen dazu beitragen, die durch eine API erzwungene kognitive Auslastung zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-331">Though rich IDE support can mitigate this to a large extent, good design and adherence to common conventions can also help to minimize the cognitive load imposed by an API.</span></span>

<span data-ttu-id="fdd6e-332">Wenn möglich, kann es hilfreich sein, die Anzahl der Eingaben zu verringern, die von einem Vorgang oder einer Funktion erwartet werden, damit die Rolle der einzelnen Eingaben sowohl für Entwickler, die diesen Vorgang oder diese Funktion aufrufen, als auch für Entwickler, die diesen Code später lesen, gleichzeitig offensichtlich ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-332">Where possible, it can be helpful to reduce the number of inputs expected by an operation or function, so that the role of each input is more immediately obvious both to developers calling into that operation or function, and to developers reading that code later.</span></span>
<span data-ttu-id="fdd6e-333">Besonders wenn es nicht möglich oder sinnvoll ist, die Anzahl der Argumente für einen Vorgang oder eine Funktion zu reduzieren, ist es wichtig, dass eine konsistente Reihenfolge vorhanden ist, die die Überraschung des Benutzers beim Vorhersagen der Reihenfolge der Eingaben minimiert.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-333">Especially when it is not possible or reasonable to reduce the number of arguments to an operation or function, it is important to have a consistent ordering that minimizes the surprise that a user faces when predicting the order of inputs.</span></span>

<span data-ttu-id="fdd6e-334">Wir empfehlen eine Eingabe Reihenfolge Konventionen, die größtenteils von der Betrachtung einer partiellen Anwendung als Generalisierung von f (x, y) ≡ f (x) (y) abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-334">We recommend an input ordering conventions that largely derives from thinking of partial application as a generalization of currying 𝑓(𝑥, 𝑦) ≡ 𝑓(𝑥)(𝑦).</span></span>
<span data-ttu-id="fdd6e-335">Folglich sollte das partielle anwenden der ersten Argumente zu einem Aufruf baren Ergebnis führen, das immer nützlich ist, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-335">Thus, partially applying the first arguments should result in a callable that is useful in its own right whenever that is reasonable.</span></span>
<span data-ttu-id="fdd6e-336">Nach diesem Prinzip sollten Sie die folgende Reihenfolge von Argumenten verwenden:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-336">Following this principle, consider using the following order of arguments:</span></span>

- <span data-ttu-id="fdd6e-337">Klassische, nicht Aufruf Bare Argumente, wie z. b. Winkel, Vektoren von Mächten usw.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-337">Classical non-callable arguments such as angles, vectors of powers, etc.</span></span>
- <span data-ttu-id="fdd6e-338">Aufruf Bare Argumente (Funktionen und Argumente).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-338">Callable arguments (functions and arguments).</span></span>
  <span data-ttu-id="fdd6e-339">Wenn sowohl Funktionen als auch Vorgänge als Argumente verwendet werden, erwägen Sie das Platzieren von Vorgängen nach Funktionen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-339">If both functions and operations are taken as arguments, consider placing operations after functions.</span></span>
- <span data-ttu-id="fdd6e-340">Auflistungen, auf die durch Aufruf Bare Argumente in ähnlicher Weise wie `Map` , `Iter` , und agiert werden `Enumerate` `Fold` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-340">Collections acted upon by callable arguments in a similar way to `Map`, `Iter`, `Enumerate`, and `Fold`.</span></span>
- <span data-ttu-id="fdd6e-341">Als Steuerelemente verwendete Qubit-Argumente.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-341">Qubit arguments used as controls.</span></span>
- <span data-ttu-id="fdd6e-342">Als Ziele verwendete Qubit-Argumente.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-342">Qubit arguments used as targets.</span></span>

<span data-ttu-id="fdd6e-343">Stellen Sie sich einen Vorgang `ApplyPhaseEstimationIteration` zur Verwendung in der Phasen Schätzung vor, der einen Winkel und einen Oracle annimmt, den Winkel `Rz` von einem Array mit unterschiedlichen Skalierungsfaktoren an geändert übergibt und dann Anwendungen des Oracle steuert.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-343">Consider an operation `ApplyPhaseEstimationIteration` for use in phase estimation that takes an angle and an oracle, passes the angle to `Rz` modified by an array of different scaling factors, and then controls applications of the oracle.</span></span>
<span data-ttu-id="fdd6e-344">Wir würden die Eingaben `ApplyPhaseEstimationIteration` folgendermaßen sortieren:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-344">We would order the inputs to `ApplyPhaseEstimationIteration` in the following fashion:</span></span>

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
<span data-ttu-id="fdd6e-345">Im besonderen Fall, dass eine Überraschung minimiert wird, imitieren einige Funktionen und Vorgänge das Verhalten der integrierten Funktoren `Adjoint` und `Controlled` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-345">As a special case of minimizing surprise, some functions and operations mimic the behavior of the built-in functors `Adjoint` and `Controlled`.</span></span>
<span data-ttu-id="fdd6e-346">Hat z. b. den- `ControlledOnInt<'T>` Typ `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)` , z. b. `ControlledOnInt<Qubit[]>(5, _)` wie das- `Controlled` Funktor, aber für die Bedingung, dass das Steuerelement registriert den Status $ \ket {5} = \ket {101} $ darstellt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-346">For instance, `ControlledOnInt<'T>` has type `(Int, ('T => Unit is Adj + Ctl)) => ((Qubit[], 'T) => Unit is Adj + Ctl)`, such that `ControlledOnInt<Qubit[]>(5, _)` acts like the `Controlled` functor, but on the condition that the control register represents the state $\ket{5} = \ket{101}$.</span></span>
<span data-ttu-id="fdd6e-347">Daher erwartet ein Entwickler, dass die Eingaben `ControlledOnInt` den aufrufenden, der zuletzt transformiert wird, und dass der resultierende Vorgang als Eingabe `(Qubit[], 'T)` ---der gleichen Reihenfolge wie die Ausgabe des `Controlled` funktors.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-347">Thus, a developer expects that the inputs to `ControlledOnInt` place the callable being transformed last, and that the resulting operation takes as its input `(Qubit[], 'T)` --- the same order as followed by the output of the `Controlled` functor.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-348">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-348">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-349">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-349">We suggest:</span></span>

- <span data-ttu-id="fdd6e-350">Verwenden Sie Eingabe Sortierungen in Übereinstimmung mit der Verwendung der partiellen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-350">Use input orderings consistent with the use of partial application.</span></span>
- <span data-ttu-id="fdd6e-351">Verwenden Sie Eingabe Sortierungen, die mit integrierten Funktoren konsistent sind.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-351">Use input orderings consistent with built-in functors.</span></span>
- <span data-ttu-id="fdd6e-352">Platzieren Sie alle klassischen Eingaben vor allen Quantum-Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-352">Place all classical inputs before any quantum inputs.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-353">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-353">Examples</span></span>](#tab/examples)

***

## <a name="documentation-conventions"></a><span data-ttu-id="fdd6e-354">Konventionen in der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="fdd6e-354">Documentation Conventions</span></span> ##

<span data-ttu-id="fdd6e-355">Die Q# Sprache ermöglicht das Anfügen von Dokumentationen an Vorgänge, Funktionen und benutzerdefinierte Typen durch die Verwendung von speziell formatierten Dokumentations Kommentaren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-355">The Q# language allows for attaching documentation to operations, functions, and user-defined types through the use of specially formatted documentation comments.</span></span>
<span data-ttu-id="fdd6e-356">Diese Dokumentations Kommentare sind durch drei Schrägstriche () gekennzeichnet und `///` sind kleine [markdown-Dokumente mit docfx-Geschmack](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) , mit denen der Zweck der einzelnen Vorgänge, Funktionen und benutzerdefinierten Typen beschrieben werden kann, welche Eingaben jeweils erwartet werden usw.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-356">Denoted by triple-slashes (`///`), these documentation comments are small [DocFX-flavored Markdown](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html) documents that can be used to describing the purpose of each operation, function, and user-defined type, what inputs each expects, and so forth.</span></span>
<span data-ttu-id="fdd6e-357">Der mit dem Quantum Development Kit bereitgestellte Compiler extrahiert diese Kommentare und verwendet diese, um die besitzen-Dokumentation in ähnlicher Weise wie bei zu unterstützen https://docs.microsoft.com/quantum .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-357">The compiler provided with the Quantum Development Kit extracts these comments and uses them to help typeset documentation similar to that at https://docs.microsoft.com/quantum.</span></span>
<span data-ttu-id="fdd6e-358">Entsprechend verwendet der Sprachserver, der mit dem Quantum Development Kit bereitgestellt wird, diese Kommentare, um Benutzern Hilfe zu bieten, wenn Sie mit dem Mauszeiger auf Symbole in Ihrem Q# Code zeigen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-358">Similarly, the language server provided with the Quantum Development Kit uses these comments to provide help to users when they hover over symbols in their Q# code.</span></span>
<span data-ttu-id="fdd6e-359">Durch die Verwendung von Dokumentations Kommentaren können Benutzer den Code sinnvoll machen, indem Sie einen nützlichen Verweis auf Details bereitstellen, die nicht ohne weiteres mit den anderen Konventionen in diesem Dokument ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-359">Making use of documentation comments can thus help users to make sense of code by providing a useful reference for details that are not easily expressed using the other conventions in this document.</span></span>

> [!div class="nextstepaction"]
> <span data-ttu-id="fdd6e-360">[Syntax Referenz für Dokumentations Kommentare](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-360">[Documentation comment syntax reference](xref:microsoft.quantum.guide.filestructure#documentation-comments).</span></span>

<span data-ttu-id="fdd6e-361">Um diese Funktionalität für Benutzer effektiv nutzen zu können, empfiehlt es sich, beim Schreiben von Dokumentations Kommentaren einige Punkte zu berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-361">In order to effectively use this functionality to help users, we recommend keeping a few things in mind as you write documentation comments.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-362">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-362">Guidance</span></span>](#tab/guidance)

<span data-ttu-id="fdd6e-363">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-363">We suggest:</span></span>

- <span data-ttu-id="fdd6e-364">Jeder öffentlichen Funktion, jedem Vorgang und jedem benutzerdefinierten Typ sollte unmittelbar ein Dokumentations Kommentar vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-364">Each public function, operation, and user-defined type should be immediately preceded by a documentation comment.</span></span>
- <span data-ttu-id="fdd6e-365">Jeder Dokumentations Kommentar sollte mindestens die folgenden Abschnitte enthalten:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-365">At a minimum, each documentation comment should include the following sections:</span></span>
    - <span data-ttu-id="fdd6e-366">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="fdd6e-366">Summary</span></span>
    - <span data-ttu-id="fdd6e-367">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fdd6e-367">Input</span></span>
    - <span data-ttu-id="fdd6e-368">Ausgabe (falls zutreffend)</span><span class="sxs-lookup"><span data-stu-id="fdd6e-368">Output (if applicable)</span></span>
- <span data-ttu-id="fdd6e-369">Stellen Sie sicher, dass alle Zusammenfassungen zwei oder weniger Sätze sind.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-369">Ensure that all summaries are two sentences or less.</span></span> <span data-ttu-id="fdd6e-370">Wenn mehr Platz benötigt wird, geben Sie einen `# Description` direkt folgenden Abschnitt `# Summary` mit umfassenden Details an.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-370">If more room is needed, provide a `# Description` section immediately following `# Summary` with complete details.</span></span>
- <span data-ttu-id="fdd6e-371">Wenn Sie vernünftig Vorgehen, sollten Sie mathematische nicht in Zusammenfassungen einschließen, da nicht alle Clients eine TeX-Notation in Zusammenfassungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-371">Where reasonable, do not include math in summaries, as not all clients support TeX notation in summaries.</span></span> <span data-ttu-id="fdd6e-372">Beachten Sie, dass beim Schreiben von Prosa Dokumenten (z. b. tex oder markdown) die Verwendung längerer Zeilenlängen vorzuziehen ist.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-372">Note that when writing prose documents (e.g. TeX or Markdown), it may be preferable to use longer line lengths.</span></span>
- <span data-ttu-id="fdd6e-373">Stellen Sie alle relevanten mathematischen Ausdrücke im- `# Description` Abschnitt bereit.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-373">Provide all relevant mathematical expressions in the `# Description` section.</span></span>
- <span data-ttu-id="fdd6e-374">Wenn Sie Eingaben beschreiben, wiederholen Sie nicht die Typen der einzelnen Eingaben, da diese vom Compiler abgeleitet werden können, und das Risiko der Inkonsistenz.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-374">When describing inputs, do not repeat the types of each input as these can be inferred by the compiler and risk introducing inconsistency.</span></span>
- <span data-ttu-id="fdd6e-375">Geben Sie nach Bedarf Beispiele an, die jeweils in einem eigenen Abschnitt enthalten sind `# Example` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-375">Provide examples as appropriate, each in their own `# Example` section.</span></span>
- <span data-ttu-id="fdd6e-376">Beschreiben Sie kurz die einzelnen Beispiele, bevor Sie Code auflisten.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-376">Briefly describe each example before listing code.</span></span>
- <span data-ttu-id="fdd6e-377">Nennen Sie alle relevanten akademischen Veröffentlichungen (z. b. Beiträge, Verfahren, Blogbeiträge und alternative Implementierungen) in einem `# References` Abschnitt als Auflistungs Liste mit Links.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-377">Cite all relevant academic publications (e.g.: papers, proceedings, blog posts, and alternative implementations) in a `# References` section as a bulleted list of links.</span></span>
- <span data-ttu-id="fdd6e-378">Stellen Sie sicher, dass, sofern möglich, alle anfügelinks zu permanenten und unveränderlichen bezeichmern (Dois-oder versionierte arXiv-Nummern) gehören.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-378">Ensure that, where possible, all citation links are to permanent and immutable identifiers (DOIs or versioned arXiv numbers).</span></span>
- <span data-ttu-id="fdd6e-379">Wenn ein Vorgang oder eine Funktion mit anderen Vorgängen oder Funktionen verknüpft ist, können Sie im Abschnitt andere Varianten als Aufzählungs Zeichen auflisten `# See Also` .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-379">When an operation or function is related to other operations or functions by functor variants, list other variants as bullets in the `# See Also` section.</span></span>
- <span data-ttu-id="fdd6e-380">Belassen Sie eine leere Kommentar Linie zwischen den Abschnitten der Ebene-1 ( `/// #` ), lassen Sie jedoch keine Leerzeile zwischen den Abschnitten der Ebene 2 ( `/// ##` ).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-380">Leave a blank comment line between level-1 (`/// #`) sections, but do not leave a blank line between level-2 (`/// ##`) sections.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-381">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-381">Examples</span></span>](#tab/examples)

#### <a name=""></a><span data-ttu-id="fdd6e-382">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-382">☑</span></span> ####

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

## <a name="formatting-conventions"></a><span data-ttu-id="fdd6e-383">Formatierungs Konventionen</span><span class="sxs-lookup"><span data-stu-id="fdd6e-383">Formatting Conventions</span></span> ##

<span data-ttu-id="fdd6e-384">Zusätzlich zu den oben genannten Vorschlägen ist es hilfreich, den Code so lesbar wie möglich zu machen, um konsistente Formatierungs Regeln zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-384">In addition to the preceding suggestions, it is helpful to help make code as legible as possible to use consistent formatting rules.</span></span>
<span data-ttu-id="fdd6e-385">Diese Formatierungs Regeln sind eher willkürlich und stark bis zur persönlichen Ästhetik.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-385">Such formatting rules by nature tend to be somewhat arbitrary and strongly up to personal aesthetics.</span></span>
<span data-ttu-id="fdd6e-386">Trotzdem empfiehlt es sich, einen konsistenten Satz von Formatierungs Konventionen innerhalb einer Gruppe von Projektmitarbeitern zu verwalten, insbesondere für große Q# Projekte wie das Quantum Development Kit selbst.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-386">Nonetheless, we recommend maintaining a consistent set of formatting conventions within a group of collaborators, and especially for large Q# projects such as the Quantum Development Kit itself.</span></span>
<span data-ttu-id="fdd6e-387">Diese Regeln können automatisch mithilfe des in den Compiler integrierten Formatierungs Tools angewendet werden Q# .</span><span class="sxs-lookup"><span data-stu-id="fdd6e-387">These rules can be automatically applied by using the formatting tool integrated with the Q# compiler.</span></span>

# <a name="guidance"></a>[<span data-ttu-id="fdd6e-388">Leitfaden</span><span class="sxs-lookup"><span data-stu-id="fdd6e-388">Guidance</span></span>](#tab/guidance) 

<span data-ttu-id="fdd6e-389">Wir empfehlen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-389">We suggest:</span></span>

- <span data-ttu-id="fdd6e-390">Verwenden Sie vier Leerzeichen anstelle von Registerkarten für die Portabilität.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-390">Use four spaces instead of tabs for portability.</span></span>
  <span data-ttu-id="fdd6e-391">Beispielsweise in vs Code:</span><span class="sxs-lookup"><span data-stu-id="fdd6e-391">For instance, in VS Code:</span></span>
  ```json
    "editor.insertSpaces": true,
    "editor.tabSize": 4
  ```
- <span data-ttu-id="fdd6e-392">Zeilenumbruch um 79 Zeichen, soweit angemessen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-392">Line wrap at 79 characters where reasonable.</span></span>
- <span data-ttu-id="fdd6e-393">Verwenden Sie Leerzeichen um binäre Operatoren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-393">Use spaces around binary operators.</span></span>
- <span data-ttu-id="fdd6e-394">Verwenden Sie Leerzeichen auf beiden Seiten von Doppelpunkten, die für Typanmerkungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-394">Use spaces on either side of colons used for type annotations.</span></span>
- <span data-ttu-id="fdd6e-395">Verwenden Sie ein einzelnes Leerzeichen nach Kommas, das in Array-und tupelliteralen verwendet wird (z. b. in Eingaben für Funktionen und Vorgänge).</span><span class="sxs-lookup"><span data-stu-id="fdd6e-395">Use a single space after commas used in array and tuple literals (e.g.: in inputs to functions and operations).</span></span>
- <span data-ttu-id="fdd6e-396">Verwenden Sie keine Leerzeichen nach Funktions-, Vorgangs-oder UDT-Namen oder nach den `@` in-Attribut Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-396">Do not use spaces after function, operation, or UDT names, or after the `@` in attribute declarations.</span></span>
- <span data-ttu-id="fdd6e-397">Jede Attribut Deklaration sollte sich in einer eigenen Zeile befinden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-397">Each attribute declaration should be on its own line.</span></span>

# <a name="examples"></a>[<span data-ttu-id="fdd6e-398">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd6e-398">Examples</span></span>](#tab/examples)

|   | <span data-ttu-id="fdd6e-399">Codeausschnitt</span><span class="sxs-lookup"><span data-stu-id="fdd6e-399">Snippet</span></span> | <span data-ttu-id="fdd6e-400">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fdd6e-400">Description</span></span> |
|---|---------|-------------|
| <span data-ttu-id="fdd6e-401">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-401">☒</span></span> | <s>`2+3`</s> | <span data-ttu-id="fdd6e-402">Verwenden Sie Leerzeichen um binäre Operatoren.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-402">Use spaces around binary operators.</span></span> |
| <span data-ttu-id="fdd6e-403">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-403">☒</span></span> | <s>`target:Qubit`</s> | <span data-ttu-id="fdd6e-404">Verwenden Sie Leerzeichen um Doppelpunkte der Typanmerkung.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-404">Use spaces around type annotation colons.</span></span> |
| <span data-ttu-id="fdd6e-405">☑</span><span class="sxs-lookup"><span data-stu-id="fdd6e-405">☑</span></span> | `Example(a, b, c)` | <span data-ttu-id="fdd6e-406">Elemente im eingabetupel sind zur besseren Lesbarkeit ordnungsgemäß verteilt.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-406">Items in input tuple are correctly spaced for readability.</span></span> |
| <span data-ttu-id="fdd6e-407">☒</span><span class="sxs-lookup"><span data-stu-id="fdd6e-407">☒</span></span> | <s>`Example (a, b, c)`</s> | <span data-ttu-id="fdd6e-408">Leerzeichen sollten nach Funktions-, Vorgangs-oder UDT-Namen unterdrückt werden.</span><span class="sxs-lookup"><span data-stu-id="fdd6e-408">Spaces should be suppressed after function, operation, or UDT names.</span></span> |

***
