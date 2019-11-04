---
title: Einführung in die numerische Quantenbibliothek | Microsoft-Dokumentation
description: Einführung in die numerische Quantenbibliothek
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.intro
ms.openlocfilehash: efd1a712616534ac281433fc008f0983271881d7
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442448"
---
# <a name="introduction-to-the-quantum-numerics-library"></a><span data-ttu-id="12fd5-103">Einführung in die numerische Quantenbibliothek</span><span class="sxs-lookup"><span data-stu-id="12fd5-103">Introduction to the Quantum Numerics Library</span></span>

<span data-ttu-id="12fd5-104">Viele Quantenalgorithmen basieren auf [Orakeln](xref:microsoft.quantum.concepts.oracles), die mathematische Funktionen anhand einer Überlagerung von Eingaben auswerten.</span><span class="sxs-lookup"><span data-stu-id="12fd5-104">Many quantum algorithms rely on [oracles](xref:microsoft.quantum.concepts.oracles) that evaluate mathematical functions on a superposition of inputs.</span></span>
<span data-ttu-id="12fd5-105">Die Hauptkomponente des Shor-Algorithmus wertet beispielsweise $f(x) = a^x\operatorname{mod} N$ für ein festes $a$, den Faktor für $N$, sowie $x$ als ein ganzzahliges $2n$-Qubit in einer einheitlichen Überlagerung aller Zeichenfolgen mit $2n$ Bits aus.</span><span class="sxs-lookup"><span data-stu-id="12fd5-105">The main component of Shor's algorithm, for example, evaluates $f(x) = a^x\operatorname{mod} N$ for a fixed $a$, the number to factor $N$, and $x$ a $2n$-qubit integer in a uniform superposition over all $2n$-bit strings.</span></span>

<span data-ttu-id="12fd5-106">Soll der Shor-Algorithmus auf einem echten Quantencomputer ausgeführt werden, muss diese Funktion als Term der nativen Vorgänge des Zielcomputers geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="12fd5-106">To run Shor's algorithm on an actual quantum computer, this function has to be written in terms of the native operations of the target machine.</span></span>
<span data-ttu-id="12fd5-107">Wird die binäre Darstellung von $x$ verwendet, bei der $x_i$ das $i$-te Bit beginnend mit dem unwichtigsten Bit angibt, kann $f(x)$ als $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$ geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="12fd5-107">Using the binary representation of $x$ with $x_i$ denoting the $i$-th bit counting from the least-significant bit, $f(x)$ can be written as $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$.</span></span>
<span data-ttu-id="12fd5-108">Dies kann wiederum als Produkt (mod N) der Terme $a^{2^i x_i}=(a^{2^i})^{x_i}$ geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="12fd5-108">In turn, this can be written as a product (mod N) of terms $a^{2^i x_i}=(a^{2^i})^{x_i}$.</span></span> <span data-ttu-id="12fd5-109">Die Funktion $f(x)$ kann daher mit einer Sequenz von $2n$ (modularen) Multiplikationen mit $a^{2^i}$ implementiert werden, sofern $x_i$ ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="12fd5-109">The function $f(x)$ can thus be implemented using a sequence of $2n$ (modular) multiplications by $a^{2^i}$ conditional on $x_i$ being nonzero.</span></span> <span data-ttu-id="12fd5-110">Die Konstanten $a^{2^i}$ können vor der Ausführung des Algorithmus vorab berechnet und um Modulo N reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="12fd5-110">The constants $a^{2^i}$ can be precomputed and reduced modulo N before running the algorithm.</span></span>

<span data-ttu-id="12fd5-111">Diese Sequenz kontrollierter modularer Multiplikationen kann noch weiter vereinfacht werden: Jede Multiplikation kann mit einer Sequenz aus $n$ kontrollierten modularen Additionen ausgeführt werden, und jede modulare Addition kann aus einer regulären Addition und einem Vergleichsoperator gebildet werden.</span><span class="sxs-lookup"><span data-stu-id="12fd5-111">This sequence of controlled modular multiplications can be simplified further: Each multiplication can be performed using a sequence of $n$ controlled modular additions; and each modular addition can be built from a regular addition and a comparator.</span></span>


<span data-ttu-id="12fd5-112">Angesichts der Vielzahl an Schritten, die für die tatsächliche Implementierung erforderlich sind, wäre es äußerst hilfreich, diese Funktion schon gleich zu Beginn zur Verfügung zu haben.</span><span class="sxs-lookup"><span data-stu-id="12fd5-112">Given that so many steps are necessary to arrive at an actual implementation, it would be extremely helpful to have such functionality available from the start.</span></span>
<span data-ttu-id="12fd5-113">Aus diesem Grund bietet das Quantum Development Kit Unterstützung für eine ganze Reihe numerischer Funktionen.</span><span class="sxs-lookup"><span data-stu-id="12fd5-113">This is why the Quantum Development Kit provides support for a wide range of numerics functionality.</span></span>


## <a name="functionality"></a><span data-ttu-id="12fd5-114">Funktionalität</span><span class="sxs-lookup"><span data-stu-id="12fd5-114">Functionality</span></span>

<span data-ttu-id="12fd5-115">Neben der bisher erwähnten Ganzzahlarithmetik bietet die numerische Bibliothek Funktionen mit</span><span class="sxs-lookup"><span data-stu-id="12fd5-115">Besides the integer arithmetic mentioned thus far, the numerics library provides</span></span>

 - <span data-ttu-id="12fd5-116">ganzen Zahlen mit/ohne Vorzeichen (Multiplikation, Quadrierung, Division mit Rest, Inversion usw.) mit einer oder zwei ganzzahligen Quantenzahlen als Eingabe</span><span class="sxs-lookup"><span data-stu-id="12fd5-116">(Un)signed integer functionality (multiply, square, division with remainder, inversion, ...) with one or two quantum integer numbers as input</span></span>
 - <span data-ttu-id="12fd5-117">Festkommawerten (Addition, Subtraktion, Multiplikation, Quadrierung, 1/x, Polynomauswertung) mit einer oder zwei Festkomma-Quantenzahlen als Eingabe</span><span class="sxs-lookup"><span data-stu-id="12fd5-117">Fixed-point functionality (add / subtract, multiply, square, 1/x, polynomial evaluation) with one or two quantum fixed-point numbers as input</span></span>

## <a name="getting-started"></a><span data-ttu-id="12fd5-118">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="12fd5-118">Getting started</span></span>

<span data-ttu-id="12fd5-119">Informationen zu den ersten Schritten mit der numerischen Bibliothek finden Sie im [Installationshandbuch](xref:microsoft.quantum.numerics.installation) sowie weitere Informationen unter [Verwenden der numerischen Bibliothek](xref:microsoft.quantum.numerics.usage).</span><span class="sxs-lookup"><span data-stu-id="12fd5-119">To get started with the Numerics Library, check out the [installation guide](xref:microsoft.quantum.numerics.installation) and more information on [using the Numerics Library](xref:microsoft.quantum.numerics.usage).</span></span>
