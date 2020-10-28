---
uid: Microsoft.Quantum.Arrays.Swapped
title: Vertauscht Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: fa5b37b4caf5d8f19ed05075ddd7bc4217036bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705746"
---
# <a name="swapped-function"></a>Vertauscht Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


Wendet einen Austausch zweier Elemente in einem Array an.

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="firstindex--int"></a>firstindex: [int](xref:microsoft.quantum.lang-ref.int)

Der Index des ersten Elements, das ausgetauscht werden soll.


### <a name="secondindex--int"></a>secondindex: [int](xref:microsoft.quantum.lang-ref.int)

Der Index des zweiten Elements, das ausgetauscht werden soll.


### <a name="arr--t"></a>Arr: 't []

Array mit Elementen, die ausgetauscht werden sollen.



## <a name="output--t"></a>Ausgabe: 't []

Das Array, für das der in-Place-Swap angewendet wurde.

## <a name="example"></a>Beispiel

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

