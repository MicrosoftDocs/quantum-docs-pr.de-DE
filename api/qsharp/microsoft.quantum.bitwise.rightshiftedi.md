---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Rightshif Tedi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b0ca7d3cb84c58429e9b3a29893a6140a717006b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705583"
---
# <a name="rightshiftedi-function"></a>Rightshif Tedi-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paketen [](https://nuget.org/packages/)


Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Eingabe

### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)

Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).


### <a name="amount--int"></a>Betrag: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der Wert von `value` , nach rechts nach `amount` Bits verschoben.

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```