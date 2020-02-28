---
title: Dirac-Notation
description: Erfahren Sie mehr über die Verwendung der Dirac-Notation zum Darstellen von Quantum-Zuständen und zum Simulieren von Quantum
author: QuantumWriter
uid: microsoft.quantum.concepts.dirac
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 204e56cc97fe28f9c52dcfb882aadec7e09bb2dc
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907561"
---
# <a name="dirac-notation"></a>Dirac-Notation

Obwohl die Spalten Vektor Notation in linearer Algebra allgegenwärtig ist, ist Sie in der Quantum-Berechnung häufig mühsam, besonders beim Umgang mit mehreren Qubits.  Wenn wir z. b. $ \psi $ als Vektor definieren, ist nicht explizit klar, ob $ \psi $ ein Zeilen-oder Spalten Vektor ist.  Wenn also "$ \phi $" und "$ \psi $" Vektoren sind, ist es gleichermaßen unklar, wenn "$ \phi \psi $" sogar definiert ist, weil die Formen von "$ \phi $" und "$ \psi $" im Kontext unklar sein können.  Abgesehen von der Mehrdeutigkeit der Formen von Vektoren kann das Ausdrücken von sogar einfachen Vektoren, die die zuvor eingeführte lineare algebraische Notation verwenden, sehr mühsam sein. Wenn Sie z. b. einen $n $-Qubit-Status beschreiben möchten, bei dem jedes Qubit den Wert $0 $ annimmt, wird der Zustand formal als 

$ $ \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \cdots \otimes\begin{bmatrix}1 \\\\ 0 \end{bmatrix}. $$  

Das Auswerten dieses tensorflow-Produkts ist natürlich nicht praktikabel, da der Vektor in einem exponentiell großen Raum liegt und diese Notation tatsächlich die beste Beschreibung des Zustands ist, der mithilfe der vorherigen Notation angegeben werden kann.  

Die [*Dirac-Notation*](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation) löst diese Probleme, indem Sie eine neue Sprache für die exakten Anforderungen von Quantum-Mechanismen darstellt.  Aus diesem Grund wird empfohlen, dass der Reader die Beispiele in diesem Abschnitt nicht als eine strikte Anleitung zum Beschreiben von quantumzuständen betrachtet, sondern den Reader ermutigt, diese als Vorschläge anzuzeigen, mit denen Quantum-Ideen kurz gesagt werden können.

Es gibt zwei Arten von Vektoren in der Dirac-Notation: den *Bra* -Vektor und den *Ket* -Vektor, die so benannt sind, dass Sie, wenn Sie vereint sind, eine *Klammer* oder ein inneres Produkt bilden.  Wenn $ \psi $ ein Spalten Vektor ist, können wir ihn in der Dirac-Notation als $ \ket{\psi} $ schreiben, wobei $ \ket{\cdot} $ angibt, dass es sich um einen Einheits Spalten Vektor handelt, d. h. einen *Ket* -Vektor.  Ebenso wird der Zeilen Vektor $ \psi ^ \dagger $ als $ \bra{\psi} $ ausgedrückt. Mit anderen Worten: $ \psi ^ \dagger $ wird durch Anwenden der Eintrags Weise komplexen Konjugation auf die Elemente des Erbens von $ \psi $ abgerufen. Die Bra-Ket-Notation impliziert direkt, dass $ \braket{\psi | \psi} $ das innere Produkt von Vector $ \psi $ mit sich selbst ist. Dies entspricht der Definition $1 $.  

Im Allgemeinen gilt: Wenn $ \psi $ und $ \phi $ die Quantum State Vektoren sind, ist Ihr internes Produkt $ \braket{\phi | \psi} $. Dies impliziert, dass die Wahrscheinlichkeit, dass der Status $ \ket{\psi} $ auf $ \ket{\phi} $ festgelegt wird, $ | \braket{\phi | \psi} |  

Die folgende Konvention wird verwendet, um die Quantum-Zustände zu beschreiben, die die Werte 0 (null) und eins (Single-Qubit-Berechnungsbasis Zustände) codieren:

$ $ \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} = \ket{0}, \qquad \begin{bmatrix} 0 \\\\ 1 \end{bmatrix} = \ket{1}.
$$

### <a name="example-representing-the-hadamard-operation-with-dirac-notation"></a>Beispiel: darstellen des Hadamard-Vorgangs mit Dirac-Notation

Die folgende Notation wird häufig verwendet, um die Zustände zu beschreiben, die sich aus der Anwendung des Hadamard-Gates auf $ \ket{0}$ und $ \ket{1}$ ergeben (die den Einheiten Vektoren in der $ + x $-und $-x $ Directions in der Bloch-Kugel entsprechen):

$ $ \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\\\ 1 \end{bmatrix} = h\ket{0} = \ket{+}, \qquad \frac{1}{\sqrt{2}} \begin{bmatrix} 1 \\\\-1 \end{bmatrix} = h\ket{1} = \ket{-}.
$$

Diese Zustände können auch mit der Dirac-Notation als Summe von $ \ket{0}$ und $ \ket{1}$ erweitert werden:

$ $ \ket{+} = \frac{1}{\sqrt{2}} (\ket{0} + \ket{1}), \qquad \ket{-} = \frac{1}{\sqrt{2}} (\ket{0}-\ket{1}).
$$

### <a name="computational-basis-vectors"></a>Berechnungsbasis Vektoren
Dadurch wird veranschaulicht, warum diese Zustände oft als *Berechnungsbasis*bezeichnet werden: jeder Quantenzustand kann immer als Summe von Berechnungs-Basis-Vektoren ausgedrückt werden, und diese Summen werden problemlos mithilfe der Dirac-Notation ausgedrückt.  Das Gegenteil gilt auch, wenn die Zustände $ \ket{+} $ und $ \ket{-}$ auch eine Grundlage für den Quantum-Status bilden.  Dies wird anhand der Tatsache angezeigt, dass

$ $ \ket{0} = \frac{1}{\sqrt{2}} (\ket{+} + \ket{-}), \qquad \ket{1} = \frac{1}{\sqrt{2}} (\ket{+}-\ket{-}).
$$

Sehen Sie sich als Beispiel für die Dirac-Notation die Braket $ \braket{0 | 1} $ an, bei der es sich um das innere Produkt zwischen $0 $ und $1 $ handelt.  Sie kann als 

$ $ \braket{0 | 1} = \begin{bmatrix} 1 & 0 \end{bmatrix}\begin{bmatrix}0\\\\ 1 \ Ende {bmatrix} = 0. $ $

Dies bedeutet, dass $ \ket{0}$ und $ \ket{1}$ orthogonale Vektoren sind, d. h. $ \braket{0 | 1} = \braket{1| 0} = $0.  Auch in der Definition $ \braket{0 | 0} = \braket{1| 1} = 1 $. Dies bedeutet, dass die beiden Berechnungsbasis Vektoren auch " *orthonormal*" genannt werden können.
Diese orthonormal-Eigenschaften sind im folgenden Beispiel nützlich. Wenn Sie den Status $ \ket{\psi} = {\frac{3}{5}} \ket{1} + {\frac{4}{5}} \ket{0}$ then haben, weil $ \braket{1 | 0} = $0 die Wahrscheinlichkeit der Messung von $1 $ beträgt  

$ $ \big | \braket{1 | \psi}\big | ^ 2 = \left | \frac{3}{5}\braket{1 | 1} + \frac{4}{5}\braket{1 | 0} \right | ^ 2 = \frac{9}{25}. $ $ 

### <a name="tensor-product-notation"></a>Tensor-Produkt Notation
Die Dirac-Notation umfasst auch eine implizite tensorflow-Produktstruktur darin.  Dies ist wichtig, da bei der Quantenberechnung der Zustands Vektor, der von zwei nicht korrelierten quantenregistern beschrieben wird, die tensorflow-Produkte der beiden Zustands Vektoren ist.  Wenn Sie eine Quantum-Berechnung erläutern möchten, ist es wichtig, die tensorflow-Produktstruktur zu beschreiben, oder Sie ist nicht so wichtig.  Die tensorflow-Produktstruktur impliziert, dass wir $ \psi \otimes \phi $ für alle zwei Quantum State Vektoren $ \phi $ und $ \psi $ als $ \ket{\psi} \ket{\phi} $ schreiben können. manchmal explizit als $ \ket{\psi} \otimes \ket{\phi} $ geschrieben, jedoch nach der Konvention, die $ \otimes $ schreibt zwischen den Vektoren ist nicht erforderlich.  Beispielsweise wird der Zustand, in dem zwei Qubits mit dem Zustand NULL initialisiert werden, von angegeben.

$ $ \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ 0 \end{bmatrix} = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} \otimes \begin{bmatrix} 1 \\\\ 0 \ End{bmatrix} = \ket{0} \otimes \ket{0}= \ket{0} \ket{0}.
$$

Entsprechend stellt der Status $ \ket{p} $ für Integer-$p $ einen Quantenzustand dar, der in der binären Darstellung der Ganzzahl $p $ codiert.  Wenn Sie z. b. die Zahl $5 $ mithilfe einer nicht signierten Binär Codierung ausdrücken möchten, können wir Sie gleichermaßen als

$ $ \ket{1}\ket{0}\ket{1} = \ket{101} = \ket{5}.
$$

Innerhalb dieser Notation muss $ \ket{0}$ nicht auf einen Single-Qubit-Zustand verweisen, sondern auf eine *Qubit-Registrierung* , die eine binäre Codierung von $0 $ speichert.  Die Unterschiede zwischen diesen beiden Notationen sind normalerweise aus dem Kontext eindeutig.  Diese Konvention ist nützlich, um das erste Beispiel zu vereinfachen, das auf eine der folgenden Arten geschrieben werden kann:

$ $ \begin{bmatrix}1 \\\\ 0 \end{bmatrix}\otimes \cdots \otimes\begin{bmatrix}1 \\\\ 0 \end{bmatrix} = \ket{0} \otimes \cdots \otimes \ket{0}= | 0 \ cdots 0 \ rangle = \ket{0}^ {\otimes n} = \ket{0}.
$$

### <a name="example-describing-superposition-with-dirac-notation"></a>Beispiel: Beschreiben der übergeordneten Position mit Dirac-Notation
Ein weiteres Beispiel für die Verwendung der Dirac-Notation zum Beschreiben eines Quantum-Zustands finden Sie in den folgenden Methoden zum Schreiben eines Quantum-Zustands, bei dem es sich um eine gleiche Superposition für jede mögliche Bitzeichenfolge der Länge handelt $n $

$ $ H ^ {\otimes n} \ket{0} = \frac{1}{2 ^ {n/2}} \ sum_ {j = 0} ^ {2 ^ n-1} \ket{j} = \ket{+} ^ {\otimes n}.
$$

Hier Fragen Sie sich vielleicht, warum die Summe von $0 $ auf $2 ^ {n}-$1 für $n $ Bits reicht.  Beachten Sie zunächst, dass es $2 ^ {n} $ verschiedene Konfigurationen gibt, die $n $ Bits annehmen kann.  Sie können dies sehen, indem Sie feststellen, dass ein Bit $2 $-Werte annehmen kann, zwei Bits jedoch $4 $-Werte und so weiter. Im Allgemeinen bedeutet dies, dass es $2 ^ n $ verschiedene mögliche Bitzeichenfolgen gibt, aber der größte Wert, der in einem von Ihnen codiert ist, $1 \ cdots 1 = 2 ^ n-$1 und somit die Obergrenze für die Summe.
In diesem Beispiel haben wir in diesem Beispiel nicht $ \ket{+} ^ {\otimes n} = \ket{+} $ in Analogie zu $ \ket{0}^ {\otimes n} = \ket{0}$ verwendet, da diese notalisierungskonvention in der Regel für den Berechnungs Status reserviert ist, wobei jedes Qubit auf NULL initialisiert wird.  Eine solche Konvention wäre in diesem Fall sinnvoll, aber Sie wird nicht in der Quantum Computing-Literatur eingesetzt.

### <a name="expressing-linearity-with-dirac-notation"></a>Ausdrücken von Linearität mit Dirac-Notation
Eine weitere nützliche Funktion der Dirac-Notation ist die Tatsache, dass Sie linear ist.  Wenn wir für vier Quantum State Vectors schreiben möchten, 

$ $ (\alpha \ket{\psi} + \beta\ket{\phi}) \otimes (\gamma \ket{\chi} + \delta \ket{\omega}) = \alpha\gamma \ket{\psi}\ket{\chi} + \alpha\delta \ket{\psi}\ket{\omega} + \beta\gamma\ket{\phi}\ket{\chi} + \beta\delta\ket{\phi}\ket{\omega}. $ $

Sie können z. b. die tensorflow-Produkt Notation in der Dirac-Notation verteilen, sodass tensorflow-Produkte zwischen Bundesstaaten Vektoren als normale Multiplikation betrachtet werden.

Bei Bra-Vektoren wird eine ähnliche Konvention wie bei Ket-Vektoren befolgt.  Beispielsweise entspricht der Vektor $ \bra{\psi}\bra{\phi} $ dem Zustands Vektor $ \psi ^ \dagger \otimes \phi ^ \dagger = (\psi\otimes \phi) ^ \dagger $. Wenn der Ket-Vektor $ \ket{\psi} $ den Wert $ \alpha \ket{0} + \beta \ket{1}$ hat, lautet die Bra Vector-Version des Vektors $ \bra{\psi} = \ket{\psi} ^ \dagger = (\bra{0}\alpha ^ * + \bra{1}\beta ^ *) $.

Stellen Sie sich beispielsweise vor, dass die Wahrscheinlichkeit berechnet werden soll, dass der Status $ \ket{\psi} = \frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}$ gemessen wird, wobei ein Quantum-Programm zum Messen der Zustände entweder $ \ket{+} $ oder $ \ket{-}$ verwendet werden soll. Die Wahrscheinlichkeit, dass das Gerät den Status "$ \ket{-}$" ausgibt, ist 

$ $ | \braket{-| \psi} | ^ 2 = \left | \frac{1}{\sqrt{2}} (\bra{0}-\bra{1}) (\frac{3}{5} \ket{1} + \frac{4}{5} \ket{0}) \right | ^ 2 = \left |-\frac{3}{5 \ sqrt{2}} + \frac{4}{5 \ sqrt{2}} \right | ^ 2 = \frac{1}{50}. $ $

Die Tatsache, dass das negative Vorzeichen in der Berechnung der Wahrscheinlichkeit angezeigt wird, ist eine Manifestation von Quantum-Störungen, bei der es sich um einen Mechanismus handelt, mit dem Quantum Computing gegenüber klassischem Computing Vorteile erzielt.

## <a name="ketbra-or-outer-product"></a>ketbra oder äußeres Produkt
Das abschließende Element, das in der Dirac-Notation diskutiert werden sollte, ist das *ketbra* -oder Outer-Produkt  Das äußere Produkt wird in Dirac-Notationen als $ \ket{\psi} \bra{\phi} $ dargestellt und manchmal als "ketbras" bezeichnet, da die BHS und die Ken in umgekehrter Reihenfolge als Klammer vorkommen.  Das äußere Produkt wird über die Matrix Multiplikation als $ \ket{\psi} \bra{\phi} = \psi \phi ^ \dagger $ für die Quantum State Vektoren $ \psi $ und $ \phi $ definiert.  Das einfachste und wohl häufigste Beispiel für diese Notation ist

$ $ \ket{0} \bra{0} = \begin{bmatrix}1\\\\ 0 \end{bmatrix}\begin{bmatrix}1 & 0 \end{bmatrix} = \begin{bmatrix}1 & 0\\\\ 0 & 0 \ Ende {bmatrix} \qquad \ket{1} \bra{1} = \begin{bmatrix}0\\\\ 1 \end{bmatrix}\begin{bmatrix}0 & 1 \end{bmatrix} = \begin{bmatrix}0 & 0\\\\ 0 & 1 \ Ende {bmatrix}.
$$

Ketbras werden oft als Projektoren bezeichnet, da Sie einen Quantum-Zustand auf einen festgelegten Wert projizieren.  Da diese Vorgänge nicht einheitlich sind (und nicht einmal die Norm eines Vektors behalten), sollte ein Quantum-Computer nicht deterministisch einen Projektor anwenden.  Projektoren führen jedoch eine schöne Aufgabe aus, die Aktion zu beschreiben, die die Messung in einem Quantum-Status aufweist.  Wenn wir z. b. den Status $ \ket{\psi} $ auf $0 $ Messen, ist die resultierende Transformation, die der Zustand als Ergebnis der Messung hat,

  $ $ \ket{\psi} \rightarrow \bruch{(\ket{0} \bra{0}) \ket{\psi}}{| \braket{0 | \psi} |} = \ket{0}, $ $

Es wird davon ausgegangen, dass Sie den Status Messen und als $ \ket{0}$ feststellen.  Zur Wiederholung können solche Projektoren nicht deterministisch auf einen Zustand in einem Quantum-Computer angewendet werden.  Stattdessen können Sie am besten nach dem Zufallsprinzip mit dem Ergebnis $ \ket{0}$, das mit einer festgelegten Wahrscheinlichkeit angezeigt wird, angewendet werden.  Die Wahrscheinlichkeit, dass eine solche Messung erfolgreich ist, kann als Erwartungswert des Quantum-Projektors im Zustand geschrieben werden.

$ $ \bra{\psi} (\ket{0} \bra{0}) \ket{\psi} = | \braket{\psi | 0} | ^ 2, $ $

Dies veranschaulicht, dass Projektoren einfach eine neue Methode zum Ausdrücken des Messprozesses bietet.

Wenn Sie stattdessen das erste Qubit eines multiqubit-Zustands als $1 $ Messen, können wir diesen Prozess auch bequem mithilfe von Projektoren und Dirac-Notation beschreiben:

$ $ P (\text{First Qubit = 1}) = \bra{\psi}\left (\ket{1}\bra{1}\otimes \boldone ^ {\otimes n-1} \right) \ket{\psi}.
$$

Hier kann die Identitätsmatrix bequem in der Dirac-Notation geschrieben werden.

$ $ \boldone = \ket{0} \bra{0}+ \ket{1} \bra{1}= \begin{bmatrix}1 & 0\\\\ 0 & 1 \end{bmatrix}.
$$

Für den Fall, dass zwei-Qubits vorhanden sind, kann der Projektor erweitert werden. 

$ $ \ket{1} \bra{1} \otimes \id = \ket{1}\bra{1} \otimes (\ket{0} \bra{0}+ \ket{1} \bra{1}) = \ket{10}\bra{10} + \ket{11}\bra{11}.
$$

Wir können dann sehen, dass dies mit der Erörterung von Mess Wahrscheinlichkeiten für multiqubit-Zustände mit Spalten Vektor Notation konsistent ist:

$ $ P (\text{First Qubit = 1}) = \psi ^ \dagger (e\_{10}e\_{10}^ \dagger + e\_{11}e\_{11}^ \dagger) \psi = | e\_{10}^ \dagger \psi | ^ 2 + | e\_{11}^ \dagger \psi | ^ 2, $ $

, der mit der Multi-Qubit-Mess Diskussion übereinstimmt.  Die Verallgemeinerung dieses Ergebnisses in den multiqubit-Fall ist jedoch etwas einfacher, wenn Sie die Dirac-Notation als Column-Vector-Notation verwenden, und ist vollständig Äquivalent zur vorherigen Behandlung.

## <a name="density-operators"></a>Density-Operatoren

Ein weiterer nützlicher Operator zum Ausdrücken mithilfe der Dirac-Notation ist ein *Dichte Operator*, der manchmal auch als *Zustands Operator*bezeichnet wird.
Ein Density-Operator für einen Quantum-Status Vektor hat das Format $ \rho = \ket{\psi} \bra{\psi} $.
Dieses Konzept, das den Zustand als Matrix anstelle eines Vektors darstellt, ist häufig nützlich, da es eine bequeme Möglichkeit darstellt, Wahrscheinlichkeitsberechnungen darzustellen, und eine Möglichkeit bietet, sowohl statistische Unsicherheiten als auch Quantum-Ungewissheit zu beschreiben. innerhalb desselben Formalismus.
Allgemeine Quantum-Zustands Operatoren sind in einigen Bereichen des Quantums, aber nicht notwendig, um die Grundlagen des Felds zu verstehen.
Für den interessierten Reader empfiehlt es sich, eines der in bereitgestellten Referenzbücher [zu lesen, um weitere Informationen](xref:microsoft.quantum.more-information)zu erhalten.

## <a name="q-gate-sequences-equivalent-to-quantum-states"></a>Q # Gate-Sequenzen, die den Quantum-Zuständen entsprechen
Ein letzter Punkt, der sich auf die Quantum-Notation und die f #-Programmiersprache aufhebt: zu Beginn dieses Dokuments haben wir erwähnt, dass der Quantum-Status das grundlegende Objekt der Informationen in Quantum Computing ist.  Es kann dann eine Überraschung sein, dass es in f # keine Vorstellung von einem Quantum-Zustand gibt.  Stattdessen werden alle Zustände nur durch die Vorgänge beschrieben, die zur Vorbereitung verwendet werden.  Das vorherige Beispiel ist eine hervorragende Abbildung.  Anstatt eine einheitliche Superposition für jede Quantum-Bitzeichenfolge in einem Register auszudrücken, können wir das Ergebnis als $H ^ {\otimes n} \ket{0}$ darstellen.  Diese exponentiell kürzere Beschreibung des Zustands hat nicht nur den Vorteil, dass wir uns klassisch darauf auswirken können, sondern auch die Vorgänge definieren, die durch den Software Stapel zur Implementierung des Algorithmus weitergegeben werden müssen.  Aus diesem Grund ist Q # für das Ausgeben von Gate-Sequenzen anstelle von Quantum-Zuständen konzipiert. auf der theoretischen Ebene sind jedoch die beiden Perspektiven gleichwertig.
