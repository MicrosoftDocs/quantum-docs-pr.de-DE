---
title: Intrinsische Vorgänge und Funktionen im QDK
description: Erfahren Sie mehr über die intrinsischen Vorgänge und Funktionen im QDK, einschließlich klassischer Funktionen und einheitlicher, Rotations-und maßoperationen.
author: QuantumWriter
uid: microsoft.quantum.libraries.standard.prelude
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: b1c26c632f36b6c254d940a89b13638f7592ab80
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907204"
---
# <a name="the-prelude"></a>Der Auftakt #

Der Q#-Compiler und die im Quantum Development Kit enthaltenen Zielcomputer stellen eine Reihe von intrinsischen Funktionen und Vorgängen bereit, die beim Schreiben von Quantum-Programmen in Q# verwendet werden können.

## <a name="intrinsic-operations-and-functions"></a>Intrinsische Vorgänge und Funktionen ##

Die in der Standardbibliothek definierten systeminternen Vorgänge sind in einer von mehreren Kategorien unterteilt:

- Wichtige klassische Funktionen, die im <xref:microsoft.quantum.core>-Namespace gesammelt werden.
- Vorgänge, die die von [Clifford und $T $ Gates erstellten unitoren](xref:microsoft.quantum.concepts.qubit)darstellen.
- Vorgänge, die Drehungen zu verschiedenen Operatoren darstellen.
- Vorgänge zum Implementieren von Messungen.

Da der Clifford + $T $ Gate-Satz für das Quantum Computing [universell](xref:microsoft.quantum.concepts.multiple-qubits) ist, reichen diese Vorgänge aus, um einen beliebigen Quantum-Algorithmus innerhalb eines negisch kleinen Fehlers zu implementieren.
Durch die Bereitstellung von Rotationen ermöglicht Q# dem Programmierer, in der einzelnen Qubit-Bibliothek mit einheitlicher und CNOT Gate zu arbeiten. Diese Bibliothek ist viel leichter zu überprüfen, da der Programmierer keinen direkten Ausdruck der Clifford + $T $-Zerlegung erfordert, und da für die Kompilierung einzelner Qubit-unitoren in Clifford und $T $ Gates sehr effiziente Methoden vorhanden sind (Weitere Informationen finden Sie [hier](xref:microsoft.quantum.more-information) ).

Wenn möglich ermöglichen die in der Einleitung definierten Vorgänge, die auf Qubits reagieren, das Anwenden des `Controlled` Variant, sodass der Zielcomputer die geeignete Zerlegung ausführt.

Viele der in diesem Teil der Einleitung definierten Funktionen und Vorgänge befinden sich im @"microsoft.quantum.intrinsic"-Namespace, sodass die meisten Q#-Quelldateien über eine `open Microsoft.Quantum.Intrinsic;` Direktive verfügen, die direkt auf die anfängliche Namespace Deklaration folgt.
Der <xref:microsoft.quantum.core>-Namespace wird automatisch geöffnet, sodass Funktionen wie <xref:microsoft.quantum.core.length> ohne eine `open`-Anweisung verwendet werden können.

### <a name="common-single-qubit-unitary-operations"></a>Allgemeine Single-Qubit-einheitliche Vorgänge ###

Der-Auftakt definiert außerdem viele gängige [Single-Qubit-Vorgänge](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).
Alle diese Vorgänge ermöglichen sowohl das `Controlled`-als auch das `Adjoint`-funktors.

#### <a name="pauli-operators"></a>Pauli-Operatoren ####

Der <xref:microsoft.quantum.intrinsic.x> Vorgang implementiert den "Pauli $X $"-Operator.
Dies wird manchmal auch als `NOT` Gate bezeichnet.
Sie verfügt über eine Signatur `(Qubit => Unit is Adj + Ctl)`.
Dies entspricht der einheitlichen Single-Qubit-Version:

\begin{Equation} \begin{bmatrix} 0 & 1 \\\\% FIXME: aktuell wird der quadwhack-Hack verwendet.
1 & 0 \ End{bmatrix} \end{Equation}

Der <xref:microsoft.quantum.intrinsic.y> Vorgang implementiert den "Pauli $Y $"-Operator.
Sie verfügt über eine Signatur `(Qubit => Unit is Adj + Ctl)`.
Dies entspricht der einheitlichen Single-Qubit-Version:

\begin{Equation} \begin{bmatrix} 0 &-i \\\\% FIXME: aktuell wird der quadwhack-Hack verwendet.
i & 0 \ End{bmatrix} \end{Equation}

Der <xref:microsoft.quantum.intrinsic.z> Vorgang implementiert den "Pauli $Z $"-Operator.
Sie verfügt über eine Signatur `(Qubit => Unit is Adj + Ctl)`.
Dies entspricht der einheitlichen Single-Qubit-Version:

\begin{Equation} \begin{bmatrix} 1 & 0 \\\\% FIXME: aktuell wird der quadwhack-Hack verwendet.
0 &-1 \end{bmatrix} \end{Equation}

Unten sehen Sie, dass diese Transformationen der [Bloch-Kugel](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) zugeordnet sind (die Drehungs Achse in jedem Fall wird rot hervorgehoben):

![Auf der Bloch-Kugel zugeordnete Pauli-Vorgänge](~/media/prelude_pauliBloch.png)

Es ist wichtig zu beachten, dass durch das doppelte Anwenden desselben Pauli-Tors auf das gleiche Qubit der Vorgang abgebrochen wird (da Sie nun eine vollständige Rotation von 2 (360 °) über der Oberfläche bis zur Bloch-Kugel durchgeführt haben und somit am Ausgangspunkt zurückkehren. Dies bringt uns zur folgenden Identität:

$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \boldone $ $

Dies kann auf der Bloch-Kugel visualisiert werden:

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a>Andere einzelqubit Clif-Fords ####

Der <xref:microsoft.quantum.intrinsic.h> Vorgang implementiert das Hadamard-Gate.
Dadurch wird die Pauli-$X $ und $Z $-Achse des Ziel-Qubit geändert, sodass $H \ket{0} = \ket{+} \mathrel{: =} (\ket{0} + \ket{1})/\sqrt{2}$ und $H \ket{+} = \ket{0}$.
Sie verfügt über eine Signatur `(Qubit => Unit is Adj + Ctl)`und entspricht der einheitlichen Single-Qubit:

\begin{Equation} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\% FIXME: aktuell wird der quadwhack-Hack verwendet.
1 &-1 \end{bmatrix} \end{Equation}

Das Hadamard-Gate ist besonders wichtig, da es verwendet werden kann, um eine übergeordnete Position von $ \ket{0}$ und $ \ket{1}$ States zu erstellen. In der Bloch Sphere-Darstellung ist es am einfachsten, dies als Drehung von $ \ket{\psi} $ um die x-Achse um $ \pi $ radiane ($ 180 ^ \circ $), gefolgt von einer (im Uhrzeigersinn) Drehung um die y-Achse durch $ \ Pi/2 $ radiane ($ 90 ^ \circ $)

![Hadamard-Vorgang auf der Bloch-Kugel zugeordnet](~/media/prelude_hadamardBloch.png)

Der <xref:microsoft.quantum.intrinsic.s> Vorgang implementiert das-Phasen Gate $S $.
Dies ist die Quadratwurzel der Matrix des Pauli-$Z $-Vorgangs.
Das heißt, $S ^ 2 = Z $.
Sie verfügt über eine Signatur `(Qubit => Unit is Adj + Ctl)`und entspricht der einheitlichen Single-Qubit:

\begin{Equation} \begin{bmatrix} 1 & 0 \\\\% FIXME: aktuell wird der quadwhack-Hack verwendet.
0 & i \end{bmatrix} \end{Equation}

#### <a name="rotations"></a>Drehungen ####

Zusätzlich zu den oben beschriebenen Pauli-und Clifford-Vorgängen bietet Q# Prelude eine Vielzahl von Möglichkeiten, um Drehungen auszudrücken.
Wie in [Single-Qubit-Vorgängen](xref:microsoft.quantum.concepts.qubit#single-qubit-operations)beschrieben, ist die Möglichkeit der Rotation für Quantum-Algorithmen von entscheidender Bedeutung.

Wir gehen zunächst von der Erinnerung aus, dass wir jeden einzelnen Qubit-Vorgang mithilfe der $H $ und $T $ Gates Ausdrücken können. dabei ist $H $ der Hadamard-Vorgang und WHERE \begin{Equation} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\\\% FIXME: Dies verwendet derzeit den Quad Back zerstören
0 & e ^ {i \pi/4} \end{bmatrix} \end{Equation} Dies ist die Quadratwurzel des <xref:microsoft.quantum.intrinsic.s> Vorgangs, d. h. $T ^ 2 = S $.
Die $T $ Gate wird wiederum vom <xref:microsoft.quantum.intrinsic.t>-Vorgang implementiert und verfügt über eine Signatur `(Qubit => Unit is Adj + Ctl)`, die angibt, dass es sich um einen einheitlichen Vorgang auf einem Single-Qubit handelt.

Obwohl dies im Prinzip ausreichend ist, um einen beliebigen Single-Qubit-Vorgang zu beschreiben, haben unterschiedliche Zielcomputer möglicherweise effizientere Darstellungen für Rotationen von Pauli-Operatoren, sodass die Zusammenführung eine Vielzahl von Methoden für die Arbeit enthält. Diese Rotationen werden ausgedrückt.
Die grundlegendste davon ist der <xref:microsoft.quantum.intrinsic.r> Vorgang, der eine Drehung um eine angegebene Pauli-Achse implementiert. \begin{Equation} R (\sigma, \phi) \mathrel{: =} \exp (-i \phi \sigma/2), \end{Equation}, wobei $ \sigma $ ein Pauli-Operator ist, $ \phi $ ein Winkel ist und $ \exp $ den exponentiellen Wert der Matrix darstellt.
Es verfügt über eine Signatur `((Pauli, Double, Qubit) => Unit is Adj + Ctl)`, wobei die ersten beiden Teile der Eingabe die klassischen Argumente $ \sigma $ und $ \phi $ darstellen, um den einheitlichen Operator $R (\sigma, \phi) $ anzugeben.
Wir können $ \sigma $ und $ \phi $ teilweise anwenden, um einen Vorgang zu erhalten, dessen Typ mit einer Single-Qubit-einheitlich ist.
`R(PauliZ, PI() / 4, _)` hat z. b. den Typ `(Qubit => Unit is Adj + Ctl)`.

> [!NOTE]
> Der <xref:microsoft.quantum.intrinsic.r>-Vorgang dividiert den Eingabe Winkel um 2 und multipliziert ihn mit-1.
> Bei $Z $-Drehungen bedeutet dies, dass der $ \ket-{0}$ eigen State um $-\phi/$2 gedreht wird und der $ \ket-{1}$ eigen State durch $ \phi/$2 gedreht wird, sodass der $ \ket{1}$ eigen State um $ \phi $ in Relation zum $ \ket{0}$ eigen State gedreht wird.
>
> Dies bedeutet insbesondere, dass sich `T` und `R(PauliZ, PI() / 8, _)` nur durch eine irrelevante [globale Phase](xref:microsoft.quantum.glossary#global-phase)unterscheiden.
> Aus diesem Grund wird $T $ manchmal als $ \bruchteil {\pi}{8}$-Gate bezeichnet.
>
> Beachten Sie auch, dass beim Drehen um `PauliI` einfach eine globale Phase von $ \phi/$2 angewendet wird. Obwohl solche Phasen irrelevant sind, wie in [den konzeptionellen Dokumenten](xref:microsoft.quantum.concepts.qubit)argumentiert, sind Sie für gesteuerte `PauliI` Drehungen relevant.

Innerhalb von Quantum-Algorithmen ist es häufig hilfreich, Rotationen als dyadic-Bruchteile auszudrücken, z. b. $ \phi = \pi k/2 ^ n $ für einige $k \in \mathbb{z} $ und $n \in \mathbb{n} $.
Der <xref:microsoft.quantum.intrinsic.rfrac> Vorgang implementiert eine Drehung um eine angegebene Pauli-Achse, die diese Konvention verwendet.
Dies unterscheidet sich von der <xref:microsoft.quantum.intrinsic.r>, dass der Drehungs Winkel als zwei Eingaben vom Typ "`Int`" angegeben wird, die als dyadic-Bruchteil interpretiert werden.
Daher `RFrac` eine Signatur `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)`.
Es implementiert die einheitliche Single-Qubit-$ \exp (i \pi k \sigma/2 ^ n) $, wobei $ \sigma $ die für das erste Argument entsprechende Pauli-Matrix ist, $k $ das zweite Argument und $n $ das dritte Argument ist.
`RFrac(_,k,n,_)` ist mit `R(_,-πk/2^n,_)`identisch. Beachten Sie, dass der Winkel der *negative* Anteil des Bruchteils ist.

Der <xref:microsoft.quantum.intrinsic.rx> Vorgang implementiert eine Drehung um die Pauli $X $-Achse.
Sie verfügt über eine Signatur `((Double, Qubit) => Unit is Adj + Ctl)`.
`Rx(_, _)` ist identisch mit `R(PauliX, _, _)`.

Der <xref:microsoft.quantum.intrinsic.ry> Vorgang implementiert eine Drehung um die Pauli $Y $-Achse.
Sie verfügt über eine Signatur `((Double, Qubit) => Unit is Adj + Ctl)`.
`Ry(_, _)` ist identisch mit `R(PauliY,_ , _)`.

Der <xref:microsoft.quantum.intrinsic.rz> Vorgang implementiert eine Drehung um die Pauli $Z $-Achse.
Sie verfügt über eine Signatur `((Double, Qubit) => Unit is Adj + Ctl)`.
`Rz(_, _)` ist identisch mit `R(PauliZ, _, _)`.

Der <xref:microsoft.quantum.intrinsic.r1> Vorgang implementiert eine Drehung um den angegebenen Betrag um $ \ket{1}$, den $-$1-eigen Status von $Z $.
Sie verfügt über eine Signatur `((Double, Qubit) => Unit is Adj + Ctl)`.
`R1(phi,_)` ist identisch mit `R(PauliZ,phi,_)` gefolgt von `R(PauliI,-phi,_)`.

Der <xref:microsoft.quantum.intrinsic.r1frac>-Vorgang implementiert eine Bruch Bruch Drehung um den angegebenen Betrag um den Z = 1-eigen Zustand.
Sie verfügt über eine Signatur `((Int,Int, Qubit) => Unit is Adj + Ctl)`.
`R1Frac(k,n,_)` ist identisch mit `RFrac(PauliZ,-k.n+1,_)` gefolgt von `RFrac(PauliI,k,n+1,_)`.

Im folgenden wird ein Beispiel für einen Rotations Vorgang (um die in der Bloch-Kugel zugeordnete Pauli-$Z $-Achse) dargestellt:

![Drehvorgang auf der Bloch-Kugel zugeordnet](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a>Multiqubit-Vorgänge ####

Zusätzlich zu den oben beschriebenen Single-Qubit-Vorgängen definiert der-Auftakt auch mehrere multiqubit-Vorgänge.

Zuerst führt der <xref:microsoft.quantum.intrinsic.cnot> Vorgang ein Standardmäßiges kontrolliertes`NOT` Gate aus, \begin{Equation} \operatschmue{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}.
\end{Equation} es weist eine Signatur `((Qubit, Qubit) => Unit is Adj + Ctl)`auf, die angibt, dass $ \operatorname{CNOT} $ auf zwei einzelnen Qubits einheitlich agiert.
`CNOT(q1, q2)` ist identisch mit `(Controlled X)([q1], q2)`.
Da das `Controlled`-Funktor das Steuern von für ein Register ermöglicht, verwenden wir das Array Literale `[q1]`, um anzugeben, dass nur das einzige Steuerelement verwendet werden soll.

Der <xref:microsoft.quantum.intrinsic.ccnot> Vorgang führt ein doppelt kontrolliertes not-Gate durch, das manchmal auch als "tffoli Gate" bezeichnet wird.
Sie verfügt über eine Signatur `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)`.
`CCNOT(q1, q2, q3)` ist identisch mit `(Controlled X)([q1, q2], q3)`.

Der <xref:microsoft.quantum.intrinsic.swap> Vorgang tauscht die Quantum-Zustände von zwei Qubits aus.
Das heißt, es implementiert die einheitliche Matrix \begin{Equation} \operatorname{tauap} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}.
\end{Equation} verfügt über eine Signatur `((Qubit, Qubit) => Unit is Adj + Ctl)`.
`SWAP(q1,q2)` entspricht `CNOT(q1, q2)`, gefolgt von `CNOT(q2, q1)` und dann `CNOT(q1, q2)`.

> [!NOTE]
> Das austauschgate ist *nicht* identisch mit dem Neuanordnen der Elemente einer Variablen mit dem Typ `Qubit[]`.
> Das Anwenden von `SWAP(q1, q2)` bewirkt eine Änderung des Status der Qubits, auf die von `q1` und `q2`verwiesen wird. `let swappedRegister = [q2, q1];` wirkt sich nur darauf aus, wie auf diese Qubits verwiesen wird.
> Darüber hinaus ermöglicht `(Controlled SWAP)([q0], (q1, q2))`, dass `SWAP` auf den Zustand eines dritten Qubit, das nicht durch Neuanordnen von Elementen dargestellt werden kann, bedingt ist.
> Das Tor des kontrollierten Austauschs, das auch als "Fredkin Gate" bezeichnet wird, ist leistungsfähig genug, um die gesamte klassische Berechnung einzubeziehen.

Schließlich bietet das präspiel zwei Vorgänge zum Darstellen von exponentialen von multiqubit-Pauli-Operatoren.
Der <xref:microsoft.quantum.intrinsic.exp> Vorgang führt eine Drehung auf Grundlage eines tensorflow-Produkts von Pauli-Matrizen durch, wie durch das Multi-Qubit-einheitliches \begin{Equation} \operatorname{Exp} (\vec{\sigma}) dargestellt. \phi) \mathrel{: =} \exp\left (i \phi \ sigma_0 \otimes \ sigma_1 \otimes \cdots \otimes \ sigma_n \right), \end{Equation} WHERE $ \vec{\sigma} = (\ sigma_0, \ sigma_1, \dots, \ sigma_n) $ ist eine Sequenz von Single-Qubit-Pauli-Operatoren, wobei $ \phi $ ein Winkel ist.
Die `Exp` Drehung stellt "$ \vec{\sigma} $" als Array von `Pauli` Elementen dar, sodass Sie über eine Signatur `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)`verfügt.

Der <xref:microsoft.quantum.intrinsic.expfrac> Vorgang führt dieselbe Drehung aus, wobei die oben beschriebene dyadic-Bruch Notation verwendet wird.
Sie verfügt über eine Signatur `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)`.

> [!WARNING]
> Exponentiale des tensorflow-Produkts von Pauli-Operatoren sind nicht mit tensorflow-Produkten der exponentiale von Pauli-Operatoren identisch.
> Das heißt, $e ^ {i (z \otimes Z) \phi} \nE e ^ {i z \phi} \otimes e ^ {i z \phi} $.

### <a name="measurements"></a>Messungen ###

Beim Messen entspricht der + 1-eigen Wert des gemessenen Operators einem `Zero` Ergebnis und dem Eigen Wert-1 für ein `One` Ergebnis.

> [!NOTE]
> Diese Konvention mag merkwürdig erscheinen, hat jedoch zwei sehr gute Vorteile.
> Zuerst wird das Ergebnis "$ \ket{0}$" durch den `Result` Wert `Zero`dargestellt, während "$ \ket{1}$" `One`entspricht.
> Zweitens können wir heraus schreiben, dass der Eigen Wert $ \lambda $, der einem Ergebnis $r $ entspricht, $ \lambda = (-1) ^ r $ entspricht.

Messvorgänge unterstützen weder den `Adjoint` noch den `Controlled`-Funktor.

Der <xref:microsoft.quantum.intrinsic.measure> Vorgang führt eine gemeinsame Messung von einem oder mehreren Qubits im angegebenen Produkt von Pauli-Operatoren aus.
Wenn die Länge des Pauli-Arrays und des Qubit-Arrays unterschiedlich ist, schlägt der Vorgang fehl.
`Measure` verfügt über eine Signatur `((Pauli[], Qubit[]) => Result)`.

Beachten Sie, dass eine gemeinsame Messung nicht mit der Messung der einzelnen Qubits identisch ist.
Sehen Sie sich beispielsweise den Status $ \ket{11} = \ket{1} \otimes \ket{1} = x\otimes X \ket{00}$ an.
Wenn Sie $Z _0 $ und $Z _1 $ einzeln Messen, erhalten wir die Ergebnisse $r _0 = $1 und $r _1 = $1.
Wenn Sie $Z _0 Z_1 $ Messen, erhalten wir jedoch das einzige Ergebnis $r _ {\textrm{Joint}} = $0, das angibt, dass die Größe von $ \ket{11}$ positiv ist.
Unterschiedlich platzieren, $ (-1) ^ {r_0 + r_1} = (-1) ^ R_ {\textrm{Joint}}) $.
Da wir *nur* die Parität dieser Messung erlernen, werden alle Quantum-Informationen, die in der übergeordneten Position zwischen den 2 2-Qubit-Zuständen der positiven Parität ($ \ket{00}$ und $ \ket{11}$) dargestellt werden, beibehalten.
Diese Eigenschaft ist später erforderlich, da wir die Fehlerkorrektur erörtern.

Der Vorteil ist, dass die Einleitung auch zwei weitere Vorgänge zum Messen von Qubits bereitstellt.
Da das Ausführen von Single-Qubit-Messungen recht häufig ist, definiert das präspiel eine kurzzahl für diesen Fall.
Der <xref:microsoft.quantum.intrinsic.m>-Vorgang misst den Pauli-$Z $-Operator auf einem einzelnen Qubit und verfügt über eine Signatur `(Qubit => Result)`.
`M(q)` entspricht `Measure([PauliZ], [q])`.

Der <xref:microsoft.quantum.measurement.multim> misst den Pauli $Z $-Operator *separat* für jedes Array von Qubits und gibt das *Array* von `Result` Werten zurück, die für jedes Qubit abgerufen werden.
In einigen Fällen kann dies optimiert werden. Sie verfügt über eine Signatur (`Qubit[] => Result[])`.
`MultiM(qs)` ist äquivalent zu:

```qsharp
mutable rs = new Result[Length(qs)];
for (index in 0..Length(qs)-1)
{
    set rs[index] = M(qs[index]);
}
return rs;
```

## <a name="extension-functions-and-operations"></a>Erweiterungsfunktionen und-Vorgänge ##

Außerdem definiert der-Auftakt einen umfangreichen Satz mathematischer und Typkonvertierungs Funktionen auf der .NET-Ebene für die Verwendung in Q#-Code.
Der <xref:microsoft.quantum.extensions.math>-Namespace definiert z. b. nützliche Vorgänge, z. b. <xref:microsoft.quantum.extensions.math.sin> und <xref:microsoft.quantum.extensions.math.log>.
Die vom Quantum Development Kit bereitgestellte Implementierung verwendet die klassische .net-Basisklassen Bibliothek und kann daher einen zusätzlichen kommunikationsroundtrip zwischen Quantum-Programmen und ihren klassischen Treibern beinhalten.
Dies stellt zwar kein Problem für einen lokalen Simulator dar, dies kann jedoch bei der Verwendung eines Remote Simulators oder der tatsächlichen Hardware als Zielcomputer ein Leistungsproblem darstellen.
Dies bedeutet, dass ein einzelner Zielcomputer diese Auswirkungen auf die Leistung verringern kann, indem er diese Vorgänge mit Versionen außer Kraft setzt, die für das jeweilige System effizienter sind.

### <a name="math"></a>Mathematisch ###

Der <xref:microsoft.quantum.extensions.math>-Namespace stellt viele nützliche Funktionen aus der [`System.Math` Klasse](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1)der .net-Basisklassen Bibliothek bereit.
Diese Funktionen können auf die gleiche Weise wie alle anderen Q#-Funktionen verwendet werden:

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

Wenn eine statische .NET-Methode basierend auf dem Typ ihrer Argumente überladen wurde, wird die entsprechende Q#-Funktion mit einem Suffix kommentiert, das den Typ der Eingabe angibt:

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a>Bitweise Vorgänge ###

Schließlich stellt der <xref:microsoft.quantum.extensions.bitwise>-Namespace mehrere nützliche Funktionen zum Bearbeiten ganzer Zahlen durch bitweise Operatoren bereit.
Beispielsweise gibt <xref:microsoft.quantum.extensions.bitwise.parity> die bitweise Parität einer Ganzzahl als eine andere Ganzzahl zurück.
