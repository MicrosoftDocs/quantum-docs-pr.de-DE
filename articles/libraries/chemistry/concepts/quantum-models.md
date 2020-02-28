---
title: Quantum-Modelle für elektronische Systeme
description: Erfahren Sie, wie Molekulare elektronische Systeme mithilfe von Quantum-Modellierung simuliert werden.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantummodels
ms.openlocfilehash: 9f9fc37944dd76026c2641d9cdf126e71053a598
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904416"
---
# <a name="quantum-models-for-electronic-systems"></a>Quantum-Modelle für elektronische Systeme

Zum simulieren elektronischer Systeme müssen Sie zunächst den hamiltonan angeben, der durch die oben beschriebene kanonische quantifizierungsprozedur gefunden werden kann.
Insbesondere für $N _E $-Elektronen mit momenta $p _I $ (in drei Dimensionen) und Massen $m _E $ und Positions Vektoren $x _I $ zusammen mit Kernen mit Gebühren $Z _K e $ an Positionen $y _K $, der hamiltonan-Operator liest \begin{Equation} \hat{h} = \sum\_{i = 1} ^ {N\_e} \bruchteil {\hat{p}\_i ^ 2} {2 m\_e} + \frac{1}{2}\sum\_{i\ne j} \bruchteil {e ^ 2} {| \hat{x}\_i-\hat{x}\_j |}-\sum\_{i , k} \bruchteil {z\_KE ^ 2} {| \hat{x}\_i-{y}\_k |} + \frac{1}{2} \ sum_ {k\ne k '} \bruchteil {z\_KZ\_{k '} e ^ 2} {| y\_k-y\_k ' |}. \label{EQ: Ham} \end{Equation} die momenta-Operatoren $ \hat{p}\_i ^ 2 $ können als laplacian-Operatoren in einem echten Bereich angezeigt werden. d. h. $ \hat{p}\_i ^ 2 =-\partielle\_{x\_i} ^ 2-\partielle\_{y\_i} ^ 2-\ partiell\_{z\_i} ^ 2 $.
Hier haben wir die vereinfachte Annahme gemacht, dass die Kerne für das Molekül im Ruhezustand sind.
Dies wird als "Born-Oppenheimer Näherung" bezeichnet und ist in der Regel für das Energieverbrauchs Spektrum von $ \hat{h} $ gültig, da die Elektronenmasse ungefähr $1/1836 $ der Masse eines Proton entspricht.
Dieser Hamiltonoperator kann problemlos gefunden werden, indem die Energie für ein System von $N\_e $-Elektronen geschrieben und der in [Quantum Dynamics](xref:microsoft.quantum.chemistry.concepts.quantumdynamics)beschriebene kanonische quantifizierungsprozess angewendet wird.

Um die einheitliche Matrix Darstellung für $e ^ {-i\hat {H} t} $ zu erstellen, muss der Operator $ \hat{h} $ als Matrix dargestellt werden.
Hierfür müssen wir ein Koordinatensystem oder eine Basis auswählen, um das Problem in darzustellen.
Wenn z. b. $ \ psi_j $ eine Reihe von orthogonalen Basisfunktionen für die $N _E $-Elektronen sind, können wir die Matrix definieren.

\begin{Equation} H\_{i, j} = \int\_{-\infty} ^ \infty\int\_{-\infty} ^ \infty \psi ^ {\*}\_i (x\_1) \hat{h} \psi\_j (x\_2) \dd ^ 3X\_1 \dd ^ 3X\_2. \ Bezeichnung {EQ: diskreteham} \end{Equation}

Im Prinzip ist der Operator $ \hat{h} $ unbegrenzt und führt nicht zu einem begrenzten dimensionalen Raum. die Matrix mit Elementen $H\_\{i, j\}$ oben.
Dies bedeutet, dass Fehler auftreten, indem eine zu geringe Basis festgelegt wird. Wenn Sie jedoch eine große Basis auswählen, kann die Simulation der chemischen Dynamics nicht praktikabel sein.
Aus diesem Grund ist es wichtig, eine Grundlage für die Lösung des Problems mit der elektronischen Struktur auszuwählen.

Es gibt viele geeignete Grundlagen, die verwendet werden können, und die Wahl einer guten Grundlage für das Problem ist ein Großteil der Kunst der Quantum-Chemie.
Die einfachsten diese Basissätze sind Slater-Type-Orbitals (STO), bei denen es sich um (orthogonalisierte) Lösungen für die Schrödinger-Gleichung (d. h. Eigenfunktionen von $ \hat{h} $) für Wasserstoff ähnliche Atome handelt.
Andere Basissätze, wie z. b. "Plane-Wellen" oder "Real-Space Orbitals", können verwendet werden, und für detailliertere Informationen wird der neugierige Reader auf den standardmäßigen Text ["Molekulare elektronischer Struktur Theorie"](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119019572) von helgaker verwiesen.

Obwohl die im obigen Modell verwendeten Zustände willkürlich erscheinen können, werden von Quantum-Mechanismen Einschränkungen hinsichtlich der Zustände festgestellt, die sich in der Art befinden.
Insbesondere müssen alle gültigen elektronischen Quantum-Zustände unter austauschen von Elektronen Bezeichnungen antisymmetrisch sein.
Das heißt, wenn $ \psi (x_1 x_2) $ die Wave-Funktion für den gemeinsamen Quantum-Status von zwei Elektronen wäre, benötigen wir dieses $ $ \psi (x_1, x_2) =-\psi (x_2, x_1).
$ $ Das Ausschlussprinzip von Pauli, das zwei Elektronen verbietet, sich jemals im gleichen Quantum-Zustand befinden zu müssen, ist, dass es sich um eine direkte Folge dieses Gesetzes handelt, die von der Tatsache als intuitiv betrachtet werden kann, dass zwei andere Elektronen an derselben Position $ \psi (x_1 x_1) \mapsto \psi ausgetauscht werden. x_1, x_1) \nE-\psi (x_1, x_1) $, es sei denn, $ \psi (x_1, x_1) = 0 $.
Daher müssen die anfänglichen Zustände für diese antisymmetrieneigenschaft ausgewählt werden, und es gibt wiederum nie zwei-Elektronen im gleichen Zustand gleichzeitig.
Dies ist für die elektronische Struktur von entscheidender Bedeutung, da es nicht mehr möglich ist, dass sich mehrere Elektronen im selben Zustand befinden, und die Verwendung eines einzelnen Quantum-Bits zum Speichern der Anzahl von Elektronen in einem bestimmten Quantum-Zustand durch Quantum-Computer ermöglicht wird.

Obwohl die Quantum-Mechanismen auf einem Quantum-Computer durch diskretisierungsweise simuliert werden können, hat die meisten Aufgaben im Feld Diese Vorgehensweise vermieden, weil Sie viele Qubits zum Speichern der Zustände benötigt und eine komplizierte Zustands Vorbereitungs Prozedur zum Vorbereiten eines antisymmetrischer Anfangszustand.
Glücklicherweise können diese Probleme jedoch durch die Anzeige des Simulations Problems aus einer anderen Perspektive ausgeblendet werden.
