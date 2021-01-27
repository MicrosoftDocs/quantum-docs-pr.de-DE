---
uid: Microsoft.Quantum.Logical.Or
title: Or-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848465"
---
# <a name="or-function"></a>Or-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die boolesche Disjunktion von zwei Werten zurück.

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

Der erste zu berücksichtigende Wert.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

Der zweite zu berücksichtigende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` nur dann, wenn entweder `a` oder `b` ist `true` .

## <a name="remarks"></a>Bemerkungen

Im Gegensatz zum- `or` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.

Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:

```qsharp
let x = a or b;
let x = Or(a, b);
```