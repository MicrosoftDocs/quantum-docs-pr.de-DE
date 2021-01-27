---
uid: Microsoft.Quantum.Arithmetic.CompareGreaterThanFxP
title: Comparegreaterthanf XP-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareGreaterThanFxP
qsharp.summary: Compares two fixed-point numbers stored in quantum registers, and controls a flip on the result.
ms.openlocfilehash: f49c713c8a1e8a6451f2c54fa59a72f00bfbb4c4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843319"
---
# <a name="comparegreaterthanfxp-operation"></a>Comparegreaterthanf XP-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Vergleicht zwei in quantenregistern gespeicherte Fixed-Point-Nummern und steuert einen Flip-Wert für das Ergebnis.

```qsharp
operation CompareGreaterThanFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint, result : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="fp1--fixedpoint"></a>Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die erste zu vergleichende fixpunktzahl.


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die zweite zu vergleichende Festkomma Zahl.


### <a name="result--qubit"></a>Ergebnis: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Ergebnis des Vergleichs. Wird gekippt, wenn `fp1 > fp2` .



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Die aktuelle Implementierung erfordert, dass die zwei Festkomma Zahlen dieselbe Punktposition und dieselbe Anzahl von Qubits aufweisen.