---
uid: Microsoft.Quantum.Arithmetic.LittleEndian
title: Benutzerdefinierter Typ "littleenddian"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: LittleEndian
qsharp.summary: Register that encodes an unsigned integer in little-endian order. The qubit with index `0` encodes the lowest bit of an unsigned integer.
ms.openlocfilehash: 2a00e499bf59e6d22a774706331737461e8e95e1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222778"
---
# <a name="littleendian-user-defined-type"></a>Benutzerdefinierter Typ "littleenddian"

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Registrieren, das eine Ganzzahl ohne Vorzeichen in Little-in-der-Reihenfolge codiert. Das Qubit mit Index `0` codiert das niedrigste Bit einer Ganzzahl ohne Vorzeichen.

```qsharp

newtype LittleEndian = (Qubit[]);
```



## <a name="remarks"></a>Bemerkungen

Wir kürzen Sie `LittleEndian` als `LE` in der-Dokumentation.