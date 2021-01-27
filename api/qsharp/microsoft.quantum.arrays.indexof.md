---
uid: Microsoft.Quantum.Arrays.IndexOf
title: IndexOf-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848524"
---
# <a name="indexof-function"></a>IndexOf-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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



## <a name="example"></a>Beispiel

Angenommen, `IsEven : Int -> Bool` Es handelt sich um eine Funktion, die nur dann zurückgibt, wenn `true` Ihre Eingabe gerade ist. Anschließend kann dies mit verwendet werden, `IndexOf` um das erste gerade Element in einem Array zu finden:

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```