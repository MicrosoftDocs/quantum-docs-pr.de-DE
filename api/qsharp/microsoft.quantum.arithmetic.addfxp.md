---
uid: Microsoft.Quantum.Arithmetic.AddFxP
title: Addfxp-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AddFxP
qsharp.summary: Adds two fixed-point numbers stored in quantum registers.
ms.openlocfilehash: cf1f1379b7e1c32aefb0fccb55f4d13c95c78d8f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707663"
---
# <a name="addfxp-operation"></a>Addfxp-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Addiert zwei in quantenregistern gespeicherte Fixed-Point-Nummern.

```qsharp
operation AddFxP (fp1 : Microsoft.Quantum.Arithmetic.FixedPoint, fp2 : Microsoft.Quantum.Arithmetic.FixedPoint) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Bei Angabe von zwei fixpointregistern in den Zuständen $ \ket{f_1} $ und $ \ket{f_2} $ wird der Vorgang "$ \ket{f_1} \ket{f_2} \mapsto \ket{f_1} \ket{f_1 + f_2} $" durchführt.

## <a name="input"></a>Eingabe

### <a name="fp1--fixedpoint"></a>Fp1: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Erste festpunktzahl


### <a name="fp2--fixedpoint"></a>FP2: [FixedPoint](xref:Microsoft.Quantum.Arithmetic.FixedPoint)

Die zweite festpunktzahl wird aktualisiert und enthält nun die Summe der beiden Eingaben.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Die aktuelle-Implementierung erfordert, dass die zwei fest Komma Zahlen die gleiche Punktposition aufweisen, die vom unbedeutenden Bit gezählt wird, d. h. $n _I $ und $p, dass _I $ gleich sein muss.