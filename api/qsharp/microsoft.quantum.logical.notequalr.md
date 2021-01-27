---
uid: Microsoft.Quantum.Logical.NotEqualR
title: Notequalr-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 39601396a75d8c1b9193d4b8f34fa05466beff06
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848499"
---
# <a name="notequalr-function"></a>Notequalr-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt nur dann true zurück, wenn zwei Eingaben nicht gleich sind.

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--__invalidresult__"></a>a: __ungültig <Result>__

Der erste zu vergleichende Wert.


### <a name="b--__invalidresult__"></a>b: __ungültig <Result>__

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn nicht gleich ist `b` .

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
let cond = a != b;
let cond = NotEqualR(a, b);
```