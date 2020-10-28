---
uid: Microsoft.Quantum.Simulation.PauliBlockEncoding
title: Pauliblockencoding-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliBlockEncoding
qsharp.summary: >-
  Creates a block-encoding unitary for a Hamiltonian.

  The Hamiltonian $H=\sum_{j}\alpha_j P_j$ is described by a sum of Pauli terms $P_j$, each with real coefficient $\alpha_j$.
ms.openlocfilehash: 1426c7cbc257f9263ff45a96738fe798c3679ba1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706674"
---
# <a name="pauliblockencoding-function"></a>Pauliblockencoding-Funktion

Namespace: [Microsoft. Quantum. Simulation](xref:Microsoft.Quantum.Simulation)

Paketen [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Hinweise

Dies wird erreicht, indem der Status $ \ sum_ {j} \sqrt{\ alpha_j/\alpha}\ket{j} $ vorbereitet und die Vorbereitung wieder vorbereitet wird, und das Erstellen einer multiplizierten, einheitlichen <xref:microsoft.quantum.preparation.statepreparationpositivecoefficients> und- <xref:microsoft.quantum.canon.multiplexoperationsfromgenerator> .