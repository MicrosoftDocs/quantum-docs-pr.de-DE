---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Pauliblockencoding-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 2e37b40c60d19aa747114de988dddc19f0d7c50b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848004"
---
# <a name="pauliblockencoding-function"></a>Pauliblockencoding-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt eine einheitliche Block Codierung für ein hamiltonan.

Die hamiltonan $H = \ sum_ {j} \ alpha_j P_j $ wird durch eine Summe von Pauli-Begriffen $P _J $, jeweils mit dem tatsächlichen Koeffizienten $ \ alpha_j $, beschrieben.

```qsharp
function PauliBlockEncoding (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Double, Microsoft.Quantum.Simulation.BlockEncodingReflection)
```


## <a name="input"></a>Eingabe

### <a name="generatorsystem--generatorsystem"></a>Generatorsystem: [Generatorsystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Eine `GeneratorSystem` , die $H $ als Summe von Pauli-Begriffen beschreibt.



## <a name="output--doubleblockencodingreflection"></a>Ausgabe: ([Double](xref:microsoft.quantum.lang-ref.double),[blockencodingreflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection))

## <a name="first-parameter"></a>Erster Parameter

Die einnorm der Koeffizienten $ \alpha = \ sum_ {j} | \ alpha_j | $.

## <a name="second-parameter"></a>Zweiter Parameter

Ein `BlockEncodingReflection` einheitlicher $U $ der hamiltonan $H $. Da diese einheitliche $U ^ 2 = I $ erfüllt, ist Sie auch eine Reflektion.

## <a name="remarks"></a>Bemerkungen

Dies wird erreicht, indem der Status $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ vorbereitet und die Vorbereitung wieder vorbereitet wird, und das Erstellen einer multiplizierten, einheitlichen <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> und- <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .