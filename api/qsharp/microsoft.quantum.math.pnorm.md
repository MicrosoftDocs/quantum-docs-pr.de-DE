---
uid: Microsoft.Quantum.Math.PNorm
title: Pnorm-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: cea85715e448305486f6d8a6c10e11da56edf3ee
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92722303"
---
# <a name="pnorm-function"></a>Pnorm-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Gibt die `L(p)` Norm eines Vektors von `Double` s zurück.

Das heißt, wenn ein Array $x $ vom Typ ist `Double[]` , wird der $p $-Norm $ \| x \| \_ p = (\ sum_ {j} | x_j | ^ {p}) ^ {1/p} $ zurückgegeben.

```qsharp
function PNorm (p : Double, array : Double[]) : Double
```


## <a name="input"></a>Eingabe

### <a name="p--double"></a>p: [Double](xref:microsoft.quantum.lang-ref.double)

Der Exponent $p $ in der $p $-Norm.


### <a name="array--double"></a>Array: [Double](xref:microsoft.quantum.lang-ref.double)[]





## <a name="output--double"></a>Ausgabe: [Double](xref:microsoft.quantum.lang-ref.double)

Der $p $-Norm $ \| x \| _P $.