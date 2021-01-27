---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLECA
title: Reversetdopleca-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLECA
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d4245437f2b71abb8bf1bbe4db43ae7d2ee23799
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845749"
---
# <a name="reversedopleca-function"></a>Reversetdopleca-Funktion

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt bei einem Vorgang, der eine Little-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Big-Endian-Eingabe annimmt.

```qsharp
function ReversedOpLECA (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Eingabe

### <a name="op--littleendian--unit--is-adj--ctl"></a>OP: [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Der Vorgang, dessen Eingabe umgekehrt werden soll.



## <a name="output--bigendian--unit--is-adj--ctl"></a>Ausgabe: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL

Ein neuer Vorgang, der seine Eingabe als Big-tedian-Register akzeptiert.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. applyreversegdopleca](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLECA)
- [Microsoft. Quantum. Arithmetik. reverldople](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Microsoft. Quantum. Arithmetik. revereindoplea](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Microsoft. Quantum. Arithmetik. revereindoplec](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)