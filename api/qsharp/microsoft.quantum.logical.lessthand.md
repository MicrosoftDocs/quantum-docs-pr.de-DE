---
uid: Microsoft.Quantum.Logical.LessThanD
title: Lessthand-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 7135ed4b3414d143f5020496ae524bf89980a8a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849170"
---
# <a name="lessthand-function"></a>Lessthand-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt nur dann true zurück, wenn eine Zahl kleiner als eine andere Zahl ist.

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--double"></a>a: [Double](xref:microsoft.quantum.lang-ref.double)

Der erste zu vergleichende Wert.


### <a name="b--double"></a>b: [Double](xref:microsoft.quantum.lang-ref.double)

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true` , wenn und nur, wenn `a` streng kleiner als ist `b` .

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
let cond = a < b;
let cond = LessThanD(a, b);
```