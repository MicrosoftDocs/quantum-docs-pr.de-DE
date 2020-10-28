---
uid: Microsoft.Quantum.Arithmetic.CopyMostSignificantBit
title: Copymustsignifiantbit-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CopyMostSignificantBit
qsharp.summary: Copies the most significant bit of a qubit register `from` representing an unsigned integer into the qubit `target`.
ms.openlocfilehash: 02119103fa7b5776f0e1681535115e0773a34c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707338"
---
# <a name="copymostsignificantbit-operation"></a>Copymustsignifiantbit-Vorgang

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Kopiert das signifikanteste Bit eines Qubit-Registers, das `from` eine Ganzzahl ohne Vorzeichen in das Qubit darstellt `target` .

```qsharp
operation CopyMostSignificantBit (from : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit
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