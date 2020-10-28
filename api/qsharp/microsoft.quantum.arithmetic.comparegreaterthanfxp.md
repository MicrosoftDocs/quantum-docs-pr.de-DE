---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Comparegreaterthanf XP-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: bd3bcedd7a4a81fc600f7f4b6bdf1d2a797abbd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707394"
---
# <a name="comparegreaterthanfxp-operation"></a>Comparegreaterthanf XP-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Vergleicht zwei in quantenregistern gespeicherte Fixed-Point-Nummern und steuert einen Flip-Wert für das Ergebnis.

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit
```


## <a name="input"></a>Eingabe

### <a name="fp1--fixedpoint"></a>Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die erste zu vergleichende fixpunktzahl.


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die zweite zu vergleichende Festkomma Zahl.


### <a name="result--qubit"></a>Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ergebnis des Vergleichs. Wird gekippt, wenn `fp1 > fp2` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Die aktuelle Implementierung erfordert, dass die zwei Festkomma Zahlen dieselbe Punktposition und dieselbe Anzahl von Qubits aufweisen.