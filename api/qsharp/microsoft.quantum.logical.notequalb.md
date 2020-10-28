---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Notequalb-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: d5a9819bf3baa7c914487277fef308abbc8d25bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701411"
---
# <a name="notequalb-function"></a>Notequalb-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

Der erste zu vergleichende Wert.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn nicht gleich ist `b` .

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```