---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Copymustsignifiantbit-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 609e937a03bebf45aa9398225bd1b7e2b717807a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843268"
---
# <a name="copymostsignificantbit-operation"></a>Copymustsignifiantbit-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Kopiert das signifikanteste Bit eines Qubit-Registers, das `from` eine Ganzzahl ohne Vorzeichen in das Qubit darstellt `target` .

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj
```


## <a name="input"></a>Eingabe

### <a name="from--littleendian"></a>von: [littleddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Die Ganzzahl ohne Vorzeichen, von der das höchste Bit kopiert wird.
die Ganzzahl wird im Little-Endian-Format codiert.


### <a name="target--qubit"></a>Ziel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Das Qubit, in dem das höchste Bit kopiert wird. Die Bitcodierung erfolgt auf Berechnungsbasis.



## <a name="output--unit"></a>Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arithmetik. Little-Dian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)