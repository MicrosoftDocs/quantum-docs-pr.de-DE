---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Benutzerdefinierter bigEndian-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 64590606f7c36e0598a9d29c5c6a7ba6d6451aa1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707434"
---
# <a name="bigendian-user-defined-type"></a>Benutzerdefinierter bigEndian-Typ

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paketen [](https://nuget.org/packages/)


Registrieren, das eine Ganzzahl ohne Vorzeichen in Big-d-Reihenfolge codiert. Das Qubit mit Index `0` codiert das höchste Bit einer Ganzzahl ohne Vorzeichen.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>Hinweise

Wir kürzen Sie `BigEndian` als `BE` in der-Dokumentation.