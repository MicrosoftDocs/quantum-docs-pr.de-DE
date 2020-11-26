---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Addfxp-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: 36a5d585a493f0e6f33f74b1686aaa01cca7ac0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191039"
---
# <a name="addfxp-operation"></a>Addfxp-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Addiert zwei in quantenregistern gespeicherte Fixed-Point-Nummern.

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit is Adj + Ctl
```


## <a name="description"></a>BESCHREIBUNG

Bei Angabe von zwei fixpointregistern in den Zuständen $ \ket{f_1} $ und $ \ket{f_2} $ wird der Vorgang "$ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $" durchführt.

## <a name="input"></a>Eingabe

### <a name="fp1--fixedpoint"></a>Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Erste festpunktzahl


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die zweite festpunktzahl wird aktualisiert und enthält nun die Summe der beiden Eingaben.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Die aktuelle-Implementierung erfordert, dass die zwei fest Komma Zahlen die gleiche Punktposition aufweisen, die vom unbedeutenden Bit gezählt wird, d. h. $n _I $ und $p, dass _I $ gleich sein muss.