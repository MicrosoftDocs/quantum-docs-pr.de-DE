---
uid: Microsoft.Quantum.Math.Fraction
title: Benutzerdefinierter Bruchteil-Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: a56d28e34938729a8e4ffda5f870e0b6a25be017
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857511"
---
# <a name="fraction-user-defined-type"></a>Benutzerdefinierter Bruchteil-Typ

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt eine rationale Zahl der Form dar `p/q` . "Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="numerator--int"></a>Zähler: [int](xref:microsoft.quantum.lang-ref.int)

Zähler des Bruchteils.
### <a name="denominator--int"></a>Nenner: [int](xref:microsoft.quantum.lang-ref.int)

Nenner des Bruchteils/