---
uid: Microsoft.Quantum.Arrays.Reversed
title: Umgekehrte Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 270f15c1d10b4397e258c750876095efc2b8e951
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220432"
---
# <a name="reversed-function"></a>Umgekehrte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellen Sie ein Array, das dieselben Elemente wie ein Eingabe Array, jedoch in umgekehrter Reihenfolge enthält.

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't []

Ein Array, dessen Elemente in umgekehrter Reihenfolge kopiert werden sollen.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array, das die Elemente enthält `array[Length(array) - 1]` . `array[0]`.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Arrayelemente.