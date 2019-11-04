---
title: Programmiersprache Q# | Microsoft-Dokumentation
description: Programmiersprache Q#
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.language.intro
ms.openlocfilehash: 560926f6f3e05c32a935f01ca5107a614e743ee2
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442484"
---
# <a name="the-q-programming-language"></a><span data-ttu-id="0ef33-103">Programmiersprache Q#</span><span class="sxs-lookup"><span data-stu-id="0ef33-103">The Q# Programming Language</span></span>

## <a name="introduction"></a><span data-ttu-id="0ef33-104">Einführung</span><span class="sxs-lookup"><span data-stu-id="0ef33-104">Introduction</span></span>

<span data-ttu-id="0ef33-105">Eine gängige Vorgehensweise beim Quantencomputing ist die Behandlung des Quantencomputers als Coprozessor, ähnlich wie bei GPUs, FPGAs und anderen ergänzenden Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="0ef33-105">A natural model for quantum computation is to treat the quantum computer as a coprocessor, similar to that used for GPUs, FPGAs, and other adjunct processors.</span></span>
<span data-ttu-id="0ef33-106">Von der Hauptsteuerlogik wird klassischer Code auf einem klassischen „Hostcomputer“ ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-106">The primary control logic runs classical code on a classical "host" computer.</span></span>
<span data-ttu-id="0ef33-107">Falls dies gewünscht bzw. erforderlich ist, kann über das Hostprogramm eine Unterroutine aufgerufen werden, die auf dem ergänzenden Prozessor ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef33-107">When appropriate and necessary, the host program can invoke a subroutine that runs on the adjunct processor.</span></span>
<span data-ttu-id="0ef33-108">Nach Abschluss der Unterroutine erhält das Hostprogramm Zugriff auf die entsprechenden Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="0ef33-108">When the subroutine completes, the host program gets access to the subroutine's results.</span></span>

<span data-ttu-id="0ef33-109">Q# (Q-Sharp) ist eine domänenspezifische Programmiersprache, die zum Ausdrücken von Quantenalgorithmen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ef33-109">Q# (Q-sharp) is a domain-specific programming language used for expressing quantum algorithms.</span></span>
<span data-ttu-id="0ef33-110">Sie wird zum Schreiben von Unterroutinen genutzt, die auf einem ergänzenden Quantenprozessor ausgeführt werden. Für die Steuerung werden hierbei ein klassisches Hostprogramm und ein Computer eingesetzt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-110">It is to be used for writing subroutines that execute on an adjunct quantum processor, under the control of a classical host program and computer.</span></span>
<span data-ttu-id="0ef33-111">Bis zur allgemeinen Verfügbarkeit von Quantenprozessoren werden Q#-Unterroutinen auf einem Simulator ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-111">Until quantum processors are widely available, Q# subroutines execute on a simulator.</span></span>

<span data-ttu-id="0ef33-112">Von Q# werden einige primitive Typen bereitgestellt, und es gibt zwei Möglichkeiten (Arrays und Tupel) zum Erstellen von neuen strukturierten Typen.</span><span class="sxs-lookup"><span data-stu-id="0ef33-112">Q# provides a small set of primitive types, along with two ways (arrays and tuples) for creating new, structured types.</span></span>
<span data-ttu-id="0ef33-113">Es wird ein einfaches Prozedurmodell zum Schreiben von Programmen mit Schleifen und If/Then-Anweisungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-113">It supports a basic procedural model for writing programs, with loops and if/then statements.</span></span>
<span data-ttu-id="0ef33-114">Die Konstrukte der obersten Ebene in Q# sind benutzerdefinierte Typen, Vorgänge und Funktionen.</span><span class="sxs-lookup"><span data-stu-id="0ef33-114">The top-level constructs in Q# are user defined types, operations, and functions.</span></span>

<span data-ttu-id="0ef33-115">In den folgenden Abschnitten finden Sie hilfreiche Informationen:</span><span class="sxs-lookup"><span data-stu-id="0ef33-115">The following sections detail:</span></span>
- [<span data-ttu-id="0ef33-116">Typmodell</span><span class="sxs-lookup"><span data-stu-id="0ef33-116">The Type Model</span></span>](xref:microsoft.quantum.language.type-model)
- [<span data-ttu-id="0ef33-117">Ausdrücke</span><span class="sxs-lookup"><span data-stu-id="0ef33-117">Expressions</span></span>](xref:microsoft.quantum.language.expressions)
- [<span data-ttu-id="0ef33-118">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="0ef33-118">Statements</span></span>](xref:microsoft.quantum.language.statements)
- [<span data-ttu-id="0ef33-119">Dateistruktur</span><span class="sxs-lookup"><span data-stu-id="0ef33-119">File Structure</span></span>](xref:microsoft.quantum.language.file-structure)

## <a name="conventions"></a><span data-ttu-id="0ef33-120">Konventionen</span><span class="sxs-lookup"><span data-stu-id="0ef33-120">Conventions</span></span>

<span data-ttu-id="0ef33-121">Derzeit arbeiten wir auf das Ziel hin, dass in allen Fällen eine einheitliche allgemeine Interpunktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ef33-121">We are working to ensure that common punctuation marks are used consistently in all situations.</span></span>
<span data-ttu-id="0ef33-122">Dahinter steht die Erwartung, dass Q# so einfacher zu erlernen und zu lesen ist. Der Grund ist, dass die Interpunktion dann immer die gleiche Bedeutung hat und ein Konzept immer auf die gleiche Weise dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="0ef33-122">We expect that this will make Q# easier to learn and to read because these marks always mean the same thing, and the same concept is always represented the same way.</span></span>

<span data-ttu-id="0ef33-123">Dies gilt insbesondere in folgenden Fällen:</span><span class="sxs-lookup"><span data-stu-id="0ef33-123">Specifically:</span></span>

- <span data-ttu-id="0ef33-124">Das Semikolon (`;`) wird als Abschluss einer ein- oder mehrzeiligen Anweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ef33-124">The semi-colon, `;`, is used to end a statement or single-line directive.</span></span>
  <span data-ttu-id="0ef33-125">Es wird nicht für andere Zwecke genutzt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-125">It is not used for any other purpose.</span></span>
- <span data-ttu-id="0ef33-126">Das Komma (`,`) wird verwendet, um Elemente einer Sequenz zu trennen.</span><span class="sxs-lookup"><span data-stu-id="0ef33-126">The comma, `,`, is used to separate elements of a sequence.</span></span> <span data-ttu-id="0ef33-127">Es wird für Tupelliterale, Arrayliterale, Argumentlisten, Tupeldefinitionen und Typlisten genutzt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-127">It is used for tuple literals, array literals, argument lists, tuple definitions, and type lists.</span></span> <span data-ttu-id="0ef33-128">**Aufgrund einer Änderung gegenüber früheren Versionen wird `;` nicht mehr als Arrayliteral-Trennzeichen unterstützt.**</span><span class="sxs-lookup"><span data-stu-id="0ef33-128">**In a change from earlier versions, `;` is no longer supported as an array literal separator.**</span></span>
- <span data-ttu-id="0ef33-129">Der Doppelpunkt (`:`) wird verwendet, um eine Typanmerkung einzufügen.</span><span class="sxs-lookup"><span data-stu-id="0ef33-129">The colon, `:`, is used to introduce a type annotation.</span></span> <span data-ttu-id="0ef33-130">Er wird hauptsächlich in aufrufbaren Signaturen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ef33-130">It is primarily used in callable signatures.</span></span>
  <span data-ttu-id="0ef33-131">Da mit dem Doppelpunkt immer eine Typsignatur eingefügt wird, wird für den in 0.3 eingeführten ternären bedingten Operator ein vertikaler Balken (`|`) verwendet, um die Wahr- und Falsch-Werte zu trennen. Aus diesem Grund wird in Q# als Trennzeichen `cond ? tval | fval` anstelle des Doppelpunkts wie in C genutzt.</span><span class="sxs-lookup"><span data-stu-id="0ef33-131">Because colon always introduces a type signature, the ternary conditional operator introduced in 0.3 uses a vertical bar, `|`, to separate the true and false values; thus, Q# uses `cond ? tval | fval` instead of the colon as separator as in C.</span></span>
  
