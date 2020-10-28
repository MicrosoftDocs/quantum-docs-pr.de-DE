---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Lookupfunction-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: c929054b96ee499db896cacf0e3ae4da6f6c4b98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705911"
---
# <a name="lookupfunction-function"></a>Lookupfunction-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Gibt bei Angabe eines Arrays eine Funktion zurück, die Elemente dieses Arrays zurückgibt.

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't []

Das Array, das als Suchfunktion dargestellt werden soll.



## <a name="output--int---t"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int) -> 't

Eine Funktion `f` , die ist `f(idx) == f[idx]` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Elemente des Arrays, das als Suchfunktion dargestellt wird.

## <a name="remarks"></a>Hinweise

Diese Funktion ist besonders nützlich für die Interaktion mit Funktionen und Vorgängen, die `Int -> 'T` Funktionen als Argumente annehmen. Dies ist beispielsweise in der Generator-Darstellungs Bibliothek üblich, in der Funktionen verwendet werden, um zu vermeiden, dass ein gesamtes Array im Arbeitsspeicher aufgezeichnet werden muss.