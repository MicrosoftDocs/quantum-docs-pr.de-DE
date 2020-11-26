---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: Withzeroinsertedat-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228864"
---
# <a name="withzeroinsertedat-function"></a>Withzeroinsertedat-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Einfügen eines 0-Bit-Wert in eine ganze Zahl

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a>BESCHREIBUNG

Dieser Vorgang nimmt eine Ganzzahl an, fügt ein Bit 0 (null) ein `position` und gibt den aktualisierten Wert als Ganzzahl zurück.  Wenn beispielsweise 0 an Position 2 in der Zahl 10 ($10 _ {10} = 1010_ $) eingefügt wird, wird {2} die Zahl 18 (18 bis 18 _ {10} = 10010_ {2} $) zurückgegeben.

## <a name="input"></a>Eingabe

### <a name="position--int"></a>Position: [int](xref:microsoft.quantum.lang-ref.int)

Die Position, an der 0 eingefügt wird.


### <a name="value--int"></a>Wert: [int](xref:microsoft.quantum.lang-ref.int)

Der geänderte Wert.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Geänderter Wert