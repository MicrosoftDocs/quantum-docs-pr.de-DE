---
uid: Microsoft.Quantum.Math.Fraction
title: Benutzerdefinierter Bruchteil-Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 1838bb2b605b109742948ec0633b08ca01baea98
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210674"
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