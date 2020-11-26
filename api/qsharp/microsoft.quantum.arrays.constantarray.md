---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Constantarray-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210062"
---
# <a name="constantarray-function"></a>Constantarray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt ein Array mit der angegebenen Länge, wobei alle Elemente gleich dem angegebenen Wert sind.

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="length--int"></a>Länge: [int](xref:microsoft.quantum.lang-ref.int)

Länge des neuen Arrays.


### <a name="value--t"></a>Wert: 't

Der Wert jedes Elements des neuen Arrays.



## <a name="output--t"></a>Ausgabe: 't []

Ein neues Array der Länge `length` , sodass jedes Element ist `value` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

