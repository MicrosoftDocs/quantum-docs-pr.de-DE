---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentI
title: Continuedfractionconvergenti-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentI
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: 2322e005a5afb73d9719eb65d9ebf50740f1c9fc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723185"
---
# <a name="continuedfractionconvergenti-function"></a>Continuedfractionconvergenti-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`

```qsharp
function ContinuedFractionConvergentI (fraction : Microsoft.Quantum.Math.Fraction, denominatorBound : Int) : Microsoft.Quantum.Math.Fraction
```


## <a name="input"></a>Eingabe

### <a name="fraction--fraction"></a>Bruchteil: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)




### <a name="denominatorbound--int"></a>Nenner-gebunden: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--fraction"></a>Ausgabe: [Bruchteil](xref:Microsoft.Quantum.Math.Fraction)

Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`