---
uid: Microsoft.Quantum.Arrays.Reversed
title: Umgekehrte Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 99244195e581dc00db24b938f5aa1c541cd4433a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705802"
---
# <a name="reversed-function"></a>Umgekehrte Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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