---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Assertmugesignifiantbit-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: b0b52a4ba7492d68896669aeb0b6b550d2f27f64
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843422"
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