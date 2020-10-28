---
uid: Microsoft.Quantum.Logical.EqualD
title: Equald-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 024ddee785a6a907b4a39d0eccc5990b4c5d5d83
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702078"
---
# <a name="equald-function"></a>Equald-Funktion

Namespace: [Microsoft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Paketen [](https://nuget.org/packages/)


Gibt nur dann true zurück, wenn zwei Eingaben gleich sind.

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Eingabe

### <a name="a--double"></a>a: [Double](xref:microsoft.quantum.lang-ref.double)

Der erste zu vergleichende Wert.


### <a name="b--double"></a>b: [Double](xref:microsoft.quantum.lang-ref.double)

Der zweite zu vergleichende Wert.



## <a name="output--bool"></a>Ausgabe: [bool](xref:microsoft.quantum.lang-ref.bool)

`true``a`, wenn gleich ist `b` .

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let cond = a == b;
let cond = EqualD(a, b);
```