---
uid: Microsoft.Quantum.Math.ComplexPolar
title: Complexpolar-benutzerdefinierter Typ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ComplexPolar
qsharp.summary: >-
  Represents a complex number in polar form.

  The polar representation of a complex number is $c=r e^{i t}$.
ms.openlocfilehash: 174e75b82a3ee740cd4d07e5bcd091de65bbc6b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847349"
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