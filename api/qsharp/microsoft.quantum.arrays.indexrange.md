---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Indexrange-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705962"
---
# <a name="indexrange-function"></a>Indexrange-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt bei Angabe eines Arrays einen Bereich über die Indizes dieses Arrays zurück, der für die Verwendung in einer for-Schleife geeignet ist.

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a>Eingabe

### <a name="array--telement"></a>Array: ' telements []

Ein Array, für das ein Bereich von Indizes zurückgegeben werden soll.



## <a name="output--range"></a>Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)

Ein Bereich über alle Indizes des Arrays.

## <a name="type-parameters"></a>Typparameter

### <a name="telement"></a>' Telements '

Der Typ der Elemente des Arrays.