---
title: Simulieren von hamiltona Dynamics | Microsoft-Dokumentation
description: Simulieren von hamiltonan Dynamics-Konzepten
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
ms.openlocfilehash: 4d1924386eadb427e8f53bc0a177453a341f185f
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2019
ms.locfileid: "74864456"
---
# <a name="simulating-hamiltonian-dynamics"></a>Simulieren von hamiltona Dynamics

Sobald der hamiltonan als Summe der elementaren Operatoren ausgedrückt wurde, kann die Dynamics dann mithilfe eines Hosts bekannter Techniken in grundlegende Gate-Vorgänge kompiliert werden.
Zu den drei effizienten Ansätzen gehören Trotter – Suzuki-Formeln, lineare Kombinationen von Uni-und qubisierungen.
Im folgenden werden diese drei Ansätze erläutert und konkrete Q #-Beispiele für die Implementierung dieser Methoden mithilfe der hamiltonan Simulations Bibliothek erläutert.


## <a name="trottersuzuki-formulas"></a>Trotter – Suzuki-Formeln
Die Idee hinter Trotter – Suzuki-Formeln ist einfach: Ausdrücken Sie die hamiltonan als Summe von leicht zu simulierten hamiltonaten, und nähern Sie die Gesamtentwicklung als Sequenz dieser einfacheren Entwicklungen.
Legen Sie insbesondere $H = \ sum_ {j = 1} ^ m H_j $ der hamiltonan.
Dann $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \ prod_ {j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $, was heißt, dass, wenn $t \ll $1, der Fehler in dieser Näherungs Weise unerheblich wird.
Beachten Sie, dass der Fehler in dieser Näherung nicht $O (m ^ 2 t ^ 2) $, wenn $e ^ {-i H t} $ eine gewöhnliche exponentielle ist.
Dieser Fehler tritt auf, weil $e ^ {-IHT} $ ein Operator exponentiell ist und daher bei der Verwendung dieser Formel ein Fehler aufgetreten ist, da die $H _J $ Terms nicht übernehmen (*d. h.* $H _J H_k \nE H_k H_j $ im allgemeinen).

Wenn $t $ groß ist, kann Trotter– Suzuki-Formeln weiterhin verwendet werden, um die Dynamics genau zu simulieren, indem Sie Sie in eine Abfolge kurzer Zeit Schritte aufteilen.
$R $ ist die Anzahl der Schritte, die in der Zeitentwicklung ausgeführt wurden.
Dann haben wir die $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \left (\ prod_ {j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r), $ $. Dies impliziert, dass der Fehler, wenn $r $ als $m ^ 2 t ^ 2/\ Epsilon $ skaliert werden kann, höchstens $ \epsilon $ für alle $ \epsilon-> 0 $.

Genauere Näherungen können erstellt werden, indem eine Sequenz von Operator exponentialen erstellt wird, sodass die fehlerbegriffe abgebrochen werden.
Die einfachste Formel, die symmetrische trockformel oder die Rollen Aufteilung, hat die Form $ $ U_1 (t) = \ prod_ {j = 1} ^ m e ^ {-iH_j t/2} \ prod_ {j = m} ^ 1 e ^ {-iH_j t} = e ^ {-IHT} + O (m ^ 3 t ^ 3), $ $, die für alle $ \epsilon-> 0 $ weniger als $ \epsilon $ erstellt werden können, indem Sie $r $ zum Skalieren als $m ^ {3/2} t ^ {3/2}/\sqrt {\ Epsilon} $ auswählen.

Sogar auf $U _1 $ basierende trotterformeln können erstellt werden.
Die einfachste ist die folgende Formel für die vierte Bestellung: ursprünglich eingeführt von Suzuki: $ $ U_2 (t) = U_1 ^ 2 (s_1t) U_1 ([1-4s_1] t) U_1 ^ 2 (s_1 t) = e ^ {-IHT} + O (m ^ 5T ^ 5), $ $ WHERE $s _1 = (4-4 ^ {1/3}) ^{-1}$.
Im Allgemeinen können beliebig hochwertige Formeln ähnlich konstruiert werden. die Kosten, die durch die Verwendung komplexerer Integratoren entstehen, überwiegen jedoch häufig die Vorteile der vierten Reihenfolge für die meisten praktischen Probleme.

Damit die oben genannten Strategien funktionieren, benötigen wir eine Methode zum Simulieren einer breiten Klasse von $e ^ {-iH_j t} $.
Die einfachste Familie der hamiltoner und ist wohl nützlichsten, die wir hier verwenden können, sind Pauli-Operatoren.
Die Pauli-Operatoren können problemlos simuliert werden, da Sie mithilfe von Clifford-Vorgängen (Standard Gates in Quantum Computing) diagonalisiert werden können.
Nach der Diagonalisierung können auch Ihre Eigenwerte gefunden werden, indem die Parität der Qubits berechnet wird, auf die Sie reagieren.

Beispiel: $ $ e ^ {-ix\otimes X t} = (h\otimes h) e ^ {-iz\otimes Z t} (h\otimes h), $ $ WHERE $ $ e ^ {-i Z \otimes Z t} = \begin{bmatrix} e ^ {-IT} & 0 & 0 & 0 \\\
        0 & e ^ {i t} & 0 & 0 \\\
        0 & 0 & e ^ {IT} & 0 \\\
        0 & 0 & 0 & e ^ {-IT} \end{bmatrix}.
$ $ Hier, $e ^ {-IHT} \ket{00} = e ^ {IT} \ket{00}$ und $e ^ {-IHT} \ket{01} = e ^ {-IT} \ket{01}$, das direkt als Folge der Tatsache angesehen werden kann, dass die Parität von $0 $ $0 $ ist, während die Parität der Bitzeichenfolge $1 $ $1 $ ist.

Exponentiale von Pauli-Operatoren können mithilfe des <xref:microsoft.quantum.primitive.exp>-Vorgangs direkt in Q # implementiert werden:
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies e^{- i X \otimes X t} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

Bei fermionic hamiltoniern ordnet die [– Wigner-Zerlegung von Jordanien](xref:microsoft.quantum.chemistry.concepts.jordanwigner) die hamiltonan einer Summe von Pauli-Operatoren zu.
Dies bedeutet, dass die oben beschriebene Vorgehensweise problemlos an die Simulation der Chemie angepasst werden kann.
Anstatt alle Pauli-Begriffe in der Jordanien-Wigner-Darstellung manuell zu durchlaufen, finden Sie unten ein einfaches Beispiel für die Ausführung einer solchen Simulation innerhalb der Chemie.
Unser Ausgangspunkt ist eine [Jordanien – Wigner-Codierung](xref:microsoft.quantum.chemistry.concepts.jordanwigner) der fermionic hamiltonan, ausgedrückt als Instanz der `JordanWignerEncoding`-Klasse.

```csharp
    // This example uses the following namespaces:
    // using Microsoft.Quantum.Chemistry.OrbitalIntegrals;
    // using Microsoft.Quantum.Chemistry.Fermion;
    // using Microsoft.Quantum.Chemistry.Pauli;
    // using Microsoft.Quantum.Chemistry.QSharpFormat;

    // We create an instance of the `FermionHamiltonian` objecclasst to store the terms.
    var hamiltonian = new OrbitalIntegralHamiltonian(new[] 
    {
        new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123),
        new OrbitalIntegral(new[] { 0, 1 }, 0.456)
    }).ToFermionHamiltonian(IndexConvention.UpDown);

    // We convert this fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = hamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);

    // We now convert this representation into a format consumable by Q#.
    var qSharpData = jordanWignerEncoding.ToQSharpFormat();
```

Dieses Format der –-Darstellung von Jordanien, das von den Q #-Simulations Algorithmen genutzt werden kann, ist ein benutzerdefinierter Typ `JordanWignerEncodingData`.
In Q # wird dieses Format an eine Hilfsfunktion `TrotterStepOracle`, die einen Operator zurückgibt, der die Zeit Weiterentwicklung mithilfe des Trotter – Suzuki Integrator zusätzlich zu anderen Parametern zurückgibt, die für seine Ausführung erforderlich sind.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single time-step.
using(qubits = Qubit[nQubits]){

    // Apply single step of time-evolution
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

Wichtig ist, dass diese Implementierung einige Optimierungen anwendet, die in [Simulation der elektronischen Struktur mit Quantum-Computern](https://arxiv.org/abs/1001.3855) erläutert werden, und die [Quantum-Algorithmen für die Quantum-Chemie verbessern](https://arxiv.org/abs/1403.1539) , um die erforderliche Anzahl von Single-Qubit-Drehungen zu minimieren und Simulations Fehler zu verringern.

## <a name="qubitization"></a>Qubisierung

Die qubisierung ist eine alternative Methode für die Simulation, bei der Ideen aus Quantum-Durchgängen zum Simulieren von Quantum Dynamics verwendet werden.
Obwohl die qubisierung mehr Qubits als trotterformeln erfordert, verspricht die Methode eine optimale Skalierung mit der Entwicklungszeit und der Fehlertoleranz.
Aus diesen Gründen wurde sie zu einer bevorzugten Methode zum Simulieren von hamiltona Dynamics im allgemeinen und zum Lösen des Problems mit der elektronischen Struktur.

Auf hoher Ebene wird dies durch die qubisierung durch die folgenden Schritte erreicht.
Lassen Sie zunächst $H = \ sum_j H_J H_j $ für einheitlich und hermitian $H _J $ und $h _J \ge $0.
Durch die Durchführung eines paar von Reflektionen implementiert die qubisierung einen Operator, der $ $W = e ^ {\pm i \cos ^{-1}(H/| H | _1)}, $ $, wobei $ | H | _1 = \ sum_j | H_J | $ entspricht.
Der nächste Schritt umfasst das Transformieren der Eigenwerte des Walk-Operators aus $e ^ {i\pm \cos ^{-1}(E_k/| h | _1)} $, wobei $E _K $ die Eigenwerte von $H $ bis $e ^ {-iE_k t} $ sind.
Dies kann durch eine Vielzahl von Methoden zur Verwendung von Quantum-Singular-Werten erreicht werden, einschließlich der [Quantum-Signalverarbeitung](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).

Wenn nur statische Mengen gewünscht werden (z. b. die Grund Zustands Energie der hamiltonan), genügt es, die [Phasen Schätzung](xref:microsoft.quantum.libraries.characterization) direkt auf $W $ anzuwenden, um die Energie des Grund Zustands aus dem Ergebnis zu schätzen, indem der Kosinus des Ergebnisses übernommen wird.
Dies ist von großer Bedeutung, da die Transformation für das Spektral-und nicht eine Quantum-Methode zur Singular-Wert-Transformation ermöglicht wird.

Auf einer detaillierteren Ebene erfordert die Implementierung der qubisierung zwei Unterroutinen, die die Schnittstellen für die hamiltonan bereitstellen.
Im Gegensatz zu Trotter– Suzuki-Methoden sind diese Unterroutinen Quantum nicht klassisch, und ihre Implementierung erfordert, dass logarithmisch mehr Qubits verwendet werden, als für eine trotterbasierte Simulation erforderlich wären.

Die erste Quantum-Unterroutine, die von der qubisierung verwendet wird, heißt $ \operatschmue{SELECT} $, und es wird versprochen, dass Sie "\begin{Equation} \operatorname{Select} \ket{j} \ket{\psi} = \ket{j} H_j \ket{\psi}" ergeben. \end{Equation}, wobei jeder $H _J $ als hermitian angenommen wird. und einheitlich.
Obwohl dies möglicherweise restriktiv ist, erinnern Sie sich, dass die Pauli-Operatoren hermitian und einheitlich sind und dass Anwendungen wie die Quantum-Chemie-Simulation natürlich in dieses Framework fallen.
Der $ \operatorname{Select} $-Vorgang, vielleicht überraschend, ist tatsächlich ein reflektionevorgang.
Dies kann von der Tatsache eingesehen werden, dass $ \operatschmue{Select} ^ 2 \ Ket {j} \ket{\psi} = \ket{j} \ket{\psi} $ seit jeder $H _J $ einheitlich und hermitian ist und somit die Eigenwerte $ \pm $1 aufweisen.

Die zweite Unterroutine heißt $ \operatschmue{Prepare} $.
Während der SELECT-Vorgang eine Möglichkeit bietet, auf jeden der hamiltona-Begriffe einheitlich zuzugreifen $H _J $ bietet die Prepare-Unterroutine eine Methode für den Zugriff auf die Koeffizienten $h _J $, \begin{Equation} \operatorname{Prepare}\ket{0} = \ sum_j \sqrt{\bruchteil {H_J} {| H | _1}} \ket{j}.
\end{Equation} bei Verwendung eines multipliziert kontrollierten Phasen Gates sehen wir, dass $ $ \lambda\ket{0}^ {\otimes n} = \begin{Cases} \-\ket{x} & \text{if} x = 0 \\\
        \ket{x} & \text{otherwi*} \end{Cases}.
$$

Der $ \operatorname{Prepare} $-Vorgang wird nicht direkt in der qubisierung verwendet, sondern stattdessen verwendet, um eine Reflektion über den Status zu implementieren, den $ \operatorname{Prepare} $ erstellt $ $ \begin{align} R &amp; = 1-2 \ Operatorname {Prepare} \ket{0}\bra{0} \operatschmue{Prepare} ^{-1} \\\\ &amp; = \operatschmue{Prepare} \lambda \operatschmue{Prepare} ^{-1}.
\end{align} $ $

Der Walk-Operator, $W $, kann im Format $ \operatschmue{SELECT} $ und $R $ als $ $ W = \operatorname{Select} R ausgedrückt werden. $ $, das wiederum angezeigt werden kann, um einen Operator zu implementieren, der (bis zu einem isometry) zum $e ^ {\pm i \cos ^{-1}(H/| H | _1)} $ entspricht.

Diese Unterroutinen können einfach in Q # eingerichtet werden.
Stellen Sie sich als Beispiel das einfache Qubit-Kreuz, das eine Kreuz Zerlegung durch $H = x_1 + X_2 + Z_1 Z_2 $ in Erwägung.
In diesem Fall wird der f #-Code, der den Vorgang $ \operatschmue{Select} $ implementiert, von <xref:microsoft.quantum.canon.multiplexoperations>aufgerufen, während der $ \operatorname{Prepare} $-Vorgang mithilfe von <xref:microsoft.quantum.preparation.preparearbitrarystate>implementiert werden kann.
Ein Beispiel zum Simulieren des Hubbard-Modells finden Sie in einem [Q #](https://github.com/microsoft/Quantum/tree/master/samples/simulation/hubbard)-Beispiel.

Wenn Sie diese Schritte für willkürliche chemische Probleme manuell angeben, wäre dies sehr aufwändig, was mithilfe der Chemie Bibliothek vermieden werden sollte.
Ähnlich wie beim Trotter– Suzuki-Simulations Algorithmus wird der `JordanWignerEncodingData` an die Hilfsfunktion `QubitizationOracle` weitergegeben, die den walkoperator zurückgibt, zusätzlich zu anderen Parametern, die für die Ausführung erforderlich sind.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/oneNorm`, where oneNorm is the sum of absolute values of all probabilities in state prepared by `Prepare`.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  QubitizationOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single step of the quantum walk.
using(qubits = Qubit[nQubits]){

    // Apply single step of quantum walk.
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

Wichtig ist, dass die Implementierungs <xref:microsoft.quantum.chemistry.jordanwigner.qubitizationoracle> auf beliebige hamiltonane anwendbar ist, die als lineare Kombination von Pauli-Zeichen folgen angegeben werden.
Eine Version, die für Chemie Simulationen optimiert ist, wird mithilfe von <xref:microsoft.quantum.chemistry.jordanwigner.optimizedqubitizationoracle>aufgerufen.
Diese Version ist so optimiert, dass die Anzahl der T-Gates mithilfe der Techniken, die in [Encoding Electronic Spectra in Quantum-Leitungen mit linearer T-Komplexität](https://arxiv.org/abs/1805.03662)erläutert werden,
