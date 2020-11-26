---
uid: Microsoft.Quantum.Logical.Conditioned
title: Bedingte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198485"
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

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```