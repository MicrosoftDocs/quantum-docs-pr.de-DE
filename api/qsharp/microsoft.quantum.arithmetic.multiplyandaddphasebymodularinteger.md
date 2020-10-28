---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Multiplyandaddphasebymodularinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: be7df50f040697329c2fe8bbc319c8cebb8b2687
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706399"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a>Multiplyandaddphasebymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Das gleiche wie bei multiplyandaddbymodularinteger, jedoch wird davon ausgegangen, dass die Summen-und-Werte Ganzzahlen in QFT codieren.

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="constmultiplier--int"></a>constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl $a $, die jeder Basis Zustands Bezeichnung hinzugefügt werden soll.


### <a name="modulus--int"></a>Modulo: [int](xref:microsoft.quantum.lang-ref.int)

Der Modulo $N $, bei dem Addition und Multiplikation in Bezug auf übernommen werden.


### <a name="multiplier--littleendian"></a>Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, deren Wert jeder Basis Zustands Bezeichnung von hinzugefügt werden soll `summand` .


### <a name="phasesummand--phaselittleendian"></a>phasesummand: [phaselittleendian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, die als Ziel für diesen Vorgang verwendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Geht davon aus, dass `phaseSummand` das höchste Bit auf 0 festgelegt ist.
Außerdem wird davon ausgegangen, dass der Wert von `phaseSummand` kleiner als $N $ ist.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. multiplyandaddbymodularinteger](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)