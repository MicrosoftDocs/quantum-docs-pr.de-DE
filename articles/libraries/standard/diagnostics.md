---
title: 'Diagnose in den Q # Standard-Bibliotheken'
description: 'Erfahren Sie mehr über die Diagnosefunktionen und-Vorgänge in den Q # Standard-Bibliotheken, die zum Abfangen von Fehlern oder Fehlern in quantenprogrammen verwendet werden'
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: ba2f248327bb3db4ee895f8e65ea31c17e42b5f4
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906235"
---
# <a name="diagnostics"></a>Diagnose #

Wie bei der klassischen Entwicklung ist es wichtig, dass Sie Fehler und Fehler in quantumprogrammen diagnostizieren können.
Die Q #-Standardbibliotheken bieten eine Vielzahl verschiedener Möglichkeiten, um die Richtigkeit von quantenprogrammen sicherzustellen, wie in <xref:microsoft.quantum.techniques.testing-and-debugging>ausführlich beschrieben.
Diese Unterstützung wird größtenteils in Form von Funktionen und Vorgängen bereitgestellt, die entweder den Zielcomputer anweisen, zusätzliche Diagnoseinformationen für das Host Programm oder den Entwickler bereitzustellen, oder die Richtigkeit von Bedingungen und invarianten erzwingen, ausgedrückt durch den Funktions-oder Vorgangs aufzurufenden.

## <a name="machine-diagnostics"></a>Computer Diagnose ##

Die Diagnose von klassischen Werten kann mithilfe der <xref:microsoft.quantum.intrinsic.message>-Funktion abgerufen werden, um eine Nachricht auf Computer abhängige Weise zu protokollieren.
Standardmäßig wird die Zeichenfolge in die Konsole geschrieben.
Wird in Verbindung mit interintermierten Zeichen folgen verwendet, <xref:microsoft.quantum.intrinsic.message> das Melden von Diagnoseinformationen über klassische Werte erleichtert:

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> `Message` verfügt über eine Signatur `(String -> Unit)`, die wiederum darstellt, dass das Ausgeben einer Debug-Protokollmeldung nicht innerhalb von Q # beobachtet werden kann.

Die <xref:microsoft.quantum.diagnostics.dumpmachine>-und <xref:microsoft.quantum.diagnostics.dumpregister> callables weisen Zielcomputer an, Diagnoseinformationen zu allen derzeit zugeordneten Qubits bzw. zu einem bestimmten Register von Qubits bereitzustellen.
Jeder Zielcomputer variiert in Abhängigkeit von den Diagnoseinformationen, die als Reaktion auf eine dumpanweisung bereitgestellt werden.
Der Zielcomputer des [vollständigen Zustands Simulators](xref:microsoft.quantum.machines.full-state-simulator) stellt beispielsweise dem Host Programm den Zustands Vektor bereit, den er intern zur Darstellung eines Register von Qubits verwendet.
Im Vergleich dazu stellt der Zielcomputer des Dienst Bereitstellungs- [Simulators](xref:microsoft.quantum.machines.toffoli-simulator) für jedes Qubit ein einzelnes klassisches Bit bereit.

 Weitere Informationen zur `DumpMachine` Ausgabe des [vollständigen Zustands Simulators](xref:microsoft.quantum.machines.full-state-simulator) finden Sie im Abschnitt zu den Dumpfunktionen in unserem [Artikel zum Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions).


## <a name="facts-and-assertions"></a>Fakten und Assertionen ##

Wie unter [Testen und Debuggen](xref:microsoft.quantum.techniques.testing-and-debugging)erläutert, kann eine Funktion oder ein Vorgang mit Signatur `Unit -> Unit` oder `Unit => Unit`als Komponenten *Test*gekennzeichnet werden.
Jeder Komponenten Test besteht in der Regel aus einem kleinen Quantum-Programm zusammen mit einer oder mehreren Bedingungen, die die Richtigkeit des Programms überprüfen.
Diese Bedingungen können in Form von _Fakten_ _auftreten, die_die Werte Ihrer Eingaben überprüfen, oder Assertionen, die die Zustände von einem oder mehreren als Eingabe übergebenen Qubits überprüfen.

`EqualityFactI(1 + 1, 2, "1 + 1 != 2")` stellt z. b. die mathematische Tatsache dar, dass $1 + 1 = $2, während `AssertQubit(One, qubit)` die Bedingung darstellt, die das Messen `qubit` eine `One` mit Sicherheit zurückgibt.
Im ersten Fall können wir die Richtigkeit der Bedingung nur anhand ihrer Werte überprüfen, während wir im letzteren Fall etwas über den Zustand des Qubit wissen müssen, um die Aussage auszuwerten.

Die Q # Standard-Bibliotheken bieten verschiedene Funktionen für die Darstellung von Fakten, einschließlich:

- <xref:microsoft.quantum.diagnostics.fact>
- <xref:microsoft.quantum.diagnostics.equalitywithintolerancefact>
- <xref:microsoft.quantum.diagnostics.nearequalityfactc>
- <xref:microsoft.quantum.diagnostics.equalityfacti>


### <a name="testing-qubit-states"></a>Testen von Qubit-Zuständen ###

In der Praxis basieren Assertionen auf der Tatsache, dass klassische Simulationen von Quantum-Mechanismen das [No-Klon-Theorem](https://arxiv.org/abs/quant-ph/9607018)nicht einhalten müssen, sodass wir bei der Verwendung eines Simulators für den Zielcomputer nicht physische Messungen und Assertionen durchführen können.
Daher können wir einzelne Vorgänge auf einem klassischen Simulator testen, bevor Sie auf Hardware bereitgestellt werden.
Auf Ziel Computern, die keine Auswertung von Assertionen zulassen, können Aufrufe von <xref:microsoft.quantum.intrinsic.assert> problemlos ignoriert werden.

Im Allgemeinen wird durch den <xref:microsoft.quantum.intrinsic.assert> Vorgang bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis immer das angegebene Ergebnis hat.
Wenn die-Übersetzung fehlschlägt, wird die Ausführung beendet, indem `fail` mit der angegebenen Meldung aufgerufen wird.
Standardmäßig ist dieser Vorgang nicht implementiert. Simulatoren, die diese unterstützen können, sollten eine Implementierung bereitstellen, die eine Lauf Zeit Überprüfung ausführt.
`Assert` verfügt über eine Signatur `((Pauli[], Qubit[], Result, String) -> ())`.
Da `Assert` eine Funktion mit einem leeren Tupel als Ausgabetyp ist, können keine Auswirkungen von aufgerufenen `Assert` in einem Q #-Programm beobachtet werden.

Die Funktion <xref:microsoft.quantum.intrinsic.assertprob> Operation bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.
Toleranz ist additiv (z. b. `abs(expected-actual) < tol`).
Wenn die-Übersetzung fehlschlägt, wird die Ausführung beendet, indem `fail` mit der angegebenen Meldung aufgerufen wird.
Standardmäßig ist dieser Vorgang nicht implementiert. Simulatoren, die diese unterstützen können, sollten eine Implementierung bereitstellen, die eine Lauf Zeit Überprüfung ausführt.
`AssertProb` verfügt über eine Signatur `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)`. Der erste `Double` Parameter gibt die gewünschte Wahrscheinlichkeit des Ergebnisses und der zweite die Toleranz.

Wir können mehr als Assert-Vorgänge durchführen, indem wir die klassischen Informationen verwenden, die von einem Simulator verwendet werden, um den internen Zustand eines Qubit darzustellen, sodass es nicht erforderlich ist, um unsere Assertionen zu testen.
Dies ermöglicht es uns insbesondere, auf nicht *kompatible* Messungen zu gründen, die auf tatsächlicher Hardware nicht möglich wären.

Angenommen, `P : Qubit => Unit` ist ein Vorgang, der den Status $ \ket{\psi} $ vorbereiten soll, wenn sich die Eingabe im Status $ \ket{0}$ befindet.
"$ \Ket{\psi '} $" ist der tatsächliche Zustand, der von `P`vorbereitet wurde.
Und dann $ \ket{\psi} = \ket{\psi '} $ if und only gibt nur dann `Zero`zurück, wenn $ \ket{\psi '} $ in der durch $ \ket{\psi} $ beschriebenen Achse gemessen wird.
Das heißt: \begin{align} \ket{\psi} = \ket{\psi '} \text{if und only if} \braket{\psi | \psi '} = 1.
\end{align} mit den primitiven Vorgängen, die in der Einleitung definiert sind, können wir direkt eine Messung ausführen, die `Zero` zurückgibt, wenn "$ \ket{\psi} $" ein eigen Zustand von einem der Pauli-Operatoren ist.


Der Vorgang <xref:microsoft.quantum.diagnostics.assertqubit> bietet eine besonders hilfreiche kurznote, um dies zu tun, wenn wir die Bestätigung $ \ket{\psi} = \ket{0}$ testen möchten.
Dies ist beispielsweise häufig der Fall, wenn nicht berechnet wurde, dass "Ancilla Qubits" vor der Freigabe an "$ \ket{0}$" zurückgegeben wird.
Die Bestätigung von $ \ket{0}$ ist auch hilfreich, wenn wir bestätigen möchten, dass zwei Zustands Vorbereitungs `P` und `Q` Vorgänge beide den gleichen Status vorbereiten und `Q` `Adjoint`unterstützt.
Insbesondere

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

Im Allgemeinen haben wir jedoch möglicherweise keinen Zugriff auf Assertionen über Zustände, die nicht mit den eigen Zuständen von Pauli-Operatoren übereinstimmen.
Beispielsweise ist $ \ket{\psi} = (\ket{0} + e ^ {i \pi/8} \ket{1})/\sqrt{2}$ nicht der Eigen Status eines Pauli-Operators, sodass wir mit <xref:microsoft.quantum.intrinsic.assertprob> nicht eindeutig feststellen können, dass der Status $ \ket{\psi '} $ gleich $ \ket{\psi} $ ist.
Stattdessen müssen wir die Assert-Assertionen $ \ket{\psi '} = \ket{\psi} $ in Annahmen zerlegen, die direkt mit den primitiven getestet werden können, die von unserem Simulator unterstützt werden.
Verwenden Sie hierzu $ \ket{\psi} = \alpha \ket{0} + \beta \ket{1}$ für die komplexen Zahlen $ \alpha = a\_r + a\_i i $ und $ \beta $.
Beachten Sie, dass dieser Ausdruck vier reelle Zahlen von $\{a\_r, a\_i, b\_r, b\_i\}$ zum angeben erfordert, da jede komplexe Zahl als Summe eines echten und imaginären Teils ausgedrückt werden kann.
Aufgrund der globalen Phase können Sie jedoch $a\_i = $0 auswählen, sodass nur drei reelle Zahlen erforderlich sind, um einen Single-Qubit-Zustand eindeutig anzugeben.

Daher müssen wir drei Assertionen angeben, die voneinander unabhängig sind, um den erwarteten Status zu bestätigen.
Hierzu wird die Wahrscheinlichkeit ermittelt, `Zero` für die einzelnen Pauli-Messungen mit "$ \alpha $" und "$ \beta $" zu beobachten und die einzelnen Ansprüche unabhängig zu bestätigen.
Lassen Sie $x $, $y $ und $z $ `Result` Werte für Pauli $X $, $Y $ und $Z $-Messungen.
Verwenden Sie dann die Wahrscheinlichkeitsfunktion für Quantum-Messungen, \begin{align} \pr (x = \texttt{Zero} | \alpha, \beta) & = \bruchteil 12 + a\_r b\_r + a\_i b\_i \\\\ \pr (y = \texttt{Zero} | \alpha, \beta) & = \bruch12 + a\_r b\_i-a\_i b\_r \\\\ \pr (z = \texttt{Zero} | \alpha, \beta) & = \bruchteil 12\left (1 + a\_r ^ 2 + a\_i ^ 2 + b\_r ^ 2 + b\_i ^ 2 \right).
\end{align}

Der <xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Vorgang implementiert diese Assertionen anhand der Darstellungen von $ \alpha $ und $ \beta $ als Werte des Typs <xref:microsoft.quantum.math.complex>.
Dies ist hilfreich, wenn der erwartete Zustand mathematisch berechnet werden kann.

### <a name="asserting-equality-of-quantum-operations"></a>Assert-Gleichheit von Quantum-Vorgängen ###

Bisher haben wir uns mit Test Vorgängen beschäftigt, bei denen bestimmte Zustände vorbereitet werden sollen.
Häufig ist es jedoch interessant, wie ein Vorgang für willkürliche Eingaben und nicht für eine einzelne, behobene Eingabe agiert.
Angenommen, wir haben einen Vorgang implementiert `U : ((Double, Qubit[]) => () : Adjoint)` der einer Familie einheitlicher Operatoren $U (t) $ entspricht, und haben einen expliziten `adjoint` Block bereitgestellt, anstatt `adjoint auto`zu verwenden.
Wir sind vielleicht daran interessiert, dass $U ^ \dagger (t) = U (-t) $, wie erwartet, wenn $t $ eine Entwicklungszeit darstellt.

Im Allgemeinen gibt es zwei verschiedene Strategien, die Sie befolgen können, um die Behauptung zu treffen, dass zwei Vorgänge `U` und `V` identisch agieren.
Zunächst können Sie überprüfen, ob `U(target); (Adjoint V)(target);` jeden Status in einer bestimmten Weise beibehält.
Zweitens können Sie überprüfen, ob `U(target); (Adjoint V)(target);`, der in der Hälfte eines entzweitigen Zustands agiert, diese entanglement beibehält.
Diese Strategien werden von den Canon-Vorgängen implementiert, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> bzw. <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced>.

> [!NOTE]
> Die oben beschriebene referenzierte-Assertionen basiert auf dem [' Choi – jamiłkowski '-"isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality)", einem mathematischen Framework, das Vorgänge auf $n $ Qubits mit entbickten Zuständen in $2N $ Qubits verknüpft.
> Insbesondere wird der Identitäts Vorgang auf $n $ Qubits durch $n $ Kopien des entspitzen Zustands $ \ket{\ beta_{00}} \mathrel{: =} (\ket{00} + \ket{11})/\sqrt{2}$ dargestellt.
> Der Vorgang <xref:microsoft.quantum.preparation.preparechoistate> implementiert dieses "isomorphism" und bereitet einen Zustand vor, der einen bestimmten Vorgang darstellt.

Diese Strategien werden ungefähr durch einen Zeit-–-Bereich unterschieden.
Das Durchlaufen der einzelnen Eingabe Zustände erfordert zusätzliche Zeit, während für die Verwendung von jede Verflechtungen als Verweis zusätzliche Qubits gespeichert werden müssen.
In Fällen, in denen ein Vorgang einen umkehrbaren klassischen Vorgang implementiert, sodass wir nur an seinem Verhalten auf der Grundlage von Berechnungs Zuständen interessiert sind, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> Tests der Gleichheit dieser eingeschränkten Eingaben.

> [!TIP]
> Die Iteration von Eingabe Zuständen wird von den enumerationsvorgängen <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> und <xref:microsoft.quantum.canon.iteratethroughcartesianpower>behandelt.
> Diese Vorgänge sind in der Regel für das Anwenden eines Vorgangs auf jedes Element des kartesischen Produkts zwischen zwei oder mehr Sätzen nützlich.

Kritischer ist jedoch, dass in den beiden Ansätzen verschiedene Eigenschaften der Vorgänge überprüft werden, die überprüft werden.
Da die direkte-Assertionen jeden Vorgang mehrmals aufruft, können sich alle zufälligen Optionen und Messergebnisse zwischen den Aufrufen jeweils einmal für jeden Eingabe Status ändern.
Im Gegensatz dazu wird jeder Vorgang von der referenzierten-Assertionen genau einmal aufgerufen, sodass überprüft wird, ob die Vorgänge *in einem einzelnen Screenshot*gleich sind.
Beide Tests sind nützlich, um die Richtigkeit von Quantum-Programmen sicherzustellen.


## <a name="further-reading"></a>Weitere nützliche Informationen ##

- <xref:microsoft.quantum.techniques.testing-and-debugging>
- <xref:microsoft.quantum.diagnostics>
