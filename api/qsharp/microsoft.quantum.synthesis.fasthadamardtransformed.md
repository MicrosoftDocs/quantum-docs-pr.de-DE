---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Fasthadamardtransformierte-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 3e48701f22ddf154721355866e15a85fca0bc7df
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203092"
---
# <a name="fasthadamardtransformed-function"></a>Fasthadamardtransformierte-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet die Hadamard-Transformation einer booleschen Funktion in {-1,1} der Codierung mithilfe der Yates-Methode.

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="func--int"></a>Func: [int](xref:microsoft.quantum.lang-ref.int)[]

Wahrheitstabelle in der {-1,1} Codierung



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Die Spektral Koeffizienten der Funktion