---
uid: Microsoft.Quantum.Bitwise.Or
title: Or-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Or
qsharp.summary: Returns the bitwise OR of two integers. This performs the same computation as the built-in `|||` operator.
ms.openlocfilehash: 811e7cf64424e8302c5745c4c71d76de50ab8c08
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845278"
---
# <a name="or-function"></a>Or-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt das bitweise OR von zwei Ganzzahlen zurück.
Dies führt die gleiche Berechnung durch wie der integrierte `|||` Operator.

```qsharp
function Or (a : Int, b : Int) : Int
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Beispiel

```qsharp
let a = 248;      //                 11111000₂
let b = 63;       //                 00111111₂
let x = Or(a, b); // x : Int = 255 = 11111111₂.
```

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter [c# | -Operator](https://docs.microsoft.com/dotnet/csharp/language-reference/operators/or-operator) , um weitere Details anzuzeigen.