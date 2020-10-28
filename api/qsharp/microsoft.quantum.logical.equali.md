---
uid: Microsoft.Quantum.Logical.EqualI
title: Equali-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 6b805e76217e033cb0135cf85bd8f37a3eb8636a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701502"
---
# <a name="equali-function"></a>Equali-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Der erste zu vergleichende Wert.


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn gleich ist `b` .

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```