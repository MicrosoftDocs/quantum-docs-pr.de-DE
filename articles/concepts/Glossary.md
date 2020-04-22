---
title: Quantum Computing Glossar
description: Ein Glossar mit gängigen Begriffen, Aktionen und Objekten, die im Quantencomputing verwendet werden.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.glossary
ms.openlocfilehash: ee78515a0f47730b7d3df10da0853c5b8a7f6624
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "81482229"
---
# <a name="quantum-computing-glossary"></a>Quantum Computing Glossar

## <a name="adjoint"></a>Adjoint

Das komplexe Konjugat transponieren einer [Operation](xref:microsoft.quantum.glossary#operation). Bei Vorgängen, die einen [einheitlichen](xref:microsoft.quantum.glossary#unitary-operator) Operator implementieren, ist das Adjoint die Umkehrung des Vorgangs und wird durch ein Dolchsymbol gekennzeichnet. Wenn der Vorgang `U` z. B. den einheitlichen `Adjoint U` Operator $U darstellt, stellt er $U-Dolch dar. Weitere Informationen finden Sie unter [Adjoint](xref:microsoft.quantum.language.file-structure#adjoint).

## <a name="ancilla"></a>Ancilla

Ein [Qubit,](xref:microsoft.quantum.glossary#qubit) das als temporärer Speicher für einen Quantencomputer dient und bei Bedarf zugewiesen und de-zugeordnet wird.  Weitere Informationen finden Sie unter [Mehrere Qubits](xref:microsoft.quantum.concepts.multiple-qubits).

## <a name="bell-state"></a>Bell State

Einer von vier spezifischen maximal [verhedderten](xref:microsoft.quantum.glossary#entanglement) [Quantenzuständen](xref:microsoft.quantum.glossary#quantum-state) von zwei Qubits. Die vier Zustände sind definiert: "ket" beta_"ij" = ('mathbb'I'',omalS{00} X'iZ'j) ('ket + 'ket{11}'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''{2} Ein Glockenzustand ist auch als [EPR-Paar](xref:microsoft.quantum.glossary#epr-pair)bekannt.

## <a name="bloch-sphere"></a>Bloch-Kugel

Eine grafische Darstellung eines [ein-qubit-Quantenzustandes](xref:microsoft.quantum.glossary#quantum-state) als Punkt in einer dreidimensionalen Einheitenkugel.[qubit](xref:microsoft.quantum.glossary#qubit) Weitere Informationen finden Sie unter [Visualisieren von Qubits und Transformationen mithilfe der Bloch-Sphäre](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).

## <a name="callable"></a>Aufrufbaren

Ein [Vorgang](xref:microsoft.quantum.glossary#operation) oder [eine Funktion](xref:microsoft.quantum.glossary#function) in der Sprache Q. Weitere Informationen finden Sie unter [Vorgangs- und Funktionstypen](xref:microsoft.quantum.language.type-model#operation-and-function-types).

## <a name="clifford-group"></a>Clifford-Gruppe

Der Satz von Operationen, die die Oktanten der [Bloch-Kugel](xref:microsoft.quantum.glossary#bloch-sphere) besetzen und Effektpermutationen der [Pauli-Operatoren](xref:microsoft.quantum.glossary#pauli-operators). Dazu gehören die Vorgänge [$X](xref:microsoft.quantum.intrinsic.x), [$Y](xref:microsoft.quantum.intrinsic.y), [$Z](xref:microsoft.quantum.intrinsic.z), [$H](xref:microsoft.quantum.intrinsic.h) und [$S .](xref:microsoft.quantum.intrinsic.s)

## <a name="controlled"></a>Kontrolliert

Eine [Quantenoperation,](xref:microsoft.quantum.glossary#operation) die ein oder mehrere [Qubits](xref:microsoft.quantum.glossary#qubit) als Enabler für den Zielvorgang benötigt. Weitere Informationen finden Sie unter [Kontrolliertes](xref:microsoft.quantum.language.type-model#controlled).

## <a name="dirac-notation"></a>Dirac Notation

Eine symbolische Abkürzung, die die Darstellung von [Quantenzuständen](xref:microsoft.quantum.glossary#quantum-state)vereinfacht, auch *BRA-Ket-Notation* genannt.  Der *BH-Teil* stellt einen Zeilenvektor dar, z. B. ""Bra" " = "begin"bmatrix" "A"-& A-_2-"End"-Bmatrix, und der *Ket-Teil* stellt einen \\ \\ Spaltenvektor dar, "Ket" = "Begin-Bmatrix" "B"-B-_2-"""""" " " " . Weitere Informationen finden Sie unter [Dirac Notation](xref:microsoft.quantum.concepts.dirac).

## <a name="eigenvalue"></a>Eigenvalue

Der Faktor, durch den die Größe eines [Eigenvektors](xref:microsoft.quantum.glossary#eigenvector) einer gegebenen Transformation durch die Anwendung der Transformation geändert wird.  Wenn Sie eine quadratische Matrix $M und einen Eigenvektor $v, dann $Mv = cv, wobei $c der Eigenwert ist und eine komplexe Anzahl jedes Arguments sein kann. Weitere Informationen finden Sie unter [Erweiterte Matrixkonzepte](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="eigenvector"></a>Eigenvector

Ein Vektor, dessen Richtung durch eine gegebene Transformation unverändert bleibt und dessen Größe um einen Faktor geändert wird, der dem [Eigenwert](xref:microsoft.quantum.glossary#eigenvalue)dieses Vektors entspricht. Bei einer quadratischen Matrix $M und einem Eigenwert $c, dann $Mv = cv, wobei $v ein Eigenvektor der Matrix ist und eine komplexe Anzahl jedes Arguments sein kann. Weitere Informationen finden Sie unter [Erweiterte Matrixkonzepte](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="entanglement"></a>Verschränkung

Quantenteilchen, wie [z. B. Qubits,](xref:microsoft.quantum.glossary#qubit)können so miteinander verbunden oder *verheddert* werden, dass sie nicht unabhängig voneinander beschrieben werden können. Ihre Messergebnisse sind korreliert, auch wenn sie unendlich weit voneinander entfernt sind. Verflechtung ist wichtig, um den [Zustand](xref:microsoft.quantum.glossary#quantum-state) eines Qubits zu [messen.](xref:microsoft.quantum.glossary#measurement)  Weitere Informationen finden Sie unter [Erweiterte Matrixkonzepte](xref:microsoft.quantum.concepts.matrix-advanced).

## <a name="epr-pair"></a>EPR-Paar

Einer von vier spezifischen maximal verhedderten [Quantenzuständen](xref:microsoft.quantum.glossary#quantum-state) von zwei [Qubits](xref:microsoft.quantum.glossary#qubit). Die vier Zustände sind definiert: "Ket" beta_,ij"{1} = ('mathbb''otimes X'iZ'j) ('''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''{00} {11}{2} Ein EPR-Paar ist auch als [Glockenzustand](xref:microsoft.quantum.glossary#bell-state) bekannt

## <a name="evolution"></a>Evolution

Wie sich ein [Quantenzustand](xref:microsoft.quantum.glossary#quantum-state) im Laufe der Zeit ändert. Weitere Informationen finden Sie unter [Matrix-Exponentiale](xref:microsoft.quantum.concepts.matrix-advanced#matrix-exponentials).

## <a name="function"></a>Funktion
Eine Art von Unterroutine in der Sprache Q, die rein klassisch ist (nicht quanten) Während Funktionen innerhalb von Quantenalgorithmen verwendet werden, können sie nicht auf [Qubits](xref:microsoft.quantum.glossary#qubit) oder [Aufrufoperationen](xref:microsoft.quantum.glossary#operation)reagieren. Weitere Informationen finden Sie unter [Vorgangs- und Funktionstypen](xref:microsoft.quantum.language.type-model#operation-and-function-types).

## <a name="gate"></a>Tor

Ein Vermächtnisbegriff für eine [Quantenoperation](xref:microsoft.quantum.glossary#operation), basierend auf dem Konzept der klassischen Logiktore. Ein [Quantenkreis](xref:microsoft.quantum.glossary#quantum-circuit-diagram) ist ein Netz von Toren (oder Operationen), basierend auf dem ähnlichen Konzept klassischer Logikschaltungen.

## <a name="global-phase"></a>Globale Phase

Wenn zwei [Zustände](xref:microsoft.quantum.glossary#quantum-state) bis zu einem Vielfachen einer komplexen Zahl $e identisch sind, werden sie bis zu einer globalen Phase unterschiedlich sein. Im Gegensatz zu lokalen Phasen können globale Phasen nicht durch [Messungen](xref:microsoft.quantum.glossary#measurement)beobachtet werden. Weitere Informationen finden Sie unter [Der Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="hadamard"></a>Hadamard

Die Hadamard-Operation (auch als Hadamard-Gate oder -Transformation bezeichnet) wirkt auf ein einzelnes [Qubit](xref:microsoft.quantum.glossary#qubit) und{1}versetzt sie in eine gleichmäßige [Überlagerung](xref:microsoft.quantum.glossary#superposition) von "ket"{0}oder "Ket", wenn sich der Qubit zunächst im Zustand "ket"{0}befindet. Dieser Vorgang wird in der Datei Q- durch den vordefinierten [`H`](xref:microsoft.quantum.intrinsic.h) Vorgang angewendet.

## <a name="immutable"></a>Unveränderlich

Eine Variable, deren Wert nicht geändert werden kann. Eine unveränderliche Variable in Q' wird mit dem `let` Schlüsselwort erstellt. Um Variablen zu deklarieren, die geändert werden `set` *können,* verwenden Sie das [veränderbare](xref:microsoft.quantum.glossary#immutable) Schlüsselwort zum Deklarieren und das Schlüsselwort, um den Wert zu ändern. 

## <a name="measurement"></a>Messung

Eine Manipulation eines [Qubits](xref:microsoft.quantum.glossary#qubit) (oder einer Reihe von Qubits), die das Ergebnis einer Beobachtung ergibt und in der Tat ein klassisches Bit erhält. Weitere Informationen finden Sie unter [Der Qubit](xref:microsoft.quantum.concepts.qubit#measuring-a-qubit).

## <a name="mutable"></a>Veränderlich

Eine Variable, deren Wert nach der Erstellung geändert werden kann. Eine veränderliche Variable in Q' wird mit dem `mutable` Schlüsselwort deklariert und mit dem `set` Schlüsselwort geändert. Variablen, die `let` mit dem Schlüsselwort erstellt wurden, sind [unveränderlich,](xref:microsoft.quantum.glossary#immutable) und ihr Wert kann nicht geändert werden.

## <a name="namespace"></a>Namespace

Eine Bezeichnung für eine Auflistung verwandter Namen (d. h. [Vorgänge](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function)und [benutzerdefinierte Typen](xref:microsoft.quantum.glossary#user-defined-type)). Beispielsweise beschriftet der Namespace [Microsoft.Quantum.Preparation](xref:microsoft.quantum.preparation) alle in der Standardbibliothek definierten Symbole, die beim Vorbereiten von Anfangszuständen helfen.

## <a name="operation"></a>Vorgang

Die grundeinheit der Quantenausführung in Q. Sie entspricht in etwa einer Funktion in C, C++ oder Python oder einer statischen Methode in C- oder Java. Weitere Informationen finden Sie unter [Vorgangs- und Funktionstypen](xref:microsoft.quantum.language.type-model#operation-and-function-types).

## <a name="operator-application"></a>Operatoranwendung

Durchführen einer Quantenoperation. Dies wendet in der Regel eine einheitliche Matrix auf den aktuellen Quantenzustandsvektor an.

## <a name="oracle"></a>Oracle

Eine Unterroutine, die datenabhängige Informationen für einen Quantenalgorithmus zur Laufzeit bereitstellt. In der Regel besteht das Ziel darin, eine [Überlagerung](xref:microsoft.quantum.glossary#superposition) von Ausgängen bereitzustellen, die den Eingängen entspricht, die sich in Überlagerung befinden. Weitere Informationen finden Sie unter [Oracles](xref:microsoft.quantum.libraries.data-structures#oracles).

## <a name="partial-application"></a>Teilanmeldung

Aufruf einer [Funktion](xref:microsoft.quantum.glossary#function) oder [eines Vorgangs](xref:microsoft.quantum.glossary#operation) ohne alle erforderlichen Eingaben. Dadurch wird ein neuer [Aufrufwert zurückgegeben,](xref:microsoft.quantum.glossary#callable) der nur die fehlenden Parameter (angezeigt durch einen Unterstrich) benötigt, um während einer zukünftigen Anwendung bereitgestellt zu werden. Beispielsweise können Sie `MyFunc(x : int, y : int) : int {return x + y;}` sie bei der Funktion teilweise `let NewFunc = MyFunc(_, 3)`auf eine neue Funktion anwenden. Sie können die neue Funktion dann zu einem `NewFunc(2)` späteren Zeitpunkt mit dem fehlenden Parameter aufrufen, der den Wert *5*zurückgibt.  Weitere Informationen finden Sie unter [Teilanwendung](xref:microsoft.quantum.language.expressions#partial-application).

## <a name="pauli-operators"></a>Pauli-Betreiber

Ein Satz von drei 2 x 2 einheitshaften Matrizen, die als die `X` `Y` , und `Z` Quantenoperationen bekannt sind. Die Identitätsmatrix, $I, ist oft auch im Set enthalten.  $I = "begin"bmatrix" \\ \\ 1 & 0 0 & 1 ,,end"bmatrix", $X \\ \\ = "begin"bmatrix" 0 & 1 1 & 0 "end"bmatrix", $Y = "begin"bmatrix" 0 \\ \\ & -i \\ \\ & 0 "end"bmatrix", $Z = "begin"bmatrix" 1 & 0 0 & -1   Weitere Informationen finden Sie unter [Single-Qubit-Vorgänge](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).

## <a name="quantum-circuit-diagram"></a>Quanten-Schaltplan

Eine Methode zur grafischen Darstellung der [Operationsabfolge](xref:microsoft.quantum.glossary#operation) (oder [Gates](xref:microsoft.quantum.glossary#gate)) für einfache Quantenprogramme, z. B. ![Beispielschaltplan](~/media/qpe.png). Weitere Informationen finden Sie unter [Quantenschaltungen](xref:microsoft.quantum.concepts.circuits).

## <a name="quantum-libraries"></a>Quantenbibliotheken

Auflistungen von [Vorgängen](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function) und benutzerdefinierten Typen zum Erstellen von [Q-Programmen.](xref:microsoft.quantum.glossary#user-defined-type) Die [Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro) ist standardmäßig installiert. Weitere verfügbare Bibliotheken sind die [Chemiebibliothek](xref:microsoft.quantum.chemistry.concepts.intro), die [Numerics-Bibliothek](xref:microsoft.quantum.numerics.intro) und die [Machine Learning-Bibliothek](xref:microsoft.quantum.machine-learning.concepts.intro).

## <a name="quantum-state"></a>Quantenzustand

Der genaue Zustand eines isolierten Quantensystems, aus dem [Messwahrscheinlichkeiten](xref:microsoft.quantum.glossary#measurement) extrahiert werden können. Im Quantencomputer verwendet der Quantensimulator diese Informationen, um zu simulieren, wie Qubits auf Operationen reagieren. Weitere Informationen finden Sie unter [Der Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="qubit"></a>Qubit

Eine grundlegende Einheit von Quanteninformationen, analog zu einem *Bit* im klassischen Rechnen. Weitere Informationen finden Sie unter [Der Qubit](xref:microsoft.quantum.concepts.qubit).

## <a name="repeat-until-success"></a>Wiederholungbis-Erfolg

Ein Quantenalgorithmus, der probabilistisch erfolgreich ist. Nach einem Fehler wird die Routine erneut versucht, bis erfolgreich (oder ein Limit erreicht wurde). Weitere Informationen finden Sie unter [Wiederholen bis zum Erfolg (RUS)](xref:microsoft.quantum.techniques.qubits#measurements)

## <a name="standard-libraries"></a>Standardbibliotheken

[Vorgänge](xref:microsoft.quantum.glossary#operation), [Funktionen](xref:microsoft.quantum.glossary#function) und [benutzerdefinierte Typen,](xref:microsoft.quantum.glossary#user-defined-type) die zusammen mit dem Q-Compiler während der Installation installiert werden. Die Standardbibliotheksimplementierung ist in Bezug auf Zielmaschinen agnostisch. Weitere Informationen finden Sie unter [Standardbibliotheken](xref:microsoft.quantum.libraries.standard.intro).

## <a name="superposition"></a>Überlagerung

Das Konzept im Quantencomputing, dass ein [Qubit](xref:microsoft.quantum.glossary#qubit) eine lineare Kombination aus zwei Zuständen ist, ,,,,,,,,,,,,,,,,,,""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""" [measured](xref:microsoft.quantum.glossary#measurement)  Weitere Informationen finden Sie unter [Was ist Quantencomputer](xref:microsoft.quantum.overview.what).

## <a name="target-machine"></a>Zielmaschine

Ein Kompilierungsziel, das ein abstraktes Quantenprogramm in Richtung Hardware oder Simulation senkt. Dies umfasst in der Regel Neuschreibungen für viele Zwecke, einschließlich Gate-Ersatz, Codierung für Fehlerkorrektur, geometrisches Layout und andere. Weitere Informationen finden Sie unter [Quantensimulatoren und Hostanwendungen](xref:microsoft.quantum.machines).

## <a name="teleportation"></a>Teleportation

Eine Methode zum Regenerieren von Daten oder des [Quantenzustands](xref:microsoft.quantum.glossary#quantum-state)von einem [Qubit](xref:microsoft.quantum.glossary#qubit) von einem Ort zum anderen, ohne das Qubit physisch zu bewegen, mit [Verflechtung](xref:microsoft.quantum.glossary#entanglement) und [Messung](xref:microsoft.quantum.glossary#measurement).  Weitere Informationen finden Sie unter [Quantenschaltungen](xref:microsoft.quantum.concepts.circuits) und [Zusammensetzen](xref:microsoft.quantum.techniques.puttingittogether).

## <a name="tuple"></a>Tupel

Eine Auflistung von durch Kommas getrennten Werten, die als einzelner Wert fungiert. Der *Typ* eines Tupels wird durch die darin enthaltenen Wertetypen definiert. Die Tupeln sind [unveränderlich](xref:microsoft.quantum.glossary#immutable) und können geschachtelt werden, Arrays enthalten oder in einem Array verwendet werden. Weitere Informationen finden Sie unter [Tuple-Typen](xref:microsoft.quantum.language.type-model#tuple-types).

## <a name="unitary-operator"></a>Einheitsoperator

Ein Operator, dessen Inverse gleich seinem [Adjoint](xref:microsoft.quantum.glossary#adjoint)ist, d. h. $UU .

## <a name="user-defined-type"></a>Benutzerdefinierter Typ

Eine Auflistung integrierter oder zuvor definierter Typen, die als einzelne Einheit bezeichnet werden können. Weitere Informationen finden Sie unter [Benutzerdefinierte Typen](xref:microsoft.quantum.language.type-model#user-defined-types).