---
uid: Microsoft.Quantum.Logical.NotEqualB
title: Notequalb-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 9f362b9e08f8a798bf7f7d9c323fee6576dccd9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814420"
---
# <a name="notequalb-function"></a>Notequalb-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
let cond = a != b;
let cond = NotEqualB(a, b);
```