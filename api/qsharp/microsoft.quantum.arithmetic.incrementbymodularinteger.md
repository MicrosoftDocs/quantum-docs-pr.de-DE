---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Incrementbymodularinteger-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: 271033b32b0de6cf600dca82126dab19c2bb4f5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707263"
---
# <a name="incrementbymodularinteger-operation"></a>Incrementbymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Führt ein modulares Inkrement für ein Qubit-Register durch eine ganzzahlige Konstante aus.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>BESCHREIBUNG

Geben Sie `increment` $a $ an, indem Sie `modulus` $N $ und Integer in `target` durch $y $ codiert haben.
Anschließend führt der Vorgang die folgende Transformation aus: \begin{align} \ket{y} \mapsto \ket{(y + a) \operatschmue{mod} N} \end{align} ganze Zahlen werden im Little-Endian-Format codiert.

## <a name="input"></a>Eingabe

### <a name="increment--int"></a>Inkrement: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahliges Inkrement $a $, das $y $ hinzugefügt werden soll.


### <a name="modulus--int"></a>Modulo: [int](xref:microsoft.quantum.lang-ref.int)

Ganzzahliger $N $, $y + a $.


### <a name="target--littleendian"></a>Ziel: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ganzzahliger $y $ im `LittleEndian` Format, dem `increment` $a $ hinzugefügt wird.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Geht davon aus, dass der Anfangswert von Target kleiner als $N $ und die Inkrement-$a $ kleiner als $N $ ist.
Beachten Sie, dass <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> denselben Vorgang in der `PhaseLittleEndian` Basis implementiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. incrementphasebymodularinteger](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)