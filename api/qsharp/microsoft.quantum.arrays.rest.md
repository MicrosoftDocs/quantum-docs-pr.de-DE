---
uid: Microsoft.Quantum.Arrays.Rest
title: Rest-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Rest
qsharp.summary: Creates an array that is equal to an input array except that the first array element is dropped.
ms.openlocfilehash: b6c579df354185a2defb08cd78bce816d8cc5959
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845476"
---
# <a name="rest-function"></a>Rest-Funktion

Namespace: [Microsoft. Quantum. Arrays](xref:Microsoft.Quantum.Arrays)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt ein Array, das gleich einem Eingabe Array ist, außer dass das erste Array Element gelöscht wird.

```qsharp
function Rest<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Eingabe

### <a name="array--t"></a>Array: 't []

Ein Array, dessen zweites bis letztes Element das Ausgabe Array bilden soll.



## <a name="output--t"></a>Ausgabe: 't []

Ein Array, das die Elemente enthält `array[1..Length(array) - 1]` .

## <a name="type-parameters"></a>Typparameter

### <a name="t"></a>GIF

Der Typ der Arrayelemente.