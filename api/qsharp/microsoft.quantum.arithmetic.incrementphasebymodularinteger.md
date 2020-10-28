---
uid: Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger
title: Incrementphasebymodularinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementPhaseByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 52309c056a3eae25ffdfbfa848f94bf744c71132
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707234"
---
# <a name="incrementphasebymodularinteger-operation"></a>Incrementphasebymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Führt ein modulares Inkrement für ein Qubit-Register durch eine ganzzahlige Konstante aus.

```qsharp
operation IncrementPhaseByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Geben Sie `increment` $a $ an, indem Sie `modulus` $N $ und Integer in `target` durch $y $ codiert haben.
Anschließend führt der Vorgang die folgende Transformation aus: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatorname{mod} N} \end{align} ganze Zahlen werden im Little-Endian-Format in QFT codiert.

## <a name="input"></a>Eingabe

### <a name="increment--int"></a>Inkrement: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahliges Inkrement $a $, das $y $ hinzugefügt werden soll.


### <a name="modulus--int"></a>Modulo: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahliger $N $, $y + a $.


### <a name="target--phaselittleendian"></a>Ziel: [phaselittleenddian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)

Ganzzahliger $y $ in Phasen codiertem Little-Endian-Format, dem `increment` $a $ hinzugefügt wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Geht davon aus, dass `target` das höchste Bit auf 0 festgelegt ist.
Außerdem wird davon ausgegangen, dass der Wert von Target kleiner als $N $ ist.

Das Verbindungs Diagramm und die Erläuterung finden Sie in Abbildung 5 auf [Seite 5 von arXiv: quant-ph/0205095v3](https://arxiv.org/pdf/quant-ph/0205095v3.pdf#page=5).

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. incrementbymodularinteger](xref:Microsoft.Quantum.Arithmetic.IncrementByModularInteger)