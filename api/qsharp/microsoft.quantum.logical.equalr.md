---
uid: Microsoft.Quantum.Logical.EqualR
title: Equalr-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701495"
---
# <a name="equalr-function"></a>Equalr-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--__invalidresult__"></a>a: __ungültig <Result>__

Der erste zu vergleichende Wert.


### <a name="b--__invalidresult__"></a>b: __ungültig <Result>__

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn gleich ist `b` .

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```