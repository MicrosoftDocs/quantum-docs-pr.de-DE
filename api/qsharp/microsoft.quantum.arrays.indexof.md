---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705978"
---
# <a name="indexof-function"></a>IndexOf-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt den ersten Index des ersten Elements in einem Array zurück, das ein angegebenes Prädikat erfüllt. Wenn kein solches Element vorhanden ist, wird-1 zurückgegeben.

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a>Eingabe

### <a name="predicate--t---bool"></a>Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Prädikat Funktion, die für Elemente des Arrays fungiert.


### <a name="arr--t"></a>Arr: 't []

Ein Array, das mithilfe des angegebenen Prädikats durchsucht werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Entweder der kleinste Index `idx` , der `predicate(arr[idx])` true ist, oder-1, wenn kein solches Element vorhanden ist.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

