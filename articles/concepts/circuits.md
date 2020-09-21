---
Title: Quantum-Verbindungs Beschreibung: erfahren Sie, wie Sie einfache und komplexe Quantum-Vorgänge mithilfe von Quantum-Verbindungs Diagrammen visuell darstellen.
Autor: quantumwriter UID: Microsoft. Quantum. Concepts. Circuits ms. Author: v-benbra ms. Date: 12/11/2017 ms. Topic: article NO-LOC:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="quantum-circuits"></a>Quantum-Verbindungen
Stellen Sie sich einen Moment für die einheitliche Transformation $ \text { CNOT } _ { 01 } (H \otimes 1) vor $ .
Diese Gate-Sequenz ist von grundlegender Bedeutung für das Quantum Computing, da Sie einen maximalen entbickten zwei-Qubit-Zustand erstellt:

$$\mathrm{CNOT } _ { 01 } (H \otimes 1) \ket { 00 } = \frac { 1 } { \sqrt { 2 } } \left ( \ket { 00 }  +  \ket { 11 } \right ),$$

Vorgänge mit dieser oder einer größeren Komplexität sind bei Quantum-Algorithmen und der Quantum-Fehlerkorrektur universell. Daher sollte Sie als eine einfache Methode für die Visualisierung bezeichnet werden, die als *Quantum*-Verbindungs Diagramm bezeichnet wird.
Das Verbindungs Diagramm zum Vorbereiten dieses maximale entkoppelt Quantum-Zustands lautet wie folgt:

<!--- ![](.\media\1.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Leitungs Diagramm für einen maximalen entzweitigen zwei-Qubit-Zustand](~/media/1.svg)

## <a name="quantum-circuit-diagram-conventions"></a>Konventionen für das Quantum Circuit-Diagramm
Diese visuelle Sprache für Quantum-Vorgänge kann leichter verdaulich sein als das Schreiben der äquivalenten Matrix, sobald Sie die Konventionen zum Ausdrücken einer Quantum-Verbindung verstanden haben.
Wir überprüfen die folgenden Konventionen.

In einem Verbindungs Diagramm zeigt jede voll solide Linie ein Qubit oder mehr im Allgemeinen ein Qubit-Register an.
Gemäß der Konvention ist die oberste Zeile Qubit Register $ 0, $ und der Rest wird sequenziell beschriftet. Die obige Beispiel Verbindung wird als agieren auf zwei Qubits (oder gleichmäßig zwei Register, bestehend aus einem Qubit) dargestellt.
Gates, die für ein oder mehrere Qubit-Register agieren, werden als Box bezeichnet.
Beispielsweise das Symbol

<!--- ![](.\media\2.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Symbol für einen Hadamard-Vorgang, der auf einem Single-Qubit-Register agiert](~/media/2.svg)

ist ein [Hadamard](xref:microsoft.quantum.intrinsic.h) -Vorgang, der auf einem Single-Qubit-Register agiert.

Quantum-Gates werden in chronologischer Reihenfolge mit dem am weitesten links gerichteten Tor sortiert, wenn das Gate zuerst auf die Qubits angewendet wird.
Mit anderen Worten: Wenn Sie die Drähte mit dem Quantum-Zustand betrachten, bringen die Drähte den Quantenzustand durch die einzelnen Gates im Diagramm von links nach rechts.
Das heißt, 

<!--- ![](.\media\3.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Diagramm der von links nach rechts angewendeten Quantum-Gates](~/media/3.svg)

ist der einheitliche Matrix- $ CBA $ .
Die Matrix Multiplikation befolgt die gegenteilige Konvention: die ganz rechts gerichtete Matrix wird zuerst angewendet. In Quantum-Verbindungs Diagrammen wird jedoch das am weitesten links öffnende Gate zuerst angewendet.
Dieser Unterschied kann zu Verwirrung führen. Daher ist es wichtig, dass Sie diesen signifikanten Unterschied zwischen der linearen algebraischen Notation und den quantumleitungs Diagrammen beachten.

## <a name="inputs-and-outputs-of-quantum-circuits"></a>Eingaben und Ausgaben von Quantum-Verbindungen
Alle vorherigen Beispiele haben genau dieselbe Anzahl von Drähten (Qubits) für ein Quantum Gate als die Anzahl von Drähten aus dem Quantum-Gate.
Es scheint sinnvoll zu sein, dass Quantum-Verbindungen mehr oder weniger Ausgaben als Eingaben im Allgemeinen haben können.
Dies ist jedoch nicht möglich, da alle Quantum-Vorgänge, das Speichern von Messungen, einheitlich und somit umkehrbar sind.
Wenn Sie nicht über die gleiche Anzahl von Ausgaben wie Eingaben verfügen, sind Sie nicht umkehrbar und somit nicht einheitlich, was ein Widerspruch ist.
Aus diesem Grund muss jedes in einem Verbindungs Diagramm gezeichnete Feld genau die gleiche Anzahl von Drähten aufweisen, die es als beendet eingeben.

Multiqubit-Leitungs Diagramme folgen ähnlichen Konventionen wie Single-Qubit.
Als Verdeutlichung können wir eine zwei-Qubit-einheitliche Operation B als $ $ $ (H S \otimes X) definieren $ und die Leitung gleichwertig Ausdrücken.

<!--- ![](.\media\4.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Leitungs Diagramm eines zwei-Qubit-einheitlichen Vorgangs](~/media/4.svg)

Sie können B auch anzeigen, $ $ Wenn eine Aktion für ein einzelnes zwei-Qubit-Register statt 2 1-Qubit registriert ist, je nachdem, in welchem Kontext die Verbindung verwendet wird. Vielleicht ist die nützlichste Eigenschaft von solchen abstrakten Verbindungs Diagrammen, dass Sie komplizierte Quantum-Algorithmen auf hoher Ebene beschreiben können, ohne Sie in grundlegende Gates kompilieren zu müssen.
Dies bedeutet, dass Sie eine intuitions Informationen über den Datenfluss für einen großen Quantum-Algorithmus erhalten können, ohne alle Details zu verstehen, wie die einzelnen Unterroutinen innerhalb des Algorithmus funktionieren.

## <a name="controlled-gates"></a>Kontrollierte Gates
Das andere Konstrukt, das in Multi-Qubit-Quantum-Verbindungs Diagramme integriert ist, ist Control.
Die Aktion eines Quorums, das einzeln gesteuert wird $ \Lambda (d), $ wobei der Wert eines einzelnen Qubits die Anwendung von G steuert, $ $ kann durch betrachten des folgenden Beispiels einer Product State input $ \Lambda (g) ( \alpha \ket { 0 }  +  \beta \ket { 1 } ) \ket { \psi } = \alpha \ket { 0 } \ket { \psi }  +  \beta \ket { 1 } G \ket { \psi } $ interpretiert werden. Dies heißt, dass das kontrollierte Gate $ G $ auf das Register anwendet, das nur dann enthält, wenn $ \psi $ das Steuerelement-Qubit den Wert $ 1 annimmt $ .
Im Allgemeinen werden solche kontrollierten Vorgänge in Leitungs Diagrammen als

<!--- ![](.\media\5.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Leitungs Diagramm eines einzeln kontrollierten Gates](~/media/5.svg)

Hier gibt der schwarze Kreis das Quantum-Bit an, auf dem das Gate gesteuert wird, und ein vertikales Netzwerk gibt den einheitlichen an, der angewendet wird, wenn das Steuerelement-Qubit den Wert $ 1 annimmt $ .
In den Sonderfällen, in denen $ g = X $ und $ g = Z enthalten $ sind, wird die folgende Notation eingeführt, um die kontrollierte Version der Gates zu beschreiben (Beachten Sie, dass das gesteuerte X-Gate das [ $ CNOT $ Gate](xref:microsoft.quantum.intrinsic.cnot)ist):

<!--- ![](.\media\6.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Leitungs Diagramm für Sonderfälle kontrollierter Gates](~/media/6.svg)

Q# stellt Methoden bereit, mit denen die gesteuerte Version eines Vorgangs automatisch generiert werden kann. Dadurch wird der Programmierer daran bewahrt, diese Vorgänge zu codieren. Ein Beispiel hierfür finden Sie unten:

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a>Mess Operator
Der verbleibende Vorgang für die Visualisierung in Verbindungs Diagrammen ist Maßeinheit.
Die Messung nimmt eine Qubit-Registrierung an, misst Sie und gibt das Ergebnis als klassische Informationen aus.
Ein Messungs Vorgang wird durch ein Messungs Symbol bezeichnet und übernimmt immer als Eingabe ein Qubit-Register (gekennzeichnet durch eine durch Strichlinie) und gibt klassische Informationen (gekennzeichnet durch eine doppelte Linie) aus.
Eine solche unter Leitung sieht insbesondere wie folgt aus:

<!--- ![](.\media\7.svg) ---->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Symbol, das einen Messungs Vorgang darstellt](~/media/7.svg)

Q# implementiert zu diesem Zweck einen [Measure-Operator](xref:microsoft.quantum.intrinsic.measure) .
Weitere Informationen finden Sie im [Abschnitt zu Messungen](xref:microsoft.quantum.libraries.standard.prelude#measurements) .

Ebenso wird die unter Leitung

<!--- ![](.\media\8.svg) --->
<!--Keine Möglichkeit finden, diese problemlos zu zentrieren... wahrscheinlich ist eine Erweiterung erforderlich:-->
![Leitungs Diagramm, das einen kontrollierten Vorgang darstellt](~/media/8.svg)

bietet ein klassisch kontrolliertes Gate, wobei $ G $ auf das klassische Steuerelement Bit, das Wert 1 ist, angewendet wird $ $ .

## <a name="teleportation-circuit-diagram"></a>Teleportations-Verbindungs Diagramm
Quantum-Teleportation ist möglicherweise der beste Quantum-Algorithmus für die Veranschaulichung dieser Komponenten.
Sie können sich mit der entsprechenden [quanturequantum](xref:microsoft.quantum.overview.katas) -Teleportation vertraut machen. Dies ist eine Methode zum Verschieben von Daten innerhalb eines Quantum-Computers (oder sogar zwischen entfernten Quantum-Computern in einem Quantum-Netzwerk) durch die Verwendung von jede Verflechtungen und Messungen.
Interessanterweise ist es in der Lage, einen Quantenzustand, z. b. den Wert in einem bestimmten Qubit, von einem Qubit zu einem anderen zu verschieben, ohne dass Sie wissen, was der Qubit-Wert ist.
Dies ist erforderlich, damit das Protokoll gemäß den Gesetzen der Quantum-Mechanik funktioniert.
Die Verbindung mit der Quantum-Teleportation ist unten angegeben. Außerdem wird eine Version der Verbindung mit Anmerkungen bereitgestellt, um zu veranschaulichen, wie die Quantum-Verbindung gelesen wird.

<!--- ![](.\media\tp2.svg) { Breite = 50%} --->
![Quantum-Teleportations-Leitung](~/media/tp2.svg)
