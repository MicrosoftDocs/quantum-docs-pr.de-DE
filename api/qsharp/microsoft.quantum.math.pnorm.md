---
uid: Microsoft.Quantum.Math.PNorm
title: Pnorm-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: PNorm
qsharp.summary: >-
  Returns the `L(p)` norm of a vector of `Double`s.

  That is, given an array $x$ of type `Double[]`, this returns the $p$-norm $\|x\|\_p= (\sum_{j}|x_j|^{p})^{1/p}$.
ms.openlocfilehash: 6207cca6cda5f9030facd31c327e58bdb9ecbf14
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847654"
---
# <a name="pnorm-function"></a>Pnorm-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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