---
uid: Microsoft.Quantum.Math.BigFraction
title: Bigbruchteil-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a8daa54947097b95040a2dfa7a4d1b90bfaff856
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723213"
---
# <a name="bigfraction-user-defined-type"></a>Bigbruchteil-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Stellt eine rationale Zahl der Form dar `p/q` . "Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="numerator--bigint"></a>Zähler: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Zähler des Bruchteils.
### <a name="denominator--bigint"></a>Nenner: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Nenner des Bruchteils/