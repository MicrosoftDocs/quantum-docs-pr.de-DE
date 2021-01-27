---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: Lessthanorequali-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 9438fc05b4ccb041b087f9cfeb30ac0c8cfcabd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815606"
---
# <a name="lessthanorequali-function"></a>Lessthanorequali-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt nur dann true zurück, wenn eine Zahl kleiner oder gleich einer anderen Zahl ist.

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Der erste zu vergleichende Wert.


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn kleiner oder gleich ist `b` .

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```