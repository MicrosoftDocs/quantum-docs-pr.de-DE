---
uid: Microsoft.Quantum.Core.RangeReverse
title: Rangereverse-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702864"
---
# <a name="rangereverse-function"></a>Rangereverse-Funktion

Namespace: [Microsoft. Quantum. Core](xref:Microsoft.Quantum.Core)

Paketen [](https://nuget.org/packages/)


Gibt einen neuen Bereich zurück, bei dem es sich um den umgekehrten Bereich des Eingabe Bereichs handelt.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>Eingabe

### <a name="r--range"></a>r: [Bereich](xref:microsoft.quantum.lang-ref.range)

Eingabebereich.



## <a name="output--range"></a>Ausgabe: [Bereich](xref:microsoft.quantum.lang-ref.range)

Ein neuer Bereich, der das Gegenteil des angegebenen Bereichs ist.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass der umgekehrte Bereich eines Bereichs nicht einfach " `end` .. `-step` .." ist `start` , da das tatsächliche letzte Element eines Bereichs möglicherweise nicht mit identisch `end` ist.