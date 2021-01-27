---
uid: Microsoft.Quantum.Arrays.IndexRange
title: Indexrange-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 043b56a1ac3cbe5cd59cdd45d3725f301d81a6ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845780"
---
# <a name="indexrange-function"></a>Indexrange-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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

## <a name="example"></a>Beispiel

Die folgenden `for` Schleifen sind äquivalent:

```qsharp
for (idx in IndexRange(array)) { ... }
for (idx in IndexRange(array)) { ... }
```