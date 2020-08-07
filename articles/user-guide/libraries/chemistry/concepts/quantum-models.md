---
title: Quantum-Modelle für elektronische Systeme
description: Erfahren Sie, wie Molekulare elektronische Systeme mithilfe von Quantum-Modellierung simuliert werden.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantummodels
no-loc:
- Q#
- $$v
ms.openlocfilehash: f6b652ef3e315ded5b4e39fd65a2f6be7070d7fa
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869476"
---
# <a name="quantum-models-for-electronic-systems"></a>Quantum-Modelle für elektronische Systeme

Zum simulieren elektronischer Systeme müssen Sie zunächst den hamiltonan angeben, der durch die oben beschriebene kanonische quantifizierungsprozedur gefunden werden kann.
Insbesondere für $N _E $-Elektronen mit momenta $p _I $ (in drei Dimensionen) und Massen $m _E $ und Positions Vektoren $x _I $ zusammen mit Kernen mit Gebühren $Z _K e $ an Positionen $y _K $, der hamiltonan-Operator liest \begin{Equation} \hat{h} = \sum \_ {i = 1} ^ {N \_ e} \bruchteil {\hat{p} \_ i ^ 2} {2M \_ e} + \frac {1} {2} \sum \_ {i\ne j} \bruchteil {e ^ 2} {| \hat{x} \_ i-\hat{x} \_ j |}-\sum \_ {i, k} \bruchteil {z \_ KE ^ 2} {| \hat{x} \_ i-{y} \_ k |} + \frac {1} {2} \ sum_ {k\ne k '} \bruchteil {z \_ KZ \_ {k '} e ^ 2} {| y \_ k-y \_ ' |}. \label{EQ: Ham} \end{Equation} die momenta-Operatoren $ \hat{p} \_ i ^ 2 $ können im echten Raum als laplacian-Operatoren angezeigt werden, d. h. $ \hat{p} \_ i ^ 2 =-\partielle \_ {x \_ i} ^ 2-\partial { \_ y \_ i} ^ 2-\partiell \_ {z \_ i}
Hier haben wir die vereinfachte Annahme gemacht, dass die Kerne für das Molekül im Ruhezustand sind.
Dies wird als "Born-Oppenheimer Näherung" bezeichnet und ist in der Regel für das Energieverbrauchs Spektrum von $ \hat{h} $ gültig, da die Elektronenmasse ungefähr $1/1836 $ der Masse eines Proton entspricht.
Dieser hamiltonaloperator kann problemlos gefunden werden, indem die Energie für ein System mit $N \_ e $-Elektronen geschrieben und der in [Quantum Dynamics](xref:microsoft.quantum.chemistry.concepts.quantumdynamics)beschriebene kanonische quantifizierungsprozess angewendet wird.

Um die einheitliche Matrix Darstellung für $e ^ {-i\hat {H} t} $ zu erstellen, muss der Operator $ \hat{h} $ als Matrix dargestellt werden.
Hierfür müssen wir ein Koordinatensystem oder eine Basis auswählen, um das Problem in darzustellen.
Wenn z. b. $ \ psi_j $ eine Reihe von orthogonalen Basisfunktionen für die $N _E $-Elektronen sind, können wir die Matrix definieren.

\begin{Equation} H \_ {i, j} = \int \_ {-\infty} ^ \infty\int \_ {-\infty} ^ \infty \psi ^ { \* } \_ i (x \_ 1) \hat{h} \psi \_ j (x \_ 2) \dd ^ 3X \_ 1 \dd ^ 3X \_ 2. \ Bezeichnung {EQ: diskreteham} \end{Equation}

Im Prinzip ist der Operator $ \hat{h} $ unbegrenzt und wirkt sich nicht auf einen begrenzten dimensionalen Raum aus, die Matrix mit den Elementen $H \_ \{ i, j \} $ oben.
Dies bedeutet, dass Fehler auftreten, indem eine zu geringe Basis festgelegt wird. Wenn Sie jedoch eine große Basis auswählen, kann die Simulation der chemischen Dynamics nicht praktikabel sein.
Aus diesem Grund ist es wichtig, eine Grundlage für die Lösung des Problems mit der elektronischen Struktur auszuwählen.

Es gibt viele geeignete Grundlagen, die verwendet werden können, und die Wahl einer guten Grundlage für das Problem ist ein Großteil der Kunst der Quantum-Chemie.
Die einfachsten diese Basissätze sind Slater-Type-Orbitals (STO), bei denen es sich um (orthogonalisierte) Lösungen für die Schrödinger-Gleichung (d. h. Eigenfunktionen von $ \hat{h} $) für Wasserstoff ähnliche Atome handelt.
Andere Basissätze, wie z. b. "Plane-Wellen" oder "Real-Space Orbitals", können verwendet werden, und für detailliertere Informationen wird der neugierige Reader auf den standardmäßigen Text ["Molekulare elektronischer Struktur Theorie"](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119019572) von helgaker verwiesen.

Obwohl die im obigen Modell verwendeten Zustände willkürlich erscheinen können, werden von Quantum-Mechanismen Einschränkungen hinsichtlich der Zustände festgestellt, die sich in der Art befinden.
Insbesondere müssen alle gültigen elektronischen Quantum-Zustände unter austauschen von Elektronen Bezeichnungen antisymmetrisch sein.
Das heißt, wenn $ \psi (x_1 x_2) $ die Wave-Funktion für den gemeinsamen Quantum-Status von zwei Elektronen wäre, benötigen wir dieses $ $ \psi (x_1, x_2) =-\psi (x_2, x_1).
$ $ Das-Ausschlussprinzip von Pauli, das zwei Elektronen verbietet, jemals denselben Quantum-Zustand zu haben, lautet: im Grunde genommen kann eine direkte Konsequenz dieses Gesetzes als intuitional aus der Tatsache bestehen, dass zwei Elektronen, die sich an derselben Position wie $ \psi (x_1, x_1) \mapsto \psi (x_1, x_1) \nE-\psi (x_1, x_1) $ befinden, außer $ \psi (x_1 , x_1) = 0 $.
Daher müssen die anfänglichen Zustände für diese antisymmetrieneigenschaft ausgewählt werden, und es gibt wiederum nie zwei-Elektronen im gleichen Zustand gleichzeitig.
Dies ist für die elektronische Struktur von entscheidender Bedeutung, da es nicht mehr möglich ist, dass sich mehrere Elektronen im selben Zustand befinden, und die Verwendung eines einzelnen Quantum-Bits zum Speichern der Anzahl von Elektronen in einem bestimmten Quantum-Zustand durch Quantum-Computer ermöglicht wird.

Obwohl die Quantum-Mechanismen auf einem Quantum-Computer durch diskretisierungsweise simuliert werden können, hat die meisten Aufgaben im Feld Diese Vorgehensweise vermieden, weil Sie viele Qubits zum Speichern der Zustände benötigt und eine komplizierte Zustands Vorbereitungs Prozedur benötigt, um einen antisymmetrischen Anfangszustand vorzubereiten.
Glücklicherweise können diese Probleme jedoch durch die Anzeige des Simulations Problems aus einer anderen Perspektive ausgeblendet werden.
