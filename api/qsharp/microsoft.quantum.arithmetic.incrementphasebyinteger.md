---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByInteger
title: Incrementphasebyinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: fb67455dadbc7a2f38880581f0e413a747faa8ef
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707247"
---
# <a name="incrementphasebyinteger-operation"></a>Incrementphasebyinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Erhöht mithilfe von Phasen Drehungen ein unsigniertes Quantum-Register durch eine klassische Ganzzahl.

```qsharp
operation IncrementPhaseByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Angenommen, das `target` codiert eine Ganzzahl ohne Vorzeichen $x $ in einer Little-in-codiercodierung und `increment` ist gleich $a $.
Anschließend implementiert dieser Vorgang die einheitliche $ \ket{x} \mapsto \ket{x + a} $, wobei die Addition Modulo $2 ^ n $ ist, wobei $n = \texttt{length (Target!)} $.

## <a name="input"></a>Eingabe

### <a name="increment--int"></a>Inkrement: [int](xref:microsoft.quantum.lang-ref.int)

Die ganze Zahl, um die die `target` inkrementiert wird.


### <a name="target--phaselittleendian"></a>Ziel: [phaselittleenddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Ein Quantum-Register codiert eine Ganzzahl ohne Vorzeichen unter Verwendung der Little-d-Codierung in der Dual (QFT)-Basis.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Beachten Sie, dass wir die Verbindung vereinfacht haben, da das Inkrement eine klassische Konstante und kein Quantum-Register ist.

Ein Leitungs Diagramm und eine Erläuterung finden Sie in der Abbildung auf der [ Seite 6 von arXiv: quant-ph/0008033v1 ](https://arxiv.org/pdf/quant-ph/0008033.pdf#page=6) .

## <a name="references"></a>Referenzen

- [*Thomas G. Draper* , arXiv: quant-ph/0008033](https://arxiv.org/pdf/quant-ph/0008033v1.pdf)

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. incrementbyinteger](xref:Microsoft.Quantum.Arithmetic.IncrementByInteger)