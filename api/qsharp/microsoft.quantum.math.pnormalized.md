---
uid: Microsoft.Quantum.Math.PNormalized
title: Pnormalized-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: 6f9dfebe83f52cbf486cd8e6874d3699f5e6b8ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722289"
---
# <a name="pnormalized-function"></a>Pnormalized-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Normalisiert einen Vektor von `Double` s in der `L(p)` Norm.

Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird ein Array zurückgegeben, in dem alle Elemente durch die $p $-Norm $ \| x _P $ dividiert werden \| .

```qsharp
function PNormalized (p : Double, array : Double[]) : Double[]
```


## <a name="input"></a>Eingabe

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

Der Exponent $p $ in der $p $-Norm.


### <a name="array--double"></a>Array: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)[]

Das Array $x $ normalisiert durch die $p $-Norm $ \| x \| _P $.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Math. pnorm](xref:Microsoft.Quantum.Math.PNorm)