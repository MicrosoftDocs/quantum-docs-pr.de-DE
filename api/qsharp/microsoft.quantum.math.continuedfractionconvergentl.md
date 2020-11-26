---
uid: Microsoft.Quantum.Math.ContinuedFractionConvergentL
title: Continuedfractionconvergentl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ContinuedFractionConvergentL
qsharp.summary: Finds the continued fraction convergent closest to `fraction` with the denominator less or equal to `denominatorBound`
ms.openlocfilehash: c10fcbbe63d3d4c7d6c56196768c1062be1ca350
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210929"
---
# <a name="continuedfractionconvergentl-function"></a>Continuedfractionconvergentl-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Sucht den fortgesetzten Bruchteil konvergent, der sich am nächsten befindet, wenn `fraction` der Nenner kleiner oder gleich ist. `denominatorBound`

```qsharp
function ContinuedFractionConvergentL (fraction : Microsoft.Quantum.Math.BigFraction, denominatorBound : BigInt) : Microsoft.Quantum.Math.BigFraction
```


## <a name="input"></a>Eingabe

### <a name="fraction--bigfraction"></a>Bruchteil: [bigbruchzahl](xref:Microsoft.Quantum.Math.BigFraction)




### <a name="denominatorbound--bigint"></a>Nenner-gebunden: [bigint](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigfraction"></a>Ausgabe: [bigbruch](xref:Microsoft.Quantum.Math.BigFraction)

Fortgesetzter Bruchteil am nächsten, wenn `fraction` der Nenner kleiner oder gleich `denominatorBound`