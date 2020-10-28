---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Assertmugesignifiantbit-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707450"
---
# <a name="assertmostsignificantbit-operation"></a>Assertmugesignifiantbit-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Bestätigt, dass das signifikanteste Qubit eines Qubit-Registers, das eine Ganzzahl ohne Vorzeichen darstellt, in einem bestimmten Zustand ist.

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a>Eingabe

### <a name="value--__invalidresult__"></a>Wert: __ungültig <Result>__

Der Wert des höchsten zu überprüfenden Bits.


### <a name="number--littleendian"></a>Zahl: [littleenumdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ganze Zahl ohne Vorzeichen, bei der das höchste Bit aktiviert ist.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Hinweise

Von der kontrollierten Version dieses Vorgangs werden Steuerelemente ignoriert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. intrinsisch. Assert](xref:Microsoft.Quantum.Intrinsic.Assert)