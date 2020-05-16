---
title: 'Diagnose in den Q # Standard-Bibliotheken'
description: 'Erfahren Sie mehr über die Diagnosefunktionen und-Vorgänge in den Q # Standard-Bibliotheken, die zum Abfangen von Fehlern oder Fehlern in quantenprogrammen verwendet werden'
author: cgranade
uid: microsoft.quantum.libraries.diagnostics
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: fa5173f710dd9e0b0b2c110e45aa0bf019111aca
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426309"
---
# <a name="diagnostics"></a>Diagnose #

Wie bei der klassischen Entwicklung ist es wichtig, dass Sie Fehler und Fehler in quantumprogrammen diagnostizieren können.
Die Q #-Standardbibliotheken bieten eine Vielzahl verschiedener Möglichkeiten, um die Richtigkeit von quantenprogrammen sicherzustellen, wie in beschrieben <xref:microsoft.quantum.guide.testingdebugging> .
Diese Unterstützung wird größtenteils in Form von Funktionen und Vorgängen bereitgestellt, die entweder den Zielcomputer anweisen, zusätzliche Diagnoseinformationen für das Host Programm oder den Entwickler bereitzustellen, oder die Richtigkeit der Bedingungen und invarianten erzwingen, die durch den Funktions-oder Vorgangs Aufrufsatz ausgedrückt werden.

## <a name="machine-diagnostics"></a>Computer Diagnose ##

Die Diagnose von klassischen Werten kann mithilfe der-Funktion abgerufen werden <xref:microsoft.quantum.intrinsic.message> , um eine Nachricht auf Computer abhängige Weise zu protokollieren.
Standardmäßig wird die Zeichenfolge in die Konsole geschrieben.
Wird in Verbindung mit interinterpolierten Zeichen folgen verwendet und <xref:microsoft.quantum.intrinsic.message> erleichtert das Melden von Diagnoseinformationen über klassische Werte:

```Q#
let angle = Microsoft.Quantum.Math.PI() * 2.0 / 3.0;
Message($"About to rotate by an angle of {angle}...");
```

> [!NOTE]
> `Message`weist eine Signatur auf `(String -> Unit)` , die wiederum darstellt, dass die Ausgabe einer Debugprotokollierung nicht innerhalb von Q # beobachtet werden kann.

Die <xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics.dumpregister> callables und weisen Zielcomputer an, Diagnoseinformationen zu allen derzeit zugeordneten Qubits bzw. zu einem bestimmten Register von Qubits bereitzustellen.
Jeder Zielcomputer variiert in Abhängigkeit von den Diagnoseinformationen, die als Reaktion auf eine dumpanweisung bereitgestellt werden.
Der Zielcomputer des [vollständigen Zustands Simulators](xref:microsoft.quantum.machines.full-state-simulator) stellt beispielsweise dem Host Programm den Zustands Vektor bereit, den er intern zur Darstellung eines Register von Qubits verwendet.
Im Vergleich dazu stellt der Zielcomputer des Dienst Bereitstellungs- [Simulators](xref:microsoft.quantum.machines.toffoli-simulator) für jedes Qubit ein einzelnes klassisches Bit bereit.

 Weitere Informationen zur Ausgabe des [vollständigen Zustands Simulators](xref:microsoft.quantum.machines.full-state-simulator) `DumpMachine` finden Sie im Abschnitt Dumpfunktionen in unserem [Artikel zum Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging#dump-functions).


## <a name="facts-and-assertions"></a>Fakten und Assertionen ##

Wie unter [Testen und Debuggen](xref:microsoft.quantum.guide.testingdebugging)erläutert, kann eine Funktion oder ein Vorgang mit der Signatur `Unit -> Unit` `Unit => Unit` bzw. als Komponenten *Test*gekennzeichnet werden.
Jeder Komponenten Test besteht in der Regel aus einem kleinen Quantum-Programm zusammen mit einer oder mehreren Bedingungen, die die Richtigkeit des Programms überprüfen.
Diese Bedingungen können in Form von _Fakten_ _auftreten, die_die Werte Ihrer Eingaben überprüfen, oder Assertionen, die die Zustände von einem oder mehreren als Eingabe übergebenen Qubits überprüfen.

Beispielsweise `EqualityFactI(1 + 1, 2, "1 + 1 != 2")` stellt die mathematische Tatsache dar, dass $1 + 1 = $2, während `AssertQubit(One, qubit)` die Bedingung darstellt, die die Messung `qubit` `One` mit Sicherheit zurückgibt.
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

Im allgemeinen <xref:microsoft.quantum.intrinsic.assert> wird durch den Vorgang bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis immer das angegebene Ergebnis hat.
Wenn die-Übersetzung fehlschlägt, wird die Ausführung beendet, indem `fail` mit der angegebenen Meldung aufgerufen wird.
Standardmäßig ist dieser Vorgang nicht implementiert. Simulatoren, die diese unterstützen können, sollten eine Implementierung bereitstellen, die eine Lauf Zeit Überprüfung ausführt.
`Assert`hat die Signatur `((Pauli[], Qubit[], Result, String) -> ())` .
Da `Assert` eine Funktion mit einem leeren Tupel als Ausgabetyp ist, sind keine Auswirkungen des Aufrufs `Assert` in einem Q #-Programm Observable-Ausdrücke.

Die <xref:microsoft.quantum.intrinsic.assertprob> Vorgangs Funktion bestätigt, dass das Messen der angegebenen Qubits in der angegebenen Pauli-Basis das angegebene Ergebnis mit der angegebenen Wahrscheinlichkeit innerhalb einiger Toleranz hat.
Toleranz ist additiv (z. b. `abs(expected-actual) < tol` ).
Wenn die-Übersetzung fehlschlägt, wird die Ausführung beendet, indem `fail` mit der angegebenen Meldung aufgerufen wird.
Standardmäßig ist dieser Vorgang nicht implementiert. Simulatoren, die diese unterstützen können, sollten eine Implementierung bereitstellen, die eine Lauf Zeit Überprüfung ausführt.
`AssertProb`hat die Signatur `((Pauli[], Qubit[], Result, Double, String, Double) -> Unit)` . Der erste `Double` Parameter gibt die gewünschte Wahrscheinlichkeit des Ergebnisses und der zweite die Toleranz an.

Wir können mehr als Assert-Vorgänge durchführen, indem wir die klassischen Informationen verwenden, die von einem Simulator verwendet werden, um den internen Zustand eines Qubit darzustellen, sodass es nicht erforderlich ist, um unsere Assertionen zu testen.
Dies ermöglicht es uns insbesondere, auf nicht *kompatible* Messungen zu gründen, die auf tatsächlicher Hardware nicht möglich wären.

Angenommen, `P : Qubit => Unit` Es handelt sich um einen Vorgang, der für die Vorbereitung des Zustands $ \ket{\psi} $ vorgesehen ist, wenn seine Eingabe im Status $ \ket {0} $ liegt.
Let $ \ket{\psi '} $ ist der tatsächliche Zustand, der von vorbereitet wird `P` .
Dann gibt $ \ket{\psi} = \ket{\psi '} $ nur dann zurück, wenn $ \ket{\psi '} $ in der durch $ \ket{\psi} $ beschriebenen Achse gemessen wird `Zero` .
Das heißt: \begin{align} \ket{\psi} = \ket{\psi '} \text{if und only if} \braket{\psi | \psi '} = 1.
\end{align} mit den primitiven Vorgängen, die in der Einleitung definiert sind, können wir direkt eine Messung ausführen, die zurückgibt, `Zero` Wenn $ \ket{\psi} $ ein eigen Zustand eines der Pauli-Operatoren ist.


Der Vorgang <xref:microsoft.quantum.diagnostics.assertqubit> bietet eine besonders hilfreiche kurznote, um dies zu tun, wenn wir die Assertionen $ \ket{\psi} = \ket $ testen möchten {0} .
Dies ist beispielsweise häufig der Fall, wenn die Berechnung von Ancilla Qubits an $ \ket $ vor der Freigabe nicht berechnet wurde {0} .
Die Bestätigung von $ \ket {0} $ ist auch hilfreich, wenn wir bestätigen möchten, dass zwei Zustands Vorbereitung `P` und- `Q` Vorgänge jeweils denselben Status vorbereiten und wenn von `Q` unterstützt wird `Adjoint` .
Insbesondere

```qsharp
using (register = Qubit()) {
    P(register);
    Adjoint Q(register);

    AssertQubit(Zero, register);
}
```

Im Allgemeinen haben wir jedoch möglicherweise keinen Zugriff auf Assertionen über Zustände, die nicht mit den eigen Zuständen von Pauli-Operatoren übereinstimmen.
Beispielsweise ist $ \ket{\psi} = (\ket {0} + e ^ {i \pi/8} \ket {1} )/\sqrt {2} $ kein eigen Zustand eines Pauli-Operators, sodass wir nicht verwenden können, <xref:microsoft.quantum.intrinsic.assertprob> um eindeutig zu ermitteln, ob der Status $ \ket{\psi '} $ gleich $ \ket{\psi} $ ist.
Stattdessen müssen wir die Assert-Assertionen $ \ket{\psi '} = \ket{\psi} $ in Annahmen zerlegen, die direkt mit den primitiven getestet werden können, die von unserem Simulator unterstützt werden.
Verwenden Sie hierzu $ \ket{\psi} = \alpha \ket {0} + \beta \ket {1} $ für die komplexen Zahlen $ \alpha = a \_ r + a \_ i i $ und $ \beta $.
Beachten Sie, dass für diesen Ausdruck vier reelle Zahlen ($ \{ a \_ r), a \_ i, b \_ r, b \_ i \} $ zur Angabe erforderlich sind, da jede komplexe Zahl als Summe eines reellen und imaginären Teils ausgedrückt werden kann.
Aufgrund der globalen Phase können Sie jedoch $a \_ i = $0 auswählen, sodass nur drei reelle Zahlen erforderlich sind, um einen Single-Qubit-Zustand eindeutig anzugeben.

Daher müssen wir drei Assertionen angeben, die voneinander unabhängig sind, um den erwarteten Status zu bestätigen.
Hierzu finden Sie die Wahrscheinlichkeit `Zero` , dass die einzelnen Pauli-Messungen für "$ \alpha $" und "$ \beta $" beachtet werden, und die einzelnen Ansprüche unabhängig voneinander zu bestätigen.
Lassen Sie $x $, $y $ und $z $ be- `Result` Werte für Pauli $X $, $Y $, bzw. $Z $-Messungen aus.
Verwenden Sie dann die Wahrscheinlichkeitsfunktion für Quantum-Messungen, \begin{align} \pr (x = \texttt{Zero} | \alpha, \beta) & = \bruchteil 12 + a \_ r b \_ r + a \_ i b \_ i \\ \\ \pr (y = \texttt{Zero} | \alpha, \beta) & = \bruchteil 12 + a \_ r b \_ i-a \_ i b \_ r \\ \\ \pr (z = \texttt{Zero} | \alpha, \beta) & = \bruch12\left (1 + a \_ r ^ 2 + a \_ i ^ 2 + b \_ r ^ 2 + b \_ i ^ 2 \right).
\end{align}

Der- <xref:microsoft.quantum.diagnostics.assertqubitisinstatewithintolerance> Vorgang implementiert diese Assertionen anhand von Darstellungen von $ \alpha $ und $ \beta $ als Werte des Typs <xref:microsoft.quantum.math.complex> .
Dies ist hilfreich, wenn der erwartete Zustand mathematisch berechnet werden kann.

### <a name="asserting-equality-of-quantum-operations"></a>Assert-Gleichheit von Quantum-Vorgängen ###

Bisher haben wir uns mit Test Vorgängen beschäftigt, bei denen bestimmte Zustände vorbereitet werden sollen.
Häufig ist es jedoch interessant, wie ein Vorgang für willkürliche Eingaben und nicht für eine einzelne, behobene Eingabe agiert.
Angenommen, wir haben einen Vorgang implementiert, `U : ((Double, Qubit[]) => () : Adjoint)` der einer Familie einheitlicher Operatoren $U (t) $ entspricht, und haben einen expliziten Block bereitgestellt, `adjoint` anstatt zu verwenden `adjoint auto` .
Wir sind vielleicht daran interessiert, dass $U ^ \dagger (t) = U (-t) $, wie erwartet, wenn $t $ eine Entwicklungszeit darstellt.

Im Allgemeinen gibt es zwei verschiedene Strategien, die Sie befolgen können, um die-Assertionen für zwei Vorgänge durchführen `U` und `V` identisch agieren.
Zuerst können wir überprüfen, ob `U(target); (Adjoint V)(target);` jeden Status in einer bestimmten Weise beibehält.
Zum anderen können wir überprüfen, ob die-Funktion `U(target); (Adjoint V)(target);` bei der Hälfte eines entzweitigen Zustands diese entanglement beibehält.
Diese Strategien werden von den Canon <xref:microsoft.quantum.diagnostics.assertoperationsequalinplace> -Vorgängen <xref:microsoft.quantum.diagnostics.assertoperationsequalreferenced> bzw. implementiert.

> [!NOTE]
> Die oben beschriebene referenzierte-Assertionen basiert auf dem [' Choi – jamiłkowski '-"isomorphism](https://en.wikipedia.org/wiki/Channel-state_duality)", einem mathematischen Framework, das Vorgänge auf $n $ Qubits mit entbickten Zuständen in $2N $ Qubits verknüpft.
> Insbesondere wird der Identitäts Vorgang für $n $ Qubits durch $n $ Kopien des entspitzen Zustands $ \ket{\ beta_ {00} } \mathrel{: =} (\ket {00} + \ket {11} )/\sqrt {2} $ dargestellt.
> Der Vorgang <xref:microsoft.quantum.preparation.preparechoistate> implementiert dieses "isomorphism" und bereitet einen Zustand vor, der einen bestimmten Vorgang darstellt.

Diese Strategien werden ungefähr durch einen Zeit-–-Bereich unterschieden.
Das Durchlaufen der einzelnen Eingabe Zustände erfordert zusätzliche Zeit, während für die Verwendung von jede Verflechtungen als Verweis zusätzliche Qubits gespeichert werden müssen.
In Fällen, in denen ein Vorgang einen umkehrbaren klassischen Vorgang implementiert, sodass wir nur an seinem Verhalten hinsichtlich der Berechnungsbasis Zustände interessiert sind, <xref:microsoft.quantum.diagnostics.assertoperationsequalinplacecompbasis> testet die Gleichheit dieser eingeschränkten Eingaben.

> [!TIP]
> Die Iteration von Eingabe Zuständen wird von den enumerationsvorgängen <xref:microsoft.quantum.canon.iteratethroughcartesianproduct> und behandelt <xref:microsoft.quantum.canon.iteratethroughcartesianpower> .
> Diese Vorgänge sind in der Regel für das Anwenden eines Vorgangs auf jedes Element des kartesischen Produkts zwischen zwei oder mehr Sätzen nützlich.

Kritischer ist jedoch, dass in den beiden Ansätzen verschiedene Eigenschaften der Vorgänge überprüft werden, die überprüft werden.
Da die direkte-Assertionen jeden Vorgang mehrmals aufruft, können sich alle zufälligen Optionen und Messergebnisse zwischen den Aufrufen jeweils einmal für jeden Eingabe Status ändern.
Im Gegensatz dazu wird jeder Vorgang von der referenzierten-Assertionen genau einmal aufgerufen, sodass überprüft wird, ob die Vorgänge *in einem einzelnen Screenshot*gleich sind.
Beide Tests sind nützlich, um die Richtigkeit von Quantum-Programmen sicherzustellen.


## <a name="further-reading"></a>Weitere nützliche Informationen ##

- <xref:microsoft.quantum.guide.testingdebugging>
- <xref:microsoft.quantum.diagnostics>
