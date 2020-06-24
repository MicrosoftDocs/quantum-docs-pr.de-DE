---
title: Darstellung von Jordanien-Wigner
description: Erfahren Sie mehr über die Darstellung von Jordanien-Wigner, bei der hamiltona-Operatoren einheitlichen Matrizen zugeordnet werden, die auf einem Quantum-Computer leichter implementiert werden können.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.jordanwigner
ms.openlocfilehash: 17cb473c6d33e3356d5da886f47985c3828d4d1f
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275097"
---
# <a name="jordan-wigner-representation"></a>Darstellung von Jordanien-Wigner

Während zweite quantifizierte hamiltonane in Bezug auf $a ^ \dagger $ (Creation) und $a $ (Vernichtung) praktisch dargestellt werden, sind diese Vorgänge keine grundlegenden Vorgänge in Quantum-Computern.
Daher müssen wir die Operatoren den einheitlichen Matrizen zuordnen, die auf einem Quantum-Computer implementiert werden können, wenn Sie auf einem Quantum-Computer implementiert werden sollen.
Die Darstellung von Jordan – Wigner bietet eine solche Zuordnung.
Andere, wie z. b. die "Bravyi – Kitaev"-Darstellung, sind jedoch auch vorhanden und haben ihre eigenen relativen vor-und Nachteile.
Der Hauptvorteil der Darstellung von Jordanien-Wigner ist die Einfachheit.

Die Darstellung von Jordanien-Wigner ist direkt zu ableiten.
Beachten Sie, dass der Status $ \ket {0} _J $ impliziert, dass Spin-Orbital $j $ leer ist, und $ \ket {1} _J $ impliziert, dass es belegt ist.
Dies bedeutet, dass Qubits die Besetzung einer bestimmten Drehfeld-Orbital-Methode auf natürliche Weise speichern kann.
Diese $a ^ \ dagger_j \ket {0} _J = \ket {1} _J $ und $a ^ \ dagger_j \ket {1} _J = $0.
Es ist leicht zu überprüfen, ob \begin{align} a ^ \ dagger_j &= \begin{bmatrix}0 & 0 \\ \ 1 &0 \ End{bmatrix} = \bruch{X_j-iY_j} {2} , \nonneuber \\ \\ a_j &= \begin{bmatrix}0 & 1 \\ \ 0 &0 \end{bmatrix} = \bruch{X_j + iY_j} {2} , \end{align}, wobei $X _J $ und $Y _J $ die "Pauli-$X $" und "-$Y $" sind, die für Qubit $j $ fungieren.

>[!NOTE]
> In f # stellt $ \ket {0} $ State den + 1-eigen Zustand des $Z $-Operators dar. In einigen Bereichen der Physik ist "$ \ket {0} $" der niedrige Energiezustand und somit der "-1"-eigen Status des $Z $-Operators. Daher können sich einige Formeln von gängigen Literatur unterscheiden.

In der Chemie Bibliothek verwenden wir $ \ket {0} $, um ein nicht belegtes Spin-Orbital darzustellen.
Dies zeigt, dass es bei einer einzelnen Spin-Orbital-Schnittstelle einfach Erstellungs-und Vernichtungs Operatoren in Bezug auf einheitliche Matrizen darstellen kann, die von Quantum-Computern verstanden werden
Beachten Sie, dass $X $ und $Y $ einheitlich sind $a ^ \dagger $ und $a $ nicht.
Wir werden später sehen, dass dies keine Herausforderung für die Simulation darstellt.

Ein Problem, das weiterhin besteht, besteht darin, dass für Systeme mit zwei oder mehr Spin-Orbitals ein Fehler auftritt.
Da Fermions antisymmetisch sind, wissen wir, dass $a ^ \ dagger_j a ^ \ dagger_k =-a ^ \ dagger_k a ^ \ dagger_j $ für beliebige $j $ und $k $.
$ $ \Left (\bruch{X_j-iY_j} {2} \right) \left (\bruchteil {X_k-iY_k} {2} \right) = \left (\bruchteil {X_k-iY_k} {2} \right) \left (\bruch{X_j-iY_j} {2} \right).
$ $ Mit anderen Worten: die beiden Erstellungs Operatoren führen bei Bedarf keinen eigenen Commit durch.
Dies kann jedoch in einem uneleganten Stil behoben werden.
Die Korrektur besteht darin, dass die "Pauli"-Operatoren auf natürliche Weise gegen den Verkehr
Insbesondere $XZ =-ZX $ und $YZ =-Zy $.
Durch die interspersing-$Z $-Operatoren in die Konstruktion des Operators können wir also die richtige Anti-typkommunikation emulieren.
Die vollständige Erstellung lautet wie folgt: 

\begin{align} a ^ \ dagger_1 &= \left (\bruchteil {x-iy} {2} \right) \otimes 1 \otimes 1 \otimes 1 \otimes \cdots \otimes 1, \\ \\ a ^ \ dagger_2 &= z\otimes\left (\bruchteil {x-iy} {2} \right) \otimes 1 \ otimes 1 \otimes \cdots \otimes 1, \\ \\ a ^ \ dagger_3 &= z\otimes z\otimes \left (\bruchteil {x-iy} {2} \right) \otimes 1 \otimes \cdots \otimes 1, \\ \\ & \vdots \\ \\ a ^ \ dagger_N &= z\otimes z\otimes z\otimes Z \otimes \cdots \otimes z\otimes \left (\bruchteil {x-iy} {2} \right). \label{EQ: JW} \end{align}

Es ist auch praktisch, die Zahlen Operatoren, $n _J $, in Bezug auf die Pauli-Operatoren auszudrücken.
Glücklicherweise brechen die Zeichen folgen von $Z $-Operatoren (als "Jordan-Wigner Strings" bezeichnet) ab, indem Sie diese Ersetzung durchführt.
Nach dem Ausführen dieser Aktion (und der $X _jY_j = iZ_j $) ist "\begin{Equation} n_j = a ^ \ dagger_j a_j = \bruchteil {(1-Z_j)}" vorhanden {2} .
\end{equation}


## <a name="constructing-hamiltonians-in-jordan-wigner-representation"></a>Erstellen von hamiltonane in der Darstellung von Jordanien-Wigner

Nachdem wir die Jordanien-Wigner-Darstellung aufgerufen haben, ist die Übersetzung der hamiltonan in eine Summe von Pauli-Operatoren gerade vorwärts.
Sie müssen lediglich jeden der $a ^ \dagger $ und $a $-Operatoren in der fermionic hamiltonan durch die oben angegebenen Zeichen folgen der Pauli-Operatoren ersetzen.
Wenn eine solche Ersetzung durchführt, gibt es nur fünf Klassen von Begriffen innerhalb der hamiltonan.
Diese fünf Klassen entsprechen den verschiedenen Methoden, mit denen wir die $p, q $ und $p, q, r, s $ im Textkörper und die zwei Text Begriffe in der hamiltonan auswählen können.
Diese fünf Klassen, bei denen $p>q>r #d2 s $ und Real-Wert-Orbitals

\begin{align} H_ {PP} a_p ^ \dagger a_p &= \ sum_p \bruchteil {H_ {PP}} {2} (1-Z_p) \\ \\ H_ {PQ} (a_p ^ \dagger a_q + a ^ \ dagger_q a_p) &= \bruchteil {H_ {PQ}} {2} \left (\ prod_ {j = q + 1} ^ {p-1} Z_j \right) \left (X_pX_q + Y_pY_q \right) \\ \\ H_ {pqqp} n_p n_q &= \bruch{H_ {pqqp}} {4} \left (1-Z_p-Z_q + Z_pZ_q \right) \\ \\ H_ {pqqr} &= \bruchteil {H_ {pqqr}} {2} \left (\ prod_ {j = r + 1} ^ {p-1} Z_j \right) \left (X_pX_r + Y_pY_r \right) \left (\bruchteil {1-Z_q} {2} \right) \\ \\ H_ {pqrs} &= \bruchteil {H_ {pqrs}} {8} \ prod_ {j = s + 1} ^ {r-1} Z_j \ prod_ {k = q + 1} ^ {p-1} Z_k \big (xxxx-XXYY + xyxy\nonneuber \\ \\ & \qquad\qquad\qquad\qquad\qquad + yxxy + YXYX-YYXX\nonumber \\ \\ & \qquad\qquad\qquad\qquad\qquad + xyyx + yyyy\big) \end{align}

Beim erzeugen solcher hamiltonane per Hand müssen diese Ersetzungs Regeln angewendet werden. Dies ist jedoch für große Moleküle, die aus Millionen von hamiltona-Begriffen bestehen können, nicht möglich.
Als Alternative können wir die `JordanWignerEncoding` angegebene `FermionHamiltonian` Darstellung der hamiltonan automatisch erstellen.

```csharp
    // We load the namespace containing fermion and Pauli objects. 
    using Microsoft.Quantum.Chemistry.Fermion;
    using Microsoft.Quantum.Chemistry.Pauli;
    
    // We create an example `FermionHamiltonian` instance.
    var fermionHamiltonian = new FermionHamiltonian();

    // We convert this Fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);
```

Nachdem die hamiltonane in dieser Form erstellt wurden, können wir einen Host von Quantum-Simulations Algorithmen verwenden, um die von $e ^ {-IHT} $ generierte Dynamics in eine Sequenz von elementaren Gates (innerhalb einiger benutzerdefinierbarer Fehlertoleranz) zu kompilieren.
In der algorithmischen Dokumentation werden die beiden am häufigsten verwendeten Methoden für die Quantum-Simulation, die qubisierung und Trotter – Suzuki-Formeln erläutert. Wir stellen Implementierungen für beide Methoden in der hamiltonan-Simulations Bibliothek bereit.
