---
uid: Microsoft.Quantum.Math.BigFraction
title: Bigbruchteil-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BigFraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1c9b9e350c4fa3664b2c66da05149005b1170ec3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211082"
---
# <a name="bigfraction-user-defined-type"></a>Bigbruchteil-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt eine rationale Zahl der Form dar `p/q` . "Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.

```qsharp

newtype BigFraction = (Numerator : BigInt, Denominator : BigInt);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="numerator--bigint"></a>Zähler: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Zähler des Bruchteils.
### <a name="denominator--bigint"></a>Nenner: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Nenner des Bruchteils/