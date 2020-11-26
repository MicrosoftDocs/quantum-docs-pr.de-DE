---
uid: Microsoft.Quantum.Arrays.Unique
title: Unique-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: 7964d5d41eb68cb05f9414164d69496c1f76eb08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220007"
---
# <a name="unique-function"></a>Unique-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt ein neues Array zurück, das keine gleich benachbarten Elemente aufweist.

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a>BESCHREIBUNG

Bei einem bestimmten Array von Elementen und einer Funktion zum Testen der Gleichheit gibt diese Funktion ein neues Array zurück, in dem die relative Reihenfolge der Elemente beibehalten wird. alle angrenzenden Elemente, die gleich sind, werden jedoch nur nach einem einzelnen Element gefiltert.

## <a name="input"></a>Eingabe

### <a name="equal--tt---bool"></a>gleich: ('t, 't)-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion, die zwei-Elemente als vergleicht, die `a` als gleich betrachtet werden, `b` wenn gleich `equal(a, b)` ist `true` .


### <a name="array--t"></a>Array: 't []

Das Array, das nach eindeutigen Elementen gefiltert werden soll.



## <a name="output--t"></a>Ausgabe: 't []

Array ohne gleich angrenzende Elemente.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `array` .

## <a name="remarks"></a>Bemerkungen

Wenn mehrere Elemente gleich sind, jedoch nicht nebeneinander, werden mehrere Vorkommen im Ausgabe Array angezeigt.  Verwenden Sie diese Funktion in Verbindung mit `Sorted` , um ein Array mit Gesamtzahl der eindeutigen Elemente zu erhalten.