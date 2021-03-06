---
uid: Microsoft.Quantum.Arithmetic.IncrementByModularInteger
title: Incrementbymodularinteger-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByModularInteger
qsharp.summary: Performs a modular increment of a qubit register by an integer constant.
ms.openlocfilehash: f5bacef299ab0b3627e757abdcaa798cf9b2e7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846597"
---
# <a name="incrementbymodularinteger-operation"></a>Incrementbymodularinteger-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Führt ein modulares Inkrement für ein Qubit-Register durch eine ganzzahlige Konstante aus.

```qsharp
operation IncrementByModularInteger (increment : Int, modulus : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschreibung

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



## <a name="remarks"></a>Bemerkungen

Geht davon aus, dass der Anfangswert von Target kleiner als $N $ und die Inkrement-$a $ kleiner als $N $ ist.
Beachten Sie, dass <xref:microsoft.quantum.arithmetic.incrementphasebymodularinteger> denselben Vorgang in der `PhaseLittleEndian` Basis implementiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. incrementphasebymodularinteger](xref:Microsoft.Quantum.Arithmetic.IncrementPhaseByModularInteger)