---
title: Quantum Dynamics
description: Informieren Sie sich über die Ähnlichkeiten und Unterschiede zwischen Quantum Dynamics und Classic Dynamics.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.quantumdynamics
no-loc:
- Q#
- $$v
ms.openlocfilehash: e63ec497f2a7747e172d5fbdc249fe4064c482b6
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869493"
---
# <a name="quantum-dynamics"></a>Quantum Dynamics

Die Quantum-Mechanik ist größtenteils die Studie von Quantum Dynamics, mit der erläutert wird, wie ein ursprünglicher Quantum-Zustand $ \ket{\psi (0)} $ im Laufe der Zeit variiert (Weitere Informationen zur Dirac-Notation finden Sie in den [konzeptionellen](xref:microsoft.quantum.concepts.dirac) Dokumentation zu Quantum Computing).
Insbesondere bei dieser anfänglichen Bedingung wird ein Quantum-Status, eine Evolution-Zeit und eine Spezifikation des quantalen dynamischen Systems, der Quantum-Status $ \ket{\psi (t)} $ gesucht.
Bevor wir mit der Erläuterung von Quantum Dynamics fortfahren, empfiehlt es sich, einen Schritt zurück zu machen und sich über klassische Dynamics Gedanken zu machen, da er Einblicke in die Möglichkeiten von Quantum-Mechanismen bietet, die sich von klassischen Dynamics unterscheiden.

In klassischer Dynamics: Wir wissen aus dem zweiten Gesetz von Newton, dass die Position eines Partikels gemäß $F (x, t) = MA = m\frac {\ DD ^ 2} {\dd t ^ 2} {x} (t) $ weiterentwickelt wird, wobei $F (x, t) $ die Kraft ist, $m $ die Beschleunigung ist und $a $ die Beschleunigung ist.
Bei einer anfänglichen Position $x (0) $, der Evolution time $t $ und der Beschreibung der Erzwingung der Kräfte, die auf das Partikel reagieren, können wir dann $x (t) $ suchen, indem wir die differenzielle Gleichung lösen, die von Newton-Gleichungen für $x (t) $ angegeben wird.
Das Angeben der Kräfte auf diese Weise ist ein wenig.
Wir werden also häufig die Erzwingung in Bezug auf die potenzielle Energie des Systems Ausdrücken, die US $-\ partial_x V (x, t) = m \bruchteil {\dd ^ 2} {\dd t ^ 2} {x} (t) $ ergibt.
Daher wird die Dynamik des Systems bei einem Partikel nur von der potenziellen Energie Funktion, der Partikelmasse und der Entwicklungszeit angegeben.

Eine umfassendere Sprache wird häufig für klassische Dynamics eingeführt, die über $F = MA $ hinausgeht.
Eine Formulierung, die besonders nützlich in der Quantum-Mechanik ist, ist hamiltona Mechanics.
In hamiltonan-Mechanismen enthalten die Gesamtenergie eines Systems und die (verallgemeinerten) Positionen und momenta alle Informationen, die zum Beschreiben der Bewegung eines beliebigen klassischen Objekts benötigt werden.
Lassen Sie $f (x, p, t) $ eine Funktion der generalisierten Positionen $x $ und momenta $p $ eines Systems, und lassen Sie $H (x, p, t) $ die hamiltonan-Funktion sein.
Wenn wir z. b. $f (x, p, t) = x (t) $ und $H (x, p, t) = p ^ 2 (t)/2M-V (x, t) $ nehmen, würden wir den obigen Fall von newtonan Dynamics wiederherstellen.
In der Generalität haben wir diese \begin{align} \frac{d}{dt} f &= \ partial_t f-(\ partial_x H \ partial_p f + \ partial_p H \ partial_x f) \\ \\ & \besiegq \ partial_t f + \\ {f, H \\ }.
\end{align} hier \\ wird $ {f, H \\ } $ als [Poisson-Klammer](https://en.wikipedia.org/wiki/Poisson_bracket) bezeichnet und ist aufgrund der zentralen Rolle, die beim Definieren von Dynamics spielt, in klassischer Dynamics allgegenwärtig.

Quantum Dynamics kann mit exakt derselben Sprache beschrieben werden.
Die hamiltonan oder die gesamte Energie gibt die Dynamics eines beliebigen geschlossenen Quantum-Systems vollständig an.
Es gibt jedoch einige wesentliche Unterschiede zwischen den beiden Theorien.
In klassischen Mechanismen $x $ und $p $ nur Zahlen, wohingegen Sie in Quantum-Mechanismen nicht.
Tatsächlich ist dies nicht der Fall: $XP \nE px $.

Das richtige mathematische Konzept zum Beschreiben dieser Objekte, die keine Objekte sind, ist ein Operator, der in Fällen, in denen $x $ und $p $ nur einen diskreten Satz von Werten annehmen kann, mit dem Konzept einer Matrix übereinstimmt.
Aus Gründen der Einfachheit gehen wir davon aus, dass unser Quantum-System so begrenzt ist, dass es mit [Vektoren und Matrizen](xref:microsoft.quantum.concepts.vectors)beschrieben werden kann.
Wir verlangen, dass diese Matrizen hermitian sind (was bedeutet, dass die konjugierte, die die Matrix durchläuft, mit der ursprünglichen Matrix identisch ist).
Dadurch wird sichergestellt, dass die Eigenwerte der Matrizen Real-wertig sind. eine Bedingung, die wir erzwingen, um sicherzustellen, dass eine Menge wie die Position gemessen wird, die wir nicht zurückerhalten.

Ebenso wie die analog zu Position und Schwung in der Quantum-Mechanik durch Operatoren ersetzt werden müssen, muss die hamiltonan-Funktion durch einen Operator ersetzt werden.
Bei einem Partikel im freien Speicherplatz haben wir z. b. $H (x, p) = p ^ 2/2M $, während in der Quantum-Mechanik der hamiltonan-Operator $ \hat{h} $ den Wert $ \hat{h} = \hat{p} ^ 2/2M $ hat.
Aus dieser Perspektive besteht der Wechsel von "klassisch" zu "Quantum Dynamics" lediglich darin, die in normaler Dynamics verwendeten Variablen durch Operatoren zu ersetzen.
Nachdem wir den hamiltonan-Operator durch Übersetzen der normalen klassischen hamiltona in die Quantum-Sprache erstellt haben, können wir die Dynamics einer beliebigen quantschen Menge Ausdrücken (d. h. Quantum-mechanischer Operator) $ \hat{fi} (t) $ Via \begin{align} \frac{d}{dt} \hat{fi} = \ partial_t \hat{Fi} + [\hat{fi}, \hat{h}], \end{align}, wobei $ [f, H] = fH-HF $ als der komorname bezeichnet wird.
Dieser Ausdruck ähnelt dem klassischen Ausdruck, der oben angegeben wurde. der Unterschied besteht darin, dass die Poisson-Klammer $ \\ {f, H \\ } $ durch den Pendler zwischen $f $ und $H $ ersetzt wird.
Dieses Verfahren, mit dem eine klassische hamiltona und die Verwendung zum Suchen eines Quantums hamiltonan verwendet werden, wird im Quantum-Jargon als kanonische Quantisierung bezeichnet.

An welchen Operatoren $f $ am meisten interessiert?  Die Antwort darauf hängt von dem Problem ab, das wir lösen möchten.
Die vielleicht nützlichste Menge, die Sie finden, ist der Quantum State-Operator, der in der vorherigen konzeptionellen Dokumentation verwendet werden kann, um alles zu extrahieren, was wir über die Dynamics erfahren würden.
Wenn Sie dies durchgeführt haben (und das Ergebnis so vereinfachen, dass es einen reinen Zustand hat), wird die Schrödinger-Gleichung für den Quantum-Status "\begin{align} i \ partial_t \ket{\psi (t)} = \hat{h} (t) \ket{\psi (t)}" gefunden.
\end{align}

Diese Gleichung, aber vielleicht weniger intuitiv als die oben genannten, liefert vielleicht den einfachsten Ausdruck, um zu verstehen, wie die Quantum-Dynamics auf einem Quantum-oder klassischen Computer simuliert werden kann.
Dies liegt daran, dass die Lösung der differenziellen Gleichung in der folgenden Form ausgedrückt werden kann (für den Fall, dass hamiltonan konstant ist in $t $) \begin{align} \ket{\psi (t)} = e ^ {-IHT} \ket{\psi (0)}.
\end{align} hier $e ^ {-IHT} $ eine einheitliche Matrix ist.
Dies bedeutet, dass eine Quantum-Verbindung vorhanden ist, die für die Ausführung entworfen werden kann, da Quantum-Computer eine genaue Näherung für jede einheitliche Matrix erreichen können.
Das Auffinden einer Quantum-Verbindung, um den Quantum Time Evolution-Operator $e ^ {-IHT} $ zu implementieren, ist das, was häufig als Quantum-Simulation bezeichnet wird, oder in einer speziellen Dynamical-Quantum-Simulation.
