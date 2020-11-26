---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: Rightshif tedl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 3d941e1a0bcd96fe54ab01019293d883f11547a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219514"
---
# <a name="rightshiftedl-function"></a>Rightshif tedl-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Verschiebt die bitweise Darstellung einer Zahl um eine angegebene Anzahl von Bits nach rechts.

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Eingabe

### <a name="value--bigint"></a>Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Die Zahl, deren bitweise Darstellung nach rechts verschoben werden soll (weniger signifikant).


### <a name="amount--int"></a>Betrag: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits, um die `value` nach rechts verschoben werden soll.



## <a name="output--bigint"></a>Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Der Wert von `value` , nach rechts nach `amount` Bits verschoben.

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```