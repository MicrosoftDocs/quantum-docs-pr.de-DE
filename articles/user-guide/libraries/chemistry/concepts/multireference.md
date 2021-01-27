---
title: Korrelierte Wellenfunktionen
description: Erfahren Sie mehr über dynamische und nicht dynamische Korrelationen in wavefunctions mithilfe der Microsoft Quantum Chemistry-Bibliothek.
author: guanghaolow
ms.author: gulow
ms.date: 05/28/2019
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.multireference
no-loc:
- Q#
- $$v
ms.openlocfilehash: ab3d90d79c7c14a1ef5b3aa833df49be186f3dd7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856270"
---
# <a name="correlated-wavefunctions"></a>Korrelierte Wellenfunktionen

Für viele Systeme, insbesondere solche, die sich in der Nähe der Gleichgewichts Geometrie befinden, stellt die " [Hartree – Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) "-Theorie eine qualitative Beschreibung von molekularen Eigenschaften durch einen einzigen Determinanten Verweis Status bereit. Um jedoch eine quantitative Genauigkeit zu erzielen, müssen Sie auch Korrelations Effekte in Erwägung gezogen. 

In diesem Kontext ist es wichtig, sich zwischen dynamischen und nicht dynamischen Korrelationen zu unterscheiden.
Dynamical-Korrelationen ergeben sich aus der Tendenz, dass sich die Elektronen voneinander unterscheiden, z. b. aufgrund der interelektronischen Abwehr. Dieser Effekt kann modelliert werden, indem die Erregung von Elektronen aus dem Verweis Zustand berücksichtigt wird. Nicht dynamische Korrelationen treten auf, wenn die Wellenfunktion von mindestens zwei Konfigurationen in nulloverreihenfolge dominiert wird, auch wenn nur eine qualitative Beschreibung des Systems erreicht werden soll.
Dies erfordert eine untergeordnete Position von Determinanten und ist ein Beispiel für eine multireference-wavefunction.

Die Bibliothek "Chemistry" bietet eine Möglichkeit, eine nullte-Reihenfolge-wavefunction für das multireference-Problem als Superposition von Determinanten anzugeben. Dieser Ansatz, der als "Sparse multireference wavefunctions" bezeichnet wird, ist wirksam, wenn nur wenige Komponenten ausreichen, um die Superposition anzugeben. Die Bibliothek bietet auch eine Methode zum einbeziehen dynamischer Korrelationen über einen einzigen Determinanten Verweis über den generalisierten einheitlichen gekoppelt-Cluster-Ansatz. Außerdem erstellt Sie auch Quantum-Leitungen, die diese Zustände auf einem Quantum-Computer generieren. Diese Zustände können im [broombridge-Schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)angegeben werden, und es wird auch die Funktionalität bereitgestellt, um diese Zustände manuell über die Chemie Bibliothek anzugeben.

## <a name="sparse-multi-reference-wavefunction"></a>Multireference-Wellenfunktion mit geringer Dichte
Der multiverweisstatus "$ \ket{\ psi_ {\rM {mcscf}}} $" kann explizit als lineare Kombination von $N "$--Elektronen-Slater determininants" angegeben werden.
\begin{align} \ket{\ psi_ {\rM {mcscf}}} \propto \ sum_ {i_1 < i_2 < \cdots < i_N} \ lambda_ {i_1, i_2, \cdots, i_N} a ^ \ dagger_ {i_1} a ^ \ dagger_ {i_2} \cdots a ^ \ dagger_ {i_N} \ket {0} .
\end{align} beispielsweise kann der Status $ \propto (0,1 a ^ \ dagger_1a ^ \ dagger_2a ^ \ dagger_6-0,2 a ^ \ dagger_2a ^ \ dagger_1a ^ \ dagger_5) \ket {0} $ wie folgt in der Chemie Bibliothek angegeben werden.
```csharp
// Create a list of tuples where the first item of each 
// tuple are indices to the creation operators acting on the
// vacuum state, and the second item is the coefficient
// of that basis state.
var superposition = new[] {
    (new[] {1, 2, 6}, 0.1),
    (new[] {2, 1, 5}, -0.2) };

// Create a fermion wavefunction object that represents the superposition.
var wavefunction = new FermionWavefunction<int>(superposition);
```
Diese explizite Darstellung der superposition-Komponenten ist wirksam, wenn nur wenige Komponenten angegeben werden müssen. Sie sollten diese Darstellung vermeiden, wenn viele Komponenten erforderlich sind, um den gewünschten Zustand exakt zu erfassen. Der Grund hierfür sind die Gate-Kosten der Quantum-Leitung, die diesen Status auf einem Quantum-Computer vorbereiten, der mindestens linear mit der Anzahl der superposition-Komponenten skaliert, und höchstens quadratisch mit der einnorm der superposition-Verstärkung.

## <a name="unitary-coupled-cluster-wavefunction"></a>Einheitliche gekoppelte Cluster Wellenfunktion
Es ist auch möglich, eine einheitliche gekoppelte Cluster-wavefunction $ \ket{\ psi_ {\rM {UCC}}} $ mithilfe der chemisteriebibliothek anzugeben. In dieser Situation haben wir einen einzelnen Determinanten Verweis Status, z. & # # amp; a. $ \ket{\ psi_ {\rM{SCF}}} $. Die Komponenten der einheitlichen, gekoppelten Cluster-wavefunction werden dann mithilfe eines einheitlichen Operators, der auf einen Referenz Zustand agiert, als implizität angegeben.
Dieser einheitliche Operator wird häufig als $e ^ {T-T ^ \dagger} $ geschrieben, wobei $T-T ^ \dagger $ der Anti-hermitian-Cluster Operator ist. Folglich \begin{align} \ket{\ psi_ {\rM {UCC}}} = e ^ {T-T ^ \dagger}\ket{\ psi_ {\rM{SCF}}}.
\end{align}

Es ist auch üblich, den Cluster Operator $T = T_1 + T_2 + \cdots $ in Teile aufzuteilen, wobei jeder Teil $T _J $ $j $-Body-Bedingungen enthält. In der Theorie des verallgemeinerten verknüpften Clusters hat der Einzel Text Cluster-Operator (Singles) das Format \begin{align} T_1 = \ sum_ {PQ} T ^ {p} _ {q} a ^ \ dagger_p a_q, \end{align}

und zwei Text Cluster Operator (Doubles) haben das Format \begin{align} T_2 = \ sum_ {pqrs} T ^ {PQ} _ {RS} a ^ \ dagger_p a ^ \ dagger_q a_r a_s.
\end{align}

Bedingungen höherer Ordnung (dreipel, Vierbeiner usw.) sind möglich, werden aber derzeit von der Chemie Bibliothek nicht unterstützt.

Beispiel: $ \ket{\ psi_ {\rM{SCF}}} = a ^ \ dagger_1 a ^ \ dagger_2 \ket {0} $ und Let $T = 0,123 a ^ \ dagger_0 A_1 dagger_0a + 0,456 a ^ \ dagger_3 ^ \ A_1 a_2 dagger_3a-0,789 a ^ \ dagger_2 ^ \ A_1 a_0 $. Dieser Status wird in der Chemie Bibliothek wie folgt instanziiert.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { 1, 2 };

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {0, 1}, 0.123),
    (new [] {0, 3, 1, 2}, 0.456),
    (new [] {3, 2, 1, 0}, 0.789)
};

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunction = new FermionWavefunction<int>(reference, clusterOperator);
```

Die drehkonverzierung kann explizit durch Angabe von `SpinOrbital` Indizes anstelle von ganzzahligen Indizes vorgenommen werden. Beispiel: $ \ket{\ psi_ {\rM{SCF}}} = a ^ \ dagger_ {1, \uparamerow} a ^ \ dagger_ {2, \downarrow}\ket {0} $ und Let $T = 0,123 a ^ \ dagger_ {0, \uparser} a_ {1, \uparamerow} + 0,456 a ^ \ dagger_ {0, \uparamerow} a ^ \ dagger_ {3, \downarrow} a_ {1, \uanrow} a_ {2, \downarrow}-0,789 a ^ \ dagger_ {3, \ubirow} a ^ \ dagger_ {2, \ubirow} a_ {1, \uparamerow} a_ {0, \uparamerow} $ be-/zulasstuf. Dieser Status wird in der Chemie Bibliothek wie folgt instanziiert.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {(0, Spin.u), (1, Spin.u)}, 0.123),
    (new [] {(0, Spin.u), (3, Spin.d), (1, Spin.u), (2, Spin.d)}, 0.456),
    (new [] {(3, Spin.u), (2, Spin.u), (1, Spin.u), (0, Spin.u)}, 0.789)
}.Select(o => (o.Item1.ToSpinOrbitals(), o.Item2);

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(reference, clusterOperator);

// Convert the wavefunction indexed by spin-orbitals to one indexed
// by integers
var wavefunctionInteger = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

Wir stellen auch eine Hilfsfunktion bereit, die alle Spin-konversing-Cluster Operatoren auflistet, die nur besetzte Spin-Orbitals und begeistern nur auf nicht belegte Spin-Orbitals-Elemente zurücksetzen.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Generate all spin-conversing excitations from spin-orbitals 
// occupied by the reference state to virtual orbitals.
var generatedExcitations = reference.CreateAllUCCSDSingletExcitations(nOrbitals: 3).Excitations;

// This is the list of expected spin-consvering excitations
var expectedExcitations = new[]
{
    new []{ (0, Spin.u), (1,Spin.u)},
    new []{ (2, Spin.u), (1,Spin.u)},
    new []{ (0, Spin.d), (2,Spin.d)},
    new []{ (1, Spin.d), (2,Spin.d)},
    new []{ (0, Spin.u), (0, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.u), (1, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)},
    new []{ (1, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)}
}.Select(o => new IndexOrderedSequence<SpinOrbital>(o.ToLadderSequence()));

// The following two assertions are true, and verify that the generated 
// excitations exactly match the expected excitations.
var bool0 = generatedExcitations.Keys.All(expectedExcitations.Contains);
var bool1 = generatedExcitations.Count() == expectedExcitations.Count();
```
