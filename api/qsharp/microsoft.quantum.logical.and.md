---
uid: Microsoft.Quantum.Logical.And
title: And-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: cc81f650216c4db219a79c4fe89a42447a4e95b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707063"
---
# <a name="and-function"></a>And-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt die boolesche Verbindung von zwei Werten zurück.

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--bool"></a>a: [bool](xref:microsoft.quantum.lang-ref.bool)

Der erste zu berücksichtigende Wert.


### <a name="b--bool"></a>b: [bool](xref:microsoft.quantum.lang-ref.bool)

Der zweite zu berücksichtigende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` nur dann, wenn `a` und gleich `b` sind `true` .

## <a name="remarks"></a>Hinweise

Im Gegensatz zum- `and` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.

Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:

```Q#
let x = a and b;
let x = And(a, b);
```