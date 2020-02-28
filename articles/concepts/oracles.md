---
title: Quantenorakel
description: Erfahren Sie, wie Sie mithilfe von Quantum-Oracles, Black Box-Vorgängen, die als Eingabe für einen anderen Algorithmus verwendet werden, arbeiten und definieren.
author: cgranade
uid: microsoft.quantum.concepts.oracles
ms.author: Christopher.Granade@microsoft.com
ms.date: 07/11/2018
ms.topic: article
ms.openlocfilehash: 1d1d0b0903db8e994166c3e8a5798f70742a1c7e
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904926"
---
# <a name="quantum-oracles"></a>Quantum-Oracles

Bei einem Oracle-$O $ handelt es sich um einen "Blackbox"-Vorgang, der als Eingabe für einen anderen Algorithmus verwendet wird.
Häufig werden solche Vorgänge mithilfe eines klassischen Funktions $f definiert: \\{0, 1\\} ^ n \to \\{0, 1\\} ^ m $, das eine $n $-Bit-Binär Eingabe annimmt und eine $m $-Bit-Binär Ausgabe erzeugt.
Beachten Sie hierzu eine bestimmte binäre Eingabe $x = (x_{0}, x_{1}, \dots, x_ {n-1}) $.
Wir können Qubit-Zustände als "$ \ket{\vec{x}} = \ket{x_{0}} \otimes \ket{x_{1}} \otimes \cdots \otimes \ket{x_ {n-1}} $" bezeichnen.

Wir könnten zuerst versuchen, $O $ zu definieren, sodass $O \ket{x} = \ket{f (x)} $, dies hat jedoch einige Probleme.
Erstens kann $f $ eine andere Größe von Eingabe und Ausgabe aufweisen ($n \nE m $), sodass die Anzahl der Qubits im Register durch Anwenden von $O $ geändert würde.
Zweitens, auch wenn $n = m $, ist die Funktion möglicherweise nicht invertierbar: Wenn $f (x) = f (y) $ für einige $x \nE y $, $O \ket{x} = o\ket {y} $, aber $O ^ \dagger o\ket {x} \nE O ^ \dagger o\ket {y} $.
Dies bedeutet, dass wir den Adjoint-Vorgang nicht erstellen können $O ^ \dagger $, und für Oracles muss ein Adjoint-Element definiert sein.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>Definieren eines Oracle-Effekts durch seine Auswirkung auf den Berechnungsbasis Status
Wir können diese beiden Probleme behandeln, indem wir ein zweites Register $m $ Qubits zum Speichern unserer Antwort einführen.
Anschließend definieren wir die Auswirkung des Oracle auf alle Berechnungs Status Zustände: für alle $x \in \\{0, 1\\} ^ n $ und $y \in \\{0, 1\\} ^ m $,

$ $ \begin{align} O (\ket{x} \otimes \ket{y}) = \ket{x} \otimes \ket{y \oplus f (x)}.
\end{align} $ $

Nun $O = O ^ \dagger $ by Construction, daher haben wir beide früheren Probleme gelöst.

> [!TIP]
> Um zu sehen, dass $O = O ^ {\dagger} $ ist, beachten Sie, dass $O ^ 2 = \boldone $ seit $a \oplus b \oplus b = a $ for all $a, b \in \{0, 1\}$.
> Als Ergebnis $O \ket{x} \ket{y \oplus f (x)} = \ket{x} \ket{y \oplus f (x) \oplus f (x)} = \ket{x} \ket{y} $.

Wichtig: die Definition eines Oracle auf diese Weise für jeden Berechnungsbasis Status $ \ket{x}\ket{y} $ definiert auch, wie $O $ für jeden anderen Zustand agiert.
Dies folgt unmittelbar daran, dass $O $ (wie alle Quantum-Vorgänge) linear in dem Zustand ist, in dem Sie agiert.
Beachten Sie beispielsweise den Hadamard-Vorgang, der durch $H \ket{0} = \ket{+} $ und $H \ket{1} = \ket{-}$ definiert wird.
Wenn Sie wissen möchten, wie $H $ auf $ \ket{+} $ reagiert, können wir diesen $H $ ist linear verwenden,

$ $ \begin{align} h\ket {+} & = \frac{1}{\sqrt{2}} H (\ket{0} + \ket{1}) = \frac{1}{\sqrt{2}} (h\ket{0} + h\ket{1}) \\\\ & = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}) = \bruch12 (\ket{0} + \ket{1} + \ket{0}-\ket{1}) = \ket{0}.
\end{align} $ $

Wenn wir unsere Oracle-$O $ definieren, können wir auf ähnliche Weise den Status $ \ket{\psi} $ auf $n + m $ Qubits schreiben als

$ $ \begin{align} \ket{\psi} & = \ sum_ {x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \alpha (x, y) \ket{x} \ket{y} \end{align} $ $

wobei $ \alpha: \\{0, 1\\} ^ n \times \\{0, 1\\} ^ m \to \mathbb{c} $ die Koeffizienten des Zustands $ \ket{\psi} $ darstellt. Bisher

$ $ \begin{align} O \ket{\psi} & = o \ sum_ {x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \alpha (x, y) \ket{x} \ket{y} \\\\ & = \ sum_ {x \in \\{0, 1\\} ^ n, y \in \\{0, 1\\} ^ m} \alpha (x, y) O \ket{x} \ket{y} \\\\ & = \ sum_ {x \in \\{0, 1\\} ^ n , y \in \\{0, 1\\} ^ m} \alpha (x, y) \ket{x} \ket{y \oplus f (x)}.
\end{align} $ $

## <a name="phase-oracles"></a>Phasen-Oracles
Alternativ dazu können Sie $f $ in eine Oracle-$O $ codieren, indem Sie eine _Phase_ auf der Grundlage der Eingabe für $O $ anwenden.
Beispielsweise können wir $O $ so definieren, dass $ $ \begin{align} O \ket{x} = (-1) ^ {f (x)} \ket{x}.
\end{align} $ $ wenn ein Phasen-Oracle zuerst auf ein Register im Berechnungs Status $ \ket{x} $ zuarbeitet, ist diese Phase eine globale Phase und daher nicht Observable.
Ein solches Oracle kann jedoch eine sehr leistungsfähige Ressource sein, wenn Sie auf eine übergeordnete Position oder einen kontrollierten Vorgang angewendet wird.
Nehmen Sie z. b. eine Phase Orcale $O _F $ für eine Single-Qubit-Funktion $f $.
Dann $ $ \begin{align} O_f \ket{+} & = O_f (\ket{0} + \ket{1})/\sqrt{2} \\\\ & = ((-1) ^ {f (0)} \ket{0} + (-1) ^ {f (1)} \ket{1})/\sqrt{2} \\\\ & = (-1) ^ {f (0)} (\ket{0} + (-1) ^ {f (1)-f (0)} \ket{1})/\sqrt{2} \\\\ & = (-1) ^ {f (0)} Z ^ {f (0)-f (1)} \ket{+}.
\end{align} $ $

Im Allgemeinen können beide Sichten von Oracles erweitert werden, um klassische Funktionen darzustellen, die anstelle eines einzelnen Bits reelle Zahlen zurückgeben.

Das Auswählen der besten Methode zum Implementieren eines Oracle hängt stark davon ab, wie dieses Oracle innerhalb eines bestimmten Algorithmus verwendet werden soll.
Der " [Deutsch-Jozsa"-Algorithmus](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) basiert z. b. auf dem Oracle, der auf die erste Weise implementiert ist, während der [-Algorithmus von Grover](https://en.wikipedia.org/wiki/Grover's_algorithm) auf die zweite Weise implementiert ist.


Weitere Informationen finden Sie unter [gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465).
