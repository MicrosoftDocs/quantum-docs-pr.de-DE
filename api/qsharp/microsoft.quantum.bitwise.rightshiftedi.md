---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: Rightshif Tedi-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 5c3106eb73178554184cbfb37333c027805c69f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845256"
---
# <a name="rightshiftedi-function"></a>Rightshif Tedi-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```qsharp
let c = a >>> b;
let c = RightShiftedI(a, b);
```