---
uid: Microsoft.Quantum.Arithmetic.BigEndian
title: Benutzerdefinierter bigEndian-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndian
qsharp.summary: Register that encodes an unsigned integer in big-endian order. The qubit with index `0` encodes the highest bit of an unsigned integer.
ms.openlocfilehash: 2f6ec9f83ac124ce9b06c278f8fda820c35c23aa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843390"
---
# <a name="bigendian-user-defined-type"></a>Benutzerdefinierter bigEndian-Typ

Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Registrieren, das eine Ganzzahl ohne Vorzeichen in Big-d-Reihenfolge codiert. Das Qubit mit Index `0` codiert das höchste Bit einer Ganzzahl ohne Vorzeichen.

```qsharp

newtype BigEndian = (Qubit[]);
```



## <a name="remarks"></a>Bemerkungen

Wir kürzen Sie `BigEndian` als `BE` in der-Dokumentation.