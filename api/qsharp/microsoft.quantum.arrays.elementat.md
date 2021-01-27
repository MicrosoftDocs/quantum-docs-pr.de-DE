---
uid: Microsoft.Quantum.Arrays.ElementAt
title: ElementAt-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementAt
qsharp.summary: Returns the at the given index of an array.
ms.openlocfilehash: 2d31c62a4a5ba3b273e7440b5dfe4482b47e3a8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842802"
---
# <a name="elementat-function"></a>ElementAt-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt den am angegebenen Index eines Arrays zurück.

```qsharp
function ElementAt<'T> (index : Int, array : 'T[]) : 'T
```


## <a name="input"></a>Eingabe

### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)

Index des Elements


### <a name="array--t"></a>Array: 't []

Das Array, das indiziert wird.



## <a name="output--t"></a>Ausgabe: 't



## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der einzelnen Elemente von `array` .

## <a name="example"></a>Beispiel

Holen Sie sich die dritte Zahl in vier berühmten ganzzahligen Sequenzen. (Beachten Sie, dass der Index 0 dem _ersten_ Wert der Sequenz entspricht.)

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famous2 = Mapped(ElementAt<Int>(2, _), [lucas, prime, fibonacci, catalan]);
// same as: famous2 = [3, 5, 1, 2]
```

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Arrays. lookupfunction](xref:Microsoft.Quantum.Arrays.LookupFunction)
- [Microsoft. Quantum. Arrays. elementsat](xref:Microsoft.Quantum.Arrays.ElementsAt)