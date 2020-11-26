---
uid: Microsoft.Quantum.Logical.Or
title: Or-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 7093d908696a8cfda6b5ef648f9dfafcfac97144
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197125"
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

```Q#
let x = a or b;
let x = Or(a, b);
```