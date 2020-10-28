---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Leftshibtedi-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: ce68311adf211169c2fb499bb189332370a6d6ac
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705639"
---
# <a name="leftshiftedi-function"></a>Leftshibtedi-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paketen [](https://nuget.org/packages/)


Verschiebt die bitweise Darstellung einer Zahl nach links um eine angegebene Anzahl von Bits.

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Eingabe

### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)

Die Zahl, deren bitweise Darstellung nach links verschoben werden soll (signifikanter).


### <a name="amount--int"></a>Betrag: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits, um die `value` nach links verschoben werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Der Wert von `value` , nach links um `amount` Bits verschoben.

## <a name="remarks"></a>Hinweise

Die folgenden sind gleichwertig:

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```