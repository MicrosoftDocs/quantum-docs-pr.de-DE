---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: Leftshibtedi-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3f551bdba5c8e2a1456838769e4cee0660d0f969
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845302"
---
# <a name="leftshiftedi-function"></a>Leftshibtedi-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
let c = a <<< b;
let c = LeftShiftedI(a, b);
```