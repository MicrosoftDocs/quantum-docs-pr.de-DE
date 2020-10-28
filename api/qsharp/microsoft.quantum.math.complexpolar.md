---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Complexpolar-benutzerdefinierter Typ
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 0c18c3f02cb036f22a68b6e4b46fd19049dc34cc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701328"
---
# <a name="complexpolar-user-defined-type"></a>Complexpolar-benutzerdefinierter Typ

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paketen [](https://nuget.org/packages/)


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