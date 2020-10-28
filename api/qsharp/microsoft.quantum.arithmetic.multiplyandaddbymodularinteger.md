---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger
title: Multiplyandaddbymodularinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddByModularInteger
qsharp.summary: Performs a modular multiply-and-add by integer constants on a qubit register.
ms.openlocfilehash: 3f85f6aaea1d6f8095709c6f387322df7a5e047c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706402"
---
# <a name="multiplyandaddbymodularinteger-operation"></a>Multiplyandaddbymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Führt einen modularen Multiplikations-und-Add by integer-Konstanten für ein Qubit-Register aus.

```qsharp
operation MultiplyAndAddByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, summand : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Implementiert die Zuordnung $ $ \begin{align} \ket{x} \ket{b} \mapsto \ket{x} \ket{(b + a \cdot x) \operatschmue{mod} N} \end{align} $ $ für einen angegebenen Modulo $N $, Konstanten Multiplikator $a $ und sumand $y $.

## <a name="input"></a>Eingabe

### <a name="constmultiplier--int"></a>constmultiplikator: [int](xref:microsoft.quantum.lang-ref.int)

Eine ganze Zahl $a $, die jeder Basis Zustands Bezeichnung hinzugefügt werden soll.


### <a name="modulus--int"></a>Modulo: [int](xref:microsoft.quantum.lang-ref.int)

Der Modulo $N $, bei dem Addition und Multiplikation in Bezug auf übernommen werden.


### <a name="multiplier--littleendian"></a>Multiplikator: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, deren Wert jeder Basis Zustands Bezeichnung von hinzugefügt werden soll `summand` .


### <a name="summand--littleendian"></a>sumand: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein Quantum-Register, das eine Ganzzahl ohne Vorzeichen darstellt, die als Ziel für diesen Vorgang verwendet werden soll.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

- Ein Leit Diagramm und eine Erläuterung finden Sie in Abbildung 6 auf [Seite 7 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=7)
- Dieser Vorgang entspricht cmult (a) mod (N) in [arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. multiplyandaddphasebymodularinteger](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger)