---
uid: Microsoft.Quantum.Logical.Conditioned
title: Bedingte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707055"
---
# <a name="conditioned-function"></a>Bedingte Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt je nach dem Wert einer booleschen Bedingung einen von zwei Werten zurück.

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a>Eingabe

### <a name="condition--bool"></a>Bedingung: [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Bedingung, mit der gesteuert wird, welche Eingaben zurückgegeben werden.


### <a name="iftrue--t"></a>IfTrue: 't

Der Wert, der zurückgegeben werden soll, wenn `condition` ist `true` .


### <a name="iffalse--t"></a>IfFalse: 't

Der Wert, der zurückgegeben werden soll, wenn `condition` ist `false` .



## <a name="output--t"></a>Ausgabe: 't

`ifTrue` , wenn den Wert `condition` `true` hat und `ifFalse` andernfalls.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF



## <a name="remarks"></a>Hinweise

Im Gegensatz zum- `?|` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.

Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```