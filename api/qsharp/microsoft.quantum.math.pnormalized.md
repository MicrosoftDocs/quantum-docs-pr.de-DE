---
uid: Microsoft.Quantum.Math.PNormalized
title: Pnormalized-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNormalized
qsharp.summary: >-
  Normalizes a vector of `Double`s in the `L(p)` norm.

  That is, given an array $x$ of type `Double[]`, this returns an array where all elements are divided by the $p$-norm $\|x\|_p$.
ms.openlocfilehash: ea6a88d07d3b246f666b793f0b10ab6598ea4ff6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854845"
---
# <a name="pnormalized-function"></a>Pnormalized-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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