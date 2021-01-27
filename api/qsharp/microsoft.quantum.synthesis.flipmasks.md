---
uid: Microsoft.Quantum.Synthesis.FlipMasks
title: Flipmasken-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FlipMasks
qsharp.summary: For every 2-level unitary calculates "flip mask", which denotes qubits which should be inverted before and after applying corresponding 1-qubit gate. For convenience prepends result with 0.
ms.openlocfilehash: ca0ce69b3353379a42cc109cebb32efe4e364825
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859201"
---
# <a name="flipmasks-function"></a>Flipmasken-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Für jede einheitliche 2-Ebene berechnet "Flip Mask", was Qubits angibt, die vor und nach dem Anwenden des entsprechenden 1-Qubit-Gates invertiert werden sollen.
Aus Gründen der praktische Bereitstellung mit 0.

```qsharp
function FlipMasks (decomposition : (Microsoft.Quantum.Math.Complex[][], Int, Int)[], allQubitsMask : Int) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="decomposition--complexintint"></a>Zerlegung: ([Komplex](xref:Microsoft.Quantum.Math.Complex)[] [],[int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []




### <a name="allqubitsmask--int"></a>allqubitsmask: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

