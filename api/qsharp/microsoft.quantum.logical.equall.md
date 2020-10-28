---
uid: Microsoft.Quantum.Logical.EqualL
title: Equall-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f0a2bfa866068746e9c6e249573eb61c0d08c0f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701496"
---
# <a name="equall-function"></a>Equall-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Der erste zu vergleichende Wert.


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn gleich ist `b` .

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```