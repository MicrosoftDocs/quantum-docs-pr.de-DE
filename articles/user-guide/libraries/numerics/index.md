---
title: Einführung in die numerische Quantenbibliothek | Microsoft-Dokumentation
description: Einführung in die numerische Quantenbibliothek
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: conceptual
uid: microsoft.quantum.numerics.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 017fd075596e7b5fb7107d3bc5f149b77dc4e504
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854005"
---
# <a name="introduction-to-the-quantum-numerics-library"></a>Einführung in die numerische Quantenbibliothek

Viele Quantenalgorithmen basieren auf [Orakeln](xref:microsoft.quantum.concepts.oracles), die mathematische Funktionen anhand einer Überlagerung von Eingaben auswerten.
Die Hauptkomponente des Shor-Algorithmus wertet beispielsweise $f(x) = a^x\operatorname{mod} N$ für ein festes $a$, den Faktor für $N$, sowie $x$ als ein ganzzahliges $2n$-Qubit in einer einheitlichen Überlagerung aller Zeichenfolgen mit $2n$ Bits aus.

Soll der Shor-Algorithmus auf einem echten Quantencomputer ausgeführt werden, muss diese Funktion als Term der nativen Vorgänge des Zielcomputers geschrieben werden.
Wird die binäre Darstellung von $x$ verwendet, bei der $x_i$ das $i$-te Bit beginnend mit dem unwichtigsten Bit angibt, kann $f(x)$ als $f(x) = a^{\sum_{i=0}^{2n-1} x_i 2^i} \operatorname{mod} N$ geschrieben werden.
Dies kann wiederum als Produkt (mod N) der Terme $a^{2^i x_i}=(a^{2^i})^{x_i}$ geschrieben werden. Die Funktion $f(x)$ kann daher mit einer Sequenz von $2n$ (modularen) Multiplikationen mit $a^{2^i}$ implementiert werden, sofern $x_i$ ungleich 0 (null) ist. Die Konstanten $a^{2^i}$ können vor der Ausführung des Algorithmus vorab berechnet und um Modulo N reduziert werden.

Diese Sequenz kontrollierter modularer Multiplikationen kann noch weiter vereinfacht werden: Jede Multiplikation kann mit einer Sequenz aus $n$ kontrollierten modularen Additionen ausgeführt werden, und jede modulare Addition kann aus einer regulären Addition und einem Vergleichsoperator gebildet werden.


Angesichts der Vielzahl an Schritten, die für die tatsächliche Implementierung erforderlich sind, wäre es äußerst hilfreich, diese Funktion schon gleich zu Beginn zur Verfügung zu haben.
Aus diesem Grund bietet das Quantum Development Kit Unterstützung für eine ganze Reihe numerischer Funktionen.


## <a name="functionality"></a>Funktionalität

Neben der bisher erwähnten Ganzzahlarithmetik bietet die numerische Bibliothek Funktionen mit

- ganzen Zahlen mit/ohne Vorzeichen (Multiplikation, Quadrierung, Division mit Rest, Inversion usw.) mit einer oder zwei ganzzahligen Quantenzahlen als Eingabe
- Festkommawerten (Addition, Subtraktion, Multiplikation, Quadrierung, 1/x, Polynomauswertung) mit einer oder zwei Festkomma-Quantenzahlen als Eingabe

## <a name="getting-started"></a>Erste Schritte

> [!div class="nextstepaction"]
> [Erfahren Sie mehr zur Verwendung der numerischen Bibliothek](xref:microsoft.quantum.numerics.usage)
