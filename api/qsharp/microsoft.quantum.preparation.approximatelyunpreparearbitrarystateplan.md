---
uid: Microsoft.Quantum.Preparation.ApproximatelyUnprepareArbitraryStatePlan
title: Ungefäatelyunpreparearbitrarystateplan-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: ApproximatelyUnprepareArbitraryStatePlan
qsharp.summary: Implementation step of arbitrary state preparation procedure.
ms.openlocfilehash: 2aab8b7a21ded729e90695c82709901bfacc18e7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226501"
---
# <a name="approximatelyunpreparearbitrarystateplan-function"></a>Ungefäatelyunpreparearbitrarystateplan-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementierungs Schritt eines willkürlichen Zustands Vorbereitungs Verfahrens.

```qsharp
function ApproximatelyUnprepareArbitraryStatePlan (tolerance : Double, coefficients : Microsoft.Quantum.Math.ComplexPolar[], (rngControl : Range, idxTarget : Int)) : (Qubit[] => Unit is Adj + Ctl)[]
```


## <a name="input"></a>Eingabe

### <a name="tolerance--double"></a>Toleranz: [Double](xref:microsoft.quantum.lang-ref.double)




### <a name="coefficients--complexpolar"></a>Koeffizienten: [complexpolar](xref:Microsoft.Quantum.Math.ComplexPolar)[]




### <a name="rngcontrol--range"></a>rngcontrol: [Bereich](xref:microsoft.quantum.lang-ref.range)




### <a name="idxtarget--int"></a>idxtarget: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--qubit--unit--is-adj--ctl"></a>Ausgabe: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL []



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. preparearbitrarystate](xref:Microsoft.Quantum.Preparation.PrepareArbitraryState)
- [Microsoft. Quantum. Canon. multiplexpauli](xref:Microsoft.Quantum.Canon.MultiplexPauli)