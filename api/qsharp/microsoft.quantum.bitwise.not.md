---
uid: Microsoft.Quantum.Bitwise.Not
title: Not-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Not
qsharp.summary: Returns the bitwise NOT of an integer. This performs the same computation as the built-in `~~~` operator.
ms.openlocfilehash: 9c7642770c4f1db4878ccc1aba288fb9254e017e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842117"
---
# <a name="not-function"></a>Not-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt das bitweise NOT einer Ganzzahl zurück.
Dies führt die gleiche Berechnung durch wie der integrierte `~~~` Operator.

```qsharp
function Not (a : Int) : Int
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Beispiel

```qsharp
let a = 248;
let x = Not(a); // x : Int = -249, due to two's complement representation.
```

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter [c# ~-Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/bitwise-complement-operator) .