---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Continuedfractionconvergenti-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c5316c13ce499da88c0d5c45b9d8c5e3a8c6162d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853857"
---
# <a name="continuedfractionconvergenti-function"></a>Continuedfractionconvergenti-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a>Eingabe

### <a name="fraction--fraction"></a>Bruchteil: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)




### <a name="denominatorbound--int"></a>Nenner-gebunden: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--fraction"></a>Ausgabe: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)

Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`