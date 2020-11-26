---
uid: Microsoft.Quantum.Core.RangeReverse
title: Rangereverse-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213836"
---
# <a name="rangereverse-function"></a>Rangereverse-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paket: [Microsoft. Quantum. qsharp. Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Gibt einen neuen Bereich zurück, bei dem es sich um den umgekehrten Bereich des Eingabe Bereichs handelt.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>Eingabe

### <a name="r--range"></a>r: [Bereich](xref:microsoft.quantum.lang-ref.range)

Eingabebereich.



## <a name="output--range"></a>Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)

Ein neuer Bereich, der das Gegenteil des angegebenen Bereichs ist.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass der umgekehrte Bereich eines Bereichs nicht einfach " `end` .. `-step` .." ist `start` , da das tatsächliche letzte Element eines Bereichs möglicherweise nicht mit identisch `end` ist.