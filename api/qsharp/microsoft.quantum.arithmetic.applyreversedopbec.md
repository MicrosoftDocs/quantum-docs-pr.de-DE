---
uid: Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC
title: Applyrevereindopbec-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyReversedOpBEC
qsharp.summary: Applies an operation that takes big-endian input to a register encoding an unsigned integer using little-endian format.
ms.openlocfilehash: 3a5fef3bb4549433540b2a7b5e94d3cd2d527639
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202769"
---
# <a name="applyreversedopbec-operation"></a>Applyrevereindopbec-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Wendet einen Vorgang an, der eine Big-Endian-Eingabe an eine Register Codierung einer Ganzzahl ohne Vorzeichen unter Verwendung des Little-Endian-Formats nimmt.

```qsharp
operation ApplyReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl), register : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Ctl
```


## <a name="input"></a>Eingabe

### <a name="op--bigendian--unit--is-ctl"></a>OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL

Der Vorgang, der auf ein Big-in-Register-Register angewendet wird.


### <a name="register--littleendian"></a>Register: [littleerdian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Ein zu transformierende Little--zu-Ende-Registrierung.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. applyrevereldopbe](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [Microsoft. Quantum. Arithmetik. applyrevereldopbea](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEA)
- [Microsoft. Quantum. Arithmetik. applyreversegdopbeca](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)