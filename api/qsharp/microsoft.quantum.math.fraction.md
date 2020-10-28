---
uid: Microsoft.Quantum.Math.Fraction
title: Benutzerdefinierter Bruchteil-Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: Fraction
qsharp.summary: Represents a rational number of the form `p/q`. Integer `p` is the first element of the tuple and `q` is the second element of the tuple.
ms.openlocfilehash: 350d470c374fc8e0a3f4c4a9a68ad8566ab88727
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723661"
---
# <a name="fraction-user-defined-type"></a>Benutzerdefinierter Bruchteil-Typ

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


Stellt eine rationale Zahl der Form dar `p/q` . "Integer" `p` ist das erste Element des Tupels und `q` ist das zweite Element des Tupels.

```qsharp

newtype Fraction = (Numerator : Int, Denominator : Int);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="numerator--int"></a>Zähler: [int](xref:microsoft.quantum.lang-ref.int)

Zähler des Bruchteils.
### <a name="denominator--int"></a>Nenner: [int](xref:microsoft.quantum.lang-ref.int)

Nenner des Bruchteils/