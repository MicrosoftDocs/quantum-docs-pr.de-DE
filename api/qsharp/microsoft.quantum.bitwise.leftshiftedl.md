---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: Leftshibtedl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 00d4f9151c620e044074930933ea2912b52534ed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219667"
---
# <a name="leftshiftedl-function"></a>Leftshibtedl-Funktion

Namespace: [Microsoft. Quantum. bitse](xref:Microsoft.Quantum.Bitwise)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Verschiebt die bitweise Darstellung einer Zahl nach links um eine angegebene Anzahl von Bits.

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Eingabe

### <a name="value--bigint"></a>Wert: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Die Zahl, deren bitweise Darstellung nach links verschoben werden soll (signifikanter).


### <a name="amount--int"></a>Betrag: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Bits, um die `value` nach links verschoben werden soll.



## <a name="output--bigint"></a>Ausgabe: [bigint](xref:microsoft.quantum.lang-ref.bigint)

Der Wert von `value` , nach links um `amount` Bits verschoben.

## <a name="remarks"></a>Bemerkungen

Die folgenden sind gleichwertig:

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```