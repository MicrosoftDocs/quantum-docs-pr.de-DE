---
uid: Microsoft.Quantum.Logical.Conditioned
title: Bedingte Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817287"
---
# <a name="conditioned-function"></a>Bedingte Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="remarks"></a>Bemerkungen

Im Gegensatz zum- `?|` Operator ist diese Funktion nicht kurz, sodass beide Eingaben vollständig ausgewertet werden.

Bis zu einem kurzen Schluss Verhalten sind die folgenden äquivalent:

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```