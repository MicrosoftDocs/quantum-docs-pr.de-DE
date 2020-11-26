---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Assertmugesignifiantbit-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 41381455d1a96970647f887e038f7dff3a4eb204
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223781"
---
# <a name="assertmostsignificantbit-operation"></a>Assertmugesignifiantbit-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bestätigt, dass das signifikanteste Qubit eines Qubit-Registers, das eine Ganzzahl ohne Vorzeichen darstellt, in einem bestimmten Zustand ist.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Eingabe

### <a name="value--__invalidresult__"></a>Wert: __ungültig <Result>__

Der Wert des höchsten zu überprüfenden Bits.


### <a name="number--littleendian"></a>Zahl: [littleenumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ganze Zahl ohne Vorzeichen, bei der das höchste Bit aktiviert ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Bemerkungen

Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. intrinsisch. Assert](xref:Microsoft.Quantum.Intrinsic.Assert)