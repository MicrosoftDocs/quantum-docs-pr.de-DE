---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: Lookupfunction-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: 22b56bb7e9f03ebc5b2225efb2e6450d56022664
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845701"
---
# <a name="lookupfunction-function"></a>Lookupfunction-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Diese Funktion ist besonders nützlich für die Interaktion mit Funktionen und Vorgängen, die `Int -> 'T` Funktionen als Argumente annehmen. Dies ist beispielsweise in der Generator-Darstellungs Bibliothek üblich, in der Funktionen verwendet werden, um zu vermeiden, dass ein gesamtes Array im Arbeitsspeicher aufgezeichnet werden muss.