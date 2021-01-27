---
Title: Beschreibung von Quantum Computing Glossar: ein Glossar allgemeiner Begriffe, Aktionen und Objekte, die bei der Quantenberechnung verwendet werden.
Autor: bradben ms. Author: v-benbra ms. Date: 9/1/2020 ms. Topic: Reference UID: Microsoft. Quantum. Glossar NO-LOC:
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

# <a name="quantum-computing-glossary"></a>Quantum Computing-Glossar

## <a name="adjoint"></a>Adjoint

Die komplexe konjugierte, die einen [Vorgang](xref:microsoft.quantum.glossary#operation)durchsetzen. Bei Vorgängen, die einen [einheitlichen](xref:microsoft.quantum.glossary#unitary-operator) Operator implementieren, ist das Adjoint das Gegenteil des Vorgangs und wird durch ein Kreuz-Symbol angegeben. Wenn der Vorgang z. b `U` . den einheitlichen Operator $ u darstellt $ , `Adjoint U` stellt $ u ^ dar \dagger $ . Weitere Informationen finden Sie unter [Functor Application](xref:microsoft.quantum.qsharp.functorapplication#functor-application).

## <a name="ancilla"></a>Ancilla

Ein [Qubit](xref:microsoft.quantum.glossary#qubit) , das als temporärer Speicher für einen Quantum-Computer fungiert und bei Bedarf zugewiesen und dessen Zuordnung aufgehoben wird.  Weitere Informationen finden Sie unter [Multiple Qubits (mehrere Qubits](xref:microsoft.quantum.concepts.multiple-qubits)).

## <a name="bell-state"></a>Glocken Zustand

Einer von vier bestimmten maxitional [entbickten](xref:microsoft.quantum.glossary#entanglement) [Quantum-Zuständen](xref:microsoft.quantum.glossary#quantum-state) mit zwei Qubits. Die vier Zustände sind definiert $ \ket { \beta _ { IJ } } = ( \mathbb { I } \otimes X ^ iz ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ . Ein Glocken Zustand wird auch als [EPR-paar](xref:microsoft.quantum.glossary#epr-pair)bezeichnet.

## <a name="bloch-sphere"></a>Bloch-Kugel

Eine grafische Darstellung eines Single-[Qubit](xref:microsoft.quantum.glossary#qubit) - [Quantum-Zustands](xref:microsoft.quantum.glossary#quantum-state) als Punkt in einer dreidimensionalen Einheits Kugel. Weitere Informationen finden Sie unter  [visualisieren von Qubits und Transformationen mithilfe der Bloch-Kugel](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

## <a name="callable"></a>Callable

Ein [Vorgang](xref:microsoft.quantum.glossary#operation) oder eine [Funktion](xref:microsoft.quantum.glossary#function) in der [ Q# Sprache](https://github.com/microsoft/qsharp-language/tree/main/Specifications/Language#q-language).
Weitere Informationen finden Sie unter [ Q# Programme](xref:microsoft.quantum.guide.programs)

## <a name="clifford-group"></a>Clifford-Gruppe

Der Satz von Vorgängen, die die oktanten der [Bloch-Kugel](xref:microsoft.quantum.glossary#bloch-sphere) und Auswirkung Permutationen der [Pauli-Operatoren](xref:microsoft.quantum.glossary#pauli-operators)belegen. Hierzu gehören die Vorgänge [ $ X $ ](xref:Microsoft.Quantum.Intrinsic.X), [ $ Y $ ](xref:Microsoft.Quantum.Intrinsic.Y), [ $ Z $ ](xref:Microsoft.Quantum.Intrinsic.Z), [ $ H $ ](xref:Microsoft.Quantum.Intrinsic.H) und [ $ S $ ](xref:Microsoft.Quantum.Intrinsic.S).

## <a name="controlled"></a>Klimatisiert

Ein Quantum- [Vorgang](xref:microsoft.quantum.glossary#operation) , der ein oder mehrere [Qubits](xref:microsoft.quantum.glossary#qubit) als Enabler für den Ziel Vorgang annimmt. Weitere Informationen finden Sie unter [Functor Application](xref:microsoft.quantum.qsharp.functorapplication#functor-application).

## <a name="dirac-notation"></a>Dirac-Notation

Eine symbolische Kurznotiz, die die Darstellung von [Quantum-Zuständen](xref:microsoft.quantum.glossary#quantum-state)vereinfacht, auch als *Bra-Ket-* Notation bezeichnet.  Der *Bra* -Teil stellt einen Zeilen Vektor dar, z $ \bra { } = \begin{bmatrix} { } & { . B. a _1 a _2, } \end{bmatrix} $ und der *Ket* -Teil stellt einen Spalten Vektor, $ \ket { b } = \begin{bmatrix} b { _1 } \\\\ b { _2 } \end{bmatrix} $ , dar. Weitere Informationen finden Sie unter [Dirac-Notation](xref:microsoft.quantum.concepts.dirac).

## <a name="eigenvalue"></a>Eigen Wert

Der Faktor, um den die Größe eines [eigen Vektors](xref:microsoft.quantum.glossary#eigenvector) einer bestimmten Transformation von der Anwendung der Transformation geändert wird.  Bei einer quadratischen Matrix $ M $ und einem eigen Vektor $ v $ , dann $ mv = CV $ , wobei $ c $ der Eigen Wert ist und eine komplexe Zahl beliebiger Argumente sein kann. Weitere Informationen finden Sie unter [Advanced Matrix Concepts](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="eigenvector"></a>Eigen Vektor

Ein Vektor, dessen Richtung durch eine angegebene Transformation unverändert bleibt und dessen Größe durch einen Faktor geändert wird, der dem [eigen Wert](xref:microsoft.quantum.glossary#eigenvalue)dieses Vektors entspricht. Bei einer quadratischen Matrix $ M $ und einem eigen Wert $ c $ $ = ist MV CV $ , wobei $ v $ ein eigen Vektor der Matrix ist und eine komplexe Zahl beliebiger Argumente sein kann. Weitere Informationen finden Sie unter [Advanced Matrix Concepts](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="entanglement"></a>Verschränkung

Quantum-Partikel (z. b. [Qubits](xref:microsoft.quantum.glossary#qubit)) können verbunden oder *entkoppelt* werden, sodass Sie nicht unabhängig voneinander beschrieben werden können. Die Messergebnisse werden auch dann korreliert, wenn Sie unendlich weit entfernt sind. "Entanglement" ist für die [Messung](xref:microsoft.quantum.glossary#measurement) des [Status](xref:microsoft.quantum.glossary#quantum-state) eines Qubit unabdingbar.  Weitere Informationen finden Sie unter [Advanced Matrix Concepts](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="epr-pair"></a>EPR-paar

Einer von vier bestimmten maxitional entbickten [Quantum-Zuständen](xref:microsoft.quantum.glossary#quantum-state) mit zwei [Qubits](xref:microsoft.quantum.glossary#qubit). Die vier Zustände sind definiert $ \ket { \beta _ { IJ } } = ( \mathbb { 1 } \otimes X ^ iz ^ j) ( \ket { 00 }  +  \ket { 11 } )/ \sqrt { 2 } $ . Ein EPR-Paar wird auch als [Glocken Zustand](xref:microsoft.quantum.glossary#bell-state) bezeichnet.

## <a name="evolution"></a>Entwicklungs

Die Art und Weise, in der sich ein [Quantum-Zustand](xref:microsoft.quantum.glossary#quantum-state) Weitere Informationen finden Sie unter [Matrix exponentiale](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).

## <a name="function"></a>Funktion
Ein Typ von Unterroutine in der Q# Sprache, der rein deterministisch ist. Obwohl Funktionen innerhalb von Quantum-Algorithmen verwendet werden, können Sie nicht auf [Qubits](xref:microsoft.quantum.glossary#qubit) oder Aufrufe von [Vorgängen](xref:microsoft.quantum.glossary#operation)reagieren. Weitere Informationen finden Sie unter [ Q# Programme](xref:microsoft.quantum.guide.programs)

## <a name="gate"></a>Tors

Ein Legacy Begriff für bestimmte intrinsische Quantum- [Vorgänge](xref:microsoft.quantum.glossary#operation), basierend auf dem Konzept der klassischen Logik Gates. Eine [Quantum](xref:microsoft.quantum.glossary#quantum-circuit-diagram) -Verbindung ist ein Netzwerk von Gates, das auf dem gleichen Konzept klassischer Logik Leitungen basiert.

## <a name="global-phase"></a>Globale Phase

Wenn zwei [Zustände](xref:microsoft.quantum.glossary#quantum-state) mit einem Vielfachen einer komplexen Zahl $ e ^ i identisch sind { \phi } $ , werden Sie sich bis zu einer globalen Phase unterscheiden. Im Gegensatz zu lokalen Phasen können globale Phasen nicht durch eine beliebige [Measurment](xref:microsoft.quantum.glossary#measurement)beobachtet werden. Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="hadamard"></a>Hadamard

Der Hadamard-Vorgang (auch als "Hadamard Gate or Transform" bezeichnet) agiert mit einem einzelnen [Qubit](xref:microsoft.quantum.glossary#qubit) und versetzt ihn in eine gerade [Superposition](xref:microsoft.quantum.glossary#superposition) von $ \ket { 0 } $ oder $ \ket { 1, } $ Wenn sich das Qubit anfänglich im Zustand "0" befindet $ \ket { } $ . In Q# wird dieser Vorgang durch den vordefinierten [`H`](xref:Microsoft.Quantum.Intrinsic.H) Vorgang angewendet.

## <a name="immutable"></a>Unveränderlich

Eine Variable, deren Wert nicht geändert werden kann. Eine unveränderliche Variable in Q# wird mit dem- `let` Schlüsselwort erstellt. Verwenden Sie zum Deklarieren von Variablen, die geändert werden *können* , das [änderbare](xref:microsoft.quantum.glossary#immutable) -Schlüsselwort, um und das-Schlüsselwort zu deklarieren und den `set` Wert 

## <a name="measurement"></a>Messung

Eine Manipulation eines [Qubits](xref:microsoft.quantum.glossary#qubit) (oder eines Satzes von Qubits), der das Ergebnis einer Beobachtung ergibt, was das Abrufen eines klassischen Bits bewirkt. Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).

## <a name="mutable"></a>Veränderlich

Eine Variable, deren Wert geändert werden kann, nachdem Sie erstellt wurde. Eine änderbare Variable in Q# wird mit dem `mutable` -Schlüsselwort deklariert und mithilfe des- `set` Schlüssel Worts geändert. Mit dem `let` -Schlüsselwort erstellte Variablen sind [unveränderlich](xref:microsoft.quantum.glossary#immutable) , und ihr Wert kann nicht geändert werden.

## <a name="namespace"></a>Namespace

Eine Bezeichnung für eine Auflistung verwandter Namen (d. h. [Vorgänge](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function)und [benutzerdefinierte Typen](xref:microsoft.quantum.glossary#user-defined-type)). Beispielsweise zeichnet der Namespace [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation) alle Symbole auf, die in der Standardbibliothek definiert sind und bei der Vorbereitung von anfänglichen Zuständen helfen.

## <a name="operation"></a>Vorgang

Die grundlegende Einheit der Quantum-Berechnung in Q# . Dies entspricht ungefähr einer Funktion in C, C++ oder python oder einer statischen Methode in c# oder Java. Weitere Informationen finden Sie unter [ Q# Programme](xref:microsoft.quantum.guide.programs).

## <a name="oracle"></a>Oracle

Eine Unterroutine, die zur Laufzeit Daten abhängige Informationen für einen Quantum-Algorithmus bereitstellt. In der Regel besteht das Ziel darin, eine [Superposition](xref:microsoft.quantum.glossary#superposition) der Ausgaben bereitzustellen, die den Eingaben in der superposition entsprechen. Weitere Informationen finden Sie unter [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>Teilweise Anwendung

Aufrufen einer [Funktion](xref:microsoft.quantum.glossary#function) oder eines [Vorgangs](xref:microsoft.quantum.glossary#operation) ohne alle erforderlichen Eingaben. Dadurch wird eine neue [Aufruf Bare](xref:microsoft.quantum.glossary#callable) zurückgegeben, bei der nur die fehlenden Parameter (die durch einen Unterstrich angegeben werden) während einer zukünftigen Anwendung bereitgestellt werden müssen. Weitere Informationen finden Sie unter [partielle Anwendung](xref:microsoft.quantum.qsharp.partialapplication).

## <a name="pauli-operators"></a>Pauli-Operatoren

Eine Reihe von 3 2 x 2-einheitlichen Matrizen, die als `X` , `Y` und Quantum-Vorgänge bezeichnet werden `Z` . Die Identitätsmatrix $ I $ ist häufig auch in der Gruppe enthalten.  $I = \begin{bmatrix} 1 & 0 \\\\ 0 & 1 \end{bmatrix} $ , $ X = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} $ , $ Y = \begin{bmatrix} 0 & -i \\\\ i & 0 \end{bmatrix} $ , $ Z = \begin{bmatrix} 1 & 0 \\\\ 0 & -1 \end{bmatrix} $ .   Weitere Informationen finden Sie unter [Single-Qubit-Vorgänge](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).

## <a name="quantum-circuit-diagram"></a>Quantum-Verbindungs Diagramm

Eine Methode zur grafischen Darstellung der Abfolge von [Gates](xref:microsoft.quantum.glossary#gate) für einfache Quantum-Programme, z. b. 

![Beispiel für ein Verbindungs Diagramm](~/media/qpe.png). 

Weitere Informationen finden Sie unter [Quantum](xref:microsoft.quantum.concepts.circuits)-Verbindungen.

## <a name="quantum-libraries"></a>Quantum-Bibliotheken

Auflistungen von [Vorgängen](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function) und [benutzerdefinierten Typen](xref:microsoft.quantum.glossary#user-defined-type) zum Erstellen von Q# Programmen. Die [Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro) wird standardmäßig installiert. Weitere verfügbare Bibliotheken sind die [Chemie Bibliothek](xref:microsoft.quantum.chemistry.concepts.intro), die [Numerics-Bibliothek](xref:microsoft.quantum.numerics.intro) und die [Machine Learning-Bibliothek](xref:microsoft.quantum.machine-learning.concepts.intro).

## <a name="quantum-state"></a>Quantum-Status

Der genaue Zustand eines isolierten Quantum-Systems, von dem [Mess](xref:microsoft.quantum.glossary#measurement) Wahrscheinlichkeiten extrahiert werden können. In Quantum Computing verwendet der Quantum-Simulator diese Informationen, um zu simulieren, wie Qubits auf Vorgänge reagieren. Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="qubit"></a>Qubit

Eine grundlegende Einheit von Quantum-Informationen, analog zu einem *Bit* im klassischen Computing. Weitere Informationen finden Sie [unter Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="repeat-until-success"></a>Wiederholung-bis-Erfolg

Ein Konzept, das häufig in Quantum-Algorithmen verwendet wird, das wiederholt eine Berechnung verwendet, bis eine bestimmte Bedingung erfüllt ist. Wenn die Bedingung nicht erfüllt wird, ist häufig ein Fixup erforderlich, bevor Sie den Vorgang wiederholen, indem Sie die nächste Iterationen eingeben. Weitere Informationen finden Sie im [ Q# Benutzerhandbuch](xref:microsoft.quantum.guide) .

## <a name="standard-libraries"></a>Standardbibliotheken

[Vorgänge](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function) und [benutzerdefinierte Typen](xref:microsoft.quantum.glossary#user-defined-type) , die während der Installation zusammen mit dem Compiler installiert werden Q# . Die Implementierung der Standardbibliothek ist in Bezug auf die Zielcomputer agnostisch. Weitere Informationen finden Sie unter [Standard Bibliotheken](xref:microsoft.quantum.libraries.standard.intro).

## <a name="superposition"></a>Superposition

Das Konzept von Quantum Computing, dass ein [Qubit](xref:microsoft.quantum.glossary#qubit) eine lineare Kombination aus zwei Zuständen ( $ \ket { 0 } $ und 1) ist $ \ket { } $ , bis es [gemessen](xref:microsoft.quantum.glossary#measurement)wird.  Weitere Informationen finden Sie Untergrund Legendes zu [Quantum Computing](xref:microsoft.quantum.overview.understanding).

## <a name="target-machine"></a>Zielcomputer

Ein Kompilierungs Ziel, das ein abstraktes Quantum-Programm auf Hardware oder Simulation senkt. Dies schließt in der Regel Umschreib Vorgänge für viele Zwecke ein, einschließlich Gate-Ersetzung, Codierung für die Fehlerkorrektur, geometrisches Layout und andere. Weitere Informationen finden Sie unter [Quantum Simulatoren und Host Applications](xref:microsoft.quantum.machines).

## <a name="teleportation"></a>Teleportation

Eine Methode zum erneuten Generieren von Daten (bzw. des [Quantums](xref:microsoft.quantum.glossary#quantum-state)) von einem [Qubit](xref:microsoft.quantum.glossary#qubit) von einem Ort zu einem anderen, ohne dass das Qubit mithilfe von [jede Verflechtungen](xref:microsoft.quantum.glossary#entanglement) und [Messung](xref:microsoft.quantum.glossary#measurement)physisch verschoben wird.  Weitere Informationen finden Sie unter [Quantum](xref:microsoft.quantum.concepts.circuits) -Verbindungen und die jeweilige Kata bei [Quantum Katas](xref:microsoft.quantum.overview.katas).

## <a name="tuple"></a>Tupel

Eine Auflistung von durch Trennzeichen getrennten Werten, die als einzelner Wert fungieren. Der *Typ* eines Tupels wird durch die Typen der darin enthaltenen Werte definiert. In Q# sind Tupel [unveränderlich und können geschmustet](xref:microsoft.quantum.glossary#immutable) werden, Arrays enthalten oder in einem Array verwendet werden. Weitere Informationen finden Sie unter [Tupel](xref:microsoft.quantum.qsharp.valueliterals#tuple-literals).

## <a name="unitary-operator"></a>Einheitlicher Operator

Ein Operator, dessen Umkehrung gleich dem zugehörigen [Adjoint](xref:microsoft.quantum.glossary#adjoint)ist, d. h. $ UU ^ { \dagger } = \id $ .

## <a name="user-defined-type"></a>Benutzerdefinierter Typ

Ein benutzerdefinierter Typ, der ein oder mehrere benannte oder anonyme Elemente enthalten kann. Weitere Informationen finden Sie unter [Typdeklarationen] Microsoft. Quantum. qsharp. typedeklarationen # Type-Deklarationen).
