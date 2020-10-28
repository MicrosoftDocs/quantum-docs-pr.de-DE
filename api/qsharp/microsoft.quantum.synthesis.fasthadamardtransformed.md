---
uid: Microsoft.Quantum.Synthesis.FastHadamardTransformed
title: Fasthadamardtransformierte-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: FastHadamardTransformed
qsharp.summary: Computes Hadamard transform of a Boolean function in {-1,1} encoding using Yates's method
ms.openlocfilehash: 2b84e92d08a3baad2552780cae91f447830cac82
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92725187"
---
# <a name="fasthadamardtransformed-function"></a>Fasthadamardtransformierte-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paketen [](https://nuget.org/packages/)


Berechnet die Hadamard-Transformation einer booleschen Funktion in {-1,1} der Codierung mithilfe der Yates-Methode.

```qsharp
function FastHadamardTransformed (func : Int[]) : Int[]
```


## <a name="input"></a>Eingabe

### <a name="func--int"></a>Func: [int](xref:microsoft.quantum.lang-ref.int)[]

Wahrheitstabelle in der {-1,1} Codierung



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)[]

Die Spektral Koeffizienten der Funktion