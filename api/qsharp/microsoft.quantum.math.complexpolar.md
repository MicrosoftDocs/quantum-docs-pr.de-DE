---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Complexpolar-benutzerdefinierter Typ
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: a4f3a7b6ffa73271d7ac9674d8c718f6f09c0291
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210980"
---
# <a name="complexpolar-user-defined-type"></a>Complexpolar-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Stellt eine komplexe Zahl in Polar Form dar.

Die Polar Darstellung einer komplexen Zahl ist $c = r e ^ {i t} $.

```qsharp

newtype ComplexPolar = (Magnitude : Double, Argument : Double);
```



## <a name="named-items"></a>Benannte Elemente

### <a name="magnitude--double"></a>Größe: [Double](xref:microsoft.quantum.lang-ref.double)

Der absolute Wert $r \ge $0 von $c $.
### <a name="argument--double"></a>Argument: [Double](xref:microsoft.quantum.lang-ref.double)

Die Phase $t \in \mathbb R $ von $c $.