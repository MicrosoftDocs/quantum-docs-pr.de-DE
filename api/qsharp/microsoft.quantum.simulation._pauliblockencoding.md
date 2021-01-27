---
uid: Microsoft.Quantum.Simulation._PauliBlockEncoding
title: _PauliBlockEncoding-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: c27ef1a6b7cd7c84defe2a783e9fb1610e52d1e7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851064"
---
# <a name="_pauliblockencoding-function"></a>_PauliBlockEncoding-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt eine einheitliche Block Codierung für ein hamiltonan.

Die hamiltonan $H = \ sum_ {j} \ alpha_j P_j $ wird durch eine Summe von Pauli-Begriffen $P _J $, jeweils mit dem tatsächlichen Koeffizienten $ \ alpha_j $, beschrieben.

```qsharp
function _PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem, statePrepUnitary : (Double[] -> (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)), multiplexer : ((Int, (Int -> (Qubit[] => Unit is Adj + Ctl))) -> ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl))) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Eingabe

### <a name="generatorsystem--generatorsystem"></a>Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Eine `GeneratorSystem` , die $H $ als Summe von Pauli-Begriffen beschreibt.


### <a name="stateprepunitary--double---littleendian--unit--is-adj--ctl"></a>stateprepeinheitlicher: [Double](xref:microsoft.quantum.lang-ref.double)[]-> [littleeindian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein einheitlicher Vorgang $V $, der die einheitliche $V _J $ gesteuert für Index $ \ket{j} $ anwendet, wenn eine Funktion $f: j\rightarrow V_j $.


### <a name="multiplexer--intint---qubit--unit--is-adj--ctl---littleendianqubit--unit--is-adj--ctl"></a>Multiplexer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL)-> ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL





## <a name="output--doubleblockencodingreflection"></a>Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Erster Parameter

Die einnorm der Koeffizienten $ \alpha = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Zweiter Parameter

Ein `BlockEncodingReflection` einheitlicher $U $ der hamiltonan $U $. Da diese einheitliche $U ^ 2 = I $ erfüllt, ist Sie auch eine Reflektion.

## <a name="remarks"></a>Bemerkungen

Beispiel Vorgänge für die Vorbereitung und Aufhebung der Vorbereitung des Zustands $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ und das Erstellen einer Multiplikations kontrollierten einheitlich sind <xref:microsoft.quantum.canon.statepreparationpositivecoefficients> und <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .