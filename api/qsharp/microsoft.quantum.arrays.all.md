---
uid: Microsoft.Quantum.Arrays.All
title: All-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 345c3fb92babd4ae2e54803b6c3b79b3313ef417
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706183"
---
# <a name="all-function"></a>All-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Bei Angabe eines Arrays und eines Prädikats, das für die Elemente des Arrays definiert ist, und überprüft, ob alle Elemente des Arrays dem Prädikat entsprechen.

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Eingabe

### <a name="predicate--t---bool"></a>Prädikat: 't-> [bool](xref:microsoft.quantum.lang-ref.bool)

Eine Funktion von `'T` zu `Bool` , die zum Überprüfen von Elementen verwendet wird.


### <a name="array--t"></a>Array: 't []

Ein Array von-Elementen `'T` .



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

Ein `Bool` Wert der and-Funktion des Prädikats, das auf alle-Elemente angewendet wird.

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der `array` Elemente.

## <a name="remarks"></a>Hinweise

Die-Funktion ist für generische Typen definiert, d. h., wenn ein Array `'T[]` und eine Funktion vorhanden sind, `predicate: 'T -> Bool` können wir einen Wert entwickeln, `Bool` der angibt, ob alle Elemente erfüllen `predicate` .