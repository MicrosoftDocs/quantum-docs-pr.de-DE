---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: Constantarray-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706138"
---
# <a name="constantarray-function"></a>Constantarray-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paketen [](https://nuget.org/packages/)


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

